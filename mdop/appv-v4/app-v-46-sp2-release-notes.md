---
title: App-V 4.6 SP2 릴리스 정보
description: App-V 4.6 SP2 릴리스 정보
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822343"
---
# App-V 4.6 SP2 릴리스 정보


**이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.**

이 릴리스 정보는 Microsoft App-v (Application Virtualization) 4.6 SP2를 설치 하기 전에 자세히 읽어 보세요.

이 릴리스 정보에는 Application Virtualization 4.6 SP2를 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있습니다. 릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다. 이러한 릴리스 노트와 다른 앱-V 4.6 SP2 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## 제품 설명서 정보


App-v에 대 한 설명서에 대 한 자세한 내용은 Microsoft TechNet의 [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) 페이지를 참조 하세요.

## 사용자 의견 제공


앱-V 4.6 SP2에 대 한 피드백에 관심이 있습니다. 귀하의 의견을 보낼 수 있습니다 <mdopdocs@microsoft.com> .

**참고**  이 전자 메일 주소는 지원 채널이 아니지만, 귀하의 의견은 설명서 및 제품 릴리스에 대 한 향후 변경 사항을 계획 하는 데 도움이 됩니다.

 

MDOP 및 추가 학습 리소스에 대 한 최신 정보는 [Mdop 정보 경험](https://go.microsoft.com/fwlink/p/?LinkId=236032) 페이지를 참조 하세요.

새 업데이트 또는 피드백을 제공 하는 방법에 대 한 자세한 내용은 [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 참조 하세요.

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a>앱-V 4.6 SP2의 알려진 문제점


### 시스템을 시퀀싱 하는 경우 비시스템 물리적 드라이브에 대 한 짧은 파일 이름 지원이 비활성화 됨

Windows 8 또는 Windows Server 2012에서 시퀀스를 사용 하는 경우 비시스템 물리적 드라이브에 대 한 짧은 파일 이름 (8.3)에 대 한 지원은 기본적으로 비활성화 되어 있습니다.

시퀀싱 스테이션의 기본 가상 응용 프로그램 디렉터리 (예: "Q:\\appname")와 연결 된 기본 물리적 드라이브는 가상 응용 프로그램 패키지를 만들 때 App-v 4.6 SP2 Sequencer에서 짧은 파일 이름을 생성 하기 위해 짧은 파일 이름 (8.3) 지원을 제공 해야 합니다. Windows 8 또는 Windows Server 2012의 비시스템 물리적 드라이브에 대 한 짧은 파일 이름 (8.3) 지원은 기본적으로 사용 되지 않습니다.

**해결 방법:** 비시스템 물리적 드라이브에서 짧은 파일 이름 (8.3) 지원을 사용 하도록 설정 합니다. 다음 명령을 사용 하 여 Windows 8 또는 Windows Server 2012에서 짧은 파일 이름 지원을 사용 하도록 설정할 수 있습니다.

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

예를 들어 드라이브 문자가 "Q:" 이면 다음 명령을 사용 합니다.

``` syntax
fsutil 8dot3name set Q: 0
```

**참고**  App-v 파일 시스템은 Windows 8 또는 Windows Server 2012에서 짧은 경로를 올바르게 처리 하기 때문에 App-v 클라이언트에서이 설정을 변경할 필요는 없습니다.

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> App-v는 Windows 8의 파일 형식 또는 프로토콜 연결에 대 한 기본 처리기를 재정의 하지 않습니다.

Windows 8의 **제어판** 에서 **기본** 프로그램을 사용 하 여 기본 응용 프로그램을 선택 하는 경우 app-v는 해당 응용 프로그램의 연결 된 파일 형식 연결을 재정의 하지 않습니다.

**해결 방법:** 않아야.

### 가상화 된 Outlook 2010는 Windows 8의 mailto 클릭 가능 링크에 대 한 옵션으로 제공 되지 않습니다.

Mailto 셸 확장 기능은 Windows 8에서 가상화 된 Outlook 2010을 제공 하지 않습니다. 예를 들어 Windows 8에서 실행 되는 가상화 된 Outlook 2010의 mailto: 링크를 클릭 하면 새 전자 메일 창이 만들어지지 않습니다. 이 옵션은 windows 7 및 이전 버전의 Windows 운영 체제에서 올바르게 작동 합니다.

**해결 방법:** 않아야.

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> Microsoft 업데이트를 사용 하는 일부 로캘에서는 응용 프로그램 가상화 4.6 SP2 업데이트가 제공 되지 않음

Microsoft 업데이트를 사용 하는 경우 다음 언어 로캘에 대 한 앱-V 4.6 SP2 업데이트를 사용할 수 없습니다.

-   카자흐어

-   힌디어

-   세르비아어-키릴 자모

**해결 방법:** Microsoft WSUS (Windows Server Update Services)를 사용 하는 경우 영어 버전의 업데이트를 사용 하거나 Microsoft 업데이트 카탈로그에서 업데이트를 다운로드 합니다.

## 릴리스 노트 저작권 정보


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune 및 WindowsPowerShell는 Microsoft의 회사 그룹의 상표입니다. 다른 모든 상표는 해당 소유자의 재산입니다.



## 관련 항목


[Microsoft Application Virtualization 4.6 SP2 정보](about-microsoft-application-virtualization-46-sp2.md)

 

 





