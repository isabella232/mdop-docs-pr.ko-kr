---
title: App-V 5.0 지원되는 구성
description: App-V 5.0 지원되는 구성
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814788"
---
# App-V 5.0 지원되는 구성


이 항목에서는 환경에서 Microsoft Application Virtualization (App-v) 5.0을 설치 하 고 실행 하는 데 필요한 요구 사항을 설명 합니다.

**중요**  
**이 문서의 지원 되는 구성은 app-v 5.0에만 적용**됩니다. App-v 5.0 서비스 팩에 적용 되는 지원 되는 구성에 대해서는 다음 웹 페이지를 참조 하세요.

-   [App-V 5.0 SP1의 새로운 기능](whats-new-in-app-v-50-sp1.md)

-   [App-V 5.0 SP2 정보](about-app-v-50-sp2.md)

-   [App-V 5.0 SP3 지원되는 구성](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> 앱-V 5.0 서버 시스템 요구 사항


**중요**  
App-v 5.0 서버는 다음 시나리오를 지원 하지 않습니다.



-   Microsoft Windows Server Core를 실행 하는 컴퓨터에 배포

-   이전 버전의 App-v 5.0 서버 구성 요소를 실행 하는 컴퓨터에 배포 합니다.

    **참고**  
    App-v 4.5 경량 스트리밍 서버 (LWS) 서버를 사용 하 여 App-v 5.0를 나란히 설치할 수 있습니다. App-v 5.0 for HWS (Application Virtualization Management Service) 서버를 4.5 나란히 배치 하는 작업은 지원 되지 않습니다.



-   Microsoft SQL Server Express edition을 실행 하는 컴퓨터에 배포

-   관리 서버 데이터베이스 또는 보고 데이터베이스의 원격 배포 Microsoft SQL을 실행 하는 컴퓨터에서 설치 관리자를 직접 실행 하 여 데이터베이스를 성공적으로 설치 해야 합니다.

-   도메인 컨트롤러에 배포.

-   짧은 경로는 지원 되지 않습니다. 짧은 경로를 사용할 계획인 경우 새 볼륨을 만들어야 합니다.

### 관리 서버 운영 체제 요구 사항

다음 표에는 App-v 5.0 관리 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter 또는 웹 서버)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1 이상</p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



**중요**  
원격 데스크톱 공유 (RDS)를 사용 하도록 설정한 컴퓨터에 관리 서버 역할을 배포 하는 것은 지원 되지 않습니다.



### <a href="" id="management-server-hardware-requirements-"></a>관리 서버 하드웨어 요구 사항

-   프로세서-1.4 GHz 이상, 64 비트 (x64) 프로세서

-   RAM-1GB RAM (64 비트)

-   디스크 공간-하드 디스크 공간-200mb 사용할 수 있습니다 (콘텐츠 디렉터리는 포함 하지 않음).

### 서버 운영 체제 요구 사항 게시

다음 표에는 App-v 5.0 게시 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter 또는 웹 서버)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>서버 하드웨어 요구 사항 게시

-   프로세서-1.4 GHz 이상. 64 비트 (x64) 프로세서

-   RAM-2GB RAM (64 비트)

-   디스크 공간 – 200mb의 하드 디스크 공간이 사용 가능 합니다. 콘텐츠 디렉터리 포함 안 함

### 보고 서버 운영 체제 요구 사항

