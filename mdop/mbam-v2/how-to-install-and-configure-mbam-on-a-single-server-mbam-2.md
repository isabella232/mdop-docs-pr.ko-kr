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
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824068"
---
# 단일 서버에서 MBAM을 설치 및 구성하는 방법


이 항목의 절차에서는 단일 서버의 독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하는 방법에 대해 설명 합니다. 단일 서버 구성은 테스트 환경 에서만 사용 합니다. 프로덕션 환경의 경우 두 개 이상의 서버를 사용 합니다. Configuration Manager 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 하는 경우 [구성 관리자를 사용 하 여 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)를 참조 하세요.

다음 다이어그램에서는 단일 서버 아키텍처의 예를 보여 줍니다. 데이터베이스 및 기능에 대 한 설명은 [MBAM 2.0의 상위 수준 아키텍처](high-level-architecture-for-mbam-20-mbam-2.md)를 참조 하세요.

![mbam 2 단일 서버 배포 토폴로지](images/mbam2-1-server.gif)

각 서버 기능에는 특정 필수 구성 요소가 있습니다. 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md) 및 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요. 또한 일부 기능에는 설치 프로세스가 기능을 성공적으로 배포 하는 동안 제공 해야 하는 정보가 있습니다. MBAM 배포를 시작 하기 전에 [mbam 2.0에 대 한 환경 준비](preparing-your-environment-for-mbam-20-mbam-2.md) 도 검토 해야 합니다.

**참고**  
설치 로그 파일을 얻으려면 Msiexec package와/L location 옵션을 사용 하 여 **/L** &lt; &gt; mbam을 설치 합니다. 로그 파일은 사용자가 지정한 위치에 만들어집니다.

추가 설치 로그 파일은 MBAM을 설치 하는 사용자 서버의% temp% 폴더에 만들어집니다.



## 단일 서버에 MBAM 서버 기능을 설치 하려면


다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.

**MBAM 서버 기능 설치를 시작 하려면**

1.  MBAM을 설치 하려는 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.

2.  **시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

4.  **토폴로지 선택** 페이지에서 **독립 실행형** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.

5.  **설치할 기능 선택** 페이지에서 설치할 기능을 선택 합니다. 기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다. 같은 컴퓨터에 설치할 기능을 동시에 함께 설치 해야 합니다. 다른 곳에 설치 하려는 기능에 대 한 확인란의 선택을 취소 합니다. 다음과 같은 순서로 MBAM 기능을 설치 해야 합니다.

    -   복구 데이터베이스

    -   준수 및 감사 데이터베이스

    -   규정 준수 및 감사 보고서

    -   셀프 서비스 서버

    -   관리 및 모니터링 서버

    -   MBAM 그룹 정책 서식 파일

    **참고**  
    설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다. 모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다. 누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다. 이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.



6.  **네트워크 통신 보안 구성** 페이지에서 관리 및 모니터링 서버와 클라이언트의 웹 서비스 간 통신을 암호화할지 여부를 선택 합니다. 통신을 암호화 하기로 결정 한 경우 암호화에 사용할 인증 기관 프로 비전 된 인증서를 선택 합니다. 이 단계를 수행 하기 전에 인증서를 만들어이 페이지에서 선택할 수 있도록 해야 합니다.

    **참고**  
    이 페이지는 **설치할 기능 선택** 페이지에서 셀프 서비스 포털 또는 관리 및 모니터링 서버 기능을 선택한 경우에만 표시 됩니다.



7.  **다음**을 클릭 하 고 다음 단계 집합을 계속 진행 하 여 Mbam 서버 기능을 구성 합니다.

**MBAM 서버 기능을 구성 하려면**

1.  **복구 데이터베이스 구성** 페이지에서 SQL Server 인스턴스 이름 및 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다. 또한 데이터베이스 파일의 위치와 로그 정보가 위치할 위치를 모두 지정 해야 합니다.

2.  **Next**(다음)를 클릭하여 계속합니다.

3.  **준수 및 감사 데이터베이스 구성** 페이지에서 SQL Server 인스턴스 이름과 규정 준수 및 감사 데이터를 저장할 데이터베이스의 이름을 지정 합니다. 또한 데이터베이스 파일을 어디에 저장 하 고 로그 정보가 어디에 있는지 지정 해야 합니다.

4.  **Next**(다음)를 클릭하여 계속합니다.

5.  준수 및 감사 **보고서 구성** 페이지에서 준수 및 감사 보고서가 설치 될 SQL Server Reporting Services 인스턴스를 지정 하 고 규정 준수 및 감사 데이터베이스에 액세스 하기 위한 도메인 사용자 계정 및 암호를 제공 합니다. 이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다. 사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.

6.  **Next**(다음)를 클릭하여 계속합니다.

7.  **셀프 서비스 포털 구성** 페이지에서 셀프 서비스 포털의 포트 번호, 호스트 이름, 가상 디렉터리 이름, 설치 경로를 입력 합니다.

    **참고**  
    고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다. Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.



8.  **Next**(다음)를 클릭하여 계속합니다.

9.  Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다. 이 경우 Windows의 자동 업데이트는 설정 되지 않습니다.

10. **관리 및 모니터링 서버 구성** 페이지에서 지원 센터 웹 사이트의 포트 번호, 호스트 이름, 가상 디렉터리 이름, 설치 경로를 입력 합니다.

    **참고**  
    고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다. Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.



