---
title: UE-V 1.0과 동기화할 응용 프로그램 계획
description: UE-V 1.0과 동기화할 응용 프로그램 계획
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812417"
---
# UE-V 1.0과 동기화할 응용 프로그램 계획


Microsoft UE-V (User Experience Virtualization)는 UE-V를 통해 캡처 및 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다. UE-V는 미리 정의 된 설정 위치 템플릿의 집합을 포함 하며, 관리자는 엔터프라이즈에서 사용 되는 타사 또는 lob (기간 업무) 응용 프로그램에 대 한 사용자 지정 설정 위치 서식 파일을 만들 수도 있습니다.

관리자는 UE-V 솔루션에 포함할 응용 프로그램을 고려할 때 사용자가 지정할 수 있는 설정과 응용 프로그램이 해당 설정을 저장 하는 방법 및 위치를 고려해 야 합니다. 일부 응용 프로그램에는 사용자 지정할 수 있는 설정이 포함 되어 있지 않거나 정기적으로 사용자 지정 되어 있습니다. 또한 일부 응용 프로그램 설정은 여러 컴퓨터 또는 환경에서 안전 하 게 로밍할 수 없습니다. 다음 조건에 맞는 설정을 동기화 합니다.

-   사용자가 액세스할 수 있는 위치에 저장 되는 설정 예를 들어 system32 또는 레지스트리의 외부 HKCU 섹션에 저장 된 설정을 동기화 하지 마세요.

-   특정 컴퓨터에 국한 되지 않는 설정입니다. 예를 들어 네트워크 또는 하드웨어 구성을 제외 합니다.

-   데이터 손상 위험 없이 컴퓨터 간에 동기화 될 수 있는 설정 예를 들어 데이터베이스 파일에 저장 된 설정을 사용 하지 마세요.

## UE-V에 포함 된 설정 위치 템플릿


**UE-V 응용 프로그램 설정 위치 템플릿**

UE-V 에이전트 설치 소프트웨어는 에이전트를 설치 하 고 공통 Microsoft 응용 프로그램에 대 한 기본 설정 위치 템플릿 그룹을 등록 합니다. 이러한 설정 위치 템플릿은 다음 응용 프로그램에 대 한 설정 값을 캡처합니다.

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
<td align="left"><p>Microsoft Office 2010 응용 프로그램</p></td>
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
<p>Microsoft OneNote 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>브라우저 옵션 (Internet Explorer 8, Internet Explorer 9 및 Internet Explorer 10)</p></td>
<td align="left"><p>즐겨찾기, 홈 페이지, 탭, 도구 모음</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 액세서리</p></td>
<td align="left"><p>계산기, 메모장, 워드 패드</p></td>
</tr>
</tbody>
</table>

 

응용 프로그램은 응용 프로그램을 시작할 때 응용 프로그램에 적용 됩니다. 응용 프로그램이 닫힐 때 저장 됩니다.

**UE-V Windows 설정 위치 템플릿**

사용자 환경 가상화에는 다음 Windows 설정에 대 한 설정 값을 캡처하는 설정 위치 템플릿이 포함 됩니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows 설정</th>
<th align="left">설명</th>
<th align="left">적용 기준</th>
<th align="left">기본 상태</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>바탕 화면 배경</p></td>
<td align="left"><p>현재 활성 상태인 바탕 화면 배경입니다.</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결</p></td>
<td align="left"><p>설정됨</p></td>
</tr>
<tr class="even">
<td align="left"><p>접근성</p></td>
<td align="left"><p>접근성 및 입력 설정, 돋보기, 내레이터, 화상 키보드</p></td>
<td align="left"><p>로그온, 잠금 해제, 원격 연결</p></td>
<td align="left"><p>해제됨</p></td>
</tr>
<tr class="odd">
<td align="left"><p>바탕 화면 설정</p></td>
<td align="left"><p>시작 메뉴 및 작업 표시줄 설정, 폴더 옵션, 기본 바탕 화면 아이콘, 추가 시계, 지역 및 언어 설정</p></td>
<td align="left"><p>로그온만 가능 합니다.</p></td>
<td align="left"><p>해제됨</p></td>
</tr>
</tbody>
</table>

 

