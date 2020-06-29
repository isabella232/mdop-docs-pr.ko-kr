---
title: Configuration Manager 통합 토폴로지에 대한 MBAM 2.5 보고서 보기
description: Configuration Manager 통합 토폴로지에 대한 MBAM 2.5 보고서 보기
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824043"
---
# <span data-ttu-id="80697-103">Configuration Manager 통합 토폴로지에 대한 MBAM 2.5 보고서 보기</span><span class="sxs-lookup"><span data-stu-id="80697-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="80697-104">이 항목에서는 Configuration Manager 통합 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 구성할 때 사용할 수 있는 보고서에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="80697-105">이 보고서에는 엔터프라이즈 및 MBAM이 관리 하는 개별 컴퓨터 및 장치에 대 한 BitLocker 호환성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="80697-106">보고서는 테이블 형식 정보와 차트를 제공 하며 다양 한 관점에서 데이터를 볼 수 있는 필터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="80697-107">Configuration Manager 통합 토폴로지에서 관리 및 모니터링 웹 사이트에서 계속 표시 되는 **복구 감사 보고서**를 제외 하 고는 관리 및 모니터링 웹 사이트 대신 configuration manager에서 보고서를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="80697-108">독립 실행형 토폴로지에 대 한 MBAM 보고서에 대 한 자세한 내용은 [독립 실행형 토폴로지에 대 한 mbam 2.5 보고서 보기](viewing-mbam-25-reports-for-the-stand-alone-topology.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80697-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="80697-109">Configuration Manager에서 보고서에 액세스</span><span class="sxs-lookup"><span data-stu-id="80697-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="80697-110">Configuration Manager에서 보고서 기능에 액세스 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-111">버전의 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="80697-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="80697-112">보고서를 보는 방법</span><span class="sxs-lookup"><span data-stu-id="80697-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-113">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="80697-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="80697-114">왼쪽 창에서 <strong> 모니터링 작업 영역을 선택 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="80697-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="80697-115">트리에서 " <strong> 개요 </strong> &gt; <strong> 보고 </strong> &gt; <strong> 보고서" </strong> &gt; <strong> mbam을 확장 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="80697-116">보고서를 표시할 언어를 나타내는 폴더를 선택한 다음 오른쪽 창에서 보고서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-117">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="80697-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="80697-118">왼쪽 창에서 <strong> 컴퓨터 관리 </strong> &gt; <strong> 보고 </strong> &gt; <strong> reporting Services </strong> &gt; <strong> &lt; 서버 이름 &gt; </strong> &gt; <strong> 보고서 폴더를 확장 </strong> &gt; <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="80697-119">보고서를 표시할 언어를 나타내는 폴더를 선택한 다음 오른쪽 창에서 보고서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="80697-120">Configuration Manager의 보고서에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="80697-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="80697-121">Configuration Manager 통합 토폴로지와 독립 실행형 토폴로지에 대 한 보고서에는 몇 가지 사소한 차이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="80697-122">다음 섹션에서는 Configuration Manager 통합 토폴로지에 대 한 MBAM 보고서의 데이터에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="80697-123">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="80697-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="80697-124">BitLocker 엔터프라이즈 준수 세부 정보</span><span class="sxs-lookup"><span data-stu-id="80697-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="80697-125">BitLocker Enterprise 규정 준수 요약</span><span class="sxs-lookup"><span data-stu-id="80697-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="80697-126">BitLocker 컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="80697-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="80697-127">BitLocker 엔터프라이즈 준수 대시보드</span><span class="sxs-lookup"><span data-stu-id="80697-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="80697-128">BitLocker 엔터프라이즈 준수 대시보드는 엔터프라이즈 전체의 BitLocker 준수 상태를 보여 주는 다음과 같은 그래프를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="80697-129">준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="80697-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="80697-130">비 준수 오류 분포</span><span class="sxs-lookup"><span data-stu-id="80697-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="80697-131">드라이브 유형별 준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="80697-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="80697-132">준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="80697-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="80697-133">이 원형 차트는 엔터프라이즈 내의 컴퓨터에 대 한 준수 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80697-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="80697-134">또한 선택한 컬렉션의 총 컴퓨터 수와 해당 준수 상태가 있는 컴퓨터의 백분율이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="80697-135">각 상태를 포함 하는 실제 컴퓨터 수도 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="80697-136">원형 차트에는 다음과 같은 준수 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="80697-137">기준</span><span class="sxs-lookup"><span data-stu-id="80697-137">Compliant</span></span>

-   <span data-ttu-id="80697-138">비 준수</span><span class="sxs-lookup"><span data-stu-id="80697-138">Non Compliant</span></span>

