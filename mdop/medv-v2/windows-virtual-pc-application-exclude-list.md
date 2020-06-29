---
title: Windows 가상 PC 응용 프로그램 제외 목록
description: Windows 가상 PC 응용 프로그램 제외 목록
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823693"
---
# <span data-ttu-id="17ce9-103">Windows 가상 PC 응용 프로그램 제외 목록</span><span class="sxs-lookup"><span data-stu-id="17ce9-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="17ce9-104">경우에 따라 MED-V 작업 영역에 설치 된 응용 프로그램을 호스트 컴퓨터의 **시작** 메뉴에 게시 하지 않는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="17ce9-105">[Med-v 작업 영역에서 응용 프로그램을 게시](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)하는 방법에 대 한 지침에 따라 이러한 응용 프로그램의 게시를 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="17ce9-106">그러나 프로그램이 자동으로 업데이트 되는 경우에도 자동으로 다시 게시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="17ce9-107">이렇게 하면 응용 프로그램을 다시 게시 취소 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="17ce9-108">Windows 가상 PC에는 호스트 **시작** 메뉴에 게시 하지 않으려는 특정 설치 된 응용 프로그램을 지정할 수 있는 "제외 목록" 이라는 기능이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="17ce9-109">"Exclude List"는 HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList 키의 게스트 레지스트리에 있으며 호스트 **시작** 메뉴에 게시 되지 않은 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="17ce9-110">"제외 목록"이 표시 되는 응용 프로그램에 대 한 자동 업데이트 때문에 자동으로 다시 게시 되지 않으므로 지정 된 응용 프로그램을 영구적으로 게시 취소 하는 것으로 생각할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="17ce9-111">Windows 가상 PC에서 제외 목록을 사용 하 여 응용 프로그램 관리</span><span class="sxs-lookup"><span data-stu-id="17ce9-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="17ce9-112">전체 화면에서 MED-V 작업 영역을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="17ce9-113">MED-V 관리 도구 키트를 사용 하 여 전체 화면 모드로 MED-V 작업 영역을 여는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 구성 보기](viewing-med-v-workspace-configurations.md#bkmk-fullscreen)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17ce9-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="17ce9-114">또는 **시작**을 클릭 하 고 **모든 프로그램**, **Windows 가상 pc**, **windows 가상 pc**를 차례로 클릭 한 다음 med-v 작업 영역을 두 번 클릭 하 여 전체 화면으로 수동으로 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="17ce9-115">MED-V 작업 영역 Windows 가상 PC 창에서 레지스트리 편집기를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="17ce9-116">**시작**을 클릭 하 고 **실행**을 클릭 한 다음 regedit를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="17ce9-117">그런 다음 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="17ce9-118">레지스트리 편집기에서 HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList 레지스트리 키를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="17ce9-119">호스트 컴퓨터 **시작** 메뉴에 게시 하지 않으려는 설치 된 응용 프로그램에 대 한 새 레지스트리 값을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="17ce9-120">예를 들어 Microsoft Silverlight 자동으로 게시 된 프로그램의 게시를 취소 하려면 다음 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="17ce9-121">VPCVAppExcludeList 레지스트리 키가 강조 표시 된 상태에서 **편집**을 클릭 하 고 **새로 만들기**를 클릭 한 다음 **문자열 값**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="17ce9-122">새 레지스트리 값의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="17ce9-123">예를 들어 Microsoft Silverlight의 경우 sllauncher.exe를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="17ce9-124">새 레지스트리 값을 두 번 클릭 하 고 값 데이터를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="17ce9-125">값 데이터는 게시 취소 하려는 명령의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="17ce9-126">게시 하지 않으려는 응용 프로그램의 **시작** 메뉴에서 바로 가기를 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 클릭 하 여 전체 경로를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="17ce9-127">전체 경로는 **바로 가기** 탭의 **대상**아래에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="17ce9-128">예를 들어 Microsoft Silverlight 프로그램의 전체 경로는 "C:\\program files Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="17ce9-129">**중요**  해당 하는 경우 값 데이터 필드에 입력할 때 전체 경로에서 따옴표를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="17ce9-130">레지스트리 편집기를 닫고 MED-V 작업 영역 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="17ce9-131">응용 프로그램이 MED-V 작업 영역에 여전히 설치 되어 있지만 이제 호스트 컴퓨터 **시작** 메뉴에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="17ce9-132">VPCVAppExcludeList 키에서 해당 값을 삭제 하 여 제외 된 응용 프로그램을 호스트 **시작** 메뉴에 다시 게시할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="17ce9-133">예를 들어 Microsoft Silverlight를 다시 게시 하려면 sllauncher.exe 레지스트리 값을 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ce9-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="17ce9-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="17ce9-134">Related topics</span></span>


[<span data-ttu-id="17ce9-135">MED-V에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="17ce9-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="17ce9-136">MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="17ce9-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





