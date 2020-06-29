---
title: 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법
description: 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823568"
---
# <span data-ttu-id="f8ea8-103">원격 파티션으로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="f8ea8-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="f8ea8-104">DaRT 복구 이미지 마법사 실행을 마치고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 네트워크의 원격 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="f8ea8-105">DaRT를 원격 파티션으로 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="f8ea8-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="f8ea8-106">DaRT ISO 이미지 파일에서 부팅 .wim 파일을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="f8ea8-107">회사의 기본 이미지 탑재 방법을 사용 하 여 **시작 이미지 만들기** 대화 상자에서 만든 ISO 이미지 파일을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="f8ea8-108">ISO 이미지 파일을 열고 탑재 된 이미지의 \\sources 폴더에서 컴퓨터 또는 외부 드라이브의 위치로 부팅 .wim 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="f8ea8-109">**참고**  복구 이미지의 CD 또는 DVD를 구운 경우 CD 또는 DVD의 파일을 열고 \\sources 폴더에서 boot.ini 파일을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="f8ea8-110">이렇게 하면 이미지를 탑재할 필요를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="f8ea8-111">엔터프라이즈의 최종 사용자 컴퓨터에서 액세스할 수 있는 WDS 서버에 부팅 .wim 파일을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="f8ea8-112">표준 WDS 배포 절차에 따라 DaRT 용 부팅 .wim 파일을 사용 하도록 WDS 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="f8ea8-113">DaRT를 원격 파티션으로 배포 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8ea8-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="f8ea8-114">연습: PXE를 사용 하 여 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="f8ea8-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="f8ea8-115">Windows 배포 서비스 시작 가이드</span><span class="sxs-lookup"><span data-stu-id="f8ea8-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="f8ea8-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f8ea8-116">Related topics</span></span>


[<span data-ttu-id="f8ea8-117">DaRT 7.0 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="f8ea8-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





