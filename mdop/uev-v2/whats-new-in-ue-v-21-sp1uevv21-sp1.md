---
title: UE-V 2.1 SP1의 새로운 기능
description: UE-V 2.1 SP1의 새로운 기능
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827428"
---
# UE-V 2.1 SP1의 새로운 기능


사용자 환경 가상화 2.1 SP1은 UE-V 2.1에 비해 이러한 새로운 기능과 기능을 제공 합니다. [MICROSOFT ue-v (User Experience Virtualization) 2.1 Sp1 릴리스](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) 정보는 UE-V 2.1 SP1 릴리스에 대 한 자세한 정보를 제공 합니다.

## Windows 10 지원


UE-V 2.1 SP1은 이전 버전의 UE-V에서 지원 되는 소프트웨어 외에도 Windows 10에 대 한 지원을 추가 합니다.

### Microsoft Azure와의 호환성

Windows 10에서 엔터프라이즈 사용자는 windows 앱 설정 및 Windows 운영 체제 설정을 OneDrive 대신 Azure로 동기화 할 수 있습니다. Windows 10 enterprise 동기화 기능은 온-프레미스 도메인에 가입 된 컴퓨터에만 UE-V를 사용 하 여 사용할 수 있습니다. Windows 10 및 UE-V를 함께 사용할 수 있도록 설정 하려면 각 클라이언트 또는 그룹 정책의 PowerShell을 사용 하 여 다음 UE-V 템플릿을 사용 하지 않도록 설정 해야 합니다.

그룹 정책의 Microsoft 사용자 환경 가상화 노드에서 다음 정책 설정을 구성 합니다.

-   "Windows 앱을 동기화 하지 않음" 사용

-   "Windows 설정 동기화" 사용 안 함

### Windows 10 지원에 대해 변경 된 설정 동기화 동작

UE-V 2.1 SP1은 Windows 10 장치 간의 작업 표시줄 설정을 로밍 합니다. 그러나 UE-V는 이전 운영 체제를 실행 하는 Windows 10 장치 및 장치 간에 작업 표시줄 설정을 동기화 하지 않습니다.

또한 UE-V 2.1 SP1은 Windows 10의 Microsoft 계산기와 이전 운영 체제의 Microsoft 계산기 간 설정을 동기화 하지 않습니다.

## 로밍 네트워크 프린터용 지원 추가


UE-V 2.1 SP1에서는 네트워크 프린터가 네트워크의 모든 장치에 로그온 되어 있는 경우 사용자가 네트워크 프린터에 액세스할 수 있도록 디바이스 간에 로밍이 가능 합니다. 여기에는 기본값으로 설정 된 프린터를 로밍 하는 것이 포함 됩니다.

UE-V의 Printer 로밍에는 다음 시나리오 중 하나가 필요 합니다.

-   인쇄 서버는 새 장치로 로밍할 때 필요한 드라이버를 다운로드할 수 있습니다.

-   로밍 네트워크 프린터용 드라이버는 해당 네트워크 프린터에 액세스 해야 하는 모든 장치에 사전 설치 되어 있습니다.

-   프린터 드라이버는 Windows 업데이트에서 구할 수 있습니다.

**참고**  UE-V 프린터 로밍 기능은 양면 인쇄와 같은 프린터 설정이 나 기본 **설정을 로밍하지 않습니다** .

 

## Office 2013 설정 위치 템플릿


UE-V 2.1 및 2.1 SP1에는 Outlook 서명 지원이 향상 된 Microsoft Office 2013 설정 위치 템플릿이 포함 되어 있습니다. 새, 회신 및 전달 된 전자 메일에 대 한 기본 서명 설정을 동기화 했습니다. 고객은 더 이상 기본 서명 설정을 선택할 필요가 없습니다.

**참고**  Outlook 프로필은 사용자가 Outlook 서명을 동기화 하려는 모든 장치에 대해 만들어야 합니다. 프로필이 아직 만들어지지 않은 경우 사용자가 프로필을 만든 다음 해당 장치에서 Outlook을 다시 시작 하 여 서명 동기화를 사용 하도록 설정할 수 있습니다.

 

이전에는 UE-V 에이전트를 사용 하 여 자동으로 배포 되 고 등록 된 Microsoft Office 2010 설정 위치 템플릿이 포함 되어 있습니다. Office 365에서 UE-V 2.1를 사용 하 여 office 2013 설정이 office 365에서 roamed 여부를 결정 합니다. 설정이 Office 365에 의해 roamed 경우 UE-V를 통해 roamed 되지 않습니다. [Office 2013의 사용자 및 로밍 설정 개요](https://go.microsoft.com/fwlink/p/?LinkID=391220) 자세한 정보를 제공 합니다.

UE-V 2.1를 사용 하 여 설정 동기화를 사용 하도록 설정 하려면 다음 중 하나를 수행 합니다.

-   그룹 정책을 사용 하 여 Office 365 동기화를 사용 하지 않도록 설정

-   Office 2013 설치 중에 Office 365 동기화 환경 사용 안 함

UE-V 2.1은 [office 2013 및 office 2010 템플릿을](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)제공 합니다. 이 릴리스는 Office 2007 서식 파일을 제거 합니다. 사용자는 UE-V 2.0 또는 이전 버전의 Office 2007 서식 파일을 계속 사용할 수 있으며 [여기](https://go.microsoft.com/fwlink/p/?LinkID=246589)에 있는 ue-v 템플릿 갤러리에서 서식 파일을 가져올 수 있습니다.






## 관련 항목


[UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

[UE-V 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Microsoft User Experience Virtualization(UE-V) 2.1 SP1 릴리스 정보](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





