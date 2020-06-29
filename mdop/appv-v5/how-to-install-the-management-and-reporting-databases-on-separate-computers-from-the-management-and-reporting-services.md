---
title: 관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법
description: 관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814025"
---
# <span data-ttu-id="2c2c3-103">관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="2c2c3-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="2c2c3-104">다음 절차를 사용 하 여 데이터베이스 서버와 관리 서버를 서로 다른 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="2c2c3-105">데이터베이스 서버를 설치 하려는 컴퓨터에서 지원 되는 Microsoft SQL 버전을 실행 하 고 있어야 하며 설치에 실패 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="2c2c3-106">참고</span><span class="sxs-lookup"><span data-stu-id="2c2c3-106">Note</span></span>**  
<span data-ttu-id="2c2c3-107">배포를 완료 한 후 관리자가 서비스를 설치 하 여 해당 데이터베이스에 연결할 수 있으려면 **MICROSOFT SQL Server 이름**, **인스턴스 이름** 및 **데이터베이스 이름이** 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="2c2c3-108">관리 데이터베이스와 관리 서버를 별도의 컴퓨터에 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="2c2c3-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="2c2c3-109">설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="2c2c3-110">App-v 5.0 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="2c2c3-111">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-111">Click **Install**.</span></span>

2.  <span data-ttu-id="2c2c3-112">**시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="2c2c3-113">**Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="2c2c3-114">Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="2c2c3-115">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-115">Click **Next**.</span></span>

4.  <span data-ttu-id="2c2c3-116">**기능 선택** 페이지에서 **관리 서버 데이터베이스** 확인란을 선택 하 여 설치 하려는 구성 요소를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="2c2c3-117">**설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="2c2c3-118">초기 **새 관리 서버 데이터베이스 만들기 페이지**에서 필요에 따라 기본 선택 항목을 적용 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="2c2c3-119">사용자 지정 SQL Server 인스턴스를 사용 하는 경우 **사용자 지정 인스턴스 사용** 을 선택 하 고 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="2c2c3-120">사용자 지정 데이터베이스 이름을 사용 하는 경우 **사용자 지정 구성을** 선택 하 고 데이터베이스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="2c2c3-121">다음 **새 관리 서버 데이터베이스 만들기** 페이지에서 **원격 컴퓨터 사용**을 선택 하 고 다음 형식을 사용 하 여 원격 컴퓨터 계정을 입력 합니다. **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="2c2c3-122">참고</span><span class="sxs-lookup"><span data-stu-id="2c2c3-122">Note</span></span>**  
    <span data-ttu-id="2c2c3-123">동일한 컴퓨터에 관리 서버를 배포 하려는 경우 **이 로컬 컴퓨터 사용**을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="2c2c3-124">설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="2c2c3-125">보고 데이터베이스와 보고 서버를 별도의 컴퓨터에 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="2c2c3-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="2c2c3-126">설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="2c2c3-127">App-v 5.0 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="2c2c3-128">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-128">Click **Install**.</span></span>

2.  <span data-ttu-id="2c2c3-129">**시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="2c2c3-130">**Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="2c2c3-131">Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="2c2c3-132">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-132">Click **Next**.</span></span>

4.  <span data-ttu-id="2c2c3-133">**기능 선택** 페이지에서 **보고 서버 데이터베이스** 확인란을 선택 하 여 설치 하려는 구성 요소를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="2c2c3-134">**설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="2c2c3-135">초기 **새 보고 서버 데이터베이스 만들기** 페이지에서 필요에 따라 기본 선택 항목을 적용 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="2c2c3-136">사용자 지정 SQL Server 인스턴스를 사용 하는 경우 **사용자 지정 인스턴스 사용** 을 선택 하 고 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="2c2c3-137">사용자 지정 데이터베이스 이름을 사용 하는 경우 **사용자 지정 구성을** 선택 하 고 데이터베이스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="2c2c3-138">다음 **새 보고 서버 데이터베이스 만들기** 페이지에서 **원격 컴퓨터 사용**을 선택 하 고 다음 형식을 사용 하 여 원격 컴퓨터 계정을 입력 합니다. **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="2c2c3-139">참고</span><span class="sxs-lookup"><span data-stu-id="2c2c3-139">Note</span></span>**  
    <span data-ttu-id="2c2c3-140">같은 컴퓨터에 보고 서버를 배포 하려는 경우 **이 로컬 컴퓨터 사용**을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="2c2c3-141">설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="2c2c3-142">앱-V 5.0 데이터베이스 스크립트를 사용 하 여 관리 및 보고 데이터베이스를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="2c2c3-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="2c2c3-143">설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="2c2c3-144">App-v 5.0 데이터베이스 스크립트의 압축을 풀려면 명령 프롬프트를 열고 설치 파일이 저장 되는 위치를 지정 하 고 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="2c2c3-145">**appv\_server\_setup.exe** **/LAYOUT** **/Layoutdir = "설치 extractionlocation" "** 입니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="2c2c3-146">추출이 완료 된 후 App-v 5.0 데이터베이스 스크립트 및 지침 추가 정보 파일에 액세스 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="2c2c3-147">앱-V 5.0 관리 데이터베이스 스크립트 및 지침 추가 정보는 **설치 extractionlocation**  \\  **데이터베이스 스크립트**  \\  **관리 데이터베이스**폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="2c2c3-148">앱-V 5.0 보고 데이터베이스 스크립트 및 지침 추가 정보는 **설치 extractionlocation**  \\  **데이터베이스 스크립트**  \\  **보고 데이터베이스**폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="2c2c3-149">각 데이터베이스에 대해 스크립트를 공유에 복사 하 고 추가 정보 파일의 지침에 따라 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="2c2c3-150">참고</span><span class="sxs-lookup"><span data-stu-id="2c2c3-150">Note</span></span>**  
    <span data-ttu-id="2c2c3-151">스크립트에 포함 된 필수 Sid를 수정 하는 방법에 대 한 자세한 내용은 [App-v 데이터베이스를 설치 하는 방법 및 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="2c2c3-152">Microsoft SQL Server를 실행 하는 컴퓨터에서 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="2c2c3-153">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="2c2c3-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2c2c3-154">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2c2c3-155">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="2c2c3-155">Got an App-V issue?</span></span>** <span data-ttu-id="2c2c3-156">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2c3-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2c2c3-157">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2c2c3-157">Related topics</span></span>


[<span data-ttu-id="2c2c3-158">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="2c2c3-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









