---
title: MBAM 보고서 이해
description: MBAM 보고서 이해
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822868"
---
# <span data-ttu-id="cd74f-103">MBAM 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="cd74f-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="cd74f-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 사용 및 준수 모니터링을 위해 다양 한 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="cd74f-105">이 항목에서는 엔터프라이즈 준수, 개별 컴퓨터, 하드웨어 호환성 및 키 복구 활동에 대 한 MBAM 보고서에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="cd74f-106">보고서 이해</span><span class="sxs-lookup"><span data-stu-id="cd74f-106">Understanding Reports</span></span>


<span data-ttu-id="cd74f-107">MBAM의 보고서 기능에 액세스 하려면 MBAM 관리 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="cd74f-108">탐색 창에서 **보고서** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="cd74f-109">그런 다음 기본 콘텐츠 창에서 보고서 유형의 탭을 클릭 합니다. **엔터프라이즈 준수 보고서**, **컴퓨터 준수 보고서**, **하드웨어 감사 보고서**또는 **복구 감사**보고서.</span><span class="sxs-lookup"><span data-stu-id="cd74f-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="cd74f-110">엔터프라이즈 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="cd74f-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="cd74f-111">엔터프라이즈 준수 보고서는 조직의 전반적인 BitLocker 준수에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="cd74f-112">이 보고서에 사용할 수 있는 필터를 통해 준수 상태 및 오류 상태에 따라 검색 결과를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="cd74f-113">이 보고서는 6 시간 마다 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-113">This report runs every six hours.</span></span>

**<span data-ttu-id="cd74f-114">엔터프라이즈 준수 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="cd74f-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd74f-115">열 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="cd74f-116">설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-117">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-118">MBAM에서 관리 되는 사용자 지정 DNS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-119">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-120">클라이언트 컴퓨터가 상주 하 고 있으며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-121">준수 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-122">컴퓨터에 대해 지정 된 정책에 따라 컴퓨터에 대 한 규정 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="cd74f-123">사용할 수 있는 상태는 비규격이 고 준수입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="cd74f-124">자세한 내용은이 항목의 엔터프라이즈 준수 보고서 준수 상태를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd74f-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-125">제외</span><span class="sxs-lookup"><span data-stu-id="cd74f-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-126">하드웨어 종류 식별 및 컴퓨터가 정책에서 제외 되었는지 여부를 확인 하는 컴퓨터 하드웨어의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="cd74f-127">하드웨어는 알려지지 않음 (하드웨어 종류는 MBAM으로 식별 되지 않음), 하드웨어 예외 (하드웨어 종류는 확인 되었으며, MBAM 정책에서 제외 된 것으로 표시 됨), 예외 (하드웨어 식별 됨 및 정책에서 제외 되지 않음) 등 세 가지 상태일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-128">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="cd74f-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-129">MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-130">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cd74f-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-131">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-132">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="cd74f-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-133">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="cd74f-134">이 시간은 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-134">This time is configurable.</span></span> <span data-ttu-id="cd74f-135">MBAM 정책 설정을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd74f-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="cd74f-136">엔터프라이즈 준수 보고서 준수 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd74f-137">준수 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="cd74f-138">제외</span><span class="sxs-lookup"><span data-stu-id="cd74f-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="cd74f-139">설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-139">Description</span></span></th>
<th align="left"><span data-ttu-id="cd74f-140">사용자 작업</span><span class="sxs-lookup"><span data-stu-id="cd74f-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-141">맞지</span><span class="sxs-lookup"><span data-stu-id="cd74f-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-142">예외 아님</span><span class="sxs-lookup"><span data-stu-id="cd74f-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-143">컴퓨터가 지정 된 정책에 따라 비규격 이며 하드웨어 종류가 정책에서 제외로 표시 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-144">컴퓨터 <strong> 이름을 클릭 </strong> 하 여 컴퓨터 준수 보고서를 확장 하 고 각 드라이브의 상태가 지정 된 정책을 준수 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="cd74f-145">암호화 상태에 컴퓨터가 암호화 되지 않은 것으로 표시 되는 경우 암호화가 계속 진행 중이거나 컴퓨터에 오류가 있는 것일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="cd74f-146">오류가 없는 경우에는 컴퓨터가 여전히 암호화 상태를 연결 하거나 설정 하는 과정에서 발생 하는 것일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="cd74f-147">나중에 다시 확인 하 여 상태가 변경 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-148">기준</span><span class="sxs-lookup"><span data-stu-id="cd74f-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-149">예외 아님</span><span class="sxs-lookup"><span data-stu-id="cd74f-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-150">컴퓨터는 지정 된 정책에 따라 규격을 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-151">작업이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-151">No Action needed.</span></span> <span data-ttu-id="cd74f-152">필요에 따라 컴퓨터 준수 보고서를 보고 컴퓨터의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-153">기준</span><span class="sxs-lookup"><span data-stu-id="cd74f-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-154">하드웨어 예외</span><span class="sxs-lookup"><span data-stu-id="cd74f-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-155">하드웨어 종류가 면제 인 경우</span><span class="sxs-lookup"><span data-stu-id="cd74f-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="cd74f-156">정책이 설정 되는 방법과 각 하드 드라이브의 개별 상태에 관계 없이 전체 상태는 규격으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-157">작업이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-158">기준</span><span class="sxs-lookup"><span data-stu-id="cd74f-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-159">알 수 없는 하드웨어</span><span class="sxs-lookup"><span data-stu-id="cd74f-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-160">MBAM은 하드웨어 유형을 인식 하지만, MBAM은 예외 또는 예외 인지 여부를 알 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="cd74f-161">관리자가 하드웨어에 대해 호환 되는 상태를 설정 하지 않은 경우이 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="cd74f-162">따라서 MBAM은 기본적으로 규격 상태로 되돌려집니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-163">새로 배포 된 MBAM 클라이언트의 초기 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="cd74f-164">일반적으로 일시적인 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-164">It is typically only a transient state.</span></span> <span data-ttu-id="cd74f-165">관리자가 하드웨어를 호환 되는 것으로 표시 했더라도 클라이언트 컴퓨터가 다시 보고 되기 전에 상당한 지연 또는 구성 가능한 대기 시간이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="cd74f-166">마지막 대화 상대의 시간을 기록 하 고 지정 된 간격 후에 다시 체크 인 하 여 상태가 변경 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="cd74f-167">상태가 변경 되지 않은 경우이 컴퓨터 또는 하드웨어 종류에 오류가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="cd74f-168">컴퓨터 준수 보고서</span><span class="sxs-lookup"><span data-stu-id="cd74f-168">Computer Compliance Report</span></span>

