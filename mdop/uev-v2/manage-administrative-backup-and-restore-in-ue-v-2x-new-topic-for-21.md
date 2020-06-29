---
title: UE-V 2. x에서 관리 백업 및 복원 관리
description: UE-V 2. x에서 관리 백업 및 복원 관리
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827388"
---
# <span data-ttu-id="ec7cb-103">UE-V 2. x에서 관리 백업 및 복원 관리</span><span class="sxs-lookup"><span data-stu-id="ec7cb-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="ec7cb-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1의 관리자는 응용 프로그램 및 Windows 설정을 원래 상태로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="ec7cb-105">또한 UE-V 2.1의 새로운 기능을 사용 하면 사용자가 새 장치를 사용할 때 추가 설정을 복원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="ec7cb-106">사용자가 새 장치를 사용할 때 UE-V 2.1 또는 UE-V 2.1 SP1의 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="ec7cb-107">사용자가 새 장치를 사용할 때 설정을 복원 하려면 Set Uev서식 파일 PowerShell cmdlet을 사용 하 여 **백업** 또는 **로밍 (기본)** 프로필에 설정 위치 템플릿을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="ec7cb-108">이렇게 하면 컴퓨터 설정이 사용자 설정 외에도 새 컴퓨터와 동기화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="ec7cb-109">백업 프로필에 할당 된 서식 파일은 해당 장치에 대해 백업 되 고 장치별로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="ec7cb-110">서식 파일에 대 한 설정을 백업 하려면 Windows PowerShell에서 다음 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="ec7cb-111">&lt;TemplateID &gt; 는 Ue-v 템플릿 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="ec7cb-112">&lt;백업은 &gt; 백업 또는 로밍 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="ec7cb-113">사용자의 장치를 바꿀 때 UE-V는 사용자의 도메인, 사용자 이름 및 장치 이름이 모두 일치 하는 경우 설정을 자동으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="ec7cb-114">모든 동기화 및 백업 데이터는 장치에서 자동으로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="ec7cb-115">새 PowerShell cmdlet, Restore UevBackup을 사용 하 여 다른 장치에서 설정을 복원할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="ec7cb-116">새 장치에 대 한 설정 패키지를 복제 하려면 Windows PowerShell에서 다음 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="ec7cb-117">여기서 &lt; MachineName &gt; 는 디바이스의 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="ec7cb-118">여러 응용 프로그램을 포함 하는 Office 2013 서식 파일 등의 서식 파일은 모두 roamed (기본값) 또는 백업 프로필에 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="ec7cb-119">서식 파일 모음의 개별 앱은 그룹을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="ec7cb-120">Office 2013 in box 서식 파일에는 로밍 및 백업 전용 설정이 모두 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="ec7cb-121">로밍 프로필에는 백업 전용 설정을 포함할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="ec7cb-122">백업/복원 기능의 일부로 **마지막으로 알려진 양호한 (LKG)** 를 설정으로 롤백하는 옵션에 추가 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="ec7cb-123">이번 릴리스에서는 원래 설정 또는 LKG 설정으로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="ec7cb-124">LKG 설정을 사용 하면 사용자가 설정의 사전 UE-V 상태 앞에 있는 중간 및 안정적인 시점으로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="ec7cb-125">UE-V를 사용 하 여 템플릿을 백업/복원 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ec7cb-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="ec7cb-126">다음은 UE-V의 키 백업 및 복원 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="ec7cb-127">서식 파일 프로필</span><span class="sxs-lookup"><span data-stu-id="ec7cb-127">Template profiles</span></span>

-   <span data-ttu-id="ec7cb-128">설정 저장소 위치 템플릿 내의 설정 패키지 위치</span><span class="sxs-lookup"><span data-stu-id="ec7cb-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="ec7cb-129">백업 트리거</span><span class="sxs-lookup"><span data-stu-id="ec7cb-129">Backup trigger</span></span>

-   <span data-ttu-id="ec7cb-130">설정 복원 방법</span><span class="sxs-lookup"><span data-stu-id="ec7cb-130">How settings are restored</span></span>

**<span data-ttu-id="ec7cb-131">서식 파일 프로필</span><span class="sxs-lookup"><span data-stu-id="ec7cb-131">Template Profiles</span></span>**

<span data-ttu-id="ec7cb-132">UE-V 템플릿 프로필은 템플릿이 디바이스에 등록 되거나 PowerShell/WMI 구성 유틸리티를 통해 등록 후에 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="ec7cb-133">프로필 유형에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-133">The profile types include:</span></span>

-   <span data-ttu-id="ec7cb-134">로밍 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec7cb-134">Roaming (default)</span></span>

-   <span data-ttu-id="ec7cb-135">백업</span><span class="sxs-lookup"><span data-stu-id="ec7cb-135">Backup</span></span>

-   <span data-ttu-id="ec7cb-136">BackupOnly</span><span class="sxs-lookup"><span data-stu-id="ec7cb-136">BackupOnly</span></span>

