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
# <span data-ttu-id="d675c-103">스크립트를 사용하여 App-V 5.1 Server를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="d675c-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="d675c-104">명령줄을 사용 하 여 **appv\_server\_setup.exe** 서버 설치를 완료 하려면 여러 매개 변수를 지정 하 고 결합 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="d675c-105">스크립트를 사용 하 여 App-v 5.1 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="d675c-106">명령줄을 사용 하 여 App-v 5.1 서버를 설치 하는 방법에 대 한 다음 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d675c-107">다음 표에는 **appv\_server\_setup.exe/?** 명령을 입력 하 여 명령줄을 사용 하 여이 정보에 액세스할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="d675c-108">로컬 컴퓨터에 관리 서버 및 관리 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="d675c-109">다음 매개 변수는 Microsoft SQL Server의 기본 인스턴스와 사용자 지정 인스턴스 모두에 대해 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="d675c-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="d675c-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="d675c-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="d675c-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="d675c-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="d675c-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="d675c-117">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용</span><span class="sxs-lookup"><span data-stu-id="d675c-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="d675c-118">로컬 컴퓨터에서 기존 관리 데이터베이스를 사용 하 여 관리 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="d675c-119">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="d675c-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="d675c-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="d675c-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="d675c-127">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이).</span><span class="sxs-lookup"><span data-stu-id="d675c-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="d675c-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="d675c-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="d675c-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="d675c-135">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용</span><span class="sxs-lookup"><span data-stu-id="d675c-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="d675c-136">원격 컴퓨터에서 기존 관리 데이터베이스를 사용 하 여 관리 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="d675c-137">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="d675c-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="d675c-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="d675c-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="d675c-145">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="d675c-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="d675c-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="d675c-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="d675c-153">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="d675c-154">동일한 컴퓨터에 관리 데이터베이스와 관리 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="d675c-155">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="d675c-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="d675c-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="d675c-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="d675c-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="d675c-161">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="d675c-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="d675c-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="d675c-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="d675c-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="d675c-167">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용</span><span class="sxs-lookup"><span data-stu-id="d675c-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="d675c-168">관리 서버와 다른 컴퓨터에 관리 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="d675c-169">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="d675c-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="d675c-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="d675c-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="d675c-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="d675c-175">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="d675c-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="d675c-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="d675c-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="d675c-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="d675c-181">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용</span><span class="sxs-lookup"><span data-stu-id="d675c-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="d675c-182">게시 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-182">Install the publishing server</span></span>

<span data-ttu-id="d675c-183">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="d675c-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="d675c-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="d675c-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="d675c-188">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="d675c-189">로컬 컴퓨터에 보고 서버 및 보고 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="d675c-190">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-191">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="d675c-192">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-193">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="d675c-195">/보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-196">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="d675c-197">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-198">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="d675c-199">/보고 _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="d675c-200">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-201">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="d675c-203">/보고 _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-204">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="d675c-205">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="d675c-206">로컬 컴퓨터에서 보고 서버 설치 및 기존 보고 데이터베이스 사용</span><span class="sxs-lookup"><span data-stu-id="d675c-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="d675c-207">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-208">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="d675c-209">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-210">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="d675c-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="d675c-214">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-215">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="d675c-216">/보고 _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="d675c-217">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-218">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="d675c-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="d675c-222">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="d675c-223">원격 컴퓨터에서 기존 보고 데이터베이스를 사용 하 여 보고 서버 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="d675c-224">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-225">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="d675c-226">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-227">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="d675c-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="d675c-231">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-232">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="d675c-233">/보고 _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="d675c-234">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="d675c-235">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="d675c-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="d675c-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="d675c-239">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="d675c-240">보고 데이터베이스를 보고서 서버와 같은 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="d675c-241">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="d675c-243">/보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="d675c-244">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="d675c-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="d675c-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="d675c-247">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="d675c-249">/보고 _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="d675c-250">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="d675c-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="d675c-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="d675c-253">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="d675c-254">보고 서버와 다른 컴퓨터에 보고 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="d675c-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="d675c-255">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 사용자 지정 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="d675c-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="d675c-257">/보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="d675c-258">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="d675c-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="d675c-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="d675c-261">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다 ( *기울임꼴로*표시 된 기본 인스턴스의 차이점).</span><span class="sxs-lookup"><span data-stu-id="d675c-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="d675c-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="d675c-263">/보고 _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="d675c-264">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="d675c-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="d675c-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="d675c-267">예: Microsoft SQL Server의 사용자 지정 인스턴스 사용:</span><span class="sxs-lookup"><span data-stu-id="d675c-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="d675c-268">매개 변수 정의</span><span class="sxs-lookup"><span data-stu-id="d675c-268">Parameter Definitions</span></span>

#### <span data-ttu-id="d675c-269">일반 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-269">General Parameters</span></span>

