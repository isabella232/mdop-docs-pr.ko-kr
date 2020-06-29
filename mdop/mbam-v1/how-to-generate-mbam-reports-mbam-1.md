---
title: MBAM 보고서를 생성하는 방법
description: MBAM 보고서를 생성하는 방법
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824528"
---
# <span data-ttu-id="0d939-103">MBAM 보고서를 생성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0d939-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="0d939-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 암호화 사용 및 준수 모니터링을 위한 다양 한 보고서를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="0d939-105">이 항목에서는 MBAM 관리 웹 사이트를 여는 방법과 엔터프라이즈 준수, 개별 컴퓨터, 하드웨어 호환성 및 키 복구 활동에 대해 MBAM 보고서를 생성 하는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="0d939-106">MBAM 보고서에 대 한 자세한 내용은 [MBAM 보고서 이해](understanding-mbam-reports-mbam-1.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d939-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="0d939-107">**참고**  보고서를 실행 하려면 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 준수 및 감사 보고서를 설치한 컴퓨터의 **사용자 역할 보고서** 의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="0d939-108">MBAM 관리 웹 사이트를 열려면</span><span class="sxs-lookup"><span data-stu-id="0d939-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="0d939-109">웹 브라우저를 열고 MBAM 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="0d939-110">웹 사이트의 기본 URL은 Microsoft BitLocker 관리 및 모니터링 서버의 \*http:// &lt; computername &gt; \* 입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="0d939-111">**참고**  MBAMadministration 웹 사이트가 포트 80 이외의 포트에 설치 되어 있는 경우 URL에서 해당 포트 번호를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="0d939-112">예를 들어 \*http:// &lt; computername &gt; : &lt; port &gt; \*입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="0d939-113">설치 중에 MBAMadministration 웹 사이트의 호스트 이름을 지정한 경우 URL이 \*http:// &lt; hostname &gt; \*입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="0d939-114">탐색 창에서 **보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="0d939-115">기본 창에서 보고서 유형의 탭을 클릭 합니다. **엔터프라이즈 준수 보고서**, **컴퓨터 준수 보고서**, **하드웨어 감사 보고서**또는 **복구 감사**보고서.</span><span class="sxs-lookup"><span data-stu-id="0d939-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="0d939-116">**참고**  기록 MBAM 클라이언트 데이터는 준수 데이터베이스에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="0d939-117">이 보존 된 데이터는 컴퓨터를 분실 하거나 도난당 하는 경우에 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="0d939-118">Enterprise 보고서를 실행할 때는 적절 한 시작 및 종료 날짜를 사용 하 여 보고서 데이터의 정확성을 높이는 데 1 ~ 2 주에 해당 하는 시간 프레임의 범위를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="0d939-119">엔터프라이즈 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="0d939-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="0d939-120">MBAMadministration 웹 사이트의 탐색 창에서 **보고서** 를 클릭 한 다음 **엔터프라이즈 준수 보고서** 탭을 클릭 하 고 보고서에 대 한 적절 한 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="0d939-121">엔터프라이즈 준수 보고서의 경우 다음 필터를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="0d939-122">**준수 상태**.</span><span class="sxs-lookup"><span data-stu-id="0d939-122">**Compliance Status**.</span></span> <span data-ttu-id="0d939-123">이 필터를 사용 하 여 준수 상태 형식 (예: 규격 또는 비규격)을 보고서에 포함할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="0d939-124">**오류 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-124">**Error State**.</span></span> <span data-ttu-id="0d939-125">이 필터를 사용 하 여 오류 또는 오류 등의 오류 상태 유형을 보고서에 포함할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="0d939-126">**보고서 보기** 를 클릭 하 여 지정 된 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="0d939-127">보고서 결과는 HTML, Microsoft Word, Microsoft Excel 등 사용 가능한 다양 한 파일 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="0d939-128">**참고**  6 시간 마다 실행 되는 SQL 작업으로 엔터프라이즈 준수 보고서가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="0d939-129">따라서 처음으로 보고서를 보려고 할 때 일부 데이터가 누락 된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="0d939-130">컴퓨터 호환성 보고서에서 컴퓨터에 대 한 정보를 보려면 컴퓨터 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="0d939-131">컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="0d939-132">컴퓨터 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="0d939-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="0d939-133">MBAMadministration 웹 사이트의 탐색 창에서 **보고서** 노드를 선택한 다음 **컴퓨터 준수 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="0d939-134">컴퓨터 준수 보고서를 사용 하 여 **사용자 이름** 또는 **컴퓨터 이름을**검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="0d939-135">**보고서 보기** 를 클릭 하 여 컴퓨터 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="0d939-136">결과는 HTML, Microsoft Word, Microsoft Excel 등 사용 가능한 다양 한 파일 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="0d939-137">컴퓨터에 대 한 자세한 정보를 표시 하는 방법 보고서를 보려면 컴퓨터 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="0d939-138">컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="0d939-139">**참고**  컴퓨터가 MBAM 정책 설정의 요구 사항과 일치 하거나 컴퓨터의 하드웨어 모델이 호환 되지 않는 것으로 설정 된 경우 MBAM 클라이언트 컴퓨터는 호환 되는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="0d939-140">따라서 컴퓨터와 연결 된 디스크 볼륨에 대 한 자세한 정보를 보고 있는 경우 하드웨어 호환성으로 인해 BitLocker 암호화에서 제외 되는 컴퓨터는 해당 드라이브 볼륨 암호화 상태가 비규격으로 표시 되기는 하지만 규격으로 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="0d939-141">하드웨어 호환성 감사 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="0d939-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="0d939-142">MBAMadministration 웹 사이트의 탐색 창에서 **보고서** 노드를 선택한 다음 **하드웨어 감사 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="0d939-143">하드웨어 감사 보고서에 대 한 적절 한 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="0d939-144">하드웨어 감사 보고서는 다음 사용 가능한 필터를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="0d939-145">**사용자 (Domain\\User)**.</span><span class="sxs-lookup"><span data-stu-id="0d939-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="0d939-146">변경 내용을 적용 한 사용자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="0d939-147">**변경 형식**.</span><span class="sxs-lookup"><span data-stu-id="0d939-147">**Change Type**.</span></span> <span data-ttu-id="0d939-148">찾으려는 변경 내용의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="0d939-149">**시작 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-149">**Start Date**.</span></span> <span data-ttu-id="0d939-150">보고 하려는 날짜 범위의 시작 날짜 부분을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="0d939-151">**종료 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-151">**End Date**.</span></span> <span data-ttu-id="0d939-152">보고 하려는 날짜 범위의 끝 날짜 부분을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="0d939-153">보고서 **보기** 를 클릭 하 여 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="0d939-154">결과는 HTML, Microsoft Word, Microsoft Excel 등 사용 가능한 다양 한 파일 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="0d939-155">복구 키 감사 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="0d939-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="0d939-156">MBAMadministration 웹 사이트의 탐색 창에서 **보고서** 노드를 선택한 다음 **복구 감사 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="0d939-157">복구 키 감사 보고서에 대 한 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="0d939-158">복구 키 감사에 사용할 수 있는 필터는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="0d939-159">**요청자**.</span><span class="sxs-lookup"><span data-stu-id="0d939-159">**Requestor**.</span></span> <span data-ttu-id="0d939-160">요청자의 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="0d939-161">요청자는 사용자를 대신 하 여 키에 액세스 한 헬프 데스크의 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="0d939-162">**Requestee**.</span><span class="sxs-lookup"><span data-stu-id="0d939-162">**Requestee**.</span></span> <span data-ttu-id="0d939-163">Requestee의 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="0d939-164">Requestee는 지원 센터를 호출 하 여 복구 키를 획득 하는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="0d939-165">**요청 결과** 성공 또는 실패와 같은 요청 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="0d939-166">예를 들어 실패 한 키 액세스 시도를 보려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="0d939-167">**키 유형**입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-167">**Key Type**.</span></span> <span data-ttu-id="0d939-168">복구 키 암호 또는 TPM 암호 해시와 같은 키 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="0d939-169">**시작 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-169">**Start Date**.</span></span> <span data-ttu-id="0d939-170">날짜 범위의 시작 날짜 부분을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="0d939-171">**종료 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-171">**End Date**.</span></span> <span data-ttu-id="0d939-172">날짜 범위의 끝 날짜 부분을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="0d939-173">보고서 **보기** 를 클릭 하 여 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="0d939-174">결과는 HTML, Microsoft Word, Microsoft Excel 등 사용 가능한 다양 한 파일 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d939-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="0d939-175">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0d939-175">Related topics</span></span>


[<span data-ttu-id="0d939-176">MBAM 1.0으로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="0d939-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





