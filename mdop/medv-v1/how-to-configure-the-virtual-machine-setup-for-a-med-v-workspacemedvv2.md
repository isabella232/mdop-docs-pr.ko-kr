---
title: MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법
description: MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827073"
---
# <span data-ttu-id="cd4f7-103">MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="cd4f7-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="cd4f7-104">모든 가상 컴퓨터 설정 구성 설정은 **정책** 모듈의 **VM 설정** 탭에서 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="cd4f7-105">영구 MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cd4f7-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="cd4f7-106">영구 MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="cd4f7-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="cd4f7-107">구성할 영구 MED-V 작업 영역을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="cd4f7-108">**영구 VM 설정** 섹션에서 다음 표에 설명 된 대로 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="cd4f7-109">참고</span><span class="sxs-lookup"><span data-stu-id="cd4f7-109">Note</span></span>**  
    <span data-ttu-id="cd4f7-110">영구 VM 설정 속성은 영구 MED-V 작업 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="cd4f7-111">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="cd4f7-112">영구 VM 설치 속성</span><span class="sxs-lookup"><span data-stu-id="cd4f7-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd4f7-113">속성</span><span class="sxs-lookup"><span data-stu-id="cd4f7-113">Property</span></span></th>
<th align="left"><span data-ttu-id="cd4f7-114">설명</span><span class="sxs-lookup"><span data-stu-id="cd4f7-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd4f7-115">VM 설치 프로그램 실행</span><span class="sxs-lookup"><span data-stu-id="cd4f7-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd4f7-116">MED-V 작업 영역을 처음 실행할 때 설정 스크립트를 실행 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd4f7-117">스크립트 편집기</span><span class="sxs-lookup"><span data-stu-id="cd4f7-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd4f7-118">설치 스크립트를 구성 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-118">Click to configure the setup script.</span></span> <span data-ttu-id="cd4f7-119">자세한 내용은 <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> 스크립트 동작을 설정 하는 방법을 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cd4f7-120">참고</span><span class="sxs-lookup"><span data-stu-id="cd4f7-120">Note</span></span></strong><br/><p><span data-ttu-id="cd4f7-121">이 단추는 <strong> VM 설치 스크립트 실행이 선택 된 경우에만 사용할 수 </strong> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd4f7-122">스크립트가 실행 중일 때 표시 되는 메시지</span><span class="sxs-lookup"><span data-stu-id="cd4f7-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd4f7-123">스크립트를 실행 하는 동안 표시할 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="cd4f7-124">공백으로 두면 기본 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cd4f7-125">참고</span><span class="sxs-lookup"><span data-stu-id="cd4f7-125">Note</span></span></strong><br/><p><span data-ttu-id="cd4f7-126">이 필드는 <strong> VM 설치 스크립트 실행이 선택 되어 있는 경우에만 사용할 수 </strong> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cd4f7-127">Revertible MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="cd4f7-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="cd4f7-128">Revertible MED-V 작업 영역에 대 한 가상 컴퓨터 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="cd4f7-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="cd4f7-129">Revertible MED-V 작업 영역을 클릭 하 여 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="cd4f7-130">**REVERTIBLE VM 설정** 섹션에서 다음 표에 설명 된 대로 속성을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="cd4f7-131">참고</span><span class="sxs-lookup"><span data-stu-id="cd4f7-131">Note</span></span>**  
    <span data-ttu-id="cd4f7-132">Revertible VM 설치 속성은 revertible MED-V 작업 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="cd4f7-133">**정책** 메뉴에서 **커밋을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="cd4f7-134">Revertible VM 설치 속성</span><span class="sxs-lookup"><span data-stu-id="cd4f7-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd4f7-135">속성</span><span class="sxs-lookup"><span data-stu-id="cd4f7-135">Property</span></span></th>
<th align="left"><span data-ttu-id="cd4f7-136">설명</span><span class="sxs-lookup"><span data-stu-id="cd4f7-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd4f7-137">컴퓨터 이름 패턴에 따라 VM 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="cd4f7-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd4f7-138">동일한 MED-V 작업 영역을 사용 하 여 여러 컴퓨터를 구분할 수 있도록 MED-V 작업 영역을 사용 하 여 각 컴퓨터에 고유한 이름을 할당 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd4f7-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="cd4f7-139">컴퓨터 이미지 이름을 구성 하는 방법에 대 한 자세한 내용은 <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="cd4f7-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cd4f7-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cd4f7-140">Related topics</span></span>


[<span data-ttu-id="cd4f7-141">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="cd4f7-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="cd4f7-142">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="cd4f7-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="cd4f7-143">가상 컴퓨터 구성의 예</span><span class="sxs-lookup"><span data-stu-id="cd4f7-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









