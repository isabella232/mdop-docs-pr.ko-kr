---
title: SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기
description: SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c119f1d43a70cce04dd6151697318f7cf6a8d1f2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910593"
---
# <a name="creating-app-v-45-databases-using-sql-scripting"></a>SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기


**Who 이 솔루션이 용도가 있나요?** App-V(Application Virtualization) 4.5 데이터베이스를 관리하는 정보 기술 전문가

**이 가이드를 통해 어떤 도움을 줄 수 있나요?** 이 솔루션에서는 관리자 설치 시 응용 프로그램에 대한 "sysadmin" 권한이 없는 경우 Microsoft Application Virtualization Server를 설치하는 절차를 설명하고 SQL Server.

## <a name="overview"></a>개요


Microsoft App-V(Application Virtualization 4.5)를 설치할 때의 문제 중 하나는 설치 프로그램에서 서버 기능을 설치하는 사용자가 로컬 컴퓨터 관리자일 뿐 아니라 데이터 저장소를 호스팅할 SQL 서버에서 SQL 관리자 권한도 있는 것으로 가정하고 있습니다. 이 요구 사항은 적절한 역할 및 사용 권한뿐만 아니라 데이터베이스가 설치의 일부로 만들어졌다는 사실에 따라 결정됩니다. 그러나 대부분의 기업에서는 SQL 설치할 인프라 팀과 별도로 서버가 관리됩니다. 이러한 보안 요구 사항을 통해 SQL 관리자에게 App-V를 설치하는 데 적절한 권한을 제공하기가 어렵습니다. 마찬가지로 SQL 관리자에게는 인프라 팀용 제품을 설치하는 데 필요한 권한이 없습니다.

현재 App-V 설치를 시도하는 관리자에게는 "sysadmin" SQL 권한이 있어야 합니다. 이전 버전의 제품에서는 SQL 관리자가 임시 "sysadmin" 계정을 만들거나 설치 중에 자격 증명을 제공하도록 허용하여 "sysadmin" 권한을 부여할 수 있습니다. 이 릴리스에서 스크립트는 모든 관리자가 인프라를 구현할 때 사용할 수 있도록 릴리스된 제품에서 제공됩니다.

이 백서에서는 설치를 두 개의 개별 작업, 즉 SQL 데이터베이스 만들기 및 App-V 서버 기능 설치로 구분해야 하는 시나리오에 대해 설명합니다. 이 SQL 관리자는 SQL 스크립트를 검토하고 다른 데이터베이스와의 충돌을 해결하거나 다른 도구와의 통합을 지원하기 위해 수정할 수 있습니다. 스크립트의 결과는 SQL 관리자에게 데이터베이스를 준비할 수 있도록 하여 인프라 관리자에게 데이터베이스 서버에 대한 고급 권한을 부여하지 SQL 것입니다. 이는 보안 정책으로 이러한 제한이 금지되는 환경에서 중요합니다.

### <a name="sql-database-creation-process"></a>SQL Database 만들기 프로세스

SQL 스크립트를 사용하면 SQL 관리자가 필요한 데이터베이스를 만들고 App-V 관리자가 환경을 성공적으로 설치하고 관리할 수 있는 권한을 설정할 수 있습니다. 이러한 작업을 완료하기 위한 단계는 이 문서 의 부분에 나와 있습니다.

이 프로세스는 데이터베이스 만들기 및 구성 작업을 실제 App-V 설치와 분리합니다.

**관리자에게 SQL 정보**

-   App-V 관리자로 지정될 AD 그룹의 이름입니다.

-   App-V Management Server를 설치할 서버의 이름입니다.

**인프라 관리자에게 반환할 정보**

-   데이터베이스 서버 또는 인스턴스의 이름 및 App-V 데이터베이스의 이름

데이터베이스가 준비된 후 App-V 관리자는 관리자 권한 없이 App-V 설치를 SQL 있습니다.

### <a name="using-the-sql-setup-scripts"></a>설치 SQL 스크립트 사용

**요구 사항**

다음은 선택한 추출 위치의 루트에 있는 support\\createdb 폴더에 있는 스크립트를 사용하는 데 필요한 요구 사항 목록입니다.

-   스크립트가 실행될 컴퓨터의 쓰기 가능한 위치에 스크립트를 복사해야 합니다(복사한 후 이러한 스크립트에서 읽기 전용 특성을 제거해야 합니다) SQL 클라이언트 도구를 해당 컴퓨터에 로드해야 합니다(osql은 로컬 컴퓨터에서 예제 배치 파일을 실행하는 데만 필요).

-   인증 SQL Server 지원해야 Windows 합니다.

-   SQL Server 및 SQL 에이전트 서비스가 실행되고 있는지 확인

-   스크립트가 수행될 컴퓨터에서 SQL 관리자(sysadmin)인 도메인 계정으로 로그온합니다.

