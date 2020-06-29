---
title: MED-V 이미지를 업데이트하는 방법
description: MED-V 이미지를 업데이트하는 방법
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812497"
---
# <span data-ttu-id="6dcb8-103">MED-V 이미지를 업데이트하는 방법</span><span class="sxs-lookup"><span data-stu-id="6dcb8-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="6dcb8-104">MED-V 이미지를 업데이트하는 방법</span><span class="sxs-lookup"><span data-stu-id="6dcb8-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="6dcb8-105">기존 MED-V 이미지를 업데이트 하 여 새 버전의 이미지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="6dcb8-106">그런 다음 새 버전을 클라이언트 컴퓨터에 배포 하 여 기존 이미지를 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="6dcb8-107">**참고**  새 버전이 클라이언트에 배포 되 면 기존 이미지를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="6dcb8-108">이미지를 업데이트 하는 경우 클라이언트에 저장 해야 할 데이터가 없는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="6dcb8-109">MED-V 이미지를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="6dcb8-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="6dcb8-110">가상 PC2007에서 기존 이미지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="6dcb8-111">이미지를 필요한 대로 변경 하 고 이미지 (예: 새 소프트웨어 설치)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="6dcb8-112">가상 PC2007을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="6dcb8-113">이미지를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-113">Test the image.</span></span>

5.  <span data-ttu-id="6dcb8-114">이미지를 테스트 한 후 기존 이미지와 동일한 이름을 사용 하 여 로컬 저장소에 압축 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="6dcb8-115">**참고**  기존 버전과 다른 이름으로 이미지 이름을 지정할 경우 기존 이미지의 새 버전이 아닌 새 이미지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="6dcb8-116">서버에 새 버전을 업로드 하거나 배포 패키지를 통해 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="6dcb8-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="6dcb8-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6dcb8-117">Related topics</span></span>


[<span data-ttu-id="6dcb8-118">MED-V에 대한 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="6dcb8-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="6dcb8-119">MED-V 이미지를 만들고 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="6dcb8-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="6dcb8-120">MED-V 이미지를 압축하는 방법</span><span class="sxs-lookup"><span data-stu-id="6dcb8-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="6dcb8-121">서버에 MED-V 이미지를 업로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="6dcb8-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="6dcb8-122">MED-V 작업 영역 이미지 업데이트</span><span class="sxs-lookup"><span data-stu-id="6dcb8-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





