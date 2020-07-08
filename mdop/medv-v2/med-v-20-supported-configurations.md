---
title: MED-V 2.0 지원되는 구성
description: MED-V 2.0 지원되는 구성
author: dansimp
ms.assetid: 88f1d232-aa01-45ab-8da7-d086269250b5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0fed090ec04cf67a32b13533f4003c01ae167493
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825218"
---
# MED-V 2.0 지원되는 구성


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0를 설치 하 고 실행할 수 있도록 사용자의 환경이 이미 여기에 제공 된 구성 요구 사항을 충족 했을 수 있습니다. 호스트 운영 체제, 디스크 공간, MED-V 작업 영역 요구 사항 등의 요구 사항이 포함 되었습니다.

## MED-V 2.0 호스트 컴퓨터 요구 사항


### MED-V 2.0 호스트 운영 체제 요구 사항

다음 표에는 호스트 컴퓨터의 MED-V 2.0 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise 또는 Ultimate</p></td>
<td align="left"><p>없음 또는 SP1</p></td>
<td align="left"><p>x86 또는 x64</p></td>
</tr>
</tbody>
</table>

 

다음 표에는 MED-V 2.0에서 지원 되는 각 운영 체제에 필요한 최소 RAM이 나와 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">필요한 최소 RAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7 x86</p></td>
<td align="left"><p>GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7 x64</p></td>
<td align="left"><p>GB</p></td>
</tr>
</tbody>
</table>

 

### 최소 권장 디스크 공간

최소 10GB의 스토리지를 사용 하는 것이 좋습니다. 그러나 필요한 디스크 공간은 매우 다양 하며 MED-V 작업 영역에 게시 되는 응용 프로그램 수에 따라 달라 집니다.

### <a href="" id="med-v-2-0-host-configuration-"></a>MED-V 2.0 호스트 구성

**.NET Framework 버전**

.NET Framework 3.5 SP1 버전의 Microsoft .NET Framework는 MED-V 2.0에 필요 합니다. 그러나 .net Framework 3.5이 이미 설치 되어 있는 경우 .NET Framework 4 이상 버전을 설치할 수 있습니다.

**가상화 엔진**

Microsoft 기술 자료 문서 977206에서 설명 하는 핫픽스가 있는 Windows 가상 Pc는 MED-V 2.0에 지원 됩니다.

**인터넷 브라우저**

Windows Internet Explorer8 및 Windows Internet Explorer 9는 MED-V 2.0에서 지원 됩니다.

**Microsoft 서버 환경**

MED-V 호스트 에이전트와 MED-V 작업 영역 포장기는 모든 서버 환경에서 지원 되지 않습니다.

## MED-V 2.0 작업 영역 요구 사항


### MED-V 2.0 Workspace 운영 체제 요구 사항

다음 표에는 MED-V 2.0 작업 영역에 대해 지원 되는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>이상을</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="med-v-2-0-workspace-configuration-"></a>MED-V 2.0 작업 영역 구성

**.NET Framework 버전**

MED-V 2.0 작업 영역 설치의 경우 .NET Framework 3.5 SP1 버전의 Microsoft .NET Framework만 지원 됩니다.

**인터넷 브라우저**

MED-V 2.0 작업 영역 설치에는 windows Internet Explorer6, Windows Internet Explorer7, Windows Internet Explorer8 및 Windows Internet Explorer9이 지원 됩니다.

### MED-V 2.0 작업 영역 만들기

MED-V 2.0 작업 영역 패키지를 작성 하는 데 사용 되는 가상 하드 디스크는 Windows 가상 PC를 사용 하 여 만들어야 합니다.

## MED-V 2.0 세계화 정보


### MED-V 2.0 호스트 에이전트 세계화 정보

MED-V 2.0 호스트 에이전트에 대해 다음 Windows 운영 체제 언어 버전이 지원 됩니다.

-   프랑스어

-   이탈리아어

-   독일어

-   스페인어

-   한국어

-   일본어

-   브라질 포르투갈어

-   러시아어

-   중국어(번체)

-   중국어 간체

-   네덜란드어

-   스웨덴어

-   덴마크어

-   핀란드어

-   포르투갈어

-   노르웨이어

-   폴란드어

-   터키어

-   헝가리어

-   체코어

-   그리스어

-   슬로바키아어

-   슬로베니아어

### MED-V 2.0 작업 영역 포장기 세계화 정보

MED-V 2.0 작업 영역 포장기에 대해 다음 Windows 운영 체제 언어 버전이 지원 됩니다.

-   프랑스어

-   이탈리아어

-   독일어

-   스페인어

-   한국어

-   일본어

-   브라질 포르투갈어

-   러시아어

-   중국어(번체)

-   중국어 간체

## 관련 항목


[MED-V 배포](deployment-of-med-v.md)

 

 





