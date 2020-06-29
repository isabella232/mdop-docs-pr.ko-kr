---
title: 관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법
description: 관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법
author: dansimp
ms.assetid: 4f249ee3-cc2d-4b1e-afe5-d1cbf9cabd88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57ce4b82cc552e0a4adc2272f849111d8da0be71
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814252"
---
# <span data-ttu-id="f8c91-103">관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="f8c91-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="f8c91-104">AD (Active Directory) 그룹에 대 한 가상 응용 프로그램 확장을 사용자 지정 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="f8c91-105">광고 그룹에 대 한 가상 응용 프로그램 확장을 사용자 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="f8c91-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="f8c91-106">구성 하고자 하는 패키지를 보려면 App-v 5.0 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="f8c91-107">지정 된 사용자 그룹에 할당 되는 구성을 보려면 패키지를 선택 하 고 패키지 이름을 마우스 오른쪽 단추로 클릭 하 고 **active directory Access 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="f8c91-108">또는 패키지를 선택 하 고 **광고 액세스** 창에서 **편집** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="f8c91-109">광고 그룹을 사용자 지정 하려면 **Access를 사용 하 여 광고 엔터티**목록에서 그룹을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="f8c91-110">그런 다음 **할당 된 구성** 창의 드롭다운 상자를 사용 하 여 **사용자 지정**을 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="f8c91-111">지정 된 응용 프로그램의 모든 확장을 사용 하지 않도록 설정 하려면 **사용**을 선택 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="f8c91-112">선택한 응용 프로그램에 대 한 새 바로 가기를 추가 하려면 **바로 가기** 창에서 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **새 바로 가기 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="f8c91-113">바로 가기를 제거 하려면 바로 **가기** 창에서 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **바로 가기 제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="f8c91-114">기존 바로 가기를 편집 하려면 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **바로 가기 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="f8c91-115">다른 응용 프로그램 확장을 보려면 Advanced ( **고급**)를 클릭 하 고 **구성 내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="f8c91-116">파일 이름을 입력 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="f8c91-117">구성 파일을 사용 하 여 패키지와 연결 된 모든 응용 프로그램 확장을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="f8c91-118">추가 응용 프로그램 확장을 편집 하려면 구성 파일을 수정 하 고 가져오기를 클릭 하 여 **이 구성을 덮어씁니다**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="f8c91-119">수정 된 파일을 선택 하 고 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="f8c91-120">대화 상자에서 **덮어쓰기를** 클릭 하 여 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="f8c91-121">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="f8c91-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f8c91-122">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f8c91-123">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="f8c91-123">Got an App-V issue?</span></span>** <span data-ttu-id="f8c91-124">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c91-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f8c91-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f8c91-125">Related topics</span></span>


[<span data-ttu-id="f8c91-126">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="f8c91-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





