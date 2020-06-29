---
title: 수동으로 MED-V 호스트 에이전트를 설치하는 방법
description: 수동으로 MED-V 호스트 에이전트를 설치하는 방법
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812897"
---
# <span data-ttu-id="f9e83-103">수동으로 MED-V 호스트 에이전트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9e83-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="f9e83-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 솔루션에는 별도의 두 가지 관련 구성 요소가 있습니다 (MED-V 호스트 에이전트와 게스트 에이전트).</span><span class="sxs-lookup"><span data-stu-id="f9e83-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="f9e83-105">호스트 에이전트는 호스트 컴퓨터 (Windows 7을 실행 하는 사용자 컴퓨터)에 있으며 MED-V 게스트 (호스트 컴퓨터에서 실행 되는 MED-V 가상 컴퓨터)와 통신 하는 데 사용 되는 채널을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="f9e83-106">또한 응용 프로그램 게시와 같은 특정 MED-V 관련 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="f9e83-107">일반적으로 회사의 기본 제공 소프트웨어 방법을 사용 하 여 MED-V 호스트 에이전트를 배포 하 고 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="f9e83-108">그러나 엔터프라이즈에서 MED-V를 배포 하기 전에 테스트를 위해 로컬로 호스트 에이전트를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="f9e83-109">이 섹션에서는 MED-V 호스트 에이전트를 수동으로 설치 하는 방법에 대 한 단계별 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="f9e83-110">**참고**  MED-V 게스트 에이전트는 처음 설정 하는 동안 자동으로 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="f9e83-111">**중요**  MED-V 호스트 에이전트를 설치 하기 전에 Internet Explorer를 닫은 경우 나중에 URL 리디렉션으로 충돌이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="f9e83-112">배포 중에 컴퓨터 다시 시작을 지정 하 여이 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="f9e83-113">MED-V 호스트 에이전트를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="f9e83-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="f9e83-114">소프트웨어 다운로드의 일부로 받은 MED-V 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="f9e83-115">MED-V \ _HostAgent \ _Setup 설치 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="f9e83-116">**Microsoft 엔터프라이즈 데스크톱 가상화 (med-v) 호스트 에이전트 설정** 마법사가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="f9e83-117">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="f9e83-118">Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="f9e83-119">MED-V 호스트 에이전트를 설치할 대상 폴더를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="f9e83-120">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-120">Click **Next**.</span></span>

5.  <span data-ttu-id="f9e83-121">호스트 에이전트 설치를 시작 하려면 **설치**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="f9e83-122">설치가 성공적으로 완료 되 면 **마침을** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="f9e83-123">호스트 에이전트를 성공적으로 설치 했는지 확인 하려면 **시작**, **모든 프로그램**, **Microsoft 엔터프라이즈 데스크톱 가상화**, **med-v 호스트 에이전트**를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="f9e83-124">**참고**  MED-V 작업 영역이 설치 될 때까지 MED-V 호스트 에이전트를 시작 하 고 실행할 수 있지만 기능은 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e83-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="f9e83-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f9e83-125">Related topics</span></span>


[<span data-ttu-id="f9e83-126">전자 소프트웨어 배포 시스템을 통해 MED-V 구성 요소를 배포하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9e83-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="f9e83-127">MED-V 작업 영역 패키지 관리자를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9e83-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="f9e83-128">MED-V 구성 요소를 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="f9e83-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





