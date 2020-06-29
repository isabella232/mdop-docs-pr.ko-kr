---
title: MBAM에 대한 네트워크 부하 분산을 구성하는 방법
description: MBAM에 대한 네트워크 부하 분산을 구성하는 방법
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825513"
---
# <span data-ttu-id="0df78-103">MBAM에 대한 네트워크 부하 분산을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0df78-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="0df78-104">관리 및 모니터링 서버 기능을 설치 하기 위한 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0df78-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="0df78-105">**참고**  설치 로그 파일을 얻으려면 **msiexec** 패키지 및 **/l** 위치 옵션을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (mbam)을 설치 해야 합니다 &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="0df78-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="0df78-106">로그 파일은 사용자가 지정한 위치에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="0df78-107">추가 설치 로그 파일은 MBAM을 설치 하는 사용자 의% temp% 폴더에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="0df78-108">관리 및 모니터링 서버 기능의 NLB (네트워크 부하 분산) 클러스터는 MBAM에 확장성을 제공 하 고 55000 MBAM 클라이언트 컴퓨터를 지원 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="0df78-109">**참고**  Windows Server 네트워크 부하 분산은 단일 서버 클러스터에 구성 된 서버 집합을 통해 클라이언트 요청을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="0df78-110">클러스터의 각 서버 (호스트)에 네트워크 부하 분산이 설치 되 면 클러스터는 클라이언트 요청에 가상 IP 주소 또는 FQDN (정규화 된 도메인 이름)을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="0df78-111">초기 클라이언트 요청이 클러스터의 모든 호스트로 이동 하지만 한 호스트만 요청을 수락 하 고 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="0df78-112">NLB 클러스터에 포함 되는 모든 컴퓨터에는 다음과 같은 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="0df78-113">NLB 클러스터의 모든 컴퓨터는 같은 도메인에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="0df78-114">NLB 클러스터의 각 컴퓨터는 고정 IP 주소를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="0df78-115">NLB 클러스터의 각 컴퓨터는 네트워크 부하 분산을 사용 하도록 설정 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="0df78-116">NLB 클러스터에는 고정 IP 주소가 필요 하며 DNS (domain name system)에 호스트 레코드를 수동으로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="0df78-117">MBAM 관리 및 모니터링 서버에 대 한 네트워크 부하 분산 구성</span><span class="sxs-lookup"><span data-stu-id="0df78-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="0df78-118">다음 단계에서는 2 MBAM 관리 및 모니터링 서버에 대해 NLB 클러스터 가상 이름과 IP 주소를 구성 하는 방법과 NLB 클러스터를 사용 하도록 MBAM 클라이언트를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="0df78-119">이 항목에서 설명 하는 절차를 시작 하기 전에, MBAM 서버 기능 설치 및 NLB 클러스터 구성에 대 한 필수 조건을 충족 하는 두 개의 개별 서버 컴퓨터에서 동일한 IIS 포트 바인딩을 사용 하 여 MBAM 관리 및 모니터링 서버 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="0df78-120">**참고**  이 항목에서는 네트워크 부하 분산 관리자를 사용 하 여 NLB 클러스터를 만드는 기본 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="0df78-121">Windows Server를 NLB 클러스터의 일부로 구성 하는 정확한 단계는 사용 중인 Windows Server 버전에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="0df78-122">WindowsServer2008에서 NLBs를 만드는 방법에 대 한 자세한 내용은 Windows Server2008 TechNet 라이브러리에서 [네트워크 부하 분산 클러스터 만들기](https://go.microsoft.com/fwlink/?LinkId=197176) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0df78-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="0df78-123">두 개의 MBAM 관리 및 모니터링 서버에 대 한 NLB 클러스터 가상 이름과 IP 주소를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="0df78-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="0df78-124">**시작**을 클릭 하 고 **모든 프로그램**, **관리 도구**를 차례로 클릭 한 다음 **네트워크 부하 분산 관리자**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="0df78-125">**참고**  NLB 관리자가 없는 경우 WindowsServer 기능으로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="0df78-126">이 기능을 NLB 클러스터에 구성 하려면 MBAM 관리 및 모니터링 서버 모두에이 기능을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="0df78-127">메뉴 모음에서 **클러스터**를 클릭 한 다음 **새로 만들기** 를 클릭 하 여 **클러스터 매개 변수** 대화 상자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="0df78-128">**클러스터 매개 변수** 대화 상자에서 NLB 클러스터 IP 구성에 대 한 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="0df78-129">**IP 주소:** DNS에 등록 된 NLB 클러스터 IP 주소</span><span class="sxs-lookup"><span data-stu-id="0df78-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="0df78-130">**서브넷 마스크:** DNS에 등록 된 NLB 클러스터 IP 주소 서브넷 마스크</span><span class="sxs-lookup"><span data-stu-id="0df78-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="0df78-131">**전체 인터넷 이름:** DNS에 등록 된 NLB 클러스터 이름의 FQDN</span><span class="sxs-lookup"><span data-stu-id="0df78-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="0df78-132">**클러스터 작동 모드**에서 **유니캐스트** 가 선택 되어 있는지 확인 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="0df78-133">**클러스터 IP 주소** 페이지에서 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="0df78-134">**포트 규칙** 페이지에서 **편집** 을 클릭 하 여 nlb 클러스터가 응답할 포트를 정의 하 고 사이트에 대해 정의 된 대로 클라이언트에서 사이트 간 시스템 통신에 사용 되는 포트를 구성 하거나 **다음** 을 클릭 하 여 nlb 클러스터 IP 주소가 모든 tcp/ip 포트에 응답 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="0df78-135">**참고**  **Affinity** 가 **Single**로 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="0df78-136">**연결** 페이지에서 **호스트**의 NLB 클러스터에 포함 될 Mbam 관리 및 모니터링 서버 인스턴스 호스트 이름을 입력 한 다음 **연결**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="0df78-137">**새 클러스터를 구성 하는 데 사용할 수 있는 인터페이스**에서 NLB 클러스터 통신에 응답 하도록 구성 되는 네트워킹 인터페이스를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="0df78-138">**호스트 매개 변수** 페이지에서 표시 되는 정보를 검토 하 여 **전용 IP 구성** 설정이 올바른 NLB 클러스터 호스트에 대 한 전용 호스트 IP 구성을 표시 하는지 확인 하 고, 초기 호스트 상태 **기본 상태:** 가 **시작**되었는지 확인 한 다음 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="0df78-139">**참고**  **호스트 매개 변수** 페이지에는 또한 NLB 클러스터 호스트 우선 순위 (1 ~ 32)가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="0df78-140">NLB 클러스터에 새 호스트가 추가 되 면 호스트 우선 순위는 이전에 추가 된 호스트와 달라 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="0df78-141">네트워크 부하 분산 관리자를 사용 하면 우선 순위가 자동으로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="0df78-142">\*\* &lt; Nlb 클러스터 이름을 &gt; \*\* 클릭 하 고 계속 하기 전에 Nlb 호스트 인터페이스 **상태가** **수렴** 된 것으로 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="0df78-143">이 단계를 실행 하려면 nlb 관리자가 수정 하는 호스트 TCP/IP 구성으로 NLB 클러스터 디스플레이를 새로 고쳐야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="0df78-144">NLB 클러스터에 다른 호스트를 추가 하려면 \*\* &lt; nlb 클러스터 이름을 &gt; \*\*마우스 오른쪽 단추로 클릭 하 고 **클러스터에 호스트 추가를** 클릭 한 다음 NLB 클러스터에 포함 될 각 사이트 시스템에 대해 7 ~ 10 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="0df78-145">MBAM 그룹 정책 템플릿이 설치 되어 있는 컴퓨터에서 NLB 클러스터 이름을 사용 하도록 mbam 그룹 정책 설정을 수정 하 고 NLB 클러스터 컴퓨터에 설치 된 MBAM 관리 및 모니터링 서버 기능에 액세스 하기 위해 해당 IIS 포트 바인딩을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="0df78-146">MBAM GPO 설정을 편집 하는 방법에 대 한 자세한 내용은 [mbam 1.0 GPO 설정을 편집 하는 방법을](how-to-edit-mbam-10-gpo-settings.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0df78-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="0df78-147">MBAM 관리 및 모니터링 서버가 환경에 대 한 새로운 요소인 경우 필요한 로컬 보안 그룹 구성원 자격이 올바르게 구성 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="0df78-148">보안 그룹 요구 사항에 대 한 자세한 내용은 [MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0df78-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="0df78-149">NLB 클러스터 구성이 완료 되 면 MBAM 관리 및 모니터링 NLB 클러스터가 작동 하는지 확인 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="0df78-150">이렇게 하려면 NLB에 구성 된 서버 이외의 컴퓨터에서 웹 브라우저를 열고, NLB FQDN을 사용 하 여 MBAM 관리 및 모니터링 웹 사이트에 액세스할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df78-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="0df78-151">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0df78-151">Related topics</span></span>


[<span data-ttu-id="0df78-152">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="0df78-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





