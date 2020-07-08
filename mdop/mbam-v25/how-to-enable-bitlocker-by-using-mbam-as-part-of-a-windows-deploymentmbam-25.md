---
title: Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법
description: Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826228"
---
# Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법


이 항목에서는 Windows 이미징 및 배포 프로세스의 일부로 MBAM을 사용 하 여 최종 사용자의 컴퓨터에서 BitLocker를 사용 하도록 설정 하는 방법에 대해 설명 합니다. 컴퓨터를 다시 시작할 때 검정색 화면이 표시 되는 경우 (단계 종료 이후 설치 후) 드라이브의 잠금을 해제할 수 없음을 나타내는 windows [10, 버전 1511에서 BitLocker를 미리 프로 비전 하는 경우 "windows 및 Configuration Manager 설정" 단계를 참조 하 여 이전 Windows 버전이 시작 되지 않도록](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)합니다.

**필수 조건:**

-   기존 Windows 이미지 배포 프로세스 – Microsoft 배포 툴킷 (MDT), Microsoft System Center Configuration Manager 또는 일부 다른 이미징 도구 또는 프로세스가 필요 합니다.

-   TPM을 BIOS에서 사용 하도록 설정 하 고 OS에 표시 해야 합니다.

-   MBAM 서버 인프라는 현재 위치에 있고 액세스할 수 있어야 합니다.

-   BitLocker에 필요한 시스템 파티션을 만들어야 합니다.

-   컴퓨터는 MBAM에서 BitLocker를 완전히 사용 하도록 설정 하기 전에 이미징 중에 도메인에 가입 되어 있어야 합니다.

**Windows 배포의 일부로 MBAM 2.5 SP1을 사용 하 여 BitLocker를 사용 하도록 설정 하려면**

