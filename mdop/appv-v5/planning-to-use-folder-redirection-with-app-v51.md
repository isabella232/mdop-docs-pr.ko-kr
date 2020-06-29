---
title: App-V로 폴더 리디렉션 사용 계획
description: App-V로 폴더 리디렉션 사용 계획
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813385"
---
# App-V로 폴더 리디렉션 사용 계획


Microsoft App-v (Application Virtualization) 5.1는 사용자 및 관리자가 폴더 경로를 새 위치로 리디렉션할 수 있는 기능인 폴더 리디렉션 사용을 지원 합니다.

이 항목의 섹션:

-   [폴더 리디렉션 사용에 대 한 요구 사항](#bkmk-folder-redir-reqs)

-   [앱과 함께 사용 하도록 폴더 리디렉션을 구성 하는 방법-V](#bkmk-folder-redir-cfg)

-   [App-V에서 폴더 리디렉션이 작동 하는 방식](#bkmk-folder-redir-works)

-   [폴더 리디렉션 개요](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>폴더 리디렉션 사용을 위한 요구 사항 및 지원 되지 않는 시나리오


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>요구 사항</p></td>
<td align="left"><p>% AppData% 폴더 리디렉션을 사용 하려면 다음을 수행 해야 합니다.</p>
<ul>
<li><p>AppData 가상 파일 시스템 (VFS) 폴더가 있는 App-v 패키지를 사용 합니다.</p></li>
<li><p>폴더 리디렉션을 사용 하도록 설정 하 고 사용자의 폴더를 공유 폴더 (일반적으로 네트워크 폴더)로 리디렉션합니다.</p></li>
<li><p>다음 두 가지 모두 또는 모두 로밍:</p>
<ul>
<li><p>%Appdata%\Microsoft\AppV\Client\Catalog 아래에 있는 파일</p></li>
<li><p>HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages의 레지스트리 설정</p>
<p>자세한 내용은 <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> 응용 프로그램 게시 및 클라이언트 조작을 참조 하세요 </a> .</p></li>
</ul></li>
<li><p>App-v 5.0 SP2 이상 클라이언트를 실행 하는 컴퓨터에 로그인 하는 각 사용자가 다음 폴더를 사용할 수 있는지 확인 합니다.</p>
<ul>
<li><p>% AppData%가 원하는 네트워크 위치로 구성 되어 <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> 있습니다 (오프 라인 파일 지원 여부에 관계 없이 </a> ).</p></li>
<li><p>% LocalAppData%가 원하는 로컬 폴더로 구성 되었습니다.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>지원되지 않는 시나리오</p></td>
<td align="left"><ul>
<li><p>% LocalAppData%을 (를) 네트워크 드라이브로 구성 하 고 있습니다.</p></li>
<li><p>여러 사용자를 위해 시작 메뉴를 단일 폴더로 리디렉션합니다.</p></li>
<li><p>로밍 AppData (% AppData%) 이 (가) 사용할 수 없는 네트워크 공유로 리디렉션 되었습니다. 앱 V 응용 프로그램은 다음과 같이 실행 되지 않습니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 버전</th>
<th align="left">시나리오 설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>앱-V 5.0 SP2 plus 핫픽스를 통해 app-v 5.0</p></td>
<td align="left"><p>이 오류는 오프 라인 파일을 사용할 수 있는지 여부에 관계 없이 발생 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 5.0 SP3 이상</p></td>
<td align="left"><p>사용할 수 없는 네트워크 공유가 오프 라인 파일에 대해 사용 하도록 설정 된 경우 App-v 응용 프로그램이 성공적으로 시작 됩니다.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>앱과 함께 사용 하도록 폴더 리디렉션을 구성 하는 방법-V


폴더 리디렉션은 데스크톱, 내 문서, 내 사진 등의 다른 폴더에 적용할 수 있습니다. 그러나 앱 V 응용 프로그램 사용에 영향을 주는 유일한 폴더는 사용자의 로밍 AppData 폴더 (% AppData%)입니다. 앱-V에 영향을 주지 않고 폴더 리디렉션을 지원 되는 다른 모든 폴더에 적용할 수 있습니다.

## <a href="" id="bkmk-folder-redir-works"></a>App-V에서 폴더 리디렉션이 작동 하는 방식


다음 표에서 는% AppData%가 네트워크로 리디렉션되는 경우와이 문서의 앞 부분에 나열 된 요구 사항을 충족 하는 경우 폴더 리디렉션이 작동 하는 방식을 설명 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">가상 환경 상태</th>
<th align="left">발생 하는 작업</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>가상 환경이 시작 되는 경우</p></td>
<td align="left"><p>VFS (가상 파일 시스템) AppData 폴더는 로컬 AppData 폴더 (% LocalAppData%)에 매핑됩니다. 사용자의 로밍 AppData 폴더 (% AppData%)를 사용 하지 않습니다.</p>
<ul>
<li><p>LocalAppData에는 사용 중인 패키지에 대 한 사용자 로밍 AppData 폴더의 로컬 캐시가 포함 되어 있습니다. 로컬 캐시의 위치는 다음과 같습니다.</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>사용자의 로밍 AppData 폴더에서 최신 데이터를 복사 하 여 현재 로컬 캐시에 있는 데이터에 바꿉니다.</p></li>
<li><p>가상 환경이 실행 되는 동안에는 데이터가 계속 로컬 캐시에 저장 됩니다. 데이터 는% LocalAppData% 밖에만 제공 되며, 최종 사용자가 컴퓨터를 종료할 때 까지% AppData%로 이동 하거나 동기화 할 수 없습니다.</p></li>
<li><p>AppData 폴더에 대 한 항목은 시스템 컨텍스트가 아닌 사용자 컨텍스트를 사용 하 여 만들어집니다.</p></li>
</ul>
<div class="alert">
<strong>참고</strong><br/><p>App-v 클라이언트 폴더 리디렉션은 파일 을% AppData% 에서% LocalAppData%까지 이동 하지 못하는 경우가 있습니다. <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">앱-V 5.0 SP2에 대 한 릴리스 정보를 참조 하세요 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>가상 환경이 종료 되는 경우</p></td>
<td align="left"><p>AppData (로밍)의 로컬 캐시 된 데이터가 압축 되 고 "실제" 로밍 AppData 폴더 (% AppData%)에 복사 됩니다. 마지막으로 알려진 업로드가 표시 된 타임 스탬프는 다음의 레지스트리 키로 동시에 저장 됩니다.</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>중복성을 제공 하기 위해 App-v는 압축 된 데이터의 가장 최근 복사본 3 개 를% AppData%로 유지 합니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>폴더 리디렉션 개요


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>목적</p></td>
<td align="left"><p>로컬 드라이브에 파일이 있는 것 처럼 최종 사용자가 다른 폴더로 리디렉션되는 파일로 작업할 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설명</p></td>
<td align="left"><p>폴더 리디렉션을 통해 사용자와 관리자는 폴더의 경로를 네트워크 위치로 리디렉션할 수 있습니다. 폴더의 문서는 네트워크의 모든 컴퓨터에서 사용자가 사용할 수 있습니다.</p>
<ul>
<li><p>폴더 리디렉션을 통해 사용자와 관리자는 폴더의 경로를 네트워크 위치로 리디렉션할 수 있습니다. 폴더의 문서는 네트워크의 모든 컴퓨터에서 사용자가 사용할 수 있습니다.</p></li>
<li><p>새 위치는 로컬 컴퓨터의 폴더 이거나 공유 네트워크의 폴더 일 수 있습니다.</p></li>
<li><p>폴더 리디렉션은 파일을 즉시 업데이트 하는 반면, 로밍 데이터는 일반적으로 사용자가 로그인 하거나 로그 오프할 때 동기화 됩니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>사용 예제</p></td>
<td align="left"><p>일반적으로 컴퓨터&#39;s 로컬 하드 디스크에 저장 된 문서 폴더를 네트워크 위치에 리디렉션할 수 있습니다. 사용자는 네트워크의 모든 컴퓨터에서 폴더의 문서에 액세스할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>추가 리소스</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">폴더 리디렉션 개요</a></p></td>
</tr>
</tbody>
</table>
















