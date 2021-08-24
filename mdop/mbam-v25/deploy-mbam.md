---
title: 독립 실행형 구성에서 MBAM 2.5 배포
description: 독립 실행형 구성에서 MBAM 2.5를 배포하는 방법을 소개합니다.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 1ceccf3973bb131484f91917c2b80cd676d1c31b
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910473"
---
# <a name="deploying-mbam-25-in-a-standalone-configuration"></a>독립 실행형 구성에서 MBAM 2.5 배포

이 문서에서는 독립 실행형 구성에서 Microsoft BitLocker 관리 및 모니터링(MBAM) 2.5를 설치하기 위한 단계별 지침을 제공합니다. 이 가이드에서는 두 서버 구성을 사용하게 됩니다. 두 서버 중 하나는 2012에서 실행되는 Microsoft SQL Server 서버입니다. 이 서버는 MBAM 데이터베이스 및 보고서를 호스팅합니다. 추가 서버는 "관리 Windows Server 2012 모니터링 서버" 및 "셀프 서비스 포털"을 호스팅하는 웹 서버입니다.

## <a name="preparation-steps-before-installing-mbam-25-server-software"></a>MBAM 2.5 서버 소프트웨어 설치 전 준비 단계

### <a name="step-1-installation-and-configuration-of-servers"></a>1단계: 서버 설치 및 구성

MBAM 2.5 구성을 시작하기 전에 두 서버가 MBAM 시스템 요구 사항에 따라 구성됩니다. [MBAM 최소](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)시스템 요구 사항 을 참조하고 이러한 요구 사항을 충족하는 구성을 선택합니다. 

#### <a name="step-11-deploying-prerequisites-for-database-and-reporting-server"></a>1.1단계: 데이터베이스 및 보고 서버의 선행 작업 배포

1. Windows Server 2008 R2 이상 운영 체제를 실행하는 서버를 설치 및 구성합니다.

2. 3.Windows PowerShell 설치합니다.

3. 최신 Microsoft SQL Server 포함된 2008 R2 이상 버전을 설치합니다. MBAM용 SQL Server 인스턴스를 설치하는 경우 설치하는 SQL Server 데이터 SQL_Latin1_General_CP1_CI_AS 데이터 데이터 지정을 포함해야 합니다. 다음 SQL Server 설치해야 합니다.

    * 데이터베이스 엔진
    * Reporting Services
    * 클라이언트 도구 연결
    * 관리 도구 - 완료

    > [!Note]
    > 원하는 경우 에서 [TDE(투명한 데이터 암호화)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)기능을 설치할 수도 SQL Server.

    SQL Server Reporting Services 구성되지 않은 모드나 "기본" 모드가 아닌 "기본" 모드로 SharePoint 구성해야 합니다.

    ![필요한 SQL Server 기능입니다.](images/deploying-MBAM-1.png)

4. 관리 및 모니터링 웹 사이트에 SSL을 사용하도록 계획하는 경우 관리 및 모니터링 웹 사이트를 구성하기 전에 SQL Server Reporting Services(Secure Sockets Layer) 프로토콜을 사용하도록 SSRS(Secure Sockets Layer)를 구성해야 합니다. 그렇지 않으면 보고서 기능에서 암호화되지 않은(HTTP) 데이터 전송 대신 암호화되지 않은(HTTP) 데이터 전송을 사용합니다.

    기본 모드 보고서 서버에서 [SSL](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) 연결 구성에 따라 보고서 서버에서 SSL을 구성할 수 있습니다.
    
    > [!Note]
    > 각 버전의 SQL Server 설치 가이드에 따라 설치 SQL Server 수 SQL Server. 링크는 다음과 같습니다.
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. SQL Server 설치 후 SQL Server 사용자 계정을 프로비전하고 데이터베이스 서버에서 MBAM 데이터베이스 및 보고 역할을 구성할 사용자에게 다음 권한을 할당합니다.

    다음 역할의 인스턴스에 대한 SQL Server.
        
    * dbcreator
    * processadmin

    다음의 인스턴스에 대한 SQL Server Reporting Services.
    
    * 폴더 만들기
    * 보고서 게시

데이터베이스 서버가 MBAM 2.5 역할을 구성할 준비가 완료되었습니다. 다음 서버로 이동해보아야 합니다.

#### <a name="step-12-deploying-prerequisites-for-administration-and-monitoring-server"></a>1.2단계: 관리 및 모니터링 서버의 선행 조건 배포

MBAM 시스템 요구 사항 문서에 설명된 하드웨어 구성을 충족하는 서버를 [선택하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements) 최신 서비스 팩 및 Windows Server 2008 R2 이상 운영 체제에서 실행되고 있어야 합니다. 서버가 준비되면 다음 역할 및 기능을 설치합니다.

##### <a name="roles"></a>역할

* 웹 서버(IIS) 관리 도구(IIS 관리 스크립트 및 도구 선택)

* 웹 서버 역할 서비스

    * 일반적인 HTTP 기능<br />
      정적 콘텐츠<br />
      기본 문서

    * 응용 프로그램 개발<br />
      ASP.NET<br />
      .NET Extensibility<br />
      ISAPI 확장<br />
      ISAPI 필터<br />
      보안<br />
      Windows 인증<br />
      요청 필터링

    * 웹 서비스 IIS 관리 도구

##### <a name="feature"></a>기능

* .NET Framework 4.5 기능
  
  * Microsoft .NET Framework 4.5
  
    R2 Windows Server 2012 Windows Server 2012 경우 .NET Framework 4.5가 이러한 버전의 Windows 서버에 대해 Windows 있습니다. 그러나 사용하도록 설정해야 합니다.
  
    Windows Server 2008 R2의 경우 .NET Framework 4.5는 Windows R2에 포함되어 있지 않습니다. 따라서 4..NET Framework 다운로드하고 별도로 설치해야 합니다.
  
  * WCF 정품 인증<br />
    HTTP 정품 인증<br />
    비 HTTP 정품 인증
  
  * TCP 정품 인증
  
  * Windows 프로세스 활성화 서비스:<br />
    프로세스 모델<br />
    .NET Framework 환경<br />
    구성 API

