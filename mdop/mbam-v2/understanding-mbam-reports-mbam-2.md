---
title: MBAM 보고서 이해
description: MBAM 보고서 이해
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823813"
---
# <span data-ttu-id="745fa-103">MBAM 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="745fa-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="745fa-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치할 때 독립 실행형 토폴로지를 선택한 경우 MBAM에서 다른 보고서를 실행 하 여 BitLocker 사용 및 준수를 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="745fa-105">MBAM은 관리자가 관리 하는 모든 컴퓨터 및 장치에 대 한 규정 준수 및 기타 정보를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="745fa-106">이 항목의 정보는 엔터프라이즈 및 개별 컴퓨터 준수 및 키 복구 작업에 대 한 Microsoft BitLocker 관리 및 모니터링 보고서를 이해 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="745fa-107">**참고**  Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치할 때 구성 관리자 토폴로지를 선택 하면 보고서가 MBAM이 아닌 Configuration Manager에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="745fa-108">Configuration Manager에서 실행 되는 보고서에 대 한 자세한 내용은 [구성 관리자에서 MBAM 보고서 이해](understanding-mbam-reports-in-configuration-manager.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="745fa-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="745fa-109">보고서 이해</span><span class="sxs-lookup"><span data-stu-id="745fa-109">Understanding Reports</span></span>


<span data-ttu-id="745fa-110">Microsoft BitLocker 관리 및 모니터링의 보고서 기능에 액세스 하려면 웹 브라우저를 열고 관리 및 모니터링 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="745fa-111">왼쪽 메뉴 모음에서 **보고서** 를 선택한 다음 위쪽 메뉴 모음에서 선택 합니다. 생성 하려는 보고서 종류</span><span class="sxs-lookup"><span data-stu-id="745fa-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="745fa-112">엔터프라이즈 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="745fa-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="745fa-113">조직의 전반적인 BitLocker 준수에 대 한 정보를 수집 하려면이 보고서 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="745fa-114">여러 필터를 사용 하 여 검색 결과를 준수 상태 및 오류 상태로 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="745fa-115">보고서 정보는 6 시간 마다 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="745fa-116">엔터프라이즈 준수 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="745fa-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="745fa-117">열 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="745fa-118">설명</span><span class="sxs-lookup"><span data-stu-id="745fa-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-119">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-120">MBAM으로 관리 되는 사용자 지정 DNS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-121">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-122">클라이언트 컴퓨터가 상주 하 고 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-123">준수 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-124">컴퓨터에 대해 지정 된 정책에 따라 컴퓨터를 준수 하는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="745fa-125">상태는 비규격이 고 규격입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="745fa-126">준수 상태를 해석 하는 방법에 대 한 자세한 내용은 엔터프라이즈 준수 보고서 준수 상태 테이블을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="745fa-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-127">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="745fa-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-128">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-129">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="745fa-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-130">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="745fa-131">대화 상대 주파수를 구성할 수 있습니다 (MBAM 정책 설정 참조).</span><span class="sxs-lookup"><span data-stu-id="745fa-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="745fa-132">엔터프라이즈 준수 보고서 준수 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="745fa-133">준수 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="745fa-134">제외</span><span class="sxs-lookup"><span data-stu-id="745fa-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="745fa-135">설명</span><span class="sxs-lookup"><span data-stu-id="745fa-135">Description</span></span></th>
<th align="left"><span data-ttu-id="745fa-136">사용자 작업</span><span class="sxs-lookup"><span data-stu-id="745fa-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-137">맞지</span><span class="sxs-lookup"><span data-stu-id="745fa-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-138">예외 아님</span><span class="sxs-lookup"><span data-stu-id="745fa-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-139">지정 된 정책에 따라 컴퓨터가 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-140"><strong>컴퓨터 이름을 클릭 하 </strong> 고 각 드라이브의 상태가 지정 된 정책을 따르는지 확인 하 여 컴퓨터 준수 보고서 세부 정보를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="745fa-141">암호화 상태에 컴퓨터가 암호화 되지 않은 것으로 표시 되는 경우 암호화가 진행 중이거나 컴퓨터에 오류가 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="745fa-142">오류가 없는 경우에는 컴퓨터가 여전히 암호화 상태를 연결 하거나 설정 하는 과정에서 발생 하는 것일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="745fa-143">나중에 다시 확인 하 여 상태가 변경 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-144">기준</span><span class="sxs-lookup"><span data-stu-id="745fa-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-145">예외 아님</span><span class="sxs-lookup"><span data-stu-id="745fa-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-146">지정 된 정책에 따라 컴퓨터가 규격입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-147">작업이 필요 하지 않습니다. 컴퓨터의 상태는 컴퓨터 준수 보고서를 확인 하 여 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="745fa-148">컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="745fa-148">Computer Compliance Report</span></span>

