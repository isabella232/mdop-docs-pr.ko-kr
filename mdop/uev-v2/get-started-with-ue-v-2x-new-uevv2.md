---
title: UE-V 2.x 시작
description: UE-V 2.x 시작
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823288"
---
# <span data-ttu-id="35bb4-103">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="35bb4-103">Get Started with UE-V 2.x</span></span>


<span data-ttu-id="35bb4-104">이 가이드의 단계를 따라 작은 테스트 환경에서 Microsoft UE-V (User Experience Virtualization) 2.0 또는 2.1을 신속 하 게 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-104">Follow the steps in this guide to quickly deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 in a small test environment.</span></span> <span data-ttu-id="35bb4-105">이는 UE-V가 엔터프라이즈 내의 여러 장치에서 사용자 설정을 관리 하기 위한 올바른 솔루션 인지 여부를 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-105">This helps you determine whether UE-V is the right solution to manage user settings across multiple devices within your enterprise.</span></span>

<span data-ttu-id="35bb4-106">**참고**  이 섹션의 정보는 설명서의 나머지 부분에 걸쳐 더 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-106">**Note** The information in this section is repeated in greater detail throughout the rest of the documentation.</span></span> <span data-ttu-id="35bb4-107">따라서 UE-V 2가 올바른 솔루션이 고이를 평가할 필요가 없는 경우에는 오른쪽으로 이동 하 여 [ue-v 2. x 배포를 준비할](prepare-a-ue-v-2x-deployment-new-uevv2.md)수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-107">So if you already know that UE-V 2 is the right solution and you don’t need to evaluate it, you can just go right to [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md).</span></span>

 

<span data-ttu-id="35bb4-108">UE-V의 표준 설치는 기본 Microsoft Windows 및 Office 설정과 여러 Windows 앱 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-108">The standard installation of UE-V synchronizes the default Microsoft Windows and Office settings and many Windows app settings.</span></span> <span data-ttu-id="35bb4-109">테스트 환경에 네트워크 액세스를 공유 하는 두 명 이상의 사용자 컴퓨터가 포함 되어 있는지 확인 하 고 짧은 시간에 UE-V을 평가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-109">Make sure your test environment includes two or more user computers that share network access and you’ll be evaluating UE-V in just a short time.</span></span>

