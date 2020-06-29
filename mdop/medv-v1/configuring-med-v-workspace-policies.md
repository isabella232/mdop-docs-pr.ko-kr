---
title: MED-V 작업 영역 정책 구성
description: MED-V 작업 영역 정책 구성
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824858"
---
# <span data-ttu-id="e7a68-103">MED-V 작업 영역 정책 구성</span><span class="sxs-lookup"><span data-stu-id="e7a68-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="e7a68-104">MED-V 작업 영역 정책은 호스트 컴퓨터에서 가상화 된 환경과 응용 프로그램이 수행 하는 방법을 정의 하는 구성 가능한 설정 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="e7a68-105">이 섹션의 항목에서는 MED-V 작업 영역 정책의 구성 가능한 모든 설정과이 설정이 MED-V 작업 영역에 어떤 영향을 미치는지 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="e7a68-106">다음과 같은 MED-V 작업 영역 유형을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="e7a68-107">**Persistent**-영구 med-v 작업 영역에서 사용자가 med-v 작업 영역에 대해 변경한 모든 내용이 med-v 작업 영역에 세션 간에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="e7a68-108">또한 영구 MED-V 작업 영역은 도메인 환경에서 일반적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="e7a68-109">**Revertible**-Revertible med-v 작업 영역에서 각 세션을 완료 하면 (즉 med-v 작업 영역이 중지 되는 경우) med-v 작업 영역은 배포 중에 원래 상태로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="e7a68-110">사용자가 변경한 내용이 나 추가 사항은 세션 간에 MED-V 작업 영역에 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="e7a68-111">도메인 환경에서는 revertible MED-V 작업 영역을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="e7a68-112">정책이 사용자에 게 배포 된 후 MED-V 작업 영역의 유형을 다시 구성 하지 않는 것이 좋지만 MED-V 작업 영역을 배포 하기 전에 만들려는 MED-V 작업 영역의 유형을 결정 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="e7a68-113">**참고**  정책을 구성할 때 채워지지 않은 필수 필드 옆에는 경고 기호가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="e7a68-114">필수 필드를 입력 하지 않은 경우에는 해당 기호도 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="e7a68-115">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="e7a68-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="e7a68-116">MED-V 작업 영역에 일반 설정을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="e7a68-117">MED-V 작업 영역의 일반적인 설정과이를 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="e7a68-118">MED-V 작업 영역에 가상 컴퓨터 설정을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="e7a68-119">MED-V 작업 영역에 대 한 가상 컴퓨터 설정 및 정책을 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="e7a68-120">도메인 사용자 또는 그룹을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="e7a68-121">도메인 사용자 및 그룹을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="e7a68-122">게시된 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="e7a68-123">게시 된 응용 프로그램 및 메뉴 및이를 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="e7a68-124">MED-V 작업 영역에 대한 웹 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="e7a68-125">MED-V 작업 영역에 사용할 수 있는 웹 설정과이를 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="e7a68-126">MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="e7a68-127">MED-V 작업 영역에 대 한 가상 컴퓨터 설정 및 정책을 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="e7a68-128">MED-V 작업 영역에 네트워크 설정을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="e7a68-129">MED-V 작업 영역의 네트워크 설정 및 정책을 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="e7a68-130">MED-V 작업 영역에 성능 설정을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="e7a68-131">MED-V 작업 영역의 성능 설정과이를 정책에 적용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="e7a68-132">정책을 가져오고 내보내는 방법</span><span class="sxs-lookup"><span data-stu-id="e7a68-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="e7a68-133">정책을 가져오고 내보내는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a68-133">Describes how to import and export a policy.</span></span>

 

 