Windows 데스크톱 배경과 접근성 설정은 사용자가 로그온 하거나 컴퓨터를 잠그거나, 원격으로 다른 컴퓨터에 연결할 때 적용 됩니다. 에이전트는 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있거나 원격 연결이 끊어질 때 이러한 설정을 저장 합니다. 기본적으로 Windows 바탕 화면 배경 설정은 동일한 운영 체제 버전의 컴퓨터 간에 roamed 됩니다.

Windows 데스크톱과 접근성 설정은 데스크톱이 사용자에 게 표시 되기 전에 로그온 할 때 적용 됩니다. 로그온 환경을 최적화 하기 위해 이러한 설정은 기본적으로 roamed 되지 않습니다. 데스크톱 및 접근성 설정은 그룹 정책, PowerShell, WMI를 사용 하 여 설정할 수 있습니다.

UE-V는 다른 언어의 운영 체제 간에 설정 로밍을 지원 하지 않습니다. 예를 들어, 영어와 독일어 간의 동기화는 지원 되지 않습니다. UE-V를 로밍 하는 모든 컴퓨터의 언어는 사용자 설정에 일치 해야 합니다.

**참고**  Microsoft에서 제공 하는 설정 위치 서식 파일을 변경 하는 경우 사용자 환경 가상화가 지정 된 응용 프로그램 또는 Windows 설정 그룹에 대해 제대로 작동 하지 않을 수 있습니다.

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a>의도 하지 않은 사용자 설정 구성 방지


사용자 환경 가상화는 새 사용자 설정 정보를 확인 하 고 설정 저장소 위치에서 해당 정보를 다운로드 합니다. 이렇게 하면 다음과 같은 경우 로컬 컴퓨터에 설정이 적용 됩니다.

-   등록 된 UE-V 템플릿이 있는 응용 프로그램이 시작 될 때마다

-   사용자가 컴퓨터에 로그온 하는 경우

-   사용자가 컴퓨터의 잠금을 해제 하는 경우

-   UE-V를 설치한 원격 데스크톱 컴퓨터에 연결 하는 경우

UE-V을 컴퓨터 A 및 컴퓨터 B에 설치 하 고 응용 프로그램에 대 한 원하는 설정이 컴퓨터 A에 있는 경우 컴퓨터 A가 먼저 응용 프로그램을 열고 닫아야 합니다. 컴퓨터 B에서 응용 프로그램을 열고 닫은 경우 컴퓨터 A의 응용 프로그램 설정이 컴퓨터 B의 응용 프로그램 설정과 동일 하 게 구성 됩니다.

이 시나리오는 Windows 설정에도 적용 됩니다. 컴퓨터 B의 Windows 설정이 컴퓨터 A의 Windows 설정과 동일 해야 하는 경우 사용자는 먼저 컴퓨터 A에 로그온 하 고 로그 아웃 해야 합니다.

원하는 사용자 설정이 잘못 된 순서로 적용 되는 경우 설정을 덮어쓴 컴퓨터에서 특정 응용 프로그램 또는 Windows 구성에 대 한 복원 작업을 수행 하 여 복구할 수 있습니다. 자세한 내용은 [ue-v 1.0와 동기화 된 응용 프로그램 및 Windows 설정 복원을](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)참조 하세요.

## 사용자 지정 UE-V 설정 위치 템플릿


UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들 수 있습니다. 테스트 환경에서 사용자 지정 설정 위치 템플릿을 만들고 테스트 한 후 엔터프라이즈의 컴퓨터에 설정 위치 템플릿을 배포할 수 있습니다. 사용자 지정 설정 위치 템플릿은 ESD (엔터프라이즈 소프트웨어 배포) 메서드, 기본 설정 또는 UE-V 설정 템플릿 카탈로그를 구성 하는 등 기존 배포 인프라와 함께 배포 해야 합니다. ESD 또는 그룹 정책을 사용 하 여 배포 된 서식 파일은 UE-V WMI 또는 PowerShell을 사용 하 여 등록 해야 합니다. 사용자 지정 설정 위치 서식 파일에 대 한 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.

Lob (기간 업무) 응용 프로그램을 동기화할지 여부에 대 한 지침은 [ue-v 1.0의 lob (기간 업무) 응용 프로그램 평가에 대 한 검사 목록을](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md)참조 하세요.

## 관련 항목


[UE-V 1.0 계획](planning-for-ue-v-10.md)

[UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)

[UE-V 1.0 배포](deploying-ue-v-10.md)

 

 





