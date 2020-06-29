---
title: MBAM 2.5 서버 기능 구성의 유효성 검사
description: MBAM 2.5 서버 기능 구성의 유효성 검사
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827083"
---
# MBAM 2.5 서버 기능 구성의 유효성 검사


Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 서버 기능 배포를 완료 한 경우 모든 기능이 성공적으로 구성 되었는지 배포의 유효성을 검사 하는 것이 좋습니다. 배포한 토폴로지 (독립 실행형 또는 System Center Configuration Manager 통합)와 일치 하는 절차를 사용 합니다.

## 독립 실행형 토폴로지를 사용 하 여 MBAM 서버 배포 유효성 검사


다음 단계를 사용 하 여 단독 토폴로지로 MBAM 서버 배포의 유효성을 검사 합니다.

**독립 실행형 MBAM 서버 배포의 유효성을 검사 하려면**

1.  Mbam 기능이 배포 되는 각 서버에서 **제어판** &gt; **프로그램** 프로그램 &gt; **및 기능**을 클릭 합니다. **Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.

    **참고**  
    유효성 검사를 수행 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.



2.  복구 데이터베이스가 구성 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 구성 되어 있는지 확인 합니다.

3.  준수 및 감사 데이터베이스가 구성 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태 데이터베이스가** 구성 되어 있는지 확인 합니다.

4.  보고서 기능이 구성 된 서버에서 관리 자격 증명을 사용 하는 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.

    SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 다음과 같습니다.

    http (s)// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /Reports.aspx

    실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정한 인스턴스를 선택 합니다.

5.  **Microsoft BitLocker 관리 및 모니터링** 이라는 보고서 폴더에 **MaltaDataSource** 이라는 데이터 원본과 언어 폴더가 포함 되어 있는지 확인 합니다. 데이터 원본에는 언어를 나타내는 이름 (예: en-us)이 포함 된 폴더가 있습니다. 보고서는 언어 폴더에 있습니다.

    **참고**  
    SQL Server Reporting Services (SSRS)가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http (s)// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /reports\_ &lt; *SSRSInstanceName*&gt;



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. 관리 및 모니터링 웹 사이트 기능이 구성 된 서버에서 **서버 관리자**를 실행 하 고 **역할**을 찾은 다음 **웹 서버 (iis** ) &gt; **iis (인터넷 정보 서비스) 관리자**를 선택 합니다.

7. **연결**에서 * &lt; 컴퓨터 이름 &gt; * 으로 이동 하 여 **Sites** &gt; **Microsoft BitLocker 관리 및 모니터링**사이트를 선택 합니다. 다음이 나열 되는지 확인 합니다.

   -   **MBAMAdministrationService**

   -   **MBAMComplianceStatusService**

   -   **MBAMRecoveryAndHardwareService**

8. 관리 및 모니터링 웹 사이트와 셀프 서비스 포털이 구성 된 서버에서 관리 자격 증명을 사용 하 여 웹 브라우저를 엽니다.

9. 다음 웹 사이트를 탐색 하 여 성공적으로 로드 되었는지 확인 합니다.

   -   https// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /HelpDesk/-탐색 및 보고서에 대 한 각 링크 확인

   -   http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /SelfService/

   **참고**  
   네트워크 암호화 없이 기본 포트에서 서버 기능을 구성한 것으로 가정 합니다. 다른 포트 또는 가상 디렉터리에 서버 기능을 구성한 경우에는 다음과 같이 해당 포트를 포함 하도록 Url을 변경 합니다.

   http (s)// &lt; *호스트 이름* &gt; : &lt; *포트* &gt; /HelpDesk/

   http (s)// &lt; *호스트 이름* &gt; : &lt; *포트* &gt; / &lt; *virtualdirectory*&gt;/

   네트워크 암호화를 사용 하 여 서버 기능을 구성한 경우 http://를 https://로 변경 합니다.



10. 다음 웹 서비스를 찾아 제대로 로드 되었는지 확인 합니다. 서비스가 실행 중임을 나타내는 페이지가 열리고, 페이지에 메타 데이터가 표시 되지 않습니다.

    -   http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMAdministrationService/AdministrationService.svc

    -   http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMUserSupportService/UserSupportService.svc

    -   http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc

    -   http (s)// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc

## Configuration Manager 통합 토폴로지를 사용 하 여 MBAM 서버 배포 유효성 검사


