---
title: 작업 영역 이미지를 배포하는 방법
description: 작업 영역 이미지를 배포하는 방법
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827003"
---
# <span data-ttu-id="0b703-103">작업 영역 이미지를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b703-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="0b703-104">엔터프라이즈 소프트웨어 배포 시스템을 사용 하는 경우 다음 중 한 가지 방법으로 새 이미지를 클라이언트 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="0b703-105">웹 다운로드</span><span class="sxs-lookup"><span data-stu-id="0b703-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="0b703-106">이미지 사전 준비</span><span class="sxs-lookup"><span data-stu-id="0b703-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="0b703-107">웹을 통해 작업 영역 이미지를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b703-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="0b703-108">웹을 통해 작업 영역 이미지를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="0b703-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="0b703-109">MED-V 이미지를 서버에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="0b703-110">이미지 업로드에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b703-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="0b703-111">엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 사용자의 컴퓨터에 MED-V 클라이언트 .msi 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="0b703-112">MED-V 클라이언트 .msi 패키지를 설치 하는 방법에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientesds.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b703-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="0b703-113">MED-V 클라이언트는 처음 설치 및 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="0b703-114">처음 시작 시 클라이언트는 클라이언트 설치에 지정 된 서버 주소에서 이미지를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="0b703-115">이미지 사전 준비를 사용 하 여 작업 영역 이미지를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b703-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="0b703-116">이미지 사전 준비를 사용 하 여 작업 영역 이미지를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="0b703-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="0b703-117">이미지의 스테이지 미리 만들기 폴더를 만들고 이미지를 폴더에 밀어넣습니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="0b703-118">이미지 준비 사전 구성에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b703-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="0b703-119">엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 사용자의 컴퓨터에 MED-V 클라이언트 .msi 패키지를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="0b703-120">MED-V 클라이언트 .msi 패키지를 설치 하는 방법에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법을](how-to-install-med-v-clientesds.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b703-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="0b703-121">MED-V 클라이언트는 처음 설치 및 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="0b703-122">처음 시작 시 클라이언트는 클라이언트 설치에 지정 된 단계 전 폴더에서 이미지를 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="0b703-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="0b703-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0b703-123">Related topics</span></span>


[<span data-ttu-id="0b703-124">이미지 웹 배포 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b703-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





