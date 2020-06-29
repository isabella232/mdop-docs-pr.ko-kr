---
title: MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법
description: MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법
author: dansimp
ms.assetid: a4659b4d-18b2-45b1-9605-8b5adc438f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dafcc1dbb88b65bb301ba4d0f1d89bb587470a76
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824178"
---
# <span data-ttu-id="3aa60-103">MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3aa60-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="3aa60-104">이 섹션의 절차에서는 최초 설치를 위해 가상 컴퓨터를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aa60-104">The procedures in this section describe how to configure the virtual machine for first-time setup.</span></span>

<span data-ttu-id="3aa60-105">가상 컴퓨터 설정에서는 가상 컴퓨터가 처음으로 클라이언트에서 실행 될 때 수행 되는 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aa60-105">The virtual machine setup configures the setup performed when the virtual machine is run on the client for the first time.</span></span> <span data-ttu-id="3aa60-106">가상 머신 설정은 영구 및 revertible MED-V 작업 영역에 대해 다르게 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3aa60-106">The virtual machine setup is configured differently for persistent and revertible MED-V workspaces.</span></span> <span data-ttu-id="3aa60-107">영구 및 revertible MED-V 작업 영역에 대 한 자세한 내용은 [Med-v 작업 영역 정책 구성을](configuring-med-v-workspace-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3aa60-107">For more information about persistent and revertible MED-V workspaces, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="3aa60-108">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="3aa60-108">In This Section</span></span>


<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="3aa60-109">MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3aa60-109">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)  
<span data-ttu-id="3aa60-110">영구 및 revertible MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aa60-110">Describes how to configure the virtual machine setup for persistent and revertible MED-V workspaces.</span></span>

<a href="" id="how-to-configure-vm-computer-name-pattern-properties"></a>[<span data-ttu-id="3aa60-111">VM 컴퓨터 이름 패턴 속성을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="3aa60-111">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)  
<span data-ttu-id="3aa60-112">영구 및 revertible MED-V 작업 영역에 대 한 가상 컴퓨터 컴퓨터 이름 패턴 속성을 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aa60-112">Describes how to configure virtual machine computer name pattern properties for persistent and revertible MED-V workspaces.</span></span>

<a href="" id="examples-of-virtual-machine-configurations"></a>[<span data-ttu-id="3aa60-113">가상 컴퓨터 구성의 예</span><span class="sxs-lookup"><span data-stu-id="3aa60-113">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)  
<span data-ttu-id="3aa60-114">영구 및 revertible MED-V 작업 영역에서 가상 컴퓨터 구성의 예를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aa60-114">Provides examples of virtual machine configurations in both persistent and revertible MED-V workspaces.</span></span>

## <span data-ttu-id="3aa60-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3aa60-115">Related topics</span></span>


[<span data-ttu-id="3aa60-116">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="3aa60-116">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="3aa60-117">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="3aa60-117">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="3aa60-118">스크립트 동작을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="3aa60-118">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





