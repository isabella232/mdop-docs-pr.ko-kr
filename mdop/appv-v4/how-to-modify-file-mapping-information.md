---
title: 파일 매핑 정보를 수정하는 방법
description: 파일 매핑 정보를 수정하는 방법
author: dansimp
ms.assetid: d3a9d10a-6cc8-4399-9479-b20f729c4dd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6dbc030367408299e0daaf06f7f97ab5369574db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817023"
---
# <span data-ttu-id="b5fd4-103">파일 매핑 정보를 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="b5fd4-103">How to Modify File-Mapping Information</span></span>


<span data-ttu-id="b5fd4-104">응용 프로그램을 시퀀싱 한 후 저장 하기 전에 가상 파일 시스템을 수동으로 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-104">After you sequence an application but before you save it, you can manually modify the virtual file system.</span></span> <span data-ttu-id="b5fd4-105">가상 파일 시스템에서 파일을 추가, 삭제 또는 편집 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-105">Use the following procedures to add, delete, or edit a file in the virtual file system.</span></span>

**<span data-ttu-id="b5fd4-106">파일 시스템에서 파일을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="b5fd4-106">To add a file in the file system</span></span>**

1.  <span data-ttu-id="b5fd4-107">**가상 파일 시스템** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-107">Click the **Virtual File System** tab.</span></span>

2.  <span data-ttu-id="b5fd4-108">왼쪽 창의 가상 파일 시스템 루트 아래에서 파일을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-108">Right-click a file under the virtual file system root in the left pane.</span></span> <span data-ttu-id="b5fd4-109">메뉴에서 **추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-109">On the menu, select **Add**.</span></span>

3.  <span data-ttu-id="b5fd4-110">**새 가상 파일 시스템 매핑** 대화 상자에서 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-110">Complete the following tasks in the **New Virtual File System Mapping** dialog box:</span></span>

    1.  <span data-ttu-id="b5fd4-111">새 파일 연결을 지정 하려면 새 파일에 대 한 전체 네트워크 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-111">To specify the new file association type the full network path to the new file.</span></span>

    2.  <span data-ttu-id="b5fd4-112">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-112">Click **OK**.</span></span>

4.  <span data-ttu-id="b5fd4-113">로컬 디렉터리를 재정의 하려면 방금 추가한 파일을 마우스 오른쪽 단추로 클릭 하 고 메뉴에서 **로컬 디렉터리 재정의**를 선택 합니다. 로컬 디렉터리와 병합 하려면 **로컬 디렉터리와 병합**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-113">To override the local directory, right-click the file you just added and, on the menu, select **Override Local Directory**; or to merge with the local directory, select **Merge with Local Directory**.</span></span>

5.  <span data-ttu-id="b5fd4-114">**파일** 메뉴에서 **저장** 을 선택 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-114">On the **File** menu, select **Save** to save this change.</span></span>

**<span data-ttu-id="b5fd4-115">파일 시스템에서 파일을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="b5fd4-115">To delete a file in the file system</span></span>**

1.  <span data-ttu-id="b5fd4-116">**가상 파일 시스템** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-116">Click the **Virtual File System** tab.</span></span>

2.  <span data-ttu-id="b5fd4-117">가상 파일 시스템에서 파일을 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-117">Right-click a file in the virtual file system, and select **Delete**.</span></span>

3.  <span data-ttu-id="b5fd4-118">**확인을**클릭 하 여 확인 메시지를 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-118">Accept the confirmation message by clicking **OK**.</span></span>

4.  <span data-ttu-id="b5fd4-119">**파일** 메뉴에서 **저장** 을 선택 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-119">On the **File** menu, select **Save** to save this change.</span></span>

**<span data-ttu-id="b5fd4-120">파일 시스템에서 파일을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="b5fd4-120">To edit a file in the file system</span></span>**

1.  <span data-ttu-id="b5fd4-121">**가상 파일 시스템** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-121">Click the **Virtual File System** tab.</span></span>

2.  <span data-ttu-id="b5fd4-122">가상 파일 시스템에서 파일을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-122">Right-click a file in the virtual file system.</span></span> <span data-ttu-id="b5fd4-123">메뉴에서 **편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-123">On the menu, select **Edit**.</span></span>

3.  <span data-ttu-id="b5fd4-124">**가상 파일 시스템 매핑 편집** 대화 상자에서 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-124">Complete the following tasks in the **Edit Virtual File System Mapping** dialog box:</span></span>

    1.  <span data-ttu-id="b5fd4-125">파일 연결을 편집 하려면 새 파일의 전체 네트워크 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-125">To edit the file association, specify the full network path to the new file.</span></span>

    2.  <span data-ttu-id="b5fd4-126">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-126">Click **OK**.</span></span>

4.  <span data-ttu-id="b5fd4-127">로컬 디렉터리를 재정의 하려면 방금 편집한 파일을 마우스 오른쪽 단추로 클릭 하 고 메뉴에서 **로컬 디렉터리 재정의**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-127">To override the local directory, right-click the file you just edited and, on the menu, select **Override Local Directory**.</span></span>

5.  <span data-ttu-id="b5fd4-128">**파일** 메뉴에서 **저장** 을 선택 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5fd4-128">On the **File** menu, select **Save** to save this change.</span></span>

## <span data-ttu-id="b5fd4-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b5fd4-129">Related topics</span></span>


[<span data-ttu-id="b5fd4-130">가상 파일 시스템 탭 정보</span><span class="sxs-lookup"><span data-stu-id="b5fd4-130">About the Virtual File System Tab</span></span>](about-the-virtual-file-system-tab.md)

[<span data-ttu-id="b5fd4-131">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="b5fd4-131">Sequencer Console</span></span>](sequencer-console.md)

 

 





