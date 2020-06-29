---
title: App-V 5.1 지원되는 구성
description: App-V 5.1 지원되는 구성
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814724"
---
# App-V 5.1 지원되는 구성

>적용 대상: Windows 10, 버전 1607, Window 서버 2019; Windows Server 2016 Windows Server 2012 R2 Windows Server 2012 Windows Server 2008 R2 (확장 보안 업데이트)

이 항목에서는 환경에서 Microsoft App-v (Application Virtualization) 5.1를 설치 하 고 실행 하기 위한 요구 사항을 지정 합니다.

## 앱-V 서버 시스템 요구 사항

이 섹션에는 모든 App-v 서버 구성 요소에 대 한 운영 체제 및 하드웨어 요구 사항이 나열 되어 있습니다.

### 지원 되지 않는 앱-V 5.1 서버 시나리오

App-v 5.1 서버는 다음 시나리오를 지원 하지 않습니다.

-   Microsoft Windows Server Core를 실행 하는 컴퓨터에 배포

-   이전 버전의 App-v 5.1 서버 구성 요소를 실행 하는 컴퓨터에 배포 합니다. App-v 4.5 경량 스트리밍 서버 (LWS) 서버만을 사용 하 여 App-v 5.1를 나란히 설치할 수 있습니다. 앱이 app-v를 통해 나란히 배포 됨-V 4.5 Application Virtualization 관리 서비스 (HWS) 서버는 지원 되지 않습니다.

-   Microsoft SQL Server Express edition을 실행 하는 컴퓨터에 배포

-   도메인 컨트롤러에 배포.

-   짧은 경로. 짧은 경로를 사용할 계획 이라면 새 볼륨을 만들어야 합니다.

### 관리 서버 운영 체제 요구 사항

다음 표에는 App-v 5.1 관리 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

> [!NOTE]
> Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) 를 참조 하세요.

 | 운영 체제                 | 서비스 팩 | 시스템 아키텍처 |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64비트       |
| Microsoft Windows Server 2016    |              |        64비트       |
| Microsoft Windows Server 2012 R2 |              |        64비트       |
| Microsoft Windows Server 2012    |              |        64비트       |
| Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates)|      SP1     |        64비트       |
 

**중요**  원격 데스크톱 공유 (RDS)를 사용 하도록 설정한 컴퓨터에 관리 서버 역할을 배포 하는 것은 지원 되지 않습니다.

 

### <a href="" id="management-server-hardware-requirements-"></a>관리 서버 하드웨어 요구 사항

-   프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서

-   RAM-1GB RAM (64 비트)

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)

### 관리 서버 데이터베이스 요구 사항

다음 표에는 App-v 5.1 관리 데이터베이스 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server 버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>이상을</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>

SQL server 2016 이상을 사용 하는 사용자 구성 파일에 대 한 자세한 내용은 [지원 문서](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f)를 참조 하세요.

### 서버 운영 체제 요구 사항 게시

다음 표에는 App-v 5.1 게시 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

| 운영 체제                 | 서비스 팩 | 시스템 아키텍처 |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64비트       |
| Microsoft Windows Server 2016    |              |        64비트       |
| Microsoft Windows Server 2012 R2 |              |        64비트       |
| Microsoft Windows Server 2012    |              |        64비트       |
| Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates) |      SP1     |        64비트       |

### <a href="" id="publishing-server-hardware-requirements-"></a>서버 하드웨어 요구 사항 게시

App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.

-   프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서

-   RAM-2GB RAM (64 비트)

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간 (콘텐츠 디렉터리는 포함 하지 않음)

### 보고 서버 운영 체제 요구 사항

다음 표에는 App-v 5.1 Reporting server 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

| 운영 체제                 | 서비스 팩 | 시스템 아키텍처 |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64비트       |
| Microsoft Windows Server 2016    |              |        64비트       |
| Microsoft Windows Server 2012 R2 |              |        64비트       |
| Microsoft Windows Server 2012    |              |        64비트       |
| Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates) |      SP1     |        64비트       |

### <a href="" id="reporting-server-hardware-requirements-"></a>보고 서버 하드웨어 요구 사항

App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.

-   프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서

-   RAM-2GB RAM (64 비트)

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간

### 보고 서버 데이터베이스 요구 사항

다음 표에는 App-v 5.1 보고 데이터베이스 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">SQL Server 버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>이상을</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>App-v 클라이언트 시스템 요구 사항