-   <span data-ttu-id="35bb4-110">[1 단계: 선행 조건 확인](#step1): 지원 되는 구성에 대 한 세부 정보를 포함 하 여 사용자의 환경이 ue-v를 실행할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-110">[Step 1: Confirm Prerequisites](#step1): Make sure your environment is able to run UE-V, including details about supported configurations.</span></span>

-   <span data-ttu-id="35bb4-111">[2 단계: ue-v 2에 대 한 설정 저장소 위치 배포](#step2): 모든 ue-v 배포에는 동기화 된 설정 값이 포함 된 설정 패키지의 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-111">[Step 2: Deploy the Settings Storage Location for UE-V 2](#step2): All UE-V deployments require a location for settings packages that contain the synchronized setting values.</span></span>

-   <span data-ttu-id="35bb4-112">[3 단계:](#step3)ue-v를 사용 하 여 설정을 동기화 하려면 장치에 ue-v agent가 설치 되어 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-112">[Step 3: Deploy the UE-V 2 Agent](#step3): To synchronize settings using UE-V, devices must have the UE-V Agent installed and running.</span></span>

-   <span data-ttu-id="35bb4-113">[4 단계:](#step4)ue-v agent가 설치 된 두 대의 컴퓨터에서 몇 가지 테스트를 실행 하 고 ue-v를 사용 하 여 작동 하는 방법을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-113">[Step 4: Test Your UE-V 2 Evaluation Deployment](#step4): Run a few tests on two computers that have the UE-V Agent installed and see how UE-V works.</span></span>

<span data-ttu-id="35bb4-114">그거에요!</span><span class="sxs-lookup"><span data-stu-id="35bb4-114">That’s it!</span></span> <span data-ttu-id="35bb4-115">이 단계를 수행 하 고 나면 엔터프라이즈에서 UE-V를 사용 하는 방법을 평가할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-115">Once you follow the steps, you’ll be able to evaluate how UE-V can work in your enterprise.</span></span>

<span data-ttu-id="35bb4-116">**추가 평가:** 또한 [사용자 지정 응용 프로그램의 배포 ue-v](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)를 사용 하 여 설정을 동기화 하도록 일부 타사 및 lob (기간 업무) 응용 프로그램을 구성 하는 추가 단계를 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-116">**Further evaluation:** You can also perform additional steps to configure some third-party and line-of-business applications to synchronize their settings using UE-V as detailed in [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <a href="" id="step1"></a><span data-ttu-id="35bb4-117">1 단계: 필수 구성 요소 확인</span><span class="sxs-lookup"><span data-stu-id="35bb4-117">Step 1: Confirm Prerequisites</span></span>


<span data-ttu-id="35bb4-118">계속 하기 전에 UE-V를 실행 하기 위한 요구 사항이 환경에 포함 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-118">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

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
<th align="left"><strong><span data-ttu-id="35bb4-119">운영 체제</span><span class="sxs-lookup"><span data-stu-id="35bb4-119">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="35bb4-120">버전</span><span class="sxs-lookup"><span data-stu-id="35bb4-120">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="35bb4-121">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="35bb4-121">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="35bb4-122">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="35bb4-122">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="35bb4-123">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="35bb4-123">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="35bb4-124">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="35bb4-124">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35bb4-125">Windows7</span><span class="sxs-lookup"><span data-stu-id="35bb4-125">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-126">Ultimate, Enterprise 또는 Professional Edition</span><span class="sxs-lookup"><span data-stu-id="35bb4-126">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-127">SP1</span><span class="sxs-lookup"><span data-stu-id="35bb4-127">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-128">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="35bb4-128">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-129">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-129">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-130">.NET Framework 4 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-130">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="35bb4-131">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="35bb4-131">Windows Server2008R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-132">표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</span><span class="sxs-lookup"><span data-stu-id="35bb4-132">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-133">SP1</span><span class="sxs-lookup"><span data-stu-id="35bb4-133">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-134">64비트</span><span class="sxs-lookup"><span data-stu-id="35bb4-134">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-135">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-135">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-136">.NET Framework 4 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-136">.NET Framework 4 or higher</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35bb4-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="35bb4-137">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-138">엔터프라이즈 또는 Pro</span><span class="sxs-lookup"><span data-stu-id="35bb4-138">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-139">없음</span><span class="sxs-lookup"><span data-stu-id="35bb4-139">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-140">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="35bb4-140">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-141">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-141">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-142">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="35bb4-142">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="35bb4-143">Windows Server 2012 또는 Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="35bb4-143">Windows Server 2012 or Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-144">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="35bb4-144">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-145">없음</span><span class="sxs-lookup"><span data-stu-id="35bb4-145">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-146">64비트</span><span class="sxs-lookup"><span data-stu-id="35bb4-146">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-147">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-147">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-148">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="35bb4-148">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="35bb4-149">Windows 10, 1607 전 verison</span><span class="sxs-lookup"><span data-stu-id="35bb4-149">Windows 10, pre-1607 verison</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-150">엔터프라이즈 또는 Pro</span><span class="sxs-lookup"><span data-stu-id="35bb4-150">Enterprise or Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="35bb4-151">32비트 또는 64비트</span><span class="sxs-lookup"><span data-stu-id="35bb4-151">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-152">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-152">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-153">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="35bb4-153">.NET Framework 4.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="35bb4-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="35bb4-154">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-155">표준 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="35bb4-155">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-156">없음</span><span class="sxs-lookup"><span data-stu-id="35bb4-156">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-157">64비트</span><span class="sxs-lookup"><span data-stu-id="35bb4-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-158">Windows PowerShell 3.0 이상</span><span class="sxs-lookup"><span data-stu-id="35bb4-158">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="35bb4-159">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="35bb4-159">.NET Framework 4.5</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35bb4-160">**참고:** Windows 10, 버전 1607, UE-V를 사용 하는 경우 [엔터프라이즈 용 windows 10](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) 에 포함 되어 있으며 더 이상 Microsoft 데스크톱 최적화 팩의 일부가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-160">**Note:** Starting with Windows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack</span></span>

<span data-ttu-id="35bb4-161">또한</span><span class="sxs-lookup"><span data-stu-id="35bb4-161">Also…</span></span>

-   <span data-ttu-id="35bb4-162">**MDOP 라이선스:** 이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-162">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="35bb4-163">엔터프라이즈 고객은 Microsoft 소프트웨어 보증을 통해 MDOP를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-163">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="35bb4-164">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 MDOP를 가져오는 방법 (을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="35bb4-164">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="35bb4-165">설치할 컴퓨터에 대 한 **관리 자격 증명**</span><span class="sxs-lookup"><span data-stu-id="35bb4-165">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

## <a href="" id="step2"></a><span data-ttu-id="35bb4-166">2 단계: UE-V 2에 대 한 설정 저장소 위치 배포</span><span class="sxs-lookup"><span data-stu-id="35bb4-166">Step 2: Deploy the Settings Storage Location for UE-V 2</span></span>


<span data-ttu-id="35bb4-167">사용자 설정이 설정 패키지 파일에 저장 된 표준 네트워크 공유 인 설정 저장소 위치를 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-167">You’ll need to deploy a settings storage location, a standard network share where user settings are stored in a settings package file.</span></span> <span data-ttu-id="35bb4-168">설정 저장소 공유를 만들 때는이를 필요로 하는 사용자에 대 한 액세스를 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-168">When you create the settings storage share, you should limit access to users that require it.</span></span> <span data-ttu-id="35bb4-169">[설정 저장소 위치 배포](https://technet.microsoft.com/library/dn458891.aspx#ssl) 더 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-169">[Deploy a Settings Storage Location](https://technet.microsoft.com/library/dn458891.aspx#ssl) provides more detailed information.</span></span>

**<span data-ttu-id="35bb4-170">네트워크 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="35bb4-170">Create a network share</span></span>**

1.  <span data-ttu-id="35bb4-171">새 보안 그룹을 만들고 UE-V 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-171">Create a new security group and add UE-V users to it.</span></span>

2.  <span data-ttu-id="35bb4-172">UE-V 설정 패키지를 저장 하는 중앙 컴퓨터에서 새 폴더를 만든 다음이 폴더에 대 한 그룹 사용 권한을 사용 하 여 UE-V 사용자에 게 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-172">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="35bb4-173">UE-V를 지 원하는 관리자는이 공유 폴더에 대 한 사용 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-173">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="35bb4-174">연결할 때 디렉터리를 만들 수 있는 권한을 UE-V users 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-174">Assign UE-V users permission to create a directory when they connect.</span></span> <span data-ttu-id="35bb4-175">해당 디렉터리의 모든 하위 디렉터리에 대해 모든 권한을 부여 하 되, 위의 항목에 대 한 액세스를 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-175">Grant full permission to all subdirectories of that directory, but block access to anything above.</span></span>

    1.  <span data-ttu-id="35bb4-176">설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준 서버 메시지 블록) 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-176">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="35bb4-177">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="35bb4-177">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="35bb4-178">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="35bb4-178">Recommended permissions</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="35bb4-179">모두</span><span class="sxs-lookup"><span data-stu-id="35bb4-179">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="35bb4-180">권한 없음</span><span class="sxs-lookup"><span data-stu-id="35bb4-180">No permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="35bb4-181">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="35bb4-181">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="35bb4-182">모든 권한</span><span class="sxs-lookup"><span data-stu-id="35bb4-182">Full control</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

    2.  <span data-ttu-id="35bb4-183">설정 저장소 위치 폴더에 대해 다음 NTFS 파일 시스템 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-183">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong><span data-ttu-id="35bb4-184">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="35bb4-184">User account</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="35bb4-185">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="35bb4-185">Recommended permissions</span></span></strong></th>
        <th align="left"><strong><span data-ttu-id="35bb4-186">Folder</span><span class="sxs-lookup"><span data-stu-id="35bb4-186">Folder</span></span></strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="35bb4-187">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="35bb4-187">Creator/owner</span></span></p></td>
        <td align="left"><p><span data-ttu-id="35bb4-188">모든 권한</span><span class="sxs-lookup"><span data-stu-id="35bb4-188">Full control</span></span></p></td>
        <td align="left"><p><span data-ttu-id="35bb4-189">하위 폴더 및 파일만</span><span class="sxs-lookup"><span data-stu-id="35bb4-189">Subfolders and files only</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="35bb4-190">UE-V 사용자의 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="35bb4-190">Security group of UE-V users</span></span></p></td>
        <td align="left"><p><span data-ttu-id="35bb4-191">폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</span><span class="sxs-lookup"><span data-stu-id="35bb4-191">List folder/read data, create folders/append data</span></span></p></td>
        <td align="left"><p><span data-ttu-id="35bb4-192">이 폴더만</span><span class="sxs-lookup"><span data-stu-id="35bb4-192">This folder only</span></span></p></td>
        </tr>
        </tbody>
        </table>

         

**<span data-ttu-id="35bb4-193">보안 참고:</span><span class="sxs-lookup"><span data-stu-id="35bb4-193">Security Note:</span></span>**

<span data-ttu-id="35bb4-194">Windows Server 운영 체제를 실행 하는 컴퓨터에서 설정 저장소 공유를 만드는 경우 UE-V를 구성 하 여 로컬 관리자 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-194">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="35bb4-195">이 추가 보안을 사용 하도록 설정 하려면 Windows Server 레지스트리 편집기에서 다음 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-195">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="35bb4-196">**"RepositoryOwnerCheckEnabled"** 이라는 **REG \ _DWORD** 레지스트리 키를 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-196">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="35bb4-197">레지스트리 키 값을 *1*로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-197">Set the registry key value to *1*.</span></span>

## <a href="" id="step3"></a><span data-ttu-id="35bb4-198">3 단계: UE-V 2 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="35bb4-198">Step 3: Deploy the UE-V 2 Agent</span></span>


<span data-ttu-id="35bb4-199">UE-V Agent는 사용자 컴퓨터와 장치 간에 응용 프로그램 및 Windows 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-199">The UE-V Agent synchronizes application and Windows settings between users’ computers and devices.</span></span> <span data-ttu-id="35bb4-200">평가를 위해 테스트 환경에서 동일한 사용자에 속하는 적어도 두 대 이상의 컴퓨터에 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-200">For evaluation purposes, install the agent on at least two computers in your test environment that belong to the same user.</span></span>

<span data-ttu-id="35bb4-201">명령줄에서 AgentSetup.exe 파일을 실행 하 여 UE-V 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-201">Run the AgentSetup.exe file from the command line to install the UE-V Agent.</span></span> <span data-ttu-id="35bb4-202">32 비트 및 64 비트 운영 체제 모두에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-202">It installs on both 32-bit and 64-bit operating systems.</span></span>

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

<span data-ttu-id="35bb4-203">SettingsStoragePath 명령줄 매개 변수를 2 단계의 네트워크 공유로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-203">You must specify the SettingsStoragePath command line parameter as the network share from Step 2.</span></span> <span data-ttu-id="35bb4-204">[Ue-v Agent 배포는](https://technet.microsoft.com/library/dn458891.aspx#agent) 보다 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-204">[Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more detailed information.</span></span>

## <a href="" id="step4"></a><span data-ttu-id="35bb4-205">4 단계: UE-V 2 평가판 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="35bb4-205">Step 4: Test Your UE-V 2 Evaluation Deployment</span></span>


<span data-ttu-id="35bb4-206">이제 UE-V 계산 배포에서 몇 가지 테스트를 실행 하 여 UE-V가 작동 하는 방식을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-206">You can now run a few tests on your UE-V evaluation deployment to see how UE-V works.</span></span>

****

1.  <span data-ttu-id="35bb4-207">첫 번째 컴퓨터 (컴퓨터 A)에 다음 중 하나 이상의 변경 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-207">On the first computer (Computer A), make one or more of these changes:</span></span>

    1.  <span data-ttu-id="35bb4-208">Windows 데스크톱으로 열고 작업 표시줄을 창의 다른 위치로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-208">Open to Windows Desktop and move the taskbar to a different location in the window.</span></span>

    2.  <span data-ttu-id="35bb4-209">기본 글꼴을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-209">Change the default fonts.</span></span>

    3.  <span data-ttu-id="35bb4-210">계산기를 열고 **공학용**으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-210">Open Calculator and set to **scientific**.</span></span>

    4.  <span data-ttu-id="35bb4-211">[Windows PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿을 관리 하는 방법](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)에 따라 windows 앱의 동작을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-211">Change the behavior of any Windows app, as detailed in [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    5.  <span data-ttu-id="35bb4-212">Microsoft 계정 설정 동기화 및 로밍 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-212">Disable Microsoft Account settings synchronization and Roaming Profiles.</span></span>

2.  <span data-ttu-id="35bb4-213">컴퓨터 A. 설정은 사용자가 응용 프로그램을 잠그거나 로그 오프 하거나 종료 하거나 동기화 공급자가 실행 될 때 (기본적으로 30 분 마다) UE-V 설정 패키지에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-213">Log off Computer A. Settings are saved in a UE-V settings package when users lock, logoff, exit an application, or when the sync provider runs (every 30 minutes by default).</span></span>

3.  <span data-ttu-id="35bb4-214">두 번째 컴퓨터 (컴퓨터 B)에 컴퓨터 A와 동일한 사용자로 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-214">Log in to the second computer (Computer B) as the same user as Computer A.</span></span>

4.  <span data-ttu-id="35bb4-215">Windows 데스크톱으로 열고 작업 표시줄 위치가 컴퓨터 A와 일치 하는지 확인 합니다. 기본 글꼴이 일치 하 고 계산기가 **공학용**으로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-215">Open to Windows Desktop and verify that the taskbar location matches that of Computer A. Verify that the default fonts match and that Calculator is set to **scientific**.</span></span> <span data-ttu-id="35bb4-216">또한 Windows 앱에 대 한 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-216">Also verify the change you made to any Windows app.</span></span>

<span data-ttu-id="35bb4-217">컴퓨터 B의 설정을 원래 컴퓨터의 설정으로 다시 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-217">You can change the settings in Computer B back to the original Computer A settings.</span></span> <span data-ttu-id="35bb4-218">그런 다음 컴퓨터 B를 로그 오프 하 고 컴퓨터 A에 로그인 하 여 변경 내용을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="35bb4-218">Then log off Computer B and log in to Computer A to verify the changes.</span></span>

## <span data-ttu-id="35bb4-219">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="35bb4-219">Other resources for this product</span></span>


-   [<span data-ttu-id="35bb4-220">Microsoft UE-V (User Experience Virtualization) 2. x</span><span class="sxs-lookup"><span data-stu-id="35bb4-220">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="35bb4-221">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="35bb4-221">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="35bb4-222">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="35bb4-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="35bb4-223">UE-V 2. x 문제 해결</span><span class="sxs-lookup"><span data-stu-id="35bb4-223">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="35bb4-224">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="35bb4-224">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





