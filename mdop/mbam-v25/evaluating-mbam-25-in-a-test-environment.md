---
title: 테스트 환경에서 MBAM 2.5 평가
description: 테스트 환경에서 MBAM 2.5 평가
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823153"
---
# 테스트 환경에서 MBAM 2.5 평가


이 항목에서는 독립 실행형 또는 System Center Configuration Manager 통합 토폴로지에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 평가 하도록 테스트 환경을 설정 하는 방법에 대해 설명 합니다.

## 독립 실행형 토폴로지를 사용 하 여 MBAM 2.5 평가


독립 실행형 토폴로지를 사용 하 여 MBAM을 평가 하려면 다음 표의 정보를 사용 하 여 MBAM 서버 소프트웨어를 설치한 다음 테스트 환경에서 MBAM 서버 기능을 구성 합니다.

**독립 실행형 토폴로지를 사용 하 여 MBAM 2.5을 평가 하려면**

1. MBAM을 설치 하기 전에 다음을 수행 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">작업</th>
   <th align="left">지침을 받을 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>필수 하드웨어, RAM 및 기타 사양을 확인 합니다.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Cmdlet을 사용 하 여 MBAM을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 합니다.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</a></p></td>
   </tr>
   </tbody>
   </table>



2. MBAM 서버 소프트웨어를 설치한 다음 원하는 기능을 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">작업</th>
   <th align="left">지침을 받을 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>MBAM 서버 기능을 구성 하려는 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">MBAM 2.5 데이터베이스를 구성하는 방법</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>보고서 기능을 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">MBAM 2.5 보고서를 구성하는 방법</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>웹 응용 프로그램을 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</a></p></td>
   </tr>
   </tbody>
   </table>



3. 클라이언트 컴퓨터에서 다음을 수행 합니다.

   1.  클라이언트 컴퓨터에 MBAM 클라이언트를 설치 합니다.

   2.  컴퓨터에 MBAM Gpo (그룹 정책 개체)를 적용 합니다.

   3.  다음 레지스트리 키를 설정 하 여 MBAM 클라이언트가 정기적인 간격으로 더 빠르게 절전 모드를 해제 하도록 합니다.

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **참고**  
       이러한 키는 약 MBAM 클라이언트를 종료 하므로 테스트 환경 에서만 이러한 레지스트리 키 설정을 사용 하는 것이 좋습니다.



   4.  **BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.

## System Center 2012 Configuration Manager 통합 토폴로지를 사용 하 여 MBAM 2.5 평가


Configuration Manager 통합 토폴로지를 사용 하 여 MBAM을 평가 하려면 다음 표의 정보를 사용 하 여 MBAM 서버 소프트웨어를 설치한 다음 테스트 환경에서 MBAM 서버 기능을 구성 합니다. 클라이언트 컴퓨터에 MBAM 클라이언트를 설치한 후에는 MBAM 클라이언트가 컴퓨터의 상태를 MBAM에 더 빠르게 보고 하도록 하는 추가 단계를 완료 합니다.

**System Center 2012 Configuration Manager 통합 토폴로지를 사용 하 여 MBAM 2.5을 평가 하려면**

1. MBAM을 설치 하기 전에 필수 구성 요소 소프트웨어 및 지원 되는 구성을 검토 하세요.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">작업</th>
   <th align="left">지침을 받을 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>필수 하드웨어, RAM 및 기타 사양을 확인 합니다.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Cmdlet을 사용 하 여 MBAM을 구성할 계획인 경우 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 합니다.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>.Mof 파일을 만들거나 편집 합니다.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Configuration.mof 파일 편집</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Sms_def.mof 파일 만들기 또는 편집</a></p></td>
   </tr>
   </tbody>
   </table>



2. MBAM 서버 소프트웨어를 설치한 다음 원하는 기능을 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">작업</th>
   <th align="left">지침을 받을 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>MBAM 서버 기능을 구성 하려는 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>Windows PowerShell 또는 내보낸 데이터 계층 응용 프로그램 (DAC) 패키지를 사용 하 여 원격 SQL Server 컴퓨터에 데이터베이스를 설치할 수 있습니다. DAC 패키지에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> 데이터 계층 응용 프로그램을 참조 </a> 하세요.</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">MBAM 2.5 데이터베이스를 구성하는 방법</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>보고서 기능을 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">MBAM 2.5 보고서를 구성하는 방법</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>웹 응용 프로그램을 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>System Center Configuration Manager를 구성 하 여 Configuration Manager 개체를 설치 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</a></p></td>
   </tr>
   </tbody>
   </table>