다음 표에는 App-v 5.1 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

> [!NOTE]
> Windows 10 예정일 릴리스 (라고도 함 1607 버전)를 사용 하는 경우 App-v 클라이언트가 box에 있으며, 이전 버전의 App-v 클라이언트에 대 한 설치를 차단 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows10 (1607 이전 버전)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>

 

다음 App-v 클라이언트 설치 시나리오가 지원 되지 않습니다 (언급 된 경우 제외).

-   Windows Server를 실행 하는 컴퓨터

-   App-V 4.6 SP1 또는 이전 버전을 실행 하는 컴퓨터

-   앱-V 5.1 원격 데스크톱 서비스 클라이언트는 RDS 사용 서버에 대해서만 지원 됩니다.

### <a href="" id="app-v-client-hardware-requirements-"></a>App-v 클라이언트 하드웨어 요구 사항

다음 목록에는 App-v 5.1 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.

-   프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서

-   RAM (1 GB (32 비트) 또는 2gb (64 비트)

-   Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.

## 원격 데스크톱 서비스 클라이언트 시스템 요구 사항


다음 표에는 RDS (원격 데스크톱 서비스) 클라이언트 설치 5.1에 지원 되는 운영 체제 목록이 나와 있습니다.

| 운영 체제                 | 서비스 팩 | 시스템 아키텍처 |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64비트       |
| Microsoft Windows Server 2016    |              |        64비트       |
| Microsoft Windows Server 2012 R2 |              |        64비트       |
| Microsoft Windows Server 2012    |              |        64비트       |
| Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates) |      SP1     |        64비트       |

### 원격 데스크톱 서비스 클라이언트 하드웨어 요구 사항

App-v는 Windows Server의 추가 요구 사항을 추가 하지 않습니다.

-   프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서

-   RAM-2GB RAM (64 비트)

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간

## Sequencer 시스템 요구 사항

다음 표에는 App-v 5.1 Sequencer 설치에 지원 되는 운영 체제 목록이 나와 있습니다.

| 운영 체제                 | 서비스 팩 | 시스템 아키텍처 |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64비트       |
| Microsoft Windows Server 2016    |              |        64비트       |
| Microsoft Windows Server 2012 R2 |              |        64비트       |
| Microsoft Windows Server 2012    |              |        64비트       |
| Microsoft Windows Server 2008 R2 [연장 보안 업데이트](https://www.microsoft.com/windows-server/extended-security-updates) |      SP1     |        64비트       |
| Microsoft Windows 10             |              | 32비트 및 64비트   |
| Microsoft Windows 8.1            |              | 32비트 및 64비트   |
| Microsoft Windows 7              |      SP1     | 32비트 및 64비트   |

### 시퀀서 하드웨어 요구 사항

하드웨어 요구 사항에 대해서는 Windows 또는 Windows Server 설명서를 참조 하세요. 앱-V는 추가 하드웨어 요구 사항을 추가 하지 않습니다.

## <a href="" id="bkmk-supp-ver-sccm"></a>지원 되는 버전의 System Center Configuration Manager

App-v 클라이언트는 다음 버전의 System Center Configuration Manager를 지원 합니다.

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

다음 App-v 및 System Center Configuration Manager 버전 매트릭스는 앱-V 및 구성 관리자의 공식적으로 지원 되는 조합을 모두 보여 줍니다.

> [!NOTE]
> 앱-V 4.5 및 4.6에서 기본 지원이 종료 되었습니다.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 버전</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">System Center 2012 Configuration Manager</th>
<th align="left">System Center 2012 Configuration Manager SP1</th>
<th align="left">System Center 2012 R2 Configuration Manager</th>
<th align="left">System Center 2012 R2 Configuration Manager SP1</th>
<th align="left">System Center 2012 Configuration Manager SP2</th>
<th align="left">System Center Configuration Manager 버전 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 5.0 SP3</p></td>
<td align="left"><p>MSI-래퍼만</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.1</p></td>
<td align="left"><p>MSI-래퍼만</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
</tbody>
</table>

 

Configuration Manager를 App-v와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager를 사용 하 여 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx)을 참조 하세요.

## 관련 항목

[App-V 배포 계획](planning-to-deploy-app-v51.md)

[App-V 5.1 필수 구성 요소](app-v-51-prerequisites.md)
