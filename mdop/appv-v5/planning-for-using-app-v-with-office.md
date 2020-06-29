---
title: Office와 App-V 사용 계획
description: Office와 App-V 사용 계획
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813425"
---
# Office와 App-V 사용 계획


다음 정보를 사용 하 여 App-v를 사용 하 여 Office를 배포 하는 방법을 계획 합니다. 이 문서에는 다음이 포함 됩니다.

-   [앱-V 언어 팩에 대 한 지원](#bkmk-lang-pack)

-   [지원 되는 Microsoft Office 버전](#bkmk-office-vers-supp-appv)

-   [동시 버전의 Office를 사용 하 여 App-v 사용 계획](#bkmk-plan-coexisting)

-   [Office를 배포 하는 데 앱을 배포할 때 Office가 Windows와 통합 되는 방식](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>앱-V 언어 팩에 대 한 지원


앱-V 5.0 시퀀서를 사용 하 여 언어 팩, 언어 인터페이스 팩, 교정 도구 및 화면 설명 언어에 대 한 플러그 인 패키지를 만들 수 있습니다. 그런 다음 Office 배포 도구 키트를 사용 하 여 만드는 Office 2013 패키지와 함께 연결 그룹에 플러그 인 패키지를 포함할 수 있습니다. Office 응용 프로그램 및 플러그 인 언어 팩은 연결 그룹에서 함께 그룹화 되는 다른 모든 패키지와 마찬가지로 같은 연결 그룹에서 원활 하 게 상호 작용 합니다.

**참고**  Microsoft Visio 및 Microsoft Project에서는 태국어 언어 팩을 지원 하지 않습니다.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>지원 되는 Microsoft Office 버전


다음 표에는 앱-V가 지 원하는 Microsoft Office 버전, Office 패키지 만들기 방법, 지원 되는 라이선스, 지원 되는 배포 목록이 나와 있습니다.

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
<th align="left">지원 되는 Office 버전</th>
<th align="left">지원 되는 App-v 버전</th>
<th align="left">패키지 만들기</th>
<th align="left">지원 되는 라이선스</th>
<th align="left">지원 되는 배포</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>엔터프라이즈 용 Microsoft 365 앱</p>
<p>지원 되는 항목:</p>
<ul>
<li><p>Visio Pro for Office 365</p></li>
<li><p>Project Pro for Office 365</p></li>
</ul></td>
<td align="left"><ul>
<li><p>App-V 5.0</p></li>
<li><p>App-v 5.0 SP1</p></li>
<li><p>App-v 5.0 SP2</p></li>
</ul></td>
<td align="left"><p>Office 배포 도구</p></td>
<td align="left"><p>구독</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>개인 VDI</p></li>
<li><p>풀링된 VDI</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Office Professional Plus 2013</p>
<p>지원 되는 항목:</p>
<ul>
<li><p>Visio Professional 2013</p></li>
<li><p>Project Professional 2013</p></li>
</ul></td>
<td align="left"><ul>
<li><p>App-V 5.0</p></li>
<li><p>App-v 5.0 SP1</p></li>
<li><p>App-v 5.0 SP2</p></li>
</ul></td>
<td align="left"><p>Office 배포 도구</p></td>
<td align="left"><p>볼륨 라이선스</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>개인 VDI</p></li>
<li><p>풀링된 VDI</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a>동시 버전의 Office를 사용 하 여 App-v 사용 계획


"Microsoft Office 공존"을 사용 하 여 같은 컴퓨터에 두 가지 버전의 Microsoft Office를 함께 설치할 수 있습니다. Windows Installer 기반 (MSi) 버전의 Office, 간편 실행, App-v 5.0 SP2를 사용 하 여 모든 주요 버전의 Office 및 설치 방법을 비롯 한 office 공존을 구현할 수 있습니다. 그러나 Microsoft는 Office 공존을 사용 하지 않는 것이 좋습니다.

Microsoft의 권장 가장 좋은 방법은 호환성 문제를 방지 하기 위해 Office 공존을 완전히 방지 하는 것입니다. 그러나 최신 버전의 Office로 마이그레이션하는 경우에는 즉시 해결할 수 없는 문제가 발생할 수 있으므로, 최신 제품 버전으로 더 빠른 마이그레이션을 위해 동시 사용을 일시적으로 구현 하는 것이 좋습니다. 장기간에 Office 공존을 사용 하는 것은 바람직하지 않으며 조직에는 향후에 완벽 하 게 전환 하는 계획이 있어야 합니다.

### Office 공존을 구현 하기 전에

Office 공존을 구현 하기 전에 다음 Office 문서를 검토 하세요. 공존을 구현 하려는 최신 버전의 Office에 해당 하는 문서를 선택 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Office 버전</th>
<th align="left">지침 링크</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">다른 버전의 Office를 실행 하는 컴퓨터에서 Office 2013 도구 모음 및 프로그램 (MSI 배포)을 사용 하는 방법에 대 한 정보</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">다른 버전의 Office를 실행 하는 컴퓨터에서 Office 2010 제품군 및 프로그램을 사용 하는 방법에 대 한 정보</a></p></td>
</tr>
</tbody>
</table>

 

Office 설명서는 Windows Installer 기반 (MSi) 및 간편 실행 설치에 대 한 광범위 한 지침을 제공 합니다. 공존에 대 한이 App-v 항목은 App-v 배포와 관련 된 정보를 사용 하 여 Office 지침을 보완 합니다.

### 지원 되는 Office 공존 시나리오

다음 표에는 지원 되는 공존 시나리오가 요약 되어 있습니다. 이는 현재 사용 중인 버전 및 배포 방법과 마이그레이션하는 버전 및 배포 방법에 따라 구성 됩니다. 프로덕션 청중에 게 배포 하기 전에 모든 공존 솔루션을 철저히 테스트 해야 합니다.

**참고**  Microsoft는 원격 데스크톱 세션 호스트 역할 서비스를 사용 하도록 설정한 Windows Server 환경에서 여러 버전의 Office를 사용 하는 것을 지원 하지 않습니다. Office 공존 시나리오를 실행 하려면이 역할 서비스를 사용 하지 않도록 설정 해야 합니다.

 

### Windows 통합 & Office 공존

Windows Installer 기반 및 간편 실행 Office 설치 방법은 기본 Windows 운영 체제의 특정 지점과 통합 됩니다. 공존을 사용 하는 경우 두 Office 버전 간의 일반적인 운영 체제 통합이 충돌할 수 있으며,이 경우 호환성 및 사용자 경험 문제가 발생 합니다. App-v를 사용 하 여 특정 버전의 Office를 시퀀싱 하 여 통합을 제외 하 여 운영 체제에서 "격리" 할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">App-v가이 버전의 Office를 시퀀싱 할 수 있는 모드</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>항상 비 통합. App-v는 가상화 된 버전의 Office 2007와의 운영 체제 통합을 제공 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>통합 및 통합 되지 않음 모드.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>항상 통합 됩니다. Windows 운영 체제 통합은 사용 하지 않도록 설정할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

Microsoft는 통합 된 Office 인스턴스 하나로 Office 공존을 배포 하는 것이 좋습니다. 예를 들어 App-v를 사용 하 여 Office 2010 및 Office 2013을 배포 하는 경우 Office 2010을 통합 되지 않은 모드로 전환 해야 합니다. 통합 되지 않은 (격리 된) 모드에서의 Office 시퀀싱에 대 한 자세한 내용은 [Microsoft Application Virtualization 5.0에서 Microsoft Office 2010의 순서를 만드는 방법을](https://support.microsoft.com/kb/2830069)참조 하세요.

### Office 공존 시나리오의 알려진 제한 사항

다음 섹션에서는 Office와 함께 공존을 구현 하는 데 App-v를 사용할 때 발생할 수 있는 몇 가지 문제에 대해 설명 합니다.

### Windows Installer 기반/간편 실행 및 App-v Office 공존 시나리오에 공통적으로 적용 되는 제한 사항

동일한 컴퓨터에 다음 버전의 Office를 설치 하는 경우 다음과 같은 제한이 발생할 수 있습니다.

-   Windows Installer 기반 버전을 사용 하 여 Office 2010

-   Office 2013-V 앱 사용

이전 버전의 Windows Installer 기반 Office 2010과 함께 app-v를 사용 하 여 Office 2013을 게시 한 후에도 Windows Installer가 시작 될 수 있습니다. 이는 Windows Installer 기반 또는 간편 실행 버전의 Office 2010가 자동으로 컴퓨터에 등록 하려고 하기 때문입니다.

기본 Word 2010에 대 한 자동 등록 작업을 무시 하려면 다음 단계를 따르세요.

1.  Word 2010을 종료 합니다.

2.  다음을 실행 하 여 레지스트리 편집기를 시작 합니다.

    -   Windows 7: **시작**을 클릭 하 고 검색 시작 상자에 **regedit** 를 입력 한 다음 enter 키를 누릅니다.

    -   Windows 8에서 **regedit** 를 입력 하 고 시작 페이지에서 enter 키를 누른 다음 enter 키를 누릅니다.

    관리자 암호나 확인을 요청 하는 메시지가 표시 되 면 암호를 입력 하거나 **계속**을 클릭 합니다.

3.  다음 레지스트리 하위 키를 찾아 선택 합니다.

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  **편집** 메뉴에서 **새로 만들기**를 클릭 한 다음 **DWORD 값**을 클릭 합니다.

5.  없음/ **예**를 입력 하 고 enter 키를 누릅니다.

6.  없음을 마우스 오른쪽 **단추로 클릭 한** 다음 **수정을**클릭 합니다.

7.  **Valuedata** 상자에 **1**을 입력 한 다음 **확인**을 클릭 합니다.

8.  파일 메뉴에서 **끝내기** 를 클릭 하 여 레지스트리 편집기를 닫습니다.

## <a href="" id="bkmk-office-integration-win"></a>App-v를 사용 하 여 Office를 배포할 때 Office와 Windows가 통합 되는 방식


App-v를 사용 하 여 Office 2013를 배포 하는 경우 office가 App-v 없이 배포 될 때 office의 기능 및 기능을 최종 사용자에 게 제공 하는 운영 체제와 완벽 하 게 통합 됩니다.

Office 2013 App-v 패키지는 Windows 운영 체제와 함께 다음과 같은 통합 지점을 지원 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">확장점</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Firefox 및 Chrome 용 Lync 모임 참가 플러그 인</p></td>
<td align="left"><p>사용자가 Firefox 및 Chrome에서 Lync 모임에 참가할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OneNote 인쇄 드라이버로 전송 됨</p></td>
<td align="left"><p>사용자가 OneNote에 인쇄할 수 있음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OneNote에 연결 된 노트</p></td>
<td align="left"><p>OneNote에 연결 된 노트</p></td>
</tr>
<tr class="even">
<td align="left"><p>OneNote Internet Explorer 추가 기능으로 보내기</p></td>
<td align="left"><p>IE에서 OneNote로 보낼 수 있는 사용자</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Lync 및 Outlook에 대 한 방화벽 예외</p></td>
<td align="left"><p>Lync 및 Outlook에 대 한 방화벽 예외</p></td>
</tr>
<tr class="even">
<td align="left"><p>MAPI 클라이언트</p></td>
<td align="left"><p>기본 앱과 추가 기능은 MAPI를 통해 가상 Outlook과 상호 작용할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Firefox 용 SharePoint 플러그 인</p></td>
<td align="left"><p>사용자가 Firefox에서 SharePoint 기능을 사용할 수 있음</p></td>
</tr>
<tr class="even">
<td align="left"><p>메일 제어판 애플릿</p></td>
<td align="left"><p>사용자가 Outlook의 메일 제어판 애플릿을 가져옵니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>기본 Interop 어셈블리</p></td>
<td align="left"><p>관리 되는 추가 기능 지원</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 문서 캐시 처리기</p></td>
<td align="left"><p>Office 응용 프로그램에 대해 문서 캐시를 허용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outlook 프로토콜 검색 처리기</p></td>
<td align="left"><p>사용자가 outlook에서 검색할 수 있음</p></td>
</tr>
<tr class="even">
<td align="left"><p>Active X 컨트롤:</p></td>
<td align="left"><p>ActiveX 컨트롤에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> Activex 컨트롤 API 참조를 참조 </a> 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SiteClient</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Sharepoint. OpenXMLDocuments</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Sharepoint. ClipboardCtl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   이 (가) Copysud.</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx 관리자</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Active X 컨트롤</p></td>
</tr>
<tr class="even">
<td align="left"><p>   OneDrive Pro 브라우저 도우미</p></td>
<td align="left"><p>Active X Control]</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OneDrive Pro 아이콘 오버레이</p></td>
<td align="left"><p>사용자가 폴더를 찾을 때 Windows 탐색기 셸 아이콘 오버레이 (OneDrive Pro 폴더)</p></td>
</tr>
<tr class="even">
<td align="left"><p>셸 확장</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>정의</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 검색</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





