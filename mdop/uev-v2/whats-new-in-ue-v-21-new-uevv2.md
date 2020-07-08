---
title: UE-V 2.1의 새로운 기능
description: UE-V 2.1의 새로운 기능
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826263"
---
# UE-V 2.1의 새로운 기능


사용자 환경 가상화 2.1는 UE-V 2.0에 비해 이러한 새로운 기능과 기능을 제공 합니다. [MICROSOFT ue-v (User Experience Virtualization) 2.1 릴리스](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) 정보는 ue-v 2.1 릴리스에 대 한 자세한 정보를 제공 합니다.

## Office 2013 설정 위치 템플릿


UE-V 2.1에는 향상 된 Outlook 서명이 지원 되는 Microsoft Office 2013 설정 위치 서식 파일이 포함 되어 있습니다. UE-V 2.1에서 서명 데이터는 사용자 장치 간에 동기화 됩니다. 새, 회신 및 전달 된 전자 메일에 대 한 기본 서명 설정을 동기화 했습니다. 고객은 더 이상 기본 서명 설정을 선택할 필요가 없습니다.

**참고**  Outlook 프로필은 사용자가 Outlook 서명을 동기화 하려는 모든 장치에 대해 만들어야 합니다. 프로필이 아직 만들어지지 않은 경우 사용자가 프로필을 만든 다음 해당 장치에서 Outlook을 다시 시작 하 여 서명 동기화를 사용 하도록 설정할 수 있습니다.

 

