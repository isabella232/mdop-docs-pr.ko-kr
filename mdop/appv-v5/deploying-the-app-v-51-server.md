---
title: App-V 5.1 Server 배포
description: App-V 5.1 Server 배포
author: dansimp
ms.assetid: 987b61dc-00d6-49ba-8f1b-92d7b948e702
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bcff2a3211ea3e2f666aff1d6f2ad919509aa3a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814564"
---
# <span data-ttu-id="221d3-103">App-V 5.1 Server 배포</span><span class="sxs-lookup"><span data-stu-id="221d3-103">Deploying the App-V 5.1 Server</span></span>

<span data-ttu-id="221d3-104">이 항목에서 설명 하는 다양 한 배포 구성을 사용 하 여 Microsoft App-v (Application Virtualization) 5.1 서버 기능을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-104">You can install the Microsoft Application Virtualization (App-V) 5.1 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="221d3-105">서버 기능을 설치 하기 전에 [app-v 5.1 보안 고려](app-v-51-security-considerations.md)사항의 서버 섹션을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-105">Before you install the server features, review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

<span data-ttu-id="221d3-106">App-v 서버 배포에 대 한 자세한 내용은 [앱-v 5.1 정보](about-app-v-51.md#bkmk-migrate-to-51)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="221d3-106">For information about deploying the App-V Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="221d3-107">App-v 5.1 서버를 설치 하 고 구성 하기 전에 각 구성 요소를 호스팅할 포트를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-107">Before you install and configure the App-V 5.1 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="221d3-108">또한 들어오는 요청에 대해 지정 된 포트에 액세스할 수 있도록 연결 된 방화벽 규칙도 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="221d3-109">설치 관리자가 방화벽 설정을 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-109">The installer does not modify firewall settings.</span></span>

## <a href="" id="---------app-v-5-1-server-overview"></a> <span data-ttu-id="221d3-110">앱-V 5.1 서버 개요</span><span class="sxs-lookup"><span data-stu-id="221d3-110">App-V 5.1 Server overview</span></span>

<span data-ttu-id="221d3-111">App-v 5.1 서버는 다섯 개의 구성 요소로 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-111">The App-V 5.1 Server is made up of five components.</span></span> <span data-ttu-id="221d3-112">각 구성 요소는 App-v 5.1 환경에서 서로 다른 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-112">Each component serves a different purpose within the App-V 5.1 environment.</span></span> <span data-ttu-id="221d3-113">다음의 다섯 가지 구성 요소 각각에 대해 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-113">Each of the five components is briefly described here:</span></span>

- <span data-ttu-id="221d3-114">관리 서버-App-v 5.1 인프라에 대 한 전반적인 관리 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-114">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>
- <span data-ttu-id="221d3-115">관리 데이터베이스 – App-v 5.1 management에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-115">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>
- <span data-ttu-id="221d3-116">게시 서버 – 가상 응용 프로그램에 대 한 호스팅 및 스트리밍 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>
- <span data-ttu-id="221d3-117">보고 서버-App-v 5.1 reporting services를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-117">Reporting Server – provides App-V 5.1 reporting services.</span></span>
- <span data-ttu-id="221d3-118">보고 데이터베이스-App-v 5.1 reporting에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-118">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

## <a href="" id="---------app-v-5-1-stand-alone-deployment"></a> <span data-ttu-id="221d3-119">App-v 5.1 독립 실행형 배포</span><span class="sxs-lookup"><span data-stu-id="221d3-119">App-V 5.1 stand-alone deployment</span></span>

<span data-ttu-id="221d3-120">App-v 5.1 독립 실행형 배포는 소규모 배포 또는 테스트 환경에 적합 한 토폴로지를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-120">The App-V 5.1 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="221d3-121">이러한 유형의 구현을 사용 하는 경우 모든 서버 구성 요소가 단일 컴퓨터에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="221d3-122">서비스 및 관련 데이터베이스는 App-v 5.1 구성 요소를 실행 하는 컴퓨터의 리소스에 대 한 경합을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.1 components.</span></span> <span data-ttu-id="221d3-123">따라서 대규모 배포에는이 토폴로지를 사용해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="221d3-124">App-V 5.1 Server 배포 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-124">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)

