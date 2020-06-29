---
title: 수동으로 가상 응용 프로그램을 관리하는 방법
description: 수동으로 가상 응용 프로그램을 관리하는 방법
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817113"
---
# <span data-ttu-id="1e70f-103">수동으로 가상 응용 프로그램을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="1e70f-104">Application Virtualization (App-v) 클라이언트 관리 콘솔을 사용 하 여 App-v 데스크톱 클라이언트의 가상 응용 프로그램을 관리 하거나 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="1e70f-105">앱-V 관리자는 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="1e70f-106">App-v 응용 프로그램을 로드 하거나 언로드하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="1e70f-107">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용** 프로그램 노드의 **결과** 창에 있는 응용 프로그램을 캐시에서 직접 로드 하거나 언로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="1e70f-108">이 노드를 선택 하면 **결과** 창에 응용 프로그램 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="1e70f-109">**참고**  패키지를 로드 하거나 언로드하면 패키지의 모든 응용 프로그램이 캐시에서 로드 되거나 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="1e70f-110">패키지를 로드할 때 캐시에 응용 프로그램을 로드 하는 데 적절 한 공간이 없는 경우 캐시 크기를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="1e70f-111">캐시 크기에 대 한 자세한 내용은 [캐시 크기 및 드라이브 문자 지정을 변경 하는 방법을](how-to-change-the-cache-size-and-the-drive-letter-designation.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e70f-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="1e70f-112">App-v 응용 프로그램을 로드 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="1e70f-113">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **로드** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-114">응용 프로그램이 자동으로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-114">The application is automatically loaded.</span></span> <span data-ttu-id="1e70f-115">진행률은 **패키지 상태**레이블이 붙은 열에서 추적 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="1e70f-116">로드가 완료 되었는지 확인 하거나 진행률을 확인 하려면 보기를 새로 고쳐야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="1e70f-117">App-v 응용 프로그램을 언로드하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="1e70f-118">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **언로드** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-119">응용 프로그램이 자동으로 언로드되고, **패키지 상태** 열이 업데이트 되어 변경 내용이 반영 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="1e70f-120">App-v 응용 프로그램을 지우는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-120">How to clear an App-V application</span></span>


<span data-ttu-id="1e70f-121">응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용 프로그램** 노드의 **결과** 창에서 직접 콘솔의 응용 프로그램을 지울 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="1e70f-122">응용 프로그램을 지우면 시스템에서 응용 프로그램에 해당 하는 설정, 바로 가기 및 파일 형식 연결을 제거 하 고 사용자의 응용 프로그램 목록에서 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="1e70f-123">**참고**  콘솔에서 응용 프로그램을 지우면 해당 응용 프로그램을 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="1e70f-124">그러나 응용 프로그램은 캐시에 유지 되며 동일한 시스템의 다른 사용자가 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="1e70f-125">게시 새로 고침 후에는 지워진 응용 프로그램을 다시 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="1e70f-126">패키지에 여러 응용 프로그램이 있는 경우 모든 응용 프로그램이 지워질 때까지 사용자의 설정이 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="1e70f-127">콘솔에서 응용 프로그램을 지우려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="1e70f-128">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **지우기를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-129">확인 메시지에서 **예** 를 클릭 하 여 응용 프로그램을 제거 하거나 **아니요** 를 클릭 하 여 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="1e70f-130">App-v 응용 프로그램을 복구 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-130">How to Repair an App-V application</span></span>


<span data-ttu-id="1e70f-131">선택한 응용 프로그램을 복구 하려면 응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용 프로그램** 노드의 **결과** 창에서 직접 다음 절차를 수행 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="1e70f-132">응용 프로그램을 복구 하는 경우 사용자 지정 사용자 설정을 제거 하 고 기본 설정을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="1e70f-133">이 작업은 바로 가기 또는 파일 형식 연결을 변경 하거나 삭제 하지 않으며 캐시에서 응용 프로그램을 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="1e70f-134">App-v 응용 프로그램을 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="1e70f-135">커서를 **결과** 창으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="1e70f-136">원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **복구** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="1e70f-137">확인 메시지에서 **예** 를 클릭 하 여 응용 프로그램을 복구 **하거나 취소** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="1e70f-138">App-v 응용 프로그램을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-138">How to import an App-V application</span></span>


