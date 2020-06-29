---
title: MBAM 서버 기능 또는 소프트웨어 제거
description: MBAM 서버 기능 또는 소프트웨어 제거
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824978"
---
# <span data-ttu-id="16f43-103">MBAM 서버 기능 또는 소프트웨어 제거</span><span class="sxs-lookup"><span data-stu-id="16f43-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="16f43-104">이 지침에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM)에서 소프트웨어와 기능을 제거 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="16f43-105">MBAM 서버 기능을 제거 하는 경우 구성 된 기능만 MBAM 서버 소프트웨어가 아닌 서버에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="16f43-106">MBAM 서버 소프트웨어를 제거 하면 해당 서버에서 구성한 소프트웨어와 모든 MBAM 서버 기능이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="16f43-107">**참고**  데이터가 실수로 제거 되는 것을 방지 하기 위해 MBAM은 데이터베이스를 제거 하는 메커니즘을 제공 하지 않습니다. 수동으로 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="16f43-108">MBAM 서버 기능 제거</span><span class="sxs-lookup"><span data-stu-id="16f43-108">Removing MBAM Server features</span></span>


<span data-ttu-id="16f43-109">다음 방법 중 하나를 사용 하 여 구성한 MBAM 서버 기능을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="16f43-110">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="16f43-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="16f43-111">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="16f43-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="16f43-112">MBAM 서버 구성 마법사를 사용 하 여 기능 제거</span><span class="sxs-lookup"><span data-stu-id="16f43-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="16f43-113">이 지침에 따라 MBAM 서버 구성 마법사를 사용 하 여 서버에서 구성 된 MBAM 서버 기능을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="16f43-114">마법사를 사용 하 여 MBAM 기능을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="16f43-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="16f43-115">기능을 제거 하려는 서버에서 **Mbam 서버 구성을** 선택 하 여 구성 마법사를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="16f43-116">**기능 제거**를 클릭 하 고 제거할 기능을 선택한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="16f43-117">제거를 위해 선택한 기능이 **요약** 페이지에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="16f43-118">**제거** 를 클릭 하 여 기능 제거를 시작 하 고 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="16f43-119">Windows PowerShell을 사용 하 여 기능 제거</span><span class="sxs-lookup"><span data-stu-id="16f43-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="16f43-120">Windows PowerShell cmdlet을 사용 하 여 MBAM 서버 기능을 제거 하는 일반적인 지침으로 다음 단계를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="16f43-121">Windows PowerShell을 사용 하 여 MBAM 기능을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="16f43-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="16f43-122">기능을 제거 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16f43-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="16f43-123">다음 cmdlet을 사용 하 여 MBAM 서버 기능을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="16f43-124">사용 안 함-MbamReport</span><span class="sxs-lookup"><span data-stu-id="16f43-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="16f43-125">Disable-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="16f43-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="16f43-126">사용 안 함-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="16f43-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="16f43-127">Windows powershell cmdlet에 대 한 도움말을 보려면 **get-help** &lt; *cmdlet* 을 입력 &gt; 하거나, mbam windows powershell cmdlet에 대해 [Windows PowerShell 페이지를 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화](https://go.microsoft.com/fwlink/?LinkId=393498) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16f43-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="16f43-128">MBAM 서버 소프트웨어 제거</span><span class="sxs-lookup"><span data-stu-id="16f43-128">Removing MBAM Server software</span></span>


<span data-ttu-id="16f43-129">다음 단계를 사용 하 여 MBAM 서버 소프트웨어와 해당 서버에서 구성한 모든 MBAM 서버 기능을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="16f43-130">MBAM 서버 소프트웨어를 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="16f43-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="16f43-131">MBAM 서버 소프트웨어를 제거 하려는 서버에서 **MBAMserversetup.exe** 를 실행 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="16f43-132">**제거**를 선택 하 고 나머지 메시지에 따라 Mbam 서버 소프트웨어 제거 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="16f43-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="16f43-133">Related topics</span></span>


[<span data-ttu-id="16f43-134">MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="16f43-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="16f43-135">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="16f43-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="16f43-136">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="16f43-137">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f43-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



