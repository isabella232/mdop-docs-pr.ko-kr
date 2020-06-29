---
title: UE-V 2. x 배포 준비
description: UE-V 2. x 배포 준비
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826423"
---
# <span data-ttu-id="ba058-103">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="ba058-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="ba058-104">Microsoft UE-V (사용자 환경 가상화) 2.0 또는 2.1을 사용자가 엔터프라이즈에서 액세스 하는 장치 간에 설정을 동기화 하는 솔루션으로 배포 하기 전에 몇 가지 계획 및 준비를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="ba058-105">이 항목에서는 수행할 배포 유형 및 배포를 성공적으로 수행할 수 있는 준비 방법을 결정 하는 데 도움이 되는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="ba058-106">먼저 UE-V를 배포 하는 데 사용할 수 있는 작업을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="ba058-107">UE-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="ba058-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="ba058-108">배포 하기 전에 먼저 어떤 UE-V 기능을 배포할지 결정할 수 있도록 약간의 계획을 수행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="ba058-109">이 페이지를 나가면 아래 계획 정보를 읽어 보고 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="ba058-110">UE-V 2.x에 대한 필수 기능 배포</span><span class="sxs-lookup"><span data-stu-id="ba058-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="ba058-111">모든 UE-V 배포에는 다음 활동이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="ba058-112">설정 저장소 위치 정의</span><span class="sxs-lookup"><span data-stu-id="ba058-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="ba058-113">UE-V Agent를 배포 하 고 UE-V 구성을 관리 하는 방법 결정</span><span class="sxs-lookup"><span data-stu-id="ba058-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="ba058-114">설정이 동기화 되어야 하는 모든 사용자 컴퓨터에 [Ue-v Agent 설치](https://technet.microsoft.com/library/dn458891.aspx#agent)</span><span class="sxs-lookup"><span data-stu-id="ba058-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="ba058-115">선택적으로 [사용자 지정 응용 프로그램에 대 한 ue-v 2. x를 배포할](deploy-ue-v-2x-for-custom-applications-new-uevv2.md) 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="ba058-116">계획은 다음과 같은 UE-V 기능이 필요한 사용자 지정 응용 프로그램 (타사 또는 lob (기간 업무))의 설정 동기화를 지원 하도록 UE-V를 사용할지 여부를 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="ba058-117">[UEV 생성기를 설치](https://technet.microsoft.com/library/dn458942.aspx#uevgen) 하 여 사용자 지정 응용 프로그램 설정을 동기화 하는 데 필요한 사용자 지정 설정 위치 템플릿을 만들고 편집 하 고 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="ba058-118">UE-V 생성기를 사용 하 여 [사용자 지정 설정 위치 서식 파일 만들기](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates)</span><span class="sxs-lookup"><span data-stu-id="ba058-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="ba058-119">사용자 지정 설정 위치 템플릿을 저장 하는 데 사용 하는 [ue-v 설정 템플릿 카탈로그 배포](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)</span><span class="sxs-lookup"><span data-stu-id="ba058-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="ba058-120">이 워크플로 다이어그램은 UE-V 배포에 대 한 개략적인 수준의 이해와 엔터프라이즈에서 UE-V를 배포 하는 방법을 결정 하는 의사 결정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="ba058-122">**Ue-v 배포 계획:** 먼저 몇 가지 계획을 선택 하 여 배포할 UE-V 구성 요소를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="ba058-123">UE-V 배포 계획에는 다음 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="ba058-124">사용자 지정 응용 프로그램의 설정 동기화 여부 결정</span><span class="sxs-lookup"><span data-stu-id="ba058-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="ba058-125">이는 배포 중에 UE-V 생성기를 설치할지 여부를 결정 하며,이를 통해 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="ba058-126">이 작업에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-126">It involves the following:</span></span>

    <span data-ttu-id="ba058-127">[Ue-v 배포에서 자동으로 동기화 되는 설정을](#autosyncsettings)검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="ba058-128">[다른 응용 프로그램에 대해 설정 동기화가 필요한 지 여부를 결정](#determinesettingssync)합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="ba058-129">고가용성 및 용량 계획과 같은 [ue-v 배포에 대 한 기타 고려 사항을](#considerations)검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="ba058-130">UE-V의 필수 구성 요소 및 지원 되는 구성 확인</span><span class="sxs-lookup"><span data-stu-id="ba058-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="ba058-131">사용자 지정 응용 프로그램의 설정 동기화 여부 결정</span><span class="sxs-lookup"><span data-stu-id="ba058-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="ba058-132">UE-V 배포의 경우 여러 설정이 자동으로 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="ba058-133">그러나 UE-V를 사용자 지정 하 여 lob (기간 업무) 및 타사 앱 등의 다른 응용 프로그램에 대 한 설정을 동기화 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="ba058-134">UE-V를 통해 사용자 지정 응용 프로그램의 설정을 동기화 하도록 할지 결정 하는 것이 UE-V 배포 계획의 가장 중요 한 부분입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="ba058-135">이 섹션의 항목은 해당 결정을 내리는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="ba058-136">UE-V 배포에서 자동으로 동기화 되는 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="ba058-137">이 섹션에서는 다음을 포함 하 여 기본적으로 UE-V에서 동기화 되는 설정에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="ba058-138">설정이 기본적으로 동기화 되는 데스크톱 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="ba058-139">기본적으로 동기화 되는 Windows 바탕 화면 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="ba058-140">Windows 앱 설정 동기화에 대 한 지원 문</span><span class="sxs-lookup"><span data-stu-id="ba058-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="ba058-141">UE-V를 통해 동기화 되는 특정 Microsoft Office 2013, Microsoft Office 2010 및 Microsoft Office 2007 설정의 전체 목록을 다운로드 하려면 [Microsoft office 용 ue-v (User Experience Virtualization) 설정 템플릿을](https://www.microsoft.com/download/details.aspx?id=46367) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="ba058-142">UE-V 2.1 및 UE-V 2.1 SP1에서 기본적으로 동기화 된 데스크톱 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="ba058-143">UE-V 2.1 또는 2.1 SP1 에이전트를 설치 하면 이러한 공통 Microsoft 응용 프로그램에 대 한 설정 값을 캡처하는 기본 설정 위치 템플릿 그룹이 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="ba058-144">팁</span><span class="sxs-lookup"><span data-stu-id="ba058-144">Tip</span></span>**  
<span data-ttu-id="ba058-145">**Microsoft Office 2007 설정 동기화** – ue-v 2.1 및 2.1 SP1에서는 설정 위치 템플릿이 Office 2007 응용 프로그램에 기본적으로 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="ba058-146">그러나 UE-V 2.0 또는 이전 버전의 Office 2007 서식 파일을 계속 사용할 수 있으며 [ue-v 서식 파일 갤러리](https://go.microsoft.com/fwlink/p/?LinkID=246589)에서 서식 파일을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ba058-147">응용 프로그램 범주</span><span class="sxs-lookup"><span data-stu-id="ba058-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-148">설명</span><span class="sxs-lookup"><span data-stu-id="ba058-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-149">Microsoft Office 2010 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="ba058-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</span><span class="sxs-lookup"><span data-stu-id="ba058-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="ba058-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="ba058-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="ba058-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="ba058-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="ba058-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="ba058-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="ba058-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="ba058-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="ba058-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="ba058-161">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="ba058-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="ba058-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-164">Microsoft Office 2013 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="ba058-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</span><span class="sxs-lookup"><span data-stu-id="ba058-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="ba058-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="ba058-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="ba058-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="ba058-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="ba058-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="ba058-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="ba058-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="ba058-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="ba058-175">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="ba058-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="ba058-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="ba058-178">Microsoft Office 2013 업로드 센터</span><span class="sxs-lookup"><span data-stu-id="ba058-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="ba058-179">Microsoft 비즈니스용 OneDrive 2013</span><span class="sxs-lookup"><span data-stu-id="ba058-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="ba058-180">UE-V 2.1 및 2.1 SP1 Microsoft Office 2013 설정 위치 템플릿에는 향상 된 Outlook 서명 지원이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="ba058-181">새, 회신 및 전달 된 전자 메일에 대 한 기본 서명 설정을 동기화 했습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ba058-182">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-182">Note</span></span></strong><br/><p><span data-ttu-id="ba058-183">Outlook 프로필은 사용자가 Outlook 서명을 동기화 하려는 모든 장치에 대해 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="ba058-184">프로필이 아직 만들어지지 않은 경우 사용자가 프로필을 만든 다음 해당 장치에서 Outlook을 다시 시작 하 여 서명 동기화를 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-185">브라우저 옵션: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 및 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="ba058-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-186">즐겨찾기, 홈 페이지, 탭, 도구 모음</span><span class="sxs-lookup"><span data-stu-id="ba058-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ba058-187">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-187">Note</span></span></strong><br/><p><span data-ttu-id="ba058-188">UE-V는 Internet Explorer 쿠키에 대 한 설정을 로밍 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-189">Windows 액세서리</span><span class="sxs-lookup"><span data-stu-id="ba058-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-190">Microsoft 계산기, 메모장, 워드 패드</span><span class="sxs-lookup"><span data-stu-id="ba058-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ba058-191">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-191">Note</span></span>**  
<span data-ttu-id="ba058-192">UE-V 2.1 SP1은 Windows 10의 Microsoft 계산기와 이전 운영 체제의 Microsoft 계산기 간에 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="ba058-193">UE-V 2.0에서 기본적으로 동기화 된 데스크톱 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="ba058-194">UE-V 2.0 Agent를 설치 하면 이러한 공통 Microsoft 응용 프로그램에 대 한 설정 값을 캡처하는 기본 설정 위치 템플릿 그룹이 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="ba058-195">팁</span><span class="sxs-lookup"><span data-stu-id="ba058-195">Tip</span></span>**  
<span data-ttu-id="ba058-196">**Microsoft office 2013 설정 동기화** – ue-v 2.0에서는 설정 위치 템플릿이 Office 2013 응용 프로그램에 기본적으로 포함 되어 있지 않지만 [ue-v 템플릿 갤러리](https://go.microsoft.com/fwlink/p/?LinkID=246589)에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="ba058-197">[Office 2013를 ue-v 2.0와 동기화](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) 하면 office 2013 설정을 동기화 하는 지원 되는 서식 파일에 대 한 세부 정보가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ba058-198">응용 프로그램 범주</span><span class="sxs-lookup"><span data-stu-id="ba058-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-199">설명</span><span class="sxs-lookup"><span data-stu-id="ba058-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-200">Microsoft Office 2007 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="ba058-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</span><span class="sxs-lookup"><span data-stu-id="ba058-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="ba058-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="ba058-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="ba058-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="ba058-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="ba058-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="ba058-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="ba058-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="ba058-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="ba058-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="ba058-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="ba058-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="ba058-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-214">Microsoft Office 2010 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="ba058-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> 동기화 된 모든 설정 목록 다운로드 </a> )</span><span class="sxs-lookup"><span data-stu-id="ba058-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="ba058-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="ba058-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="ba058-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="ba058-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="ba058-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="ba058-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="ba058-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="ba058-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="ba058-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="ba058-226">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="ba058-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="ba058-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="ba058-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-229">브라우저 옵션: Internet Explorer 8, Internet Explorer 9 및 Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="ba058-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-230">즐겨찾기, 홈 페이지, 탭, 도구 모음</span><span class="sxs-lookup"><span data-stu-id="ba058-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ba058-231">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-231">Note</span></span></strong><br/><p><span data-ttu-id="ba058-232">UE-V는 Internet Explorer 쿠키에 대 한 설정을 로밍 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-233">Windows 액세서리</span><span class="sxs-lookup"><span data-stu-id="ba058-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-234">Microsoft 계산기, 메모장, 워드 패드</span><span class="sxs-lookup"><span data-stu-id="ba058-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="ba058-235">Windows 설정이 기본적으로 동기화 됨</span><span class="sxs-lookup"><span data-stu-id="ba058-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="ba058-236">UE-V는 이러한 Windows 설정에 대 한 설정 값을 캡처하는 설정 위치 템플릿을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba058-237">Windows 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="ba058-238">설명</span><span class="sxs-lookup"><span data-stu-id="ba058-238">Description</span></span></th>
<th align="left"><span data-ttu-id="ba058-239">적용 기준</span><span class="sxs-lookup"><span data-stu-id="ba058-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="ba058-240">으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="ba058-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="ba058-241">기본 상태</span><span class="sxs-lookup"><span data-stu-id="ba058-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-242">바탕 화면 배경</span><span class="sxs-lookup"><span data-stu-id="ba058-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-243">현재 활성 상태인 바탕 화면 배경 또는 배경 무늬</span><span class="sxs-lookup"><span data-stu-id="ba058-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-244">로그온, 잠금 해제, 원격 연결, 예약 된 작업 이벤트</span><span class="sxs-lookup"><span data-stu-id="ba058-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-245">로그 오프, 잠금, 원격 연결 끊기, 사용자가 <strong> </strong> 회사 설정 센터에서 지금 동기화 클릭 또는 예약 된 작업 간격</span><span class="sxs-lookup"><span data-stu-id="ba058-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-246">설정됨</span><span class="sxs-lookup"><span data-stu-id="ba058-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-247">접근성</span><span class="sxs-lookup"><span data-stu-id="ba058-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-248">접근성 및 입력 설정, Microsoft 돋보기, 내레이터, 화상 키보드.</span><span class="sxs-lookup"><span data-stu-id="ba058-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-249">로그온만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-250">로그 오프, 사용자가 <strong> 지금 </strong> 회사 설정 센터에서 동기화 클릭 또는 예약 된 작업 간격</span><span class="sxs-lookup"><span data-stu-id="ba058-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-251">설정됨</span><span class="sxs-lookup"><span data-stu-id="ba058-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-252">바탕 화면 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-253">시작 메뉴 및 작업 표시줄 설정, 폴더 옵션, 기본 바탕 화면 아이콘, 추가 시계, 지역 및 언어 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-254">로그온만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-255">로그 오프, 사용자가 <strong> </strong> 회사 설정 센터에서 지금 동기화 또는 예약 된 작업을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-256">설정됨</span><span class="sxs-lookup"><span data-stu-id="ba058-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ba058-257">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-257">Note</span></span>**  
<span data-ttu-id="ba058-258">Windows 8부터 UE-V는 시작 화면 (예: 항목 및 위치)과 관련 된 설정을 로밍 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="ba058-259">또한 UE-V는 고정 된 작업 표시줄 항목 또는 Windows 파일 바로 가기의 동기화를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="ba058-260">중요</span><span class="sxs-lookup"><span data-stu-id="ba058-260">Important</span></span>**  
<span data-ttu-id="ba058-261">UE-V 2.1 SP1은 Windows 10 장치 간의 작업 표시줄 설정을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="ba058-262">그러나 UE-V는 이전 운영 체제를 실행 하는 Windows 10 장치 및 장치 간에 작업 표시줄 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba058-263">설정 그룹</span><span class="sxs-lookup"><span data-stu-id="ba058-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="ba058-264">범주</span><span class="sxs-lookup"><span data-stu-id="ba058-264">Category</span></span></th>
<th align="left"><span data-ttu-id="ba058-265">캡처하면</span><span class="sxs-lookup"><span data-stu-id="ba058-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="ba058-266">적용</span><span class="sxs-lookup"><span data-stu-id="ba058-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ba058-267">응용 프로그램 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ba058-268">Windows 앱  </span><span class="sxs-lookup"><span data-stu-id="ba058-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-269">앱 닫기</span><span class="sxs-lookup"><span data-stu-id="ba058-269">Close app</span></span></p>
<p><span data-ttu-id="ba058-270">Windows 앱 설정 변경 이벤트</span><span class="sxs-lookup"><span data-stu-id="ba058-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-271">시작 시 UE-V App Monitor 시작</span><span class="sxs-lookup"><span data-stu-id="ba058-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="ba058-272">앱 열기</span><span class="sxs-lookup"><span data-stu-id="ba058-272">Open app</span></span></p>
<p><span data-ttu-id="ba058-273">Windows 앱 설정 변경 이벤트</span><span class="sxs-lookup"><span data-stu-id="ba058-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="ba058-274">설정 패키지 도착</span><span class="sxs-lookup"><span data-stu-id="ba058-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ba058-275">데스크톱 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ba058-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-276">응용 프로그램이 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-277">응용 프로그램이 열리고 닫힙니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ba058-278">바탕 화면 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ba058-279">바탕 화면 배경</span><span class="sxs-lookup"><span data-stu-id="ba058-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-280">잠금 또는 로그 오프</span><span class="sxs-lookup"><span data-stu-id="ba058-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-281">로그온, 잠금 해제, 원격 연결, 새 패키지 도착에 대 한 알림, 지금 사용자가 <strong> </strong> 회사 설정 센터에서 동기화 클릭 또는 예약 된 작업 실행을 진행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ba058-282">접근성 (공통 – 접근성, 내레이터, 돋보기, 화상 키보드)</span><span class="sxs-lookup"><span data-stu-id="ba058-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-283">잠금 또는 로그 오프</span><span class="sxs-lookup"><span data-stu-id="ba058-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-284">로그온</span><span class="sxs-lookup"><span data-stu-id="ba058-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ba058-285">접근성 (셸-오디오, 접근성, 키보드, 마우스)</span><span class="sxs-lookup"><span data-stu-id="ba058-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-286">잠금 또는 로그 오프</span><span class="sxs-lookup"><span data-stu-id="ba058-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-287">로그온, 잠금 해제, 원격 연결, 새 패키지 도착에 대 한 알림, 지금 사용자가 <strong> </strong> 회사 설정 센터에서 동기화 클릭 또는 예약 된 작업 실행</span><span class="sxs-lookup"><span data-stu-id="ba058-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ba058-288">바탕 화면 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-289">잠금 또는 로그 오프</span><span class="sxs-lookup"><span data-stu-id="ba058-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-290">로그온</span><span class="sxs-lookup"><span data-stu-id="ba058-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="ba058-291">UE-V-Windows 앱에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="ba058-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="ba058-292">Windows 앱의 경우 앱 개발자는 동기화 되는 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="ba058-293">설정 동기화를 사용 하도록 설정 된 Windows 앱을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="ba058-294">Windows PowerShell 명령 프롬프트에서 컴퓨터의 설정을 동기화 할 수 있는 Windows 앱 목록 (패키지 패밀리 이름, 사용 상태 및 활성화 된 원본)을 표시 하려면 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="ba058-295">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-295">Note</span></span>**  
<span data-ttu-id="ba058-296">Windows 8에서 UE-V는 도메인 사용자가 로그인 자격 증명을 Microsoft 계정에 연결 하는 경우 Windows 앱 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="ba058-297">이 링크는 Windows 앱 설정 동기화를 사용 하지 않도록 설정을 Microsoft OneDrive에 동기화 합니다 (UE-V-V).</span><span class="sxs-lookup"><span data-stu-id="ba058-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="ba058-298">UE-V-로밍 프린터 지원</span><span class="sxs-lookup"><span data-stu-id="ba058-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="ba058-299">UE-V 2.1 SP1에서는 네트워크 프린터가 네트워크의 모든 장치에 로그온 되어 있는 경우 사용자가 네트워크 프린터에 액세스할 수 있도록 디바이스 간에 로밍이 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="ba058-300">여기에는 기본값으로 설정 된 프린터를 로밍 하는 것이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="ba058-301">UE-V의 Printer 로밍에는 다음 시나리오 중 하나가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="ba058-302">인쇄 서버는 새 장치로 로밍할 때 필요한 드라이버를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="ba058-303">로밍 네트워크 프린터용 드라이버는 해당 네트워크 프린터에 액세스 해야 하는 모든 장치에 사전 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="ba058-304">프린터 드라이버는 Windows 업데이트에서 구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="ba058-305">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-305">Note</span></span>**  
<span data-ttu-id="ba058-306">UE-V 프린터 로밍 기능은 양면 인쇄와 같은 프린터 설정이 나 기본 **설정을 로밍하지 않습니다** .</span><span class="sxs-lookup"><span data-stu-id="ba058-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="ba058-307">다른 응용 프로그램에 대해 동기화 된 설정이 필요한 지 여부 결정</span><span class="sxs-lookup"><span data-stu-id="ba058-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="ba058-308">UE-V 배포에서 자동으로 동기화 되는 설정을 검토 한 후에는 다른 응용 프로그램에 대 한 설정을 동기화할지 여부를 결정 하 여 엔터프라이즈 전체에서 UE-V를 배포 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="ba058-309">관리자는 UE-V 솔루션에 포함할 데스크톱 응용 프로그램을 고려 하는 경우 사용자가 지정할 수 있는 설정 및 응용 프로그램이 해당 설정을 저장 하는 방법 및 위치를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="ba058-310">일부 데스크톱 응용 프로그램은 사용자 지정할 수 있는 설정을 포함 하지 않으며, 사용자가 일상적으로 사용자 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="ba058-311">또한, 모든 데스크톱 응용 프로그램 설정을 여러 컴퓨터 또는 환경에서 안전 하 게 동기화 할 수 있는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="ba058-312">일반적으로 다음 조건을 충족 하는 설정을 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="ba058-313">사용자가 액세스할 수 있는 위치에 저장 되는 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="ba058-314">예를 들어 System32 또는 레지스트리의 HKEY \ _CURRENT \ _USER (HKCU) 섹션 외부에 저장 된 설정을 동기화 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="ba058-315">특정 컴퓨터에 국한 되지 않는 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="ba058-316">예를 들어 네트워크 또는 하드웨어 구성을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="ba058-317">데이터 손상 위험 없이 컴퓨터 간에 동기화 될 수 있는 설정</span><span class="sxs-lookup"><span data-stu-id="ba058-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="ba058-318">예를 들어 데이터베이스 파일에 저장 된 설정을 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="ba058-319">사용자 지정 응용 프로그램 평가를 위한 검사 목록</span><span class="sxs-lookup"><span data-stu-id="ba058-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="ba058-320">다른 응용 프로그램에 대해 동기화가 설정 되어 있어야 하는 경우이 검사 목록을 사용 하 여 포함할 응용 프로그램을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="ba058-321">설명</span><span class="sxs-lookup"><span data-stu-id="ba058-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-322">이 응용 프로그램에 사용자가 사용자 지정할 수 있는 설정이 포함 되어 있습니까?</span><span class="sxs-lookup"><span data-stu-id="ba058-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-323">사용자가 이러한 설정을 동기화 하는 것이 중요 한가요?</span><span class="sxs-lookup"><span data-stu-id="ba058-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-324">이러한 사용자 설정이 응용 프로그램 관리 또는 설정 정책 솔루션에 의해 이미 관리 되나요?</span><span class="sxs-lookup"><span data-stu-id="ba058-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="ba058-325">UE-V는 로그온, 잠금 해제 또는 원격 연결 이벤트의 응용 프로그램 시작 및 Windows 설정에 대 한 응용 프로그램 설정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="ba058-326">다른 설정 공유 솔루션과 함께 UE-V를 사용 하는 경우 사용자가 동기화 된 설정 간에 일관성 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-327">컴퓨터에 대 한 응용 프로그램 설정이 있나요?</span><span class="sxs-lookup"><span data-stu-id="ba058-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="ba058-328">하드웨어 또는 특정 컴퓨터 구성과 연결 된 응용 프로그램 기본 설정 및 사용자 지정은 세션 간에 일관성 없이 동기화 되므로 응용 프로그램 환경이 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-329">Application Files directory 또는 사용자의 파일 디렉터리 (사용자 <strong> </strong> 이름]에 &lt; 강력한 &gt; AppData </strong> &lt; 강력한 &gt; </strong> locallow에 저장 되어 있는 응용 프로그램의 설정을 사용 합니까?</span><span class="sxs-lookup"><span data-stu-id="ba058-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="ba058-330">이러한 위치 중 하나에 저장 된 응용 프로그램 데이터는 해당 컴퓨터에 대 한 정보를 포함 하거나 데이터가 너무 커서 동기화 할 수 없기 때문에 사용자와 동기화 되지 않는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-331">응용 프로그램이 동기화 하지 않아야 하는 다른 응용 프로그램 데이터를 포함 하는 파일에 대 한 설정을 저장 합니까?</span><span class="sxs-lookup"><span data-stu-id="ba058-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="ba058-332">UE-V는 파일을 단일 단위로 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="ba058-333">설정이 아닌 다른 응용 프로그램 데이터를 포함 하는 파일에 설정을 저장 한 경우이 추가 데이터를 동기화 하면 응용 프로그램 환경이 잘못 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ba058-334">설정이 포함 된 파일의 크기</span><span class="sxs-lookup"><span data-stu-id="ba058-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="ba058-335">설정 동기화의 성능은 크기가 큰 파일의 영향을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="ba058-336">큰 파일을 포함 하면 설정 동기화의 성능에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="ba058-337">UE-V 배포를 준비할 때 고려해 야 할 사항</span><span class="sxs-lookup"><span data-stu-id="ba058-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="ba058-338">UE-V를 배포 하려고 준비 하는 경우에도 다음 사항을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="ba058-339">자격 증명 동기화 관리</span><span class="sxs-lookup"><span data-stu-id="ba058-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="ba058-340">Windows 앱 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="ba058-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="ba058-341">사용자 지정 UE-V 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="ba058-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="ba058-342">의도 하지 않은 사용자 설정 구성</span><span class="sxs-lookup"><span data-stu-id="ba058-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="ba058-343">성능 및 용량</span><span class="sxs-lookup"><span data-stu-id="ba058-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="ba058-344">고가용성</span><span class="sxs-lookup"><span data-stu-id="ba058-344">High availability</span></span>](#high)

-   [<span data-ttu-id="ba058-345">컴퓨터 시계 동기화</span><span class="sxs-lookup"><span data-stu-id="ba058-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="ba058-346">UE-V 2.1 및 UE-V 2.1 SP1의 자격 증명 동기화 관리</span><span class="sxs-lookup"><span data-stu-id="ba058-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="ba058-347">Microsoft Outlook 및 Lync를 비롯 한 많은 엔터프라이즈 응용 프로그램은 로그인 시 사용자에 게 도메인 자격 증명을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="ba058-348">사용자는 해당 자격 증명을 디스크에 저장 하 여 해당 응용 프로그램을 열 때마다 입력할 필요가 없도록 하는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="ba058-349">로밍 자격 증명 동기화를 사용 하도록 설정 하면 사용자가 한 컴퓨터에 자격 증명을 저장 하 고 해당 환경에서 사용 하는 모든 컴퓨터에 다시 입력 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="ba058-350">사용자는 일부 도메인 자격 증명을 UE-V 2.1 및 2.1 SP1과 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="ba058-351">중요</span><span class="sxs-lookup"><span data-stu-id="ba058-351">Important</span></span>**  
<span data-ttu-id="ba058-352">자격 증명 동기화는 기본적으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="ba058-353">이 기능을 구현 하려면 배포 중에 자격 증명 동기화를 명시적으로 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="ba058-354">UE-V 2.1 및 2.1 SP1은 엔터프라이즈 자격 증명을 동기화 할 수 있지만, 로컬 컴퓨터 에서만 사용 하도록 설정 된 자격 증명은 로밍되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="ba058-355">자격 증명은 동기화 설정 이므로 UE-V가 동기화 된 후 처음으로 컴퓨터에 로그인 할 때 프로필에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="ba058-356">자격 증명 동기화는 해당 설정 위치 템플릿에서 관리 되며 기본적으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="ba058-357">다른 서식 파일에 사용 되는 것과 동일한 방법으로이 서식 파일을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="ba058-358">이 기능에 대 한 서식 파일 식별자는 RoamingCredentialSettings입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="ba058-359">중요</span><span class="sxs-lookup"><span data-stu-id="ba058-359">Important</span></span>**  
<span data-ttu-id="ba058-360">환경에서 Active Directory 자격 증명 로밍을 사용 하는 경우 UE-V 자격 증명 로밍 서식 파일을 사용 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="ba058-361">다음 방법 중 하나를 사용 하 여 자격 증명 동기화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="ba058-362">회사 설정 센터</span><span class="sxs-lookup"><span data-stu-id="ba058-362">Company Settings Center</span></span>

-   <span data-ttu-id="ba058-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba058-363">PowerShell</span></span>

-   <span data-ttu-id="ba058-364">그룹 정책</span><span class="sxs-lookup"><span data-stu-id="ba058-364">Group Policy</span></span>

**<span data-ttu-id="ba058-365">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-365">Note</span></span>**  
<span data-ttu-id="ba058-366">동기화 하는 동안 자격 증명이 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="ba058-367">[회사 설정 센터](https://technet.microsoft.com/library/dn458903.aspx)**:** Windows 설정 아래의 로밍 자격 증명 설정 확인란을 선택 하 여 자격 증명 동기화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="ba058-368">확인란의 선택을 취소 하 여 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="ba058-369">이 확인란은 계정이 Microsoft 계정을 사용 하 여 설정을 동기화 하도록 구성 되어 있지 않은 경우 회사 설정 센터에만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="ba058-370">[Powershell](https://technet.microsoft.com/library/dn458937.aspx)**:** 이 PowerShell cmdlet은 자격 증명 동기화를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="ba058-371">이 PowerShell cmdlet은 자격 증명 동기화를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="ba058-372">[그룹 정책](https://technet.microsoft.com/library/dn458893.aspx)**:** 그룹 정책을 통해 자격 증명 동기화를 사용 하도록 설정 하려면 [최신 MDOP ADMX 템플릿을 배포](https://go.microsoft.com/fwlink/p/?LinkId=393944) 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="ba058-373">자격 증명 동기화는 Windows 설정으로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="ba058-374">그룹 정책을 사용 하 여이 기능을 관리 하려면 Windows 동기화 설정 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="ba058-375">그룹 정책 편집기를 열고 **사용자 구성 – 관리 템플릿 (Windows 구성 요소-Microsoft 사용자 환경 가상화**)으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="ba058-376">**Windows 설정 동기화**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="ba058-377">이 정책을 사용 하는 경우 **로밍 자격 증명** 확인란을 선택 하 여 자격 증명 동기화를 사용 하도록 설정 하거나, 선택을 취소 하 여 자격 증명 동기화를 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="ba058-378">**확인**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-378">Click **OK**.</span></span>

### <span data-ttu-id="ba058-379">UE-V를 통해 동기화 된 자격 증명 위치</span><span class="sxs-lookup"><span data-stu-id="ba058-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="ba058-380">응용 프로그램에서 다음 위치로 저장 한 자격 증명 파일이 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="ba058-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="ba058-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="ba058-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="ba058-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="ba058-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="ba058-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="ba058-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="ba058-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="ba058-385">다른 위치에 저장 된 자격 증명은 UE-V를 통해 동기화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="ba058-386">Windows 앱 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="ba058-386">Windows app settings synchronization</span></span>

<span data-ttu-id="ba058-387">UE-V는 다음 세 가지 방법으로 Windows 앱 설정 동기화를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="ba058-388">**Windows 앱 동기화:** 모든 Windows 앱 동기화 허용 또는 거부</span><span class="sxs-lookup"><span data-stu-id="ba058-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="ba058-389">**Windows 앱 목록:** Windows 앱 목록 동기화</span><span class="sxs-lookup"><span data-stu-id="ba058-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="ba058-390">**목록에 없는 기본 동기화 동작:** Windows 앱 목록에 없는 Windows 앱의 동기화 동작을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="ba058-391">자세한 내용은 [Windows 앱 목록을](https://technet.microsoft.com/library/dn458925.aspx#win8applist)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="ba058-392">사용자 지정 UE-V 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="ba058-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="ba058-393">사용자 지정 응용 프로그램의 설정을 동기화 하기 위해 UE-V를 배포 하는 경우 UE-V 생성기를 사용 하 여 해당 데스크톱 응용 프로그램에 대 한 사용자 지정 설정 위치 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="ba058-394">테스트 환경에서 사용자 지정 설정 위치 템플릿을 만들고 테스트 한 후 엔터프라이즈의 컴퓨터에 설정 위치 템플릿을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="ba058-395">사용자 지정 설정 위치 템플릿은 시스템 센터 구성 관리자, 환경 설정, UE-V 설정 템플릿 카탈로그 구성 등의 ESD (엔터프라이즈 소프트웨어 배포) 메서드 같은 기존 배포 인프라를 사용 하 여 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="ba058-396">구성 관리자 또는 그룹 정책을 사용 하 여 배포 된 템플릿은 UE-V WMI 또는 Windows PowerShell을 사용 하 여 등록 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="ba058-397">사용자 지정 설정 위치 서식 파일에 대 한 자세한 내용은 [사용자 지정 응용 프로그램에 ue-v: x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="ba058-398">구성 관리자에서 UE-V를 사용 하는 방법에 대 한 자세한 내용은 [System Center Configuration Manager 2012에서 ue-v 2. x 구성을](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="ba058-399">의도 하지 않은 사용자 설정 구성 방지</span><span class="sxs-lookup"><span data-stu-id="ba058-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="ba058-400">UE-V는 설정 저장소 위치에서 새 사용자 설정 정보를 다운로드 하 고 다음 인스턴스의 설정을 로컬 컴퓨터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="ba058-401">등록 된 UE-V 템플릿이 있는 응용 프로그램이 시작 될 때마다</span><span class="sxs-lookup"><span data-stu-id="ba058-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="ba058-402">사용자가 컴퓨터에 로그온 하는 경우</span><span class="sxs-lookup"><span data-stu-id="ba058-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="ba058-403">사용자가 컴퓨터의 잠금을 해제 하는 경우</span><span class="sxs-lookup"><span data-stu-id="ba058-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="ba058-404">UE-V를 설치한 원격 데스크톱 컴퓨터에 연결 하는 경우</span><span class="sxs-lookup"><span data-stu-id="ba058-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="ba058-405">동기화 컨트롤러 응용 프로그램 예약 된 작업이 실행 되는 경우</span><span class="sxs-lookup"><span data-stu-id="ba058-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="ba058-406">컴퓨터 A 및 컴퓨터 B에 UE-V를 설치한 경우 응용 프로그램에 대해 원하는 설정이 컴퓨터 A에 있으면 컴퓨터 A가 먼저 응용 프로그램을 열고 닫아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="ba058-407">컴퓨터 B에서 응용 프로그램을 열고 닫은 경우 컴퓨터 A의 응용 프로그램 설정이 컴퓨터 B의 응용 프로그램 설정으로 구성 됩니다. 설정은 응용 프로그램 별로 컴퓨터 간에 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="ba058-408">시간이 지남에 따라 기본 설정으로 컴퓨터를 열고 닫을 때의 설정이 일관 되 게 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="ba058-409">이 시나리오는 Windows 설정에도 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="ba058-410">컴퓨터 B의 Windows 설정이 컴퓨터 A의 Windows 설정과 동일 해야 하는 경우 사용자는 먼저 로그온 하 고 컴퓨터 A를 로그 오프 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="ba058-411">사용자가 원하는 사용자 설정이 잘못 된 순서로 적용 되는 경우 설정을 덮어쓴 컴퓨터에서 특정 응용 프로그램 또는 Windows 구성에 대 한 복원 작업을 수행 하 여 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="ba058-412">자세한 내용은 [ue-v on-V 2. x에서 관리 백업 및 복원 관리](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="ba058-413">성능 및 용량 계획</span><span class="sxs-lookup"><span data-stu-id="ba058-413">Performance and capacity planning</span></span>

<span data-ttu-id="ba058-414">표준 디스크 용량 및 네트워크 상태 모니터링을 통해 UE-V에 대 한 요구 사항을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="ba058-415">UE-V가 설정 패키지 저장소에 대 한 SMB (서버 메시지 블록) 공유를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="ba058-416">설정 패키지의 크기는 각 응용 프로그램의 설정 정보에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="ba058-417">대부분의 설정 패키지는 작지만 데스크톱 이미지와 같은 잠재적으로 크기가 큰 파일을 동기화 하면 성능이 저하 될 수 있으며, 특히 네트워크 속도가 느릴 때 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="ba058-418">네트워크 지연 문제를 줄이려면 사용자 컴퓨터가 있는 동일한 로컬 네트워크에 설정 저장소 위치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="ba058-419">설정 저장소 위치에 대해 사용자 당 20mb의 디스크 공간을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="ba058-420">기본적으로 UE-V 동기화는 2 초 후에 시간이 초과 되어 대규모 설정 패키지 때문에 과도 한 지연이 발생 하는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="ba058-421">[그룹 정책 개체](https://technet.microsoft.com/library/dn458893.aspx)를 사용 하 여 syncmethod = syncmethod 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="ba058-422">UE-V의 고가용성</span><span class="sxs-lookup"><span data-stu-id="ba058-422">High Availability for UE-V</span></span>

<span data-ttu-id="ba058-423">UE-V 설정 저장소 위치 및 설정 템플릿 카탈로그는 쓰기 가능한 공유에 사용자 데이터를 저장 하는 것을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="ba058-424">고가용성을 보장 하려면 다음 조건을 따르세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="ba058-425">NTFS 파일 시스템을 사용 하 여 저장소 볼륨을 포맷 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="ba058-426">공유에서 DFS (분산 파일 시스템)를 사용할 수 있지만 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="ba058-427">특히 dfs (분산 파일 시스템 이름) 네임 스페이스 (DFS-N)를 사용 하거나 사용할 수 없을 때 (예를 들어 Cd-r) 단일 대상 구성이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="ba058-428">마찬가지로, DFS-N에서는 단일 대상 구성만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="ba058-429">자세한 내용은 [복제 된 사용자 프로필 데이터에 대 한 Microsoft 지원 문의](https://go.microsoft.com/fwlink/p/?LinkId=313991) 및 [dfs 및 dfs 배포 시나리오에 대 한 microsoft 지원 정책에 대 한 정보](https://support.microsoft.com/kb/2533009)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="ba058-430">또한 SYSVOL은 복제에 DFS-R을 사용 하기 때문에 UE-V 데이터 파일 복제에 SYSVOL을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="ba058-431">[Ue-v 2. x에 대 한 설정 저장소 위치 배포](https://technet.microsoft.com/library/dn458891.aspx#ssl)에 지정 된 대로 공유 사용 권한과 NTFS acl (액세스 제어 목록)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="ba058-432">UE-V Agent와 함께 파일 서버 클러스터링을 사용 하 여 통신 실패 시 사용자 상태 데이터의 복사본에 대 한 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="ba058-433">설정 저장소 경로 데이터 (사용자 데이터) 및 설정 템플릿 카탈로그 템플릿을 클러스터 된 공유에 저장 하거나 DFS-N 공유 또는 둘 다에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="ba058-434">UE-V 설정 동기화에 대 한 컴퓨터 시계 동기화</span><span class="sxs-lookup"><span data-stu-id="ba058-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="ba058-435">UE-V 에이전트를 실행 하는 컴퓨터는 일관성 있는 설정 환경을 유지 하기 위해 시간 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="ba058-436">UE-V는 타임 스탬프를 사용 하 여 설정 저장소 위치에서 설정을 동기화 해야 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="ba058-437">컴퓨터 시계가 정확 하지 않으면 이전 설정이 최신 설정을 덮어쓰거나 새 설정이 설정 저장소 위치에 저장 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="ba058-438">UE-V의 필수 구성 요소 및 지원 되는 구성 확인</span><span class="sxs-lookup"><span data-stu-id="ba058-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="ba058-439">계속 하기 전에 UE-V를 실행 하기 위한 요구 사항이 환경에 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ba058-440">운영 체제</span><span class="sxs-lookup"><span data-stu-id="ba058-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-441">버전</span><span class="sxs-lookup"><span data-stu-id="ba058-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-442">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="ba058-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-443">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="ba058-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba058-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="ba058-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ba058-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-446">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba058-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-447">Ultimate, Enterprise 또는 Professional Edition</span><span class="sxs-lookup"><span data-stu-id="ba058-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-448">SP1</span><span class="sxs-lookup"><span data-stu-id="ba058-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-449">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="ba058-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-450">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-451">UE-V 2.1의 경우 .NET Framework 4.5 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="ba058-452">UE-V 2.0의 경우 .NET Framework 4 이상의 기능을 사용할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-453">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba058-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-454">표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</span><span class="sxs-lookup"><span data-stu-id="ba058-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-455">SP1</span><span class="sxs-lookup"><span data-stu-id="ba058-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-456">64비트</span><span class="sxs-lookup"><span data-stu-id="ba058-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-457">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-458">UE-V 2.1의 경우 .NET Framework 4.5 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="ba058-459">UE-V 2.0의 경우 .NET Framework 4 이상의 기능을 사용할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-460">Windows 8 및 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ba058-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-461">엔터프라이즈 또는 Pro</span><span class="sxs-lookup"><span data-stu-id="ba058-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-462">없음</span><span class="sxs-lookup"><span data-stu-id="ba058-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-463">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="ba058-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-464">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-465">.NET Framework 4.5 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-466">Windows 10, 1607 이전 버전</span><span class="sxs-lookup"><span data-stu-id="ba058-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ba058-467">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-467">Note</span></span></strong><br/><p><span data-ttu-id="ba058-468">UE-V 2.1 SP1만이 Windows 10, 1607 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ba058-469">엔터프라이즈 또는 Pro</span><span class="sxs-lookup"><span data-stu-id="ba058-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-470">없음</span><span class="sxs-lookup"><span data-stu-id="ba058-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-471">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="ba058-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-472">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-473">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="ba058-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba058-474">Windows Server 2012 및 Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ba058-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-475">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="ba058-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-476">없음</span><span class="sxs-lookup"><span data-stu-id="ba058-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-477">64비트</span><span class="sxs-lookup"><span data-stu-id="ba058-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-478">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-479">.NET Framework 4.5 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba058-480">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba058-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-481">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="ba058-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-482">없음</span><span class="sxs-lookup"><span data-stu-id="ba058-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-483">64비트</span><span class="sxs-lookup"><span data-stu-id="ba058-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-484">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba058-485">.NET Framework 4.6 이상</span><span class="sxs-lookup"><span data-stu-id="ba058-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ba058-486">또한</span><span class="sxs-lookup"><span data-stu-id="ba058-486">Also…</span></span>

-   <span data-ttu-id="ba058-487">**MDOP 라이선스:** 이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="ba058-488">엔터프라이즈 고객은 Microsoft 소프트웨어 보증을 통해 MDOP를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="ba058-489">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 MDOP를 가져오는 방법 (을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="ba058-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="ba058-490">설치할 컴퓨터에 대 한 **관리 자격 증명**</span><span class="sxs-lookup"><span data-stu-id="ba058-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="ba058-491">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-491">Note</span></span>**  

-   <span data-ttu-id="ba058-492">WIndows 10, 버전 1607, UE-V를 사용 하 여 [엔터프라이즈 용 windows 10](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) 에 포함 되어 있으며 더 이상 Microsoft 데스크톱 최적화 팩의 일부가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="ba058-493">UE-V Agent의 UE-V Windows PowerShell 기능을 사용 하려면 .NET Framework 4 이상 및 Windows PowerShell 3.0 이상이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="ba058-494">[여기](https://go.microsoft.com/fwlink/?LinkId=309609)에서 Windows PowerShell 3.0을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="ba058-495">Windows 7 또는 Windows Server 2008 R2 운영 체제를 실행 하는 컴퓨터에 .NET Framework 4 또는 .NET Framework 4.5을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="ba058-496">Windows 8, Windows 8.1 및 Windows Server 2012 운영 체제에는 .NET Framework 4.5이 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="ba058-497">Windows 10 운영 체제에는 .NET Framework 4.6이 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="ba058-498">UE-V에서는 필수 프로필에 대 한 "로밍 캐시 삭제" 정책이 지원 되지 않으므로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="ba058-499">UE-V와 관련 된 특수 한 RAM (임의 액세스 메모리) 요구 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="ba058-500">동기화 공급자를 통해 설정 동기화</span><span class="sxs-lookup"><span data-stu-id="ba058-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="ba058-501">동기화 공급자는 로컬 캐시를 다음 인스턴스의 설정 저장소 위치와 동기화 하는 사용자의 기본 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="ba058-502">로그온/로그 오프</span><span class="sxs-lookup"><span data-stu-id="ba058-502">Logon/logoff</span></span>

-   <span data-ttu-id="ba058-503">잠금/잠금 해제</span><span class="sxs-lookup"><span data-stu-id="ba058-503">Lock/unlock</span></span>

-   <span data-ttu-id="ba058-504">원격 데스크톱 연결/연결 끊기</span><span class="sxs-lookup"><span data-stu-id="ba058-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="ba058-505">응용 프로그램 열기/닫기</span><span class="sxs-lookup"><span data-stu-id="ba058-505">Application open/close</span></span>

<span data-ttu-id="ba058-506">예약 된 작업은 특정 응용 프로그램에 대 한 특정 트리거 이벤트를 통해 30 분 마다 설정 동기화를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="ba058-507">자세한 내용은 [ue-v 2. x 예약 작업의 빈도 변경을](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="ba058-508">UE-V Agent는 엔터프라이즈 네트워크 (원격 컴퓨터 및 랩톱)에 항상 연결 되어 있지 않은 컴퓨터 및 네트워크에 항상 연결 되는 컴퓨터 (Windows Server 및 VDI (가상 데스크톱 인터페이스) 세션을 실행 하는 컴퓨터)에 대 한 사용자 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="ba058-509">**항상 사용 가능한 연결이 있는 컴퓨터 동기화:** 항상 네트워크에 연결 된 컴퓨터에서 UE-V를 사용 하는 경우 설정 저장소 서버를 표준 네트워크 공유로 처리 하는 *Syncmethod = 없음* 매개 변수를 사용 하 여 설정을 동기화 하도록 ue-v agent를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="ba058-510">이 구성에서는 응용 프로그램 설정 가져오기가 지연 되는 경우이를 알리기 위해 UE-V Agent를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="ba058-511">다음 방법 중 하나를 통해이 구성을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="ba058-512">UE-V를 설치 하는 동안 명령 프롬프트나 배치 파일에서 AgentSetup.exe 매개 변수 *Syncmethod = 없음*을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="ba058-513">[Ue-v 2. x 에이전트 배포는](https://technet.microsoft.com/library/dn458891.aspx#agent) 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="ba058-514">UE-V를 설치한 후 System Center 2012 구성 관리자 또는 MDOP ADMX 템플릿의 설정 관리 기능을 사용 하 여 *Syncmethod = 없음* 구성을 푸시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="ba058-515">Windows PowerShell 또는 WMI (Windows Management Instrumentation)를 사용 하 여 *Syncmethod = 없음* 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="ba058-516">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-516">Note</span></span>**  
    <span data-ttu-id="ba058-517">이러한 마지막 두 메서드는 풀링된 VDI (가상 데스크톱 인프라) 환경에는 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="ba058-518">설정 동기화를 시작 하기 전에 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="ba058-519">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-519">Note</span></span>**  
<span data-ttu-id="ba058-520">*Syncmethod = 없음*을 설정 하면 설정 변경 내용이 서버에 직접 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="ba058-521">설정 저장소 경로에 대 한 네트워크 연결을 찾지 못한 경우 설정 변경 내용이 장치에 캐시 되 고 다음에 동기화 공급자가 실행 될 때 동기화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="ba058-522">설정 저장소 경로를 찾을 수 없고 로그 오프할 때 풀링된 VDI 환경에서 사용자 프로필이 제거 되는 경우 설정 변경 내용이 손실 되 고 컴퓨터를 설정 저장소 경로에 다시 연결 하면 사용자가 변경 내용을 재적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="ba058-523">**외부 동기화 엔진 동기화:** *Syncmethod = External* 매개 변수는 사용자 컴퓨터의 로컬 폴더에 ue-v 설정이 기록 되는 경우 모든 외부 동기화 엔진 (예: 비즈니스용 OneDrive, 클라우드 폴더, Sharepoint 또는 Dropbox)을 사용 하 여 사용자가 액세스 하는 다른 컴퓨터에 이러한 설정을 적용할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="ba058-524">**공유 VDI 세션에 대 한 지원:** UE-V 2.1 및 2.1 SP1은 최종 사용자 간에 공유 되는 VDI 세션에 대 한 지원을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="ba058-525">특수 VDI 템플릿을 등록 하 고 구성할 수 있으며,이는 UE-V가 비영구 VDI 세션에 대해 모든 기능을 그대로 유지 하도록 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="ba058-526">참고</span><span class="sxs-lookup"><span data-stu-id="ba058-526">Note</span></span>**  
<span data-ttu-id="ba058-527">비 영구적인 VDI 세션에 VDI 모드를 사용 하도록 설정 하지 않으면 [백업/복원 및 마지막으로 알려진 양호한 속도 (LKG)](https://technet.microsoft.com/library/dn878331.aspx)와 같은 특정 기능이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="ba058-528">VDI 템플릿은 UE-V 2.1 및 2.1 SP1과 함께 제공 되며 일반적으로 설치 후에 사용할 수 있습니다. C:\\program files Files\\Microsoft 사용자 환경 Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="ba058-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="ba058-529">UE-V 생성기 지원에 대 한 필수 조건</span><span class="sxs-lookup"><span data-stu-id="ba058-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="ba058-530">사용자 지정 설정 위치 서식 파일을 만드는 데 사용 되는 컴퓨터에 UE-V 생성기를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="ba058-531">이 컴퓨터는 설정이 동기화 된 응용 프로그램을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="ba058-532">UE-V 생성기 소프트웨어를 실행 하는 컴퓨터에서 관리자 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="ba058-533">UE-V 생성기는 NTFS 파일 시스템을 사용 하는 컴퓨터에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="ba058-534">UE-V 생성기 소프트웨어에는 .NET Framework 4가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba058-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="ba058-535">자세한 내용은 [사용자 지정 응용 프로그램에 대 한 ue-v 2. x 배포](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba058-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="ba058-536">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="ba058-536">Other resources for this product</span></span>


-   [<span data-ttu-id="ba058-537">Microsoft UE-V (User Experience Virtualization) 2. x</span><span class="sxs-lookup"><span data-stu-id="ba058-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="ba058-538">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="ba058-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="ba058-539">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="ba058-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="ba058-540">UE-V 2. x 문제 해결</span><span class="sxs-lookup"><span data-stu-id="ba058-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="ba058-541">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="ba058-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)














