---
title: AGPM 4.0 SP1의 새로운 기능
description: AGPM 4.0 SP1의 새로운 기능
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818153"
---
# <span data-ttu-id="f36a3-103">AGPM 4.0 SP1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f36a3-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="f36a3-104">이 "새로운 기능" 콘텐츠는 Microsoft AGPM (고급 그룹 정책 관리) 4.0 SP1에 대 한 개선 및 지원 되는 구성을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="f36a3-105">이 콘텐츠 및 다른 AGPM 설명서 사이에 차이가 있는 경우이 콘텐츠는 정식으로 간주 되어야 하며이 제품에 포함 된 콘텐츠를 대체 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="f36a3-106">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="f36a3-106">What’s new</span></span>


<span data-ttu-id="f36a3-107">AGPM 4.0 SP1에서는 다음과 같은 향상 된 기능을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="f36a3-108">새로 만들고 변경 된 클라이언트 쪽 확장</span><span class="sxs-lookup"><span data-stu-id="f36a3-108">New and changed client-side extensions</span></span>

<span data-ttu-id="f36a3-109">Windows 8 및 Windows Server 2012에서 새 그룹 정책을 지원 하도록 AGPM에 대해 CSEs (그룹 정책 클라이언트 쪽 확장)가 추가 또는 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="f36a3-110">그룹 정책 관리자는 이러한 그룹 정책을 사용 하 여 두 Gpo (그룹 정책 개체) 또는 서식 파일 간에 변경 되는 Windows 8 관련 그룹 정책 설정을 관리 하 고 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="f36a3-111">Windows 8 관련 설정을 사용 하 여 사용자 지정 Gpo를 만들고 Gpo를 서식 파일로 구성 하 고 저장할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="f36a3-112">CSEs를 보려면 AGPM 4.0 SP1 클라이언트에서 사용할 수 있는 설정 및 차이점 보고서를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="f36a3-113">새로 만들고 변경 된 그룹 정책 클라이언트 쪽 확장명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="f36a3-114">**중앙 액세스 정책:** 그룹 정책 관리자가 그룹 정책 서버 (예: 파일 서버)에서 중앙 액세스 정책을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="f36a3-115">중앙 액세스 정책은 GPO 항목으로 지정 되 고, 리소스의 중앙 집중화 된 액세스 및 제어를 위해 정책 대상에 적용 되는 권한 부여 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="f36a3-116">이러한 중앙 액세스 정책은 Active Directory 내에서 그룹 정책 클라이언트 컴퓨터에 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="f36a3-117">그룹 정책은 해당 중앙 액세스 정책에 대 한 정보를 적용 해야 하는 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="f36a3-118">**이름 확인 정책 변경 내용:** 그룹 정책 관리자가 DNS 클라이언트 컴퓨터에서 DNS 보안 및 DirectAccess에 대 한 설정을 구성할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="f36a3-119">일반 DNS 서버 설정 및 인코딩 설정 구성을 위한 새 탭이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="f36a3-120">**그룹 정책 기본 설정 변경 내용:** Windows 8에 추가 된 Internet Explorer 10 설정의 구성 및 관리에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="f36a3-121">**원격 응용 프로그램 및 데스크톱 연결:** 그룹 정책 관리자가 원격 응용 프로그램 및 데스크톱 연결에 사용 되는 기본 연결 URL을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="f36a3-122">**Windows To Go 시작 옵션:** Windows To Go 작업 영역이 포함 된 USB 장치가 연결 되어 있는 경우 그룹 정책 관리자가 Windows to Go로 부팅 되는지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="f36a3-123">**Windows To Go 최대 절전 모드 옵션:** Windows To Go 작업 영역에서 컴퓨터를 시작할 때 컴퓨터에서 최대 절전 모드 절전 상태 (S4)를 사용할 수 있는지 여부를 그룹 정책 관리자가 구성할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="f36a3-124">고객 의견 및 핫픽스 롤업</span><span class="sxs-lookup"><span data-stu-id="f36a3-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="f36a3-125">AGPM 4.0 SP1에는 AGPM 4.0 릴리스 이후 발견 된 문제 해결에 대 한 수정 롤업이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="f36a3-126">AGPM 4.0 SP1에는 Microsoft 고급 그룹 정책 관리 4.0 핫픽스 1에 대 한 최신 수정 사항이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="f36a3-127">설정 및 차이점 보고서에 새 그룹 정책 확장이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="f36a3-128">설정 및 차이점 보고서에 새 그룹 정책 확장이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="f36a3-129">설치 관리자 변경 및 지원</span><span class="sxs-lookup"><span data-stu-id="f36a3-129">Installer changes and support</span></span>

