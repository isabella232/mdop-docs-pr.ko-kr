---
title: MBAM 2.5 웹 응용 프로그램을 구성하는 방법
description: MBAM 2.5 웹 응용 프로그램을 구성하는 방법
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824498"
---
# MBAM 2.5 웹 응용 프로그램을 구성하는 방법


이 항목에서는 다음 방법 중 하나를 사용 하 여 [mbam 2.5의 권장 상위 수준 아키텍처](high-level-architecture-for-mbam-25.md) 에 대해 Microsoft BitLocker 관리 및 모니터링 (mbam) 2.5 웹 응용 프로그램을 구성 하는 방법에 대해 설명 합니다.

-   Windows PowerShell cmdlet

-   MBAM 서버 구성 마법사

웹 응용 프로그램에는 다음 웹 사이트와 해당 웹 서비스가 구성 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Website</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>관리 및 모니터링 웹 사이트</p></td>
<td align="left"><p>지정 된 사용자가 보고서를 볼 수 있고 사용자가 PIN 또는 암호를 잊어버린 경우 컴퓨터를 복구 하는 데 도움이 되는 웹 사이트</p></td>
</tr>
<tr class="even">
<td align="left"><p>셀프 서비스 포털</p></td>
<td align="left"><p>자신의 PIN 또는 암호를 잊어버린 경우 최종 사용자가 개별적으로 액세스할 수 있는 웹 사이트의 컴퓨터에 대 한 액세스 권한 다시 가져오기</p></td>
</tr>
</tbody>
</table>



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
<td align="left"><p>각 서버에서 필수 구성 요소를 완성 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>관리 및 모니터링 웹 사이트를 구성 하기 전에 SSL (Secure Sockets layer)을 사용 하도록 SQL ServerReporting Services (SSRS)를 구성 해야 합니다. 그렇지 않으면 보고서 기능이 HTTPS 대신 HTTP를 사용 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2.5 구성 관리자 통합 토폴로지에만 적용 되는 서버 필수 구성 요소 </a> (해당 하는 경우)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>웹 사이트의 응용 프로그램 풀 계정에 대 한 Spn (서비스 사용자 이름)을 등록 합니다. AD DS (Active Directory 도메인 서비스)에 관리 도메인 권한이 없는 경우에만이 단계를 수행 해야 합니다. AD DS에 이러한 권한이 있으면 MBAM이 사용자를 위한 Spn을 만듭니다.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">MBAM 웹 사이트를 보호하는 방법 계획</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 서버 기능을 구성할 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>웹 사이트를 한 대의 서버에 설치 하는 경우에는 <strong> 사용-MbamWebApplication Windows PowerShell cmdlet을 사용 하는 것 으로만 구성할 수 있습니다 </strong> . MBAM 서버 구성 마법사는 별도의 서버에서 이러한 항목을 구성 하는 것을 지원 하지 않습니다.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlet을 사용 하 여 MBAM 서버 기능을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 조건을 검토 합니다.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</a></p></td>
</tr>
</tbody>
</table>



**Windows PowerShell을 사용 하 여 웹 응용 프로그램을 구성 하려면**

1.  구성을 시작 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.

2.  **Enable-MbamWebApplication** cmdlet을 사용 하 여 Windows PowerShell을 사용 하 여 웹 응용 프로그램을 구성 합니다. 이 cmdlet에 대 한 정보를 얻으려면 **Get-help Enable-MbamWebApplication**을 입력 합니다.

**마법사를 사용 하 여 모든 웹 응용 프로그램에 대 한 설정을 구성 하려면**

1. 웹 응용 프로그램을 구성할 서버에서 MBAM 서버 구성 마법사를 시작 합니다. **시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.

2. **새 기능 추가**를 클릭 하 **고 관리 및 모니터링 웹 사이트** 및 **셀프 서비스 포털**을 선택한 후 **다음**을 클릭 합니다. 마법사는 웹 응용 프로그램에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.

3. 필수 구성 요소 확인에 성공 하면 **다음** 을 클릭 하 여 계속 합니다. 그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 합니다.

