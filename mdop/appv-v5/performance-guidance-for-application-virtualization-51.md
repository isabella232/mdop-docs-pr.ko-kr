---
title: Application Virtualization 5.1에 대한 성능 지침
description: Application Virtualization 5.1에 대한 성능 지침
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813521"
---
# <span data-ttu-id="1367c-103">Application Virtualization 5.1에 대한 성능 지침</span><span class="sxs-lookup"><span data-stu-id="1367c-103">Performance Guidance for Application Virtualization 5.1</span></span>


<span data-ttu-id="1367c-104">최적화 된 성능을 위해 App-v 5.1를 구성 하는 방법과 가상 앱 패키지를 최적화 하 고 RDS 및 VDI에서 더 나은 사용자 환경을 제공 하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-104">Learn how to configure App-V 5.1 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="1367c-105">여러 메서드를 구현 하면 최종 사용자 환경을 개선 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="1367c-106">그러나 환경에서 일부 메서드를 지원 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="1367c-107">이 문서를 읽기 전에 다음 정보를 읽고 이해 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="1367c-108">Microsoft Application Virtualization 5.1 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="1367c-108">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="1367c-109">앱-V 5 SP2 응용 프로그램 게시 및 클라이언트 조작</span><span class="sxs-lookup"><span data-stu-id="1367c-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="1367c-110">Microsoft Application Virtualization 시퀀싱 가이드</span><span class="sxs-lookup"><span data-stu-id="1367c-110">Microsoft Application Virtualization Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="1367c-111">참고</span><span class="sxs-lookup"><span data-stu-id="1367c-111">Note</span></span>**  
<span data-ttu-id="1367c-112">이 문서에서 사용 되는 일부 용어는 외부 원본 및 컨텍스트에 따라 의미가 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="1367c-113">이 문서에 사용 된 용어에 대 한 자세한 내용을 보려면 **\\** 이 문서의 " [Application Virtualization 성능 지침 용어](#bkmk-terms1) " 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="1367c-114">마지막으로이 문서는 앱-V 5.1 클라이언트를 실행 하는 컴퓨터와 최적의 성능을 위한 환경을 구성 하는 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-114">Finally, this document will provide you with the information to configure the computer running App-V 5.1 client and the environment for optimal performance.</span></span> <span data-ttu-id="1367c-115">Sequencer를 사용 하 여 성능을 위해 가상 응용 프로그램 패키지를 최적화 하 고, RDS (원격 데스크톱 서비스) 및 VDI (비영구 가상 데스크톱 인프라)에서 앱-V 5.1을 사용 하 여 최적의 사용자 환경을 제공 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.1 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="1367c-116">해당 환경과 관련 된 정보를 확인 하려면 각 섹션의 간략 한 개요 및 적응성 검사 목록을 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="1367c-117">앱-V 5.1의 상태 저장 \ \* 비 영구적인 배포</span><span class="sxs-lookup"><span data-stu-id="1367c-117">App-V 5.1 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="1367c-118">이 섹션에서는 사용자가 로그인 한 후 몇 초 이내에 모든 가상 응용 프로그램에 액세스할 수 있도록 하는 접근 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="1367c-119">이는 자주 실행 되는 앱-V 5.1 게시 새로 고침을 고유 하 게 처리 하 여 달성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-119">This is achieved by uniquely addressing the often long-running App-V 5.1 publishing refresh.</span></span> <span data-ttu-id="1367c-120">접근 방식에 대 한 기본 사항은 빠른 게시 새로 고침 이지만 실제로는 아무런 작업도 수행 하지 않는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="1367c-121">최상의 사용자 환경을 제공 하기 위해서는 여러 조건을 충족 해야 하며 단계를 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="1367c-122">자세한 내용은 다음 섹션의 정보를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="1367c-123">[사용 시나리오](#bkmk-us) -두 시나리오를 검토할 때이 방법이 extremes 것을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="1367c-124">사용 요구 사항에 따라 사용자 및/또는 가상 응용 프로그램 패키지의 하위 집합에 이러한 단계를 적용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="1367c-125">성능 최적화 – 최상의 환경을 제공 하기 위해 기본 이미지에 App-v 가상 응용 프로그램 패키지 중 일부를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="1367c-126">이 및 기타 요구 사항이 논의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="1367c-127">저장소에 최적화 됨 – 저장소 영향이 염려 되는 경우이 시나리오에 따라 이러한 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="1367c-128">환경 준비</span><span class="sxs-lookup"><span data-stu-id="1367c-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="1367c-129">비 영구적인 VDI 또는 RDSH 환경에서 기본 이미지를 준비 하는 단계에서는이 방법을 사용 하려면 기본 이미지에서 몇 단계만 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="1367c-130">2.1 UE-V (사용자 프로필 관리) 솔루션의 UPM (cornerstone 접근 권한)을 사용 하는 경우에는이 접근 방식으로 몇 가지 레지스트리와 파일 위치의 콘텐츠를 유지 하는 UEM 솔루션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-130">Use UE-V 2.1 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="1367c-131">이러한 위치는 사용자 통합 \ \*를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="1367c-132">UPM 솔루션에 대 한 특정 요구 사항을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="1367c-133">사용자 환경 실습</span><span class="sxs-lookup"><span data-stu-id="1367c-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="1367c-134">실습 – App-v 및 UE-V 작업을 단계별로 진행 하 고 사용자에 게 기대 되는 예측 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="1367c-135">결과 – 예상 결과를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="1367c-136">패키지 수명 주기에 미치는 영향</span><span class="sxs-lookup"><span data-stu-id="1367c-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="1367c-137">성능 최적화/조정을 통해 VDI 환경 개선</span><span class="sxs-lookup"><span data-stu-id="1367c-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="1367c-138">적응성 검사 목록</span><span class="sxs-lookup"><span data-stu-id="1367c-138">Applicability Checklist</span></span>

<span data-ttu-id="1367c-139">배포 환경</span><span class="sxs-lookup"><span data-stu-id="1367c-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1367c-140">비 영구적인 VDI 또는 RDSH.</span><span class="sxs-lookup"><span data-stu-id="1367c-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1367c-141">UE-V (사용자 환경 가상화), 기타 UPM 솔루션 또는 사용자 프로필 디스크 (UPD).</span><span class="sxs-lookup"><span data-stu-id="1367c-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1367c-142">예상 되는 구성</span><span class="sxs-lookup"><span data-stu-id="1367c-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1367c-143">앱-V 사용자 상태 템플릿을 사용 하거나 UPM (사용자 프로필 관리) 소프트웨어가 있는 UE-V (user Experience Virtualization)</span><span class="sxs-lookup"><span data-stu-id="1367c-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="1367c-144">비 UE-V UPM 소프트웨어는 로그인 또는 프로세스/응용 프로그램 시작 및 로그 오프에서 트리거할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1367c-145">앱-V 공유 콘텐츠 저장소 (SCS)를 구성 하거나 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1367c-146">IT 관리</span><span class="sxs-lookup"><span data-stu-id="1367c-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1367c-147">최적의 성능을 유지 하기 위해 관리자는 VM 기본 이미지를 정기적으로 업데이트 해야 하며, 관리자는 여러 사용자 그룹에 대해 다양 한 이미지를 관리 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="1367c-148">사용 시나리오</span><span class="sxs-lookup"><span data-stu-id="1367c-148">Usage Scenario</span></span>

<span data-ttu-id="1367c-149">두 가지 시나리오를 검토 하는 동안에는 이러한 방식으로 extremes을 염두에 두어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="1367c-150">사용 요구 사항에 따라 사용자, 가상 응용 프로그램 패키지 또는 둘 다의 하위 집합에 이러한 단계를 적용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-151">성능 최적화</span><span class="sxs-lookup"><span data-stu-id="1367c-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="1367c-152">저장소에 최적화 됨</span><span class="sxs-lookup"><span data-stu-id="1367c-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-153">최적화 된 사용자 환경을 제공 하기 위해이 접근 방식은 UPM 솔루션의 기능을 활용 하 고 추가 이미지 준비를 수행 하며 추가 이미지 관리 오버 헤드를 유발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="1367c-154">다음은 상태 저장 비 영구적인 배포의 다양 한 성능 개선 사항에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="1367c-155">자세한 내용은 <strong> </strong> <strong> </strong> <strong> 이 문서의 참고 항목 섹션에 있는 </strong> 게시 성능에 대 한 패키지 최적화 및 app-v 시퀀싱 가이드에 대 한 참조를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-156">이전 시나리오의 일반적인 기대는 계속 해 서 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="1367c-157">그러나 일반적으로 VM 이미지는 매우 비용이 많이 드는 배열에 저장 된다는 점에 유의 하세요. 접근 방식이 약간 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="1367c-158">기본 이미지에서 사용자가 대상으로 하는 가상 응용 프로그램 패키지를 미리 구성 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="1367c-159">이러한 변경으로 인 한 영향은이 문서의 사용자 환경 연습 섹션에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="1367c-160">환경 준비</span><span class="sxs-lookup"><span data-stu-id="1367c-160">Preparing your Environment</span></span>

<span data-ttu-id="1367c-161">다음 표에는 기본 이미지와 접근 방법에 대 한 UE-V 또는 다른 UPM 솔루션을 준비 하는 데 필요한 단계가 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="1367c-162">기본 이미지 준비</span><span class="sxs-lookup"><span data-stu-id="1367c-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-163">성능 최적화</span><span class="sxs-lookup"><span data-stu-id="1367c-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="1367c-164">저장소에 최적화 됨</span><span class="sxs-lookup"><span data-stu-id="1367c-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="1367c-165">클라이언트의 App-v 5.1 클라이언트 버전을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-165">Install the App-V 5.1 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="1367c-166">UE-V를 설치 하 고 UE-V 템플릿 갤러리에서 앱-V 설정 서식 파일을 다운로드 하려면 다음 단계를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="1367c-167">SCS (공유 콘텐츠 저장소) 모드를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="1367c-168">자세한 내용은 <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> 공유 콘텐츠 저장소 모드 용 app-v 5.1 클라이언트를 설치 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="1367c-168">For more information see <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)">How to Install the App-V 5.1 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-169">로그인 레지스트리 DWORD에 사용자 통합 유지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="1367c-170">모든 사용자 및 전역 대상 패키지 (예: <strong> Add-AppvClientPackage를 미리 구성 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-171">모든 사용자 및 전역 대상 연결 그룹 (예: <strong> Add-AppvClientConnectionGroup을 미리 구성 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-172">모든 전역 대상 패키지를 미리 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="1367c-173">반대로</span><span class="sxs-lookup"><span data-stu-id="1367c-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-174">전역 게시/새로 고침을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="1367c-175">사용자 게시/새로 고침을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="1367c-176">모든 사용자 대상 패키지의 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="1367c-177">다음 사용자의 VFS (가상 파일 시스템) 항목을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="1367c-178">클라이언트의 App-v 5.1 클라이언트 버전을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-178">Install the App-V 5.1 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="1367c-179">UE-V를 설치 하 고 UE-V 템플릿 갤러리에서 앱-V 설정 서식 파일을 다운로드 하려면 다음 단계를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="1367c-180">SCS (공유 콘텐츠 저장소) 모드를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="1367c-181">자세한 내용은 <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> 공유 콘텐츠 저장소 모드 용 app-v 5.1 클라이언트를 설치 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="1367c-181">For more information see <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)">How to Install the App-V 5.1 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-182">로그인 레지스트리 DWORD에 사용자 통합 유지를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="1367c-183">모든 전역 대상 패키지를 미리 구성 합니다 (예: <strong> Add-AppvClientPackage) </strong> .</span><span class="sxs-lookup"><span data-stu-id="1367c-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-184">모든 전역 대상 연결 그룹 (예: <strong> Add-AppvClientConnectionGroup을 미리 구성 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-185">모든 전역 대상 패키지를 미리 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1367c-186">**구성** -중요 한 app-v 클라이언트 구성에 대 한 자세한 컨텍스트 및 방법에 대 한 자세한 내용은 다음 정보를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-187">구성 설정</span><span class="sxs-lookup"><span data-stu-id="1367c-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="1367c-188">이렇게 하면 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="1367c-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="1367c-189">어떻게 사용 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="1367c-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-190">SCS (공유 콘텐츠 저장소) 모드</span><span class="sxs-lookup"><span data-stu-id="1367c-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-191"><strong>Set-AppvClientConfiguration </strong> - <strong> sharedcontentstoremode </strong> 를 사용 하 여 PowerShell에서 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="1367c-192">App-v 클라이언트를 설치 하는 동안</span><span class="sxs-lookup"><span data-stu-id="1367c-192">During installation of the App-V client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1367c-193">공유 콘텐츠 저장소를 실행할 때 게시 데이터만 하드 디스크에서 유지 관리 됩니다. 다른 가상 응용 프로그램 자산은 메모리 (RAM)에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="1367c-194">이는 로컬 저장소를 절약 하 고 초당 디스크 I/o (IOPS)를 최소화 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-195">App-v 클라이언트 끝점과 SCS 콘텐츠 서버, SAN 간에 대기 시간이 짧은 연결을 사용할 수 있는 경우이 방법을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1367c-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="1367c-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-197"><strong>HKEY_LOCAL_MACHINE </strong>  \  <strong> 소프트웨어 </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> 클라이언트 </strong>  \  <strong> 통합 </strong> 아래에서 레지스트리에 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-198"><strong>값이 1 인 DWORD 값 PreserveUserIntegrationsOnLogin을 만듭니다 </strong> <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="1367c-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-199">App-v 클라이언트 서비스를 다시 시작 하거나 App-v 클라이언트를 실행 하는 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1367c-200">특정 패키지를 미리 구성 하지 않은 경우 ( <strong> AppvClientPackage </strong> )이 설정이 구성 되어 있지 않으면 app-v 클라이언트는 영구 사용자 통합 \* 통합 \*을 해제 한 다음 \*를 다시 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="1367c-201">위의 조건을 충족 하는 모든 패키지에 대해 게시/새로 고침 중 작업을 두 번 효과적으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-202">기본 이미지에서 사용 가능한 모든 사용자 패키지를 미리 구성할 계획이 없다면이 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="1367c-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-204"><strong>HKEY_LOCAL_MACHINE </strong> &lt; 강력한 &gt; 소프트웨어 </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong> &lt; 강력한 &gt; 클라이언트 </strong>  \  <strong> 게시 </strong> 아래에서 레지스트리에 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1367c-205"><strong> </strong> 원하는 최대 동시 게시 새로 고침 수를 사용 하 여 DWORD 값 MaxConcurrentPublishingrefresh를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="1367c-206">App-v 클라이언트 서비스 및 컴퓨터는 다시 시작할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1367c-207">이 설정은 동시에 게시 새로 고침/동기화를 수행할 수 있는 사용자 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="1367c-208">기본 설정은 제한 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-209">동시 게시 새로 고침 횟수를 제한 하면 과도 한 CPU 사용을 방지 하 여 컴퓨터 성능에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="1367c-210">이 제한은 여러 사용자가 동시에 같은 컴퓨터에 로그인 하 여 게시 새로 고침 동기화를 수행할 수 있는 RDS 환경에서 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="1367c-211">동시 게시 새로 고침 임계값에 도달 하는 경우, 새 응용 프로그램을 게시 하 고 로그인 한 후 최종 사용자가 사용할 수 있도록 하는 데 필요한 시간은 결정 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1367c-212">App-v 접근 방법에 대 한 UE-V 솔루션 구성</span><span class="sxs-lookup"><span data-stu-id="1367c-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="1367c-213">Microsoft UE-V (User Experience Virtualization)를 사용 하 여 특정 사용자에 대 한 응용 프로그램 설정 및 Windows 운영 체제 설정을 캡처 및 중앙 집중화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="1367c-214">이러한 설정은 데스크톱 컴퓨터, 랩톱 컴퓨터, VDI (가상 데스크톱 인프라) 세션을 비롯 하 여 사용자가 액세스 하는 다른 컴퓨터에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="1367c-215">UE-V는 RDS 및 VDI 시나리오에 최적화 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="1367c-216">자세한 내용은 [사용자 환경 가상화 시작을](https://technet.microsoft.com/library/dn458926.aspx) 참조 하세요. 2.0</span><span class="sxs-lookup"><span data-stu-id="1367c-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458926.aspx)</span></span>

<span data-ttu-id="1367c-217">기본적으로 UE-V 클라이언트를 설치 하 고 [MICROSOFT ue-v (User Experience Virtualization) 템플릿 갤러리](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33)에서 다음 microsoft 작성 된 앱-V 설정 서식 파일을 다운로드 하는 것이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="1367c-218">서식 파일을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-218">Register the template.</span></span> <span data-ttu-id="1367c-219">UE-V 템플릿에 대 한 자세한 내용은 [템플릿을 가져오고 등록 하기 위한 ue-v 특정 리소스를](https://technet.microsoft.com/library/dn458926.aspx)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458926.aspx).</span></span>

**<span data-ttu-id="1367c-220">참고</span><span class="sxs-lookup"><span data-stu-id="1367c-220">Note</span></span>**  
<span data-ttu-id="1367c-221">추가 구성 단계를 수행 하지 않고 Microsoft UE-V (사용자 환경 가상화)가 대상 컴퓨터의 시작 메뉴 바로 가기 (.lnk 파일)를 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="1367c-222">.Lnk 파일 형식은 기본적으로 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="1367c-223">UE-V는 모든 사용자의 장치가 같은 위치에 설치 된 동일한 응용 프로그램 집합을가지고 있으며 모든 .lnk 파일이 모든 사용자의 장치에 대해 유효 하 게 되는 RDS 및 VDI 시나리오의 제외 목록에서 .lnk 파일 형식의 제거만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="1367c-224">예를 들어, UE-V는 일부 장치 에서만 바로 가기가 유효 하기 때문에 현재 다음 두 시나리오를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="1367c-225">사용자가 .lnk 파일을 사용 하도록 설정 된 하나의 장치에 설치 된 응용 프로그램이 있고 다른 장치에 설치 된 동일한 네이티브 응용 프로그램이 .lnk 파일을 사용 하는 다른 설치 루트에 설정 되어 있는 경우</span><span class="sxs-lookup"><span data-stu-id="1367c-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="1367c-226">사용자가 한 장치에 응용 프로그램을 설치 했지만 .lnk 파일을 사용 하도록 설정한 경우는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="1367c-227">중요</span><span class="sxs-lookup"><span data-stu-id="1367c-227">Important</span></span>**  
<span data-ttu-id="1367c-228">이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="1367c-229">Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="1367c-230">레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="1367c-231">Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="1367c-232">레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="1367c-233">Microsoft 레지스트리 편집기 (regedit.exe)를 사용 하 여 **HKEY \ _LOCAL \ _MACHINE**  \\  **소프트웨어**  \\  **Microsoft**  \\  **UEV**  \\  **에이전트**구성 ExcludedFileTypes으로 이동 하 여  \\  **Configuration**  \\  **ExcludedFileTypes** 제외 된 파일 형식에서 **.lnk** 를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="1367c-234">앱에 대 한 다른 UPM (사용자 프로필 관리) 솔루션 구성-V 접근 방법</span><span class="sxs-lookup"><span data-stu-id="1367c-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="1367c-235">상태 저장 환경에서 예상 되는 경우 UPM 솔루션이 구현 되 고 로그인과 세션 간에 사용자 데이터의 지 속성을 지원할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="1367c-236">UPM 솔루션에 대 한 요구 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="1367c-237">사용자에 대 한 App-v 5.1 방법과 같이 최적화 된 로그인 환경을 사용 하려면 솔루션은 다음을 수행할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-237">To enable an optimized login experience, for example the App-V 5.1 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="1367c-238">사용자 프로필의 일부로 다음 사용자 통합을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="1367c-239">로그인 (또는 응용 프로그램 시작)에 대 한 사용자 프로필 동기화를 트리거하여 모든 사용자 통합이 게시/새로 고침 시작 전에 적용 되도록 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="1367c-240">사용자 통합을 포함 하는 UPD (사용자 프로필 디스크) 또는 유사한 기술을 연결 하 여 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

    **<span data-ttu-id="1367c-241">참고</span><span class="sxs-lookup"><span data-stu-id="1367c-241">Note</span></span>**  
    <span data-ttu-id="1367c-242">UPD는 전체 프로필이 사용자 프로필 디스크에 저장 된 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-242">App-V is supported when using UPD only when the entire profile is stored on the user profile disk.</span></span>

    <span data-ttu-id="1367c-243">사용자 프로필 디스크에 저장 된 선택한 폴더와 UPD를 사용 하는 경우 app-v 패키지가 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-243">App-V packages are not supported when using UPD with selected folders stored in the user profile disk.</span></span> <span data-ttu-id="1367c-244">쓰기 드라이버의 복사본은 UPD 선택한 폴더를 처리 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-244">The Copy on Write driver does not handle UPD selected folders.</span></span>



-   <span data-ttu-id="1367c-245">세션 로그 오프 전에 사용자 통합을 구성 하는 위치에 대 한 변경 내용 캡처</span><span class="sxs-lookup"><span data-stu-id="1367c-245">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="1367c-246">게시 서버를 추가할 때 App-v 5.1 (**추가 기능**)를 사용 하 여 동기화를 구성할 수 있습니다 (예: AppvPublishingServer). 또는 지정 된 새로 고침 간격 이후 새로 고침 및/또는 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-246">With App-V 5.1 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="1367c-247">두 경우 모두에 예약 된 작업이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-247">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="1367c-248">이전 버전의 App-v 5.1에서는 사용자와 전역 새로 고침을 시작 하는 VBScript를 사용 하 여 예약 된 작업을 모두 구성 했습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-248">In previous versions of App-V 5.1, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="1367c-249">앱 가상화 5.0 SP2 용 핫픽스 패키지 4를 사용 하 여 로그온 할 때 사용자 새로 고침은 **SyncAppvPublishingServer.exe**에 의해 시작 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-249">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on was initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="1367c-250">이 변경은 UPM 솔루션에 트리거 프로세스를 제공 하기 위해 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-250">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="1367c-251">이 프로세스는 UPM 솔루션이 사용자 통합을 적용할 수 있도록 게시/새로 고침을 지연 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-251">This process delays the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="1367c-252">게시/새로 고침이 완료 되 면 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-252">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="1367c-253">사용자 통합</span><span class="sxs-lookup"><span data-stu-id="1367c-253">User Integrations</span></span>**

<span data-ttu-id="1367c-254">Registry – HKEY _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="1367c-254">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="1367c-255">경로-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="1367c-255">Path - Software\\Classes</span></span>

    <span data-ttu-id="1367c-256">Exclude: 지역 설정, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="1367c-256">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="1367c-257">경로-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="1367c-257">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="1367c-258">경로-Software\\Microsoft\\Windows\\CurrentVersion\\App 경로</span><span class="sxs-lookup"><span data-stu-id="1367c-258">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="1367c-259">파일 위치</span><span class="sxs-lookup"><span data-stu-id="1367c-259">File Locations</span></span>**

-   <span data-ttu-id="1367c-260">Root – "환경 변수" APPDATA</span><span class="sxs-lookup"><span data-stu-id="1367c-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="1367c-261">경로-Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="1367c-261">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="1367c-262">Root – "환경 변수" APPDATA</span><span class="sxs-lookup"><span data-stu-id="1367c-262">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="1367c-263">경로-Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="1367c-263">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="1367c-264">Root – "환경 변수" APPDATA</span><span class="sxs-lookup"><span data-stu-id="1367c-264">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="1367c-265">경로-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="1367c-265">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="1367c-266">(모든 바탕 화면 바로 가기를 유지 하려면 가상 및 비가상)</span><span class="sxs-lookup"><span data-stu-id="1367c-266">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="1367c-267">Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ \* .lnk</span><span class="sxs-lookup"><span data-stu-id="1367c-267">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="1367c-268">Microsoft UE-V (User Experience Virtualization)</span><span class="sxs-lookup"><span data-stu-id="1367c-268">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="1367c-269">또한 UE-V (사용자 환경 가상화)를 사용 하 여 특정 사용자에 대 한 응용 프로그램 설정 및 Windows 운영 체제 설정을 캡처 및 중앙 집중화 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-269">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="1367c-270">이러한 설정은 데스크톱 컴퓨터, 랩톱 컴퓨터, VDI (가상 데스크톱 인프라) 세션을 비롯 하 여 사용자가 액세스 하는 다른 컴퓨터에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-270">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="1367c-271">자세한 내용은 [Ue-v 템플릿 갤러리를 사용 하](https://technet.microsoft.com/library/jj679972.aspx)여 [사용자 환경 가상화 1.0 시작](https://technet.microsoft.com/library/jj680015.aspx) 및 설정 위치 템플릿 공유를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-271">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="1367c-272">사용자 환경 실습</span><span class="sxs-lookup"><span data-stu-id="1367c-272">User Experience Walk-through</span></span>

<span data-ttu-id="1367c-273">다음은 App-v 및 UPM 작업을 단계별로 살펴보고 예상 되는 사용자가 기대 하는 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-273">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-274">성능 최적화</span><span class="sxs-lookup"><span data-stu-id="1367c-274">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="1367c-275">저장소에 최적화 됨</span><span class="sxs-lookup"><span data-stu-id="1367c-275">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-276">VDI/RDSH 환경에서이 방법을 구현한 후에는 첫 번째 로그인에</span><span class="sxs-lookup"><span data-stu-id="1367c-276">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-277">작업 사용자 게시/새로 고침이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-277">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="1367c-278">있다는 사용자가 가상 응용 프로그램 (예: 비영구)을 처음으로 게시 한 경우에는 게시/새로 고침을 수행 하는 데 평소와 같은 시간이 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-278">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="1367c-279">작업 게시/새로 고침 후 UPM 솔루션은 사용자 통합을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-279">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="1367c-280">있다는 UPM 솔루션이 구성 되는 방법에 따라 로그 오프 프로세스의 일부로 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-280">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="1367c-281">이렇게 하면 사용자 상태를 유지 하는 것과 동일한/비슷한 오버 헤드가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-281">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="1367c-282">후속 로그인:</span><span class="sxs-lookup"><span data-stu-id="1367c-282">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-283">작업 UPM 솔루션은 게시/새로 고침 전에 시스템에 사용자 통합을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-283">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="1367c-284">있다는 바탕 화면이 나 시작 메뉴에 바로 가기가 표시 되며 즉시 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-284">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="1367c-285">게시/새로 고침이 완료 되 면 (예: 패키지 권리 변경) 일부는 종료 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-285">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="1367c-286">작업 게시/새로 고침을 수행 하면 사용자 패키지 자격의 변경에 대 한 게시 취소 및 게시 작업이 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-286">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="1367c-287">있다는 자격을 변경할 수 없는 경우 publishing1가 초 내에 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-287">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="1367c-288">그렇지 않으면 가상 응용 프로그램의 수 및 복잡도 \*를 기준으로 게시/새로 고침이 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-288">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="1367c-289">작업 UPM 솔루션은 로그 오프할 때 사용자 통합을 다시 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-289">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="1367c-290">있다는 이전과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-290">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="1367c-291">¹ 게시 작업 ( <strong> 게시-AppVClientPackage </strong> )은 사용자 카탈로그에 항목을 추가 하 고, 사용자에 게 자격을 매핑하고, 로컬 저장소를 식별 하 고, 통합 단계를 완료 하 여 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-291">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-292">VDI/RDSH 환경에서이 방법을 구현한 후에는 첫 번째 로그인에</span><span class="sxs-lookup"><span data-stu-id="1367c-292">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-293">작업 사용자 게시/새로 고침이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-293">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="1367c-294">있다는</span><span class="sxs-lookup"><span data-stu-id="1367c-294">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-295">사용자가 가상 응용 프로그램 (예: 비영구)을 처음으로 게시 한 경우에는 게시/새로 고침의 일반적인 시간이 소요 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-295">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="1367c-296">첫 번째 및 후속 로그인은 패키지 사전 구성 (추가/새로 고침)의 영향을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-296">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="1367c-297">작업 게시/새로 고침 후 UPM 솔루션은 사용자 통합을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-297">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="1367c-298">있다는 UPM 솔루션이 구성 되는 방법에 따라 로그 오프 프로세스의 일부로 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-298">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="1367c-299">이는 사용자 상태를 유지 하는 것과 동일한/유사한 오버 헤드를 초래 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-299">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="1367c-300">후속 로그인:</span><span class="sxs-lookup"><span data-stu-id="1367c-300">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-301">작업 UPM 솔루션은 게시/새로 고침 전에 시스템에 사용자 통합을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-301">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="1367c-302">작업 추가/새로 고침은 모든 사용자 대상 응용 프로그램을 미리 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-302">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="1367c-303">있다는</span><span class="sxs-lookup"><span data-stu-id="1367c-303">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-304">이를 통해 응용 프로그램 가용성에 걸리는 시간 (10 초의 순서 대로)이 현저 하 게 증가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-304">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="1367c-305">이렇게 하면 가상 응용 프로그램의 수 및 복잡도 \*를 기준으로 게시 새로 고침 시간이 늘어납니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-305">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="1367c-306">작업 게시/새로 고침을 수행 하면 사용자 패키지 자격에 대 한 변경 내용에 대 한 게시 취소 및 게시 작업이 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-306">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-307">Fail</span><span class="sxs-lookup"><span data-stu-id="1367c-307">Outcome</span></span></th>
<th align="left"><span data-ttu-id="1367c-308">Fail</span><span class="sxs-lookup"><span data-stu-id="1367c-308">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="1367c-309">사용자 통합은 완전히 유지 되므로, 예를 들어, 게시/새로 고침이 완료 될 수 있도록 통합에 대 한 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-309">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="1367c-310">로그인의 초 내에 모든 가상 응용 프로그램을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-310">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="1367c-311">게시/새로 고침을 통해 환경에 영향을 주는 가상 응용 프로그램의 사용자에 대 한 변경 내용이 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-311">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1367c-312">추가/새로 고침이 모든 가상 응용 프로그램을 VM으로 다시 구성 해야 하기 때문에 모든 로그인의 게시 새로 고침 시간이 연장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-312">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="1367c-313">패키지 수명 주기에 대 한 영향</span><span class="sxs-lookup"><span data-stu-id="1367c-313">Impact to Package Life Cycle</span></span>

<span data-ttu-id="1367c-314">패키지 업그레이드는 패키지 수명 주기의 중요 한 측면입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-314">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="1367c-315">사용자가 적절 한 업그레이드 (게시) 또는 다운 그레이드 (게시 취소 된) 가상 응용 프로그램 패키지에 액세스할 수 있도록 하려면이 변경 내용을 반영 하도록 기본 이미지를 업데이트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-315">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="1367c-316">다음 섹션을 검토 하는 이유를 이해 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-316">To understand why review the following section:</span></span>

<span data-ttu-id="1367c-317">App-v 5.0 SP2에는 보류 상태의 개념이 도입 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-317">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="1367c-318">과거에는</span><span class="sxs-lookup"><span data-stu-id="1367c-318">In the past,</span></span>

-   <span data-ttu-id="1367c-319">관리자가 자격을 변경 하거나 패키지의 새 버전을 만들고 (업그레이드) 해당 패키지를 사용 하 고 있는 게시/새로 고침을 수행 하는 동안에는 게시 취소 또는 게시 작업이 각각 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-319">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="1367c-320">이제 패키지가 사용 중인 경우 작업이 보류 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-320">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="1367c-321">게시 취소 및 게시 대기 작업이 서비스를 다시 시작할 때 처리 되거나 다른 게시 또는 게시 취소 명령이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-321">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="1367c-322">후자의 경우, 가상 응용 프로그램이 사용 중인 경우에는 가상 응용 프로그램이 보류 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-322">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="1367c-323">전역적으로 게시 된 패키지의 경우 일반적으로 다시 시작 (또는 서비스 다시 시작)이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-323">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="1367c-324">비영구 환경에서는 이러한 보류 된 작업이 처리 되지 않을 가능성은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-324">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="1367c-325">예를 들어 보류 된 작업은 **HKEY \ _CURRENT \ _USER**  \\  **소프트웨어**  \\  **Microsoft**  \\  **AppV**  \\  **클라이언트**  \\  **pendingtasks**아래에 캡처됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-325">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="1367c-326">이 위치는 UPM 솔루션에 의해 유지 되지만 로그온 하기 전에 환경에 적용 되지 않으면 처리 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-326">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="1367c-327">성능 최적화 조정을 통해 VDI 환경 개선</span><span class="sxs-lookup"><span data-stu-id="1367c-327">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="1367c-328">다음 섹션에는 환경을 최적화 하는 데 유용할 수 있는 Microsoft 문서 및 다운로드에 대 한 정보가 포함 된 목록이 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-328">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="1367c-329">.NET NGEN 블로그 및 스크립트 (적극 권장)</span><span class="sxs-lookup"><span data-stu-id="1367c-329">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="1367c-330">NGEN 기술 정보</span><span class="sxs-lookup"><span data-stu-id="1367c-330">About NGEN technology</span></span>

-   [<span data-ttu-id="1367c-331">NGEN 최적화 속도를 향상 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1367c-331">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="1367c-332">스크립트</span><span class="sxs-lookup"><span data-stu-id="1367c-332">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="1367c-333">Windows Server 및 서버 역할</span><span class="sxs-lookup"><span data-stu-id="1367c-333">Windows Server and Server Roles</span></span>**

<span data-ttu-id="1367c-334">에 대 한 서버 성능 조정 지침</span><span class="sxs-lookup"><span data-stu-id="1367c-334">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="1367c-335">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1367c-335">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="1367c-336">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1367c-336">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="1367c-337">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1367c-337">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="1367c-338">서버 역할</span><span class="sxs-lookup"><span data-stu-id="1367c-338">Server Roles</span></span>**

-   [<span data-ttu-id="1367c-339">원격 데스크톱 가상화 호스트</span><span class="sxs-lookup"><span data-stu-id="1367c-339">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="1367c-340">원격 데스크톱 세션 호스트</span><span class="sxs-lookup"><span data-stu-id="1367c-340">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="1367c-341">IIS 관련성: 앱-V 관리, 게시, 보고 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="1367c-341">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="1367c-342">파일 서버 (SMB) 관련성: SCS 모드에서의 App-v 콘텐츠 저장소 및 배달에 사용 되는 경우</span><span class="sxs-lookup"><span data-stu-id="1367c-342">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="1367c-343">Windows 클라이언트 (게스트 OS) 성능 조정 지침</span><span class="sxs-lookup"><span data-stu-id="1367c-343">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="1367c-344">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="1367c-344">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="1367c-345">최적화 스크립트: (Microsoft 지원에서 제공)</span><span class="sxs-lookup"><span data-stu-id="1367c-345">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="1367c-346">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="1367c-346">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="1367c-347">최적화 스크립트: (Microsoft 지원에서 제공)</span><span class="sxs-lookup"><span data-stu-id="1367c-347">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="1367c-348">게시 성능을 위해 패키지를 최적화 하는 시퀀싱 단계</span><span class="sxs-lookup"><span data-stu-id="1367c-348">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="1367c-349">새로운 시나리오를 활용 하거나 새로운 고객 배포 시나리오를 사용할 수 있도록 하는 몇 가지 App-v 기능.</span><span class="sxs-lookup"><span data-stu-id="1367c-349">Several App-V features facilitate new scenarios or enable new customer deployment scenarios.</span></span> <span data-ttu-id="1367c-350">이러한 다음 기능은 게시 및 시작 작업의 성능에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-350">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-351">단계</span><span class="sxs-lookup"><span data-stu-id="1367c-351">Step</span></span></th>
<th align="left"><span data-ttu-id="1367c-352">고려 사항</span><span class="sxs-lookup"><span data-stu-id="1367c-352">Consideration</span></span></th>
<th align="left"><span data-ttu-id="1367c-353">혜택</span><span class="sxs-lookup"><span data-stu-id="1367c-353">Benefits</span></span></th>
<th align="left"><span data-ttu-id="1367c-354">최선의</span><span class="sxs-lookup"><span data-stu-id="1367c-354">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-355">기능 블록 1 (FB1, 기본 FB 라고도 함) 없음</span><span class="sxs-lookup"><span data-stu-id="1367c-355">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-356">No FB1는 시작 하는 동안 응용 프로그램이 즉시 실행 되 고 오류를 스트림 합니다 (응용 프로그램은 파일, DLL이 필요 하며, 네트워크를 통해 아래로 가져와야 함). 네트워크 제한 사항이 있는 경우 FB1는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-356">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="1367c-357">처음으로 응용 프로그램을 시작할 때 사용 되는 스트림 폴트 및 네트워크 대역폭 수를 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-357">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="1367c-358">전체 FB1 스트리밍할 때까지 시작을 지연 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-358">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="1367c-359">스트림이 실패 하면 실행 시간이 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-359">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-360">FB1 구성 된 가상 응용 프로그램 패키지는 다시 시퀀싱 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-360">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1367c-361">FB1 제거</span><span class="sxs-lookup"><span data-stu-id="1367c-361">Removing FB1</span></span>

<span data-ttu-id="1367c-362">FB1를 제거 하는 경우 원래 응용 프로그램 설치 관리자가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-362">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="1367c-363">다음 단계를 완료 한 후 시퀀서를 실행 하는 컴퓨터를 정리 스냅숏으로 되돌리는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-363">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="1367c-364">**SEQUENCER UI** -새 가상 응용 프로그램 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-364">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="1367c-365">사용자 지정-스트리밍을 위한 시퀀싱 단계를 완료 &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-365">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="1367c-366">스트리밍 단계에서 **느리거나 불안정 한 네트워크를 통해 배포용 패키지 최적화**를 선택 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-366">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="1367c-367">원하는 경우 **대상 OS**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-367">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="1367c-368">기존 가상 응용 프로그램 패키지 수정</span><span class="sxs-lookup"><span data-stu-id="1367c-368">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="1367c-369">스트리밍을 위한 시퀀싱 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-369">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="1367c-370">**느리거나 불안정 한 네트워크를 통해 배포용으로 패키지 최적화**를 선택 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-370">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="1367c-371">**패키지 만들기**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-371">Move to **Create Package**.</span></span>

<span data-ttu-id="1367c-372">**PowerShell** -기존 가상 응용 프로그램 패키지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-372">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="1367c-373">관리자 권한 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-373">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="1367c-374">가져오기-모듈 **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="1367c-374">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="1367c-375">**업데이트-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="1367c-375">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="1367c-376">"C:\\Packages\\MyPackage.appv"-설치 관리자</span><span class="sxs-lookup"><span data-stu-id="1367c-376">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="1367c-377">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1367c-377">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="1367c-378">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="1367c-378">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="1367c-379">참고</span><span class="sxs-lookup"><span data-stu-id="1367c-379">Note</span></span>**  
    <span data-ttu-id="1367c-380">이 cmdlet에는 실행 (.exe) 또는 배치 파일 (.bat)이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-380">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="1367c-381">비어 있는 (아무 작업도 수행 하지 않음) 실행 파일이 나 배치 파일을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-381">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-382">단계</span><span class="sxs-lookup"><span data-stu-id="1367c-382">Step</span></span></th>
<th align="left"><span data-ttu-id="1367c-383">고려 사항</span><span class="sxs-lookup"><span data-stu-id="1367c-383">Considerations</span></span></th>
<th align="left"><span data-ttu-id="1367c-384">혜택</span><span class="sxs-lookup"><span data-stu-id="1367c-384">Benefits</span></span></th>
<th align="left"><span data-ttu-id="1367c-385">최선의</span><span class="sxs-lookup"><span data-stu-id="1367c-385">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-386">게시할 때 SXS 설치 없음 (사전 설치 SxS 어셈블리)</span><span class="sxs-lookup"><span data-stu-id="1367c-386">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-387">가상 응용 프로그램 패키지는 다시 시퀀싱 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-387">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="1367c-388">SxS 어셈블리는 가상 응용 프로그램 패키지에 남아 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-388">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-389">게시 시간에 SxS 어셈블리 종속성이 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-389">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-390">SxS 어셈블리 종속성은 사전 설치 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-390">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1367c-391">Sequencer에서 새 가상 응용 프로그램 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="1367c-391">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="1367c-392">시퀀서 모니터링 중에 응용 프로그램 설치의 일부로 SxS 어셈블리 (예: VC + + 런타임)가 설치 되어 있으면 SxS 어셈블리가 자동으로 검색 되 고 패키지에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-392">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="1367c-393">관리자에 게 알림이 표시 되 고 SxS 어셈블리를 제외 하는 옵션이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-393">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="1367c-394">**클라이언트측**:</span><span class="sxs-lookup"><span data-stu-id="1367c-394">**Client Side**:</span></span>

<span data-ttu-id="1367c-395">가상 응용 프로그램 패키지를 게시할 때 App-v 클라이언트는 필수 SxS 종속성이 이미 설치 되어 있는지 여부를 감지 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-395">When publishing a virtual application package, the App-V Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="1367c-396">컴퓨터에서 종속성을 사용할 수 없고 패키지에 포함 된 경우 기존 Windows Installer (.\*\* msi\*\*) SxS 어셈블리 설치가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-396">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="1367c-397">앞에서 설명한 대로 클라이언트를 실행 하는 컴퓨터에 종속성을 설치 하면 Windows Installer (.msi) 설치가 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-397">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-398">단계</span><span class="sxs-lookup"><span data-stu-id="1367c-398">Step</span></span></th>
<th align="left"><span data-ttu-id="1367c-399">고려 사항</span><span class="sxs-lookup"><span data-stu-id="1367c-399">Considerations</span></span></th>
<th align="left"><span data-ttu-id="1367c-400">혜택</span><span class="sxs-lookup"><span data-stu-id="1367c-400">Benefits</span></span></th>
<th align="left"><span data-ttu-id="1367c-401">최선의</span><span class="sxs-lookup"><span data-stu-id="1367c-401">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-402">선택적으로 동적 구성 파일을 채택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-402">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-403">App-v 5.1 클라이언트는 이러한 동적 구성 파일을 구문 분석 하 고 처리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-403">The App-V 5.1 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="1367c-404">파일의 크기와 복잡도 (스크립트 실행, VREG 포함/제외)에 대해 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-404">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="1367c-405">많은 가상 응용 프로그램 패키지에 사용자 또는 컴퓨터 관련 동적 구성 파일이 이미 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-405">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-406">이러한 파일이 선택적으로 또는 전혀 사용 되지 않는 경우 게시 시간이 향상 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-406">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-407">가상 응용 프로그램 패키지는 연결 된 동적 구성 파일을 제거 하기 위해 개별적으로 또는 App-v 서버 관리 콘솔을 통해 다시 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-407">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1367c-408">Powershell을 사용 하 여 동적 구성 비활성화</span><span class="sxs-lookup"><span data-stu-id="1367c-408">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="1367c-409">이미 게시 된 패키지의 경우 다음 없이 사용할 수 있습니다. `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv`</span><span class="sxs-lookup"><span data-stu-id="1367c-409">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="1367c-410">**-Dynamicdeploymentconfiguration** 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1367c-410">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="1367c-411">마찬가지로,를 사용 하 여 새 패키지를 추가 하는 경우 다음을 `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` 사용 하지 마십시오.</span><span class="sxs-lookup"><span data-stu-id="1367c-411">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="1367c-412">**-Dynamicdeploymentconfiguration** 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="1367c-412">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="1367c-413">동적 구성을 적용 하는 방법에 대 한 설명서는 다음을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-413">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="1367c-414">PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="1367c-414">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [<span data-ttu-id="1367c-415">PowerShell을 사용하여 배포 구성 파일을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="1367c-415">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1367c-416">단계</span><span class="sxs-lookup"><span data-stu-id="1367c-416">Step</span></span></th>
<th align="left"><span data-ttu-id="1367c-417">고려 사항</span><span class="sxs-lookup"><span data-stu-id="1367c-417">Considerations</span></span></th>
<th align="left"><span data-ttu-id="1367c-418">혜택</span><span class="sxs-lookup"><span data-stu-id="1367c-418">Benefits</span></span></th>
<th align="left"><span data-ttu-id="1367c-419">최선의</span><span class="sxs-lookup"><span data-stu-id="1367c-419">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1367c-420">패키지 수명 주기 동안 동기 스크립트 실행을 위한 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-420">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-421">스크립트 참고가 패키지에 포함 된 경우 추가 (Powershell)가 매우 느릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-421">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="1367c-422">가상 응용 프로그램 시작 (StartVirtualEnvironment, StartProcess) 및/또는 추가 + 게시 중 스크립트를 실행 하면 이러한 주기 작업 중 하나 이상에서 인식 되는 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-422">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-423">비동기 (비블로킹) 스크립트를 사용 하 여 수명 주기 작업이 효율적으로 완료 되도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-423">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-424">이 단계에서는 포함 된 스크립트 참조를 사용 하는 모든 가상 응용 프로그램 패키지에 대 한 지식 (동적 구성 파일이 연결 되어 있고 스크립트를 동기적으로 실행 하는 경우)이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-424">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1367c-425">패키지에서 불필요 한 가상 글꼴을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-425">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-426">App-v 제품 팀에서 조사 하는 대부분의 응용 프로그램에는 적은 수의 글꼴이 포함 되어 있으며 일반적으로 20 개 미만입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-426">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-427">가상 글꼴은 게시 새로 고침 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-427">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1367c-428">원하는 글꼴은 기본적으로 사용 하도록 설정/설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-428">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="1367c-429">지침은 글꼴 설치 또는 제거를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1367c-429">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1367c-430">패키지에 존재 하는 가상 글꼴 확인</span><span class="sxs-lookup"><span data-stu-id="1367c-430">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="1367c-431">패키지 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-431">Make a copy of the package.</span></span>

-   <span data-ttu-id="1367c-432">패키지 \ _copy의 이름을 바꿉니다. Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="1367c-432">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="1367c-433">AppxManifest.xml를 열고 다음을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-433">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="1367c-434">&lt;appv: 확장 범주 = "AppV. 글꼴"&gt;</span><span class="sxs-lookup"><span data-stu-id="1367c-434">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="1367c-435">&lt;appv: Fonts&gt;</span><span class="sxs-lookup"><span data-stu-id="1367c-435">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="1367c-436">&lt;appv: 글꼴 경로 = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /appv: font&gt;</span><span class="sxs-lookup"><span data-stu-id="1367c-436">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="1367c-437">참고</span><span class="sxs-lookup"><span data-stu-id="1367c-437">Note</span></span>**  
    <span data-ttu-id="1367c-438">**Delayload**로 표시 된 글꼴이 있는 경우 첫 번째 시작에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-438">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="1367c-439">패키지에서 가상 글꼴 제외</span><span class="sxs-lookup"><span data-stu-id="1367c-439">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="1367c-440">사용자 범위에 가장 적합 한 동적 구성 파일 사용-컴퓨터의 모든 사용자에 대 한 배포 구성, 특정 사용자에 대 한 사용자 구성</span><span class="sxs-lookup"><span data-stu-id="1367c-440">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="1367c-441">배포 또는 사용자 구성에서 글꼴을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-441">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="1367c-442">글꼴</span><span class="sxs-lookup"><span data-stu-id="1367c-442">Fonts</span></span>

--&gt;

<span data-ttu-id="1367c-443">&lt;글꼴 사용 = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="1367c-443">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="1367c-444">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="1367c-444">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="1367c-445">앱-V 5.1 성능 지침 용어</span><span class="sxs-lookup"><span data-stu-id="1367c-445">App-V 5.1 Performance Guidance Terminology</span></span>


<span data-ttu-id="1367c-446">다음 용어는 App-v 5.1 성능 최적화와 관련 된 개념 및 작업을 설명 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-446">The following terms are used when describing concepts and actions related to App-V 5.1 performance optimization.</span></span>

-   <span data-ttu-id="1367c-447">**복잡도** – 사전 구성 (**추가-AppvClientPackage**) 또는 통합 (**게시-AppvClientPackage**) 중에 성능에 영향을 줄 수 있는 하나 이상의 패키지 특성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-447">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="1367c-448">일부 특성은 매니페스트 크기, 가상 글꼴 수, 파일 수 등입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-448">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="1367c-449">**비 통합** -사용자 통합이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-449">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="1367c-450">**다시 통합** -사용자 통합을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-450">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="1367c-451">**비 영구적인, 풀링됨** – 로그인 할 때마다 가상 환경을 실행 하는 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-451">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="1367c-452">**영구, 개인** – 모든 로그인에 대해 동일 하 게 유지 되는 가상 환경을 실행 하는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-452">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="1367c-453">이 문서의 **상태 저장** -사용자 통합이 세션 간에 유지 되며 사용자 환경 관리 기술이 비영구 RDSH 또는 VDI와 결합 하 여 사용 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-453">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="1367c-454">**상태 비저장** – 세션 간에 사용자 상태가 유지 되지 않는 시나리오를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-454">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="1367c-455">**트리거** – (또는 네이티브 동작 트리거).</span><span class="sxs-lookup"><span data-stu-id="1367c-455">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="1367c-456">UPM는 이러한 유형의 트리거를 사용 하 여 모니터링 또는 동기화 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-456">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="1367c-457">**사용자 환경** -app-v 5.1의 컨텍스트에서 quantitatively 사용자 환경은 다음 부분에 대 한 합계입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-457">**User Experience** - In the context of App-V 5.1, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="1367c-458">사용자가 데스크톱을 조작할 수 있을 때 로그인을 시작 하는 시점부터</span><span class="sxs-lookup"><span data-stu-id="1367c-458">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="1367c-459">데스크톱을 해당 지점으로 상호 작용할 수 있는 시점부터 (App-v 5.1 full server 인프라를 사용 하는 경우에는 PowerShell 용어로 동기화 됨) 게시 새로 고침이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-459">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.1 full server infrastructure.</span></span> <span data-ttu-id="1367c-460">독립 실행형 인스턴스에서 **AppVClientPackage** 및 **게시-AppVClientPackage Powershell** 명령이 시작 되는 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-460">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="1367c-461">게시 새로 고침 시작부터 완료까지</span><span class="sxs-lookup"><span data-stu-id="1367c-461">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="1367c-462">독립 실행형 인스턴스에서는 처음부터 마지막으로 게시 된 가상 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-462">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="1367c-463">바로 가기에서 가상 응용 프로그램을 사용할 수 있는 지점부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-463">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="1367c-464">또는 파일 형식 연결이 등록 된 시점부터 지정 된 가상 응용 프로그램을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-464">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="1367c-465">**사용자 프로필 관리** -환경과 연결 된 사용자 구성 요소를 관리 하는 제어 되 고 구조적인 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-465">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="1367c-466">예를 들어 사용자 프로필, 기본 설정 및 정책 관리, 응용 프로그램 제어 및 응용 프로그램 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-466">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="1367c-467">스크립팅 또는 타사 솔루션을 사용 하 여 필요에 따라 환경을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1367c-467">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="1367c-468">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1367c-468">Related topics</span></span>


[<span data-ttu-id="1367c-469">Microsoft Application Virtualization 5.1 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="1367c-469">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)









