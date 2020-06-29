---
title: UE-V 2.x용 동기화 메서드
description: UE-V 2.x용 동기화 메서드
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823578"
---
# <span data-ttu-id="dce89-103">UE-V 2.x용 동기화 메서드</span><span class="sxs-lookup"><span data-stu-id="dce89-103">Sync Methods for UE-V 2.x</span></span>


<span data-ttu-id="dce89-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1 에이전트를 사용 하 여 사용자의 응용 프로그램 및 Windows 설정을 설정 저장소 위치와 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent lets you synchronize users’ application and Windows settings with the settings storage location.</span></span> <span data-ttu-id="dce89-105">*동기화 방법* 구성은 ue-v agent가 해당 설정을 업로드 하 고 설정 저장소 위치로 다운로드 하는 방법을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-105">The *Sync Method* configuration defines how the UE-V Agent uploads and downloads those settings to the settings storage location.</span></span> <span data-ttu-id="dce89-106">UE-V 2. x에는 *Syncmethod*라는 새 syncmethod가 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-106">UE-V 2.x introduces a new SyncMethod called the *SyncProvider*.</span></span> <span data-ttu-id="dce89-107">응용 프로그램 및 Windows 설정의 동기화를 시작 하는 트리거 이벤트에 대 한 자세한 내용은 [ue-v 2. x에 대 한 트리거 이벤트 동기화](sync-trigger-events-for-ue-v-2x-both-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dce89-107">For more information about trigger events that start the synchronization of application and Windows settings, see [Sync Trigger Events for UE-V 2.x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="dce89-108">SyncMethod 구성</span><span class="sxs-lookup"><span data-stu-id="dce89-108">SyncMethod Configuration</span></span>


<span data-ttu-id="dce89-109">이 표에서는 UE-V v 1.0에서 v 2.0에 v 2.1으로의 SyncMethod 변경 사항 및 각 구성에 대 한 설정에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-109">This table explains the changes to SyncMethod from UE-V v1.0 to v2.0 to v2.1, as well as the settings for each configuration:</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="dce89-110">SyncMethod 구성</span><span class="sxs-lookup"><span data-stu-id="dce89-110">SyncMethod Configuration</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="dce89-111">V 1.0</span><span class="sxs-lookup"><span data-stu-id="dce89-111">V1.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="dce89-112">V 2.0</span><span class="sxs-lookup"><span data-stu-id="dce89-112">V2.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="dce89-113">V 2.1 및 V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="dce89-113">V2.1 and V2.1 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="dce89-114">설명</span><span class="sxs-lookup"><span data-stu-id="dce89-114">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dce89-115">SyncProvider</span><span class="sxs-lookup"><span data-stu-id="dce89-115">SyncProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-116">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dce89-116">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-117">Default</span><span class="sxs-lookup"><span data-stu-id="dce89-117">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-118">Default</span><span class="sxs-lookup"><span data-stu-id="dce89-118">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-119">특정 응용 프로그램 또는 전역 Windows 데스크톱 설정에 대 한 설정 변경 내용은 로컬 캐시 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-119">Settings changes for a specific application or for global Windows desktop settings are saved locally to a cache folder.</span></span> <span data-ttu-id="dce89-120">이러한 변경 내용은 동기화 트리거 이벤트가 발생 하는 경우 설정 저장소 위치와 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-120">These changes are then synchronized with the settings storage location when a synchronization trigger event takes place.</span></span> <span data-ttu-id="dce89-121">변경 내용을 푸시하여 로컬 변경 내용이 설정 저장소 경로에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-121">Pushing out changes will save the local changes to the settings storage path.</span></span></p>
<p><span data-ttu-id="dce89-122">이 기본 설정은 컴퓨터에 대 한 골드 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-122">This default setting is the gold standard for computers.</span></span> <span data-ttu-id="dce89-123">이 옵션은 응용 프로그램이 나 운영 체제 시작이 장기간 지연 되지 않도록 짧은 지연 후 설정을 동기화 하 고 시간 초과 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-123">This option attempts to synchronize the setting and times out after a short delay to ensure that the application or operating system startup isn’t delayed for a long period of time.</span></span></p>
<p><span data-ttu-id="dce89-124">이 기능은 예약 된 작업 – 동기화 컨트롤러 응용 프로그램에도 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-124">This functionality is also tied to the Scheduled task – Sync Controller Application.</span></span> <span data-ttu-id="dce89-125">관리자는 예약 된 작업의 빈도를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-125">The administrator controls the frequency of the Scheduled task.</span></span> <span data-ttu-id="dce89-126">기본적으로 컴퓨터는 로그온 한 후 30 분 마다 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-126">By default, computers synchronize their settings every 30 min after logging on.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dce89-127">로 파일</span><span class="sxs-lookup"><span data-stu-id="dce89-127">OfflineFiles</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-128">Default</span><span class="sxs-lookup"><span data-stu-id="dce89-128">Default</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-129">사용 중단</span><span class="sxs-lookup"><span data-stu-id="dce89-129">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-130">사용 중단</span><span class="sxs-lookup"><span data-stu-id="dce89-130">Deprecated</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-131">V 2.0의 SyncProvider와 동일 하 게 동작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-131">Behaves the same as SyncProvider in V2.0.</span></span></p>
<p><span data-ttu-id="dce89-132">오프 라인 파일을 사용 하도록 설정 하 고 폴더가 고정 되어 있으면 UE-V가이 폴더의 고정을 해제 하 고 중앙 SMB 디렉터리로 직접 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-132">If Offline files are enabled and the folder is pinned then UE-V will unpin this folder and sync directly to the central SMB directory.</span></span></p>
<p><strong><span data-ttu-id="dce89-133">참고: </strong> CorpNet 연결 되지 않은 방식으로 ue-v를 사용 하려는 경우 (라고도 함 노트북으로 여행 하는 경우), 오프 라인 파일을 사용 하 여 설정이 roamed 확인 하는 지침을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dce89-133">NOTE:</strong> In V1.0 if you wanted to use UE-V in a CorpNet disconnected manner (aka traveling with a Laptop), then the guidance is to use Offline Files to ensure that your settings roamed.</span></span><span data-ttu-id="dce89-134">오프 라인 파일을 설정 하는 것은 사소한 기업 차단 인 충분 한 고객 피드백을 받게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-134"> We received sufficient customer feedback that turning on Offline files is a non-trivial enterprise blocker.</span></span> <span data-ttu-id="dce89-135">따라서 UE-V 2에서는 데이터를 로컬로 캐시 하 고 중앙 서버와 동기화 하는 밀접 하 게 결합 된 동기화 엔진을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-135">So in UE-V 2, we created a tightly coupled synchronization engine to cache your data locally and synchronize the settings to the central server.</span></span> <span data-ttu-id="dce89-136">이 기능 영역은 오프 라인 파일 또는 폴더 리디렉션을 대체 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-136">This feature area does not replace Offline Files or Folder Redirection.</span></span></p>
<p><span data-ttu-id="dce89-137">UE-V 2가 오프 라인 폴더에서 제대로 작동 하지 않으므로 지침에 따라 고정 된 오프 라인 또는 CSC 폴더로 설정 저장소 경로를 설정 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-137">UE-V 2 does not work well with Offline folders so the guidance is not to set the settings storage path to a pinned Offline or CSC folder.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dce89-138">외부</span><span class="sxs-lookup"><span data-stu-id="dce89-138">External</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-139">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dce89-139">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-140">해당 없음</span><span class="sxs-lookup"><span data-stu-id="dce89-140">n/a</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-141">지원함</span><span class="sxs-lookup"><span data-stu-id="dce89-141">Supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-142">UE-V 2.1의 새로운 기능은이 구성 메서드를 사용 하 여 사용자 컴퓨터의 로컬 폴더에 UE-V 설정이 기록 되는 경우 모든 외부 동기화 엔진 (예: 비즈니스용 OneDrive, 클라우드 폴더, Sharepoint 또는 Dropbox)을 통해 사용자가 액세스 하는 다른 컴퓨터에 이러한 설정을 적용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-142">New in UE-V 2.1, this configuration method specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dce89-143">없음</span><span class="sxs-lookup"><span data-stu-id="dce89-143">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-144">예</span><span class="sxs-lookup"><span data-stu-id="dce89-144">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-145">예</span><span class="sxs-lookup"><span data-stu-id="dce89-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-146">예</span><span class="sxs-lookup"><span data-stu-id="dce89-146">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="dce89-147">이 구성 설정은 기본적으로 VDI (가상 데스크톱 인프라) 및 스트리밍된 응용 프로그램 환경에 맞게 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-147">This configuration setting is designed for the Virtual Desktop Infrastructure (VDI) and Streamed Application experience primarily.</span></span> <span data-ttu-id="dce89-148">이 설정은 항상 연결을 사용할 수 있는 데이터 센터에서 사용 되는 Windows Server 상자에서 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-148">This setting should be used on Windows Server boxes used in a datacenter, where the connection will always be available.</span></span></p>
<p><span data-ttu-id="dce89-149">설정 변경 사항은 서버에 직접 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-149">Any settings changes are saved directly to the server.</span></span> <span data-ttu-id="dce89-150">설정 저장소 경로에 대 한 네트워크 연결을 사용할 수 없는 경우 설정 변경 내용이 장치에 캐시 되 고 다음에 동기화 공급자가 실행 될 때 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-150">If the network connection to the settings storage path is not available, then the settings changes are cached on the device and are synchronized the next time that the Sync Provider runs.</span></span> <span data-ttu-id="dce89-151">설정 저장소 경로를 찾을 수 없고 로그 오프할 때 풀링된 VDI 환경에서 사용자 프로필이 제거 되는 경우 이러한 설정 변경은 손실 되며, 사용자는 컴퓨터가 설정 저장소 경로에 다시 도달할 때 변경 내용을 재적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-151">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, then these settings changes are lost, and the user must reapply the change when the computer can again reach the settings storage path.</span></span></p>
<p><span data-ttu-id="dce89-152">앱과 OS는 위치가 제공 될 때까지 무기한 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-152">Apps and OS will wait indefinitely for the location to be present.</span></span> <span data-ttu-id="dce89-153">이로 인해 위치를 찾을 수 없는 경우 앱 로드 또는 OS 로그온 시간이 크게 증가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-153">This could cause App load or OS logon time to dramatically increase if the location is not found.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="dce89-154">다음과 같은 방법으로 sync 메서드를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dce89-154">You can configure the sync method in these ways:</span></span>

-   <span data-ttu-id="dce89-155">명령줄 매개 변수 또는 일괄 처리 스크립트를 통해 [Ue-v 에이전트를 배포](https://technet.microsoft.com/library/dn458891.aspx#agent) 하는 경우</span><span class="sxs-lookup"><span data-stu-id="dce89-155">When you [Deploy the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="dce89-156">[그룹 정책](https://technet.microsoft.com/library/dn458893.aspx) 설정</span><span class="sxs-lookup"><span data-stu-id="dce89-156">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="dce89-157">UE-V 용 [System Center 구성 팩](https://technet.microsoft.com/library/dn458917.aspx) 사용</span><span class="sxs-lookup"><span data-stu-id="dce89-157">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="dce89-158">UE-V 에이전트를 설치한 후 [Windows PowerShell 또는 WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx) 를 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="dce89-158">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>






## <span data-ttu-id="dce89-159">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dce89-159">Related topics</span></span>


[<span data-ttu-id="dce89-160">UE-V 2.x에 대한 필수 기능 배포</span><span class="sxs-lookup"><span data-stu-id="dce89-160">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[<span data-ttu-id="dce89-161">UE-V 2.x에 대한 필수 기능 배포</span><span class="sxs-lookup"><span data-stu-id="dce89-161">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[<span data-ttu-id="dce89-162">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="dce89-162">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