3. 클라이언트 컴퓨터에서 다음을 수행 합니다.

   1.  클라이언트 컴퓨터에 MBAM 클라이언트와 Configuration Manager 클라이언트를 설치 합니다.

   2.  컴퓨터에 MBAM 그룹 정책 개체를 적용 합니다.

   3.  다음 레지스트리 키를 설정 하 여 MBAM 클라이언트가 정기적인 간격으로 더 빠르게 절전 모드를 해제 하도록 합니다.

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **참고**  
       이러한 키는 약 MBAM 클라이언트를 종료 하므로 테스트 환경 에서만 이러한 레지스트리 키 설정을 사용 하는 것이 좋습니다.



   4.  **BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.

   5.  제어판에서 **구성 관리자**를 연 다음 **작업** 탭을 클릭 합니다.

   6.  **하드웨어 인벤토리 주기**를 선택한 다음 **지금 실행**을 클릭 합니다. 이 단계에서는 .mof 파일로 가져온 새 클래스를 사용 하 여 하드웨어 인벤토리를 실행 한 다음 데이터를 Configuration Manager 서버로 보냅니다.

   7.  **컴퓨터 정책 검색 & 평가 주기**를 선택한 다음 **지금 실행** 을 클릭 하 여 해당 클라이언트 컴퓨터와 관련 된 그룹 정책 개체를 적용 합니다.



4. Configuration Manager 콘솔에서 다음을 수행 합니다.

   1.  탐색 창에서 **Mbam 지원 컴퓨터**를 마우스 오른쪽 단추로 클릭 하 고 **구성원 업데이트**를 클릭 한 다음 **예** 를 클릭 하 여 클라이언트 컴퓨터가 구성원 자격을 즉시 보고 하도록 합니다.

   2.  탐색 창에서 **Mbam (지원 되는 컴퓨터** )을 클릭 하 여 클라이언트 컴퓨터가 컬렉션에 표시 되는지 확인 합니다.

5. 클라이언트 컴퓨터의 제어판에서 **구성 관리자** 를 다시 열고 다음을 수행 합니다.

   1.  **동작** 탭을 클릭 한 다음 **컴퓨터 정책 검색 & 평가 주기**를 다시 실행 합니다.

   2.  **구성** 탭을 클릭 하 고 BitLocker 기준을 선택한 다음 **평가**를 클릭 합니다.

6. Configuration Manager 콘솔에서 다음과 같이 엔터프라이즈 준수 보고서에 클라이언트 컴퓨터가 표시 되는지 확인 합니다.

   1.  탐색 창에서 **모니터링** 작업 영역을 선택 합니다.

   2.  콘솔 트리에서 " **개요** &gt; **보고** &gt; **보고서** " &gt; **mbam**을 확장 합니다.

   3.  보고서를 표시할 언어를 나타내는 폴더를 선택한 다음 결과 창에서 보고서를 선택 합니다.

## System Center Configuration Manager 2007 통합 토폴로지를 사용 하 여 MBAM 2.5 평가


Configuration Manager 통합 토폴로지를 사용 하 여 MBAM을 평가 하려면 프로덕션 환경에서 사용 하는 것과 동일한 단계를 따라 테스트 환경에 MBAM을 설치 하 고 구성 합니다. 클라이언트 컴퓨터에 MBAM 클라이언트를 설치한 후에이 항목의 추가 단계를 완료 하 여 MBAM 클라이언트가 컴퓨터의 상태를 MBAM에 더 빠르게 보고 하도록 설정할 수 있습니다.

**Configuration Manager 2007 통합 토폴로지를 사용 하 여 MBAM을 평가 하려면**

1. MBAM을 설치 하기 전에 다음을 수행 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">작업</th>
   <th align="left">지침을 받을 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>필수 구성 요소 소프트웨어를 모두 설치 했는지 확인 합니다.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Configuration Manager 통합 토폴로지에만 적용되는 MBAM 2.5 서버 필수 구성 요소</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>필수 하드웨어, RAM 및 기타 사양을 확인 합니다.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>.Mof 파일을 만들거나 편집 합니다.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Configuration.mof 파일 편집</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Sms_def.mof 파일 만들기 또는 편집</a></p></td>
   </tr>
   </tbody>
   </table>



