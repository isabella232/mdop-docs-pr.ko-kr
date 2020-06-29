---
title: UE-V 2.x에 대한 구성 관리
description: UE-V 2.x에 대한 구성 관리
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827383"
---
# <span data-ttu-id="97e3a-103">UE-V 2.x에 대한 구성 관리</span><span class="sxs-lookup"><span data-stu-id="97e3a-103">Manage Configurations for UE-V 2.x</span></span>


<span data-ttu-id="97e3a-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1 수명 주기를 진행 하는 동안 UE-V Agent의 구성을 관리 하 고 설정 패키지 파일과 같은 리소스에 대 한 저장소 위치도 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-104">In the course of the Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span> <span data-ttu-id="97e3a-105">사용자가 UE-V를 사용 하 여 상호 작용 하는 방식을 정의 하도록 회사 설정 센터를 구성 하는 등 다른 작업을 수행 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-105">You might have to perform other tasks, for example, configuring the Company Settings Center to define how users interact with UE-V.</span></span> <span data-ttu-id="97e3a-106">다음 항목에서는 이러한 UE-V 리소스 관리에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-106">The following topics provide guidance for managing these UE-V resources.</span></span>

## <span data-ttu-id="97e3a-107">그룹 정책 개체를 사용 하 여 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="97e3a-107">Configuring UE-V 2.x by using Group Policy Objects</span></span>


<span data-ttu-id="97e3a-108">그룹 정책 개체를 사용 하 여 UE-V가 컴퓨터에서 설정을 동기화 하는 방식을 정의 하는 설정을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-108">You can use Group Policy Objects to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="97e3a-109">그룹 정책 개체를 사용 하 여 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="97e3a-109">Configuring UE-V 2.x with Group Policy Objects</span></span>](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## <span data-ttu-id="97e3a-110">System Center Configuration Manager 2012에서 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="97e3a-110">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="97e3a-111">SystemCenter2012 ConfigurationManager를 사용 하 여 ue-v 2 구성 팩을 사용 하 여 UE-V 에이전트를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-111">You can use SystemCenter2012 ConfigurationManager to manage the UE-V Agent by using the UE-V 2 Configuration Pack.</span></span>

