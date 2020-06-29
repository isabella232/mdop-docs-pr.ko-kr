---
title: 전자 소프트웨어 배포 기반 시나리오
description: 전자 소프트웨어 배포 기반 시나리오
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821593"
---
# <span data-ttu-id="0b3cd-103">전자 소프트웨어 배포 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="0b3cd-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="0b3cd-104">Microsoft 응용 프로그램 가상화 환경에 대 한 ESD (전자 소프트웨어 배포) 배포 시나리오를 사용 하는 경우에는 해당 의사 결정에 영향을 주는 요소를 이해 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="0b3cd-105">이 섹션의 항목에서는 ESD 시나리오에 대해 설명 하 고 배포 전략에서 고려해 야 하는 패키지 전달 메서드, 전송 프로토콜 및 외부 구성 요소에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="0b3cd-106">이 섹션의 절차를 사용 하 여 배포 확인 단계를 통해 서버 구성 단계에서 배포를 완료할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="0b3cd-107">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="0b3cd-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="0b3cd-108">전자 소프트웨어 배포 기반 시나리오 개요</span><span class="sxs-lookup"><span data-stu-id="0b3cd-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="0b3cd-109">ESD 기반 배포에 사용할 수 있는 게시 및 스트리밍 메서드에 대 한 중요 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="0b3cd-110">ESD 기반 배포용 서버를 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b3cd-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="0b3cd-111">이 섹션에서는 전자 소프트웨어 배포 기반 배포 전략에 대 한 응용 프로그램 가상화 스트리밍 서버, IIS 서버, 파일 서버를 구성 하는 데 사용할 수 있는 절차에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="0b3cd-112">명령줄을 사용하여 클라이언트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b3cd-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="0b3cd-113">setup.exe 또는 setup.msi 파일 중 하나를 사용 하 여 응용 프로그램 가상화 클라이언트를 설치 하기 위한 명령줄 프로시저를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="0b3cd-114">App-V Client 제거 방법</span><span class="sxs-lookup"><span data-stu-id="0b3cd-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="0b3cd-115">응용 프로그램 가상화 클라이언트가 설치 되었고 올바르게 작동 하는지 확인 하는 데 사용할 수 있는 단계별 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="0b3cd-116">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="0b3cd-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="0b3cd-117">Windows Installer 또는 SFTMIME 중 하나를 사용 하 여 응용 프로그램 패키지를 게시 하기 위한 명령줄 프로시저를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3cd-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="0b3cd-118">참고자료</span><span class="sxs-lookup"><span data-stu-id="0b3cd-118">Reference</span></span>


[<span data-ttu-id="0b3cd-119">Application Virtualization Client 설치 관리자 명령줄 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b3cd-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="0b3cd-120">관련 섹션</span><span class="sxs-lookup"><span data-stu-id="0b3cd-120">Related Sections</span></span>


[<span data-ttu-id="0b3cd-121">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="0b3cd-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="0b3cd-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0b3cd-122">Related topics</span></span>


[<span data-ttu-id="0b3cd-123">Application Virtualization 배포 및 업그레이드 고려 사항</span><span class="sxs-lookup"><span data-stu-id="0b3cd-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="0b3cd-124">Application Virtualization Client에 대한 독립 실행형 배달 시나리오</span><span class="sxs-lookup"><span data-stu-id="0b3cd-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





