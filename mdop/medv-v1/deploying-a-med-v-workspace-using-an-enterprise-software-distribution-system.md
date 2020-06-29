---
title: 엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포
description: 엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823628"
---
# <span data-ttu-id="57782-103">엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포</span><span class="sxs-lookup"><span data-stu-id="57782-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="57782-104">MED-V 클라이언트는 Microsoft System Center Configuration Manager와 같은 엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57782-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="57782-105">**참고**  Microsoft System Center Configuration Manager를 사용 하 여 MED-V를 설치한 경우 MED-V에 대 한 패키지를 만들 때 실행 모드를 관리 권한으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="57782-106">엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MED-V를 배포 하기 전에 배포 준비를 위한 MED-V 이미지를 만들었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="57782-107">MED-V 이미지를 만드는 방법에 대 한 자세한 내용은 [Med-v 이미지 만들기](creating-a-med-v-image.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57782-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="57782-108">MED-V 이미지를 준비한 후에는 환경에서 이미지를 배포 하는 가장 좋은 방법을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="57782-109">이미지는 다음 방법 중 하나로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57782-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="57782-110">웹에 업로드 되 고 웹 다운로드를 통해 배포 되며 필요에 따라 트리밍 전환 기술을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57782-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="57782-111">이미지 사전 준비를 사용 하 여 배포</span><span class="sxs-lookup"><span data-stu-id="57782-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="57782-112">웹을 통해 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="57782-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="57782-113">웹을 통해 이미지를 배포 하는 경우에는 이미지 웹 배포 서버에 MED-V 이미지를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="57782-114">이미지 웹 배포 서버를 구성 하는 방법에 대 한 자세한 내용은 [이미지 웹 배포 서버를 구성 하는 방법을](how-to-configure-the-image-web-distribution-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57782-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="57782-115">서버에 이미지를 업로드 하는 방법에 대 한 자세한 내용은 [서버에 Med-v 이미지를 업로드 하는 방법을](how-to-upload-a-med-v-image-to-the-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57782-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="57782-116">사전 준비를 통해 이미지 배포</span><span class="sxs-lookup"><span data-stu-id="57782-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="57782-117">이미지를 미리 준비 하 여 이미지를 배포 하는 경우 단계 전 폴더를 구성 하 고 MED-V 이미지를 폴더에 밀어넣습니다.</span><span class="sxs-lookup"><span data-stu-id="57782-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="57782-118">이미지 사전 준비 구성에 대 한 자세한 내용은 [이미지 사전 준비를 구성 하는 방법을](how-to-configure-image-pre-staging.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57782-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="57782-119">**참고**  이미지 사전 준비를 사용 하는 경우에는 클라이언트 .msi 패키지를 푸시 하기 전에 이미지 미리 스테이지 폴더를 구성 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="57782-120">폴더 경로는 클라이언트 .msi 패키지에 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="57782-121">마지막으로, 엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 클라이언트 .msi 패키지를 푸시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57782-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="57782-122">그런 다음 MED-V를 설치 하 고 이미지를 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57782-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="57782-123">MED-V 클라이언트 설치에 대 한 자세한 내용은 [Med-v 클라이언트를 설치 하는 방법](how-to-install-med-v-clientesds.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57782-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="57782-124">이미지 배포에 대 한 자세한 내용은 [작업 영역 이미지를 배포 하는 방법을](how-to-deploy-a-workspace-imageesds.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57782-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





