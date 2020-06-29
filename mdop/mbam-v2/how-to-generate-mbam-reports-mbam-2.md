---
title: MBAM 보고서를 생성하는 방법
description: MBAM 보고서를 생성하는 방법
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824093"
---
# <span data-ttu-id="6ac3a-103">MBAM 보고서를 생성하는 방법</span><span class="sxs-lookup"><span data-stu-id="6ac3a-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="6ac3a-104">독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치할 때 BitLocker 암호화 사용 및 준수를 모니터링 하는 다른 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="6ac3a-105">이 항목의 절차에서는 관리 및 모니터링 웹 사이트를 여는 방법과 엔터프라이즈 준수, 개별 컴퓨터 및 키 복구 작업에서 Microsoft BitLocker 관리 및 모니터링 보고서를 생성 하는 데 필요한 단계에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="6ac3a-106">MBAM 보고서를 이해 하는 데 도움이 되는 자세한 내용은 [MBAM 보고서 이해](understanding-mbam-reports-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="6ac3a-107">**참고**  보고서를 실행 하려면 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 준수 및 감사 보고서가 설치 되어 있는 컴퓨터에서 **사용자 역할 보고서** 의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="6ac3a-108">관리 및 모니터링 웹 사이트를 열려면</span><span class="sxs-lookup"><span data-stu-id="6ac3a-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="6ac3a-109">웹 브라우저를 열고 관리 및 모니터링 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="6ac3a-110">관리 및 모니터링 웹 사이트의 기본 URL은 \*http:// &lt; computername &gt; \*입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="6ac3a-111">**참고**  관리 및 모니터링 웹 사이트가 80 이외의 포트에 설치 되어 있는 경우 URL에서 포트를 지정 해야 합니다 (예를 들어, \*http:// &lt; computername &gt; : &lt; port &gt; \*).</span><span class="sxs-lookup"><span data-stu-id="6ac3a-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="6ac3a-112">설치 중에 관리 및 모니터링 웹 사이트의 호스트 이름을 지정한 경우 URL이 \*http:// &lt; hostname &gt; \*입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="6ac3a-113">왼쪽 창에서 **보고서** 를 클릭 한 다음 위쪽 메뉴 모음에서 실행 하려는 보고서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="6ac3a-114">컴퓨터를 분실 하거나 도난당 한 경우 기록 참조에 대 한 정책 준수 데이터베이스에 기록 MBAM 클라이언트 데이터가 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="6ac3a-115">Enterprise 보고서를 실행할 때 적절 한 시작 및 종료 날짜를 사용 하 여 보고서 데이터의 정확성을 높이기 위해 1 ~ 2 주 동안 보고 하는 시간 프레임의 범위를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="6ac3a-116">**참고**  보안 소켓 계층을 사용 하도록 SSRS를 구성 하지 않은 경우, MBAM 서버를 설치할 때 보고서에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="6ac3a-117">그런 다음 지원 센터 포털로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="6ac3a-118">보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="6ac3a-119">엔터프라이즈 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="6ac3a-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="6ac3a-120">관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택 하 고 **엔터프라이즈 준수 보고서**를 선택한 다음 사용할 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="6ac3a-121">엔터프라이즈 준수 보고서에 사용할 수 있는 필터는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="6ac3a-122">**준수 상태**.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-122">**Compliance Status**.</span></span> <span data-ttu-id="6ac3a-123">이 필터를 사용 하 여 보고서의 준수 상태 유형 (예: 규격 또는 비규격)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="6ac3a-124">**오류 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-124">**Error State**.</span></span> <span data-ttu-id="6ac3a-125">이 필터를 사용 하 여 보고서의 오류 상태 유형 (예: 오류 또는 오류)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="6ac3a-126">**보고서 보기** 를 클릭 하 여 선택한 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="6ac3a-127">결과는 HTML, Microsoft Word, Microsoft Excel 등의 다양 한 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="6ac3a-128">**참고**  6 시간 마다 실행 되는 SQL 작업으로 엔터프라이즈 준수 보고서가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="6ac3a-129">따라서 보고서를 처음으로 볼 때 일부 데이터가 누락 된 것을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="6ac3a-130">SQL Management Studio를 사용 하 여 업데이트 된 보고서 데이터를 수동으로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="6ac3a-131">**개체 탐색기** 창에서 **SQL Server 에이전트**, **작업**을 차례로 확장 하 고 **CreateCache** 작업을 마우스 오른쪽 단추로 클릭 한 다음 **단계에서 작업 시작** ...을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="6ac3a-132">컴퓨터 이름을 선택 하 여 컴퓨터 준수 보고서에 컴퓨터에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="6ac3a-133">컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="6ac3a-134">컴퓨터 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="6ac3a-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="6ac3a-135">관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택한 다음 **컴퓨터 준수 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="6ac3a-136">컴퓨터 준수 보고서를 사용 하 여 **사용자 이름** 또는 **컴퓨터 이름을**검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="6ac3a-137">**보고서 보기** 를 클릭 하 여 컴퓨터 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="6ac3a-138">결과는 HTML, Microsoft Word, Microsoft Excel 등의 다양 한 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="6ac3a-139">컴퓨터 이름을 선택 하 여 컴퓨터 준수 보고서에 컴퓨터에 대 한 추가 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="6ac3a-140">컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="6ac3a-141">**참고**  컴퓨터가 MBAM 정책 설정의 요구 사항과 일치 하는 경우 MBAM 클라이언트 컴퓨터는 호환 되는 것으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="6ac3a-142">복구 키 감사 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="6ac3a-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="6ac3a-143">관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택한 다음 **복구 감사 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="6ac3a-144">복구 키 감사 보고서에 대 한 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="6ac3a-145">복구 키 감사에 사용할 수 있는 필터는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="6ac3a-146">**요청자**.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-146">**Requestor**.</span></span> <span data-ttu-id="6ac3a-147">이 필터는 사용자가 요청자의 사용자 이름을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="6ac3a-148">요청자는 사용자를 대신 하 여 키에 액세스 한 헬프 데스크의 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="6ac3a-149">**Requestee**.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-149">**Requestee**.</span></span> <span data-ttu-id="6ac3a-150">이 필터는 사용자가 requestee의 사용자 이름을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="6ac3a-151">Requestee는 지원 센터를 호출 하 여 복구 키를 획득 하는 사람입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="6ac3a-152">**요청 결과**.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-152">**Request Result**.</span></span> <span data-ttu-id="6ac3a-153">이 필터는 사용자가 보고서의 기반으로 사용할 요청 결과 형식 (예: 성공 또는 실패)을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="6ac3a-154">예를 들어 사용자가 실패 한 키 액세스 시도를 보려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="6ac3a-155">**키 유형**입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-155">**Key Type**.</span></span> <span data-ttu-id="6ac3a-156">이 필터는 사용자가 보고서의 기반으로 사용할 키 유형 (예: 복구 키 암호 또는 TPM 암호 해시)을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="6ac3a-157">**시작 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-157">**Start Date**.</span></span> <span data-ttu-id="6ac3a-158">이 필터는 사용자가 보고 하려는 날짜 범위의 시작 날짜 부분을 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="6ac3a-159">**종료 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-159">**End Date**.</span></span> <span data-ttu-id="6ac3a-160">이 필터는 사용자가 보고 하려는 날짜 범위의 끝 날짜 부분을 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="6ac3a-161">보고서 **보기** 를 클릭 하 여 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="6ac3a-162">결과는 HTML, Microsoft Word, Microsoft Excel 등의 다양 한 형식으로 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ac3a-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="6ac3a-163">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6ac3a-163">Related topics</span></span>


[<span data-ttu-id="6ac3a-164">MBAM 2.0으로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="6ac3a-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





