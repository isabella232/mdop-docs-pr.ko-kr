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
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626185"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a>Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법

> [!IMPORTANT]
> 이러한 지침은 Configuration Manager BitLocker 관리와는 다릅니다. `Invoke-MbamClientDeployment.ps1`PowerShell 스크립트는 Configuration Manager의 BitLocker 관리에서 사용할 수 없습니다. 여기에는 Configuration Manager 작업 순서 중에 BitLocker 복구 키의 에스크로킹이 포함됩니다. 또한 Configuration Manager Current Branch 2103부터 Configuration Manager BitLocker Management는 더 이상 MBAM 키 복구 서비스 사이트를 사용하여 에스클로 키를 사용할 수 없습니다. Configuration Manager 현재 분기 2103 이상에서 PowerShell 스크립트를 사용하려고 시도하면 Configuration Manager 사이트에 심각한 문제가 `Invoke-MbamClientDeployment.ps1` 발생할 수 있습니다. 알려진 문제로는 정책 폭주를 일으킬 수 있는 모든 장치를 대상으로 하는 많은 양의 정책 생성이 포함됩니다. 이로 인해 Configuration Manager의 성능 저하는 주로 관리 지점에서 SQL 저하될 수 있습니다.

이 항목에서는 MBAM을 이미징 및 배포 프로세스의 일부로 사용하여 최종 사용자 컴퓨터에서 BitLocker를 사용하도록 Windows 방법을 설명합니다. 다시 시작 시(설치 단계가 종료된 후) 드라이브의 잠금을 해제할 수 없다는 검은색 화면이 표시될 경우 Windows 10 버전 [1511과](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)함께 사전 프로비전 BitLocker를 사용하는 경우 이전 Windows 버전이 "설치 Windows 및 Configuration Manager" 단계 후에 시작되지 않습니다를 참조합니다.

**필수 조건:**

-   MDT(Microsoft Deployment Toolkit), Microsoft System Center Configuration Manager 또는 기타 이미징 도구 또는 프로세스인 기존 Windows 이미지 배포 프로세스가 있어야 합니다.

-   BIOS에서 TPM을 사용하도록 설정하고 OS에 표시되어야 합니다.

-   MBAM 서버 인프라가 있으며 액세스 가능해야 합니다.

-   BitLocker에 필요한 시스템 파티션을 만들어야 합니다.

-   MBAM에서 BitLocker를 완전히 사용하려면 이미징 중에 컴퓨터 도메인에 가입되어 있어야 합니다.

**MBAM 2.5 SP1을 배포의 일부로 사용하여 BitLocker를 사용하도록 Windows**