1. MBAM 2.5 SP1에서는 Windows 배포 중에 PowerShell 스크립트를 사용 하 여 BitLocker를 사용 하는 것이 권장 되는 접근 방법입니다 `Invoke-MbamClientDeployment.ps1` .

   -   이 `Invoke-MbamClientDeployment.ps1` 스크립트는 이미징 프로세스 중에 BitLocker를 enacts. BitLocker 정책에 따라 필요할 때, MBAM 에이전트는 도메인 사용자가 이미징 후 처음으로 로그온 할 때 PIN 또는 암호를 만들도록 메시지를 표시 합니다.

   -   MDT, System Center Configuration Manager 또는 독립 실행형 이미징 프로세스에서 쉽게 사용할 수 있습니다.

   -   PowerShell 2.0 이상과 호환 가능

   -   TPM 키 보호기를 사용 하 여 OS 볼륨 암호화

   -   BitLocker 사전 프로비저닝 완전 지원

   -   선택적으로 FDDs 암호화

   -   Windows 7에 대 한 에스크로 TPM 소유자 인증, MBAM은 에스크로를 발생 시킬 TPM을 소유 하 고 있어야 합니다.
   Windows 8.1의 경우 Windows 10 RTM 및 Windows 10 버전 1511, TPM 소유자의 에스크로 인증이 지원 됩니다.
   Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다. Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다. 자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.

   -   에스크로 복구 키 및 복구 키 패키지

   -   즉시 암호화 상태 보고

   -   새 WMI 공급자

   -   자세한 로깅

   -   강력한 오류 처리

   `Invoke-MbamClientDeployment.ps1` [Microsoft.com 다운로드 센터](https://www.microsoft.com/download/details.aspx?id=54439)에서 스크립트를 다운로드할 수 있습니다. 이는 배포 시스템에서 MBAM 서버를 사용 하 여 BitLocker 드라이브 암호화 및 레코드 복구 키를 구성 하기 위해 호출할 주 스크립트입니다.

   **MBAM에 대 한 WMI 배포 방법:** 이 PowerShell 스크립트를 사용 하 여 BitLocker 사용을 지원 하기 위해 다음 WMI 메서드가 MBAM 2.5 SP1에 추가 되었습니다 `Invoke-MbamClientDeployment.ps1` .

   <a href="" id="mbam-machine-wmi-class"></a>**Mbam \ _MACHINE WMI 클래스** 
    **PrepareTpmAndEscrowOwnerAuth:** TPM 소유자 인증을 읽고 MBAM 복구 서비스를 사용 하 여이를 MBAM 데이터베이스로 보냅니다. TPM이 소유 되지 않고 자동 프로비저닝이 켜져 있지 않으면 TPM 소유자 인증을 생성 하 고 소유권을 가져옵니다. 실패 하면 문제 해결을 위해 오류 코드가 반환 됩니다.

   **참고** Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다. Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다. 자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.

| 매개 변수 | 설명 |
| -------- | ----------- |
| RecoveryServiceEndPoint | MBAM 복구 서비스 끝점을 지정 하는 문자열입니다. |

일반적인 오류 메시지 목록은 다음과 같습니다.

| 일반적인 반환 값 | 오류 메시지 |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | 메서드가 성공적으로 수행 되었습니다. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | TPM이 컴퓨터에 없거나 BIOS 구성에서 사용 하지 않도록 설정 되어 있습니다. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | TPM의 상태가 올바르지 않습니다 (사용 가능, 활성화 됨, 소유자 설치가 허용 됨). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM은 자동 프로비저닝이 보류 중 이므로 TPM의 소유권을 가질 수 없습니다. 자동 프로비저닝이 완료 된 후 다시 시도해 주십시오. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM은 TPM 소유자 권한 부여 값을 읽을 수 없습니다. 성공적으로 에스크로 한 후에도 값이 제거 되었을 수 있습니다. Windows 7에서는 TPM을 다른 사용자가 소유한 경우 MBAM에서 값을 읽을 수 없습니다. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | TPM을 올바른 상태로 설정 하려면 컴퓨터를 다시 시작 해야 합니다. 컴퓨터를 수동으로 다시 부팅 해야 할 수 있습니다. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | TPM을 올바른 상태로 설정 하려면 컴퓨터를 종료 하 고 다시 켜야 합니다. 컴퓨터를 수동으로 다시 부팅 해야 할 수 있습니다. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0X800005) | 원격 끝점에 의해 액세스가 거부 되었습니다. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | 원격 끝점이 없거나 찾을 수 없습니다. |
| * * WS_E_ENDPOINT_FAILURE<br />2151481357 (0X80이상 000F) | 원격 끝점이 요청을 처리할 수 없습니다. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0X80이상 0010) | 원격 끝점에 연결할 수 없습니다. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0X80이상 0013) | 원격 끝점에서 오류가 포함 된 메시지를 받았습니다. 올바른 서비스 끝점에 연결 하 고 있는지 확인 합니다. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0X80이상 0020) | 끝점 주소 URL이 잘못 되었습니다. URL은 "http" 또는 "https"로 시작 해야 합니다. |

   **보고서 상태:** 볼륨의 준수 상태를 읽고 MBAM 상태 보고 서비스를 사용 하 여이를 MBAM 준수 상태 데이터베이스로 보냅니다. 상태에는 암호화 수준, 보호기 유형, 보호기 상태 및 암호화 상태가 포함 됩니다. 실패 하면 문제 해결을 위해 오류 코드가 반환 됩니다.

   | 매개 변수 | 설명 |
   | --------- | ----------- |
   | ReportingServiceEndPoint | MBAM 상태 보고 서비스 끝점을 지정 하는 문자열입니다. |

   일반적인 오류 메시지 목록은 다음과 같습니다.

   | 일반적인 반환 값 | 오류 메시지 |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | 메서드 성공 |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0X800005) | 원격 끝점에 의해 액세스가 거부 되었습니다.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | 원격 끝점이 없거나 찾을 수 없습니다. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0X80이상 000F) | 원격 끝점이 요청을 처리할 수 없습니다. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0X80이상 0010) | 원격 끝점에 연결할 수 없습니다. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0X80이상 0013) | 원격 끝점에서 오류가 포함 된 메시지를 받았습니다. 올바른 서비스 끝점에 연결 하 고 있는지 확인 합니다. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0X80.0020) | 끝점 주소 URL이 잘못 되었습니다. URL은 "http" 또는 "https"로 시작 해야 합니다. |

   <a href="" id="mbam-volume-wmi-class"></a>**Mbam \ _VOLUME WMI 클래스** **EscrowRecoveryKey:** 볼륨의 복구 숫자 암호와 키 패키지를 읽고 mbam 복구 서비스를 사용 하 여 mbam 복구 데이터베이스로 보냅니다. 실패 하면 문제 해결을 위해 오류 코드가 반환 됩니다.

   | 매개 변수 | 설명 |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | MBAM 복구 서비스 끝점을 지정 하는 문자열입니다. |

   일반적인 오류 메시지 목록은 다음과 같습니다.

   | 일반적인 반환 값 | 오류 메시지 |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | 메서드 성공 |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | 볼륨이 잠겼습니다. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | 볼륨에 대 한 숫자 암호 보호기를 찾을 수 없습니다. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0X800005) | 원격 끝점에 의해 액세스가 거부 되었습니다. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | 원격 끝점이 없거나 찾을 수 없습니다. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0X80이상 000F) | 원격 끝점이 요청을 처리할 수 없습니다. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0X80이상 0010) | 원격 끝점에 연결할 수 없습니다. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0X80이상 0013) | 원격 끝점에서 오류가 포함 된 메시지를 받았습니다. 올바른 서비스 끝점에 연결 하 고 있는지 확인 합니다. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0X80.0020) | 끝점 주소 URL이 잘못 되었습니다. URL은 "http" 또는 "https"로 시작 해야 합니다. |
     

