---
title: App-V 5.0 용량 계획
description: App-V 5.0 용량 계획
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814852"
---
# <span data-ttu-id="845e1-103">App-V 5.0 용량 계획</span><span class="sxs-lookup"><span data-stu-id="845e1-103">App-V 5.0 Capacity Planning</span></span>


<span data-ttu-id="845e1-104">다음 권장 사항은 조직의 App-v 5.0 인프라에 적합 한 용량 계획 정보를 결정 하는 데 도움이 되는 기준으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="845e1-105">**중요**  이 섹션의 정보는 App-v 5.0 배포 계획을 위한 일반적인 가이드로만 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.0 deployment.</span></span> <span data-ttu-id="845e1-106">시스템 용량 요구 사항은 하드웨어 및 응용 프로그램 환경의 특정 정보에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="845e1-107">또한이 문서에 표시 되는 성과 번호는 예제 이며 결과는 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="845e1-108">프로젝트 범위 결정</span><span class="sxs-lookup"><span data-stu-id="845e1-108">Determine the Project Scope</span></span>


<span data-ttu-id="845e1-109">App-v 5.0 인프라를 디자인 하기 전에 프로젝트의 범위를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-109">Before you design the App-V 5.0 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="845e1-110">범위는 사실상 사용할 수 있는 응용 프로그램을 결정 하 고 대상 사용자 및 해당 위치를 식별 하는 데에도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="845e1-111">이 정보는 구현 해야 하는 App-v 5.0 인프라 유형을 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-111">This information will help determine what type of App-V 5.0 infrastructure should be implemented.</span></span> <span data-ttu-id="845e1-112">프로젝트 범위에 대 한 결정은 조직의 특정 요구 사항에 근거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-113">작업</span><span class="sxs-lookup"><span data-stu-id="845e1-113">Task</span></span></th>
<th align="left"><span data-ttu-id="845e1-114">추가 정보</span><span class="sxs-lookup"><span data-stu-id="845e1-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-115">응용 프로그램 범위 결정</span><span class="sxs-lookup"><span data-stu-id="845e1-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-116">가상화 할 응용 프로그램에 따라 App-v 5.0 인프라를 다양 한 방식으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-116">Depending on the applications to be virtualized, the App-V 5.0 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="845e1-117">첫 번째 작업은 가상화 하려는 응용 프로그램을 정의 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-118">위치 범위 결정</span><span class="sxs-lookup"><span data-stu-id="845e1-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-119">위치 범위는 가상 응용 프로그램을 실행할 계획인 실제 위치 (예: enterprise 전체 또는 특정 지리적 위치)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="845e1-120">또한 가상 응용 프로그램을 실행 하는 사용자 집단 (예: 단일 부서)을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="845e1-121">연결 경로 뿐만 아니라 각 위치에 대 한 사용 가능한 대역폭과 가상화 된 응용 프로그램을 사용 하는 사용자 수 및 WAN 연결 속도를 포함 하는 네트워크 맵을 구해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="845e1-122">어떤 App-v 5.0 인프라가 필요 하다는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-122">Determine Which App-V 5.0 Infrastructure is Required</span></span>