<span data-ttu-id="1e70f-139">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔의 **응용 프로그램** 노드의 **결과** 창에서 직접 캐시로 응용 프로그램을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="1e70f-140">App-v 응용 프로그램을 가져오려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="1e70f-141">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **가져오기를** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-142">**찾아보기** 창에서 원하는 응용 프로그램에 대 한 패키지 파일의 위치로 이동한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="1e70f-143">**참고**  가져오기 검색 경로를 이미 구성 했거나 SFT 파일이 마지막으로 성공한 가져오기와 같은 경로에 있으면 2 단계가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="1e70f-144">App-v 응용 프로그램을 잠그거나 잠금 해제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="1e70f-145">다음 절차를 사용 하 여 Application Virtualization 데스크톱 클라이언트 캐시 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 캐시의 클라이언트에서 응용 프로그램을 잠그거나 잠금을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="1e70f-146">잠긴 응용 프로그램을 캐시에서 제거 하 여 새 응용 프로그램을 위한 공간을 확보할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="1e70f-147">응용 프로그램 가상화 데스크톱 클라이언트 캐시 또는 원격 데스크톱 서비스 캐시의 클라이언트에서 잠긴 응용 프로그램을 제거 하려면 먼저 잠금을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="1e70f-148">응용 프로그램을 잠그려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-148">To lock an application</span></span>**

1.  <span data-ttu-id="1e70f-149">커서를 **결과** 창으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="1e70f-150">원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **잠금을** 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="1e70f-151">선택한 응용 프로그램이 캐시에서 잠겼습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="1e70f-152">응용 프로그램의 잠금을 해제 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-152">To unlock an application</span></span>**

1.  <span data-ttu-id="1e70f-153">커서를 **결과** 창으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="1e70f-154">원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **잠금 해제** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="1e70f-155">선택한 응용 프로그램이 캐시에서 잠금 해제 되어 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="1e70f-156">App-v 응용 프로그램을 삭제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-156">How to delete an App-V application</span></span>


<span data-ttu-id="1e70f-157">응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용 프로그램** 노드를 선택 하면 **결과** 창에 응용 프로그램 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="1e70f-158">다음 절차를 사용 하 여 **결과** 창에서 응용 프로그램을 삭제 하 고 캐시에서 응용 프로그램을 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="1e70f-159">**참고**  응용 프로그램을 삭제 하면 해당 클라이언트의 모든 사용자가 선택한 응용 프로그램을 더 이상 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="1e70f-160">바로 가기 및 파일 형식 연결이 숨겨지고 응용 프로그램이 캐시에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="1e70f-161">그러나 다른 응용 프로그램에서 선택한 응용 프로그램의 파일 시스템 캐시 데이터에 있는 데이터를 참조 하는 경우 이러한 항목은 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="1e70f-162">게시 새로 고침을 수행한 후에는 삭제 된 응용 프로그램을 다시 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="1e70f-163">응용 프로그램을 삭제 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-163">To delete an application</span></span>**

1.  <span data-ttu-id="1e70f-164">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **삭제** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-165">확인 메시지에서 **예** 를 클릭 하 여 응용 프로그램을 제거 하거나 **아니요** 를 클릭 하 여 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="1e70f-166">앱-V 응용 프로그램 아이콘을 변경 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-166">How to change an App-V application icon</span></span>


<span data-ttu-id="1e70f-167">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔의 **응용 프로그램** 노드의 **결과** 창에서 직접 선택한 응용 프로그램과 연결 된 아이콘을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="1e70f-168">응용 프로그램 아이콘을 변경 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-168">To change an application icon</span></span>**

