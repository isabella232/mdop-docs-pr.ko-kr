---
title: Application Virtualization 배포 및 업그레이드 고려 사항
description: Application Virtualization 배포 및 업그레이드 고려 사항
author: dansimp
ms.assetid: c3c38930-0da3-43e6-b240-945edfd00a01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09e6943c74c7f17b6a61bc7be4bcde925a54be56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822273"
---
# <span data-ttu-id="98b1f-103">Application Virtualization 배포 및 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="98b1f-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="98b1f-104">Microsoft Application Virtualization (App-v) 배포를 시작 하기 전에 다양 한 응용 프로그램 가상화 구성 요소를 설치 하기 위한 하드웨어 및 소프트웨어 요구 사항을 포함 하는 환경 요구 사항을 검토 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-104">Before you begin the deployment of Microsoft Application Virtualization (App-V), you might have to review your environment requirements that includes the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="98b1f-105">또한 이전 버전에서 업그레이드 하는 경우이 섹션의 항목에서는 현재 Sequencer, 서버 및 클라이언트 버전을 업그레이드 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-105">Also, if you are upgrading from an earlier version, the topics in this section provide information about how to upgrade your current Sequencer, Server, and Client versions.</span></span>

## <span data-ttu-id="98b1f-106">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="98b1f-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="98b1f-107">Application Virtualization 배포 요구 사항</span><span class="sxs-lookup"><span data-stu-id="98b1f-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="98b1f-108">응용 프로그램 가상화 배포에 대 한 시스템 요구 사항 및 업그레이드 고려 사항에 대 한 일반적인 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="application-virtualization-deployment-and-upgrade-checklists"></a>[<span data-ttu-id="98b1f-109">Application Virtualization 배포 및 업그레이드 검사 목록</span><span class="sxs-lookup"><span data-stu-id="98b1f-109">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)  
<span data-ttu-id="98b1f-110">특정 절차에 대 한 링크가 포함 된 설치 및 업그레이드 작업에 대 한 자세한 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-110">Provides detailed lists of installation and upgrade tasks with links to the specific procedures.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="98b1f-111">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="98b1f-111">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="98b1f-112">서버 기반 배포에 필요한 Application Virtualization (App-v) 플랫폼 구성 요소를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-112">Describes how to install the Application Virtualization (App-V) platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-manually-install-the-application-virtualization-client"></a>[<span data-ttu-id="98b1f-113">Application Virtualization Client를 수동으로 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="98b1f-113">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)  
<span data-ttu-id="98b1f-114">Application Virtualization 클라이언트 소프트웨어를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-114">Describes how to install the Application Virtualization Client software.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="98b1f-115">Application Virtualization Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="98b1f-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="98b1f-116">Application Virtualization Sequencer를 설치 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-116">Describes how to install the Application Virtualization Sequencer.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="98b1f-117">Application Virtualization Client를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="98b1f-117">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="98b1f-118">원격 데스크톱 서비스 (이전의 터미널 서비스) 용 application Virtualization 데스크톱 클라이언트 또는 Application Virtualization 클라이언트를 업그레이드 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-118">Describes how to upgrade the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="98b1f-119">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="98b1f-119">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="98b1f-120">모든 응용 프로그램 가상화 관리 시스템 컴퓨터에 설치 된 소프트웨어 구성 요소를 업그레이드 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-120">Describes how to upgrade the software components installed on all Application Virtualization Management System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="98b1f-121">Application Virtualization Sequencer 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="98b1f-121">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="98b1f-122">WindowsVista 또는 WindowsXP를 실행 하는 컴퓨터에서 Sequencer를 업그레이드 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="98b1f-122">Describes how to upgrade the Sequencer on computers that are running WindowsVista or WindowsXP.</span></span>

## <span data-ttu-id="98b1f-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="98b1f-123">Related topics</span></span>


[<span data-ttu-id="98b1f-124">Application Virtualization 참조</span><span class="sxs-lookup"><span data-stu-id="98b1f-124">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="98b1f-125">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="98b1f-125">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="98b1f-126">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="98b1f-126">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="98b1f-127">Application Virtualization Client에 대한 독립 실행형 배달 시나리오</span><span class="sxs-lookup"><span data-stu-id="98b1f-127">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





