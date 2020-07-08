---
title: App-V 5.0 SP2 릴리스 정보
description: App-V 5.0 SP2 릴리스 정보
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813329"
---
# App-V 5.0 SP2 릴리스 정보


**이러한 릴리스 노트에서 특정 문제를 검색 하려면 CTRL + F를 누릅니다.**

App-v 5.0 SP2를 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요.

이러한 릴리스 정보에는 App-v 5.0 SP2를 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있습니다. 릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다. 이러한 릴리스 노트와 다른 앱-V 5.0 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## 제품 설명서 정보


App-v 5.0 설명서에 대 한 자세한 내용은 Microsoft TechNet의 App-v 5.0 홈 페이지를 참조 하세요.

## 피드백 제공


앱-V 5.0에 대 한 피드백에 관심이 있습니다. 귀하의 의견을 보낼 수 있습니다 <mdopdocs@microsoft.com> .

**참고**  이 이메일 주소는 지원 채널이 아니지만, 귀하의 문서와 제품 릴리스에서 향후에 변경 사항을 계획 하는 데 도움이 될 것입니다.

 

MDOP 및 추가 학습 리소스에 대 한 최신 정보는 [Mdop 정보 경험](https://go.microsoft.com/fwlink/p/?LinkId=236032) 페이지를 참조 하세요.

새 업데이트 또는 피드백을 제공 하는 방법에 대 한 자세한 내용은 [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 참조 하세요.

## 앱 가상화 5.0 SP2 용 핫픽스 패키지 4의 알려진 문제


### 앱 가상화 5.0 SP2 용 핫픽스 패키지 4를 제거한 후 패키지가 작동을 중지 함

앱 가상화 5.0 SP2 용 핫픽스 패키지 4를 적용 한 경우 게시 된 패키지 Application Virtualization 5.0 SP2 용 핫픽스 패키지 4가 제거 되 면 작동을 중지 합니다.

방법을

다음 폴더가 있으면 삭제 해야 합니다.

**% localappdata%**  \\  **Microsoft**  \\  **AppV**  \\  **클라이언트**  \\  **VFS**  \\  게시 된 각 패키지에 대 한 ** &lt; 패키지 ID &gt; ** 입니다.

**참고**  이 폴더를 삭제 하려면 관리자 권한이 있어야 합니다.

 

앱을 사용 하 여 컴퓨터의 각 사용자 계정 및 핫픽스 패키지 4를 설치한 후에 게시 된 각 패키지 id에 대해 다음을 수행 합니다. 5.0 SP2:

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   바로 가기는 이전 섹션의 디렉터리에서 폴더를 삭제 한 후에도 사용자 세션에 계속 남아 있기 때문에 응용 프로그램을 다시 실행할 수 있습니다. 응용 프로그램을 다시 게시할 필요는 없습니다.

-   이 문제는 사용자가 게시 한 패키지 된 패키지와 전역적으로 게시 되는 Microsoft Office2013 등 모두에 대해 발생 합니다. 두 가지 유형의 패키지 모두에 대해 폴더를 삭제 해야 합니다.

-   로밍 앱 데이터 (**% appdata%**)에서 VFS 폴더를 삭제할 필요는 없습니다. **% Localappdata%** 만 삭제 해야 합니다.

### Microsoft Office 통합이 잘못 된 파일 시스템 위치를 가리킵니다.

Microsoft Office 통합이 잘못 된 파일 시스템 위치 (Groove.exe 오류 메시지)를 가리킵니다.

방법을

다음 방법 중 하나를 사용합니다.

1.  업그레이드 후 시작 폴더에서 바로 가기를 삭제 합니다.

2.  스크립트를 사용 하 여 시작 폴더의 바로 가기를 변경 합니다.

3.  배포 구성 파일을 사용 하 여 통합 루트에 대 한 바로 가기 대상을 지정 합니다.

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> Application Virtualization 5.0 SP2 설치 관리자 용 핫픽스 패키지 4는 시간이 오래 걸릴 수 있음

앱 가상화 5.0 SP2 설치 관리자 용 핫픽스 패키지 4는 기존 패키지 캐시에 저장 된 파일 수에 따라 시간이 오래 걸릴 수 있습니다.

핫픽스 패키지 4 중에 응용 프로그램 가상화에 대 한 관련 패키지 보안 설명자 업데이트 5.0 SP2 설치는 설치 하는 데 걸리는 시간에 상당한 영향을 미칩니다. 이전에 설치 설치는 지속 시간이 표준 이었습니다. 그러나 이제 패키지 캐시에서 준비 된 파일 수에 따라 달라 집니다.

해결 방법: 없음

### JIT V 패키지를 사용 하는 경우 응용 프로그램 가상화 5.0 SP2에 대 한 핫픽스 패키지 4를 제거 하지 못한다

핫픽스 패키지 4를 Application Virtualization 5.0 SP2에 설치한 다음 JIT (just-in-time 가상화)를 사용 중일 때 핫픽스를 제거 하려고 하면 다음 조건에 모두 해당 하는 경우 작업이 실패 합니다.

-   Windows Installer 파일 (.msi)을 사용 하 여 설치한 다음 Microsoft Installer 패치 파일 (.msp)을 사용 하 여 업데이트를 적용 합니다.

-   제어판의 프로그램 추가/제거 항목을 사용 하 여 업데이트를 제거 하려고 합니다.

-   컴퓨터에서 JIT-V를 사용 하는 패키지가 실행 되 고 있습니다.

해결 방법: 다음 단계를 완료 합니다.

1.  Windows PowerShell을 열고 다음 명령을 실행 합니다.

    -   **가져오기-모듈 appvclient**

    -   **Get-AppvClientPackage | 중지-AppvClientPackage**

2.  프로그램 추가/제거를 사용 하 여 업데이트를 제거 합니다.

## 앱-V 5.0 SP2의 알려진 문제점


### <a href="" id="bkmk-folderredirection"></a>App-v 클라이언트 폴더 리디렉션에서 파일 을% AppData% 에서% LocalAppData%로 이동 하지 못하는 경우가 있습니다.

% AppData%가 폴더 리디렉션에 대해 구성한 공유 네트워크 폴더 이면 최종 사용자가 컴퓨터를 전환할 때 또는 로밍 하는 동안 로컬 AppData 지워질 때 해당 변경 내용을 손실 하 고 다시 로그온 할 수 있습니다. 이 오류는 마지막으로 알려진 업로드를 나타내는 레지스트리 키 (AppDataTime)가 로컬 캐시 된 AppData와 동기화 되지 않기 때문에 발생 합니다.

해결 방법: 최종 사용자가 로그온 하거나 로그 오프할 때 각 관련 패키지에 대해 다음 레지스트리 키를 수동으로 삭제 합니다.

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

마지막 사용자가 로그인 한 후 패키지의 응용 프로그램을 처음으로 시작 하는 경우% LocalAppData%이 (가) 이미 최신 상태 이더라도 App-V는 압축 된% AppData%를 강제로 다운로드 합니다.

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> App-v 5.0 서비스 팩 2 (App-v 5.0 SP2)에 App-v 서버의 새 버전이 포함 되어 있지 않음

App-v 5.0 SP2에는 App-v 서버의 새 버전이 포함 되어 있지 않습니다. 환경에서 Windows 8.1를 실행 하는 App-v 5.0 SP2 클라이언트를 배포 하 고 App-v 인프라를 사용 하 여 클라이언트를 관리 하려는 경우 [핫픽스 패키지 2 For Microsoft Application Virtualization 5.0 서비스 팩 1](https://go.microsoft.com/fwlink/?LinkId=386634)을 설치 해야 합니다. (https://go.microsoft.com/fwlink/?LinkId=386634)

다음 메서드 중 하나를 사용 하 여 App-v 5.0 SP2 클라이언트를 실행 하 고 관리 하는 경우 클라이언트 업데이트는 필요 하지 않습니다.

-   독립 실행형 모드.

-   Configuration Manager.

-   제 3 자 ESD.

App-v 5.0 SP2 클라이언트는 Windows 8.1과 완벽 하 게 호환 됩니다.

해결 방법: 없음

## 릴리스 노트 저작권 정보


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune 및 WindowsPowerShell는 Microsoft의 회사 그룹의 상표입니다. 다른 모든 상표는 해당 소유자의 재산입니다.








## 관련 항목


[App-V 5.0 SP2 정보](about-app-v-50-sp2.md)

 

 





