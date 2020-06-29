---
title: 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법
description: 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 0d2192c1-4058-49fb-b0b6-baf4699ac7f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: bc5f295d35dff1e4fc2a84c47188be40153b85c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813068"
---
# <span data-ttu-id="4eefb-103">복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="4eefb-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="4eefb-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 10 복구 이미지 마법사 실행을 완료 하 고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 10 이미지에 복구 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 10 image.</span></span> <span data-ttu-id="4eefb-105">Windows 운영 체제를 시작 하는 것을 방지 하는 손상 문제로 인해 복구 이미지가 시작 되지 않는 등 파티션을 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-105">A partition is recommended, because any corruption issues that prevent the Windows operating system from starting would also prevent the recovery image from starting.</span></span> <span data-ttu-id="4eefb-106">또한 별도의 파티션을 통해 BitLocker 복구 키를 두 번 제공할 필요가 없어집니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-106">A separate partition also eliminates the need to provide the BitLocker recovery key twice.</span></span> <span data-ttu-id="4eefb-107">사용자가 파일을 저장할 수 없도록 파티션을 숨기는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-107">Consider hiding the partition to prevent users from storing files on it.</span></span>

**<span data-ttu-id="4eefb-108">Windows 10 이미지의 복구 파티션에 DaRT를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="4eefb-108">To deploy DaRT in the recovery partition of a Windows 10 image</span></span>**

1.  <span data-ttu-id="4eefb-109">Windows 10 이미지에서 **DaRT 10 복구 이미지 마법사**를 사용 하 여 만든 ISO 이미지 파일의 크기 보다 크거나 같은 대상 파티션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-109">Create a target partition in your Windows 10 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT 10 Recovery Image wizard**.</span></span>

    <span data-ttu-id="4eefb-110">DaRT 파티션에 필요한 최소 크기는 DaRT의 원격 연결 기능을 수용 하는 500MB입니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-110">The minimum size required for a DaRT partition is 500MB to accommodate the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="4eefb-111">DaRT ISO 이미지 파일에서 부팅 .wim 파일을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-111">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="4eefb-112">회사의 선호 하는 방법을 사용 하 여 **시작 이미지 만들기** 페이지에서 만든 ISO 이미지 파일을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-112">Using your company’s preferred method, mount the ISO image file that you created on the **Create Startup Image** page.</span></span>

    2.  <span data-ttu-id="4eefb-113">ISO 이미지 파일을 열고 탑재 된 이미지의 \\sources 폴더에서 컴퓨터 또는 외부 드라이브의 위치로 부팅 .wim 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-113">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="4eefb-114">**참고**  복구 이미지의 CD, DVD 또는 USB를 구운 경우 이동식 미디어에서 파일을 열고 \\sources 폴더에서 boot.ini 파일을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-114">**Note** If you burned a CD, DVD, or USB of the recovery image, you can open the files on the removable media and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="4eefb-115">부팅 .wim 파일을 복사 하는 경우 이미지를 탑재할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-115">If you copy boot.wim file, you don’t need to mount the image.</span></span>

         

3.  <span data-ttu-id="4eefb-116">Boot.ini 파일을 사용 하 여 사용자 지정 Windows RE 이미지 만들기에 대 한 회사의 표준 방법을 사용 하 여 부팅 가능한 복구 파티션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-116">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="4eefb-117">복구 파티션을 만들거나 사용자 지정 하는 방법에 대 한 자세한 내용은 [WINDOWS RE 환경 사용자 지정](https://go.microsoft.com/fwlink/?LinkId=214222)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4eefb-117">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="4eefb-118">Windows 10 이미지의 대상 파티션을 복구 파티션으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4eefb-118">Replace the target partition in your Windows 10 image with the recovery partition.</span></span>

    <span data-ttu-id="4eefb-119">시스템 실패가 발생 하는 경우에 복구 솔루션을 배포 하 여 공장 이미지를 다시 설치 하는 방법에 대 한 자세한 내용은 [시스템 복구 이미지 배포](https://go.microsoft.com/fwlink/?LinkId=214221)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4eefb-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="4eefb-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4eefb-120">Related topics</span></span>


[<span data-ttu-id="4eefb-121">DaRT 10 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="4eefb-121">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

[<span data-ttu-id="4eefb-122">DaRT 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="4eefb-122">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

[<span data-ttu-id="4eefb-123">DaRT 10 계획</span><span class="sxs-lookup"><span data-stu-id="4eefb-123">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

 

 





