---
title: Application Virtualization Streaming Server 구성 방법
description: Application Virtualization Streaming Server 구성 방법
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817823"
---
# <span data-ttu-id="39f5a-103">Application Virtualization Streaming Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="39f5a-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="39f5a-104">가상 응용 프로그램을 Application Virtualization 데스크톱 클라이언트 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 클라이언트로 스트림할 수 있으려면 먼저 Application Virtualization 스트리밍 서버를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="39f5a-105">서버를 구성할 때 SFT 파일이 로드 되 고 저장 되는 *콘텐츠 디렉터리* 를 설정 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="39f5a-106">SFT 파일에는 가상 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="39f5a-107">**중요**  Application Virtualization 서버는 RTSP 또는 RTSPS 프로토콜만 사용 하 여 원격 데스크톱 서비스에 대 한 클라이언트와 데스크톱 클라이언트에 SFT 파일을 스트리밍합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="39f5a-108">.ICO (아이콘) 파일 및 OSD (개방형 소프트웨어 설명자) 파일은 다른 파일 또는 HTTP 서버에서 스트림할 수 있도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="39f5a-109">Application Virtualization 스트리밍 서버를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="39f5a-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="39f5a-110">Application Virtualization 스트리밍 서버용 설치 절차를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="39f5a-111">설치 절차 중에 **콘텐츠 경로** 화면에서 \\content 디렉터리의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="39f5a-112">\\Content 디렉터리에 대해 지정한 위치로 이동 하 고 필요한 경우 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="39f5a-113">콘텐츠 디렉터리가 만들어지면이 디렉터리를 표준 파일 공유로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="39f5a-114">Content 디렉터리 아래에 있는 콘텐츠 디렉터리와 패키지 폴더에 대 한 NTFS 파일 시스템 사용 권한을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="39f5a-115">각 응용 프로그램에 액세스할 수 있는 사용자를 정의 하는 Active Directory 도메인 서비스의 보안 그룹을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f5a-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="39f5a-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="39f5a-116">Related topics</span></span>


[<span data-ttu-id="39f5a-117">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="39f5a-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="39f5a-118">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="39f5a-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="39f5a-119">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="39f5a-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="39f5a-120">파일 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="39f5a-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="39f5a-121">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="39f5a-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





