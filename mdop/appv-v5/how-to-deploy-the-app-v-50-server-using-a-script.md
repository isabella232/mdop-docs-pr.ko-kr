---
title: 스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법
description: 스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814169"
---
# 스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법


명령줄을 사용 하 여 **appv\_server\_setup.exe** 서버 설치를 완료 하려면 여러 매개 변수를 지정 하 고 결합 해야 합니다.

명령줄을 사용 하 여 App-v 5.0 서버를 설치 하는 방법에 대 한 자세한 내용은 다음 표를 사용 하세요.

>[!NOTE]
> 다음 표의 정보는 다음 명령을 입력 하 여 명령줄을 사용 하 여 액세스할 수도 있습니다.
>```
> appv\_server\_setup.exe /?
>```

## 공통 매개 변수 및 예제

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>로컬 컴퓨터에 관리 서버 및 관리 데이터베이스를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV Management 서비스"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>로컬 컴퓨터의 기존 관리 데이터베이스를 사용 하 여 관리 서버를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV Management 서비스"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>원격 컴퓨터의 기존 관리 데이터베이스를 사용 하 여 관리 서버를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV Management 서비스"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine"</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>관리 데이터베이스와 관리 서버를 같은 컴퓨터에 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>관리 서버와 다른 컴퓨터에 관리 데이터베이스를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>게시 서버를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/PUBLISHING_SERVER</p></li>
    <li><p>/PUBLISHING_MGT_SERVER</p></li>
    <li><p>/PUBLISHING_WEBSITE_NAME</p></li>
    <li><p>/PUBLISHING_WEBSITE_PORT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/PUBLISHING_SERVER</p>
    <p>/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</p>
    <p>/PUBLISHING_WEBSITE_NAME = "Microsoft AppV Publishing 서비스"</p>
    <p>/PUBLISHING_WEBSITE_PORT = "8081"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>로컬 컴퓨터에 보고 서버 및 보고 데이터베이스를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/보고 _SERVER</p></li>
    <li><p>/보고 _WEBSITE_NAME</p></li>
    <li><p>/보고 _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/보고 _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/보고 _DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/보고 _SERVER</p></li>
    <li><p>/보고 _ADMINACCOUNT</p></li>
    <li><p>/보고 _WEBSITE_NAME</p></li>
    <li><p>/보고 _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/보고 _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/보고 _DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <ul>
    <li><p>/appv_server_setup.exe/QUIET</p></li>
    <li><p>/REPORTING_SERVER</p></li>
    <li><p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p></li>
    <li><p>/REPORTING_WEBSITE_PORT = "8082"</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p></li>
    <li><p>/REPORTING_DB_NAME = "AppVReporting"</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>로컬 컴퓨터에서 보고 서버를 설치 하 고 기존 보고 데이터베이스를 사용 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/보고 _SERVER</p></li>
    <li><p>/보고 _WEBSITE_NAME</p></li>
    <li><p>/보고 _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/보고 _SERVER</p></li>
    <li><p>/보고 _ADMINACCOUNT</p></li>
    <li><p>/보고 _WEBSITE_NAME</p></li>
    <li><p>/보고 _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>원격 컴퓨터의 기존 보고 데이터베이스를 사용 하 여 보고 서버를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/보고 _SERVER</p></li>
    <li><p>/보고 _WEBSITE_NAME</p></li>
    <li><p>/보고 _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/보고 _SERVER</p></li>
    <li><p>/보고 _ADMINACCOUNT</p></li>
    <li><p>/보고 _WEBSITE_NAME</p></li>
    <li><p>/보고 _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine"</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>보고 데이터베이스를 보고 서버와 같은 컴퓨터에 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/보고 _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/보고 _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/보고 _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/보고 _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>보고 서버와 다른 컴퓨터에 보고 데이터베이스를 설치 합니다.</p></td>
    <td align="left"><p>Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/보고 _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/보고 _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/보고 _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/보고 _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

## 매개 변수 정의

### 일반 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/QUIET</p></td>
    <td align="left"><p>자동 설치를 지정 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/UNINSTALL</p></td>
    <td align="left"><p>제거를 지정 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/LAYOUT</p></td>
    <td align="left"><p>레이아웃 작업을 지정 합니다. 이렇게 하면 실제로 제품을 설치 하지 않고도 폴더에 MSIs 및 스크립트 파일의 압축이 풀립니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/LAYOUTDIR</p></td>
    <td align="left"><p>레이아웃 디렉터리를 지정 합니다. 문자열을 가져옵니다. 예를 들어/LAYOUTDIR = "C:\Application Virtualization Server"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/INSTALLDIR</p></td>
    <td align="left"><p>설치 디렉터리를 지정 합니다. 문자열을 가져옵니다. 예: /INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MUOPTIN</p></td>
    <td align="left"><p>Microsoft 업데이트를 사용 하도록 설정 합니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/ACCEPTEULA</p></td>
    <td align="left"><p>사용권 계약을 수락 합니다. 무인 설치에 필요 합니다. 사용 예: <strong> /ACCEPTEULA </strong> 또는 <strong> /ACCEPTEULA = 1 </strong></p></td>
    </tr>
    </tbody>
    </table>

