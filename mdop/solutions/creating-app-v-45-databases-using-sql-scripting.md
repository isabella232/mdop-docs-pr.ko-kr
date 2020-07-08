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
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825978"
---
# SQL 스크립트를 사용하여 App-V 4.5 데이터베이스 만들기


**이 솔루션의 용도는 무엇 인가요?** App-v (Application Virtualization) 4.5 데이터베이스를 관리 하는 정보 기술 전문가입니다.

**이 가이드는 어떤 도움을 하나요?** 이 솔루션에서는 관리자가 설치 될 때 SQL Server에 대 한 "sysadmin" 권한이 없는 경우 Microsoft Application Virtualization 서버를 설치 하는 절차에 대해 설명 하 고 문서화 합니다.

## 개요


Microsoft Application Virtualization 4.5 (App-v)을 설치 하는 경우의 문제 중 하나는 설치 프로그램에서 서버 기능을 설치 하는 사용자가 로컬 컴퓨터 관리자 뿐만 아니라 데이터 저장소를 호스팅할 SQL server에 대 한 SQL 관리자 권한이 있는 것으로 가정 하는 것입니다. 이 요구 사항은 설치의 일부로 데이터베이스와 적절 한 역할 및 권한이 모두 생성 된다는 사실에 따라 달라 집니다. 그러나 대부분의 기업은 SQL server가 App-v를 설치할 인프라 팀과 별도로 관리 됩니다. 이러한 보안 요구 사항은 인프라 관리자에 게 App-v의 적절 한 권한을 설치 하는 SQL 관리자의 액세스를 어렵게 만드는 것입니다. 마찬가지로, SQL 관리자에 게는 인프라 팀을 위해 제품을 설치 하는 데 필요한 권한이 없습니다.

현재 App-v 설치를 시도 하는 관리자에 게는 SQL "sysadmin" 권한이 있어야 합니다. 이전 버전의 제품에서는 "sysadmin" 권한이 있는 자격 증명을 제공 하기 위해 SQL 관리자가 임시 "sysadmin" 계정을 만들거나 설치 중에 나타날 수 있도록 설정 했습니다. 이 릴리스에서 스크립트는 해당 인프라를 구현할 때 모든 관리자가 사용할 수 있도록 출시 된 제품에서 제공 됩니다.

이 백서에서는 설치를 별도의 두 가지 작업으로 나누고 (SQL 데이터베이스 만들기 및 App-v server 기능 설치) 시나리오에 대해 설명 합니다. SQL 관리자는 SQL 스크립트를 검토 하 고 다른 데이터베이스와의 충돌을 해결 하거나 다른 도구와의 통합을 지원 하기 위해 수정 작업을 수행할 수 있습니다. 이 스크립트의 결과는 인프라 관리자가 SQL server에 고급 권한을 부여할 필요가 없도록 SQL 관리자가 데이터베이스를 준비할 수 있도록 하는 것입니다. 이는 보안 정책이이를 금지 하는 환경에서 중요 합니다.

### SQL 데이터베이스 만들기 프로세스

Sql 스크립트를 사용 하 여 SQL 관리자는 필요한 데이터베이스를 만들고, 환경을 성공적으로 설치 하 고 관리 하기 위해 App-v 관리자에 대 한 권한을 설정할 수도 있습니다. 이러한 작업을 완료 하는 단계는이 문서의 뒷부분에 나열 되어 있습니다.

이 프로세스는 실제 App-v 설치와 데이터베이스 만들기 및 구성 작업을 분리 합니다.

**SQL 관리자에 게 제공 되는 정보**

-   App-v 관리자가 될 광고 그룹의 이름입니다.

-   App-v 관리 서버가 설치 될 서버의 이름입니다.

**인프라 관리자에 게 반환 되는 정보**

-   데이터베이스 서버 또는 인스턴스의 이름과 App-v 데이터베이스의 이름

데이터베이스를 준비한 후에는 App-v 관리자가 SQL 관리자 권한 없이 App-v 설치를 실행할 수 있습니다.