1.  <span data-ttu-id="1e70f-169">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="1e70f-170">**속성**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="1e70f-171">**일반** 탭에서 **아이콘 변경을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="1e70f-172">원하는 아이콘을 선택 하거나 다른 위치를 찾아 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="1e70f-173">아이콘을 선택한 후 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="1e70f-174">**결과** 창에 새로 만들기 아이콘이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="1e70f-175">App-v 응용 프로그램을 추가 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-175">How to add an App-V application</span></span>


<span data-ttu-id="1e70f-176">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔의 **응용 프로그램** 노드에 대 한 **결과** 창에서 직접 응용 프로그램을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="1e70f-177">응용 프로그램을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-177">To add an application</span></span>**

1.  <span data-ttu-id="1e70f-178">**결과** 창에서 팝업 메뉴에서 **새 응용 프로그램** 을 마우스 오른쪽 단추로 클릭 하 고 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-179">마법사 페이지에서 다음 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="1e70f-180">**아이콘 변경**— 표준 Windows 아이콘 브라우저를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="1e70f-181">원하는 아이콘을 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="1e70f-182">**OSD 파일 경로 또는 URL**-로컬 절대 경로, 전체 UNC 경로 (네트워크의 공유 파일 또는 디렉터리) 또는 HTTP URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="1e70f-183">**(OSD browse button)**-표준 Windows **파일 열기** 대화 상자를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="1e70f-184">원하는 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="1e70f-185">**마침을** 클릭 하 여 **결과** 창에 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="1e70f-186">앱을 게시 하는 방법-V 응용 프로그램 바로 가기</span><span class="sxs-lookup"><span data-stu-id="1e70f-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="1e70f-187">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔의 **응용 프로그램** 노드의 **결과** 창에서 직접 응용 프로그램에 대 한 바로 가기를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="1e70f-188">응용 프로그램 바로 가기를 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="1e70f-189">커서를 **결과** 창으로 이동 하 고 원하는 응용 프로그램을 마우스 오른쪽 단추로 클릭 한 다음 팝업 메뉴에서 **새 바로 가기를** 선택 하 여 새 바로 가기 마법사를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="1e70f-190">새 바로 가기 마법사의 첫 번째 페이지에서 아이콘을 선택 하 고 바로 가기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="1e70f-191">**아이콘 변경**— 표준 Windows 아이콘 브라우저를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="1e70f-192">원하는 아이콘을 찾아 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="1e70f-193">**바로 가기 제목**-바로 가기에 지정할 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="1e70f-194">이 필드는 응용 프로그램의 기존 이름 및 버전으로 기본 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="1e70f-195">마법사의 두 번째 페이지에서 게시 된 바로 가기의 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="1e70f-196">**바탕 화면**-바로 가기를 바탕 화면에 게시 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="1e70f-197">**빠른**실행 도구 모음-빠른 실행 도구 모음에 바로 가기를 게시 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="1e70f-198">**보내기 메뉴**- **보내기** 메뉴에 바로 가기를 게시 하려면이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="1e70f-199">**시작 메뉴의 프로그램**- **시작 메뉴** 의 확인란을 선택 하면이 필드가 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="1e70f-200">바로 가기를 프로그램 폴더의 루트에 직접 게시 하려면이 필드를 비워 두거나, 폴더 이름 또는 계층 구조를 입력 합니다 (예: "My \ _Computer \\Office 응용 프로그램").</span><span class="sxs-lookup"><span data-stu-id="1e70f-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="1e70f-201">이 방법으로 만든 바로 가기는 현재 사용자만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="1e70f-202">**다른 위치** 및 **찾아보기** 단추- **다른 위치** 확인란을 선택 하면이 필드가 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="1e70f-203">컴퓨터의 유효한 위치 또는 사용 가능한 UNC 경로 (네트워크의 공유 파일 또는 디렉터리)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="1e70f-204">**찾아보기** 단추를 클릭 하면 표준 Windows **파일 열기** 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="1e70f-205">마법사의 세 번째 페이지에 원하는 명령줄 매개 변수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="1e70f-206">**마침을** 클릭 하 여 바로 가기를 게시 하 고 **결과** 창으로 나갑니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="1e70f-207">앱에 대 한 파일 형식 연결을 추가 하는 방법-V 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="1e70f-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="1e70f-208">다음 절차를 사용 하 여 응용 프로그램 가상화 클라이언트 관리 콘솔의 **파일 형식 연결** 노드를 사용 하 여 파일 형식 연결을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="1e70f-209">파일 형식 연결을 추가 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-209">To add a file type association</span></span>**

