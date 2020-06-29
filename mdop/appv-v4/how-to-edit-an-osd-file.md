---
title: OSD 파일을 편집하는 방법
description: OSD 파일을 편집하는 방법
author: dansimp
ms.assetid: 0d126ba7-72fb-42ce-982e-90ed01a852c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a0ff4a8efe1fa177f6847c344add94bca3648cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817438"
---
# <span data-ttu-id="0b478-103">OSD 파일을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b478-103">How to Edit an OSD File</span></span>


<span data-ttu-id="0b478-104">다음 절차를 사용 하 여 요소 또는 특성을 추가 하거나 삭제 하 여 시퀀싱 된 응용 프로그램 패키지의 OSD (Open Software Descriptor) 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-104">Use the following procedures to modify a sequenced application package's Open Software Descriptor (OSD) file by adding or deleting an element or an attribute.</span></span>

<span data-ttu-id="0b478-105">**참고**  일부 요소에는 특성이 없으므로 모든 요소에 특성을 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-105">**Note** Some elements do not have an attribute, so it is not possible to add an attribute to every element.</span></span>

 

<span data-ttu-id="0b478-106">**중요**  Osd 편집기를 사용 하 여 OSD 파일의 CODEBASE 요소에 대 한 HREF 특성을 변경 하려면 다른 이름 **으로 저장** 명령을 사용 하 여 변경 내용을 프로젝트 파일에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-106">**Important** If you use the OSD editor to change the .sft file name, the HREF attribute of the CODEBASE element in the OSD file, you must use the **Save As** command to save the change to the project files.</span></span>

 

**<span data-ttu-id="0b478-107">요소를 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="0b478-107">To add an element</span></span>**

1.  <span data-ttu-id="0b478-108">**OSD 파일** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-108">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="0b478-109">탐색 창에서 수정 하려는 시퀀싱 된 응용 프로그램 패키지의 OSD 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-109">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="0b478-110">탐색 창에서 수정 하려는 요소를 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-110">In the navigation pane, right-click the element that you want to modify.</span></span> <span data-ttu-id="0b478-111">메뉴에서 **요소** 를 선택 하 고 **추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-111">On the menu, select **Element** and select **Add**.</span></span>

4.  <span data-ttu-id="0b478-112">메뉴에서 추가 하려는 요소 (예: **Codebase**)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-112">From the menu, select the element you want to add—for example, **Codebase**.</span></span>

5.  <span data-ttu-id="0b478-113">**파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-113">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="0b478-114">요소를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="0b478-114">To delete an element</span></span>**

1.  <span data-ttu-id="0b478-115">**OSD 파일** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-115">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="0b478-116">탐색 창에서 수정 하려는 시퀀싱 된 응용 프로그램 패키지의 OSD 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-116">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="0b478-117">탐색 창에서 삭제 하려는 요소를 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-117">In the navigation pane, right-click the element that you want to delete.</span></span> <span data-ttu-id="0b478-118">메뉴에서 **요소** 를 선택 하 고 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-118">On the menu, select **Element** and select **Delete**.</span></span>

4.  <span data-ttu-id="0b478-119">**파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-119">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="0b478-120">특성을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="0b478-120">To add an attribute</span></span>**

1.  <span data-ttu-id="0b478-121">**OSD 파일** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-121">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="0b478-122">탐색 창에서 수정 하려는 시퀀싱 된 응용 프로그램 패키지의 OSD 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-122">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="0b478-123">왼쪽 창에서 특성을 추가 하려는 요소를 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-123">In the left pane, right-click the element to which you want to add an attribute.</span></span> <span data-ttu-id="0b478-124">메뉴에서 **특성** 을 선택 하 고 **추가**를 선택 하 여 사용 가능한 특성 목록에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-124">On the menu, select **Attribute** and select **Add**, choosing from the listed available attributes.</span></span>

4.  <span data-ttu-id="0b478-125">**파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-125">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="0b478-126">특성을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="0b478-126">To delete an attribute</span></span>**

1.  <span data-ttu-id="0b478-127">**OSD 파일** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-127">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="0b478-128">탐색 창에서 수정 하려는 시퀀싱 된 응용 프로그램 패키지의 OSD 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-128">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="0b478-129">탐색 창에서 특성을 삭제 하려는 요소를 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-129">In the navigation pane, right-click the element from which you want to delete an attribute.</span></span> <span data-ttu-id="0b478-130">메뉴에서 **특성** 을 선택한 다음 **삭제**를 선택 하 여 삭제할 특성을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-130">On the menu, select **Attribute** and then select **Delete**, choosing the attribute you wish to delete.</span></span>

4.  <span data-ttu-id="0b478-131">**파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b478-131">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="0b478-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0b478-132">Related topics</span></span>


[<span data-ttu-id="0b478-133">OSD 탭 정보</span><span class="sxs-lookup"><span data-stu-id="0b478-133">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="0b478-134">텍스트 편집기를 사용하여 OSD 파일을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b478-134">How to Edit an OSD File Using a Text Editor</span></span>](how-to-edit-an-osd-file-using-a-text-editor.md)

[<span data-ttu-id="0b478-135">OSD 파일 요소</span><span class="sxs-lookup"><span data-stu-id="0b478-135">OSD File Elements</span></span>](osd-file-elements.md)

[<span data-ttu-id="0b478-136">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="0b478-136">Sequencer Console</span></span>](sequencer-console.md)

 

 





