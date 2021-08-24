---
title: 단일 서버에서 MBAM을 설치 및 구성하는 방법
description: 단일 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4dffe2e2dcb82866b86a3ac281aca8a0dcaab686
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910663"
---
# <a name="how-to-install-and-configure-mbam-on-a-single-server"></a>단일 서버에서 MBAM을 설치 및 구성하는 방법


이 항목의 절차에서는 단일 서버에 독립 실행형 토폴로지에서 Microsoft BitLocker 관리 및 모니터링(MBAM)을 설치하는 방법을 설명합니다. 테스트 환경에서만 단일 서버 구성을 사용 합니다. 프로덕션 환경의 경우 둘 이상의 서버를 사용합니다. Configuration Manager 토폴로지로 Microsoft BitLocker 관리 및 모니터링을 설치하는 경우 Configuration Manager를 사용하여 [MBAM 배포를 참조합니다.](deploying-mbam-with-configuration-manager-mbam2.md)

다음 다이어그램은 단일 서버 아키텍처의 예를 보여줍니다. 데이터베이스 및 기능에 대한 설명은 [High-Level Architecture for MBAM 2.0을 참조하세요.](high-level-architecture-for-mbam-20-mbam-2.md)

![mbam 2 단일 서버 배포 토폴로지](images/mbam2-1-server.gif)

각 서버 기능에는 특정 선행 조건이 있습니다. 선행 조건 및 하드웨어 및 소프트웨어 요구 사항을 충족하는지 확인하려면 [MBAM 2.0 배포](mbam-20-deployment-prerequisites-mbam-2.md) 선행 조건 및 [MBAM 2.0 지원되는 구성을 참조하세요.](mbam-20-supported-configurations-mbam-2.md) 또한 일부 기능에는 설치 프로세스 중에 기능을 성공적으로 배포하기 위해 제공해야 하는 정보도 있습니다. 또한 MBAM 배포를 시작하기 전에 [MBAM 2.0에](preparing-your-environment-for-mbam-20-mbam-2.md) 대한 환경 준비를 검토해야 합니다.

**참고**  
설치 로그 파일을 얻습니다. Msiexec 패키지 및 **/L** 위치 옵션을 사용하여 &lt; &gt; MBAM을 설치해야 합니다. 지정한 위치에 로그 파일이 만들어집니다.

추가 설치 로그 파일은 MBAM을 설치하는 사용자의 서버의 %temp% 폴더에 만들어집니다.



## <a name="to-install-mbam-server-features-on-a-single-server"></a>단일 서버에 MBAM Server 기능을 설치하려면


다음 단계에서는 일반적인 MBAM 기능을 설치하는 방법을 설명합니다.

**MBAM Server 기능 설치를 시작해야 합니다.**

1.  MBAM을 설치하려는 서버에서 MBAM **** MBAMSetup.exe실행하여 MBAM 설치 마법사를 시작하십시오.

2.  시작 **페이지에서** 원하는 경우 사용자 환경 개선 **프로그램을**선택한 다음 시작 을 **클릭합니다.**

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음을** 클릭하여 설치를 계속합니다.

4.  **토폴로지 선택 페이지에서** **** 독립 실행형 토폴로지, 다음을 **클릭합니다.**

5.  설치할 **기능** 선택 페이지에서 설치할 기능을 선택합니다. 기본적으로 모든 MBAM 기능은 설치를 위해 선택되어 있습니다. 동일한 컴퓨터에 설치할 기능은 동시에 함께 설치해야 합니다. 다른 곳에 설치할 기능에 대한 확인란의 선택을 취소합니다. MBAM 기능은 다음 순서로 설치해야 합니다.

    -   복구 데이터베이스

    -   준수 및 감사 데이터베이스

    -   준수 및 감사 보고서

    -   Self-Service Server

    -   관리 및 모니터링 서버

    -   MBAM 그룹 정책 템플릿

    **참고**  
    설치 마법사는 설치의 선행 준비를 확인하고 누락된 선행 구성표를 표시됩니다. 모든 선행 구성이 충족될 경우 설치가 계속됩니다. 누락된 선행 조처가 감지되면 누락된 선행 문제를 해결한 다음 다시 선행 준비 상태 확인 을 **클릭해야 합니다.** 이번에는 모든 선행 구성이 충족되는 경우 설치가 다시 시작됩니다.



6.  네트워크 **통신 보안** 구성 페이지에서 관리 및 모니터링 서버의 웹 서비스와 클라이언트 간의 통신을 암호화할지 여부를 선택합니다. 통신을 암호화하기로 결정한 경우 암호화에 사용할 인증 기관 프로비전 인증서를 선택합니다. 이 페이지에서 선택할 수 있도록 이 단계 전에 인증서를 만들어야 합니다.

    **참고**  
    이 페이지는 설치할 기능 선택 페이지에서 Self-Service 포털 또는 관리 및 모니터링 서버 기능을 선택한 **경우만** 표시됩니다.



