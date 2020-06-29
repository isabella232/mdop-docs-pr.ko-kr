---
title: Application Virtualization 5.1에 대한 성능 지침
description: Application Virtualization 5.1에 대한 성능 지침
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813521"
---
# Application Virtualization 5.1에 대한 성능 지침


최적화 된 성능을 위해 App-v 5.1를 구성 하는 방법과 가상 앱 패키지를 최적화 하 고 RDS 및 VDI에서 더 나은 사용자 환경을 제공 하는 방법을 알아봅니다.

여러 메서드를 구현 하면 최종 사용자 환경을 개선 하는 데 도움이 될 수 있습니다. 그러나 환경에서 일부 메서드를 지원 하지 않을 수 있습니다.

이 문서를 읽기 전에 다음 정보를 읽고 이해 해야 합니다.

-   [Microsoft Application Virtualization 5.1 관리자 가이드](microsoft-application-virtualization-51-administrators-guide.md)

-   [앱-V 5 SP2 응용 프로그램 게시 및 클라이언트 조작](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [Microsoft Application Virtualization 시퀀싱 가이드](https://go.microsoft.com/fwlink/?LinkId=269953)

**참고**  
이 문서에서 사용 되는 일부 용어는 외부 원본 및 컨텍스트에 따라 의미가 다를 수 있습니다. 이 문서에 사용 된 용어에 대 한 자세한 내용을 보려면 **\\** 이 문서의 " [Application Virtualization 성능 지침 용어](#bkmk-terms1) " 섹션을 참조 하세요.



마지막으로이 문서는 앱-V 5.1 클라이언트를 실행 하는 컴퓨터와 최적의 성능을 위한 환경을 구성 하는 정보를 제공 합니다. Sequencer를 사용 하 여 성능을 위해 가상 응용 프로그램 패키지를 최적화 하 고, RDS (원격 데스크톱 서비스) 및 VDI (비영구 가상 데스크톱 인프라)에서 앱-V 5.1을 사용 하 여 최적의 사용자 환경을 제공 하는 방법에 대해 설명 합니다.

해당 환경과 관련 된 정보를 확인 하려면 각 섹션의 간략 한 개요 및 적응성 검사 목록을 검토 해야 합니다.

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> 앱-V 5.1의 상태 저장 \ * 비 영구적인 배포


이 섹션에서는 사용자가 로그인 한 후 몇 초 이내에 모든 가상 응용 프로그램에 액세스할 수 있도록 하는 접근 방법에 대 한 정보를 제공 합니다. 이는 자주 실행 되는 앱-V 5.1 게시 새로 고침을 고유 하 게 처리 하 여 달성할 수 있습니다. 접근 방식에 대 한 기본 사항은 빠른 게시 새로 고침 이지만 실제로는 아무런 작업도 수행 하지 않는 것입니다. 최상의 사용자 환경을 제공 하기 위해서는 여러 조건을 충족 해야 하며 단계를 따라야 합니다.

자세한 내용은 다음 섹션의 정보를 사용 하세요.

[사용 시나리오](#bkmk-us) -두 시나리오를 검토할 때이 방법이 extremes 것을 염두에 두어야 합니다. 사용 요구 사항에 따라 사용자 및/또는 가상 응용 프로그램 패키지의 하위 집합에 이러한 단계를 적용 하도록 선택할 수 있습니다.

-   성능 최적화 – 최상의 환경을 제공 하기 위해 기본 이미지에 App-v 가상 응용 프로그램 패키지 중 일부를 포함할 수 있습니다. 이 및 기타 요구 사항이 논의 됩니다.

-   저장소에 최적화 됨 – 저장소 영향이 염려 되는 경우이 시나리오에 따라 이러한 문제를 해결할 수 있습니다.

[환경 준비](#bkmk-pe)

-   비 영구적인 VDI 또는 RDSH 환경에서 기본 이미지를 준비 하는 단계에서는이 방법을 사용 하려면 기본 이미지에서 몇 단계만 완료 해야 합니다.

-   2.1 UE-V (사용자 프로필 관리) 솔루션의 UPM (cornerstone 접근 권한)을 사용 하는 경우에는이 접근 방식으로 몇 가지 레지스트리와 파일 위치의 콘텐츠를 유지 하는 UEM 솔루션이 있습니다. 이러한 위치는 사용자 통합 \ *를 구성 합니다. UPM 솔루션에 대 한 특정 요구 사항을 검토 하세요.

[사용자 환경 실습](#bkmk-uewt)

-   실습 – App-v 및 UE-V 작업을 단계별로 진행 하 고 사용자에 게 기대 되는 예측 사항입니다.

-   결과 – 예상 결과를 설명 합니다.

[패키지 수명 주기에 미치는 영향](#bkmk-plc)

[성능 최적화/조정을 통해 VDI 환경 개선](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a>적응성 검사 목록

배포 환경

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>비 영구적인 VDI 또는 RDSH.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>UE-V (사용자 환경 가상화), 기타 UPM 솔루션 또는 사용자 프로필 디스크 (UPD).</p></td>
</tr>
</tbody>
</table>



예상 되는 구성

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>앱-V 사용자 상태 템플릿을 사용 하거나 UPM (사용자 프로필 관리) 소프트웨어가 있는 UE-V (user Experience Virtualization) 비 UE-V UPM 소프트웨어는 로그인 또는 프로세스/응용 프로그램 시작 및 로그 오프에서 트리거할 수 있어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>앱-V 공유 콘텐츠 저장소 (SCS)를 구성 하거나 구성할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



IT 관리

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>최적의 성능을 유지 하기 위해 관리자는 VM 기본 이미지를 정기적으로 업데이트 해야 하며, 관리자는 여러 사용자 그룹에 대해 다양 한 이미지를 관리 해야 할 수 있습니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a>사용 시나리오

두 가지 시나리오를 검토 하는 동안에는 이러한 방식으로 extremes을 염두에 두어야 합니다. 사용 요구 사항에 따라 사용자, 가상 응용 프로그램 패키지 또는 둘 다의 하위 집합에 이러한 단계를 적용 하도록 선택할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">성능 최적화</th>
<th align="left">저장소에 최적화 됨</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>최적화 된 사용자 환경을 제공 하기 위해이 접근 방식은 UPM 솔루션의 기능을 활용 하 고 추가 이미지 준비를 수행 하며 추가 이미지 관리 오버 헤드를 유발할 수 있습니다.</p>
<p>다음은 상태 저장 비 영구적인 배포의 다양 한 성능 개선 사항에 대 한 설명입니다. 자세한 내용은 <strong> </strong> <strong> </strong> <strong> 이 문서의 참고 항목 섹션에 있는 </strong> 게시 성능에 대 한 패키지 최적화 및 app-v 시퀀싱 가이드에 대 한 참조를 참조 하세요.</p></td>
<td align="left"><p>이전 시나리오의 일반적인 기대는 계속 해 서 적용 됩니다. 그러나 일반적으로 VM 이미지는 매우 비용이 많이 드는 배열에 저장 된다는 점에 유의 하세요. 접근 방식이 약간 변경 되었습니다. 기본 이미지에서 사용자가 대상으로 하는 가상 응용 프로그램 패키지를 미리 구성 하지 마세요.</p>
<p>이러한 변경으로 인 한 영향은이 문서의 사용자 환경 연습 섹션에 자세히 설명 되어 있습니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a>환경 준비

다음 표에는 기본 이미지와 접근 방법에 대 한 UE-V 또는 다른 UPM 솔루션을 준비 하는 데 필요한 단계가 표시 되어 있습니다.

**기본 이미지 준비**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">성능 최적화</th>
<th align="left">저장소에 최적화 됨</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>클라이언트의 App-v 5.1 클라이언트 버전을 설치 합니다.</p></li>
<li><p>UE-V를 설치 하 고 UE-V 템플릿 갤러리에서 앱-V 설정 서식 파일을 다운로드 하려면 다음 단계를 참조 하세요.</p></li>
<li><p>SCS (공유 콘텐츠 저장소) 모드를 구성 합니다. 자세한 내용은 <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> 공유 콘텐츠 저장소 모드 용 app-v 5.1 클라이언트를 설치 하는 방법을 참조 하세요 </a> .</p></li>
<li><p>로그인 레지스트리 DWORD에 사용자 통합 유지를 구성 합니다.</p></li>
<li><p>모든 사용자 및 전역 대상 패키지 (예: <strong> Add-AppvClientPackage를 미리 구성 </strong> 합니다.</p></li>
<li><p>모든 사용자 및 전역 대상 연결 그룹 (예: <strong> Add-AppvClientConnectionGroup을 미리 구성 </strong> 합니다.</p></li>
<li><p>모든 전역 대상 패키지를 미리 게시 합니다.</p>
<p></p>
<p>반대로</p>
<ul>
<li><p>전역 게시/새로 고침을 수행 합니다.</p></li>
<li><p>사용자 게시/새로 고침을 수행 합니다.</p></li>
<li><p>모든 사용자 대상 패키지의 게시를 취소 합니다.</p></li>
<li><p>다음 사용자의 VFS (가상 파일 시스템) 항목을 삭제 합니다.</p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>클라이언트의 App-v 5.1 클라이언트 버전을 설치 합니다.</p></li>
<li><p>UE-V를 설치 하 고 UE-V 템플릿 갤러리에서 앱-V 설정 서식 파일을 다운로드 하려면 다음 단계를 참조 하세요.</p></li>
<li><p>SCS (공유 콘텐츠 저장소) 모드를 구성 합니다. 자세한 내용은 <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> 공유 콘텐츠 저장소 모드 용 app-v 5.1 클라이언트를 설치 하는 방법을 참조 하세요 </a> .</p></li>
<li><p>로그인 레지스트리 DWORD에 사용자 통합 유지를 구성 합니다.</p></li>
<li><p>모든 전역 대상 패키지를 미리 구성 합니다 (예: <strong> Add-AppvClientPackage) </strong> .</p></li>
<li><p>모든 전역 대상 연결 그룹 (예: <strong> Add-AppvClientConnectionGroup을 미리 구성 </strong> 합니다.</p></li>
<li><p>모든 전역 대상 패키지를 미리 게시 합니다.</p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



**구성** -중요 한 app-v 클라이언트 구성에 대 한 자세한 컨텍스트 및 방법에 대 한 자세한 내용은 다음 정보를 참조 하세요.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">구성 설정</th>
<th align="left">이렇게 하면 어떻게 되나요?</th>
<th align="left">어떻게 사용 해야 하나요?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SCS (공유 콘텐츠 저장소) 모드</p>
<ul>
<li><p><strong>Set-AppvClientConfiguration </strong> - <strong> sharedcontentstoremode </strong> 를 사용 하 여 PowerShell에서 구성할 수 있습니다.</p></li>
<li><p>App-v 클라이언트를 설치 하는 동안</p></li>
</ul></td>
<td align="left"><p>공유 콘텐츠 저장소를 실행할 때 게시 데이터만 하드 디스크에서 유지 관리 됩니다. 다른 가상 응용 프로그램 자산은 메모리 (RAM)에 유지 됩니다.</p>
<p>이는 로컬 저장소를 절약 하 고 초당 디스크 I/o (IOPS)를 최소화 하는 데 도움이 됩니다.</p></td>
<td align="left"><p>App-v 클라이언트 끝점과 SCS 콘텐츠 서버, SAN 간에 대기 시간이 짧은 연결을 사용할 수 있는 경우이 방법을 사용 하는 것이 좋습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreserveUserIntegrationsOnLogin</p>
<ul>
<li><p><strong>HKEY_LOCAL_MACHINE </strong>  \  <strong> 소프트웨어 </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> 클라이언트 </strong>  \  <strong> 통합 </strong> 아래에서 레지스트리에 구성 합니다.</p></li>
<li><p><strong>값이 1 인 DWORD 값 PreserveUserIntegrationsOnLogin을 만듭니다 </strong> <strong> </strong> .</p></li>
<li><p>App-v 클라이언트 서비스를 다시 시작 하거나 App-v 클라이언트를 실행 하는 컴퓨터를 다시 시작 합니다.</p></li>
</ul></td>
<td align="left"><p>특정 패키지를 미리 구성 하지 않은 경우 ( <strong> AppvClientPackage </strong> )이 설정이 구성 되어 있지 않으면 app-v 클라이언트는 영구 사용자 통합 * 통합 *을 해제 한 다음 *를 다시 통합 합니다.</p>
<p>위의 조건을 충족 하는 모든 패키지에 대해 게시/새로 고침 중 작업을 두 번 효과적으로 수행할 수 있습니다.</p></td>
<td align="left"><p>기본 이미지에서 사용 가능한 모든 사용자 패키지를 미리 구성할 계획이 없다면이 설정을 사용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxConcurrentPublishingRefresh</p>
<ul>
<li><p><strong>HKEY_LOCAL_MACHINE </strong> &lt; 강력한 &gt; 소프트웨어 </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong> &lt; 강력한 &gt; 클라이언트 </strong>  \  <strong> 게시 </strong> 아래에서 레지스트리에 구성 합니다.</p></li>
<li><p><strong> </strong> 원하는 최대 동시 게시 새로 고침 수를 사용 하 여 DWORD 값 MaxConcurrentPublishingrefresh를 만듭니다.</p></li>
<li><p>App-v 클라이언트 서비스 및 컴퓨터는 다시 시작할 필요가 없습니다.</p></li>
</ul></td>
<td align="left"><p>이 설정은 동시에 게시 새로 고침/동기화를 수행할 수 있는 사용자 수를 결정 합니다. 기본 설정은 제한 없음입니다.</p></td>
<td align="left"><p>동시 게시 새로 고침 횟수를 제한 하면 과도 한 CPU 사용을 방지 하 여 컴퓨터 성능에 영향을 줄 수 있습니다. 이 제한은 여러 사용자가 동시에 같은 컴퓨터에 로그인 하 여 게시 새로 고침 동기화를 수행할 수 있는 RDS 환경에서 권장 됩니다.</p>
<p>동시 게시 새로 고침 임계값에 도달 하는 경우, 새 응용 프로그램을 게시 하 고 로그인 한 후 최종 사용자가 사용할 수 있도록 하는 데 필요한 시간은 결정 시간이 오래 걸릴 수 있습니다.</p></td>
</tr>
</tbody>
</table>



### App-v 접근 방법에 대 한 UE-V 솔루션 구성

Microsoft UE-V (User Experience Virtualization)를 사용 하 여 특정 사용자에 대 한 응용 프로그램 설정 및 Windows 운영 체제 설정을 캡처 및 중앙 집중화 하는 것이 좋습니다. 이러한 설정은 데스크톱 컴퓨터, 랩톱 컴퓨터, VDI (가상 데스크톱 인프라) 세션을 비롯 하 여 사용자가 액세스 하는 다른 컴퓨터에 적용 됩니다. UE-V는 RDS 및 VDI 시나리오에 최적화 되어 있습니다.

자세한 내용은 [사용자 환경 가상화 시작을](https://technet.microsoft.com/library/dn458926.aspx) 참조 하세요. 2.0

기본적으로 UE-V 클라이언트를 설치 하 고 [MICROSOFT ue-v (User Experience Virtualization) 템플릿 갤러리](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33)에서 다음 microsoft 작성 된 앱-V 설정 서식 파일을 다운로드 하는 것이 필요 합니다. 서식 파일을 등록 합니다. UE-V 템플릿에 대 한 자세한 내용은 [템플릿을 가져오고 등록 하기 위한 ue-v 특정 리소스를](https://technet.microsoft.com/library/dn458926.aspx)참조 하세요.

**참고**  
추가 구성 단계를 수행 하지 않고 Microsoft UE-V (사용자 환경 가상화)가 대상 컴퓨터의 시작 메뉴 바로 가기 (.lnk 파일)를 동기화 할 수 없습니다. .Lnk 파일 형식은 기본적으로 제외 됩니다.

UE-V는 모든 사용자의 장치가 같은 위치에 설치 된 동일한 응용 프로그램 집합을가지고 있으며 모든 .lnk 파일이 모든 사용자의 장치에 대해 유효 하 게 되는 RDS 및 VDI 시나리오의 제외 목록에서 .lnk 파일 형식의 제거만 지원 합니다. 예를 들어, UE-V는 일부 장치 에서만 바로 가기가 유효 하기 때문에 현재 다음 두 시나리오를 지원 하지 않습니다.

-   사용자가 .lnk 파일을 사용 하도록 설정 된 하나의 장치에 설치 된 응용 프로그램이 있고 다른 장치에 설치 된 동일한 네이티브 응용 프로그램이 .lnk 파일을 사용 하는 다른 설치 루트에 설정 되어 있는 경우

-   사용자가 한 장치에 응용 프로그램을 설치 했지만 .lnk 파일을 사용 하도록 설정한 경우는 없습니다.



**중요**  
이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다. Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다. 레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다. Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다. 레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.



Microsoft 레지스트리 편집기 (regedit.exe)를 사용 하 여 **HKEY \ _LOCAL \ _MACHINE**  \\  **소프트웨어**  \\  **Microsoft**  \\  **UEV**  \\  **에이전트**구성 ExcludedFileTypes으로 이동 하 여  \\  **Configuration**  \\  **ExcludedFileTypes** 제외 된 파일 형식에서 **.lnk** 를 제거 합니다.

**앱에 대 한 다른 UPM (사용자 프로필 관리) 솔루션 구성-V 접근 방법**

상태 저장 환경에서 예상 되는 경우 UPM 솔루션이 구현 되 고 로그인과 세션 간에 사용자 데이터의 지 속성을 지원할 수 있다는 것입니다.

UPM 솔루션에 대 한 요구 사항은 다음과 같습니다.

사용자에 대 한 App-v 5.1 방법과 같이 최적화 된 로그인 환경을 사용 하려면 솔루션은 다음을 수행할 수 있어야 합니다.

-   사용자 프로필의 일부로 다음 사용자 통합을 유지 합니다.

-   로그인 (또는 응용 프로그램 시작)에 대 한 사용자 프로필 동기화를 트리거하여 모든 사용자 통합이 게시/새로 고침 시작 전에 적용 되도록 보장할 수 있습니다.

-   사용자 통합을 포함 하는 UPD (사용자 프로필 디스크) 또는 유사한 기술을 연결 하 여 분리 합니다.

    **참고**  
    UPD는 전체 프로필이 사용자 프로필 디스크에 저장 된 경우에만 사용할 수 있습니다.

    사용자 프로필 디스크에 저장 된 선택한 폴더와 UPD를 사용 하는 경우 app-v 패키지가 지원 되지 않습니다. 쓰기 드라이버의 복사본은 UPD 선택한 폴더를 처리 하지 않습니다.



-   세션 로그 오프 전에 사용자 통합을 구성 하는 위치에 대 한 변경 내용 캡처

게시 서버를 추가할 때 App-v 5.1 (**추가 기능**)를 사용 하 여 동기화를 구성할 수 있습니다 (예: AppvPublishingServer). 또는 지정 된 새로 고침 간격 이후 새로 고침 및/또는 작업을 수행 합니다. 두 경우 모두에 예약 된 작업이 만들어집니다.

이전 버전의 App-v 5.1에서는 사용자와 전역 새로 고침을 시작 하는 VBScript를 사용 하 여 예약 된 작업을 모두 구성 했습니다. 앱 가상화 5.0 SP2 용 핫픽스 패키지 4를 사용 하 여 로그온 할 때 사용자 새로 고침은 **SyncAppvPublishingServer.exe**에 의해 시작 되었습니다. 이 변경은 UPM 솔루션에 트리거 프로세스를 제공 하기 위해 도입 되었습니다. 이 프로세스는 UPM 솔루션이 사용자 통합을 적용할 수 있도록 게시/새로 고침을 지연 합니다. 게시/새로 고침이 완료 되 면 종료 됩니다.

**사용자 통합**

Registry – HKEY _CURRENT \ _USER

-   경로-Software\\Classes

    Exclude: 지역 설정, ActivatableClasses, AppX \ *

-   경로-Software\\Microsoft\\AppV

-   경로-Software\\Microsoft\\Windows\\CurrentVersion\\App 경로

**파일 위치**

-   Root – "환경 변수" APPDATA

    경로-Microsoft\\AppV\\Client\\Catalog

-   Root – "환경 변수" APPDATA

    경로-Microsoft\\AppV\\Client\\Integration

-   Root – "환경 변수" APPDATA

    경로-Microsoft\\Windows\\Start Menu\\Programs

-   (모든 바탕 화면 바로 가기를 유지 하려면 가상 및 비가상)

    Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ * .lnk

**Microsoft UE-V (User Experience Virtualization)**

또한 UE-V (사용자 환경 가상화)를 사용 하 여 특정 사용자에 대 한 응용 프로그램 설정 및 Windows 운영 체제 설정을 캡처 및 중앙 집중화 하는 것이 좋습니다. 이러한 설정은 데스크톱 컴퓨터, 랩톱 컴퓨터, VDI (가상 데스크톱 인프라) 세션을 비롯 하 여 사용자가 액세스 하는 다른 컴퓨터에 적용 됩니다.

자세한 내용은 [Ue-v 템플릿 갤러리를 사용 하](https://technet.microsoft.com/library/jj679972.aspx)여 [사용자 환경 가상화 1.0 시작](https://technet.microsoft.com/library/jj680015.aspx) 및 설정 위치 템플릿 공유를 참조 하세요.

### <a href="" id="bkmk-uewt"></a>사용자 환경 실습

다음은 App-v 및 UPM 작업을 단계별로 살펴보고 예상 되는 사용자가 기대 하는 내용입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">성능 최적화</th>
<th align="left">저장소에 최적화 됨</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>VDI/RDSH 환경에서이 방법을 구현한 후에는 첫 번째 로그인에</p>
<ul>
<li><p>작업 사용자 게시/새로 고침이 시작 됩니다. 있다는 사용자가 가상 응용 프로그램 (예: 비영구)을 처음으로 게시 한 경우에는 게시/새로 고침을 수행 하는 데 평소와 같은 시간이 소요 됩니다.</p></li>
<li><p>작업 게시/새로 고침 후 UPM 솔루션은 사용자 통합을 캡처합니다. 있다는 UPM 솔루션이 구성 되는 방법에 따라 로그 오프 프로세스의 일부로 발생할 수 있습니다. 이렇게 하면 사용자 상태를 유지 하는 것과 동일한/비슷한 오버 헤드가 발생 합니다.</p></li>
</ul>
<p>후속 로그인:</p>
<ul>
<li><p>작업 UPM 솔루션은 게시/새로 고침 전에 시스템에 사용자 통합을 적용 합니다.</p>
<p>있다는 바탕 화면이 나 시작 메뉴에 바로 가기가 표시 되며 즉시 작동 합니다. 게시/새로 고침이 완료 되 면 (예: 패키지 권리 변경) 일부는 종료 될 수 있습니다.</p></li>
<li><p>작업 게시/새로 고침을 수행 하면 사용자 패키지 자격의 변경에 대 한 게시 취소 및 게시 작업이 처리 됩니다. 있다는 자격을 변경할 수 없는 경우 publishing1가 초 내에 완료 됩니다. 그렇지 않으면 가상 응용 프로그램의 수 및 복잡도 *를 기준으로 게시/새로 고침이 증가 합니다.</p></li>
<li><p>작업 UPM 솔루션은 로그 오프할 때 사용자 통합을 다시 캡처합니다. 있다는 이전과 동일 합니다.</p></li>
</ul>
<p>¹ 게시 작업 ( <strong> 게시-AppVClientPackage </strong> )은 사용자 카탈로그에 항목을 추가 하 고, 사용자에 게 자격을 매핑하고, 로컬 저장소를 식별 하 고, 통합 단계를 완료 하 여 완료 합니다.</p></td>
<td align="left"><p>VDI/RDSH 환경에서이 방법을 구현한 후에는 첫 번째 로그인에</p>
<ul>
<li><p>작업 사용자 게시/새로 고침이 시작 됩니다. 있다는</p>
<ul>
<li><p>사용자가 가상 응용 프로그램 (예: 비영구)을 처음으로 게시 한 경우에는 게시/새로 고침의 일반적인 시간이 소요 됩니다.</p></li>
<li><p>첫 번째 및 후속 로그인은 패키지 사전 구성 (추가/새로 고침)의 영향을 받습니다.</p>
<p></p></li>
</ul></li>
<li><p>작업 게시/새로 고침 후 UPM 솔루션은 사용자 통합을 캡처합니다. 있다는 UPM 솔루션이 구성 되는 방법에 따라 로그 오프 프로세스의 일부로 발생할 수 있습니다. 이는 사용자 상태를 유지 하는 것과 동일한/유사한 오버 헤드를 초래 합니다.</p></li>
</ul>
<p>후속 로그인:</p>
<ul>
<li><p>작업 UPM 솔루션은 게시/새로 고침 전에 시스템에 사용자 통합을 적용 합니다.</p></li>
<li><p>작업 추가/새로 고침은 모든 사용자 대상 응용 프로그램을 미리 구성 해야 합니다. 있다는</p>
<ul>
<li><p>이를 통해 응용 프로그램 가용성에 걸리는 시간 (10 초의 순서 대로)이 현저 하 게 증가할 수 있습니다.</p></li>
<li><p>이렇게 하면 가상 응용 프로그램의 수 및 복잡도 *를 기준으로 게시 새로 고침 시간이 늘어납니다.</p>
<p></p></li>
</ul></li>
<li><p>작업 게시/새로 고침을 수행 하면 사용자 패키지 자격에 대 한 변경 내용에 대 한 게시 취소 및 게시 작업이 처리 됩니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fail</th>
<th align="left">Fail</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>사용자 통합은 완전히 유지 되므로, 예를 들어, 게시/새로 고침이 완료 될 수 있도록 통합에 대 한 작업은 없습니다. 로그인의 초 내에 모든 가상 응용 프로그램을 사용할 수 있습니다.</p></li>
<li><p>게시/새로 고침을 통해 환경에 영향을 주는 가상 응용 프로그램의 사용자에 대 한 변경 내용이 처리 됩니다.</p></li>
</ul></td>
<td align="left"><p>추가/새로 고침이 모든 가상 응용 프로그램을 VM으로 다시 구성 해야 하기 때문에 모든 로그인의 게시 새로 고침 시간이 연장 됩니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a>패키지 수명 주기에 대 한 영향

패키지 업그레이드는 패키지 수명 주기의 중요 한 측면입니다. 사용자가 적절 한 업그레이드 (게시) 또는 다운 그레이드 (게시 취소 된) 가상 응용 프로그램 패키지에 액세스할 수 있도록 하려면이 변경 내용을 반영 하도록 기본 이미지를 업데이트 하는 것이 좋습니다. 다음 섹션을 검토 하는 이유를 이해 하려면 다음을 수행 합니다.

App-v 5.0 SP2에는 보류 상태의 개념이 도입 되었습니다. 과거에는

-   관리자가 자격을 변경 하거나 패키지의 새 버전을 만들고 (업그레이드) 해당 패키지를 사용 하 고 있는 게시/새로 고침을 수행 하는 동안에는 게시 취소 또는 게시 작업이 각각 실패 합니다.

-   이제 패키지가 사용 중인 경우 작업이 보류 됩니다. 게시 취소 및 게시 대기 작업이 서비스를 다시 시작할 때 처리 되거나 다른 게시 또는 게시 취소 명령이 실행 됩니다. 후자의 경우, 가상 응용 프로그램이 사용 중인 경우에는 가상 응용 프로그램이 보류 상태로 유지 됩니다. 전역적으로 게시 된 패키지의 경우 일반적으로 다시 시작 (또는 서비스 다시 시작)이 필요 합니다.

비영구 환경에서는 이러한 보류 된 작업이 처리 되지 않을 가능성은 없습니다. 예를 들어 보류 된 작업은 **HKEY \ _CURRENT \ _USER**  \\  **소프트웨어**  \\  **Microsoft**  \\  **AppV**  \\  **클라이언트**  \\  **pendingtasks**아래에 캡처됩니다. 이 위치는 UPM 솔루션에 의해 유지 되지만 로그온 하기 전에 환경에 적용 되지 않으면 처리 되지 않습니다.

### <a href="" id="bkmk-evdi"></a>성능 최적화 조정을 통해 VDI 환경 개선

다음 섹션에는 환경을 최적화 하는 데 유용할 수 있는 Microsoft 문서 및 다운로드에 대 한 정보가 포함 된 목록이 들어 있습니다.

**.NET NGEN 블로그 및 스크립트 (적극 권장)**

NGEN 기술 정보

-   [NGEN 최적화 속도를 향상 하는 방법](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [스크립트](https://aka.ms/DrainNGenQueue)

**Windows Server 및 서버 역할**

에 대 한 서버 성능 조정 지침

-   [Microsoft Windows Server 2012 R2](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [Microsoft Windows Server 2012](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [Microsoft Windows Server 2008 R2](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**서버 역할**

-   [원격 데스크톱 가상화 호스트](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [원격 데스크톱 세션 호스트](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [IIS 관련성: 앱-V 관리, 게시, 보고 웹 서비스](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [파일 서버 (SMB) 관련성: SCS 모드에서의 App-v 콘텐츠 저장소 및 배달에 사용 되는 경우](https://technet.microsoft.com/library/jj134210.aspx)

**Windows 클라이언트 (게스트 OS) 성능 조정 지침**

-   [Microsoft Windows 7](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [최적화 스크립트: (Microsoft 지원에서 제공)](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [Microsoft Windows 8](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [최적화 스크립트: (Microsoft 지원에서 제공)](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## 게시 성능을 위해 패키지를 최적화 하는 시퀀싱 단계


새로운 시나리오를 활용 하거나 새로운 고객 배포 시나리오를 사용할 수 있도록 하는 몇 가지 App-v 기능. 이러한 다음 기능은 게시 및 시작 작업의 성능에 영향을 줄 수 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">고려 사항</th>
<th align="left">혜택</th>
<th align="left">최선의</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>기능 블록 1 (FB1, 기본 FB 라고도 함) 없음</p></td>
<td align="left"><p>No FB1는 시작 하는 동안 응용 프로그램이 즉시 실행 되 고 오류를 스트림 합니다 (응용 프로그램은 파일, DLL이 필요 하며, 네트워크를 통해 아래로 가져와야 함). 네트워크 제한 사항이 있는 경우 FB1는 다음을 수행 합니다.</p>
<ul>
<li><p>처음으로 응용 프로그램을 시작할 때 사용 되는 스트림 폴트 및 네트워크 대역폭 수를 줄입니다.</p></li>
<li><p>전체 FB1 스트리밍할 때까지 시작을 지연 합니다.</p></li>
</ul></td>
<td align="left"><p>스트림이 실패 하면 실행 시간이 줄어듭니다.</p></td>
<td align="left"><p>FB1 구성 된 가상 응용 프로그램 패키지는 다시 시퀀싱 해야 합니다.</p></td>
</tr>
</tbody>
</table>



### FB1 제거

FB1를 제거 하는 경우 원래 응용 프로그램 설치 관리자가 필요 하지 않습니다. 다음 단계를 완료 한 후 시퀀서를 실행 하는 컴퓨터를 정리 스냅숏으로 되돌리는 것이 좋습니다.

**SEQUENCER UI** -새 가상 응용 프로그램 패키지를 만듭니다.

1.  사용자 지정-스트리밍을 위한 시퀀싱 단계를 완료 &gt; 합니다.

2.  스트리밍 단계에서 **느리거나 불안정 한 네트워크를 통해 배포용 패키지 최적화**를 선택 하지 마세요.

3.  원하는 경우 **대상 OS**로 이동 합니다.

**기존 가상 응용 프로그램 패키지 수정**

1.  스트리밍을 위한 시퀀싱 단계를 완료 합니다.

2.  **느리거나 불안정 한 네트워크를 통해 배포용으로 패키지 최적화**를 선택 하지 마세요.

3.  **패키지 만들기**로 이동 합니다.

**PowerShell** -기존 가상 응용 프로그램 패키지를 업데이트 합니다.

1.  관리자 권한 PowerShell 세션을 엽니다.

2.  가져오기-모듈 **appvsequencer**.

3.  **업데이트-AppvSequencerPackage**  -  **AppvPackageFilePath**

    "C:\\Packages\\MyPackage.appv"-설치 관리자

    "C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath

    "C:\\UpgradedPackages"

    **참고**  
    이 cmdlet에는 실행 (.exe) 또는 배치 파일 (.bat)이 필요 합니다. 비어 있는 (아무 작업도 수행 하지 않음) 실행 파일이 나 배치 파일을 제공 해야 합니다.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">고려 사항</th>
<th align="left">혜택</th>
<th align="left">최선의</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>게시할 때 SXS 설치 없음 (사전 설치 SxS 어셈블리)</p></td>
<td align="left"><p>가상 응용 프로그램 패키지는 다시 시퀀싱 하지 않아도 됩니다. SxS 어셈블리는 가상 응용 프로그램 패키지에 남아 있을 수 있습니다.</p></td>
<td align="left"><p>게시 시간에 SxS 어셈블리 종속성이 설치 되지 않습니다.</p></td>
<td align="left"><p>SxS 어셈블리 종속성은 사전 설치 되어야 합니다.</p></td>
</tr>
</tbody>
</table>



### Sequencer에서 새 가상 응용 프로그램 패키지 만들기

시퀀서 모니터링 중에 응용 프로그램 설치의 일부로 SxS 어셈블리 (예: VC + + 런타임)가 설치 되어 있으면 SxS 어셈블리가 자동으로 검색 되 고 패키지에 포함 됩니다. 관리자에 게 알림이 표시 되 고 SxS 어셈블리를 제외 하는 옵션이 표시 됩니다.

**클라이언트측**:

가상 응용 프로그램 패키지를 게시할 때 App-v 클라이언트는 필수 SxS 종속성이 이미 설치 되어 있는지 여부를 감지 합니다. 컴퓨터에서 종속성을 사용할 수 없고 패키지에 포함 된 경우 기존 Windows Installer (.** msi**) SxS 어셈블리 설치가 시작 됩니다. 앞에서 설명한 대로 클라이언트를 실행 하는 컴퓨터에 종속성을 설치 하면 Windows Installer (.msi) 설치가 수행 되지 않습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">고려 사항</th>
<th align="left">혜택</th>
<th align="left">최선의</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>선택적으로 동적 구성 파일을 채택 합니다.</p></td>
<td align="left"><p>App-v 5.1 클라이언트는 이러한 동적 구성 파일을 구문 분석 하 고 처리 해야 합니다.</p>
<p>파일의 크기와 복잡도 (스크립트 실행, VREG 포함/제외)에 대해 주의 해야 합니다.</p>
<p>많은 가상 응용 프로그램 패키지에 사용자 또는 컴퓨터 관련 동적 구성 파일이 이미 있을 수 있습니다.</p></td>
<td align="left"><p>이러한 파일이 선택적으로 또는 전혀 사용 되지 않는 경우 게시 시간이 향상 됩니다.</p></td>
<td align="left"><p>가상 응용 프로그램 패키지는 연결 된 동적 구성 파일을 제거 하기 위해 개별적으로 또는 App-v 서버 관리 콘솔을 통해 다시 구성 해야 합니다.</p></td>
</tr>
</tbody>
</table>



### Powershell을 사용 하 여 동적 구성 비활성화

-   이미 게시 된 패키지의 경우 다음 없이 사용할 수 있습니다. `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv`

    **-Dynamicdeploymentconfiguration** 매개 변수

-   마찬가지로,를 사용 하 여 새 패키지를 추가 하는 경우 다음을 `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` 사용 하지 마십시오.

    **-Dynamicdeploymentconfiguration** 매개 변수.

동적 구성을 적용 하는 방법에 대 한 설명서는 다음을 참조 하세요.

-   [PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [PowerShell을 사용하여 배포 구성 파일을 적용하는 방법](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">고려 사항</th>
<th align="left">혜택</th>
<th align="left">최선의</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>패키지 수명 주기 동안 동기 스크립트 실행을 위한 계정입니다.</p></td>
<td align="left"><p>스크립트 참고가 패키지에 포함 된 경우 추가 (Powershell)가 매우 느릴 수 있습니다.</p>
<p>가상 응용 프로그램 시작 (StartVirtualEnvironment, StartProcess) 및/또는 추가 + 게시 중 스크립트를 실행 하면 이러한 주기 작업 중 하나 이상에서 인식 되는 성능에 영향을 줍니다.</p></td>
<td align="left"><p>비동기 (비블로킹) 스크립트를 사용 하 여 수명 주기 작업이 효율적으로 완료 되도록 할 수 있습니다.</p></td>
<td align="left"><p>이 단계에서는 포함 된 스크립트 참조를 사용 하는 모든 가상 응용 프로그램 패키지에 대 한 지식 (동적 구성 파일이 연결 되어 있고 스크립트를 동기적으로 실행 하는 경우)이 필요 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지에서 불필요 한 가상 글꼴을 제거 합니다.</p></td>
<td align="left"><p>App-v 제품 팀에서 조사 하는 대부분의 응용 프로그램에는 적은 수의 글꼴이 포함 되어 있으며 일반적으로 20 개 미만입니다.</p></td>
<td align="left"><p>가상 글꼴은 게시 새로 고침 성능에 영향을 줍니다.</p></td>
<td align="left"><p>원하는 글꼴은 기본적으로 사용 하도록 설정/설치 해야 합니다. 지침은 글꼴 설치 또는 제거를 참조 하세요.</p></td>
</tr>
</tbody>
</table>



### 패키지에 존재 하는 가상 글꼴 확인

-   패키지 복사본을 만듭니다.

-   패키지 \ _copy의 이름을 바꿉니다. Package\_copy.zip

-   AppxManifest.xml를 열고 다음을 찾습니다.

    &lt;appv: 확장 범주 = "AppV. 글꼴"&gt;

    &lt;appv: Fonts&gt;

    &lt;appv: 글꼴 경로 = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /appv: font&gt;

    **참고**  
    **Delayload**로 표시 된 글꼴이 있는 경우 첫 번째 시작에는 영향을 주지 않습니다.



~~~
&lt;/appv:Fonts&gt;
~~~

### 패키지에서 가상 글꼴 제외

사용자 범위에 가장 적합 한 동적 구성 파일 사용-컴퓨터의 모든 사용자에 대 한 배포 구성, 특정 사용자에 대 한 사용자 구성

-   배포 또는 사용자 구성에서 글꼴을 사용 하지 않도록 설정 합니다.

글꼴

--&gt;

&lt;글꼴 사용 = "false"/&gt;

&lt;!--

## <a href="" id="bkmk-terms1"></a> 앱-V 5.1 성능 지침 용어


다음 용어는 App-v 5.1 성능 최적화와 관련 된 개념 및 작업을 설명 하는 데 사용 됩니다.

-   **복잡도** – 사전 구성 (**추가-AppvClientPackage**) 또는 통합 (**게시-AppvClientPackage**) 중에 성능에 영향을 줄 수 있는 하나 이상의 패키지 특성을 나타냅니다. 일부 특성은 매니페스트 크기, 가상 글꼴 수, 파일 수 등입니다.

-   **비 통합** -사용자 통합이 제거 됩니다.

-   **다시 통합** -사용자 통합을 적용 합니다.

-   **비 영구적인, 풀링됨** – 로그인 할 때마다 가상 환경을 실행 하는 컴퓨터를 만듭니다.

-   **영구, 개인** – 모든 로그인에 대해 동일 하 게 유지 되는 가상 환경을 실행 하는 컴퓨터입니다.

-   이 문서의 **상태 저장** -사용자 통합이 세션 간에 유지 되며 사용자 환경 관리 기술이 비영구 RDSH 또는 VDI와 결합 하 여 사용 됨을 의미 합니다.

-   **상태 비저장** – 세션 간에 사용자 상태가 유지 되지 않는 시나리오를 나타냅니다.

-   **트리거** – (또는 네이티브 동작 트리거). UPM는 이러한 유형의 트리거를 사용 하 여 모니터링 또는 동기화 작업을 시작 합니다.

-   **사용자 환경** -app-v 5.1의 컨텍스트에서 quantitatively 사용자 환경은 다음 부분에 대 한 합계입니다.

    -   사용자가 데스크톱을 조작할 수 있을 때 로그인을 시작 하는 시점부터

    -   데스크톱을 해당 지점으로 상호 작용할 수 있는 시점부터 (App-v 5.1 full server 인프라를 사용 하는 경우에는 PowerShell 용어로 동기화 됨) 게시 새로 고침이 시작 됩니다. 독립 실행형 인스턴스에서 **AppVClientPackage** 및 **게시-AppVClientPackage Powershell** 명령이 시작 되는 경우입니다.

    -   게시 새로 고침 시작부터 완료까지 독립 실행형 인스턴스에서는 처음부터 마지막으로 게시 된 가상 응용 프로그램입니다.

    -   바로 가기에서 가상 응용 프로그램을 사용할 수 있는 지점부터 시작 합니다. 또는 파일 형식 연결이 등록 된 시점부터 지정 된 가상 응용 프로그램을 시작 합니다.

-   **사용자 프로필 관리** -환경과 연결 된 사용자 구성 요소를 관리 하는 제어 되 고 구조적인 방법입니다. 예를 들어 사용자 프로필, 기본 설정 및 정책 관리, 응용 프로그램 제어 및 응용 프로그램 배포입니다. 스크립팅 또는 타사 솔루션을 사용 하 여 필요에 따라 환경을 구성할 수 있습니다.






## 관련 항목


[Microsoft Application Virtualization 5.1 관리자 가이드](microsoft-application-virtualization-51-administrators-guide.md)









