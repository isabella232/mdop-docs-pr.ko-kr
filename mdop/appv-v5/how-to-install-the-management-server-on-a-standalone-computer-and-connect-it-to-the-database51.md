---
title: 독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법
description: 독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814012"
---
# <span data-ttu-id="ded48-103">독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="ded48-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="ded48-104">독립 실행형 컴퓨터에 관리 서버를 설치 하 고 데이터베이스에 연결 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="ded48-105">독립 실행형 컴퓨터에 관리 서버를 설치 하 고 데이터베이스에 연결 하려면</span><span class="sxs-lookup"><span data-stu-id="ded48-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="ded48-106">설치 하려는 컴퓨터에 App-v 5.1 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-106">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="ded48-107">App-v 5.1 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-107">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="ded48-108">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-108">Click **Install**.</span></span>

2.  <span data-ttu-id="ded48-109">**시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="ded48-110">**Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="ded48-111">Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="ded48-112">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-112">Click **Next**.</span></span>

4.  <span data-ttu-id="ded48-113">**기능 선택** 페이지에서 **관리 서버** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="ded48-114">**설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="ded48-115">**기존 관리 데이터베이스 구성** 페이지에서 **원격 SQL Server 사용**을 선택 하 고 Microsoft SQL sql을 실행 하는 컴퓨터의 컴퓨터 이름 (예: **SqlServerMachine**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="ded48-116">참고</span><span class="sxs-lookup"><span data-stu-id="ded48-116">Note</span></span>**  
    <span data-ttu-id="ded48-117">Microsoft SQL Server가 같은 서버에 배포 된 경우 **로컬 Sql Server 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="ded48-118">**관리 서버 구성 구성** 페이지에서 관리 콘솔에 연결할 AD 그룹 또는 계정 (예: **MyDomain\\MyUser** 또는 **MyDomain\\AdminGroup**)을 관리 하기 위해 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="ded48-119">지정 하는 계정이 나 광고 그룹이 관리 콘솔을 통해 서버를 관리 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="ded48-120">설치 후 관리 콘솔을 사용 하 여 추가 사용자 또는 그룹을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="ded48-121">관리 서비스에 사용할 **웹 사이트 이름을** 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="ded48-122">사용자 지정 이름이 없는 경우 기본값을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="ded48-123">**포트 바인딩에서**사용할 고유 포트 번호 (예: **12345**)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="ded48-124">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-124">Click **Install**.</span></span>

9. <span data-ttu-id="ded48-125">설정이 성공적으로 완료 되었는지 확인 하려면 웹 브라우저를 열고 다음 URL을 입력 http://managementserver:portnumber/Console 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.</span></span> <span data-ttu-id="ded48-126">성공적으로 설치 되 면 오류 메시지 또는 경고가 표시 되지 않고 **관리 콘솔이** 나타날 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-126">If the installation was successful, you should see the **Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="ded48-127">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="ded48-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ded48-128">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ded48-129">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="ded48-129">Got an App-V issue?</span></span>** <span data-ttu-id="ded48-130">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ded48-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ded48-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ded48-131">Related topics</span></span>


[<span data-ttu-id="ded48-132">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="ded48-132">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









