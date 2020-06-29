---
title: Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법
description: Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824623"
---
# Windows 배포의 일부로 MBAM 클라이언트를 배포하는 방법


관리자는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트를 사용 하 여 엔터프라이즈의 컴퓨터에서 BitLocker 드라이브 암호화를 적용 하 고 모니터링할 수 있습니다. TPM (신뢰할 수 있는 플랫폼 모듈) 칩이 있는 컴퓨터의 경우 이미징 및 Windows 배포 프로세스의 일부로 클라이언트 컴퓨터에서 BitLocker 관리 및 암호화를 사용 하도록 설정 하 여 BitLocker 클라이언트를 조직에 통합할 수 있습니다.

**참고**  
Microsoft BitLocker 관리 및 클라이언트 시스템 요구 사항 모니터링을 검토 하려면 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요.



Windows 배포의 초기 이미징 단계 동안 BitLocker로 클라이언트 컴퓨터를 암호화 하면 조직에 MBAM을 구현 하는 데 필요한 관리 오버 헤드가 낮아질 수 있습니다. 또한 배포 된 모든 컴퓨터에 이미 BitLocker가 실행 되 고 있으며 올바르게 구성 되어 있는지 확인 합니다.

**참고**  
이 항목의 절차에서는 Windows 레지스트리를 수정 하는 방법에 대해 설명 합니다. 레지스트리 편집기를 잘못 사용 하면 심각한 문제가 발생할 수 있으며,이 경우 Windows를 다시 설치 해야 할 수 있습니다. Microsoft는 레지스트리 편집기의 잘못 된 사용으로 인해 발생 하는 문제에 대 한 해결을 보장할 수 없습니다. 레지스트리 편집기 사용에 따른 모든 책임은 사용자에 게 있습니다.



**Windows 배포의 일부로 컴퓨터를 암호화 하려면**

1.  조직이 TPM (신뢰할 수 있는 플랫폼 모듈) 보호기 또는 BitLocker의 TPM + PIN 보호기 옵션을 사용할 계획 이라면, MBAM을 배포 하기 전에 TPM 칩을 활성화 해야 합니다. TPM 칩을 정품 인증 하는 경우 프로세스에서 나중에 재부팅을 피하고 조직의 요구 사항에 따라 TPM 칩이 올바르게 구성 되어 있는지 확인 합니다. 컴퓨터의 BIOS에서 수동으로 TPM 칩을 정품 인증 해야 합니다.

    **참고**  
    일부 공급 업체는 운영 체제 내에서 BIOS의 TPM 칩을 켜고 정품 인증 하는 도구를 제공 합니다. TPM 칩을 구성 하는 방법에 대 한 자세한 내용은 제조업체 문서를 참조 하세요.



2.  Microsoft BitLocker 관리 및 모니터링 클라이언트 에이전트를 설치 합니다.

3.  컴퓨터를 도메인에 가입 (권장)

    -   컴퓨터가 도메인에 가입 되어 있지 않으면 복구 암호가 MBAM 키 복구 서비스에 저장 되지 않습니다. 복구 키를 저장할 수 없는 경우 기본적으로 MBAM은 암호화를 허용 하지 않습니다.

    -   복구 키가 MBAM 서버에 저장 되기 전에 컴퓨터가 복구 모드에서 시작 되는 경우 컴퓨터를 reimaged 해야 합니다. 사용할 수 있는 복구 방법이 없습니다.

4.  관리자 권한으로 명령 프롬프트를 실행 하 고, MBAM 서비스를 중지 한 다음 서비스를 **수동** 또는 **요청에**맞게 설정한 후 다음 명령을 입력 하 여 시작 합니다.

    **net stop mbamagent**

    **sc config mbamagent 시작 = 요청**

5.  MBAM 에이전트에 대 한 레지스트리 설정을 설정 하 여 그룹 정책을 무시 하 고, **Regedit**를 실행 하 여 **운영 체제 전용 암호화** 용 TPM을 실행 한 다음 C:\\program files Files\\Microsoft\\MDOP Mbam\\mbamdeploymentkeytemplate에서 레지스트리 키 템플릿을 가져옵니다.

6.  Regedit에서 HKLM\\SOFTWARE\\Microsoft\\MBAM로 이동 하 여 다음 표에 나열 된 설정을 구성 합니다.

    레지스트리 항목

    구성 설정

    DeploymentTime

    0 = 해제

    1 = 배포 시간 정책 설정 사용 (기본값)

    UseKeyRecoveryService

    0 = key 에스크로를 사용 하지 않음 (이 경우 다음 두 레지스트리 항목은 필요 없음)

    1 = 키 복구 시스템에서 키 에스크로 사용 (기본값)

    권장: 컴퓨터가 키 복구 서비스와 통신할 수 있어야 합니다. 계속 하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인 합니다.

    KeyRecoveryOptions

    0 = 복구 키만 업로드

    1 = 복구 키 및 키 복구 패키지를 업로드 합니다 (기본값).

    KeyRecoveryServiceEndPoint

    이 값을 키 복구 웹 서버의 URL (예: http:// &lt; computer name/MBAMRecoveryAndHardwareService/CoreService.svc.)으로 설정 합니다 &gt; .



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. Mbam 에이전트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작 합니다. 다시 부팅할 준비가 되 면 관리자 권한으로 명령 프롬프트에서 다음 명령을 실행 합니다.

   **net start mbamagent**

8. 컴퓨터가 다시 시작 되 고 BIOS에서 TPM 변경을 수락 하 라는 메시지가 표시 되 면 변경 사항을 적용 합니다.

9. Windows 클라이언트 운영 체제 이미징 프로세스 중에 암호화를 시작할 준비가 되 면, MBAM 에이전트 서비스를 다시 시작 하 고 관리자 권한으로 명령 프롬프트를 실행 하 고 다음 명령을 입력 하 여 **자동** 으로 시작을 설정 합니다.

   **sc config mbamagent 시작 = 자동**

   **net start mbamagent**

10. Regedit를 실행 하 고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목으로 이동해 서 bypass 레지스트리 값을 제거 합니다. **Mbam** 노드를 삭제 하려면 노드를 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 클릭 합니다.

## 관련 항목


[MBAM 2.0 클라이언트 배포](deploying-the-mbam-20-client-mbam-2.md)









