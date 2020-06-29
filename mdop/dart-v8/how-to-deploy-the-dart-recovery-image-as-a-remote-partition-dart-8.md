---
title: 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법
description: 원격 파티션으로 DaRT 복구 이미지를 배포하는 방법
author: dansimp
ms.assetid: 58f4a6c6-6193-42bd-a095-0de868711af9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e9a6e3a9dc25139210ae22ba767da984e9a7b86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821268"
---
# <span data-ttu-id="f6b7d-103">원격 파티션으로 DaRT 복구 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="f6b7d-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="f6b7d-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 복구 이미지 마법사 실행을 완료 하 고 복구 이미지를 만든 후에는 ISO 이미지 파일에서 boot.ini 파일을 추출 하 여 네트워크에 원격 파티션으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="f6b7d-105">DaRT 8.0을 원격 파티션으로 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="f6b7d-105">To deploy DaRT 8.0 as a remote partition</span></span>**

1.  <span data-ttu-id="f6b7d-106">DaRT ISO 이미지 파일에서 부팅 .wim 파일을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="f6b7d-107">회사의 기본 이미지 탑재 방법을 사용 하 여 **시작 이미지 만들기** 대화 상자에서 만든 ISO 이미지 파일을 탑재 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="f6b7d-108">ISO 이미지 파일을 열고 탑재 된 이미지의 \\sources 폴더에서 컴퓨터 또는 외부 드라이브의 위치로 부팅 .wim 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="f6b7d-109">**참고**  복구 이미지의 CD 또는 DVD를 구운 경우 CD 또는 DVD의 파일을 열고 \\sources 폴더에서 boot.ini 파일을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="f6b7d-110">이렇게 하면 이미지를 탑재할 필요를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="f6b7d-111">엔터프라이즈의 최종 사용자 컴퓨터에서 액세스할 수 있는 WDS 서버에 부팅 .wim 파일을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="f6b7d-112">표준 WDS 배포 절차에 따라 DaRT 용 부팅 .wim 파일을 사용 하도록 WDS 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="f6b7d-113">DaRT를 원격 파티션으로 배포 하는 방법에 대 한 자세한 내용은 연습: PXE 및 [Windows 배포 서비스 시작 가이드](https://go.microsoft.com/fwlink/?LinkId=212106)를 [사용 하 여 이미지 배포](https://go.microsoft.com/fwlink/?LinkId=212108) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f6b7d-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="f6b7d-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f6b7d-114">Related topics</span></span>


[<span data-ttu-id="f6b7d-115">DaRT 8.0 복구 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="f6b7d-115">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="f6b7d-116">DaRT 복구 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="f6b7d-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="f6b7d-117">DaRT 8.0 계획</span><span class="sxs-lookup"><span data-stu-id="f6b7d-117">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





