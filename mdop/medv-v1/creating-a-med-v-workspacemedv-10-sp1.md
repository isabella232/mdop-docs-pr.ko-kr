---
title: MED-V 작업 영역 만들기
description: MED-V 작업 영역 만들기
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824863"
---
# <span data-ttu-id="08543-103">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="08543-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="08543-104">MED-V 작업 영역은 MED-V에서 제공 하는 가상 컴퓨터와 최종 사용자가 상호 작용 하는 데스크톱 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="08543-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="08543-105">MED-V 작업 영역이 만들어지고 관리자가 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="08543-106">이는 MED-V 작업 영역의 규칙과 기능을 정의 하는 이미지와 정책으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08543-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="08543-107">여러 MED-V 작업 영역을 만들 수 있으며, 각각 고유한 구성, 설정 및 규칙을 사용 하 여 사용자 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08543-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="08543-108">사용자, 그룹 또는 여러 사용자 또는 그룹을 각 MED-V 작업 영역에 연결 하 여 연결 된 사용자 또는 그룹의 컴퓨터에 대해서만 MED-V 작업 영역을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08543-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="08543-109">MED-V 작업 영역을 추가 하는 방법</span><span class="sxs-lookup"><span data-stu-id="08543-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="08543-110">MED-V 작업 영역을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="08543-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="08543-111">**정책 관리 단추** 를 클릭 하 여 **정책** 모듈을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="08543-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="08543-112">**정책** 모듈은 왼쪽에 있는 **작업 영역** 메뉴와 **일반**, **가상 컴퓨터**, **배포**, **응용 프로그램**, **웹**, **VM 설치**, **네트워크**및 **성능** 탭으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08543-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="08543-113">**정책** 메뉴에서 **새 작업 영역**을 선택 하거나 **추가** 를 클릭 하 여 새 med-v 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08543-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="08543-114">**일반** 탭의 **이름** 필드에 med-v 작업 영역의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="08543-115">**설명** 필드에 med-v 작업 영역에 대 한 설명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="08543-116">**지원 연락처 정보** 필드에 기술 지원에 대 한 연락처 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="08543-117">MED-V 작업 영역을 구성 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 정책 구성을](configuring-med-v-workspace-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08543-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="08543-118">MED-V 작업 영역을 복제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="08543-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="08543-119">Med-v 작업 영역을 복제 하 여 기존 MED-V 작업 영역과 동일 하 게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08543-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="08543-120">MED-V 작업 영역을 복제 하려면</span><span class="sxs-lookup"><span data-stu-id="08543-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="08543-121">복제 하려는 MED-V 작업 영역을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="08543-122">**정책** 메뉴에서 **작업 영역 복제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="08543-123">이름이 &lt; 원본 med-v 작업 영역 이름-2 인 새 med-v 작업 영역이 만들어집니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="08543-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="08543-124">MED-V 작업 영역을 삭제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="08543-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="08543-125">MED-V 작업 영역을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="08543-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="08543-126">**정책** 모듈에서 작업 영역 창이 포커스를 둔 상태에서 **제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="08543-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="08543-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="08543-127">Related topics</span></span>


[<span data-ttu-id="08543-128">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="08543-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





