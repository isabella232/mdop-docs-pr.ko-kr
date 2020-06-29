---
title: Server Management Console에서 응용 프로그램 그룹을 관리하는 방법
description: Server Management Console에서 응용 프로그램 그룹을 관리하는 방법
author: dansimp
ms.assetid: 46997971-bdc8-4565-aefd-f47e90d6d7a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 59a357d93ea63cc728f59a0633b7a5b9953aad14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817203"
---
# <span data-ttu-id="431fc-103">Server Management Console에서 응용 프로그램 그룹을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-103">How to Manage Application Groups in the Server Management Console</span></span>


<span data-ttu-id="431fc-104">응용 프로그램 가상화 서버 관리 콘솔의 응용 프로그램 그룹에서 하나 이상의 응용 프로그램을 표시 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-104">You can display and manage one or more applications in application groups in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="431fc-105">이는 다음을 수행 하려는 경우 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-105">This can be useful when you want to do the following:</span></span>

-   <span data-ttu-id="431fc-106">여러 응용 프로그램을 관리 하기 쉬운 하위 그룹으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-106">Organize many applications into more manageable subgroups.</span></span>

-   <span data-ttu-id="431fc-107">부서나 기타 회사 디비전에 해당 하는 응용 프로그램 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-107">Create groups of applications specific to a department or other company division.</span></span>

-   <span data-ttu-id="431fc-108">재무 소프트웨어와 같은 유사한 유형의 응용 프로그램을 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-108">Group similar types of applications, such as financial software.</span></span>

-   <span data-ttu-id="431fc-109">그룹을 기준으로 액세스 권한 또는 라이선스 관리를 간소화 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-109">Simplify access permissions or license management by group.</span></span>

-   <span data-ttu-id="431fc-110">그룹 내에서 동시에 응용 프로그램 및 응용 프로그램 그룹의 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-110">Change the properties of applications and application groups within a group simultaneously.</span></span>

<span data-ttu-id="431fc-111">그룹을 만들고, 콘솔의 **응용 프로그램** 트리에 원하는 위치에 배치 하 고, 그룹으로 응용 프로그램을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-111">You can create a group, place it where you would like in the console's **Applications** tree, and import applications to the group.</span></span> <span data-ttu-id="431fc-112">그런 다음 그룹의 속성을 구성 하 고 관리 하 여 모든 응용 프로그램에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-112">Then you can configure and manage the group's properties to affect all of its applications.</span></span> <span data-ttu-id="431fc-113">그룹 간에 응용 프로그램을 이동할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-113">You can also move applications among groups.</span></span>

<span data-ttu-id="431fc-114">**참고**  응용 프로그램을 그룹으로 이동 해도 서버의 파일 시스템에 있는 파일 (SFT, OSD 또는 SPRJ)의 위치에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-114">**Note** Moving applications into groups does not affect the locations of their files (SFT, OSD, or SPRJ) on the server's file system.</span></span>

 

## <span data-ttu-id="431fc-115">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="431fc-115">In This Section</span></span>


<a href="" id="how-to-create-an-application-group"></a>[<span data-ttu-id="431fc-116">응용 프로그램 그룹을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-116">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)  
<span data-ttu-id="431fc-117">응용 프로그램 그룹을 만들기 위한 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-117">Provides step-by-step instructions for creating an application group.</span></span>

<a href="" id="how-to-move-an-application-group"></a>[<span data-ttu-id="431fc-118">응용 프로그램 그룹을 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-118">How to Move an Application Group</span></span>](how-to-move-an-application-group.md)  
<span data-ttu-id="431fc-119">응용 프로그램 그룹을 이동 하는 방법에 대 한 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-119">Provides step-by-step instructions for moving an application group.</span></span>

<a href="" id="how-to-rename-an-application-group"></a>[<span data-ttu-id="431fc-120">응용 프로그램 그룹 이름을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-120">How to Rename an Application Group</span></span>](how-to-rename-an-application-group.md)  
<span data-ttu-id="431fc-121">응용 프로그램 그룹의 이름을 바꾸는 방법에 대 한 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-121">Provides step-by-step instructions for renaming an application group.</span></span>

<a href="" id="how-to-remove-an-application-group"></a>[<span data-ttu-id="431fc-122">응용 프로그램 그룹을 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-122">How to Remove an Application Group</span></span>](how-to-remove-an-application-group.md)  
<span data-ttu-id="431fc-123">응용 프로그램 그룹을 제거 하거나 삭제 하는 방법에 대 한 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="431fc-123">Provides step-by-step instructions for removing or deleting an application group.</span></span>

## <span data-ttu-id="431fc-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="431fc-124">Related topics</span></span>


[<span data-ttu-id="431fc-125">Server Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="431fc-126">Application Virtualization Server Management Console에서 관리 작업을 수행하는 방법</span><span class="sxs-lookup"><span data-stu-id="431fc-126">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