<span data-ttu-id="745fa-149">컴퓨터 또는 사용자와 관련 된 정보를 수집 하려면이 보고서 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="745fa-150">이 보고서는 엔터프라이즈 준수 보고서에서 컴퓨터 이름을 클릭 하거나 컴퓨터 준수 보고서에 컴퓨터 이름을 입력 하 여 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="745fa-151">컴퓨터 준수 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 제공 하 고 컴퓨터의 각 드라이브 유형에 적용 되는 정책을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="745fa-152">각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="745fa-153">**참고**  이동식 데이터 볼륨 암호화 상태가 보고서에 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="745fa-154">컴퓨터 준수 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="745fa-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="745fa-155">열 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="745fa-156">설명</span><span class="sxs-lookup"><span data-stu-id="745fa-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-157">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-158">MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-159">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-160">클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-161">컴퓨터 종류</span><span class="sxs-lookup"><span data-stu-id="745fa-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-162">컴퓨터의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-162">Type of computer.</span></span> <span data-ttu-id="745fa-163">유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-164">운영 체제</span><span class="sxs-lookup"><span data-stu-id="745fa-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-165">MBAM 관리 클라이언트 컴퓨터에서 찾을 수 있는 운영 체제 유형.</span><span class="sxs-lookup"><span data-stu-id="745fa-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-166">준수 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-167">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="745fa-168">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="745fa-169">드라이브 (다음 표 참조)의 준수 상태가 서로 다른 준수 상태를 나타낼 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="745fa-170">그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-171">정책 암호화 수준</span><span class="sxs-lookup"><span data-stu-id="745fa-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-172">MBAM 정책 사양 중 관리자가 선택한 암호화 수준 (예: 128-디퓨저)</span><span class="sxs-lookup"><span data-stu-id="745fa-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-173">정책 운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="745fa-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-174">운영 체제에 암호화가 필요한 경우 적절 한 보호기 형식을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-175">정책 고정 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="745fa-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-176">고정 데이터 드라이브에 대해 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-177">정책 이동식 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="745fa-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-178">이동식 드라이브에 대 한 암호화가 필요한 경우에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-179">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="745fa-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-180">MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-181">제조업체</span><span class="sxs-lookup"><span data-stu-id="745fa-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-182">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-183">모델</span><span class="sxs-lookup"><span data-stu-id="745fa-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-184">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-185">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="745fa-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-186">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-187">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="745fa-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-188">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="745fa-189">대화 상대 주파수를 구성할 수 있습니다 (MBAM 정책 설정 참조).</span><span class="sxs-lookup"><span data-stu-id="745fa-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="745fa-190">컴퓨터 준수 보고서 드라이브 필드</span><span class="sxs-lookup"><span data-stu-id="745fa-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="745fa-191">열 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="745fa-192">설명</span><span class="sxs-lookup"><span data-stu-id="745fa-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-193">드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="745fa-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-194">사용자가 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="745fa-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-195">드라이브 종류</span><span class="sxs-lookup"><span data-stu-id="745fa-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-196">드라이브의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-196">Type of drive.</span></span> <span data-ttu-id="745fa-197">올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="745fa-198">이는 논리 볼륨이 아닌 실제 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-199">암호화 수준</span><span class="sxs-lookup"><span data-stu-id="745fa-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-200">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-201">보호 기능 유형</span><span class="sxs-lookup"><span data-stu-id="745fa-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-202">운영 체제 또는 고정 데이터 볼륨을 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-203">보호기 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-204">MBAM으로 관리 되는 컴퓨터가 정책에 지정 된 보호기 형식을 사용 하도록 설정 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="745fa-205">유효한 상태는 ON 또는 OFF입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-206">암호화 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-207">드라이브의 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-207">Encryption state of the drive.</span></span> <span data-ttu-id="745fa-208">유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-209">준수 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-210">드라이브가 정책에 따라 사용 되는지 여부를 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="745fa-211">상태는 비규격이 고 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-212">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="745fa-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-213">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="745fa-214">복구 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="745fa-214">Recovery Audit Report</span></span>

