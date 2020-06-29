---
title: App-V 5.0 Server 배포 방법
description: App-V 5.0 Server 배포 방법
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814177"
---
# <span data-ttu-id="f596c-103">App-V 5.0 Server 배포 방법</span><span class="sxs-lookup"><span data-stu-id="f596c-103">How to Deploy the App-V 5.0 Server</span></span>


<span data-ttu-id="f596c-104">다음 절차를 사용 하 여 App-v 5.0 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-104">Use the following procedure to install the App-V 5.0 server.</span></span> <span data-ttu-id="f596c-105">App-v 5.0 SP3 서버 배포에 대 한 자세한 내용은 [앱-v 5.0 sp3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3)정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f596c-105">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

**<span data-ttu-id="f596c-106">시작 하기 전에:</span><span class="sxs-lookup"><span data-stu-id="f596c-106">Before you start:</span></span>**

-   <span data-ttu-id="f596c-107">필수 구성 요소 소프트웨어를 설치 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="f596c-108">[앱-V 5.0 필수 구성 요소](app-v-50-prerequisites.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f596c-108">See [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

-   <span data-ttu-id="f596c-109">[App-V 5.0 보안 고려](app-v-50-security-considerations.md)사항의 서버 섹션을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-109">Review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

-   <span data-ttu-id="f596c-110">각 구성 요소를 호스트할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="f596c-111">들어오는 요청에 대해 지정 된 포트에 액세스 하도록 허용 하는 방화벽 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="f596c-112">Windows Installer 대신 SQL 스크립트를 사용 하 여 관리 데이터베이스 또는 보고 데이터베이스를 설정 하는 경우 관리 서버 또는 보고 서버를 설치 하기 전에 SQL 스크립트를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="f596c-113">[SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법을](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f596c-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).</span></span>

**<span data-ttu-id="f596c-114">App-v 5.0 서버를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="f596c-114">To install the App-V 5.0 server</span></span>**

1. <span data-ttu-id="f596c-115">설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-115">Copy the App-V 5.0 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="f596c-116">관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 고 실행 하 여 app-v 5.0 서버 설치를 시작 하 고 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-116">Start the App-V 5.0 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="f596c-117">사용 조건을 검토 하 고 동의한 다음 Microsoft 업데이트를 사용할지 여부를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="f596c-118">**기능 선택** 페이지에서 다음 구성 요소를 모두 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f596c-119">구성 요소</span><span class="sxs-lookup"><span data-stu-id="f596c-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="f596c-120">설명</span><span class="sxs-lookup"><span data-stu-id="f596c-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f596c-121">관리 서버</span><span class="sxs-lookup"><span data-stu-id="f596c-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-122">App-v 인프라에 대 한 전반적인 관리 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f596c-123">관리 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f596c-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-124">앱-V 관리를 위한 데이터베이스 사전 배포를 용이 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f596c-125">게시 서버</span><span class="sxs-lookup"><span data-stu-id="f596c-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-126">가상 응용 프로그램에 대 한 호스팅 및 스트리밍 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f596c-127">보고 서버</span><span class="sxs-lookup"><span data-stu-id="f596c-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-128">앱-V 5.0 reporting services를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-128">Provides App-V 5.0 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f596c-129">보고 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f596c-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-130">앱-V reporting에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="f596c-131">**설치 위치** 페이지에서 선택한 구성 요소가 설치 될 기본 위치를 적용 하거나 **설치 위치** 줄에 새 경로를 입력 하 여 위치를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="f596c-132">초기 **새 관리 데이터베이스 만들기** 페이지에서 아래에서 적절 한 옵션을 선택 하 여 **Microsoft SQL Server 인스턴스** 및 **관리 서버 데이터베이스** 를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f596c-133">메서드</span><span class="sxs-lookup"><span data-stu-id="f596c-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="f596c-134">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="f596c-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f596c-135">사용자 지정 Microsoft SQL Server 인스턴스를 사용 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-136"><strong>사용자 지정 인스턴스 사용 </strong> 을 선택 하 고 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="f596c-137">형식 인스턴스를 <strong> 사용 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="f596c-138">가정 된 설치 위치는 로컬 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="f596c-139">지원 되지 않음: ServerName의 strong format 인스턴스를 사용 하는 서버 이름 <strong> </strong> &lt; &gt; </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f596c-140">사용자 지정 데이터베이스 이름을 사용 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-141"><strong>사용자 지정 구성을 선택 </strong> 하 고 데이터베이스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="f596c-142">데이터베이스 이름은 고유 해야 하며 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="f596c-143">**구성** 페이지에서 기본 값인 **이 로컬 컴퓨터 사용**을 그대로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="f596c-144">참고</span><span class="sxs-lookup"><span data-stu-id="f596c-144">Note</span></span>**  
   <span data-ttu-id="f596c-145">관리 서버 및 관리 데이터베이스를 나란히 설치 하는 경우에는이 페이지의 일부 옵션을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="f596c-146">이 경우 적절 한 옵션이 기본적으로 선택 되어 있으며 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="f596c-147">초기 **새 보고 데이터베이스 만들기** 페이지에서 아래에서 적절 한 옵션을 선택 하 여 **Microsoft SQL Server 인스턴스** 및 **보고 서버 데이터베이스** 를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f596c-148">메서드</span><span class="sxs-lookup"><span data-stu-id="f596c-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="f596c-149">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="f596c-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f596c-150">사용자 지정 Microsoft SQL Server 인스턴스를 사용 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-151"><strong>사용자 지정 인스턴스 사용 </strong> 을 선택 하 고 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="f596c-152">형식 인스턴스를 <strong> 사용 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="f596c-153">가정 된 설치 위치는 로컬 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="f596c-154">지원 되지 않음: ServerName의 strong format 인스턴스를 사용 하는 서버 이름 <strong> </strong> &lt; &gt; </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f596c-155">사용자 지정 데이터베이스 이름을 사용 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f596c-156"><strong>사용자 지정 구성을 선택 </strong> 하 고 데이터베이스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="f596c-157">데이터베이스 이름은 고유 해야 하며 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="f596c-158">**구성** 페이지에서 기본값을 적용 합니다. **이 로컬 컴퓨터를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="f596c-159">참고</span><span class="sxs-lookup"><span data-stu-id="f596c-159">Note</span></span>**  
   <span data-ttu-id="f596c-160">관리 서버 및 관리 데이터베이스를 나란히 설치 하는 경우에는이 페이지의 일부 옵션을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="f596c-161">이 경우 적절 한 옵션이 기본적으로 선택 되어 있으며 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="f596c-162">**구성** (관리 서버 구성) 페이지에서 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f596c-163">구성할 항목</span><span class="sxs-lookup"><span data-stu-id="f596c-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="f596c-164">설명 및 예제</span><span class="sxs-lookup"><span data-stu-id="f596c-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f596c-165">앱-V 환경을 관리할 수 있는 권한이 있는 광고 그룹을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-166">예: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="f596c-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="f596c-167">설치 후 관리 콘솔을 사용 하 여 다른 사용자 또는 그룹을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="f596c-168">그러나 전역 보안 그룹과 AD DS (Active Directory 도메인 서비스) 메일 그룹은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="f596c-169"><strong> </strong> <strong> </strong> 이 작업을 수행 하려면 도메인 로컬 또는 유니버설 그룹을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="f596c-170">웹 사이트 이름 </strong> : 게시 서비스를 실행 하는 데 사용 되는 사용자 지정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-171">사용자 지정 이름이 없는 경우에는 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="f596c-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f596c-172">포트 바인딩 </strong> : app-v에 사용 되는 고유한 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-173">예: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="f596c-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="f596c-174">지정 된 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="f596c-175">**게시 서버 구성** **구성** 페이지에서 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f596c-176">구성할 항목</span><span class="sxs-lookup"><span data-stu-id="f596c-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="f596c-177">설명 및 예제</span><span class="sxs-lookup"><span data-stu-id="f596c-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f596c-178">관리 서비스의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-179">예<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="f596c-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="f596c-180">웹 사이트 이름 </strong> : 게시 서비스를 실행 하는 데 사용 되는 사용자 지정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-181">사용자 지정 이름이 없는 경우에는 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="f596c-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f596c-182">포트 바인딩 </strong> : app-v에 사용 되는 고유한 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-183">예: 54321</span><span class="sxs-lookup"><span data-stu-id="f596c-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="f596c-184">지정 된 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="f596c-185">**보고 서버** 페이지에서 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f596c-186">구성할 항목</span><span class="sxs-lookup"><span data-stu-id="f596c-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="f596c-187">설명 및 예제</span><span class="sxs-lookup"><span data-stu-id="f596c-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f596c-188">웹 사이트 이름 </strong> : 보고 서비스를 실행 하는 데 사용 되는 사용자 지정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-189">사용자 지정 이름이 없는 경우에는 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="f596c-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="f596c-190">포트 바인딩 </strong> : app-v에 사용 되는 고유한 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f596c-191">예: 55555</span><span class="sxs-lookup"><span data-stu-id="f596c-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="f596c-192">지정 된 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="f596c-193">설치를 시작 하려면 **준비** 페이지에서 **설치** 를 클릭 한 다음 **완료** 페이지에서 **닫기를** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="f596c-194">설치가 성공적으로 완료 되었는지 확인 하려면 웹 브라우저를 열고 다음 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="f596c-195">**http:// &lt; 관리 서버 컴퓨터 이름 &gt; : &lt; 관리 서비스 포트 번호 &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="f596c-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="f596c-196">예: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="f596c-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="f596c-197">설치가 완료 되 면 앱에 오류 없이 App-v 관리 콘솔이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="f596c-198">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="f596c-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f596c-199">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f596c-200">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="f596c-200">Got an App-V issue?</span></span>** <span data-ttu-id="f596c-201">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f596c-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f596c-202">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f596c-202">Related topics</span></span>


[<span data-ttu-id="f596c-203">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="f596c-203">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="f596c-204">관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="f596c-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="f596c-205">원격 컴퓨터에 게시 서버를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="f596c-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="f596c-206">스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="f596c-206">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="f596c-207">PowerShell을 사용하여 App-V 5.0 Client에서 보고를 사용하도록 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="f596c-207">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