7.  **다음을**클릭하고 다음 단계 집합으로 계속하여 MBAM 서버 기능을 구성합니다.

**MBAM 서버 기능을 구성하기 위해**

1.  복구 **데이터베이스** 구성 페이지에서 복구 SQL Server 저장할 데이터베이스의 이름과 인스턴스 이름을 지정합니다. 또한 데이터베이스 파일이 있는 위치와 로그 정보가 있는 위치를 모두 지정해야 합니다.

2.  **Next**(다음)를 클릭하여 계속합니다.

3.  준수 **및** 감사 데이터베이스 구성 페이지에서 SQL Server 및 감사 데이터를 저장할 데이터베이스의 이름과 인스턴스 이름을 지정합니다. 또한 데이터베이스 파일의 위치와 로그 정보가 있는 위치를 지정해야 합니다.

4.  **Next**(다음)를 클릭하여 계속합니다.

5.  **준수** 및 감사 보고서 구성 페이지에서 준수 및 감사 SQL Server Reporting Services 설치할 SQL Server Reporting Services 인스턴스를 지정하고 준수 및 감사 데이터베이스에 액세스하기 위한 도메인 사용자 계정과 암호를 제공합니다. 만료되지 않는 계정의 암호를 구성합니다. 사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있습니다.

6.  **Next**(다음)를 클릭하여 계속합니다.

7.  Self-Service 포털 구성 **페이지에서** Self-Service 포털의 포트 번호, 호스트 이름, 가상 디렉터리 이름 및 설치 경로를 Self-Service.

    **참고**  
    고유한 호스트 헤더 이름을 지정하지 않는 한 지정하는 포트 번호는 관리 및 모니터링 서버에서 사용되지 않는 포트 번호입니다. 방화벽을 Windows 경우 포트가 자동으로 열립니다.



8.  **Next**(다음)를 클릭하여 계속합니다.

9.  Microsoft 업데이트를 사용하여 컴퓨터 보안을 유지할지 여부를 지정하고 다음 을 **클릭합니다.** 이렇게 해서 2016년 8월 2일부로 자동 업데이트가 Windows.

10. 관리 **및 모니터링** 서버 구성 페이지에서 지원 센터 웹 사이트의 포트 번호, 호스트 이름, 가상 디렉터리 이름 및 설치 경로를 입력합니다.

    **참고**  
    고유한 호스트 헤더 이름을 지정하지 않는 한 지정하는 포트 번호는 관리 및 모니터링 서버에서 사용되지 않는 포트 번호입니다. 방화벽을 Windows 경우 포트가 자동으로 열립니다.



11. 설치 **요약 페이지에서** 설치할 기능 목록을 검토하고 설치를 클릭하여 **** MBAM 기능 설치를 클릭합니다. 설치 **설정을** 검토하거나 변경해야 하는 경우 뒤로를 클릭하여 마법사를 통과하거나 취소를 클릭하여 설치를 종료합니다. **** 설치 프로그램이 MBAM 기능을 설치하고 설치가 완료되었습니다.

12. **마친을** 클릭하여 마법사를 종료합니다. Microsoft BitLocker 관리 및 모니터링 서버 기능을 설치한 후 다음 섹션을 계속 진행하고 Microsoft BitLocker 관리 및 모니터링 역할에 사용자를 추가해야 하는 단계를 완료합니다. 역할에 대한 자세한 내용은 [Planning for MBAM 2.0 Administrator Roles을 참조하십시오.](planning-for-mbam-20-administrator-roles-mbam-2.md)

**설치 후 구성을 수행하려면**

1.  관리 및 모니터링 서버에서 사용자를 다음 로컬 그룹에 추가하여 MBAM 지원 센터 웹 사이트 기능에 대한 액세스 권한을 부여합니다.

    -   **MBAM 헬프데스크 사용자:** 이 로컬 그룹의 구성원은 MBAM 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 액세스할 수 있습니다. 드라이브 복구 및 TPM 관리의 모든 필드는 Helpdesk 사용자에 대한 필수 필드입니다.

    -   **MBAM Advanced Helpdesk Users:** 이 로컬 그룹의 구성원은 MBAM 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 대한 고급 액세스 권한이 있습니다. 고급 헬프데스크 사용자의 경우 드라이브 복구에는 키 **ID** 필드만 필요합니다. TPM 관리에서 컴퓨터 도메인 **필드와** 컴퓨터 **이름** 필드만 필요합니다.

