---
title: 응용 프로그램 가상화 시퀀싱 마법사 고급 옵션 페이지
description: 응용 프로그램 가상화 시퀀싱 마법사 고급 옵션 페이지
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819598"
---
# <span data-ttu-id="b2eb5-103">응용 프로그램 가상화 시퀀싱 마법사 고급 옵션 페이지</span><span class="sxs-lookup"><span data-stu-id="b2eb5-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="b2eb5-104">Application Virtualization (App-v) 시퀀싱 마법사의 **고급 옵션** 페이지를 사용 하 여 설치할 응용 프로그램에 대 한 고급 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="b2eb5-105">이 페이지에는 다음 표에 설명 된 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b2eb5-106">이름</span><span class="sxs-lookup"><span data-stu-id="b2eb5-106">Name</span></span></th>
<th align="left"><span data-ttu-id="b2eb5-107">설명</span><span class="sxs-lookup"><span data-stu-id="b2eb5-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b2eb5-108">블록 크기</span><span class="sxs-lookup"><span data-stu-id="b2eb5-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-109">네트워크 상에 서 SFT 파일을 스트리밍할 때 나눌 블록의 크기를 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="b2eb5-110">모든 블록은 지정 된 크기와 동일 합니다. 그러나 마지막 블록이 지정 된 것 보다 작을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="b2eb5-111">다음 값 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="b2eb5-112">4KB</span><span class="sxs-lookup"><span data-stu-id="b2eb5-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="b2eb5-113">16kb</span><span class="sxs-lookup"><span data-stu-id="b2eb5-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="b2eb5-114">32 KB</span><span class="sxs-lookup"><span data-stu-id="b2eb5-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="b2eb5-115">64 KB</span><span class="sxs-lookup"><span data-stu-id="b2eb5-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="b2eb5-116">참고</span><span class="sxs-lookup"><span data-stu-id="b2eb5-116">Note</span></span></strong><br/><p><span data-ttu-id="b2eb5-117">블록 크기를 선택 하는 경우 SFT 파일과 네트워크 대역폭의 크기를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="b2eb5-118">더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="b2eb5-119">블록 크기가 더 많은 파일은 스트리밍할 수 있지만 더 많은 네트워크 대역폭을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="b2eb5-120">실험을 통해 네트워크의 스트리밍 응용 프로그램에 대 한 최적의 블록 크기를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b2eb5-121">모니터링 중 Microsoft Update 사용</span><span class="sxs-lookup"><span data-stu-id="b2eb5-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-122">시퀀싱 마법사&#39;s 모니터링 단계 중에 Microsoft 업데이트를 설치할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b2eb5-123">Dll 다시 기준 다시 하기</span><span class="sxs-lookup"><span data-stu-id="b2eb5-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-124">지원 되는 동적 연결 라이브러리를 RAM의 연속 공간으로 다시 매핑하는 데 사용할 수 있도록 하 여 메모리를 절약 하 고 성능을 개선 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b2eb5-125">Back</span><span class="sxs-lookup"><span data-stu-id="b2eb5-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-126">시퀀싱 마법사&#39;s 이전 페이지에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b2eb5-127">Next</span><span class="sxs-lookup"><span data-stu-id="b2eb5-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-128">시퀀싱 마법사&#39;s 다음 페이지에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b2eb5-129">취소</span><span class="sxs-lookup"><span data-stu-id="b2eb5-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-130">시퀀싱 마법사의 작업을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b2eb5-131">\ [Template 토큰 값 \]</span><span class="sxs-lookup"><span data-stu-id="b2eb5-131">\[Template Token Value\]</span></span>

<span data-ttu-id="b2eb5-132">앱-V 시퀀싱 마법사의 **고급 옵션** 페이지를 사용 하 여 시퀀싱 하는 응용 프로그램의 고급 옵션을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="b2eb5-133">이 페이지에는 다음 표에 설명 된 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b2eb5-134">이름</span><span class="sxs-lookup"><span data-stu-id="b2eb5-134">Name</span></span></th>
<th align="left"><span data-ttu-id="b2eb5-135">설명</span><span class="sxs-lookup"><span data-stu-id="b2eb5-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b2eb5-136">모니터링 중 Microsoft Update 실행 허용</span><span class="sxs-lookup"><span data-stu-id="b2eb5-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-137">응용 프로그램 시퀀싱 중 모니터링 단계에서 소프트웨어 업데이트를 응용 프로그램에 적용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="b2eb5-138">이 옵션은 응용 프로그램 설치를 성공적으로 완료 하기 위해 업데이트가 필요한 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="b2eb5-139">이 옵션은 기본적으로 선택 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b2eb5-140">Dll 다시 기준 다시 하기</span><span class="sxs-lookup"><span data-stu-id="b2eb5-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-141">지원 되는 동적 연결 라이브러리를 RAM의 연속 공간으로 다시 매핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="b2eb5-142">이 옵션을 선택 하면 메모리를 관리 하 고 응용 프로그램 성능을 향상 시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="b2eb5-143">이 옵션은 기본적으로 선택 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b2eb5-144">Back</span><span class="sxs-lookup"><span data-stu-id="b2eb5-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-145">마법사의 이전 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b2eb5-146">Next</span><span class="sxs-lookup"><span data-stu-id="b2eb5-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-147">마법사의 다음 페이지로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b2eb5-148">취소</span><span class="sxs-lookup"><span data-stu-id="b2eb5-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b2eb5-149">설정을 취소 하 고 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b2eb5-150">\ [Template 토큰 값 \]</span><span class="sxs-lookup"><span data-stu-id="b2eb5-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="b2eb5-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b2eb5-151">Related topics</span></span>


[<span data-ttu-id="b2eb5-152">시퀀싱 마법사</span><span class="sxs-lookup"><span data-stu-id="b2eb5-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









