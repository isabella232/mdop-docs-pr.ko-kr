---
title: UE-V 2. x에 대 한 회사 설정 센터 구성
description: UE-V 2. x에 대 한 회사 설정 센터 구성
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823293"
---
# <span data-ttu-id="27bf3-103">UE-V 2. x에 대 한 회사 설정 센터 구성</span><span class="sxs-lookup"><span data-stu-id="27bf3-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="27bf3-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1에는 사용자가 동기화 할 설정을 관리 하는 데 도움이 되는 새 응용 프로그램 (예를 들어, 회사 설정 센터)이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="27bf3-105">회사 설정 센터는 UE-V Agent를 사용 하 여 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="27bf3-106">사용자는 제어판, **시작** 메뉴 또는 **시작** 화면에서, ue-v 알림 영역 아이콘을 통해 회사 설정 센터에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="27bf3-107">회사 설정 센터에서는 동기화 되는 설정을 표시 하 고 사용자가 UE-V의 동기화 상태를 볼 수 있도록 도와줍니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="27bf3-108">사용자는 회사 설정 센터를 사용 하 여 컴퓨터 간에 설정을 동기화 하는 응용 프로그램 또는 Windows 기능을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="27bf3-109">**지금 동기화** 단추를 클릭 하 여 모든 설정을 즉시 동기화 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="27bf3-110">또한 관리자는 회사 설정 센터에 지원 링크를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="27bf3-111">회사 설정 센터 정보</span><span class="sxs-lookup"><span data-stu-id="27bf3-111">About the Company Settings Center</span></span>


<span data-ttu-id="27bf3-112">회사 설정 센터 데스크톱 응용 프로그램은 사용자에 게 UE-V 설정 동기화에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="27bf3-113">회사 설정 센터에는 다양 한 방법으로 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="27bf3-114">알림 영역 아이콘 – **트레이 아이콘** 그룹 정책 설정 또는 Windows PowerShell 구성을 사용 하면 알림 영역에 ue-v 아이콘이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="27bf3-115">UE-V 아이콘을 클릭 하 여 회사 설정 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="27bf3-116">**참고**  다음 설정을 사용 하 여 알림 영역 아이콘을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="27bf3-117">그룹 정책 설정:</span><span class="sxs-lookup"><span data-stu-id="27bf3-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="27bf3-118">Windows PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27bf3-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="27bf3-119">SystemCenter2012 ConfigurationManager에 대 한 UE-V 구성 팩의 구성 항목:</span><span class="sxs-lookup"><span data-stu-id="27bf3-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="27bf3-120">제어판의 응용 프로그램-제어판에서 **모양 및 개인**설정을 찾아본 다음, **회사 설정 센터**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="27bf3-121">첫 번째 사용 알림-비활성화 하지 않는 한, UE-V Agent가 사용자에 게 이제 UE-V agent가 컴퓨터에서 처음 실행 될 때 동기화를 설정 한다는 알림을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="27bf3-122">알림 대화 상자를 클릭 하 여 회사 설정 센터를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="27bf3-123">**시작** 화면 또는 **시작** 메뉴에는 회사 설정 센터 링크가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="27bf3-124">회사 설정 검색 센터에서 응용 프로그램을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="27bf3-125">회사 설정 센터에서 지원 링크 구성</span><span class="sxs-lookup"><span data-stu-id="27bf3-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="27bf3-126">회사 설정 센터에는 사용자가 UE-V 설정 동기화 문제를 지원 하기 위해 클릭할 수 있는 하이퍼링크가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="27bf3-127">이 링크는 웹 페이지나 mailto://의 http://같은 유효한 URL 프로토콜 (예: 전자 메일)을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="27bf3-128">지원 링크는 그룹 정책, Windows PowerShell 또는 System Center 2012 Configuration Manager UE-V 구성 팩을 사용 하 여 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="27bf3-129">회사 설정 센터 지원 링크를 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="27bf3-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="27bf3-130">다음과 같이 원하는 관리 도구를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="27bf3-131">**그룹 정책** -아직 [MDOP 관리 템플릿에서](https://go.microsoft.com/fwlink/p/?LinkId=393941)ue-v 2에 대 한 ADMX 서식 파일을 다운로드 하지 않은 경우이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="27bf3-132">**Windows powershell** – ue-v agent가 설치 된 컴퓨터에서 **windows powershell**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="27bf3-133">Windows PowerShell을 사용 하 여 UE-V를 관리 하는 방법에 대 한 자세한 내용은 [Windows powershell 및 WMI에서 ue-v 2. x 관리](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27bf3-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="27bf3-134">**System Center 2012 MICROSOFT ue-v (User Experience Virtualization) 용 구성 팩** -Ue-v 구성 팩을 가져오고 구성 팩 문서를 따라 구성 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="27bf3-135">UE-V 구성 팩에 대 한 자세한 내용은 [System Center Configuration Manager 2012에서 ue-v 2. x 구성을](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27bf3-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="27bf3-136">다음 정책에 대 한 설정을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="27bf3-137">**It 담당자에 게 연결 텍스트** -이 설정은 회사 설정 센터에 있는 연락처 URL 하이퍼링크의 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="27bf3-138">이 설정을 사용 하면 회사 설정 센터에 연락처 URL에 대 한 링크에 지정 된 텍스트가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="27bf3-139">그룹 정책 설정:</span><span class="sxs-lookup"><span data-stu-id="27bf3-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="27bf3-140">Windows PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27bf3-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="27bf3-141">구성 팩 구성 항목:</span><span class="sxs-lookup"><span data-stu-id="27bf3-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="27bf3-142">**IT URL에 문의** -이 설정은 전자 메일의 웹 페이지 또는 mailto://에 대 한 http://같은 유효한 URL 프로토콜에서 회사 설정 센터의 연락처 링크에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="27bf3-143">그룹 정책 설정:</span><span class="sxs-lookup"><span data-stu-id="27bf3-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="27bf3-144">Windows PowerShell cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27bf3-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="27bf3-145">구성 팩 구성 항목:</span><span class="sxs-lookup"><span data-stu-id="27bf3-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="27bf3-146">관리 도구를 사용 하 여 사용자의 컴퓨터에 설정을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bf3-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





