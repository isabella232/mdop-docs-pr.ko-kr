---
title: MED-V 이미지 리포지토리 디자인
description: MED-V 이미지 리포지토리 디자인
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823613"
---
# <span data-ttu-id="d99a6-103">MED-V 이미지 리포지토리 디자인</span><span class="sxs-lookup"><span data-stu-id="d99a6-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="d99a6-104">MED-V 이미지를 만들어 압축 한 후에는 임의의 위치에 있는 파일 서버에 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="d99a6-105">파일이 HTTP 또는 HTTPS를 통해 하나 이상의 IIS 서버에 의해 전송 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="d99a6-106">이미지 리포지토리는 여러 MED-V 인스턴스에서 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="d99a6-107">이미지 리포지토리를 디자인 하려면 먼저 각 클라이언트에 이미지를 배포 하는 방법과 해당 클라이언트에 로컬 이미지 리포지토리가 필요한 지 여부를 결정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="d99a6-108">그런 다음 각 리포지토리가 해당 IIS 서버와 함께 디자인 및 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="d99a6-109">이미지가 배포 되는 방법 결정</span><span class="sxs-lookup"><span data-stu-id="d99a6-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="d99a6-110">각 MED-V 작업 영역에 대해 클라이언트에 MED-V 이미지를 배포 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="d99a6-111">이는 압축 된 이미지를 저장 하는 데 필요한 저장소 수를 결정 하 고 해당 리포지토리를 배치할 다음 해당 리포지토리를 디자인할 때 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="d99a6-112">압축 된 이미지는 다음과 같은 방식으로 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="d99a6-113">파일 서버 및 IIS 서버로 구성 된 이미지 배포 서버에서 네트워크를 통해 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="d99a6-114">USB 드라이브 또는 DVD와 같은 이동식 미디어</span><span class="sxs-lookup"><span data-stu-id="d99a6-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="d99a6-115">엔터프라이즈 소프트웨어 배포 센터를 사용 하 여 클라이언트 컴퓨터의 이미지 저장소 디렉터리에 미리 준비 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="d99a6-116">각 클라이언트에 MED-V 이미지를 배포 하는 데 사용할 메서드 또는 메서드를 결정 하 고 위치에 이미지 리포지토리가 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="d99a6-117">이미지 리포지토리의 수 결정</span><span class="sxs-lookup"><span data-stu-id="d99a6-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="d99a6-118">이제 필요한 최소 저장소 수를 결정 했으므로 다음 조건 중 하나라도 적용 되는 경우 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="d99a6-119">MED-V 이미지를 구분 하는 조직 또는 규정 상의 이유, 일부 MED-V 이미지는 동일한 리포지토리에 공존할 수 없을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="d99a6-120">예를 들어 중요 한 개인 데이터에는 데이터에 액세스 해야 하는 제한 된 직원 에게만 사용할 수 있는 서버에 저장소가 필요할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="d99a6-121">격리 된 네트워크의 클라이언트-이미지가 네트워크를 통해 배포 되는 경우 네트워크가 격리 되 고 별도의 저장소가 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="d99a6-122">예를 들어 조직에서 랩 네트워크를 프로덕션 네트워크에서 격리 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="d99a6-123">원격 네트워크의 클라이언트-이미지가 네트워크를 통해 배포 되는 경우에는 클라이언트가 MED-V 작업 영역을 로드할 때 적절 한 환경을 제공 하기에 충분 한 대역폭이 없는 네트워크 링크를 통해 일부 클라이언트 컴퓨터가 리포지토리와 분리 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="d99a6-124">필요한 경우이 요구 사항을 해결 하기 위해 추가 MED-V 인스턴스를 디자인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="d99a6-125">이러한 리포지토리를 디자인에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-125">Add these repositories to the design.</span></span> <span data-ttu-id="d99a6-126">각 리포지토리의 이름과 디자인 이유를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="d99a6-127">리포지토리에서 보관할 MED-V 이미지와 리포지토리의 이미지를 사용 하 여 MED-V 작업 영역을 로드할 MED-V 클라이언트를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="d99a6-128">이미지 리포지토리 디자인 및 배치</span><span class="sxs-lookup"><span data-stu-id="d99a6-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="d99a6-129">클라이언트가 새 이미지를 사용할 수 있게 되 면 클라이언트가 동시에 이미지를 다운로드 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="d99a6-130">이는 리포지토리에 대 한 높은 수요를 만들며, 이미지 리포지토리를 설계할 때 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="d99a6-131">각 저장소에 대해 저장할 데이터의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="d99a6-132">리포지토리에 저장 되는 이미지의 크기를 합산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="d99a6-133">파일 서버에 필요한 디스크 공간 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="d99a6-134">그런 다음 리포지토리에 MED-V 이미지를 다운로드할 수 있는 클라이언트 수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="d99a6-135">이는 새 MED-V 이미지가 리포지토리에 로드 될 때 발생할 수 있는 최대 동시 다운로드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="d99a6-136">파일 서버는이를 만들 IO 요구를 충족 시킬 수 있는 디스크 하위 시스템으로 설계 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="d99a6-137">이미지 리포지토리는 MED-V 서버와 동일한 시스템, SQL Server를 실행 하는 서버 또는 원격 파일 공유에 상주할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="d99a6-138">Windows Server2008 Hyper-v VM 에서도 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="d99a6-139">이미지 리포지토리가 서비스 하는 클라이언트의 네트워크 위치를 확인 하 고 해당 클라이언트의 서비스 수준 요구에 맞는 충분 한 대역폭을 네트워크 위치에 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="d99a6-140">내결함성은</span><span class="sxs-lookup"><span data-stu-id="d99a6-140">Fault Tolerance</span></span>

