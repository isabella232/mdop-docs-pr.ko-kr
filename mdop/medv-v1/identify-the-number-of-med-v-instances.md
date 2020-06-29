---
title: MED-V 인스턴스의 수 식별
description: MED-V 인스턴스의 수 식별
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824258"
---
# <span data-ttu-id="734cd-103">MED-V 인스턴스의 수 식별</span><span class="sxs-lookup"><span data-stu-id="734cd-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="734cd-104">서버 인프라를 디자인할 수 있도록 각 인스턴스의 범위를 정의 하는 것은 물론 MED-V 인스턴스의 수를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="734cd-105">MED-V 인스턴스에는 다음이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="734cd-106">Active Directory 권한을 포함 하 여 MED-V 서버와 서버에 저장 된 MED-V 작업 영역</span><span class="sxs-lookup"><span data-stu-id="734cd-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="734cd-107">클라이언트 이벤트를 저장 하는 SQL Server 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="734cd-108">데이터베이스가 여러 MED-V 인스턴스에서 공유 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="734cd-109">압축 된 MED-V 이미지의 이미지 리포지토리입니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="734cd-110">리포지토리가 여러 MED-V 인스턴스에서 공유 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="734cd-111">이미지를 만들고 압축 하 고 MED-V 작업 영역을 만드는 데 사용 되는 관리 콘솔입니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="734cd-112">콘솔은 여러 MED-V 인스턴스에서 동시에 사용할 수 없지만 MED-V 서버 하나에서 연결을 끊은 다음 다른 MED-V 서버에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="734cd-113">MED-V 작업 영역을 수신 하는 MED-V 클라이언트와 서버에서 사용할 수 있는 권한 부여</span><span class="sxs-lookup"><span data-stu-id="734cd-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="734cd-114">별도의 MED-V 인스턴스는 통합 하거나 MED-V 작업 영역을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="734cd-115">따라서 각 추가 인스턴스는 각각 가상화 관리를 decentralizes.</span><span class="sxs-lookup"><span data-stu-id="734cd-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="734cd-116">필요한 MED-V 인스턴스 수를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="734cd-117">먼저 MED-V 인스턴스 하나를 사용 한다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="734cd-118">그런 다음 다음 조건을 고려 하 고 인프라에 적용 되는 각 조건에 대해 다른 인스턴스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="734cd-119">지원 되는 사용자 수 — 각 MED-V 인스턴스는 최대 5000 개의 동시 활성 클라이언트를 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="734cd-120">동시 활성 상태는 클라이언트가 MED-V 서버와 온라인 상태 이며 정책 및 이미지 업데이트 및 이벤트에 대 한 투표를 서버에 보내는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="734cd-121">인프라에 5000 활성 사용자가 포함 될 경우 모든 5000 사용자에 대해 하나의 인스턴스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="734cd-122">신뢰할 수 없는 도메인의 사용자-MED-V 서버는 Active Directory 사용자 및/또는 그룹과의 MED-V 작업 영역 사용 권한을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="734cd-123">이를 위해서는 med-v 사용자가 MED-V 서버의 신뢰 경계 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="734cd-124">신뢰할 수 없는 별도의 도메인에 있는 각 MED-V 사용자 그룹에 대해 MED-V 인스턴스를 하나씩 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="734cd-125">격리 된 네트워크의 클라이언트-클라이언트가 격리 되어 별도의 MED-V 인스턴스가 필요한 네트워크에 존재 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="734cd-126">예를 들어 조직에서 랩 네트워크를 프로덕션 네트워크에서 격리 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="734cd-127">MED-V 클라이언트를 포함할 격리 된 각 네트워크에 대 한 MED-V 인스턴스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="734cd-128">조직 요구 사항-조직에서 중요 한 응용 프로그램이 도메인 내의 제한 된 사용자 에게만 제공 되는 경우와 같이 보안 상의 이유로 인해 클라이언트 그룹을 별도의 MED-V 인스턴스에서 관리 하도록 요구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="734cd-129">예를 들어, 급여 부서가 급여 처리에 대 한 정책을 저장 하는 MED-V 인스턴스에 대 한 액세스를 다른 부서의 사용자에 게 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="734cd-130">또한 조직에서 분산 관리 모델을 사용 하는 경우 해당 그룹이 자체 가상화 된 환경을 관리할 수 있도록 하기 위해 MED-V 클라이언트가 있는 각 비즈니스 그룹에 대해 별도의 MED-V 인스턴스가 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="734cd-131">각각의 개별 조직 요구 사항에 대해 MED-V 인스턴스를 하나씩 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="734cd-132">법률 고려 사항-국내 보안 또는 개인정보 보호 문제 및 fiduciary 법률은 특정 데이터를 분리 하거나 다른 데이터의 국경가 교차 되지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="734cd-133">필요한 경우이 요구 사항을 해결 하기 위해 MED-V 인스턴스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="734cd-134">인프라에 필요한 MED-V 인스턴스와 각 인스턴스에 대 한 이유를 결정 한 후 각 인스턴스의 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="734cd-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 





