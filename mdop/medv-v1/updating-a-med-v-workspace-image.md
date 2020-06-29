---
title: MED-V 작업 영역 이미지 업데이트
description: MED-V 작업 영역 이미지 업데이트
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825853"
---
# <span data-ttu-id="1651e-103">MED-V 작업 영역 이미지 업데이트</span><span class="sxs-lookup"><span data-stu-id="1651e-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="1651e-104">이미지는 다음 방법 중 하나로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="1651e-105">엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 업데이트를 게스트 운영 체제에 밀어넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="1651e-106">업데이트를 이미지 웹 배포 서버에 업로드 한 다음 클라이언트에서 다운로드 하 고 MED-V 이미지에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="1651e-107">MED-V 기본 이미지는 업데이트 및 다시 배포 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="1651e-108">엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MED-V 이미지를 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1651e-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="1651e-109">엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 MED-V 이미지를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="1651e-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="1651e-110">사용 중인 시스템의 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1651e-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="1651e-111">웹 다운로드를 사용 하 여 MED-V 이미지를 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1651e-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="1651e-112">웹 다운로드를 사용 하 여 MED-V 이미지를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="1651e-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="1651e-113">MED-V 관리의 **가상 컴퓨터** 탭에서 다음 설정이 업데이트 되는 med-v 이미지와 연결 된 med-v 작업 영역 정책에 적용 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="1651e-114">**새 버전을 사용할 수 있을 때 업데이트 제안** 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="1651e-115">필요에 따라 **클라이언트가이 작업 영역의 이미지를 다운로드 하는 동안 트리밍 전송 사용** 확인란을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="1651e-116">자세한 내용은 [Med-v 작업 영역에 가상 컴퓨터 설정을 적용 하는 방법을](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1651e-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="1651e-117">이미지 업데이트를 이미지 웹 배포 서버에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="1651e-118">업데이트 해야 하는 이미지가 포함 된 모든 클라이언트는 자동으로 업데이트를 다운로드 하 여 이미지에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="1651e-119">MED-V 기본 이미지를 업데이트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1651e-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="1651e-120">MED-V 기본 이미지를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="1651e-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="1651e-121">가상 PC2007에서 기존 이미지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="1651e-122">이미지를 필요한 대로 변경 하 고 이미지 (예: 새 소프트웨어 설치)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="1651e-123">가상 PC2007을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="1651e-124">이미지를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-124">Test the image.</span></span>

5.  <span data-ttu-id="1651e-125">이미지를 테스트 한 후 기존 이미지와 동일한 이름을 사용 하 여 로컬 저장소에 압축 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="1651e-126">**참고**  기존 버전과 다른 이름으로 이미지 이름을 지정할 경우 기존 이미지의 새 버전이 아닌 새 이미지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="1651e-127">서버에 새 버전을 업로드 하 고 이미지 준비 단계 폴더로 푸시 하거나 배포 패키지를 통해 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="1651e-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="1651e-128">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1651e-128">Related topics</span></span>


[<span data-ttu-id="1651e-129">MED-V 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="1651e-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="1651e-130">MED-V 이미지를 업데이트하는 방법</span><span class="sxs-lookup"><span data-stu-id="1651e-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="1651e-131">MED-V 작업 영역 정책 구성</span><span class="sxs-lookup"><span data-stu-id="1651e-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="1651e-132">이미지 웹 배포 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="1651e-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





