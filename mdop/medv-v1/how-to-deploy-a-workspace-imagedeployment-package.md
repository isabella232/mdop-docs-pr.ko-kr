---
title: 작업 영역 이미지를 배포하는 방법
description: 작업 영역 이미지를 배포하는 방법
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827013"
---
# <span data-ttu-id="d2e91-103">작업 영역 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="d2e91-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="d2e91-104">배포 패키지를 사용 하는 경우 다음 중 한 가지 방법으로 새 이미지를 클라이언트 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="d2e91-105">웹 다운로드</span><span class="sxs-lookup"><span data-stu-id="d2e91-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="d2e91-106">이미지 사전 준비</span><span class="sxs-lookup"><span data-stu-id="d2e91-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="d2e91-107">배포 패키지 내에 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="d2e91-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="d2e91-108">웹을 통해 작업 영역 이미지를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="d2e91-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="d2e91-109">웹을 통해 작업 영역 이미지를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="d2e91-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="d2e91-110">MED-V 이미지를 서버에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="d2e91-111">이미지 업로드에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="d2e91-112">배포 패키지를 만들고 이미지의 위치에 대 한 서버 경로를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="d2e91-113">배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="d2e91-114">패키지를 최종 사용자에 게 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="d2e91-115">패키지 배포에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientdeployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="d2e91-116">MED-V 클라이언트는 처음 설치 및 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="d2e91-117">처음 시작 시 클라이언트는 클라이언트 설치에 지정 된 서버 주소에서 이미지를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="d2e91-118">이미지 사전 준비를 사용 하 여 작업 영역 이미지를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="d2e91-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="d2e91-119">이미지 사전 준비를 사용 하 여 작업 영역 이미지를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="d2e91-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="d2e91-120">이미지의 스테이지 미리 만들기 폴더를 만들고 이미지를 폴더에 밀어넣습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="d2e91-121">이미지 준비 사전 구성에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="d2e91-122">배포 패키지를 만들고 이미지의 스테이지 준비 폴더 경로를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="d2e91-123">배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="d2e91-124">패키지를 최종 사용자에 게 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="d2e91-125">패키지 배포에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientdeployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="d2e91-126">MED-V 클라이언트는 처음 설치 및 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="d2e91-127">처음 시작 시 클라이언트는 클라이언트 설치에 지정 된 단계 전 폴더에서 이미지를 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="d2e91-128">배포 패키지를 사용 하 여 작업 영역 이미지를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="d2e91-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="d2e91-129">배포 패키지를 사용 하 여 작업 영역 이미지를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="d2e91-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="d2e91-130">배포 패키지를 만들고 패키지에 이미지를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="d2e91-131">배포 패키지를 만드는 방법에 대 한 자세한 내용은 [배포 패키지를 구성 하는 방법을](how-to-configure-a-deployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="d2e91-132">패키지를 최종 사용자에 게 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="d2e91-133">패키지 배포에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientdeployment-package.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2e91-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="d2e91-134">패키지 설치의 일부로 이미지를 호스트로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2e91-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="d2e91-135">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d2e91-135">Related topics</span></span>


[<span data-ttu-id="d2e91-136">이미지 웹 배포 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d2e91-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="d2e91-137">배포 패키지를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="d2e91-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





