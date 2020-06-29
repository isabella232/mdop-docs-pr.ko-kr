---
title: UE-V 2.1의 새로운 기능
description: UE-V 2.1의 새로운 기능
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826263"
---
# <span data-ttu-id="adb84-103">UE-V 2.1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="adb84-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="adb84-104">사용자 환경 가상화 2.1는 UE-V 2.0에 비해 이러한 새로운 기능과 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="adb84-105">[MICROSOFT ue-v (User Experience Virtualization) 2.1 릴리스](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) 정보는 ue-v 2.1 릴리스에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="adb84-106">Office 2013 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="adb84-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="adb84-107">UE-V 2.1에는 향상 된 Outlook 서명이 지원 되는 Microsoft Office 2013 설정 위치 서식 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="adb84-108">UE-V 2.1에서 서명 데이터는 사용자 장치 간에 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="adb84-109">새, 회신 및 전달 된 전자 메일에 대 한 기본 서명 설정을 동기화 했습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="adb84-110">고객은 더 이상 기본 서명 설정을 선택할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="adb84-111">**참고**  Outlook 프로필은 사용자가 Outlook 서명을 동기화 하려는 모든 장치에 대해 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="adb84-112">프로필이 아직 만들어지지 않은 경우 사용자가 프로필을 만든 다음 해당 장치에서 Outlook을 다시 시작 하 여 서명 동기화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="adb84-113">이전에는 UE-V 에이전트를 사용 하 여 자동으로 배포 되 고 등록 된 Microsoft Office 2010 설정 위치 템플릿이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="adb84-114">Office 365에서 UE-V 2.1를 사용 하 여 office 2013 설정이 office 365에서 roamed 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="adb84-115">설정이 Office 365에 의해 roamed 경우 UE-V를 통해 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="adb84-116">[Office 2013의 사용자 및 로밍 설정 개요](https://go.microsoft.com/fwlink/p/?LinkID=391220) 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="adb84-117">UE-V 2.1를 사용 하 여 설정 동기화를 사용 하도록 설정 하려면 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="adb84-118">그룹 정책을 사용 하 여 Office 365 동기화를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="adb84-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="adb84-119">Office 2013 설치 중에 Office 365 동기화 환경 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="adb84-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="adb84-120">UE-V 2.1은 [office 2013 및 office 2010 템플릿을](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="adb84-121">이 릴리스는 Office 2007 서식 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="adb84-122">사용자는 UE-V 2.0 또는 이전 버전의 Office 2007 서식 파일을 계속 사용할 수 있으며 [여기](https://go.microsoft.com/fwlink/p/?LinkID=246589)에 있는 ue-v 템플릿 갤러리에서 서식 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="adb84-123">분산 파일 시스템 네임 스페이스 사용자를 위한 수정</span><span class="sxs-lookup"><span data-stu-id="adb84-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="adb84-124">UE-V를 사용 하 여 DFSN (Distributed File System 네임 스페이스) 지원이 향상 되었습니다. Syncprovider이 설정 된 UE-V 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="adb84-125">PowerShell 또는 WMI를 사용 하 여이 구성을 사용 하지 않도록 설정 하면 사용자가 UE-V ping을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="adb84-126">DFSN 서버를 사용 하는 경우 UE-V ping이이 서버가 ping에 응답 하지 않기 때문에 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="adb84-127">비 응답은 UE-V가 설정을 동기화 하지 못하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="adb84-128">UE-V ping을 사용 하지 않도록 설정 하면 UE-V 동기화가 정상적으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="adb84-129">UE-V ping을 사용 하지 않도록 설정 하려면 다음 PowerShell cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="adb84-130">자격 증명 동기화</span><span class="sxs-lookup"><span data-stu-id="adb84-130">Synchronization for Credentials</span></span>