4. 다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>필드</strong></th>
   <th align="left">설명</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>보안 인증서</strong></p></td>
   <td align="left"><p>이전에 만든 인증서를 선택 하 여 웹 사이트를 구성 하는 웹 서비스와 서버 간의 통신을 선택적으로 암호화 합니다. <strong>인증서 사용 안 함을 선택 하면 </strong> 웹 통신이 안전 하지 않을 수 있습니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>호스트 이름</strong></p></td>
   <td align="left"><p>웹 사이트를 구성 하는 호스트 컴퓨터의 이름입니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>설치 경로</strong></p></td>
   <td align="left"><p>웹 사이트를 설치 하는 경로입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>웹 사이트 및 서비스 통신에 사용 하는 포트 번호입니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>지정 된 포트를 통해 통신을 사용 하도록 설정 하려면 방화벽 예외를 설정 해야 합니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>웹 서비스 응용 프로그램 풀 도메인 계정 및 암호</strong></p></td>
   <td align="left"><p>웹 서비스 응용 프로그램 풀에 대 한 도메인 사용자 계정 및 암호입니다.</p>
   <p><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 사용자 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 같은 값을 입력 해야 합니다.</p>
   <p><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 그룹 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 입력 하는 값은 해당 그룹의 구성원 이어야 합니다.</p>
   <p>자격 증명을 지정 하지 않으면 이전에 사용 하도록 설정 된 웹 응용 프로그램에 대해 지정 된 자격 증명이 사용 됩니다. 모든 웹 응용 프로그램은 동일한 응용 프로그램 풀 자격 증명을 사용 해야 합니다. 여러 웹 응용 프로그램에 대해 다른 자격 증명을 지정 하는 경우 가장 최근에 지정 된 값이 사용 됩니다.</p>
   <div class="alert">
   <strong>중요</strong><br/><p>보안 향상을 위해 자격 증명에 지정 된 계정에 제한 된 사용자 권한을 설정 합니다. 또한 계정 암호가 만료 되지 않도록 설정 합니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. **인증 후** 기본 제공 IIS \ _IUSRS 계정이 나 응용 프로그램 풀 계정이 클라이언트 가장으로 추가 되었는지 확인 하 고 **일괄 작업으로 로그온** 로컬 보안 설정입니다.

   로컬 보안 설정에 추가 되었는지 여부를 확인 하려면 **로컬 보안 정책 편집기**를 열고, **로컬 정책** 노드를 확장 하 고, **사용자 권한 할당** 노드를 클릭 하 고, **인증 후 클라이언트로 가장** 을 두 번 클릭 하 고 권한으로 로그인 한 다음에는, **일괄 작업으로 로그온** 정책을 사용 합니다.

**마법사를 사용 하 여 데이터베이스에 대 한 연결 정보를 구성 하려면**

1.  마법사에서 준수 및 감사 데이터베이스에 대 한 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.

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
    <td align="left"><p><strong>SQL Server 이름</strong></p></td>
    <td align="left"><p>규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>SQL Server 데이터베이스 인스턴스</strong></p></td>
    <td align="left"><p>규정 준수 및 감사 데이터베이스가 구성 된 SQL Server 인스턴스 이름입니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>데이터베이스 이름</strong></p></td>
    <td align="left"><p>준수 및 감사 데이터베이스의 이름입니다.</p></td>
    </tr>
    </tbody>
    </table>



2.  복구 데이터베이스에 대 한 마법사에서 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.

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
    <td align="left"><p><strong>SQL Server 이름</strong></p></td>
    <td align="left"><p>복구 데이터베이스가 구성 된 서버의 이름입니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>SQL Server 데이터베이스 인스턴스</strong></p></td>
    <td align="left"><p>복구 데이터베이스가 구성 된 SQL Server 인스턴스 이름입니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>데이터베이스 이름</strong></p></td>
    <td align="left"><p>복구 데이터베이스의 이름입니다.</p></td>
    </tr>
    </tbody>
    </table>



**마법사를 사용 하 여 웹 응용 프로그램을 구성 하려면**

1. 마법사에서 필드 값을 입력 하 여 관리 및 모니터링 웹 사이트를 구성 하려면 다음 설명을 사용 합니다.

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
   <td align="left"><p><strong>고급 헬프데스크 역할 도메인 그룹</strong></p></td>
   <td align="left"><p>구성원이 보고서 영역을 제외한 관리 및 모니터링 웹 사이트의 모든 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>헬프데스크 역할 도메인 그룹</strong></p></td>
   <td align="left"><p>구성원이 <strong> </strong> <strong> </strong> 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>System Center Configuration Manager 통합 사용</strong></p></td>
   <td align="left"><p>Configuration Manager 통합 토폴로지에서 MBAM을 구성 하는 경우이 확인란을 선택 합니다. 이 확인란을 선택 하면 복구 감사 보고서를 제외한 모든 보고서가 관리 및 모니터링 웹 사이트 대신 구성 관리자에 표시 됩니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>보고 역할 도메인 그룹</strong></p></td>
   <td align="left"><p>구성원에 게 관리 및 모니터링 웹 사이트의 보고서 영역에 대 한 읽기 전용 액세스 권한이 있는 도메인 사용자 그룹입니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>SQL Server Reporting Services URL</strong></p></td>
   <td align="left"><p>MBAM 보고서가 구성 된 SSRS 서버의 URL입니다.</p>
   <p>보고서 Url의 예:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">호스트 이름 유형</th>
   <th align="left">예</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>정규화 된 도메인 이름의 예</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>사용자 지정 호스트 이름을 사용 하는 예제</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>가상 디렉터리</strong></p></td>
   <td align="left"><p>관리 및 모니터링 웹 사이트의 가상 디렉터리입니다. 이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당 하 고 웹 사이트의 호스트 이름 (예:)에 추가 됩니다.</p>
   <p>http (s)// &lt; <em> 호스트 이름 </em> &gt; : &lt; <em> 포트 </em> &gt; /HelpDesk/</p>
   <p>가상 디렉터리를 지정 하지 않으면 값 <strong> 헬프데스크를 </strong> 사용 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>데이터 마이그레이션 역할 도메인 그룹 </strong> (선택 사항)</p></td>
   <td align="left"><p>해당 멤버가이 끝점을 통해 복구 정보를 기록할 수 있는 액세스 권한이 있는 도메인 사용자 그룹입니다.</p></td>
   </tr>
   </tbody>
   </table>



