---
title: 서버 기반 배포용 서버를 구성하는 방법
description: 서버 기반 배포용 서버를 구성하는 방법
author: dansimp
ms.assetid: 6371c37a-46eb-44e8-ad6b-4430c866c8b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c60ae89bc42fddad8aeb6a4f6df0f2c0b4ee4f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817918"
---
# <span data-ttu-id="a089e-103">서버 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-103">How to Configure Servers for Server-Based Deployment</span></span>


<span data-ttu-id="a089e-104">이 섹션에서는 Microsoft System Center Application Virtualization (App-v) 관리 서버와 Microsoft System Center 응용 프로그램 가상화 스트리밍 서버와 응용 프로그램 가상화 서버 기반 배포 전략에 맞게 IIS (인터넷 정보 서비스) 및 파일 서버를 구성 하는 데 사용할 수 있는 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-104">This section provides procedures you can use to configure the Microsoft System Center Application Virtualization (App-V) Management Servers and Microsoft System Center Application Virtualization Streaming Servers, and the Internet Information Services (IIS) and file servers, as appropriate for your Application Virtualization Server-based deployment strategy.</span></span>

## <span data-ttu-id="a089e-105">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="a089e-105">In This Section</span></span>


<a href="" id="how-to-configure-the-application-virtualization-management-servers"></a>[<span data-ttu-id="a089e-106">Application Virtualization Management Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-106">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)  
<span data-ttu-id="a089e-107">응용 프로그램 가상화 관리 서버를 구성 하기 위한 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-107">Provides a step-by-step procedure for configuring the Application Virtualization Management Servers.</span></span>

<a href="" id="how-to-configure-the-application-virtualization-streaming-servers"></a>[<span data-ttu-id="a089e-108">Application Virtualization Streaming Server 구성 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-108">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)  
<span data-ttu-id="a089e-109">Application Virtualization 스트리밍 서버를 구성 하기 위한 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-109">Provides a step-by-step procedure for configuring the Application Virtualization Streaming Servers.</span></span>

<a href="" id="how-to-configure-the-server-for-iis"></a>[<span data-ttu-id="a089e-110">IIS용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-110">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)  
<span data-ttu-id="a089e-111">서버 기반 배포에 대해 IIS 서버를 구성 하는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-111">Provides a step-by-step procedure for configuring the IIS server for your server-based deployment.</span></span>

<a href="" id="how-to-configure-the-server-to-be-trusted-for-delegation"></a>[<span data-ttu-id="a089e-112">위임을 위해 신뢰할 수 있는 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-112">How to Configure the Server to be Trusted for Delegation</span></span>](how-to-configure-the-server-to-be-trusted-for-delegation.md)  
<span data-ttu-id="a089e-113">위임용으로 트러스트 되도록 서버를 구성 하는 방법에 대 한 자세한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-113">Provides detailed instructions about how to configure the server to be trusted for delegation.</span></span>

<a href="" id="configuring-the-firewall-for-the-app-v-servers"></a>[<span data-ttu-id="a089e-114">App-V Server용 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="a089e-114">Configuring the Firewall for the App-V Servers</span></span>](configuring-the-firewall-for-the-app-v-servers.md)  
<span data-ttu-id="a089e-115">App-v 서버에 필요한 방화벽 설정에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-115">Describes the firewall settings required for the App-V servers.</span></span>

<a href="" id="how-to-install-and-configure-the-default-application"></a>[<span data-ttu-id="a089e-116">기본 응용 프로그램을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-116">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)  
<span data-ttu-id="a089e-117">App-v 시스템을 테스트 하기 위한 기본 응용 프로그램을 설치 하 고 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089e-117">Describes how to install and configure the default application for testing the App-V system.</span></span>

## <span data-ttu-id="a089e-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a089e-118">Related topics</span></span>


[<span data-ttu-id="a089e-119">Application Virtualization Server 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="a089e-119">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="a089e-120">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="a089e-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="a089e-121">서버 및 시스템 구성 요소 설치 방법</span><span class="sxs-lookup"><span data-stu-id="a089e-121">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