<span data-ttu-id="745fa-215">이 보고서 유형을 사용 하 여 복구 키에 대 한 액세스를 요청한 사용자를 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="745fa-216">보고서는 원하는 필터링 조건을 기준으로 여러 필터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="745fa-217">사용자는 지원 센터 사용자 또는 최종 사용자, 요청 실패 여부, 요청 된 특정 키 형식, 검색을 수행 하는 날짜 범위 등 특정 유형의 사용자를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="745fa-218">관리자는 필요에 따라 상황별 보고서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="745fa-219">복구 감사 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="745fa-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="745fa-220">열 이름</span><span class="sxs-lookup"><span data-stu-id="745fa-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="745fa-221">설명</span><span class="sxs-lookup"><span data-stu-id="745fa-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-222">날짜 및 시간 요청</span><span class="sxs-lookup"><span data-stu-id="745fa-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-223">최종 사용자 또는 지원 센터 사용자가 키 검색 요청을 수행한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-224">요청 상태</span><span class="sxs-lookup"><span data-stu-id="745fa-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-225">요청 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-225">Status of the request.</span></span> <span data-ttu-id="745fa-226">유효한 상태는 성공적 (키 검색 됨) 또는 실패 (키가 검색 되지 않음) 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-227">헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="745fa-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-228">키 검색 요청을 시작한 지원 센터 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="745fa-229">참고: 지원 센터 사용자가 최종 사용자에 게 해당 키를 대신 검색 하는 경우 최종 사용자 필드는 비어 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-230">사용자</span><span class="sxs-lookup"><span data-stu-id="745fa-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-231">키 검색 요청을 시작한 최종 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="745fa-232">키 유형</span><span class="sxs-lookup"><span data-stu-id="745fa-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-233">지원 센터 사용자 또는 최종 사용자가 요청한 키의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="745fa-234">MBAM에는 복구 키 암호 (복구 모드에서 컴퓨터를 복구 하는 데 사용 됨), 복구 키 ID (다른 사용자 대신 복구 모드에서 컴퓨터를 복구 하는 데 사용 됨), TPM 암호 해시 (tpm이 잠겨 있는 컴퓨터를 복구 하는 데 사용 됨) 등 세 가지 키 유형이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="745fa-235">이유 설명</span><span class="sxs-lookup"><span data-stu-id="745fa-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="745fa-236">지정 된 키 유형이 지원 센터 사용자 또는 최종 사용자에 의해 요청 된 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="745fa-237">이유는 관리 및 모니터링 웹 사이트의 TPM 및 복구 기능을 관리 하는 방법에 명시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="745fa-238">유효한 항목은 사용자가 입력 한 텍스트 이거나 다음 이유 코드 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="745fa-239">운영 체제 부팅 순서 변경 됨</span><span class="sxs-lookup"><span data-stu-id="745fa-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="745fa-240">BIOS 변경 됨</span><span class="sxs-lookup"><span data-stu-id="745fa-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="745fa-241">운영 체제 파일이 변경 됨</span><span class="sxs-lookup"><span data-stu-id="745fa-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="745fa-242">분실 한 시작 키</span><span class="sxs-lookup"><span data-stu-id="745fa-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="745fa-243">핀 분실</span><span class="sxs-lookup"><span data-stu-id="745fa-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="745fa-244">TPM 다시 설정</span><span class="sxs-lookup"><span data-stu-id="745fa-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="745fa-245">암호 손실</span><span class="sxs-lookup"><span data-stu-id="745fa-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="745fa-246">스마트 카드 분실</span><span class="sxs-lookup"><span data-stu-id="745fa-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="745fa-247">PIN 잠금 다시 설정</span><span class="sxs-lookup"><span data-stu-id="745fa-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="745fa-248">TPM 켜기</span><span class="sxs-lookup"><span data-stu-id="745fa-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="745fa-249">TPM 끄기</span><span class="sxs-lookup"><span data-stu-id="745fa-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="745fa-250">TPM 암호 변경</span><span class="sxs-lookup"><span data-stu-id="745fa-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="745fa-251">TPM 지우기</span><span class="sxs-lookup"><span data-stu-id="745fa-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="745fa-252">**참고**  보고서 메뉴 모음에서 **내보내기** 단추를 클릭 하 여 결과를 파일에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745fa-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="745fa-253">MBAM 보고서를 실행 하는 방법에 대 한 자세한 내용은 [Mbam 보고서를 생성 하는 방법을](how-to-generate-mbam-reports-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="745fa-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="745fa-254">관련 항목</span><span class="sxs-lookup"><span data-stu-id="745fa-254">Related topics</span></span>


[<span data-ttu-id="745fa-255">MBAM 2.0으로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="745fa-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





