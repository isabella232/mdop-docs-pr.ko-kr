---
title: 독립 실행형 구성에서 MBAM 2.5 배포
description: 독립 실행형 구성에서 MBAM 2.5를 배포 하는 방법을 소개 합니다.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826433"
---
# 독립 실행형 구성에서 MBAM 2.5 배포

이 문서에서는 독립 실행형 구성에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 설치 하는 단계별 지침을 제공 합니다. 이 가이드에서는 2 서버 구성을 사용 합니다. 두 서버 중 하나는 Microsoft SQL Server 2012를 실행 하는 데이터베이스 서버입니다. 이 서버는 MBAM 데이터베이스와 보고서를 호스팅합니다. 추가 서버는 Windows Server 2012 웹 서버에서 "관리 및 모니터링 서버" 및 "셀프 서비스 포털"을 호스팅합니다.

## MBAM 2.5 서버 소프트웨어를 설치 하기 전의 준비 단계

### 1 단계: 서버 설치 및 구성

MBAM 2.5 구성을 시작 하기 전에 두 서버 모두 MBAM 시스템 요구 사항으로 구성 되어 있는지 확인 해야 합니다. [Mbam 최소 시스템 요구 사항을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)확인 하 고 이러한 요구 사항을 충족 하는 구성을 선택 합니다. 

#### 1.1 단계: 데이터베이스 및 보고 서버에 대 한 필수 구성 요소 배포

1. Windows Server 2008 R2 이상) 운영 체제를 실행 하는 서버를 설치 하 고 구성 합니다.

2. Windows PowerShell 3.0를 설치 합니다.

3. 최신 서비스 팩이 포함 된 Microsoft SQL Server 2008 R2 이상 버전을 설치 합니다. MBAM 용 SQL Server의 새 인스턴스를 설치 하는 경우 설치 하는 SQL Server에 SQL_Latin1_General_CP1_CI_AS 데이터 정렬이 포함 되어 있는지 확인 합니다. 다음 SQL Server 기능을 설치 해야 합니다.

    * 데이터베이스 엔진
    * Reporting Services
    * 클라이언트 도구 연결
    * 관리 도구 – 완료

    > [!Note]
    > 필요에 따라 [SQL Server에 TDE (투명 데이터 암호화) 기능](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)을 설치할 수도 있습니다.

    SQL Server Reporting Services는 "기본" 모드에서 설치 및 구성 해야 하며,이는 설정 되지 않은 또는 "SharePoint" 모드에 있어야 합니다.

    ![필요한 SQL Server 기능](images/deploying-MBAM-1.png)

4. 관리 및 모니터링 웹 사이트에 SSL을 사용 하려는 경우 관리 및 모니터링 웹 사이트를 구성 하기 전에 SSL (Secure Sockets layer) 프로토콜을 사용 하도록 SQL Server Reporting Services (SSRS)를 구성 해야 합니다. 그렇지 않으면 보고서 기능에서 암호화 (HTTPS) 대신 부호화 되지 않은 (HTTP) 데이터 전송을 사용 하 게 됩니다.

    기본 모드 보고서 서버에서 [Ssl 연결 구성을](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) 팔 로우 하 여 보고서 서버에서 ssl을 구성할 수 있습니다.
    
    > [!Note]
    > Sql server 설치 가이드의 각 버전의 SQL server를 참조 하 여 SQL Server를 설치할 수 있습니다. 링크는 다음과 같습니다.
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. SQL Server의 사후 설치에서 SQL Server에 사용자 계정을 프로 비전 하 고 데이터베이스 서버에서 MBAM 데이터베이스와 보고 역할을 구성할 사용자에 게 다음 사용 권한을 할당 합니다.

    SQL Server 인스턴스의 역할:
        
    * dbcreator
    * processadmin

    SQL Server Reporting Services 인스턴스에 대 한 권한:
    
    * 폴더 만들기
    * 보고서 게시

데이터베이스 서버는 MBAM 2.5 역할을 구성할 준비가 되었습니다. 다음 서버로 이동 하겠습니다.

#### 1.2 단계: 관리 및 모니터링 서버에 대 한 필수 구성 요소 배포

[Mbam 시스템 요구 사항 문서](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)에 설명 된 대로 하드웨어 구성을 충족 하는 서버를 선택 합니다. 최신 서비스 팩과 업데이트를 사용 하 여 Windows Server 2008 R2 이상을 운영 체제에서 실행 해야 합니다. 서버가 준비 되 면 다음 역할 및 기능을 설치 합니다.

##### 역할

* 웹 서버 (IIS) 관리 도구 (IIS 관리 스크립트 및 도구를 선택 합니다.)

* 웹 서버 역할 서비스

    * 일반적인 HTTP 기능<br />
      정적 콘텐츠<br />
      기본 문서

    * 응용 프로그램 개발<br />
      ASP.NET<br />
      .NET 확장성<br />
      ISAPI 확장<br />
      ISAPI 필터<br />
      보안<br />
      Windows 인증<br />
      요청 필터링

    * 웹 서비스 IIS 관리 도구

##### 기능

* .NET Framework 4.5 기능
  
  * Microsoft .NET Framework 4.5
  
    Windows Server 2012 또는 Windows Server 2012 R2의 경우 이러한 버전의 Windows Server에 대해 .NET Framework 4.5이 이미 설치 되어 있습니다. 그러나이 기능을 사용 하도록 설정 해야 합니다.
  
    Windows Server 2008 R2의 경우 .NET Framework 4.5는 Windows Server 2008 R2에 포함 되어 있지 않습니다. 따라서 .NET Framework 4.5을 다운로드 하 고 별도로 설치 해야 합니다.
  
  * WCF 활성화<br />
    HTTP 활성화<br />
    비 HTTP 활성화
  
  * TCP 활성화
  
  * Windows Process Activation Service:<br />
    프로세스 모델<br />
    .NET Framework 환경<br />
    구성 Api

