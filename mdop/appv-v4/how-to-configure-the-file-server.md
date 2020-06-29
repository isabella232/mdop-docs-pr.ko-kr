---
title: 파일 서버를 구성하는 방법
description: 파일 서버를 구성하는 방법
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817783"
---
# <span data-ttu-id="24487-103">파일 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="24487-103">How to Configure the File Server</span></span>


<span data-ttu-id="24487-104">다음 절차를 사용 하 여 파일 공유로 사용 되는 로컬 컴퓨터를 구성 하 고 응용 프로그램 가상화 데스크톱 클라이언트와 원격 데스크톱 서비스용 클라이언트 (이전의 터미널 서비스)로 스트림 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24487-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="24487-105">이 시나리오는 기존 하드웨어 환경에 추가 서버 인프라를 추가 하지 않으려는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24487-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="24487-106">로컬 사무실에 설치 된 파일 공유의 배포 지점으로 응용 프로그램 가상화 관리 서버를 사용 하는 경우 가상 응용 프로그램을 파일 공유로 사용 되는 컴퓨터로 스트림할 수 있으려면 먼저이 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24487-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="24487-107">서버와 파일 공유를 구성 하는 경우 SFT 파일이 로드 되 고 저장 되는 콘텐츠 디렉터리를 설정 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24487-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="24487-108">SFT 파일에는 가상 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24487-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="24487-109">**중요**  응용 프로그램 가상화 데스크톱 클라이언트 및 원격 데스크톱 서비스에 대 한 클라이언트에 올바르게 스트리밍할 수 있도록 응용 프로그램에서 가상 응용 프로그램을 저장 하는 서버의 콘텐츠 디렉터리에서 SFT 파일이 스트리밍됩니다. .ICO (아이콘) 파일 및 OSD (개방형 소프트웨어 설명자) 파일을 다른 서버에서 스트림할 수 있도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24487-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="24487-110">Application Virtualization 파일 서버를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="24487-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="24487-111">배포 점으로 사용 되는 서버를 구성 하려면 다음 설치 절차를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="24487-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="24487-112">Application Virtualization Management Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="24487-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="24487-113">**참고**  설치 절차 중에 **콘텐츠 경로** 화면에서 \\content 디렉터리의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24487-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="24487-114">서버를 설치할 때 지정한 디렉터리에 해당 하는 \\Content 디렉터리를 파일 공유로 사용 하는 각 컴퓨터에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24487-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="24487-115">**중요**  Application Virtualization Server 또는 IIS 서버가 아닌 파일 공유로 사용 하는 컴퓨터에서 응용 프로그램을 스트림 하는 응용 프로그램 가상화 데스크톱 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="24487-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="24487-116">\\Content 디렉터리가 만들어지면이 디렉토리를 표준 파일 공유로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="24487-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="24487-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="24487-117">Related topics</span></span>


[<span data-ttu-id="24487-118">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="24487-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="24487-119">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="24487-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="24487-120">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="24487-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="24487-121">Application Virtualization Streaming Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="24487-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="24487-122">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="24487-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





