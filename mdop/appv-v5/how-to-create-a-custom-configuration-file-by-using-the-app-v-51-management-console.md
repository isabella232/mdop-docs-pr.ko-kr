---
title: App-V 5.1 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법
description: App-V 5.1 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814324"
---
# <span data-ttu-id="8606b-103">App-V 5.1 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="8606b-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="8606b-104">동적 구성을 사용 하 여 특정 사용자에 대 한 App-v 5.1 패키지를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="8606b-105">그러나 파일을 사용 하려면 먼저 동적 사용자 구성 (.xml) 파일 또는 동적 배포 구성 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="8606b-106">파일 생성은 고급 수동 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="8606b-107">동적 사용자 구성 파일에 대 한 일반적인 내용은 [앱-V 5.1 동적 구성을](about-app-v-51-dynamic-configuration.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8606b-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="8606b-108">App-v 5.1 관리 콘솔을 사용 하 여 동적 사용자 구성 파일을 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="8606b-109">동적 사용자 구성 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="8606b-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="8606b-110">보려는 패키지의 이름을 마우스 오른쪽 단추로 클릭 하 고 **active directory Access 편집** 을 선택 하 여 해당 사용자 그룹에 할당 된 구성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="8606b-111">또는 패키지를 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="8606b-112">**액세스 권한이 있는 광고 엔터티**목록을 사용 하 여 사용자 지정 하려는 광고 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="8606b-113">아직 선택 하지 않은 경우 드롭다운 목록에서 **사용자 지정** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="8606b-114">**편집** 이라는 링크가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="8606b-115">**편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-115">Click **Edit**.</span></span> <span data-ttu-id="8606b-116">광고 그룹에 할당 된 동적 사용자 구성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="8606b-117">**고급**을 클릭 한 다음 **구성 내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="8606b-118">파일 이름을 입력 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="8606b-119">이제 파일을 편집 하 여 사용자에 대 한 패키지를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="8606b-120">참고</span><span class="sxs-lookup"><span data-stu-id="8606b-120">Note</span></span>**  
    <span data-ttu-id="8606b-121">Windows Server에서 실행 되는 동안 구성을 내보내려면 "IE 보안 강화 구성"을 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="8606b-122">이 기능을 사용 하 여 다운로드를 차단 하도록 설정 하면 App-v 서버에서 아무것도 다운로드할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8606b-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="8606b-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8606b-123">Related topics</span></span>


[<span data-ttu-id="8606b-124">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="8606b-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