-   <span data-ttu-id="80697-139">사용자 예외</span><span class="sxs-lookup"><span data-stu-id="80697-139">User Exempt</span></span>

-   <span data-ttu-id="80697-140">임시 사용자 예외</span><span class="sxs-lookup"><span data-stu-id="80697-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="80697-141">정책이 적용 되지 않음</span><span class="sxs-lookup"><span data-stu-id="80697-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="80697-142">없는.</span><span class="sxs-lookup"><span data-stu-id="80697-142">Unknown.</span></span> <span data-ttu-id="80697-143">이러한 컴퓨터는 상태 오류를 보고 했거나 컬렉션의 일부 이지만 준수 상태를 보고 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="80697-144">컴퓨터가 조직 으로부터 연결이 끊어지면 준수 상태가 부족 하 게 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="80697-145">비 준수 오류 분포</span><span class="sxs-lookup"><span data-stu-id="80697-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="80697-146">이 원형 차트는 엔터프라이즈에서 BitLocker 드라이브 암호화 정책과 호환 되지 않는 컴퓨터 범주를 표시 하 고 각 범주의 컴퓨터 수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80697-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="80697-147">각 범주 비율은 컬렉션에 있는 비규격 컴퓨터의 총 수를 기준으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="80697-148">사용자가 연기 한 암호화</span><span class="sxs-lookup"><span data-stu-id="80697-148">User postponed encryption</span></span>

-   <span data-ttu-id="80697-149">호환 되는 TPM을 찾을 수 없음</span><span class="sxs-lookup"><span data-stu-id="80697-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="80697-150">시스템 파티션이 사용할 수 없는 경우 또는 충분히 큰 경우</span><span class="sxs-lookup"><span data-stu-id="80697-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="80697-151">정책 충돌</span><span class="sxs-lookup"><span data-stu-id="80697-151">Policy conflict</span></span>

