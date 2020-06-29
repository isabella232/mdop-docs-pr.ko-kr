---
title: App-V 5.0 보고 정보
description: App-V 5.0 보고 정보
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815023"
---
# <span data-ttu-id="6c618-103">App-V 5.0 보고 정보</span><span class="sxs-lookup"><span data-stu-id="6c618-103">About App-V 5.0 Reporting</span></span>


<span data-ttu-id="6c618-104">Microsoft App-v (Application Virtualization) 5.0에는 App-v 5.0 클라이언트를 실행 하는 컴퓨터와 가상 응용 프로그램 패키지 사용에 대 한 정보를 수집 하는 데 도움이 되는 기본 제공 보고 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-104">Microsoft Application Virtualization (App-V) 5.0 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.0 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="6c618-105">이 정보를 사용 하 여 중앙 집중화 된 데이터베이스에서 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-0-reporting-overview"></a> <span data-ttu-id="6c618-106">앱-V 5.0 보고 개요</span><span class="sxs-lookup"><span data-stu-id="6c618-106">App-V 5.0 Reporting Overview</span></span>


<span data-ttu-id="6c618-107">다음 목록에는 App-v 5.0에서 보고에 대 한 종단 간 상위 수준 워크플로가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.0.</span></span>

1.  <span data-ttu-id="6c618-108">Microsoft App-v (Application Virtualization) 5.0 보고 서버에는 다음과 같은 전제 조건이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-108">The Microsoft Application Virtualization (App-V) 5.0 Reporting server has the following prerequisites:</span></span>

    -   <span data-ttu-id="6c618-109">IIS (인터넷 정보 서비스) 웹 서버 역할</span><span class="sxs-lookup"><span data-stu-id="6c618-109">Internet Information Service (IIS) web server role</span></span>

    -   <span data-ttu-id="6c618-110">Windows 인증 역할 ( **IIS/보안**)</span><span class="sxs-lookup"><span data-stu-id="6c618-110">Windows Authentication role (under **IIS / Security**)</span></span>

    -   <span data-ttu-id="6c618-111">Sql Server가 SSRS (SQL Server Reporting Services)로 설치 및 실행 되는 경우</span><span class="sxs-lookup"><span data-stu-id="6c618-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="6c618-112">SQL Server Reporting Services가 실행 중인지 확인 하려면 `http://localhost/Reports` 웹 브라우저에서 app-v 5.0 Reporting을 호스팅할 서버의 관리자로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.0 Reporting.</span></span> <span data-ttu-id="6c618-113">SQL Server Reporting Services 홈 페이지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-113">The SQL Server Reporting Services Home page should display.</span></span>

2.  <span data-ttu-id="6c618-114">App-v 5.0 reporting server 및 연결 된 데이터베이스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-114">Install the App-V 5.0 reporting server and associated database.</span></span> <span data-ttu-id="6c618-115">보고 서버를 설치 하는 방법에 대 한 자세한 내용은 [독립 실행형 컴퓨터에 보고 서버를 설치 하 고 데이터베이스에 연결 하는 방법을](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md).</span></span> <span data-ttu-id="6c618-116">App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 보고 서버로 데이터를 보내야 하는 시간을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-116">Configure the time when the computer running the App-V 5.0 client should send data to the reporting server.</span></span>

3.  <span data-ttu-id="6c618-117">구성 관리자와 같은 전자 소프트웨어 배포 시스템을 사용 하 여 보고서를 보려면 SQL Server Reporting Service에서 보고서를 정의 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="6c618-118">의 다운로드 센터에서 미리 정의 된 appvshort 보고서를 다운로드 <https://go.microsoft.com/fwlink/?LinkId=397255> 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-118">Download predefined appvshort Reports from the Download Center at <https://go.microsoft.com/fwlink/?LinkId=397255>.</span></span>

    <span data-ttu-id="6c618-119">**참고**  앱-V 5.0와 함께 구성 관리자 통합을 사용 하는 경우 대부분의 보고서가 App-v 5.0이 아닌 구성 관리자에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-119">**Note** If you are using the Configuration Manager integration with App-V 5.0, most reports are generated from Configuration Manager rather than from App-V 5.0.</span></span>

     

