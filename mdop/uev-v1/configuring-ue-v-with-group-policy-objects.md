---
title: 그룹 정책 개체를 사용하여 UE-V 구성
description: 그룹 정책 개체를 사용하여 UE-V 구성
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826698"
---
# 그룹 정책 개체를 사용하여 UE-V 구성


일부 Microsoft UE-V (사용자 환경 가상화) 그룹 정책 설정은 컴퓨터에 대해 정의 될 수 있으며 다른 사용자를 위해 정의할 수 있습니다. 컴퓨터 또는 사용자에 대해 UE-V 에이전트 구성 정책 설정을 정의할 수 있습니다. UE-V 그룹 정책 ADMX 파일을 설치 하는 방법에 대 한 자세한 내용은 [Ue-v 그룹 정책 Admx 템플릿 설치](installing-the-ue-v-group-policy-admx-templates.md)를 참조 하세요.

UE-V에 대해 다음 정책 설정을 구성할 수 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>정책 설정 이름</strong></p></td>
<td align="left"><p><strong>대상</strong></p></td>
<td align="left"><p><strong>정책 설정 설명</strong></p></td>
<td align="left"><p><strong>구성 옵션</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 환경 가상화 사용 (UE-V)</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정을 통해 UE-V (User Experience Virtualization)를 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</p></td>
<td align="left"><p>이 정책 설정을 사용 하거나 사용 하지 않도록 설정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정 저장소 경로</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정은 사용자 설정이 저장 되는 위치를 구성 합니다.</p></td>
<td align="left"><p>\Server\SettingsShare%username%.와 같은 UNC (범용 명명 규칙) 경로 및 변수를 제공 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정 서식 파일 카탈로그 경로</p></td>
<td align="left"><p>컴퓨터만</p></td>
<td align="left"><p>이 정책 설정은 사용자 지정 설정 위치 템플릿이 저장 되는 위치를 구성 합니다. 이 정책 설정은 또한 UE-V agent를 사용 하 여 설치 된 기본 Microsoft 템플릿을 바꾸는 데 카탈로그를 사용할지 여부를 구성 합니다.</p></td>
<td align="left"><p>\Server\TemplateShare 또는 컴퓨터의 폴더 위치와 같은 UNC (범용 명명 규칙) 경로를 제공 합니다.</p>
<p></p>
<p>기본 Microsoft 서식 파일을 바꾸려면 확인란을 선택 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>오프 라인 파일을 사용 하지 않음</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정을 통해 UE-V가 Windows 오프 라인 파일 기능을 사용할지 여부를 구성할 수 있습니다. 이 정책 설정을 사용 하면 사용자 설정 가져오기가 지연 되는 경우 알림을 수행할 수도 있습니다.</p></td>
<td align="left"><p>오프 라인 파일을 사용 하지 않도록 UE-V Agent를 구성 하려면이 설정을 사용 하도록 설정 합니다.</p>
<p></p>
<p>설정 가져오기가 지연 되는 경우 알림을 제공 해야 하는지 여부를 지정 합니다.</p>
<p></p>
<p>알림이 나타나기 전에 대기할 시간 (초)을 지정 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>동기화 시간 제한</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정은 원격 설정 위치에서 사용자 설정을 검색할 때 컴퓨터가 시간 초과 되기 전에 대기 하는 시간 (밀리초)을 구성 합니다. 원격 저장소 위치를 사용할 수 없는 경우 응용 프로그램 시작이이 시간 (밀리초) 만큼 지연 됩니다.</p></td>
<td align="left"><p>기본 설정 동기화 시간 제한을 밀리초로 지정 합니다. 기본 값인 2000 밀리초입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지 크기 경고 임계값</p></td>
<td align="left"><p>컴퓨터 및 사용자</p></td>
<td align="left"><p>이 정책 설정을 통해 UE-V agent가 설정 패키지 파일 크기가 정의 된 임계값에 도달할 때 보고 하도록 구성할 수 있습니다.</p></td>
<td align="left"><p>설정 패키지 크기 (kb)에 대 한 기본 설정 임계값을 지정 합니다.</p>
<p>기본적으로 UE-V agent에는 패키지 파일 크기 임계값이 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>로밍 응용 프로그램 설정</p></td>
<td align="left"><p>사용자만</p></td>
<td align="left"><p>이 정책 설정은 응용 프로그램의 사용자 설정 로밍을 구성 합니다.</p></td>
<td align="left"><p>컴퓨터 간에 로밍 되는 Windows 설정을 선택 합니다.</p>
<p>기본적으로 UE-V를 통해 설정 템플릿이 제공 하는 응용 프로그램의 사용자 설정은 컴퓨터 간에 roamed 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>로밍 Windows 설정</p></td>
<td align="left"><p>사용자만</p></td>
<td align="left"><p>이 정책 설정은 Windows 설정의 로밍을 구성 합니다.</p></td>
<td align="left"><p>컴퓨터 간에 로밍할 응용 프로그램을 선택 합니다.</p>
<p>기본적으로 Windows 테마는 동일한 운영 체제 버전의 컴퓨터 간에 roamed 됩니다. Windows 데스크톱 설정 및 접근성 설정은 roamed 되지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

**컴퓨터 대상 정책을 구성 하려면**

1.  UE-V 컴퓨터에 대 한 그룹 정책을 관리 하는 도메인 컨트롤러 컴퓨터의 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 사용 합니다. **컴퓨터 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.

2.  편집할 정책 설정을 선택 합니다.

**사용자 대상 정책을 구성 하려면**

1.  UE-V (Microsoft 데스크톱 최적화 팩)의 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) 도구를 사용 합니다. i V m에 대 한 그룹 정책을 관리 하는 도메인 컨트롤러 컴퓨터의 MDOP **사용자 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.

2.  편집한 정책 설정을 선택 합니다.

UE-V agent는 다음 우선 순위를 사용 하 여 동기화를 결정 합니다.

**UE-V 설정의 우선 순위 순서**

1.  그룹 정책에서 관리 하는 사용자 대상 설정-이러한 구성 설정은 아래에 있는 그룹 정책에 의해 레지스트리 키에 저장 됩니다 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  그룹 정책에서 관리 하는 컴퓨터 대상 설정-이러한 구성 설정은 그룹 정책에 따라 레지스트리 키에 저장 됩니다 `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  PowerShell 또는 WMI를 사용 하 여 현재 사용자가 정의한 구성 설정-이러한 구성 설정은 UE-V agent가 다음 레지스트리 위치에 저장 `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` 됩니다.

4.  PowerShell 또는 WMI를 사용 하 여 컴퓨터에 대해 정의 된 구성 설정입니다. 이러한 구성 설정은의 UE-V agent에 저장 됩니다 `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .

## 관련 항목


[UE-V 1.0 관리](administering-ue-v-10.md)

[UE-V 1.0 작업](operations-for-ue-v-10.md)

 

 





