---
title: Client Management Console에서 응용 프로그램을 관리하는 방법
description: Client Management Console에서 응용 프로그램을 관리하는 방법
author: dansimp
ms.assetid: 15cb5133-539b-499d-adca-ed02da20194a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f29c26c972017eb9ba0dfd2d934c4fd07f2fae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817183"
---
# <span data-ttu-id="d3785-103">Client Management Console에서 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-103">How to Manage Applications in the Client Management Console</span></span>


<span data-ttu-id="d3785-104">Application virtualization 클라이언트 관리 콘솔을 사용 하 여 응용 프로그램 가상화 데스크톱 클라이언트 또는 이전의 터미널 서비스 (원격 데스크톱 서비스) 캐시 클라이언트에서 가상 응용 프로그램을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-104">You can use the Application Virtualization Client Management Console to manage virtual applications in the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="d3785-105">응용 프로그램 가상화의 컨텍스트에서, 캐시는 가상 응용 프로그램을 저장 하기 위해 예약 된 클라이언트 컴퓨터의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-105">In the context of application virtualization, the cache is the area on the client computer reserved to store virtual applications.</span></span>

## <span data-ttu-id="d3785-106">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="d3785-106">In This Section</span></span>


<a href="" id="how-to-load-or-unload-an-application"></a>[<span data-ttu-id="d3785-107">응용 프로그램을 로드 또는 언로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-107">How to Load or Unload an Application</span></span>](how-to-load-or-unload-an-application.md)  
<span data-ttu-id="d3785-108">클라이언트 캐시에서 응용 프로그램을 로드 하거나 언로드하는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-108">Provides procedures for loading or unloading an application into or from the client cache.</span></span>

<a href="" id="how-to-clear-an-application"></a>[<span data-ttu-id="d3785-109">응용 프로그램을 지우는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-109">How to Clear an Application</span></span>](how-to-clear-an-application.md)  
<span data-ttu-id="d3785-110">응용 프로그램 가상화 데스크톱 클라이언트 또는 원격 데스크톱 서비스용 클라이언트에서 설정, 파일 형식 연결, 바로 가기를 지우는 데 사용할 수 있는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-110">Provides a procedure you can use to clear the settings, file type associations, and shortcuts from the Application Virtualization Desktop Client or Client for Remote Desktop Services.</span></span>

<a href="" id="how-to-repair-an-application"></a>[<span data-ttu-id="d3785-111">응용 프로그램을 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-111">How to Repair an Application</span></span>](how-to-repair-an-application.md)  
<span data-ttu-id="d3785-112">응용 프로그램 가상화 데스크톱 클라이언트 또는 원격 데스크톱 서비스용 클라이언트에서 응용 프로그램을 복구 하는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-112">Provides a procedure for repairing an application from the Application Virtualization Desktop Client or Client for Remote Desktop Services.</span></span>

<a href="" id="how-to-import-an-application"></a>[<span data-ttu-id="d3785-113">응용 프로그램을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-113">How to Import an Application</span></span>](how-to-import-an-application.md)  
<span data-ttu-id="d3785-114">원격 데스크톱 서비스에 대 한 응용 프로그램 가상화 데스크톱 클라이언트 또는 클라이언트에 새 응용 프로그램을 추가 하는 데 사용할 수 있는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-114">Provides a procedure you can use to add a new application to the Application Virtualization Desktop Client or Client for Remote Desktop Services.</span></span>

<a href="" id="how-to-lock-or-unlock-an-application"></a>[<span data-ttu-id="d3785-115">응용 프로그램을 잠금 또는 잠금 해제하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-115">How to Lock or Unlock an Application</span></span>](how-to-lock-or-unlock-an-application.md)  
<span data-ttu-id="d3785-116">캐시에서 응용 프로그램을 잠그거나 잠금 해제 하는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-116">Provides procedures for locking or unlocking an application in the cache.</span></span>

<a href="" id="how-to-delete-an-application"></a>[<span data-ttu-id="d3785-117">응용 프로그램을 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-117">How to Delete an Application</span></span>](how-to-delete-an-application.md)  
<span data-ttu-id="d3785-118">파일 시스템 캐시에서 응용 프로그램을 제거 하는 데 사용할 수 있는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-118">Provides a procedure you can use to remove an application from the file system cache.</span></span>

<a href="" id="how-to-change-an-application-icon"></a>[<span data-ttu-id="d3785-119">응용 프로그램 아이콘을 변경하는 방법</span><span class="sxs-lookup"><span data-stu-id="d3785-119">How to Change an Application Icon</span></span>](how-to-change-an-application-icon.md)  
<span data-ttu-id="d3785-120">선택한 응용 프로그램과 연결 된 아이콘을 변경 하는 데 사용할 수 있는 절차를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3785-120">Provides a procedure you can use to change the icon associated with the selected application.</span></span>

## <span data-ttu-id="d3785-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d3785-121">Related topics</span></span>


[<span data-ttu-id="d3785-122">Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="d3785-122">Application Virtualization Client Management Console</span></span>](application-virtualization-client-management-console.md)

 

 





