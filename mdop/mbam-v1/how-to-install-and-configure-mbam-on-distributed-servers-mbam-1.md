---
title: 분산 서버에서 MBAM을 설치 및 구성하는 방법
description: 분산 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825658"
---
# 분산 서버에서 MBAM을 설치 및 구성하는 방법


이 항목의 절차에서는 분산 서버의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능을 모두 설치 하는 방법에 대해 설명 합니다.

각 서버 기능에는 특정 필수 구성 요소가 있습니다. 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요. 또한 일부 기능을 설치 하는 동안 특정 정보를 제공 해야 기능을 성공적으로 배포할 수 있습니다.

**참고**  
설치 로그 파일을 얻으려면 **msiexec** 패키지 및 **/l &lt; 위치 &gt; ** 옵션을 사용 하 여 mbam을 설치 해야 합니다. 로그 파일은 사용자가 지정한 위치에 만들어집니다.

추가 설치 로그 파일은 MBAM 설치를 실행 하는 사용자 의% temp% 폴더에 만들어집니다.



## <a href="" id="deploy-the-mbam-server-features-"></a>MBAM 서버 기능 배포


다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.

**참고**  
32 비트 서버와 64 비트 서버에서 64 비트 설정으로 32 비트 설치를 사용 해야 합니다.



**MBAM 서버 기능을 배포 하려면**

1.  MBAM 설치 마법사를 시작 하 고 시작 페이지에서 **설치** 를 클릭 합니다.

2.  Microsoft 소프트웨어 사용 조건을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

3.  기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다. 다른 곳에 설치 하려는 기능을 선택 취소 합니다. 동일한 컴퓨터에 설치 하려는 기능은 모두 동시에 설치 해야 합니다. MBAM 기능은 다음 순서로 설치 해야 합니다.

    -   복구 및 하드웨어 데이터베이스

    -   준수 및 감사 데이터베이스

    -   준수 감사 및 보고서

    -   관리 및 모니터링 서버

    -   MBAM 그룹 정책 서식 파일

    **참고**  
    설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다. 모든 필수 조건이 충족 되 면 설치가 계속 됩니다. 누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다. 이 시간에 모든 전제 조건이 충족 되 면 설치가 다시 시작 됩니다.



4.  MBAM 설정 마법사가 선택한 기능에 대 한 설치 페이지를 표시 합니다. 다음 섹션에서는 각 기능에 대 한 설치 절차에 대해 설명 합니다.

    **참고**  
    일반적으로 각 기능은 별도의 서버에 설치 됩니다. 단일 서버에 여러 기능을 설치 하려는 경우 다음 단계 중 일부를 변경 하거나 제거할 수 있습니다.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.

6. 선택한 MBAM 기능 정보가 완료 되 면 설치 마법사를 사용 하 여 MBAM 설치를 시작할 준비가 된 것입니다. 설치 설정을 검토 하거나 변경 해야 하는 경우 마법사를 이동 하려면 **뒤로** 를 클릭 합니다. 설치를 **클릭 하 여 설치를 시작** 합니다. 마법사를 종료 하려면 **취소** 를 클릭 합니다. 설치 프로그램이 사용자가 선택한 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.

7. **마침을** 클릭 하 여 마법사를 종료 합니다.

8. MBAM 서버 기능이 설치 된 후 적절 한 MBAM 역할에 사용자를 추가 합니다. 자세한 내용은 [MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)을 참조 하세요.

**설치 후 구성**

1.  MBAM 설정이 완료 되 면 사용자가 MBAM 관리 웹 사이트의 기능에 액세스할 수 있으려면 먼저 사용자 역할을 추가 해야 합니다. 관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 합니다.

    -   **Mbam 하드웨어 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 하드웨어 기능에 액세스할 수 있습니다.

    -   **Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 드라이브 복구 및 TPM (신뢰할 수 있는 플랫폼 모듈) 기능을 관리 하는 방법에 액세스할 수 있습니다. 드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.

    -   **Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다. 고급 헬프데스크 사용자의 경우 드라이브 복구에 키 ID 필드만 필요 합니다. TPM 관리에서 컴퓨터 도메인 필드 및 컴퓨터 이름 필드만 필요 합니다.

2.  관리 및 모니터링 서버, 준수 및 감사 데이터베이스에서 준수 및 감사 보고서를 호스팅하는 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 웹 사이트의 보고서 기능에 대 한 액세스 권한을 부여 합니다.

    -   **Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 mbam 관리 웹 사이트의 보고서에 액세스할 수 있습니다.

    **참고**  
    **Mbam 보고서** 의 동일한 사용자 또는 그룹 구성원 자격을 가진 모든 컴퓨터에서 Mbam 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 설치 되어 있어야 합니다.



## MBAM 서버 기능 설치의 유효성을 검사 합니다.


MBAM 서버 기능 설치가 완료 되 면 해당 설치가 MBAM에 대해 필요한 모든 기능을 성공적으로 설정 했는지 확인 해야 합니다. 다음 절차를 사용 하 여 MBAM 서비스가 작동 하는지 확인 합니다.

**MBAM 설치의 유효성을 검사 하려면**

1. MBAM 기능이 배포 되는 각 서버에서 **제어판**을 열고 **프로그램**을 클릭 한 다음 **프로그램 및 기능**을 클릭 합니다. **Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.

   **참고**  
   MBAM 설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.



2. 복구 및 하드웨어 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.

3. 준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태** 데이터베이스가 설치 되어 있는지 확인 합니다.

4. 준수 및 감사 보고서가 설치 된 서버에서 관리자 권한이 있는 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.

   SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.에서 찾을 수 있습니다. 실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.

   **몰타 호환성 보고서** 가 나열 되어 있고 다섯 개의 보고서와 하나의 데이터 원본을 포함 하 고 있는지 확인 합니다.

   **참고**  
   SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; srsinstancename &gt; *



5. 관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾아 **웹 서버 (IIS)** 를 선택한 다음 **iis (인터넷 정보 서비스) 관리자**를 클릭 합니다. **연결** 에서 * &lt; computername &gt; *으로 이동 하 고 **사이트**를 클릭 한 다음 **Microsoft BitLocker 관리 및 모니터링**을 클릭 합니다. **MBAMAdministrationService**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되는지 확인 합니다.

6. 관리 및 모니터링 기능이 설치 된 서버에서 관리자 권한으로 웹 브라우저를 열고 MBAM 웹 사이트에서 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.

   -   *http:// &lt; computername &gt; /default.aspx* 및 탐색 및 보고서에 대 한 각 링크 확인

   -   *http:// &lt; computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **참고**  
   일반적으로 서비스는 네트워크 암호화 없이 기본 포트 80에 설치 됩니다. 서비스가 다른 포트에 설치 되어 있는 경우 해당 포트를 포함 하도록 Url을 변경 합니다. 예를 들어 http://* &lt; computername &gt; : &lt; port &gt; */default.aspx 또는 http:// <em> &lt; hostheadername &gt; / </em> default.aspx

   네트워크 암호화를 사용 하 여 서비스를 설치한 경우 http://를 https://로 변경 합니다.



~~~
Verify that each web page loads successfully.
~~~

## 관련 항목


[MBAM 1.0 서버 인프라 배포](deploying-the-mbam-10-server-infrastructure.md)









