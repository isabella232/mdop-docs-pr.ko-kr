---
title: App-V 5.1 용량 계획
description: App-V 5.1 용량 계획
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814785"
---
# <span data-ttu-id="64a9c-103">App-V 5.1 용량 계획</span><span class="sxs-lookup"><span data-stu-id="64a9c-103">App-V 5.1 Capacity Planning</span></span>


<span data-ttu-id="64a9c-104">다음 권장 사항은 조직의 App-v 5.1 인프라에 적합 한 용량 계획 정보를 결정 하는 데 도움이 되는 기준으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.1 infrastructure.</span></span>

<span data-ttu-id="64a9c-105">**중요**  이 섹션의 정보는 App-v 5.1 배포 계획을 위한 일반적인 가이드로만 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.1 deployment.</span></span> <span data-ttu-id="64a9c-106">시스템 용량 요구 사항은 하드웨어 및 응용 프로그램 환경의 특정 정보에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="64a9c-107">또한이 문서에 표시 되는 성과 번호는 예제 이며 결과는 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="64a9c-108">프로젝트 범위 결정</span><span class="sxs-lookup"><span data-stu-id="64a9c-108">Determine the Project Scope</span></span>


<span data-ttu-id="64a9c-109">App-v 5.1 인프라를 디자인 하기 전에 프로젝트의 범위를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-109">Before you design the App-V 5.1 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="64a9c-110">범위는 사실상 사용할 수 있는 응용 프로그램을 결정 하 고 대상 사용자 및 해당 위치를 식별 하는 데에도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="64a9c-111">이 정보는 구현 해야 하는 App-v 5.1 인프라 유형을 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-111">This information will help determine what type of App-V 5.1 infrastructure should be implemented.</span></span> <span data-ttu-id="64a9c-112">프로젝트 범위에 대 한 결정은 조직의 특정 요구 사항에 근거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64a9c-113">작업</span><span class="sxs-lookup"><span data-stu-id="64a9c-113">Task</span></span></th>
<th align="left"><span data-ttu-id="64a9c-114">추가 정보</span><span class="sxs-lookup"><span data-stu-id="64a9c-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-115">응용 프로그램 범위 결정</span><span class="sxs-lookup"><span data-stu-id="64a9c-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-116">가상화 할 응용 프로그램에 따라 App-v 5.1 인프라를 다양 한 방식으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-116">Depending on the applications to be virtualized, the App-V 5.1 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="64a9c-117">첫 번째 작업은 가상화 하려는 응용 프로그램을 정의 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-118">위치 범위 결정</span><span class="sxs-lookup"><span data-stu-id="64a9c-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-119">위치 범위는 가상 응용 프로그램을 실행할 계획인 실제 위치 (예: enterprise 전체 또는 특정 지리적 위치)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="64a9c-120">또한 가상 응용 프로그램을 실행 하는 사용자 집단 (예: 단일 부서)을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="64a9c-121">연결 경로 뿐만 아니라 각 위치에 대 한 사용 가능한 대역폭과 가상화 된 응용 프로그램을 사용 하는 사용자 수 및 WAN 연결 속도를 포함 하는 네트워크 맵을 구해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="64a9c-122">어떤 App-v 5.1 인프라가 필요 하다는 것을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-122">Determine Which App-V 5.1 Infrastructure is Required</span></span>


