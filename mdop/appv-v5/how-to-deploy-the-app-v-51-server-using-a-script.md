---
title: 스크립트를 사용하여 App-V 5.1 Server를 배포하는 방법
description: 스크립트를 사용하여 App-V 5.1 Server를 배포하는 방법
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814129"
---
# 스크립트를 사용하여 App-V 5.1 Server를 배포하는 방법

명령줄을 사용 하 여 **appv\_server\_setup.exe** 서버 설치를 완료 하려면 여러 매개 변수를 지정 하 고 결합 해야 합니다.

## 스크립트를 사용 하 여 App-v 5.1 서버 설치

- 명령줄을 사용 하 여 App-v 5.1 서버를 설치 하는 방법에 대 한 다음 정보를 사용 합니다.

    > [!NOTE]
    > 다음 표에는 **appv\_server\_setup.exe/?** 명령을 입력 하 여 명령줄을 사용 하 여이 정보에 액세스할 수도 있습니다.

### 로컬 컴퓨터에 관리 서버 및 관리 데이터베이스 설치

다음 매개 변수는 Microsoft SQL Server의 기본 인스턴스와 사용자 지정 인스턴스 모두에 대해 유효 합니다.

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### 로컬 컴퓨터에서 기존 관리 데이터베이스를 사용 하 여 관리 서버 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### 원격 컴퓨터에서 기존 관리 데이터베이스를 사용 하 여 관리 서버 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### 동일한 컴퓨터에 관리 데이터베이스와 관리 서버 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### 관리 서버와 다른 컴퓨터에 관리 데이터베이스 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### 게시 서버 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### 로컬 컴퓨터에 보고 서버 및 보고 데이터베이스 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /보고 _SERVER
- /보고 _WEBSITE_NAME
- /보고 _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */보고 _DB_SQLINSTANCE_USE_DEFAULT*
- /보고 _DB_NAME

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /보고 _SERVER
- */보고 _ADMINACCOUNT*
- /보고 _WEBSITE_NAME
- /보고 _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */보고 _DB_CUSTOM_SQLINSTANCE*
- /보고 _DB_NAME

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### 로컬 컴퓨터에서 보고 서버 설치 및 기존 보고 데이터베이스 사용

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /보고 _SERVER
- /보고 _WEBSITE_NAME
- /보고 _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /보고 _SERVER
- */보고 _ADMINACCOUNT*
- /보고 _WEBSITE_NAME
- /보고 _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### 원격 컴퓨터에서 기존 보고 데이터베이스를 사용 하 여 보고 서버 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /보고 _SERVER
- /보고 _WEBSITE_NAME
- /보고 _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /보고 _SERVER
- */보고 _ADMINACCOUNT*
- /보고 _WEBSITE_NAME
- /보고 _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### 보고 데이터베이스를 보고서 서버와 같은 컴퓨터에 설치 합니다.

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /DB_PREDEPLOY_REPORTING
- */보고 _DB_SQLINSTANCE_USE_DEFAULT*
- /보고 _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /DB_PREDEPLOY_REPORTING
- */보고 _DB_CUSTOM_SQLINSTANCE*
- /보고 _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### 보고 서버와 다른 컴퓨터에 보고 데이터베이스 설치

Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).

- /DB_PREDEPLOY_REPORTING
- /보고 _DB_SQLINSTANCE_USE_DEFAULT
- /보고 _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).

- /DB_PREDEPLOY_REPORTING
- /보고 _DB_CUSTOM_SQLINSTANCE
- /보고 _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### 매개 변수 정의

#### 일반 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /QUIET | 자동 설치를 지정 합니다. |
| /UNINSTALL | 제거를 지정 합니다. |
| /LAYOUT | 레이아웃 작업을 지정 합니다. 이렇게 하면 실제로 제품을 설치 하지 않고도 폴더에 MSIs 및 스크립트 파일의 압축이 풀립니다. 값이 필요 하지 않습니다. |
| /LAYOUTDIR | 레이아웃 디렉터리를 지정 합니다. 문자열을 가져옵니다. 사용 예: **/Layoutdir = "C:\\Application Virtualization Server"** |
| /INSTALLDIR | 설치 디렉터리를 지정 합니다. 문자열을 가져옵니다. 사용 예: **/INSTALLDIR = "C:\\program files Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Microsoft 업데이트를 사용 하도록 설정 합니다. 값이 필요 하지 않습니다. |
| /ACCEPTEULA | 사용권 계약을 수락 합니다. 무인 설치에 필요 합니다. 사용 예: **/ACCEPTEULA** 또는 **/ACCEPTEULA = 1** |

#### 관리 서버 설치 매개 변수