다음 단계를 사용 하 여 Configuration Manager 통합 토폴로지로 MBAM 배포의 유효성을 검사 합니다. 사용 중인 구성 관리자 버전과 일치 하는 유효성 검사 단계를 완료 합니다.

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a>System Center 2012 구성 관리자를 사용 하 여 MBAM 서버 배포 유효성 검사

시스템 센터 2012 구성 관리자에서 MBAM을 사용 하는 경우 다음 단계를 사용 하 여 MBAM 서버 배포의 유효성을 검사 합니다.

**Configuration Manager 통합의 유효성을 검사 하려면 MBAM 서버 배포 – 시스템 센터 2012 구성 관리자**

1.  System Center 2012 구성 관리자가 배포 되는 서버에서 **제어판**의 **프로그램 및 기능** 을 열고 **Microsoft BitLocker 관리 및 모니터링** 이 표시 되는지 확인 합니다.

    **참고**  
    구성의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.



2.  Configuration Manager 콘솔에서 **자산 및 준수** 작업 영역 &gt; **디바이스 모음**을 클릭 하 고 **Mbam이 지원** 되는 컴퓨터 라는 새 컬렉션이 표시 되는지 확인 합니다.

3.  Configuration Manager 콘솔에서 **모니터링** 작업 영역 &gt; **보고** &gt; **보고서** ( &gt; **mbam**)를 클릭 합니다.

4.  **Mbam** 폴더에 다른 언어를 나타내는 이름을 가진 하위 폴더가 있고 각 언어 하위 폴더에 다음 보고서가 나열 되어 있는지 확인 합니다.

    -   BitLocker 컴퓨터 준수

    -   BitLocker 엔터프라이즈 준수 대시보드

    -   BitLocker 엔터프라이즈 준수 세부 정보

    -   BitLocker Enterprise 규정 준수 요약

5.  Configuration Manager 콘솔에서 **자산 및 준수** 작업 영역 &gt; **준수 설정** &gt; **구성 기준을**클릭 하 고 구성 기준 **BitLocker 보호가** 나열 되어 있는지 확인 합니다.

6.  Configuration Manager 콘솔에서 **자산 및 준수** 작업 영역 &gt; **준수 설정** &gt; **구성 항목**을 클릭 하 고 다음 새 구성 항목이 표시 되는지 확인 합니다.

    -   BitLocker 고정 데이터 드라이브 보호

    -   BitLocker 운영 체제 드라이브 보호

### Configuration Manager 2007를 사용 하 여 MBAM 서버 배포 유효성 검사

이 단계를 사용 하 여 구성 관리자 2007에서 MBAM을 사용 하는 경우 MBAM 서버 배포의 유효성을 검사할 수 있습니다.

**Configuration Manager 통합의 유효성을 검사 하려면 MBAM 서버 배포-구성 관리자 2007**

1.  Configuration Manager 2007을 배포한 서버에서 **제어판** 의 **프로그램 및 기능** 을 열고 **Microsoft BitLocker 관리 및 모니터링** 이 표시 되는지 확인 합니다.

    **참고**  
    구성의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.



2.  Configuration Manager 콘솔에서 **사이트 데이터베이스 &lt; SiteCode &gt;  -  &lt; ServerName &gt; , &lt; SiteName &gt; ), 컴퓨터 관리**를 차례로 클릭 하 고 **mbam 지원 컴퓨터** 라는 새 컬렉션이 표시 되는지 확인 합니다.

3.  Configuration Manager 콘솔에서 reporting **Reporting** &gt; **Services** &gt; ** \\\\ &lt; 서버 이름 &gt; ** 보고 &gt; **보고서 폴더** 를 클릭 &gt; **MBAM**합니다.

    **Mbam** 폴더에 다른 언어를 나타내는 이름을 가진 하위 폴더가 있고 각 언어 하위 폴더에 다음 보고서가 나열 되어 있는지 확인 합니다.

    -   BitLocker 컴퓨터 준수

    -   BitLocker 엔터프라이즈 준수 대시보드

    -   BitLocker 엔터프라이즈 준수 세부 정보

    -   BitLocker Enterprise 규정 준수 요약

4.  Configuration Manager 콘솔에서 **원하는 구성 관리** &gt; **구성 기준을**클릭 하 고 구성 기준 **BitLocker 보호가** 나열 되어 있는지 확인 합니다.

5.  Configuration Manager 콘솔에서 **원하는 구성 관리** &gt; **구성 항목**을 클릭 하 고 다음 새 구성 항목이 표시 되는지 확인 합니다.

    -   BitLocker 고정 데이터 드라이브 보호

    -   BitLocker 운영 체제 드라이브 보호



## 관련 항목


[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)


## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.






