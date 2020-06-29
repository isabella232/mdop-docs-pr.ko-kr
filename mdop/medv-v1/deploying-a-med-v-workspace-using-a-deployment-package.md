---
title: 배포 패키지를 사용하여 MED-V 작업 영역 배포
description: 배포 패키지를 사용하여 MED-V 작업 영역 배포
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823633"
---
# <span data-ttu-id="3dfce-103">배포 패키지를 사용하여 MED-V 작업 영역 배포</span><span class="sxs-lookup"><span data-stu-id="3dfce-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="3dfce-104">배포 패키지 설치는 필요한 모든 필수 구성 요소와 관리자가 미리 정의한 모든 설정과 함께 MED-V 클라이언트를 설치 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="3dfce-105">배포 패키지를 사용 하는 경우 패키지가 공유 네트워크 또는 이동식 미디어를 통해 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="3dfce-106">이미지는 패키지에 포함 되거나 별도로 배포 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="3dfce-107">배포 패키지를 만들기 전에 배포 준비가 된 MED-V 이미지를 만들었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="3dfce-108">MED-V 이미지를 만드는 방법에 대 한 자세한 내용은 [Med-v 이미지 만들기](creating-a-med-v-image.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="3dfce-109">MED-V 이미지를 준비한 후에는 환경에서 이미지를 배포 하는 가장 좋은 방법을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="3dfce-110">이미지는 다음 방법 중 하나로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="3dfce-111">웹에 업로드 되 고 웹 다운로드를 통해 배포 되며 선택적으로 트리밍 전환 기술을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="3dfce-112">이미지 사전 준비를 사용 하 여 배포</span><span class="sxs-lookup"><span data-stu-id="3dfce-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="3dfce-113">배포 패키지에 포함 되어 다른 모든 MED-V 구성 요소와 함께 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="3dfce-114">이미지가 패키지에 포함 되는 경우 이미지에 다른 구성은 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="3dfce-115">이미지가 배포 패키지에 포함 되지 않을 경우 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="3dfce-116">웹을 통해 이미지를 배포 하는 경우에는 이미지 웹 배포 서버에 MED-V 이미지를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="3dfce-117">이미지 웹 배포 서버를 구성 하는 방법에 대 한 자세한 내용은 [이미지 웹 배포 서버를 구성 하는 방법을](how-to-configure-the-image-web-distribution-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="3dfce-118">서버에 이미지를 업로드 하는 방법에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="3dfce-119">이미지를 미리 준비 하 여 이미지를 배포 하는 경우 단계 전 폴더를 구성 하 고 MED-V 이미지를 폴더에 밀어넣습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="3dfce-120">미리 준비 이미지를 구성 하는 방법에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="3dfce-121">**참고**  이미지 사전 준비를 사용 하는 경우 배포 패키지를 만들기 전에 이미지 미리 스테이지 폴더를 구성 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="3dfce-122">폴더 경로를 배포 패키지에 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="3dfce-123">마지막으로 배포 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-123">Finally, create the deployment package.</span></span> <span data-ttu-id="3dfce-124">배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="3dfce-125">패키지가 완료 되 면 배포를 위해 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="3dfce-126">배포 패키지가 배포 된 후에는 MED-V 클라이언트를 설치 하 고 이미지를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfce-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="3dfce-127">MED-V 클라이언트 설치에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법](how-to-install-med-v-clientdeployment-package.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="3dfce-128">이미지 배포에 대 한 자세한 내용은 [작업 영역 이미지를 배포 하는 방법을](how-to-deploy-a-workspace-imagedeployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dfce-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





