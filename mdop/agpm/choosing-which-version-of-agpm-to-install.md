---
title: 설치할 AGPM 버전 선택
description: 설치할 AGPM 버전 선택
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905605"
---
# <span data-ttu-id="03315-103">설치할 AGPM 버전 선택</span><span class="sxs-lookup"><span data-stu-id="03315-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="03315-104">AGPM (MicrosoftAdvanced Group Policy Management)의 각 릴리스는 특정 버전의 Windows 운영 체제를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03315-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="03315-105">같은 시스템의 운영 체제에서 AGPM 클라이언트와 AGPM 서버를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="03315-106">예를 들어 windows Server 2016, windows 8.1 for windows Server2012 R2 등이 포함 되어 있는 Windows 10</span><span class="sxs-lookup"><span data-stu-id="03315-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="03315-107">해당 도메인에 있는 최신 버전의 운영 체제에 AGPM 서버를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="03315-108">AGPM은 Gpo (그룹 정책 개체)를 백업 및 복원 하기 위해 GPMC (그룹 정책 관리 콘솔)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="03315-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="03315-109">최신 버전의 GPMC는 이전 버전에서 사용할 수 없는 추가 정책 설정을 제공 하기 때문에 최신 버전의 운영 체제를 사용 하 여 더 많은 정책 설정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="03315-110">모든 버전의 AGPM은 AGPM이 실행 되는 운영 체제의 버전 또는 이전 버전에서 도입 된 정책 설정만 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="03315-111">예를 들어 Windows Server 2012에 AGPM 4.0 SP2를 설치 하는 경우 Windows Server 2012 또는 이전 버전에서 도입 된 정책 설정을 관리할 수 있지만, Windows 8.1 또는 Windows Server2012 R2에서 나중에 도입 된 정책 설정은 관리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="03315-112">AGPM 서버의 GPMC 버전이 관리자가 그룹 정책을 관리 하는 데 사용 하는 컴퓨터의 버전 보다 오래 된 경우 AGPM 서버는 이전 버전의 GPMC에서 사용할 수 없는 모든 정책 설정을 저장할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03315-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="03315-113">Windows에 포함된 그룹 정책 설정의 스프레드시트에 대해서는 [Windows 및 Windows Server에 대한 그룹 정책 설정 참조](https://go.microsoft.com/fwlink/p/?LinkId=613627)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03315-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="03315-114">AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="03315-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="03315-115">Windows 10을 실행 하는 컴퓨터를 사용 하 여 Gpo를 관리 하는 경우 AGPM 4.0 SP3을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03315-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="03315-116">Windows 10 운영 체제를 실행 하는 컴퓨터에는 이전 버전의 AGPM을 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="03315-117">표 1에는 AGPM 4.0 SP3을 설치할 수 있는 운영 체제와 AGPM 4.0 SP3을 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="03315-118">표 1: AGPM 4.0 SP3에서 지원 되는 운영 체제 및 정책 설정</span><span class="sxs-lookup"><span data-stu-id="03315-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="03315-119">AGPM 서버에서 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="03315-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="03315-120">AGPM 클라이언트에 대해 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="03315-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="03315-121">AGPM 지원</span><span class="sxs-lookup"><span data-stu-id="03315-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-122">Windows Server 2019 또는 Windows 10</span><span class="sxs-lookup"><span data-stu-id="03315-122">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-123">Windows Server 2019 또는 Windows 10</span><span class="sxs-lookup"><span data-stu-id="03315-123">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-124">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-124">Supported</span></span></p></td>
</tr>
 <tr class="even">
<td align="left"><p><span data-ttu-id="03315-125">Windows Server 2019 또는 Windows 10</span><span class="sxs-lookup"><span data-stu-id="03315-125">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-126">Windows Server 2019 또는 Windows 10</span><span class="sxs-lookup"><span data-stu-id="03315-126">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-127">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-127">Supported</span></span></p></td>
</tr>
<tr class="edd">
<td align="left"><p><span data-ttu-id="03315-128">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="03315-128">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-129">Windows 10</span><span class="sxs-lookup"><span data-stu-id="03315-129">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-130">KB 4015786에서 설명한 주의 사항으로 지원 됩니다. <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"></span><span class="sxs-lookup"><span data-stu-id="03315-130">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-131">Windows Server2012 R2 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-131">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-132">Windows Server2012 R2 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-132">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-133">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-133">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-134">Windows Server2012 R2, Windows Server 2012 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-134">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-135">Windows Server 2012 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-135">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-136">지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03315-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-137">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-137">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-138">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-139">지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03315-139">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-140">Windows Server 2012, Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-140">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-141">Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</span><span class="sxs-lookup"><span data-stu-id="03315-141">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-142">지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-142">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-143">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-144">Windows Server 2012, Windows Server2008R2, Windows 8 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-144">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-145">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="03315-145">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-146">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-146">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-147">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-147">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-148">지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-148">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="03315-149">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="03315-149">AGPM4.0 SP2</span></span>


