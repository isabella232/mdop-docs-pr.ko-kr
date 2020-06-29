---
title: MBAM 2.5 보고서를 이동하는 방법
description: MBAM 2.5 보고서를 이동하는 방법
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812393"
---
# <span data-ttu-id="fefc0-103">MBAM 2.5 보고서를 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="fefc0-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="fefc0-104">이 절차를 사용 하 여 보고서 기능을 한 컴퓨터에서 다른 컴퓨터로 이동 (즉, 보고서 기능을 서버 A에서 서버 B로 이동) 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="fefc0-105">보고서 기능을 이동 하는 상위 수준 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="fefc0-106">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="fefc0-107">서버 B에 MBAM 2.5 서버 소프트웨어를 설치 하 고 서버 B에서 보고서 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="fefc0-108">MBAM 관리 및 모니터링 서버에서 보고서 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="fefc0-109">MBAM 관리 및 모니터링 웹 사이트의 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="fefc0-110">**참고**  이 항목의 예제 Windows PowerShell 스크립트를 실행 하려면 스크립트를 실행할 수 있도록 Windows PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="fefc0-111">자세한 내용은 [Windows PowerShell 스크립트 실행](https://technet.microsoft.com/library/ee176949.aspx) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fefc0-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="fefc0-112">MBAM 관리 및 모니터링 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="fefc0-113">관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="fefc0-114">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="fefc0-115">MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행</span><span class="sxs-lookup"><span data-stu-id="fefc0-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="fefc0-116">서버 B에 MBAM 서버 소프트웨어를 설치 합니다. 지침은 [MBAM 2.5 서버 소프트웨어 설치](installing-the-mbam-25-server-software.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fefc0-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="fefc0-117">서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **보고서** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="fefc0-118">또는 **Enable-MbamReport** Windows PowerShell cmdlet을 사용 하 여 보고서를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="fefc0-119">보고서를 구성 하는 방법에 대 한 지침은 [MBAM 2.5 보고서를 구성](how-to-configure-the-mbam-25-reports.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fefc0-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="fefc0-120">관리 및 모니터링 서버에서 보고서 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="fefc0-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="fefc0-121">보고서 기능을 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 보고서 URL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="fefc0-122">**Microsoft BitLocker 관리 및 모니터링**을 확장 한 다음 **헬프데스크** 노드를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="fefc0-123">**기능 보기**의 **관리** 섹션에서 **구성 편집기**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="fefc0-124">**섹션** 필드에서 **appSettings**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="fefc0-125">**컬렉션** 행을 선택한 다음 창의 맨 오른쪽에 있는 "줄임표" 단추 **(...)** 를 클릭 하 여 **컬렉션 편집기**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="fefc0-126">**컬렉션 편집기**에서 **microsoft. r**e m. e a l. e a m .에 대 한 값을 업데이트 하 고 서버 B에 대 한 서버 이름을 반영 하는 url을 선택 합니다 **.**</span><span class="sxs-lookup"><span data-stu-id="fefc0-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="fefc0-127">이전에 SQL Server Reporting Services의 명명 된 인스턴스에서 보고서 기능을 구성한 경우에는 다음과 같이 인스턴스의 이름을 URL에 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="fefc0-128">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 관리 및 모니터링 서버에서 다음 코드 예제와 유사한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="fefc0-129">다음 표의 설명을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fefc0-130">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fefc0-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="fefc0-131">설명</span><span class="sxs-lookup"><span data-stu-id="fefc0-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fefc0-132">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="fefc0-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fefc0-133">보고서를 이동한 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fefc0-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="fefc0-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fefc0-135">보고서가 이동 된 SQL Server Reporting Services 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="fefc0-136">관리 및 모니터링 웹 사이트 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="fefc0-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="fefc0-137">관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="fefc0-138">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="fefc0-139">**참고**  이 명령을 실행 하려면 windows powershell 용 IIS 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="fefc0-140">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fefc0-140">Related topics</span></span>


[<span data-ttu-id="fefc0-141">MBAM 2.5 보고서를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="fefc0-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="fefc0-142">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="fefc0-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="fefc0-143">다른 서버로 MBAM 2.5 기능 이동</span><span class="sxs-lookup"><span data-stu-id="fefc0-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="fefc0-144">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="fefc0-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fefc0-145">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="fefc0-146">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fefc0-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





