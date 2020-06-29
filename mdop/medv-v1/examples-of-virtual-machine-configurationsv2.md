---
title: 가상 컴퓨터 구성의 예
description: 가상 컴퓨터 구성의 예
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824588"
---
# <span data-ttu-id="b90a6-103">가상 컴퓨터 구성의 예</span><span class="sxs-lookup"><span data-stu-id="b90a6-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="b90a6-104">다음은 일반적인 가상 컴퓨터 구성의 예입니다. 하나는 영구 MED-V 작업 영역에 있고 하나는 revertible MED-V 작업 영역에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="b90a6-105">**참고**  이러한 예제는 모든 환경에서 사용할 수 있는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="b90a6-106">환경에 따라 구성을 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="b90a6-107">영구 MED-V 작업 영역에서 일반적인 도메인 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b90a6-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="b90a6-108">기본 이미지에 Sysprep를 구성 하 여 고유한 SID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="b90a6-109">자세한 내용은 [med-v에 대 한 가상 PC 이미지 만들기](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b90a6-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="b90a6-110">**Vm 설정** 탭에서 **vm 설치 실행** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="b90a6-111">**VM 컴퓨터 이름 패턴** 섹션에서 컴퓨터 이미지 이름에 대 한 패턴을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="b90a6-112">자세한 내용은 [VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b90a6-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="b90a6-113">**스크립트 편집기**를 클릭 하 고 **VM 설정 스크립트 편집기** 대화 상자에서 다음 작업을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="b90a6-114">컴퓨터 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="b90a6-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="b90a6-115">Windows 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b90a6-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="b90a6-116">연결 확인</span><span class="sxs-lookup"><span data-stu-id="b90a6-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="b90a6-117">도메인 참가</span><span class="sxs-lookup"><span data-stu-id="b90a6-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="b90a6-118">자동 로그온 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b90a6-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="b90a6-119">자세한 내용은 [스크립트 동작을 설정 하는 방법을](how-to-set-up-script-actions.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b90a6-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="b90a6-120">**정책** 메뉴에서 **커밋을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="b90a6-121">Revertible 작업 영역에서 일반적인 설정을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b90a6-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="b90a6-122">**Vm 설정** 탭에서 **컴퓨터 이름 패턴을 기반으로 VM 이름 바꾸기** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="b90a6-123">**VM 컴퓨터 이름 패턴** 섹션에서 컴퓨터 이미지 이름에 대 한 패턴을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="b90a6-124">자세한 내용은 [VM 컴퓨터 이름 패턴 속성을 구성 하는 방법을](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b90a6-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="b90a6-125">**정책** 메뉴에서 **커밋을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90a6-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="b90a6-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b90a6-126">Related topics</span></span>


[<span data-ttu-id="b90a6-127">MED-V 작업 영역에 대한 가상 컴퓨터 설정을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="b90a6-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="b90a6-128">VM 컴퓨터 이름 패턴 속성을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="b90a6-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="b90a6-129">스크립트 동작을 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b90a6-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