11. **설치 요약** 페이지에서 설치할 기능 목록을 검토 하 고 **설치** 를 클릭 하 여 mbam 기능 설치를 시작 합니다. 설치 설정을 검토 하거나 변경 해야 하는 경우 **뒤로** 를 클릭 하 여 마법사를 뒤로 이동 하거나 **취소** 를 클릭 하 여 설치를 종료 합니다. 설치 프로그램이 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.

12. **마침을** 클릭 하 여 마법사를 종료 합니다. Microsoft BitLocker 관리 및 모니터링 서버 기능을 설치한 후에는 다음 섹션으로 이동 하 여 Microsoft BitLocker 관리 및 모니터링 역할에 사용자를 추가 하는 단계를 완료 합니다. 역할에 대 한 자세한 내용은 [MBAM 2.0 관리자 역할 계획](planning-for-mbam-20-administrator-roles-mbam-2.md)을 참조 하세요.

**설치 후 구성을 수행 하려면**

1.  관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 지원 센터 웹 사이트 기능에 대 한 액세스 권한을 부여 합니다.

    -   **Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 액세스할 수 있습니다. 드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.

    -   **Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다. 고급 헬프데스크 사용자의 경우 드라이브 복구에 **키 ID** 필드만 필요 합니다. TPM 관리에서 **컴퓨터 도메인** 필드 및 **컴퓨터 이름** 필드만 필요 합니다.

2.  관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 및 모니터링 웹 사이트의 보고서 기능에 액세스할 수 있도록 합니다.

    -   **Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트의 보고서 기능에 액세스할 수 있습니다.

    -   회사 이름, 고 지 사항 텍스트 및 기타 회사 관련 정보를 사용 하 여 셀프 서비스 포털에 브랜드를 지정 합니다. 자세한 내용은 [셀프 서비스 포털을 브랜딩 하는 방법](how-to-brand-the-self-service-portal.md)을 참조 하세요.

    **참고**  
    **Mbam 보고서** 의 동일한 사용자 또는 그룹 구성원 자격 사용자 로컬 그룹은 Mbam 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 준수 및 감사 보고서가 설치 된 모든 컴퓨터에서 유지 되어야 합니다. 이 작업을 수행 하는 데 권장 되는 방법은 도메인 보안 그룹을 만들고 해당 도메인 그룹을 각 로컬 MBAM 보고서 사용자 그룹에 추가 하는 것입니다. 이 프로세스를 사용 하는 경우 도메인 그룹을 통해 그룹 구성원 자격을 관리 합니다.



## MBAM 서버 기능 설치 유효성 검사


Microsoft BitLocker 관리 및 모니터링 설치가 완료 되 면 설치 시 BitLocker 관리에 필요한 모든 필요한 MBAM 기능을 성공적으로 설정 했는지 확인 합니다. 다음 절차를 사용 하 여 MBAM 서비스가 작동 하는지 확인 합니다.

**MBAM 서버 기능 설치의 유효성을 검사 하려면**

1. MBAM 기능이 배포 된 각 서버에서 **제어판**을 엽니다. **프로그램**을 선택한 다음 **프로그램 및 기능**을 선택 합니다. **Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.

   **참고**  
   설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.



2. 복구 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.

3. 준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태 데이터베이스가** 설치 되어 있는지 확인 합니다.

4. 준수 및 감사 보고서가 설치 된 서버에서 관리 자격 증명으로 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.

   SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.입니다. 실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.

   Microsoft BitLocker 관리 및 모니터링 이라는 보고서 폴더에 **MaltaDataSource** 이라는 데이터 원본이 포함 되어 있고 **en-us** 폴더에 4 개의 보고서가 포함 되어 있는지 확인 합니다.

   **참고**  
   SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 해야 합니다. http://* &lt; NameofMBAMReportsServer &gt; */Reportent\_* &lt; srsinstancename &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. 관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾습니다. **웹 서버 (iis)** 를 선택한 다음 **Iis (인터넷 정보 서비스) 관리자를 클릭 합니다.**

6. **연결** 에서 * &lt; computername &gt; *으로 이동 하 여 **사이트**를 선택한 다음 **Microsoft BitLocker 관리 및 모니터링**을 선택 합니다. **MBAMAdministrationService**, **mbamusersupportservice**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되어 있는지 확인 합니다.

7. 관리 및 모니터링 기능 및 셀프 서비스 포털이 설치 되어 있는 서버에서 관리 자격 증명을 사용 하는 웹 브라우저를 열고 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.

   -   *http:// &lt; 호스트 이름 &gt; /HelpDesk/default.aspx* 및 탐색 및 보고서에 대 한 각 링크 확인

   -   *http:// &lt; hostname &gt; /SelfService&gt;/*

   -   *http:// &lt; computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **참고**  
   네트워크 암호화 없이 기본 포트에 서버 기능이 설치 되어 있다고 가정 합니다. 다른 포트 또는 가상 디렉터리에 서버 기능을 설치한 경우 *http:// &lt; hostname &gt; : &lt; port &gt; /HelpDesk/default.asp*x 또는*http:// &lt; hostname &gt; : &lt; port &gt; / &lt; virtualdirectory &gt; /default.aspx* 와 같이 해당 포트를 포함 하도록 url을 변경 합니다.

   네트워크 암호화를 사용 하 여 서버 기능을 설치한 경우 http://을 https://로 변경 합니다.



## 관련 항목


[MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









