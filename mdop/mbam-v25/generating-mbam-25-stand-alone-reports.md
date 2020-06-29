---
title: MBAM 2.5 독립 실행형 보고서 생성
description: MBAM 2.5 독립 실행형 보고서 생성
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823123"
---
# <span data-ttu-id="a2de4-103">MBAM 2.5 독립 실행형 보고서 생성</span><span class="sxs-lookup"><span data-stu-id="a2de4-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="a2de4-104">독립 실행형 토폴로지로 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 구성할 때 BitLocker 드라이브 암호화 사용 및 준수를 모니터링 하는 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="a2de4-105">이 항목에서는 다음 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="a2de4-106">관리 및 모니터링 웹 사이트를 열려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="a2de4-107">엔터프라이즈 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="a2de4-108">컴퓨터 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="a2de4-109">복구 키 감사 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="a2de4-110">독립 실행형 보고서에 대 한 설명은 [MBAM 2.5 독립 실행형 보고서 이해](understanding-mbam-25-stand-alone-reports.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2de4-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="a2de4-111">**참고**  보고서를 실행 하려면 Active Directory 도메인 서비스에서 구성한 **Mbam 보고서 사용자** 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="a2de4-112">자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2de4-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="a2de4-113">관리 및 모니터링 웹 사이트를 열려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="a2de4-114">웹 브라우저를 열고 관리 및 모니터링 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="a2de4-115">관리 및 모니터링 웹 사이트의 기본 URL은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="a2de4-116">http (s)// &lt; MBAMAdministrationServerName &gt; : &lt; 포트 &gt; /helpdesk</span><span class="sxs-lookup"><span data-stu-id="a2de4-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="a2de4-117">왼쪽 창에서 **보고서**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="a2de4-118">위쪽 메뉴 모음에서 실행할 보고서를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="a2de4-119">MBAM 클라이언트 데이터는 컴퓨터를 분실 하거나 도난당 한 경우 기록 참조에 대 한 준수 및 감사 데이터베이스에 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="a2de4-120">Enterprise 보고서를 실행할 때 적절 한 시작 및 종료 날짜를 사용 하 여 보고서 데이터의 정확성을 높이기 위해 1 ~ 2 주 동안 보고 하는 시간 프레임의 범위를 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="a2de4-121">보고서를 생성 한 후에는 HTML, Microsoft Word, Microsoft Excel 등의 다양 한 형식으로 결과를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="a2de4-122">**참고**  관리 및 모니터링 웹 사이트를 구성 하기 전에 SSL (Secure Sockets layer)을 사용 하도록 SSRS (SQL Server Reporting Services)를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="a2de4-123">어떤 이유로 든 지 SSRS가 SSL을 사용 하도록 구성 되어 있지 않은 경우, 관리 및 모니터링 웹 사이트를 구성할 때 보고서의 URL이 HTTPS 대신 HTTP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="a2de4-124">그런 다음 관리 및 모니터링 웹 사이트로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="a2de4-125">보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="a2de4-126">엔터프라이즈 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="a2de4-127">관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택 하 고 **엔터프라이즈 준수 보고서**를 선택한 다음 사용할 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="a2de4-128">엔터프라이즈 준수 보고서에 사용할 수 있는 필터는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="a2de4-129">**준수 상태**.</span><span class="sxs-lookup"><span data-stu-id="a2de4-129">**Compliance Status**.</span></span> <span data-ttu-id="a2de4-130">이 필터를 사용 하 여 보고서의 준수 상태 유형을 지정 합니다 (예: 규격 또는 비규격).</span><span class="sxs-lookup"><span data-stu-id="a2de4-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="a2de4-131">**오류 상태**입니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-131">**Error State**.</span></span> <span data-ttu-id="a2de4-132">이 필터를 사용 하 여 보고서의 오류 상태 유형을 지정 합니다 (예: 오류 또는 오류 없음).</span><span class="sxs-lookup"><span data-stu-id="a2de4-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="a2de4-133">**보고서 보기** 를 클릭 하 여 선택한 보고서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="a2de4-134">컴퓨터 이름을 선택 하 여 컴퓨터 준수 보고서에 컴퓨터에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="a2de4-135">컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="a2de4-136">컴퓨터 준수 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="a2de4-137">관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택한 다음 **컴퓨터 준수 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="a2de4-138">컴퓨터 준수 보고서를 사용 하 여 **사용자 이름** 또는 **컴퓨터 이름을**검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="a2de4-139">**보고서 보기** 를 클릭 하 여 컴퓨터 준수 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="a2de4-140">컴퓨터 이름을 선택 하 여 컴퓨터 준수 보고서에 컴퓨터에 대 한 추가 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="a2de4-141">컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="a2de4-142">**참고**  컴퓨터가 MBAM 그룹 정책 설정의 요구 사항을 충족 하거나 초과 하는 경우 MBAM 클라이언트 컴퓨터는 규격으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="a2de4-143">복구 키 감사 보고서를 생성 하려면</span><span class="sxs-lookup"><span data-stu-id="a2de4-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="a2de4-144">관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택한 다음 **복구 감사 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="a2de4-145">복구 키 감사 보고서에 대 한 필터를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="a2de4-146">복구 키 감사에 사용할 수 있는 필터는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="a2de4-147">**헬프데스크 사용자**.</span><span class="sxs-lookup"><span data-stu-id="a2de4-147">**Helpdesk User**.</span></span> <span data-ttu-id="a2de4-148">이 필터는 사용자가 요청자의 사용자 이름을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="a2de4-149">요청자는 최종 사용자를 대신 하 여 키에 액세스 한 지원 센터의 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="a2de4-150">**최종 사용자**.</span><span class="sxs-lookup"><span data-stu-id="a2de4-150">**End User**.</span></span> <span data-ttu-id="a2de4-151">이 필터는 사용자가 requestee의 사용자 이름을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="a2de4-152">Requestee는 지원 센터를 호출 하 여 복구 키를 획득 하는 최종 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="a2de4-153">**요청 결과**.</span><span class="sxs-lookup"><span data-stu-id="a2de4-153">**Request Result**.</span></span> <span data-ttu-id="a2de4-154">이 필터는 사용자가 보고서의 기반으로 사용할 요청 결과 형식 (예: 성공 또는 실패)을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="a2de4-155">예를 들어 사용자가 실패 한 키 액세스 시도를 보려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="a2de4-156">**키 유형**입니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-156">**Key Type**.</span></span> <span data-ttu-id="a2de4-157">이 필터는 사용자가 보고서의 기반으로 사용할 키 유형 (예: 복구 키 암호 또는 TPM 암호 해시)을 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="a2de4-158">**시작 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-158">**Start Date**.</span></span> <span data-ttu-id="a2de4-159">이 필터는 사용자가 보고 하려는 날짜 범위의 시작 날짜 부분을 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="a2de4-160">**종료 날짜**입니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-160">**End Date**.</span></span> <span data-ttu-id="a2de4-161">이 필터는 사용자가 보고 하려는 날짜 범위의 끝 날짜 부분을 정의 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="a2de4-162">보고서 **보기** 를 클릭 하 여 보고서를 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="a2de4-163">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a2de4-163">Related topics</span></span>


[<span data-ttu-id="a2de4-164">MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고</span><span class="sxs-lookup"><span data-stu-id="a2de4-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="a2de4-165">MBAM 2.5 독립 실행형 보고서 이해</span><span class="sxs-lookup"><span data-stu-id="a2de4-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="a2de4-166">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="a2de4-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a2de4-167">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a2de4-168">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2de4-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





