---
title: 그룹 정책 개체를 사용 하 여 UE-V 2. x 구성
description: 그룹 정책 개체를 사용 하 여 UE-V 2. x 구성
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824423"
---
# 그룹 정책 개체를 사용 하 여 UE-V 2. x 구성


일부 Microsoft UE-V (사용자 환경 가상화) 2.0, 2.1 및 2.1 SP1 그룹 정책 설정은 컴퓨터에 대해 정의 될 수 있으며 다른 그룹 정책 설정은 사용자에 대해 정의 될 수 있습니다. UE-V 그룹 정책 ADMX 파일을 설치 하는 방법에 대 한 자세한 내용은 [ue-v 2 그룹 정책 Admx 템플릿 설치](https://technet.microsoft.com/library/dn458891.aspx#admx)를 참조 하세요.

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
<td align="left"><p>연락처 링크 텍스트</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 회사 설정 센터에 있는 IT 대화 상대 URL 하이퍼링크의 텍스트를 지정 합니다.</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 하면 회사 설정 센터에 연락처 URL에 대 한 링크에 지정 된 텍스트가 표시 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>연락처 URL</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 회사 설정 센터의 IT 연락처 링크에 대 한 URL을 지정 합니다.</p></td>
<td align="left"><p>이 설정을 사용 하면 회사 설정 센터에서 지정 된 URL에 대 한 텍스트 링크를 연결 합니다. 링크는 HTTP 또는 mailto와 같은 표준 프로토콜 일 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>동기화 공급자 사용 안 함</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 하 여 UE-V가 동기화 공급자 기능을 사용 하는지 여부를 구성할 수 있습니다. 이 정책 설정을 사용 하면 사용자 설정 가져오기가 지연 될 때 알림이 표시 되도록 할 수도 있습니다.</p></td>
<td align="left"><p>이 설정을 사용 하면 UE-V Agent가 동기화 공급자를 사용 하지 않도록 구성할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>첫 번째 사용 알림</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V를 사용 하 여 표시 되는 알림 영역에서 알림을</p>
<p>에이전트를 처음 실행할 때 실행 됩니다.</p></td>
<td align="left"><p>기본값을 사용 하도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 설정 로밍</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 Windows 설정의 동기화를 구성 합니다.</p></td>
<td align="left"><p>컴퓨터 간에 동기화 할 Windows 설정을 선택 합니다.</p>
<p>기본적으로 Windows 테마, 데스크톱 설정 및 접근성 설정은 동일한 운영 체제 버전의 컴퓨터 간에 설정을 동기화 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정 패키지 크기 경고 임계값</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 하 여 설정 패키지 파일 크기가 정의 된 임계값에 도달 하는 경우 UE-V 에이전트를 보고 하도록 구성할 수 있습니다.</p></td>
<td align="left"><p>설정 패키지 크기 (KB)에 대 한 기본 임계값을 지정 합니다.</p>
<p>기본적으로 UE-V Agent에는 패키지 파일 크기 임계값이 없습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정 저장소 경로</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 사용자 설정을 저장할 위치를 구성 합니다.</p></td>
<td align="left"><p>UNC (범용 명명 규칙) 경로 및 \Server\SettingsShare%username%. 등의 변수를 입력 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정 서식 파일 카탈로그 경로</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정은 사용자 지정 설정 위치 템플릿이 저장 되는 위치를 구성 합니다. 이 정책 설정은 또한 UE-V Agent를 사용 하 여 설치 된 기본 Microsoft 템플릿을 바꾸는 데 카탈로그를 사용할지 여부를 구성 합니다.</p></td>
<td align="left"><p>\Server\TemplateShare 또는 컴퓨터의 폴더 위치와 같은 UNC (범용 명명 규칙) 경로를 입력 합니다.</p>
<p>기본 Microsoft 서식 파일을 바꾸려면 확인란을 선택 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>데이터 통신 연결을 통한 설정 동기화</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V가 유료 연결을 통해 설정을 동기화할지 여부를 정의 합니다.</p></td>
<td align="left"><p>기본적으로 UE-V Agent는 데이터 통신 연결을 통해 설정을 동기화 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>로밍할 때에도 데이터 통신 연결을 통해 설정 동기화</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 데이터 연결이 로밍 모드일 때와 같이 홈 공급자 네트워크 외부에서 UE-V가 통신 연결을 통해 설정을 동기화할지 여부를 정의 합니다.</p></td>
<td align="left"><p>기본적으로 UE-V는 로밍 모드일 때 데이터 통신 연결을 통해 설정을 동기화 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>동기화 시간 제한</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 원격 설정 위치에서 사용자 설정을 검색할 때 시간 초과 되기 전에 컴퓨터가 대기 하는 밀리초 수를 구성 합니다. 원격 저장소 위치를 사용할 수 없고 사용자가 동기화 공급자를 사용 하지 않는 경우에는 응용 프로그램 시작이이 시간 (밀리초) 만큼 지연 됩니다.</p></td>
<td align="left"><p>기본 설정 동기화 시간 초과 (밀리초)를 지정 합니다. 기본값은 2000 밀리초입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>트레이 아이콘</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 그룹 정책 설정을 통해 UE-V (User Experience Virtualization) 트레이 아이콘을 사용할 수 있습니다.</p></td>
<td align="left"><p>기본값을 사용 하도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 환경 가상화 사용 (UE-V)</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정을 통해 UE-V (User Experience Virtualization)를 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</p></td>
<td align="left"><p>이 그룹 정책 설정을 사용 하거나 사용 하지 않도록 설정 합니다.</p></td>
</tr>
</tbody>
</table>

 

**참고**  또한 다양 한 데스크톱 응용 프로그램 및 Windows 앱에서 그룹 정책 설정을 사용할 수 있습니다. 이러한 설정을 사용 하 여 특정 응용 프로그램에 대 한 설정 동기화를 설정 하거나 해제할 수 있습니다.

 

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
<td align="left"><p>Windows 앱 동기화 안 함</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 UE-V Agent가 Windows 앱에 대 한 설정을 동기화할지 여부를 정의 합니다.</p></td>
<td align="left"><p>기본값은 Windows 앱을 동기화 하는 것입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 앱 목록</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 설정에는 UE-V가 해당 앱의 설정을 동기화할지 여부를 명시적으로 Windows 앱 및 상태의 패밀리 패키지 이름이 나열 됩니다.</p></td>
<td align="left"><p>이 설정을 사용 하 여 다른 모든 Windows 앱의 설정이 동기화 된 경우에도 앱의 설정이 UE-V를 통해 동기화 되지 않도록 지정할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>목록에 없는 Windows 앱 동기화</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 그룹 정책 설정은 Windows 앱 목록에 명시적으로 나열 되지 않은 Windows 용 UE-V Agent의 기본 설정 동기화 동작을 정의 합니다.</p></td>
<td align="left"><p>기본적으로 UE-V Agent는 Windows 앱 목록에 포함 된 Windows 앱의 설정만 동기화 합니다.</p></td>
</tr>
</tbody>
</table>

 

Windows 앱을 동기화 하는 방법에 대 한 자세한 내용은 [Windows 앱 목록을](https://technet.microsoft.com/library/dn458925.aspx#win8applist)참조 하세요.

**컴퓨터 대상 그룹 정책 설정을 구성 하려면**

1.  UE-V 컴퓨터에 대 한 그룹 정책 설정을 관리 하려면 도메인 컨트롤러 역할을 하는 컴퓨터의 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 사용 합니다. **컴퓨터 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.

2.  편집할 그룹 정책 설정을 선택 합니다.

**사용자 대상 그룹 정책 설정을 구성 하려면**

1.  UE-V (Microsoft 데스크톱 최적화 팩)의 GPMC (그룹 정책 관리 콘솔) 또는 MDOP (고급 그룹 정책 관리) 도구를 사용 하 여 온-V에 대 한 그룹 정책 설정을 관리 합니다. **사용자 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.

2.  편집 된 그룹 정책 설정을 선택 합니다.

UE-V Agent는 다음 우선 순위를 사용 하 여 동기화를 결정 합니다.

**UE-V 설정의 우선 순위 순서**

1.  그룹 정책 설정으로 관리 되는 사용자 대상 설정-이러한 구성 설정은의 그룹 정책에 따라 레지스트리 키에 저장 됩니다 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  그룹 정책 설정으로 관리 되는 컴퓨터 대상 설정-이러한 구성 설정은 아래의 그룹 정책에 의해 레지스트리 키에 저장 됩니다 `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Windows PowerShell 또는 WMI (Windows management Instrumentation)를 사용 하 여 현재 사용자가 정의한 구성 설정-이 구성 설정은 다음 레지스트리 위치에 UE-V Agent에 의해 저장 됩니다 `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Windows PowerShell 또는 WMI를 사용 하 여 컴퓨터에 대해 정의 된 구성 설정입니다. 이러한 구성 설정은 UE-V Agent에서 다음 레지스트리 위치에 저장 `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` 됩니다.

    **Ue-v에 대 한 제안이 있으십니까**? [여기](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)에서 제안을 추가 하거나 투표 합니다. **Ue-v 문제가**있나요? [Ue-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)을 사용 합니다.

## 관련 항목


[UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

[UE-V 2.x에 대한 구성 관리](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





