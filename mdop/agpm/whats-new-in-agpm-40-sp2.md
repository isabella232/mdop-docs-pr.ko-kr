---
title: AGPM 4.0 SP2의 새로운 기능
description: AGPM 4.0 SP2의 새로운 기능
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818148"
---
# <span data-ttu-id="194d0-103">AGPM 4.0 SP2의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="194d0-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="194d0-104">이 콘텐츠는 Microsoft AGPM (고급 그룹 정책 관리)의 Pack2에 대 한 향상 된 구성 및 지원 되는 SP2 (서비스)를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="194d0-105">이 콘텐츠와 다른 AGPM 설명서 사이에 차이가 있는 경우이 콘텐츠를 신뢰할 수 있는 것으로 간주 하 고 다른 문서를 대체 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="194d0-106">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="194d0-106">What’s new</span></span>


<span data-ttu-id="194d0-107">AGPM 4.0 SP2는 다음 기능과 기능을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="194d0-108">Windows 8.1 및 Windows Server2012 R2에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="194d0-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="194d0-109">AGPM 4.0 SP2는 Windows 8.1 및 Windows Server2012 R2 운영 시스템에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="194d0-110">새로 만들고 변경 된 클라이언트 쪽 확장</span><span class="sxs-lookup"><span data-stu-id="194d0-110">New and changed client-side extensions</span></span>

