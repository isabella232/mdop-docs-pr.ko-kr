---
title: UE-V 2.x용 동기화 트리거 이벤트
description: UE-V 2.x용 동기화 트리거 이벤트
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826798"
---
# <span data-ttu-id="19a42-103">UE-V 2.x용 동기화 트리거 이벤트</span><span class="sxs-lookup"><span data-stu-id="19a42-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="19a42-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1을 사용 하면 모든 도메인에 가입한 장치에서 응용 프로그램 및 Windows 설정을 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="19a42-105">*동기화 트리거 이벤트* 는 ue-v agent가 설정 저장소 위치와 이러한 설정을 동기화 하는 시점을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="19a42-106">UE-V 2에는 *Syncprovider*라는 새로운 *동기화 메서드가* 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="19a42-107">동기화 방법 구성에 대 한 자세한 내용은 [ue-v 2. x에 대 한 Sync 메서드](sync-methods-for-ue-v-2x-both-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19a42-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="19a42-108">UE-V 2 동기화 트리거 이벤트</span><span class="sxs-lookup"><span data-stu-id="19a42-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="19a42-109">다음 표에서는 클래식 응용 프로그램 및 Windows 설정의 트리거 이벤트에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a42-110">UE-V 2 트리거 이벤트</span><span class="sxs-lookup"><span data-stu-id="19a42-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="19a42-111">SyncMethod = Syncmethod</span><span class="sxs-lookup"><span data-stu-id="19a42-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="19a42-112">SyncMethod = 없음</span><span class="sxs-lookup"><span data-stu-id="19a42-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19a42-113">Windows 로그온</span><span class="sxs-lookup"><span data-stu-id="19a42-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="19a42-114">설정 저장소 위치에서 응용 프로그램 및 Windows 설정을 로컬 캐시로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="19a42-115">비동기 Windows 설정이 </a> 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="19a42-116">다음 Windows 로그온 중에 동기 Windows 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="19a42-117">응용 프로그램이 시작 되 면 응용 프로그램 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="19a42-118">설정 저장소 위치에서 직접 응용 프로그램 및 Windows 설정을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="19a42-119">비동기 및 동기 Windows 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="19a42-120">응용 프로그램이 시작 되 면 응용 프로그램 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a42-121">Windows 로그 오프</span><span class="sxs-lookup"><span data-stu-id="19a42-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a42-122">로컬에서 변경 내용을 저장 하 고 비동기 및 동기 Windows 설정을 설정 저장소 위치 서버 (사용 가능한 경우)에 캐시 하 고 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="19a42-123">비동기 및 동기 Windows 설정 저장소 위치에 대 한 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="19a42-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19a42-124">RDP (Windows Connect)/잠금 해제</span><span class="sxs-lookup"><span data-stu-id="19a42-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a42-125">가능한 경우 설정 저장소 위치에서 로컬 캐시로 비동기 Windows 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="19a42-126">캐시 된 Windows 설정 적용</span><span class="sxs-lookup"><span data-stu-id="19a42-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="19a42-127">설정 저장소 위치에서 비동기 windows 설정 다운로드 및 적용</span><span class="sxs-lookup"><span data-stu-id="19a42-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a42-128">RDP (Windows 연결 끊김)/잠금</span><span class="sxs-lookup"><span data-stu-id="19a42-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a42-129">로컬 캐시에 비동기 Windows 설정 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="19a42-130">로컬 캐시에서 설정 저장소 위치에 비동기 Windows 설정 (사용 가능한 경우)을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="19a42-131">설정 저장소 위치에 비동기 Windows 설정 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="19a42-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19a42-132">응용 프로그램 시작</span><span class="sxs-lookup"><span data-stu-id="19a42-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a42-133">응용 프로그램이 시작 될 때 로컬 캐시에서 응용 프로그램 설정 적용</span><span class="sxs-lookup"><span data-stu-id="19a42-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="19a42-134">응용 프로그램이 시작 될 때 설정 저장소 위치에서 응용 프로그램 설정 적용</span><span class="sxs-lookup"><span data-stu-id="19a42-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a42-135">응용 프로그램이 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a42-136">로컬 캐시에 대 한 응용 프로그램 설정 변경 내용을 저장 하 고 설정 저장소 위치에 대 한 설정을 복사 합니다 (사용 가능한 경우).</span><span class="sxs-lookup"><span data-stu-id="19a42-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="19a42-137">설정 저장소 위치에 대 한 응용 프로그램 설정 변경 내용 저장</span><span class="sxs-lookup"><span data-stu-id="19a42-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="19a42-138">회사 설정 센터에서 동기화 컨트롤러 예약 작업 또는 "지금 동기화"가 실행 됨</span><span class="sxs-lookup"><span data-stu-id="19a42-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="19a42-139">설정 저장소 위치와 로컬 캐시 간에 응용 프로그램 및 Windows 설정이 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="19a42-140">참고</span><span class="sxs-lookup"><span data-stu-id="19a42-140">Note</span></span></strong><br/><p><span data-ttu-id="19a42-141">설정 변경 내용은 응용 프로그램이 닫힐 때까지 로컬로 캐시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="19a42-142">이 트리거는 현재 실행 중인 응용 프로그램에 대 한 변경 내용을 내보내지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="19a42-143">Windows 설정의 경우, 변경 사항은 로컬로 캐시 되지 않고 다음 잠금 (비동기) 또는 로그 오프 (비동기 및 동기)로 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="19a42-144">설정은 다음과 같은 경우에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="19a42-145">비동기 Windows 설정이 직접 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="19a42-146">응용 프로그램 설정이 시작 되 면 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="19a42-147">비동기 및 동기 Windows 설정은 다음 Windows 로그온 중에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="19a42-148">다음 새로 고침 중에는 AppX (Windows 앱) 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="19a42-149"><a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">자세한 내용은 응용 프로그램 설정 모니터링을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="19a42-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="19a42-150">NA</span><span class="sxs-lookup"><span data-stu-id="19a42-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="19a42-151">원격 저장소에서 비동기 설정 업데이트 \*</span><span class="sxs-lookup"><span data-stu-id="19a42-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="19a42-152">캐시에서 새 비동기 설정을 로드 하 고 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="19a42-153">중앙 서버의 설정 로드 및 적용</span><span class="sxs-lookup"><span data-stu-id="19a42-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="19a42-154">관련 항목</span><span class="sxs-lookup"><span data-stu-id="19a42-154">Related topics</span></span>


[<span data-ttu-id="19a42-155">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="19a42-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="19a42-156">UE-V 2. x 예약 된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="19a42-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="19a42-157">UE-V 2. x에 대 한 구성 방법을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a42-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









