---
title: Application Virtualization Management Server 구성 방법
description: Application Virtualization Management Server 구성 방법
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817843"
---
# <span data-ttu-id="f2faf-103">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="f2faf-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="f2faf-104">가상화 된 응용 프로그램을 Application Virtualization 데스크톱 클라이언트 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 클라이언트로 스트림할 수 있으려면 먼저 Application Virtualization 관리 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="f2faf-105">서버를 구성할 때 SFT 파일이 로드 되 고 저장 되는 *콘텐츠 디렉터리* 를 설정 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="f2faf-106">SFT 파일에는 가상화 된 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="f2faf-107">**중요**  Application Virtualization 서버는 RTSP 또는 RTSPS 프로토콜만 사용 하 여 원격 데스크톱 서비스에 대 한 클라이언트와 데스크톱 클라이언트에 SFT 파일을 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="f2faf-108">.ICO (아이콘) 파일 및 OSD (개방형 소프트웨어 설명자) 파일은 다른 파일 또는 HTTP 서버에서 스트림할 수 있도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="f2faf-109">응용 프로그램 가상화 관리 서버를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="f2faf-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="f2faf-110">다음 절차를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="f2faf-111">Application Virtualization Management Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="f2faf-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="f2faf-112">**참고**  설치 절차 중에 **콘텐츠 경로** 화면에서 \\content 디렉터리의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="f2faf-113">\\Content 디렉터리에 대해 지정한 위치로 이동 하 고, 필요한 경우 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="f2faf-114">콘텐츠 디렉터리가 만들어지면이 디렉터리를 표준 파일 공유로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2faf-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="f2faf-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f2faf-115">Related topics</span></span>


[<span data-ttu-id="f2faf-116">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="f2faf-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="f2faf-117">Application Virtualization 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="f2faf-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="f2faf-118">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="f2faf-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="f2faf-119">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="f2faf-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





