---
title: 관리 콘솔에서 응용 프로그램 및 기본 가상 응용 프로그램 확장 구성
description: 관리 콘솔을 사용하여 응용 프로그램 및 기본 가상 응용 프로그램 확장을 보고 구성하는 방법
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814705"
---
#   <span data-ttu-id="01253-103">관리 콘솔에서 응용 프로그램 및 기본 가상 응용 프로그램 확장 구성</span><span class="sxs-lookup"><span data-stu-id="01253-103">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>

<span data-ttu-id="01253-104">다음 절차를 사용 하 여 기본 패키지 확장을 *보고* *구성* 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-104">Use the following procedure to *view* and *configure* default package extensions.</span></span>

**<span data-ttu-id="01253-105">기본 가상 응용 프로그램 확장을 보고 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="01253-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="01253-106">구성 하고자 하는 패키지를 보려면 App-v 5.1 관리 콘솔을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="01253-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="01253-107">구성 하려는 패키지를 선택 하 고 패키지 이름을 마우스 오른쪽 단추로 클릭 한 다음 **기본 구성 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="01253-108">지정 된 패키지에 포함 된 응용 프로그램을 보려면 **기본 구성** 창에서 **응용 프로그램**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="01253-109">해당 패키지의 바로 가기를 보려면 **바로 가기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="01253-110">해당 패키지의 파일 형식 연결을 보려면 **파일 형식을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="01253-111">응용 프로그램 확장을 사용 하도록 설정 하려면 **사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="01253-112">바로 가기를 사용 하려면 **바로 가기 사용**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="01253-113">선택한 응용 프로그램에 대 한 새 바로 가기를 추가 하려면 **바로 가기** 창에서 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **새 바로 가기 추가**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="01253-114">바로 가기를 제거 하려면 바로 **가기** 창에서 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **바로 가기 제거**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="01253-115">기존 바로 가기를 편집 하려면 응용 프로그램을 마우스 오른쪽 단추로 클릭 하 고 **바로 가기 편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="01253-116">다른 응용 프로그램 확장을 보려면 **고급** 을 클릭 하 고 **구성 내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="01253-117">파일 이름을 입력 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="01253-118">구성 파일을 사용 하 여 패키지와 연결 된 모든 응용 프로그램 확장명을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01253-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="01253-119">다른 응용 프로그램 확장을 편집 하려면 구성 파일을 수정 하 고 **가져오기 및이 구성을 덮어쓰도록**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="01253-120">수정 된 파일을 선택 하 고 **열기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="01253-121">대화 상자에서 **덮어쓰기를** 클릭 하 여 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

><span data-ttu-id="01253-122">**참고** 업로드가 실패 하 고 구성 파일 크기가 4MB를 넘으면 서버에서 허용 하는 최대 파일 크기를 늘려야 할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="01253-122">**Note** If the upload fails and the size of your configuration file is above 4MB, you will need to increase the maximum file size allowed by the server.</span></span> <span data-ttu-id="01253-123">이 작업은 구성 파일의 크기 (KB) 보다 큰 값을 포함 하는 maxRequestLength 특성을 26 번째 줄의 httpRuntime 요소에 추가 하 여 수행할 수 있습니다 `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .</span><span class="sxs-lookup"><span data-stu-id="01253-123">This can be done by adding the maxRequestLength attribute with a value greater than the size of your configuration file (in KB) to the httpRuntime element on line 26 of `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config`.</span></span>  
<span data-ttu-id="01253-124">예를 들어, `<httpRuntime targetFramework="4.5"/>` 로 변경 하면 `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` 최대 크기가 8mb로 증가 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-124">For example, changing `<httpRuntime targetFramework="4.5"/>` to `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` will increase the maximum size to 8MB</span></span>


<span data-ttu-id="01253-125">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="01253-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="01253-126">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="01253-127">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="01253-127">Got an App-V issue?</span></span>** <span data-ttu-id="01253-128">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01253-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="01253-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="01253-129">Related topics</span></span>


[<span data-ttu-id="01253-130">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="01253-130">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 