<span data-ttu-id="cd74f-169">컴퓨터 준수 보고서에 컴퓨터 또는 사용자와 관련 된 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="cd74f-170">컴퓨터 준수 보고서는 운영 체제 드라이브 및 고정 데이터 드라이브를 포함 하 여 컴퓨터의 각 드라이브에 대 한 자세한 암호화 정보 및 적용 가능한 정책을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="cd74f-171">이 보고서 유형을 보려면 엔터프라이즈 준수 보고서에서 컴퓨터 이름을 클릭 하거나 컴퓨터 준수 보고서에 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="cd74f-172">각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="cd74f-173">**참고**  이 보고서는 이동식 데이터 볼륨에 대 한 암호화 상태를 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="cd74f-174">컴퓨터 준수 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="cd74f-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd74f-175">열 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="cd74f-176">설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-177">컴퓨터 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-178">MBAM에서 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-179">도메인 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-180">클라이언트 컴퓨터가 상주 하 고 있으며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-181">컴퓨터 종류</span><span class="sxs-lookup"><span data-stu-id="cd74f-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-182">컴퓨터의 이식성 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-182">The portability type of computer.</span></span> <span data-ttu-id="cd74f-183">유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-184">운영 체제</span><span class="sxs-lookup"><span data-stu-id="cd74f-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-185">MBAM 관리 클라이언트 컴퓨터에 설치 된 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-186">준수 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-187">MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="cd74f-188">유효한 상태는 규격 및 비규격입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="cd74f-189">동일한 컴퓨터에 규격 및 비규격 드라이브가 있을 수 있지만,이 필드에는 지정 된 정책에 따른 전반적인 컴퓨터 준수 여부가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-190">정책 Cypher 강도</span><span class="sxs-lookup"><span data-stu-id="cd74f-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-191">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="cd74f-192">예를 들어 128 비트에 디퓨저</span><span class="sxs-lookup"><span data-stu-id="cd74f-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-193">정책 운영 체제 드라이브</span><span class="sxs-lookup"><span data-stu-id="cd74f-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-194">해당 되는 경우 O/S 및 보호기 유형에 대해 암호화가 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-195">정책 고정 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="cd74f-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-196">고정 드라이브에 대해 암호화가 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-197">정책 이동식 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="cd74f-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-198">이동식 드라이브에 대해 암호화가 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-199">장치 사용자</span><span class="sxs-lookup"><span data-stu-id="cd74f-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-200">컴퓨터에서 알려진 사용자의 id를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-201">제외</span><span class="sxs-lookup"><span data-stu-id="cd74f-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-202">컴퓨터 하드웨어 유형이 MBAM에서 인식 되는지, 알려진 경우 컴퓨터가 정책에서 제외로 지정 되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="cd74f-203">하드웨어를 알 수 없음 (하드웨어 종류가 MBAM으로 식별 되지 않음) 이라는 세 가지 상태가 있습니다. 하드웨어 예외 (하드웨어 종류는 확인 되었으며, MBAM 정책에서 제외로 표시 됨), (하드웨어가 식별 되었으며 정책에서 제외 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="cd74f-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-204">제조업체</span><span class="sxs-lookup"><span data-stu-id="cd74f-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-205">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-206">모델</span><span class="sxs-lookup"><span data-stu-id="cd74f-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-207">컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-208">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cd74f-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-209">지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-210">마지막 연락처</span><span class="sxs-lookup"><span data-stu-id="cd74f-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-211">컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="cd74f-212">T</span><span class="sxs-lookup"><span data-stu-id="cd74f-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="cd74f-213">컴퓨터 준수 보고서 드라이브 필드</span><span class="sxs-lookup"><span data-stu-id="cd74f-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd74f-214">열 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="cd74f-215">설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-216">드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="cd74f-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-217">사용자가이 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</span><span class="sxs-lookup"><span data-stu-id="cd74f-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-218">드라이브 종류</span><span class="sxs-lookup"><span data-stu-id="cd74f-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-219">드라이브의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-219">Type of drive.</span></span> <span data-ttu-id="cd74f-220">올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="cd74f-221">이는 논리 볼륨이 아닌 실제 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-222">Cypher 힘</span><span class="sxs-lookup"><span data-stu-id="cd74f-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-223">MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-224">보호 기능 유형</span><span class="sxs-lookup"><span data-stu-id="cd74f-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-225">운영 체제 또는 고정 볼륨을 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="cd74f-226">운영 체제 드라이브의 유효한 보호기 유형은 TPM 또는 TPM + PIN입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="cd74f-227">고정 데이터 볼륨에 유효한 보호기 유형은 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-228">보호기 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-229">이 필드는 컴퓨터에서 정책에 지정 된 보호기 유형을 사용 하도록 설정 했는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="cd74f-230">유효한 상태는 ON 또는 OFF입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-231">암호화 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-232">드라이브의 현재 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="cd74f-233">유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-234">준수 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-235">드라이브가 정책에 따라 사용 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="cd74f-236">상태는 비규격이 고 준수 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-237">준수 상태 세부 정보</span><span class="sxs-lookup"><span data-stu-id="cd74f-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-238">컴퓨터의 준수 상태와 관련 된 오류 및 상태 메시지를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="cd74f-239">하드웨어 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="cd74f-239">Hardware Audit Report</span></span>

<span data-ttu-id="cd74f-240">이 보고서는 특정 컴퓨터의 하드웨어 호환성 상태와 모델에 대 한 변경 사항을 감사 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="cd74f-241">검색 결과의 범위를 좁히는 데 도움이 되도록이 보고서에는 변경 유형 및 발생 시간 등의 기준에 대 한 필터링이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="cd74f-242">각 상태 변경은 사용자 및 날짜 및 시간을 기준으로 추적 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="cd74f-243">하드웨어 종류는 클라이언트 컴퓨터에서 실행 되는 MBAM 에이전트에 의해 자동으로 채워집니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="cd74f-244">이 보고서는 MBAM 관리 컴퓨터에서 직접 수집한 정보에 대 한 사용자 변경을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="cd74f-245">일반적인 관리 변경 내용이 호환 되지 않는 것으로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="cd74f-246">그러나 관리자는 필드를 수정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="cd74f-247">하드웨어 감사 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="cd74f-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd74f-248">열 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="cd74f-249">설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-250">날짜 및 시간</span><span class="sxs-lookup"><span data-stu-id="cd74f-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-251">하드웨어 종류를 변경한 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="cd74f-252">모든 고유 하드웨어 종류에는 적어도 하나 이상의 항목이 할당 되어 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd74f-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-253">사용자</span><span class="sxs-lookup"><span data-stu-id="cd74f-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-254">특정 항목을 변경한 관리 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-255">유형 변경</span><span class="sxs-lookup"><span data-stu-id="cd74f-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-256">하드웨어 종류 정보에 대 한 변경 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="cd74f-257">유효한 값은 더하기 (새 항목), 업데이트 (기존 항목 변경) 또는 삭제 (기존 항목 제거)입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-258">원래 값</span><span class="sxs-lookup"><span data-stu-id="cd74f-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-259">변경 전의 하드웨어 종류 사양 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-260">현재 값</span><span class="sxs-lookup"><span data-stu-id="cd74f-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-261">변경이 이루어진 후의 하드웨어 종류 사양 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="cd74f-262">복구 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="cd74f-262">Recovery Audit Report</span></span>

<span data-ttu-id="cd74f-263">복구 감사 보고서는 복구 키에 대 한 액세스를 요청한 사용자를 감사 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="cd74f-264">이 보고서에 대 한 필터 조건에는 요청을 수행 하는 사용자 유형, 요청 된 키 유형, 성공 또는 실패, 발생 시간, 사용자 요청 (지원 센터, 최종 사용자)의 유형 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="cd74f-265">이 보고서를 통해 관리자는 필요에 따라 상황별 보고서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="cd74f-266">복구 감사 보고서 필드</span><span class="sxs-lookup"><span data-stu-id="cd74f-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd74f-267">열 이름</span><span class="sxs-lookup"><span data-stu-id="cd74f-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="cd74f-268">설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-269">날짜 및 시간 요청</span><span class="sxs-lookup"><span data-stu-id="cd74f-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-270">최종 사용자 또는 지원 센터 사용자가 키 검색 요청을 수행한 날짜와 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-271">요청 상태</span><span class="sxs-lookup"><span data-stu-id="cd74f-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-272">요청 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-272">Status of the request.</span></span> <span data-ttu-id="cd74f-273">유효한 상태는 성공적 (키 검색 됨) 또는 실패 (키가 검색 되지 않음) 중 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-274">헬프데스크 사용자</span><span class="sxs-lookup"><span data-stu-id="cd74f-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-275">키 검색 요청을 시작한 지원 센터 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="cd74f-276">지원 센터 사용자가 최종 사용자를 대신 하 여 키를 검색 하는 경우 최종 사용자 필드는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-277">사용자</span><span class="sxs-lookup"><span data-stu-id="cd74f-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-278">키 검색 요청을 시작한 최종 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd74f-279">키 유형</span><span class="sxs-lookup"><span data-stu-id="cd74f-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-280">요청 된 키의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-280">The type of key that was requested.</span></span> <span data-ttu-id="cd74f-281">MBAM은 복구 키 암호 (복구 모드에서 컴퓨터 복구) 라는 세 가지 키 유형을 수집 합니다. 복구 키 ID (다른 사용자 대신 복구 모드로 컴퓨터를 복구 하는 경우) TPM (신뢰할 수 있는 플랫폼 모듈) 암호 해시 (TPM이 잠겨 있는 컴퓨터를 복구 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="cd74f-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd74f-282">이유 설명</span><span class="sxs-lookup"><span data-stu-id="cd74f-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd74f-283">지정 된 키 형식을 요청한 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="cd74f-284">이유는 관리 웹 사이트의 TPM (드라이브 복구) 및 TPM 관리 기능에 명시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="cd74f-285">유효한 항목에는 사용자가 입력 한 텍스트 또는 다음 이유 코드 중 하나가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="cd74f-286">운영 체제 부팅 순서 변경 됨</span><span class="sxs-lookup"><span data-stu-id="cd74f-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="cd74f-287">BIOS 변경 됨</span><span class="sxs-lookup"><span data-stu-id="cd74f-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="cd74f-288">운영 체제 파일이 변경 됨</span><span class="sxs-lookup"><span data-stu-id="cd74f-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="cd74f-289">분실 한 시작 키</span><span class="sxs-lookup"><span data-stu-id="cd74f-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="cd74f-290">핀 분실</span><span class="sxs-lookup"><span data-stu-id="cd74f-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="cd74f-291">TPM 다시 설정</span><span class="sxs-lookup"><span data-stu-id="cd74f-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="cd74f-292">암호 손실</span><span class="sxs-lookup"><span data-stu-id="cd74f-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="cd74f-293">스마트 카드 분실</span><span class="sxs-lookup"><span data-stu-id="cd74f-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="cd74f-294">PIN 잠금 다시 설정</span><span class="sxs-lookup"><span data-stu-id="cd74f-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="cd74f-295">TPM 켜기</span><span class="sxs-lookup"><span data-stu-id="cd74f-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="cd74f-296">TPM 끄기</span><span class="sxs-lookup"><span data-stu-id="cd74f-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="cd74f-297">TPM 암호 변경</span><span class="sxs-lookup"><span data-stu-id="cd74f-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="cd74f-298">TPM 지우기</span><span class="sxs-lookup"><span data-stu-id="cd74f-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cd74f-299">**참고**  보고서 결과를 파일에 저장 하려면 보고서 메뉴 모음에서 **내보내기** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd74f-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="cd74f-300">관련 항목</span><span class="sxs-lookup"><span data-stu-id="cd74f-300">Related topics</span></span>


[<span data-ttu-id="cd74f-301">MBAM 1.0으로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="cd74f-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