셀프 서비스 포털을 사용 하려면 [ASP.NET MVC 4.0도 다운로드 하 여 설치](https://go.microsoft.com/fwlink/?linkid=392271)해야 합니다.

다음 단계는 Active Directory에서 필요한 MBAM 사용자 및 그룹을 만드는 것입니다.

### 2 단계: Active Directory 도메인 서비스에서 사용자 및 그룹 만들기
 
필수 구성 요소의 일환으로, SQL Server 인스턴스에서 실행 되는 데이터베이스 및 관리 및 모니터링 서버에서 실행 되는 웹 응용 프로그램 등 특정 서버와 기능에 대 한 보안 및 액세스 권한을 제공 하기 위해 MBAM에서 사용 되는 특정 역할 및 계정을 정의 해야 합니다.

Active Directory에 다음 그룹 및 사용자를 만듭니다. (그룹 및 사용자에 대해 원하는 이름을 사용할 수 있습니다.) 사용자는 더 큰 사용자 권한을 가질 필요가 없습니다. 도메인 사용자 계정으로 충분 합니다. MBAM 2.5 구성 중에 이러한 그룹의 이름을 지정 해야 합니다.

* **MBAMAppPool**  

  **유형**: 도메인 사용자

  **설명**: 웹 응용 프로그램에서 해당 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록 준수 및 감사 데이터베이스와 복구 데이터베이스에 대 한 읽기 또는 쓰기 권한이 있는 도메인 사용자입니다. 웹 응용 프로그램의 응용 프로그램 풀 에서도 사용 됩니다.

  **계정 역할 (MBAM을 구성 하는 동안)**:

  1. 웹 서비스 응용 프로그램 풀 도메인 계정

  2. 준수 및 감사 데이터베이스 및 복구 데이터베이스 보고서에 대 한 사용자 읽기/쓰기

* **MBAMROUser**

  **유형**: 도메인 사용자

  **설명**: 보고서에서이 데이터베이스의 규정 준수 및 감사 데이터에 액세스할 수 있도록 준수 및 감사 데이터베이스에 대 한 읽기 전용 액세스 권한을 갖는 도메인 사용자입니다. 또한 로컬 SQL Server Reporting Services 인스턴스에서 규정 준수 및 감사 데이터베이스에 액세스 하는 데 사용 하는 도메인 사용자 계정도 됩니다.

  **계정 역할 (MBAM을 구성 하는 동안)**:

  1. 보고서에 대 한 읽기 전용 사용자 준수 및 감사 데이터베이스

  2. 준수 및 감사 데이터베이스 도메인 사용자 계정

* **MBAMAdvHelpDsk**

  **유형**: 도메인 그룹

  **설명**: Mbam 헬프데스크 사용자 액세스 그룹: 구성원이 관리 및 모니터링 웹 사이트의 모든 영역에 액세스할 수 있는 도메인 사용자 그룹입니다. 이 역할을 가진 사용자가 사용자의 도메인 및 사용자 이름 대신 복구 키만 입력 해야 하는 경우 사용자가 드라이브를 복구 하는 데 도움이 됩니다. 사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 그룹 사용 권한 보다 우선 합니다.

  **계정 역할 (mbam을 구성 하는 동안)**: Mbam 헬프데스크 사용자

* **Mbam**

  **유형**: 도메인 그룹

  **설명**: Mbam 헬프데스크 사용자 액세스 그룹: 구성원이 mbam 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다. 이 역할이 있는 사용자는 두 옵션 중 하나를 사용할 때 모든 필드를 채워야 합니다. 여기에는 사용자의 도메인 및 계정 이름이 포함 됩니다.

  **계정 역할 (mbam을 구성 하는 동안)**: Mbam 헬프데스크 사용자

* **Mbam Grp**

  **유형**: 도메인 그룹

  **설명**: 구성원이 관리 및 모니터링 웹 사이트의 보고서 영역에 있는 보고서에 대해 읽기 전용으로 액세스할 수 있는 도메인 사용자 그룹입니다.

  **계정 역할 (MBAM을 구성 하는 동안)**:

  1. 읽기 전용 도메인 액세스 그룹 보고

  2. MBAM 보고서 사용자 액세스 그룹

### 3 단계 (선택 사항): 관리 및 모니터링 서버에 SSL 인증서 구성 및 설치

선택 사항 이지만, 인증서를 사용 하 여 MBAM 클라이언트와 관리 및 모니터링 웹 사이트와 셀프 서비스 포털 웹 사이트 간 통신을 보호 하는 것이 좋습니다. 명백한 보안상의 이유로 자체 서명 된 인증서를 사용 하지 않는 것이 좋습니다. 신뢰할 수 있는 인증 기관에서 제공 하는 웹 서버 형식 인증서를 사용 하는 것이 좋습니다. 이를 위해 [KB 2754259](https://support.microsoft.com/help/2754259)에서 "인증 기관에서 승인한 인증서 사용" 섹션을 참조할 수 있습니다.

인증서가 발급 되 면 관리 및 모니터링 서버의 개인 저장소에 인증서를 추가 해야 합니다. 인증서를 추가 하려면 로컬 컴퓨터에서 인증서 저장소를 엽니다. 이렇게 하려면 다음 단계를 따르세요.

1. 시작을 마우스 오른쪽 단추로 선택한 다음 실행을 선택 합니다.

   ![선택 ](images/deploying-MBAM-2.png)

2. "MMC.EXE" (따옴표 없이)을 입력 하 고 **확인**을 선택 합니다.

   ![실행 상자](images/deploying-MBAM-3.png) 

3. 새 MMC에서 연 **파일** 을 선택한 다음 **스냅인 추가/제거**를 선택 합니다.
   
   ![선택](images/deploying-MBAM-4.png)

4. **인증서** 스냅인을 강조 표시 한 다음 **추가**를 선택 합니다.

   ![스냅인 추가 또는 제거 창](images/deploying-MBAM-5.png)

5. **컴퓨터 계정** 옵션을 선택 하 고 **다음**을 선택 합니다.
   
   ![인증서 스냅인 창](images/deploying-MBAM-6.png)

6. 다음 화면에서 **로컬 컴퓨터** 를 선택 하 고 **마침을**선택 합니다.
   
   ![컴퓨터 창 선택](images/deploying-MBAM-7.png)

7. 이제 인증서 스냅인이 추가 되었습니다. 이렇게 하면 컴퓨터의 인증서 저장소에 있는 모든 인증서를 사용할 수 있습니다.

   ![스냅인 추가 또는 제거 창](images/deploying-MBAM-8.png)

8. 컴퓨터의 인증서 저장소로 웹 서버 인증서를 가져옵니다.

   이제 인증서 스냅인에 대 한 액세스 권한이 있으므로, 웹 서버 인증서를 컴퓨터의 인증서 저장소로 가져올 수 있습니다. 이렇게 하려면 다음 단계를 따르세요.

9. 인증서 (로컬 컴퓨터) 스냅인을 열고 **Personal** 로 이동한 다음 **인증서**를 찾습니다.
   
   ![인증서 (로컬 컴퓨터) 스냅인 창](images/deploying-MBAM-9.png)

   > [!Note]
   > 인증서 스냅인이 나열 되지 않을 수 있습니다. 그렇지 않으면 인증서가 설치 되지 않은 것입니다.

10. **인증서**를 마우스 오른쪽 단추로 선택 하 고 **모든 작업**을 선택한 다음 **가져오기를**선택 합니다.

    ![인증서 (로컬 컴퓨터) 스냅인 창](images/deploying-MBAM-10.png)

11. 마법사가 시작 되 면 **다음**을 선택 합니다. 서버 인증서와 개인 키를 포함 하 여 만든 파일을 찾은 후 **다음**을 선택 합니다.

    ![인증서 가져오기 마법사 창](images/deploying-MBAM-11.png)

12. 파일을 만들 때 지정한 경우 암호를 입력 합니다.

   ![암호 입력 창](images/deploying-MBAM-12.png)

   > [!Note]
   > 이 컴퓨터에서 키 쌍을 다시 내보낼 수 있도록 하려면 내보내기 **가능한 키로 표시** 옵션이 선택 되어 있는지 확인 합니다. 보안을 강화 하기 위해이 옵션을 선택 하지 않고 개인 키를 백업할 수 없도록 하는 것이 좋습니다.
 
13. **다음**을 선택 하 고 인증서를 저장 하려는 **인증서 저장소** 를 선택 합니다.

    ![인증서 가져오기 마법사 창](images/deploying-MBAM-13.png)

    > [!Note]
    > 웹 서버 인증서 이기 때문에 **개인**을 선택 해야 합니다. 인증서를 인증 계층 구조에 포함 한 경우에는이 저장소에도 추가 됩니다.
 
14. **다음**을 선택 하 고 **마침을**선택 합니다.

    ![인증서 가져오기 마법사 창](images/deploying-MBAM-14.png)

이제 웹 서버에 대 한 서버 인증서가 개인 인증서 목록에 표시 됩니다. 서버의 일반 이름으로 표시 됩니다. (인증서의 제목 섹션에서 찾을 수 있습니다.)

추가 참조:

[MBAM 2.5 보안 고려 사항](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[MBAM 웹 사이트를 보호하는 방법 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

다음 단계는 응용 프로그램 풀 계정에 대 한 서비스 주체 이름을 등록 하는 것입니다.

### 4 단계: MBAM 웹 서버용 SSL 인증서 구성

클라이언트와 서버 간의 SSL 통신을 사용 하는 경우 인증서에 확장 된 키 사용 Oid (1.3.6.1.5.5.7.3.1) 및 (1.3.6.1.5.5.7.3.2)가 있는지 확인 해야 합니다. 즉, 서버 인증 및 클라이언트 인증이 추가 되었는지 확인 해야 합니다.

서비스 Url을 탐색 하려고 할 때 인증서 오류가 표시 되는 경우 다른 이름으로 발급 된 인증서를 사용 중이거나 잘못 된 URL을 사용 하 여 검색 하는 경우입니다.

브라우저에 인증서 오류 메시지가 표시 되지만 계속할 수 있지만,이 경우 MBAM 웹 서비스는 인증서 오류를 무시 하지 않으며 연결이 차단 됩니다. MBAM 클라이언트의 MBAM 관리자 이벤트 로그에서 인증서 관련 오류를 볼 수 있습니다. 별칭을 사용 하 여 관리 및 모니터링 서버에 연결 하는 경우 별칭 이름에 대 한 인증서를 발급 해야 합니다. 즉, 인증서의 주체 이름은 별칭 이름 이어야 하 고 로컬 서버의 DNS 이름은 인증서의 **주체 대체 이름** 필드에 추가 되어야 합니다.

예:

가상 이름이 "bitlocker.contoso.com"이 고 MBAM 관리 및 모니터링 서버 이름이 "adminserver.contoso.com" 인 경우 인증서는 bitlocker.contoso.com (주체 이름)에 발급 되어야 하 고, adminserver.contoso.com는 인증서의 **주체 대체 이름** 필드에 추가 되어야 합니다.

마찬가지로 부하 분산 장치를 사용 하 여 부하의 균형을 유지 하기 위해 여러 관리 및 모니터링 서버가 설치 되어 있는 경우에는 가상 이름에 SSL 인증서를 발급 해야 합니다. 즉, 인증서의 주체 이름 필드에는 가상 이름이 있어야 하 고, 인증서의 **주체 대체 이름** 필드에 모든 로컬 서버의 이름이 추가 되어야 합니다.

예:

가상 이름이 "bitlocker.contoso.com"이 고 서버가 "adminserver1.contoso.com"이 고 "adminiserver2.contoso.com" 인 경우 인증서는 bitlocker.contoso.com (주체 이름) 및 adminserver1.contoso.com에 발급 되어야 하 고, 인증서의 **주체 대체 이름** 필드에는 adminiserver2.contoso.com이 추가 되어야 합니다.

MBAM을 사용 하 여 SSL 통신을 구성 하는 단계는 다음 기술 자료 문서에 설명 되어 있습니다. [KB 2754259](https://support.microsoft.com/help/2754259).

### 5 단계: 응용 프로그램 풀 계정에 대 한 SPN을 등록 하 고 제한 위임을 구성 합니다.

> [!Note]
> 제한 된 위임은 2.5에만 필요 하며 2.5 서비스 팩 1 이상에는 필요 하지 않습니다.

MBAM 서버에서 관리 및 모니터링 웹 사이트와 셀프 서비스 포털의 통신을 인증 하도록 설정 하려면 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 호스트 이름에 대 한 SPN (서비스 사용자 이름)을 등록 해야 합니다. Spn을 등록 하는 단계별 지침은 다음과 같습니다. [MBAM 웹 사이트의 보안을 유지 하는 방법 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

SPN을 구성한 후에는 SPN에 대 한 제한 된 위임을 설정 해야 합니다. 이렇게 하려면 다음 단계를 따르세요.

1. Active Directory로 이동 하 여 이전 단계에서 MBAM 웹 사이트에 대해 구성한 앱 풀 자격 증명을 찾습니다.

2. 자격 증명을 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 선택 합니다.

3. **위임** 탭을 선택 합니다.

4. Kerberos 인증 옵션을 선택 합니다.

5. **찾아보기를**선택 하 고 앱 풀 자격 증명을 다시 찾습니다. 그러면 앱 풀 자격 증명 계정에 설정 된 모든 Spn이 표시 됩니다. (SPN은 "http/bitlocker. fqdn.")와 유사 합니다. MBAM 설치 중에 지정한 호스트 이름과 동일한 SPN을 강조 표시 합니다.

6. **확인**을 선택합니다.

이제 필수 구성 요소에 대해 잘 알고 있습니다. 다음 단계에서는 서버에 MBAM 소프트웨어를 설치 하 고 구성 합니다.

## MBAM 2.5 서버 소프트웨어 설치 및 구성

### 6 단계: MBAM 2.5 서버 소프트웨어 설치 

데이터베이스 서버와 관리 및 모니터링 서버 모두에서 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하 여 MBAM 서버 소프트웨어를 설치 하려면 다음 단계를 따르세요.

1. MBAM을 설치 하려는 서버에서 MBAMserversetup.exe를 실행 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 시작 합니다.

2. 시작 페이지에서 **다음**을 선택 합니다.

3. Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 선택 하 여 설치를 계속 합니다.

4. 업데이트를 확인할 때 Microsoft Update를 사용할지 여부를 결정 하 고 **다음**을 선택 합니다.

5. 사용자 환경 개선 프로그램에 참여할지 여부를 결정 하 고 **다음**을 선택 합니다.

6. 설치를 시작 하려면 **설치**를 선택 합니다.

7. MBAM 서버 소프트웨어 설치가 완료 된 후 서버 기능을 구성 하려면 **마법사를 닫은 후에 Mbam 서버 구성 실행** 확인란을 선택 합니다. 또는 서버 설치가 **시작** 메뉴에 생성 하는 **Mbam 서버 구성** 바로 가기를 사용 하 여 나중에 mbam을 구성할 수 있습니다.

8. **마침을**선택 합니다.

자세한 내용은 [MBAM 2.5 서버 소프트웨어 설치](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)를 참조 하세요.

### 7 단계: MBAM 2.5 데이터베이스 및 보고서 역할 구성

이 단계에서는 MBAM 마법사를 사용 하 여 MBAM 2.5 데이터베이스 및 보고 구성 요소를 구성 합니다.

1. 마법사를 사용 하 여 준수 및 감사 데이터베이스와 복구 데이터베이스를 구성 합니다.
   
   1. 데이터베이스를 구성 하려는 서버에서 **Mbam 서버 구성 마법사**를 시작 합니다. **시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.

   2. **새 기능 추가**, **준수 및 감사 데이터베이스**, **복구 데이터베이스 및 보고서**를 차례로 선택 하 고 **다음**을 선택 합니다. 마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되는지 확인 합니다.

   3. 필수 구성 요소 확인이 완료 되 면 **다음** 을 선택 하 여 계속 합니다. 그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 선택 합니다.
   
   4. 다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.

2. 준수 및 감사 데이터베이스

   |필드   |설명|
   |-------|-------|
   |SQL Server 이름 |준수 및 감사 데이터베이스를 구성 중인 서버의 이름입니다. <br /> SQL Server 포트에서 수신 되는 인바운드 트래픽을 사용 하려면 준수 및 감사 데이터베이스 컴퓨터에 예외를 추가 해야 합니다. 기본 포트 번호는 1433입니다.|
   |SQL Server 데이터베이스 인스턴스    |준수 및 감사 데이터가 저장 되는 데이터베이스 인스턴스의 이름입니다. 기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다. 또한 데이터베이스 정보 위치를 지정 해야 합니다.|
   |데이터베이스 이름   |준수 데이터를 저장할 데이터베이스의 이름입니다. 나중에이 정보를 제공 해야 하므로 여기에서 지정 하는 데이터베이스의 이름을 기록해 야 합니다.|
   |읽기/쓰기 권한 도메인 사용자 또는 그룹  |2 단계에서 구성한 MBAMAppPool 사용자의 이름을 지정 합니다.|
   |읽기 전용 액세스 도메인 사용자 또는 그룹   |2 단계에서 구성한 MBAMROUser 사용자의 이름을 지정 합니다.|

3. 복구 데이터베이스.

   |필드   |설명|
   |-----|-----|
   |SQL Server 이름 |복구 데이터베이스를 구성 중인 서버의 이름입니다. SQL Server 포트에서 수신 되는 인바운드 트래픽을 사용 하려면 복구 데이터베이스 컴퓨터에 예외를 추가 해야 합니다. 기본 포트 번호는 1433입니다.|
   |SQL Server 데이터베이스 인스턴스    |복구 데이터를 저장할 데이터베이스 인스턴스의 이름입니다. 기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다. 또한 데이터베이스 정보 위치를 지정 해야 합니다.|
   |데이터베이스 이름   |복구 데이터를 저장 하는 데이터베이스의 이름입니다.|
   |읽기/쓰기 권한 도메인 사용자 또는 그룹  |웹 응용 프로그램이이 데이터베이스의 데이터 및 보고서에 액세스할 수 있도록이 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹입니다. <br />이 필드에 사용자를 입력 하는 경우 **웹 응용 프로그램 구성** 페이지의 **웹 서비스 응용 프로그램 풀 도메인 계정** 필드에 있는 값과 동일 해야 합니다. <br />이 필드에 그룹을 입력 하는 경우 **웹 응용 프로그램 구성** 페이지의 **웹 서비스 응용 프로그램 풀 도메인 계정** 필드에 있는 값이이 필드에 입력 하는 그룹의 구성원 이어야 합니다.|
   
   항목을 모두 마쳤으면 **다음**을 선택 합니다. 마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되는지 확인 합니다.
   
   필수 구성 요소 확인이 완료 되 면 **다음** 을 선택 하 여 계속 합니다. 그렇지 않으면 누락 된 필수 구성 요소를 해결 하 고 **다음** 을 다시 선택 합니다.

4. 보고서.

   |필드   |설명|
   |----|----|
   |SQL Server Reporting Services 인스턴스  |보고서를 구성 하는 SQL Server Reporting Services의 인스턴스입니다. 기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다.|
   |보고 역할 도메인 그룹 |2 단계에서 설명한 대로 Mbam Grp의 이름을 지정 합니다.|
   |SQL Server 이름 |규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.|
   |SQL Server 데이터베이스 인스턴스    |규정 준수 및 감사 데이터가 구성 된 데이터베이스 인스턴스의 이름입니다. 기본 인스턴스를 사용 하는 경우에는이 필드를 비워 두어야 합니다. <br />보고 서버의 포트에서 들어오는 트래픽을 사용할 수 있도록 하려면 보고서 컴퓨터에 예외를 추가 해야 합니다. (기본 포트는 80입니다.)|
   |데이터베이스 이름|  준수 및 감사 데이터베이스의 이름입니다. 기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다.|
   |준수 및 감사 데이터베이스 도메인 계정    |2 단계에서 구성한 MBAMROUser 사용자의 이름을 지정 합니다.|
   
   항목을 모두 마쳤으면 **다음**을 선택 합니다. 마법사가 보고서 기능에 대 한 모든 필수 구성 요소를 충족 하는지 확인 합니다. 계속하려면 다음을 선택합니다. **요약** 페이지에서 추가 되는 기능을 검토 합니다.
   
   자세한 내용은 다음 문서를 참조 하세요. [MBAM 2.5 데이터베이스를 구성 하는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)에 대해 설명 합니다.

### 8 단계: MBAM 2.5 웹 응용 프로그램 역할 구성

1. 웹 응용 프로그램을 구성 하려는 서버에서 MBAM 서버 구성 마법사를 시작 합니다. **시작** 메뉴에서 **Mbam 서버 구성을** 선택 하 여 마법사를 열 수 있습니다.

2. **새 기능 추가**를 선택 하 **고 관리 및 모니터링 웹 사이트** 및 **셀프 서비스 포털**을 선택한 후 **다음**을 선택 합니다. 마법사에서 데이터베이스에 대 한 모든 필수 조건이 충족 되는지 확인 합니다.

3. 필수 구성 요소 확인이 완료 되 면 **다음** 을 선택 하 여 계속 합니다. 그렇지 않으면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 선택 합니다.

4. 다음 설명을 사용 하 여 마법사에 필드 값을 입력 합니다.

   |필드   |설명|
   |-----|-----|
   |보안 인증서    |3 단계에서 이전에 만든 인증서를 선택 하 여 관리 및 모니터링 웹 사이트를 구성 하는 웹 서비스와 서버 간의 통신을 선택적으로 암호화 합니다. 인증서 사용 안 함을 선택 하면 웹 통신이 안전 하지 않을 수 있습니다.|
   |호스트 이름   |관리 및 모니터링 웹 사이트를 구성 하는 호스트 컴퓨터의 이름입니다. <br />이는 컴퓨터의 호스트 이름이 될 필요는 없으며 모든 것이 될 수 있습니다. 그러나 호스트 이름이 컴퓨터의 netbios 이름과 다른 경우 A 레코드를 만들고 SPN이 netbios 이름이 아닌 사용자 지정 hostname을 사용 하는지 확인 해야 합니다. 이는 부하 분산 시나리오에서 일반적입니다.|
   |설치 경로   |관리 및 모니터링 웹 사이트를 설치 하는 경로입니다.|
   |Port    |웹 사이트 통신에 사용할 포트 번호입니다. <br /> 지정 된 포트를 통해 통신을 사용 하도록 설정 하려면 방화벽 예외를 설정 해야 합니다.|
   |웹 서비스 응용 프로그램 풀 도메인 계정 및 암호    |2 단계에서 구성한 MBAMAppPool 사용자의 사용자 계정 및 암호를 지정 합니다. <br /> 보안 향상을 위해 자격 증명에 지정 된 계정에 제한 된 사용자 권한을 설정 합니다. 또한 계정 암호가 만료 되지 않도록 설정 합니다.|

5. **인증 후** 에 기본 제공 IIS_IUSRS 계정 또는 응용 프로그램 풀 계정이 클라이언트 가장으로 추가 되었는지 확인 하 고 **일괄 작업으로 로그온** 로컬 보안 설정입니다.

   계정이 로컬 보안 설정에 추가 되었는지 여부를 확인 하려면 **로컬 보안 정책 편집기**를 열고, **로컬 정책** 노드를 확장 하 고, **사용자 권한 할당** 노드를 선택 하 고, **인증 후 클라이언트 가장** 을 두 번 선택 하 고 오른쪽 창에서 **일괄 작업으로 로그온** 정책을 사용 합니다.

6. 마법사에서 준수 및 감사 데이터베이스에 대 한 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.
   |필드   |설명|
   |------|------|
   |SQL Server 이름 |규정 준수 및 감사 데이터베이스가 구성 된 서버의 이름입니다.|
   |SQL Server 데이터베이스 인스턴스    |SQL Server 인스턴스의 이름 (예: \<Server Name\> )과 준수 및 감사 데이터베이스가 구성 된 기본 인스턴스를 사용 하는 경우이를 비워 둡니다.|
   |데이터베이스 이름   |준수 및 감사 데이터베이스의 이름입니다. 기본적으로 "MBAM 준수 상태"입니다.|

7. 복구 데이터베이스에 대 한 마법사에서 연결 정보를 구성 하려면 다음 필드 설명을 사용 합니다.
   |필드   |설명|
   |----|----|
   |SQL Server 이름 |복구 데이터베이스가 구성 된 서버의 이름입니다.|
   |SQL Server 데이터베이스 인스턴스    |복구 데이터베이스가 구성 된 SQL Server 인스턴스의 이름 (예: \<Server Name\> )입니다. 기본 인스턴스를 사용 하는 경우이를 비워 둡니다.|
   |데이터베이스 이름   |복구 데이터베이스의 이름입니다. 기본적으로 "MBAM 복구 및 하드웨어"입니다.|

8. 마법사에서 필드 값을 입력 하 여 관리 및 모니터링 웹 사이트를 구성 하려면 다음 설명을 사용 합니다.
   |필드   |설명|
   |----|----|
   |고급 헬프데스크 역할 도메인 그룹 |2 단계에서 구성한 MBAMAdvHelpDsk 그룹의 이름을 지정 합니다.|
   |헬프데스크 역할 도메인 그룹  |2 단계에서 구성한 대로 Mbam 그룹의 이름을 지정 합니다.|
   |System Center Configuration Manager 통합 사용 |이 확인란을 선택 취소 합니다.     |
   |보고 역할 도메인 그룹 |2 단계에서 구성한 대로 Mbam Grp Group의 이름을 지정 합니다.    |
   |SQL Server Reporting Services URL   |MBAM 보고서가 구성 된 SSRS 서버의 웹 서비스 URL을 지정 합니다. 데이터베이스 서버에서 Reporting Services 구성 관리자에 로그인 하 여이 정보를 찾을 수 있습니다. <br /> 정규화 된 도메인 이름의 예:https://MyReportServer.Contoso.com/ReportServer <br />사용자 지정 호스트 이름의 예:https://MyReportServer/ReportServer|
   |가상 디렉터리   |관리 및 모니터링 웹 사이트의 가상 디렉터리입니다. 이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당 하며 웹 사이트의 호스트 이름에 추가 됩니다. 예: <br />http (s)// *\<host name\>* : *\<port\>* /HelpDesk/ <br />가상 디렉터리를 지정 하지 않으면 값 헬프데스크를 사용 합니다.     |

9. 마법사에서 필드 값을 입력 하 여 셀프 서비스 포털을 구성 하려면 다음 설명을 사용 합니다.

   |필드   |설명|
   |----|----|
   |가상 디렉터리   |웹 응용 프로그램의 가상 디렉터리입니다. 이 이름은 서버의 웹 사이트의 실제 디렉터리에 해당 하며 웹 사이트의 호스트 이름에 추가 됩니다. 예:<br />http (s)// *\<host name\>* : *\<port\>* /SelfService/<br /> 가상 디렉터리를 지정 하지 않으면 "SelfService" 값이 사용 됩니다.|

10. 항목을 모두 마쳤으면 **다음**을 선택 합니다. 마법사가 웹 응용 프로그램의 모든 필수 구성 요소를 충족 하는지 확인 합니다.

11. **Next (다음** )를 선택 하 여 계속 합니다.

12. **요약** 페이지에서 추가 되는 기능을 검토 합니다.

13. 서버에 웹 응용 프로그램을 추가 하려면 **추가** 를 선택 하 고 **닫기를**선택 합니다.

## MBAM 2.5 서버 소프트웨어 설치 후 단계 사용자 지정 및 유효성 검사

### 9 단계: 조직에 대 한 셀프 서버 포털 사용자 지정

사용자 지정 알림 텍스트, 회사 이름, 추가 정보에 대 한 포인터 등을 추가 하 여 셀프 서비스 포털을 사용자 지정 하려면 [조직에 대 한 셀프 서비스 포털 사용자 지정](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization)을 참조 하세요.
 
### 10 단계: 클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서버 포털 구성 

클라이언트 컴퓨터에 Microsoft CDN (콘텐츠 배달 네트워크)에 대 한 액세스 권한이 있는지 확인 합니다. CDN은 특정 JavaScript 파일에 필요한 액세스 권한을 셀프 서비스 포털에 제공 합니다. 클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하지 않으면 사용자가 로그인 한 회사 이름과 계정만 표시 됩니다. 오류 메시지가 표시 되지 않습니다.

다음 중 하나를 수행합니다.

* 클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 있는 경우 아무 작업도 수행 하지 않습니다. 셀프 서비스 포털 구성이 완료 되었습니다.

* 클라이언트 컴퓨터에 CDN에 대 한 액세스 권한이 없는 경우 [클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network)의 단계를 따릅니다.

### 11 단계: MBAM 2.5 서버 기능 구성 확인 

단독 토폴로지를 사용 하기 위해 MBAM 서버 배포의 유효성을 검사 하려면 다음 단계를 따릅니다.

1. Mbam 기능이 배포 된 각 서버에서 **제어판**  >  **프로그램**프로그램  >  **및 기능**을 선택 합니다. **Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.
   > [!Note]
   > 유효성 검사를 수행 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.

2. 복구 데이터베이스가 구성 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 구성 되어 있는지 확인 합니다.

3. 준수 및 감사 데이터베이스가 구성 된 서버 om에서 SQL Server Management Studio를 열고 MBAM 준수 상태 데이터베이스가 구성 되어 있는지 확인 합니다.

4. 보고서 기능이 구성 된 서버 onm에서 관리 자격 증명을 사용 하 여 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 홈페이지를 찾습니다.
   
   SQL Server Reporting Services 사이트 인스턴스의 기본 홈 페이지 위치는 다음과 같습니다. http (s)// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정한 인스턴스를 선택 합니다.
   
5. Microsoft BitLocker 관리 및 모니터링 이라는 보고서 폴더에 MaltaDataSource 이라는 데이터 원본이 포함 되어 있는지 확인 합니다. 이 데이터 원본에는 언어 로캘을 나타내는 이름 (예: en-us)이 포함 된 폴더가 있습니다. 보고서는 언어 폴더에 있습니다.

   > [!Note]
   > SQL Server Reporting Services (SSRS)가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http (s)// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > SSL (Secure Socket Layer)을 사용 하도록 SSRS를 구성 하지 않은 경우, MBAM 서버를 설치할 때 보고서에 대 한 URL이 "HTTPS" 대신 "HTTP"로 설정 됩니다. 그런 다음 관리 및 모니터링 웹 사이트 (헬프데스크 라고도 함)로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 나타납니다. 보고서를 표시 하려면 **모든 콘텐츠 표시**를 선택 합니다.

6. 관리 및 모니터링 웹 사이트 기능이 구성 된 서버에서 서버 관리자를 실행 하 고 **역할**을 찾은 다음 **웹 서버 (iis**)  >  **iis (인터넷 정보 서비스** ) 관리자를 선택 합니다.

7. **연결**에서 \<computer name\> **Sites**  >  **Microsoft BitLocker 관리 및 모니터링**사이트를 찾아 선택 합니다. 다음이 나열 되는지 확인 합니다.

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. 관리 및 모니터링 웹 사이트와 셀프 서비스 포털이 구성 된 서버에서 관리 자격 증명을 사용 하 여 웹 브라우저를 엽니다.

9. 다음 웹 사이트를 탐색 하 여 성공적으로 로드 되었는지 확인 합니다.
   * https:// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/(탐색 및 보고서에 대 한 각 링크 확인)
   * http (s)// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > 네트워크 암호화 없이 기본 포트에서 서버 기능을 구성한 것으로 가정 합니다. 다른 포트 또는 가상 디렉터리에서 서버 기능을 구성한 경우 해당 포트를 포함 하도록 Url을 변경 합니다. 예: http (s)// \<host name\> : \<port\> /HelpDesk/http (s)// \<host name\> : \<port\> / \<virtualdirectory\> /서버 기능이 네트워크 암호화를 사용 하도록 구성 된 경우 http://를 https://로 변경 합니다.
   
10. 다음 웹 서비스를 찾아 제대로 로드 되었는지 확인 합니다. 서비스가 실행 중임을 나타내는 페이지가 열립니다. 그러나 페이지에는 메타 데이터가 표시 되지 않습니다.

    * http (s)// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http (s)// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http (s)// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http (s)// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### 12 단계: MBAM 그룹 정책 서식 파일 구성

MBAM을 배포 하려면 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정을 설정 해야 합니다. 이 작업을 완료 하려면 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있는 서버 또는 워크스테이션에 MBAM 그룹 정책 템플릿을 복사한 다음 설정을 편집 해야 합니다.

> [!Important]
> **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다. **MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.
 
#### MBAM 2.5 그룹 정책 서식 파일 복사

MBAM 클라이언트를 설치 하기 전에, 관리 워크스테이션에 MBAM Gpo (그룹 정책 개체)를 복사 해야 합니다. 이러한 Gpo는 BitLocker에 대 한 MBAM 구현 설정을 정의 합니다. 그룹 정책 템플릿을 지원 되는 Windows 기반 서버 또는 클라이언트 컴퓨터인 모든 서버 또는 워크스테이션에 복사 하 여 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있습니다.

자세한 내용은 [MBAM 2.5 그룹 정책 서식 파일 복사](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates)를 참조 하세요.
 
#### MBAM 2.5 GPO 설정 편집

필요한 Gpo를 만든 후에는 조직의 클라이언트 컴퓨터에 MBAM 그룹 정책 설정을 배포 해야 합니다. Gpo를 보고 만들려면 GPMC (그룹 정책 관리) 콘솔 또는 AGPM (고급 그룹 정책 관리)이 설치 되어 있어야 합니다.

자세한 내용은 [mbam 2.5 그룹 정책 설정](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) 및 [Mbam 2.5 그룹 정책 요구 사항에 대 한 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)편집을 참조 하세요.
 
### 13 단계: MBAM 2.5 클라이언트 배포

Microsoft BitLocker 관리 및 모니터링 클라이언트 소프트웨어를 배포 하는 경우 사용자가 컴퓨터를 받기 전이나 나중에 (또는 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여) MBAM 클라이언트 소프트웨어를 배포 하거나 그룹 정책을 구성 하 여 조직의 컴퓨터에서 BitLocker를 사용 하도록 설정할 수 있습니다.
 
#### 데스크톱 또는 휴대용 컴퓨터에 MBAM 클라이언트 배포

그룹 정책 설정을 구성한 후 Microsoft System Center 2012 구성 관리자 또는 AD DS (Active Directory 도메인 서비스) 등의 엔터프라이즈 소프트웨어 배포 시스템 제품을 사용 하 여 대상 컴퓨터에 MBAM 클라이언트 설치 Windows Installer 파일을 배포할 수 있습니다. 32 비트 또는 64 비트 MbamClientSetup.exe 파일을 사용 하거나 32 비트 또는 64 비트 MBAMClient.msi 파일을 사용할 수 있습니다. 이는 MBAM 클라이언트 소프트웨어와 함께 제공 됩니다.

자세한 내용은 [데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트를 배포 하는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25)참조 하세요.
 
#### Windows 배포의 일부로 MBAM 클라이언트 배포

컴퓨터를 중앙에서 받고 구성 하는 조직에서 MBAM 클라이언트를 설치 하 여 사용자 데이터를 기록 하기 전에 각 컴퓨터에서 BitLocker 드라이브 암호화를 관리할 수 있습니다. 이 프로세스의 장점은 모든 컴퓨터가 BitLocker 규격을 준수 한다는 것입니다. 관리자가 이미 컴퓨터를 암호화 했기 때문에이 메서드는 사용자 작업에 의존 하지 않습니다. 이 시나리오의 주요 전제는 조직의 정책이 사용자에 게 컴퓨터를 전달 하기 전에 회사 Windows 이미지를 설치 하는 것입니다. PIN을 요구 하도록 그룹 정책 설정을 구성한 경우 사용자가 정책을 받은 후 PIN을 설정 하 라는 메시지가 표시 됩니다.

자세한 내용은 [Windows 배포의 일부로 MBAM 클라이언트를 배포 하는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25)참조 하세요.
 
#### 명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법

자세한 내용은 [명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line)참조 하세요.

#### 클라이언트 배포 후

이제 배포 작업을 완료 했으므로 다음 로그를 검토 하 고 클라이언트가 MBAM 데이터베이스에 성공적으로 보고 되는지 여부를 확인 해야 합니다.

## FAQ

### 부하 분산 된 IIS 서버를 만드는 방법

* SPN은 친근 한 이름 (예: bitlocker.corp.net)에만 등록 해야 하며 개별 IIS 서버에 등록 되어 있지 않아야 합니다.

* 인증서를 사용 하는 경우 인증서에는 부하 분산 그룹의 모든 IIS 서버에 대 한 **주체 대체 이름** 필드에 입력 한 FQDN 및 NetBIOS 이름과 친근 한 이름 (예: bitlocker.corp.net)이 모두 포함 되어 있어야 합니다. 그렇지 않으면 부하 분산 된 주소를 검색할 때 인증서가 브라우저에서 신뢰할 수 없는 것으로 보고 됩니다.

자세한 내용은 [IIS 네트워크 부하 분산](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) 및 [응용 프로그램 풀 계정에 대 한 spn 등록](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account)을 참조 하세요.

### 인증서를 구성 하는 방법

* 두 개의 인증서가 있어야 합니다. 하나의 인증서가 SQL server에 사용 되 고 그 외에는 IIS에 사용 됩니다. MBAM 설치를 시작 하기 전에 설치 해야 합니다.

* 설치 관리자를 사용 하 여 web.config 파일을 수동으로 편집 하는 대신 IIS 구성에 인증서를 추가 하는 것이 좋습니다.

* 인증서의 "발급 대상" 필드가 서버 이름과 일치 하지 않는 경우 MBAM 구성자에서 인증서를 허용 하지 않습니다. 이 경우에는 IIS 콘솔에서 자체 서명 된 인증서를 임시로 만들고이를 구성자에서 사용 합니다. 이렇게 하면 SSL 및 HTTPS에 대해 웹 앱이 설치 되어 있는지 확인 합니다. 그 후에는 MBAM 웹 사이트에 대 한 IIS 바인딩에서 인증서를 변경할 수 있습니다.

### 설치에 필요한 SQL 권한 요구 사항

MBAM 앱 풀에 대 한 계정을 만들고 SecurityAdmin, Public 및 DBCreator 권한만 제공 합니다.

자세한 내용은 [Mbam 데이터베이스 구성 – 최소 사용 권한을](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) 참조 하세요.

> [!Note]
> * 경우에 따라 초기 설치 및 업그레이드 작업에 대 한 추가 권한이 필요 합니다.
> * 설치에 임시 SA가 있는 계정을 사용 합니다.
> * SQL Server에 대 한 변경을 수행할 수 있는 권한이 없는 사용자 계정 (실행)의 컨텍스트에서는 설치 오류를 초래 하므로 구성자를 시작 하지 마세요.
> * SQL Server에 대 한 사용 권한이 있는 계정을 사용 하 여 로그온 해야 합니다. MBAM Configurator를 원격으로 실행 하 여 SQL Server 데이터베이스만 만들거나 업데이트할 수 있습니다. SSRS 서버의 경우 mbam을 설치 하 고 Configurator를 로컬로 실행 하 여 MBAM SSRS 보고서를 설치 하거나 업데이트 해야 합니다.

### SPN 등록에 필요한 사용 권한

IIS 포털 설치에 사용 되는 계정에는 쓰기 ServicePrincipalName 및 확인 된 SPN 사용 권한이 있어야 합니다. 이러한 권한이 없으면 설치 시 SPN을 등록할 수 없다는 경고 메시지가 반환 됩니다.

> [!Note]
> 이 경고 메시지가 두 번 표시 됩니다. 이는 SPN에 등록 된 두 개체가 있어야 한다는 의미는 아닙니다.

자세한 내용은 [Mbam 설정이 "SPN 지연 등록" 오류 메시지와 함께 실패](https://support.microsoft.com/help/2754138/)하세요.

### ADMX 서식 파일을 최신 버전으로 업데이트 해야 하나요?

ADMX 서식 파일을 최신 버전으로 업데이트 한 후 GPO에 대 한 MBAM 루트 노드에서 여러 OS 옵션이 표시 됩니다. 예를 들어 Windows 7, Windows 8.1 및 Windows 10, 버전 1511 이상 버전.

ADMX 템플릿을 업데이트 하는 방법에 대 한 자세한 내용은 다음 문서를 참조 하세요.
* [MDOP 그룹 정책(.admx) 템플릿을 다운로드 및 배포하는 방법](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [MBAM 2.5 그룹 정책 요구 사항 계획](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Microsoft 데스크톱 최적화 팩 그룹 정책 관리 서식 파일](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