1. MBAM 2.5 SP1에서는 배포 중에 BitLocker를 사용하도록 설정하는 Windows `Invoke-MbamClientDeployment.ps1` PowerShell 스크립트를 사용하는 것이 좋습니다.

   -   이 `Invoke-MbamClientDeployment.ps1` 스크립트는 이미징 프로세스 중에 BitLocker를 실행합니다. BitLocker 정책에 필요한 경우 MBAM 에이전트는 도메인 사용자가 이미징 후 처음 로그온할 때 PIN 또는 암호를 만들지 묻는 메시지를 도메인 사용자에게 즉시 제공합니다.

   -   MDT, System Center Configuration Manager 또는 독립 실행형 이미징 프로세스에서 사용하기 쉬운 경우

   -   PowerShell 2.0 이상과 호환

   -   TPM 키 보호기로 OS 볼륨 암호화

   -   BitLocker 사전 프로비전을 완전히 지원

   -   선택적으로 FDD 암호화

   -   Escrow TPM OwnerAuth Windows 7의 경우 에스로가 발생하려면 MBAM이 TPM을 소유해야 합니다.
   이 Windows 8.1 RTM Windows 10 Windows 10 버전 1511의 경우 TPM OwnerAuth의 에스로가 지원됩니다.
   Windows 10 버전 1607 이상의 경우 TPM의 Windows 수만 있습니다. addiiton에서는 Windows 프로비전할 때 TPM 소유자 암호를 유지하지 않습니다. 자세한 [내용은 TPM 소유자 암호를](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 참조하세요.

   -   에스로 복구 키 및 복구 키 패키지

   -   즉시 암호화 상태 보고

   -   새 WMI 공급자

   -   자세한 로깅

   -   강력한 오류 처리

   다운로드 센터에서 스크립트를 `Invoke-MbamClientDeployment.ps1` [다운로드할 Microsoft.com 있습니다.](https://www.microsoft.com/download/details.aspx?id=54439) 이 스크립트는 배포 시스템에서 BitLocker 드라이브 암호화를 구성하고 MBAM Server를 사용하여 복구 키를 기록하기 위해 호출하는 기본 스크립트입니다.

   **MBAM에** 대한 WMI 배포 방법: PowerShell 스크립트를 사용하여 BitLocker 사용을 지원하기 위해 다음 WMI 메서드가 MBAM 2.5 SP1에 `Invoke-MbamClientDeployment.ps1` 추가되었습니다.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM\_Machine WMI 클래스** 
    **PrepareTpmAndEscrowOwnerAuth:** TPM OwnerAuth를 읽고 MBAM 복구 서비스를 사용하여 MBAM 복구 데이터베이스로 전송합니다. TPM이 소유되지 않은 경우 자동 프로비저닝이 사용되지 않는 경우 TPM OwnerAuth가 생성됩니다. 오류가 발생하면 문제 해결을 위해 오류 코드가 반환됩니다.

   **참고** Windows 10 버전 1607 이상의 경우 TPM의 Windows 수만 있습니다. addiiton에서는 Windows 프로비전할 때 TPM 소유자 암호를 유지하지 않습니다. 자세한 [내용은 TPM 소유자 암호를](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 참조하세요.

| 매개 변수 | 설명 |
| -------- | ----------- |
| RecoveryServiceEndPoint | MBAM 복구 서비스 끝점을 지정하는 문자열입니다. |

다음은 일반적인 오류 메시지 목록입니다.

| 일반 반환 값 | 오류 메시지 |
| -------------------- | ------------- |
|  **S_OK**<br />0(0x0) | 메서드가 성공했습니다. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304(0x80040200) | TPM이 컴퓨터에 존재하지 않는 경우 또는 BIOS 구성에서 사용하지 않도록 설정되어 있습니다. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305(0x80040201) | TPM이 올바른 상태(사용, 활성화 및 소유자 설치 허용)에 없습니다. |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306(0x80040202) | 자동 프로비전이 보류 중이기 때문에 MBAM은 TPM의 소유권을 사용할 수 없습니다. 자동 프로비전이 완료된 후 다시 시도하십시오. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307(0x80040203) | MBAM은 TPM 소유자 권한 부여 값을 읽을 수 없습니다. 이 값은 에스크로에 성공한 후 제거된 것일 수 있습니다. 7 Windows TPM이 다른 사용자가 소유한 경우 MBAM은 값을 읽을 수 없습니다. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308(0x80040204) | TPM을 올바른 상태로 설정하려면 컴퓨터를 다시 시작해야 합니다. 컴퓨터를 수동으로 다시 시작해야 할 수 있습니다. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309(0x80040205) | TPM을 올바른 상태로 설정하려면 컴퓨터를 종료했다가 다시 켜야 합니다. 컴퓨터를 수동으로 다시 시작해야 할 수 있습니다. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349(0x803D0005) | 원격 끝점에서 액세스가 거부됩니다. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357(0x803D000D) | 원격 끝점이 존재하지 않을 수도 있습니다. |
| **WS_E_ENDPOINT_FAILURE<br />2151481357(0x803D000F) | 원격 끝점에서 요청을 처리하지 못했습니다. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360(0x803D0010) | 원격 끝점에 도달할 수 없습니다. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363(0x803D0013) | 원격 끝점에서 오류가 포함된 메시지를 수신했습니다. 올바른 서비스 끝점에 연결하고 있는지 확인합니다. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376(0x803D0020) | 끝점 주소 URL이 유효하지 않습니다. URL은 "http" 또는 "https"로 시작해야 합니다. |

   **ReportStatus:** 볼륨의 준수 상태를 읽고 MBAM 상태 보고 서비스를 사용하여 MBAM 준수 상태 데이터베이스로 전송합니다. 상태에는 암호화 강도, 보호기 유형, 보호기 상태 및 암호화 상태가 포함됩니다. 오류가 발생하면 문제 해결을 위해 오류 코드가 반환됩니다.

   | 매개 변수 | 설명 |
   | --------- | ----------- |
   | ReportingServiceEndPoint | MBAM 상태 보고 서비스 끝점을 지정하는 문자열입니다. |

   다음은 일반적인 오류 메시지 목록입니다.

   | 일반 반환 값 | 오류 메시지 |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0(0x0) | 메서드가 성공했습니다. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349(0x803D0005) | 원격 끝점에서 액세스가 거부됩니다.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357(0x803D000D) | 원격 끝점이 존재하지 않을 수도 있습니다. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357(0x803D000F) | 원격 끝점에서 요청을 처리하지 못했습니다. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360(0x803D0010) | 원격 끝점에 도달할 수 없습니다. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363(0x803D0013) | 원격 끝점에서 오류가 포함된 메시지를 수신했습니다. 올바른 서비스 끝점에 연결하고 있는지 확인합니다. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376(0x803D0020) | 끝점 주소 URL이 유효하지 않습니다. URL은 "http" 또는 "https"로 시작해야 합니다. |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM\_Volume WMI** 클래스 **EscrowRecoveryKey:** 볼륨의 복구 숫자 암호 및 키 패키지를 읽고 MBAM 복구 서비스를 사용하여 MBAM 복구 데이터베이스로 전송합니다. 오류가 발생하면 문제 해결을 위해 오류 코드가 반환됩니다.

   | 매개 변수 | 설명 |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | MBAM 복구 서비스 끝점을 지정하는 문자열입니다. |

   다음은 일반적인 오류 메시지 목록입니다.

   | 일반 반환 값 | 오류 메시지 |
   | -------------------- | ------------- |
   | **S_OK**<br />0(0x0) | 메서드가 성공했습니다. |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912(0x80310000) | 볼륨이 잠겨 있습니다. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963(0x80310033) | 볼륨에 대한 숫자 암호 보호를 찾을 수 없습니다. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349(0x803D0005) | 원격 끝점에서 액세스가 거부됩니다. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357(0x803D000D) | 원격 끝점이 존재하지 않을 수도 있습니다. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357(0x803D000F) | 원격 끝점에서 요청을 처리하지 못했습니다. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360(0x803D0010) | 원격 끝점에 도달할 수 없습니다. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363(0x803D0013) | 원격 끝점에서 오류가 포함된 메시지를 수신했습니다. 올바른 서비스 끝점에 연결하고 있는지 확인합니다. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376(0x803D0020) | 끝점 주소 URL이 유효하지 않습니다. URL은 "http" 또는 "https"로 시작해야 합니다. |
     

2. **MDT(Microsoft Deployment Toolkit) 및 PowerShell을 사용하여 MBAM 배포**

   1.  MDT에서 새 배포 공유를 만들거나 기존 배포 공유를 니다.

       **참고**  
       PowerShell 스크립트는 모든 이미징 프로세스 또는 `Invoke-MbamClientDeployment.ps1` 도구에서 사용할 수 있습니다. 이 섹션에서는 MDT를 사용하여 통합하는 방법을 보여 주지만 단계는 다른 프로세스 또는 도구와 통합하는 방법과 비슷합니다.

       **주의**  
       WinPE(BitLocker 사전 프로비전)를 사용하는 경우 TPM 소유자 권한 부여 값을 유지하려면 설치가 전체 운영 체제로 다시 시작되기 직전에 WinPE에서 스크립트를 `SaveWinPETpmOwnerAuth.wsf` 추가해야 합니다. **이 스크립트를 사용하지 않는 경우 다시 시작 시 TPM 소유자 권한 부여 값이 손실됩니다.**

   2.  `Invoke-MbamClientDeployment.ps1` ** &lt; DeploymentShare &gt; \\Scripts에 복사합니다.** 사전 프로비전을 사용하는 경우 `SaveWinPETpmOwnerAuth.wsf` 파일을 ** &lt; DeploymentShare &gt; \\Scripts 에 복사합니다.**

   3.  배포 공유의 응용 프로그램 노드에 MBAM 2.5 SP1 클라이언트 응용 프로그램을 추가합니다.

       1.  응용 프로그램 **노드에서** 새 응용 **프로그램을 클릭합니다.**

       2.  원본 **파일이 있는 응용 프로그램을 선택합니다.** **다음**을 클릭합니다.

       3.  응용 **프로그램 이름에**"MBAM 2.5 SP1 Client"를 입력합니다. **다음**을 클릭합니다.

       4.  를 포함하는 디렉터리로 `MBAMClientSetup-<Version>.msi` 검색합니다. **다음**을 클릭합니다.

       5.  만들 디렉터리로 "MBAM 2.5 SP1 Client"를 입력합니다. **다음**을 클릭합니다.

       6.  `msiexec /i MBAMClientSetup-<Version>.msi /quiet`명령줄에 입력합니다. **다음**을 클릭합니다.

       7.  나머지 기본값을 적용하여 새 응용 프로그램 마법사를 완료합니다.

   4.  MDT에서 배포 공유의 이름을 마우스 오른쪽 단추로 클릭하고 속성을 **클릭합니다.** 규칙 **탭을** 클릭합니다. 다음 줄을 추가합니다.

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       확인을 클릭하여 창을 닫습니다.

   5.  Task Sequences 노드에서 Deployment에 사용되는 기존 작업 Windows 편집합니다. 원하는 경우 Task **Sequences** 노드를 마우스 오른쪽 단추로 클릭하고 새 **** 작업 순서를 선택한 다음 마법사를 완료하여 새 작업 순서를 만들 수 있습니다.

       선택한 **작업 순서의** 작업 순서 탭에서 다음 단계를 수행합니다.

       1.  **WinPE에서** **BitLocker를** 사용하도록 설정하려면 사전 설치 폴더에서 사용된 공간만 암호화하는 선택적 작업인 BitLocker(오프라인)를 사용하도록 설정합니다.

       2.  사전 프로비저닝을 사용할 때 TPM OwnerAuth를 유지하여 MBAM이 나중에 에스로를 에버로 할 수 있도록 허용하기 위해 다음을 합니다.

           1.  운영 체제 **설치 단계** 찾기

           2.  다음에 새 **실행 명령줄** 단계 추가

           3.  **TPM OwnerAuth 유지 단계의 이름을 지정합니다.**

           4.  명령줄을 참고로 `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **설정:** Windows 10 버전 1607 이상의 경우 TPM의 Windows 수만 있습니다. addiiton에서는 Windows 프로비전할 때 TPM 소유자 암호를 유지하지 않습니다. 자세한 [내용은 TPM 소유자 암호를](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 참조하세요.

       3.  State **Restore 폴더에서** **BitLocker** 사용 작업을 삭제합니다.

       4.  사용자 **지정 작업 아래 상태 복원** 폴더에서 새 응용 프로그램 설치 작업을 만들고 이름을 **** **** **MBAM 에이전트 설치로 지정합니다.** 단일 **응용 프로그램 설치** 라디오 단추를 클릭하고 앞에서 만든 MBAM 2.5 SP1 클라이언트 응용 프로그램으로 연결합니다.

       5.  사용자 지정 작업의 **** **상태 복원** 폴더에서 다음 설정(환경에 따라 매개 변수 업데이트)을 사용하여 새 **PowerShell** 스크립트 실행 작업(MBAM 2.5 SP1 클라이언트 응용 프로그램 단계 후)을 생성합니다.

           -   이름: MBAM에 대해 BitLocker 구성

           -   PowerShell 스크립트: `Invoke-MbamClientDeployment.ps1`

           -   매개 변수:

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
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>선택 사항</p></td>
               <td align="left"><p>암호화 방법(기본값: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>데이터 볼륨 및 에스로 데이터 볼륨 복구 키를 암호화하기 위해 지정</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>암호화가 완료될 때까지 기다릴 지정</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>배포 스크립트가 일시 중단된 암호화를 다시 시작하지 못하게 지정</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>TPM 소유자-에스크로 실패를 무시할지 지정합니다. MBAM이 TPM 소유자-auth를 읽을 수 없는 시나리오(예: TPM 자동 프로비저닝을 사용하도록 설정한 경우)에서 사용해야 합니다.</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>볼륨 복구 키 에스로 오류 무시를 지정합니다.</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>스위치</p></td>
               <td align="left"><p>상황 보고 실패를 무시하기 위해 지정</p></td>
               </tr>
               </tbody>
               </table>

                 

**MBAM 2.5 또는 이전 버전 배포의 일부로 BitLocker를 사용하도록 Windows**

1.  MBAM 클라이언트를 설치합니다. 자세한 내용은 [How to Deploy the MBAM Client by Using a Command Line을 참조하십시오.](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

2.  컴퓨터를 도메인에 가입합니다(권장).

    -   컴퓨터가 도메인에 가입되어 있지 않은 경우 복구 암호는 MBAM 키 복구 서비스에 저장되지 않습니다. 기본적으로 MBAM은 복구 키를 저장할 수 없는 경우 암호화가 발생하도록 허용하지 않습니다.

    -   복구 키가 MBAM Server에 저장되기 전에 컴퓨터가 복구 모드로 시작되는 경우 복구 방법을 사용할 수 없는 것이 아니며 컴퓨터를 다시 설치해야 합니다.

3.  관리자 권한으로 명령 프롬프트를 열고 MBAM 서비스를 중지합니다.

4.  다음 명령을 입력하여 **서비스를 수동** 또는 On **demand로** 설정하십시오.

    **net stop mbamagent**

    **sc config mbamagent start= demand**

5.  MBAM 클라이언트가 그룹 정책 설정을 무시하고 대신 암호화를 설정하여 해당 클라이언트 컴퓨터에 배포되는 Windows 수 있도록 레지스트리 값을 설정하십시오.

    **주의**  
    이 단계에서는 레지스트리를 수정하는 Windows 설명합니다. 레지스트리 편집기를 잘못 사용하면 레지스트리 편집기를 다시 설치해야 할 수 있는 심각한 문제가 Windows. 레지스트리 편집기가 잘못 사용되어 발생하는 문제를 해결할 수 있는 것은 보장할 수 없습니다. 레지스트리 편집기는 모든 위험에 노출될 수 있습니다.

    1.  운영 체제 전용 **** 암호화에 대한 TPM을 설정하고 Regedit.exe 실행한 다음 C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg에서 레지스트리 키 템플릿을 가져올 수 있습니다.

    2.  이 Regedit.exe HKLM\\SOFTWARE\\Microsoft\\MBAM으로 이동하여 다음 표에 나와 있는 설정을 구성합니다.

        **참고**  
        여기에서 MBAM과 관련된 그룹 정책 설정 또는 레지스트리 값을 설정할 수 있습니다. 이러한 설정은 이전에 설정한 값을 다시 정합니다.

        레지스트리 항목 구성 설정

        DeploymentTime

        0 = 꺼집니다.

        1 = 배포 시간 정책 설정 사용(기본값) - 이 설정을 사용하여 클라이언트 컴퓨터에 배포할 Windows 암호화를 사용하도록 설정할 수 있습니다.

        UseKeyRecoveryService

        0 = 키 에스로를 사용하지 않습니다(이 경우 다음 두 레지스트리 항목이 필요하지 않습니다).

        1 = 키 복구 시스템에서 키 에스로 사용(기본값)

        이 설정은 MBAM이 복구 키를 저장할 수 있는 권장 설정입니다. 컴퓨터가 MBAM 키 복구 서비스와 통신할 수 있어야 합니다. 계속하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인합니다.

        KeyRecoveryOptions

        0 = 복구 키만 업로드

        1 = 복구 키 및 키 복구 패키지 업로드(기본값)

        KeyRecoveryServiceEndPoint

        키 복구 서비스를 실행하는 서버의 URL(예: http:// 컴퓨터 이름 &lt; &gt; /MBAMRecoveryAndHardwareService/CoreService.svc)으로 이 값을 설정하십시오.


6.  MBAM 클라이언트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작합니다. 이 다시 시작할 준비가 되면 명령 프롬프트에서 관리자 권한으로 다음 명령을 실행합니다.

    **net start mbamagent**

7.  컴퓨터가 다시 시작될 때 BIOS에 메시지가 표시될 때 TPM 변경을 수락합니다.

8.  Windows 클라이언트 운영 체제 이미징 프로세스 중에 암호화를 시작할 준비가 되면 관리자 권한으로 명령 프롬프트를 열고 **** 다음 명령을 입력하여 시작을 자동으로 설정하고 MBAM 클라이언트 에이전트를 다시 시작합니다.

    **sc config mbamagent start= auto**

    **net start mbamagent**

9.  무시 레지스트리 값을 삭제하려면 Regedit.exe 실행하고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목으로 이동하십시오. **MBAM 노드를 마우스** 오른쪽 단추로 클릭한 다음 삭제를 **클릭합니다.**

## <a name="related-topics"></a>관련 항목

[MBAM 2.5 클라이언트 배포](deploying-the-mbam-25-client.md)

[MBAM 2.5 클라이언트 배포 계획](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a>MBAM에 대한 제안이 있나요?
- 여기에 제안을 추가하거나 [투표합니다.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- MBAM 문제의 경우 [MBAM TechNet 포럼 을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)