1.  <span data-ttu-id="1e70f-210">**파일 형식 연결** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **새 연결** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="1e70f-211">다음 정보를 완료 하 여 대화 상자의 첫 번째 단계를 완료 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="1e70f-212">**확장명**-새 파일 이름 확장명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="1e70f-213">이 필드는 기본적으로 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="1e70f-214">**이 설명으로 새 파일 형식 만들기**-활성 필드에 새 파일 형식 설명을 입력 하려면이 라디오 단추를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="1e70f-215">이 단추는 기본적으로 선택 되어 있으며 활성 필드는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="1e70f-216">**이 파일 형식을 모든 사용자에 게 적용**—이 연관을 모든 사용자에 대해 전역으로 설정할 때이 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="1e70f-217">기본적으로이 상자는 선택 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="1e70f-218">기존 파일 형식으로 **이 확장명 연결**-이 라디오 단추를 선택 하 여 확장명을 기존 파일 형식과 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="1e70f-219">드롭다운 목록에서 파일 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="1e70f-220">이 옵션을 선택 하면 **다음** 이 **완료**로 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="1e70f-221">다음 정보를 완료 하 여 대화 상자의 두 번째 단계를 완료 하 고 **마침을** 클릭 하 여 클라이언트 관리 콘솔로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="1e70f-222">**아이콘 변경**—이 단추를 클릭 하 여 응용 프로그램 아이콘을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="1e70f-223">사용 가능한 아이콘 중 하나를 선택 하거나 새 위치를 찾아 아이콘을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="1e70f-224">**선택한 응용 프로그램을 사용 하 여 파일 열기**—이 라디오 단추를 선택 하 여 기존 응용 프로그램에서 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="1e70f-225">사용 가능한 응용 프로그램의 드롭다운 목록에서 응용 프로그램을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="1e70f-226">**이 osd 파일에 설명 된 연결을 사용 하 여 파일 열기**—이 라디오 단추를 선택 하 여 파일을 열 때 사용 되는 응용 프로그램을 결정 하는 OSD (Open Software Descriptor) 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="1e70f-227">찾아보기 단추를 사용 하 여 기존 위치를 선택 하거나이 필드에 경로 또는 HTTP 형식의 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="1e70f-228">앱-V 응용 프로그램의 파일 형식 연결을 삭제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1e70f-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="1e70f-229">다음 절차를 사용 하 여 파일 형식 연결을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="1e70f-230">**파일 형식 연결** 노드는 **범위** 창의 **Application Virtualization** 노드 보다 한 수준 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="1e70f-231">이 노드를 선택 하면 **결과** 창에 파일 형식 연결 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="1e70f-232">파일 형식 연결을 제거 하려면</span><span class="sxs-lookup"><span data-stu-id="1e70f-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="1e70f-233">**결과** 창에서 삭제 하려는 파일 형식 연결의 확장명을 마우스 오른쪽 단추로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="1e70f-234">팝업 메뉴에서 **삭제** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="1e70f-235">**예** 를 클릭 하 여 연결을 삭제 하거나 **아니요** 를 클릭 하 여 **결과** 창으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="1e70f-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="1e70f-236">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1e70f-236">Related topics</span></span>


[<span data-ttu-id="1e70f-237">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="1e70f-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