스크립트는 로그온한 사용자의 도메인 자격 증명으로 실행됩니다.

**스크립트를 사용하여 SQL 만들기**

**관리자가 수행할 작업은 SQL 합니다.**

1.  선택한 추출 위치의 루트에서 support\\createdb 폴더에 포함된 스크립트를 스크립트를 실행할 컴퓨터로 복사합니다. 스크립트를 제대로 실행하려면 다음 파일이 필요하며 아래 제시된 순서대로 호출해야 합니다.

    -   database.sql

    -   roles.sql

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

2.  필요한 경우 파일을 검토하고 `database.sql` 수정합니다. 기본 설정은 데이터베이스 이름을 "APPVIRTDB"로 지정합니다.

    -   필요한 경우 의 인스턴스를 `APPVIRTDB` 사용할 `database name` 인스턴스로 바 대체합니다.

    -   스크립트에서 데이터베이스를 만들 위치의 SQL Server `FILENAME` 경로로 속성을 수정합니다.

3.  필요한 경우 database.sql 파일에 사용된 파일의 을 검토하고 `database name [APPVIRTDB]` `roles.sql` 수정합니다.

****

### <a name="example-of-how-to-automate-the-process-using-batch-files"></a>배치 파일을 사용하여 프로세스를 자동화하는 방법의 예

사용하는 경우 제공된 두 개의 예제 일괄 처리 파일은 다음과 SQL 스크립트를 실행합니다.

1.  **Create\_schema.bat (1)**

    -   database.sql

    -   roles.sql

2.  **Create\_tables.bat (2)**

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

**참고**  
스크립트를 수정할 때 신중하게 고려해야 하며 적절한 지식이 있는 사람만 수행해야 합니다. 또한 다음과 같은 예제 파일만 변경해야 **합니다. **create\_schema.bat,create\_tables.bat, **database.sql** **및 ** **roles.sql**. 다른 모든 파일은 수정하지 말아야 합니다. 이렇게 하면 데이터베이스가 잘못 만들어질 수 있습니다. 그러면 App-V 서비스가 설치되지 않습니다.



두 예제 일괄 처리 파일은 나머지 SQL 스크립트가 컴퓨터에 복사된 동일한 디렉터리에 배치되어야 합니다.

1.  예제 ** 파일 **create\_schema.bat실행하여 데이터베이스를 만듭니다. 이 스크립트는 완료하는 데 몇 초 정도 걸릴 것이고 중단되지 않습니다.

    -   복사한 schema.bat 파일 만들기 파일을 실행합니다. 구문은 `SQLSERVERNAME` "Create\_schema.bat"

        ![AppV46SQLcreatebat.](images/appv46sqlcreatebat.bmp)

    -   새 "APPVIRTDB" 데이터베이스를 만들 때 이 스크립트가 실패하면 표시된 로그를 확인하여 문제를 해결합니다. 이후에 시도가 제대로 작동하도록 스크립트를 부분적으로 실행하여 만든 데이터베이스를 삭제해야 합니다.

2.  파일을 `create_tables.bat` 실행하여 데이터베이스의 테이블을 만듭니다. 이 스크립트는 완료하는 데 몇 초 정도 걸릴 것이고 중단되지 않습니다.

    -   복사한 create\_tables.bat 파일에서 파일 파일을 실행합니다. 구문은 `SQLSERVERNAME DBNAME` "create\_tables.bat"

        ![app-v 4.6 sql create\-table.bat.](images/appv46sqlcreate-tablebat.gif)

        테이블을 만들 때 스크립트가 실패하면 표시된 로그를 확인하여 문제를 해결합니다. 이후의 모든 시도에서 create\_schema.bat 실행하기 전에 데이터베이스를 삭제하고 create\_tables.bat 실행해야 합니다.

### <a name="setting-permissions-on-the-app-v-database"></a>App-V 데이터베이스에 대한 사용 권한 설정

다음 계정은 App-V 환경의 설치SQL 배포 및 지속적인 관리에 대한 새 데이터베이스에 대한 특정 사용 권한 및 역할과 함께 SQL 서버에서 만들어야 합니다.

-   SQL Server 및 APPVIRTDB 데이터베이스에서 "domain\\App-V Admins"(사용자의 환경을 반영하도록 "domain" 및 "App-V Admins"가 변경되는 경우)에 대한 App-V 관리자 그룹에 대한 로그인을 만들고 SFTAdmin 및 SFTEveryone 데이터베이스 역할에 추가합니다.

    ![app-v 4.6 sql 스크립트는 사용 권한 및 역할을 설정합니다.](images/appv46sqlscriptsetpermsroles.gif)