<span data-ttu-id="d99a6-141">이미지 리포지토리를 사용할 수 없는 경우 클라이언트에서 새 MED-V 이미지를 다운로드 하거나 업데이트를 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="d99a6-142">파일 서버 및 결함 허용 디스크에 대 한 내결함성 옵션을 디자인 하려면 [인프라 계획 및 디자인 MICROSOFT SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) 가이드를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d99a6-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="d99a6-143">IIS 서버 디자인 및 배치</span><span class="sxs-lookup"><span data-stu-id="d99a6-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="d99a6-144">이 섹션은 클라이언트가 HTTP 또는 HTTPS를 사용 하 여 네트워크를 통해 이미지 파일을 다운로드 하는 경우에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="d99a6-145">IIS 서버는 MED-V 서버와 SQL Server를 실행 하는 서버와 동일한 시스템에 공존할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="d99a6-146">Windows Server2008 Hyper-v VM 에서도 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="d99a6-147">IIS 서버 인프라는 조직의 서비스 수준에 대 한 기대 범위 내에서 클라이언트에 이미지를 전달 하는 데 충분 한 처리량이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="d99a6-148">이는 자신이 만드는 IO 요구를 충족 시킬 수 있는 디스크 하위 시스템으로 설계 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="d99a6-149">각 이미지 리포지토리에 대해 IIS를 사용 하 여 MED-V 이미지를 다운로드할 수 있는 클라이언트 수의 합계를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="d99a6-150">이는 이미지가 리포지토리에 로드 될 때 발생할 수 있는 최대 동시 다운로드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="d99a6-151">[프로젝트 범위 정의](define-the-project-scope.md) 에서 결정 된 처리량 합계 및 서비스 수준 기대치를 사용 하 여 IIS 서버 인프라의 디자인을 계획 하 고 리포지토리에 할당할 적절 한 대역폭을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="d99a6-152">IIS 인프라를 디자인 하려면 [Microsoft 인터넷 정보 서비스 가이드의 인프라 계획 및 디자인](https://go.microsoft.com/fwlink/?LinkId=160826) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d99a6-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="d99a6-153">내결함성은</span><span class="sxs-lookup"><span data-stu-id="d99a6-153">Fault Tolerance</span></span>

<span data-ttu-id="d99a6-154">IIS 서버 인프라를 사용할 수 없는 경우 클라이언트에서 새 이미지나 업데이트 된 이미지를 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="d99a6-155">내결함성 구성을 위해 Windows Server2008 기반 IIS 서버를 장애 조치 클러스터에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d99a6-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="d99a6-156">IIS 서버 인프라에 대 한 내결함성을 디자인 하려면 [Microsoft 인터넷 정보 서비스 가이드의 인프라 계획 및 디자인](https://go.microsoft.com/fwlink/?LinkId=160826) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d99a6-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="d99a6-157">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d99a6-157">Related topics</span></span>


[<span data-ttu-id="d99a6-158">엔터프라이즈 소프트웨어 배포 시스템을 사용하여 MED-V 작업 영역 배포</span><span class="sxs-lookup"><span data-stu-id="d99a6-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="d99a6-159">배포 패키지를 사용하여 MED-V 작업 영역 배포</span><span class="sxs-lookup"><span data-stu-id="d99a6-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