<span data-ttu-id="64a9c-123">**중요**  다음 두 모델에서는 가상 응용 프로그램을 실행 하려는 컴퓨터에 App-v 5.1 클라이언트를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-123">**Important** Both of the following models require the App-V 5.1 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="64a9c-124">Microsoft 시스템 센터 구성 관리자와 같은 ESD (전자 소프트웨어 배포) 솔루션을 사용 하 여 App-v 5.1 환경을 관리할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-124">You can also manage your App-V 5.1 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="64a9c-125">자세한 내용은 [전자 소프트웨어 배포를 사용 하 여 app-v 5.1 패키지를 배포 하는 방법을](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-125">For more information see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

 

-   <span data-ttu-id="64a9c-126">**독립 실행형 모델** -독립 실행형 모델을 통해 가상 응용 프로그램을 Windows Installer로 설정 하 여 스트리밍 없이 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="64a9c-127">독립 실행형 모드의 app-v 5.1는 시퀀서 및 클라이언트로 구성 됩니다. 추가 구성 요소가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-127">App-V 5.1 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="64a9c-128">시퀀싱 이라는 프로세스를 사용 하 여 응용 프로그램의 가상화를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="64a9c-129">자세한 내용은 [앱-V 5.1 시퀀서 및 클라이언트 배포 계획](planning-for-the-app-v-51-sequencer-and-client-deployment.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-129">For more information see, [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="64a9c-130">다음과 같은 시나리오에는 독립 실행형 모델을 사용할 것을 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="64a9c-131">앱-V 5.1 인프라에 연결할 수 없는 연결이 끊긴 원격 사용자</span><span class="sxs-lookup"><span data-stu-id="64a9c-131">With disconnected remote users who cannot connect to the App-V 5.1 infrastructure.</span></span>

    -   <span data-ttu-id="64a9c-132">소프트웨어 관리 시스템을 실행 중인 경우 (예: 구성 관리자 2012)</span><span class="sxs-lookup"><span data-stu-id="64a9c-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="64a9c-133">네트워크 대역폭 제한으로 인해 전자 소프트웨어 배포가 금지 되는 경우</span><span class="sxs-lookup"><span data-stu-id="64a9c-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="64a9c-134">**전체 인프라 모델** -전체 인프라 모델은 소프트웨어 배포, 관리 및 보고 기능을 제공 합니다. 또한 네트워크를 통해 응용 프로그램의 스트리밍을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="64a9c-135">App-v 5.1 전체 인프라 모델은 하나 이상의 App-v 5.1 관리 서버로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-135">The App-V 5.1 Full Infrastructure Model consists of one or more App-V 5.1 management servers.</span></span> <span data-ttu-id="64a9c-136">관리 서버를 사용 하 여 모든 클라이언트에 응용 프로그램을 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="64a9c-137">게시 프로세스에는 가상 응용 프로그램 아이콘과 바로 가기가 대상 컴퓨터에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="64a9c-138">또한 응용 프로그램을 로컬 사용자에 게 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-138">It can also stream applications to local users.</span></span> <span data-ttu-id="64a9c-139">관리 서버를 설치 하는 방법에 대 한 자세한 내용은 [app-v 5.1 서버 배포 계획](planning-for-the-app-v-51-server-deployment.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-139">For more information about installing the management server see, [Planning for the App-V 5.1 Server Deployment](planning-for-the-app-v-51-server-deployment.md).</span></span> <span data-ttu-id="64a9c-140">전체 인프라 모델은 다음과 같은 시나리오에 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="64a9c-141">**중요**  앱-V 5.1 전체 인프라 모델에는 Microsoft SQL Server가 구성 데이터를 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-141">**Important** The App-V 5.1 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="64a9c-142">자세한 내용은 [앱-V 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-142">For more information see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="64a9c-143">관리 서버를 사용 하 여 대상 컴퓨터에 응용 프로그램을 게시 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="64a9c-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="64a9c-144">대상 컴퓨터에 응용 프로그램을 신속 하 게 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="64a9c-145">App-v 5.1 보고 기능을 사용 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="64a9c-145">When you want to use App-V 5.1 reporting.</span></span>

## <span data-ttu-id="64a9c-146">엔드 투 엔드 서버 크기 조정 지침</span><span class="sxs-lookup"><span data-stu-id="64a9c-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="64a9c-147">다음 섹션에서는 종단간 앱-V 5.1 크기 조정 및 계획에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-147">The following section provides information about end-to-end App-V 5.1 sizing and planning.</span></span> <span data-ttu-id="64a9c-148">자세한 내용은 후속 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="64a9c-149">**참고**  클라이언트의 라운드트립 응답 시간은 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 게시 서버 로부터 성공적으로 알림을 수신 하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.1 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="64a9c-150">게시 서버의 라운드트립 응답 시간은 게시 서버를 실행 하는 컴퓨터에서 관리 서버 로부터 성공적인 패키지 메타 데이터 업데이트를 수신 하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="64a9c-151">2만 클라이언트는 단일 게시 서버를 대상으로 하 여 적절 한 라운드트립 시간에 패키지 새로 고침을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="64a9c-152">( &lt; 3 초)</span><span class="sxs-lookup"><span data-stu-id="64a9c-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="64a9c-153">단일 관리 서버는 허용 되는 라운드트립 시간에 패키지 메타 데이터 새로 고침에 대 한 최대 50 게시 서버를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="64a9c-154">( &lt; 5 초)</span><span class="sxs-lookup"><span data-stu-id="64a9c-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="64a9c-155">앱-V 5.1 관리 서버 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="64a9c-155">App-V 5.1 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="64a9c-156">앱-V 5.1 게시 서버는 패키지 새로 고침 요청과 패키지 새로 고침 응답을 위한 관리 서버가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-156">The App-V 5.1 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="64a9c-157">그런 다음 관리 서버에서 정보를 검색 하기 위해 관리 데이터베이스로 정보를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="64a9c-158">앱-V 5.1 관리 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-158">For more information about App-V 5.1 management server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="64a9c-159">**참고**  App-v 5.1 게시 서버의 기본 새로 고침 시간은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-159">**Note** The default refresh time on the App-V 5.1 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="64a9c-160">여러 동시 게시 서버가 패키지 메타 데이터 새로 고침을 위해 단일 관리 서버에 연결 되 면 다음 세 가지 요소가 게시 서버의 라운드트립 응답 시간에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="64a9c-161">동시 요청을 보내는 게시 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="64a9c-162">관리 서버에 구성 된 연결 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="64a9c-163">관리 서버에 구성 된 액세스 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="64a9c-164">다음 표에서는 라운드트립 시간에 영향을 주는 각 요소에 대 한 자세한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="64a9c-165">**참고**  라운드트립 응답 시간은 관리 서버에서 성공적인 패키지 메타 데이터 업데이트를 받기 위해 App-v 5.1 게시 서버를 실행 하는 컴퓨터에 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64a9c-166">라운드트립 응답 시간에 영향을 주는 요인</span><span class="sxs-lookup"><span data-stu-id="64a9c-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="64a9c-167">추가 정보</span><span class="sxs-lookup"><span data-stu-id="64a9c-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-168">동시에 패키지 메타 데이터 새로 고침을 요청 하는 게시 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-169">단일 관리 서버는 게시 메타 데이터를 동시에 요청 하는 최대 320 게시 서버에 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-170">320 pub 서버에 대 한 라운드트립 응답 시간은 ~ 40 초입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-171">&lt;메타 데이터를 동시에 요청 하는 50 게시 서버의 경우 라운드트립 응답 시간은 &lt; 5 초입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-172">50에서 320 게시 서버로 응답 시간이 선형적으로 증가 합니다 (약 2x).</span><span class="sxs-lookup"><span data-stu-id="64a9c-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-173">관리 서버에 구성 된 연결 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-174">최대 100 개의 연결 그룹에 대해 게시 서버의 라운드트립 응답 시간이 크게 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-175">100-400 연결 그룹의 경우 라운드트립 응답 시간에 약간의 선형 증가를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-176">관리 서버에 구성 된 액세스 그룹의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-177">최대 40 액세스 그룹의 경우 게시 서버의 라운드트립 응답 시간에 선형 (약 3/3)이 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-178">다음 표에는 각 이전 요인에 대 한 예제 값이 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="64a9c-179">각 변형에서 120 패키지는 App-v 5.1 관리 서버에서 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-179">In each variation, 120 packages are refreshed from the App-V 5.1management server.</span></span>

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
<th align="left"><span data-ttu-id="64a9c-180">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-181">변형</span><span class="sxs-lookup"><span data-stu-id="64a9c-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="64a9c-182">연결 그룹 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="64a9c-183">액세스 그룹 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="64a9c-184">게시 서버 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="64a9c-185">네트워크 연결 형식 게시 서버/관리 서버</span><span class="sxs-lookup"><span data-stu-id="64a9c-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="64a9c-186">게시 서버에서 라운드트립 응답 시간 (초)</span><span class="sxs-lookup"><span data-stu-id="64a9c-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="64a9c-187">관리 서버의 CPU 이용률</span><span class="sxs-lookup"><span data-stu-id="64a9c-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-188">게시 서버는 메타 데이터 게시를 위해 관리 서버에 동시에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-189">게시 서버 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-190">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-190">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-191">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-191">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-192">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-192">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-193">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-193">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-194">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-194">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-195">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-196">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-196">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-197">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-197">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-198">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-198">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-199">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-199">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-200">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-200">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-201">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-202">50</span><span class="sxs-lookup"><span data-stu-id="64a9c-202">50</span></span></p></li>
<li><p><span data-ttu-id="64a9c-203">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-203">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-204">200</span><span class="sxs-lookup"><span data-stu-id="64a9c-204">200</span></span></p></li>
<li><p><span data-ttu-id="64a9c-205">300</span><span class="sxs-lookup"><span data-stu-id="64a9c-205">300</span></span></p></li>
<li><p><span data-ttu-id="64a9c-206">315</span><span class="sxs-lookup"><span data-stu-id="64a9c-206">315</span></span></p></li>
<li><p><span data-ttu-id="64a9c-207">320</span><span class="sxs-lookup"><span data-stu-id="64a9c-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-208">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-209">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-210">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-211">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-212">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-213">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-214">5mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-214">5</span></span></p></li>
<li><p><span data-ttu-id="64a9c-215">1천만</span><span class="sxs-lookup"><span data-stu-id="64a9c-215">10</span></span></p></li>
<li><p><span data-ttu-id="64a9c-216">인치</span><span class="sxs-lookup"><span data-stu-id="64a9c-216">19</span></span></p></li>
<li><p><span data-ttu-id="64a9c-217">32</span><span class="sxs-lookup"><span data-stu-id="64a9c-217">32</span></span></p></li>
<li><p><span data-ttu-id="64a9c-218">30</span><span class="sxs-lookup"><span data-stu-id="64a9c-218">30</span></span></p></li>
<li><p><span data-ttu-id="64a9c-219">37</span><span class="sxs-lookup"><span data-stu-id="64a9c-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-220">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-220">17</span></span></p></li>
<li><p><span data-ttu-id="64a9c-221">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-221">17</span></span></p></li>
<li><p><span data-ttu-id="64a9c-222">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-222">17</span></span></p></li>
<li><p><span data-ttu-id="64a9c-223">~</span><span class="sxs-lookup"><span data-stu-id="64a9c-223">15</span></span></p></li>
<li><p><span data-ttu-id="64a9c-224">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-224">17</span></span></p></li>
<li><p><span data-ttu-id="64a9c-225">~</span><span class="sxs-lookup"><span data-stu-id="64a9c-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-226">게시 메타 데이터에 연결 그룹 포함</span><span class="sxs-lookup"><span data-stu-id="64a9c-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-227">연결 그룹 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-228">1천만</span><span class="sxs-lookup"><span data-stu-id="64a9c-228">10</span></span></p></li>
<li><p><span data-ttu-id="64a9c-229">50</span><span class="sxs-lookup"><span data-stu-id="64a9c-229">50</span></span></p></li>
<li><p><span data-ttu-id="64a9c-230">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-230">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-231">150</span><span class="sxs-lookup"><span data-stu-id="64a9c-231">150</span></span></p></li>
<li><p><span data-ttu-id="64a9c-232">300</span><span class="sxs-lookup"><span data-stu-id="64a9c-232">300</span></span></p></li>
<li><p><span data-ttu-id="64a9c-233">400</span><span class="sxs-lookup"><span data-stu-id="64a9c-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-234">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-234">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-235">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-235">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-236">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-236">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-237">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-237">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-238">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-238">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-239">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-240">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-240">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-241">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-241">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-242">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-242">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-243">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-243">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-244">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-244">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-245">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-246">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-247">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-248">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-249">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-250">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-251">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-252">1천만</span><span class="sxs-lookup"><span data-stu-id="64a9c-252">10</span></span></p></li>
<li><p><span data-ttu-id="64a9c-253">mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-253">11</span></span></p></li>
<li><p><span data-ttu-id="64a9c-254">mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-254">11</span></span></p></li>
<li><p><span data-ttu-id="64a9c-255">16</span><span class="sxs-lookup"><span data-stu-id="64a9c-255">16</span></span></p></li>
<li><p><span data-ttu-id="64a9c-256">khz</span><span class="sxs-lookup"><span data-stu-id="64a9c-256">22</span></span></p></li>
<li><p><span data-ttu-id="64a9c-257">km</span><span class="sxs-lookup"><span data-stu-id="64a9c-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-258">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-258">17</span></span></p></li>
<li><p><span data-ttu-id="64a9c-259">인치</span><span class="sxs-lookup"><span data-stu-id="64a9c-259">19</span></span></p></li>
<li><p><span data-ttu-id="64a9c-260">khz</span><span class="sxs-lookup"><span data-stu-id="64a9c-260">22</span></span></p></li>
<li><p><span data-ttu-id="64a9c-261">인치</span><span class="sxs-lookup"><span data-stu-id="64a9c-261">19</span></span></p></li>
<li><p><span data-ttu-id="64a9c-262">명</span><span class="sxs-lookup"><span data-stu-id="64a9c-262">20</span></span></p></li>
<li><p><span data-ttu-id="64a9c-263">명</span><span class="sxs-lookup"><span data-stu-id="64a9c-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-264">게시 메타 데이터에 액세스 그룹 포함</span><span class="sxs-lookup"><span data-stu-id="64a9c-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-265">액세스 그룹 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-266">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-266">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-267">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-267">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-268">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-268">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-269">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-270">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-270">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-271">1천만</span><span class="sxs-lookup"><span data-stu-id="64a9c-271">10</span></span></p></li>
<li><p><span data-ttu-id="64a9c-272">명</span><span class="sxs-lookup"><span data-stu-id="64a9c-272">20</span></span></p></li>
<li><p><span data-ttu-id="64a9c-273">40</span><span class="sxs-lookup"><span data-stu-id="64a9c-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-274">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-274">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-275">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-275">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-276">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-276">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-277">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-278">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-279">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-280">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-281">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-282">1천만</span><span class="sxs-lookup"><span data-stu-id="64a9c-282">10</span></span></p></li>
<li><p><span data-ttu-id="64a9c-283">43</span><span class="sxs-lookup"><span data-stu-id="64a9c-283">43</span></span></p></li>
<li><p><span data-ttu-id="64a9c-284">153</span><span class="sxs-lookup"><span data-stu-id="64a9c-284">153</span></span></p></li>
<li><p><span data-ttu-id="64a9c-285">535</span><span class="sxs-lookup"><span data-stu-id="64a9c-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-286">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-286">17</span></span></p></li>
<li><p><span data-ttu-id="64a9c-287">kbps</span><span class="sxs-lookup"><span data-stu-id="64a9c-287">26</span></span></p></li>
<li><p><span data-ttu-id="64a9c-288">fps</span><span class="sxs-lookup"><span data-stu-id="64a9c-288">24</span></span></p></li>
<li><p><span data-ttu-id="64a9c-289">fps</span><span class="sxs-lookup"><span data-stu-id="64a9c-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-290">관리 서버를 실행 하는 컴퓨터의 CPU 사용률이이를 대상으로 하는 게시 서버 수에 관계 없이 25%입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="64a9c-291">Microsoft SQL Server 데이터베이스 트랜잭션/초, 일괄 처리 요청/초 및 사용자 연결은 게시 서버 수에 관계 없이 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="64a9c-292">예를 들어, 초당 거래 수는 ~ 30, 일괄 처리 요청 ~ 200, 사용자 연결 ~ 6이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="64a9c-293">관리 서버 & 게시 서버는 서로 느린 연결 네트워크를 사용 하는 지리적 분산 배포를 통해 &lt; 단일 관리 서버에 대 한 100 동시 요청에도 게시 서버의 라운드트립 응답 시간이 허용 되는 시간 제한 (5 초) 내에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

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
<th align="left"><span data-ttu-id="64a9c-294">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-295">변형</span><span class="sxs-lookup"><span data-stu-id="64a9c-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="64a9c-296">연결 그룹 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="64a9c-297">액세스 그룹 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="64a9c-298">게시 서버 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="64a9c-299">네트워크 연결 형식 게시 서버/관리 서버</span><span class="sxs-lookup"><span data-stu-id="64a9c-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="64a9c-300">게시 서버에서 라운드트립 응답 시간 (초)</span><span class="sxs-lookup"><span data-stu-id="64a9c-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="64a9c-301">관리 서버의 CPU 이용률</span><span class="sxs-lookup"><span data-stu-id="64a9c-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-302">게시 서버와 관리 서버 간의 네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="64a9c-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-303">1.5 Mbps 느린 연결 네트워크</span><span class="sxs-lookup"><span data-stu-id="64a9c-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-304">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-304">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-305">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-306">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-306">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-307">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-308">50</span><span class="sxs-lookup"><span data-stu-id="64a9c-308">50</span></span></p></li>
<li><p><span data-ttu-id="64a9c-309">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-310">1.5 mbps 케이블 DSL</span><span class="sxs-lookup"><span data-stu-id="64a9c-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="64a9c-311">1.5 mbps 케이블 DSL</span><span class="sxs-lookup"><span data-stu-id="64a9c-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-312">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="64a9c-312">4</span></span></p></li>
<li><p><span data-ttu-id="64a9c-313">5mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-314">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-314">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-315">2</span><span class="sxs-lookup"><span data-stu-id="64a9c-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-316">게시 서버와 관리 서버 간의 네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="64a9c-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-317">LAN/WIFI 네트워크</span><span class="sxs-lookup"><span data-stu-id="64a9c-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-318">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-318">0</span></span></p></li>
<li><p><span data-ttu-id="64a9c-319">0</span><span class="sxs-lookup"><span data-stu-id="64a9c-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-320">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-320">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-321">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-322">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-322">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-323">200</span><span class="sxs-lookup"><span data-stu-id="64a9c-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-324">Wifi</span><span class="sxs-lookup"><span data-stu-id="64a9c-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="64a9c-325">Wifi</span><span class="sxs-lookup"><span data-stu-id="64a9c-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-326">mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-326">11</span></span></p></li>
<li><p><span data-ttu-id="64a9c-327">명</span><span class="sxs-lookup"><span data-stu-id="64a9c-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-328">~</span><span class="sxs-lookup"><span data-stu-id="64a9c-328">15</span></span></p></li>
<li><p><span data-ttu-id="64a9c-329">17</span><span class="sxs-lookup"><span data-stu-id="64a9c-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-330">관리 서버와 게시 서버가 느린 연결 네트워크 또는 고속 네트워크를 통해 연결 되어 있는지 여부에 관계 없이 관리 서버는 약 15000 패키지 새로 고침 요청을 30 분 내에 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="64a9c-331">앱-V 5.1 보고 서버 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="64a9c-331">App-V 5.1 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="64a9c-332">App-v 5.1 클라이언트 보고 데이터를 보고 서버로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-332">App-V 5.1 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="64a9c-333">그러면 보고 서버는 Microsoft SQL Server 데이터베이스에 정보를 기록 하 고 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 성공적으로 다시 알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.1 client.</span></span> <span data-ttu-id="64a9c-334">앱-V 5.1 보고 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-334">For more information about App-V 5.1 Reporting Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="64a9c-335">**참고**  라운드트립 응답 시간은 reporting server에 보고 정보를 보내고 보고 서버에서 성공적으로 알림을 받기 위해 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 수행 되는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64a9c-336">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-337">요약</span><span class="sxs-lookup"><span data-stu-id="64a9c-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-338">여러 App-v 5.1 클라이언트는 보고 정보를 보고 서버에 동시에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-338">Multiple App-V 5.1 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-339">보고 서버의 라운드트립 응답 시간은 500 클라이언트에 2.6 초입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-340">보고 서버의 라운드트립 응답 시간은 1000 클라이언트에 5.65 초입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-341">라운드 트립 응답 시간은 클라이언트 수에 따라 선형적으로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-342">보고 서버에서 처리 한 초당 요청 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-343">단일 보고 서버와 단일 데이터베이스는 초당 최대 139 개의 요청을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="64a9c-344">평균은 121 요청/초입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-345">동일한 Microsoft SQL Server 데이터베이스에 보고 하는 두 개의 보고 서버를 사용 하는 경우 평균 요청/초는 단일 보고 서버 = ~ 127와 비슷하지만 최대 278 요청 수는 초입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-346">단일 보고 서버는 500 동시/활성 연결을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-347">단일 보고 서버는 최대 1500 동시 연결을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-348">보고 데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="64a9c-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-349">Microsoft SQL Server를 실행 하는 컴퓨터의 잠금 경합은 초당 요청에 대 한 제한 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-350">처리량 및 응답 시간은 데이터베이스 크기와 무관 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-351">**임의 지연 계산**:</span><span class="sxs-lookup"><span data-stu-id="64a9c-351">**Calculating random delay**:</span></span>

<span data-ttu-id="64a9c-352">임의 지연은 보고 서버로 전송 되는 데이터의 최대 지연 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="64a9c-353">예약 된 작업이 시작 되 면 클라이언트는 **0** 과 **ReportingRandomDelay** 사이의 임의 지연 시간을 생성 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="64a9c-354">임의 지연 = 4 \ \* 클라이언트 수/초 당 평균 요청</span><span class="sxs-lookup"><span data-stu-id="64a9c-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="64a9c-355">예: 500 클라이언트의 경우 초당 120 요청이 있는 경우 임의 지연은 4 \ \* 500/120 = ~ 17 분입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="64a9c-356">앱-V 5.1 게시 서버 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="64a9c-356">App-V 5.1 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="64a9c-357">App-v 5.1 클라이언트를 실행 하는 컴퓨터는 앱 V 5.1 게시 서버에 연결 하 여 게시 새로 고침 요청을 보내고 응답을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-357">Computers running the App-V 5.1 client connect to the App-V 5.1 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="64a9c-358">라운드 트립 응답 시간은 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 측정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-358">Round trip response time is measured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="64a9c-359">프로세서 시간은 게시 서버에서 측정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="64a9c-360">앱-V 5.1 게시 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64a9c-360">For more information about App-V 5.1 Publishing Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="64a9c-361">**중요**  다음 목록에는 App-v 5.1 게시 서버를 설정할 때 고려해 야 하는 주요 요소가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.1 publishing server:</span></span>

-   <span data-ttu-id="64a9c-362">단일 게시 서버에 동시에 연결 하는 클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="64a9c-363">각 새로 고침의 패키지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="64a9c-364">클라이언트와 App-v 5.1 게시 서버 간의 환경에서 사용할 수 있는 네트워크 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-364">The available network bandwidth in your environment between the client and the App-V 5.1 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64a9c-365">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-366">요약</span><span class="sxs-lookup"><span data-stu-id="64a9c-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-367">여러 App-v 5.1 클라이언트는 단일 게시 서버에 동시에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-367">Multiple App-V 5.1 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-368">듀얼 코어 프로세서를 실행 하는 게시 서버는 동시에 새로 고침을 요청 하는 최대 5000 클라이언트에 응답할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-369">5000-10000 클라이언트의 경우 게시 서버에는 최소 쿼드 코어가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-370">10000-20000 클라이언트의 경우 더 효율적인 응답 시간을 위해 게시 서버에 듀얼 쿼드 코어를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="64a9c-371">쿼드 코어를 사용 하는 게시 서버는 3 초 내에 1만 패키지를 새로 고칠 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="64a9c-372">(1만 동시 클라이언트 지원)</span><span class="sxs-lookup"><span data-stu-id="64a9c-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-373">새로 고칠 때마다 패키지의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-374">패키지 수를 늘리면 응답 시간이 ~ 40% (최대 1000 패키지)로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-375">App-v 5.1 클라이언트와 게시 서버 간의 네트워크.</span><span class="sxs-lookup"><span data-stu-id="64a9c-375">Network between the App-V 5.1 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-376">느린 네트워크 (1.5 Mbps 대역폭)에서 LAN (최대 1000 명의 사용자)과 비교 하 여 응답 시간이 97% 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-377">**참고**  게시 서버 CPU 사용은 동시 요청 ( &gt; 대부분의 경우 90%)을 처리 해야 하는 시간 간격 동안 항상 높습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="64a9c-378">게시 서버는 1 초에 ~ 1500 클라이언트 요청을 처리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

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
<th align="left"><span data-ttu-id="64a9c-379">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-380">변형</span><span class="sxs-lookup"><span data-stu-id="64a9c-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="64a9c-381">앱-V 5.1 클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-381">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="64a9c-382">패키지 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="64a9c-383">게시 서버의 프로세서 구성</span><span class="sxs-lookup"><span data-stu-id="64a9c-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="64a9c-384">네트워크 연결 형식 게시 서버/App-v 5.1 클라이언트</span><span class="sxs-lookup"><span data-stu-id="64a9c-384">Network connection type publishing server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="64a9c-385">App-v 5.1 클라이언트 (초)에 대 한 왕복 시간</span><span class="sxs-lookup"><span data-stu-id="64a9c-385">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="64a9c-386">게시 서버의 CPU 사용률 (%)</span><span class="sxs-lookup"><span data-stu-id="64a9c-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-387">App-v 5.1 클라이언트에서 게시 새로 고침 요청이 &amp; 응답을 수신 하 고, 각 요청이 120 패키지를 포함 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-387">App-V 5.1 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-388">클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-389">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-389">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-390">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-390">1000</span></span></p></li>
<li><p><span data-ttu-id="64a9c-391">5000</span><span class="sxs-lookup"><span data-stu-id="64a9c-391">5000</span></span></p></li>
<li><p><span data-ttu-id="64a9c-392">1만</span><span class="sxs-lookup"><span data-stu-id="64a9c-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-393">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-393">120</span></span></p></li>
<li><p><span data-ttu-id="64a9c-394">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-394">120</span></span></p></li>
<li><p><span data-ttu-id="64a9c-395">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-395">120</span></span></p></li>
<li><p><span data-ttu-id="64a9c-396">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-397">듀얼 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="64a9c-398">듀얼 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="64a9c-399">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="64a9c-400">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-401">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-402">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-403">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-404">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-405">raid-1</span><span class="sxs-lookup"><span data-stu-id="64a9c-405">1</span></span></p></li>
<li><p><span data-ttu-id="64a9c-406">2</span><span class="sxs-lookup"><span data-stu-id="64a9c-406">2</span></span></p></li>
<li><p><span data-ttu-id="64a9c-407">2</span><span class="sxs-lookup"><span data-stu-id="64a9c-407">2</span></span></p></li>
<li><p><span data-ttu-id="64a9c-408">3-4</span><span class="sxs-lookup"><span data-stu-id="64a9c-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-409">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-409">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-410">99</span><span class="sxs-lookup"><span data-stu-id="64a9c-410">99</span></span></p></li>
<li><p><span data-ttu-id="64a9c-411">89</span><span class="sxs-lookup"><span data-stu-id="64a9c-411">89</span></span></p></li>
<li><p><span data-ttu-id="64a9c-412">77</span><span class="sxs-lookup"><span data-stu-id="64a9c-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-413">각 새로 고침의 여러 패키지</span><span class="sxs-lookup"><span data-stu-id="64a9c-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-414">패키지 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-415">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-415">1000</span></span></p></li>
<li><p><span data-ttu-id="64a9c-416">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-417">500</span><span class="sxs-lookup"><span data-stu-id="64a9c-417">500</span></span></p></li>
<li><p><span data-ttu-id="64a9c-418">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-419">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="64a9c-420">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-421">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-422">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-423">2</span><span class="sxs-lookup"><span data-stu-id="64a9c-423">2</span></span></p></li>
<li><p><span data-ttu-id="64a9c-424">3-4</span><span class="sxs-lookup"><span data-stu-id="64a9c-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-425">92</span><span class="sxs-lookup"><span data-stu-id="64a9c-425">92</span></span></p></li>
<li><p><span data-ttu-id="64a9c-426">91</span><span class="sxs-lookup"><span data-stu-id="64a9c-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-427">클라이언트와 게시 서버 간의 네트워크</span><span class="sxs-lookup"><span data-stu-id="64a9c-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-428">1.5 Mbps 느린 연결 네트워크</span><span class="sxs-lookup"><span data-stu-id="64a9c-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-429">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-429">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-430">500</span><span class="sxs-lookup"><span data-stu-id="64a9c-430">500</span></span></p></li>
<li><p><span data-ttu-id="64a9c-431">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-432">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-432">120</span></span></p></li>
<li><p><span data-ttu-id="64a9c-433">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-433">120</span></span></p></li>
<li><p><span data-ttu-id="64a9c-434">120</span><span class="sxs-lookup"><span data-stu-id="64a9c-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-435">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="64a9c-436">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="64a9c-437">쿼드 코어</span><span class="sxs-lookup"><span data-stu-id="64a9c-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-438">1.5 Mbps 내 대륙과 네트워크</span><span class="sxs-lookup"><span data-stu-id="64a9c-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-439">3-4</span><span class="sxs-lookup"><span data-stu-id="64a9c-439">3</span></span></p></li>
<li><p><span data-ttu-id="64a9c-440">10 (0.2% 실패 율)</span><span class="sxs-lookup"><span data-stu-id="64a9c-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="64a9c-441">17 (1% 실패 율 사용)</span><span class="sxs-lookup"><span data-stu-id="64a9c-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="64a9c-442">앱-V 5.1 스트리밍 용량 계획 권장 사항</span><span class="sxs-lookup"><span data-stu-id="64a9c-442">App-V 5.1 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="64a9c-443">앱-V 5.1 클라이언트를 실행 하는 컴퓨터는 스트리밍 서버에서 가상 응용 프로그램 패키지를 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-443">Computers running the App-V 5.1 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="64a9c-444">라운드트립 응답 시간은 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 측정 되며 전체 패키지를 스트리밍하는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-444">Round trip response time is measured on the computer running the App-V 5.1 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="64a9c-445">**중요**  다음 목록에서는 App-v 5.1 스트리밍 서버를 설정할 때 고려해 야 하는 주요 요인을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.1 streaming server:</span></span>

-   <span data-ttu-id="64a9c-446">단일 스트리밍 서버에서 응용 프로그램 패키지를 동시에 스트리밍하는 클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="64a9c-447">스트리밍 중인 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="64a9c-448">클라이언트와 스트리밍 서버 간의 환경에서 사용할 수 있는 네트워크 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64a9c-449">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-450">요약</span><span class="sxs-lookup"><span data-stu-id="64a9c-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-451">여러 App-v 5.1 클라이언트는 단일 스트리밍 서버에서 동시에 응용 프로그램을 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-451">Multiple App-V 5.1 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-452">동일한 서버에서 동시에 스트리밍하는 클라이언트 수가 늘어나면 패키지 다운로드/스트리밍 시간에 대 한 선형 관계가 있는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-453">스트리밍 중인 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-454">패키지 크기는 크기가 ~ 1GB 인 대용량 패키지에 대해서만 스트리밍/다운로드 시간에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="64a9c-455">3 MB에서 100 MB 까지의 패키지 크기에 대 한 스트리밍 시간은 20 초에서 100 초로, 100 동시 클라이언트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-456">App-v 5.1 클라이언트와 스트리밍 서버 간의 네트워크.</span><span class="sxs-lookup"><span data-stu-id="64a9c-456">Network between the App-V 5.1 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-457">느린 네트워크 (1.5 Mbps 대역폭)에서 LAN (최대 100 명의 사용자)과 비교 하 여 응답 시간이 70-80% 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-458">다음 표에는 이전 목록의 각 요소에 대 한 예제 값이 표시 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-458">The following table displays sample values for each of the factors in the previous list:</span></span>

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
<th align="left"><span data-ttu-id="64a9c-459">시나리오</span><span class="sxs-lookup"><span data-stu-id="64a9c-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="64a9c-460">변형</span><span class="sxs-lookup"><span data-stu-id="64a9c-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="64a9c-461">앱-V 5.1 클라이언트 수</span><span class="sxs-lookup"><span data-stu-id="64a9c-461">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="64a9c-462">각 패키지의 크기</span><span class="sxs-lookup"><span data-stu-id="64a9c-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="64a9c-463">네트워크 연결 형식 스트리밍 서버/App-v 5.1 클라이언트</span><span class="sxs-lookup"><span data-stu-id="64a9c-463">Network connection type streaming server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="64a9c-464">App-v 5.1 클라이언트 (초)에 대 한 왕복 시간</span><span class="sxs-lookup"><span data-stu-id="64a9c-464">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-465">여러 앱-V 5.1 클라이언트는 스트리밍 서버에서 가상 응용 프로그램 패키지를 스트리밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-465">Multiple App-V 5.1 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-466">클라이언트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-467">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-467">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-468">200</span><span class="sxs-lookup"><span data-stu-id="64a9c-468">200</span></span></p></li>
<li><p><span data-ttu-id="64a9c-469">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-470">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-470">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-471">200</span><span class="sxs-lookup"><span data-stu-id="64a9c-471">200</span></span></p></li>
<li><p><span data-ttu-id="64a9c-472">1000</span><span class="sxs-lookup"><span data-stu-id="64a9c-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-473">3.5MB</span><span class="sxs-lookup"><span data-stu-id="64a9c-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="64a9c-474">3.5MB</span><span class="sxs-lookup"><span data-stu-id="64a9c-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="64a9c-475">3.5MB</span><span class="sxs-lookup"><span data-stu-id="64a9c-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-476">5mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="64a9c-477">5mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="64a9c-478">5mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-479">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-480">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-481">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-482">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-483">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-484">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-485">개가</span><span class="sxs-lookup"><span data-stu-id="64a9c-485">29</span></span></p></li>
<li><p><span data-ttu-id="64a9c-486">39</span><span class="sxs-lookup"><span data-stu-id="64a9c-486">39</span></span></p></li>
<li><p><span data-ttu-id="64a9c-487">391</span><span class="sxs-lookup"><span data-stu-id="64a9c-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-488">35</span><span class="sxs-lookup"><span data-stu-id="64a9c-488">35</span></span></p></li>
<li><p><span data-ttu-id="64a9c-489">68</span><span class="sxs-lookup"><span data-stu-id="64a9c-489">68</span></span></p></li>
<li><p><span data-ttu-id="64a9c-490">461</span><span class="sxs-lookup"><span data-stu-id="64a9c-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64a9c-491">스트리밍된 각 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-492">각 패키지의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-493">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-493">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-494">200</span><span class="sxs-lookup"><span data-stu-id="64a9c-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-495">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-495">100</span></span></p></li>
<li><p><span data-ttu-id="64a9c-496">200</span><span class="sxs-lookup"><span data-stu-id="64a9c-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-497">21MB</span><span class="sxs-lookup"><span data-stu-id="64a9c-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="64a9c-498">21MB</span><span class="sxs-lookup"><span data-stu-id="64a9c-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-499">109</span><span class="sxs-lookup"><span data-stu-id="64a9c-499">109</span></span></p></li>
<li><p><span data-ttu-id="64a9c-500">109</span><span class="sxs-lookup"><span data-stu-id="64a9c-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-501">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-502">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-503">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="64a9c-504">LAN</span><span class="sxs-lookup"><span data-stu-id="64a9c-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="64a9c-505">33</span><span class="sxs-lookup"><span data-stu-id="64a9c-505">33</span></span></p>
<p><span data-ttu-id="64a9c-506">83</span><span class="sxs-lookup"><span data-stu-id="64a9c-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="64a9c-507">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-507">100</span></span></p>
<p><span data-ttu-id="64a9c-508">160</span><span class="sxs-lookup"><span data-stu-id="64a9c-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64a9c-509">클라이언트와 App-v 5.1 스트리밍 서버 간의 네트워크 연결.</span><span class="sxs-lookup"><span data-stu-id="64a9c-509">Network connection between client and App-V 5.1 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64a9c-510">1.5 Mbps 느린 연결 네트워크.</span><span class="sxs-lookup"><span data-stu-id="64a9c-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-511">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-512">100</span><span class="sxs-lookup"><span data-stu-id="64a9c-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-513">3.5MB</span><span class="sxs-lookup"><span data-stu-id="64a9c-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="64a9c-514">5mb</span><span class="sxs-lookup"><span data-stu-id="64a9c-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="64a9c-515">1.5 Mbps 내 대륙과 네트워크</span><span class="sxs-lookup"><span data-stu-id="64a9c-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="64a9c-516">102</span><span class="sxs-lookup"><span data-stu-id="64a9c-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="64a9c-517">121</span><span class="sxs-lookup"><span data-stu-id="64a9c-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="64a9c-518">각 App-v 5.1 스트리밍 서버는 가상화 된 응용 프로그램을 동시에 스트리밍하는 최소 200 클라이언트를 처리할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-518">Each App-V 5.1 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="64a9c-519">**참고**  실제로 스트림 하는 데 걸리는 실제 시간은 동시 스트리밍 클라이언트 수, 패키지 수, 패키지 크기, 서버의 네트워크 활동 및 네트워크 상태에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="64a9c-520">예를 들어, 100 동시 클라이언트가 서버에서 스트리밍하는 경우 평균 사용자는 2 분 이내에 100 MB 패키지를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="64a9c-521">그러나 크기가 1 GB 인 패키지는 최대 30 분까지 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="64a9c-522">대부분의 실제 환경에서는 스트리밍 요구가 일관 되 게 분산 되지 않으며, 필요한 스트리밍 서버 수의 크기를 적절히 조정 하기 위해 해당 환경에 존재 하는 대략적인 최대 스트리밍 요구 사항을 이해 하는 것이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="64a9c-523">스트리밍 서버가 지원할 수 있는 클라이언트 수가 현저 하 게 늘어나고, 응용 프로그램을 미리 캐시 하는 경우 최대 스트리밍 요구 사항이 줄어들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="64a9c-524">또한 요청에 따라 스트리밍 서버에서 지원 되는 클라이언트 수를 늘리면 최적화 된 패키지를 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="64a9c-525">앱-V 5.1 서버 역할 결합</span><span class="sxs-lookup"><span data-stu-id="64a9c-525">Combining App-V 5.1 Server Roles</span></span>


<span data-ttu-id="64a9c-526">확장 및 내결함성 요구 사항을 Discounting Active Directory에 연결 된 위치에 필요한 최소 서버 수가 하나입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="64a9c-527">이 서버는 관리 서버, 관리 서버 서비스 및 Microsoft SQL Server 역할을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="64a9c-528">따라서 서버 역할은 서로 충돌 하지 않으므로 원하는 조합으로 정렬할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="64a9c-529">크기 조정 요구 사항을 무시 하 여 오류 허용 구현을 제공 하는 데 필요한 최소 서버 수는 4 개입니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="64a9c-530">관리 서버 및 Microsoft SQL Server 역할은 내결함성이 있는 구성에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="64a9c-531">관리 서버 서비스를 역할 중 하 나와 결합할 수 있지만, 단일 오류 지점이 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="64a9c-532">내결함성이 많은 전략과 기술이 제공 되는 것은 아니지만, 제공 되는 서비스에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="64a9c-533">또한 App-v 5.1 역할이 결합 된 경우 비 호환성으로 인해 특정 내결함성 옵션이 더 이상 적용 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64a9c-533">Additionally, if App-V 5.1 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="64a9c-534">관련 항목</span><span class="sxs-lookup"><span data-stu-id="64a9c-534">Related topics</span></span>


[<span data-ttu-id="64a9c-535">App-V 5.1 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="64a9c-535">App-V 5.1 Supported Configurations</span></span>](app-v-51-supported-configurations.md)

[<span data-ttu-id="64a9c-536">App-V 5.1을 사용한 고가용성 계획</span><span class="sxs-lookup"><span data-stu-id="64a9c-536">Planning for High Availability with App-V 5.1</span></span>](planning-for-high-availability-with-app-v-51.md)

[<span data-ttu-id="64a9c-537">App-V 배포 계획</span><span class="sxs-lookup"><span data-stu-id="64a9c-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





