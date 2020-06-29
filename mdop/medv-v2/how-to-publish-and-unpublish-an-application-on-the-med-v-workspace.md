---
title: MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법
description: MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826923"
---
# <span data-ttu-id="548c0-103">MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="548c0-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="548c0-104">응용 프로그램이 MED-V 작업 영역에 설치 되어 있는 경우에도 최종 사용자가 응용 프로그램을 사용할 수 있게 되기 전에이를 게시 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="548c0-105">기본적으로 대부분의 응용 프로그램은 설치 하 고 바로 가기를 만들고 사용할 수 있는 시점에 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="548c0-106">일부 경우에는 바이러스 검사 소프트웨어와 같이 최종 사용자가 사용할 수 있도록 설정 하지 않고 MED-V 작업 영역에 응용 프로그램을 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="548c0-107">마찬가지로 이전에 최종 사용자가 사용할 수 없었던 MED-V 작업 영역에 설치 된 응용 프로그램을 게시 하려는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="548c0-108">예를 들어 설치 시 **시작** 메뉴에 바로 가기가 자동으로 만들어지지 않은 경우 설치 된 응용 프로그램을 게시 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="548c0-109">**중요**  UNC 경로를 지원 하지 않는 응용 프로그램을 게시 하는 경우에는 응용 프로그램을 드라이브에 매핑하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="548c0-110">다음 작업 중 하나를 수행 하 여 배포 된 MED-V 작업 영역에 대 한 응용 프로그램을 게시 또는 게시 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="548c0-111">설치 된 응용 프로그램 게시 또는 게시 취소</span><span class="sxs-lookup"><span data-stu-id="548c0-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="548c0-112">배포 된 MED-V 작업 영역에 응용 프로그램을 게시 하려면 해당 응용 프로그램의 바로 가기를 가상 컴퓨터의 다음 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="548c0-113">C:\\Documents 및 Settings\\All Users\\Start 메뉴</span><span class="sxs-lookup"><span data-stu-id="548c0-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="548c0-114">필요한 경우 그룹 정책 또는 ESD 시스템을 사용 하 여 해당 응용 프로그램의 바로 가기를 모두 Users\\Start 메뉴 폴더로 복사 하는 스크립트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="548c0-115">배포 된 MED-V 작업 영역에서 응용 프로그램의 게시를 취소 하려면 가상 컴퓨터의 다음 폴더에서 해당 응용 프로그램의 바로 가기를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="548c0-116">C:\\Documents 및 Settings\\All Users\\Start 메뉴</span><span class="sxs-lookup"><span data-stu-id="548c0-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="548c0-117">필요한 경우 그룹 정책 또는 ESD 시스템을 사용 하 여 모든 Users\\Start 메뉴 폴더에서 해당 응용 프로그램의 바로 가기를 삭제 하는 스크립트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="548c0-118">**참고**  응용 프로그램을 제거할 때 호스트 컴퓨터 **시작** 메뉴에서 바로 가기가 자동으로 삭제 되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="548c0-119">그러나 공유 컴퓨터의 모든 사용자에 대해 구성 된 MED-V 작업 영역과 같은 경우에는 응용 프로그램이 제거 된 후 **시작** 메뉴에서 바로 가기를 수동으로 삭제 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="548c0-120">최종 사용자는 바로 가기를 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="548c0-121">응용 프로그램이 게시 되거나 게시 취소 되었는지 테스트 하려면 MED-V 작업 영역에서 해당 바로 가기를 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="548c0-122">**참고**  Windows XP SP3에 포함 되 고 가상 컴퓨터 시작 메뉴 폴더에 있는 응용 프로그램은 호스트에 자동으로 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="548c0-123">자동 게시를 차단 하는 레지스트리 설정으로 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="548c0-124">자세한 내용은 [Windows 가상 PC 응용 프로그램 제외 목록을](windows-virtual-pc-application-exclude-list.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="548c0-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="548c0-125">제어판 항목을 게시 하려면</span><span class="sxs-lookup"><span data-stu-id="548c0-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="548c0-126">대상이 항목의 이름 (예: C:\\WINDOWS\\system32\\appwiz.cpl) 인 가상 컴퓨터에서 바로 가기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="548c0-127">바로 가기는 "%allpeople Profile%\\start Menu\\" 폴더 또는 하위 폴더 중 하나에 생성 또는 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="548c0-128">항목은 호스트 시작 메뉴 폴더의 해당 위치에 있는 호스트 컴퓨터에 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="548c0-129">호스트의 항목에 대 한 바로 가기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="548c0-130">**주의**  사항 바로 가기를 만들 때% SystemRoot% \\control.exe를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="548c0-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="548c0-131">이 응용 프로그램은 자동 게시를 차단 하는 레지스트리 설정에 포함 되어 있기 때문에 게시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="548c0-132">MED-V가 자동 응용 프로그램 게시를 처리 하는 방법</span><span class="sxs-lookup"><span data-stu-id="548c0-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="548c0-133">응용 프로그램이 게시 되는 동안 MED-V는 게스트에 있는 폴더 계층 구조와 일치 하도록 게스트 가상 컴퓨터의 바로 가기를 호스트 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="548c0-134">이를 통해 MED-V는 다음 단계에 따라 게스트의 바로 가기를 호스트로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="548c0-135">MED-V는 바로 가기가 있는 게스트의 폴더와 동일한 이름을 가진 호스트 컴퓨터에서 시작 하는 폴더를 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="548c0-136">일치 하는 폴더가 없는 경우 MED-V는 바로 가기가 있는 게스트의 폴더와 같은 호스트 시작 메뉴 폴더에서 폴더를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="548c0-137">일치 하는 폴더가 없는 경우 MED-V는 호스트의 기본 폴더 (시작 메뉴 \ 프로그램 폴더)에 바로 가기를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="548c0-138">응용 프로그램 게시 프로세스의 예:</span><span class="sxs-lookup"><span data-stu-id="548c0-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="548c0-139">게스트의 시작 Menu\\Programs\\AppShortcuts 폴더에 응용 프로그램 바로 가기가 게시 되는 경우 MED-V는 시작 Menu\\Programs\\ AppShortcuts 가기 폴더에 대 한 호스트 컴퓨터에서 검색 하 고 찾은 경우 바로 가기를 해당 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="548c0-140">폴더를 찾을 수 없는 경우 MED-V가 호스트 컴퓨터에서 시작 Menu\\AppShortcuts 바로 가기 폴더에 대 한 검색을 찾은 후 해당 폴더에 바로 가기를 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="548c0-141">폴더를 찾을 수 없는 경우 MED-V는 바로 가기를 시작 Menu\\Programs 폴더에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="548c0-142">**참고**  이 폴더에 대 한 바로 가기를 복사 하려면 MED-V에 대 한 호스트 컴퓨터의 시작 메뉴 폴더에 폴더가 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="548c0-143">MED-V가 아직 없는 경우 폴더를 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="548c0-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="548c0-144">관련 항목</span><span class="sxs-lookup"><span data-stu-id="548c0-144">Related topics</span></span>


[<span data-ttu-id="548c0-145">MED-V 작업 영역에 응용 프로그램 설치 및 제거</span><span class="sxs-lookup"><span data-stu-id="548c0-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="548c0-146">MED-V 작업 영역에 대한 소프트웨어 업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="548c0-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="548c0-147">Windows 가상 PC 응용 프로그램 제외 목록</span><span class="sxs-lookup"><span data-stu-id="548c0-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 





