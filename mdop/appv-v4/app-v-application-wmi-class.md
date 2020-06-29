---
title: App-V 응용 프로그램 WMI 클래스
description: App-V 응용 프로그램 WMI 클래스
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822323"
---
# <span data-ttu-id="d40c8-103">App-V 응용 프로그램 WMI 클래스</span><span class="sxs-lookup"><span data-stu-id="d40c8-103">App-V Application WMI Class</span></span>


<span data-ttu-id="d40c8-104">Application Virtualization (App-v) 클라이언트에서 **응용 프로그램** 클래스는 클라이언트의 모든 가상 응용 프로그램을 나타내는 WMI (Windows Management Instrumentation) 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="d40c8-105">다음 구문은 MOF (관리 개체 형식) 코드에서 간소화 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="d40c8-106">코드에는 상속 된 속성이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="d40c8-107">구문</span><span class="sxs-lookup"><span data-stu-id="d40c8-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="d40c8-108">요구 사항</span><span class="sxs-lookup"><span data-stu-id="d40c8-108">Requirements</span></span>


## <span data-ttu-id="d40c8-109">특성</span><span class="sxs-lookup"><span data-stu-id="d40c8-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="d40c8-110">이름</span><span class="sxs-lookup"><span data-stu-id="d40c8-110">Name</span></span>**  
<span data-ttu-id="d40c8-111">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="d40c8-111">Data type: **String**</span></span>

<span data-ttu-id="d40c8-112">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-112">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-113">한정자: 키</span><span class="sxs-lookup"><span data-stu-id="d40c8-113">Qualifiers: Key</span></span>

<span data-ttu-id="d40c8-114">가상 응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="d40c8-115">버전</span><span class="sxs-lookup"><span data-stu-id="d40c8-115">Version</span></span>**  
<span data-ttu-id="d40c8-116">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="d40c8-116">Data type: **String**</span></span>

<span data-ttu-id="d40c8-117">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-117">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-118">한정자: 키</span><span class="sxs-lookup"><span data-stu-id="d40c8-118">Qualifiers: Key</span></span>

<span data-ttu-id="d40c8-119">가상 응용 프로그램의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="d40c8-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="d40c8-120">PackageGUID</span></span>**  
<span data-ttu-id="d40c8-121">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="d40c8-121">Data type: **String**</span></span>

<span data-ttu-id="d40c8-122">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-122">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-123">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="d40c8-123">Qualifiers: None</span></span>

<span data-ttu-id="d40c8-124">가상 응용 프로그램이 연결 된 패키지의 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="d40c8-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="d40c8-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="d40c8-126">데이터 형식: **날짜/시간**</span><span class="sxs-lookup"><span data-stu-id="d40c8-126">Data type: **DateTime**</span></span>

<span data-ttu-id="d40c8-127">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-127">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-128">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="d40c8-128">Qualifiers: None</span></span>

<span data-ttu-id="d40c8-129">가상 응용 프로그램을 마지막으로 시작한 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="d40c8-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="d40c8-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="d40c8-131">데이터 형식: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d40c8-131">Data type: **UInt32**</span></span>

<span data-ttu-id="d40c8-132">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-132">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-133">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="d40c8-133">Qualifiers: None</span></span>

<span data-ttu-id="d40c8-134">직접 시작 된 가상 응용 프로그램의 실행 중인 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="d40c8-135">불러오는 중</span><span class="sxs-lookup"><span data-stu-id="d40c8-135">Loading</span></span>**  
<span data-ttu-id="d40c8-136">데이터 형식: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d40c8-136">Data type: **Boolean**</span></span>

<span data-ttu-id="d40c8-137">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-137">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-138">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="d40c8-138">Qualifiers: None</span></span>

<span data-ttu-id="d40c8-139">가상 응용 프로그램이 시작 되는 경우 **true** 이 고, 그렇지 않으면 false입니다. 그렇지 않으면 **false**입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="d40c8-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="d40c8-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="d40c8-141">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="d40c8-141">Data type: **String**</span></span>

<span data-ttu-id="d40c8-142">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-142">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-143">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="d40c8-143">Qualifiers: None</span></span>

<span data-ttu-id="d40c8-144">App-v 클라이언트에 등록 된 OSD 파일의 원래 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="d40c8-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="d40c8-145">CachedOsdPath</span></span>**  
<span data-ttu-id="d40c8-146">데이터 형식: **문자열**</span><span class="sxs-lookup"><span data-stu-id="d40c8-146">Data type: **String**</span></span>

<span data-ttu-id="d40c8-147">Access 형식: 읽기 전용</span><span class="sxs-lookup"><span data-stu-id="d40c8-147">Access type: Read-only</span></span>

<span data-ttu-id="d40c8-148">한정자: 없음</span><span class="sxs-lookup"><span data-stu-id="d40c8-148">Qualifiers: None</span></span>

<span data-ttu-id="d40c8-149">App-v 클라이언트가 OSD 파일을 로컬로 캐시 한 경우 OSD 파일의 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d40c8-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





