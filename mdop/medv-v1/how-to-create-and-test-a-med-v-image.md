---
title: MED-V 이미지를 만들고 테스트하는 방법
description: MED-V 이미지를 만들고 테스트하는 방법
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827043"
---
# <span data-ttu-id="7e6e3-103">MED-V 이미지를 만들고 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="7e6e3-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="7e6e3-104">MED-V 관리자가 med-v 이미지를 업로드 한 후에는 MED-V 작업 영역과 연결 하 고 웹을 통해 클라이언트에 배포 하거나 MED-V 패키지에 추가 하거나 타사 시스템을 사용 하 여 클라이언트에 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="7e6e3-105">먼저 테스트 이미지를 만들고이를 배포 하기 전에 MED-V 클라이언트에서 테스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="7e6e3-106">MED-V 이미지를 만들 때 다음 단계를 거칩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="7e6e3-107">**로컬 테스트 이미지**-로컬에서 테스트할 수 있는 기본 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="7e6e3-108">**로컬 압축 이미지**-이미지를 테스트 한 후에는 테스트 하기 전에 있던 이미지가 압축 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="7e6e3-109">테스트 중에 발생 한 변경 내용은 압축 된 이미지에 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="7e6e3-110">**서버에서 압축 한 이미지**-압축 된 이미지가 서버에 업로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="7e6e3-111">MED-V 테스트 이미지를 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="7e6e3-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="7e6e3-112">새 MED-V 테스트 이미지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="7e6e3-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="7e6e3-113">**이미지** 관리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="7e6e3-114">**이미지** 모듈을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="7e6e3-115">**Images** 모듈은 다음 창으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="7e6e3-116">**로컬 테스트 이미지**-로컬의 압축을 푼 이미지</span><span class="sxs-lookup"><span data-stu-id="7e6e3-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="7e6e3-117">로컬 **압축 이미지**-로컬 컴퓨터에 압축 된 모든 이미지</span><span class="sxs-lookup"><span data-stu-id="7e6e3-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="7e6e3-118">**서버에 압축 된 이미지**-압축 되어 서버에 업로드 한 모든 이미지</span><span class="sxs-lookup"><span data-stu-id="7e6e3-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="7e6e3-119">서버 창의 **로컬 압축 이미지** 및 **압축 된 이미지** 에서 각 이미지의 최신 버전이 부모 노드로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="7e6e3-120">부모 노드를 클릭 하 여 다른 모든 기존 버전의 이미지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="7e6e3-121">**로컬 테스트 이미지** 창에서 **새로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="7e6e3-122">**테스트 이미지 만들기** 대화 상자에서 다음 중 하나를 수행 하 여 med-v 테스트 이미지로 구성 하려는 가상 컴퓨터 이미지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="7e6e3-123">**기본 이미지** 파일 필드에 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="7e6e3-124">**찾아보기를** 클릭 하 여 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="7e6e3-125">**이미지 이름** 필드에서 원하는 이름을 입력 하거나 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="7e6e3-126">**참고**  Image 이름에는 다음 문자를 포함할 수 없습니다: space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="7e6e3-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="7e6e3-127">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-127">Click **OK**.</span></span>

    <span data-ttu-id="7e6e3-128">다음 표에 정의 된 속성을 사용 하 여 호스트 컴퓨터에 새 MED-V 테스트 이미지가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="7e6e3-129">MED-V 작업 영역 이미지를 구성 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 정책 구성을](configuring-med-v-workspace-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="7e6e3-130">로컬 테스트 이미지 속성</span><span class="sxs-lookup"><span data-stu-id="7e6e3-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7e6e3-131">속성</span><span class="sxs-lookup"><span data-stu-id="7e6e3-131">Property</span></span></th>
<th align="left"><span data-ttu-id="7e6e3-132">설명</span><span class="sxs-lookup"><span data-stu-id="7e6e3-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e6e3-133">이미지 이름</span><span class="sxs-lookup"><span data-stu-id="7e6e3-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6e3-134">관리자가 이미지를 만들었을 때 정의 된 테스트 이미지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e6e3-135">이미지 경로</span><span class="sxs-lookup"><span data-stu-id="7e6e3-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6e3-136">테스트 이미지의 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e6e3-137">만들어져야</span><span class="sxs-lookup"><span data-stu-id="7e6e3-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6e3-138">테스트 이미지를 만든 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7e6e3-139">MED-V 클라이언트에서 MED-V 이미지를 테스트 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7e6e3-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="7e6e3-140">MED-V 테스트 이미지를 만든 후 다음 절차를 사용 하 여 이미지를 로컬로 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="7e6e3-141">MED-V 이미지를 테스트 하려면</span><span class="sxs-lookup"><span data-stu-id="7e6e3-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="7e6e3-142">**정책** 관리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="7e6e3-143">**정책** 모듈에서 다음 작업을 수행 하 여 med-v 테스트 이미지를 med-v 작업 영역에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="7e6e3-144">**가상 컴퓨터** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="7e6e3-145">할당 된 **이미지** 필드에서 직접 만든 med-v 테스트 이미지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="7e6e3-146">테스트 이미지가 목록에 없으면 **새로 고침**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="7e6e3-147">도구 모음에서 **변경 내용 저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="7e6e3-148">다른 MED-V 작업 영역 설정을 테스트 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="7e6e3-149">자세한 내용은 [Med-v 작업 영역 정책 구성을](configuring-med-v-workspace-policies.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="7e6e3-150">MED-V 클라이언트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="7e6e3-151">**테스트 실행 확인** 상자에서 **테스트 이미지 사용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="7e6e3-152">MED-V 작업 영역 테스트 이미지를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="7e6e3-153">MED-V 클라이언트를 시작 하 고 실행 하는 방법에 대 한 자세한 내용은 [Med-v 클라이언트 작업](med-v-client-operations.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="7e6e3-154">**참고**  이미지를 테스트 하는 동안 VPC를 열고 이미지를 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="7e6e3-155">**참고**  이미지를 테스트 하는 경우 세션 간에 이미지에 변경 내용이 저장 되지 않습니다. 대신 별도의 임시 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="7e6e3-156">이는 이미지가 프로덕션 환경에서 압축 및 실행 될 때 깨끗 한 원본 이미지입니다.</span><span class="sxs-lookup"><span data-stu-id="7e6e3-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="7e6e3-157">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7e6e3-157">Related topics</span></span>


[<span data-ttu-id="7e6e3-158">MED-V에 대한 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="7e6e3-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="7e6e3-159">MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="7e6e3-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="7e6e3-160">MED-V 작업 영역 정책 구성</span><span class="sxs-lookup"><span data-stu-id="7e6e3-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="7e6e3-161">MED-V 클라이언트 작업</span><span class="sxs-lookup"><span data-stu-id="7e6e3-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





