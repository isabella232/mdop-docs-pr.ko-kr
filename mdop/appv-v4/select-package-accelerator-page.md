---
title: 패키지 가속기 선택 페이지
description: 패키지 가속기 선택 페이지
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815593"
---
# <span data-ttu-id="5e182-103">패키지 가속기 선택 페이지</span><span class="sxs-lookup"><span data-stu-id="5e182-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="5e182-104">**패키지 가속기 선택** 페이지를 사용 하 여 새 가상 응용 프로그램 패키지를 만드는 데 사용 되는 패키지 가속기를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="5e182-105">패키지 가속기는 App-v Sequencer를 실행 하는 컴퓨터의 폴더에 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="5e182-106">자세한 내용은 [앱-v 패키지 가속기 정보 (app-v 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5e182-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="5e182-107">신뢰할 수 있는 게시자의 패키지 바로 연결만 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="5e182-108">패키지 가속기에는 일반적으로 디지털 서명이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="5e182-109">디지털 서명은 소프트웨어의 게시자를 표시 하는 데 도움이 될 수 있는 전자 보안 표시와 변환이 원래 서명 된 후 패키지가 훼손 되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="5e182-110">게시자에 의해 디지털 서명 된 변환을 사용 하는 경우 게시자가 인증 기관에서 해당 id를 확인 한 경우 해당 게시자가 변환을 생성 하 고 변경 되지 않았다는 확신을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="5e182-111">App-v Sequencer는 다음 조건 중 하나라도 충족 되는 경우 사용자에 게 알립니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="5e182-112">선택한 변환이 디지털 서명 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="5e182-113">선택한 변환이 인증 기관에서 해당 id를 확인 하지 않은 게시자에 의해 서명 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="5e182-114">디지털 서명 및 해제 된 후 선택한 변환이 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="5e182-115">패키지 가속기를 사용할 때 이러한 메시지가 표시 되는 경우 패키지 가속기 게시자의 웹 사이트를 방문 하 여 디지털 서명 된 버전의 변환을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="5e182-116">이 페이지에는 다음 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="5e182-117">찾아보기</span><span class="sxs-lookup"><span data-stu-id="5e182-117">Browse</span></span>**  
<span data-ttu-id="5e182-118">**찾아보기를** 클릭 하 여 가상 응용 프로그램 패키지를 만드는 데 사용할 패키지 가속기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="5e182-119">Sequencer를 실행 하는 컴퓨터에 로컬로 지정 된 패키지 가속기를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e182-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="5e182-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5e182-120">Related topics</span></span>


[<span data-ttu-id="5e182-121">Sequencer 마법사 - 패키지 가속기(App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="5e182-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