셀프 서비스 포털이 작동하려면 [MVC 4.ASP.NET 설치해야 합니다.](https://go.microsoft.com/fwlink/?linkid=392271)

다음 단계는 Active Directory에서 필요한 MBAM 사용자 및 그룹을 만드는 것입니다.

### <a name="step-2-creating-users-and-groups-in-active-directory-domain-services"></a>2단계: Active Directory 도메인 서비스에서 사용자 및 그룹 만들기
 
선행 조건의 일부로 MBAM에서 사용되는 특정 역할 및 계정을 정의하여 SQL Server 인스턴스에서 실행되는 데이터베이스 및 관리 및 모니터링 서버에서 실행되는 웹 응용 프로그램과 같은 특정 서버 및 기능에 대한 보안 및 액세스 권한을 제공해야 합니다.

Active Directory에서 다음 그룹 및 사용자를 만드십시오. 그룹 및 사용자에 대해 이름을 사용할 수 있습니다. 사용자는 더 큰 사용자 권한을 들이지 않습니다. 도메인 사용자 계정으로 충분합니다. MBAM 2.5를 구성하는 동안 다음 그룹의 이름을 지정해야 합니다.

* **MBAMAppPool**  

  **유형:** 도메인 사용자

  **설명:** 웹 응용 프로그램이 이러한 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록 하는 준수 및 감사 데이터베이스 및 복구 데이터베이스에 대한 읽기 또는 쓰기 권한이 있는 도메인 사용자입니다. 웹 응용 프로그램의 응용 프로그램 풀에서도 사용됩니다.

  **계정 역할(MBAM 구성 중)**:

  1. 웹 서비스 응용 프로그램 풀 도메인 계정

  2. 보고서에 대한 준수 및 감사 데이터베이스 및 복구 데이터베이스 읽기/쓰기 사용자

* **MBAMROUser**

  **유형:** 도메인 사용자

  **설명:** 준수 Read-Only 및 감사 데이터베이스에 대한 액세스 권한을 부여할 도메인 사용자로, 보고서가 이 데이터베이스의 규정 준수 및 감사 데이터에 액세스할 수 있도록 합니다. 또한 로컬 서버 인스턴스가 준수 및 감사 데이터베이스에 액세스하는 데 SQL Server Reporting Services 도메인 사용자 계정이 됩니다.

  **계정 역할(MBAM 구성 중)**:

  1. 보고서에 대한 준수 및 감사 데이터베이스 읽기 전용 사용자

  2. 준수 및 감사 데이터베이스 도메인 사용자 계정

* **MBAMAdvHelpDsk**

  **유형:** 도메인 그룹

  **설명:** MBAM Advanced Helpdesk Users access group: Domain user group whose members have access to all areas of the Administration and Monitoring Website. 이 역할이 있는 사용자는 사용자의 드라이브 복구를 지원할 때 사용자의 도메인 및 사용자 이름이 아닌 복구 키만 입력해야 합니다. 사용자가 MBAM Helpdesk Users 그룹과 MBAM Advanced Helpdesk Users 그룹의 구성원인 경우 MBAM Advanced Helpdesk Users 그룹 사용 권한은 MBAM 지원 팀 그룹 사용 권한을 보다도하게 합니다.

  **계정 역할(MBAM**구성 중) : MBAM 고급 헬프데스크 사용자

* **MBAMHelpDsk**

  **유형:** 도메인 그룹

  **설명:** MBAM 헬프데스크 사용자 액세스 그룹: 구성원이 MBAM 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다. 이 역할이 있는 사용자가 두 옵션을 사용할 때 모든 필드를 채워야 합니다. 여기에는 사용자의 도메인 및 계정 이름이 포함됩니다.

  **계정 역할(MBAM**구성 중) : MBAM 헬프데스크 사용자

* **MBAMRUGrp**

  **유형:** 도메인 그룹

  **설명:** 구성원이 관리 및 모니터링 웹 사이트의 보고서 영역에 있는 보고서에 대한 읽기 전용 액세스 권한을 가진 도메인 사용자 그룹입니다.

  **계정 역할(MBAM 구성 중)**:

  1. 읽기 전용 도메인 액세스 그룹을 보고합니다.

  2. MBAM 보고서 사용자 액세스 그룹

### <a name="step-3-optional-configure-and-install-ssl-certificate-on-administration-and-monitoring-server"></a>3단계(선택 사항): 관리 및 모니터링 서버에 SSL 인증서 구성 및 설치

선택 사항이지만 인증서를 사용하여 MBAM 클라이언트와 관리 및 모니터링 웹 사이트와 Self-Service 포털 웹 사이트 간의 통신을 보호하는 것이 좋습니다. 명확한 보안상의 이유로 인해 자체 서명된 인증서를 사용하지 않는 것이 좋습니다. 신뢰할 수 있는 인증 기관의 웹 서버 유형 인증서를 사용하는 것이 좋습니다. 이를 위해 [KB](https://support.microsoft.com/help/2754259)인증 기관의 "인증 기관에서 승인한 인증서 사용" 섹션을 2754259.

인증서가 발급된 후 관리 및 모니터링 서버의 개인 저장소에 인증서를 추가해야 합니다. 인증서를 추가하려면 로컬 컴퓨터에서 인증서 저장소를 여는 것입니다. 이렇게 하려면 다음 단계를 따르세요.

1. 시작을 오른쪽으로 선택한 다음 실행을 선택합니다.

   ![선택합니다.](images/deploying-MBAM-2.png)

2. "MMC.EXE"(인용 부호 없이)를 입력한 다음 확인 을 **선택합니다.**

   ![실행 상자.](images/deploying-MBAM-3.png) 

3. 연 **** 새 MMC에서 파일을 선택한 다음 **스냅인 추가/제거를 선택합니다.**
   
   ![선택합니다.](images/deploying-MBAM-4.png)

4. 인증서 **스냅인을** 강조 표시한 다음 추가 를 **선택합니다.**

   ![스냅인 창을 추가하거나 제거합니다.](images/deploying-MBAM-5.png)

5. 컴퓨터 **계정 옵션을 선택하고** 다음 을 **선택합니다.**
   
   ![인증서 스냅인 창입니다.](images/deploying-MBAM-6.png)

6. 다음 **화면에서** 로컬 컴퓨터를 선택하고 마친 을 **선택합니다.**
   
   ![컴퓨터 창을 선택합니다.](images/deploying-MBAM-7.png)

7. 이제 인증서 스냅인을 추가했습니다. 이렇게 하면 컴퓨터의 인증서 저장소에 있는 인증서로 작업할 수 있습니다.

   ![스냅인 창을 추가하거나 제거합니다.](images/deploying-MBAM-8.png)

8. 웹 서버 인증서를 컴퓨터의 인증서 저장소로 가져오기

   이제 인증서 스냅인에 액세스할 수 있습니다. 웹 서버 인증서를 컴퓨터의 인증서 저장소로 가져올 수 있습니다. 이 작업을 수행하기 위해 다음 단계를 수행합니다.

9. 인증서(로컬 컴퓨터) 스냅인을 열고 **개인** 및 **인증서로 연결합니다.**
   
   ![인증서(로컬 컴퓨터) 스냅인 창입니다.](images/deploying-MBAM-9.png)

   > [!Note]
   > 인증서 스냅인이 나열되지 않을 수 있습니다. 그렇지 않은 경우 인증서가 설치되지 않습니다.

10. 인증서를 **오른쪽에서 선택하고**모든 **작업을 선택한**다음 가져오기 를 **선택합니다.**

    ![인증서(로컬 컴퓨터) 스냅인 창입니다.](images/deploying-MBAM-10.png)

11. 마법사가 시작되면 다음 을 **선택합니다.** 서버 인증서와 개인 키가 포함된 파일을 찾은 후 다음 을 **선택합니다.**

    ![인증서 가져오기 마법사 창입니다.](images/deploying-MBAM-11.png)

12. 파일을 만들 때 파일에 대해 암호를 지정한 경우 암호를 입력합니다.

   ![암호 창을 입력합니다.](images/deploying-MBAM-12.png)

   > [!Note]
   > 이 컴퓨터에서 **** 키 쌍을 다시 내보낼 수 있도록 하려는 경우 키를 내보낼 수 있는 키로 표시 옵션이 선택되어 있는지 확인합니다. 보안 조치로 이 옵션을 지워서 아무도 개인 키를 백업할 수 없는지 확인하려는 경우도 있습니다.
 
13. **다음을**선택하고 인증서를 **** 저장할 인증서 저장소를 선택합니다.

    ![인증서 가져오기 마법사 창입니다.](images/deploying-MBAM-13.png)

    > [!Note]
    > 웹 서버 인증서이기 때문에 **개인**을 선택해야 합니다. 인증 계층 구조에 인증서를 포함하면 이 저장소에도 인증서가 추가됩니다.
 
14. **다음을**선택하고 마친 을 **선택합니다.**

    ![인증서 가져오기 마법사 창입니다.](images/deploying-MBAM-14.png)

이제 개인 인증서 목록에 웹 서버의 서버 인증서가 표시됩니다. 이 이름은 서버의 일반 이름으로 표시됩니다. 인증서의 제목 섹션에서 찾을 수 있습니다.

추가 참조를 위해:

[MBAM 2.5 보안 고려 사항](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[MBAM 웹 사이트를 보호하는 방법 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

다음 단계에서는 응용 프로그램 풀 계정에 대한 서비스 원칙 이름을 등록합니다.

### <a name="step-4-configuring-ssl-certificate-for-mbam-web-server"></a>4단계: MBAM 웹 서버에 대해 SSL 인증서 구성

클라이언트와 서버 간에 SSL 통신을 사용하는 경우 인증서에 확장된 키 사용 ID(1.3.6.1.5.5.7.3.1) 및 (1.3.6.1.5.5.7.3.2)이 있는지 확인해야 합니다. 즉, 서버 인증 및 클라이언트 인증을 추가해야 합니다.

서비스 URL을 찾아보려고 할 때 인증서 오류가 발생하는 경우 다른 이름으로 발급된 인증서를 사용 중이거나 잘못된 URL을 사용하여 검색 중입니다.

브라우저에서 인증서 오류 메시지가 표시될 수 있지만 계속할 수 있지만 MBAM 웹 서비스는 인증서 오류를 무시하지는 못하며 연결을 차단합니다. MBAM 클라이언트의 MBAM 관리자 이벤트 로그에 인증서 관련 오류가 표시됩니다. 별칭을 사용하여 관리 및 모니터링 서버에 연결하는 경우 별칭 이름에 인증서를 발급해야 합니다. 즉, 인증서의 주체 이름은 별칭 이름이고 로컬 서버의 DNS 이름은 인증서의 주체 대체 이름 필드에 추가해야 합니다. ****

예제:

가상 이름이 "bitlocker.contoso.com"이고 MBAM 관리 및 모니터링 서버 이름이 "adminserver.contoso.com"인 경우 인증서를 bitlocker.contoso.com(주체 이름)로 발급해야 adminserver.contoso.com 인증서의 주체 **** 대체 이름 필드에 추가해야 합니다.

마찬가지로 부하를 균형 조정하기 위해 여러 관리 및 모니터링 서버가 설치된 경우 가상 이름에 SSL 인증서를 발급해야 합니다. 즉, 인증서의 주체 이름 필드에 가상 이름이 있으며 모든 로컬 서버의 이름을 인증서의 주체 대체 이름 필드에 추가해야 합니다. ****

예제:

가상 이름이 "bitlocker.contoso.com"이고 서버가 "adminserver1.contoso.com" 및 "adminiserver2.contoso.com"인 경우 인증서를 bitlocker.contoso.com(주체 이름) 및 adminserver1.contoso.com adminiserver2.contoso.com 인증서의 주체 대체 이름 필드에 추가해야 **** 합니다.

MBAM을 사용하여 SSL 통신을 구성하는 단계는 기술 자료 문서 [KB](https://support.microsoft.com/help/2754259)2754259.

### <a name="step-5-register-spns-for-the-application-pool-account-and-configure-constrained-delegation"></a>5단계: 응용 프로그램 풀 계정에 SPNS를 등록하고 제한 위임 구성

> [!Note]
> 제한 위임은 2.5에만 필요하며 2.5 서비스 팩 1 이상에는 필요하지 않습니다.

MBAM 서버가 관리 및 모니터링 웹 사이트 및 Self-Service 포털에서 통신을 인증할 수 있도록 설정하려면 웹 응용 프로그램 풀에 대해 사용하는 도메인 계정 아래에 호스트 이름에 대해 SPN(서비스 사용자 이름)을 등록해야 합니다. 다음 문서에는 SPNS를 등록하는 단계별 지침: MBAM 웹 사이트를 보호하는 방법 [계획이 포함되어 있습니다.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

SPN을 구성한 후 SPN에 대해 제한 위임 설정을 해야 합니다. 이렇게 하려면 다음 단계를 따르세요.

1. Active Directory로 이동하여 이전 단계에서 MBAM 웹 사이트에 대해 구성한 앱 풀 자격 증명을 확인합니다.

2. 자격 증명을 마우스 오른쪽 단추로 클릭한 다음 속성을 **선택합니다.**

3. 위임 **탭을** 선택합니다.

4. Kerberos 인증 옵션을 선택합니다.

5. **찾아보기를**선택하고 앱 풀 자격 증명을 다시 검색합니다. 그러면 앱 풀 creds 계정에 설정된 모든 SPNS가 표시됩니다. SPN은 "http/bitlocker.fqdn.com"입니다. MBAM 설치 중에 지정한 호스트 이름과 동일한 SPN을 강조합니다.

6. **확인**을 선택합니다.

이제 선행 조처를 잘했습니다. 다음 단계에서는 서버에 MBAM 소프트웨어를 설치하고 구성합니다.

## <a name="installing-and-configuring-mbam-25-server-software"></a>MBAM 2.5 서버 소프트웨어 설치 및 구성

### <a name="step-6-install-mbam-25-server-software"></a>6단계: MBAM 2.5 서버 소프트웨어 설치 

데이터베이스 서버와 관리 및 모니터링 서버에서 모두 Microsoft BitLocker 관리 및 모니터링 설치 마법사를 사용하여 MBAM Server 소프트웨어를 설치하려면 다음 단계를 수행합니다.

1. MBAM을 설치하려는 서버에서 MBAM을 MBAMserversetup.exe Microsoft BitLocker 관리 및 모니터링 설치 마법사를 시작하십시오.

2. 시작 페이지에서 다음 을 **선택합니다.**

3. Microsoft 소프트웨어 사용권 계약을 읽고 **** 동의한 후 다음을 선택하여 설치를 계속합니다.

4. 업데이트를 확인할 때 Microsoft Update를 사용할지 여부를 결정하고 다음 을 **선택합니다.**

5. 사용자 환경 개선 프로그램에 참여할지 여부를 결정하고 다음 을 **선택합니다.**

6. 설치를 시작하려면 설치를 **선택합니다.**

7. MBAM Server 소프트웨어 설치가 완료된 후 서버 기능을 구성하려면 마법사를 닫은 후 **MBAM Server 구성** 실행 확인란을 선택합니다. 또는 나중에 시작 메뉴에 서버 설치에서 만드는 MBAM 서버 구성 바로 가기를 사용하여 **MBAM을** 구성할 **수** 있습니다.

8. 마친 **을 선택합니다.**

자세한 내용은 [Installing the MBAM 2.5 Server Software를 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)

### <a name="step-7-configure-mbam-25-database-and-reports-role"></a>7단계: MBAM 2.5 데이터베이스 및 보고서 역할 구성

이 단계에서는 MBAM 마법사를 사용하여 MBAM 2.5 데이터베이스 및 보고 구성 요소를 구성합니다.

1. 마법사를 사용하여 준수 및 감사 데이터베이스 및 복구 데이터베이스를 구성합니다.
   
   1. 데이터베이스를 구성할 서버에서 **MBAM Server 구성 마법사를 시작하십시오.** 시작 메뉴에서 **MBAM Server 구성을** **선택하여** 마법사를 열 수 있습니다.

   2. 새 **기능 추가를 선택하고**준수 및 감사 **데이터베이스,** 복구 데이터베이스 및 **보고서**를 선택한 후 다음 을 **선택합니다.** 마법사는 데이터베이스의 모든 선행 구성이 충족하는지 검사합니다.

   3. 선행 검사가 성공하면 다음을 **** 선택하여 계속합니다. 그렇지 않은 경우 누락된 선행 문제를 해결한 다음 다시 선행 준비 상태 **확인 을 선택합니다.**
   
   4. 다음 설명을 사용하여 마법사에 필드 값을 입력합니다.

2. 준수 및 감사 데이터베이스

   |필드   |설명|
   |-------|-------|
   |SQL Server 이름 |준수 및 감사 데이터베이스를 구성할 서버의 이름입니다. <br /> 준수 및 감사 데이터베이스 컴퓨터에 예외를 추가하여 포트에서 들어오는 인바운드 트래픽을 SQL Server 합니다. 기본 포트 번호는 1433입니다.|
   |SQL Server 데이터베이스 인스턴스    |준수 및 감사 데이터가 저장될 데이터베이스 인스턴스의 이름입니다. 기본 인스턴스를 사용하는 경우 이 필드를 비워 두십시오. 또한 데이터베이스 정보가 있는 위치를 지정해야 합니다.|
   |데이터베이스 이름   |준수 데이터를 저장할 데이터베이스의 이름입니다. 이 정보는 이후 단계에서 제공해야 하기 때문에 여기서 지정하는 데이터베이스의 이름을 메모해야 합니다.|
   |읽기/쓰기 권한 도메인 사용자 또는 그룹  |2단계에서 구성한 MBAMAppPool 사용자의 이름을 지정합니다.|
   |읽기 전용 액세스 도메인 사용자 또는 그룹   |2단계에서 구성한 MBAMROUser 사용자의 이름을 지정합니다.|

3. 복구 데이터베이스.

   |필드   |설명|
   |-----|-----|
   |SQL Server 이름 |복구 데이터베이스를 구성할 서버의 이름입니다. 복구 데이터베이스 컴퓨터에 예외를 추가하여 포트에서 들어오는 인바운드 트래픽을 SQL Server 합니다. 기본 포트 번호는 1433입니다.|
   |SQL Server 데이터베이스 인스턴스    |복구 데이터를 저장할 데이터베이스 인스턴스의 이름입니다. 기본 인스턴스를 사용하는 경우 이 필드를 비워 두십시오. 또한 데이터베이스 정보가 있는 위치를 지정해야 합니다.|
   |데이터베이스 이름   |복구 데이터를 저장할 데이터베이스의 이름입니다.|
   |읽기/쓰기 권한 도메인 사용자 또는 그룹  |웹 응용 프로그램이 이 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록 이 데이터베이스에 대한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹입니다. <br />이 필드에 사용자를 입력하는 경우 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 **도메인 계정** 필드 값과 **같아야** 합니다. <br />이 필드에 그룹을 입력하는 경우 웹 **** 응용 프로그램 구성 페이지의 **** 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값은 이 필드에 입력하는 그룹의 구성원이 되어야 합니다.|
   
   항목을 마쳤을 때 다음 을 **선택합니다.** 마법사는 데이터베이스의 모든 선행 구성이 충족하는지 검사합니다.
   
   선행 검사가 성공하면 다음을 **** 선택하여 계속합니다. 그렇지 않은 경우 누락된 선행 문제를 해결한 후 **다음을** 다시 선택합니다.

4. 보고서.

   |필드   |설명|
   |----|----|
   |SQL Server Reporting Services 인스턴스  |보고서를 SQL Server Reporting Services 위치의 인스턴스입니다. 기본 인스턴스를 사용하는 경우 이 필드를 비워 두십시오.|
   |보고 역할 도메인 그룹 |2단계에서 설명한 MBAMRUGrp의 이름을 지정합니다.|
   |SQL Server 이름 |준수 및 감사 데이터베이스가 구성된 서버의 이름입니다.|
   |SQL Server 데이터베이스 인스턴스    |준수 및 감사 데이터가 구성된 데이터베이스 인스턴스의 이름입니다. 기본 인스턴스를 사용하는 경우 이 필드를 비워 두십시오. <br />Reporting Server의 포트에서 들어오는 트래픽을 사용하도록 설정하려면 보고서 컴퓨터에 예외를 추가해야 합니다. 기본 포트는 80입니다.|
   |데이터베이스 이름|  준수 및 감사 데이터베이스의 이름입니다. 기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다.|
   |준수 및 감사 데이터베이스 도메인 계정    |2단계에서 구성한 MBAMROUser 사용자의 이름을 지정합니다.|
   
   항목을 마쳤을 때 다음 을 **선택합니다.** 마법사는 보고서 기능에 대한 모든 선행이 충족하는지 검사합니다. 계속하려면 다음을 선택합니다. 요약 **페이지에서** 추가할 기능을 검토합니다.
   
   자세한 내용은 How [to Configure the MBAM 2.5 Databases을 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)

### <a name="step-8-configure-the-mbam-25-web-applications-role"></a>8단계: MBAM 2.5 웹 응용 프로그램 역할 구성

1. 웹 응용 프로그램을 구성할 서버에서 MBAM 서버 구성 마법사를 시작하십시오. 시작 메뉴에서 **MBAM Server 구성을** **선택하여** 마법사를 열 수 있습니다.

2. 새 **기능 추가를 선택하고**관리 **및** 모니터링 웹 사이트 및 **셀프 서비스 포털을 선택한**후 다음 을 **선택합니다.** 마법사는 데이터베이스의 모든 선행 구성이 충족하는지 검사합니다.

3. 선행 검사가 성공하면 다음을 **** 선택하여 계속합니다. 그렇지 않은 경우 누락된 선행 문제를 해결한 다음 다시 선행 준비 상태 **확인 을 선택합니다.**

4. 다음 설명을 사용하여 마법사에 필드 값을 입력합니다.

   |필드   |설명|
   |-----|-----|
   |보안 인증서    |3단계에서 이전에 만든 인증서를 선택하여 선택적으로 관리 및 모니터링 웹 사이트를 구성할 서버와 웹 서비스 간의 통신을 암호화합니다. 인증서 사용 안 을 선택하면 웹 통신이 안전하지 않을 수 있습니다.|
   |호스트 이름   |관리 및 모니터링 웹 사이트를 구성할 호스트 컴퓨터의 이름입니다. <br />컴퓨터의 호스트 이름일 수도 없습니다. 그러나 호스트 이름이 컴퓨터의 netbios 이름과 다른 경우 A 레코드를 만들고 SPN이 netbios 이름이 아닌 사용자 지정 호스트 이름을 사용하는지 확인해야 합니다. 이는 부하 분산 시나리오에서 일반적입니다.|
   |설치 경로   |관리 및 모니터링 웹 사이트를 설치할 경로입니다.|
   |Port    |웹 사이트 통신에 사용할 포트 번호입니다. <br /> 지정된 포트를 통한 통신을 사용하도록 설정하려면 방화벽 예외를 설정해야 합니다.|
   |웹 서비스 응용 프로그램 풀 도메인 계정 및 암호    |2단계에서 구성한 MBAMAppPool 사용자의 사용자 계정 및 암호를 지정합니다. <br /> 보안을 강화하려면 자격 증명에 지정된 계정을 제한된 사용자 권한을 하도록 설정하십시오. 또한 계정의 암호가 만료되지 않는 것으로 설정됩니다.|

5. 기본 제공 IIS_IUSRS 계정 또는 응용 프로그램 풀 계정이 인증 **** 후 클라이언트 가장 및 일괄 작업으로 로그온 로컬 보안 설정에 추가되어 있는지 확인합니다. ****

   계정이 로컬 보안 설정에 추가 는지 **** 확인하려면 로컬 보안 정책 편집기, **** 로컬 정책 노드를 확장하고 사용자 권한 할당 노드를 선택한 다음 인증 후 클라이언트 가장을 두 번 선택하고 오른쪽 창에서 일괄 작업 정책으로 로그온을 두 번 선택합니다. **** **** ****

6. 다음 필드 설명을 사용하여 준수 및 감사 데이터베이스에 대한 마법사에서 연결 정보를 구성합니다.
   |필드   |설명|
   |------|------|
   |SQL Server 이름 |준수 및 감사 데이터베이스가 구성된 서버의 이름입니다.|
   |SQL Server 데이터베이스 인스턴스    |준수 및 감사 데이터베이스가 SQL Server 인스턴스의 \<Server Name\> 이름(예: )입니다. 기본 인스턴스를 사용하는 경우 이 비워 두십시오.|
   |데이터베이스 이름   |준수 및 감사 데이터베이스의 이름입니다. 기본적으로 "MBAM 준수 상태"입니다.|

7. 다음 필드 설명을 사용하여 복구 데이터베이스에 대한 마법사에서 연결 정보를 구성합니다.
   |필드   |설명|
   |----|----|
   |SQL Server 이름 |복구 데이터베이스가 구성된 서버의 이름입니다.|
   |SQL Server 데이터베이스 인스턴스    |복구 데이터베이스가 구성된 SQL Server \<Server Name\> 인스턴스의 이름(예: )입니다. 기본 인스턴스를 사용하는 경우 이 비워 두십시오.|
   |데이터베이스 이름   |복구 데이터베이스의 이름입니다. 기본적으로 "MBAM 복구 및 하드웨어"입니다.|

8. 다음 설명을 사용하여 마법사에서 필드 값을 입력하여 관리 및 모니터링 웹 사이트를 구성합니다.
   |필드   |설명|
   |----|----|
   |고급 헬프데스크 역할 도메인 그룹 |2단계에서 구성한 MBAMAdvHelpDsk 그룹의 이름을 지정합니다.|
   |헬프데스크 역할 도메인 그룹  |2단계에서 구성한 MBAMHelpDsk 그룹의 이름을 지정합니다.|
   |통합 System Center Configuration Manager 사용 |이 확인란의 선택을 취소합니다.     |
   |보고 역할 도메인 그룹 |2단계에서 구성한 MBAMRUGrp 그룹의 이름을 지정합니다.    |
   |SQL Server Reporting Services URL   |MBAM 보고서가 구성된 SSRS 서버의 웹 서비스 URL을 지정합니다. 이 정보는 데이터베이스 서버의 Reporting Services 구성 관리자에 로그인하여 찾을 수 있습니다. <br /> 정식 도메인 이름의 예: https://MyReportServer.Contoso.com/ReportServer <br />사용자 지정 호스트 이름의 예: https://MyReportServer/ReportServer|
   |가상 디렉터리   |관리 및 모니터링 웹 사이트의 가상 디렉터리입니다. 이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당하며 웹 사이트의 호스트 이름에 추가됩니다. 예를 들어 다음과 같은 가치를 제공해야 합니다. <br />http(s):// *\<host name\>* : *\<port\>* /HelpDesk/ <br />가상 디렉터리를 지정하지 않으면 HelpDesk 값이 사용됩니다.     |

9. 다음 설명을 사용하여 마법사에서 필드 값을 입력하여 포털을 Self-Service 있습니다.

   |필드   |설명|
   |----|----|
   |가상 디렉터리   |웹 응용 프로그램의 가상 디렉터리입니다. 이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당하며 웹 사이트의 호스트 이름에 추가됩니다. 예를 들어 다음과 같은 가치를 제공해야 합니다.<br />http(s):// *\<host name\>* : *\<port\>* /SelfService/<br /> 가상 디렉터리를 지정하지 않으면 "SelfService" 값이 사용됩니다.|

10. 항목을 마쳤을 때 다음 을 **선택합니다.** 마법사는 웹 응용 프로그램의 모든 선행이 충족하는지 검사합니다.

11. 계속하려면 **다음을** 선택합니다.

12. 요약 **페이지에서** 추가할 기능을 검토합니다.

13. 서버에 **** 웹 응용 프로그램을 추가하려면 추가를 선택한 다음 닫기 **를 선택합니다.**

## <a name="customizing-and-validating-steps-after-installing-mbam-25-server-software"></a>MBAM 2.5 서버 소프트웨어 설치 후 단계 사용자 지정 및 유효성 검사

### <a name="step-9-customizing-the-self-server-portal-for-your-organization"></a>9단계: 조직에 대한 셀프 서버 포털 사용자 지정

사용자 지정 알림 Self-Service, 회사 이름, 추가 정보에 대한 포인터를 추가하여 Self-Service Portal 사용자 지정을 [참조하세요.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization)
 
### <a name="step-10-configure-the-self-server-portal-if-client-computers-cannot-access-the-cdn"></a>10단계: 클라이언트 컴퓨터가 서버에 액세스할 수 없는 경우 셀프 서버 포털을 CDN 

클라이언트 컴퓨터에 Microsoft AJAX(Microsoft AJAX 서버)에 액세스할 수 Content Delivery Network(CDN). 이 CDN 포털에 Self-Service JavaScript 파일에 필요한 액세스 권한을 제공합니다. 클라이언트 컴퓨터가 Self-Service 액세스할 수 없는 경우 CDN Portal을 구성하지 않는 경우 사용자가 로그인한 회사 이름과 계정만 표시됩니다. 오류 메시지가 표시되지 않습니다.

다음 중 하나를 수행합니다.

* 클라이언트 컴퓨터에서 클라이언트 컴퓨터에 액세스 권한이 CDN 아무 것도 하지 않습니다. 포털 Self-Service 완료되었습니다.

* 클라이언트 컴퓨터에 액세스 권한이 없는 CDN 클라이언트 컴퓨터가 Microsoft 2013에 액세스할 수 없는 경우 Self-Service 포털을 구성하는 [방법의 단계를 Content Delivery Network.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network)

### <a name="step-11-validate-the-mbam-25-server-feature-configuration"></a>11단계: MBAM 2.5 서버 기능 구성 유효성 검사 

독립 실행형 토폴로지 사용을 위해 MBAM Server 배포의 유효성을 검사하기 위해 다음 단계를 수행합니다.

1. MBAM 기능이 배포된 각 서버에서 제어판 **** 프로그램 프로그램 및 기능을  >  ****  >  **선택합니다.** Microsoft **BitLocker 관리** 및 모니터링이 프로그램 및 기능 목록에 **나타나는지** 확인
   > [!Note]
   > 유효성 검사를 수행하려면 각 서버에 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용해야 합니다.

2. 복구 데이터베이스가 구성된 서버에서 복구 데이터베이스를 SQL Server Management Studio **MBAM** 복구 및 하드웨어 데이터베이스가 구성되어 있는지 확인해야 합니다.

3. 준수 및 감사 데이터베이스가 구성된 서버 om에서 MBAM SQL Server Management Studio 열고 MBAM 준수 상태 데이터베이스가 구성되어 있는지 확인해야 합니다.

4. 보고서 기능이 구성된 서버의 관리 자격 증명을 사용하여 웹 브라우저를 열고 사이트 SQL Server Reporting Services 탐색합니다.
   
   SQL Server Reporting Services 사이트 인스턴스의 기본 홈페이지 위치는 http(s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx입니다.
   
   실제 URL을 찾으하려면 Reporting Services Configuration Manager 도구를 사용하여 설치 중에 지정한 인스턴스를 선택합니다.
   
5. Microsoft BitLocker Administration and Monitoring이라는 보고서 폴더에 MaltaDataSource라는 데이터 원본이 포함되어 있는지 확인합니다. 이 데이터 원본에는 언어 로 로컬(예: en-us)을 나타내는 이름이 있는 폴더가 포함되어 있습니다. 보고서는 언어 폴더에 있습니다.

   > [!Note]
   > SSRS(SQL Server Reporting Services)가 명명된 인스턴스로 구성된 경우 URL은 http(s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > SSRS가 SSL(Secure Socket Layer)을 사용하도록 구성되지 않은 경우 MBAM 서버를 설치할 때 보고서의 URL이 "HTTPS" 대신 "HTTP"로 설정됩니다. 그런 다음 관리 및 모니터링 웹 사이트(헬프데스크라고도 하는)로 이동하여 보고서를 선택하면 "보안 콘텐츠만 표시되었습니다."라는 메시지가 표시됩니다. 보고서를 표시하려면 모든 콘텐츠 **표시 를 선택합니다.**

6. 관리 및 모니터링 웹 사이트 기능이 구성된 서버에서 서버 관리자를 실행하고 역할 을 검색한 다음 **** **IIS(웹**  >  **서버)** 인터넷 정보 서비스 선택합니다.

7. **연결에서**사이트 Microsoft \<computer name\> ****  >  **BitLocker 관리 및 모니터링**을 찾아 선택합니다. 다음이 나열되어 있는지 확인

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. 관리 및 모니터링 웹 사이트 및 Self-Service 포털이 구성된 서버에서 관리 자격 증명을 사용하여 웹 브라우저를 열습니다.

9. 다음 웹 사이트를 찾아 성공적으로 로드하는지 확인할 수 있습니다.
   * https(s):// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/ (탐색 및 보고서에 대한 각 링크 확인)
   * http(s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > 네트워크 암호화 없이 기본 포트에 서버 기능을 구성했다고 가정합니다. 다른 포트 또는 가상 디렉터리에 서버 기능을 구성한 경우 해당 포트를 포함하도록 URL을 변경합니다. 예: http(s):// \<host name\> : \<port\> /HelpDesk/ http(s):// : / 서버 기능이 네트워크 암호화를 사용하도록 구성된 경우 http:// 를 \<host name\> \<port\> / \<virtualdirectory\> https://.
   
10. 다음 웹 서비스를 찾아 성공적으로 로드하는지 확인할 수 있습니다. 서비스가 실행되고 있는 것을 나타내는 페이지가 열립니다. 그러나 페이지에 메타데이터가 표시하지 않습니다.

    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### <a name="step-12-configure-the-mbam-group-policy-templates"></a>12단계: MBAM 그룹 정책 템플릿 구성

MBAM을 배포하려면 BitLocker 드라이브 암호화에 대한 MBAM 구현 설정을 정의하는 그룹 정책 설정을 설정해야 합니다. 이 작업을 완료하려면 MBAM 그룹 정책 템플릿을 GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리)을 실행할 수 있는 서버 또는 Workstation에 복사한 다음 설정을 편집해야 합니다.

> [!Important]
> **BitLocker** 드라이브 암호화 노드의 그룹 정책 설정을 변경하지 않으면 MBAM이 제대로 작동하지 않습니다. **MDOP MBAM(BitLocker 관리)** 노드에서 그룹 정책 설정을 구성하면 MBAM에서 **BitLocker** 드라이브 암호화 설정을 자동으로 구성합니다.
 
#### <a name="copying-the-mbam-25-group-policy-templates"></a>MBAM 2.5 그룹 정책 템플릿 복사

MBAM 클라이언트를 설치하기 전에 관리 Workstation에 MBAM 관련 GOS(그룹 정책 개체)를 복사해야 합니다. 이러한 GOS는 BitLocker에 대한 MBAM 구현 설정을 정의합니다. 그룹 정책 템플릿을 지원되는 모든 서버 또는 Windows 기반 서버 또는 클라이언트 컴퓨터에 복사할 수 있으며 GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리)을 실행할 수 있습니다.

자세한 내용은 [Copying the MBAM 2.5 Group Policy Templates을 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates)
 
#### <a name="editing-mbam-25-gpo-settings"></a>MBAM 2.5 GPO 설정 편집

필요한 GPOS를 만든 후 조직의 클라이언트 컴퓨터에 MBAM 그룹 정책 설정을 배포해야 합니다. GPMC(그룹 정책 관리 콘솔) 또는 AGPM(고급 그룹 정책 관리)이 설치되어 있어야 GPOS를 보고 만들 수 있습니다.

자세한 내용은 [Editing the MBAM 2.5 Group Policy 설정](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) and [Planning for MBAM 2.5 Group Policy Requirements을 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
 
### <a name="step-13-deploying-the-mbam-25-client"></a>13단계: MBAM 2.5 클라이언트 배포

Microsoft BitLocker 관리 및 모니터링 클라이언트 소프트웨어를 배포하는 경우 사용자가 컴퓨터를 받기 전이나 이후에 엔터프라이즈 소프트웨어 배포 시스템을 사용하여 그룹 정책을 구성하고 MBAM 클라이언트 소프트웨어를 배포하여 조직의 컴퓨터에서 BitLocker를 사용하도록 설정할 수 있습니다.
 
#### <a name="deploy-the-mbam-client-to-desktop-or-portable-computers"></a>데스크톱 또는 휴대용 컴퓨터에 MBAM 클라이언트 배포

그룹 정책 설정을 구성한 후 Microsoft System Center 2012 Configuration Manager 또는 AD DS(Active Directory 도메인 서비스)와 같은 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용하여 대상 컴퓨터에 MBAM 클라이언트 설치 Windows 설치 관리자 파일을 배포할 수 있습니다. 32비트 또는 64비트 MbamClientSetup.exe 또는 32비트 또는 64비트 MBAMClient.msi 있습니다. 이러한 구성은 MBAM 클라이언트 소프트웨어와 함께 제공됩니다.

자세한 내용은 [How to Deploy the MBAM Client to Desktop or Laptop Computers을 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25)
 
#### <a name="deploy-the-mbam-client-as-part-of-a-windows-deployment"></a>MBAM 클라이언트를 배포의 일부로 Windows 배포

중앙에서 컴퓨터를 수신 및 구성하는 조직에서는 사용자 데이터를 기록하기 전에 MBAM 클라이언트를 설치하여 각 컴퓨터에서 BitLocker 드라이브 암호화를 관리할 수 있습니다. 이 프로세스의 이점은 모든 컴퓨터가 BitLocker와 호환됩니다. 이 방법은 관리자가 이미 컴퓨터를 암호화한 것이기 때문에 사용자 작업을 수행하지 않습니다. 이 시나리오의 주요 가정은 컴퓨터가 사용자에게 배달되기 전에 회사 Windows 이미지를 설치하는 것입니다. 그룹 정책 설정이 PIN을 요구하도록 구성된 경우 정책을 받은 후 PIN을 설정하라는 메시지가 표시됩니다.

자세한 내용은 [How to Deploy the MBAM Client as part of a Windows 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25)
 
#### <a name="how-to-deploy-the-mbam-client-by-using-a-command-line"></a>명령줄을 사용하여 MBAM 클라이언트를 배포하는 방법

자세한 내용은 [How to Deploy the MBAM Client by Using a Command Line을 참조하십시오.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line)

#### <a name="post-deployment-of-clients"></a>클라이언트 배포 후

배포 활동을 완료한 후 다음 로그를 검토하고 클라이언트가 MBAM 데이터베이스에 성공적으로 보고하고 있는지 여부를 결정해야 합니다.

## <a name="faq"></a>FAQ

### <a name="how-to-create-a-load-balanced-iis-servers"></a>부하가 균형이 잡힌 IIS 서버를 만드는 방법

* SPN은 이름(예: bitlocker.corp.net)에만 등록해야 하며 개별 IIS 서버에 등록하면 안 됩니다.

* 인증서를 사용하는 경우 인증서에는 부하 조정 그룹의 모든 IIS 서버에 대한 **** 주체 대체 이름 필드에 FQDN 및 NetBIOS 이름을 모두 입력하고 친숙한 이름(예: bitlocker.corp.net)으로 입력해야 합니다. 그렇지 않으면 부하가 조정된 주소를 검색할 때 브라우저에서 인증서를 신뢰할 수 없는 것으로 보고됩니다.

자세한 내용은 응용 프로그램 풀 계정에 [대한 IIS](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) 네트워크 부하 분산 및 [SPNS 등록을 참조하세요.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account)

### <a name="how-to-configure-a-certificate"></a>인증서를 구성하는 방법

* 두 개의 인증서가 있습니다. 인증서 하나는 SQL 사용하며 다른 하나는 IIS에 사용됩니다. MBAM 설치를 시작하기 전에 설치해야 합니다.

* 설치 관리자를 사용하여 설치 파일을 수동으로 편집하는 대신 IIS 구성에 인증서를 web.config 좋습니다.

* 인증서의 "발급된 사용자" 필드가 서버 이름과 일치하지 않는 경우 MBAM 구성자는 인증서를 수락하지 않습니다. 이 경우 IIS 콘솔에서 자체 서명된 인증서를 일시적으로 만들고 구성기에서 해당 인증서를 사용하게 됩니다. 이렇게 하면 웹앱이 SSL 및 HTTPS에 대해 설치됩니다. 그런 다음 MBAM 웹 사이트의 IIS 바인딩에서 인증서를 1로 변경할 수 있습니다.

### <a name="the-sql-permissions-requirement-for-installation"></a>설치 SQL 대한 사용 권한 요구 사항

MBAM 앱 풀에 대한 계정을 만들고 SecurityAdmin, Public 및 DBCreator 권한만 부여합니다.

자세한 [내용은 MBAM 데이터베이스 구성 - 최소 사용](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) 권한을 참조하세요.

> [!Note]
> * 경우에 따라 초기 설치 및 업그레이드 작업에 더 많은 사용 권한이 필요합니다.
> * 설치에 임시 SA가 있는 계정을 사용하세요.
> * 설치 오류가 발생하기 때문에 사용자 계정의 컨텍스트에서 구성자를 시작하지 말고(다른 SQL Server) 변경할 수 있는 권한이 없는 경우 구성자를 시작하지 않습니다.
> * 사용자 계정의 사용 권한이 있는 계정을 사용하여 로그온해야 SQL Server. MBAM SQL Server 원격으로 실행하여 데이터베이스를 만들거나 업데이트할 수 있습니다. SSRS 서버의 경우 MBAM을 설치하고 Configurator를 로컬로 실행하여 MBAM SSRS 보고서를 설치하거나 업데이트해야 합니다.

### <a name="the-permission-required-for-spn-registration"></a>SPN 등록에 필요한 권한

IIS 포털 설치에 사용되는 계정에는 Write ServicePrincipalName 및 Write Validated SPN 권한이 있어야 합니다. 이러한 권한이 없는 경우 설치 시 SPN을 등록할 수 없다는 경고 메시지가 반환됩니다.

> [!Note]
> 이 경고 메시지가 두 번 수신됩니다. SPN에 등록된 개체가 두 개 있어야 하는 것은 아니라는 의미입니다.

자세한 내용은 "SPN 지연 등록" 오류 [메시지로 MBAM](https://support.microsoft.com/help/2754138/)설치 실패를 참조하세요.

### <a name="did-i-have-to-update-the-admx-templates-to-the-latest-version"></a>ADMX 템플릿을 최신 버전으로 업데이트해야 하나요?

ADMX 템플릿을 최신 버전으로 업데이트하면 GPO의 MBAM 루트 노드에 여러 OS 옵션이 표시됩니다. 예를 들어 Windows 7, Windows 8.1 및 Windows 10 버전 1511 이상을 사용할 수 있습니다.

ADMX 템플릿을 업데이트하는 방법에 대한 자세한 내용은 다음 문서를 참조하세요.
* [MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [MBAM 2.5 그룹 정책 요구 사항 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Microsoft 데스크톱 최적화 팩 그룹 정책 관리 템플릿](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
