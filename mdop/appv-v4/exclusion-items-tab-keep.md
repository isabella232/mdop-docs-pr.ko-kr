---
title: 제외 항목 탭
description: 제외 항목 탭
author: dansimp
ms.assetid: 864e46dd-3d6e-4a1b-acf4-9dc00548117e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f472fb61c121a1977c3c4ff927bd1ba6f680d86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821578"
---
# <span data-ttu-id="26c60-103">제외 항목 탭</span><span class="sxs-lookup"><span data-stu-id="26c60-103">Exclusion Items Tab</span></span>


<span data-ttu-id="26c60-104">**제외 항목** 탭에는 응용 프로그램 가상화 시퀀서에서 가상 파일 시스템 또는 가상 레지스트리에서 제외한 식이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-104">The **Exclusion Items** tab displays the expressions that the Application Virtualization Sequencer excludes from the virtual file system or virtual registry.</span></span> <span data-ttu-id="26c60-105">이러한 식은 응용 프로그램 가상화 데스크톱 클라이언트에서 시퀀싱 된 응용 프로그램 패키지를 실행할 수 있도록 하기 위해 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-105">These expressions are excluded to ensure that the sequenced application package can run on Application Virtualization Desktop Clients.</span></span> <span data-ttu-id="26c60-106">또한 순서 대로 원치 않을 수 있는 비표준 설치 디렉터리를 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-106">You can also exclude non-standard installation directories that might be unwanted in the sequencing.</span></span>

<span data-ttu-id="26c60-107">이 탭에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-107">This tab contains the following elements.</span></span>

<a href="" id="exclude-path"></a>**<span data-ttu-id="26c60-108">제외 경로</span><span class="sxs-lookup"><span data-stu-id="26c60-108">Exclude Path</span></span>**  
<span data-ttu-id="26c60-109">가상 파일 시스템 항목 또는 가상 레지스트리 항목을 구문 분석 하는 동안 발생 한 시퀀서에서 제외 되는 변수 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-109">Displays variable names that the Sequencer excludes if encountered while parsing virtual file system items or virtual registry items.</span></span>

<a href="" id="resolves-to"></a>**<span data-ttu-id="26c60-110">(으)로 확인</span><span class="sxs-lookup"><span data-stu-id="26c60-110">Resolves To</span></span>**  
<span data-ttu-id="26c60-111">시퀀서 변수에 해당 하는 실제 경로를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-111">Displays the actual paths that correspond to the Sequencer variables.</span></span>

<a href="" id="map-type"></a>**<span data-ttu-id="26c60-112">지도 종류</span><span class="sxs-lookup"><span data-stu-id="26c60-112">Map Type</span></span>**  
<span data-ttu-id="26c60-113">Sequencer가 가상 파일 시스템 또는 가상 레지스트리의 항목을 구문 분석 하는 데 적용 하는 매핑 규칙을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-113">Displays mapping rules that the Sequencer applies to parse items in the virtual file system or virtual registry.</span></span> <span data-ttu-id="26c60-114">다음 값 중 하나가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-114">One of the following values can occur:</span></span>

<a href="" id="new"></a>**<span data-ttu-id="26c60-115">신규</span><span class="sxs-lookup"><span data-stu-id="26c60-115">New</span></span>**  
<span data-ttu-id="26c60-116">을 클릭 하 여 새 제외 항목을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-116">Click to enter a new exclusion item.</span></span>

<a href="" id="edit"></a>**<span data-ttu-id="26c60-117">Edit</span><span class="sxs-lookup"><span data-stu-id="26c60-117">Edit</span></span>**  
<span data-ttu-id="26c60-118">선택한 제외를 편집 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-118">Click to edit a selected exclusion.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="26c60-119">삭제</span><span class="sxs-lookup"><span data-stu-id="26c60-119">Delete</span></span>**  
<span data-ttu-id="26c60-120">선택 된 제외를 제거 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-120">Click to remove a selected exclusion.</span></span>

<a href="" id="save-as-default"></a>**<span data-ttu-id="26c60-121">기본값으로 저장</span><span class="sxs-lookup"><span data-stu-id="26c60-121">Save As Default</span></span>**  
<span data-ttu-id="26c60-122">현재 제외 항목을 기본값으로 저장 하려면을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-122">Click to save the current exclusion items as your default.</span></span>

<a href="" id="restore-defaults"></a>**<span data-ttu-id="26c60-123">기본값 복원</span><span class="sxs-lookup"><span data-stu-id="26c60-123">Restore Defaults</span></span>**  
<span data-ttu-id="26c60-124">기본 지정 제외 항목을 복원 하 고 추가한 항목을 제거 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-124">Click to restore default-assigned exclusion items and remove any items you added.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="26c60-125">확인</span><span class="sxs-lookup"><span data-stu-id="26c60-125">OK</span></span>**  
<span data-ttu-id="26c60-126">표시 된 예외를 수락 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-126">Click to accept the displayed exceptions.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="26c60-127">취소</span><span class="sxs-lookup"><span data-stu-id="26c60-127">Cancel</span></span>**  
<span data-ttu-id="26c60-128">변경한 내용을 취소 하려면 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c60-128">Click to cancel any changes you have made.</span></span>

## <span data-ttu-id="26c60-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="26c60-129">Related topics</span></span>


[<span data-ttu-id="26c60-130">Application Virtualization Sequencer 옵션 대화 상자</span><span class="sxs-lookup"><span data-stu-id="26c60-130">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

[<span data-ttu-id="26c60-131">제외 항목 대화 상자</span><span class="sxs-lookup"><span data-stu-id="26c60-131">Exclusion Item Dialog Box</span></span>](exclusion-item-dialog-box.md)

 

 





