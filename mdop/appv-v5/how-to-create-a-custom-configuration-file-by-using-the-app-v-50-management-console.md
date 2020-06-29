---
title: App-V 5.0 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법
description: App-V 5.0 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814329"
---
# <span data-ttu-id="95636-103">App-V 5.0 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="95636-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="95636-104">동적 구성을 사용 하 여 특정 사용자에 대 한 App-v 5.0 패키지를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95636-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="95636-105">그러나 파일을 사용 하려면 먼저 동적 사용자 구성 (.xml) 파일 또는 동적 배포 구성 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="95636-106">파일 생성은 고급 수동 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="95636-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="95636-107">동적 사용자 구성 파일에 대 한 일반적인 내용은 [앱-V 5.0 동적 구성을](about-app-v-50-dynamic-configuration.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95636-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="95636-108">App-v 5.0 관리 콘솔을 사용 하 여 동적 사용자 구성 파일을 만들려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="95636-109">동적 사용자 구성 파일을 만들려면</span><span class="sxs-lookup"><span data-stu-id="95636-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="95636-110">보려는 패키지의 이름을 마우스 오른쪽 단추로 클릭 하 고 **active directory Access 편집** 을 선택 하 여 해당 사용자 그룹에 할당 된 구성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="95636-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="95636-111">또는 패키지를 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="95636-112">**액세스 권한이 있는 광고 엔터티**목록을 사용 하 여 사용자 지정 하려는 광고 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="95636-113">아직 선택 하지 않은 경우 드롭다운 목록에서 **사용자 지정** 을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="95636-114">**편집** 이라는 링크가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95636-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="95636-115">**편집**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-115">Click **Edit**.</span></span> <span data-ttu-id="95636-116">광고 그룹에 할당 된 동적 사용자 구성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="95636-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="95636-117">**고급**을 클릭 한 다음 **구성 내보내기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="95636-118">파일 이름을 입력 하 고 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="95636-119">이제 파일을 편집 하 여 사용자에 대 한 패키지를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95636-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="95636-120">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="95636-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="95636-121">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="95636-122">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="95636-122">Got an App-V issue?</span></span>** <span data-ttu-id="95636-123">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95636-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="95636-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="95636-124">Related topics</span></span>


[<span data-ttu-id="95636-125">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="95636-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





