---
title: Configuration Manager에서 MBAM 보고서 이해
description: Configuration Manager에서 MBAM 보고서 이해
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823823"
---
# <span data-ttu-id="1665b-103">Configuration Manager에서 MBAM 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="1665b-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="1665b-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)이 Configuration Manager 통합 토폴로지로 설치 되 면 하드웨어 준수 및 보고 기능이 구성 관리자 인프라로, 그리고 MBAM으로 이동 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="1665b-105">구성 관리자 토폴로지를 사용 하는 경우 관리 및 모니터링 웹 사이트를 사용 하 여 계속 액세스할 수 있는 복구 감사 보고서를 제외 하 고는 MBAM이 아닌 Configuration Manager에서 보고서를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="1665b-106">Configuration Manager 통합 토폴로지의 보고서에는 엔터프라이즈 및 MBAM이 관리 하는 개별 컴퓨터 및 장치에 대 한 BitLocker 준수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="1665b-107">보고서는 테이블 형식 정보와 차트를 모두 제공 하며, 보고서를 필터링 하 여 다양 한 관점에서 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="1665b-108">이 항목의 정보는 Configuration Manager에서 실행 하는 MBAM 보고서에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="1665b-109">독립 실행형 토폴로지에 대 한 MBAM 보고서에 대 한 자세한 내용은 [Mbam 보고서 이해](understanding-mbam-reports-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1665b-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="1665b-110">Configuration Manager에서 보고서에 액세스</span><span class="sxs-lookup"><span data-stu-id="1665b-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="1665b-111">Configuration Manager에서 보고서 기능에 액세스 하려면 **Configuration manager 콘솔**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="1665b-112">사용 가능한 보고서 목록을 표시 하려면 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="1665b-113">Configuration Manager 2007에서 **컴퓨터 관리** 노드를 확장 한 다음 **보고** 노드를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="1665b-114">SystemCenter2012 ConfigurationManager의 모니터링 작업 영역에 있는 **개요**아래에서 **보고** 노드를 확장 한 다음 **보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="1665b-115">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="1665b-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="1665b-116">BitLocker 엔터프라이즈 준수 대시보드는 엔터프라이즈 전체의 BitLocker 준수 상태를 보여 주는 다음과 같은 그래프를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="1665b-117">준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="1665b-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="1665b-118">비 준수 오류 분포</span><span class="sxs-lookup"><span data-stu-id="1665b-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="1665b-119">드라이브 유형별 준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="1665b-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="1665b-120">준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="1665b-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="1665b-121">이 원형 차트는 엔터프라이즈 내의 컴퓨터 준수 상태를 표시 하 고, 선택한 컬렉션에 있는 컴퓨터의 총 수와 해당 준수 상태가 있는 컴퓨터의 백분율을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="1665b-122">각 상태를 포함 하는 실제 컴퓨터 수도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="1665b-123">원형 차트에는 다음과 같은 준수 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="1665b-124">기준</span><span class="sxs-lookup"><span data-stu-id="1665b-124">Compliant</span></span>

-   <span data-ttu-id="1665b-125">비 준수</span><span class="sxs-lookup"><span data-stu-id="1665b-125">Non Compliant</span></span>

-   <span data-ttu-id="1665b-126">사용자 예외</span><span class="sxs-lookup"><span data-stu-id="1665b-126">User Exempt</span></span>

-   <span data-ttu-id="1665b-127">임시 사용자 예외</span><span class="sxs-lookup"><span data-stu-id="1665b-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="1665b-128">정책이 적용 되지 않음</span><span class="sxs-lookup"><span data-stu-id="1665b-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="1665b-129">알 수 없음-상태가 오류로 보고 된 컴퓨터 또는 컬렉션에 속해 있지만 준수 상태 (예: 조직에서 연결이 해제 된 경우)를 보고 한 경우는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="1665b-130">비 준수 오류 분포</span><span class="sxs-lookup"><span data-stu-id="1665b-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="1665b-131">이 원형 차트는 엔터프라이즈에서 BitLocker 드라이브 암호화 정책과 호환 되지 않는 컴퓨터 범주를 표시 하 고 각 범주의 컴퓨터 수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="1665b-132">각 범주 비율은 컬렉션에 있는 비규격 컴퓨터의 총 수를 기준으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="1665b-133">사용자가 연기 한 암호화</span><span class="sxs-lookup"><span data-stu-id="1665b-133">User postponed encryption</span></span>