2. 마법사에서 필드 값을 입력 하 여 셀프 서비스 포털을 구성 하려면 다음 설명을 사용 합니다.

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
   <td align="left"><p><strong>가상 디렉터리</strong></p></td>
   <td align="left"><p>웹 응용 프로그램의 가상 디렉터리입니다. 이 이름은 서버의 실제 디렉터리에 해당 하 고 웹 사이트의 호스트 이름에 추가 됩니다 (예:).</p>
   <p>http (s)// &lt; <em> 호스트 이름 </em> &gt; : &lt; <em> 포트 </em> &gt; /SelfService/</p>
   <p>가상 디렉터리를 지정 하지 않으면 <strong> SelfService 값 </strong> 이 사용 됩니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>회사 이름</p></td>
   <td align="left"><p>셀프 서비스 포털의 회사 이름을 지정 합니다 예:</p>
   <p>Contoso IT</p>
   <p>이 회사 이름은 모든 셀프 서비스 포털 사용자가 볼 수 있습니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>헬프 데스크 URL 텍스트</p></td>
   <td align="left"><p>사용자를 조직의 헬프데스크 웹 사이트로 연결 하는 텍스트 문을 지정 합니다 (예:).</p>
   <p>헬프데스크 또는 IT 부서에 문의</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>헬프데스크 URL</p></td>
   <td align="left"><p>조직의 헬프 데스크 웹 사이트 URL을 다음과 같이 지정 합니다.</p>
   <p>http (s)// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>주목 텍스트 파일</p></td>
   <td align="left"><p>셀프 서비스 포털 랜딩 페이지에서 사용자에 게 표시 하려는 알림이 포함 된 파일을 선택 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>사용자에 게 알림 텍스트 표시 안 함</p></td>
   <td align="left"><p>알림 텍스트가 사용자에 게 표시 되지 않도록 지정 하려면이 확인란을 선택 합니다.</p></td>
   </tr>
   </tbody>
   </table>



3. 항목을 모두 마쳤으면 **다음**을 클릭 합니다.

   마법사는 웹 응용 프로그램에 대 한 모든 필수 조건이 충족 되었는지 확인 합니다.

4. **Next**(다음)를 클릭하여 계속합니다.

5. **요약** 페이지에서 추가 되는 기능을 검토 합니다.

   **참고**  
   입력 한 항목에 대 한 Windows PowerShell 스크립트를 만들려면 **PowerShell 스크립트 내보내기** 및 스크립트 저장을 클릭 합니다.



6. **추가** 를 클릭 하 여 웹 응용 프로그램을 서버에 추가 하 고 **닫기를**클릭 합니다.

   사용자 지정 알림 텍스트, 회사 이름, 추가 정보에 대 한 포인터 등을 추가 하 여 셀프 서비스 포털을 사용자 지정 하려면 [조직에 대 한 셀프 서비스 포털 사용자 지정](customizing-the-self-service-portal-for-your-organization.md)을 참조 하세요.

**클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하려면**

1.  Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1을 실행 하 고 있는지 확인 합니다. 그럴 경우 아무 작업도 수행 하지 않습니다. 셀프 서비스 포털 구성이 완료 되었습니다.

    **참고**  
    Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1은 설치 프로그램에서 JavaScript 파일을 설치 하므로 셀프 서비스 포털을 구성 하기 위해 Microsoft Ajax 콘텐츠 배달 네트워크에 연결 하지 않아도 됩니다. 다음 단계는 SP1 이전 버전의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 사용 하는 경우에만 필요 합니다.



2.  클라이언트 컴퓨터에 Microsoft CDN (콘텐츠 배달 네트워크)에 대 한 액세스 권한이 있는지 확인 합니다.

    CDN은 특정 JavaScript 파일에 필요한 액세스 권한을 셀프 서비스 포털에 제공 합니다. 클라이언트 컴퓨터가 CDN에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하지 않은 경우에는 최종 사용자가 로그인 한 회사 이름과 계정만 표시 됩니다. 오류 메시지가 표시 되지 않습니다.

3.  다음 중 하나를 수행합니다.

    -   클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 있는 경우 아무 작업도 수행 하지 않습니다. 셀프 서비스 포털 구성이 완료 되었습니다.

    -   클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 없는 경우 [클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하는 방법](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)에 대 한 단계를 완료 합니다.


## 관련 항목


[서버 이벤트 로그](server-event-logs.md)

[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)

[클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[조직에 대한 셀프 서비스 포털 사용자 지정](customizing-the-self-service-portal-for-your-organization.md)

[MBAM 2.5 서버 기능 구성의 유효성 검사](validating-the-mbam-25-server-feature-configuration.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