|매개 변수 |정보 |
|--|--|
| /MANAGEMENT_SERVER | 관리 서버가 설치 됨을 지정 합니다. 값이 필요 하지 않습니다. |
| /MANAGEMENT_ADMINACCOUNT | 관리 서버에 대 한 관리자 액세스가 허용 되는 계정을 지정 합니다. 이 계정은 사용자 계정 또는 그룹 일 수 있습니다. 사용 예: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**. **/MANAGEMENT_SERVER** 를 지정 하지 않으면 무시 됩니다. |
| /MANAGEMENT_WEBSITE_NAME | 관리 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다. 사용 예: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V 관리 서비스"** |
| MANAGEMENT_WEBSITE_PORT | 관리 서비스에 사용 되는 포트 번호를 지정 합니다. 사용 예: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### 관리 서버 데이터베이스용 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | 관리 데이터베이스를 설치 하도록 지정 합니다. 이 설치를 완료 하려면 충분 한 데이터베이스 권한이 있어야 합니다. 값이 필요 하지 않습니다. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | 기본 SQL 인스턴스를 사용 해야 함을 나타냅니다. 값이 필요 하지 않습니다. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | 새 데이터베이스를 만드는 데 사용 되는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 사용 예: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하지 않으면 무시 됩니다. |
| /MANAGEMENT_DB_NAME | 만들어야 하는 새 관리 데이터베이스의 이름을 지정 합니다. 사용 예: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하지 않으면 무시 됩니다. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | 데이터베이스에 액세스할 관리 서버가 로컬 서버에 설치 되어 있는지 여부를 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | 관리 서버가 설치 되는 원격 컴퓨터의 컴퓨터 계정을 지정 합니다. 사용 예: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername \ \ \ \** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | 관리 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다. 사용 예: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### 게시 서버를 설치 하기 위한 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /PUBLISHING_SERVER | 게시 서버가 설치 됨을 지정 합니다. 값이 필요 하지 않습니다. |
| /PUBLISHING_MGT_SERVER | 게시 서버가 연결 될 관리 서비스의 URL을 지정 합니다. 사용 예: **http:// &lt; management server name &gt; : &lt; 관리 서버 포트 번호 &gt; **입니다. **/PUBLISHING_SERVER** 을 사용 하지 않으면이 매개 변수는 무시 됩니다. |
| /PUBLISHING_WEBSITE_NAME | 게시 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다. 사용 예: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V PUBLISHING 서비스"** |
| /PUBLISHING_WEBSITE_PORT | 게시 서비스에 사용 되는 포트 번호를 지정 합니다. 사용 예: **/PUBLISHING_WEBSITE_PORT = 83** |

#### 보고 서버용 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /REPORTING_SERVER | 보고 서버가 설치 됨을 지정 합니다. 값이 필요 하지 않습니다. |
| /REPORTING_WEBSITE_NAME | 보고 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다. 사용 예: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | 보고 서비스에 사용 되는 포트 번호를 지정 합니다. 사용 예: **/REPORTING_WEBSITE_PORT = 82** |

#### 기존 보고 서버 데이터베이스를 사용 하기 위한 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Microsoft SQL Server가 로컬 서버에 설치 되어 있음을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ 보고 _DB_SQLINSTANCE_USE_DEFAULT | 기본 SQL 인스턴스가 사용 됨을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | 사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"** |
| /EXISTING_ 보고 _DB_NAME | 사용 해야 하는 기존 보고 데이터베이스의 이름을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"** |

#### 보고 서버 데이터베이스를 설치 하기 위한 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /DB_PREDEPLOY_REPORTING | 보고 데이터베이스를 설치 하도록 지정 합니다. 이 설치에는 DBA 권한이 필요 합니다. 값이 필요 하지 않습니다. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | 사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"** |
| /REPORTING_DB_NAME | 만들어야 하는 새 보고 데이터베이스의 이름을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/REPORTING_DB_NAME = "AppVMgmtDB"** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | 데이터베이스에 액세스할 보고 서버가 로컬 서버에 설치 되어 있음을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Reporting server가 설치 될 원격 컴퓨터의 컴퓨터 계정을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | App-v 보고 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다. 문자열을 가져옵니다. 사용 예: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### 기존 관리 서버 데이터베이스를 사용 하기 위한 매개 변수

| 매개 변수 | 정보 |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | 로컬 서버에 SQL Server가 설치 되어 있음을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다. 문자열을 가져옵니다. 사용 예: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | 기본 SQL 인스턴스가 사용 됨을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | 사용 될 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 사용 예 **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다. |
| /EXISTING_MANAGEMENT_DB_NAME | 사용 해야 하는 기존 관리 데이터베이스의 이름을 지정 합니다. 사용 예: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다. |

App-v 문제가 있나요? [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목

[App-V 5.1 Server 배포](deploying-the-app-v-51-server.md)