-   <span data-ttu-id="1665b-134">호환 되는 TPM을 찾을 수 없음</span><span class="sxs-lookup"><span data-stu-id="1665b-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="1665b-135">시스템 파티션이 사용할 수 없는 경우 또는 충분히 큰 경우</span><span class="sxs-lookup"><span data-stu-id="1665b-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="1665b-136">정책 충돌</span><span class="sxs-lookup"><span data-stu-id="1665b-136">Policy conflict</span></span>

-   <span data-ttu-id="1665b-137">TPM 자동 프로 비전 대기 중</span><span class="sxs-lookup"><span data-stu-id="1665b-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="1665b-138">알 수 없는 오류가 발생 하였습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="1665b-139">정보 없음-MBAM 클라이언트가 설치 되지 않았거나 MBAM 클라이언트가 설치 되었지만 정품 인증 되지 않은 컴퓨터 (예: 서비스가 작동 하지 않는)</span><span class="sxs-lookup"><span data-stu-id="1665b-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="1665b-140">드라이브 유형별 준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="1665b-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="1665b-141">이 막대 차트는 드라이브 유형별 현재 BitLocker 준수 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="1665b-142">상태는 "규격" 및 "비규격"입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="1665b-143">고정 데이터 드라이브 및 운영 체제 드라이브에 대 한 막대가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="1665b-144">고정 데이터 드라이브가 없는 컴퓨터는 운영 체제 드라이브 표시줄에만 포함 되며 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="1665b-145">이 차트에는 BitLocker 드라이브 암호화 정책 또는 "정책 없음" 범주에서 예외를 허용한 사용자가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="1665b-146">BitLocker 엔터프라이즈 준수 정보 보고서</span><span class="sxs-lookup"><span data-stu-id="1665b-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="1665b-147">이 보고서는 엔터프라이즈 전체의 bitlocker 사용을 대상으로 하는 컴퓨터 컬렉션에 대 한 전반적인 BitLocker 준수에 대 한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="1665b-148">BitLocker 엔터프라이즈 준수 정보 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="1665b-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1665b-149">열 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="1665b-150">설명</span><span class="sxs-lookup"><span data-stu-id="1665b-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-151">관리 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1665b-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-152">MBAM이 관리 하는 컴퓨터 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-153">% 규격</span><span class="sxs-lookup"><span data-stu-id="1665b-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-154">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-155">% 규격이 아닌%</span><span class="sxs-lookup"><span data-stu-id="1665b-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-156">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-157">% 알 수 없는 규정</span><span class="sxs-lookup"><span data-stu-id="1665b-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-158">규정 준수 상태를 알 수 없는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-159">% 예외</span><span class="sxs-lookup"><span data-stu-id="1665b-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-160">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-161">% 비 면제</span><span class="sxs-lookup"><span data-stu-id="1665b-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-162">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-163">기준</span><span class="sxs-lookup"><span data-stu-id="1665b-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-164">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-165">비호환</span><span class="sxs-lookup"><span data-stu-id="1665b-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-166">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-167">알 수 없는 규정 준수</span><span class="sxs-lookup"><span data-stu-id="1665b-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-168">규정 준수 상태를 알 수 없는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-169">제외 등급</span><span class="sxs-lookup"><span data-stu-id="1665b-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-170">BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1665b-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-171">비 예외</span><span class="sxs-lookup"><span data-stu-id="1665b-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-172">BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1665b-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1665b-173">BitLocker 엔터프라이즈 준수 정보 보고서-준수 상태</span><span class="sxs-lookup"><span data-stu-id="1665b-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1665b-174">준수 상태</span><span class="sxs-lookup"><span data-stu-id="1665b-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="1665b-175">제외</span><span class="sxs-lookup"><span data-stu-id="1665b-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="1665b-176">설명</span><span class="sxs-lookup"><span data-stu-id="1665b-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-177">맞지</span><span class="sxs-lookup"><span data-stu-id="1665b-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-178">예외 아님</span><span class="sxs-lookup"><span data-stu-id="1665b-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-179">지정 된 정책에 따라 컴퓨터가 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-180">기준</span><span class="sxs-lookup"><span data-stu-id="1665b-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-181">예외 아님</span><span class="sxs-lookup"><span data-stu-id="1665b-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-182">컴퓨터는 지정 된 정책에 따라 규격을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1665b-183">BitLocker 엔터프라이즈 준수 요약 보고서</span><span class="sxs-lookup"><span data-stu-id="1665b-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="1665b-184">이 보고서 유형을 사용 하 여 엔터프라이즈 전체의 전반적인 BitLocker 준수에 대 한 정보를 표시 하 고 BitLocker 사용을 대상으로 하는 컴퓨터 컬렉션에 있는 개별 컴퓨터에 대 한 준수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="1665b-185">BitLocker 엔터프라이즈 준수 요약 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="1665b-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1665b-186">열 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="1665b-187">설명</span><span class="sxs-lookup"><span data-stu-id="1665b-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-188">관리 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1665b-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-189">MBAM이 관리 하는 컴퓨터 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-190">% 규격</span><span class="sxs-lookup"><span data-stu-id="1665b-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-191">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-192">% 규격이 아닌%</span><span class="sxs-lookup"><span data-stu-id="1665b-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-193">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-194">% 알 수 없는 규정</span><span class="sxs-lookup"><span data-stu-id="1665b-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-195">규정 준수 상태를 알 수 없는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-196">% 예외</span><span class="sxs-lookup"><span data-stu-id="1665b-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-197">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-198">% 비 면제</span><span class="sxs-lookup"><span data-stu-id="1665b-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-199">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-200">기준</span><span class="sxs-lookup"><span data-stu-id="1665b-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-201">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-202">비호환</span><span class="sxs-lookup"><span data-stu-id="1665b-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-203">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-204">알 수 없는 규정 준수</span><span class="sxs-lookup"><span data-stu-id="1665b-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-205">규정 준수 상태를 알 수 없는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-206">제외 등급</span><span class="sxs-lookup"><span data-stu-id="1665b-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-207">BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1665b-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-208">비 예외</span><span class="sxs-lookup"><span data-stu-id="1665b-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-209">BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1665b-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1665b-210">BitLocker 엔터프라이즈 준수 요약 보고서-컴퓨터 세부 정보</span><span class="sxs-lookup"><span data-stu-id="1665b-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1665b-211">열 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="1665b-212">설명</span><span class="sxs-lookup"><span data-stu-id="1665b-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-213">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-214">MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-215">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-216">클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-217">준수 상태</span><span class="sxs-lookup"><span data-stu-id="1665b-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-218">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="1665b-219">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="1665b-220">Drive (다음 표에 나와 있는 참조)는 각 드라이브의 준수 상태에 따라 서로 다른 준수 상태를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="1665b-221">그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-222">제외</span><span class="sxs-lookup"><span data-stu-id="1665b-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-223">사용자가 BitLocker 정책에서 제외 되었는지 아니면 예외를 표시 하지 않음을 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-224">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="1665b-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-225">디바이스의 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-226">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="1665b-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-227">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-228">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="1665b-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-229">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="1665b-230">대화 상대 주파수를 구성할 수 있습니다 (MBAM 정책 설정 참조).</span><span class="sxs-lookup"><span data-stu-id="1665b-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1665b-231">BitLocker 컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="1665b-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="1665b-232">이 보고서 유형을 사용 하 여 컴퓨터에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="1665b-233">컴퓨터 준수 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 제공 하 고 컴퓨터의 각 드라이브 유형에 적용 되는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="1665b-234">각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="1665b-235">**참고**  이동식 데이터 볼륨 암호화 상태가 보고서에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="1665b-236">BitLocker 컴퓨터 준수 보고서-컴퓨터 세부 정보 필드</span><span class="sxs-lookup"><span data-stu-id="1665b-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1665b-237">열 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="1665b-238">설명</span><span class="sxs-lookup"><span data-stu-id="1665b-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-239">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-240">MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-241">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-242">클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-243">컴퓨터 종류</span><span class="sxs-lookup"><span data-stu-id="1665b-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-244">컴퓨터의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-244">Type of computer.</span></span> <span data-ttu-id="1665b-245">유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-246">운영 체제</span><span class="sxs-lookup"><span data-stu-id="1665b-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-247">MBAM 관리 클라이언트 컴퓨터에서 찾을 수 있는 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-248">전반적인 준수</span><span class="sxs-lookup"><span data-stu-id="1665b-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-249">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="1665b-250">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="1665b-251">Drive (다음 표에 나와 있는 참조)는 각 드라이브의 준수 상태에 따라 서로 다른 준수 상태를 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="1665b-252">그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-253">운영 체제 준수</span><span class="sxs-lookup"><span data-stu-id="1665b-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-254">MBAM으로 관리 되는 운영 체제의 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="1665b-255">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-256">고정 데이터 드라이브 준수</span><span class="sxs-lookup"><span data-stu-id="1665b-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-257">MBAM으로 관리 되는 고정 데이터 드라이브의 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="1665b-258">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-259">마지막 업데이트 날짜</span><span class="sxs-lookup"><span data-stu-id="1665b-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-260">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="1665b-261">대화 상대 주파수를 구성할 수 있습니다 (MBAM 정책 설정 참조).</span><span class="sxs-lookup"><span data-stu-id="1665b-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-262">제외</span><span class="sxs-lookup"><span data-stu-id="1665b-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-263">사용자가 BitLocker 정책에서 제외 되었는지 아니면 예외를 표시 하지 않음을 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-264">제외 사용자</span><span class="sxs-lookup"><span data-stu-id="1665b-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-265">BitLocker 정책에서 제외 된 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-266">면제 날짜</span><span class="sxs-lookup"><span data-stu-id="1665b-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-267">면제를 부여 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-268">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="1665b-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-269">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-270">정책 암호화 수준</span><span class="sxs-lookup"><span data-stu-id="1665b-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-271">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="1665b-272">(예: 디퓨저와 128-비트)</span><span class="sxs-lookup"><span data-stu-id="1665b-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-273">정책: 운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="1665b-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-274">O/S 및 적절 한 보호기 유형에 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-275">정책: 고정 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="1665b-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-276">고정 드라이브에 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-277">제조업체</span><span class="sxs-lookup"><span data-stu-id="1665b-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-278">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-279">모델</span><span class="sxs-lookup"><span data-stu-id="1665b-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-280">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-281">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="1665b-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-282">MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="1665b-283">BitLocker 컴퓨터 준수 보고서-컴퓨터 볼륨 필드</span><span class="sxs-lookup"><span data-stu-id="1665b-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1665b-284">열 이름</span><span class="sxs-lookup"><span data-stu-id="1665b-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="1665b-285">설명</span><span class="sxs-lookup"><span data-stu-id="1665b-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-286">드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="1665b-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-287">사용자가 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="1665b-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-288">드라이브 종류</span><span class="sxs-lookup"><span data-stu-id="1665b-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-289">드라이브의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-289">Type of drive.</span></span> <span data-ttu-id="1665b-290">올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="1665b-291">이는 논리 볼륨이 아닌 실제 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-292">암호화 수준</span><span class="sxs-lookup"><span data-stu-id="1665b-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-293">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-294">보호 기능 유형</span><span class="sxs-lookup"><span data-stu-id="1665b-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-295">운영 체제 또는 고정 볼륨을 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="1665b-296">운영 체제의 유효한 보호기 유형은 TPM 또는 TPM + PIN 이며, 고정 데이터 볼륨에는 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1665b-297">보호기 상태</span><span class="sxs-lookup"><span data-stu-id="1665b-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-298">MBAM으로 관리 되는 컴퓨터가 정책에 지정 된 보호기 형식을 사용 하도록 설정 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="1665b-299">유효한 상태는 ON 또는 OFF입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1665b-300">암호화 상태</span><span class="sxs-lookup"><span data-stu-id="1665b-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="1665b-301">드라이브의 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-301">Encryption state of the drive.</span></span> <span data-ttu-id="1665b-302">유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1665b-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1665b-303">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1665b-303">Related topics</span></span>


[<span data-ttu-id="1665b-304">Configuration Manager와 함께 MBAM 사용</span><span class="sxs-lookup"><span data-stu-id="1665b-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





