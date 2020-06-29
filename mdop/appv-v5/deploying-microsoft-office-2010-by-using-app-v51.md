---
title: App-V를 사용하여 Microsoft Office 2010 배포
description: App-V를 사용하여 Microsoft Office 2010 배포
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814625"
---
# App-V를 사용하여 Microsoft Office 2010 배포


다음 방법 중 하나를 사용 하 여 Microsoft App-v (Application Virtualization) 5.1에 대 한 Office 2010 패키지를 만들 수 있습니다.

-   Application Virtualization (App-v) Sequencer

-   App-v (Application Virtualization) 패키지 가속기

## Office 2010에 대 한 앱-V 지원


다음 표에서는 App-v 버전, Office 패키지 만들기 방법, 지원 되는 라이선스, Office 2010에 대해 지원 되는 배포를 보여 줍니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">지원 되는 항목</th>
<th align="left">지원 수준</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>지원 되는 App-v 버전</p></td>
<td align="left"><ul>
<li><p>4.6</p></li>
<li><p>5.0</p></li>
<li><p>5.1</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 만들기</p></td>
<td align="left"><ul>
<li><p>시퀀스</p></li>
<li><p>패키지 가속기</p></li>
<li><p>Office 배포 키트</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>지원 되는 라이선스</p></td>
<td align="left"><p>볼륨 라이선스</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원되는 배포</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>개인 VDI</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Sequencer를 사용 하 여 Office 2010 앱-V 5.1 만들기


Office 2010는 앱-V 5.1에서 Office 2010 패키지를 만들기 위한 주요 방법 중 하나입니다. Microsoft는 지식 기반 문서를 통해 자세한 작성법을 제공 했습니다. App-v 5.1에서 Office 2010 패키지를 만들려면 다음 링크에서 자세한 지침을 참조 하세요.

[Microsoft Application Virtualization 5.0에서 Microsoft Office 2010을 시퀀싱 하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## 패키지 가속기를 사용 하 여 Office 2010 앱-V 5.1 패키지 만들기


Office 2010 App-v 5.1 패키지는 패키지 가속기를 통해 만들 수 있습니다. Microsoft는 Windows 10, Windows 8 및 Windows 7에서 Office 2010을 만들기 위한 패키지 가속기를 제공 했습니다. 패키지 가속기를 사용 하 여 App-v에 Office 2010 패키지를 만들려면 다음 페이지를 참조 하 여 적절 한 패키지 가속기에 액세스 합니다.

-   [Office Professional Plus 2010 용 app-v 5.0 패키지 가속기 – Windows 8](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [Office Professional Plus 2010 용 app-v 5.0 패키지 가속기-Windows 7](https://go.microsoft.com/fwlink/p/?LinkId=330678)

App-v 패키지 바로 연결을 사용 하 여 가상 응용 프로그램 패키지를 만드는 방법에 대 한 자세한 지침은 [App-v 패키지 가속기를 사용 하 여 가상 응용 프로그램 패키지를 만드는 방법을](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)참조 하세요.

## 앱에 대 한 Microsoft Office 패키지 배포-V 5.1


다음 App-v 배포 방법 중 하나를 사용 하 여 Office 2010 패키지를 배포할 수 있습니다.

-   System Center Configuration Manager

-   App-v server

-   독립 실행형-PowerShell 명령

## Office 앱-V 패키지 관리 및 사용자 지정


Office 2010 패키지는 알려진 패키지 관리 메커니즘을 통해 다른 App-v 5.1 패키지와 같이 관리할 수 있습니다. 예를 들어 Office 패키지 추가, 게시, 게시 취소 또는 제거 등 특별 한 지침이 필요 하지 않습니다.

## Windows와 Microsoft Office 통합


다음 표에는 Office 2010의 지원 되는 통합 지점에 대 한 전체 목록이 나와 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">확장점</th>
<th align="left">설명</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Firefox 및 Chrome 용 Lync 모임 참가 플러그 인</p></td>
<td align="left"><p>사용자가 Firefox 및 Chrome에서 Lync 모임에 참가할 수 있습니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>OneNote 인쇄 드라이버로 전송 됨</p></td>
<td align="left"><p>사용자가 OneNote에 인쇄할 수 있음</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OneNote에 연결 된 노트</p></td>
<td align="left"><p>OneNote에 연결 된 노트</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>OneNote Internet Explorer 추가 기능으로 보내기</p></td>
<td align="left"><p>IE에서 OneNote로 보낼 수 있는 사용자</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Lync 및 Outlook에 대 한 방화벽 예외</p></td>
<td align="left"><p>Lync 및 Outlook에 대 한 방화벽 예외</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>MAPI 클라이언트</p></td>
<td align="left"><p>기본 앱과 추가 기능은 MAPI를 통해 가상 Outlook과 상호 작용할 수 있습니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Firefox 용 SharePoint 플러그 인</p></td>
<td align="left"><p>사용자가 Firefox에서 SharePoint 기능을 사용할 수 있음</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>메일 제어판 애플릿</p></td>
<td align="left"><p>사용자가 Outlook의 메일 제어판 애플릿을 가져옵니다.</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>기본 Interop 어셈블리</p></td>
<td align="left"><p>관리 되는 추가 기능 지원</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 문서 캐시 처리기</p></td>
<td align="left"><p>Office 응용 프로그램에 대해 문서 캐시를 허용 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outlook 프로토콜 검색 처리기</p></td>
<td align="left"><p>사용자가 outlook에서 검색할 수 있음</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>Active X 컨트롤:</p></td>
<td align="left"><p>ActiveX 컨트롤에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> Activex 컨트롤 API 참조를 참조 </a> 하세요.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SiteClient</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Sharpoint Xmldocuments</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Sharepoint. ClipboardCtl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   이 (가) Copysud.</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx 관리자</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   OneDrive Pro 브라우저 도우미</p></td>
<td align="left"><p>Active X Control]</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>OneDrive Pro 아이콘 오버레이</p></td>
<td align="left"><p>사용자가 폴더를 찾을 때 Windows 탐색기 셸 아이콘 오버레이 (OneDrive Pro 폴더)</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## 추가 리소스


**Office 2013 앱-V 패키지 추가 리소스**

[Microsoft Office를 시퀀싱 된 앱으로 배포 하는 데 지원 되는 시나리오-V 패키지](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Office 2010 앱-V 패키지**

[Microsoft Application Virtualization 5.0 용 microsoft Office 2010 시퀀싱 키트](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[앱-V 5.0 Office 2010 패키지를 만들거나 사용할 때의 알려진 문제](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Microsoft Application Virtualization 5.0에서 Microsoft Office 2010을 시퀀싱 하는 방법](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**연결 그룹**

[Microsoft App-V v5에 연결 그룹 배포](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[연결 그룹 관리](managing-connection-groups51.md)

**동적 구성**

[App-V 5.1 동적 구성 정보](about-app-v-51-dynamic-configuration.md)






 

 