2. MBAM 서버 소프트웨어를 설치한 다음 원하는 기능을 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">작업</th>
   <th align="left">지침을 받을 위치</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>MBAM 서버 기능을 구성 하려는 각 서버에 MBAM 서버 소프트웨어를 설치 합니다.</p>
   <div class="alert">
   <strong>참고</strong><br/><p>Windows PowerShell 또는 내보낸 데이터 계층 응용 프로그램 (DAC) 패키지를 사용 하 여 원격 SQL Server 컴퓨터에 데이터베이스를 설치할 수 있습니다. DAC 패키지에 대 한 자세한 내용은 <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> 데이터 계층 응용 프로그램을 참조 </a> 하세요.</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">MBAM 2.5 서버 소프트웨어 설치</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">MBAM 2.5 데이터베이스를 구성하는 방법</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>보고서 기능을 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">MBAM 2.5 보고서를 구성하는 방법</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>웹 응용 프로그램을 구성 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>System Center Configuration Manager를 구성 하 여 Configuration Manager 개체를 설치 합니다.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">MBAM 2.5 System Center Configuration Manager 통합을 구성하는 방법</a></p></td>
   </tr>
   </tbody>
   </table>



3. 클라이언트 컴퓨터에서 다음을 수행 합니다.

   1.  클라이언트 컴퓨터에 MBAM 클라이언트를 설치 합니다.

   2.  컴퓨터에 MBAM 그룹 정책 개체를 적용 합니다.

   3.  다음 레지스트리 키를 설정 하 여 MBAM 클라이언트가 더 빨리 종료 되 고 더 빠른 간격으로 절전 모드를 해제 합니다.

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **참고**  
       이러한 키는 기본적으로 약 MBAM 클라이언트를 사용 하기 때문에 평가 환경 에서만 이러한 레지스트리 키 설정을 사용할 것을 권장 합니다.



   4.  **BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.

   5.  제어판에서 **구성 관리자**를 연 다음 **작업** 탭을 클릭 합니다.

   6.  **컴퓨터 정책 검색 & 평가 주기**를 선택한 다음 **지금 실행** 을 클릭 하 여 해당 클라이언트 컴퓨터와 관련 된 그룹 정책 개체를 적용 합니다.

   7.  **하드웨어 인벤토리 주기**를 선택한 다음 **지금 실행**을 클릭 합니다. 이 단계에서는 .mof 파일로 가져온 새 클래스를 사용 하 여 하드웨어 인벤토리를 실행 한 다음 데이터를 Configuration Manager 서버로 보냅니다.

4. Configuration Manager 콘솔에서 다음을 수행 합니다.

   1.  탐색 창에서 **Mbam 지원 컴퓨터**를 마우스 오른쪽 단추로 클릭 하 고 **구성원 업데이트**를 클릭 한 다음 **예** 를 클릭 하 여 클라이언트 컴퓨터가 구성원 자격을 즉시 보고 하도록 합니다.

   2.  탐색 창에서 **Mbam (지원 되는 컴퓨터** )을 클릭 하 여 클라이언트 컴퓨터가 컬렉션에 표시 되는지 확인 합니다.

5. 클라이언트 컴퓨터의 제어판에서 **구성 관리자** 를 다시 열고 다음을 수행 합니다.

   1.  **동작** 탭을 클릭 한 다음 **컴퓨터 정책 검색 & 평가 주기**를 다시 실행 합니다.

   2.  **구성** 탭을 클릭 하 고 BitLocker 기준선을 선택한 다음 **평가**를 클릭 합니다.

6. Configuration Manager 콘솔에서 다음과 같이 엔터프라이즈 준수 보고서에 클라이언트 컴퓨터가 표시 되는지 확인 합니다.

   1.  탐색 창에서 **컴퓨터 관리** &gt; **reporting** &gt; **Services** &gt; ** &lt; 서버 이름 &gt; mbam**을 확장 합니다.

   2.  **Mbam** 노드 내에서 보고서를 볼 언어를 나타내는 폴더를 선택한 다음 결과 창에서 보고서를 선택 합니다.


## 관련 항목


[MBAM 2.5 시작](getting-started-with-mbam-25.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.