<span data-ttu-id="194d0-111">Windows 8.1에서 새 정책 설정을 지원 하도록 AGPM에 대해 그룹 정책 클라이언트 쪽 확장이 추가 또는 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="194d0-112">그룹 정책 관리자는 이러한 정책 설정을 통해 두 Gpo (그룹 정책 개체) 또는 서식 파일 간에 변경 되는 Windows 8.1 관련 정책 설정을 관리 하 고 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="194d0-113">클라이언트 쪽 확장을 보려면 AGPM 클라이언트에서 사용할 수 있는 설정 및 차이점 보고서를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="194d0-114">새로 만들고 변경 된 그룹 정책 클라이언트 쪽 확장명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="194d0-115">**클라우드 폴더 설정을 지정**합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="194d0-116">이 정책 설정을 사용 하면 IT 관리자가 클라우드 폴더를 자동으로 만들도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="194d0-117">클라우드 폴더 기능을 사용 하면 최종 사용자가 Windows 데스크톱 장치에서 다른 장치로 파일을 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="194d0-118">이 정책 설정을 사용 하 여 최종 사용자의 장치에 대 한 동기화 관계를 만들고 사용자의 클라우드 폴더를 저장 하는 파일 서버를 식별 하는 방법을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="194d0-119">**자동 프로 비전 동기화** 확인란을 선택 하면 사용자 입력 없이 동기화 파트너 관계가 생성 되 고 데이터가 자동으로 사용자의 디바이스와 동기화 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="194d0-120">**자동 프로 비전 동기화** 확인란을 선택 하지 않은 경우 사용자가 동기화를 시작 하기 위한 입력을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="194d0-121">**모든 사용자에 대해 자동 설정을 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="194d0-122">이 정책 설정을 사용 하면 IT 관리자가 최종 사용자의 입력 없이 최종 사용자 장치에서 자동으로 클라우드 폴더 파트너 관계를 만들지 여부를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="194d0-123">이 정책 설정을 사용 하면 **클라우드 폴더 설정 지정** 정책 설정을 구성 하는 방법에 따라 동기화가 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="194d0-124">**모든 사용자에 대해 자동 설정 적용** 정책 설정을 **사용 안 함** 또는 **구성 되지 않음**으로 설정한 경우 **클라우드 폴더 설정 지정** 정책 설정에서 **자동 프로 비전** 옵션을 설정 하는 방법에 따라 작업 폴더의 파트너 관계가 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="194d0-125">클라우드 폴더 기능에 대 한 자세한 내용은 [클라우드 폴더 개요](https://go.microsoft.com/fwlink/?LinkId=330444)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="194d0-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="194d0-126">고객 의견 및 핫픽스 롤업</span><span class="sxs-lookup"><span data-stu-id="194d0-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="194d0-127">AGPM 4.0 SP2에는 AGPM 4.0 SP1(서비스 Pack1) 릴리스 이후 발견 된 문제를 해결 하는 핫픽스의 롤업이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="194d0-128">AGPM 4.0 SP2에는 Microsoft 고급 그룹 정책 관리 4.0 SP1 Hotfix1에 대 한 최신 수정 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="194d0-129">자세한 내용은 기술 자료 문서 [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="194d0-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="194d0-130">설정 및 차이점 보고서의 새로운 그룹 정책 확장</span><span class="sxs-lookup"><span data-stu-id="194d0-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="194d0-131">설정 및 차이점 보고서에 새 그룹 정책 확장이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="194d0-132">설치 관리자 변경 및 지원</span><span class="sxs-lookup"><span data-stu-id="194d0-132">Installer changes and support</span></span>

<span data-ttu-id="194d0-133">AGPM 4.0 SP2 설치 관리자에 대 한 변경 및 지원은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="194d0-134">Windows 8 또는 Windows Server 2012 운영 체제 이상 운영 체제에 AGPM 4.0 SP2를 설치 하는 경우 AGPM 설치 관리자가 필수 필수 구성 요소 소프트웨어 (GPMC (그룹 정책 관리 콘솔) 및 Microsoft .NET Framework 3.5)가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="194d0-135">이 필수 소프트웨어가 설치 되어 있지 않으면 AGPM 4.0 SP2 설치가 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="194d0-136">AGPM 서버를 설치할 때 WCF 활성화, 비 HTTP 활성화 및 Windows 프로세스 활성화 서비스가 자동으로 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="194d0-137">WindowsVista 클라이언트 운영 체제 및 이후 버전의 운영 시스템에서는 AGPM 4.0 SP2를 설치 하기 전에 해당 운영 체제의 적절 한 버전의 원격 시스템 관리 도구를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="194d0-138">AGPM 4.0 SP2는 이전에 지원 되는 운영 체제와의 호환성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="194d0-139">구성 매개 변수를 사용 하지 않고 AGPM 4.0 SP2로 업그레이드 하는 기능</span><span class="sxs-lookup"><span data-stu-id="194d0-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="194d0-140">다음 표에 표시 된 대로 agpm 4.0 이후 구성 매개 변수 (스마트 업그레이드)를 다시 입력 하 라는 메시지가 표시 되지 않고 agpm 클라이언트 또는 AGPM 서버를 AGPM 4.0 SP2로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="194d0-141">표에서와 같이 다른 버전의 AGPM으로 AGPM 4.0 SP2로 업그레이드 하는 경우에는 구성 매개 변수를 다시 입력 해야 하는 클래식 업그레이드를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="194d0-142">각 버전의 AGPM이 특정 운영 체제와 연결 되어 있기 때문에 [설치할 Agpm 버전 선택을](https://go.microsoft.com/fwlink/?LinkId=254350) 참조 하 여 agpm을 업그레이드 하기 전에 해당 운영 체제를 적절 하 게 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="194d0-143">AGPM 4.0 SP2 지원 되는 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-143">AGPM 4.0 SP2 supported upgrades</span></span>**

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
<td align="left"><p><strong><span data-ttu-id="194d0-144">업그레이드할 수 있는 AGPM 버전</span><span class="sxs-lookup"><span data-stu-id="194d0-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="194d0-145">2.5</span><span class="sxs-lookup"><span data-stu-id="194d0-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="194d0-146">3.0</span><span class="sxs-lookup"><span data-stu-id="194d0-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="194d0-147">4.0</span><span class="sxs-lookup"><span data-stu-id="194d0-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="194d0-148">4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="194d0-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="194d0-149">4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="194d0-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="194d0-150">2.5</span><span class="sxs-lookup"><span data-stu-id="194d0-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-151">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-152">클래식 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-153">클래식 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-154">설치 차단 됨</span><span class="sxs-lookup"><span data-stu-id="194d0-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-155">설치 차단 됨</span><span class="sxs-lookup"><span data-stu-id="194d0-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="194d0-156">3.0</span><span class="sxs-lookup"><span data-stu-id="194d0-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-157">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-158">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-159">클래식 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-160">설치 차단 됨</span><span class="sxs-lookup"><span data-stu-id="194d0-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-161">설치 차단 됨</span><span class="sxs-lookup"><span data-stu-id="194d0-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="194d0-162">4.0</span><span class="sxs-lookup"><span data-stu-id="194d0-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-163">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-164">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-165">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-166">스마트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-167">스마트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="194d0-168">4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="194d0-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-169">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-170">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-171">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-172">해당 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-173">스마트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="194d0-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="194d0-174">지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="194d0-174">Supported configurations</span></span>


<span data-ttu-id="194d0-175">AGPM 4.0 SP2는 다음 표의 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="194d0-176">AGPM이 혼합 구성을 지원 하지만, windows Server2012 R2, windows 8 for windows Server 2012와 같은 운영 체제 줄에서 AGPM 클라이언트와 AGPM 서버를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="194d0-177">AGPM 4.0 SP2 지원 되는 운영 체제 및 정책 설정</span><span class="sxs-lookup"><span data-stu-id="194d0-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="194d0-178">AGPM 서버에서 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="194d0-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="194d0-179">AGPM 클라이언트에 대해 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="194d0-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="194d0-180">AGPM 지원</span><span class="sxs-lookup"><span data-stu-id="194d0-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="194d0-181">Windows Server2012 R2 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="194d0-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-182">Windows Server2012 R2 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="194d0-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-183">지원함</span><span class="sxs-lookup"><span data-stu-id="194d0-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="194d0-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 또는 Windows 8</span><span class="sxs-lookup"><span data-stu-id="194d0-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-185">Windows Server 2012 또는 Windows 8</span><span class="sxs-lookup"><span data-stu-id="194d0-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-186">지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="194d0-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="194d0-187">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="194d0-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-188">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="194d0-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-189">지원 되지만, Windows 8.1 또는 Windows 8에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="194d0-190">Windows Server 2012, Windows Server2008R2, Windows 8 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="194d0-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-191">Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</span><span class="sxs-lookup"><span data-stu-id="194d0-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-192">지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="194d0-193">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="194d0-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-194">Windows Server 2012, Windows Server2008R2, Windows 8 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="194d0-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-195">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="194d0-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="194d0-196">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="194d0-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-197">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="194d0-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="194d0-198">지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="194d0-199">AGPM 4.0 SP2 설치를 위한 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="194d0-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="194d0-200">다음 표에서는 Windows 8.1에서 .NET Framework 3.5 또는 원격 서버 관리 도구의 GPMC가 없는 경우 AGPM 4.0 SP2 클라이언트 및 서버 설치 관리자의 동작에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="194d0-201">AGPM 클라이언트</span><span class="sxs-lookup"><span data-stu-id="194d0-201">AGPM Client</span></span>**

**<span data-ttu-id="194d0-202">AGPM 서버</span><span class="sxs-lookup"><span data-stu-id="194d0-202">AGPM Server</span></span>**

**<span data-ttu-id="194d0-203">운영 체제</span><span class="sxs-lookup"><span data-stu-id="194d0-203">Operating system</span></span>**

**<span data-ttu-id="194d0-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="194d0-204">.NET Framework</span></span>**

**<span data-ttu-id="194d0-205">원격 서버 관리 도구</span><span class="sxs-lookup"><span data-stu-id="194d0-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="194d0-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="194d0-206">.NET Framework</span></span>**

**<span data-ttu-id="194d0-207">원격 서버 관리 도구</span><span class="sxs-lookup"><span data-stu-id="194d0-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="194d0-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="194d0-208">Windows8.1</span></span>**

<span data-ttu-id="194d0-209">.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="194d0-210">GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="194d0-211">.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="194d0-212">GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되지 않은 경우 설치 관리자에서 설치가 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="194d0-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="194d0-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="194d0-214">.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="194d0-215">GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="194d0-216">.NET Framework 3.5가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자가 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="194d0-217">GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="194d0-218">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="194d0-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="194d0-219">AGPM 4.0 SP2는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="194d0-220">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="194d0-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="194d0-221">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="194d0-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="194d0-222">관련 항목</span><span class="sxs-lookup"><span data-stu-id="194d0-222">Related topics</span></span>


[<span data-ttu-id="194d0-223">고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="194d0-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="194d0-224">Microsoft 고급 그룹 정책 관리 4.0 SP2 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="194d0-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="194d0-225">설치할 AGPM 버전 선택</span><span class="sxs-lookup"><span data-stu-id="194d0-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