### 관리 서버 설치 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER</p></td>
    <td align="left"><p>관리 서버가 설치 됨을 지정 합니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_ADMINACCOUNT</p></td>
    <td align="left"><p>관리 서버에 대 한 관리자 액세스를 허용 하는 계정을 지정 합니다 .이 계정은 개인 사용자 계정 이거나 그룹 일 수 있습니다. 사용 예: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> . <strong>/MANAGEMENT_SERVER </strong> 를 지정 하지 않으면 무시 됩니다. 관리 서버에 대 한 관리자 액세스 권한이 허용 되는 계정을 지정 합니다. 이 계정은 사용자 계정 또는 그룹 일 수 있습니다. 예를 들어 <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_WEBSITE_NAME</p></td>
    <td align="left"><p>관리 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다. 예를 들어/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V 관리 서비스"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MANAGEMENT_WEBSITE_PORT</p></td>
    <td align="left"><p>관리 서비스에 사용 되는 포트 번호를 지정 합니다. 예를 들어/MANAGEMENT_WEBSITE_PORT = 82.</p></td>
    </tr>
    </tbody>
    </table>

### 관리 서버 데이터베이스용 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_MANAGEMENT</p></td>
    <td align="left"><p>관리 데이터베이스를 설치 하도록 지정 합니다. 이 설치를 완료 하려면 충분 한 데이터베이스 권한이 있어야 합니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>기본 SQL 인스턴스를 사용 해야 함을 나타냅니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>새 데이터베이스를 만드는 데 사용 되는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 사용 예: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER" </strong> . /DB_PREDEPLOY_MANAGEMENT를 지정 하지 않으면 무시 됩니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>만들어야 하는 새 관리 데이터베이스의 이름을 지정 합니다. 사용 예: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . /DB_PREDEPLOY_MANAGEMENT를 지정 하지 않으면 무시 됩니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>데이터베이스에 액세스할 관리 서버가 로컬 서버에 설치 되어 있는지 여부를 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>관리 서버가 설치 되는 원격 컴퓨터의 컴퓨터 계정을 지정 합니다. 사용 예: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>관리 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다. 사용 예: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\alias"</strong></p></td>
    </tr>
    </tbody>
    </table>

### 게시 서버를 설치 하기 위한 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_SERVER</p></td>
    <td align="left"><p>게시 서버가 설치 됨을 지정 합니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_MGT_SERVER</p></td>
    <td align="left"><p>게시 서버가 연결 될 관리 서비스의 URL을 지정 합니다. 사용 예: <strong> http:// &lt; management server name &gt; : &lt; 관리 서버 포트 번호 &gt; </strong> 입니다. /PUBLISHING_SERVER을 사용 하지 않으면이 매개 변수는 무시 됩니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_WEBSITE_NAME</p></td>
    <td align="left"><p>게시 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다. 예를 들어/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing 서비스"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_WEBSITE_PORT</p></td>
    <td align="left"><p>게시 서비스에 사용 되는 포트 번호를 지정 합니다. 예를 들어/PUBLISHING_WEBSITE_PORT = 83</p></td>
    </tr>
    </tbody>
    </table>

### 보고 서버용 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/REPORTING_SERVER</p></td>
    <td align="left"><p>보고 서버가 설치 됨을 지정 합니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_WEBSITE_NAME</p></td>
    <td align="left"><p>보고 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다. 예: /REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_WEBSITE_PORT</p></td>
    <td align="left"><p>보고 서비스에 사용 되는 포트 번호를 지정 합니다. 예: /REPORTING_WEBSITE_PORT = 82</p></td>
    </tr>
    </tbody>
    </table>

     

### 기존 보고 서버 데이터베이스를 사용 하기 위한 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Microsoft SQL Server가 로컬 서버에 설치 되어 있음을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다. 문자열을 가져옵니다. 예: /EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ 보고 <em> DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>기본 SQL 인스턴스가 사용 됨을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 문자열을 가져옵니다. 예: /EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ 보고 _DB_NAME</p></td>
    <td align="left"><p>사용 해야 하는 기존 보고 데이터베이스의 이름을 지정 합니다. 문자열을 가져옵니다. 예: /EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</p></td>
    </tr>
    </tbody>
    </table>

### 보고 서버 데이터베이스를 설치 하기 위한 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_REPORTING</p></td>
    <td align="left"><p>보고 데이터베이스를 설치 하도록 지정 합니다. 이 설치에는 DBA 권한이 필요 합니다. 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 문자열을 가져옵니다. 예: /REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_DB_NAME</p></td>
    <td align="left"><p>만들어야 하는 새 보고 데이터베이스의 이름을 지정 합니다. 문자열을 가져옵니다. 예: /REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>데이터베이스에 액세스할 보고 서버가 로컬 서버에 설치 되어 있음을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Reporting server가 설치 될 원격 컴퓨터의 컴퓨터 계정을 지정 합니다. 문자열을 가져옵니다. 예: /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>App-v 보고 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다. 문자열을 가져옵니다. 예: /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; domain\alias&quot;</p></td>
    </tr>
    </tbody>
    </table>

### 기존 관리 서버 데이터베이스를 사용 하기 위한 매개 변수

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">정보</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>로컬 서버에 SQL Server가 설치 되어 있음을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. /DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다. 문자열을 가져옵니다. 예: /EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>기본 SQL 인스턴스가 사용 됨을 나타냅니다. 매개 변수를 전환 하면 값이 필요 하지 않습니다. /DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>사용 될 사용자 지정 SQL 인스턴스의 이름을 지정 합니다. 사용 예 <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> . /DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>사용 해야 하는 기존 관리 데이터베이스의 이름을 지정 합니다. 사용 예: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . /DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</p>
    <p></p>
    <p><strong>App-v에 대 한 제안이 있으십니까 </strong> ? 여기에서 제안을 추가 하거나 <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> 투표 </a> 합니다. <strong>App-v issu e를 얻었습니다 </strong> ? <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-v TechNet 포럼을 사용 </a> 합니다.</p></td>
</tr>
</tbody>
</table>
  

## 관련 항목

[App-V 5.0 Server 배포](deploying-the-app-v-50-server.md)

 

 





