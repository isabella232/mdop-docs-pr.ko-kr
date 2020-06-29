---
title: SQL 스크립트를 사용하여 App-V 데이터베이스를 배포하는 방법
description: SQL 스크립트를 사용하여 App-V 데이터베이스를 배포하는 방법
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814113"
---
# <span data-ttu-id="f63ef-103">SQL 스크립트를 사용하여 App-V 데이터베이스를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="f63ef-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="f63ef-104">다음 지침을 사용 하 여 Windows Installer 대신 SQL 스크립트를 사용 하 여 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="f63ef-105">App-v 5.0 데이터베이스 설치</span><span class="sxs-lookup"><span data-stu-id="f63ef-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="f63ef-106">5.0 데이터베이스를 최신 버전으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f63ef-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="f63ef-107">SQL 스크립트를 사용 하 여 앱 V 데이터베이스를 설치 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f63ef-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="f63ef-108">데이터베이스 스크립트를 설치 하기 전에 App-v 라이선스 조건의 복사본을 검토 하 고 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="f63ef-109">데이터베이스 스크립트를 실행 하 여 사용 조건에 동의 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="f63ef-110">동의 하지 않는 경우에는이 소프트웨어를 사용해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="f63ef-111">App-v release 미디어의 **appv\_server\_setup.exe** 임시 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="f63ef-112">명령 프롬프트에서 **appv\_server\_setup.exe** 를 실행 하 고 데이터베이스 스크립트를 추출 하는 임시 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="f63ef-113">예: appv\_server\_setup.exe/layout c:\\ &lt; 임시 위치 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="f63ef-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="f63ef-114">만든 임시 위치로 이동 하 고 추출한 **Databasescripts** 폴더를 연 다음 적절 한 Readme.txt 파일을 검토 하 여 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="f63ef-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f63ef-115">데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f63ef-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="f63ef-116">사용할 Readme.txt 파일의 위치</span><span class="sxs-lookup"><span data-stu-id="f63ef-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f63ef-117">관리 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f63ef-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f63ef-118">ManagementDatabase 하위 폴더</span><span class="sxs-lookup"><span data-stu-id="f63ef-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f63ef-119">중요</span><span class="sxs-lookup"><span data-stu-id="f63ef-119">Important</span></span></strong><br/><p><span data-ttu-id="f63ef-120">App-v 5.0 SP3 관리 데이터베이스를 업그레이드 하거나 설치 하는 경우 <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> 앱-v 5.0 Sp3 관리 서버 데이터베이스 설치 또는 업그레이드에 대 한 SQL 스크립트를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="f63ef-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f63ef-121">보고 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f63ef-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f63ef-122">ReportingDatabase 하위 폴더</span><span class="sxs-lookup"><span data-stu-id="f63ef-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="f63ef-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f63ef-123">Related topics</span></span>


[<span data-ttu-id="f63ef-124">App-V 5.0 Server 배포</span><span class="sxs-lookup"><span data-stu-id="f63ef-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="f63ef-125">App-V 5.0 Server 배포 방법</span><span class="sxs-lookup"><span data-stu-id="f63ef-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