<span data-ttu-id="f36a3-130">AGPM 4.0 SP1 설치 관리자에 대 한 변경 및 지원은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="f36a3-131">Windows 8 또는 Windows Server 2012에 AGPM 4.0 SP1을 설치 하는 경우 AGPM 설치 관리자가 필수 필수 구성 요소 소프트웨어 (그룹 정책 관리 콘솔 및 .NET 3.5 프레임 워크)가 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="f36a3-132">이러한 전제 조건이 설치 되어 있지 않으면 AGPM 4.0 SP1 설치가 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="f36a3-133">AGPM 4.0 SP1을 설치 하면 WCF 정품 인증, 비 HTTP 정품 인증 및 Windows 프로세스 활성화 서비스가 자동으로 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="f36a3-134">Windows Vista, Windows 7 및 Windows 8 클라이언트 운영 체제에서는 AGPM 4.0 SP1을 설치 하기 전에 운영 체제에 적합 한 버전의 원격 시스템 관리 도구 키트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="f36a3-135">이전에 지원 되는 운영 체제와의 이전 버전과의 호환성이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="f36a3-136">구성 매개 변수를 다시 입력 하지 않고 AGPM 4.0 SP1로 업그레이드 하거나 업데이트 하는 기능</span><span class="sxs-lookup"><span data-stu-id="f36a3-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="f36a3-137">다음 표에 표시 된 대로 구성 매개 변수 ("Smart Upgrade")를 다시 입력 하지 않고 agpm 4.0에서 agpm 4.0 SP1로, agpm 클라이언트 또는 서버를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="f36a3-138">표에서와 같이 다른 버전의 AGPM으로 AGPM 4.0 SP1로 업그레이드 하는 경우에는 구성 매개 변수를 다시 입력 해야 하는 "클래식 업그레이드"를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="f36a3-139">각 버전의 AGPM이 특정 운영 체제와 연결 되어 있으므로 [설치할 Agpm 버전 선택](https://go.microsoft.com/fwlink/?LinkId=254350)을 참조 하 고 업그레이드를 수행 하기 전에 운영 체제를 적절 하 게 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f36a3-140">업그레이드할 수 있는 AGPM 버전</span><span class="sxs-lookup"><span data-stu-id="f36a3-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f36a3-141">2.5</span><span class="sxs-lookup"><span data-stu-id="f36a3-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f36a3-142">3.0</span><span class="sxs-lookup"><span data-stu-id="f36a3-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f36a3-143">4.0</span><span class="sxs-lookup"><span data-stu-id="f36a3-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f36a3-144">4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f36a3-145">2.5</span><span class="sxs-lookup"><span data-stu-id="f36a3-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-146">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-147">클래식 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f36a3-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-148">클래식 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f36a3-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-149">설치 차단 됨</span><span class="sxs-lookup"><span data-stu-id="f36a3-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f36a3-150">3.0</span><span class="sxs-lookup"><span data-stu-id="f36a3-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-151">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-152">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-153">클래식 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f36a3-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-154">설치 차단 됨</span><span class="sxs-lookup"><span data-stu-id="f36a3-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f36a3-155">4.0</span><span class="sxs-lookup"><span data-stu-id="f36a3-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-156">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-157">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-158">해당 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-159">스마트 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f36a3-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f36a3-160">지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="f36a3-160">Supported configurations</span></span>