<span data-ttu-id="adb84-131">UE-V 2.1는 고객에 게 Windows 자격 증명 관리자에 저장 된 자격 증명과 인증서를 동기화 할 수 있는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="adb84-132">이 구성 요소는 기본적으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-132">This component is disabled by default.</span></span> <span data-ttu-id="adb84-133">이 구성 요소를 사용 하도록 설정 하면 사용자가 도메인 자격 증명과 인증서를 동기화 상태로 유지할 수 있습니다. 사용자가 장치에서 한 번 로그인 할 수 있으며, 이러한 자격 증명은 모든 UE-V 사용 디바이스에서 해당 사용자에 대해 로밍 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="adb84-134">[Ue-v 2.1를 사용 하 여 자격 증명 관리](https://technet.microsoft.com/library/dn458932.aspx#creds) 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="adb84-135">**참고**  Windows 8 이상에서 자격 증명 관리자는 웹 자격 증명을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="adb84-136">이러한 자격 증명은 사용자의 장치 간에 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="adb84-137">UE-V 및 Microsoft 계정 동기화</span><span class="sxs-lookup"><span data-stu-id="adb84-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="adb84-138">UE-V는 Microsoft 계정 동기화 라고도 하는 "OneDrive에 설정 동기화"가 설정 되어 있는지 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="adb84-139">Microsoft 계정이 설정을 동기화 하도록 구성 되지 않은 경우 UE-V는 장치 간에 Windows 앱, AppX 패키지 및 Windows 데스크톱 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="adb84-140">이렇게 하면 사용자가 엔터프라이즈 방화벽 외부에서 동기화 하지 않고 스토어 앱, 음악, 그림 및 기타 Microsoft 계정 사용 가능 응용 프로그램에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="adb84-141">UE-V는 그룹 정책에서 OneDrive와의 설정 동기화를 중지할지 또는 사용자가 사용자 컨트롤의 **이 컴퓨터에서 설정을 동기화 할** 수 없도록 설정할지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="adb84-142">외부의 SyncMethod에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="adb84-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="adb84-143">**External** 이라는 새 [syncmethod 구성은](https://technet.microsoft.com/library/dn554321.aspx) 사용자 컴퓨터의 로컬 폴더에 ue-v 설정이 기록 되는 경우 모든 외부 동기화 엔진 (예: 비즈니스용 OneDrive, 클라우드 폴더, Sharepoint 또는 Dropbox)을 사용 하 여 사용자가 액세스 하는 다른 컴퓨터에 이러한 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="adb84-144">VDI 모드에 대 한 향상 된 지원</span><span class="sxs-lookup"><span data-stu-id="adb84-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="adb84-145">UE-V 2.1에는 최종 사용자 간에 공유 되는 [VDI 세션에 대 한 지원이](https://technet.microsoft.com/library/dn458932.aspx#vdi) 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="adb84-146">관리자는 특수 VDI 템플릿을 등록 하 고 구성할 수 있으며,이를 통해 UE-V는 영구 VDI 세션에 대해 모든 기능을 그대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="adb84-147">**참고**  비 영구적인 VDI 세션에 VDI 모드를 사용 하도록 설정 하지 않으면 백업/복원 및 LKG 같은 특정 기능이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="adb84-148">관리 백업 및 복원</span><span class="sxs-lookup"><span data-stu-id="adb84-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="adb84-149">사용자가 새 장치를 사용할 때 Set Uevtemplate 프로필 PowerShell cmdlet을 사용 하 여 설정 위치 템플릿을 **백업** 또는 **로밍 (기본)** 프로필에 배치 하 여 추가 설정을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="adb84-150">이렇게 하면 컴퓨터 설정이 사용자 설정 외에도 새 컴퓨터와 동기화 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="adb84-151">백업 프로필에 할당 된 서식 파일은 해당 장치에 대해 백업 되 고 장치별로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="adb84-152">[Ue-v 2. x에서 관리 백업 및 복원 관리에 대 한](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) 자세한 내용은 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="adb84-153">추가 Windows 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="adb84-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="adb84-154">이제 UE-V는 터치 키보드 개인 설정, 맞춤법 사전을 동기화 하 고 최근 앱 및 화면 가장자리 설정에 대 한 앱 전환 기능을 사용 하 여 Windows 8 및 Windows 8.1 장치 간에 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="adb84-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="adb84-155">관련 항목</span><span class="sxs-lookup"><span data-stu-id="adb84-155">Related topics</span></span>


[<span data-ttu-id="adb84-156">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="adb84-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="adb84-157">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="adb84-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="adb84-158">Microsoft User Experience Virtualization(UE-V) 2.1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="adb84-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





