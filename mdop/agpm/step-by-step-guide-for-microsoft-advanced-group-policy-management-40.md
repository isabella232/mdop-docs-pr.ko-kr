---
title: Microsoft 고급 그룹 정책 관리 4.0 단계별 가이드
description: Microsoft 고급 그룹 정책 관리 4.0 단계별 가이드
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820198"
---
# <span data-ttu-id="b1363-103">Microsoft 고급 그룹 정책 관리 4.0 단계별 가이드</span><span class="sxs-lookup"><span data-stu-id="b1363-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="b1363-104">이 단계별 안내서는 GPMC (그룹 정책 관리 콘솔) 및 AGPM (고급 그룹 정책 관리)을 사용 하는 그룹 정책 관리에 대 한 고급 기술을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="b1363-105">AGPM은 다음을 제공 하는 GPMC의 기능을 향상 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="b1363-106">프로덕션 환경에서 Gpo에 대 한 액세스를 위임 하는 기능 외에도 Gpo (그룹 정책 개체)를 여러 그룹 정책 관리자에 게 관리 하는 데 사용 권한을 위임 하는 표준 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="b1363-107">Gpo를 프로덕션 환경에 배포 하기 전에 그룹 정책 관리자가 오프 라인으로 Gpo를 만들고 수정할 수 있는 보관 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="b1363-108">보관 파일에서 이전 버전의 GPO로 롤백할 수 있고 보관 저장소에 저장 된 버전 수를 제한 하는 기능.</span><span class="sxs-lookup"><span data-stu-id="b1363-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="b1363-109">Gpo에 대 한 체크 인 및 체크 아웃 기능을 통해 그룹 정책 관리자가 실수로 서로의 작업을 덮어쓰지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="b1363-110">특정 특성을 가진 Gpo를 검색 하 고 표시 되는 Gpo 목록을 필터링 하는 기능</span><span class="sxs-lookup"><span data-stu-id="b1363-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="b1363-111">AGPM 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="b1363-111">AGPM scenario overview</span></span>