4.  <span data-ttu-id="6c618-120">관리자로 사용 하 여 App-v 5.0 PowerShell 모듈을 가져온 후 `Import-Module AppvClient` app-v 5.0 클라이언트를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-120">After importing the App-V 5.0 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.0 client.</span></span> <span data-ttu-id="6c618-121">이 샘플 PowerShell cmdlet은 App-v 5.0 보고 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-121">This sample PowerShell cmdlet enables App-V 5.0 reporting:</span></span>

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="6c618-122">앱-V 5.0 보고서 데이터를 즉시 보내려면 `Send-AppvClientReport` app-v 5.0 클라이언트에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-122">To immediately send App-V 5.0 report data, run `Send-AppvClientReport` on the App-V 5.0 client.</span></span>

    <span data-ttu-id="6c618-123">보고 사용으로 App-v 5.0 클라이언트를 설치 하는 방법에 대 한 자세한 내용은 [클라이언트 구성 설정 정보](about-client-configuration-settings.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-123">For more information about installing the App-V 5.0 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span> <span data-ttu-id="6c618-124">Windows PowerShell에서 App-v 5.0 Reporting을 관리 하려면 [PowerShell을 사용 하 여 app-v 5.0 클라이언트에서 보고 기능을 사용 하도록 설정 하는 방법을](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-124">To administer App-V 5.0 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).</span></span>

5.  <span data-ttu-id="6c618-125">보고 서버는 App-v 5.0 클라이언트에서 데이터를 받은 후 보고 데이터베이스로 데이터를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-125">After the reporting server receives the data from the App-V 5.0 client it sends the data to the reporting database.</span></span> <span data-ttu-id="6c618-126">데이터베이스에서 클라이언트 데이터를 받아서 처리 하는 경우 응답은 성공적으로 보고 서버로 보내지며 App-v 5.0 클라이언트에 게 알림이 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.0 client.</span></span>

6.  <span data-ttu-id="6c618-127">App-v 5.0 클라이언트는 성공 알림을 받을 때 공간을 절약 하기 위해 데이터 캐시를 비웁니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-127">When the App-V 5.0 client receives the success notification, it empties the data cache to conserve space.</span></span>

    <span data-ttu-id="6c618-128">**참고**  기본적으로 서버가 데이터 수신을 확인 한 후 캐시가 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-128">**Note** By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="6c618-129">데이터 캐시를 저장 하도록 클라이언트를 수동으로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-129">You can manually configure the client to save the data cache.</span></span>

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="6c618-130">앱-V 5.0 보고 서버 자주 묻는 질문</span><span class="sxs-lookup"><span data-stu-id="6c618-130">App-V 5.0 reporting server frequently asked questions</span></span>

