---
title: MBAM 2.5 보고서를 구성하는 방법
description: MBAM 2.5 보고서를 구성하는 방법
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826618"
---
# MBAM 2.5 보고서를 구성하는 방법


이 항목에서는 다음을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 보고서 기능을 구성 하는 방법에 대해 설명 합니다.

-   Windows PowerShell cmdlet

-   MBAM 서버 구성 마법사

이 지침은 [MBAM 2.5의 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md)에서 권장 되는 아키텍처를 기반으로 합니다.

**구성을 시작 하기 전에 다음을 수행 합니다.**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">단계</th>
<th align="left">지침을 받을 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM에 권장 되는 아키텍처를 검토 합니다.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">MBAM 2.5의 개략적인 아키텍처</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM에 대해 지원 되는 구성을 검토 합니다.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>각 서버에서 필수 구성 요소를 완성 합니다.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2.5 구성 관리자 통합 토폴로지에만 적용 되는 서버 필수 구성 요소 </a> (해당 하는 경우)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell cmdlet을 사용 하 여 MBAM 서버 기능을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 조건을 검토 합니다.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</a></p></td>
</tr>
</tbody>
</table>



**Windows PowerShell을 사용 하 여 보고서를 구성 하려면**

1.  구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.

2.  **사용-MbamReport** Windows PowerShell cmdlet을 사용 하 여 보고서를 구성 합니다. 이 Windows PowerShell cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamReport**를 입력 합니다.

**마법사를 사용 하 여 보고서를 구성 하려면**

1. 보고서를 구성할 서버에서 **Mbam 서버 구성** 마법사를 시작 합니다. **시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.

2. **새 기능 추가**를 클릭 하 고 **보고서**를 선택한 후 **다음**을 클릭 합니다. 마법사에서 보고서에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.

3. **Next**(다음)를 클릭하여 계속합니다.

4. 다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">필드</th>
   <th align="left">설명</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server Reporting Services 인스턴스</strong></p></td>
   <td align="left"><p>보고서를 구성 하는 SQL Server Reporting Services의 인스턴스입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>보고 역할 도메인 그룹</strong></p></td>
   <td align="left"><p>관리 및 모니터링 서버의 보고서에 액세스할 수 있는 권한이 있는 구성원의 도메인 사용자 그룹 이름입니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server 이름</strong></p></td>
   <td align="left"><p>규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>SQL Server 데이터베이스 인스턴스</strong></p></td>
   <td align="left"><p><em> </em> 규정 준수 및 감사 데이터베이스가 구성 된 SQL Server 인스턴스의 이름 (예: MSSQLSERVER)입니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>보고 서버의 포트에서 인바운드 트래픽을 사용 하도록 설정 하려면 보고서 컴퓨터에 예외를 추가 해야 합니다 (기본 포트는 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>데이터베이스 이름</strong></p></td>
   <td align="left"><p>준수 및 감사 데이터베이스의 이름입니다. 기본적으로 데이터베이스 이름은 <strong> mbam 준수 상태 이지만 </strong> 준수 및 감사 데이터베이스를 구성할 때 이름을 변경할 수 있습니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>이전 버전의 MBAM에서 업그레이드 하는 경우 이전 배포에 사용 된 이름과 동일한 데이터베이스 이름을 사용 해야 합니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>준수 및 감사 데이터베이스 도메인 계정</strong></p></td>
   <td align="left"><p>도메인 사용자 계정 및 암호를 사용 하 여 규정 준수 및 감사 데이터베이스에 액세스 합니다.</p>
   <p><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 한 값이 사용자 인 경우 </strong> <strong> </strong> 에는이 필드에 같은 값을 입력 해야 합니다.</p>
   <p><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 하는 값이 </strong> <strong> 그룹인 경우 </strong> 이 필드에 입력 하는 값은 해당 그룹의 구성원 이어야 합니다.</p>
   <p>이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다. 사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</p></td>
   </tr>
   </tbody>
   </table>



5. 항목을 모두 마쳤으면 **다음**을 클릭 합니다.

   마법사에서 보고서 기능에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.

6. **Next**(다음)를 클릭하여 계속합니다.

7. **요약** 페이지에서 추가 되는 기능을 검토 합니다.

   **참고**  
   방금 만든 항목의 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기를**클릭 한 다음 스크립트를 저장 합니다.



8. **추가** 를 클릭 하 여 서버에 보고서를 추가한 다음 **닫기를**클릭 합니다.



## 관련 항목


[서버 이벤트 로그](server-event-logs.md)

[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)

[MBAM 2.5 웹 응용 프로그램을 구성하는 방법](how-to-configure-the-mbam-25-web-applications.md)

[MBAM 2.5 서버 기능 구성의 유효성 검사](validating-the-mbam-25-server-feature-configuration.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.