### SQL 설치 스크립트 사용

**요구 사항**

다음은 선택한 추출 위치 루트의 support\\createdb 폴더에 있는 스크립트를 사용 하기 위한 요구 사항 목록입니다.

-   스크립트는 실행 되는 컴퓨터의 쓰기 가능한 위치 (복사한 후 이러한 스크립트에서 읽기 전용 특성을 제거 해야 함)로 복사 되 고 해당 컴퓨터에 SQL 클라이언트 도구가 로드 되어야 합니다 (osql은 로컬 컴퓨터에서 예제 배치 파일을 실행 하는 데만 필요 함).

-   SQL Server는 Windows 인증을 지원 해야 합니다.

-   SQL Server 인스턴스와 SQL 에이전트 서비스가 실행 중인지 확인 합니다.

-   스크립트가 수행 될 컴퓨터의 SQL 관리자 (sysadmin) 인 도메인 계정으로 로그온 합니다.

스크립트는 로그온 한 사용자의 도메인 자격 증명으로 실행 됩니다.

**SQL 스크립트를 사용 하 여 데이터베이스 만들기**

**SQL 관리자가 수행할 작업:**

1.  선택 된 추출 위치의 루트에서 support\\createdb 폴더에 포함 된 스크립트를 스크립트가 실행 될 컴퓨터로 복사 합니다. 다음 파일은 스크립트를 올바르게 실행 하는 데 필요 하며 아래에 표시 된 순서 대로 호출 해야 합니다.

    -   데이터베이스 .sql

    -   역할 .sql

    -   테이블 \ _CODES

    -   함수 \ _before \ _tables. sql

    -   테이블 .sql

    -   함수 .sql

    -   보기 .sql

    -   프로시저 .sql

    -   트리거 .sql

    -   데이터 \ _codes. sql

    -   데이터 \ _messages. sql

    -   데이터 \ _defaults. sql

    -   알림 \ _jobs. sql

    -   dbversion .sql

2.  필요한 경우 파일을 검토 하 고 수정 `database.sql` 합니다. 기본 설정은 데이터베이스 이름을 "APPVIRTDB"로 설정 합니다.

    -   필요한 경우 사용 되는의 인스턴스를 대체 합니다 `APPVIRTDB` `database name` .

    -   데이터베이스를 `FILENAME` 만들 SQL Server의 적절 한 경로를 사용 하 여 스크립트의 속성을 수정 합니다.

3.  필요한 경우 `database name [APPVIRTDB]` `roles.sql` 데이터베이스 .sql 파일에서 사용 된 파일을 검토 하 고 수정 합니다.

****

### 일괄 처리 파일을 사용 하 여 프로세스를 자동화 하는 방법의 예

사용 하는 경우 다음 두 가지 일괄 처리 파일은 SQL 스크립트를 다음과 같은 방식으로 실행 합니다.

1.  **Create\_schema.bat (1)**

    -   데이터베이스 .sql

    -   역할 .sql

2.  **Create\_tables.bat (2)**

    -   테이블 \ _CODES

    -   함수 \ _before \ _tables. sql

    -   테이블 .sql

    -   함수 .sql

    -   보기 .sql

    -   프로시저 .sql

    -   트리거 .sql

    -   데이터 \ _codes. sql

    -   데이터 \ _messages. sql

    -   데이터 \ _defaults. sql

    -   알림 \ _jobs. sql

    -   dbversion .sql

**참고**  
스크립트를 수정할 때는 신중 하 게 고려 하 고 적절 한 정보가 있는 사용자만이 작업을 수행 해야 합니다. 또한 샘플 파일 중에는 **create\_schema.bat**, **create\_tables.bat**, **데이터베이스 .sql**, **roles**등의 데이터만 변경 되어야 합니다. 다른 모든 파일은 데이터베이스를 잘못 만들 수 있으므로 어떤 방식으로든 수정 되어서는 안 되며,이로 인해 App-v services가 설치 되지 않습니다.



