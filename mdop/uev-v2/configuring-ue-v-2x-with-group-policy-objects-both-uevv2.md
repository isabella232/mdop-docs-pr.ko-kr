---
title: 그룹 정책 개체를 사용하여 UE-V 2.x 구성
description: 그룹 정책 개체를 사용하여 UE-V 2.x 구성
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494063"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a>그룹 정책 개체를 사용하여 UE-V 2.x 구성


컴퓨터에 대해 일부 Microsoft UE-V(User Experience Virtualization) 2.0, 2.1 및 2.1 SP1 그룹 정책 설정을 정의할 수 있으며 사용자에 대해 다른 그룹 정책 설정을 정의할 수 있습니다. UE-V 그룹 정책 ADMX 파일을 설치하는 방법에 대한 자세한 내용은 [UE-V 2](https://technet.microsoft.com/library/dn458891.aspx#admx)그룹 정책 ADMX 템플릿 설치를 참조하세요.

UE-V에 대해 다음 정책 설정을 구성할 수 있습니다.

**그룹 정책 설정**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 정책 설정 이름</th>
<th align="left">대상</th>
<th align="left">그룹 정책 설정 설명</th>
<th align="left">구성 옵션</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>동기화 방법 구성</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용하여 UE-V(User Experience Virtualization)에서 동기화 공급자 기능을 사용할지 여부를 구성할 수 있습니다. 이 정책 설정을 사용하면 사용자 설정 가져오기가 지연될 때 알림을 표시하도록 설정할 수도 있습니다.</p></td>
<td align="left"><p>UE-V 에이전트가 동기화 공급자를 사용하지 못하도록 구성하거나 외부 동기화 엔진을 사용하도록 구성하려면 이 설정을 사용합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IT 링크 텍스트에 문의</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 회사 설정 센터에서 연락처 IT URL 하이퍼링크의 텍스트를 지정합니다.</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용하면 회사 설정 센터에 연락처 IT URL 링크에 지정된 텍스트가 표시됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IT URL에 문의</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 회사 설정 센터의 연락처 IT 링크에 대한 URL을 지정합니다.</p></td>
<td align="left"><p>이 설정을 사용하면 회사 설정 센터 IT 담당자가 지정한 URL에 대한 텍스트 링크를 사용합니다. 연결은 HTTP 또는 mailto와 같은 모든 표준 프로토콜일 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>첫 번째 사용 알림</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V가 나타날 때 나타나는 알림 영역에 알림을 설정</p>
<p>에이전트가 처음으로 실행됩니다.</p></td>
<td align="left"><p>기본값은 사용하도록 설정되어 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>동기화하기 전에 설정 저장 위치 Ping</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정을 사용하면 연결을 확인하기 위해 설정을 동기화하기 전에 UE-V 동기화 공급자를 구성하여 설정 저장 경로를 ping할 수 있습니다.</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 또는 사용하지 않도록 설정</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정 패키지 크기 경고 임계값</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정을 통해 설정 패키지 파일 크기가 정의된 임계값에 도달한 경우 보고하도록 UE-V 에이전트를 구성할 수 있습니다.</p></td>
<td align="left"><p>설정 패키지 크기에 대한 기본 임계값을 KB(킬로바이트)로 지정합니다.</p>
<p>기본적으로 UE-V 에이전트에는 패키지 파일 크기 임계값이 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정 저장소 경로</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 사용자 설정을 저장할 위치를 구성합니다.</p></td>
<td align="left"><p>UNC(범용 이름 규칙) 경로 및 \Server\SettingsShare%username%와 같은 변수를 입력합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정 템플릿 카탈로그 경로</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 사용자 지정 설정 위치 템플릿이 저장되는 위치를 구성합니다. 이 정책 설정은 설치된 기본 Microsoft 템플릿을 UE-V 에이전트로 바꾸기 위해 카탈로그를 사용할지 여부도 구성합니다.</p></td>
<td align="left"><p>\Server\TemplateShare와 같은 UNC(범용 이름 규칙) 경로 또는 컴퓨터의 폴더 위치를 입력합니다.</p>
<p>기본 Microsoft 서식 파일을 바꾸기 위해 확인란을 선택합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>데이터 연결에 대한 동기화 설정</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V가 데이터 연결에서 설정을 동기화할지 여부를 정의합니다.</p></td>
<td align="left"><p>기본적으로 UE-V 에이전트는 데이터 데이터 연결을 통해 설정을 동기화하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>로밍 시에도 데이터 연결에 대한 동기화 설정</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V가 홈 공급자 네트워크 외부의 데이터 통신 연결(예: 데이터 연결이 로밍 모드인 경우)을 통해 설정을 동기화할지 여부를 정의합니다.</p></td>
<td align="left"><p>기본적으로 UE-V는 로밍 모드일 때 데이터 데이터 연결을 통해 설정을 동기화하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>동기화 시간 제한</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 컴퓨터가 원격 설정 위치에서 사용자 설정을 검색할 때 시간이 너무 되기 전에 대기하는 시간(밀리초)을 구성합니다. 원격 저장소 위치를 사용할 수 없는 경우 사용자가 동기화 공급자를 사용하지 않는 경우 응용 프로그램 시작이 이 밀리초까지 지연됩니다.</p></td>
<td align="left"><p>기본 동기화 시간(밀리초)을 지정합니다. 기본값은 2000밀리초입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 설정 동기화 </p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 Windows 설정의 동기화를 구성합니다.</p></td>
<td align="left"><p>컴퓨터 간에 동기화할 Windows 설정을 선택합니다.</p>
<p>기본적으로 Windows 테마, 데스크톱 설정 및 접근성 설정은 동일한 운영 체제 버전의 컴퓨터 간에 설정을 동기화합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>트레이 아이콘</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V 트레이 아이콘을 사용 가능하게 합니다.</p></td>
<td align="left"><p>기본값은 사용하도록 설정되어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UE-V(User Experience Virtualization) 사용</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정을 통해 UE-V를 활성화 또는 비활성화할 수 있습니다.</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 또는 사용하지 않도록 설정</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VDI 구성</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정은 풀링된 VDI 환경에서 실행되는 컴퓨터의 UE-V 롤백 정보 동기화를 구성합니다. 해당 정책을 사용하도록 설정하면 UE-V 롤백 상태가 로그아웃 시 설정 저장소 위치에 복사되고 로그인 시 복원됩니다.</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 또는 사용하지 않도록 설정</p></td>
</tr>
</tbody>
</table>

 

**참고**  
또한 그룹 정책 설정은 많은 데스크톱 응용 프로그램 및 Windows 앱에서 사용할 수 있습니다. 이러한 설정을 사용하여 특정 응용 프로그램에 대해 설정 동기화를 설정하거나 사용하지 않도록 설정할 수 있습니다.

 

**Windows 앱 그룹 정책 설정**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 정책 설정 이름</th>
<th align="left">대상</th>
<th align="left">그룹 정책 설정 설명</th>
<th align="left">구성 옵션</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 앱을 동기화하지 않습니다.</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V 에이전트가 Windows 앱의 설정을 동기화하는지 여부를 정의합니다.</p></td>
<td align="left"><p>기본값은 Windows 앱을 동기화하는 것입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 앱 목록</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 설정은 Windows 앱의 패밀리 패키지 이름을 나열하고 UE-V가 해당 앱의 설정을 동기화하는지 여부를 하여 확인합니다.</p></td>
<td align="left"><p>다른 모든 Windows 앱의 설정이 동기화된 경우에도 이 설정을 사용하여 앱 설정이 UE-V와 동기화되지 않는지 지정할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>목록에 없는 Windows 앱 동기화</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 Windows 앱 목록에 명시적으로 나열되지 않은 Windows 앱용 UE-V 에이전트의 기본 설정 동기화 동작을 정의합니다.</p></td>
<td align="left"><p>기본적으로 UE-V 에이전트는 Windows 앱 목록에 포함된 Windows 앱의 설정만 동기화합니다.</p></td>
</tr>
</tbody>
</table>

 

Windows 앱 동기화에 대한 자세한 내용은 [Windows 앱 목록 을 참조하세요.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

**컴퓨터 대상 그룹 정책 설정을 구성하려면**

1.  도메인 컨트롤러 역할을 하는 컴퓨터에서 GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리)을 사용하여 UE-V 컴퓨터에 대한 그룹 정책 설정을 관리합니다. 컴퓨터 **구성으로 이동하여** **정책을**선택하고 관리 템플릿을 선택하고 **Windows**구성 요소를 클릭한 다음 **Microsoft User Experience Virtualization 을 선택합니다.** ****

2.  편집할 그룹 정책 설정을 선택합니다.

**사용자 대상 그룹 정책 설정을 구성하려면**

1.  도메인 컨트롤러 컴퓨터에서 MDOP(Microsoft Desktop Optimization Pack)의 GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리) 도구를 사용하여 UE-V에 대한 그룹 정책 설정을 관리합니다. 사용자 **구성으로 이동하여** **정책,** 관리 **템플릿을**선택하고 **Windows**구성 요소를 클릭한 다음 **Microsoft User Experience Virtualization 을 선택합니다.**