<span data-ttu-id="6c618-131">다음 표에서는 App-v 5.0 reporting에 대 한 일반적인 질문에 대 한 대답을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-131">The following table displays answers to common questions about App-V 5.0 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6c618-132">질문</span><span class="sxs-lookup"><span data-stu-id="6c618-132">Question</span></span></th>
<th align="left"><span data-ttu-id="6c618-133">추가 정보</span><span class="sxs-lookup"><span data-stu-id="6c618-133">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6c618-134">보고서 정보를 보고 데이터베이스로 보내는 빈도는 어떻게 되나요?</span><span class="sxs-lookup"><span data-stu-id="6c618-134">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-135">빈도는 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 보고 작업을 구성 하는 방법에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-135">The frequency depends on how the reporting task is configured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="6c618-136">보고 데이터를 보낼 빈도/간격을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-136">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="6c618-137">App-v 5.0 보고 기능은 기본적으로 사용 하도록 설정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-137">App-V 5.0 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6c618-138">보고 서버 데이터베이스에 저장 되는 정보는 무엇 인가요?</span><span class="sxs-lookup"><span data-stu-id="6c618-138">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-139">다음 목록에는 보고 데이터베이스에 저장 되어 있는 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-139">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="6c618-140">App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 실행 되는 운영 체제: 호스트 이름, 버전, 서비스 팩, 형식-클라이언트/서버, 프로세서 아키텍처.</span><span class="sxs-lookup"><span data-stu-id="6c618-140">The operating system running on the computer running the App-V 5.0 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="6c618-141">앱-V 5.0 클라이언트 정보: 버전.</span><span class="sxs-lookup"><span data-stu-id="6c618-141">App-V 5.0 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="6c618-142">게시 된 패키지 목록: GUID, 버전 GUID, name.</span><span class="sxs-lookup"><span data-stu-id="6c618-142">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="6c618-143">응용 프로그램 사용 정보: 이름, 버전, 스트리밍 서버, 사용자 (domain\alias), 패키지 버전 GUID, 시작 상태 및 시간, 종료 시간.</span><span class="sxs-lookup"><span data-stu-id="6c618-143">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6c618-144">보고 서버로 보내는 정보의 평균 량은 얼마 입니까?</span><span class="sxs-lookup"><span data-stu-id="6c618-144">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-145">그것은 사정 나름이에요.</span><span class="sxs-lookup"><span data-stu-id="6c618-145">It depends.</span></span> <span data-ttu-id="6c618-146">다음 목록에는 보고 서버로 전송 되는 세 가지 데이터 집합이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-146">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="6c618-147">운영 체제, 앱-V 5.0 클라이언트 정보.</span><span class="sxs-lookup"><span data-stu-id="6c618-147">Operating system, and App-V 5.0 client information.</span></span> <span data-ttu-id="6c618-148">~ 150 바이트,이 데이터를 보낼 때마다</span><span class="sxs-lookup"><span data-stu-id="6c618-148">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="6c618-149">게시 된 패키지 목록.</span><span class="sxs-lookup"><span data-stu-id="6c618-149">Published package list.</span></span> <span data-ttu-id="6c618-150">30 개 패키지의 경우 ~ 7kb</span><span class="sxs-lookup"><span data-stu-id="6c618-150">~7 KB for 30 packages.</span></span> <span data-ttu-id="6c618-151">이는 패키지 목록이 게시 새로 고침으로 업데이트 된 경우에만 전송 되며,이는 자주 수행 되지 않습니다. 변경 내용이 없는 경우에는이 정보가 전송 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-151">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="6c618-152">가상 응용 프로그램 사용 정보 – 이벤트 당 0.25 KB 정보</span><span class="sxs-lookup"><span data-stu-id="6c618-152">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="6c618-153">정보를 보내기 전에 두 경우를 모두 열고 닫는 경우 하나의 이벤트로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-153">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="6c618-154">예약 된 작업을 사용 하 여 보내는 경우 마지막 업로드에 성공한 데이터만 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-154">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="6c618-155">PowerShell cmdlet을 통해 수동으로 전송 하는 경우 다음에 데이터를 다시 보내야 하는지 여부를 제어 하는 선택적 인수 (인수는 DeleteOnSuccess)가 있습니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="6c618-155">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="6c618-156">예를 들어 20 개의 응용 프로그램을 열고, 그리고 보고 정보를 매일 전송 하도록 예약 하는 경우 일반적인 일일 트래픽은 약 0.15 KB + 20 x 0.25 KB 또는 약 5KB/사용자에 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-156">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6c618-157">보고를 예약할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="6c618-157">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-158">예.</span><span class="sxs-lookup"><span data-stu-id="6c618-158">Yes.</span></span> <span data-ttu-id="6c618-159">PowerShell Cmdlet (AppvClientReport)을 사용 하 여 보고를 수동으로 보내는 <strong> </strong> 것 외에도 자동으로 수행 되도록 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-159">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="6c618-160">다음과 같은 두 가지 방법으로 보고를 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-160">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="6c618-161">PowerShell cmdlet을 사용 하 여 <strong> AppvClientConfiguration를 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-161">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="6c618-162">예:</span><span class="sxs-lookup"><span data-stu-id="6c618-162">For example:</span></span></p>
<p><span data-ttu-id="6c618-163">Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="6c618-163">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="6c618-164">클라이언트 구성 설정에 대 한 전체 목록은 <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> 클라이언트 구성 설정 정보를 참조 </a> 하 고 <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay, </strong> ReportingInterval <strong> </strong> 항목을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-164">For a complete list of client configuration settings see <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="6c618-165">그룹 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-165">By using Group Policy.</span></span> <span data-ttu-id="6c618-166">도메인 컨트롤러를 사용 하 여 배포 하는 경우에는 이전에 나열 된 설정과 동일 하 게 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-166">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6c618-167">참고</span><span class="sxs-lookup"><span data-stu-id="6c618-167">Note</span></span></strong><br/><p><span data-ttu-id="6c618-168">PowerShell을 사용 하 여 구성 된 로컬 설정이 그룹 정책 설정 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-168">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> <span data-ttu-id="6c618-169">앱-V 5.0 클라이언트 보고</span><span class="sxs-lookup"><span data-stu-id="6c618-169">App-V 5.0 Client Reporting</span></span>


