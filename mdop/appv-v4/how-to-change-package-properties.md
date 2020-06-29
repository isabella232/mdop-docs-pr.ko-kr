---
title: 패키지 속성을 변경하는 방법
description: 패키지 속성을 변경하는 방법
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818043"
---
# <span data-ttu-id="5a9b9-103">패키지 속성을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="5a9b9-103">How to Change Package Properties</span></span>


<span data-ttu-id="5a9b9-104">다음 절차를 사용 하 여 응용 프로그램 가상화 패키지 이름과 관련 설명을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="5a9b9-105">패키지를 처음으로 만든 경우 시퀀싱 된 응용 프로그램 패키지가 응용 프로그램 가상화 서버에서 응용 프로그램 가상화 데스크톱 클라이언트로 스트리밍되는 방법을 결정 하는 시퀀싱 매개 변수 블록 크기를 변경할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="5a9b9-106">**참고**  블록 크기를 선택할 때 SFT 파일과 네트워크 대역폭의 크기를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="5a9b9-107">더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="5a9b9-108">블록 크기가 더 많은 파일은 스트리밍할 수 있지만 더 많은 네트워크 대역폭을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="5a9b9-109">실험을 통해 네트워크의 스트리밍 응용 프로그램에 대 한 최적의 블록 크기를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="5a9b9-110">**속성** 탭의 나머지 패키지 속성은 자동으로 생성 되며이 탭에서 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="5a9b9-111">패키지 이름 또는 설명을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="5a9b9-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="5a9b9-112">**속성** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="5a9b9-113">**패키지 이름** 텍스트 상자에서 패키지에 사용 되는 단일 이름을 입력 하거나 편집 하 여 여러 응용 프로그램을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="5a9b9-114">**메모** 텍스트 상자에서 원하는 대로 메모를 입력 하거나 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="5a9b9-115">모범 사례는 패키지 및 시퀀싱에 대 한 자세한 정보를 제공 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="5a9b9-116">**파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="5a9b9-117">블록 크기를 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="5a9b9-117">To change the block size</span></span>**

1.  <span data-ttu-id="5a9b9-118">**속성** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="5a9b9-119">**블록 크기** 드롭다운 목록에서 4kb, **16kb**, **32 kb**또는 **64 KB** **를 선택 합니다**.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="5a9b9-120">**파일** 메뉴에서 **저장**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="5a9b9-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5a9b9-121">Related topics</span></span>


[<span data-ttu-id="5a9b9-122">속성 탭 정보</span><span class="sxs-lookup"><span data-stu-id="5a9b9-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="5a9b9-123">Sequencer Console</span><span class="sxs-lookup"><span data-stu-id="5a9b9-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