[<span data-ttu-id="97e3a-112">System Center Configuration Manager 2012에서 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="97e3a-112">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## <span data-ttu-id="97e3a-113">UE-V를 사용 하 여 PowerShell 및 WMI 관리</span><span class="sxs-lookup"><span data-stu-id="97e3a-113">Administering UE-V 2.x with PowerShell and WMI</span></span>


<span data-ttu-id="97e3a-114">UE-V는 관리자가 다양 한 UE-V 작업을 수행 하는 데 도움이 되는 Windows PowerShell cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-114">UE-V provides Windows PowerShell cmdlets, which can help administrators perform various UE-V tasks.</span></span>

[<span data-ttu-id="97e3a-115">Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="97e3a-115">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## <span data-ttu-id="97e3a-116">UE-V 2. x에 대 한 회사 설정 센터 구성</span><span class="sxs-lookup"><span data-stu-id="97e3a-116">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="97e3a-117">UE-V Agent를 사용 하 여 사용자가 UE-V를 사용 하는 방식을 정의 하 여 설치한 회사 설정 센터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-117">You can configure the Company Settings Center that is installed by using the UE-V Agent to define how users interact with UE-V.</span></span>

[<span data-ttu-id="97e3a-118">UE-V 2. x에 대 한 회사 설정 센터 구성</span><span class="sxs-lookup"><span data-stu-id="97e3a-118">Configuring the Company Settings Center for UE-V 2.x</span></span>](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## <span data-ttu-id="97e3a-119">UE-V 2. x에 대 한 구성 설정의 예</span><span class="sxs-lookup"><span data-stu-id="97e3a-119">Examples of configuration settings for UE-V 2.x</span></span>


<span data-ttu-id="97e3a-120">다음은 UE-V 구성 설정의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-120">Here are some examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="97e3a-121">**설정 저장소 경로:** UE-V 설정을 저장 하는 파일 공유의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-121">**Settings Storage Path:** Specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="97e3a-122">**설정 서식 파일 카탈로그 경로:** 새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-122">**Settings Template Catalog Path:** Specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="97e3a-123">**Microsoft 서식 파일 등록:** 설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-123">**Register Microsoft Templates:** Specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="97e3a-124">**동기화 방법:** UE-V가 동기화 공급자를 사용할지 아니면 "없음"을 사용 하는지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-124">**Synchronization Method:** Specifies whether UE-V uses the sync provider or "none".</span></span> <span data-ttu-id="97e3a-125">"SyncProvider"는 네트워크에 연결 되지 않은 컴퓨터를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-125">The "SyncProvider" supports computers that are disconnected from the network.</span></span> <span data-ttu-id="97e3a-126">"없음"은 컴퓨터가 항상 네트워크에 연결 되어 있는 경우 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-126">"None" applies when the computer is always connected to the network.</span></span> <span data-ttu-id="97e3a-127">Sync 메서드에 대 한 자세한 내용은 [ue-v 2. x에 대 한 Sync 메서드](sync-methods-for-ue-v-2x-both-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97e3a-127">For more information about the Sync Method, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

-   <span data-ttu-id="97e3a-128">**동기화 시간 제한:** 설정 저장소 위치에서 사용자 설정을 검색할 때 시간이 초과 되기 전에 컴퓨터가 대기 하는 시간 (밀리초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-128">**Synchronization Timeout:** Specifies the number of milliseconds that the computer waits before time-out when it retrieves the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="97e3a-129">**동기화 사용:** UE-V 설정 동기화를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-129">**Synchronization Enable:** Specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="97e3a-130">**최대 패키지 크기:** UE-V Agent가 경고를 보고 하는 설정 패키지 파일의 임계값 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-130">**Maximum Package Size:** Specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

-   <span data-ttu-id="97e3a-131">**Windows 앱 설정 동기화 안 함:** UE-V가 Windows 앱을 동기화 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-131">**Don’t Sync Windows App Settings:** Specifies that UE-V should not synchronize Windows apps.</span></span>

-   <span data-ttu-id="97e3a-132">**첫 번째 사용 알림 사용/사용 안 함:** 사용자의 컴퓨터에서 UE-V Agent가 처음 실행 될 때 UE-V가 대화 상자를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-132">**Enable/Disable First Use Notification:** Specifies whether UE-V displays a dialog box the first time that the UE-V Agent runs on a user’s computer.</span></span>

-   <span data-ttu-id="97e3a-133">**트레이 아이콘 설정/해제:** UE-V가 알림 영역에 아이콘을 표시할지 여부와 연결 된 알림을 표시할지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-133">**Enable/Disable Tray Icon:** Specifies whether UE-V displays an icon in the notification area and any notifications associated with it.</span></span> <span data-ttu-id="97e3a-134">아이콘은 회사 설정 센터에 대 한 링크를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-134">The icon provides a link to the Company Settings Center.</span></span>

-   <span data-ttu-id="97e3a-135">**사용자 지정 연락처 하이퍼링크:** 회사 설정 센터에서 **IT 대화 상대** 하이퍼링크에 대 한 경로, 텍스트 및 설명을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e3a-135">**Custom Contact IT Hyperlink:** Defines the path, text, and description for the **Contact IT** hyperlink in the Company Settings Center.</span></span>






## <span data-ttu-id="97e3a-136">관련 항목</span><span class="sxs-lookup"><span data-stu-id="97e3a-136">Related topics</span></span>


[<span data-ttu-id="97e3a-137">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="97e3a-137">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="97e3a-138">UE-V 2.x에 대한 필수 기능 배포</span><span class="sxs-lookup"><span data-stu-id="97e3a-138">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="97e3a-139">사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포</span><span class="sxs-lookup"><span data-stu-id="97e3a-139">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