두 개의 예제 배치 파일은 컴퓨터에서 나머지 SQL 스크립트를 복사한 동일한 디렉터리에 배치 해야 합니다.

1.  예제 **create\_schema.bat** 파일을 실행 하 여 데이터베이스를 만듭니다. 이 스크립트는 완료 하는 데 몇 초 정도 소요 되며 중단 되어서는 안 됩니다.

    -   복사 된 디렉터리에서 create schema.bat 파일을 실행 합니다. 구문은 "Create\_schema.bat"입니다. `SQLSERVERNAME`

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   새 "APPVIRTDB" 데이터베이스를 만드는 동안이 스크립트에 실패 하는 경우 표시 된 대로 로그를 확인 하 여 문제를 해결 합니다. 이후 시도가 제대로 작동 하는지 확인 하기 위해 스크립트의 일부를 실행 하 여 만든 데이터베이스를 삭제 해야 할 것입니다.

2.  파일을 실행 `create_tables.bat` 하 여 데이터베이스에서 테이블을 만듭니다. 이 스크립트는 완료 하는 데 몇 초 정도 소요 되며 중단 되어서는 안 됩니다.

    -   복사한 디렉터리에서 create\_tables.bat 파일을 실행 합니다. 구문은 "create\_tables.bat"입니다. `SQLSERVERNAME DBNAME`

        ![앱-v 4.6 sql create\-table.bat](images/appv46sqlcreate-tablebat.gif)

        테이블을 만드는 동안 스크립트가 실패 하는 경우 표시 된 대로 로그를 확인 하 여 문제를 해결 합니다. 모든 후속 시도에서 create\_tables.bat 파일을 실행 하기 전에 데이터베이스를 삭제 하 고 create\_schema.bat을 실행 해야 합니다.

### App-v 데이터베이스에 대 한 사용 권한 설정

다음 계정은 앱-V 환경의 설치, 배포 및 진행 관리를 위해 새 데이터베이스에 대 한 특정 사용 권한 및 역할을 사용 하 여 SQL server에서 만들어야 합니다.

-   SQL Server의 앱-V 관리자 그룹에 대 한 로그인과 "domain\\App-V Admins" (여기서 "도메인" 및 "App-v 관리자")가 자신의 환경을 반영 하도록 변경 되 게 하 고이를 SFTAdmin 및 SFTEveryone 데이터베이스 역할에 추가 합니다.

    ![앱-v 4.6 sql 스크립트에서 사용 권한 및 역할 설정](images/appv46sqlscriptsetpermsroles.gif)

-   전역 수준에서이 그룹에 "모든 정의 보기" 사용 권한을 부여 합니다 (이는 Microsoft Application Virtualization Management Server 설치 프로세스가 관리 서버 로그인이 이미 있는지 확인 하는 것을 허용 합니다). MS-SQL 2005 이상에는 master. db에 포함 된 메타 데이터에 대 한 액세스 제한 제한이 추가 되었습니다. 이전 단계에서 만든 사용자는 기본적으로 서버 설치에 필요한 권한을가지고 있지 않습니다. 이전에 만든 로그인, 로그인 속성-Securables의 속성을 엽니다 &gt; . 아래 스크린샷에 표시 된 대로 데이터베이스 인스턴스를 추가 하 고 "정의 보기"에 대해 "부여"를 사용 하도록 설정 합니다.

    ![app-v 4.6 sql 스크립트는 모든 def를 볼 때 perm을 허용 합니다.](images/appv46sqlscriptviewanydef.gif)

-   이전 단계에서 만든 로그인에 대 한 역할 \ _ASSIGNMENTS 테이블에 역할을 추가 하 여 앱-V 관리자가 응용 프로그램 가상화 관리 콘솔에 액세스 하도록 허용 합니다. role = "관리자" 및 그룹 \ _ref = "domain\\App-V 관리자" ("domain" 및 "App-V 관리자"는 자신의 환경을 반영 하도록 변경 됩니다.)

    ![앱-v 4.6 sql 스크립트 역할 할당](images/appv46sqlscriptroleassign.gif)