<span data-ttu-id="6c618-170">App-v 5.0 보고 기능을 사용 하려면 App-v 5.0 클라이언트를 설치 하 고 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-170">To use App-V 5.0 reporting you must install and configure the App-V 5.0 client.</span></span> <span data-ttu-id="6c618-171">클라이언트가 설치 되 면 **AppVClientConfiguration** PowerShell Cmdlet 또는 **ADMX 서식 파일** 을 사용 하 여 보고를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-171">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="6c618-172">보고 기능 cmdlet은 다음 링크를 사용 하 여 사용할 수 있으며, **보고**로 앞에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-172">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="6c618-173">클라이언트 구성 설정에 대 한 전체 목록은 [클라이언트 구성 설정 정보](about-client-configuration-settings.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-173">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span> <span data-ttu-id="6c618-174">다음 섹션에서는 PowerShell을 사용 하 여 App-v 5.0 클라이언트 보고 구성에 대 한 예제를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-174">The following section provides examples of App-V 5.0 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="6c618-175">PowerShell을 사용 하 여 App-v 클라이언트 보고 구성</span><span class="sxs-lookup"><span data-stu-id="6c618-175">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="6c618-176">다음 예제에서는 PowerShell 매개 변수를 통해 App-v 5.0 클라이언트의 보고 기능을 구성 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-176">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.0 client.</span></span>

