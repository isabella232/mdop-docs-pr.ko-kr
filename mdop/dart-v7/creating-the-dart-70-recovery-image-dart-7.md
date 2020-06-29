---
title: DaRT 7.0 복구 이미지 만들기
description: DaRT 7.0 복구 이미지 만들기
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823283"
---
# <span data-ttu-id="7c6a5-103">DaRT 7.0 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="7c6a5-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="7c6a5-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7에는 Windows에서 부팅 가능한 국제 표준화 (ISO) 이미지를 만드는 데 사용 되는 **DaRT 복구 이미지 마법사** 가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="7c6a5-105">ISO 이미지는 CD의 원시 콘텐츠를 나타내는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="7c6a5-106">DaRT 복구 이미지 마법사를 사용 하 여 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="7c6a5-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="7c6a5-107">DaRT 복구 이미지 마법사에서 만든 ISO에는 다른 방법으로 시작 되지 않는 경우에도 문제 컴퓨터로 부팅할 수 있는 DaRT 복구 이미지가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="7c6a5-108">컴퓨터를 DaRT로 부팅 한 후 다른 DaRT 도구를 실행 하 여 컴퓨터를 진단 하 고 복구 해 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="7c6a5-109">기록 가능한 CD 또는 DVD에 ISO를 작성 하 고, USB 플래시 드라이브에 저장 하거나, 원격 파티션이나 복구 파티션에서 DaRT로 부팅 하는 데 사용할 수 있는 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="7c6a5-110">자세한 내용은 [DaRT 7.0 복구 이미지 배포](deploying-the-dart-70-recovery-image-dart-7.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="7c6a5-111">**참고**  컴퓨터에 CD-RW 드라이브가 포함 된 경우 마법사는 ISO 이미지를 빈 CD 또는 DVD로 굽는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="7c6a5-112">컴퓨터에 마법사에서 지원 되는 드라이브가 포함 되어 있지 않은 경우 CD 또는 DVD를 구울 수 있는 대부분의 프로그램을 사용 하 여 CD 또는 DVD에 ISO 이미지를 구울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="7c6a5-113">ISO 이미지에서 부팅 가능한 CD 또는 DVD를 만들려면 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="7c6a5-114">CD-RW 드라이브.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="7c6a5-115">기록 가능한 CD 또는 DVD (기록 가능한 드라이브에서 지원 되는 형식)</span><span class="sxs-lookup"><span data-stu-id="7c6a5-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="7c6a5-116">기록 가능한 드라이브를 지원 하 고 ISO 이미지를 CD 또는 DVD로 직접 구울 수 있도록 지 원하는 소프트웨어입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="7c6a5-117">**중요**  일부 컴퓨터에서 기록 가능한 모든 종류의 미디어를 사용할 수 없기 때문에 지원 하려는 다른 모든 종류의 컴퓨터에서 만든 CD 또는 DVD를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="7c6a5-118">UFD (USB 플래시 드라이브)에 ISO 이미지를 저장 하려면 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="7c6a5-119">올바르게 형식이 지정 된 UFD.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="7c6a5-120">ISO 이미지를 탑재 하는 데 사용할 수 있는 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="7c6a5-121">DaRT 복구 이미지 마법사를 사용하여 복구 이미지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="7c6a5-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="7c6a5-122">제한 된 시간 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="7c6a5-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="7c6a5-123">특정 일 수만 생성 된 후에만 사용할 수 있는 DaRT 복구 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="7c6a5-124">이렇게 하려면 명령 프롬프트에서 **DaRT 복구 이미지 마법사** 를 실행 하 고 일 수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6a5-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="7c6a5-125">시간 제한 복구 이미지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="7c6a5-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="7c6a5-126">DaRT7 복구 이미지 만들기에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="7c6a5-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="7c6a5-127">DaRT 7.0 배포</span><span class="sxs-lookup"><span data-stu-id="7c6a5-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





