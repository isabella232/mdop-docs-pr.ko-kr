---
title: UE-V 2.x 배포 준비
description: UE-V 2.x 배포 준비
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
ms.openlocfilehash: 3e4d4b69975deda473372345733d8e8593a4775d
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910533"
---
# <a name="prepare-a-ue-v-2x-deployment"></a>UE-V 2.x 배포 준비


사용자가 엔터프라이즈에서 액세스하는 장치 간에 설정을 동기화하기 위한 솔루션으로 Microsoft User Experience Virtualization(UE-V) 2.0 또는 2.1을 배포하기 전에 계획 및 준비를 몇 가지 진행합니다. 이 항목에서는 수행하게 될 배포 유형과 배포가 성공적으로 수행될 수 있도록 준비할 수 있는 준비 작업을 결정하는 데 도움이 됩니다.

먼저 다음과 같은 작업을 배포하기 위해 수행할 작업을 UE-V.

-   배포 UE-V 계획

    아무 것도 배포하기 전에 먼저 계획을 약간 세우면 배포할 UE-V 수 있습니다. 따라서 이 페이지를 나가는 경우 아래 계획 정보를 다시 읽고 읽어야 합니다.

-   [UE-V 2.x에 대한 필수 기능 배포](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    모든 UE-V 배포하려면 다음 활동이 필요합니다.

    -   [설정 저장소 위치 정의](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [배포 에이전트를 배포하고 UE-V 구성을 관리하는 UE-V 결정](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [설정이 UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) 필요한 모든 사용자 컴퓨터에 UE-V 에이전트 설치

-   원하는 경우 사용자 지정 응용 프로그램용 UE-V [배포할 수 있습니다.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    계획을 세우면 다음과 같은 UE-V 응용 프로그램(타사 또는 LINE-OF-BUSINESS)에 대한 설정 동기화를 지원할지 여부를 UE-V 있습니다.

    -   사용자 지정 응용 프로그램 설정을 동기화하는 데 필요한 사용자 지정 설정 위치 템플릿을 만들고 편집하고 유효성을 검사할 수 있도록 [UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) 생성기를 설치합니다.

    -   [UE-V](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) 생성기를 사용하여 사용자 지정 설정 위치 템플릿 만들기

    -   [사용자 UE-V 설정 위치](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) 템플릿을 저장하는 데 사용하는 기본 설정 템플릿 카탈로그 배포

이 워크플로 다이어그램은 엔터프라이즈에서 UE-V 배포하는 방법을 결정하는 결정에 대한 높은 수준의 UE-V 제공합니다.

![deploymentworkflow.](images/deploymentworkflow.png)

**배포 UE-V 계획:** 먼저 배포할 구성 요소를 결정할 수 있도록 UE-V 약간의 계획을 세우고자 합니다. 배포 UE-V 계획에는 다음이 필요합니다.

-   [사용자 지정 응용 프로그램의 설정을 동기화할지 여부 결정](#deciding)

    이렇게 하면 사용자 지정 설정 위치 템플릿을 만들 수 있는 UE-V 생성기를 설치할지 여부가 결정됩니다. 이 예제에는 다음이 수반됩니다.

    배포에서 자동으로 동기화되는 설정을 [UE-V 검토합니다.](#autosyncsettings)

    다른 응용 프로그램에 대해 설정을 [동기화해야 하는지 여부를 확인합니다.](#determinesettingssync)

-   [고가용성 및](#considerations)용량 계획과 같은 UE-V 고려 사항을 검토합니다.

-   [구성에 대한 선행 구성 및 지원되는 구성 UE-V](#prereqs)

## <a name="decide-whether-to-synchronize-settings-for-custom-applications"></a><a href="" id="deciding"></a>사용자 지정 응용 프로그램에 설정 여부 결정


배포 UE-V 많은 설정이 자동으로 동기화됩니다. 그러나 비즈니스용 앱과 UE-V 앱과 같은 다른 응용 프로그램의 설정을 동기화하기 위해 사용자 지정할 수도 있습니다.

사용자 지정 응용 UE-V 동기화할지 결정하는 것이 사용자 지정 응용 프로그램 배포를 계획하는 UE-V 부분일 수 있습니다. 이 섹션의 항목은 이러한 결정을 내리는 데 도움이 됩니다.

### <a name="settings-that-are-automatically-synchronized-in-a-ue-v-deployment"></a><a href="" id="autosyncsettings"></a>설정 배포에서 자동으로 동기화되는 UE-V 수 있습니다.

이 섹션에서는 다음을 포함하여 UE-V 동기화되는 설정에 대한 정보를 제공합니다.

설정이 기본적으로 동기화되는 데스크톱 응용 프로그램

Windows 동기화되는 데스크톱 설정

앱 설정 Windows 지원 설명

Microsoft Office [](https://www.microsoft.com/download/details.aspx?id=46367) 2013, Microsoft Office Microsoft Office 2010 및 Microsoft Office 2007 설정의 전체 목록을 다운로드하려면 Microsoft Office 사용자 환경 가상화(UE-V) 설정 템플릿을 UE-V.

### <a name="desktop-applications-synchronized-by-default-in-ue-v-21-and-ue-v-21-sp1"></a>UE-V 2.1 및 UE-V 2.1 SP1에서 기본적으로 동기화되는 데스크톱 응용 프로그램

UE-V 2.1 또는 2.1 SP1 에이전트를 설치하면 이러한 일반적인 Microsoft 응용 프로그램의 설정 값을 캡처하는 기본 설정 위치 템플릿 그룹을 등록합니다.

**팁**  
**Microsoft Office 2007** 설정 동기화 – UE-V 2.1 및 2.1 SP1에서는 Office 2007 응용 프로그램에 대한 설정 위치 템플릿이 더 이상 포함되지 않습니다. 그러나 UE-V 2.0 이전 버전의 Office 2007 템플릿을 계속 사용할 수 있으며 UE-V 서식 파일 갤러리에서 템플릿을 얻을 [수 있습니다.](https://go.microsoft.com/fwlink/p/?LinkID=246589)



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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화된 모든 설정 목록 </a> 다운로드)</p></td>
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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화된 모든 설정 목록 </a> 다운로드)</p></td>
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
<p>Microsoft OneDrive for Business 2013</p>
<p>UE-V 2.1 및 2.1 SP1 Microsoft Office 2013 설정 위치 템플릿에는 향상된 Outlook 지원이 포함됩니다. 새 전자 메일, 회신 및 전달된 전자 메일에 대한 기본 서명 설정 동기화가 추가되었습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>사용자가 Outlook 서명을 동기화하려는 디바이스에 대해 Outlook 만들어야 합니다. 프로필이 아직 만들어지지 않은 경우 사용자는 프로필을 만든 다음 해당 장치에서 Outlook 동기화를 사용하도록 설정할 수 있습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>브라우저 옵션: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 및 Internet Explorer 11</p></td>
<td align="left"><p>즐겨찾기, 홈페이지, 탭 및 도구 모음.</p>
<div class="alert">
<strong>참고</strong><br/><p>UE-V 쿠키에 대한 설정을 로밍하지 Internet Explorer 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 액세서리</p></td>
<td align="left"><p>Microsoft 계산기, 메모장, WordPad.</p></td>
</tr>
</tbody>
</table>



**참고**  
UE-V 2.1 SP1은 이전 운영 체제의 Microsoft 계산기 Windows 10 Microsoft 계산기 설정을 동기화하지 않습니다.



### <a name="desktop-applications-synchronized-by-default-in-ue-v-20"></a>UE-V 2.0에서 기본적으로 동기화되는 데스크톱 응용 프로그램

UE-V 2.0 에이전트를 설치하면 이러한 일반적인 Microsoft 응용 프로그램에 대한 설정 값을 캡처하는 기본 설정 위치 템플릿 그룹을 등록합니다.

**팁**  
**Microsoft Office 2013** 설정 동기화 – UE-V 2.0에서는 Office 2013 응용 프로그램에 대한 설정 위치 서식 파일은 기본적으로 포함되지 않지만 UE-V 서식 파일 갤러리에서 다운로드할 [수](https://go.microsoft.com/fwlink/p/?LinkID=246589)있습니다. [Office 2013을 UE-V 2.0과](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) 동기화하면 Office 2013 설정을 동기화하는 지원되는 템플릿에 대한 세부 정보가 표시됩니다.



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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화된 모든 설정 목록 </a> 다운로드)</p></td>
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
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화된 모든 설정 목록 </a> 다운로드)</p></td>
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
<td align="left"><p>즐겨찾기, 홈페이지, 탭 및 도구 모음.</p>
<div class="alert">
<strong>참고</strong><br/><p>UE-V 쿠키에 대한 설정을 로밍하지 Internet Explorer 않습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 액세서리</p></td>
<td align="left"><p>Microsoft 계산기, 메모장, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a name="windows-settings-synchronized-by-default"></a><a href="" id="autosyncsettings2"></a>Windows 동기화되는 설정

UE-V 설정에 대한 설정 값을 캡처하는 설정 위치 템플릿이 Windows 포함됩니다.

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
<th align="left">적용</th>
<th align="left">내보내기</th>
<th align="left">기본 상태</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>바탕 화면 배경</p></td>
<td align="left"><p>현재 활성 데스크톱 배경 또는 배경 무늬입니다.</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결, 예약된 작업 이벤트</p></td>
<td align="left"><p>Logoff, lock, remote disconnect, user clicking <strong> Sync Now in Company 설정 </strong> Center, or scheduled task interval</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
<tr class="even">
<td align="left"><p>접근성</p></td>
<td align="left"><p>접근성 및 입력 설정, Microsoft 돋보기, 내레이터 및 화면 키보드.</p></td>
<td align="left"><p>로그온만 합니다.</p></td>
<td align="left"><p>로그오프, 회사 설정 센터에서 지금 동기화 클릭 또는 예약된 작업 <strong> </strong> 간격</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
<tr class="odd">
<td align="left"><p>데스크톱 설정</p></td>
<td align="left"><p>시작 메뉴 및 작업 표시줄 설정, 폴더 옵션, 기본 데스크톱 아이콘, 추가 시계 및 지역 및 언어 설정</p></td>
<td align="left"><p>로그온만 합니다.</p></td>
<td align="left"><p>로그오프, 회사 설정 센터에서 지금 동기화 클릭 <strong> </strong> 또는 예약된 작업</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
</tbody>
</table>



**참고**  
Windows 8 UE-V 시작 화면과 관련된 설정(예: 항목 및 위치)을 로밍하지 않습니다. 또한 UE-V 작업 표시줄 항목 또는 파일 바로 가기 키의 동기화를 Windows 않습니다.



**중요**  
UE-V 2.1 SP1은 장치 간에 작업 표시줄 Windows 10 로밍합니다. 그러나 UE-V 운영 체제를 실행하는 장치와 Windows 10 작업 표시줄 설정을 동기화하지 않습니다.



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
<th align="left">캡처</th>
<th align="left">적용</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>응용 프로그램 설정</strong></p></td>
<td align="left"><p>Windows 앱  </p></td>
<td align="left"><p>앱 닫기</p>
<p>Windows 설정 변경 이벤트</p></td>
<td align="left"><p>시작 시 UE-V 앱 모니터 시작</p>
<p>앱 열기</p>
<p>Windows 앱 설정 변경 이벤트</p>
<p>설정 패키지 도착</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>데스크톱 응용 프로그램</p></td>
<td align="left"><p>응용 프로그램 닫기</p></td>
<td align="left"><p>응용 프로그램이 열리고 닫히기</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>데스크톱 설정</strong></p></td>
<td align="left"><p>바탕 화면 배경</p></td>
<td align="left"><p>Lock 또는 logoff</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결, 새 패키지 도착 알림, 사용자가 회사 설정 센터에서 지금 동기화를 <strong> </strong> 클릭하거나 예약된 작업 실행을 클릭합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>접근성(일반 - 접근성, 내레이터, 돋보기, 화면 키보드)</p></td>
<td align="left"><p>Lock 또는 Logoff</p></td>
<td align="left"><p>로그온</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>접근성(셸 - 오디오, 접근성, 키보드, 마우스)</p></td>
<td align="left"><p>Lock 또는 logoff</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결, 새 패키지 도착 알림, 사용자가 회사 설정 센터에서 지금 동기화 클릭 또는 예약된 <strong> </strong> 작업 실행</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>데스크톱 설정</p></td>
<td align="left"><p>Lock 또는 logoff</p></td>
<td align="left"><p>로그온</p></td>
</tr>
</tbody>
</table>



### <a name="ue-v-support-for-windows-apps"></a>UE-V 앱에 대한 Windows 지원

앱 Windows 앱 개발자는 동기화되는 설정을 지정합니다. 설정 동기화에 사용할 Windows 앱을 지정할 수 있습니다.

컴퓨터의 설정을 패키지 패밀리 이름Windows 사용 상태 및 사용 가능한 원본과 동기화할 수 있는 앱 목록을 표시하려면 Windows PowerShell 명령 프롬프트에 다음을 입력합니다. `Get-UevAppxPackage`

**참고**  
이 Windows 8 현재 UE-V 사용자가 로그인 자격 증명을 Microsoft 계정에 Windows 경우 앱 설정을 동기화하지 않습니다. 이 연결은 설정과 Microsoft OneDrive UE-V 동기화하여 앱 설정의 Windows 비활성화합니다.



### <a name="ue-v-support-for-roaming-printers"></a>UE-V 지원

UE-V 2.1 SP1을 사용하면 네트워크의 모든 장치에 로그온할 때 사용자가 네트워크 프린터에 액세스할 수 있도록 장치 간에 네트워크 프린터를 로밍할 수 있습니다. 여기에는 기본값으로 설정된 프린터 로밍이 포함됩니다.

UE-V 프린터 로밍에는 다음 시나리오 중 하나가 필요합니다.

-   인쇄 서버는 새 장치로 로밍할 때 필요한 드라이버를 다운로드할 수 있습니다.

-   로밍 네트워크 프린터용 드라이버는 해당 네트워크 프린터에 액세스해야 하는 모든 장치에 미리 설치되어 있습니다.

-   프린터 드라이버는 업데이트에서 Windows 있습니다.

**참고**  
이 UE-V 로밍 기능은 **양면** 인쇄와 같은 프린터 설정이나 기본 설정을 로밍하지 않습니다.



### <a name="determine-whether-you-need-settings-synchronized-for-other-applications"></a><a href="" id="determinesettingssync"></a>다른 응용 프로그램에 대해 설정을 동기화해야 하는지 여부 결정

UE-V 배포에서 자동으로 동기화되는 설정을 검토한 후 다른 응용 프로그램에 대해 설정을 동기화할지 여부를 결정해야 합니다. 이렇게 하면 엔터프라이즈 전체에서 UE-V 수 있습니다.

관리자는 UE-V 솔루션에 포함할 데스크톱 응용 프로그램을 고려할 때 사용자가 사용자 지정할 수 있는 설정과 응용 프로그램에서 해당 설정을 저장하는 방법 및 위치를 고려합니다. 일부 데스크톱 응용 프로그램에는 사용자 지정하거나 사용자가 정기적으로 사용자 지정하는 설정이 없습니다. 또한 모든 데스크톱 응용 프로그램 설정을 여러 컴퓨터 또는 환경에서 안전하게 동기화할 수 있는 것은 아닙니다.

일반적으로 다음 조건을 충족하는 설정을 동기화할 수 있습니다.

-   설정 액세스할 수 있는 위치에 저장되는 위치입니다. 예를 들어 System32에 저장된 설정을 레지스트리의 HKEY\_CURRENT\_USER(HKCU) 섹션 외부에 동기화하지 않습니다.

-   설정 특정 컴퓨터와 관련이 없는 사용자 지정 예를 들어 네트워크 또는 하드웨어 구성을 제외합니다.

-   설정 손상된 데이터 위험 없이 컴퓨터 간에 동기화할 수 있습니다. 예를 들어 데이터베이스 파일에 저장된 설정은 사용하지 않습니다.

### <a name="checklist-for-evaluating-custom-applications"></a><a href="" id="checklistsettingssync"></a>사용자 지정 응용 프로그램 평가 검사 목록

다른 응용 프로그램에 대해 설정이 동기화되도록 결정한 경우 이 검사 목록을 사용하여 포함할 응용 프로그램을 확인할 수 있습니다.

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
<td align="left"><p>이 응용 프로그램에 사용자가 사용자 지정할 수 있는 설정이 포함되어 있나요?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>사용자에게 이러한 설정을 동기화하는 것이 중요한가요?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>이러한 사용자 설정은 응용 프로그램 관리 또는 설정 정책 솔루션에서 이미 관리하나요? UE-V 시작 및 로그온, 잠금 해제 또는 원격 연결 Windows 응용 프로그램 설정에 응용 프로그램 설정을 적용합니다. 다른 설정 UE-V 공유 솔루션과 함께 사용하면 동기화된 설정에서 사용자가 불일치할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>응용 프로그램 설정이 컴퓨터와 관련이 있습니까? 하드웨어 또는 특정 컴퓨터 구성과 연결된 응용 프로그램 기본 설정 및 사용자 지정은 세션 전체에서 일관되게 동기화되지 못하며 응용 프로그램 환경이 나쁨을 유발할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>응용 프로그램이 프로그램 파일 디렉터리 또는 사용자 <strong> </strong> [사용자 이름] 강력한 &lt; &gt; AppData </strong> &lt; 강력한 LocalLow 디렉터리에 있는 &gt; 파일 디렉터리에 설정을 </strong> 저장하나요? 이러한 위치 중 하나에 저장된 응용 프로그램 데이터는 컴퓨터와 관련이 있기 때문에 또는 데이터가 너무 크기 때문에 일반적으로 사용자와 동기화하면 안 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>응용 프로그램에서 동기화하면 안 되는 다른 응용 프로그램 데이터가 포함된 파일에 설정을 저장하나요? UE-V 단일 단위로 파일을 동기화합니다. 설정이 설정이 없는 응용 프로그램 데이터가 포함된 파일에 설정을 저장하는 경우 이 추가 데이터를 동기화하면 응용 프로그램 환경이 나아질 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>설정이 포함된 파일의 규모는 얼마나 하나요? 설정 동기화 성능은 큰 파일의 영향을 받을 수 있습니다. 큰 파일을 포함하면 설정 동기화 성능에 영향을 줄 수 있습니다.</p></td>
</tr>
</tbody>
</table>



## <a name="other-considerations-when-preparing-a-ue-v-deployment"></a><a href="" id="considerations"></a>배포를 준비할 때의 기타 UE-V 사항


또한 배포를 준비할 때 다음과 같은 사항도 고려해야 UE-V.

-   [자격 증명 동기화 관리](#creds)

-   [Windows 설정 동기화](#appxsettings)

-   [사용자 UE-V 설정 위치 템플릿](#custom)

-   [의도하지 않은 사용자 설정 구성](#prevent)

-   [성능 및 용량](#capacity)

-   [고가용성](#high)

-   [컴퓨터 시계 동기화](#clocksync)

### <a name="managing-credentials-synchronization-in-ue-v-21-and-ue-v-21-sp1"></a><a href="" id="creds"></a>UE-V 2.1 및 UE-V 2.1 SP1에서 자격 증명 동기화 관리

Microsoft Outlook 및 Lync를 비롯한 많은 엔터프라이즈 응용 프로그램은 로그인 시 사용자에게 도메인 자격 증명을 입력하라는 메시지를 사용자에게 제공합니다. 사용자는 자격 증명을 디스크에 저장하여 이러한 응용 프로그램을 열 때마다 자격 증명을 입력할 필요가 없습니다. 로밍 자격 증명 동기화를 사용하도록 설정하면 사용자가 자신의 자격 증명을 한 컴퓨터에 저장하고 환경에서 사용하는 모든 컴퓨터에 자격 증명을 다시 입력하지 않도록 할 수 있습니다. 사용자는 일부 도메인 자격 증명을 UE-V 2.1 및 2.1 SP1과 동기화할 수 있습니다.

**중요**  
자격 증명 동기화는 기본적으로 사용하지 않도록 설정되어 있습니다. 이 기능을 구현하려면 배포 중에 자격 증명 동기화를 명시적으로 사용하도록 설정해야 합니다.



UE-V 2.1 및 2.1 SP1에서 엔터프라이즈 자격 증명을 동기화할 수 있지만 로컬 컴퓨터에서만 사용할 자격 증명은 로밍하지 않습니다.

자격 증명은 동기 설정으로, 동기화 후 컴퓨터에 처음 로그인할 때 프로필에 UE-V 적용됩니다.

자격 증명 동기화는 기본적으로 사용하지 않도록 설정되는 자체 설정 위치 템플릿에 의해 관리됩니다. 다른 템플릿에 사용되는 동일한 메서드를 통해 이 템플릿을 사용하도록 설정하거나 사용하지 않도록 설정할 수 있습니다. 이 기능의 템플릿 식별자는 RoamingCredentialSettings입니다.

**중요**  
환경에서 Active Directory 자격 증명 로밍을 사용하는 경우 자격 증명 로밍 서식 파일을 사용하지 UE-V 것이 좋습니다.



다음 방법 중 하나를 사용하여 자격 증명 동기화를 사용하도록 설정할 수 있습니다.

-   회사 설정 센터

-   PowerShell

-   그룹 정책

**참고**  
동기화 중에 자격 증명이 암호화됩니다.



[회사 설정 센터:](https://technet.microsoft.com/library/dn458903.aspx)**** 자격 증명 동기화를 사용하도록 설정하려면 설정 자격 증명 서비스 로밍 확인란을 Windows 설정 확인란을 선택합니다. 이 확인란을 사용하지 않도록 설정하십시오. 이 확인란은 Microsoft 계정을 설정 설정을 동기화하도록 계정이 구성되어 있지 않은 경우 Company 설정 Center에만 표시됩니다.

[PowerShell:](https://technet.microsoft.com/library/dn458937.aspx)**** 이 PowerShell cmdlet은 자격 증명 동기화를 사용할 수 있도록 합니다.

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

이 PowerShell cmdlet은 자격 증명 동기화를 사용하지 않도록 설정합니다.

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[그룹 정책:](https://technet.microsoft.com/library/dn458893.aspx)**** 그룹 정책을 통해 자격 증명 동기화를 사용하도록 설정하려면 최신 [MDOP ADMX](https://go.microsoft.com/fwlink/p/?LinkId=393944) 템플릿을 배포해야 합니다. 자격 증명 동기화는 자격 증명 설정으로 Windows 관리됩니다. 그룹 정책을 사용하여 이 기능을 관리하려면 동기화 설정 Windows 사용하도록 설정하십시오.

1.  그룹 정책 편집기를 열고 사용자 구성 - 관리 템플릿 - Windows **구성 요소 -** Microsoft User Experience Virtualization.

2.  설정 동기화를 **Windows 클릭합니다.**

3.  해당 정책을 사용하는 경우 로밍 자격 증명 확인란을 확인하여 자격 증명 동기화를 사용하도록 설정하거나 자격 증명 동기화를 선택 해제하여 자격 증명 동기화를 사용하지 않도록 설정할 수 있습니다. ****

4.  **확인**을 클릭합니다.

### <a name="credential-locations-synchronized-by-ue-v"></a>사용자와 동기화된 자격 증명 UE-V

응용 프로그램에서 저장한 자격 증명 파일은 다음 위치에 동기화됩니다.

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

다른 위치에 저장된 자격 증명은 다른 위치로 UE-V.

### <a name="windows-app-settings-synchronization"></a><a href="" id="appxsettings"></a>Windows 설정 동기화

UE-V 세 가지 Windows 앱 설정 동기화를 관리합니다.

-   **앱 Windows 동기화:** 앱 동기화 허용 또는 Windows 거부

-   **Windows 목록:** 앱 목록 Windows 동기화

-   **목록에 없는 기본 동기화 동작:** 앱 목록에 없는 Windows 앱의 동기화 동작을 Windows 합니다.

자세한 내용은 앱 목록 [Windows 참조하세요.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

### <a name="custom-ue-v-settings-location-templates"></a><a href="" id="custom"></a>사용자 UE-V 설정 위치 템플릿

사용자 지정 응용 UE-V 동기화하기 위해 배포하는 경우 UE-V 생성기를 사용하여 해당 데스크톱 응용 프로그램에 대한 사용자 지정 설정 위치 템플릿을 만듭니다. 테스트 환경에서 사용자 지정 설정 위치 템플릿을 만들고 테스트한 후 엔터프라이즈의 컴퓨터에 설정 위치 템플릿을 배포할 수 있습니다.

사용자 지정 설정 위치 템플릿은 기본 설정이나 기본 설정이 있는 엔터프라이즈 ESD(소프트웨어 배포) System Center Configuration Manager 같은 기존 배포 인프라를 사용하여 배포하거나 UE-V 설정 템플릿 카탈로그를 구성해야 합니다. Configuration Manager 또는 그룹 정책으로 배포된 템플릿은 WMI 또는 그룹 정책을 사용하여 UE-V 등록해야 Windows PowerShell.

사용자 지정 설정 위치 템플릿에 대한 자세한 내용은 [Deploy UE-V 2.x for Custom Applications를 참조하십시오.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md) Configuration Manager와 함께 UE-V 대한 자세한 내용은 [Configuring UE-V 2.x with System Center Configuration Manager 2012을 참조하십시오.](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

### <a name="prevent-unintentional-user-settings-configuration"></a><a href="" id="prevent"></a>의도하지 않은 사용자 설정 구성 방지

UE-V 저장 위치에서 새 사용자 설정 정보를 다운로드하고 이러한 경우 로컬 컴퓨터에 설정을 적용합니다.

-   응용 프로그램이 등록된 응용 프로그램을 시작할 때마다 UE-V.

-   사용자가 컴퓨터에 로그온할 때

-   사용자가 컴퓨터 잠금을 해제할 때

-   설치된 원격 데스크톱 컴퓨터에 연결되는 UE-V.

-   동기화 컨트롤러 응용 프로그램 예약 작업이 실행된 경우

UE-V A와 컴퓨터 B에 설치하고 응용 프로그램에 대해 원하는 설정이 컴퓨터 A에 있는 경우 컴퓨터 A가 먼저 응용 프로그램을 열고 닫아야 합니다. 응용 프로그램을 먼저 컴퓨터 B에서 열고 닫은 경우 컴퓨터 A의 응용 프로그램 설정이 컴퓨터 B의 응용 프로그램 설정으로 구성됩니다. 설정 컴퓨터 간에 응용 프로그램 기반의 응용 프로그램 설정이 동기화됩니다. 시간이 지날 때 기본 설정으로 열고 닫을 때 컴퓨터 간에 설정이 일관되게 됩니다.

이 시나리오는 모든 설정에 Windows 적용됩니다. 컴퓨터 Windows 설정이 컴퓨터 A의 Windows 설정과 같아야 하는 경우 사용자가 먼저 컴퓨터 A에 로그온하고 로그오프해야 합니다.

사용자가 원하는 사용자 설정이 잘못된 순서로 적용된 경우 특정 응용 프로그램에 대해 복원 작업을 수행하거나 설정을 덮어 Windows 컴퓨터의 구성을 복구할 수 있습니다. 자세한 내용은 [Manage Administrative Backup and Restore in UE-V 2.x를 참조하십시오.](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

### <a name="performance-and-capacity-planning"></a><a href="" id="capacity"></a>성능 및 용량 계획

표준 디스크 용량 및 네트워크 상태 UE-V 요구 사항을 지정합니다.

UE-V SMB(서버 메시지 블록) 공유를 설정 패키지의 저장소에 사용합니다. 설정 패키지의 크기는 각 응용 프로그램의 설정 정보에 따라 다릅니다. 대부분의 설정 패키지는 작지만 데스크톱 이미지와 같은 잠재적으로 큰 파일을 동기화하면 성능이 저하될 수 있습니다( 특히 네트워크 속도가 느린 경우).

네트워크 대기 시간 문제를 줄이기 위해 사용자 컴퓨터가 있는 동일한 로컬 네트워크에서 설정 저장소 위치를 만드면 됩니다. 설정 저장 위치에 대해 사용자당 디스크 공간은 20MB인 것이 좋습니다.

기본적으로 UE-V 패키지로 인해 과도한 시간의 지형을 방지하기 위해 동기화가 2초 후에 시간도 1초가 지나지 않습니다. 그룹 정책 개체를 사용하여 SyncMethod=SyncProvider 설정을 [구성할 수 있습니다.](https://technet.microsoft.com/library/dn458893.aspx)

### <a name="high-availability-for-ue-v"></a><a href="" id="high"></a>고가용성 UE-V

이 UE-V 저장 위치 및 설정 템플릿 카탈로그는 모든 작성 가능한 공유에 사용자 데이터를 저장할 수 있도록 합니다. 고가용성을 보장하기 위해 다음 조건을 따르면 됩니다.

-   NTFS 파일 시스템을 통해 저장소 볼륨의 형식을 지정합니다.

-   공유는 DFS(분산 파일 시스템)를 사용할 수 있지만 제한이 있습니다.
특히 DFS-R(분산 파일 시스템 복제) DFS-N(분산 파일 시스템 네임스페이스)이 있는 단일 대상 구성이 지원됩니다.
마찬가지로 DFS-N에서는 단일 대상 구성만 지원됩니다.
자세한 내용은 [Microsoft의 복제된](https://go.microsoft.com/fwlink/p/?LinkId=313991) 사용자 프로필 데이터 관련 지원 설명 및 [DFS-R 및 DFS-N](https://support.microsoft.com/kb/2533009)배포 시나리오에 대한 Microsoft 지원 정책에 대한 정보를 참조하세요.

    또한 SYSVOL은 복제에 DFS-R을 사용하기 때문에 데이터 파일 복제에 SYSVOL을 UE-V 없습니다.

-   Deploying the 설정 Storage Location for UE-V 2.x에 지정된 공유 권한 및 NTFS ACL(액세스 [제어 목록)을 구성합니다.](https://technet.microsoft.com/library/dn458891.aspx#ssl)

-   파일 서버 클러스터링을 UE-V 에이전트와 함께 사용하여 통신 오류가 발생하면 사용자 상태 데이터의 복사본에 액세스할 수 있습니다.

-   클러스터된 공유, DFS-N 공유 또는 둘 다에 설정 저장소 경로 데이터(사용자 데이터) 및 설정 템플릿 카탈로그 템플릿을 저장할 수 있습니다.

### <a name="synchronize-computer-clocks-for-ue-v-settings-synchronization"></a><a href="" id="clocksync"></a>컴퓨터 시계를 동기화하여 UE-V 동기화

UE-V 실행되는 컴퓨터는 일관된 설정 환경을 유지 관리하기 위해 시간 서버를 사용해야 합니다. UE-V 타임스탬프를 사용하여 설정 저장소 위치에서 설정을 동기화해야 하는지 여부를 확인합니다. 컴퓨터 시계가 부정확하면 이전 설정으로 새 설정을 덮어치거나 새 설정을 설정 저장 위치에 저장하지 않을 수 있습니다.

## <a name="confirm-prerequisites-and-supported-configurations-for-ue-v"></a><a href="" id="prereqs"></a>구성에 대한 구성 및 지원되는 구성을 UE-V


계속하기 전에 사용자 환경에 이러한 요구 사항을 포함하는지 UE-V.

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
<td align="left"><p>.NET Framework 2.1의 경우 4.5 UE-V 이상입니다.</p>
<p>.NET Framework 2.0의 경우 UE-V 4 이상입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>표준, Enterprise, Datacenter 또는 웹 서버</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 2.1의 경우 4.5 UE-V 이상입니다.</p>
<p>.NET Framework 2.0의 경우 UE-V 4 이상입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 Windows 8.1</p></td>
<td align="left"><p>Enterprise Pro</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, 1607 이전 버전</p>
<div class="alert">
<strong>참고</strong><br/><p>2.1 SP1 UE-V 1607 이전 Windows 10 지원</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise Pro</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 Windows Server 2012 R2</p></td>
<td align="left"><p>Standard 또는 Datacenter</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard 또는 Datacenter</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.6 이상</p></td>
</tr>
</tbody>
</table>



또한...

-   **MDOP 라이선스:** 이 기술은 MDOP(Microsoft Desktop Optimization Pack)의 일부입니다. Enterprise 사용하여 MDOP를 얻을 수 Microsoft Software Assurance. MDOP를 Microsoft Software Assurance 방법에 대한 자세한 내용은 How Do I Get MDOP ( 을 https://go.microsoft.com/fwlink/p/?LinkId=322049) 참조하세요.

-   **설치할** 컴퓨터의 관리 자격 증명

**참고**  

-   WIndows 10 버전 1607부터 UE-V 업데이트는 Windows 10 [](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) Enterprise Microsoft 데스크톱 최적화 팩에 더 이상 포함되어 있지 않습니다.

-   UE-V Windows PowerShell 에이전트의 UE-V 기능을 사용하려면 .NET Framework 4 이상 Windows PowerShell 3.0 이상이 필요합니다. 여기에서 Windows PowerShell 3.0을 [다운로드합니다.](https://go.microsoft.com/fwlink/?LinkId=309609)

-   .NET Framework 7 또는 .NET Framework Windows Server 2008 R2 운영 체제를 실행하고 있는 컴퓨터에 Windows 4 또는 Windows 4.5를 설치합니다. Windows 8, Windows 8.1 및 Windows Server 2012 운영 체제에는 .NET Framework 4.5가 함께 설치됩니다. Windows 10 운영 체제는 .NET Framework 4.6과 함께 제공합니다.
-   필수 프로필에 대한 "로밍 캐시 삭제" 정책은 UE-V 사용할 수 없습니다.



특정 RAM(임의 액세스 메모리) 요구 사항은 UE-V.

### <a name="synchronization-of-settings-through-the-sync-provider"></a>동기화 공급자를 설정 동기화

동기화 공급자는 로컬 캐시를 이러한 인스턴스의 설정 저장소 위치와 동기화하는 사용자의 기본 설정입니다.

-   로그온/로그오프

-   잠금/잠금 해제

-   원격 데스크톱 연결/연결 끊기

-   응용 프로그램 열기/닫기

예약된 작업은 30분마다 또는 특정 응용 프로그램에 대한 특정 트리거 이벤트를 통해 이러한 설정 동기화를 관리합니다. 자세한 내용은 [Changing the Frequency of UE-V 2.x Scheduled Tasks을 참조하십시오.](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

UE-V 에이전트는 항상 엔터프라이즈 네트워크에 연결되어 있지 않은 컴퓨터(원격 컴퓨터 및 랩톱)와 네트워크에 연결된 컴퓨터(Windows Server를 실행하고 VDI(가상 데스크톱 인터페이스) 세션을 호스트하는 컴퓨터)에 대한 사용자 설정을 동기화합니다.

항상 사용 가능한 연결을 **사용하는 컴퓨터의 동기화:** 항상 네트워크에 UE-V 컴퓨터에서 UE-V 경우 설정 저장소 서버를 표준 네트워크 공유로 취급하는 *SyncMethod=None* 매개 변수를 사용하여 설정을 동기화하도록 UE-V Agent를 구성해야 합니다. 이 구성에서는 응용 UE-V 가져오기 지연을 알리도록 에이전트를 구성할 수 있습니다.

다음 방법 중 하나를 통해 이 구성을 사용하도록 설정할 수 있습니다.

-   설치 UE-V 명령 프롬프트 또는 배치 파일에서 AgentSetup.exe 매개 변수 *SyncMethod = 없음을 설정하십시오.* [2.UE-V 배포하면](https://technet.microsoft.com/library/dn458891.aspx#agent) 자세한 정보를 제공합니다.

-   UE-V 설치한 후 System Center 2012 Configuration Manager의 설정 관리 기능 또는 MDOP ADMX 템플릿을 사용하여 *SyncMethod = None* 구성을 푸시합니다.

-   WMI(Windows PowerShell 또는 Windows)를 사용하여 *SyncMethod = None 구성을* 설정할 수 있습니다.

    **참고**  
    이러한 마지막 두 방법은 풀된 VDI(가상 데스크톱 인프라) 환경에서는 작동하지 않습니다.



설정을 동기화하기 전에 컴퓨터를 다시 시작해야 합니다.

**참고**  
*SyncMethod = None 을*설정하면 설정 변경 내용이 서버에 직접 저장됩니다. 설정 저장소 경로에 대한 네트워크 연결을 찾을 수 없는 경우 설정 변경 내용이 장치에 캐시된 후 다음에 동기화 공급자가 실행될 때 동기화됩니다. 설정 저장 경로를 찾을 수 없는 경우 로그온 시 풀된 VDI 환경에서 사용자 프로필이 제거되면 설정 변경 내용이 손실되고 사용자가 설정을 저장 경로에 다시 연결할 때 변경 내용을 다시 적용해야 합니다.



**외부 동기화 엔진에 대한 동기화:** *SyncMethod=External* 매개 변수는 UE-V 설정을 사용자 컴퓨터의 로컬 폴더에 기록하는 경우 사용자가 액세스하는 다른 컴퓨터에 이러한 설정을 적용하는 데 비즈니스용 OneDrive, 클라우드 폴더, Sharepoint 또는 Dropbox 등의 외부 동기화 엔진을 사용할 수 있도록 지정합니다.

**공유 VDI** 세션 지원: UE-V 2.1 및 2.1 SP1에서는 최종 사용자와 공유되는 VDI 세션을 지원할 수 있습니다. 특수 VDI 템플릿을 등록하고 구성할 수 있으며, 이 템플릿을 사용하면 비영구 VDI UE-V 모든 기능을 그대로 유지할 수 있습니다.

**참고**  
비영구적 VDI 세션에 대해 VDI 모드를 사용하도록 설정하지 않은 경우 백업/복원 및 마지막으로 알려진 [양호(LKG)](https://technet.microsoft.com/library/dn878331.aspx)등의 특정 기능이 작동하지 않습니다.



VDI 템플릿은 UE-V 2.1 및 2.1 SP1과 함께 제공되어 설치 후 일반적으로 C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml

### <a name="prerequisites-for-ue-v-generator-support"></a>UE-V 생성기 지원에 대한 선행 준비

사용자 UE-V 설정 위치 템플릿을 만드는 데 사용되는 컴퓨터에 UE-V 생성기를 설치합니다. 이 컴퓨터는 설정이 동기화된 응용 프로그램을 실행할 수 있습니다. UE-V 생성기 소프트웨어를 실행하고 있는 컴퓨터에서 Administrators 그룹의 구성원이 되어야 합니다.

NTFS UE-V 사용하는 컴퓨터에 설치해야 합니다. UE-V 생성기 소프트웨어를 사용하려면 .NET Framework 4가 필요합니다. 자세한 내용은 [Deploy UE-V 2.x for Custom Applications를 참조하십시오.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

## <a name="other-resources-for-this-product"></a>이 제품에 대한 기타 리소스


-   [Microsoft User Experience Virtualization(UE-V) 2.x](index.md)

-   [UE-V 2.x 시작](get-started-with-ue-v-2x-new-uevv2.md)

-   [2.UE-V 관리](administering-ue-v-2x-new-uevv2.md)

-   [2.UE-V 문제 해결](troubleshooting-ue-v-2x-both-uevv2.md)

-   [UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)














