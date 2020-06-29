---
title: 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법
description: 복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823558"
---
# <span data-ttu-id="35dbd-103">복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="35dbd-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="35dbd-104">DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 7 이미지의 복구 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="35dbd-105">Windows 7 이미지의 복구 파티션에 DaRT를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="35dbd-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="35dbd-106">**DaRT 복구 이미지 마법사**를 사용 하 여 만든 ISO 이미지 파일의 크기 보다 크거나 같은 Windows 7 이미지에 대상 파티션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="35dbd-107">DaRT 파티션에 필요한 최소 크기는 대략 300MB입니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="35dbd-108">그러나 DaRT의 원격 연결 기능을 수용 하는 것이 450MB 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="35dbd-109">DaRT ISO 이미지 파일에서 부팅 .wim 파일을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="35dbd-110">회사의 기본 이미지 탑재 방법을 사용 하 여 **시작 이미지 만들기** 대화 상자에서 만든 ISO 이미지 파일을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="35dbd-111">ISO 이미지 파일을 열고 탑재 된 이미지의 \\sources 폴더에서 컴퓨터 또는 외부 드라이브의 위치로 부팅 .wim 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="35dbd-112">**참고**  복구 이미지의 CD 또는 DVD를 구운 경우 CD 또는 DVD의 파일을 열고 \\sources 폴더에서 boot.ini 파일을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="35dbd-113">이렇게 하면 이미지를 탑재할 필요를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="35dbd-114">Boot.ini 파일을 사용 하 여 사용자 지정 Windows RE 이미지 만들기에 대 한 회사의 표준 방법을 사용 하 여 부팅 가능한 복구 파티션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="35dbd-115">복구 파티션을 만들거나 사용자 지정 하는 방법에 대 한 자세한 내용은 [WINDOWS RE 환경 사용자 지정](https://go.microsoft.com/fwlink/?LinkId=214222)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35dbd-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="35dbd-116">Windows 7 이미지의 대상 파티션을 복구 파티션으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="35dbd-117">Windows 7 이미지가 준비 된 후 회사의 표준 이미지 배포 프로세스를 사용 하 여 이미지를 엔터프라이즈의 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="35dbd-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="35dbd-118">Windows 7 이미지를 만드는 방법에 대 한 자세한 내용은 [windows 7의 표준 이미지 빌드: 단계별 가이드](https://go.microsoft.com/fwlink/?LinkId=212103)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35dbd-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="35dbd-119">시스템 실패가 발생 하는 경우에 복구 솔루션을 배포 하 여 공장 이미지를 다시 설치 하는 방법에 대 한 자세한 내용은 [시스템 복구 이미지 배포](https://go.microsoft.com/fwlink/?LinkId=214221)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35dbd-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="35dbd-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="35dbd-120">Related topics</span></span>


[<span data-ttu-id="35dbd-121">DaRT 7.0 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="35dbd-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





