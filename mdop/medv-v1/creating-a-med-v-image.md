---
title: MED-V 이미지 만들기
description: MED-V 이미지 만들기
author: dansimp
ms.assetid: 7cbbcd22-83f5-4b60-825f-781b4c6a2d36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de1c2cd87d85bbe2fc40b9007eba8f86d2ed6f60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812500"
---
# <span data-ttu-id="1d623-103">MED-V 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="1d623-103">Creating a MED-V Image</span></span>


## <span data-ttu-id="1d623-104">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="1d623-104">In This Section</span></span>


<span data-ttu-id="1d623-105">이 섹션에서는 MED-V 클라이언트와 MED-V 관리 응용 프로그램이 설치 되어 있는 컴퓨터에서 MED-V 이미지를 구성 하는 방법에 대해 설명 하 고 다음에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-105">This section describes how to configure a MED-V image on a computer on which the MED-V client and MED-V management application are installed, and explains the following:</span></span>

<a href="" id="how-to-create-and-test-a-med-v-image"></a>[<span data-ttu-id="1d623-106">MED-V 이미지를 만들고 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d623-106">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)  
<span data-ttu-id="1d623-107">MED-V 이미지를 만든 다음 로컬로 이미지를 테스트 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-107">Describes how to create a MED-V image, and then test the image locally.</span></span>

<a href="" id="how-to-pack-a-med-v-image"></a>[<span data-ttu-id="1d623-108">MED-V 이미지를 압축하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d623-108">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)  
<span data-ttu-id="1d623-109">배포 패키지에 추가 하거나 서버로 업로드할 수 있도록 MED-V 이미지를 압축 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-109">Describes how to pack a MED-V image so that it can be added to a deployment package or uploaded to the server.</span></span>

<a href="" id="how-to-upload-a-med-v-image-to-the-server"></a>[<span data-ttu-id="1d623-110">서버에 MED-V 이미지를 업로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d623-110">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)  
<span data-ttu-id="1d623-111">MED-V 이미지를 서버에 업로드 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-111">Describes how to upload a MED-V image to the server.</span></span>

<a href="" id="how-to-localize-a-med-v-image"></a>[<span data-ttu-id="1d623-112">MED-V 이미지를 지역화하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d623-112">How to Localize a MED-V Image</span></span>](how-to-localize-a-med-v-image.md)  
<span data-ttu-id="1d623-113">이미지의 압축을 풀고 다운로드 하 여 MED-V 이미지를 지역화 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-113">Describes how to localize a MED-V image either through extracting or downloading the image.</span></span>

<a href="" id="how-to-update-a-med-v-image"></a>[<span data-ttu-id="1d623-114">MED-V 이미지를 업데이트하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d623-114">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)  
<span data-ttu-id="1d623-115">MED-V 이미지를 업데이트 하 여 새 버전의 이미지를 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-115">Describes how to update a MED-V image to create a new version of the image.</span></span>

<a href="" id="how-to-delete-a-med-v-image"></a>[<span data-ttu-id="1d623-116">MED-V 이미지를 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="1d623-116">How to Delete a MED-V Image</span></span>](how-to-delete-a-med-v-image.md)  
<span data-ttu-id="1d623-117">MED-V 이미지를 삭제 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-117">Describes how to delete a MED-V image.</span></span>

<span data-ttu-id="1d623-118">**참고**  MED-V 이미지를 구성한 후에는 클라이언트가 MED-V 작업 영역 설정의 일부로 클라이언트에 대 한 도메인 연결 절차를 배포 후에 수행 해야 하기 때문에 컴퓨터가 도메인에 속해 있지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d623-118">**Note** After the MED-V image is configured, the computer should not be part of a domain because the join domain procedure should be performed on the client after the deployment, as part of the MED-V workspace setup.</span></span>

 

 

 





