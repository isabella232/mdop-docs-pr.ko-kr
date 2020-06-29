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
# <span data-ttu-id="6b264-103">스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="6b264-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="6b264-104">명령줄을 사용 하 여 **appv\_server\_setup.exe** 서버 설치를 완료 하려면 여러 매개 변수를 지정 하 고 결합 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="6b264-105">명령줄을 사용 하 여 App-v 5.0 서버를 설치 하는 방법에 대 한 자세한 내용은 다음 표를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b264-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="6b264-106">다음 표의 정보는 다음 명령을 입력 하 여 명령줄을 사용 하 여 액세스할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="6b264-107">공통 매개 변수 및 예제</span><span class="sxs-lookup"><span data-stu-id="6b264-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-108">로컬 컴퓨터에 관리 서버 및 관리 데이터베이스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-109">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-117">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-125">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-126">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="6b264-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="6b264-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="6b264-129">/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV Management 서비스"</span><span class="sxs-lookup"><span data-stu-id="6b264-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="6b264-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="6b264-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="6b264-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="6b264-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="6b264-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-134">로컬 컴퓨터의 기존 관리 데이터베이스를 사용 하 여 관리 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-135">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-143">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-151">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-152">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="6b264-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="6b264-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="6b264-155">/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV Management 서비스"</span><span class="sxs-lookup"><span data-stu-id="6b264-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="6b264-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="6b264-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="6b264-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="6b264-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="6b264-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-160">원격 컴퓨터의 기존 관리 데이터베이스를 사용 하 여 관리 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-161">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-169">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-177">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-178">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="6b264-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="6b264-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="6b264-181">/MANAGEMENT_WEBSITE_NAME = "Microsoft AppV Management 서비스"</span><span class="sxs-lookup"><span data-stu-id="6b264-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="6b264-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="6b264-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="6b264-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine"</span><span class="sxs-lookup"><span data-stu-id="6b264-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="6b264-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="6b264-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-186">관리 데이터베이스와 관리 서버를 같은 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-187">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-193">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-199">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-200">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="6b264-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="6b264-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="6b264-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="6b264-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="6b264-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-206">관리 서버와 다른 컴퓨터에 관리 데이터베이스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-207">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-213">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-219">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-220">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="6b264-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="6b264-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="6b264-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="6b264-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="6b264-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="6b264-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-226">게시 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-227">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-232">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-233">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="6b264-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="6b264-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="6b264-236">/PUBLISHING_WEBSITE_NAME = "Microsoft AppV Publishing 서비스"</span><span class="sxs-lookup"><span data-stu-id="6b264-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="6b264-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="6b264-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-238">로컬 컴퓨터에 보고 서버 및 보고 데이터베이스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-239">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-240">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-241">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-242">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-244">/보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-245">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-246">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-247">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-248">/보고 _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-249">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-250">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-252">/보고 _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-253">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-254">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-255">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="6b264-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-257">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="6b264-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="6b264-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="6b264-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="6b264-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="6b264-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="6b264-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
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
    <td align="left"><p><span data-ttu-id="6b264-262">로컬 컴퓨터에서 보고 서버를 설치 하 고 기존 보고 데이터베이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-263">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-264">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-265">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-266">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-270">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-271">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-272">/보고 _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-273">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-274">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-278">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-279">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="6b264-281">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="6b264-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="6b264-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="6b264-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="6b264-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="6b264-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="6b264-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-286">원격 컴퓨터의 기존 보고 데이터베이스를 사용 하 여 보고 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-287">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-288">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-289">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-290">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-294">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-295">/보고 _SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="6b264-296">/보고 _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-297">/보고 _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-298">/보고 _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-302">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-303">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="6b264-305">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="6b264-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="6b264-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="6b264-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="6b264-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine"</span><span class="sxs-lookup"><span data-stu-id="6b264-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="6b264-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="6b264-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-310">보고 데이터베이스를 보고 서버와 같은 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-311">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-313">/보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-314">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-317">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-319">/보고 _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-320">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="6b264-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-323">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-324">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="6b264-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="6b264-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="6b264-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="6b264-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="6b264-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="6b264-330">보고 서버와 다른 컴퓨터에 보고 데이터베이스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-331">Microsoft SQL Server의 기본 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-333">/보고 _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-334">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-337">Microsoft SQL Server의 사용자 지정 인스턴스를 사용 하려면 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="6b264-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="6b264-339">/보고 _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="6b264-340">/보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="6b264-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="6b264-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="6b264-343">Microsoft SQL Server의 사용자 지정 인스턴스 사용 예:</span><span class="sxs-lookup"><span data-stu-id="6b264-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="6b264-344">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="6b264-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="6b264-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="6b264-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="6b264-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="6b264-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="6b264-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="6b264-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="6b264-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="6b264-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="6b264-350">매개 변수 정의</span><span class="sxs-lookup"><span data-stu-id="6b264-350">Parameter Definitions</span></span>