<span data-ttu-id="03315-150">Windows Server2012 R2 또는 Windows 8.1을 실행 하는 컴퓨터를 사용 하 여 Gpo를 관리 하는 경우 AGPM 4.0 SP2를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03315-150">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="03315-151">이러한 운영 체제를 실행 하는 컴퓨터에는 이전 버전의 AGPM을 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-151">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="03315-152">표 1에는 AGPM 4.0 SP2를 설치할 수 있는 운영 체제와 AGPM 4.0 SP2를 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-152">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="03315-153">표 2: AGPM 4.0 SP2에서 지원 되는 운영 체제 및 정책 설정</span><span class="sxs-lookup"><span data-stu-id="03315-153">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="03315-154">AGPM 서버에서 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="03315-154">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="03315-155">AGPM 클라이언트에 대해 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="03315-155">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="03315-156">AGPM 지원</span><span class="sxs-lookup"><span data-stu-id="03315-156">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-157">Windows Server2012 R2 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-157">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-158">Windows Server2012 R2 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-158">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-159">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-159">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-160">Windows Server2012 R2, Windows Server 2012 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-160">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-161">Windows Server 2012 또는 Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="03315-161">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-162">지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03315-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-163">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-163">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-164">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-164">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-165">지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03315-165">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-166">Windows Server 2012, Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-166">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-167">Windows Server2008 또는 WindowsVista SP1(서비스 팩 1)</span><span class="sxs-lookup"><span data-stu-id="03315-167">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-168">지원 되지만 Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-168">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-169">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-170">Windows Server 2012, Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-170">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-171">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="03315-171">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-172">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-172">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-173">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-173">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-174">지원 됨 (Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 또는 Windows7에만 있는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-174">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="03315-175">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="03315-175">AGPM4.0 SP1</span></span>


<span data-ttu-id="03315-176">표 2에는 AGPM 4.0 SP1을 설치할 수 있는 운영 체제와 AGPM 4.0 SP1을 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-176">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="03315-177">표 3: AGPM 4.0 SP1에서 지원 되는 운영 체제 및 정책 설정</span><span class="sxs-lookup"><span data-stu-id="03315-177">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="03315-178">AGPM 서버에서 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="03315-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="03315-179">AGPM 클라이언트에 대해 지원 되는 구성</span><span class="sxs-lookup"><span data-stu-id="03315-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="03315-180">AGPM 지원</span><span class="sxs-lookup"><span data-stu-id="03315-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03315-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03315-182">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-183">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-184">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-184">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-185">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-185">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-186">지원 되지만 Windows 8.1에만 있는 정책 설정 또는 기본 설정 항목은 편집할 수 없음</span><span class="sxs-lookup"><span data-stu-id="03315-186">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-187">Windows Server 2012, Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-187">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-188">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-189">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-189">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-190">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-191">Windows Server 2012, Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-191">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-192">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-192">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-193">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-194">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-194">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-195">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-195">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="03315-196">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="03315-196">AGPM4.0</span></span>


<span data-ttu-id="03315-197">표 3에 AGPM 4.0을 설치할 수 있는 운영 체제와 AGPM 4.0을 사용 하 여 관리할 수 있는 정책 설정이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-197">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="03315-198">표 4: AGPM 4.0에서 지원 되는 운영 체제 및 정책 설정</span><span class="sxs-lookup"><span data-stu-id="03315-198">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="03315-199">AGPM 서버용으로 지원 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="03315-199">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="03315-200">AGPM 클라이언트용으로 지원 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="03315-200">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="03315-201">AGPM 지원</span><span class="sxs-lookup"><span data-stu-id="03315-201">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-202">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-203">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-203">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-204">지원함</span><span class="sxs-lookup"><span data-stu-id="03315-204">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-205">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-205">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-206">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-206">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-207">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-207">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-208">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-209">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="03315-209">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-210">지원되지 않음</span><span class="sxs-lookup"><span data-stu-id="03315-210">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-211">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-211">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-212">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-212">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-213">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-213">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="03315-214">AGPM 4.0 이전의 AGPM 버전</span><span class="sxs-lookup"><span data-stu-id="03315-214">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="03315-215">표 4에는 AGPM 4.0 이전의 AGPM 버전을 설치할 수 있는 운영 체제 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-215">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="03315-216">운영 체제가 나열 되지 않으면 해당 운영 체제에 AGPM을 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="03315-216">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="03315-217">표 5: AGPM 4.0 이전의 AGPM 버전에 대해 지원 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="03315-217">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="03315-218">운영 체제</span><span class="sxs-lookup"><span data-stu-id="03315-218">Operating system</span></span></th>
<th align="left"><span data-ttu-id="03315-219">설치할 수 있는 AGPM 버전</span><span class="sxs-lookup"><span data-stu-id="03315-219">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-220">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="03315-220">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-221">3.0</span><span class="sxs-lookup"><span data-stu-id="03315-221">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-222">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="03315-222">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-223">3.0</span><span class="sxs-lookup"><span data-stu-id="03315-223">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="03315-224">서비스 팩이 설치 되지 않은 WindowsVista (32 비트)</span><span class="sxs-lookup"><span data-stu-id="03315-224">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-225">2.5</span><span class="sxs-lookup"><span data-stu-id="03315-225">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="03315-226">Windows Server2003 (32 비트)</span><span class="sxs-lookup"><span data-stu-id="03315-226">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="03315-227">2.5</span><span class="sxs-lookup"><span data-stu-id="03315-227">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="03315-228">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="03315-228">How to Get MDOP Technologies</span></span>


<span data-ttu-id="03315-229">AGPM 4.0 SP2는 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="03315-229">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="03315-230">MDOP는 Microsoft 소프트웨어 보장의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="03315-230">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="03315-231">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="03315-231">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="03315-232">관련 항목</span><span class="sxs-lookup"><span data-stu-id="03315-232">Related topics</span></span>


[<span data-ttu-id="03315-233">고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="03315-233">Advanced Group Policy Management</span></span>](index.md)

 

 





