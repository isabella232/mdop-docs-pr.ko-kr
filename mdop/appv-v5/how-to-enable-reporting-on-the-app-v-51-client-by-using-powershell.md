---
title: PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법
description: PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814073"
---
# <span data-ttu-id="05c21-103">PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="05c21-103">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>


<span data-ttu-id="05c21-104">다음 절차를 사용 하 여 보고용 앱-V 5.1를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-104">Use the following procedure to configure the App-V 5.1 for reporting.</span></span>

**<span data-ttu-id="05c21-105">보고를 위해 App-v 5.1 클라이언트를 실행 하는 컴퓨터를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="05c21-105">To configure the computer running the App-V 5.1 client for reporting</span></span>**

1. <span data-ttu-id="05c21-106">App-v 5.1 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-106">Install the App-V 5.1 client.</span></span> <span data-ttu-id="05c21-107">클라이언트를 설치 하는 방법에 대 한 자세한 내용은 [App-v 클라이언트를 배포 하는 방법을](how-to-deploy-the-app-v-client-51gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05c21-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

2. <span data-ttu-id="05c21-108">App-v 5.1 클라이언트를 설치한 후 **Set AppvClientConfiguration** PowerShell을 사용 하 여 적절 한 보고 구성 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-108">After you have installed the App-V 5.1 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="05c21-109">설정</span><span class="sxs-lookup"><span data-stu-id="05c21-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="05c21-110">설명</span><span class="sxs-lookup"><span data-stu-id="05c21-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="05c21-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="05c21-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-112">클라이언트가 보고 서버로 정보를 반환할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="05c21-113">클라이언트가 클라이언트에서 보고 데이터를 수집 하려면이 설정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="05c21-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="05c21-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-115">클라이언트 정보가 저장 되는 보고 서버의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="05c21-116">예를 들어 http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt;</span><span class="sxs-lookup"><span data-stu-id="05c21-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="05c21-117">참고</span><span class="sxs-lookup"><span data-stu-id="05c21-117">Note</span></span></strong><br/><p><span data-ttu-id="05c21-118">보고 서버 설정 중에 지정 된 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="05c21-119">보고 시작 시간</span><span class="sxs-lookup"><span data-stu-id="05c21-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-120">이는 클라이언트가 서버에 데이터를 자동으로 보내도록 예약 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="05c21-121">이 설정은 보고 데이터 보내기를 시작 하는 시간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="05c21-122">24 시간 형식으로 표시 되며 0-23 사이의 숫자가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="05c21-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="05c21-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-124">보고 서버로 데이터를 보낼 최대 지연 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="05c21-125">예약 된 작업이 시작 되 면 클라이언트는 0과 ReportingRandomDelay 사이의 임의 지연 시간을 생성 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="05c21-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="05c21-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-127">클라이언트가 보고 서버에 데이터를 재전송 하는 데 사용할 다시 시도 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="05c21-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="05c21-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-129">보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="05c21-130">크기는 메모리의 캐시에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="05c21-131">제한에 도달 하면 로그 파일이 롤오버 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="05c21-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="05c21-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="05c21-133">보고 정보를 저장 하기 위한 XML 캐시의 최대 크기 (MB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="05c21-134">크기는 메모리의 캐시에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="05c21-135">제한에 도달 하면 로그 파일이 롤오버 됩니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="05c21-136">적절 한 설정이 구성 되 면 App-v 5.1 클라이언트를 실행 하는 컴퓨터가 데이터를 자동으로 수집 하 고 데이터를 보고 서버로 다시 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-136">After the appropriate settings have been configured, the computer running the App-V 5.1 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="05c21-137">또한 관리자는 **AppvClientReport** PowerShell cmdlet을 사용 하 여 요청 하는 방식으로 데이터를 수동으로 다시 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="05c21-138">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="05c21-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="05c21-139">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="05c21-140">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="05c21-140">Got an App-V issue?</span></span>** <span data-ttu-id="05c21-141">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c21-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="05c21-142">관련 항목</span><span class="sxs-lookup"><span data-stu-id="05c21-142">Related topics</span></span>


[<span data-ttu-id="05c21-143">PowerShell을 사용하여 App-V 5.1 관리</span><span class="sxs-lookup"><span data-stu-id="05c21-143">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









