---
title: App-V 패키지 WMI 클래스
description: App-V 패키지 WMI 클래스
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819798"
---
# <span data-ttu-id="a3e77-103">App-V 패키지 WMI 클래스</span><span class="sxs-lookup"><span data-stu-id="a3e77-103">App-V Package WMI Class</span></span>


<span data-ttu-id="a3e77-104">Application Virtualization (App-v) 클라이언트에서 **Package** 클래스는 클라이언트의 모든 가상 패키지를 나타내는 WMI (Windows Management Instrumentation) 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="a3e77-105">가상 패키지에는 여러 가상 응용 프로그램이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="a3e77-106">구문</span><span class="sxs-lookup"><span data-stu-id="a3e77-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="a3e77-107">특성</span><span class="sxs-lookup"><span data-stu-id="a3e77-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="a3e77-108">이름</span><span class="sxs-lookup"><span data-stu-id="a3e77-108">Name</span></span>**  
<span data-ttu-id="a3e77-109">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="a3e77-109">Data type: **String**</span></span>

<span data-ttu-id="a3e77-110">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-110">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-111">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-111">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-112">사용자에 게 친숙 한 가상 패키지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="a3e77-113">버전</span><span class="sxs-lookup"><span data-stu-id="a3e77-113">Version</span></span>**  
<span data-ttu-id="a3e77-114">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="a3e77-114">Data type: **String**</span></span>

<span data-ttu-id="a3e77-115">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-115">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-116">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-116">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-117">가상 패키지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="a3e77-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="a3e77-118">PackageGUID</span></span>**  
<span data-ttu-id="a3e77-119">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="a3e77-119">Data type: **String**</span></span>

<span data-ttu-id="a3e77-120">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-120">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-121">한정자: 키</span><span class="sxs-lookup"><span data-stu-id="a3e77-121">Qualifiers: Key</span></span>

<span data-ttu-id="a3e77-122">패키지 구성 및 원본 파일의 GUID 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="a3e77-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="a3e77-123">SftPath</span></span>**  
<span data-ttu-id="a3e77-124">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="a3e77-124">Data type: **String**</span></span>

<span data-ttu-id="a3e77-125">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-125">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-126">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-126">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-127">SFT 파일의 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="a3e77-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="a3e77-128">TotalSize</span></span>**  
<span data-ttu-id="a3e77-129">데이터 형식: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3e77-129">Data type: **UInt64**</span></span>

<span data-ttu-id="a3e77-130">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-130">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-131">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-131">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-132">가상 패키지의 총 크기 (kb)입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="a3e77-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="a3e77-133">CachedSize</span></span>**  
<span data-ttu-id="a3e77-134">데이터 형식: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3e77-134">Data type: **UInt64**</span></span>

<span data-ttu-id="a3e77-135">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-135">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-136">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-136">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-137">가상 패키지에 대 한 캐시의 총 크기 (kb)입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="a3e77-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="a3e77-138">LaunchSize</span></span>**  
<span data-ttu-id="a3e77-139">데이터 형식: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3e77-139">Data type: **UInt64**</span></span>

<span data-ttu-id="a3e77-140">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-140">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-141">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-141">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-142">가상 패키지의 기본 기능 블록의 총 크기 (kb)입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="a3e77-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="a3e77-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="a3e77-144">데이터 형식: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3e77-144">Data type: **UInt64**</span></span>

<span data-ttu-id="a3e77-145">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-145">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-146">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-146">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-147">캐시 된 가상 패키지의 기본 기능 블록의 총 크기 (kb)입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="a3e77-148">InUse</span><span class="sxs-lookup"><span data-stu-id="a3e77-148">InUse</span></span>**  
<span data-ttu-id="a3e77-149">데이터 형식: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3e77-149">Data type: **Boolean**</span></span>

<span data-ttu-id="a3e77-150">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-150">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-151">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-151">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-152">가상 패키지의 가상 응용 프로그램이 실행 되 고 있으면 **true** 이 고, 그렇지 않으면 false입니다. 그렇지 않으면 **false**입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="a3e77-153">잠김</span><span class="sxs-lookup"><span data-stu-id="a3e77-153">Locked</span></span>**  
<span data-ttu-id="a3e77-154">데이터 형식: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3e77-154">Data type: **Boolean**</span></span>

<span data-ttu-id="a3e77-155">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-155">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-156">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-156">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-157">가상 패키지가 잠겨 있으면 **true** 이 고, 그렇지 않으면 false입니다. 그렇지 않으면 **false**입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="a3e77-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="a3e77-158">CachedPercentage</span></span>**  
<span data-ttu-id="a3e77-159">데이터 형식: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3e77-159">Data type: **UInt16**</span></span>

<span data-ttu-id="a3e77-160">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-160">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-161">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-161">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-162">캐시 파일의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-162">The percentage of the cache files.</span></span> <span data-ttu-id="a3e77-163">다음 공식을 기준으로 합니다. CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="a3e77-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="a3e77-164">버전 Guid</span><span class="sxs-lookup"><span data-stu-id="a3e77-164">VersionGUID</span></span>**  
<span data-ttu-id="a3e77-165">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="a3e77-165">Data type: **String**</span></span>

<span data-ttu-id="a3e77-166">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="a3e77-166">Access type: Read-only</span></span>

<span data-ttu-id="a3e77-167">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="a3e77-167">Qualifiers: None</span></span>

<span data-ttu-id="a3e77-168">패키지 버전의 GUID 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a3e77-168">The GUID identifier of the package version.</span></span>

 

 