이전에는 UE-V 에이전트를 사용 하 여 자동으로 배포 되 고 등록 된 Microsoft Office 2010 설정 위치 템플릿이 포함 되어 있습니다. Office 365에서 UE-V 2.1를 사용 하 여 office 2013 설정이 office 365에서 roamed 여부를 결정 합니다. 설정이 Office 365에 의해 roamed 경우 UE-V를 통해 roamed 되지 않습니다. [Office 2013의 사용자 및 로밍 설정 개요](https://go.microsoft.com/fwlink/p/?LinkID=391220) 자세한 정보를 제공 합니다.

UE-V 2.1를 사용 하 여 설정 동기화를 사용 하도록 설정 하려면 다음 중 하나를 수행 합니다.

-   그룹 정책을 사용 하 여 Office 365 동기화를 사용 하지 않도록 설정

-   Office 2013 설치 중에 Office 365 동기화 환경 사용 안 함

UE-V 2.1은 [office 2013 및 office 2010 템플릿을](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)제공 합니다. 이 릴리스는 Office 2007 서식 파일을 제거 합니다. 사용자는 UE-V 2.0 또는 이전 버전의 Office 2007 서식 파일을 계속 사용할 수 있으며 [여기](https://go.microsoft.com/fwlink/p/?LinkID=246589)에 있는 ue-v 템플릿 갤러리에서 서식 파일을 가져올 수 있습니다.

## 분산 파일 시스템 네임 스페이스 사용자를 위한 수정


UE-V를 사용 하 여 DFSN (Distributed File System 네임 스페이스) 지원이 향상 되었습니다. Syncprovider이 설정 된 UE-V 구성을 추가 합니다. PowerShell 또는 WMI를 사용 하 여이 구성을 사용 하지 않도록 설정 하면 사용자가 UE-V ping을 사용 하지 않도록 설정할 수 있습니다. DFSN 서버를 사용 하는 경우 UE-V ping이이 서버가 ping에 응답 하지 않기 때문에 오류가 발생 합니다. 비 응답은 UE-V가 설정을 동기화 하지 못하게 합니다. UE-V ping을 사용 하지 않도록 설정 하면 UE-V 동기화가 정상적으로 작동 합니다.

UE-V ping을 사용 하지 않도록 설정 하려면 다음 PowerShell cmdlet을 사용 합니다.

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## 자격 증명 동기화


UE-V 2.1는 고객에 게 Windows 자격 증명 관리자에 저장 된 자격 증명과 인증서를 동기화 할 수 있는 기능을 제공 합니다. 이 구성 요소는 기본적으로 사용 되지 않습니다. 이 구성 요소를 사용 하도록 설정 하면 사용자가 도메인 자격 증명과 인증서를 동기화 상태로 유지할 수 있습니다. 사용자가 장치에서 한 번 로그인 할 수 있으며, 이러한 자격 증명은 모든 UE-V 사용 디바이스에서 해당 사용자에 대해 로밍 됩니다. [Ue-v 2.1를 사용 하 여 자격 증명 관리](https://technet.microsoft.com/library/dn458932.aspx#creds) 추가 정보를 제공 합니다.

**참고**  Windows 8 이상에서 자격 증명 관리자는 웹 자격 증명을 포함 합니다. 이러한 자격 증명은 사용자의 장치 간에 동기화 되지 않습니다.

 

## UE-V 및 Microsoft 계정 동기화


UE-V는 Microsoft 계정 동기화 라고도 하는 "OneDrive에 설정 동기화"가 설정 되어 있는지 검색 합니다. Microsoft 계정이 설정을 동기화 하도록 구성 되지 않은 경우 UE-V는 장치 간에 Windows 앱, AppX 패키지 및 Windows 데스크톱 설정을 동기화 합니다. 이렇게 하면 사용자가 엔터프라이즈 방화벽 외부에서 동기화 하지 않고 스토어 앱, 음악, 그림 및 기타 Microsoft 계정 사용 가능 응용 프로그램에 액세스할 수 있습니다. UE-V는 그룹 정책에서 OneDrive와의 설정 동기화를 중지할지 또는 사용자가 사용자 컨트롤의 **이 컴퓨터에서 설정을 동기화 할** 수 없도록 설정할지 여부를 확인 합니다.

## 외부의 SyncMethod에 대 한 지원


**External** 이라는 새 [syncmethod 구성은](https://technet.microsoft.com/library/dn554321.aspx) 사용자 컴퓨터의 로컬 폴더에 ue-v 설정이 기록 되는 경우 모든 외부 동기화 엔진 (예: 비즈니스용 OneDrive, 클라우드 폴더, Sharepoint 또는 Dropbox)을 사용 하 여 사용자가 액세스 하는 다른 컴퓨터에 이러한 설정을 적용할 수 있습니다.

## VDI 모드에 대 한 향상 된 지원


UE-V 2.1에는 최종 사용자 간에 공유 되는 [VDI 세션에 대 한 지원이](https://technet.microsoft.com/library/dn458932.aspx#vdi) 포함 됩니다. 관리자는 특수 VDI 템플릿을 등록 하 고 구성할 수 있으며,이를 통해 UE-V는 영구 VDI 세션에 대해 모든 기능을 그대로 유지 합니다.

**참고**  비 영구적인 VDI 세션에 VDI 모드를 사용 하도록 설정 하지 않으면 백업/복원 및 LKG 같은 특정 기능이 작동 하지 않습니다.

 

## 관리 백업 및 복원


사용자가 새 장치를 사용할 때 Set Uevtemplate 프로필 PowerShell cmdlet을 사용 하 여 설정 위치 템플릿을 **백업** 또는 **로밍 (기본)** 프로필에 배치 하 여 추가 설정을 복원할 수 있습니다. 이렇게 하면 컴퓨터 설정이 사용자 설정 외에도 새 컴퓨터와 동기화 될 수 있습니다. 백업 프로필에 할당 된 서식 파일은 해당 장치에 대해 백업 되 고 장치별로 구성 됩니다. [Ue-v 2. x에서 관리 백업 및 복원 관리에 대 한](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) 자세한 내용은 추가 정보를 제공 합니다.

## 추가 Windows 설정 동기화


이제 UE-V는 터치 키보드 개인 설정, 맞춤법 사전을 동기화 하 고 최근 앱 및 화면 가장자리 설정에 대 한 앱 전환 기능을 사용 하 여 Windows 8 및 Windows 8.1 장치 간에 동기화 할 수 있습니다.






## 관련 항목


[UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

[UE-V 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Microsoft User Experience Virtualization(UE-V) 2.1 릴리스 정보](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





