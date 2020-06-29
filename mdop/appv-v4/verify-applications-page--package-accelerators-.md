---
title: 응용 프로그램 확인 페이지(패키지 가속기)
description: 응용 프로그램 확인 페이지(패키지 가속기)
author: dansimp
ms.assetid: e58a37db-d042-453f-aa0d-2f324600a35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 05e2aed579acfb8d809105c9cf409ee091be0ae5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815103"
---
# <span data-ttu-id="07269-103">응용 프로그램 확인 페이지(패키지 가속기)</span><span class="sxs-lookup"><span data-stu-id="07269-103">Verify Applications Page (Package Accelerators)</span></span>


<span data-ttu-id="07269-104">**응용 프로그램 확인** 페이지를 사용 하 여 패키지에 저장 된 설치 관리자 파일 종속성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-104">Use the **Verify Applications** page to review the installer file dependencies that are saved with the package.</span></span> <span data-ttu-id="07269-105">이러한 파일은 패키지 가속기를 사용 하 여 새 가상 응용 프로그램 패키지를 만들 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-105">These files are required when the Package Accelerator is used to create a new virtual application package.</span></span>

<span data-ttu-id="07269-106">다음 유형의 정보를 추가 하거나 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07269-106">You can add or edit the following types of information.</span></span> <span data-ttu-id="07269-107">응용 프로그램 **이름만** 필요 합니다. 그러나 패키지 가속기를 사용 하는 경우 새 가상 응용 프로그램 패키지가 성공적으로 만들어졌는지 확인 하는 데 최대한 많은 정보를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-107">Only the application **Name** is required; however, you should provide as much information as possible to help ensure that a new virtual application package is created successfully when you use a package accelerator:</span></span>

-   <span data-ttu-id="07269-108">**이름**.</span><span class="sxs-lookup"><span data-stu-id="07269-108">**Name**.</span></span> <span data-ttu-id="07269-109">이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-109">You must specify a name.</span></span>

-   <span data-ttu-id="07269-110">**Publisher**.</span><span class="sxs-lookup"><span data-stu-id="07269-110">**Publisher**.</span></span> <span data-ttu-id="07269-111">선택적으로 응용 프로그램 게시자에 대 한 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-111">Optionally specify information about the application publisher.</span></span>

-   <span data-ttu-id="07269-112">**버전**.</span><span class="sxs-lookup"><span data-stu-id="07269-112">**Version**.</span></span> <span data-ttu-id="07269-113">선택적으로 응용 프로그램 버전 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-113">Optionally specify application version information.</span></span>

-   <span data-ttu-id="07269-114">**언어**.</span><span class="sxs-lookup"><span data-stu-id="07269-114">**Language**.</span></span> <span data-ttu-id="07269-115">선택적으로 언어 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-115">Optionally specify language information.</span></span>

<span data-ttu-id="07269-116">이 페이지에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07269-116">This page contains the following elements:</span></span>

<a href="" id="add"></a>**<span data-ttu-id="07269-117">Add</span><span class="sxs-lookup"><span data-stu-id="07269-117">Add</span></span>**  
<span data-ttu-id="07269-118">패키지 가속기를 적용할 때 필요 하 게 될 새 설치 파일 종속성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-118">Adds a new installation file dependency that will be required when the Package Accelerator is applied.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="07269-119">삭제</span><span class="sxs-lookup"><span data-stu-id="07269-119">Delete</span></span>**  
<span data-ttu-id="07269-120">현재 패키지 가속기에 속해 있는 선택한 종속 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="07269-120">Deletes a selected dependency file that is currently part of the Package Accelerator.</span></span>

<a href="" id="edit"></a>**<span data-ttu-id="07269-121">Edit</span><span class="sxs-lookup"><span data-stu-id="07269-121">Edit</span></span>**  
<span data-ttu-id="07269-122">선택 된 설치 관리자 파일의 종속성과 연결 된 속성을 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07269-122">Enables you to edit the properties associated with the selected installer file’s dependency.</span></span>

## <span data-ttu-id="07269-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="07269-123">Related topics</span></span>


[<span data-ttu-id="07269-124">패키지 가속기 만들기 마법사(App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="07269-124">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