-   관리 서버용 SQL Server 및 App-v 데이터베이스에 대 한 로그인을 만듭니다. 이 계정은 Microsoft Application Virtualization 관리 서버가 데이터 저장소에 연결 하는 데 사용 되며 스트리밍된 응용 프로그램에 대 한 클라이언트 요청 서비스를 담당 합니다. SQL Server 및 관리 서버가 설치 되는 위치에 따라 두 가지 옵션이 있습니다.

    1.  관리 서버와 SQL Server가 동일한 컴퓨터에 설치 되는 경우 NT AUTHORITY\\NETWORK 서비스에 대 한 로그인을 추가 하 고 SFTUser 및 SFTEveryone 데이터베이스 역할에 추가 합니다.

    2.  관리 서버 및 SQL Server를 다른 컴퓨터에 설치 하는 경우 "domain\\App-V Server Name $" ("App-v server Name")에 대 한 로그인을 추가 하 여 App-v 관리 서버가 설치 되는 서버의 이름이 며 SFTUser 및 SFTEveryone 데이터베이스 역할에 추가 합니다.

-   SQL 창에서 쿼리 창을 열고 다음 SQL을 실행 합니다.

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    여기에서 APPVIRTDB는 이전 단계에서 SQL Server에 만든 App-v 데이터베이스의 이름이 고, App-v Server를 설치 하려고 하는 사용자는 "domain\\App-V Admins"의 구성원 이어야 하며 (여기서 "domain" 및 "App-V 관리자"는 자신의 환경을 반영 하도록 변경 됩니다.)

### 인프라 관리자가 수행할 작업

1.  "App-V Admins" 그룹의 관리자는 App-v를 설치 해야 합니다.

    SQL 관리자의 정보를 사용 하 여 이전 단계에서 만든 SQL Server 및 데이터베이스를 선택 합니다.

2.  "App-v Admins" 그룹의 관리자는 응용 프로그램 가상화 관리 콘솔에 로그인 하 고 관리 콘솔에서 다음 개체를 삭제 합니다.

    **Warning**  
    기존 데이터베이스에 대해 설치를 실행 하는 경우 데이터베이스에서 채워지지 않은 특정 레코드를 채우기 때문에이는 일반 설정에 필요 합니다. 다음 개체를 삭제 합니다.

    -   "서버 그룹"의 "기본 서버 그룹"에서 "응용 프로그램 가상화 관리 서버" 삭제

    -   "서버 그룹"에서 "기본 서버 그룹" 삭제

    -   "공급자 정책"에서 "Default Provider"를 삭제 합니다.



3.  그러면 App-v admins 그룹의 관리자가 다음을 만들어야 합니다.

    -   "공급자 정책"에서 새 공급자 정책 만들기

    -   "기본 서버 그룹 만들기"

        **참고**  
        사용할 수 없는 경우에도 "기본 서버" 그룹을 만들어야 합니다. 서버 설치 관리자는 서버를 추가 하려고 할 때 "기본 서버 그룹"만 찾습니다.  "기본 서버 그룹"이 없는 경우 설치에 실패 하 게 됩니다. 적절 하지 않은 기본 서버 그룹을 사용 하는 경우에는 인프라에 후속 App-v 관리 서버를 추가 하려는 경우 "기본 서버 그룹"을 유지 하는 것이 필요 합니다.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## 결론


결론적으로이 문서의 정보를 통해 관리자는 SQL 관리자와 협력 하 여 조직의 보안 및 관리 디비전에 대해 작동 하는 배포 경로를 개발할 수 있습니다. 이 문서를 읽고 문서화 된 작업을 테스트 한 후에는 관리자가이 환경 유형에 서 App-v 인프라를 구현할 준비가 되어 있어야 합니다.