-   전역 수준에서 이 그룹에 "모든 정의 보기" 권한을 부여합니다(이를 통해 Microsoft Application Virtualization Management Server 설치 프로세스에서 관리 서버 로그인이 이미 있는지 확인할 수 있습니다). MS-SQL 2005 이상에서 master.db에 포함된 메타데이터에 대한 액세스 제한이 추가되었습니다. 이전 단계에서 만든 사용자에게는 기본적으로 서버 설치에 필요한 권한은 없습니다. 이전에 만든 로그인, Login 속성 - &gt; 보안의 속성을 열 수 있습니다. 아래 스크린샷과 같이 데이터베이스 인스턴스를 추가하고 "정의 보기"에 대해 "GRANT"를 사용하도록 설정할 수 있습니다.

    ![app-v 4.6 sql 스크립트는 모든 def 보기를 위해 퍼마를 부여합니다.](images/appv46sqlscriptviewanydef.gif)

-   이전 단계에서 만든 로그인에 대한 ROLE\_ASSIGNMENTS 테이블에 역할을 추가하여 App-V 관리자가 Role = "ADMIN" 및 group\_ref = "domain\\App-V Admins"를 사용하여 Application Virtualization Management Console에 액세스할 수 있도록 합니다. 여기서 "domain" 및 "App-V Admins"는 사용자 환경을 반영하도록 변경됩니다.

    ![app-v 4.6 sql 스크립트 역할 할당.](images/appv46sqlscriptroleassign.gif)

-   관리 서버에 SQL Server 및 App-V 데이터베이스에 대한 로그인을 만듭니다. 이 계정은 Microsoft Application Virtualization Management Server에서 데이터 저장소에 연결하는 데 사용하며 스트리밍된 응용 프로그램에 대한 클라이언트 요청을 처리합니다. 클라이언트 서버와 관리 서버를 설치할 SQL Server 두 가지 옵션이 있습니다.

    1.  관리 서버 및 SQL Server 동일한 컴퓨터에 설치하려면 NT AUTHORITY\\NETWORK SERVICE에 대한 로그인을 추가하고 SFTUser 및 SFTEveryone 데이터베이스 역할에 추가합니다.

    2.  관리 서버 및 SQL Server 다른 컴퓨터에 설치하려면 "domain\\App-V Server Name$"(여기서 "App-V Server Name"은 App-V 관리 서버가 설치될 서버의 이름)에 대한 로그인을 추가하고 SFTUser 및 SFTEveryone 데이터베이스 역할에 추가합니다.

-   쿼리 창의 쿼리 SQL 열고 다음 SQL.

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    여기서 APPVIRTDB는 이전 단계에서 SQL Server 에서 만든 App-V 데이터베이스의 이름과 App-v 서버 설치를 진행할 사용자가 "domain\\App-V Admins"의 구성원이 되어야 합니다. 여기서 "domain" 및 "App-V Admins"는 사용자 환경을 반영하도록 변경됩니다.

### <a name="tasks-to-be-performed-by-the-infrastructure-administrators"></a>인프라 관리자가 수행할 작업

1.  "App-V Admins" 그룹의 관리자는 App-V를 설치해야 합니다.

    관리자의 SQL 정보를 사용하여 이전 단계에서 만든 SQL Server 데이터베이스를 선택할 수 있습니다.

2.  "App-V Admins" 그룹의 관리자가 Application Virtualization Management Console에 로그인하고 관리 콘솔에서 다음 개체를 삭제합니다.

    **Warning**  
    기존 설치 프로그램이 기존 데이터베이스에 대해 설치를 실행하면 채워지지 않은 데이터베이스의 특정 레코드를 채우는 데 필요합니다. 다음 개체를 삭제합니다.

    -   "서버 그룹" "기본 서버 그룹"에서 "Application Virtualization Management Server"를 삭제합니다.

    -   "서버 그룹"에서 "기본 서버 그룹" 삭제

    -   "공급자 정책"에서 "기본 공급자"를 삭제합니다.



3.  App-V 관리자 그룹의 관리자는 다음을 만들어야 합니다.

    -   "공급자 정책"에서 새 공급자 정책 만들기

    -   "기본 서버 그룹" 만들기

        **참고**  
        사용되지 않을 경우에도 "기본 서버" 그룹을 만들어야 합니다. 서버 설치 관리자에서 서버를 추가하려고 할 때 "기본 서버 그룹"만 검색합니다.  "기본 서버 그룹"이 없는 경우 설치가 실패합니다. 기본값이 아닐 경우 인프라에 후속 App-V 관리 서버를 추가할 계획인 경우 "기본 서버 그룹"을 유지해야 합니다.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <a name="conclusion"></a>결론


결론적으로 이 문서의 정보를 통해 관리자는 조직의 보안 및 관리 부서에 SQL 배포 경로를 개발할 수 있습니다. 이 문서를 읽고 문서화한 작업을 테스트한 후 관리자는 이 유형의 환경에서 App-V 인프라를 구현할 준비가 된 것입니다.









