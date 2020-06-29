---
title: SQL 스크립트를 사용하여 App-V 데이터베이스를 배포하는 방법
description: SQL 스크립트를 사용하여 App-V 데이터베이스를 배포하는 방법
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814105"
---
# SQL 스크립트를 사용하여 App-V 데이터베이스를 배포하는 방법

다음 지침을 사용 하 여 Windows Installer 대신 SQL 스크립트를 사용 하 여 다음을 수행 합니다.

- App-v 5.1 데이터베이스 설치
- 앱-V 데이터베이스를 최신 버전으로 업그레이드

> [!NOTE]
> App-v 5.0 SP3 데이터베이스를 이미 배포한 경우에는 SQL 스크립트를 앱-V 5.1으로 업그레이드할 필요가 없습니다.

## SQL 스크립트를 사용 하 여 앱 V 데이터베이스를 설치 하는 방법

1. 데이터베이스 스크립트를 설치 하기 전에 App-v 라이선스 조건의 복사본을 검토 하 고 유지 합니다. 데이터베이스 스크립트를 실행 하 여 사용 조건에 동의 하는 것입니다. 동의 하지 않는 경우에는이 소프트웨어를 사용해 서는 안 됩니다.
1. App-v release 미디어의 **appv\_server\_setup.exe** 임시 위치에 복사 합니다.
1. 명령 프롬프트에서 **appv\_server\_setup.exe** 를 실행 하 고 데이터베이스 스크립트를 추출 하는 임시 위치를 지정 합니다.

    예: appv\_server\_setup.exe/layout c:\\ &lt; _임시 위치 경로_&gt;

1. 만든 임시 위치로 이동 하 고 추출한 **Databasescripts** 폴더를 연 다음 적절 한 Readme.txt 파일을 검토 하 여 지침을 따릅니다.

    | 데이터베이스 | 사용할 Readme.txt 파일의 위치 |
    |--|--|
    | 관리 데이터베이스 | ManagementDatabase 하위 폴더 |
    | 보고 데이터베이스 | ReportingDatabase 하위 폴더 |

> [!CAUTION]
> ManagementDatabase 하위 폴더의 readme.txt 파일이 만료 되었습니다. 아래에 업데이트 된 readme 파일의 정보가 최신 이며, **Databasescripts** 폴더에 제공 된 readme 정보를 대체 해야 합니다.

> [!IMPORTANT]
> App-v 5.0 SP3 보다 이후 버전인 App-v 관리 데이터베이스 버전에는 InsertVersionInfo 스크립트가 필요 하지 않습니다.

사용 권한 .sql 스크립트는 [KB 문서 3031340](https://support.microsoft.com/kb/3031340)의 **2 단계** 에 따라 업데이트 해야 합니다. App-v 5.0 SP3 보다 이후 버전의 App-v에는 **1 단계가** 필요 하지 않습니다.

## 업데이트 된 관리 데이터베이스 추가 정보 파일 콘텐츠

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## 업데이트 된 보고 데이터베이스 README 파일 콘텐츠

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목

[App-V 5.1 Server 배포](deploying-the-app-v-51-server.md)

[App-V 5.1 Server 배포 방법](how-to-deploy-the-app-v-51-server.md)