2.  관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가하여 사용자가 MBAM 관리 및 모니터링 웹 사이트의 보고서 기능에 액세스할 수 있도록 합니다.

    -   **MBAM 보고서 사용자:** 이 로컬 그룹의 구성원은 MBAM 관리 및 모니터링 웹 사이트의 보고서 기능에 액세스할 수 있습니다.

    -   회사 Self-Service, 알림 텍스트 및 기타 회사 관련 정보로 회사 포털을 브랜드합니다. 자세한 내용은 [How to Brand the Self-Service 참조하세요.](how-to-brand-the-self-service-portal.md)

    **참고**  
    MBAM 보고서의 동일한 사용자 또는 그룹 구성원 **MBAM** 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스 및 규정 준수 및 감사 보고서가 설치된 모든 컴퓨터에서 사용자 로컬 그룹을 유지 관리해야 합니다. 이렇게 하는 권장 방법은 도메인 보안 그룹을 만들고 각 로컬 MBAM 보고서 사용자 그룹에 해당 도메인 그룹을 추가하는 것입니다. 이 프로세스를 사용하는 경우 도메인 그룹을 통해 그룹 구성원을 관리합니다.



## <a name="validating-the-mbam-server-feature-installation"></a>MBAM Server 기능 설치 유효성 검사


Microsoft BitLocker 관리 및 모니터링 설치가 완료되면 설치 시 BitLocker 관리에 필요한 모든 MBAM 기능이 설정되어 있는지 검사합니다. 다음 절차에 따라 MBAM 서비스가 작동하고 있는지 확인할 수 있습니다.

**MBAM Server 기능 설치의 유효성을 검사하기 위해**

1. MBAM 기능이 배포된 각 서버에서 **제어판 을 열습니다.** 프로그램 **을**선택한 다음 프로그램 및 **기능을 선택합니다.** Microsoft **BitLocker 관리** 및 모니터링이 프로그램 및 기능 목록에 **나타나는지** 확인

   **참고**  
   설치의 유효성을 검사하려면 각 서버에 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용해야 합니다.



2. 복구 데이터베이스가 설치된 서버에서 복구 데이터베이스를 SQL Server Management Studio **MBAM** 복구 및 하드웨어 데이터베이스가 설치되어 있는지 확인합니다.

3. 준수 및 감사 데이터베이스가 설치된 서버에서 MBAM 준수 SQL Server Management Studio 열고 **MBAM** 준수 상태 데이터베이스가 설치되어 있는지 확인합니다.

4. 준수 및 감사 보고서가 설치된 서버에서 관리 자격 증명이 있는 웹 브라우저를 열고 해당 사이트의 "홈"을 SQL Server Reporting Services 합니다.

   SQL Server Reporting Services 인스턴스의 기본 홈 위치는 Http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports에 있습니다. 실제 URL을 찾으하려면 Reporting Services 구성 관리자 도구를 사용하여 설치 중에 지정된 인스턴스를 선택합니다.

   Microsoft BitLocker Administration and Monitoring이라는 Reports 폴더에 **MaltaDataSource라는** 데이터 원본이 포함되어 있으며 **en-us** 폴더에 4개의 보고서가 포함되어 있는지 확인합니다.

   **참고**  
   이름이 SQL Server Reporting Services 구성된 경우 URL은* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName과 &gt; * http:// 같습니다.



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. 관리 및 모니터링 기능이 설치된 서버에서 서버 **** 관리자를 실행하고 **역할 을 검색합니다.** 웹 **서버(IIS)를**선택한 다음 **IIS(인터넷 정보 서비스 관리자)를 클릭합니다.**

6. **연결에서** * &lt; &gt; 컴퓨터*이름 으로 를 찾아 **사이트**를 선택한 다음 **Microsoft BitLocker 관리 및 모니터링 을 선택합니다.** **MBAMAdministrationService,** **MBAMUserSupportService,** **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService가** 나열되어 있는지 확인

7. 관리 및 모니터링 기능 및 Self-Service 포털이 설치된 서버에서 관리 자격 증명이 있는 웹 브라우저를 열고 다음 위치로 이동하여 해당 기능이 성공적으로 로드되어 있는지 확인합니다.

   -   *http:// &lt; &gt; /HelpDesk/default.aspx를* 사용하여 탐색 및 보고서에 대한 각 링크를 확인

   -   *http:// &lt; &gt; /SelfService&gt;/*

   -   *&lt; &gt; http:///MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **참고**  
   네트워크 암호화 없이 서버 기능이 기본 포트에 설치된 것으로 가정합니다. 다른 포트 또는 가상 디렉터리에 서버 기능을 설치한 경우 적절한 포트를 포함하도록 URL을 *변경합니다(예: http:// &lt; 호스트 &gt; 이름: 포트 &lt; &gt; /HelpDesk/default.asp*x 또는 http://*호스트 &lt; &gt; 이름: port &lt; &gt; / &lt; virtualdirectory &gt; /default.aspx).*

   네트워크 암호화를 사용하여 서버 기능을 설치한 경우 네트워크 암호화를 http:// https://.



## <a name="related-topics"></a>관련 항목


[MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









