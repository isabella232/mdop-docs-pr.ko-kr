---
title: MBAM 2.5 독립 실행형 보고서 이해
description: MBAM 2.5 독립 실행형 보고서 이해
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812777"
---
# <span data-ttu-id="5bc0c-103">MBAM 2.5 독립 실행형 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="5bc0c-103">Understanding MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="5bc0c-104">이 항목에서는 독립 실행형 토폴로지에서 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 실행 하는 경우 사용할 수 있는 보고서에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-104">This topic describes the reports that are available when you are running Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology.</span></span>

**<span data-ttu-id="5bc0c-105">참고</span><span class="sxs-lookup"><span data-stu-id="5bc0c-105">Note</span></span>**  
<span data-ttu-id="5bc0c-106">Configuration Manager 통합 토폴로지로 MBAM을 실행 중인 경우에는 MBAM이 아닌 Configuration Manager에서 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-106">If you are running MBAM with the Configuration Manager Integration topology, you generate reports from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="5bc0c-107">이러한 보고서에 대 한 자세한 내용은 [Configuration Manager 통합 토폴로지에 대 한 MBAM 2.5 보고서 보기](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-107">See [Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) for more information about these reports.</span></span>



## <span data-ttu-id="5bc0c-108">MBAM 독립 실행형 토폴로지 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="5bc0c-108">Understanding the MBAM Stand-alone topology reports</span></span>


<span data-ttu-id="5bc0c-109">MBAM은 BitLocker 준수를 위해 조직을 모니터링 하는 데 사용할 수 있는 세 가지 보고서 유형을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-109">MBAM provides three report types that you can use to monitor your organization for BitLocker compliance:</span></span>