<span data-ttu-id="845e1-123">**중요**  다음 두 모델에서는 가상 응용 프로그램을 실행 하려는 컴퓨터에 App-v 5.0 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-123">**Important** Both of the following models require the App-V 5.0 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="845e1-124">Microsoft 시스템 센터 구성 관리자와 같은 ESD (전자 소프트웨어 배포) 솔루션을 사용 하 여 App-v 5.0 환경을 관리할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-124">You can also manage your App-V 5.0 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="845e1-125">자세한 내용은 [전자 소프트웨어 배포 (ESD)를 사용 하 여 앱 V 5.0 패키지 배포를](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-125">For more information see [Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span></span>

 

-   <span data-ttu-id="845e1-126">**독립 실행형 모델** -독립 실행형 모델을 통해 가상 응용 프로그램을 Windows Installer로 설정 하 여 스트리밍 없이 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="845e1-127">독립 실행형 모드의 app-v 5.0는 시퀀서 및 클라이언트로 구성 됩니다. 추가 구성 요소가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-127">App-V 5.0 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="845e1-128">시퀀싱 이라는 프로세스를 사용 하 여 응용 프로그램의 가상화를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="845e1-129">자세한 내용은 [앱-V 5.0 시퀀서 및 클라이언트 배포 계획](planning-for-the-app-v-50-sequencer-and-client-deployment.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-129">For more information see, [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="845e1-130">다음과 같은 시나리오에는 독립 실행형 모델을 사용할 것을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="845e1-131">앱-V 5.0 인프라에 연결할 수 없는 연결이 끊긴 원격 사용자</span><span class="sxs-lookup"><span data-stu-id="845e1-131">With disconnected remote users who cannot connect to the App-V 5.0 infrastructure.</span></span>

    -   <span data-ttu-id="845e1-132">소프트웨어 관리 시스템을 실행 중인 경우 (예: 구성 관리자 2012)</span><span class="sxs-lookup"><span data-stu-id="845e1-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="845e1-133">네트워크 대역폭 제한으로 인해 전자 소프트웨어 배포가 금지 되는 경우</span><span class="sxs-lookup"><span data-stu-id="845e1-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="845e1-134">**전체 인프라 모델** -전체 인프라 모델은 소프트웨어 배포, 관리 및 보고 기능을 제공 합니다. 또한 네트워크를 통해 응용 프로그램의 스트리밍을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="845e1-135">App-v 5.0 전체 인프라 모델은 하나 이상의 App-v 5.0 관리 서버로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-135">The App-V 5.0 Full Infrastructure Model consists of one or more App-V 5.0 management servers.</span></span> <span data-ttu-id="845e1-136">관리 서버를 사용 하 여 모든 클라이언트에 응용 프로그램을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="845e1-137">게시 프로세스에는 가상 응용 프로그램 아이콘과 바로 가기가 대상 컴퓨터에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="845e1-138">또한 응용 프로그램을 로컬 사용자에 게 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-138">It can also stream applications to local users.</span></span> <span data-ttu-id="845e1-139">관리 서버를 설치 하는 방법에 대 한 자세한 내용은 [app-v 5.0 서버 배포 계획](planning-for-the-app-v-50-server-deployment.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-139">For more information about installing the management server see, [Planning for the App-V 5.0 Server Deployment](planning-for-the-app-v-50-server-deployment.md).</span></span> <span data-ttu-id="845e1-140">전체 인프라 모델은 다음과 같은 시나리오에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="845e1-141">**중요**  앱-V 5.0 전체 인프라 모델에는 Microsoft SQL Server가 구성 데이터를 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-141">**Important** The App-V 5.0 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="845e1-142">자세한 내용은 [앱-V 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-142">For more information see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="845e1-143">관리 서버를 사용 하 여 대상 컴퓨터에 응용 프로그램을 게시 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="845e1-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="845e1-144">대상 컴퓨터에 응용 프로그램을 신속 하 게 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="845e1-145">App-v 5.0 보고 기능을 사용 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="845e1-145">When you want to use App-V 5.0 reporting.</span></span>

## <span data-ttu-id="845e1-146">엔드 투 엔드 서버 크기 조정 지침</span><span class="sxs-lookup"><span data-stu-id="845e1-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="845e1-147">다음 섹션에서는 종단간 앱-V 5.0 크기 조정 및 계획에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-147">The following section provides information about end-to-end App-V 5.0 sizing and planning.</span></span> <span data-ttu-id="845e1-148">자세한 내용은 후속 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="845e1-149">**참고**  클라이언트의 라운드트립 응답 시간은 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 게시 서버 로부터 성공적으로 알림을 수신 하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.0 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="845e1-150">게시 서버의 라운드트립 응답 시간은 게시 서버를 실행 하는 컴퓨터에서 관리 서버 로부터 성공적인 패키지 메타 데이터 업데이트를 수신 하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="845e1-151">2만 클라이언트는 단일 게시 서버를 대상으로 하 여 적절 한 라운드트립 시간에 패키지 새로 고침을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="845e1-152">( &lt; 3 초)</span><span class="sxs-lookup"><span data-stu-id="845e1-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="845e1-153">단일 관리 서버는 허용 되는 라운드트립 시간에 패키지 메타 데이터 새로 고침에 대 한 최대 50 게시 서버를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="845e1-154">( &lt; 5 초)</span><span class="sxs-lookup"><span data-stu-id="845e1-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="845e1-155">앱-V 5.0 관리 서버 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="845e1-155">App-V 5.0 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="845e1-156">앱-V 5.0 게시 서버는 패키지 새로 고침 요청과 패키지 새로 고침 응답을 위한 관리 서버가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-156">The App-V 5.0 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="845e1-157">그런 다음 관리 서버에서 정보를 검색 하기 위해 관리 데이터베이스로 정보를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="845e1-158">앱-V 5.0 관리 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-158">For more information about App-V 5.0 management server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="845e1-159">**참고**  App-v 5.0 게시 서버의 기본 새로 고침 시간은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-159">**Note** The default refresh time on the App-V 5.0 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="845e1-160">여러 동시 게시 서버가 패키지 메타 데이터 새로 고침을 위해 단일 관리 서버에 연결 되 면 다음 세 가지 요소가 게시 서버의 라운드트립 응답 시간에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="845e1-161">동시 요청을 보내는 게시 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="845e1-162">관리 서버에 구성 된 연결 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="845e1-163">관리 서버에 구성 된 액세스 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="845e1-164">다음 표에서는 라운드트립 시간에 영향을 주는 각 요소에 대 한 자세한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="845e1-165">**참고**  라운드트립 응답 시간은 관리 서버에서 성공적인 패키지 메타 데이터 업데이트를 받기 위해 App-v 5.0 게시 서버를 실행 하는 컴퓨터에 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-166">라운드트립 응답 시간에 영향을 주는 요인</span><span class="sxs-lookup"><span data-stu-id="845e1-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="845e1-167">추가 정보</span><span class="sxs-lookup"><span data-stu-id="845e1-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-168">동시에 패키지 메타 데이터 새로 고침을 요청 하는 게시 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-169">단일 관리 서버는 게시 메타 데이터를 동시에 요청 하는 최대 320 게시 서버에 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="845e1-170">320 pub 서버에 대 한 라운드트립 응답 시간은 ~ 40 초입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="845e1-171">&lt;메타 데이터를 동시에 요청 하는 50 게시 서버의 경우 라운드트립 응답 시간은 &lt; 5 초입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="845e1-172">50에서 320 게시 서버로 응답 시간이 선형적으로 증가 합니다 (약 2x).</span><span class="sxs-lookup"><span data-stu-id="845e1-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-173">관리 서버에 구성 된 연결 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-174">최대 100 개의 연결 그룹에 대해 게시 서버의 라운드트립 응답 시간이 크게 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="845e1-175">100-400 연결 그룹의 경우 라운드트립 응답 시간에 약간의 선형 증가를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-176">관리 서버에 구성 된 액세스 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-177">최대 40 액세스 그룹의 경우 게시 서버의 라운드트립 응답 시간에 선형 (약 3/3)이 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-178">다음 표에는 각 이전 요인에 대 한 예제 값이 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="845e1-179">각 변형에서 120 패키지는 App-v 5.0 관리 서버에서 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-179">In each variation, 120 packages are refreshed from the App-V 5.0management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-180">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-181">변형</span><span class="sxs-lookup"><span data-stu-id="845e1-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="845e1-182">연결 그룹 수</span><span class="sxs-lookup"><span data-stu-id="845e1-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="845e1-183">액세스 그룹 수</span><span class="sxs-lookup"><span data-stu-id="845e1-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="845e1-184">게시 서버 수</span><span class="sxs-lookup"><span data-stu-id="845e1-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="845e1-185">네트워크 연결 형식 게시 서버/관리 서버</span><span class="sxs-lookup"><span data-stu-id="845e1-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="845e1-186">게시 서버에서 라운드트립 응답 시간 (초)</span><span class="sxs-lookup"><span data-stu-id="845e1-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="845e1-187">관리 서버의 CPU 이용률</span><span class="sxs-lookup"><span data-stu-id="845e1-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-188">게시 서버는 메타 데이터 게시를 위해 관리 서버에 동시에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-189">게시 서버 수</span><span class="sxs-lookup"><span data-stu-id="845e1-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-190">0</span><span class="sxs-lookup"><span data-stu-id="845e1-190">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-191">0</span><span class="sxs-lookup"><span data-stu-id="845e1-191">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-192">0</span><span class="sxs-lookup"><span data-stu-id="845e1-192">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-193">0</span><span class="sxs-lookup"><span data-stu-id="845e1-193">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-194">0</span><span class="sxs-lookup"><span data-stu-id="845e1-194">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-195">0</span><span class="sxs-lookup"><span data-stu-id="845e1-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-196">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-196">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-197">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-197">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-198">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-198">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-199">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-199">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-200">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-200">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-201">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-202">50</span><span class="sxs-lookup"><span data-stu-id="845e1-202">50</span></span></p></li>
<li><p><span data-ttu-id="845e1-203">100</span><span class="sxs-lookup"><span data-stu-id="845e1-203">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-204">200</span><span class="sxs-lookup"><span data-stu-id="845e1-204">200</span></span></p></li>
<li><p><span data-ttu-id="845e1-205">300</span><span class="sxs-lookup"><span data-stu-id="845e1-205">300</span></span></p></li>
<li><p><span data-ttu-id="845e1-206">315</span><span class="sxs-lookup"><span data-stu-id="845e1-206">315</span></span></p></li>
<li><p><span data-ttu-id="845e1-207">320</span><span class="sxs-lookup"><span data-stu-id="845e1-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-208">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-209">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-210">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-211">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-212">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-213">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-214">5mb</span><span class="sxs-lookup"><span data-stu-id="845e1-214">5</span></span></p></li>
<li><p><span data-ttu-id="845e1-215">1천만</span><span class="sxs-lookup"><span data-stu-id="845e1-215">10</span></span></p></li>
<li><p><span data-ttu-id="845e1-216">인치</span><span class="sxs-lookup"><span data-stu-id="845e1-216">19</span></span></p></li>
<li><p><span data-ttu-id="845e1-217">32</span><span class="sxs-lookup"><span data-stu-id="845e1-217">32</span></span></p></li>
<li><p><span data-ttu-id="845e1-218">30</span><span class="sxs-lookup"><span data-stu-id="845e1-218">30</span></span></p></li>
<li><p><span data-ttu-id="845e1-219">37</span><span class="sxs-lookup"><span data-stu-id="845e1-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-220">17</span><span class="sxs-lookup"><span data-stu-id="845e1-220">17</span></span></p></li>
<li><p><span data-ttu-id="845e1-221">17</span><span class="sxs-lookup"><span data-stu-id="845e1-221">17</span></span></p></li>
<li><p><span data-ttu-id="845e1-222">17</span><span class="sxs-lookup"><span data-stu-id="845e1-222">17</span></span></p></li>
<li><p><span data-ttu-id="845e1-223">~</span><span class="sxs-lookup"><span data-stu-id="845e1-223">15</span></span></p></li>
<li><p><span data-ttu-id="845e1-224">17</span><span class="sxs-lookup"><span data-stu-id="845e1-224">17</span></span></p></li>
<li><p><span data-ttu-id="845e1-225">~</span><span class="sxs-lookup"><span data-stu-id="845e1-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-226">게시 메타 데이터에 연결 그룹 포함</span><span class="sxs-lookup"><span data-stu-id="845e1-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-227">연결 그룹 수</span><span class="sxs-lookup"><span data-stu-id="845e1-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-228">1천만</span><span class="sxs-lookup"><span data-stu-id="845e1-228">10</span></span></p></li>
<li><p><span data-ttu-id="845e1-229">50</span><span class="sxs-lookup"><span data-stu-id="845e1-229">50</span></span></p></li>
<li><p><span data-ttu-id="845e1-230">100</span><span class="sxs-lookup"><span data-stu-id="845e1-230">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-231">150</span><span class="sxs-lookup"><span data-stu-id="845e1-231">150</span></span></p></li>
<li><p><span data-ttu-id="845e1-232">300</span><span class="sxs-lookup"><span data-stu-id="845e1-232">300</span></span></p></li>
<li><p><span data-ttu-id="845e1-233">400</span><span class="sxs-lookup"><span data-stu-id="845e1-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-234">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-234">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-235">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-235">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-236">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-236">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-237">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-237">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-238">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-238">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-239">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-240">100</span><span class="sxs-lookup"><span data-stu-id="845e1-240">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-241">100</span><span class="sxs-lookup"><span data-stu-id="845e1-241">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-242">100</span><span class="sxs-lookup"><span data-stu-id="845e1-242">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-243">100</span><span class="sxs-lookup"><span data-stu-id="845e1-243">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-244">100</span><span class="sxs-lookup"><span data-stu-id="845e1-244">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-245">100</span><span class="sxs-lookup"><span data-stu-id="845e1-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-246">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-247">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-248">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-249">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-250">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-251">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-252">1천만</span><span class="sxs-lookup"><span data-stu-id="845e1-252">10</span></span></p></li>
<li><p><span data-ttu-id="845e1-253">mb</span><span class="sxs-lookup"><span data-stu-id="845e1-253">11</span></span></p></li>
<li><p><span data-ttu-id="845e1-254">mb</span><span class="sxs-lookup"><span data-stu-id="845e1-254">11</span></span></p></li>
<li><p><span data-ttu-id="845e1-255">16</span><span class="sxs-lookup"><span data-stu-id="845e1-255">16</span></span></p></li>
<li><p><span data-ttu-id="845e1-256">khz</span><span class="sxs-lookup"><span data-stu-id="845e1-256">22</span></span></p></li>
<li><p><span data-ttu-id="845e1-257">km</span><span class="sxs-lookup"><span data-stu-id="845e1-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-258">17</span><span class="sxs-lookup"><span data-stu-id="845e1-258">17</span></span></p></li>
<li><p><span data-ttu-id="845e1-259">인치</span><span class="sxs-lookup"><span data-stu-id="845e1-259">19</span></span></p></li>
<li><p><span data-ttu-id="845e1-260">khz</span><span class="sxs-lookup"><span data-stu-id="845e1-260">22</span></span></p></li>
<li><p><span data-ttu-id="845e1-261">인치</span><span class="sxs-lookup"><span data-stu-id="845e1-261">19</span></span></p></li>
<li><p><span data-ttu-id="845e1-262">명</span><span class="sxs-lookup"><span data-stu-id="845e1-262">20</span></span></p></li>
<li><p><span data-ttu-id="845e1-263">명</span><span class="sxs-lookup"><span data-stu-id="845e1-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-264">게시 메타 데이터에 액세스 그룹 포함</span><span class="sxs-lookup"><span data-stu-id="845e1-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-265">액세스 그룹 수</span><span class="sxs-lookup"><span data-stu-id="845e1-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-266">0</span><span class="sxs-lookup"><span data-stu-id="845e1-266">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-267">0</span><span class="sxs-lookup"><span data-stu-id="845e1-267">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-268">0</span><span class="sxs-lookup"><span data-stu-id="845e1-268">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-269">0</span><span class="sxs-lookup"><span data-stu-id="845e1-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-270">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-270">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-271">1천만</span><span class="sxs-lookup"><span data-stu-id="845e1-271">10</span></span></p></li>
<li><p><span data-ttu-id="845e1-272">명</span><span class="sxs-lookup"><span data-stu-id="845e1-272">20</span></span></p></li>
<li><p><span data-ttu-id="845e1-273">40</span><span class="sxs-lookup"><span data-stu-id="845e1-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-274">100</span><span class="sxs-lookup"><span data-stu-id="845e1-274">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-275">100</span><span class="sxs-lookup"><span data-stu-id="845e1-275">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-276">100</span><span class="sxs-lookup"><span data-stu-id="845e1-276">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-277">100</span><span class="sxs-lookup"><span data-stu-id="845e1-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-278">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-279">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-280">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-281">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-282">1천만</span><span class="sxs-lookup"><span data-stu-id="845e1-282">10</span></span></p></li>
<li><p><span data-ttu-id="845e1-283">43</span><span class="sxs-lookup"><span data-stu-id="845e1-283">43</span></span></p></li>
<li><p><span data-ttu-id="845e1-284">153</span><span class="sxs-lookup"><span data-stu-id="845e1-284">153</span></span></p></li>
<li><p><span data-ttu-id="845e1-285">535</span><span class="sxs-lookup"><span data-stu-id="845e1-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-286">17</span><span class="sxs-lookup"><span data-stu-id="845e1-286">17</span></span></p></li>
<li><p><span data-ttu-id="845e1-287">kbps</span><span class="sxs-lookup"><span data-stu-id="845e1-287">26</span></span></p></li>
<li><p><span data-ttu-id="845e1-288">fps</span><span class="sxs-lookup"><span data-stu-id="845e1-288">24</span></span></p></li>
<li><p><span data-ttu-id="845e1-289">fps</span><span class="sxs-lookup"><span data-stu-id="845e1-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-290">관리 서버를 실행 하는 컴퓨터의 CPU 사용률이이를 대상으로 하는 게시 서버 수에 관계 없이 25%입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="845e1-291">Microsoft SQL Server 데이터베이스 트랜잭션/초, 일괄 처리 요청/초 및 사용자 연결은 게시 서버 수에 관계 없이 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="845e1-292">예를 들어, 초당 거래 수는 ~ 30, 일괄 처리 요청 ~ 200, 사용자 연결 ~ 6이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="845e1-293">관리 서버 & 게시 서버는 서로 느린 연결 네트워크를 사용 하는 지리적 분산 배포를 통해 &lt; 단일 관리 서버에 대 한 100 동시 요청에도 게시 서버의 라운드트립 응답 시간이 허용 되는 시간 제한 (5 초) 내에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-294">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-295">변형</span><span class="sxs-lookup"><span data-stu-id="845e1-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="845e1-296">연결 그룹 수</span><span class="sxs-lookup"><span data-stu-id="845e1-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="845e1-297">액세스 그룹 수</span><span class="sxs-lookup"><span data-stu-id="845e1-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="845e1-298">게시 서버 수</span><span class="sxs-lookup"><span data-stu-id="845e1-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="845e1-299">네트워크 연결 형식 게시 서버/관리 서버</span><span class="sxs-lookup"><span data-stu-id="845e1-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="845e1-300">게시 서버에서 라운드트립 응답 시간 (초)</span><span class="sxs-lookup"><span data-stu-id="845e1-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="845e1-301">관리 서버의 CPU 이용률</span><span class="sxs-lookup"><span data-stu-id="845e1-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-302">게시 서버와 관리 서버 간의 네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="845e1-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-303">1.5 Mbps 느린 연결 네트워크</span><span class="sxs-lookup"><span data-stu-id="845e1-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-304">0</span><span class="sxs-lookup"><span data-stu-id="845e1-304">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-305">0</span><span class="sxs-lookup"><span data-stu-id="845e1-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-306">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-306">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-307">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-308">50</span><span class="sxs-lookup"><span data-stu-id="845e1-308">50</span></span></p></li>
<li><p><span data-ttu-id="845e1-309">100</span><span class="sxs-lookup"><span data-stu-id="845e1-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-310">1.5 mbps 케이블 DSL</span><span class="sxs-lookup"><span data-stu-id="845e1-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="845e1-311">1.5 mbps 케이블 DSL</span><span class="sxs-lookup"><span data-stu-id="845e1-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-312">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="845e1-312">4</span></span></p></li>
<li><p><span data-ttu-id="845e1-313">5mb</span><span class="sxs-lookup"><span data-stu-id="845e1-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-314">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-314">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-315">2</span><span class="sxs-lookup"><span data-stu-id="845e1-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-316">게시 서버와 관리 서버 간의 네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="845e1-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-317">LAN/WIFI 네트워크</span><span class="sxs-lookup"><span data-stu-id="845e1-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-318">0</span><span class="sxs-lookup"><span data-stu-id="845e1-318">0</span></span></p></li>
<li><p><span data-ttu-id="845e1-319">0</span><span class="sxs-lookup"><span data-stu-id="845e1-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-320">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-320">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-321">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-322">100</span><span class="sxs-lookup"><span data-stu-id="845e1-322">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-323">200</span><span class="sxs-lookup"><span data-stu-id="845e1-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-324">Wifi</span><span class="sxs-lookup"><span data-stu-id="845e1-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="845e1-325">Wifi</span><span class="sxs-lookup"><span data-stu-id="845e1-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-326">mb</span><span class="sxs-lookup"><span data-stu-id="845e1-326">11</span></span></p></li>
<li><p><span data-ttu-id="845e1-327">명</span><span class="sxs-lookup"><span data-stu-id="845e1-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-328">~</span><span class="sxs-lookup"><span data-stu-id="845e1-328">15</span></span></p></li>
<li><p><span data-ttu-id="845e1-329">17</span><span class="sxs-lookup"><span data-stu-id="845e1-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-330">관리 서버와 게시 서버가 느린 연결 네트워크 또는 고속 네트워크를 통해 연결 되어 있는지 여부에 관계 없이 관리 서버는 약 15000 패키지 새로 고침 요청을 30 분 내에 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="845e1-331">앱-V 5.0 보고 서버 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="845e1-331">App-V 5.0 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="845e1-332">App-v 5.0 클라이언트 보고 데이터를 보고 서버로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-332">App-V 5.0 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="845e1-333">그러면 보고 서버는 Microsoft SQL Server 데이터베이스에 정보를 기록 하 고 App-v 5.0 클라이언트를 실행 하는 컴퓨터에 성공적으로 다시 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.0 client.</span></span> <span data-ttu-id="845e1-334">앱-V 5.0 보고 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-334">For more information about App-V 5.0 Reporting Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="845e1-335">**참고**  라운드트립 응답 시간은 reporting server에 보고 정보를 보내고 보고 서버에서 성공적으로 알림을 받기 위해 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 수행 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-336">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-337">요약</span><span class="sxs-lookup"><span data-stu-id="845e1-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-338">여러 App-v 5.0 클라이언트는 보고 정보를 보고 서버에 동시에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-338">Multiple App-V 5.0 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-339">보고 서버의 라운드트립 응답 시간은 500 클라이언트에 2.6 초입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="845e1-340">보고 서버의 라운드트립 응답 시간은 1000 클라이언트에 5.65 초입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="845e1-341">라운드 트립 응답 시간은 클라이언트 수에 따라 선형적으로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-342">보고 서버에서 처리 한 초당 요청 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-343">단일 보고 서버와 단일 데이터베이스는 초당 최대 139 개의 요청을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="845e1-344">평균은 121 요청/초입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="845e1-345">동일한 Microsoft SQL Server 데이터베이스에 보고 하는 두 개의 보고 서버를 사용 하는 경우 평균 요청/초는 단일 보고 서버 = ~ 127와 비슷하지만 최대 278 요청 수는 초입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="845e1-346">단일 보고 서버는 500 동시/활성 연결을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="845e1-347">단일 보고 서버는 최대 1500 동시 연결을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-348">보고 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="845e1-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-349">Microsoft SQL Server를 실행 하는 컴퓨터의 잠금 경합은 초당 요청에 대 한 제한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="845e1-350">처리량 및 응답 시간은 데이터베이스 크기와 무관 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-351">**임의 지연 계산**:</span><span class="sxs-lookup"><span data-stu-id="845e1-351">**Calculating random delay**:</span></span>

<span data-ttu-id="845e1-352">임의 지연은 보고 서버로 전송 되는 데이터의 최대 지연 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="845e1-353">예약 된 작업이 시작 되 면 클라이언트는 **0** 과 **ReportingRandomDelay** 사이의 임의 지연 시간을 생성 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="845e1-354">임의 지연 = 4 \ \* 클라이언트 수/초 당 평균 요청</span><span class="sxs-lookup"><span data-stu-id="845e1-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="845e1-355">예: 500 클라이언트의 경우 초당 120 요청이 있는 경우 임의 지연은 4 \ \* 500/120 = ~ 17 분입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="845e1-356">앱-V 5.0 게시 서버 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="845e1-356">App-V 5.0 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="845e1-357">App-v 5.0 클라이언트를 실행 하는 컴퓨터는 앱 V 5.0 게시 서버에 연결 하 여 게시 새로 고침 요청을 보내고 응답을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-357">Computers running the App-V 5.0 client connect to the App-V 5.0 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="845e1-358">라운드 트립 응답 시간은 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 측정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-358">Round trip response time is measured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="845e1-359">프로세서 시간은 게시 서버에서 측정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="845e1-360">앱-V 5.0 게시 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.0 지원 되는 구성을](app-v-50-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="845e1-360">For more information about App-V 5.0 Publishing Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="845e1-361">**중요**  다음 목록에는 App-v 5.0 게시 서버를 설정할 때 고려해 야 하는 주요 요소가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.0 publishing server:</span></span>

-   <span data-ttu-id="845e1-362">단일 게시 서버에 동시에 연결 하는 클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="845e1-363">각 새로 고침의 패키지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="845e1-364">클라이언트와 App-v 5.0 게시 서버 간의 환경에서 사용할 수 있는 네트워크 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-364">The available network bandwidth in your environment between the client and the App-V 5.0 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-365">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-366">요약</span><span class="sxs-lookup"><span data-stu-id="845e1-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-367">여러 App-v 5.0 클라이언트는 단일 게시 서버에 동시에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-367">Multiple App-V 5.0 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-368">듀얼 코어 프로세서를 실행 하는 게시 서버는 동시에 새로 고침을 요청 하는 최대 5000 클라이언트에 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="845e1-369">5000-10000 클라이언트의 경우 게시 서버에는 최소 쿼드 코어가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="845e1-370">10000-20000 클라이언트의 경우 더 효율적인 응답 시간을 위해 게시 서버에 듀얼 쿼드 코어를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="845e1-371">쿼드 코어를 사용 하는 게시 서버는 3 초 내에 1만 패키지를 새로 고칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="845e1-372">(1만 동시 클라이언트 지원)</span><span class="sxs-lookup"><span data-stu-id="845e1-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-373">새로 고칠 때마다 패키지의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-374">패키지 수를 늘리면 응답 시간이 ~ 40% (최대 1000 패키지)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-375">App-v 5.0 클라이언트와 게시 서버 간의 네트워크.</span><span class="sxs-lookup"><span data-stu-id="845e1-375">Network between the App-V 5.0 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-376">느린 네트워크 (1.5 Mbps 대역폭)에서 LAN (최대 1000 명의 사용자)과 비교 하 여 응답 시간이 97% 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-377">**참고**  게시 서버 CPU 사용은 동시 요청 ( &gt; 대부분의 경우 90%)을 처리 해야 하는 시간 간격 동안 항상 높습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="845e1-378">게시 서버는 1 초에 ~ 1500 클라이언트 요청을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-379">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-380">변형</span><span class="sxs-lookup"><span data-stu-id="845e1-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="845e1-381">앱-V 5.0 클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="845e1-381">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="845e1-382">패키지 수</span><span class="sxs-lookup"><span data-stu-id="845e1-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="845e1-383">게시 서버의 프로세서 구성</span><span class="sxs-lookup"><span data-stu-id="845e1-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="845e1-384">네트워크 연결 형식 게시 서버/App-v 5.0 클라이언트</span><span class="sxs-lookup"><span data-stu-id="845e1-384">Network connection type publishing server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="845e1-385">App-v 5.0 클라이언트 (초)에 대 한 왕복 시간</span><span class="sxs-lookup"><span data-stu-id="845e1-385">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="845e1-386">게시 서버의 CPU 사용률 (%)</span><span class="sxs-lookup"><span data-stu-id="845e1-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-387">App-v 5.0 클라이언트에서 게시 새로 고침 요청이 &amp; 응답을 수신 하 고, 각 요청이 120 패키지를 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-387">App-V 5.0 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-388">클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="845e1-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-389">100</span><span class="sxs-lookup"><span data-stu-id="845e1-389">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-390">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-390">1000</span></span></p></li>
<li><p><span data-ttu-id="845e1-391">5000</span><span class="sxs-lookup"><span data-stu-id="845e1-391">5000</span></span></p></li>
<li><p><span data-ttu-id="845e1-392">1만</span><span class="sxs-lookup"><span data-stu-id="845e1-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-393">120</span><span class="sxs-lookup"><span data-stu-id="845e1-393">120</span></span></p></li>
<li><p><span data-ttu-id="845e1-394">120</span><span class="sxs-lookup"><span data-stu-id="845e1-394">120</span></span></p></li>
<li><p><span data-ttu-id="845e1-395">120</span><span class="sxs-lookup"><span data-stu-id="845e1-395">120</span></span></p></li>
<li><p><span data-ttu-id="845e1-396">120</span><span class="sxs-lookup"><span data-stu-id="845e1-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-397">듀얼 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="845e1-398">듀얼 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="845e1-399">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="845e1-400">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-401">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-402">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-403">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-404">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-405">raid-1</span><span class="sxs-lookup"><span data-stu-id="845e1-405">1</span></span></p></li>
<li><p><span data-ttu-id="845e1-406">2</span><span class="sxs-lookup"><span data-stu-id="845e1-406">2</span></span></p></li>
<li><p><span data-ttu-id="845e1-407">2</span><span class="sxs-lookup"><span data-stu-id="845e1-407">2</span></span></p></li>
<li><p><span data-ttu-id="845e1-408">3-4</span><span class="sxs-lookup"><span data-stu-id="845e1-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-409">100</span><span class="sxs-lookup"><span data-stu-id="845e1-409">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-410">99</span><span class="sxs-lookup"><span data-stu-id="845e1-410">99</span></span></p></li>
<li><p><span data-ttu-id="845e1-411">89</span><span class="sxs-lookup"><span data-stu-id="845e1-411">89</span></span></p></li>
<li><p><span data-ttu-id="845e1-412">77</span><span class="sxs-lookup"><span data-stu-id="845e1-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-413">각 새로 고침의 여러 패키지</span><span class="sxs-lookup"><span data-stu-id="845e1-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-414">패키지 수</span><span class="sxs-lookup"><span data-stu-id="845e1-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-415">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-415">1000</span></span></p></li>
<li><p><span data-ttu-id="845e1-416">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-417">500</span><span class="sxs-lookup"><span data-stu-id="845e1-417">500</span></span></p></li>
<li><p><span data-ttu-id="845e1-418">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-419">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="845e1-420">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-421">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-422">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-423">2</span><span class="sxs-lookup"><span data-stu-id="845e1-423">2</span></span></p></li>
<li><p><span data-ttu-id="845e1-424">3-4</span><span class="sxs-lookup"><span data-stu-id="845e1-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-425">92</span><span class="sxs-lookup"><span data-stu-id="845e1-425">92</span></span></p></li>
<li><p><span data-ttu-id="845e1-426">91</span><span class="sxs-lookup"><span data-stu-id="845e1-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-427">클라이언트와 게시 서버 간의 네트워크</span><span class="sxs-lookup"><span data-stu-id="845e1-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-428">1.5 Mbps 느린 연결 네트워크</span><span class="sxs-lookup"><span data-stu-id="845e1-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-429">100</span><span class="sxs-lookup"><span data-stu-id="845e1-429">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-430">500</span><span class="sxs-lookup"><span data-stu-id="845e1-430">500</span></span></p></li>
<li><p><span data-ttu-id="845e1-431">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-432">120</span><span class="sxs-lookup"><span data-stu-id="845e1-432">120</span></span></p></li>
<li><p><span data-ttu-id="845e1-433">120</span><span class="sxs-lookup"><span data-stu-id="845e1-433">120</span></span></p></li>
<li><p><span data-ttu-id="845e1-434">120</span><span class="sxs-lookup"><span data-stu-id="845e1-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-435">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="845e1-436">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="845e1-437">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="845e1-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-438">1.5 Mbps 내 대륙과 네트워크</span><span class="sxs-lookup"><span data-stu-id="845e1-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-439">3-4</span><span class="sxs-lookup"><span data-stu-id="845e1-439">3</span></span></p></li>
<li><p><span data-ttu-id="845e1-440">10 (0.2% 실패 율)</span><span class="sxs-lookup"><span data-stu-id="845e1-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="845e1-441">17 (1% 실패 율 사용)</span><span class="sxs-lookup"><span data-stu-id="845e1-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="845e1-442">앱-V 5.0 스트리밍 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="845e1-442">App-V 5.0 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="845e1-443">앱-V 5.0 클라이언트를 실행 하는 컴퓨터는 스트리밍 서버에서 가상 응용 프로그램 패키지를 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-443">Computers running the App-V 5.0 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="845e1-444">라운드트립 응답 시간은 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 측정 되며 전체 패키지를 스트리밍하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-444">Round trip response time is measured on the computer running the App-V 5.0 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="845e1-445">**중요**  다음 목록에서는 App-v 5.0 스트리밍 서버를 설정할 때 고려해 야 하는 주요 요인을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.0 streaming server:</span></span>

-   <span data-ttu-id="845e1-446">단일 스트리밍 서버에서 응용 프로그램 패키지를 동시에 스트리밍하는 클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="845e1-447">스트리밍 중인 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="845e1-448">클라이언트와 스트리밍 서버 간의 환경에서 사용할 수 있는 네트워크 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-449">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-450">요약</span><span class="sxs-lookup"><span data-stu-id="845e1-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-451">여러 App-v 5.0 클라이언트는 단일 스트리밍 서버에서 동시에 응용 프로그램을 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-451">Multiple App-V 5.0 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-452">동일한 서버에서 동시에 스트리밍하는 클라이언트 수가 늘어나면 패키지 다운로드/스트리밍 시간에 대 한 선형 관계가 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-453">스트리밍 중인 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-454">패키지 크기는 크기가 ~ 1GB 인 대용량 패키지에 대해서만 스트리밍/다운로드 시간에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="845e1-455">3 MB에서 100 MB 까지의 패키지 크기에 대 한 스트리밍 시간은 20 초에서 100 초로, 100 동시 클라이언트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-456">App-v 5.0 클라이언트와 스트리밍 서버 간의 네트워크.</span><span class="sxs-lookup"><span data-stu-id="845e1-456">Network between the App-V 5.0 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-457">느린 네트워크 (1.5 Mbps 대역폭)에서 LAN (최대 100 명의 사용자)과 비교 하 여 응답 시간이 70-80% 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-458">다음 표에는 이전 목록의 각 요소에 대 한 예제 값이 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="845e1-459">시나리오</span><span class="sxs-lookup"><span data-stu-id="845e1-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="845e1-460">변형</span><span class="sxs-lookup"><span data-stu-id="845e1-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="845e1-461">앱-V 5.0 클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="845e1-461">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="845e1-462">각 패키지의 크기</span><span class="sxs-lookup"><span data-stu-id="845e1-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="845e1-463">네트워크 연결 형식 스트리밍 서버/App-v 5.0 클라이언트</span><span class="sxs-lookup"><span data-stu-id="845e1-463">Network connection type streaming server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="845e1-464">App-v 5.0 클라이언트 (초)에 대 한 왕복 시간</span><span class="sxs-lookup"><span data-stu-id="845e1-464">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-465">여러 앱-V 5.0 클라이언트는 스트리밍 서버에서 가상 응용 프로그램 패키지를 스트리밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-465">Multiple App-V 5.0 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-466">클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-467">100</span><span class="sxs-lookup"><span data-stu-id="845e1-467">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-468">200</span><span class="sxs-lookup"><span data-stu-id="845e1-468">200</span></span></p></li>
<li><p><span data-ttu-id="845e1-469">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-470">100</span><span class="sxs-lookup"><span data-stu-id="845e1-470">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-471">200</span><span class="sxs-lookup"><span data-stu-id="845e1-471">200</span></span></p></li>
<li><p><span data-ttu-id="845e1-472">1000</span><span class="sxs-lookup"><span data-stu-id="845e1-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-473">3.5MB</span><span class="sxs-lookup"><span data-stu-id="845e1-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="845e1-474">3.5MB</span><span class="sxs-lookup"><span data-stu-id="845e1-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="845e1-475">3.5MB</span><span class="sxs-lookup"><span data-stu-id="845e1-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-476">5mb</span><span class="sxs-lookup"><span data-stu-id="845e1-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="845e1-477">5mb</span><span class="sxs-lookup"><span data-stu-id="845e1-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="845e1-478">5mb</span><span class="sxs-lookup"><span data-stu-id="845e1-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-479">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-480">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-481">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-482">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-483">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-484">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-485">개가</span><span class="sxs-lookup"><span data-stu-id="845e1-485">29</span></span></p></li>
<li><p><span data-ttu-id="845e1-486">39</span><span class="sxs-lookup"><span data-stu-id="845e1-486">39</span></span></p></li>
<li><p><span data-ttu-id="845e1-487">391</span><span class="sxs-lookup"><span data-stu-id="845e1-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-488">35</span><span class="sxs-lookup"><span data-stu-id="845e1-488">35</span></span></p></li>
<li><p><span data-ttu-id="845e1-489">68</span><span class="sxs-lookup"><span data-stu-id="845e1-489">68</span></span></p></li>
<li><p><span data-ttu-id="845e1-490">461</span><span class="sxs-lookup"><span data-stu-id="845e1-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="845e1-491">스트리밍된 각 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-492">각 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-493">100</span><span class="sxs-lookup"><span data-stu-id="845e1-493">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-494">200</span><span class="sxs-lookup"><span data-stu-id="845e1-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-495">100</span><span class="sxs-lookup"><span data-stu-id="845e1-495">100</span></span></p></li>
<li><p><span data-ttu-id="845e1-496">200</span><span class="sxs-lookup"><span data-stu-id="845e1-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-497">21MB</span><span class="sxs-lookup"><span data-stu-id="845e1-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="845e1-498">21MB</span><span class="sxs-lookup"><span data-stu-id="845e1-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-499">109</span><span class="sxs-lookup"><span data-stu-id="845e1-499">109</span></span></p></li>
<li><p><span data-ttu-id="845e1-500">109</span><span class="sxs-lookup"><span data-stu-id="845e1-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-501">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-502">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-503">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="845e1-504">LAN</span><span class="sxs-lookup"><span data-stu-id="845e1-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="845e1-505">33</span><span class="sxs-lookup"><span data-stu-id="845e1-505">33</span></span></p>
<p><span data-ttu-id="845e1-506">83</span><span class="sxs-lookup"><span data-stu-id="845e1-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="845e1-507">100</span><span class="sxs-lookup"><span data-stu-id="845e1-507">100</span></span></p>
<p><span data-ttu-id="845e1-508">160</span><span class="sxs-lookup"><span data-stu-id="845e1-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="845e1-509">클라이언트와 App-v 5.0 스트리밍 서버 간의 네트워크 연결.</span><span class="sxs-lookup"><span data-stu-id="845e1-509">Network connection between client and App-V 5.0 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="845e1-510">1.5 Mbps 느린 연결 네트워크.</span><span class="sxs-lookup"><span data-stu-id="845e1-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-511">100</span><span class="sxs-lookup"><span data-stu-id="845e1-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-512">100</span><span class="sxs-lookup"><span data-stu-id="845e1-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-513">3.5MB</span><span class="sxs-lookup"><span data-stu-id="845e1-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="845e1-514">5mb</span><span class="sxs-lookup"><span data-stu-id="845e1-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="845e1-515">1.5 Mbps 내 대륙과 네트워크</span><span class="sxs-lookup"><span data-stu-id="845e1-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="845e1-516">102</span><span class="sxs-lookup"><span data-stu-id="845e1-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="845e1-517">121</span><span class="sxs-lookup"><span data-stu-id="845e1-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="845e1-518">각 App-v 5.0 스트리밍 서버는 가상화 된 응용 프로그램을 동시에 스트리밍하는 최소 200 클라이언트를 처리할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-518">Each App-V 5.0 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="845e1-519">**참고**  실제로 스트림 하는 데 걸리는 실제 시간은 동시 스트리밍 클라이언트 수, 패키지 수, 패키지 크기, 서버의 네트워크 활동 및 네트워크 상태에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="845e1-520">예를 들어, 100 동시 클라이언트가 서버에서 스트리밍하는 경우 평균 사용자는 2 분 이내에 100 MB 패키지를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="845e1-521">그러나 크기가 1 GB 인 패키지는 최대 30 분까지 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="845e1-522">대부분의 실제 환경에서는 스트리밍 요구가 일관 되 게 분산 되지 않으며, 필요한 스트리밍 서버 수의 크기를 적절히 조정 하기 위해 해당 환경에 존재 하는 대략적인 최대 스트리밍 요구 사항을 이해 하는 것이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="845e1-523">스트리밍 서버가 지원할 수 있는 클라이언트 수가 현저 하 게 늘어나고, 응용 프로그램을 미리 캐시 하는 경우 최대 스트리밍 요구 사항이 줄어들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="845e1-524">또한 요청에 따라 스트리밍 서버에서 지원 되는 클라이언트 수를 늘리면 최적화 된 패키지를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="845e1-525">앱-V 5.0 서버 역할 결합</span><span class="sxs-lookup"><span data-stu-id="845e1-525">Combining App-V 5.0 Server Roles</span></span>


<span data-ttu-id="845e1-526">확장 및 내결함성 요구 사항을 Discounting Active Directory에 연결 된 위치에 필요한 최소 서버 수가 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="845e1-527">이 서버는 관리 서버, 관리 서버 서비스 및 Microsoft SQL Server 역할을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="845e1-528">따라서 서버 역할은 서로 충돌 하지 않으므로 원하는 조합으로 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="845e1-529">크기 조정 요구 사항을 무시 하 여 오류 허용 구현을 제공 하는 데 필요한 최소 서버 수는 4 개입니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="845e1-530">관리 서버 및 Microsoft SQL Server 역할은 내결함성이 있는 구성에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="845e1-531">관리 서버 서비스를 역할 중 하 나와 결합할 수 있지만, 단일 오류 지점이 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="845e1-532">내결함성이 많은 전략과 기술이 제공 되는 것은 아니지만, 제공 되는 서비스에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="845e1-533">또한 App-v 5.0 역할이 결합 된 경우 비 호환성으로 인해 특정 내결함성 옵션이 더 이상 적용 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="845e1-533">Additionally, if App-V 5.0 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="845e1-534">관련 항목</span><span class="sxs-lookup"><span data-stu-id="845e1-534">Related topics</span></span>


[<span data-ttu-id="845e1-535">App-V 5.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="845e1-535">App-V 5.0 Supported Configurations</span></span>](app-v-50-supported-configurations.md)

[<span data-ttu-id="845e1-536">App-V 5.0을 사용한 고가용성 계획</span><span class="sxs-lookup"><span data-stu-id="845e1-536">Planning for High Availability with App-V 5.0</span></span>](planning-for-high-availability-with-app-v-50.md)

[<span data-ttu-id="845e1-537">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="845e1-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





