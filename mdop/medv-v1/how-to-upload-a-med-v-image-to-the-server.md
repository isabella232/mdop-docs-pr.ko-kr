---
title: 서버에 MED-V 이미지를 업로드하는 방법
description: 서버에 MED-V 이미지를 업로드하는 방법
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825703"
---
# <span data-ttu-id="2cbb5-103">서버에 MED-V 이미지를 업로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="2cbb5-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="2cbb5-104">MED-V 이미지를 테스트 한 후에 압축 한 다음 서버로 업로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="2cbb5-105">이미지 웹 배포 서버를 구성 하는 방법에 대 한 자세한 내용은 [이미지 웹 배포 서버를 구성 하는 방법을](how-to-configure-the-image-web-distribution-server.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="2cbb5-106">MED-V 이미지를 압축 하 여 서버에 업로드 한 후에는 엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 사용자에 게 배포 하거나 배포 패키지를 사용 하 여 사용자가 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="2cbb5-107">엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 배포 하는 방법에 대 한 자세한 내용은 [엔터프라이즈 소프트웨어 배포 시스템을 사용 하 여 Med-v 작업 영역 배포](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="2cbb5-108">패키지를 사용 하 여 배포 하는 방법에 대 한 자세한 내용은 [배포 패키지를 사용 하 여 Med-v 작업 영역 배포](deploying-a-med-v-workspace-using-a-deployment-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="2cbb5-109">참고</span><span class="sxs-lookup"><span data-stu-id="2cbb5-109">Note</span></span>**  
<span data-ttu-id="2cbb5-110">이미지를 업로드 하기 전에 브라우저 설정에 웹 프록시가 정의 되어 있지 않으며 Windows 업데이트가 현재 실행 되 고 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="2cbb5-111">서버에 MED-V 이미지를 업로드 하려면</span><span class="sxs-lookup"><span data-stu-id="2cbb5-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="2cbb5-112">**로컬 압축 이미지** 창에서 만든 이미지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="2cbb5-113">**업로드**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-113">Click **Upload**.</span></span>

    <span data-ttu-id="2cbb5-114">이미지가 서버에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-114">The image is uploaded to the server.</span></span> <span data-ttu-id="2cbb5-115">이는 시간이 오래 걸릴 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="2cbb5-116">서버에 있는 이미지는 다음 표에 나열 된 속성을 사용 하 여 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="2cbb5-117">서버 속성에 압축 된 이미지</span><span class="sxs-lookup"><span data-stu-id="2cbb5-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2cbb5-118">속성</span><span class="sxs-lookup"><span data-stu-id="2cbb5-118">Property</span></span></th>
<th align="left"><span data-ttu-id="2cbb5-119">설명</span><span class="sxs-lookup"><span data-stu-id="2cbb5-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb5-120">이미지 이름</span><span class="sxs-lookup"><span data-stu-id="2cbb5-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb5-121">관리자가 이미지를 만들었을 때 정의 된 압축 이미지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb5-122">버전</span><span class="sxs-lookup"><span data-stu-id="2cbb5-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb5-123">표시 된 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2cbb5-124">참고</span><span class="sxs-lookup"><span data-stu-id="2cbb5-124">Note</span></span></strong><br/><p><span data-ttu-id="2cbb5-125">이전 버전은 삭제 되지 않는 한 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cbb5-126">파일 크기 (압축)</span><span class="sxs-lookup"><span data-stu-id="2cbb5-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb5-127">이미지의 실제 압축 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cbb5-128">이미지 크기 (압축 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="2cbb5-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cbb5-129">물리적으로 압축 되지 않은 이미지 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="2cbb5-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2cbb5-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2cbb5-130">Related topics</span></span>


[<span data-ttu-id="2cbb5-131">MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="2cbb5-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="2cbb5-132">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="2cbb5-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="2cbb5-133">MED-V에 대한 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="2cbb5-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="2cbb5-134">MED-V 이미지를 압축하는 방법</span><span class="sxs-lookup"><span data-stu-id="2cbb5-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