2.  편집된 그룹 정책 설정을 선택합니다.

UE-V 에이전트는 다음 우선 순위를 사용하여 동기화를 파악합니다.

**UE-V 설정의 우선 순위**

1.  그룹 정책 설정으로 관리되는 사용자 대상 설정 - 이러한 구성 설정은 에서 그룹 정책에 의해 레지스트리 키에 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` 저장됩니다.

2.  그룹 정책 설정에 의해 관리되는 컴퓨터 대상 설정 - 이러한 구성 설정은 의 그룹 정책에 의해 레지스트리 키에 `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` 저장됩니다.

3.  Windows PowerShell 또는 WMI(Windows management Instrumentation)를 사용하여 현재 사용자가 정의하는 구성 설정 - 이러한 구성 설정은 이 레지스트리 위치의 UE-V 에이전트에 의해 저장됩니다. `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  WMI 또는 WMI를 사용하여 컴퓨터에 Windows PowerShell 설정입니다. 이러한 구성 설정은 UE-V 에이전트에 의해 이 레지스트리 위치 아래에 `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` 저장됩니다. .

    **UE-V에 대한 제안이 있나요?** 여기에 제안을 추가하거나 [투표합니다.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization) **UE-V 문제가 있나요?** [UE-V TechNet 포럼을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)

## <a name="related-topics"></a>관련 항목


[UE-V 2.x 관리](administering-ue-v-2x-new-uevv2.md)

[UE-V 2.x에 대한 구성 관리](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