[<span data-ttu-id="221d3-125">스크립트를 사용하여 App-V 5.1 Server를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-125">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

## <a href="" id="---------app-v-5-1-server-distributed-deployment"></a> <span data-ttu-id="221d3-126">App-v 5.1 서버 분산 배포</span><span class="sxs-lookup"><span data-stu-id="221d3-126">App-V 5.1 Server distributed deployment</span></span>

<span data-ttu-id="221d3-127">분산 배포 토폴로지는 대규모 App-v 5.1 클라이언트 기반을 지원할 수 있으며, 더 쉽게 환경을 관리 하 고 확장 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-127">The distributed deployment topology can support a large App-V 5.1 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="221d3-128">이 유형의 배포를 사용 하는 경우 앱-V 5.1 서버 구성 요소는 조직의 구조 및 요구 사항에 따라 여러 컴퓨터에 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-128">When you use this type of deployment, the App-V 5.1 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="221d3-129">관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="221d3-130">독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-130">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

[<span data-ttu-id="221d3-131">스크립트를 사용하여 App-V 5.1 Server를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-131">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

[<span data-ttu-id="221d3-132">원격 컴퓨터에 게시 서버를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="221d3-133">독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

## <span data-ttu-id="221d3-134">ESD (엔터프라이즈 소프트웨어 배포) 솔루션 및 앱-V 5.1 사용</span><span class="sxs-lookup"><span data-stu-id="221d3-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.1</span></span>

<span data-ttu-id="221d3-135">App-v 5.1을 배포할 필요 없이 ESD를 사용 하 여 App-v 5.1 클라이언트 및 패키지를 배포할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-135">You can also deploy the App-V 5.1 clients and packages by using an ESD without having to deploy App-V 5.1.</span></span> <span data-ttu-id="221d3-136">통합에 대 한 전체 접근 권한 값은 사용 하는 ESD에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

> [!NOTE]
> <span data-ttu-id="221d3-137">앱-V 5.1 보고 서버 및 보고 데이터베이스는 ESD와 함께 배포 하 여 App-v 5.1 클라이언트에서 보고 데이터를 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-137">The App-V 5.1 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.1 clients.</span></span> <span data-ttu-id="221d3-138">그러나 나머지 세 개의 서버 구성 요소는 ESD 기능과 충돌 하므로 배포 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

[<span data-ttu-id="221d3-139">ESD(전자 소프트웨어 배포)를 사용하여 App-V 5.1 패키지 배포</span><span class="sxs-lookup"><span data-stu-id="221d3-139">Deploying App-V 5.1 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-51-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-1-server-logs"></a> <span data-ttu-id="221d3-140">앱-V 5.1 서버 로그</span><span class="sxs-lookup"><span data-stu-id="221d3-140">App-V 5.1 Server logs</span></span>

<span data-ttu-id="221d3-141">App-v 5.1를 사용 하는 동안 서버 설치 및 작동 이벤트 문제를 해결 하는 데 도움이 되는 앱-V 5.1 서버 로그 정보를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-141">You can use App-V 5.1 server log information to help troubleshoot the server installation and operational events while using App-V 5.1.</span></span> <span data-ttu-id="221d3-142">**이벤트 뷰어**를 사용 하 여 서버 관련 로그 정보를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="221d3-143">다음 줄에는 서버 관련 이벤트의 특정 경로가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="221d3-144">이벤트 뷰어 \ \ 응용 프로그램 및 서비스 로그 \ \ Microsoft \\ App V</span><span class="sxs-lookup"><span data-stu-id="221d3-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="221d3-145">연결 된 설치 로그는 다음 디렉터리에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="221d3-146">temp</span><span class="sxs-lookup"><span data-stu-id="221d3-146">%temp%</span></span>**

<span data-ttu-id="221d3-147">App-v 5.0 SP3에서는 일부 로그가 통합 및 이동 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-147">In App-V 5.0 SP3, some logs were consolidated and moved.</span></span> <span data-ttu-id="221d3-148">[앱-V 5.0 SP3 정보](about-app-v-50-sp3.md#bkmk-event-logs-moved)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="221d3-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-1-reporting"></a> <span data-ttu-id="221d3-149">앱-V 5.1 보고</span><span class="sxs-lookup"><span data-stu-id="221d3-149">App-V 5.1 reporting</span></span>

<span data-ttu-id="221d3-150">App-v 5.1 보고 기능을 사용 하면 App-v 5.1 클라이언트가 데이터를 수집 하 고 다시 전송 하 여 중앙 리포지토리에 저장 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-150">App-V 5.1 reporting allows App-V 5.1 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="221d3-151">이 정보를 사용 하 여 조직 내에서 가상 응용 프로그램 사용 현황을 더 자세히 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="221d3-152">다음 목록에는 App-v 5.1 클라이언트가 수집 하는 일부 정보 유형이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-152">The following list displays some of the types of information the App-V 5.1 client collects:</span></span>

- <span data-ttu-id="221d3-153">App-v 5.1 클라이언트를 실행 하는 컴퓨터에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-153">Information about the computer that runs the App-V 5.1 client.</span></span>
- <span data-ttu-id="221d3-154">App-v 5.1 클라이언트를 실행 하는 특정 컴퓨터의 가상화 된 패키지에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-154">Information about virtualized packages on a specific computer that runs the App-V 5.1 client.</span></span>
- <span data-ttu-id="221d3-155">특정 사용자의 패키지 열기 및 종료에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="221d3-156">보고 정보는 보고 서버 데이터베이스로 성공적으로 전송 될 때까지 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="221d3-157">데이터를 데이터베이스에 추가한 후에는 Microsoft SQL Server Reporting Services를 사용 하 여 필요한 보고서를 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="221d3-158">보고서 정보를 검색 하려면 Microsoft SQL에서 사용할 수 있는 Microsoft SSRS (SQL Server Reporting Services)를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="221d3-159">App-v 5.1 reporting server를 설치할 때 SSRS가 설치 되지 않으며 연결 된 보고서를 생성 하려면 별도로 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="221d3-159">SSRS is not installed when you install the App-V 5.1 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="221d3-160">[앱-V 5.1 보고에 대 한](about-app-v-51-reporting.md)자세한 내용은 다음 링크를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="221d3-160">Use the following link for more information [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

[<span data-ttu-id="221d3-161">PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="221d3-161">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)

## <span data-ttu-id="221d3-162">App-v 서버에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="221d3-162">Other resources for the App-V server</span></span>

[<span data-ttu-id="221d3-163">App-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="221d3-163">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)
