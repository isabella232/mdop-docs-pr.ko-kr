---
title: 원격 컴퓨터에 게시 서버를 설치하는 방법
description: 원격 컴퓨터에 게시 서버를 설치하는 방법
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813996"
---
# <span data-ttu-id="81d07-103">원격 컴퓨터에 게시 서버를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="81d07-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="81d07-104">다음 절차를 사용 하 여 별도의 컴퓨터에 게시 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="81d07-105">다음 절차를 수행 하기 전에 데이터베이스 및 관리 서버를 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="81d07-106">게시 서버를 별도의 컴퓨터에 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="81d07-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="81d07-107">설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-107">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="81d07-108">App-v 5.0 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-108">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="81d07-109">**설치**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-109">Click **Install**.</span></span>

2. <span data-ttu-id="81d07-110">**시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="81d07-111">**Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="81d07-112">Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="81d07-113">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-113">Click **Next**.</span></span>

4. <span data-ttu-id="81d07-114">**기능 선택** 페이지에서 **게시 서버** 확인란을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="81d07-115">**설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="81d07-116">**게시 서버 구성 구성** 페이지에서 다음 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="81d07-117">게시 서버가 연결 하는 관리 서비스의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="81d07-118">예를 들어 **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="81d07-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="81d07-119">게시 서비스에 사용할 웹 사이트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="81d07-120">사용자 지정 이름이 없는 경우 기본값을 그대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="81d07-121">**포트 바인딩에**대해 app-v 5.0 (예: **54321**)에서 사용 되는 고유 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.0, for example **54321**.</span></span>

7. <span data-ttu-id="81d07-122">**설치 준비** 페이지에서 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="81d07-123">설치가 완료 되 면 게시 서버를 관리 서버에 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="81d07-124">App-v 5.0 관리 콘솔에서 다음 단계를 사용 하 여 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-124">In the App-V 5.0 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="81d07-125">App-v 5.0 관리 서버 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-125">Open the App-V 5.0 management server console.</span></span>

   2.  <span data-ttu-id="81d07-126">왼쪽 창에서 **서버**를 선택한 다음 **새 서버 등록**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="81d07-127">이 서버의 이름과 설명 (필요한 경우)을 입력 하 고 **추가**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="81d07-128">게시 서버가 올바르게 실행 되 고 있는지 확인 하려면 패키지를 관리 서버로 가져오고 패키지를 광고 그룹으로 entitle 패키지를 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="81d07-129">인터넷 브라우저를 사용 하 여 다음 URL을 엽니다 <strong> . http://publishingserver:pubport </strong></span><span class="sxs-lookup"><span data-stu-id="81d07-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="81d07-130">서버가 올바르게 실행 되는 경우 다음과 유사한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="81d07-131">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="81d07-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="81d07-132">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="81d07-133">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="81d07-133">Got an App-V issue?</span></span>** <span data-ttu-id="81d07-134">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d07-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="81d07-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="81d07-135">Related topics</span></span>


[<span data-ttu-id="81d07-136">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="81d07-136">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

 

 





