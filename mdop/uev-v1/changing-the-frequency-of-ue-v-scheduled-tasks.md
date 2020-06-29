---
title: UE-V 예약된 작업의 빈도 변경
description: UE-V 예약된 작업의 빈도 변경
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822688"
---
# <span data-ttu-id="a5b30-103">UE-V 예약된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="a5b30-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="a5b30-104">Microsoft UE-V (User Experience Virtualization) 에이전트 설치 관리자 AgentSetup.exe에서 UE-V 에이전트를 설치 하는 동안 두 개의 예약 된 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="a5b30-105">두 작업은 **서식 파일 자동 업데이트** 작업과 **설정 저장소 위치 상태** 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="a5b30-106">이러한 예약 된 작업은 UE-V 도구를 사용 하 여 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="a5b30-107">이러한 항목에 대 한 예약 된 작업을 변경 하려는 관리자는 Schtasks.exe 명령줄 옵션을 사용 하는 스크립트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="a5b30-108">Schtasks.exe에 대 한 자세한 내용은 [Schtasks를 사용 하 여 Windows Server 2003에서 작업을 예약 하는 방법을](https://go.microsoft.com/fwlink/?LinkID=264854)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5b30-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="a5b30-109">서식 파일 자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="a5b30-109">Template Auto-Update</span></span>


<span data-ttu-id="a5b30-110">**서식 파일 자동 업데이트** 작업은 설정 템플릿 카탈로그에서 새 서식 파일, 업데이트 또는 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="a5b30-111">이 작업은 SettingsTemplateCatalog가 구성 된 경우에만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="a5b30-112">**서식 파일 자동 업데이트** 작업은 ue-v 에이전트 설치 디렉터리에 있는 ApplySettingsCatalog.exe 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5b30-113">작업 이름</span><span class="sxs-lookup"><span data-stu-id="a5b30-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="a5b30-114">기본 트리거</span><span class="sxs-lookup"><span data-stu-id="a5b30-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5b30-115">\Microsoft\UE-V\Template 자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="a5b30-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5b30-116">매일 3:30 오전</span><span class="sxs-lookup"><span data-stu-id="a5b30-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5b30-117">**예:** 다음 명령은 각 시간에 설정 템플릿 카탈로그 저장소를 확인 하도록 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="a5b30-118">설정 저장소 위치 상태</span><span class="sxs-lookup"><span data-stu-id="a5b30-118">Settings Storage Location Status</span></span>


<span data-ttu-id="a5b30-119">**저장소 위치 상태 설정** 작업에서 다음 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="a5b30-120">UE-V 폴더가 여전히 고정 되어 있거나 오프 라인 파일 기능을 사용 하 여 등록 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="a5b30-121">설정 저장소 위치가 오프 라인 또는 온라인 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="a5b30-122">오프 라인 파일의 기본 간격 대신 지정 된 간격에 따라 동기화를 강제로 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="a5b30-123">사전 반입 하도록 구성 된 설정 패키지를 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="a5b30-124">Active Directory 홈 디렉터리 경로가 변경 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="a5b30-125">현재 설정 저장소 구성을 다음 위치에 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a5b30-126">작업 이름</span><span class="sxs-lookup"><span data-stu-id="a5b30-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="a5b30-127">기본 트리거</span><span class="sxs-lookup"><span data-stu-id="a5b30-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a5b30-128">\Microsoft\UE-V\Settings 저장소 위치 상태</span><span class="sxs-lookup"><span data-stu-id="a5b30-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a5b30-129">사용자에 게 로그온 할 때 – 트리거된 후 30 분 마다 무한정 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="a5b30-130">**예:** 다음 명령은 각 시간에 위의 작업을 실행 하도록 에이전트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b30-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="a5b30-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a5b30-131">Related topics</span></span>


[<span data-ttu-id="a5b30-132">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="a5b30-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="a5b30-133">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="a5b30-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