**<span data-ttu-id="6c618-177">참고</span><span class="sxs-lookup"><span data-stu-id="6c618-177">Note</span></span>**  
<span data-ttu-id="6c618-178">앱-V 5.0 ADMX 템플릿에서 그룹 정책 설정을 사용 하 여 다음 구성 작업을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-178">The following configuration task can also be configured using Group Policy settings in the App-V 5.0 ADMX template.</span></span> <span data-ttu-id="6c618-179">ADMX 서식 파일을 사용 하는 방법에 대 한 자세한 내용은 [Admx 서식 파일 및 그룹 정책을 사용 하 여 app-v 5.0 클라이언트 구성을 수정 하는 방법을](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-179">For more information about using the ADMX template, see [How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>
 


<span data-ttu-id="6c618-180">**보고 기능을 사용 하도록 설정 하 고 app-v 5.0 클라이언트를 실행 하는 컴퓨터에서 데이터 수집을 시작**하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-180">**To enable reporting and to initiate data collection on the computer running the App-V 5.0 client**:</span></span>

`Set-AppVClientConfiguration –ReportingEnabled 1`

<span data-ttu-id="6c618-181">**특정 보고 서버에 데이터를 자동으로 보내도록 클라이언트를 구성 하려면 다음을 수행 합니다**.</span><span class="sxs-lookup"><span data-stu-id="6c618-181">**To configure the client to automatically send data to a specific reporting server**:</span></span>

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

<span data-ttu-id="6c618-182">이 예제에서는 보고 데이터를 보고 서버 URL로 자동으로 보내도록 클라이언트를 구성 합니다 <strong> http://MyReportingServer:MyPort/ </strong> .</span><span class="sxs-lookup"><span data-stu-id="6c618-182">This example configures the client to automatically send the reporting data to the reporting server URL <strong>http://MyReportingServer:MyPort/</strong>.</span></span> <span data-ttu-id="6c618-183">또한 보고 데이터는 세션에 대해 생성 되는 임의 지연에 따라 매일 8:00와 8:30 PM 사이에 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-183">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="6c618-184">**클라이언트에서 데이터 캐시 크기를 제한 하려면 다음을**수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-184">**To limit the size of the data cache on the client**:</span></span>

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

<span data-ttu-id="6c618-185">App-v 5.0 클라이언트를 실행 하는 컴퓨터의 보고 캐시 최대 크기를 100 MB로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-185">Configures the maximum size of the reporting cache on the computer running the App-V 5.0 client to 100 MB.</span></span> <span data-ttu-id="6c618-186">서버로 데이터를 전송 하기 전에 캐시 제한에 도달 하면 필요한 경우 로그가 롤업되 고 데이터가 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-186">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="6c618-187">**클라이언트와 서버 간에 네트워크를 통해 전송 되는 데이터 블록 크기를 구성 하려면 다음을 수행 합니다**.</span><span class="sxs-lookup"><span data-stu-id="6c618-187">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

<span data-ttu-id="6c618-188">클라이언트가 10240 MB로 보내는 최대 데이터 블록 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-188">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="6c618-189">수집 된 데이터 형식</span><span class="sxs-lookup"><span data-stu-id="6c618-189">Types of data collected</span></span>

<span data-ttu-id="6c618-190">다음 표에는 App-v 5.0 보고를 사용 하 여 수집할 수 있는 정보의 유형이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-190">The following table displays the types of information you can collect by using App-V 5.0 reporting.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6c618-191">클라이언트 정보</span><span class="sxs-lookup"><span data-stu-id="6c618-191">Client Information</span></span></th>
<th align="left"><span data-ttu-id="6c618-192">패키지 정보</span><span class="sxs-lookup"><span data-stu-id="6c618-192">Package Information</span></span></th>
<th align="left"><span data-ttu-id="6c618-193">응용 프로그램 사용</span><span class="sxs-lookup"><span data-stu-id="6c618-193">Application Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6c618-194">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="6c618-194">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-195">패키지 이름</span><span class="sxs-lookup"><span data-stu-id="6c618-195">Package Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-196">시작 및 종료 시간</span><span class="sxs-lookup"><span data-stu-id="6c618-196">Start and End Times</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6c618-197">App-v 5.0 클라이언트 버전</span><span class="sxs-lookup"><span data-stu-id="6c618-197">App-V 5.0 Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-198">패키지 버전</span><span class="sxs-lookup"><span data-stu-id="6c618-198">Package Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-199">실행 상태</span><span class="sxs-lookup"><span data-stu-id="6c618-199">Run Status</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6c618-200">프로세서 아키텍처</span><span class="sxs-lookup"><span data-stu-id="6c618-200">Processor Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-201">패키지 원본</span><span class="sxs-lookup"><span data-stu-id="6c618-201">Package Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-202">종료 상태</span><span class="sxs-lookup"><span data-stu-id="6c618-202">Shutdown State</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6c618-203">운영 체제 버전</span><span class="sxs-lookup"><span data-stu-id="6c618-203">Operating System Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-204">캐시 된 백분율</span><span class="sxs-lookup"><span data-stu-id="6c618-204">Percent Cached</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-205">응용 프로그램 이름</span><span class="sxs-lookup"><span data-stu-id="6c618-205">Application Name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6c618-206">서비스 팩 수준</span><span class="sxs-lookup"><span data-stu-id="6c618-206">Service Pack Level</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6c618-207">응용 프로그램 버전</span><span class="sxs-lookup"><span data-stu-id="6c618-207">Application Version</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6c618-208">운영 체제 종류</span><span class="sxs-lookup"><span data-stu-id="6c618-208">Operating System Type</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6c618-209">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="6c618-209">Username</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6c618-210">연결 그룹</span><span class="sxs-lookup"><span data-stu-id="6c618-210">Connection Group</span></span></p></td>
</tr>
</tbody>
</table>
 


<span data-ttu-id="6c618-211">클라이언트는이 데이터를 수집 하 여 **.xml** 형식으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-211">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="6c618-212">데이터 캐시는 기본적으로 숨겨지며, XML 파일을 열기 위한 관리자 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-212">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="6c618-213">서버로 데이터 보내기</span><span class="sxs-lookup"><span data-stu-id="6c618-213">Sending data to the server</span></span>

<span data-ttu-id="6c618-214">앱-V 5.0 클라이언트를 실행 하는 컴퓨터를 구성 하 여 지정 된 보고 서버로 데이터를 자동으로 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-214">You can configure the computer that is running the App-V 5.0 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="6c618-215">서버를 지정 하려면 **Set-AppvClientConfiguration** cmdlet을 다음 설정으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-215">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

-   <span data-ttu-id="6c618-216">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="6c618-216">ReportingEnabled</span></span>

-   <span data-ttu-id="6c618-217">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="6c618-217">ReportingServerURL</span></span>

-   <span data-ttu-id="6c618-218">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="6c618-218">ReportingStartTime</span></span>

-   <span data-ttu-id="6c618-219">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="6c618-219">ReportingInterval</span></span>

-   <span data-ttu-id="6c618-220">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="6c618-220">ReportingRandomDelay</span></span>

<span data-ttu-id="6c618-221">이전 설정을 구성한 후에는 예약 된 작업을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-221">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="6c618-222">예약 된 작업은 **ReportingServerURL** 설정으로 지정 된 서버에 연결 하 고 전송을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-222">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="6c618-223">예약 된 시간 밖으로 데이터를 수동으로 보내려면 다음 PowerShell cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-223">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

<span data-ttu-id="6c618-224">보고 서버를 이전에 구성한 경우 **– URL** 매개 변수를 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-224">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="6c618-225">또는 데이터를 대체 위치로 보내야 하는 경우 다른 URL을 지정 하 여이 데이터 컬렉션에 대해 구성 된 **ReportingServerURL** 를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-225">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="6c618-226">**-DeleteOnSuccess** 매개 변수는 전송이 성공적으로 수행 되는 경우 데이터 캐시가 지워지는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-226">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="6c618-227">이를 지정 하지 않으면 캐시가 지워지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-227">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="6c618-228">수동 데이터 수집</span><span class="sxs-lookup"><span data-stu-id="6c618-228">Manual Data Collection</span></span>

<span data-ttu-id="6c618-229">**AppVClientReport** cmdlet을 사용 하 여 데이터를 수동으로 수집할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-229">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="6c618-230">이 솔루션은 기존 보고 서버와 함께 유용 하거나 사용 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-230">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="6c618-231">다음 목록에는 보고 서버와 함께 데이터를 수집 하거나 포함 하지 않은 상태에 대 한 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-231">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6c618-232">보고 서버 사용</span><span class="sxs-lookup"><span data-stu-id="6c618-232">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="6c618-233">보고 서버 없이</span><span class="sxs-lookup"><span data-stu-id="6c618-233">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6c618-234">기존 App-v 5.0 reporting Server가 있는 경우 사용자 지정 된 예약 작업 또는 스크립트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-234">If you have an existing App-V 5.0 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="6c618-235">클라이언트가 원하는 빈도를 사용 하 여 데이터를 지정 된 위치로 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-235">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6c618-236">기존 App-v 5.0 reporting Server가 없는 경우 <strong> – URL </strong> 매개 변수를 사용 하 여 데이터를 지정 된 공유에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-236">If you do not have an existing App-V 5.0 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="6c618-237">예:</span><span class="sxs-lookup"><span data-stu-id="6c618-237">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="6c618-238">앞의 예제에서는 <strong> &lt; &gt; <strong> -URL 매개 변수를 통해 표시 되는 \MyShare\MyData/strong 위치에 보고 데이터를 보냅니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="6c618-238">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="6c618-239">데이터를 보낸 후에는 캐시가 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-239">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6c618-240">참고</span><span class="sxs-lookup"><span data-stu-id="6c618-240">Note</span></span></strong><br/><p><span data-ttu-id="6c618-241">보고 서버 이외의 위치를 지정 하면 데이터는 <strong> 추가 처리 없이 .xml 형식을 사용 하 여 전송 됩니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="6c618-241">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6c618-242">보고서 만들기</span><span class="sxs-lookup"><span data-stu-id="6c618-242">Creating Reports</span></span>

<span data-ttu-id="6c618-243">앱-V 5.0를 사용 하 여 보고서 정보를 검색 하 고 보고서를 만들려면 다음 방법 중 하나를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-243">To retrieve report information and create reports using App-V 5.0 you must use one of the following methods:</span></span>

-   <span data-ttu-id="6c618-244">Microsoft sql server **Reporting services (SSRS)** 를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-244">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="6c618-245">App-v 5.0 reporting server를 설치할 때 SSRS가 설치 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-245">SSRS is not installed when you install the App-V 5.0 reporting server.</span></span> <span data-ttu-id="6c618-246">연결 된 보고서를 생성 하려면 별도로 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-246">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="6c618-247">[MICROSOFT SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596)를 사용 하는 방법에 대 한 자세한 내용은 다음 링크를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-247">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

-   <span data-ttu-id="6c618-248">**스크립팅** -app-v 5.0 보고 데이터베이스에 대해 직접 스크립팅 하 여 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-248">**Scripting** – You can generate reports by scripting directly against the App-V 5.0 reporting database.</span></span> <span data-ttu-id="6c618-249">예:</span><span class="sxs-lookup"><span data-stu-id="6c618-249">For example:</span></span>

    **<span data-ttu-id="6c618-250">저장 프로시저:</span><span class="sxs-lookup"><span data-stu-id="6c618-250">Stored Procedure:</span></span>**

    <span data-ttu-id="6c618-251">**Spprocessclientreport** 는 자정 또는 12:00 오전에 실행 되도록 예약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-251">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="6c618-252">Microsoft SQL Server 예약 된 저장 프로시저를 실행 하려면 Microsoft SQL Server 에이전트를 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-252">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="6c618-253">Microsoft SQL Server 에이전트가 **자동**시작으로 설정 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-253">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="6c618-254">자세한 내용은 [Sql Server 에이전트 자동 시작 (Sql Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c618-254">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="6c618-255">또한 App-v 5.0 데이터베이스 스크립트를 사용 하 여 저장 프로시저를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-255">The stored procedure is also created when using the App-V 5.0 database scripts.</span></span>

<span data-ttu-id="6c618-256">또한 보고 서버 웹 서비스의 **최대 동시 연결이** 가용성에 영향을 주지 않고 관리할 수 있는 값으로 설정 되어 있는지도 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-256">You should also ensure that the reporting server web service’s **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="6c618-257">**보고 웹 서비스** 의 권장 되는 **최대 동시 연결** 수는 **1만**입니다.</span><span class="sxs-lookup"><span data-stu-id="6c618-257">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>






## <span data-ttu-id="6c618-258">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6c618-258">Related topics</span></span>


[<span data-ttu-id="6c618-259">App-V 5.0 Server 배포</span><span class="sxs-lookup"><span data-stu-id="6c618-259">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="6c618-260">독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="6c618-260">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





