---
title: Sequencer 명령줄 사용 정보
description: Sequencer 명령줄 사용 정보
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819903"
---
# <span data-ttu-id="da5a3-103">Sequencer 명령줄 사용 정보</span><span class="sxs-lookup"><span data-stu-id="da5a3-103">About Using the Sequencer Command Line</span></span>


<span data-ttu-id="da5a3-104">명령줄을 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-104">You can use the command line to create sequenced application packages.</span></span> <span data-ttu-id="da5a3-105">명령줄을 사용 하 여 가상 응용 프로그램을 만드는 경우 다음과 같은 시나리오에서 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-105">Using the command line to create virtual applications is useful in the following scenarios:</span></span>

-   <span data-ttu-id="da5a3-106">많은 수의 시퀀싱 된 응용 프로그램 패키지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-106">You need to create a large number of sequenced application packages.</span></span>

-   <span data-ttu-id="da5a3-107">반복적으로 시퀀싱 된 응용 프로그램 패키지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-107">You need to create a sequenced application package on a recurring basis.</span></span>

<span data-ttu-id="da5a3-108">**중요**  명령 프롬프트에서 시퀀싱 하면 기본 시퀀싱만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-108">**Important** Sequencing at the command prompt allows for default sequencing only.</span></span> <span data-ttu-id="da5a3-109">기본 시퀀싱 매개 변수를 변경 해야 하는 경우에는 시퀀싱 된 응용 프로그램 패키지를 수동으로 수정 하거나 응용 프로그램을 다시 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-109">If you need to change default sequencing parameters, you must either manually modify a sequenced application package or re-sequence the application.</span></span>

 

<span data-ttu-id="da5a3-110">시퀀싱 마법사를 사용 하 여 기존 시퀀싱 된 응용 프로그램 패키지에 대 한 모든 후속 수정 작업을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-110">All subsequent modifications to existing sequenced application packages must be made using the sequencing wizard.</span></span>

## <span data-ttu-id="da5a3-111">필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="da5a3-111">Prerequisites</span></span>


<span data-ttu-id="da5a3-112">명령 프롬프트를 사용 하 여 응용 프로그램을 시퀀싱 하려면 다음 조건을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-112">To sequence an application by using the command prompt, the following conditions must be met:</span></span>

-   <span data-ttu-id="da5a3-113">시퀀싱 하려는 응용 프로그램에는 설치 관리자 또는 Windows Installer 패키지 외부에 있는 변경 또는 해결책이 필요 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-113">The application that is about to be sequenced must not require changes or workarounds made to it outside the installer or Windows Installer package.</span></span>

-   <span data-ttu-id="da5a3-114">시퀀싱 하기 전에 시퀀싱 된 응용 프로그램 패키지를 만들기 위한 배치 파일 목록을 준비 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-114">Before sequencing, you must prepare a list of batch files for creating the sequenced application packages.</span></span>

-   <span data-ttu-id="da5a3-115">검토 명령줄 매개 변수에 대 한 자세한 내용은 명령줄 [매개 변수](command-line-parameters.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da5a3-115">Review For more information about the command line parameters, see [Command-Line Parameters](command-line-parameters.md).</span></span>

-   <span data-ttu-id="da5a3-116">명령줄을 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 만들 때 표시 될 수 있는 오류를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="da5a3-116">Review the errors that might be displayed when creating a sequenced application package by using the command line.</span></span> <span data-ttu-id="da5a3-117">자세한 내용은 명령줄 [오류](command-line-errors.md)를 참조 하 여 오류를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da5a3-117">For more information, see these errors, see [Command-Line Errors](command-line-errors.md).</span></span>

## <span data-ttu-id="da5a3-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="da5a3-118">Related topics</span></span>


[<span data-ttu-id="da5a3-119">명령줄을 사용하여 가상 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="da5a3-119">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





