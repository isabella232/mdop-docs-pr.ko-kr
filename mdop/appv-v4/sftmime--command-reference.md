---
title: SFTMIME 명령 참조
description: SFTMIME 명령 참조
author: dansimp
ms.assetid: a4a69228-9dd3-4623-b773-899d03c0cf10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47aac9110febaf3f349461d74fef840326b1c6e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815348"
---
# <span data-ttu-id="4715c-103">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="4715c-103">SFTMIME Command Reference</span></span>


<span data-ttu-id="4715c-104">SFTMIME는 다양 한 클라이언트 구성 세부 정보를 관리할 수 있는 Application Virtualization (App-v)에서 사용 되는 명령줄 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-104">SFTMIME is a command-line interface used by Application Virtualization (App-V) that enables you to manage many client configuration details.</span></span> <span data-ttu-id="4715c-105">이 섹션에는 모든 명령과 해당 매개 변수가 포함 되어 있으며, 각 명령에 대 한 간략 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-105">This section contains all the commands and their parameters, with a brief description of each.</span></span>

**<span data-ttu-id="4715c-106">중요</span><span class="sxs-lookup"><span data-stu-id="4715c-106">Important</span></span>**  
-   <span data-ttu-id="4715c-107">모든 백슬래시 문자는 앞의 백슬래시를 사용 하 여 이스케이프 되어야 하며, 그렇지 않으면 경로가 올바르게 구문 분석 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-107">All backslash characters must be escaped using a preceding backslash, or the path will not be parsed correctly.</span></span>

-   <span data-ttu-id="4715c-108">호출 프로그램을 사용 하 여 **CreateProcess**로 SFTMIME를 호출 하는 경우 첫 번째 매개 변수가 sftmime.exe에 대 한 경로 인지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-108">If you are using a calling program to invoke SFTMIME with **CreateProcess**, you must ensure that the first parameter is the path to sftmime.exe.</span></span>

-   <span data-ttu-id="4715c-109">SFTMIME **쿼리 OBJ** 명령의 출력을 **findstr** 명령으로 파이프 하 여 문자열을 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-109">The output of the SFTMIME **QUERY OBJ** command cannot be piped to the **findstr** command to search for a string.</span></span>

-   <span data-ttu-id="4715c-110">**전역** 스위치를 사용 하려면 로컬 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-110">Use of the **GLOBAL** switch requires local administrator rights.</span></span>

-   <span data-ttu-id="4715c-111">짧은 경로와 상대 경로를 사용 하면 예기치 않은 결과가 발생할 수 있으므로 피해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-111">Use of short paths and relative paths can lead to unexpected results and should be avoided.</span></span> <span data-ttu-id="4715c-112">항상 전체 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4715c-112">Always use full paths.</span></span>

 

## <span data-ttu-id="4715c-113">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="4715c-113">In This Section</span></span>


[<span data-ttu-id="4715c-114">ADD APP</span><span class="sxs-lookup"><span data-stu-id="4715c-114">ADD APP</span></span>](add-app.md)

[<span data-ttu-id="4715c-115">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-115">ADD PACKAGE</span></span>](add-package.md)

[<span data-ttu-id="4715c-116">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="4715c-116">ADD SERVER</span></span>](add-server.md)

[<span data-ttu-id="4715c-117">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="4715c-117">ADD TYPE</span></span>](add-type.md)

[<span data-ttu-id="4715c-118">CLEAR APP</span><span class="sxs-lookup"><span data-stu-id="4715c-118">CLEAR APP</span></span>](clear-app.md)

[<span data-ttu-id="4715c-119">CLEAR OBJ</span><span class="sxs-lookup"><span data-stu-id="4715c-119">CLEAR OBJ</span></span>](clear-obj.md)

[<span data-ttu-id="4715c-120">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="4715c-120">CONFIGURE APP</span></span>](configure-app.md)

[<span data-ttu-id="4715c-121">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-121">CONFIGURE PACKAGE</span></span>](configure-package.md)

[<span data-ttu-id="4715c-122">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="4715c-122">CONFIGURE SERVER</span></span>](configure-server.md)

[<span data-ttu-id="4715c-123">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="4715c-123">CONFIGURE TYPE</span></span>](configure-type.md)

[<span data-ttu-id="4715c-124">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="4715c-124">DELETE APP</span></span>](delete-app.md)

[<span data-ttu-id="4715c-125">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="4715c-125">DELETE OBJ</span></span>](delete-obj.md)

[<span data-ttu-id="4715c-126">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-126">DELETE PACKAGE</span></span>](delete-package.md)

[<span data-ttu-id="4715c-127">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="4715c-127">DELETE SERVER</span></span>](delete-server.md)

[<span data-ttu-id="4715c-128">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="4715c-128">DELETE TYPE</span></span>](delete-type.md)

[<span data-ttu-id="4715c-129">HELP</span><span class="sxs-lookup"><span data-stu-id="4715c-129">HELP</span></span>](help.md)

[<span data-ttu-id="4715c-130">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="4715c-130">LOAD APP</span></span>](load-app.md)

[<span data-ttu-id="4715c-131">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-131">LOAD PACKAGE</span></span>](load-package.md)

[<span data-ttu-id="4715c-132">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="4715c-132">LOCK APP</span></span>](lock-app.md)

[<span data-ttu-id="4715c-133">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="4715c-133">PUBLISH APP</span></span>](publish-app.md)

[<span data-ttu-id="4715c-134">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-134">PUBLISH PACKAGE</span></span>](publish-package.md)

[<span data-ttu-id="4715c-135">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="4715c-135">QUERY OBJ</span></span>](query-obj.md)

[<span data-ttu-id="4715c-136">REFRESH SERVER</span><span class="sxs-lookup"><span data-stu-id="4715c-136">REFRESH SERVER</span></span>](refresh-server.md)

[<span data-ttu-id="4715c-137">REPAIR APP</span><span class="sxs-lookup"><span data-stu-id="4715c-137">REPAIR APP</span></span>](repair-app.md)

[<span data-ttu-id="4715c-138">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="4715c-138">UNLOAD APP</span></span>](unload-app.md)

[<span data-ttu-id="4715c-139">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-139">UNLOAD PACKAGE</span></span>](unload-package.md)

[<span data-ttu-id="4715c-140">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="4715c-140">UNLOCK APP</span></span>](unlock-app.md)

[<span data-ttu-id="4715c-141">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4715c-141">UNPUBLISH PACKAGE</span></span>](unpublish-package.md)

 

 





