---
title: Sequencer 설치 방법
description: Sequencer 설치 방법
author: dansimp
ms.assetid: 5e8f1696-9bc0-4f44-8cb7-b809b2daae10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b72330718a14cb8ffb0e582c946ff1e70539036c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813964"
---
# Sequencer 설치 방법


다음 절차를 사용 하 여 Microsoft App-v (Application Virtualization) 5.1 sequencer를 설치 합니다. Sequencer를 실행 하는 컴퓨터는 App-v 5.1 클라이언트 버전을 실행 하 고 있지 않아야 합니다.

이전에 App-v 시퀀서 설치를 업그레이드 하는 것은 지원 되지 않습니다.

**중요**  시퀀서 요구 사항의 전체 목록은 [app-v 5.1 필수 구성 요소](app-v-51-prerequisites.md) 및 [App-v 5.1 지원 되는 구성](app-v-51-supported-configurations.md)의 sequencer 섹션을 참조 하세요.

 

명령줄을 사용 하 여 App-v 5.1 sequencer를 설치할 수도 있습니다. 다음 목록에는 명령줄 및 **appv\_sequencer\_setup.exe**를 사용 하 여 sequencer를 설치 하는 옵션에 대 한 정보가 표시 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>설치 디렉터리를 지정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Microsoft 사용자 환경 개선 프로그램에서 참여할 수 있도록 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>설치 로그를 저장할 위치를 지정 합니다. 기본 위치는 <strong> % Temp% </strong> 입니다. 예를 들어 <strong> C:\ 로그 \ </strong> .log.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/q</p></td>
<td align="left"><p>자동 또는 자동 설치를 지정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Sequencer의 제거를 지정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>사용권 계약을 수락 합니다. 무인 설치에 필요 합니다. 사용 예: <strong> /ACCEPTEULA </strong> 또는 <strong> /ACCEPTEULA = 1 </strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>연결 된 레이아웃 작업을 지정 합니다. 또한 앱-V 5.1를 설치 하지 않고 Windows Installer (.msi) 및 스크립트 파일을 폴더로 추출 합니다. 값이 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>레이아웃 디렉터리를 지정 합니다. 문자열 값이 필요 합니다. 사용 예: <strong> /Layoutdir = "C:\Application Virtualization Client" </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? 또는/h 또는/help</p></td>
<td align="left"><p>관련 도움말을 표시 합니다.</p></td>
</tr>
</tbody>
</table>

 

**App-v 5.1 sequencer를 설치 하려면**

1.  앱-V 5.1 sequencer 설치 파일을 설치 될 컴퓨터에 복사 합니다. **appv\_sequencer\_setup.exe** 를 두 번 클릭 하 고 **설치**를 클릭 합니다.

2.  **소프트웨어 사용 조건** 페이지에서 사용 약관을 검토 해야 합니다. 사용 조건에 동의 하려면 **사용 조건에 동의를 선택 합니다.** **다음**을 클릭합니다.

3.  Microsoft **update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고 최신 페이지를 사용 하도록 설정 하려면 microsoft 업데이트를 **확인 하려면 microsoft update 사용 (권장)을 선택 합니다.** Microsoft 업데이트를 실행할 수 없도록 설정 하려면 **Microsoft Update를 사용 하지 않겠습니다**.를 선택 합니다. **다음**을 클릭합니다.

4.  **사용자 환경 개선 프로그램** 페이지에서 프로그램에 참여 하려면 **사용자 환경 개선 프로그램 참여**를 선택 합니다. 이렇게 하면 App-v 5.1을 사용 하는 방법에 대 한 정보를 수집할 수 있습니다. 프로그램에 참여 하지 않으려면 **지금 프로그램에 참여 하 고 싶지 않습니다를**선택 합니다. **설치**를 클릭합니다.

5.  시퀀서를 열려면 **시작** 을 클릭 한 다음 **Microsoft Application Virtualization sequencer**를 클릭 합니다.

**App-v 5.1 sequencer 설치 문제를 해결 하려면**

-   Sequencer 설치에 대 한 자세한 내용은 **% temp%** 폴더에서 오류 로그를 참조 하세요. 로그 파일을 검토 하려면 **시작**을 클릭 하 고 **% temp%** 를 입력 한 다음 **appv\_ 로그**를 찾습니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 배포 계획](planning-to-deploy-app-v51.md)

 

 





