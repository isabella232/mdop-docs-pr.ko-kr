---
title: 클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법
description: 클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814388"
---
# <span data-ttu-id="d74a2-103">클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d74a2-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="d74a2-104">App-v 5.0 게시 서버를 사용 하 여 패키지 및 연결 그룹을 배포 하면 단일 위치 관리와 높은 확장성을 제공 하기 때문에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="d74a2-105">게시 서버에서 업데이트를 받도록 App-v 5.0 클라이언트를 구성 하려면 다음 단계를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="d74a2-106">**참고**  다음 절차에서는 관리 서버가 **MyMgmtSrv**이라는 컴퓨터에 설치 되었고 게시 서버는 **MyPubSrv**라는 컴퓨터에 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="d74a2-107">게시 서버에서 업데이트를 받도록 App-v 5.0 클라이언트를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="d74a2-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="d74a2-108">앱-V 5.0 관리 및 게시 서버를 배포 하 고 필요한 패키지 및 연결 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="d74a2-109">패키지 및 연결 그룹을 추가 하는 방법에 대 한 자세한 내용은 [관리 콘솔을 사용 하 여 패키지를 추가 하거나 업그레이드 하는 방법과](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) [연결 그룹을 만드는](how-to-create-a-connection-group.md)방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d74a2-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="d74a2-110">관리 콘솔을 열려면 다음 링크를 클릭 하 고 브라우저를 열고 다음을 입력 합니다. http://MyMgmtSrv/AppvManagement/Console.html 웹 브라우저에서 특정 사용자 집합에 필요한 모든 패키지 및 연결 그룹을 가져오고, 게시 하 고, entitle.</span><span class="sxs-lookup"><span data-stu-id="d74a2-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="d74a2-111">App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 관리자 권한 PowerShell 명령 프롬프트를 열고 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="d74a2-112">추가-AppvPublishingServer-이름 ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="d74a2-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="d74a2-113">이 명령은 지정 된 게시 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="d74a2-114">다음과 유사한 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="d74a2-115">Id: 1</span><span class="sxs-lookup"><span data-stu-id="d74a2-115">Id : 1</span></span>

    <span data-ttu-id="d74a2-116">SetByGroupPolicy: False</span><span class="sxs-lookup"><span data-stu-id="d74a2-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="d74a2-117">이름: ABC</span><span class="sxs-lookup"><span data-stu-id="d74a2-117">Name : ABC</span></span>

    <span data-ttu-id="d74a2-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="d74a2-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="d74a2-119">GlobalRefreshEnabled: False</span><span class="sxs-lookup"><span data-stu-id="d74a2-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="d74a2-120">GlobalRefreshOnLogon: False</span><span class="sxs-lookup"><span data-stu-id="d74a2-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="d74a2-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="d74a2-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="d74a2-122">GlobalRefreshIntervalUnit: 일</span><span class="sxs-lookup"><span data-stu-id="d74a2-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="d74a2-123">UserRefreshEnabled: True</span><span class="sxs-lookup"><span data-stu-id="d74a2-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="d74a2-124">UserRefreshOnLogon: True</span><span class="sxs-lookup"><span data-stu-id="d74a2-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="d74a2-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="d74a2-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="d74a2-126">UserRefreshIntervalUnit: 일</span><span class="sxs-lookup"><span data-stu-id="d74a2-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="d74a2-127">반환 되는 Id-이 경우 1</span><span class="sxs-lookup"><span data-stu-id="d74a2-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="d74a2-128">App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 PowerShell 명령 프롬프트를 열고 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="d74a2-129">Sync-AppvPublishingServer-ServerId 1</span><span class="sxs-lookup"><span data-stu-id="d74a2-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="d74a2-130">이 명령은 관리 서버에 구성 된 패키지 및 연결 그룹에 대 한 권리를 기반으로 해당 클라이언트에 대해 추가 또는 제거 해야 하는 패키지 및 연결 그룹에 대 한 게시 서버를 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="d74a2-131">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="d74a2-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="d74a2-132">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="d74a2-133">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="d74a2-133">Got an App-V issue?</span></span>** <span data-ttu-id="d74a2-134">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d74a2-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="d74a2-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d74a2-135">Related topics</span></span>


[<span data-ttu-id="d74a2-136">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="d74a2-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





