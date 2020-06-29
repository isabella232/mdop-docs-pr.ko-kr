---
title: UE-V 2. x 예약 된 작업의 빈도 변경
description: UE-V 2. x 예약 된 작업의 빈도 변경
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824428"
---
# <span data-ttu-id="26589-103">UE-V 2. x 예약 된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="26589-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="26589-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1 에이전트 설치 관리자 AgentSetup.exe, UE-V 에이전트를 설치 하는 동안 다음과 같은 예약 된 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26589-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="26589-105">응용 프로그램 설정 모니터링</span><span class="sxs-lookup"><span data-stu-id="26589-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="26589-106">동기화 컨트롤러 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="26589-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="26589-107">로그 오프할 때 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="26589-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="26589-108">서식 파일 자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="26589-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="26589-109">CEIP 데이터 수집</span><span class="sxs-lookup"><span data-stu-id="26589-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="26589-110">CEIP 데이터 업로드</span><span class="sxs-lookup"><span data-stu-id="26589-110">Upload CEIP Data</span></span>**

<span data-ttu-id="26589-111">**참고**  CEIP 데이터 수집을 제외 하 고는 UE-V를 사용 하지 않고 작동할 수 없으므로 이러한 작업은 활성 상태로 유지 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="26589-112">이러한 예약 된 작업은 UE-V 도구를 사용 하 여 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="26589-113">이러한 항목에 대 한 예약 된 작업을 변경 하려는 관리자는 Schtasks.exe 명령줄 옵션을 사용 하는 스크립트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="26589-114">Schtasks.exe에 대 한 자세한 내용은 [Schtasks를 사용 하 여 Windows Server 2003에서 작업을 예약 하는 방법을](https://go.microsoft.com/fwlink/?LinkID=264854)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26589-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="26589-115">자세한 내용은</span><span class="sxs-lookup"><span data-stu-id="26589-115">For more information about</span></span>

## <span data-ttu-id="26589-116">UE-V 예약 작업</span><span class="sxs-lookup"><span data-stu-id="26589-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="26589-117">다음 예약 된 작업은 예제 예약 작업 구성 명령이 있는 UE-V 2에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="26589-118">CEIP 데이터 수집</span><span class="sxs-lookup"><span data-stu-id="26589-118">Collect CEIP Data</span></span>

<span data-ttu-id="26589-119">설치 시 사용자 또는 관리자가 CEIP (고객 환경 개선 프로그램)에 참여 하도록 choses 경우 UE-V는 향후 릴리스에서 제품을 개선 하는 데 도움이 되는 데이터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="26589-120">이 예약 된 작업은 로그온 할 때만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="26589-121">**CEIP 데이터 수집** 작업은 ue-v 에이전트 설치 디렉터리에 있는 UevSqmSession.exe를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26589-122">작업 이름</span><span class="sxs-lookup"><span data-stu-id="26589-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="26589-123">기본 이벤트</span><span class="sxs-lookup"><span data-stu-id="26589-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26589-124">\Microsoft\UE-V\Collect CEIP 데이터</span><span class="sxs-lookup"><span data-stu-id="26589-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-125">로그온</span><span class="sxs-lookup"><span data-stu-id="26589-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="26589-126">응용 프로그램 설정 모니터링</span><span class="sxs-lookup"><span data-stu-id="26589-126">Monitor Application Settings</span></span>

<span data-ttu-id="26589-127">Windows 앱에 대 한 설정을 동기화 하는 데 **응용 프로그램 설정 모니터링** 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="26589-128">이는 로그온 할 때 실행 되지만, 로그온 detrimentally에 영향을 주지 않도록 30 초 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="26589-129">응용 프로그램 상태 모니터링 작업은 UE-V 에이전트 설치 디렉터리에 있는 UevAppMonitor.exe 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26589-130">작업 이름</span><span class="sxs-lookup"><span data-stu-id="26589-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="26589-131">기본 이벤트</span><span class="sxs-lookup"><span data-stu-id="26589-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26589-132">\Microsoft\UE-V\Monitor 응용 프로그램 상태</span><span class="sxs-lookup"><span data-stu-id="26589-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-133">로그온</span><span class="sxs-lookup"><span data-stu-id="26589-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="26589-134">동기화 컨트롤러 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="26589-134">Sync Controller Application</span></span>

<span data-ttu-id="26589-135">동기화 컨트롤러 **응용 프로그램** 작업은 동기화 컨트롤러를 시작 하 여 컴퓨터에서 설정 저장소 위치로 설정을 동기화 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="26589-136">기본적으로 작업은 30 분 마다 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="26589-137">해당 시점에 로컬 설정이 설정 저장소 위치와 동기화 되 고 설정 저장소 위치의 업데이트 된 설정이 컴퓨터에 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="26589-138">동기화 컨트롤러 응용 프로그램은 UE-V 에이전트 설치 디렉터리에 있는 Microsoft.Uev.SyncController.exe를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="26589-139">**참고:** 이 작업은 **응용 프로그램 설정 모니터링** 작업에 따라 로그온 할 때 실행 되지만, 로그온 detrimentally에 영향을 주지 않도록 30 초 단위로 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26589-140">작업 이름</span><span class="sxs-lookup"><span data-stu-id="26589-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="26589-141">기본 이벤트</span><span class="sxs-lookup"><span data-stu-id="26589-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26589-142">\Microsoft\UE-V\Sync 컨트롤러 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="26589-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-143">로그온 및 30 분 후에 모두</span><span class="sxs-lookup"><span data-stu-id="26589-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="26589-144">예를 들어 다음 명령은 기본 30 분 대신 15 분 마다 설정을 동기화 하도록 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="26589-145">로그 오프할 때 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="26589-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="26589-146">**로그 오프할 때 설정 동기화** 작업은 ue-v를 사용 하 여 로그 오프할 때 응용 프로그램의 동기화를 제어 하는 로그온 할 때 응용 프로그램을 시작 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="26589-147">로그 오프할 때 설정 동기화 작업은 UE-V 에이전트 설치 디렉터리에 있는 Microsoft.Uev.SyncController.exe 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26589-148">작업 이름</span><span class="sxs-lookup"><span data-stu-id="26589-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="26589-149">기본 이벤트</span><span class="sxs-lookup"><span data-stu-id="26589-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26589-150">로그 오프할 때 설정 \Microsoft\UE-V\Synchronize</span><span class="sxs-lookup"><span data-stu-id="26589-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-151">로그온</span><span class="sxs-lookup"><span data-stu-id="26589-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="26589-152">서식 파일 자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="26589-152">Template Auto Update</span></span>

<span data-ttu-id="26589-153">**서식 파일 자동 업데이트** 작업은 설정 템플릿 카탈로그에서 새 서식 파일, 업데이트 또는 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="26589-154">이 작업은 SettingsTemplateCatalog가 구성 된 경우에만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="26589-155">**서식 파일 자동 업데이트** 작업은 ue-v 에이전트 설치 디렉터리에 있는 ApplySettingsCatalog.exe 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26589-156">작업 이름</span><span class="sxs-lookup"><span data-stu-id="26589-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="26589-157">기본 이벤트</span><span class="sxs-lookup"><span data-stu-id="26589-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26589-158">\Microsoft\UE-V\Template 자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="26589-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-159">시스템 시작 및 3:30 오전 1 시간 창 내 임의 시간에</span><span class="sxs-lookup"><span data-stu-id="26589-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="26589-160">**예:** 다음 명령은 UE-V Agent를 구성 하 여 각 시간에 설정 템플릿 카탈로그 저장소를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="26589-161">CEIP 데이터 업로드</span><span class="sxs-lookup"><span data-stu-id="26589-161">Upload CEIP Data</span></span>

<span data-ttu-id="26589-162">사용자나 관리자가 CEIP (사용자 환경 개선 프로그램)에 참여 하도록 선택한 경우 설치 중에 **Ceip 데이터 업로드** 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="26589-163">이 작업은 데이터를 사용 하는 CEIP 서버에 데이터를 업로드 하 여 향후 릴리스의 UE-V를 위해 제품을 개선 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26589-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="26589-164">이 예약 된 작업은 로그온 시와 4 시간 간격으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="26589-165">**CEIP 데이터 업로드** 작업은 ue-v 에이전트 설치 디렉터리에 있는 UevSqmUploader.exe 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26589-166">작업 이름</span><span class="sxs-lookup"><span data-stu-id="26589-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="26589-167">기본 이벤트</span><span class="sxs-lookup"><span data-stu-id="26589-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26589-168">\Microsoft\UE-V\Upload CEIP 데이터</span><span class="sxs-lookup"><span data-stu-id="26589-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-169">로그온 및 4 시간 마다</span><span class="sxs-lookup"><span data-stu-id="26589-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="26589-170">UE-V 2 예약 된 작업 세부 정보</span><span class="sxs-lookup"><span data-stu-id="26589-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="26589-171">다음 차트는 UE-V 2에 대 한 예약 된 작업에 대 한 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="26589-172">작업 이름 </strong> (파일 이름)</span><span class="sxs-lookup"><span data-stu-id="26589-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="26589-173">기본 빈도</span><span class="sxs-lookup"><span data-stu-id="26589-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="26589-174">전원 켜기/끄기</span><span class="sxs-lookup"><span data-stu-id="26589-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="26589-175">유휴 전용</span><span class="sxs-lookup"><span data-stu-id="26589-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="26589-176">네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="26589-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="26589-177">설명</span><span class="sxs-lookup"><span data-stu-id="26589-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="26589-178">응용 프로그램 설정 모니터링 </strong> (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="26589-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-179">로그온 후 30 초 후에 시작 되며 로그 오프할 때까지 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-180">아니오</span><span class="sxs-lookup"><span data-stu-id="26589-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-181">예</span><span class="sxs-lookup"><span data-stu-id="26589-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-182">해당 없음</span><span class="sxs-lookup"><span data-stu-id="26589-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-183">Windows (AppX) 앱에 대 한 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="26589-184">동기화 컨트롤러 응용 프로그램 </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="26589-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-185">로그온 시와 30 분 마다</span><span class="sxs-lookup"><span data-stu-id="26589-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-186">예</span><span class="sxs-lookup"><span data-stu-id="26589-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-187">예</span><span class="sxs-lookup"><span data-stu-id="26589-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-188">네트워크가 연결 된 경우에만</span><span class="sxs-lookup"><span data-stu-id="26589-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-189">로컬 설정을 설정 저장소 위치와 동기화 하는 동기화 컨트롤러를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="26589-190">로그 오프 </strong> (Microsoft.Uev.SyncController.exe)에서 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="26589-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-191">로그온 할 때 실행 되며, 로그 오프가 설정을 동기화 하기 위해 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="26589-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-192">아니오</span><span class="sxs-lookup"><span data-stu-id="26589-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-193">예</span><span class="sxs-lookup"><span data-stu-id="26589-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-194">해당 없음</span><span class="sxs-lookup"><span data-stu-id="26589-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-195">로그 오프할 때 응용 프로그램의 동기화를 제어 하는 로그온 할 때 응용 프로그램을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="26589-196">서식 파일 자동 업데이트 </strong> (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="26589-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-197">초기 로그온 시와 매일 오전 3:30 시에 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-198">예</span><span class="sxs-lookup"><span data-stu-id="26589-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-199">아니오</span><span class="sxs-lookup"><span data-stu-id="26589-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-200">해당 없음</span><span class="sxs-lookup"><span data-stu-id="26589-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-201">설정 서식 파일 카탈로그에서 새 서식 파일, 업데이트 또는 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="26589-202">이 작업은 SettingsTemplateCatalog가 구성 된 경우에만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="26589-203">CEIP 데이터 수집 </strong> (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="26589-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-204">로그온 시작 시 서비스</span><span class="sxs-lookup"><span data-stu-id="26589-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-205">아니오</span><span class="sxs-lookup"><span data-stu-id="26589-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-206">예</span><span class="sxs-lookup"><span data-stu-id="26589-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-207">해당 없음</span><span class="sxs-lookup"><span data-stu-id="26589-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-208">사용자 또는 관리자가 CEIP (고객 환경 개선 프로그램)에 opts이 작업은 UE-V 이후 릴리스를 개선 하는 데 도움이 되는 데이터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="26589-209">CEIP 데이터 업로드 </strong> (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="26589-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-210">로그온 할 때마다 실행 되며, 이후 매일 4:00 오전</span><span class="sxs-lookup"><span data-stu-id="26589-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-211">아니오</span><span class="sxs-lookup"><span data-stu-id="26589-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-212">예</span><span class="sxs-lookup"><span data-stu-id="26589-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-213">네트워크가 연결 된 경우에만</span><span class="sxs-lookup"><span data-stu-id="26589-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="26589-214">사용자나 관리자가 CEIP (사용자 환경 개선 프로그램)에 opts 경우이 작업을 통해 해당 데이터를 CEIP 서버에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="26589-215">Legend</span><span class="sxs-lookup"><span data-stu-id="26589-215">Legend</span></span>**

-   <span data-ttu-id="26589-216">**Power Toggle** -작업 스케줄러는 AC 전원에 연결 되지 않은 경우 전력 소모량을 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="26589-217">컴퓨터가 배터리 전원으로 전환 되는 경우 작업이 중지 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="26589-218">**유휴 전용** – 컴퓨터가 유휴 상태가 끝나면 작업의 실행이 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="26589-219">컴퓨터가 다시 유휴 상태일 때는 기본적으로 작업이 다시 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="26589-220">대신 다음 작업 트리거에서 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="26589-221">**네트워크 연결** – 컴퓨터가 네트워크 연결을 사용할 수 있는 경우에만 "예"로 표시 된 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="26589-222">네트워크 연결에 관계 없이 "N/A"로 표시 된 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="26589-223">예약 된 작업을 관리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="26589-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="26589-224">예약 된 작업을 찾으려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="26589-225">사용자 컴퓨터에서 "작업 예약"을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="26589-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="26589-226">이동: 작업 스케줄러- &gt; 작업 스케줄러 라이브러리- &gt; Microsoft- &gt; ue-v</span><span class="sxs-lookup"><span data-stu-id="26589-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="26589-227">세부 정보 창에서 관리 하 고 구성 하려는 예약 된 작업을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="26589-228">추가 정보</span><span class="sxs-lookup"><span data-stu-id="26589-228">Additional information</span></span>

<span data-ttu-id="26589-229">UE-V 예약 작업에는 다음과 같은 추가 정보가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="26589-230">작업 순서 프로그램은 기본적으로 UE-V Agent 설치 폴더에 있습니다 `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` .</span><span class="sxs-lookup"><span data-stu-id="26589-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="26589-231">UE-V SyncMethod가 "Syncmethod"로 설정 된 경우 동기화 컨트롤러 응용 프로그램 예약 된 작업은 중요 한 구성 요소입니다 (UE-V 2 기본 구성).</span><span class="sxs-lookup"><span data-stu-id="26589-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="26589-232">이 예약 된 작업은 SettingsSToragePath를 로컬에 캐시 된 설정 패키지 파일 버전과 동기화 상태로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="26589-233">사용자가 설정 된 설정이 자주 동기화 되지 않는 경우에는 예약 된 작업 설정을 1 분 정도 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="26589-234">필요한 경우 30 분 기본값을 더 높은 값으로 늘릴 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="26589-235">사용자가 로그온 할 때 설정이 빠른 속도로 동기화 되지 않는 경우에는 예약 된 작업에 대 한 지연 설정을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="26589-236">( **트리거 편집** 대화 상자에서 지연 설정을 찾을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="26589-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="26589-237">다른 방법을 사용 하 여 클라이언트 템플릿을 동기화 된 상태로 유지 하는 경우 (예: 그룹 정책 또는 Configuration Manager 기준) 서식 파일 자동 업데이트 예약 된 작업을 사용 하지 않도록 설정할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="26589-238">SettingsTemplateCatalog 속성 값을 비워 두면 UE-V가 사용자 지정 서식 파일의 설정 카탈로그를 검사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26589-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="26589-239">이 예약 된 작업은 ApplySettingsCatalog.exe 실행 되며 기본적으로 즉시 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26589-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="26589-240">예약 된 응용 프로그램 설정 모니터링 작업은 각 앱에 기본 제공 되는 Windows 앱 프로그램 설정 트리거를 기반으로 AppX (Windows 앱) 설정을 실시간으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26589-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="26589-241">관련 항목</span><span class="sxs-lookup"><span data-stu-id="26589-241">Related topics</span></span>


[<span data-ttu-id="26589-242">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="26589-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="26589-243">사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포</span><span class="sxs-lookup"><span data-stu-id="26589-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





