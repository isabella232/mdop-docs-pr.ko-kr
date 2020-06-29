---
title: Application Virtualization를 사용하여 온라인 또는 오프라인으로 작업하는 방법
description: Application Virtualization를 사용하여 온라인 또는 오프라인으로 작업하는 방법
author: dansimp
ms.assetid: aa532b37-8a00-4db4-9b51-e1e8354b2495
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0dfdd315fe607156135247c4a34d0248ef8fbdd9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816378"
---
# <span data-ttu-id="89873-103">Application Virtualization를 사용하여 온라인 또는 오프라인으로 작업하는 방법</span><span class="sxs-lookup"><span data-stu-id="89873-103">How to Work Offline or Online with Application Virtualization</span></span>


<span data-ttu-id="89873-104">오랜 시간 동안 네트워크에서 연결을 해제 하려는 경우 오프 라인 모드에서 작업 하 여 응용 프로그램 가상화 클라이언트가 서버와 통신 하려고 할 때 발생할 수 있는 지연을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89873-104">If you plan to be disconnected from the network for an extended period of time, you can work in offline mode to eliminate possible delays when the Application Virtualization client attempts to communicate with the server.</span></span> <span data-ttu-id="89873-105">오프 라인 모드에서 응용 프로그램 가상화 클라이언트는 게시 서버와 통신을 시도 하지 않으므로 오프 라인 모드를 사용 하도록 설정 하기 전에 응용 프로그램을 완전히 캐시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89873-105">In offline mode, the Application Virtualization client will not attempt to communicate with the publishing server, so applications must be fully cached before enabling offline mode.</span></span> <span data-ttu-id="89873-106">컴퓨터의 로컬 디스크에 있는 경우에도 콘텐츠 공유에서 응용 프로그램이 검색 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89873-106">Applications will not be retrieved from the content share even if they are on the local disk on the computer.</span></span> <span data-ttu-id="89873-107">다음 응용 프로그램 가상화 클라이언트 프로시저를 사용 하 여 오프 라인 작업과 온라인 작업 간을 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89873-107">You can use the following Application Virtualization Client procedure to toggle between working offline and online.</span></span>

<span data-ttu-id="89873-108">**참고**  기본적으로 원격 데스크톱 서비스에 대 한 클라이언트에서는 **오프 라인으로 작업** 을 사용할 수 없습니다 (이전의 터미널 서비스).</span><span class="sxs-lookup"><span data-stu-id="89873-108">**Note** By default, **Work Offline** is disabled for the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="89873-109">원격 데스크톱 서비스용 클라이언트에서이 설정을 사용할 수 있도록 시스템 관리자가 사용자 권한을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89873-109">Your system administrator must change your user permissions to allow you to use this setting on a Client for Remote Desktop Services.</span></span>

 

**<span data-ttu-id="89873-110">오프 라인으로 작업 하려면</span><span class="sxs-lookup"><span data-stu-id="89873-110">To work offline</span></span>**

-   <span data-ttu-id="89873-111">알림 영역에서 Application Virtualization System 아이콘을 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **오프 라인으로 작업** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="89873-111">Right-click the Application Virtualization System icon in the notification area, and select **Work Offline** from the pop-up menu.</span></span>

**<span data-ttu-id="89873-112">온라인으로 작업 하려면</span><span class="sxs-lookup"><span data-stu-id="89873-112">To work online</span></span>**

-   <span data-ttu-id="89873-113">알림 영역에서 Application Virtualization System 아이콘을 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **온라인으로 작업** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="89873-113">Right-click the Application Virtualization System icon in the notification area, and select **Work Online** from the pop-up menu.</span></span>

## <span data-ttu-id="89873-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="89873-114">Related topics</span></span>


[<span data-ttu-id="89873-115">Application Virtualization Client 관리에 대한 데스크톱 알림 영역을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="89873-115">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