<span data-ttu-id="f36a3-161">AGPM은 다음 표의 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="f36a3-162">AGPM이 혼합 구성을 지원 하지만, windows Server 2012, windows Server 2008 R2와 같이 windows 8과 같은 운영 체제 제품군에서 AGPM 클라이언트와 서버를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f36a3-163">AGPM 4.0 SP1 서버용으로 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="f36a3-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f36a3-164">AGPM 4.0 SP1 클라이언트에 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="f36a3-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f36a3-165">AGPM 4.0 SP1 지원</span><span class="sxs-lookup"><span data-stu-id="f36a3-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f36a3-166">Windows 8 또는 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f36a3-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-167">Windows 8 또는 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f36a3-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-168">지원함</span><span class="sxs-lookup"><span data-stu-id="f36a3-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f36a3-169">Windows Server 2008 R2 또는 Windows 7</span><span class="sxs-lookup"><span data-stu-id="f36a3-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-170">Windows Server 2008 R2 또는 Windows 7</span><span class="sxs-lookup"><span data-stu-id="f36a3-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-171">지원 되지만 Windows 8에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="f36a3-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f36a3-172">Windows Server 2008 R2 또는 Windows 7 또는 windows 8 또는 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f36a3-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-173">Windows Server 2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-174">지원 되지만, Windows Server 2008 R2 또는 Windows 7 또는 Windows 8에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f36a3-175">Windows Server 2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-176">Windows Server 2008 R2 또는 Windows 7 또는 windows 8 또는 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f36a3-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-177">지원함</span><span class="sxs-lookup"><span data-stu-id="f36a3-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f36a3-178">Windows Server 2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-179">Windows Server 2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f36a3-180">지원 되지만, Windows Server 2008 R2 또는 Windows 7 또는 Windows 8에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f36a3-181">AGPM 4.0 SP1 설치를 위한 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="f36a3-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="f36a3-182">다음 표에는 Windows 8 용 AGPM 4.0 SP1 클라이언트 및 서버 설치 관리자에서 .NET 3.5 또는 RSAT (원격 서버 관리 도구)의 그룹 정책 관리 콘솔이 없는 경우의 동작에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="f36a3-183">AGPM 클라이언트 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="f36a3-184">AGPM 서버 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f36a3-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="f36a3-185">운영 체제</span><span class="sxs-lookup"><span data-stu-id="f36a3-185">Operating System</span></span>**

**<span data-ttu-id="f36a3-186">.NET</span><span class="sxs-lookup"><span data-stu-id="f36a3-186">.NET</span></span>**

**<span data-ttu-id="f36a3-187">RSAT</span><span class="sxs-lookup"><span data-stu-id="f36a3-187">RSAT</span></span>**

**<span data-ttu-id="f36a3-188">.NET</span><span class="sxs-lookup"><span data-stu-id="f36a3-188">.NET</span></span>**

**<span data-ttu-id="f36a3-189">RSAT</span><span class="sxs-lookup"><span data-stu-id="f36a3-189">RSAT</span></span>**

**<span data-ttu-id="f36a3-190">Windows8</span><span class="sxs-lookup"><span data-stu-id="f36a3-190">Windows 8</span></span>**

<span data-ttu-id="f36a3-191">.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="f36a3-192">시스템에 GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="f36a3-193">.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="f36a3-194">시스템에 GPMC가 사용 하도록 설정 되어 있지 않거나 설치 되어 있지 않은 경우 설치 관리자에서 설치가 차단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="f36a3-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f36a3-195">Windows Server 2012</span></span>**

<span data-ttu-id="f36a3-196">.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="f36a3-197">GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="f36a3-198">.NET 3.5을 사용할 수 없거나 설치 되어 있지 않은 경우 설치 관리자에서 해당 설치를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="f36a3-199">GPMC를 사용할 수 없는 경우 설치 하는 동안 설치 관리자가 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36a3-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="f36a3-200">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f36a3-200">Related topics</span></span>


[<span data-ttu-id="f36a3-201">고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="f36a3-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="f36a3-202">Microsoft 고급 그룹 정책 관리 4.0 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="f36a3-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