<span data-ttu-id="b1363-112">이 시나리오에서는 각 역할에 대해 별도의 사용자 계정을 사용 하 여 다양 한 수준의 권한을 가진 여러 그룹 정책 관리자가 있는 환경에서 그룹 정책을 관리 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="b1363-113">구체적으로 다음과 같은 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="b1363-114">Domain Admins 그룹의 구성원 인 계정을 사용 하 여 AGPM 서버를 설치 하 고 AGPM 관리자 역할을 계정이 나 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="b1363-115">AGPM 역할을 할당 하는 계정을 사용 하 여 AGPM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="b1363-116">AGPM 관리자 역할이 있는 계정을 사용 하 여 다른 계정에 역할을 할당 하 여 AGPM을 구성 하 고 Gpo에 대 한 액세스 권한을 대리인에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="b1363-117">편집자 역할이 있는 계정에서 승인자 역할이 있는 계정을 사용 하 여 승인 하는 새 GPO를 만들도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="b1363-118">편집기 계정을 사용 하 여 보관 함에서 GPO를 확인 하 고, GPO를 편집 하 고, GPO를 보관 함으로 확인 한 다음 배포를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="b1363-119">승인자 역할이 있는 계정을 사용 하 여 GPO를 검토 하 고 프로덕션 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="b1363-120">편집자 역할이 있는 계정을 사용 하 여 GPO 서식 파일을 만들고이를 시작 점으로 사용 하 여 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="b1363-121">승인자 역할이 있는 계정을 사용 하 여 GPO를 삭제 하 고 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![그룹 정책 개체 개발 프로세스](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="b1363-123">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b1363-123">Requirements</span></span>


<span data-ttu-id="b1363-124">AGPM을 설치 하려는 컴퓨터는 다음 요구 사항을 충족 해야 하며이 시나리오에서 사용할 계정을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="b1363-125">**참고**  AGPM 2.5을 설치 하 고 Windows Server® 2003에서 Windows Server2008로 업그레이드 하거나 서비스 팩이 설치 되지 않은 WindowsVista에서 Windows7 또는 WindowsVista® SP1(서비스 Pack1)로 업그레이드 하는 경우에는 운영 체제를 업그레이드 해야만 AGPM 4.0으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="b1363-126">AGPM 3.0이 설치 되어 있는 경우 AGPM 4.0으로 업그레이드 하기 전에 운영 체제를 업그레이드할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="b1363-127">최신 및 이전 운영 체제를 모두 포함 하는 혼합 환경에서는 다음 표에 표시 된 것 처럼 기능에 몇 가지 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1363-128">AGPM 서버 4.0이 실행 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="b1363-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="b1363-129">AGPM 클라이언트 4.0이 실행 되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="b1363-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="b1363-130">AGPM 4.0 지원 상태</span><span class="sxs-lookup"><span data-stu-id="b1363-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1363-131">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="b1363-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-132">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="b1363-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-133">지원함</span><span class="sxs-lookup"><span data-stu-id="b1363-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1363-134">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="b1363-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-135">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="b1363-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-136">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목은 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1363-137">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="b1363-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-138">Windows Server2008R2 또는 Windows7</span><span class="sxs-lookup"><span data-stu-id="b1363-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-139">지원 안 됨</span><span class="sxs-lookup"><span data-stu-id="b1363-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1363-140">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="b1363-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-141">Windows Server2008 또는 Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="b1363-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1363-142">지원 되지만, Windows Server2008R2 또는 Windows7에만 존재 하는 정책 설정 또는 기본 설정 항목을 보고 하거나 편집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b1363-143">AGPM 서버 요구 사항</span><span class="sxs-lookup"><span data-stu-id="b1363-143">AGPM Server requirements</span></span>

<span data-ttu-id="b1363-144">AGPM Server 4.0에는 Windows Server2008R2, Windows Server2008, Windows7 및 GPMC (원격 서버 관리 도구) (RSAT) 또는 Windows Vista SP1 및 office RSAT의 GPMC가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="b1363-145">32 비트와 64 비트 버전이 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="b1363-146">AGPM Server를 설치 하기 전에 먼저 도메인 관리자 그룹의 구성원 이어야 하 고 다른 언급이 없는 한 다음 Windows 기능이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="b1363-147">GPMC</span><span class="sxs-lookup"><span data-stu-id="b1363-147">GPMC</span></span>

    -   <span data-ttu-id="b1363-148">Windows Server2008R2 또는 Windows Server2008: GPMC가 없는 경우에는 AGPM에 의해 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="b1363-149">Windows7: AGPM을 설치 하기 전에 RSAT에서 GPMC를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="b1363-150">자세한 내용은 [Windows 7 용 원격 서버 관리 도구](https://go.microsoft.com/fwlink/?LinkID=131280) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="b1363-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="b1363-151">Windows Vista SP1: AGPM을 설치 하기 전에 RSAT에서 GPMC를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="b1363-152">자세한 내용은 [Windows Vista 용 원격 서버 관리 도구 (서비스 팩 1](https://go.microsoft.com/fwlink/?LinkID=116179) ) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="b1363-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="b1363-153">.NET Framework 3.5 이상 버전</span><span class="sxs-lookup"><span data-stu-id="b1363-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="b1363-154">Windows Server2008R2 또는 Windows7: .NET Framework 3.5 이상 버전이 없으면 AGPM에서 자동으로 .NET Framework 3.5을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="b1363-155">Windows Server2008 또는 Windows Vista SP1: AGPM을 설치 하기 전에 .NET Framework 3.5 또는 최신 버전을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="b1363-156">다음 Windows 기능은 AGPM 서버에 필요 하며 없는 경우 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="b1363-157">WCF 활성화, 비 HTTP 활성화</span><span class="sxs-lookup"><span data-stu-id="b1363-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="b1363-158">Windows Process Activation Service</span><span class="sxs-lookup"><span data-stu-id="b1363-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="b1363-159">프로세스 모델</span><span class="sxs-lookup"><span data-stu-id="b1363-159">Process Model</span></span>

    -   <span data-ttu-id="b1363-160">.NET 환경</span><span class="sxs-lookup"><span data-stu-id="b1363-160">The .NET Environment</span></span>

    -   <span data-ttu-id="b1363-161">구성 Api</span><span class="sxs-lookup"><span data-stu-id="b1363-161">Configuration APIs</span></span>

### <span data-ttu-id="b1363-162">AGPM 클라이언트 요구 사항</span><span class="sxs-lookup"><span data-stu-id="b1363-162">AGPM Client requirements</span></span>

<span data-ttu-id="b1363-163">AGPM 클라이언트 4.0에는 Windows Server2008R2, Windows Server2008, Windows7, RSAT의 GPMC 또는 Windows Vista SP1 및 RSAT의 GPMC가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="b1363-164">32 비트와 64 비트 버전이 모두 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="b1363-165">Agpm 클라이언트는 AGPM 서버를 실행 하는 컴퓨터에 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="b1363-166">다음과 같은 Windows 기능은 AGPM 클라이언트에 필요 하며, 별도로 명시 되지 않은 경우 자동으로 설치 되지 않는 한 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="b1363-167">GPMC</span><span class="sxs-lookup"><span data-stu-id="b1363-167">GPMC</span></span>

    -   <span data-ttu-id="b1363-168">Windows Server2008R2 또는 Windows Server2008: GPMC가 없는 경우에는 AGPM에 의해 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="b1363-169">Windows7: AGPM을 설치 하기 전에 RSAT에서 GPMC를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="b1363-170">자세한 내용은 [Windows 7 용 원격 서버 관리 도구](https://go.microsoft.com/fwlink/?LinkID=131280) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="b1363-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="b1363-171">Windows Vista SP1: AGPM을 설치 하기 전에 RSAT에서 GPMC를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="b1363-172">자세한 내용은 [Windows Vista 용 원격 서버 관리 도구 (서비스 팩 1](https://go.microsoft.com/fwlink/?LinkID=116179) ) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="b1363-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="b1363-173">.NET Framework 3.0 이상 버전</span><span class="sxs-lookup"><span data-stu-id="b1363-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="b1363-174">Windows Server2008R2 또는 Windows7: .NET Framework 3.0 이상 버전이 없으면 AGPM에서 자동으로 .NET Framework 3.5을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="b1363-175">Windows Server2008 또는 Windows Vista SP1: .NET Framework 3.0 이상 버전이 없는 경우 .NET Framework 3.0는 AGPM에 의해 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="b1363-176">시나리오 요구 사항</span><span class="sxs-lookup"><span data-stu-id="b1363-176">Scenario requirements</span></span>

<span data-ttu-id="b1363-177">이 시나리오를 시작 하기 전에 4 개의 사용자 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="b1363-178">시나리오를 진행 하는 동안 다음 AGPM 역할 중 하나를 각 계정 (예: AGPM 관리자 (모든 권한), 승인자, 편집자, 검토자)에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="b1363-179">이러한 계정은 전자 메일 메시지를 보내고 받을 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="b1363-180">AGPM 관리자, 승인자 및 (선택적) 편집기 역할이 있는 계정에 대 한 **링크 gpo** 할당 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="b1363-181">**참고** 
 **Gpo 링크** 권한은 기본적으로 도메인 관리자와 엔터프라이즈 관리자의 구성원에 게 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="b1363-182">추가 사용자 또는 그룹 (예: AGPM 관리자 또는 승인자 역할을 가진 계정)에 대 한 **Gpo 링크** 사용 권한을 할당 하려면 도메인 노드를 클릭 한 다음 **위임** 탭을 클릭 하 고 **Gpo 연결**을 선택한 다음 **추가**를 클릭 하 고 사용 권한을 할당 하려는 사용자 또는 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="b1363-183">AGPM 설치 및 구성 단계</span><span class="sxs-lookup"><span data-stu-id="b1363-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="b1363-184">AGPM을 설치 하 고 구성 하려면 다음 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="b1363-185">1 단계: AGPM 서버 설치</span><span class="sxs-lookup"><span data-stu-id="b1363-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="b1363-186">2 단계: AGPM 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="b1363-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="b1363-187">3 단계: AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="b1363-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="b1363-188">4 단계: 전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="b1363-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="b1363-189">5 단계: 대리인 액세스</span><span class="sxs-lookup"><span data-stu-id="b1363-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="b1363-190">1 단계: AGPM 서버 설치</span><span class="sxs-lookup"><span data-stu-id="b1363-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="b1363-191">이 단계에서는 AGPM 서비스를 실행할 구성원 서버나 도메인 컨트롤러에 AGPM Server를 설치 하 고 보관 파일을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="b1363-192">모든 AGPM 작업은이 Windows 서비스를 통해 관리 되며 서비스의 자격 증명을 사용 하 여 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="b1363-193">AGPM 서버에서 관리 하는 보관 파일은 해당 서버나 같은 포리스트의 다른 서버에서 호스팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="b1363-194">AGPM 서비스를 호스트 하는 컴퓨터에 AGPM Server를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="b1363-195">Domain Admins 그룹의 구성원 인 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="b1363-196">Microsoft 데스크톱 최적화 팩 CD를 시작 하 고 화면의 지침에 따라 **고급 그룹 정책 관리-서버**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="b1363-197">**시작** 대화 상자에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="b1363-198">**Microsoft 소프트웨어 사용 조건** 대화 상자에서 약관에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="b1363-199">**응용 프로그램 경로** 대화 상자에서 AGPM 서버를 설치할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="b1363-200">AGPM 서버를 설치 하는 컴퓨터는 AGPM 서비스를 호스팅하고 보관 파일을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="b1363-201">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-201">Click **Next**.</span></span>

6.  <span data-ttu-id="b1363-202">**보관 경로** 대화 상자에서 AGPM 서버와 관련 하 여 보관 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="b1363-203">보관 경로는 AGPM 서버 또는 다른 위치에 있는 폴더를 가리킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="b1363-204">그러나이 AGPM 서버에서 관리 하는 모든 Gpo 및 기록 데이터를 저장 하는 데 충분 한 공간이 있는 위치를 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="b1363-205">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-205">Click **Next**.</span></span>

7.  <span data-ttu-id="b1363-206">Agpm 서비스 **계정** 대화 상자에서 agpm 서비스가 실행 될 서비스 계정을 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="b1363-207">이 계정은 Domain Admins 그룹의 구성원 이거나 최소 권한 구성의 경우 AGPM 서버에서 관리 하는 각 도메인의 다음 그룹에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="b1363-208">그룹 정책 작성자 겸 소유자</span><span class="sxs-lookup"><span data-stu-id="b1363-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="b1363-209">백업 연산자</span><span class="sxs-lookup"><span data-stu-id="b1363-209">Backup Operators</span></span>

    <span data-ttu-id="b1363-210">또한이 계정에는 다음 폴더에 대 한 모든 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="b1363-211">이 권한은 로컬 드라이브에 설치 되어 있는 경우 AGPM 서버를 설치 하는 동안 자동으로 부여 되는 AGPM 보관 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="b1363-212">로컬 시스템 임시 폴더 (일반적 으로%windir%\\temp.</span><span class="sxs-lookup"><span data-stu-id="b1363-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="b1363-213">**보관 소유자** 대화 상자에서 AGPM 관리자 (모든 권한) 역할을 할당 하는 계정이 나 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="b1363-214">AGPM 관리자는 다른 그룹 정책 관리자에 게 AGPM 역할 및 사용 권한을 할당할 수 있으므로 나중에 추가 그룹 정책 관리자에 게 AGPM 관리자의 역할을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="b1363-215">이 시나리오에서는 AGPM 관리자 역할에서 사용할 계정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="b1363-216">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-216">Click **Next**.</span></span>

9.  <span data-ttu-id="b1363-217">**포트 구성** 대화 상자에서 AGPM 서비스가 수신 대기할 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="b1363-218">포트 예외를 수동으로 구성 하거나 포트 예외를 구성 하는 규칙을 사용 하지 않는 한 **방화벽에 포트 예외 추가** 확인란의 선택을 취소 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="b1363-219">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-219">Click **Next**.</span></span>

10. <span data-ttu-id="b1363-220">**언어** 대화 상자에서 AGPM 서버용으로 설치할 표시 언어를 하나 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="b1363-221">**설치**를 클릭 한 다음 **마침을** 클릭 하 여 설정 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="b1363-222">**주의**  사항 운영 체제의 **관리 도구** 및 **서비스** 를 통해 AGPM 서비스에 대 한 설정을 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="b1363-223">이렇게 하면 AGPM 서비스가 시작 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="b1363-224">서비스에 대 한 설정을 변경 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="b1363-225">2 단계: AGPM 클라이언트 설치</span><span class="sxs-lookup"><span data-stu-id="b1363-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="b1363-226">Gpo를 만들고, 편집 하 고, 배포 하 고, 검토 하거나, 삭제 하는 모든 그룹 정책 관리자는 Gpo를 관리 하는 데 사용 하는 컴퓨터에 AGPM 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="b1363-227">여러 GPO 관리 작업을 수행 하는 데 사용 하는 변경 컨트롤 노드는 AGPM 클라이언트를 설치 하는 경우에만 그룹 정책 관리 콘솔에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="b1363-228">이 시나리오에서는 하나 이상의 컴퓨터에 AGPM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="b1363-229">그룹 정책 관리를 수행 하지 않는 최종 사용자의 컴퓨터에 AGPM 클라이언트를 설치할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="b1363-230">그룹 정책 관리자의 컴퓨터에 AGPM 클라이언트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="b1363-231">Microsoft 데스크톱 최적화 팩 CD를 시작 하 고 화면의 지침에 따라 **고급 그룹 정책 관리-클라이언트**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="b1363-232">**시작** 대화 상자에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="b1363-233">**Microsoft 소프트웨어 사용 조건** 대화 상자에서 약관에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="b1363-234">**응용 프로그램 경로** 대화 상자에서 AGPM 클라이언트를 설치할 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="b1363-235">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-235">Click **Next**.</span></span>

5.  <span data-ttu-id="b1363-236">**Agpm 서버** 대화 상자에서 DNS 이름 또는 만들려는 AGPM 서버의 IP 주소와 연결할 포트를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="b1363-237">AGPM 서비스의 기본 포트는 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="b1363-238">포트 예외를 수동으로 구성 하거나 규칙을 사용 하 여 포트 예외를 구성 하지 않는 한 **방화벽을 통해 Microsoft 관리 콘솔 허용** 확인란을 선택 취소 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="b1363-239">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-239">Click **Next**.</span></span>

6.  <span data-ttu-id="b1363-240">**언어** 대화 상자에서 AGPM 클라이언트에 대해 설치할 표시 언어를 하나 이상 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="b1363-241">**설치**를 클릭 한 다음 **마침을** 클릭 하 여 설정 마법사를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="b1363-242">3 단계: AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="b1363-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="b1363-243">AGPM은 관리 되는 각 gpo (그룹 정책 개체)의 모든 버전, 즉 AGPM이 변경 제어권을 제공 하는 각 GPO를 중앙 보관 저장소에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="b1363-244">이렇게 하면 그룹 정책 관리자가 각 GPO의 배포 된 버전에 즉시 영향을 주지 않고 Gpo를 오프 라인으로 보고 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="b1363-245">이 단계에서는 AGPM 서버 연결을 구성 하 고 모든 그룹 정책 관리자가 동일한 AGPM 서버에 연결 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="b1363-246">(여러 AGPM 서버를 구성 하는 방법에 대 한 자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="b1363-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="b1363-247">모든 그룹 정책 관리자에 대해 AGPM 서버 연결을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="b1363-248">AGPM 클라이언트를 설치한 컴퓨터에서 보관 소유자로 선택한 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="b1363-249">이 사용자는 AGPM 관리자의 역할을 합니다 (모든 권한).</span><span class="sxs-lookup"><span data-stu-id="b1363-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="b1363-250">**시작**을 클릭 하 고 **관리 도구**를 가리킨 다음 **그룹 정책 관리** 를 클릭 하 여 GPMC를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="b1363-251">모든 그룹 정책 관리자에 게 적용 되는 GPO를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="b1363-252">**그룹 정책 관리 편집기** 창에서 **사용자 구성**, **정책**, **관리 템플릿**, **Windows 구성 요소**및 **AGPM**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="b1363-253">세부 정보 창에서 **agpm: 기본 Agpm 서버 (모든 도메인) 지정**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="b1363-254">**속성** 창에서 **사용** 을 선택 하 고 보관을 호스트 하는 서버에 대 한 DNS 이름 또는 IP 주소와 포트 (예: **server.contoso.com:4600**)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="b1363-255">기본적으로 AGPM 서비스는 포트 4600를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="b1363-256">**확인**을 클릭 한 다음 **그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="b1363-257">그룹 정책이 업데이트 되 면 각 그룹 정책 관리자에 대해 AGPM 서버 연결이 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="b1363-258">4 단계: 전자 메일 알림 구성</span><span class="sxs-lookup"><span data-stu-id="b1363-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="b1363-259">AGPM 관리자 (모든 권한)는, 요청이 포함 된 전자 메일 메시지가 있는 승인자와 AGPM 관리자의 전자 메일 주소를 지정 하 고, 편집자는 GPO를 만들거나, 배포 하거나, 삭제 하려고 할 때 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="b1363-260">또한 이러한 메시지가 보내지는 별칭을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="b1363-261">AGPM에 대 한 전자 메일 알림을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="b1363-262">**그룹 정책 관리 편집기** 에서 **변경 제어** 폴더로 이동</span><span class="sxs-lookup"><span data-stu-id="b1363-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="b1363-263">세부 정보 창에서 **도메인 위임** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="b1363-264">보낸 사람 **전자 메일 주소** 필드에 알림을 보낼 AGPM의 전자 메일 별칭을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="b1363-265">**대상 전자 메일 주소** 필드에 승인자 역할을 할당할 사용자 계정의 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="b1363-266">**Smtp 서버** 필드에 유효한 SMTP 메일 서버를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="b1363-267">**사용자 이름** 및 **암호** 필드에 SMTP 서비스에 대 한 액세스 권한이 있는 사용자의 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="b1363-268">**적용**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="b1363-269">5 단계: 대리인 액세스</span><span class="sxs-lookup"><span data-stu-id="b1363-269">Step 5: Delegate access</span></span>

<span data-ttu-id="b1363-270">AGPM 관리자 (모든 권한)로 Gpo에 대 한 도메인 수준의 액세스를 위임 하 고 각 그룹 정책 관리자의 계정에 역할을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="b1363-271">**참고**  도메인 수준이 아닌 GPO 수준에서 액세스를 위임할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="b1363-272">자세한 내용은 고급 그룹 정책 관리에 대 한 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="b1363-273">**중요**  Gpo에 대 한 액세스의 AGPM 관리를 우회 하는 데 사용할 수 없도록 그룹 정책 작성자 겸 소유자 그룹의 구성원을 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="b1363-274">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="b1363-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="b1363-275">도메인 전체의 모든 Gpo에 대 한 액세스 권한을 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="b1363-276">**도메인 위임** 탭에서 **추가** 단추를 클릭 하 고 승인자 역할을 할 그룹 정책 관리자의 사용자 계정을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="b1363-277">**그룹 또는 사용자 추가** 대화 상자에서 **승인자** 역할을 선택 하 여 해당 역할을 계정에 할당 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="b1363-278">(이 역할에는 검토자 역할이 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="b1363-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="b1363-279">**추가** 단추를 클릭 하 고, 편집자 역할을 할 그룹 정책 관리자의 사용자 계정을 선택한 다음, **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="b1363-280">**그룹 또는 사용자 추가** 대화 상자에서 **편집기** 역할을 선택 하 여 해당 역할을 계정에 할당 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="b1363-281">(이 역할에는 검토자 역할이 포함 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="b1363-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="b1363-282">**추가** 단추를 클릭 하 고 검토자 역할을 할 그룹 정책 관리자의 사용자 계정을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="b1363-283">**그룹 또는 사용자 추가** 대화 상자에서 **검토자** 역할을 선택 하 여 해당 역할만 계정에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="b1363-284">Gpo 관리 단계</span><span class="sxs-lookup"><span data-stu-id="b1363-284">Steps for managing GPOs</span></span>


<span data-ttu-id="b1363-285">AGPM을 사용 하 여 Gpo를 만들고, 편집 하 고, 검토 하 고, 배포 하려면 다음 단계를 완료 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="b1363-286">또한 템플릿을 만들고, GPO를 삭제 하 고, 삭제 된 GPO를 복원 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="b1363-287">1 단계: GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="b1363-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="b1363-288">2 단계: GPO 편집</span><span class="sxs-lookup"><span data-stu-id="b1363-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="b1363-289">3 단계: GPO 검토 및 배포</span><span class="sxs-lookup"><span data-stu-id="b1363-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="b1363-290">4 단계: 서식 파일을 사용 하 여 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="b1363-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="b1363-291">5 단계: GPO 삭제 및 복원</span><span class="sxs-lookup"><span data-stu-id="b1363-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="b1363-292">1 단계: GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="b1363-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="b1363-293">여러 그룹 정책 관리자가 있는 환경에서는 편집기 역할을 사용 하 여 새 Gpo를 만들도록 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="b1363-294">그러나 승인자 역할의 사용자는 해당 요청을 승인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="b1363-295">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 새 GPO 생성을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="b1363-296">승인자 역할이 있는 계정을 사용 하 여이 요청을 승인 하 고 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="b1363-297">AGPM을 통해 새 GPO를 만들고 관리 하도록 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="b1363-298">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="b1363-299">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b1363-300">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="b1363-301">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="b1363-302">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="b1363-303">**Mygpo** 를 새 GPO의 이름으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="b1363-304">새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="b1363-305">새 GPO가 승인 즉시 프로덕션 환경에 배포 되도록 **라이브 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="b1363-306">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="b1363-307">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-308">**보류** 탭에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="b1363-309">보류 중인 요청을 승인 하 여 GPO를 만드시겠습니까?</span><span class="sxs-lookup"><span data-stu-id="b1363-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="b1363-310">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 승인자 역할을 가진 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="b1363-311">계정에 대 한 전자 메일 받은 편지함을 열고, 편집기의 요청에 맞게 AGPM 별칭 으로부터 전자 메일 메시지를 받았으며 GPO를 만들 수 있는지 확인해 보세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="b1363-312">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="b1363-313">**콘텐츠** 탭에서 **보류 중** 탭을 클릭 하 여 보류 중인 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="b1363-314">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **승인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="b1363-315">**예** 를 클릭 하 여 승인을 확인 하 고 GPO를 **제어** 탭으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="b1363-316">2 단계: GPO 편집</span><span class="sxs-lookup"><span data-stu-id="b1363-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="b1363-317">Gpo를 사용 하 여 컴퓨터 또는 사용자 설정을 구성 하 고이를 여러 컴퓨터 또는 사용자에 게 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="b1363-318">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 보관 파일에서 GPO를 체크 아웃 하 고, GPO를 오프 라인으로 편집 하 고, 편집한 GPO를 보관 함으로 확인 하 고, GPO를 프로덕션 환경에 배포 하도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="b1363-319">이 시나리오에서는 비밀 번호를 8 자 이상으로 요구 하도록 GPO의 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="b1363-320">편집을 위해 아카이브에 대해 GPO를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="b1363-321">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM에서 편집기 역할을 가진 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="b1363-322">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b1363-323">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="b1363-324">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="b1363-325">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="b1363-326">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-327">**제어** 탭에서 GPO의 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="b1363-328">오프 라인으로 GPO를 편집 하 고 최소 암호 길이를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="b1363-329">**제어** 탭에서 **mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **편집** 을 클릭 하 여 **그룹 정책 관리 편집기** 창을 열고 GPO의 오프 라인 복사본을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="b1363-330">이 시나리오에서는 최소 암호 길이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="b1363-331">**컴퓨터 구성**에서 **정책**, **Windows 설정**, **보안 설정**, **계정 정책**, **암호 정책을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="b1363-332">세부 정보 창에서 **최소 암호 길이**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="b1363-333">속성 창에서 **이 정책 설정 정의** 확인란을 선택 하 고 문자 수를 **8**로 설정한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="b1363-334">**그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="b1363-335">GPO를 보관 함으로 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="b1363-336">**제어** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 하 고 **체크**인을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="b1363-337">메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="b1363-338">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-339">**제어** 탭에서 GPO의 상태가 **체크 인**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="b1363-340">프로덕션 환경에 GPO 배포를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="b1363-341">**제어** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="b1363-342">이 계정은 승인자 또는 AGPM 관리자가 아니기 때문에 배포 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="b1363-343">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="b1363-344">GPO 기록에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="b1363-345">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-346">**Mygpo** 가 **보류** 탭의 gpo 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="b1363-347">3 단계: GPO 검토 및 배포</span><span class="sxs-lookup"><span data-stu-id="b1363-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="b1363-348">이 단계에서는 승인자 역할을 수행 하 고, 보고서를 만들고, GPO의 설정에 대 한 설정 및 변경 사항을 분석 하 여 승인 해야 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="b1363-349">GPO를 평가한 후에는 프로덕션 환경에 배포 하 고 GPO를 도메인 또는 OU (조직 구성 단위)에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="b1363-350">GPO는 해당 도메인 또는 OU의 컴퓨터에 대 한 그룹 정책이 새로 고쳐질 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="b1363-351">GPO의 설정을 검토 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="b1363-352">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="b1363-353">다른 모든 역할에 포함 된 검토자 역할을 사용 하는 모든 그룹 정책 관리자는 GPO의 설정을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="b1363-354">계정에 대 한 전자 메일 받은 편지함을 열고, 편집기의 요청과 함께 AGPM 별칭 으로부터 전자 메일 메시지를 받았으며 GPO를 배포 하는 것을 확인해 보세요.</span><span class="sxs-lookup"><span data-stu-id="b1363-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="b1363-355">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="b1363-356">세부 정보 창의 **내용** 탭에서 **보류 중** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="b1363-357">**Mygpo** 를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="b1363-358">최신 버전의 MyGPO에서 설정을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="b1363-359">**기록** 창에서 최신 타임 스탬프가 있는 GPO 버전을 마우스 오른쪽 단추로 클릭 하 고 **설정을**클릭 한 다음 **HTML 보고서** 를 클릭 하 여 gpo 설정 요약을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="b1363-360">웹 브라우저에서 **모두 표시** 를 클릭 하 여 GPO의 모든 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="b1363-361">브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-361">Close the browser.</span></span>

7. <span data-ttu-id="b1363-362">최신 버전의 MyGPO를 보관 함으로 체크 인 된 첫 번째 버전과 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="b1363-363">**기록** 창에서 최신 타임 스탬프가 있는 GPO 버전을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="b1363-364">CTRL 키를 누른 다음 **컴퓨터 버전이** \* \* \\ \* \* \*가 아닌 가장 오래 된 GPO 버전을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="b1363-365">**차이점** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-365">Click the **Differences** button.</span></span> <span data-ttu-id="b1363-366">**계정 정책/암호 정책** 섹션이 녹색으로 강조 표시 되 고 앞에 **\ [+ \ \]** 가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="b1363-367">이는 해당 설정이 GPO의 이후 버전 에서만 구성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="b1363-368">**계정 정책/암호 정책을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="b1363-369">**최소 비밀 번호 길이** 설정도 녹색으로 강조 표시 되 고 앞에 **\ [+ \]** 가 있으면 GPO의 후자 버전 으로만 구성 되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="b1363-370">웹 브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-370">Close the Web browser.</span></span>

**<span data-ttu-id="b1363-371">프로덕션 환경에 GPO를 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="b1363-372">**보류** 탭에서 **mygpo** 를 마우스 오른쪽 단추로 클릭 한 다음 **승인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="b1363-373">GPO 기록에 포함할 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="b1363-374">**예**를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-374">Click **Yes**.</span></span> <span data-ttu-id="b1363-375">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-376">GPO가 프로덕션 환경에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="b1363-377">GPO를 도메인 또는 조직 구성 단위에 연결 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="b1363-378">GPMC에서 구성 된 GPO를 적용 하려는 도메인 또는 OU (조직 구성 단위)를 마우스 오른쪽 단추로 클릭 한 다음 **기존 Gpo 연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="b1363-379">**GPO 선택** 대화 상자에서 **mygpo**를 클릭 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="b1363-380">4 단계: 서식 파일을 사용 하 여 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="b1363-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="b1363-381">이 단계에서는 편집자 역할이 있는 계정을 사용 하 여 서식 파일을 만들고 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="b1363-382">이 서식 파일은 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="b1363-383">서식 파일을 편집할 수는 없지만 서식 파일을 기반으로 새 GPO를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="b1363-384">서식 파일은 동일한 정책 설정이 여러 개 포함 된 여러 Gpo를 빠르게 만드는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="b1363-385">기존 GPO를 기반으로 서식 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="b1363-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="b1363-386">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="b1363-387">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b1363-388">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="b1363-389">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **서식 파일로 저장** 을 클릭 하 여 현재 mygpo에 있는 모든 설정을 통합 하는 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="b1363-390">서식 파일과 메모의 이름으로 **MyTemplate** 를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="b1363-391">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-392">**서식** 파일 탭에 새 서식 파일이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="b1363-393">AGPM을 통해 새 GPO를 만들고 관리 하도록 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="b1363-394">**제어** 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="b1363-395">**변경 컨트롤** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새 제어 된 GPO**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="b1363-396">**새 제어 된 GPO** 대화 상자에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="b1363-397">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="b1363-398">**Myothergpo** 를 새 gpo의 이름으로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="b1363-399">새 GPO에 대 한 메모를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="b1363-400">새 GPO가 승인 즉시 프로덕션 환경에 배포 되도록 **라이브 만들기** 를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="b1363-401">**GPO 서식 파일에서** **MyTemplate**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="b1363-402">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="b1363-403">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-404">**보류** 탭에 새 GPO가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="b1363-405">승인자 역할에 할당 된 계정을 사용 하 여 [1 단계: Gpo 만들기](#bkmk-manage1)와 같이 보류 중인 요청을 승인 하 고 gpo를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="b1363-406">MyTemplate는 MyGPO에서 구성한 모든 설정을 통합 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="b1363-407">MyOtherGPO는 MyTemplate를 사용 하 여 만들어졌기 때문에 처음에는 MyTemplate가 생성 된 시점에 MyGPO에 포함 된 모든 설정이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="b1363-408">이는 차이 보고서를 생성 하 여 MyOtherGPO를 MyTemplate로 비교 하 여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="b1363-409">편집을 위해 아카이브에 대해 GPO를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="b1363-410">AGPM 클라이언트를 설치한 컴퓨터에서 AGPM의 편집기 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="b1363-411">**Myothergpo**를 마우스 오른쪽 단추로 클릭 한 다음 **체크 아웃**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="b1363-412">체크 아웃 된 동안 GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="b1363-413">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-414">**제어** 탭에서 GPO의 상태가 **체크 아웃**으로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="b1363-415">오프 라인으로 GPO를 편집 하 고 계정 잠금 기간을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="b1363-416">**제어** 탭에서 **myothergpo**를 마우스 오른쪽 단추로 클릭 한 다음 **편집** 을 클릭 하 여 **그룹 정책 관리 편집기** 창을 열고 GPO의 오프 라인 복사본을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="b1363-417">이 시나리오에서는 최소 암호 길이를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="b1363-418">**컴퓨터 구성**에서 **정책**, **Windows 설정**, **보안 설정**, **계정 정책**, **계정 잠금 정책을**두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="b1363-419">세부 정보 창에서 **계정 잠금 기간**을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="b1363-420">속성 창에서 **이 정책 정의 설정을**선택 하 고 기간을 **30** 분으로 설정한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="b1363-421">**그룹 정책 관리 편집기** 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="b1363-422">[2 단계: GPO 편집](#bkmk-manage2)에서 myothergpo를 보관 및 요청 배포로 체크 인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="b1363-423">다른 보고서를 사용 하 여 MyOtherGPO와 MyGPO 또는 MyTemplate를 비교할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="b1363-424">검토자 역할을 포함 하는 계정 (AGPM 관리자 \ [모든 권한 \], 승인자, 편집자 또는 검토자)이 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="b1363-425">GPO와 다른 GPO를 비교 하 여 서식 파일에</span><span class="sxs-lookup"><span data-stu-id="b1363-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="b1363-426">MyGPO와 MyOtherGPO를 비교 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="b1363-427">**제어** 탭에서 **mygpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="b1363-428">CTRL 키를 누른 다음 **Myothergpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="b1363-429">**Myothergpo**를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 가리킨 다음 **HTML 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="b1363-430">MyOtherGPO와 MyTemplate를 비교 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="b1363-431">**제어** 탭에서 **myothergpo**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="b1363-432">**Myothergpo**를 마우스 오른쪽 단추로 클릭 하 고 **차이점**을 가리킨 다음 **서식 파일**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="b1363-433">**MyTemplate** 및 **HTML 보고서**를 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="b1363-434">5 단계: GPO 삭제 및 복원</span><span class="sxs-lookup"><span data-stu-id="b1363-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="b1363-435">이 단계에서는 GPO를 삭제 하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="b1363-436">GPO를 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="b1363-437">AGPM 클라이언트를 설치한 컴퓨터에서 승인자 역할이 할당 된 사용자 계정으로 로그온 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="b1363-438">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="b1363-439">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="b1363-440">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="b1363-441">**보관 및 프로덕션에서 Gpo 삭제** 를 클릭 하 여 보관 저장소의 버전과 프로덕션 환경에서 배포 된 GPO 버전을 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="b1363-442">GPO에 대 한 감사 추적에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="b1363-443">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-444">GPO가 **제어** 탭에서 제거 되 고 **휴지통** 탭에 표시 되며 복원 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="b1363-445">필요에 따라 GPO를 삭제 한 후에도 가끔 검색을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="b1363-446">이 단계에서는 삭제 된 GPO를 복원 하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="b1363-447">삭제 된 GPO를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="b1363-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="b1363-448">**콘텐츠** 탭에서 **휴지통** 탭을 클릭 하 여 삭제 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="b1363-449">**Mygpo**를 마우스 오른쪽 단추로 클릭 한 다음 **복원을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="b1363-450">GPO 기록에 표시할 메모를 입력 한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="b1363-451">**AGPM 진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-452">**휴지통** 탭에서 GPO가 제거 되 고 **제어** 탭에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="b1363-453">**참고**  GPO를 보관 함으로 복원 해도 자동으로 프로덕션 환경에 다시 배포 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="b1363-454">GPO를 프로덕션 환경으로 반환 하려면 [3 단계: Gpo 검토 및 배포](#bkmk-manage3)와 같이 gpo를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="b1363-455">GPO를 편집 하 고 배포 하면 GPO에 대 한 최근 변경 내용으로 인해 문제가 발생 한 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="b1363-456">이 단계에서는 이전 버전의 GPO로 롤백하는 승인자 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="b1363-457">GPO 기록의 모든 버전으로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="b1363-458">메모 및 레이블을 사용 하 여 알려진 좋은 버전을 식별 하 고 특정 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="b1363-459">이전 버전의 GPO로 롤백하는 방법</span><span class="sxs-lookup"><span data-stu-id="b1363-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="b1363-460">**콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="b1363-461">**Mygpo** 를 두 번 클릭 하 여 기록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="b1363-462">배포할 버전을 마우스 오른쪽 단추로 클릭 하 고 **배포**를 클릭 한 다음 **예**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="b1363-463">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b1363-464">**기록** 창에서 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="b1363-465">**참고**  다시 배포 된 버전이 의도 된 버전 인지 확인 하려면 두 버전의 차이점 보고서를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="b1363-466">GPO의 **기록** 창에서 두 버전을 선택 하 고 마우스 오른쪽 단추로 클릭 한 다음 **차이**를 가리킨 다음 **HTML 보고서** 또는 **XML 보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1363-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





