---
title: 가상 응용 프로그램 패키지를 편집하거나 업그레이드할지 여부를 결정하는 방법
description: 가상 응용 프로그램 패키지를 편집하거나 업그레이드할지 여부를 결정하는 방법
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817503"
---
# <span data-ttu-id="cdd82-103">가상 응용 프로그램 패키지를 편집하거나 업그레이드할지 여부를 결정하는 방법</span><span class="sxs-lookup"><span data-stu-id="cdd82-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="cdd82-104">다음 표를 사용 하 여 가상 응용 프로그램 패키지를 편집용으로 열 수 있는지 여부, 패키지의 새 버전을 만들어야 하는지 여부 또는 App-v Sequencer를 사용 하 여 어떤 옵션을 사용할 수 있는지 여부를 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cdd82-105">작업</span><span class="sxs-lookup"><span data-stu-id="cdd82-105">Action</span></span></th>
<th align="left"><span data-ttu-id="cdd82-106">편집용으로 열기</span><span class="sxs-lookup"><span data-stu-id="cdd82-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="cdd82-107">업그레이드를 위해 열기</span><span class="sxs-lookup"><span data-stu-id="cdd82-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-108">패키지 속성 보기.</span><span class="sxs-lookup"><span data-stu-id="cdd82-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-109">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-110">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-111">패키지 변경 내용 보기</span><span class="sxs-lookup"><span data-stu-id="cdd82-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-112">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-113">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-114">연결 된 패키지 파일을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-115">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-116">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-117">레지스트리 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-118">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-119">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-120">추가 패키지 설정 검토 (운영 체제 파일 속성 제외)</span><span class="sxs-lookup"><span data-stu-id="cdd82-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-121">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-122">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-123">관련 Windows Installer (MSI)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-124">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-125">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-126">OSD 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-127">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-128">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-129">패키지를 압축 및 압축 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-130">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-131">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-132">파일 형식 연결을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-133">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-134">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-135">바로 가기 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="cdd82-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-136">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-137">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-138">가상화 된 레지스트리 키 상태 (재정의/병합)를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-139">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-140">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-141">가상화 된 폴더 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-142">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-143">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-144">가상 파일 시스템 매핑 편집</span><span class="sxs-lookup"><span data-stu-id="cdd82-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-145">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-146">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-147">패키지에 대해 관련 된 모든 운영 체제 파일 속성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-148">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-149">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-150">다른 서비스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-151">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-152">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-153">다른 파일을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-154">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-155">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-156">연결 된 보안 설명자를 수집 하 고 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-157">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-158">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-159">보안 업데이트를 적용 하거나 새 버전으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-160">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-161">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-162">다른 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-163">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-164">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cdd82-165">응용 프로그램이 열리도록 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-166">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-167">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cdd82-168">컴퓨터를 다시 시작 해야 하는 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd82-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-169">아니오</span><span class="sxs-lookup"><span data-stu-id="cdd82-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="cdd82-170">예</span><span class="sxs-lookup"><span data-stu-id="cdd82-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="cdd82-171">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cdd82-171">Related topics</span></span>


[<span data-ttu-id="cdd82-172">기존 가상 응용 프로그램을 편집하는 방법</span><span class="sxs-lookup"><span data-stu-id="cdd82-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="cdd82-173">기존 가상 응용 프로그램을 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="cdd82-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





