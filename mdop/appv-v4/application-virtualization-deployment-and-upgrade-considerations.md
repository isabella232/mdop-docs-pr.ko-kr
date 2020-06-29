---
title: Application Virtualization 배포 및 업그레이드 고려 사항
description: Application Virtualization 배포 및 업그레이드 고려 사항
author: dansimp
ms.assetid: adc562ee-7276-4b14-b10a-da17f05e1682
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9e6c1a624b9da18bba75c5f3816a8e9c5391a8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822243"
---
# <span data-ttu-id="e50db-103">Application Virtualization 배포 및 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="e50db-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="e50db-104">Microsoft Application Virtualization 배포를 시작 하기 전에 다양 한 응용 프로그램 가상화 구성 요소를 설치 하기 위한 하드웨어 및 소프트웨어 요구 사항을 포함 하 여 환경 요구 사항을 검토 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-104">Before you begin the deployment of Microsoft Application Virtualization, you might need to review your environment requirements, including the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="e50db-105">또한 이전 버전에서 업그레이드 하는 경우이 섹션의 항목에서는 현재 Sequencer, 서버 및 클라이언트 버전을 업그레이드 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-105">Also, if you are upgrading from a previous version, the topics in this section provide information about upgrading your current Sequencer, server, and client versions.</span></span>

## <span data-ttu-id="e50db-106">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="e50db-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="e50db-107">Application Virtualization 배포 요구 사항</span><span class="sxs-lookup"><span data-stu-id="e50db-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="e50db-108">응용 프로그램 가상화 배포에 대 한 시스템 요구 사항 및 업그레이드 고려 사항에 대 한 일반적인 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="e50db-109">Application Virtualization Client를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="e50db-109">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="e50db-110">원격 데스크톱 서비스 (이전의 터미널 서비스)의 application virtualization 데스크톱 클라이언트 또는 응용 프로그램 가상화 클라이언트를 업그레이드 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-110">Provides step-by-step procedures for upgrading the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="e50db-111">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="e50db-111">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="e50db-112">모든 응용 프로그램 가상화 시스템 컴퓨터에 설치 된 소프트웨어 구성 요소를 업그레이드 하는 데 사용할 수 있는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-112">Provides a step-by-step procedure you can use to upgrade the software components installed on all Application Virtualization System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="e50db-113">Application Virtualization Sequencer 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="e50db-113">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="e50db-114">Windows Vista 또는 WindowsXP를 실행 하는 컴퓨터에서 시퀀서를 업그레이드 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-114">Provides step-by-step procedures for upgrading the Sequencer on computers running Windows Vista or WindowsXP.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="e50db-115">Application Virtualization Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="e50db-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="e50db-116">시퀀서를 설치 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50db-116">Provides a step-by-step procedure for installing the Sequencer.</span></span>

## <span data-ttu-id="e50db-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e50db-117">Related topics</span></span>


[<span data-ttu-id="e50db-118">Application Virtualization 참조</span><span class="sxs-lookup"><span data-stu-id="e50db-118">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="e50db-119">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="e50db-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="e50db-120">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="e50db-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="e50db-121">Application Virtualization Client에 대한 독립 실행형 배달 시나리오</span><span class="sxs-lookup"><span data-stu-id="e50db-121">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