### <span data-ttu-id="6b264-351">일반 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-352">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-353">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-354">/QUIET</span><span class="sxs-lookup"><span data-stu-id="6b264-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-355">자동 설치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-356">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="6b264-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-357">제거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="6b264-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-359">레이아웃 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-359">Specifies layout action.</span></span> <span data-ttu-id="6b264-360">이렇게 하면 실제로 제품을 설치 하지 않고도 폴더에 MSIs 및 스크립트 파일의 압축이 풀립니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="6b264-361">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="6b264-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-363">레이아웃 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-363">Specifies the layout directory.</span></span> <span data-ttu-id="6b264-364">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-364">Takes a string.</span></span> <span data-ttu-id="6b264-365">예를 들어/LAYOUTDIR = "C:\Application Virtualization Server"</span><span class="sxs-lookup"><span data-stu-id="6b264-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="6b264-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-367">설치 디렉터리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-367">Specifies the installation directory.</span></span> <span data-ttu-id="6b264-368">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-368">Takes a string.</span></span> <span data-ttu-id="6b264-369">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-369">E.g.</span></span> <span data-ttu-id="6b264-370">/INSTALLDIR = "C:\Program Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="6b264-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="6b264-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-372">Microsoft 업데이트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-372">Enables Microsoft Update.</span></span> <span data-ttu-id="6b264-373">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="6b264-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-375">사용권 계약을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-375">Accepts the license agreement.</span></span> <span data-ttu-id="6b264-376">무인 설치에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-376">This is required for an unattended installation.</span></span> <span data-ttu-id="6b264-377">사용 예: <strong> /ACCEPTEULA </strong> 또는 <strong> /ACCEPTEULA = 1 </strong></span><span class="sxs-lookup"><span data-stu-id="6b264-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="6b264-378">관리 서버 설치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-379">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-380">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-382">관리 서버가 설치 됨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="6b264-383">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-385">관리 서버에 대 한 관리자 액세스를 허용 하는 계정을 지정 합니다 .이 계정은 개인 사용자 계정 이거나 그룹 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="6b264-386">사용 예: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b264-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="6b264-387"><strong>/MANAGEMENT_SERVER </strong> 를 지정 하지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="6b264-388">관리 서버에 대 한 관리자 액세스 권한이 허용 되는 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="6b264-389">이 계정은 사용자 계정 또는 그룹 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-389">This can be a user account or a group.</span></span> <span data-ttu-id="6b264-390">예를 들어 <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b264-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-392">관리 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="6b264-393">예를 들어/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V 관리 서비스"</span><span class="sxs-lookup"><span data-stu-id="6b264-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-395">관리 서비스에 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="6b264-396">예를 들어/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="6b264-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="6b264-397">관리 서버 데이터베이스용 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-398">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-399">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="6b264-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-401">관리 데이터베이스를 설치 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="6b264-402">이 설치를 완료 하려면 충분 한 데이터베이스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="6b264-403">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-405">기본 SQL 인스턴스를 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="6b264-406">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-408">새 데이터베이스를 만드는 데 사용 되는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="6b264-409">사용 예: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MYSQLSERVER" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b264-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="6b264-410">/DB_PREDEPLOY_MANAGEMENT를 지정 하지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-412">만들어야 하는 새 관리 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="6b264-413">사용 예: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b264-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="6b264-414">/DB_PREDEPLOY_MANAGEMENT를 지정 하지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-416">데이터베이스에 액세스할 관리 서버가 로컬 서버에 설치 되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="6b264-417">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-419">관리 서버가 설치 되는 원격 컴퓨터의 컴퓨터 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="6b264-420">사용 예: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</span><span class="sxs-lookup"><span data-stu-id="6b264-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-422">관리 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="6b264-423">사용 예: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\alias"</span><span class="sxs-lookup"><span data-stu-id="6b264-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="6b264-424">게시 서버를 설치 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-425">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-426">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-428">게시 서버가 설치 됨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="6b264-429">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-431">게시 서버가 연결 될 관리 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="6b264-432">사용 예: <strong> http:// &lt; management server name &gt; : &lt; 관리 서버 포트 번호 &gt; </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="6b264-433">/PUBLISHING_SERVER을 사용 하지 않으면이 매개 변수는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-435">게시 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="6b264-436">예를 들어/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing 서비스"</span><span class="sxs-lookup"><span data-stu-id="6b264-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-438">게시 서비스에 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="6b264-439">예를 들어/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="6b264-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="6b264-440">보고 서버용 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-441">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-442">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="6b264-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-444">보고 서버가 설치 됨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="6b264-445">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-447">보고 서비스에 대해 생성 되는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="6b264-448">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-448">E.g.</span></span> <span data-ttu-id="6b264-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="6b264-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-451">보고 서비스에 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="6b264-452">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-452">E.g.</span></span> <span data-ttu-id="6b264-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="6b264-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="6b264-454">기존 보고 서버 데이터베이스를 사용 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-455">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-456">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-458">Microsoft SQL Server가 로컬 서버에 설치 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="6b264-459">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-461">SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="6b264-462">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-462">Takes a string.</span></span> <span data-ttu-id="6b264-463">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-463">E.g.</span></span> <span data-ttu-id="6b264-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-465">/EXISTING_ 보고 <em> DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-466">기본 SQL 인스턴스가 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="6b264-467">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-468">/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-469">사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="6b264-470">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-470">Takes a string.</span></span> <span data-ttu-id="6b264-471">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-471">E.g.</span></span> <span data-ttu-id="6b264-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-473">/EXISTING_ 보고 _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-474">사용 해야 하는 기존 보고 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="6b264-475">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-475">Takes a string.</span></span> <span data-ttu-id="6b264-476">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-476">E.g.</span></span> <span data-ttu-id="6b264-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="6b264-478">보고 서버 데이터베이스를 설치 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-479">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-480">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="6b264-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-482">보고 데이터베이스를 설치 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="6b264-483">이 설치에는 DBA 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="6b264-484">값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-486">사용 해야 하는 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="6b264-487">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-487">Takes a string.</span></span> <span data-ttu-id="6b264-488">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-488">E.g.</span></span> <span data-ttu-id="6b264-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; MYSQLSERVER&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-491">만들어야 하는 새 보고 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="6b264-492">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-492">Takes a string.</span></span> <span data-ttu-id="6b264-493">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-493">E.g.</span></span> <span data-ttu-id="6b264-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-496">데이터베이스에 액세스할 보고 서버가 로컬 서버에 설치 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="6b264-497">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-499">Reporting server가 설치 될 원격 컴퓨터의 컴퓨터 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="6b264-500">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-500">Takes a string.</span></span> <span data-ttu-id="6b264-501">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-501">E.g.</span></span> <span data-ttu-id="6b264-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6b264-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-504">App-v 보고 서버를 설치 하는 데 사용 되는 관리자 계정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="6b264-505">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-505">Takes a string.</span></span> <span data-ttu-id="6b264-506">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-506">E.g.</span></span> <span data-ttu-id="6b264-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; domain\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="6b264-508">기존 관리 서버 데이터베이스를 사용 하기 위한 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="6b264-509">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b264-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="6b264-510">정보</span><span class="sxs-lookup"><span data-stu-id="6b264-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b264-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-512">로컬 서버에 SQL Server가 설치 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="6b264-513">매개 변수를 전환 하면 값이 필요 하지 않습니다. /DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-515">SQL Server가 설치 되어 있는 원격 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="6b264-516">문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-516">Takes a string.</span></span> <span data-ttu-id="6b264-517">예:</span><span class="sxs-lookup"><span data-stu-id="6b264-517">E.g.</span></span> <span data-ttu-id="6b264-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="6b264-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b264-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-520">기본 SQL 인스턴스가 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="6b264-521">매개 변수를 전환 하면 값이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="6b264-522">/DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="6b264-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="6b264-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-524">사용 될 사용자 지정 SQL 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="6b264-525">사용 예 <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b264-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="6b264-526">/DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="6b264-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6b264-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="6b264-528">사용 해야 하는 기존 관리 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="6b264-529">사용 예: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="6b264-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="6b264-530">/DB_PREDEPLOY_MANAGEMENT를 지정 하면이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="6b264-531">App-v에 대 한 제안이 있으십니까 </strong> ?</span><span class="sxs-lookup"><span data-stu-id="6b264-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="6b264-532">여기에서 제안을 추가 하거나 <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> 투표 </a> 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="6b264-533">App-v issu e를 얻었습니다 </strong> ?</span><span class="sxs-lookup"><span data-stu-id="6b264-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="6b264-534"><a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-v TechNet 포럼을 사용 </a> 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b264-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="6b264-535">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6b264-535">Related topics</span></span>

[<span data-ttu-id="6b264-536">App-V 5.0 Server 배포</span><span class="sxs-lookup"><span data-stu-id="6b264-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





