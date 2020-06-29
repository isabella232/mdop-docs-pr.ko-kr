---
title: 관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법
description: 관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법
author: dansimp
ms.assetid: 4fd39bc2-d814-46de-a108-1c21fa404e8a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c6c8f930fb1fbd82432f6d43dae8b9bed7a563c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814417"
---
# <span data-ttu-id="12635-103">관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="12635-103">How to Configure Access to Packages by Using the Management Console</span></span>


<span data-ttu-id="12635-104">App-v 5.1 가상화 된 패키지를 배포 하기 전에 응용 프로그램에 액세스 하 고 실행 하도록 허용 되는 AD DS (Active Directory 도메인 서비스) 보안 그룹을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-104">Before you deploy an App-V 5.1 virtualized package, you must configure the Active Directory Domain Services (AD DS) security groups that will be allowed to access and run the applications.</span></span> <span data-ttu-id="12635-105">보안 그룹에는 컴퓨터 또는 사용자가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12635-105">The security groups may contain computers or users.</span></span> <span data-ttu-id="12635-106">패키지를 컴퓨터 그룹에 Entitling 그룹의 모든 컴퓨터에 패키지를 전역적으로 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-106">Entitling a package to a computer group publishes the package globally to all computers in the group.</span></span>

<span data-ttu-id="12635-107">가상화 된 패키지에 대 한 액세스를 구성 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-107">Use the following procedure to configure access to virtualized packages.</span></span>

**<span data-ttu-id="12635-108">앱-V 5.1 패키지에 대 한 액세스 권한을 부여 하려면</span><span class="sxs-lookup"><span data-stu-id="12635-108">To grant access to an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="12635-109">구성 하려는 패키지를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="12635-109">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="12635-110">App-v 5.1 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="12635-110">Open the App-V 5.1 Management console.</span></span>

    2.  <span data-ttu-id="12635-111">**광고 액세스** 페이지를 표시 하려면 구성할 패키지를 마우스 오른쪽 단추로 클릭 하 고 **Active directory ACCESS 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-111">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="12635-112">또는 패키지를 선택 하 고 **광고 액세스** 창에서 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-112">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="12635-113">패키지에 대 한 보안 그룹을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-113">Provision a security group for the package:</span></span>

    1.  <span data-ttu-id="12635-114">**유효한 ACTIVE DIRECTORY 이름 찾기 및 액세스 권한 부여** 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-114">Go to the **FIND VALID ACTIVE DIRECTORY NAMES AND GRANT ACCESS** page.</span></span>

    2.  <span data-ttu-id="12635-115">**Mydomain**형식 그룹을 사용 하 여  \\  **groupname**Active Directory group 개체 이름의 이름 또는 일부를 입력 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-115">Using the format **mydomain** \\ **groupname**, type the name or part of the name of an Active Directory group object, and click **Check**.</span></span>

        <span data-ttu-id="12635-116">**참고**  검색할 그룹에 대 한 연결 된 도메인 이름을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-116">**Note** Ensure that you provide an associated domain name for the group that you are searching for.</span></span>

         

3.  <span data-ttu-id="12635-117">패키지에 대 한 액세스 권한을 부여 하려면 원하는 그룹을 선택 하 고 **액세스 허용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-117">To grant access to the package, select the desired group and click **Grant Access**.</span></span> <span data-ttu-id="12635-118">새로 추가 된 그룹이 **광고 엔터티에서 ACCESS** 창에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12635-118">The newly added group is displayed in the **AD ENTITIES WITH ACCESS** pane.</span></span>

4.  

    <span data-ttu-id="12635-119">기본 구성 설정을 적용 하 고 **광고 액세스** 페이지를 닫으려면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-119">To accept the default configuration settings and close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="12635-120">특정 그룹에 대 한 구성을 사용자 지정 하려면 **할당 된 구성** 드롭다운을 클릭 하 고 **사용자 지정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-120">To customize configurations for a specific group, click the **ASSIGNED CONFIGURATIONS** drop-down and select **Custom**.</span></span> <span data-ttu-id="12635-121">사용자 지정 구성을 구성 하려면 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-121">To configure the custom configurations, click **EDIT**.</span></span> <span data-ttu-id="12635-122">액세스 권한을 부여한 후 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-122">After you grant access, click **Close**.</span></span>

**<span data-ttu-id="12635-123">App-v 5.1 패키지에 대 한 액세스 권한을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="12635-123">To remove access to an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="12635-124">구성 하려는 패키지를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="12635-124">Find the package you want to configure:</span></span>

    1.  <span data-ttu-id="12635-125">App-v 5.1 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="12635-125">Open the App-V 5.1 Management console.</span></span>

    2.  <span data-ttu-id="12635-126">**광고 액세스** 페이지를 표시 하려면 구성할 패키지를 마우스 오른쪽 단추로 클릭 하 고 **Active directory ACCESS 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-126">To display the **AD ACCESS** page, right-click the package to be configured, and select **Edit active directory access**.</span></span> <span data-ttu-id="12635-127">또는 패키지를 선택 하 고 **광고 액세스** 창에서 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-127">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="12635-128">제거 하려는 그룹을 선택 하 고 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-128">Select the group you want to remove, and click **DELETE**.</span></span>

3.  <span data-ttu-id="12635-129">**광고 액세스** 페이지를 닫으려면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-129">To close the **AD ACCESS** page, click **Close**.</span></span>

    <span data-ttu-id="12635-130">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="12635-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="12635-131">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="12635-132">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="12635-132">Got an App-V issue?</span></span>** <span data-ttu-id="12635-133">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="12635-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="12635-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="12635-134">Related topics</span></span>


[<span data-ttu-id="12635-135">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="12635-135">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