다음 표에는 App-v 5.0 reporting server 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



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
<td align="left"><p>Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter 또는 웹 서버)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (Standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>보고 서버 하드웨어 요구 사항

-   프로세서-1.4 GHz 이상. 64 비트 (x64) 프로세서

-   RAM-2GB RAM (64 비트)

-   디스크 공간-200mb 사용 가능한 하드 디스크 공간

### <a href="" id="sql-server-database-requirements-"></a>SQL Server 데이터베이스 요구 사항

다음 표에는 App-v 5.0 데이터베이스 및 서버 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.

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
<th align="left">App-v 5.0 서버 유형</th>
<th align="left">SQL Server 버전</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>관리/보고</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(표준, 엔터프라이즈, Datacenter 또는 Developer Edition은 다음 기능을 사용 합니다. <strong> 데이터베이스 엔진 서비스 </strong> .</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리/보고</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(표준, 엔터프라이즈, Datacenter 또는 Developer Edition은 다음 기능을 사용 합니다. <strong> 데이터베이스 엔진 서비스 </strong> .</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>관리/보고</p></td>
<td align="left"><p>Microsoft SQL Server 2012</p>
<p>(표준, 엔터프라이즈, Datacenter 또는 Developer Edition은 다음 기능을 사용 합니다. <strong> 데이터베이스 엔진 서비스 </strong> .</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> 앱-V 5.0 클라이언트 시스템 요구 사항


다음 표에는 App-v 5.0 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>중요</strong><br/><p>Windows 8.1는 앱-V 5.0 SP2 에서만 지원 됩니다.</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>



다음 App-v 클라이언트 설치 시나리오가 지원 되지 않습니다 (언급 된 경우 제외).

-   Windows Server를 실행 하는 컴퓨터

-   App-v 4.6 SP1 또는 이전 버전을 실행 하는 컴퓨터

-   앱-V 5.0 원격 데스크톱 서비스 클라이언트는 RDS 사용 서버에 대해서만 지원 됩니다.

### <a href="" id="client-hardware-requirements-"></a>클라이언트 하드웨어 요구 사항

다음 목록에는 App-v 5.0 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.

-   프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서

-   RAM (1 GB (32 비트) 또는 2gb (64 비트)

-   Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> 앱-V 5.0 원격 데스크톱 클라이언트 시스템 요구 사항


다음 표에는 App-v 5.0 원격 데스크톱 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



운영 체제 버전 서비스 팩 Microsoft Windows Server 2008

R2

SP1

Microsoft Windows Server 2012

**중요**  
Windows Server 2012 R2는 앱-V 5.0 SP2 에서만 지원 됩니다.



Microsoft Windows Server 2012 (Standard, Datacenter)

R2

64비트



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>원격 데스크톱 클라이언트 하드웨어 요구 사항

다음 목록에는 App-v 5.0 클라이언트 설치에 대해 지원 되는 하드웨어 구성이 표시 됩니다.

-   프로세서-1.4 GHz 이상 32 비트 (x86) 또는 64 비트 (x64) 프로세서

-   RAM (1 GB (32 비트) 또는 2gb (64 비트)

-   Disk-설치 시 100 MB, 가상화 된 응용 프로그램에서 사용 하는 디스크 공간을 포함 하지 않습니다.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> 앱-V 5.0 Sequencer 시스템 요구 사항


다음 표에는 App-v 5.0 Sequencer 설치에 지원 되는 운영 체제 목록이 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 및 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 및 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>중요</strong><br/><p>Windows 8.1는 앱-V 5.0 SP2 에서만 지원 됩니다.</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 및 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 및 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>중요</strong><br/><p>Windows Server 2012 R2는 앱-V 5.0 SP2 에서만 지원 됩니다.</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>지원 되는 버전의 System Center Configuration Manager


Microsoft System Center 2012 구성 관리자 또는 System Center 2012 R2 구성 관리자를 사용 하 여 App-v 가상 응용 프로그램, 보고 및 기타 기능을 관리할 수 있습니다. 다음 표에는 해당 하는 각 App-v 버전에 대해 지원 되는 버전의 구성 관리자가 나열 되어 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">지원 되는 Configuration Manager 버전</th>
<th align="left">App-V 버전</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center 2012 구성 관리자</p></td>
<td align="left"><ul>
<li><p>App-V 5.0</p></li>
<li><p>App-v 5.0 SP1</p></li>
<li><p>App-v 5.0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5.0</p></li>
<li><p>App-v 5.0 SP1</p></li>
<li><p>App-v 5.0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Configuration Manager를 App-v와 통합 하는 방법에 대 한 자세한 내용은 [Configuration manager를 사용 하 여 App-v 통합 계획](https://technet.microsoft.com/library/jj822982.aspx)을 참조 하세요.






## 관련 항목


[App-V 배포 계획](planning-to-deploy-app-v.md)

[App-V 5.0 필수 구성 요소](app-v-50-prerequisites.md)









