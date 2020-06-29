---
title: MED-V 1.0 지원되는 구성
description: MED-V 1.0 지원되는 구성
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812609"
---
# MED-V 1.0 지원되는 구성


이 항목에서는 환경에서 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 1.0를 설치 하 고 실행 하는 데 필요한 요구 사항을 설명 합니다.

## MED-V 1.0 클라이언트 시스템 요구 사항


### MED-V 클라이언트 운영 체제 요구 사항

다음 표에는 MED-V 1.0 클라이언트 설치에 지원 되는 운영 체제가 나와 있습니다.

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
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 또는 SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>비즈니스, 엔터프라이즈 또는 Ultimate Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



**참고**  
MED-V 클라이언트는 네이티브 x64 모드에서 실행 되지 않습니다. 대신, MED-V는 windows 64 비트 (WOW64) 모드의 Windows에서 64 비트 컴퓨터를 통해 실행 됩니다.



### <a href="" id="med-v-1-0-client-configuration-"></a>MED-V 1.0 클라이언트 구성

**.NET Framework 버전**

MED-V 1.0 클라이언트 설치에 지원 되는 Microsoft .NET Framework 버전은 다음과 같습니다.

-   .NET Framework 2.0 또는 .NET Framework 2.0 SP1

-   .NET Framework 3.0 또는 .NET Framework 3.0 SP1

-   .NET Framework 3.5 또는 .NET Framework 3.5 SP1

**가상화 엔진**

Microsoft 기술 자료 문서 974918에서 설명 하는 핫픽스가 포함 된 microsoft 가상 PC 2007 SP1은 다음과 같은 구성에서 MED-V 1.0 클라이언트 설치에 지원 됩니다.

-   정적 VHD (가상 하드 디스크) 파일

-   같은 디렉터리 내에 있는 여러 개의 VHD 파일

-   동적 VHD 파일

**인터넷 브라우저**

Windows Internet Explorer 7 및 Windows Internet Explorer 8은 MED-V 1.0 클라이언트 설치에 지원 됩니다.

**Microsoft Hyper-V Server**

MED-V 클라이언트는 Microsoft Hyper-v server 환경에서 지원 되지 않습니다.

## MED-V 1.0 Workspace 시스템 요구 사항


### MED-V 작업 영역 운영 체제 요구 사항

다음 표에는 MED-V 1.0 작업 영역에 대해 지원 되는 운영 체제가 나와 있습니다.

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
<td align="left"><p>Windows 2000</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>4(SP4)</p></td>
<td align="left"><p>86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 또는 SP3</p>
<div class="alert">
<strong>참고</strong><br/><p>SP3은 MED-V 작업 영역이 차기 버전의 MED-V와 호환 되도록 하는 데 적합 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a>MED-V 1.0 작업 영역 구성

**.NET Framework 버전**

MED-V 1.0 작업 영역 설치에 대해 다음과 같은 지원 되는 Microsoft .NET Framework 버전 중 하나가 필요 합니다.

-   .NET Framework 2.0 SP1

-   .NET Framework 3.0 SP1

-   .NET Framework 3.5 또는 .NET Framework 3.5 SP1

**참고**  
.NET Framework 3.5 SP1은 MED-V 작업 영역이 MED-V의 향후 버전과 호환 되도록 하는 데 권장 됩니다.



**인터넷 브라우저**

MED-V 1.0 작업 영역 설치에는 windows Internet Explorer 6 SP2 및 Windows Internet Explorer 7이 지원 됩니다.

### <a href="" id="med-v-workspace-images-"></a>MED-V 작업 영역 이미지

가상 PC 2007 SP1을 사용 하 여 MED-V 작업 영역 이미지를 만들어야 합니다.

## MED-V 1.0 서버 시스템 요구 사항


### MED-V 1.0 서버 운영 체제 요구 사항

다음 표에는 MED-V 1.0 서버 설치에 지원 되는 운영 체제가 나와 있습니다.

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
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard 또는 Enterprise</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>X86 또는 x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a>MED-V 1.0 서버 구성

**.NET Framework 버전**

MED-V 1.0 작업 영역 설치에 대해 다음과 같은 지원 되는 Microsoft .NET Framework 버전 중 하나가 필요 합니다.

-   .NET Framework 2.0 또는 .NET Framework 2.0 SP1

-   .NET Framework 3.0 또는 .NET Framework 3.0 SP1

-   .NET Framework 3.5 또는 .NET Framework 3.5 SP1

**Microsoft SQL Server 버전**

SQL Server가 MED-V 1.0 서버에서 로컬 또는 원격으로 설치 되는 경우 다음과 같은 Microsoft SQL Server 버전이 MED-V 1.0에 대해 지원 됩니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server 버전</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server 2005</p></td>
<td align="left"><p>익스프레스, Standard 또는 Enterprise Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 또는 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 2008</p></td>
<td align="left"><p>익스프레스, Standard 또는 Enterprise</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>X86 또는 x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

MED-V 서버는 Microsoft Hyper-v server 환경에서 지원 됩니다.

## MED-V 1.0 세계화 정보


MED-V는 영어 이외의 언어로 릴리스되지 않지만 MED-V 1.0 클라이언트, 작업 영역 및 서버 설치에는 다음과 같은 Windows 운영 체제 언어 버전이 지원 됩니다.

-   영어

-   프랑스어

-   독일어

-   이탈리아어

-   스페인어

-   포르투갈어(브라질)









