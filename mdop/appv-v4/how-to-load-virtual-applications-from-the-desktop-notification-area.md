---
title: 데스크톱 알림 영역에서 가상 응용 프로그램을 로드하는 방법
description: 데스크톱 알림 영역에서 가상 응용 프로그램을 로드하는 방법
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817218"
---
# <span data-ttu-id="e2de6-103">데스크톱 알림 영역에서 가상 응용 프로그램을 로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="e2de6-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="e2de6-104">모바일 사용자는 연결 되지 않은 작업 또는 오프 라인 모드에서 응용 프로그램을 사용 하도록 캐시에 완전히 로드 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="e2de6-105">Application Virtualization (App-v) 서버 또는 App-v (Application Virtualization) 스트리밍 서버에서 응용 프로그램을 스트리밍하려면 응용 프로그램을 로드 하려면 서버에 연결 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="e2de6-106">응용 프로그램을 로드 하려고 할 때 서버에 연결 되어 있지 않으면 시스템에서 적절 한 오류 메시지를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="e2de6-107">파일 또는 디스크에서 응용 프로그램을 클라이언트로 스트리밍할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="e2de6-108">응용 프로그램은 한 번에 하나씩 응용 프로그램을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="e2de6-109">진행률 표시줄에는 응용 프로그램 이름, 로드 된 응용 프로그램의 백분율, 대기 중인 응용 프로그램의 총 수와 비교 하 여 이미 처리 된 응용 프로그램 수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="e2de6-110">100%가 로드 되기 전에 진행 중인 응용 프로그램을 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="e2de6-111">나머지 모든 응용 프로그램의 로드도 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="e2de6-112">**참고**  시스템에서 응용 프로그램을 로드 하는 동안 오류가 발생 하면 오류를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="e2de6-113">오류 대화 상자를 닫은 후에는 다음 응용 프로그램을 로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="e2de6-114">모든 응용 프로그램을 로드 하려면</span><span class="sxs-lookup"><span data-stu-id="e2de6-114">To load all applications</span></span>**

1.  <span data-ttu-id="e2de6-115">알림 영역에서 Application Virtualization System 아이콘을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="e2de6-116">팝업 메뉴에서 **응용 프로그램 로드** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="e2de6-117">응용 프로그램을 건너뛰려면</span><span class="sxs-lookup"><span data-stu-id="e2de6-117">To skip applications</span></span>**

1.  <span data-ttu-id="e2de6-118">진행률 표시줄을 클릭 하 여 대화 상자를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="e2de6-119">원하는 결과를 얻으려면 다음 단추 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="e2de6-120">**건너뛰기**-현재 로드 중인 응용 프로그램을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="e2de6-121">**모두 건너뛰기**-나머지 모든 응용 프로그램을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="e2de6-122">**계속**-대화 상자를 취소 하 고 응용 프로그램 로드를 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2de6-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="e2de6-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e2de6-123">Related topics</span></span>


[<span data-ttu-id="e2de6-124">Application Virtualization Client 관리에 대한 데스크톱 알림 영역을 사용하는 방법</span><span class="sxs-lookup"><span data-stu-id="e2de6-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