-   [<span data-ttu-id="5bc0c-110">엔터프라이즈 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="5bc0c-110">Enterprise Compliance Report</span></span>](#bkmk-enterprisecompliance)

-   [<span data-ttu-id="5bc0c-111">컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="5bc0c-111">Computer Compliance Report</span></span>](#bkmk-compliance)

-   [<span data-ttu-id="5bc0c-112">복구 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="5bc0c-112">Recovery Audit Report</span></span>](#bkmk-recovery)

<span data-ttu-id="5bc0c-113">독립 실행형 토폴로지에서 MBAM을 실행 중인 경우 MBAM 보고서에 액세스 하려면 웹 브라우저를 연 다음 관리 및 모니터링 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-113">To access MBAM reports when you are running MBAM in the Stand-alone topology, open a web browser, and then open the Administration and Monitoring Website.</span></span> <span data-ttu-id="5bc0c-114">왼쪽 메뉴 모음에서 **보고서** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-114">Select **Reports** in the left menu bar.</span></span> <span data-ttu-id="5bc0c-115">최상위 메뉴 모음에서 생성 하려는 보고서 종류를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-115">From the top menu bar, select the kind of report that you want to generate.</span></span> <span data-ttu-id="5bc0c-116">이러한 보고서를 생성 하는 방법에 대 한 자세한 내용은 [MBAM 2.5 독립 실행형 보고서 생성](generating-mbam-25-stand-alone-reports.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-116">For more information about generating these reports, see [Generating MBAM 2.5 Stand-alone Reports](generating-mbam-25-stand-alone-reports.md).</span></span>

### <a href="" id="bkmk-enterprisecompliance"></a><span data-ttu-id="5bc0c-117">엔터프라이즈 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="5bc0c-117">Enterprise Compliance Report</span></span>

<span data-ttu-id="5bc0c-118">조직의 전반적인 BitLocker 준수에 대 한 정보를 수집 하려면이 보고서 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-118">Use this report type to collect information about overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="5bc0c-119">필터를 사용 하 여 조직의 컴퓨터에 대 한 규정 준수 상태 및 오류 상태에 대 한 자세한 정보를 확인 하기 위해 검색 결과의 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-119">You can use filters to narrow your search results to learn more about the compliance state and error status of computers in your organization.</span></span>

**<span data-ttu-id="5bc0c-120">엔터프라이즈 준수 개요</span><span class="sxs-lookup"><span data-stu-id="5bc0c-120">Enterprise Compliance Overview</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bc0c-121">열 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-121">Column Name</span></span></th>
<th align="left"><span data-ttu-id="5bc0c-122">설명</span><span class="sxs-lookup"><span data-stu-id="5bc0c-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-123">관리 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="5bc0c-123">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-124">MBAM이 관리 하는 컴퓨터 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-124">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-125">% 규격</span><span class="sxs-lookup"><span data-stu-id="5bc0c-125">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-126">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-126">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-127">% 규격이 아닌%</span><span class="sxs-lookup"><span data-stu-id="5bc0c-127">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-128">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-128">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-129">% 예외</span><span class="sxs-lookup"><span data-stu-id="5bc0c-129">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-130">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-130">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-131">% 비 면제</span><span class="sxs-lookup"><span data-stu-id="5bc0c-131">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-132">BitLocker 암호화 요구 사항에서 제외 되지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-132">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-133">기준</span><span class="sxs-lookup"><span data-stu-id="5bc0c-133">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-134">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-134">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-135">비호환</span><span class="sxs-lookup"><span data-stu-id="5bc0c-135">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-136">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-136">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-137">제외 등급</span><span class="sxs-lookup"><span data-stu-id="5bc0c-137">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-138">BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="5bc0c-138">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-139">비 예외</span><span class="sxs-lookup"><span data-stu-id="5bc0c-139">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-140">BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="5bc0c-140">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5bc0c-141">엔터프라이즈 준수 컴퓨터 세부 정보</span><span class="sxs-lookup"><span data-stu-id="5bc0c-141">Enterprise Compliance Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bc0c-142">열 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-142">Column Name</span></span></th>
<th align="left"><span data-ttu-id="5bc0c-143">설명</span><span class="sxs-lookup"><span data-stu-id="5bc0c-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-144">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-144">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-145">MBAM으로 관리 되는 사용자 지정 DNS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-145">User-specified DNS name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-146">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-146">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-147">클라이언트 컴퓨터가 상주 하 고 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-147">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-148">준수 상태</span><span class="sxs-lookup"><span data-stu-id="5bc0c-148">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-149">컴퓨터에 대해 지정 된 정책에 따라 컴퓨터를 준수 하는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-149">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="5bc0c-150">상태는 비규격이 고 규격입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-150">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="5bc0c-151">준수 상태를 해석 하는 방법에 대 한 자세한 내용은 다음 엔터프라이즈 준수 보고서 준수 상태 테이블을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-151">See the following Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-152">제외</span><span class="sxs-lookup"><span data-stu-id="5bc0c-152">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-153">이 컴퓨터가 BitLocker 정책에서 제외 되었는지 여부를 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-153">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-154">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="5bc0c-154">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-155">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-155">Error and status messages about the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-156">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="5bc0c-156">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-157">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-157">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="5bc0c-158">대화 상대 주파수를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-158">The contact frequency is configurable.</span></span> <span data-ttu-id="5bc0c-159">자세한 내용은 MBAM 그룹 정책 설정을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-159">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a><span data-ttu-id="5bc0c-160">컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="5bc0c-160">Computer Compliance Report</span></span>

<span data-ttu-id="5bc0c-161">컴퓨터 또는 사용자와 관련 된 정보를 수집 하려면이 보고서 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-161">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="5bc0c-162">엔터프라이즈 준수 보고서에서 컴퓨터 이름을 클릭 하거나 컴퓨터 준수 보고서에 컴퓨터 이름을 입력 하 여이 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-162">View this report by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="5bc0c-163">이 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-163">This report shows detailed encryption information about each drive (operating system and fixed data drives) on a computer.</span></span> <span data-ttu-id="5bc0c-164">또한 컴퓨터의 각 드라이브 유형에 적용 되는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-164">It also indicates the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="5bc0c-165">각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-165">To view the details of each drive, expand the Computer Name entry.</span></span>

**<span data-ttu-id="5bc0c-166">참고</span><span class="sxs-lookup"><span data-stu-id="5bc0c-166">Note</span></span>**  
<span data-ttu-id="5bc0c-167">이 보고서에는 이동식 데이터 볼륨 암호화 상태가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-167">Removable Data Volume encryption status is not shown in this report.</span></span>



**<span data-ttu-id="5bc0c-168">컴퓨터 준수 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="5bc0c-168">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bc0c-169">열 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-169">Column Name</span></span></th>
<th align="left"><span data-ttu-id="5bc0c-170">설명</span><span class="sxs-lookup"><span data-stu-id="5bc0c-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-171">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-171">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-172">MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-172">User-specified DNS computer name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-173">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-173">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-174">클라이언트 컴퓨터가 상주 하 고 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-174">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-175">컴퓨터 종류</span><span class="sxs-lookup"><span data-stu-id="5bc0c-175">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-176">컴퓨터의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-176">Type of computer.</span></span> <span data-ttu-id="5bc0c-177">유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-177">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-178">운영 체제</span><span class="sxs-lookup"><span data-stu-id="5bc0c-178">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-179">MBAM으로 관리 되는 클라이언트 컴퓨터에서 검색 된 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-179">Operating system type found on the client computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-180">준수 상태</span><span class="sxs-lookup"><span data-stu-id="5bc0c-180">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-181">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-181">Overall compliance status of the computer that is managed by MBAM.</span></span> <span data-ttu-id="5bc0c-182">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-182">Valid states are Compliant and Noncompliant.</span></span></p>
<p><span data-ttu-id="5bc0c-183">드라이브 (다음 표 참조)의 준수 상태가 서로 다른 준수 상태를 나타낼 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-183">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="5bc0c-184">그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-184">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-185">정책 암호화 수준</span><span class="sxs-lookup"><span data-stu-id="5bc0c-185">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-186">MBAM 정책 사양 중 관리자가 선택한 암호화 수준 (예: 128-디퓨저)</span><span class="sxs-lookup"><span data-stu-id="5bc0c-186">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-187">정책 운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="5bc0c-187">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-188">운영 체제에 암호화가 필요한 경우 적절 한 보호기 형식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-188">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-189">정책 고정 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="5bc0c-189">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-190">고정 데이터 드라이브에 대해 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-190">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-191">정책 이동식 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="5bc0c-191">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-192">이동식 드라이브에 대 한 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-192">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-193">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="5bc0c-193">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-194">MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-194">Known users on the computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-195">제외</span><span class="sxs-lookup"><span data-stu-id="5bc0c-195">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-196">이 컴퓨터가 BitLocker 정책에서 제외 되었는지 여부를 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-196">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-197">제조업체</span><span class="sxs-lookup"><span data-stu-id="5bc0c-197">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-198">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-198">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-199">모델</span><span class="sxs-lookup"><span data-stu-id="5bc0c-199">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-200">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-200">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-201">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="5bc0c-201">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-202">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-202">Error and status messages about the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-203">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="5bc0c-203">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-204">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-204">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="5bc0c-205">대화 상대 주파수를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-205">The contact frequency is configurable.</span></span> <span data-ttu-id="5bc0c-206">자세한 내용은 MBAM 그룹 정책 설정을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-206">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5bc0c-207">컴퓨터 준수 보고서 드라이브 필드</span><span class="sxs-lookup"><span data-stu-id="5bc0c-207">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bc0c-208">열 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-208">Column Name</span></span></th>
<th align="left"><span data-ttu-id="5bc0c-209">설명</span><span class="sxs-lookup"><span data-stu-id="5bc0c-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-210">드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="5bc0c-210">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-211">사용자가 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="5bc0c-211">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-212">드라이브 종류</span><span class="sxs-lookup"><span data-stu-id="5bc0c-212">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-213">드라이브의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-213">Type of drive.</span></span> <span data-ttu-id="5bc0c-214">올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-214">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="5bc0c-215">이는 논리 볼륨이 아닌 실제 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-215">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-216">암호화 수준</span><span class="sxs-lookup"><span data-stu-id="5bc0c-216">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-217">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-217">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-218">보호 기능 유형</span><span class="sxs-lookup"><span data-stu-id="5bc0c-218">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-219">운영 체제 또는 고정 데이터 볼륨을 암호화 하는 데 사용 되는 그룹 정책 설정을 통해 선택한 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-219">Type of protector selected through the Group Policy setting used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-220">보호기 상태</span><span class="sxs-lookup"><span data-stu-id="5bc0c-220">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-221">MBAM으로 관리 되는 컴퓨터가 정책에 지정 된 보호기 형식을 사용 하도록 설정 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-221">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="5bc0c-222">유효한 상태는 ON 또는 OFF입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-222">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-223">암호화 상태</span><span class="sxs-lookup"><span data-stu-id="5bc0c-223">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-224">드라이브의 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-224">Encryption state of the drive.</span></span> <span data-ttu-id="5bc0c-225">유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-225">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-226">준수 상태</span><span class="sxs-lookup"><span data-stu-id="5bc0c-226">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-227">드라이브가 정책에 따라 사용 되는지 여부를 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-227">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="5bc0c-228">상태는 비규격이 고 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-228">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-229">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="5bc0c-229">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-230">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-230">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a><span data-ttu-id="5bc0c-231">복구 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="5bc0c-231">Recovery Audit Report</span></span>

<span data-ttu-id="5bc0c-232">BitLocker 복구 키에 대 한 액세스를 요청한 사용자를 감사 하려면이 보고서 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-232">Use this report type to audit users who have requested access to BitLocker recovery keys.</span></span> <span data-ttu-id="5bc0c-233">보고서는 원하는 필터링 조건을 기준으로 여러 필터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-233">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="5bc0c-234">특정 유형의 사용자 (지원 센터 사용자 또는 최종 사용자)에 게 요청 실패 여부, 요청 된 특정 키 유형, 검색을 수행 하는 날짜 범위 등을 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-234">You can filter on a specific type of user (a Help Desk user or an end user), whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span>

**<span data-ttu-id="5bc0c-235">복구 감사 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="5bc0c-235">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5bc0c-236">열 이름</span><span class="sxs-lookup"><span data-stu-id="5bc0c-236">Column Name</span></span></th>
<th align="left"><span data-ttu-id="5bc0c-237">설명</span><span class="sxs-lookup"><span data-stu-id="5bc0c-237">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-238">날짜 및 시간 요청</span><span class="sxs-lookup"><span data-stu-id="5bc0c-238">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-239">최종 사용자 또는 지원 센터 사용자가 키 검색 요청을 수행한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-239">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-240">감사 요청 원본</span><span class="sxs-lookup"><span data-stu-id="5bc0c-240">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-241">요청이 시작 된 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-241">The site from which the request was initiated.</span></span> <span data-ttu-id="5bc0c-242">이 항목에는 <strong> 셀프 서비스 포털 </strong> 또는 <strong> 헬프 데스크 두 가지 값 중 하나가 </strong> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-242">This entry will have one of two values: <strong>Self-Service Portal</strong> or <strong>Helpdesk</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-243">요청 상태</span><span class="sxs-lookup"><span data-stu-id="5bc0c-243">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-244">요청 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-244">Status of the request.</span></span> <span data-ttu-id="5bc0c-245">유효한 상태가 성공적으로 (키 검색 됨) 또는 실패 했습니다 (키가 검색 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="5bc0c-245">Valid statuses are Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-246">헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="5bc0c-246">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-247">키 검색 요청을 시작한 지원 센터 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-247">Help Desk user who initiated the request for key retrieval.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5bc0c-248">참고</span><span class="sxs-lookup"><span data-stu-id="5bc0c-248">Note</span></span></strong><br/><p><span data-ttu-id="5bc0c-249">고급 헬프데스크 사용자가 최종 사용자를 지정 하지 않고 키를 복구 하는 경우 <strong> 최종 사용자 </strong> 필드는 비어 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-249">If an Advanced Helpdesk User recovers the key without specifying the end user, the <strong>End User</strong> field will be blank.</span></span> <span data-ttu-id="5bc0c-250">표준 헬프데스크 사용자는 최종 사용자를 지정 해야 하며, 해당 사용자가이 필드에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-250">A standard Helpdesk User must specify the end user, and that user will appear in this field.</span></span></p>
<p><span data-ttu-id="5bc0c-251">셀프 서비스 포털을 통한 복구에는이 필드와 최종 사용자 필드에 요청 하는 최종 사용자가 나열 됩니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="5bc0c-251">A recovery via the Self-Service Portal will list the requesting end user both in this field and in the <strong>End User</strong> field.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-252">최종 사용자</span><span class="sxs-lookup"><span data-stu-id="5bc0c-252">End User</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-253">키 검색 요청을 시작한 최종 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-253">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-254">컴퓨터</span><span class="sxs-lookup"><span data-stu-id="5bc0c-254">Computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-255">복구 된 컴퓨터의 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-255">Computer name of the computer that was recovered.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5bc0c-256">키 유형</span><span class="sxs-lookup"><span data-stu-id="5bc0c-256">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-257">지원 센터 사용자 또는 최종 사용자가 요청한 키의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-257">Type of key that was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="5bc0c-258">MBAM에서 수집 하는 세 가지 키 유형은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-258">The three types of keys that MBAM collects are:</span></span></p>
<ul>
<li><p><span data-ttu-id="5bc0c-259">복구 키 암호 (복구 모드에서 컴퓨터를 복구 하는 데 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="5bc0c-259">Recovery Key Password (used to recover a computer in recovery mode)</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-260">복구 키 ID (다른 사용자 대신 복구 모드에서 컴퓨터를 복구 하는 데 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="5bc0c-260">Recovery Key ID (used to recover a computer in recovery mode on behalf of another user)</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-261">TPM 암호 해시 (TPM이 잠긴 컴퓨터를 복구 하는 데 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="5bc0c-261">TPM Password Hash (used to recover a computer with a locked TPM)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5bc0c-262">이유 설명</span><span class="sxs-lookup"><span data-stu-id="5bc0c-262">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="5bc0c-263">지정 된 키 유형이 지원 센터 사용자 또는 최종 사용자에 의해 요청 된 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-263">Reason the specified key type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="5bc0c-264">이유는 관리 및 모니터링 웹 사이트의 TPM 및 복구 기능을 관리 하는 방법에 명시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-264">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring Website.</span></span> <span data-ttu-id="5bc0c-265">유효한 항목은 사용자가 입력 한 텍스트 또는 다음 이유 코드 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-265">The valid entries are user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="5bc0c-266">운영 체제 부팅 순서 변경 됨</span><span class="sxs-lookup"><span data-stu-id="5bc0c-266">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-267">BIOS 변경 됨</span><span class="sxs-lookup"><span data-stu-id="5bc0c-267">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-268">운영 체제 파일이 변경 됨</span><span class="sxs-lookup"><span data-stu-id="5bc0c-268">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-269">분실 한 시작 키</span><span class="sxs-lookup"><span data-stu-id="5bc0c-269">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-270">핀 분실</span><span class="sxs-lookup"><span data-stu-id="5bc0c-270">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-271">TPM 다시 설정</span><span class="sxs-lookup"><span data-stu-id="5bc0c-271">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-272">암호 손실</span><span class="sxs-lookup"><span data-stu-id="5bc0c-272">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-273">스마트 카드 분실</span><span class="sxs-lookup"><span data-stu-id="5bc0c-273">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-274">PIN 잠금 다시 설정</span><span class="sxs-lookup"><span data-stu-id="5bc0c-274">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-275">TPM 켜기</span><span class="sxs-lookup"><span data-stu-id="5bc0c-275">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-276">TPM 끄기</span><span class="sxs-lookup"><span data-stu-id="5bc0c-276">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-277">TPM 암호 변경</span><span class="sxs-lookup"><span data-stu-id="5bc0c-277">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="5bc0c-278">TPM 지우기</span><span class="sxs-lookup"><span data-stu-id="5bc0c-278">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5bc0c-279">참고</span><span class="sxs-lookup"><span data-stu-id="5bc0c-279">Note</span></span>**  
<span data-ttu-id="5bc0c-280">**보고서 메뉴 모음** 에서 **내보내기** 단추를 클릭 하 여 결과를 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-280">Report results can be saved to a file by clicking the **Export** button on the **Reports** menu bar.</span></span>




## <span data-ttu-id="5bc0c-281">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5bc0c-281">Related topics</span></span>


[<span data-ttu-id="5bc0c-282">MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="5bc0c-282">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="5bc0c-283">MBAM 2.5 독립 실행형 보고서 생성</span><span class="sxs-lookup"><span data-stu-id="5bc0c-283">Generating MBAM 2.5 Stand-alone Reports</span></span>](generating-mbam-25-stand-alone-reports.md)



## <span data-ttu-id="5bc0c-284">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="5bc0c-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5bc0c-285">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-285">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5bc0c-286">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc0c-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





