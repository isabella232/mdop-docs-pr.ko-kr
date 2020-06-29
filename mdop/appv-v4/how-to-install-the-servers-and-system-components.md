---
title: 서버 및 시스템 구성 요소 설치 방법
description: 서버 및 시스템 구성 요소 설치 방법
author: dansimp
ms.assetid: c6f5fef0-522a-4ef1-8585-05b292d0289b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ceb5b8376189aee7631229dca912140e454536b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817243"
---
# <span data-ttu-id="6a3da-103">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-103">How to Install the Servers and System Components</span></span>


<span data-ttu-id="6a3da-104">사용자에 게 응용 프로그램을 배포 하려면 먼저 Microsoft Application Virtualization Platform 구성 요소를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-104">Before you can deliver applications to users, you must install the Microsoft Application Virtualization Platform components.</span></span> <span data-ttu-id="6a3da-105">이 섹션의 항목에서는 Application Virtualization Server 및 기타 응용 프로그램 가상화 시스템 구성 요소를 설치 하는 데 필요한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-105">The topics in this section provide the information required to install the Application Virtualization Servers and the other Application Virtualization System components.</span></span>

<span data-ttu-id="6a3da-106">**참고**  이 섹션의 절차에서는 프로덕션 환경에서 권장 하는 대로 별도의 컴퓨터에 설치할 구성 요소를 선택 하는 사용자 지정 설치를 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-106">**Note** The procedures in this section take you through a customized installation, where you pick and choose components to install on separate computers, as recommended in a production environment.</span></span> <span data-ttu-id="6a3da-107">그러나 운영 절차에서 다른 접근 방법을 지시할 수 있으며 설치 프로세스 중에 구성 요소를 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-107">However, your operating procedures might dictate a different approach, and during the installation process you might want to group components together.</span></span> <span data-ttu-id="6a3da-108">구성 요소를 설치 하는 위치에 관계 없이 원하는 순서 대로 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-108">Regardless of where you install the components, you can install them in any order.</span></span>

 

## <span data-ttu-id="6a3da-109">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="6a3da-109">In This Section</span></span>


<a href="" id="how-to-install-application-virtualization-management-server"></a>[<span data-ttu-id="6a3da-110">Application Virtualization Management Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-110">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)  
<span data-ttu-id="6a3da-111">응용 프로그램 가상화 관리 서버를 설치 하 고 해당 서버 그룹에 할당 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-111">Provides a step-by-step procedure for installing the Application Virtualization Management Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-application-virtualization-streaming-server"></a>[<span data-ttu-id="6a3da-112">Application Virtualization Streaming Server 설치 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-112">How to Install the Application Virtualization Streaming Server</span></span>](how-to-install-the-application-virtualization-streaming-server.md)  
<span data-ttu-id="6a3da-113">Application Virtualization 스트리밍 서버를 설치 하 고 적절 한 서버 그룹에 할당 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-113">Provides a step-by-step procedure for installing the Application Virtualization Streaming Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-management-web-service"></a>[<span data-ttu-id="6a3da-114">Management Web Service 설치 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-114">How to Install the Management Web Service</span></span>](how-to-install-the-management-web-service.md)  
<span data-ttu-id="6a3da-115">네트워크의 대상 컴퓨터에 응용 프로그램 가상화 관리 웹 서비스를 설치 하기 위한 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-115">Provides a step-by-step procedure for installing the Application Virtualization Management Web Service on a target computer on your network.</span></span>

<a href="" id="how-to-install-the-management-console"></a>[<span data-ttu-id="6a3da-116">Management Console 설치 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-116">How to Install the Management Console</span></span>](how-to-install-the-management-console.md)  
<span data-ttu-id="6a3da-117">네트워크의 대상 컴퓨터에 응용 프로그램 가상화 관리 콘솔을 설치 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-117">Provides a step-by-step procedure for installing the Application Virtualization Management Console on a target computer on your network.</span></span>

<a href="" id="how-to-install-a-database"></a>[<span data-ttu-id="6a3da-118">데이터베이스 설치 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-118">How to Install a Database</span></span>](how-to-install-a-database.md)  
<span data-ttu-id="6a3da-119">데이터베이스를 아직 사용할 수 없는 경우 응용 프로그램 가상화의 서버 기반 배포에 대 한 데이터베이스를 설치 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-119">Provides a step-by-step procedure for installing a database for your server-based deployment of Application Virtualization, if a database is not already available.</span></span>

<a href="" id="how-to-remove-the-application-virtualization-system-components"></a>[<span data-ttu-id="6a3da-120">Application Virtualization 시스템 구성 요소를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-120">How to Remove the Application Virtualization System Components</span></span>](how-to-remove-the-application-virtualization-system-components.md)  
<span data-ttu-id="6a3da-121">대상 컴퓨터에서 모든 또는 선택한 응용 프로그램 가상화 소프트웨어 구성 요소를 제거 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3da-121">Provides step-by-step procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

## <span data-ttu-id="6a3da-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6a3da-122">Related topics</span></span>


[<span data-ttu-id="6a3da-123">Application Virtualization Server 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="6a3da-123">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="6a3da-124">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-124">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="6a3da-125">서버 및 시스템 구성 요소를 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="6a3da-125">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)

 

 





