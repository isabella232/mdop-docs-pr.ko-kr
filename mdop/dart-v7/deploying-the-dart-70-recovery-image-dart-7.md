---
title: DaRT 7.0 복구 이미지 배포
description: DaRT 7.0 복구 이미지 배포
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812657"
---
# <span data-ttu-id="9d632-103">DaRT 7.0 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="9d632-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="9d632-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 7 복구 이미지가 포함 된 국제 표준화 기구 (ISO) 파일을 만든 후에는 enterprise 전체에서 DaRT 복구 이미지를 배포 하 여 최종 사용자 및 헬프데스크 상담원에 게 제공 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="9d632-105">DaRT 복구 이미지를 배포 하는 데 사용할 수 있는 지원 되는 네 가지 메서드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="9d632-106">CD 또는 DVD에 ISO 이미지 파일 굽기</span><span class="sxs-lookup"><span data-stu-id="9d632-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="9d632-107">UFD (USB 플래시 드라이브)에 ISO 이미지 파일의 내용 저장</span><span class="sxs-lookup"><span data-stu-id="9d632-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="9d632-108">ISO 이미지에서 부팅 .wim 파일을 추출 하 고 최종 사용자 컴퓨터에서 사용할 수 있는 원격 파티션으로 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="9d632-109">ISO 이미지에서 부팅 .wim 파일을 추출 하 고 새 Windows 7 설치의 복구 파티션에 배포</span><span class="sxs-lookup"><span data-stu-id="9d632-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="9d632-110">**중요**  **DaRT 복구 이미지 마법사** 는 CD 또는 DVD를 구울 수 있는 옵션만 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="9d632-111">복구 이미지를 저장 하 고 배포 하는 다른 모든 방법에는 DaRT에 포함 되지 않은 도구를 포함 하는 추가 단계가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="9d632-112">이 섹션에는 이러한 다른 메서드에 대 한 몇 가지 지침 및 링크가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="9d632-113">USB 플래시 드라이브를 사용 하 여 DaRT 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="9d632-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="9d632-114">DaRT 복구 이미지 마법사 실행을 완료 한 후에는의 도구를 사용 하 여 <https://go.microsoft.com/fwlink/?LinkId=218888> ISO 이미지 파일을 UFD (USB 플래시 드라이브)에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="9d632-115">USB 플래시 드라이브를 사용하여 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="9d632-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="9d632-116">DaRT 복구 이미지를 복구 파티션의 일부로 배포</span><span class="sxs-lookup"><span data-stu-id="9d632-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="9d632-117">DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 7 이미지의 복구 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="9d632-118">복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="9d632-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="9d632-119">DaRT 복구 이미지를 원격 파티션으로 배포</span><span class="sxs-lookup"><span data-stu-id="9d632-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="9d632-120">DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 네트워크의 원격 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d632-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="9d632-121">원격 파티션으로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="9d632-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="9d632-122">DaRT 복구 이미지 배포를 유지 관리 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="9d632-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="9d632-123">DaRT 7.0 배포</span><span class="sxs-lookup"><span data-stu-id="9d632-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