| <span data-ttu-id="d675c-270">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-270">Parameter</span></span> | <span data-ttu-id="d675c-271">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-271">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-272">/QUIET</span><span class="sxs-lookup"><span data-stu-id="d675c-272">/QUIET</span></span> | <span data-ttu-id="d675c-273">자동 설치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-273">Specifies silent install.</span></span> |
| <span data-ttu-id="d675c-274">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="d675c-274">/UNINSTALL</span></span> | <span data-ttu-id="d675c-275">제거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="d675c-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="d675c-276">/LAYOUT</span></span> | <span data-ttu-id="d675c-277">레이아웃 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-277">Specifies layout action.</span></span> <span data-ttu-id="d675c-278">이렇게 하면 실제로 제품을 설치 하지 않고도 폴더에 MSIs 및 스크립트 파일의 압축이 풀립니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="d675c-279">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-279">No value is expected.</span></span> |
| <span data-ttu-id="d675c-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="d675c-280">/LAYOUTDIR</span></span> | <span data-ttu-id="d675c-281">레이아웃 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-281">Specifies the layout directory.</span></span> <span data-ttu-id="d675c-282">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-282">Takes a string.</span></span> <span data-ttu-id="d675c-283">사용 예: **/Layoutdir = "C:\\Application Virtualization Server"**</span><span class="sxs-lookup"><span data-stu-id="d675c-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="d675c-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="d675c-284">/INSTALLDIR</span></span> | <span data-ttu-id="d675c-285">설치 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-285">Specifies the installation directory.</span></span> <span data-ttu-id="d675c-286">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-286">Takes a string.</span></span> <span data-ttu-id="d675c-287">사용 예: **/INSTALLDIR = "C:\\program files Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="d675c-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="d675c-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="d675c-288">/MUOPTIN</span></span> | <span data-ttu-id="d675c-289">Microsoft 업데이트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-289">Enables Microsoft Update.</span></span> <span data-ttu-id="d675c-290">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-290">No value is expected.</span></span> |
| <span data-ttu-id="d675c-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="d675c-291">/ACCEPTEULA</span></span> | <span data-ttu-id="d675c-292">사용권 계약을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-292">Accepts the license agreement.</span></span> <span data-ttu-id="d675c-293">무인 설치에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-293">This is required for an unattended installation.</span></span> <span data-ttu-id="d675c-294">사용 예: **/ACCEPTEULA** 또는 **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="d675c-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="d675c-295">관리 서버 설치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="d675c-296">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-296">Parameter</span></span> |<span data-ttu-id="d675c-297">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-297">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="d675c-299">관리 서버가 설치 됨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="d675c-300">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-300">No value is expected</span></span> |
| <span data-ttu-id="d675c-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="d675c-302">관리 서버에 대 한 관리자 액세스가 허용 되는 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="d675c-303">이 계정은 사용자 계정 또는 그룹 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-303">This can be a user account or a group.</span></span> <span data-ttu-id="d675c-304">사용 예: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**.</span><span class="sxs-lookup"><span data-stu-id="d675c-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="d675c-305">**/MANAGEMENT_SERVER** 를 지정 하지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="d675c-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="d675c-307">관리 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="d675c-308">사용 예: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V 관리 서비스"**</span><span class="sxs-lookup"><span data-stu-id="d675c-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="d675c-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="d675c-310">관리 서비스에 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="d675c-311">사용 예: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="d675c-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="d675c-312">관리 서버 데이터베이스용 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="d675c-313">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-313">Parameter</span></span> | <span data-ttu-id="d675c-314">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-314">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="d675c-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="d675c-316">관리 데이터베이스를 설치 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="d675c-317">이 설치를 완료 하려면 충분 한 데이터베이스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="d675c-318">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-318">No value is expected.</span></span> |
| <span data-ttu-id="d675c-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="d675c-320">기본 SQL 인스턴스를 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="d675c-321">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-321">No value is expected.</span></span> |
| <span data-ttu-id="d675c-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="d675c-323">새 데이터베이스를 만드는 데 사용 되는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="d675c-324">사용 예: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**.</span><span class="sxs-lookup"><span data-stu-id="d675c-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="d675c-325">**/DB_PREDEPLOY_MANAGEMENT** 를 지정 하지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="d675c-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="d675c-327">만들어야 하는 새 관리 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="d675c-328">사용 예: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="d675c-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="d675c-329">**/DB_PREDEPLOY_MANAGEMENT** 를 지정 하지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="d675c-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="d675c-331">데이터베이스에 액세스할 관리 서버가 로컬 서버에 설치 되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="d675c-332">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="d675c-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="d675c-334">관리 서버가 설치 되는 원격 컴퓨터의 컴퓨터 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="d675c-335">사용 예: \**/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername \ \ \ \**</span><span class="sxs-lookup"><span data-stu-id="d675c-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="d675c-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="d675c-337">관리 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="d675c-338">사용 예: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="d675c-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="d675c-339">게시 서버를 설치 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="d675c-340">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-340">Parameter</span></span> | <span data-ttu-id="d675c-341">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-341">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="d675c-343">게시 서버가 설치 됨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="d675c-344">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-344">No value is expected.</span></span> |
| <span data-ttu-id="d675c-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="d675c-346">게시 서버가 연결 될 관리 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="d675c-347">사용 예: \*\*http:// &lt; management server name &gt; : &lt; 관리 서버 포트 번호 &gt; \*\*입니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="d675c-348">**/PUBLISHING_SERVER** 을 사용 하지 않으면이 매개 변수는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="d675c-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="d675c-350">게시 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="d675c-351">사용 예: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V PUBLISHING 서비스"**</span><span class="sxs-lookup"><span data-stu-id="d675c-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="d675c-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="d675c-353">게시 서비스에 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="d675c-354">사용 예: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="d675c-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="d675c-355">보고 서버용 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="d675c-356">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-356">Parameter</span></span> | <span data-ttu-id="d675c-357">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-357">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="d675c-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="d675c-359">보고 서버가 설치 됨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="d675c-360">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-360">No value is expected.</span></span> |
| <span data-ttu-id="d675c-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="d675c-362">보고 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="d675c-363">사용 예: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="d675c-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="d675c-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="d675c-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="d675c-365">보고 서비스에 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="d675c-366">사용 예: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="d675c-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="d675c-367">기존 보고 서버 데이터베이스를 사용 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="d675c-368">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-368">Parameter</span></span> | <span data-ttu-id="d675c-369">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-369">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="d675c-371">Microsoft SQL Server가 로컬 서버에 설치 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="d675c-372">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="d675c-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="d675c-374">SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="d675c-375">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-375">Takes a string.</span></span> <span data-ttu-id="d675c-376">사용 예: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="d675c-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="d675c-377">/EXISTING_ 보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="d675c-378">기본 SQL 인스턴스가 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="d675c-379">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="d675c-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="d675c-381">사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="d675c-382">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-382">Takes a string.</span></span> <span data-ttu-id="d675c-383">사용 예: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**</span><span class="sxs-lookup"><span data-stu-id="d675c-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="d675c-384">/EXISTING_ 보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="d675c-385">사용 해야 하는 기존 보고 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="d675c-386">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-386">Takes a string.</span></span> <span data-ttu-id="d675c-387">사용 예: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"**</span><span class="sxs-lookup"><span data-stu-id="d675c-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="d675c-388">보고 서버 데이터베이스를 설치 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="d675c-389">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-389">Parameter</span></span> | <span data-ttu-id="d675c-390">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-390">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="d675c-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="d675c-392">보고 데이터베이스를 설치 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="d675c-393">이 설치에는 DBA 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="d675c-394">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-394">No value is expected.</span></span> |
| <span data-ttu-id="d675c-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="d675c-396">사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="d675c-397">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-397">Takes a string.</span></span> <span data-ttu-id="d675c-398">사용 예: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER"**</span><span class="sxs-lookup"><span data-stu-id="d675c-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="d675c-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="d675c-400">만들어야 하는 새 보고 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="d675c-401">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-401">Takes a string.</span></span> <span data-ttu-id="d675c-402">사용 예: **/REPORTING_DB_NAME = "AppVMgmtDB"**</span><span class="sxs-lookup"><span data-stu-id="d675c-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="d675c-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="d675c-404">데이터베이스에 액세스할 보고 서버가 로컬 서버에 설치 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="d675c-405">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="d675c-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="d675c-407">Reporting server가 설치 될 원격 컴퓨터의 컴퓨터 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="d675c-408">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-408">Takes a string.</span></span> <span data-ttu-id="d675c-409">사용 예: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"**</span><span class="sxs-lookup"><span data-stu-id="d675c-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="d675c-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d675c-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="d675c-411">App-v 보고 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="d675c-412">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-412">Takes a string.</span></span> <span data-ttu-id="d675c-413">사용 예: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="d675c-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="d675c-414">기존 관리 서버 데이터베이스를 사용 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="d675c-415">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d675c-415">Parameter</span></span> | <span data-ttu-id="d675c-416">정보</span><span class="sxs-lookup"><span data-stu-id="d675c-416">Information</span></span> |
|--|--|
| <span data-ttu-id="d675c-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d675c-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="d675c-418">로컬 서버에 SQL Server가 설치 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="d675c-419">매개 변수를 전환 하면 값이 필요 하지 않습니다. **/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="d675c-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="d675c-421">SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="d675c-422">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-422">Takes a string.</span></span> <span data-ttu-id="d675c-423">사용 예: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="d675c-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="d675c-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="d675c-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="d675c-425">기본 SQL 인스턴스가 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="d675c-426">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="d675c-427">**/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="d675c-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="d675c-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="d675c-429">사용 될 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="d675c-430">사용 예 **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="d675c-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="d675c-431">**/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="d675c-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d675c-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="d675c-433">사용 해야 하는 기존 관리 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="d675c-434">사용 예: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="d675c-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="d675c-435">**/DB_PREDEPLOY_MANAGEMENT** 를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="d675c-436">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="d675c-436">Got an App-V issue?</span></span> <span data-ttu-id="d675c-437">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d675c-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d675c-438">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d675c-438">Related topics</span></span>

[<span data-ttu-id="d675c-439">App-V 5.1 Server 배포</span><span class="sxs-lookup"><span data-stu-id="d675c-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
