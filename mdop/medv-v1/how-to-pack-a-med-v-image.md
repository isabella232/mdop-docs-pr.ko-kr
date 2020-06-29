---
title: MED-V 이미지를 압축하는 방법
description: MED-V 이미지를 압축하는 방법
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824678"
---
# <span data-ttu-id="1bc96-103">MED-V 이미지를 압축하는 방법</span><span class="sxs-lookup"><span data-stu-id="1bc96-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="1bc96-104">MED-V 이미지를 배포 패키지에 추가 하거나 서버에 업로드 하기 전에 먼저 압축 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="1bc96-105">압축 된 MED-V 이미지를 만들려면</span><span class="sxs-lookup"><span data-stu-id="1bc96-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="1bc96-106">**이미지** 관리 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="1bc96-107">**이미지** 모듈의 **로컬 압축 이미지** 창에서 **새로 만들기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="1bc96-108">압축 된 **이미지 만들기** 대화 상자에서 다음 중 하나를 수행 하 여 가상 컴퓨터 이미지를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="1bc96-109">**기본 이미지 파일** 필드에 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리의 전체 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="1bc96-110">**찾아보기를** 클릭 하 여 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="1bc96-111">다음 중 하나를 수행 하 여 새 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="1bc96-112">**이미지 이름** 필드에 원하는 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="1bc96-113">참고</span><span class="sxs-lookup"><span data-stu-id="1bc96-113">Note</span></span>**  
        <span data-ttu-id="1bc96-114">Image 이름에는 다음 문자를 포함할 수 없습니다: space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="1bc96-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="1bc96-115">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-115">Click **OK**.</span></span>

   <span data-ttu-id="1bc96-116">다음 표에 정의 된 속성을 사용 하 여 호스트 컴퓨터에 새 MED-V 압축 이미지가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="1bc96-117">참고</span><span class="sxs-lookup"><span data-stu-id="1bc96-117">Note</span></span>**  
<span data-ttu-id="1bc96-118">서버 창의 **로컬 압축 이미지** 및 **압축 된 이미지** 에서 각 이미지의 최신 버전이 부모 노드로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="1bc96-119">부모 노드를 클릭 하 여 다른 모든 기존 버전의 이미지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="1bc96-120">로컬 압축 이미지 속성</span><span class="sxs-lookup"><span data-stu-id="1bc96-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1bc96-121">속성</span><span class="sxs-lookup"><span data-stu-id="1bc96-121">Property</span></span></th>
<th align="left"><span data-ttu-id="1bc96-122">설명</span><span class="sxs-lookup"><span data-stu-id="1bc96-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc96-123">이미지 이름</span><span class="sxs-lookup"><span data-stu-id="1bc96-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc96-124">관리자가 이미지를 만들었을 때 정의 된 압축 이미지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc96-125">버전</span><span class="sxs-lookup"><span data-stu-id="1bc96-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc96-126">표시 된 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1bc96-127">참고</span><span class="sxs-lookup"><span data-stu-id="1bc96-127">Note</span></span></strong><br/><p><span data-ttu-id="1bc96-128">이전 버전은 삭제 되지 않는 한 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1bc96-129">파일 크기 (압축)</span><span class="sxs-lookup"><span data-stu-id="1bc96-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc96-130">이미지의 실제 압축 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1bc96-131">이미지 크기 (압축 되지 않음)</span><span class="sxs-lookup"><span data-stu-id="1bc96-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1bc96-132">물리적으로 압축 되지 않은 이미지 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="1bc96-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="1bc96-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1bc96-133">Related topics</span></span>


[<span data-ttu-id="1bc96-134">MED-V 클라이언트 및 MED-V 관리 콘솔을 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="1bc96-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="1bc96-135">MED-V 관리 콘솔 사용자 인터페이스 사용</span><span class="sxs-lookup"><span data-stu-id="1bc96-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="1bc96-136">MED-V에 대한 가상 PC 이미지 만들기</span><span class="sxs-lookup"><span data-stu-id="1bc96-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