<span data-ttu-id="ec7cb-137">달리 지정 하지 않는 한 등록 되 면 모든 템플릿은 로밍 프로필에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="ec7cb-138">이러한 서식 파일은 해당 서식 파일을 사용 하도록 설정 된 모든 UE-V 사용 디바이스에 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="ec7cb-139">명령줄에서 PowerShell 또는 WMI를 사용 하 여 서식 파일을 추가할 수 있습니다. Set Uev서식 파일 cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="ec7cb-140">백업 프로필의 서식 파일은 특수 한 디바이스 이름 디렉터리의 설정 저장소 위치에 이러한 설정을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="ec7cb-141">지정 된 설정이이 위치에 백업 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="ec7cb-142">지정 된 BackupOnly에는 명시적으로 복원 하지 않는 한 동기화 하지 않아야 하는 장치와 관련 된 설정만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="ec7cb-143">이러한 설정은 설정 저장소 위치에서 Backedup 설정으로 동일한 디바이스 관련 설정 패키지 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="ec7cb-144">이러한 서식 파일에는이 프로필의 일부로 지정 되는 특수 식별자가 서식 파일에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="ec7cb-145">설정 저장소 위치 템플릿 내의 설정 패키지 위치</span><span class="sxs-lookup"><span data-stu-id="ec7cb-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="ec7cb-146">로밍 프로필 설정은 설정 저장소 위치에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="ec7cb-147">백업 또는 BackupOnly 프로필에 할당 된 템플릿은 해당 설정을 특수 디바이스 이름 디렉터리의 설정 저장소 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="ec7cb-148">이러한 프로필에 서식 파일을 사용 하는 각 디바이스에는 고유한 장치 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="ec7cb-149">UE-V를 통해 이러한 디렉터리가 정리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="ec7cb-150">백업 트리거</span><span class="sxs-lookup"><span data-stu-id="ec7cb-150">Backup trigger</span></span>**

<span data-ttu-id="ec7cb-151">백업은 UE-V 동기화를 트리거하는 동일한 이벤트에 의해 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="ec7cb-152">설정 복원 방법</span><span class="sxs-lookup"><span data-stu-id="ec7cb-152">How settings are restored</span></span>**

<span data-ttu-id="ec7cb-153">사용자의 장치를 복원 하면 현재 등록 된 템플릿의 설정이 다른 디바이스의 백업 폴더와 모든 동기화 된 설정 중 현재 컴퓨터에 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="ec7cb-154">설정은 다음 두 가지 방법으로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="ec7cb-155">자동 복원</span><span class="sxs-lookup"><span data-stu-id="ec7cb-155">Automatic restore</span></span>**

    <span data-ttu-id="ec7cb-156">사용자의 UE-V 설정 저장소 경로, 도메인 및 컴퓨터 이름이 현재 사용자와 일치 하는 경우에는 해당 사용자의 모든 설정이 동기화 되 고 최신 설정만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="ec7cb-157">사용자가 처음으로 새 장치에 로그온 하 고 이러한 조건이 충족 되는 경우 설정 데이터가 해당 장치에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="ec7cb-158">참고</span><span class="sxs-lookup"><span data-stu-id="ec7cb-158">Note</span></span>**  
    <span data-ttu-id="ec7cb-159">접근성 및 Windows 데스크톱 설정을 적용 하려면 사용자가 Windows에 다시 로그온 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="ec7cb-160">수동 복원</span><span class="sxs-lookup"><span data-stu-id="ec7cb-160">Manual Restore</span></span>**

    <span data-ttu-id="ec7cb-161">새로 고침 중에 장치를 복원 하 여 사용자를 지원 하려는 경우 Restore UevBackup cmdlet을 사용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="ec7cb-162">이 명령을 사용 하면 설정 저장소 위치에서 사용자의 설정이 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="ec7cb-163">응용 프로그램 및 Windows 설정을 원래 상태로 복원</span><span class="sxs-lookup"><span data-stu-id="ec7cb-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="ec7cb-164">WMI 및 Windows PowerShell 명령을 사용 하 여 UE-V Agent가 설치 된 후 처음으로 응용 프로그램을 시작할 때 컴퓨터에 있던 설정 값으로 응용 프로그램 및 Windows 설정을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="ec7cb-165">이 복원 작업은 응용 프로그램 또는 Windows 설정 기준에 따라 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="ec7cb-166">설정은 다음에 응용 프로그램을 실행할 때 복원 되거나, 사용자가 운영 체제에 로그온 할 때 설정이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="ec7cb-167">UE-V 2. x 용 Windows PowerShell을 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="ec7cb-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="ec7cb-168">Windows PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="ec7cb-169">다음 Windows PowerShell cmdlet을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="ec7cb-170">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec7cb-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="ec7cb-171">설명</span><span class="sxs-lookup"><span data-stu-id="ec7cb-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="ec7cb-172">응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="ec7cb-173">WMI를 사용 하 여 응용 프로그램 설정 및 Windows 설정을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="ec7cb-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="ec7cb-174">Windows PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="ec7cb-175">다음 WMI 명령을 입력 하 여 응용 프로그램 설정 및 Windows 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="ec7cb-176">WMI 명령</span><span class="sxs-lookup"><span data-stu-id="ec7cb-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="ec7cb-177">설명</span><span class="sxs-lookup"><span data-stu-id="ec7cb-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="ec7cb-178">응용 프로그램에 대 한 사용자 설정을 복원 하거나 Windows 설정 그룹을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7cb-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="ec7cb-179">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ec7cb-179">Related topics</span></span>


[<span data-ttu-id="ec7cb-180">Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="ec7cb-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="ec7cb-181">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="ec7cb-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









