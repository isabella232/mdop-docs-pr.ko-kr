---
title: MBAM 2.5 웹 사이트를 이동하는 방법
description: MBAM 2.5 웹 사이트를 이동하는 방법
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825748"
---
# <span data-ttu-id="df7f1-103">MBAM 2.5 웹 사이트를 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="df7f1-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="df7f1-104">다음 절차를 사용 하 여 다음 MBAM 웹 사이트를 한 컴퓨터에서 다른 컴퓨터로 이동 하 여 서버 A에서 서버 B로 다음 기능을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="df7f1-105">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="df7f1-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="df7f1-106">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="df7f1-106">Self-Service Portal</span></span>

<span data-ttu-id="df7f1-107">**중요**  두 웹 사이트를 구성 하는 동안 같은 연결 문자열, 보고서 URL, 그룹 계정 및 웹 서비스 응용 프로그램 풀 도메인 계정을 현재 사용 중인 사용자와 함께 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="df7f1-108">같은 값을 사용 하지 않는 경우에는 일부 서버에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="df7f1-109">현재 값을 가져오려면 **get-MbamWebApplication** Windows PowerShell cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="df7f1-110">관리 및 모니터링 웹 사이트를 다른 서버로 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="df7f1-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="df7f1-111">서버 B에서 MBAM 2.5 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="df7f1-112">지침은 [MBAM 2.5 서버 소프트웨어 설치](installing-the-mbam-25-server-software.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df7f1-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="df7f1-113">서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **관리 및 모니터링 웹 사이트** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="df7f1-114">또는 **Enable-MbamWebApplication** Windows PowerShell cmdlet을 사용 하 여 관리 및 모니터링 웹 사이트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="df7f1-115">관리 및 모니터링 웹 사이트를 구성 하는 방법에 대 한 지침은 [MBAM 2.5 웹 응용 프로그램을 구성](how-to-configure-the-mbam-25-web-applications.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df7f1-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="df7f1-116">셀프 서비스 포털을 다른 서버로 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="df7f1-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="df7f1-117">서버 B에서 MBAM 2.5 서버 소프트웨어를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="df7f1-118">지침은 [MBAM 2.5 서버 소프트웨어 설치](installing-the-mbam-25-server-software.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df7f1-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="df7f1-119">서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **셀프 서비스 포털** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="df7f1-120">또는 **Enable-MbamWebApplication** Windows PowerShell cmdlet을 사용 하 여 셀프 서비스 포털을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="df7f1-121">관리 및 모니터링 웹 사이트를 구성 하는 방법에 대 한 지침은 [MBAM 2.5 웹 응용 프로그램을 구성](how-to-configure-the-mbam-25-web-applications.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df7f1-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="df7f1-122">조직의 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 JavaScript 파일도 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="df7f1-123">자세한 내용은 [클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하는 방법을](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df7f1-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="df7f1-124">조직의 셀프 서비스 포털을 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="df7f1-125">[조직의 셀프 서비스 포털을 사용자 지정](customizing-the-self-service-portal-for-your-organization.md) 하는 지침을 사용 하 여 현재 사용자 지정을 검토 하 고 서버 B의 셀프 서버 포털에서 사용자 지정 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="df7f1-126">관련 항목</span><span class="sxs-lookup"><span data-stu-id="df7f1-126">Related topics</span></span>


[<span data-ttu-id="df7f1-127">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="df7f1-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="df7f1-128">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="df7f1-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="df7f1-129">다른 서버로 MBAM 2.5 기능 이동</span><span class="sxs-lookup"><span data-stu-id="df7f1-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="df7f1-130">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="df7f1-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="df7f1-131">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="df7f1-132">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f1-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





