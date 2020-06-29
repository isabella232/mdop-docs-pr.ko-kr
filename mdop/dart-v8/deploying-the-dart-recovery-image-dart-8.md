---
title: DaRT 복구 이미지 배포
description: DaRT 복구 이미지 배포
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824113"
---
# <span data-ttu-id="fb11d-103">DaRT 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="fb11d-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="fb11d-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지가 포함 된 국제 표준화 기구 (ISO) 파일을 만든 후에는 전체 엔터프라이즈에서 DaRT 8.0 복구 이미지를 배포 하 여 최종 사용자와 헬프 데스크 직원에 게 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can deploy the DaRT 8.0 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="fb11d-105">DaRT 복구 이미지를 배포 하는 데 사용할 수 있는 지원 되는 네 가지 메서드는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="fb11d-106">각 방법의 장점과 단점을 검토 하려면 [DaRT 8.0 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb11d-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="fb11d-107">DaRT 복구 이미지 마법사를 사용 하 여 CD 또는 DVD에 ISO 이미지 파일 굽기</span><span class="sxs-lookup"><span data-stu-id="fb11d-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="fb11d-108">DaRT 복구 이미지 마법사를 사용 하 여 ISO 이미지 파일의 콘텐츠를 UFD (USB 플래시 드라이브)에 저장</span><span class="sxs-lookup"><span data-stu-id="fb11d-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="fb11d-109">ISO 이미지에서 부팅 .wim 파일을 추출 하 고 최종 사용자 컴퓨터에서 사용할 수 있는 원격 파티션으로 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="fb11d-110">ISO 이미지에서 부팅 .wim 파일을 추출 하 고 새 Windows 8 설치의 복구 파티션에 배포</span><span class="sxs-lookup"><span data-stu-id="fb11d-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 8 installation</span></span>

<span data-ttu-id="fb11d-111">**중요**  **DaRT 복구 이미지 마법사** 는 이미지를 CD, DVD 또는 UFD에 굽는 옵션을 제공 하지만 복구 이미지를 저장 하 고 배포 하는 다른 방법은 DaRT에 포함 되지 않은 도구를 포함 하는 추가 단계가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="fb11d-112">이 섹션에는 이러한 다른 메서드에 대 한 몇 가지 지침 및 링크가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="fb11d-113">DaRT 복구 이미지를 복구 파티션의 일부로 배포</span><span class="sxs-lookup"><span data-stu-id="fb11d-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="fb11d-114">DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 Windows 8 이미지의 복구 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span>

[<span data-ttu-id="fb11d-115">복구 파티션의 일부로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="fb11d-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## <span data-ttu-id="fb11d-116">DaRT 복구 이미지를 원격 파티션으로 배포</span><span class="sxs-lookup"><span data-stu-id="fb11d-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="fb11d-117">Windows 배포 서비스와 같은 중앙 네트워크 부팅 서버에서 복구 이미지를 호스팅하고 사용자 또는 지원 직원이 필요에 따라 컴퓨터에 이미지를 스트리밍할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb11d-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="fb11d-118">원격 파티션으로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="fb11d-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## <span data-ttu-id="fb11d-119">DaRT 복구 이미지 배포에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="fb11d-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="fb11d-120">DaRT 8.0 배포</span><span class="sxs-lookup"><span data-stu-id="fb11d-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