-   <span data-ttu-id="80697-152">TPM 자동 프로 비전 대기 중</span><span class="sxs-lookup"><span data-stu-id="80697-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="80697-153">알 수 없는 오류가 발생 하였습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="80697-154">정보가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-154">No information.</span></span> <span data-ttu-id="80697-155">이 컴퓨터에는 MBAM 클라이언트가 설치 되어 있지 않거나, MBAM 클라이언트가 설치 되었지만 정품 인증 되지 않은 경우 (예: 서비스가 작동 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="80697-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="80697-156">드라이브 유형별 준수 상태 배포</span><span class="sxs-lookup"><span data-stu-id="80697-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="80697-157">이 막대 차트는 드라이브 유형별 현재 BitLocker 준수 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80697-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="80697-158">상태는 **규격** 이며 **준수 되지**않습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="80697-159">고정 데이터 드라이브 및 운영 체제 드라이브에 대 한 막대가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="80697-160">고정 데이터 드라이브가 없는 컴퓨터는 **운영 체제 드라이브** 표시줄에만 포함 되며 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="80697-161">이 차트에는 BitLocker 드라이브 암호화 정책 또는 정책 없음 범주에서 예외를 허용한 사용자가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="80697-162">BitLocker 엔터프라이즈 준수 세부 정보</span><span class="sxs-lookup"><span data-stu-id="80697-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="80697-163">이 보고서는 엔터프라이즈 전체의 bitlocker 사용을 대상으로 하는 컴퓨터 컬렉션에 대 한 전반적인 BitLocker 준수에 대 한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80697-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="80697-164">BitLocker Enterprise 규정 준수 세부 정보 필드</span><span class="sxs-lookup"><span data-stu-id="80697-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-165">열 이름</span><span class="sxs-lookup"><span data-stu-id="80697-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="80697-166">설명</span><span class="sxs-lookup"><span data-stu-id="80697-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-167">관리 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="80697-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-168">MBAM이 관리 하는 컴퓨터 수입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-169">% 규격</span><span class="sxs-lookup"><span data-stu-id="80697-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-170">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-171">% 규격이 아닌%</span><span class="sxs-lookup"><span data-stu-id="80697-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-172">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-173">% 알 수 없는 규정</span><span class="sxs-lookup"><span data-stu-id="80697-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-174">준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-175">% 예외</span><span class="sxs-lookup"><span data-stu-id="80697-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-176">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-177">% 비 면제</span><span class="sxs-lookup"><span data-stu-id="80697-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-178">BitLocker 암호화 요구 사항에서 제외 되지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-179">기준</span><span class="sxs-lookup"><span data-stu-id="80697-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-180">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-181">비호환</span><span class="sxs-lookup"><span data-stu-id="80697-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-182">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-183">알 수 없는 규정 준수</span><span class="sxs-lookup"><span data-stu-id="80697-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-184">준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-185">제외 등급</span><span class="sxs-lookup"><span data-stu-id="80697-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-186">BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="80697-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-187">비 예외</span><span class="sxs-lookup"><span data-stu-id="80697-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-188">BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="80697-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="80697-189">BitLocker Enterprise 규정 준수 정보 상태</span><span class="sxs-lookup"><span data-stu-id="80697-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-190">준수 상태</span><span class="sxs-lookup"><span data-stu-id="80697-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="80697-191">제외</span><span class="sxs-lookup"><span data-stu-id="80697-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="80697-192">설명</span><span class="sxs-lookup"><span data-stu-id="80697-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-193">맞지</span><span class="sxs-lookup"><span data-stu-id="80697-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-194">예외 아님</span><span class="sxs-lookup"><span data-stu-id="80697-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-195">지정 된 정책에 따라 컴퓨터가 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-196">기준</span><span class="sxs-lookup"><span data-stu-id="80697-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-197">예외 아님</span><span class="sxs-lookup"><span data-stu-id="80697-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-198">컴퓨터는 지정 된 정책에 따라 규격을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="80697-199">BitLocker Enterprise 규정 준수 요약</span><span class="sxs-lookup"><span data-stu-id="80697-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="80697-200">이 보고서 유형을 사용 하 여 엔터프라이즈 전체의 전반적인 BitLocker 준수에 대 한 정보를 표시 하 고 BitLocker 사용을 대상으로 하는 컴퓨터 컬렉션에 있는 개별 컴퓨터에 대 한 준수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="80697-201">BitLocker Enterprise 규정 준수 요약 필드</span><span class="sxs-lookup"><span data-stu-id="80697-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-202">열 이름</span><span class="sxs-lookup"><span data-stu-id="80697-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="80697-203">설명</span><span class="sxs-lookup"><span data-stu-id="80697-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-204">관리 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="80697-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-205">MBAM이 관리 하는 컴퓨터 수입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-206">% 규격</span><span class="sxs-lookup"><span data-stu-id="80697-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-207">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-208">% 규격이 아닌%</span><span class="sxs-lookup"><span data-stu-id="80697-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-209">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-210">% 알 수 없는 규정</span><span class="sxs-lookup"><span data-stu-id="80697-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-211">준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-212">% 예외</span><span class="sxs-lookup"><span data-stu-id="80697-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-213">BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-214">% 비 면제</span><span class="sxs-lookup"><span data-stu-id="80697-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-215">BitLocker 암호화 요구 사항에서 제외 되지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-216">기준</span><span class="sxs-lookup"><span data-stu-id="80697-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-217">기업에서 준수 하는 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-218">비호환</span><span class="sxs-lookup"><span data-stu-id="80697-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-219">엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-220">알 수 없는 규정 준수</span><span class="sxs-lookup"><span data-stu-id="80697-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-221">준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-222">제외 등급</span><span class="sxs-lookup"><span data-stu-id="80697-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-223">BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="80697-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-224">비 예외</span><span class="sxs-lookup"><span data-stu-id="80697-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-225">BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="80697-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="80697-226">BitLocker Enterprise 규정 준수 요약 컴퓨터 세부 정보</span><span class="sxs-lookup"><span data-stu-id="80697-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-227">열 이름</span><span class="sxs-lookup"><span data-stu-id="80697-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="80697-228">설명</span><span class="sxs-lookup"><span data-stu-id="80697-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-229">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="80697-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-230">MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-231">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="80697-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-232">클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-233">준수 상태</span><span class="sxs-lookup"><span data-stu-id="80697-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-234">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="80697-235">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="80697-236">드라이브 (팔 로우 하는 다음 표 참조)에 대 한 준수 상태가 서로 다른 준수 상태를 나타내는 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="80697-237">그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80697-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-238">제외</span><span class="sxs-lookup"><span data-stu-id="80697-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-239">사용자가 BitLocker 정책에서 제외 되었는지 또는 제외 되지 않았음을 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-240">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="80697-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-241">디바이스의 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-242">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="80697-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-243">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-244">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="80697-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-245">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="80697-246">대화 상대 빈도는 그룹 정책 설정을 통해 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="80697-247">BitLocker 컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="80697-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="80697-248">이 보고서 유형을 사용 하 여 컴퓨터에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="80697-249">BitLocker 컴퓨터 준수 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="80697-250">또한 컴퓨터의 각 드라이브 유형에 적용 되는 정책의 표시를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="80697-251">각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="80697-252">**참고**  이동식 데이터 볼륨 암호화 상태는이 보고서에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="80697-253">BitLocker 컴퓨터 준수 보고서: 컴퓨터 세부 정보 필드</span><span class="sxs-lookup"><span data-stu-id="80697-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-254">열 이름</span><span class="sxs-lookup"><span data-stu-id="80697-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="80697-255">설명</span><span class="sxs-lookup"><span data-stu-id="80697-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-256">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="80697-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-257">MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-258">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="80697-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-259">클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-260">컴퓨터 종류</span><span class="sxs-lookup"><span data-stu-id="80697-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-261">컴퓨터의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-261">Type of computer.</span></span> <span data-ttu-id="80697-262">유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-263">운영 체제</span><span class="sxs-lookup"><span data-stu-id="80697-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-264">MBAM 관리 클라이언트 컴퓨터에서 찾을 수 있는 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-265">전반적인 준수</span><span class="sxs-lookup"><span data-stu-id="80697-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-266">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="80697-267">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="80697-268">드라이브 (팔 로우 하는 다음 표 참조)에 대 한 준수 상태가 서로 다른 준수 상태를 나타내는 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="80697-269">그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80697-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-270">운영 체제 준수</span><span class="sxs-lookup"><span data-stu-id="80697-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-271">MBAM으로 관리 되는 운영 체제의 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="80697-272">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-273">고정 데이터 드라이브 준수</span><span class="sxs-lookup"><span data-stu-id="80697-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-274">MBAM으로 관리 되는 고정 데이터 드라이브의 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="80697-275">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-276">마지막 업데이트 날짜</span><span class="sxs-lookup"><span data-stu-id="80697-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-277">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="80697-278">대화 상대 빈도는 그룹 정책 설정을 통해 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80697-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-279">제외</span><span class="sxs-lookup"><span data-stu-id="80697-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-280">사용자가 BitLocker 정책에서 제외 되었는지 또는 제외 되지 않았음을 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-281">제외 사용자</span><span class="sxs-lookup"><span data-stu-id="80697-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-282">BitLocker 정책에서 제외 된 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-283">면제 날짜</span><span class="sxs-lookup"><span data-stu-id="80697-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-284">면제를 부여 받은 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-285">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="80697-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-286">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-287">정책 암호화 수준</span><span class="sxs-lookup"><span data-stu-id="80697-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-288">관리자가 MBAM 정책 명세 중에 선택한 암호화 수준 (예: 128--디퓨저)</span><span class="sxs-lookup"><span data-stu-id="80697-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-289">정책: 운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="80697-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-290">운영 체제 및 적절 한 보호기 유형에 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-291">정책: 고정 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="80697-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-292">고정 데이터 드라이브에 대해 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-293">제조업체</span><span class="sxs-lookup"><span data-stu-id="80697-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-294">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-295">모델</span><span class="sxs-lookup"><span data-stu-id="80697-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-296">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-297">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="80697-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-298">MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="80697-299">BitLocker 컴퓨터 준수 보고서: 컴퓨터 볼륨 필드</span><span class="sxs-lookup"><span data-stu-id="80697-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80697-300">열 이름</span><span class="sxs-lookup"><span data-stu-id="80697-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="80697-301">설명</span><span class="sxs-lookup"><span data-stu-id="80697-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-302">드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="80697-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-303">사용자가 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="80697-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-304">드라이브 종류</span><span class="sxs-lookup"><span data-stu-id="80697-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-305">드라이브의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-305">Type of drive.</span></span> <span data-ttu-id="80697-306">올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="80697-307">이는 논리 볼륨이 아닌 실제 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-308">암호화 수준</span><span class="sxs-lookup"><span data-stu-id="80697-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-309">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-310">보호 기능 유형</span><span class="sxs-lookup"><span data-stu-id="80697-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-311">운영 체제 또는 고정 데이터 드라이브를 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="80697-312">운영 체제의 유효한 보호기 유형은 TPM 또는 TPM + PIN입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="80697-313">고정 데이터 드라이브의 유효한 보호기 유형은 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80697-314">보호기 상태</span><span class="sxs-lookup"><span data-stu-id="80697-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-315">MBAM으로 관리 되는 컴퓨터가 정책에 지정 된 보호기 형식을 사용 하도록 설정 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="80697-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="80697-316">유효한 상태는 ON 또는 OFF입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80697-317">암호화 상태</span><span class="sxs-lookup"><span data-stu-id="80697-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="80697-318">드라이브의 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="80697-318">Encryption state of the drive.</span></span> <span data-ttu-id="80697-319">유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80697-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="80697-320">관련 항목</span><span class="sxs-lookup"><span data-stu-id="80697-320">Related topics</span></span>


[<span data-ttu-id="80697-321">MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="80697-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="80697-322">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="80697-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="80697-323">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="80697-324">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="80697-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





