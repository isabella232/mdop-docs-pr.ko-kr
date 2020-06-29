---
title: Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시
description: Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815768"
---
# <span data-ttu-id="91738-103">Application Virtualization Management Server를 사용하여 가상 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="91738-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="91738-104">응용 프로그램 가상화 서버 기반 배포에서 시퀀싱 하 고, 테스트를 수행 하 고, 배포 가능한 가상 응용 프로그램 패키지를 응용 프로그램 가상화 관리 서버에서 사용할 주 콘텐츠 공유에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="91738-105">패키지를 응용 프로그램 가상화 관리 서버에서 가져온 후 최종 사용자에 게 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91738-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="91738-106">**참고**  콘텐츠 공유는 서버의 연결 된 디스크 저장소에 위치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="91738-107">SAN 또는 DFS 공유와 같은 네트워크 저장소 장치를 사용 하는 것은 네트워크에 영향을 주므로 신중 하 게 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="91738-108">Active Directory 그룹으로 응용 프로그램을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="91738-109">일반적으로 응용 프로그램 가상화 관리자는 게시할 각 가상 응용 프로그램에 대 한 Active Directory 그룹을 만든 다음 해당 사용자를 해당 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="91738-110">사용자가 워크스테이션에 로그온 할 때 응용 프로그램 가상화 클라이언트는 기본적으로 로그온 한 사용자의 자격 증명을 사용 하 여 게시 새로 고침을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="91738-111">그러면 사용자는 바로 가기가 배치 된 위치에서 응용 프로그램을 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91738-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="91738-112">응용 프로그램 가상화 관리자는 응용 프로그램의 순서를 지정 하는 동안 클라이언트 시스템에 있는 바로 가기의 위치 및 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91738-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="91738-113">**참고**  *게시 새로 고침은* 최종 사용자가 사용할 수 있도록 클라이언트에 전송 되는 가상 응용 프로그램 바로 가기를 결정 하기 위해 응용 프로그램 가상화 클라이언트에 정의 된 응용 프로그램 가상화 서버에 대 한 호출입니다.</span><span class="sxs-lookup"><span data-stu-id="91738-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="91738-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="91738-114">Related topics</span></span>


[<span data-ttu-id="91738-115">Application Virtualization Server 기반 시나리오</span><span class="sxs-lookup"><span data-stu-id="91738-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="91738-116">클라이언트에 가상 응용 프로그램을 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="91738-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="91738-117">Application Virtualization 시스템 구성 요소 개요</span><span class="sxs-lookup"><span data-stu-id="91738-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="91738-118">Application Virtualization Server 기반 구현에서 스트리밍 솔루션 계획</span><span class="sxs-lookup"><span data-stu-id="91738-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





