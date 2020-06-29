---
title: Office와 App-V 사용 계획
description: Office와 App-V 사용 계획
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813412"
---
# <span data-ttu-id="270a8-103">Office와 App-V 사용 계획</span><span class="sxs-lookup"><span data-stu-id="270a8-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="270a8-104">Microsoft Application Virtualization (App-v) 5.1를 사용 하 여 Office를 배포 하는 방법을 계획 하려면 다음 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-104">Use the following information to plan how to deploy Office by using Microsoft Application Virtualization (App-V) 5.1.</span></span> <span data-ttu-id="270a8-105">이 문서에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-105">This article includes:</span></span>

-   [<span data-ttu-id="270a8-106">앱-V 언어 팩에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="270a8-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="270a8-107">지원 되는 Microsoft Office 버전</span><span class="sxs-lookup"><span data-stu-id="270a8-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="270a8-108">동시 버전의 Office를 사용 하 여 App-v 사용 계획</span><span class="sxs-lookup"><span data-stu-id="270a8-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="270a8-109">Office를 배포 하는 데 앱을 배포할 때 Office가 Windows와 통합 되는 방식</span><span class="sxs-lookup"><span data-stu-id="270a8-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="270a8-110">앱-V 언어 팩에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="270a8-110">App-V support for Language Packs</span></span>


<span data-ttu-id="270a8-111">앱-V 5.1 시퀀서를 사용 하 여 언어 팩, 언어 인터페이스 팩, 교정 도구 및 화면 설명 언어에 대 한 플러그 인 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-111">You can use the App-V 5.1 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="270a8-112">그런 다음 Office 배포 도구 키트를 사용 하 여 만드는 Office 2013 패키지와 함께 연결 그룹에 플러그 인 패키지를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="270a8-113">Office 응용 프로그램 및 플러그 인 언어 팩은 연결 그룹에서 함께 그룹화 되는 다른 모든 패키지와 마찬가지로 같은 연결 그룹에서 원활 하 게 상호 작용 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

><span data-ttu-id="270a8-114">**참고**  Microsoft Visio 및 Microsoft Project에서는 태국어 언어 팩을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="270a8-115">지원 되는 Microsoft Office 버전</span><span class="sxs-lookup"><span data-stu-id="270a8-115">Supported versions of Microsoft Office</span></span>

<span data-ttu-id="270a8-116">지원 되는 Office 제품 목록에 대해 [app-v가 지 원하는 Microsoft Office 제품 id를](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="270a8-116">See [Microsoft Office Product IDs that App-V supports](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) for a list of supported Office products.</span></span>
><span data-ttu-id="270a8-117">**Note** &nbsp; 참고 &nbsp; Office 배포 도구를 사용 하 여 Microsoft 365 for enterprise 앱에 대 한 App-v 패키지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-117">**Note**&nbsp;&nbsp;You must use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="270a8-118">볼륨 라이선스 버전의 Office Professional Plus 또는 Office Standard에 대 한 패키지 만들기는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-118">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span> <span data-ttu-id="270a8-119">App-v Sequencer를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-119">You cannot use the App-V Sequencer.</span></span>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="270a8-120">동시 버전의 Office를 사용 하 여 App-v 사용 계획</span><span class="sxs-lookup"><span data-stu-id="270a8-120">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="270a8-121">"Microsoft Office 공존"을 사용 하 여 같은 컴퓨터에 두 가지 버전의 Microsoft Office를 함께 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-121">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="270a8-122">Windows Installer 기반 (MSi) 버전의 Office, 간편 실행, 앱-V 5.1를 사용 하 여 office의 모든 주요 버전 조합 및 설치 방법이 적용 되는 Office 공존을 구현할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-122">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.1.</span></span> <span data-ttu-id="270a8-123">그러나 Microsoft는 Office 공존을 사용 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-123">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="270a8-124">Microsoft의 권장 가장 좋은 방법은 호환성 문제를 방지 하기 위해 Office 공존을 완전히 방지 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-124">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="270a8-125">그러나 최신 버전의 Office로 마이그레이션하는 경우에는 즉시 해결할 수 없는 문제가 발생할 수 있으므로, 최신 제품 버전으로 더 빠른 마이그레이션을 위해 동시 사용을 일시적으로 구현 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-125">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="270a8-126">장기간에 Office 공존을 사용 하는 것은 바람직하지 않으며 조직에는 향후에 완벽 하 게 전환 하는 계획이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-126">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="270a8-127">Office 공존을 구현 하기 전에</span><span class="sxs-lookup"><span data-stu-id="270a8-127">Before you implement Office coexistence</span></span>

<span data-ttu-id="270a8-128">Office 공존을 구현 하기 전에 다음 Office 문서를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="270a8-128">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="270a8-129">공존을 구현 하려는 최신 버전의 Office에 해당 하는 문서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-129">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="270a8-130">Office 버전</span><span class="sxs-lookup"><span data-stu-id="270a8-130">Office version</span></span></th>
<th align="left"><span data-ttu-id="270a8-131">지침 링크</span><span class="sxs-lookup"><span data-stu-id="270a8-131">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-132">Office 2013</span><span class="sxs-lookup"><span data-stu-id="270a8-132">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="270a8-133">다른 버전의 Office를 실행 하는 컴퓨터에서 Office 2013 도구 모음 및 프로그램 (MSI 배포)을 사용 하는 방법에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="270a8-133">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-134">Office 2010</span><span class="sxs-lookup"><span data-stu-id="270a8-134">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="270a8-135">다른 버전의 Office를 실행 하는 컴퓨터에서 Office 2010 제품군 및 프로그램을 사용 하는 방법에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="270a8-135">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="270a8-136">Office 설명서는 Windows Installer 기반 (MSi) 및 간편 실행 설치에 대 한 광범위 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-136">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="270a8-137">공존에 대 한이 App-v 항목은 App-v 배포와 관련 된 정보를 사용 하 여 Office 지침을 보완 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-137">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="270a8-138">지원 되는 Office 공존 시나리오</span><span class="sxs-lookup"><span data-stu-id="270a8-138">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="270a8-139">다음 표에는 지원 되는 공존 시나리오가 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-139">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="270a8-140">이는 현재 사용 중인 버전 및 배포 방법과 마이그레이션하는 버전 및 배포 방법에 따라 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-140">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="270a8-141">프로덕션 청중에 게 배포 하기 전에 모든 공존 솔루션을 철저히 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-141">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

><span data-ttu-id="270a8-142">**참고**  Microsoft는 원격 데스크톱 세션 호스트 역할 서비스를 사용 하도록 설정한 Windows Server 환경에서 여러 버전의 Office를 사용 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-142">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="270a8-143">Office 공존 시나리오를 실행 하려면이 역할 서비스를 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-143">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="270a8-144">Windows 통합 & Office 공존</span><span class="sxs-lookup"><span data-stu-id="270a8-144">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="270a8-145">Windows Installer 기반 및 간편 실행 Office 설치 방법은 기본 Windows 운영 체제의 특정 지점과 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-145">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="270a8-146">공존을 사용 하는 경우 두 Office 버전 간의 일반적인 운영 체제 통합이 충돌할 수 있으며,이 경우 호환성 및 사용자 경험 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-146">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="270a8-147">App-v를 사용 하 여 특정 버전의 Office를 시퀀싱 하 여 통합을 제외 하 여 운영 체제에서 "격리" 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-147">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="270a8-148">App-v가이 버전의 Office를 시퀀싱 할 수 있는 모드</span><span class="sxs-lookup"><span data-stu-id="270a8-148">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-149">Office 2007</span><span class="sxs-lookup"><span data-stu-id="270a8-149">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-150">항상 비 통합.</span><span class="sxs-lookup"><span data-stu-id="270a8-150">Always non-integrated.</span></span> <span data-ttu-id="270a8-151">App-v는 가상화 된 버전의 Office 2007와의 운영 체제 통합을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-151">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-152">Office 2010</span><span class="sxs-lookup"><span data-stu-id="270a8-152">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-153">통합 및 통합 되지 않음 모드.</span><span class="sxs-lookup"><span data-stu-id="270a8-153">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-154">Office 2013</span><span class="sxs-lookup"><span data-stu-id="270a8-154">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-155">항상 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-155">Always integrated.</span></span> <span data-ttu-id="270a8-156">Windows 운영 체제 통합은 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-156">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="270a8-157">Microsoft는 통합 된 Office 인스턴스 하나로 Office 공존을 배포 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-157">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="270a8-158">예를 들어 App-v를 사용 하 여 Office 2010 및 Office 2013을 배포 하는 경우 Office 2010을 통합 되지 않은 모드로 전환 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-158">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="270a8-159">통합 되지 않은 (격리 된) 모드에서의 Office 시퀀싱에 대 한 자세한 내용은 [Microsoft Application Virtualization 5.0에서 Microsoft Office 2010의 순서를 만드는 방법을](https://support.microsoft.com/kb/2830069)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="270a8-159">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="270a8-160">Office 공존 시나리오의 알려진 제한 사항</span><span class="sxs-lookup"><span data-stu-id="270a8-160">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="270a8-161">다음 섹션에서는 Office와 함께 공존을 구현 하는 데 App-v를 사용할 때 발생할 수 있는 몇 가지 문제에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-161">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="270a8-162">Windows Installer 기반/간편 실행 및 App-v Office 공존 시나리오에 공통적으로 적용 되는 제한 사항</span><span class="sxs-lookup"><span data-stu-id="270a8-162">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="270a8-163">동일한 컴퓨터에 다음 버전의 Office를 설치 하는 경우 다음과 같은 제한이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-163">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="270a8-164">Windows Installer 기반 버전을 사용 하 여 Office 2010</span><span class="sxs-lookup"><span data-stu-id="270a8-164">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="270a8-165">Office 2013-V 앱 사용</span><span class="sxs-lookup"><span data-stu-id="270a8-165">Office 2013 by using App-V</span></span>

<span data-ttu-id="270a8-166">이전 버전의 Windows Installer 기반 Office 2010과 함께 app-v를 사용 하 여 Office 2013을 게시 한 후에도 Windows Installer가 시작 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-166">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="270a8-167">이는 Windows Installer 기반 또는 간편 실행 버전의 Office 2010가 자동으로 컴퓨터에 등록 하려고 하기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-167">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="270a8-168">기본 Word 2010에 대 한 자동 등록 작업을 무시 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="270a8-168">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="270a8-169">Word 2010을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-169">Exit Word 2010.</span></span>

2.  <span data-ttu-id="270a8-170">다음을 실행 하 여 레지스트리 편집기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-170">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="270a8-171">Windows 7: **시작**을 클릭 하 고 검색 시작 상자에 **regedit** 를 입력 한 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-171">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="270a8-172">Windows 8.1 또는 Windows 10에서 **regedit** 를 입력 하 고 시작 페이지에서 enter 키를 누른 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-172">In Windows 8.1 or Windows 10, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="270a8-173">관리자 암호나 확인을 요청 하는 메시지가 표시 되 면 암호를 입력 하거나 **계속**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-173">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="270a8-174">다음 레지스트리 하위 키를 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-174">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="270a8-175">**편집** 메뉴에서 **새로 만들기**를 클릭 한 다음 **DWORD 값**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-175">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="270a8-176">없음/ **예**를 입력 하 고 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-176">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="270a8-177">없음을 마우스 오른쪽 **단추로 클릭 한** 다음 **수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-177">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="270a8-178">**Valuedata** 상자에 **1**을 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-178">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="270a8-179">파일 메뉴에서 **끝내기** 를 클릭 하 여 레지스트리 편집기를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-179">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="270a8-180">App-v를 사용 하 여 Office를 배포할 때 Office와 Windows가 통합 되는 방식</span><span class="sxs-lookup"><span data-stu-id="270a8-180">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="270a8-181">App-v를 사용 하 여 Office 2013를 배포 하는 경우 office가 App-v 없이 배포 될 때 office의 기능 및 기능을 최종 사용자에 게 제공 하는 운영 체제와 완벽 하 게 통합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-181">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="270a8-182">Office 2013 App-v 패키지는 Windows 운영 체제와 함께 다음과 같은 통합 지점을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-182">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="270a8-183">확장점</span><span class="sxs-lookup"><span data-stu-id="270a8-183">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="270a8-184">설명</span><span class="sxs-lookup"><span data-stu-id="270a8-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-185">Firefox 및 Chrome 용 Lync 모임 참가 플러그 인</span><span class="sxs-lookup"><span data-stu-id="270a8-185">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-186">사용자가 Firefox 및 Chrome에서 Lync 모임에 참가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-186">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-187">OneNote 인쇄 드라이버로 전송 됨</span><span class="sxs-lookup"><span data-stu-id="270a8-187">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-188">사용자가 OneNote에 인쇄할 수 있음</span><span class="sxs-lookup"><span data-stu-id="270a8-188">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-189">OneNote에 연결 된 노트</span><span class="sxs-lookup"><span data-stu-id="270a8-189">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-190">OneNote에 연결 된 노트</span><span class="sxs-lookup"><span data-stu-id="270a8-190">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-191">OneNote Internet Explorer 추가 기능으로 보내기</span><span class="sxs-lookup"><span data-stu-id="270a8-191">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-192">IE에서 OneNote로 보낼 수 있는 사용자</span><span class="sxs-lookup"><span data-stu-id="270a8-192">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-193">Lync 및 Outlook에 대 한 방화벽 예외</span><span class="sxs-lookup"><span data-stu-id="270a8-193">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-194">Lync 및 Outlook에 대 한 방화벽 예외</span><span class="sxs-lookup"><span data-stu-id="270a8-194">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-195">MAPI 클라이언트</span><span class="sxs-lookup"><span data-stu-id="270a8-195">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-196">기본 앱과 추가 기능은 MAPI를 통해 가상 Outlook과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-196">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-197">Firefox 용 SharePoint 플러그 인</span><span class="sxs-lookup"><span data-stu-id="270a8-197">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-198">사용자가 Firefox에서 SharePoint 기능을 사용할 수 있음</span><span class="sxs-lookup"><span data-stu-id="270a8-198">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-199">메일 제어판 애플릿</span><span class="sxs-lookup"><span data-stu-id="270a8-199">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-200">사용자가 Outlook의 메일 제어판 애플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-200">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-201">기본 Interop 어셈블리</span><span class="sxs-lookup"><span data-stu-id="270a8-201">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-202">관리 되는 추가 기능 지원</span><span class="sxs-lookup"><span data-stu-id="270a8-202">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-203">Office 문서 캐시 처리기</span><span class="sxs-lookup"><span data-stu-id="270a8-203">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-204">Office 응용 프로그램에 대해 문서 캐시를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="270a8-204">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-205">Outlook 프로토콜 검색 처리기</span><span class="sxs-lookup"><span data-stu-id="270a8-205">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-206">사용자가 outlook에서 검색할 수 있음</span><span class="sxs-lookup"><span data-stu-id="270a8-206">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-207">Active X 컨트롤:</span><span class="sxs-lookup"><span data-stu-id="270a8-207">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-208">ActiveX 컨트롤에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> Activex 컨트롤 API 참조를 참조 </a> 하세요.</span><span class="sxs-lookup"><span data-stu-id="270a8-208">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-209">SiteClient</span><span class="sxs-lookup"><span data-stu-id="270a8-209">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-210">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-210">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-211">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="270a8-211">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-212">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-212">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-213">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="270a8-213">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-214">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-214">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-215">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="270a8-215">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-216">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-216">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-217">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="270a8-217">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-218">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-218">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-219">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="270a8-219">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-220">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-220">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-221">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="270a8-221">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-222">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-222">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-223">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="270a8-223">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-224">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-224">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-225">Sharepoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="270a8-225">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-226">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-226">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-227">Sharepoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="270a8-227">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-228">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-228">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-229">WinProj</span><span class="sxs-lookup"><span data-stu-id="270a8-229">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-230">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-230">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-231">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="270a8-231">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-232">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-232">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-233">이 (가) Copysud.</span><span class="sxs-lookup"><span data-stu-id="270a8-233">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-234">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-234">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-235">CommunicatorMeetingJoinAx 관리자</span><span class="sxs-lookup"><span data-stu-id="270a8-235">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-236">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-236">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="270a8-237">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="270a8-237">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-238">Active X 컨트롤</span><span class="sxs-lookup"><span data-stu-id="270a8-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="270a8-239">OneDrive Pro 브라우저 도우미</span><span class="sxs-lookup"><span data-stu-id="270a8-239">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-240">Active X Control]</span><span class="sxs-lookup"><span data-stu-id="270a8-240">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-241">OneDrive Pro 아이콘 오버레이</span><span class="sxs-lookup"><span data-stu-id="270a8-241">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="270a8-242">사용자가 폴더를 찾을 때 Windows 탐색기 셸 아이콘 오버레이 (OneDrive Pro 폴더)</span><span class="sxs-lookup"><span data-stu-id="270a8-242">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-243">셸 확장</span><span class="sxs-lookup"><span data-stu-id="270a8-243">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="270a8-244">정의</span><span class="sxs-lookup"><span data-stu-id="270a8-244">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="270a8-245">Windows 검색</span><span class="sxs-lookup"><span data-stu-id="270a8-245">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





