---
title: UE-V 2. x 배포 준비
description: UE-V 2. x 배포 준비
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826423"
---
# UE-V 2. x 배포 준비


Microsoft UE-V (사용자 환경 가상화) 2.0 또는 2.1을 사용자가 엔터프라이즈에서 액세스 하는 장치 간에 설정을 동기화 하는 솔루션으로 배포 하기 전에 몇 가지 계획 및 준비를 수행 해야 합니다. 이 항목에서는 수행할 배포 유형 및 배포를 성공적으로 수행할 수 있는 준비 방법을 결정 하는 데 도움이 되는 정보를 제공 합니다.

먼저 UE-V를 배포 하는 데 사용할 수 있는 작업을 살펴보겠습니다.

-   UE-V 배포 계획

    배포 하기 전에 먼저 어떤 UE-V 기능을 배포할지 결정할 수 있도록 약간의 계획을 수행 하는 것이 좋습니다. 이 페이지를 나가면 아래 계획 정보를 읽어 보고 확인 하세요.

-   [UE-V 2.x에 대한 필수 기능 배포](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    모든 UE-V 배포에는 다음 활동이 필요 합니다.

    -   [설정 저장소 위치 정의](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [UE-V Agent를 배포 하 고 UE-V 구성을 관리 하는 방법 결정](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   설정이 동기화 되어야 하는 모든 사용자 컴퓨터에 [Ue-v Agent 설치](https://technet.microsoft.com/library/dn458891.aspx#agent)

-   선택적으로 [사용자 지정 응용 프로그램에 대 한 ue-v 2. x를 배포할](deploy-ue-v-2x-for-custom-applications-new-uevv2.md) 수 있습니다.

    계획은 다음과 같은 UE-V 기능이 필요한 사용자 지정 응용 프로그램 (타사 또는 lob (기간 업무))의 설정 동기화를 지원 하도록 UE-V를 사용할지 여부를 결정 하는 데 도움이 됩니다.

    -   [UEV 생성기를 설치](https://technet.microsoft.com/library/dn458942.aspx#uevgen) 하 여 사용자 지정 응용 프로그램 설정을 동기화 하는 데 필요한 사용자 지정 설정 위치 템플릿을 만들고 편집 하 고 유효성을 검사할 수 있습니다.

    -   UE-V 생성기를 사용 하 여 [사용자 지정 설정 위치 서식 파일 만들기](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates)

    -   사용자 지정 설정 위치 템플릿을 저장 하는 데 사용 하는 [ue-v 설정 템플릿 카탈로그 배포](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)

이 워크플로 다이어그램은 UE-V 배포에 대 한 개략적인 수준의 이해와 엔터프라이즈에서 UE-V를 배포 하는 방법을 결정 하는 의사 결정을 제공 합니다.

![deploymentworkflow](images/deploymentworkflow.png)

**Ue-v 배포 계획:** 먼저 몇 가지 계획을 선택 하 여 배포할 UE-V 구성 요소를 결정할 수 있습니다. UE-V 배포 계획에는 다음 항목이 포함 됩니다.

-   [사용자 지정 응용 프로그램의 설정 동기화 여부 결정](#deciding)

    이는 배포 중에 UE-V 생성기를 설치할지 여부를 결정 하며,이를 통해 사용자 지정 설정 위치 템플릿을 만들 수 있습니다. 이 작업에는 다음이 포함 됩니다.

    [Ue-v 배포에서 자동으로 동기화 되는 설정을](#autosyncsettings)검토 합니다.

    [다른 응용 프로그램에 대해 설정 동기화가 필요한 지 여부를 결정](#determinesettingssync)합니다.

-   고가용성 및 용량 계획과 같은 [ue-v 배포에 대 한 기타 고려 사항을](#considerations)검토 합니다.

-   [UE-V의 필수 구성 요소 및 지원 되는 구성 확인](#prereqs)

## <a href="" id="deciding"></a>사용자 지정 응용 프로그램의 설정 동기화 여부 결정


UE-V 배포의 경우 여러 설정이 자동으로 동기화 됩니다. 그러나 UE-V를 사용자 지정 하 여 lob (기간 업무) 및 타사 앱 등의 다른 응용 프로그램에 대 한 설정을 동기화 할 수도 있습니다.

UE-V를 통해 사용자 지정 응용 프로그램의 설정을 동기화 하도록 할지 결정 하는 것이 UE-V 배포 계획의 가장 중요 한 부분입니다. 이 섹션의 항목은 해당 결정을 내리는 데 도움이 됩니다.

### <a href="" id="autosyncsettings"></a>UE-V 배포에서 자동으로 동기화 되는 설정

이 섹션에서는 다음을 포함 하 여 기본적으로 UE-V에서 동기화 되는 설정에 대 한 정보를 제공 합니다.

설정이 기본적으로 동기화 되는 데스크톱 응용 프로그램

기본적으로 동기화 되는 Windows 바탕 화면 설정

Windows 앱 설정 동기화에 대 한 지원 문

UE-V를 통해 동기화 되는 특정 Microsoft Office 2013, Microsoft Office 2010 및 Microsoft Office 2007 설정의 전체 목록을 다운로드 하려면 [Microsoft office 용 ue-v (User Experience Virtualization) 설정 템플릿을](https://www.microsoft.com/download/details.aspx?id=46367) 참조 하세요.

### UE-V 2.1 및 UE-V 2.1 SP1에서 기본적으로 동기화 된 데스크톱 응용 프로그램

UE-V 2.1 또는 2.1 SP1 에이전트를 설치 하면 이러한 공통 Microsoft 응용 프로그램에 대 한 설정 값을 캡처하는 기본 설정 위치 템플릿 그룹이 등록 됩니다.

**팁**  
**Microsoft Office 2007 설정 동기화** – ue-v 2.1 및 2.1 SP1에서는 설정 위치 템플릿이 Office 2007 응용 프로그램에 기본적으로 포함 되어 있지 않습니다. 그러나 UE-V 2.0 또는 이전 버전의 Office 2007 서식 파일을 계속 사용할 수 있으며 [ue-v 서식 파일 갤러리](https://go.microsoft.com/fwlink/p/?LinkID=246589)에서 서식 파일을 가져올 수 있습니다.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>응용 프로그램 범주</strong></th>
<th align="left"><strong>설명</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office 2010 응용 프로그램</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2013 응용 프로그램</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Office 2013 업로드 센터</p>
<p>Microsoft 비즈니스용 OneDrive 2013</p>
<p>UE-V 2.1 및 2.1 SP1 Microsoft Office 2013 설정 위치 템플릿에는 향상 된 Outlook 서명 지원이 포함 되어 있습니다. 새, 회신 및 전달 된 전자 메일에 대 한 기본 서명 설정을 동기화 했습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>Outlook 프로필은 사용자가 Outlook 서명을 동기화 하려는 모든 장치에 대해 만들어야 합니다. 프로필이 아직 만들어지지 않은 경우 사용자가 프로필을 만든 다음 해당 장치에서 Outlook을 다시 시작 하 여 서명 동기화를 사용 하도록 설정할 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>브라우저 옵션: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 및 Internet Explorer 11</p></td>
<td align="left"><p>즐겨찾기, 홈 페이지, 탭, 도구 모음</p>
<div class="alert">
<strong>참고</strong><br/><p>UE-V는 Internet Explorer 쿠키에 대 한 설정을 로밍 하지 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 액세서리</p></td>
<td align="left"><p>Microsoft 계산기, 메모장, 워드 패드</p></td>
</tr>
</tbody>
</table>



**참고**  
UE-V 2.1 SP1은 Windows 10의 Microsoft 계산기와 이전 운영 체제의 Microsoft 계산기 간에 설정을 동기화 하지 않습니다.



### UE-V 2.0에서 기본적으로 동기화 된 데스크톱 응용 프로그램

UE-V 2.0 Agent를 설치 하면 이러한 공통 Microsoft 응용 프로그램에 대 한 설정 값을 캡처하는 기본 설정 위치 템플릿 그룹이 등록 됩니다.

**팁**  
**Microsoft office 2013 설정 동기화** – ue-v 2.0에서는 설정 위치 템플릿이 Office 2013 응용 프로그램에 기본적으로 포함 되어 있지 않지만 [ue-v 템플릿 갤러리](https://go.microsoft.com/fwlink/p/?LinkID=246589)에서 다운로드할 수 있습니다. [Office 2013를 ue-v 2.0와 동기화](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) 하면 office 2013 설정을 동기화 하는 지원 되는 서식 파일에 대 한 세부 정보가 제공 됩니다.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>응용 프로그램 범주</strong></th>
<th align="left"><strong>설명</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office 2007 응용 프로그램</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007</p>
<p>Microsoft Excel 2007</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007</p>
<p>Microsoft Publisher 2007</p>
<p>Microsoft SharePoint Designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2010 응용 프로그램</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>브라우저 옵션: Internet Explorer 8, Internet Explorer 9 및 Internet Explorer 10</p></td>
<td align="left"><p>즐겨찾기, 홈 페이지, 탭, 도구 모음</p>
<div class="alert">
<strong>참고</strong><br/><p>UE-V는 Internet Explorer 쿠키에 대 한 설정을 로밍 하지 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 액세서리</p></td>
<td align="left"><p>Microsoft 계산기, 메모장, 워드 패드</p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a>Windows 설정이 기본적으로 동기화 됨

UE-V는 이러한 Windows 설정에 대 한 설정 값을 캡처하는 설정 위치 템플릿을 포함 합니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows 설정</th>
<th align="left">설명</th>
<th align="left">적용 기준</th>
<th align="left">으로 내보내기</th>
<th align="left">기본 상태</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>바탕 화면 배경</p></td>
<td align="left"><p>현재 활성 상태인 바탕 화면 배경 또는 배경 무늬</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결, 예약 된 작업 이벤트</p></td>
<td align="left"><p>로그 오프, 잠금, 원격 연결 끊기, 사용자가 <strong> </strong> 회사 설정 센터에서 지금 동기화 클릭 또는 예약 된 작업 간격</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
<tr class="even">
<td align="left"><p>접근성</p></td>
<td align="left"><p>접근성 및 입력 설정, Microsoft 돋보기, 내레이터, 화상 키보드.</p></td>
<td align="left"><p>로그온만 가능 합니다.</p></td>
<td align="left"><p>로그 오프, 사용자가 <strong> 지금 </strong> 회사 설정 센터에서 동기화 클릭 또는 예약 된 작업 간격</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
<tr class="odd">
<td align="left"><p>바탕 화면 설정</p></td>
<td align="left"><p>시작 메뉴 및 작업 표시줄 설정, 폴더 옵션, 기본 바탕 화면 아이콘, 추가 시계, 지역 및 언어 설정</p></td>
<td align="left"><p>로그온만 가능 합니다.</p></td>
<td align="left"><p>로그 오프, 사용자가 <strong> </strong> 회사 설정 센터에서 지금 동기화 또는 예약 된 작업을 클릭 합니다.</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
</tbody>
</table>



**참고**  
Windows 8부터 UE-V는 시작 화면 (예: 항목 및 위치)과 관련 된 설정을 로밍 하지 않습니다. 또한 UE-V는 고정 된 작업 표시줄 항목 또는 Windows 파일 바로 가기의 동기화를 지원 하지 않습니다.



**중요**  
UE-V 2.1 SP1은 Windows 10 장치 간의 작업 표시줄 설정을 로밍 합니다. 그러나 UE-V는 이전 운영 체제를 실행 하는 Windows 10 장치 및 장치 간에 작업 표시줄 설정을 동기화 하지 않습니다.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">설정 그룹</th>
<th align="left">범주</th>
<th align="left">캡처하면</th>
<th align="left">적용</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>응용 프로그램 설정</strong></p></td>
<td align="left"><p>Windows 앱  </p></td>
<td align="left"><p>앱 닫기</p>
<p>Windows 앱 설정 변경 이벤트</p></td>
<td align="left"><p>시작 시 UE-V App Monitor 시작</p>
<p>앱 열기</p>
<p>Windows 앱 설정 변경 이벤트</p>
<p>설정 패키지 도착</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>데스크톱 응용 프로그램</p></td>
<td align="left"><p>응용 프로그램이 닫힙니다.</p></td>
<td align="left"><p>응용 프로그램이 열리고 닫힙니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>바탕 화면 설정</strong></p></td>
<td align="left"><p>바탕 화면 배경</p></td>
<td align="left"><p>잠금 또는 로그 오프</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결, 새 패키지 도착에 대 한 알림, 지금 사용자가 <strong> </strong> 회사 설정 센터에서 동기화 클릭 또는 예약 된 작업 실행을 진행 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>접근성 (공통 – 접근성, 내레이터, 돋보기, 화상 키보드)</p></td>
<td align="left"><p>잠금 또는 로그 오프</p></td>
<td align="left"><p>로그온</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>접근성 (셸-오디오, 접근성, 키보드, 마우스)</p></td>
<td align="left"><p>잠금 또는 로그 오프</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결, 새 패키지 도착에 대 한 알림, 지금 사용자가 <strong> </strong> 회사 설정 센터에서 동기화 클릭 또는 예약 된 작업 실행</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>바탕 화면 설정</p></td>
<td align="left"><p>잠금 또는 로그 오프</p></td>
<td align="left"><p>로그온</p></td>
</tr>
</tbody>
</table>



### UE-V-Windows 앱에 대 한 지원

Windows 앱의 경우 앱 개발자는 동기화 되는 설정을 지정 합니다. 설정 동기화를 사용 하도록 설정 된 Windows 앱을 지정할 수 있습니다.

Windows PowerShell 명령 프롬프트에서 컴퓨터의 설정을 동기화 할 수 있는 Windows 앱 목록 (패키지 패밀리 이름, 사용 상태 및 활성화 된 원본)을 표시 하려면 다음을 입력 합니다. `Get-UevAppxPackage`

**참고**  
Windows 8에서 UE-V는 도메인 사용자가 로그인 자격 증명을 Microsoft 계정에 연결 하는 경우 Windows 앱 설정을 동기화 하지 않습니다. 이 링크는 Windows 앱 설정 동기화를 사용 하지 않도록 설정을 Microsoft OneDrive에 동기화 합니다 (UE-V-V).



### UE-V-로밍 프린터 지원

UE-V 2.1 SP1에서는 네트워크 프린터가 네트워크의 모든 장치에 로그온 되어 있는 경우 사용자가 네트워크 프린터에 액세스할 수 있도록 디바이스 간에 로밍이 가능 합니다. 여기에는 기본값으로 설정 된 프린터를 로밍 하는 것이 포함 됩니다.

UE-V의 Printer 로밍에는 다음 시나리오 중 하나가 필요 합니다.

-   인쇄 서버는 새 장치로 로밍할 때 필요한 드라이버를 다운로드할 수 있습니다.

-   로밍 네트워크 프린터용 드라이버는 해당 네트워크 프린터에 액세스 해야 하는 모든 장치에 사전 설치 되어 있습니다.

-   프린터 드라이버는 Windows 업데이트에서 구할 수 있습니다.

**참고**  
UE-V 프린터 로밍 기능은 양면 인쇄와 같은 프린터 설정이 나 기본 **설정을 로밍하지 않습니다** .



### <a href="" id="determinesettingssync"></a>다른 응용 프로그램에 대해 동기화 된 설정이 필요한 지 여부 결정

UE-V 배포에서 자동으로 동기화 되는 설정을 검토 한 후에는 다른 응용 프로그램에 대 한 설정을 동기화할지 여부를 결정 하 여 엔터프라이즈 전체에서 UE-V를 배포 하는 방법을 결정 합니다.

관리자는 UE-V 솔루션에 포함할 데스크톱 응용 프로그램을 고려 하는 경우 사용자가 지정할 수 있는 설정 및 응용 프로그램이 해당 설정을 저장 하는 방법 및 위치를 고려해 야 합니다. 일부 데스크톱 응용 프로그램은 사용자 지정할 수 있는 설정을 포함 하지 않으며, 사용자가 일상적으로 사용자 지정할 수도 있습니다. 또한, 모든 데스크톱 응용 프로그램 설정을 여러 컴퓨터 또는 환경에서 안전 하 게 동기화 할 수 있는 것은 아닙니다.

일반적으로 다음 조건을 충족 하는 설정을 동기화 할 수 있습니다.

-   사용자가 액세스할 수 있는 위치에 저장 되는 설정 예를 들어 System32 또는 레지스트리의 HKEY \ _CURRENT \ _USER (HKCU) 섹션 외부에 저장 된 설정을 동기화 하지 마세요.

-   특정 컴퓨터에 국한 되지 않는 설정입니다. 예를 들어 네트워크 또는 하드웨어 구성을 제외 합니다.

-   데이터 손상 위험 없이 컴퓨터 간에 동기화 될 수 있는 설정 예를 들어 데이터베이스 파일에 저장 된 설정을 사용 하지 마세요.

### <a href="" id="checklistsettingssync"></a>사용자 지정 응용 프로그램 평가를 위한 검사 목록

다른 응용 프로그램에 대해 동기화가 설정 되어 있어야 하는 경우이 검사 목록을 사용 하 여 포함할 응용 프로그램을 확인할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>이 응용 프로그램에 사용자가 사용자 지정할 수 있는 설정이 포함 되어 있습니까?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>사용자가 이러한 설정을 동기화 하는 것이 중요 한가요?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>이러한 사용자 설정이 응용 프로그램 관리 또는 설정 정책 솔루션에 의해 이미 관리 되나요? UE-V는 로그온, 잠금 해제 또는 원격 연결 이벤트의 응용 프로그램 시작 및 Windows 설정에 대 한 응용 프로그램 설정을 적용 합니다. 다른 설정 공유 솔루션과 함께 UE-V를 사용 하는 경우 사용자가 동기화 된 설정 간에 일관성 문제가 발생할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>컴퓨터에 대 한 응용 프로그램 설정이 있나요? 하드웨어 또는 특정 컴퓨터 구성과 연결 된 응용 프로그램 기본 설정 및 사용자 지정은 세션 간에 일관성 없이 동기화 되므로 응용 프로그램 환경이 잘못 될 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Application Files directory 또는 사용자의 파일 디렉터리 (사용자 <strong> </strong> 이름]에 &lt; 강력한 &gt; AppData </strong> &lt; 강력한 &gt; </strong> locallow에 저장 되어 있는 응용 프로그램의 설정을 사용 합니까? 이러한 위치 중 하나에 저장 된 응용 프로그램 데이터는 해당 컴퓨터에 대 한 정보를 포함 하거나 데이터가 너무 커서 동기화 할 수 없기 때문에 사용자와 동기화 되지 않는 경우가 많습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>응용 프로그램이 동기화 하지 않아야 하는 다른 응용 프로그램 데이터를 포함 하는 파일에 대 한 설정을 저장 합니까? UE-V는 파일을 단일 단위로 동기화 합니다. 설정이 아닌 다른 응용 프로그램 데이터를 포함 하는 파일에 설정을 저장 한 경우이 추가 데이터를 동기화 하면 응용 프로그램 환경이 잘못 될 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>설정이 포함 된 파일의 크기 설정 동기화의 성능은 크기가 큰 파일의 영향을 받을 수 있습니다. 큰 파일을 포함 하면 설정 동기화의 성능에 영향을 줄 수 있습니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a>UE-V 배포를 준비할 때 고려해 야 할 사항


UE-V를 배포 하려고 준비 하는 경우에도 다음 사항을 고려해 야 합니다.

-   [자격 증명 동기화 관리](#creds)

-   [Windows 앱 설정 동기화](#appxsettings)

-   [사용자 지정 UE-V 설정 위치 템플릿](#custom)

-   [의도 하지 않은 사용자 설정 구성](#prevent)

-   [성능 및 용량](#capacity)

-   [고가용성](#high)

-   [컴퓨터 시계 동기화](#clocksync)

### <a href="" id="creds"></a>UE-V 2.1 및 UE-V 2.1 SP1의 자격 증명 동기화 관리

Microsoft Outlook 및 Lync를 비롯 한 많은 엔터프라이즈 응용 프로그램은 로그인 시 사용자에 게 도메인 자격 증명을 묻는 메시지를 표시 합니다. 사용자는 해당 자격 증명을 디스크에 저장 하 여 해당 응용 프로그램을 열 때마다 입력할 필요가 없도록 하는 옵션이 있습니다. 로밍 자격 증명 동기화를 사용 하도록 설정 하면 사용자가 한 컴퓨터에 자격 증명을 저장 하 고 해당 환경에서 사용 하는 모든 컴퓨터에 다시 입력 하지 않아도 됩니다. 사용자는 일부 도메인 자격 증명을 UE-V 2.1 및 2.1 SP1과 동기화 할 수 있습니다.

**중요**  
자격 증명 동기화는 기본적으로 사용 되지 않습니다. 이 기능을 구현 하려면 배포 중에 자격 증명 동기화를 명시적으로 사용 하도록 설정 해야 합니다.



UE-V 2.1 및 2.1 SP1은 엔터프라이즈 자격 증명을 동기화 할 수 있지만, 로컬 컴퓨터 에서만 사용 하도록 설정 된 자격 증명은 로밍되지 않습니다.

자격 증명은 동기화 설정 이므로 UE-V가 동기화 된 후 처음으로 컴퓨터에 로그인 할 때 프로필에 적용 됩니다.

자격 증명 동기화는 해당 설정 위치 템플릿에서 관리 되며 기본적으로 사용 되지 않습니다. 다른 서식 파일에 사용 되는 것과 동일한 방법으로이 서식 파일을 사용 하거나 사용 하지 않도록 설정할 수 있습니다. 이 기능에 대 한 서식 파일 식별자는 RoamingCredentialSettings입니다.

**중요**  
환경에서 Active Directory 자격 증명 로밍을 사용 하는 경우 UE-V 자격 증명 로밍 서식 파일을 사용 하지 않는 것이 좋습니다.



다음 방법 중 하나를 사용 하 여 자격 증명 동기화를 사용 하도록 설정 합니다.

-   회사 설정 센터

-   PowerShell

-   그룹 정책

**참고**  
동기화 하는 동안 자격 증명이 암호화 됩니다.



[회사 설정 센터](https://technet.microsoft.com/library/dn458903.aspx)**:** Windows 설정 아래의 로밍 자격 증명 설정 확인란을 선택 하 여 자격 증명 동기화를 사용 하도록 설정 합니다. 확인란의 선택을 취소 하 여 해제 합니다. 이 확인란은 계정이 Microsoft 계정을 사용 하 여 설정을 동기화 하도록 구성 되어 있지 않은 경우 회사 설정 센터에만 표시 됩니다.

[Powershell](https://technet.microsoft.com/library/dn458937.aspx)**:** 이 PowerShell cmdlet은 자격 증명 동기화를 사용 합니다.

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

이 PowerShell cmdlet은 자격 증명 동기화를 사용 하지 않습니다.

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[그룹 정책](https://technet.microsoft.com/library/dn458893.aspx)**:** 그룹 정책을 통해 자격 증명 동기화를 사용 하도록 설정 하려면 [최신 MDOP ADMX 템플릿을 배포](https://go.microsoft.com/fwlink/p/?LinkId=393944) 해야 합니다. 자격 증명 동기화는 Windows 설정으로 관리할 수 있습니다. 그룹 정책을 사용 하 여이 기능을 관리 하려면 Windows 동기화 설정 정책을 사용 하도록 설정 합니다.

1.  그룹 정책 편집기를 열고 **사용자 구성 – 관리 템플릿 (Windows 구성 요소-Microsoft 사용자 환경 가상화**)으로 이동 합니다.

2.  **Windows 설정 동기화**를 두 번 클릭 합니다.

3.  이 정책을 사용 하는 경우 **로밍 자격 증명** 확인란을 선택 하 여 자격 증명 동기화를 사용 하도록 설정 하거나, 선택을 취소 하 여 자격 증명 동기화를 사용 하지 않도록 설정할 수 있습니다.

4.  **확인**을 클릭합니다.

### UE-V를 통해 동기화 된 자격 증명 위치

응용 프로그램에서 다음 위치로 저장 한 자격 증명 파일이 동기화 됩니다.

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

다른 위치에 저장 된 자격 증명은 UE-V를 통해 동기화 되지 않습니다.

### <a href="" id="appxsettings"></a>Windows 앱 설정 동기화

UE-V는 다음 세 가지 방법으로 Windows 앱 설정 동기화를 관리 합니다.

-   **Windows 앱 동기화:** 모든 Windows 앱 동기화 허용 또는 거부

-   **Windows 앱 목록:** Windows 앱 목록 동기화

-   **목록에 없는 기본 동기화 동작:** Windows 앱 목록에 없는 Windows 앱의 동기화 동작을 확인 합니다.

자세한 내용은 [Windows 앱 목록을](https://technet.microsoft.com/library/dn458925.aspx#win8applist)참조 하세요.

### <a href="" id="custom"></a>사용자 지정 UE-V 설정 위치 템플릿

사용자 지정 응용 프로그램의 설정을 동기화 하기 위해 UE-V를 배포 하는 경우 UE-V 생성기를 사용 하 여 해당 데스크톱 응용 프로그램에 대 한 사용자 지정 설정 위치 템플릿을 만듭니다. 테스트 환경에서 사용자 지정 설정 위치 템플릿을 만들고 테스트 한 후 엔터프라이즈의 컴퓨터에 설정 위치 템플릿을 배포할 수 있습니다.

사용자 지정 설정 위치 템플릿은 시스템 센터 구성 관리자, 환경 설정, UE-V 설정 템플릿 카탈로그 구성 등의 ESD (엔터프라이즈 소프트웨어 배포) 메서드 같은 기존 배포 인프라를 사용 하 여 배포 해야 합니다. 구성 관리자 또는 그룹 정책을 사용 하 여 배포 된 템플릿은 UE-V WMI 또는 Windows PowerShell을 사용 하 여 등록 되어야 합니다.

사용자 지정 설정 위치 서식 파일에 대 한 자세한 내용은 [사용자 지정 응용 프로그램에 ue-v: x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)를 참조 하세요. 구성 관리자에서 UE-V를 사용 하는 방법에 대 한 자세한 내용은 [System Center Configuration Manager 2012에서 ue-v 2. x 구성을](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)참조 하세요.

### <a href="" id="prevent"></a>의도 하지 않은 사용자 설정 구성 방지

UE-V는 설정 저장소 위치에서 새 사용자 설정 정보를 다운로드 하 고 다음 인스턴스의 설정을 로컬 컴퓨터에 적용 합니다.

-   등록 된 UE-V 템플릿이 있는 응용 프로그램이 시작 될 때마다

-   사용자가 컴퓨터에 로그온 하는 경우

-   사용자가 컴퓨터의 잠금을 해제 하는 경우

-   UE-V를 설치한 원격 데스크톱 컴퓨터에 연결 하는 경우

-   동기화 컨트롤러 응용 프로그램 예약 된 작업이 실행 되는 경우

컴퓨터 A 및 컴퓨터 B에 UE-V를 설치한 경우 응용 프로그램에 대해 원하는 설정이 컴퓨터 A에 있으면 컴퓨터 A가 먼저 응용 프로그램을 열고 닫아야 합니다. 컴퓨터 B에서 응용 프로그램을 열고 닫은 경우 컴퓨터 A의 응용 프로그램 설정이 컴퓨터 B의 응용 프로그램 설정으로 구성 됩니다. 설정은 응용 프로그램 별로 컴퓨터 간에 동기화 됩니다. 시간이 지남에 따라 기본 설정으로 컴퓨터를 열고 닫을 때의 설정이 일관 되 게 유지 됩니다.

이 시나리오는 Windows 설정에도 적용 됩니다. 컴퓨터 B의 Windows 설정이 컴퓨터 A의 Windows 설정과 동일 해야 하는 경우 사용자는 먼저 로그온 하 고 컴퓨터 A를 로그 오프 해야 합니다.

사용자가 원하는 사용자 설정이 잘못 된 순서로 적용 되는 경우 설정을 덮어쓴 컴퓨터에서 특정 응용 프로그램 또는 Windows 구성에 대 한 복원 작업을 수행 하 여 복구할 수 있습니다. 자세한 내용은 [ue-v on-V 2. x에서 관리 백업 및 복원 관리](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)를 참조 하세요.

### <a href="" id="capacity"></a>성능 및 용량 계획

표준 디스크 용량 및 네트워크 상태 모니터링을 통해 UE-V에 대 한 요구 사항을 지정 합니다.

UE-V가 설정 패키지 저장소에 대 한 SMB (서버 메시지 블록) 공유를 사용 합니다. 설정 패키지의 크기는 각 응용 프로그램의 설정 정보에 따라 달라 집니다. 대부분의 설정 패키지는 작지만 데스크톱 이미지와 같은 잠재적으로 크기가 큰 파일을 동기화 하면 성능이 저하 될 수 있으며, 특히 네트워크 속도가 느릴 때 문제가 발생 합니다.

네트워크 지연 문제를 줄이려면 사용자 컴퓨터가 있는 동일한 로컬 네트워크에 설정 저장소 위치를 만듭니다. 설정 저장소 위치에 대해 사용자 당 20mb의 디스크 공간을 사용 하는 것이 좋습니다.

기본적으로 UE-V 동기화는 2 초 후에 시간이 초과 되어 대규모 설정 패키지 때문에 과도 한 지연이 발생 하는 것을 방지 합니다. [그룹 정책 개체](https://technet.microsoft.com/library/dn458893.aspx)를 사용 하 여 syncmethod = syncmethod 설정을 구성할 수 있습니다.

### <a href="" id="high"></a>UE-V의 고가용성

UE-V 설정 저장소 위치 및 설정 템플릿 카탈로그는 쓰기 가능한 공유에 사용자 데이터를 저장 하는 것을 지원 합니다. 고가용성을 보장 하려면 다음 조건을 따르세요.

-   NTFS 파일 시스템을 사용 하 여 저장소 볼륨을 포맷 합니다.

-   공유에서 DFS (분산 파일 시스템)를 사용할 수 있지만 제한 사항이 있습니다.
특히 dfs (분산 파일 시스템 이름) 네임 스페이스 (DFS-N)를 사용 하거나 사용할 수 없을 때 (예를 들어 Cd-r) 단일 대상 구성이 지원 됩니다.
마찬가지로, DFS-N에서는 단일 대상 구성만 지원 됩니다.
자세한 내용은 [복제 된 사용자 프로필 데이터에 대 한 Microsoft 지원 문의](https://go.microsoft.com/fwlink/p/?LinkId=313991) 및 [dfs 및 dfs 배포 시나리오에 대 한 microsoft 지원 정책에 대 한 정보](https://support.microsoft.com/kb/2533009)를 참조 하세요.

    또한 SYSVOL은 복제에 DFS-R을 사용 하기 때문에 UE-V 데이터 파일 복제에 SYSVOL을 사용할 수 없습니다.

-   [Ue-v 2. x에 대 한 설정 저장소 위치 배포](https://technet.microsoft.com/library/dn458891.aspx#ssl)에 지정 된 대로 공유 사용 권한과 NTFS acl (액세스 제어 목록)을 구성 합니다.

-   UE-V Agent와 함께 파일 서버 클러스터링을 사용 하 여 통신 실패 시 사용자 상태 데이터의 복사본에 대 한 액세스를 제공 합니다.

-   설정 저장소 경로 데이터 (사용자 데이터) 및 설정 템플릿 카탈로그 템플릿을 클러스터 된 공유에 저장 하거나 DFS-N 공유 또는 둘 다에 저장할 수 있습니다.

### <a href="" id="clocksync"></a>UE-V 설정 동기화에 대 한 컴퓨터 시계 동기화

UE-V 에이전트를 실행 하는 컴퓨터는 일관성 있는 설정 환경을 유지 하기 위해 시간 서버를 사용 해야 합니다. UE-V는 타임 스탬프를 사용 하 여 설정 저장소 위치에서 설정을 동기화 해야 하는지 여부를 결정 합니다. 컴퓨터 시계가 정확 하지 않으면 이전 설정이 최신 설정을 덮어쓰거나 새 설정이 설정 저장소 위치에 저장 되지 않을 수 있습니다.

## <a href="" id="prereqs"></a>UE-V의 필수 구성 요소 및 지원 되는 구성 확인


계속 하기 전에 UE-V를 실행 하기 위한 요구 사항이 환경에 포함 되어 있는지 확인 합니다.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>운영 체제</strong></th>
<th align="left"><strong>버전</strong></th>
<th align="left"><strong>서비스 팩</strong></th>
<th align="left"><strong>시스템 아키텍처</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate, Enterprise 또는 Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>UE-V 2.1의 경우 .NET Framework 4.5 이상입니다.</p>
<p>UE-V 2.0의 경우 .NET Framework 4 이상의 기능을 사용할 수가 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>UE-V 2.1의 경우 .NET Framework 4.5 이상입니다.</p>
<p>UE-V 2.0의 경우 .NET Framework 4 이상의 기능을 사용할 수가 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 및 Windows 8.1</p></td>
<td align="left"><p>엔터프라이즈 또는 Pro</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, 1607 이전 버전</p>
<div class="alert">
<strong>참고</strong><br/><p>UE-V 2.1 SP1만이 Windows 10, 1607 버전을 지원 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>엔터프라이즈 또는 Pro</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 및 Windows Server 2012 R2</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.6 이상</p></td>
</tr>
</tbody>
</table>



또한

-   **MDOP 라이선스:** 이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다. 엔터프라이즈 고객은 Microsoft 소프트웨어 보증을 통해 MDOP를 받을 수 있습니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 MDOP를 가져오는 방법 (을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   설치할 컴퓨터에 대 한 **관리 자격 증명**

**참고**  

-   WIndows 10, 버전 1607, UE-V를 사용 하 여 [엔터프라이즈 용 windows 10](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) 에 포함 되어 있으며 더 이상 Microsoft 데스크톱 최적화 팩의 일부가 아닙니다.

-   UE-V Agent의 UE-V Windows PowerShell 기능을 사용 하려면 .NET Framework 4 이상 및 Windows PowerShell 3.0 이상이 필요 합니다. [여기](https://go.microsoft.com/fwlink/?LinkId=309609)에서 Windows PowerShell 3.0을 다운로드 합니다.

-   Windows 7 또는 Windows Server 2008 R2 운영 체제를 실행 하는 컴퓨터에 .NET Framework 4 또는 .NET Framework 4.5을 설치 합니다. Windows 8, Windows 8.1 및 Windows Server 2012 운영 체제에는 .NET Framework 4.5이 설치 되어 있습니다. Windows 10 운영 체제에는 .NET Framework 4.6이 설치 되어 있습니다.
-   UE-V에서는 필수 프로필에 대 한 "로밍 캐시 삭제" 정책이 지원 되지 않으므로 사용할 수 없습니다.



UE-V와 관련 된 특수 한 RAM (임의 액세스 메모리) 요구 사항이 없습니다.

### 동기화 공급자를 통해 설정 동기화

동기화 공급자는 로컬 캐시를 다음 인스턴스의 설정 저장소 위치와 동기화 하는 사용자의 기본 설정입니다.

-   로그온/로그 오프

-   잠금/잠금 해제

-   원격 데스크톱 연결/연결 끊기

-   응용 프로그램 열기/닫기

예약 된 작업은 특정 응용 프로그램에 대 한 특정 트리거 이벤트를 통해 30 분 마다 설정 동기화를 관리 합니다. 자세한 내용은 [ue-v 2. x 예약 작업의 빈도 변경을](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)참조 하세요.

UE-V Agent는 엔터프라이즈 네트워크 (원격 컴퓨터 및 랩톱)에 항상 연결 되어 있지 않은 컴퓨터 및 네트워크에 항상 연결 되는 컴퓨터 (Windows Server 및 VDI (가상 데스크톱 인터페이스) 세션을 실행 하는 컴퓨터)에 대 한 사용자 설정을 동기화 합니다.

**항상 사용 가능한 연결이 있는 컴퓨터 동기화:** 항상 네트워크에 연결 된 컴퓨터에서 UE-V를 사용 하는 경우 설정 저장소 서버를 표준 네트워크 공유로 처리 하는 *Syncmethod = 없음* 매개 변수를 사용 하 여 설정을 동기화 하도록 ue-v agent를 구성 해야 합니다. 이 구성에서는 응용 프로그램 설정 가져오기가 지연 되는 경우이를 알리기 위해 UE-V Agent를 구성할 수 있습니다.

다음 방법 중 하나를 통해이 구성을 사용 하도록 설정 합니다.

-   UE-V를 설치 하는 동안 명령 프롬프트나 배치 파일에서 AgentSetup.exe 매개 변수 *Syncmethod = 없음*을 설정 합니다. [Ue-v 2. x 에이전트 배포는](https://technet.microsoft.com/library/dn458891.aspx#agent) 추가 정보를 제공 합니다.

-   UE-V를 설치한 후 System Center 2012 구성 관리자 또는 MDOP ADMX 템플릿의 설정 관리 기능을 사용 하 여 *Syncmethod = 없음* 구성을 푸시 합니다.

-   Windows PowerShell 또는 WMI (Windows Management Instrumentation)를 사용 하 여 *Syncmethod = 없음* 구성을 설정 합니다.

    **참고**  
    이러한 마지막 두 메서드는 풀링된 VDI (가상 데스크톱 인프라) 환경에는 작동 하지 않습니다.



설정 동기화를 시작 하기 전에 컴퓨터를 다시 시작 해야 합니다.

**참고**  
*Syncmethod = 없음*을 설정 하면 설정 변경 내용이 서버에 직접 저장 됩니다. 설정 저장소 경로에 대 한 네트워크 연결을 찾지 못한 경우 설정 변경 내용이 장치에 캐시 되 고 다음에 동기화 공급자가 실행 될 때 동기화 됩니다. 설정 저장소 경로를 찾을 수 없고 로그 오프할 때 풀링된 VDI 환경에서 사용자 프로필이 제거 되는 경우 설정 변경 내용이 손실 되 고 컴퓨터를 설정 저장소 경로에 다시 연결 하면 사용자가 변경 내용을 재적용 해야 합니다.



**외부 동기화 엔진 동기화:** *Syncmethod = External* 매개 변수는 사용자 컴퓨터의 로컬 폴더에 ue-v 설정이 기록 되는 경우 모든 외부 동기화 엔진 (예: 비즈니스용 OneDrive, 클라우드 폴더, Sharepoint 또는 Dropbox)을 사용 하 여 사용자가 액세스 하는 다른 컴퓨터에 이러한 설정을 적용할 수 있도록 지정 합니다.

**공유 VDI 세션에 대 한 지원:** UE-V 2.1 및 2.1 SP1은 최종 사용자 간에 공유 되는 VDI 세션에 대 한 지원을 제공 합니다. 특수 VDI 템플릿을 등록 하 고 구성할 수 있으며,이는 UE-V가 비영구 VDI 세션에 대해 모든 기능을 그대로 유지 하도록 보장 합니다.

**참고**  
비 영구적인 VDI 세션에 VDI 모드를 사용 하도록 설정 하지 않으면 [백업/복원 및 마지막으로 알려진 양호한 속도 (LKG)](https://technet.microsoft.com/library/dn878331.aspx)와 같은 특정 기능이 작동 하지 않습니다.



VDI 템플릿은 UE-V 2.1 및 2.1 SP1과 함께 제공 되며 일반적으로 설치 후에 사용할 수 있습니다. C:\\program files Files\\Microsoft 사용자 환경 Virtualization\\Templates\\VdiState.xml

### UE-V 생성기 지원에 대 한 필수 조건

사용자 지정 설정 위치 서식 파일을 만드는 데 사용 되는 컴퓨터에 UE-V 생성기를 설치 합니다. 이 컴퓨터는 설정이 동기화 된 응용 프로그램을 실행할 수 있습니다. UE-V 생성기 소프트웨어를 실행 하는 컴퓨터에서 관리자 그룹의 구성원 이어야 합니다.

UE-V 생성기는 NTFS 파일 시스템을 사용 하는 컴퓨터에 설치 해야 합니다. UE-V 생성기 소프트웨어에는 .NET Framework 4가 필요 합니다. 자세한 내용은 [사용자 지정 응용 프로그램에 대 한 ue-v 2. x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)를 참조 하세요.

## 이 제품에 대 한 기타 리소스


-   [Microsoft UE-V (User Experience Virtualization) 2. x](index.md)

-   [UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

-   [UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

-   [UE-V 2. x 문제 해결](troubleshooting-ue-v-2x-both-uevv2.md)

-   [UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)