2. **MDT (Microsoft Deployment Toolkit) 및 PowerShell을 사용 하 여 MBAM 배포**

   1.  MDT에서 새 배포 공유를 만들거나 기존 배포 공유를 엽니다.

       **참고**  
       `Invoke-MbamClientDeployment.ps1`PowerShell 스크립트는 모든 이미징 프로세스 또는 도구와 함께 사용할 수 있습니다. 이 섹션에서는 MDT를 사용 하 여 통합 하는 방법을 보여 주지만,이 단계는 다른 프로세스나 도구와 통합 하는 것과 유사 합니다.

       **주의**  
       WinPE (BitLocker 사전 프로비저닝)를 사용 하는 경우 TPM 소유자 권한 부여 값을 유지 관리 하려면 `SaveWinPETpmOwnerAuth.wsf` 설치가 전체 운영 체제로 다시 부팅 되기 바로 전에 WinPE에서 스크립트를 추가 해야 합니다. **이 스크립트를 사용 하지 않으면 다시 부팅할 때 TPM 소유자 권한 부여 값이 손실 됩니다.**

   2.  `Invoke-MbamClientDeployment.ps1` ** &lt; Deploymentshare. &gt; \ \ 스크립트**에 복사 합니다. 사전 배포를 사용 하는 경우 `SaveWinPETpmOwnerAuth.wsf` 파일을 ** &lt; deploymentshare &gt; \ 스크립트**에 복사 합니다.

   3.  배포 공유의 응용 프로그램 노드에 MBAM 2.5 SP1 클라이언트 응용 프로그램을 추가 합니다.

       1.  **응용 프로그램** 노드에서 **새 응용 프로그램**을 클릭 합니다.

       2.  **원본 파일을 사용 하 여 응용 프로그램을**선택 합니다. **다음**을 클릭합니다.

       3.  **응용 프로그램 이름**에 "mbam 2.5 SP1 클라이언트"를 입력 합니다. **다음**을 클릭합니다.

       4.  을 (를) 포함 하는 디렉터리로 이동 `MBAMClientSetup-<Version>.msi` 합니다. **다음**을 클릭합니다.

       5.  "MBAM 2.5 SP1 클라이언트"를 만들 디렉터리로 입력 합니다. **다음**을 클릭합니다.

       6.  `msiexec /i MBAMClientSetup-<Version>.msi /quiet`명령줄에서 Enter 키를 누르십시오. **다음**을 클릭합니다.

       7.  나머지 기본값을 적용 하 여 새 응용 프로그램 마법사를 완료 합니다.

   4.  MDT에서 배포 공유의 이름을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 클릭 합니다. **규칙** 탭을 클릭 합니다. 다음 줄을 추가 합니다.

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       확인을 클릭 하 여 창을 닫습니다.

   5.  작업 순서 노드에서 Windows 배포에 사용 되는 기존 작업 순서를 편집 합니다. 원하는 경우 **작업** 순서 노드를 마우스 오른쪽 단추로 클릭 하 고 **새 작업 순서**를 선택한 다음 마법사를 완료 하 여 새 작업 순서를 만들 수 있습니다.

       선택한 작업 순서의 **작업 순서** 탭에서 다음 단계를 수행 합니다.

       1.  WinPE에서 BitLocker를 사용 하 여 사용 하는 공간만 암호화 하려면 **사전 설치** 폴더에서 선택적 작업 **(bitlocker 사용)** 을 사용 하도록 설정 합니다.

       2.  사전 프로비저닝을 사용할 때 TPM 소유자 인증을 유지 하 고, 나중에 MBAM에서 에스크로를 허용 하려면 다음을 수행 합니다.

           1.  **설치 운영 체제** 찾기 단계

           2.  새 **실행** 명령줄을 추가 하는 단계

           3.  단계의 이름 **TPM 소유자 인증 유지**

           4.  명령줄을 `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **참고:** windows 10, 버전 1607 이상에서는 windows만 TPM 소유권을 가질 수 있습니다. Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다. 자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.

       3.  **상태 복원** 폴더에서 **BitLocker 사용 가능** 작업을 삭제 합니다.

       4.  **사용자 지정 작업**아래에 있는 **상태 복원** 폴더에서 새 **설치 응용 프로그램** 작업을 만들고 이름에 **mbam 에이전트를 설치**합니다. **단일 응용 프로그램 설치** 라디오 단추를 클릭 하 고 이전에 만든 mbam 2.5 SP1 클라이언트 응용 프로그램을 찾습니다.

       5.  **사용자 지정 작업**아래에 있는 **상태 복원** 폴더에서 다음 설정을 사용 하 여 새 **실행 PowerShell 스크립트** 작업 (mbam 2.5 SP1 클라이언트 응용 프로그램 단계 이후)을 만듭니다 (환경에 맞게 매개 변수 업데이트).

           -   이름: MBAM에 대 한 BitLocker 구성

           -   PowerShell 스크립트: `Invoke-MbamClientDeployment.ps1`

           -   변수

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p>-RecoveryServiceEndpoint</p></td>
               <td align="left"><p>필수</p></td>
               <td align="left"><p>MBAM 복구 서비스 끝점</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>선택 사항</p></td>
               <td align="left"><p>MBAM 상태 보고 서비스 끝점</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-. A 메서드</p></td>
               <td align="left"><p>선택 사항</p></td>
               <td align="left"><p>암호화 방법 (기본값: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>데이터 볼륨 및 에스크로 데이터 볼륨 복구 키를 암호화 하도록 지정 (s)</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-Waitforcomplete To완료</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>암호화가 완료 될 때까지 대기 하도록 지정</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>배포 스크립트가 일시 중단 된 암호화를 다시 시작 하지 않도록 지정 합니다.</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>TPM 소유자 인증 에스크로 오류를 무시 하도록 지정 합니다. 이는 MBAM이 TPM 소유자 인증을 읽을 수 없는 시나리오 (예: TPM 자동 프로비저닝이 사용 되는 경우)에 사용 해야 합니다.</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>볼륨 복구 키 에스크로 오류를 무시 하도록 지정</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>상태 보고 실패를 건너뛰도록 지정</p></td>
               </tr>
               </tbody>
               </table>

                 

**Windows 배포의 일부로 MBAM 2.5 또는 이전 버전을 사용 하 여 BitLocker를 사용 하도록 설정 하려면**

1.  MBAM 클라이언트를 설치 합니다. 지침은 [명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법을](how-to-deploy-the-mbam-client-by-using-a-command-line.md)참조 하세요.

2.  컴퓨터를 도메인에 가입 (권장)

    -   컴퓨터가 도메인에 가입 되어 있지 않으면 복구 암호가 MBAM 키 복구 서비스에 저장 되지 않습니다. 복구 키를 저장할 수 없는 경우 기본적으로 MBAM은 암호화를 허용 하지 않습니다.

    -   복구 키가 MBAM 서버에 저장 되기 전에 컴퓨터가 복구 모드에서 시작 되는 경우 복구 방법을 사용할 수 없으며 컴퓨터를 reimaged 야 합니다.

3.  관리자 권한으로 명령 프롬프트를 열고 MBAM 서비스를 중지 합니다.

4.  다음 명령을 입력 하 여 **수동** 또는 **주문형** 으로 서비스를 설정 합니다.

    **net stop mbamagent**

    **sc config mbamagent 시작 = 요청**

5.  MBAM 클라이언트가 그룹 정책 설정을 무시 하 고 대신 Windows가 해당 클라이언트 컴퓨터에 배포 되는 시간을 시작 하도록 암호화를 설정 하도록 레지스트리 값을 설정 합니다.

    **주의**  사항 이 단계에서는 Windows 레지스트리를 수정 하는 방법에 대해 설명 합니다. 레지스트리 편집기를 잘못 사용 하면 심각한 문제가 발생할 수 있으며,이 경우 Windows를 다시 설치 해야 할 수 있습니다. 레지스트리 편집기의 잘못 된 사용으로 인해 발생 하는 문제는 확인할 수 없습니다. 레지스트리 편집기 사용에 따른 모든 책임은 사용자에 게 있습니다.

    1.  **운영 체제 전용 암호화**용 TPM을 설정 하 고, Regedit.exe을 실행 한 다음 C:\\program files Files\\Microsoft\\MDOP Mbam\\mbamdeploymentkeytemplate 파일에서 레지스트리 키 템플릿을 가져옵니다.

    2.  Regedit.exe에서 HKLM\\SOFTWARE\\Microsoft\\MBAM으로 이동 하 여 다음 표에 나열 된 설정을 구성 합니다.

        **참고**  여기에 MBAM과 관련 된 그룹 정책 설정 또는 레지스트리 값을 설정할 수 있습니다. 이러한 설정은 이전에 설정 값을 재정의 합니다.

        레지스트리 항목 구성 설정

        DeploymentTime

        0 = 해제

        1 = 배포 시간 정책 설정 사용 (기본값) – Windows가 클라이언트 컴퓨터에 배포 될 때 암호화를 사용 하도록 설정 하려면이 설정을 사용 합니다.

        UseKeyRecoveryService

        0 = key 에스크로를 사용 하지 않음 (이 경우 다음 두 레지스트리 항목은 필요 없음)

        1 = 키 복구 시스템에서 키 에스크로 사용 (기본값)

        이 설정은 MBAM이 복구 키를 저장할 수 있도록 하는 권장 설정입니다. 컴퓨터는 MBAM 키 복구 서비스와 통신할 수 있어야 합니다. 계속 하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인 합니다.

        KeyRecoveryOptions

        0 = 복구 키만 업로드

        1 = 복구 키 및 키 복구 패키지를 업로드 합니다 (기본값).

        KeyRecoveryServiceEndPoint

        이 값을 키 복구 서비스를 실행 하는 서버의 URL (예: http:// &lt; computer name/MBAMRecoveryAndHardwareService/CoreService.svc.)으로 설정 합니다. &gt;


6.  MBAM 클라이언트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작 합니다. 이 작업을 다시 시작할 준비가 되 면 관리자 권한으로 명령 프롬프트에서 다음 명령을 실행 합니다.

    **net start mbamagent**

7.  컴퓨터가 다시 시작 되 고 BIOS에 메시지가 표시 되 면 TPM 변경 내용을 적용 합니다.

8.  Windows 클라이언트 운영 체제 이미징 프로세스 중에 암호화를 시작할 준비가 되 면 관리자 권한으로 명령 프롬프트를 열고 다음 명령을 입력 하 여 **자동** 시작을 설정 하 고 Mbam 클라이언트 에이전트를 다시 시작 합니다.

    **sc config mbamagent 시작 = 자동**

    **net start mbamagent**

9.  무시 레지스트리 값을 삭제 하려면 Regedit.exe를 실행 하 고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목으로 이동 합니다. **Mbam** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.

## 관련 항목

[MBAM 2.5 클라이언트 배포](deploying-the-mbam-25-client.md)

[MBAM 2.5 클라이언트 배포 계획](planning-for-mbam-25-client-deployment.md)

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
