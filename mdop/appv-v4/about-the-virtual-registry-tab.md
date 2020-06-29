---
title: 가상 레지스트리 탭 정보
description: 가상 레지스트리 탭 정보
author: dansimp
ms.assetid: ca8d837f-8218-4f86-95fd-13a44dccd022
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 77decee4a8e07333b466db0a1bd0513efe859c9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819893"
---
# <span data-ttu-id="a15bf-103">가상 레지스트리 탭 정보</span><span class="sxs-lookup"><span data-stu-id="a15bf-103">About the Virtual Registry Tab</span></span>


<span data-ttu-id="a15bf-104">가상 레지스트리는 시퀀싱 하는 동안 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-104">A virtual registry is created during sequencing.</span></span> <span data-ttu-id="a15bf-105">**가상 레지스트리** 탭에는 시퀀싱 된 응용 프로그램 패키지를 실행 하는 데 필요한 모든 레지스트리 키와 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-105">The **Virtual Registry** tab displays all the registry keys and values that are required for a sequenced application package to run.</span></span> <span data-ttu-id="a15bf-106">이 탭을 사용 하 여 레지스트리 키 및 레지스트리 값을 추가, 편집 및 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-106">Use this tab to add, edit, and delete registry keys and registry values.</span></span>

<span data-ttu-id="a15bf-107">또한 **로컬 키 재정의**를 선택 하 여 호스팅 시스템의 키를 무시 하도록 선택 하거나, **로컬 키를 사용**하 여 병합을 선택 하 여 가상 환경 내에서 키의 병합 된 뷰를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-107">You can also choose to ignore the hosting system’s keys by selecting **Override Local Key**, or you can create a merged view of the key from within the virtual environment by selecting **Merge with Local Key**.</span></span>

<span data-ttu-id="a15bf-108">가상 레지스트리 **설정** 탭에 대 한 변경 사항은 특정 시퀀싱 된 응용 프로그램 패키지에 포함 된 응용 프로그램에 영향을 주지만 응용 프로그램 가상화 데스크톱 클라이언트에 설치 하거나 로컬로 설치한 다른 응용 프로그램의 작동에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-108">The changes to the virtual registry **Settings** tab affect applications that are part of the specific sequenced application package, but they do not affect the operation of other applications that are streamed to or locally installed on the Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="a15bf-109">**참고**  가상 레지스트리 키 및 값을 변경할 때는 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-109">**Note** Exercise caution when changing virtual registry keys and values.</span></span> <span data-ttu-id="a15bf-110">이러한 키와 값을 변경 하면 시퀀싱 한 응용 프로그램 패키지가 작동 하지 않을 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-110">Changing these keys and values might render your sequenced application package inoperable.</span></span>

 

<span data-ttu-id="a15bf-111">**가상 레지스트리** 탭의 왼쪽 창에는 응용 프로그램을 시퀀싱 하는 동안 생성 된 가상 레지스트리에 대 한 전체 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-111">The left pane of the **Virtual Registry** tab displays the full list of virtual registries created during the sequencing of an application.</span></span>

## <span data-ttu-id="a15bf-112">열</span><span class="sxs-lookup"><span data-stu-id="a15bf-112">Columns</span></span>


<a href="" id="name"></a>**<span data-ttu-id="a15bf-113">이름</span><span class="sxs-lookup"><span data-stu-id="a15bf-113">Name</span></span>**  
<span data-ttu-id="a15bf-114">가상 레지스트리의 항목에 대 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-114">The name for the entry in the virtual registry.</span></span>

<a href="" id="type"></a>**<span data-ttu-id="a15bf-115">형식</span><span class="sxs-lookup"><span data-stu-id="a15bf-115">Type</span></span>**  
<span data-ttu-id="a15bf-116">항목이 데이터를 저장 하는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-116">How the entry stores its data.</span></span>

<a href="" id="data"></a>**<span data-ttu-id="a15bf-117">데이터</span><span class="sxs-lookup"><span data-stu-id="a15bf-117">Data</span></span>**  
<span data-ttu-id="a15bf-118">Entry에 저장 된 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-118">The value stored by the entry.</span></span>

<a href="" id="attributes"></a>**<span data-ttu-id="a15bf-119">특성</span><span class="sxs-lookup"><span data-stu-id="a15bf-119">Attributes</span></span>**  
<span data-ttu-id="a15bf-120">파일 특성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15bf-120">Displays the file attributes.</span></span>

## <span data-ttu-id="a15bf-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a15bf-121">Related topics</span></span>


[<span data-ttu-id="a15bf-122">가상 레지스트리 키 정보를 수정하는 방법</span><span class="sxs-lookup"><span data-stu-id="a15bf-122">How to Modify Virtual Registry Key Information</span></span>](how-to-modify-virtual-registry-key-information.md)

[<span data-ttu-id="a15bf-123">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="a15bf-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





