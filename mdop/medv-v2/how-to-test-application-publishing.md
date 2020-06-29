---
title: 응용 프로그램 게시를 테스트하는 방법
description: 응용 프로그램 게시를 테스트하는 방법
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826913"
---
# <span data-ttu-id="055d5-103">응용 프로그램 게시를 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="055d5-103">How to Test Application Publishing</span></span>


<span data-ttu-id="055d5-104">처음으로 설치를 완료 한 후에 다음 작업을 수행 하 여 응용 프로그램 게시 기능이 예상 대로 작동 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="055d5-105">응용 프로그램 게시를 테스트 하려면</span><span class="sxs-lookup"><span data-stu-id="055d5-105">To test application publishing</span></span>**

1.  <span data-ttu-id="055d5-106">게시에 대해 지정한 응용 프로그램이 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="055d5-107">**시작** 을 클릭 한 다음 **모든 프로그램** 을 클릭 하 고 지정 된 응용 프로그램을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="055d5-108">경우에 따라 호스트 컴퓨터에 같은 응용 프로그램을 두 번 설치 했을 때와 게스트에 한 번 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="055d5-109">동일한 이름을 가진 게시 된 응용 프로그램이 호스트 **시작** 메뉴의 동일한 위치에 게시 되는 경우 가상 컴퓨터 이름을 바로 가기 이름에 추가 하 여 호스트 응용 프로그램 바로 가기에서 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="055d5-110">예를 들어 "MEDVHost1" 이라는 가상 컴퓨터의 경우 호스트 응용 프로그램이 "Notepad"이 고 게시 된 응용 프로그램이 "Notepad (MEDVHost1)" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="055d5-111">응용 프로그램이 의도 한 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="055d5-112">호스트 컴퓨터에서 게시 한 응용 프로그램을 시작 하 고 게스트의 Windows XP SP3에서 열려 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="055d5-113">응용 프로그램이 호스트 컴퓨터 데스크톱의 Windows XP 스타일 창에 표시 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="055d5-114">해당 하는 경우 문서 리디렉션이 의도 한 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="055d5-115">게스트의 게시 된 응용 프로그램이 호스트 시스템 드라이브의 폴더를 열어야 하는 경우 지정 된 폴더를 열 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="055d5-116">**중요**  Windows 가상 PC는 이미 공유 된 폴더에서 공유 만들기를 지원 하지 않으므로 네트워크에 있는 내 문서 폴더 등 공유 폴더에서 여는 문서에 대해서는 리디렉션이 발생 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="055d5-117">자세한 내용은 [운영 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="055d5-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="055d5-118">게시 된 응용 프로그램이 설치 되어 있고 제대로 작동 하는지 확인 한 후에는 MED-V 작업 영역에서 응용 프로그램을 추가 하거나 제거할 수 있는지 여부를 테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="055d5-119">응용 프로그램을 추가 하거나 제거할 수 있는지 테스트 하려면</span><span class="sxs-lookup"><span data-stu-id="055d5-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="055d5-120">MED-V 작업 영역에서 응용 프로그램을 추가 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="055d5-121">MED-V 작업 영역에서 응용 프로그램을 추가 하 고 제거 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역에 배포 된 응용 프로그램 관리](managing-applications-deployed-to-med-v-workspaces.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="055d5-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="055d5-122">응용 프로그램을 추가한 경우에는의 단계를 반복 하 여 [응용 프로그램 게시를 테스트](#bkmk-apppub) 하 여 새 응용 프로그램이 의도 한 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="055d5-123">응용 프로그램을 제거한 경우 **시작** 을 클릭 한 다음 **모든 프로그램** 을 클릭 하 고 제거한 모든 응용 프로그램이 더 이상 나열 되지 않는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="055d5-124">**참고**  응용 프로그램 게시 설정을 확인할 때 문제가 발생 하는 경우에는 [작업 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="055d5-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="055d5-125">응용 프로그램 게시 테스트를 완료 한 후 다른 MED-V 작업 영역 구성을 테스트 하 여 의도 한 대로 작동 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="055d5-126">MED-V 작업 영역 패키지 테스트를 완료 하 고 의도 한 대로 작동 하는지 확인 한 후에는 MED-V 작업 영역을 enterprise에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055d5-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="055d5-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="055d5-127">Related topics</span></span>

[<span data-ttu-id="055d5-128">URL 리디렉션을 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="055d5-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="055d5-129">처음 설치 설정을 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="055d5-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="055d5-130">MED-V 작업 영역 패키지 배포</span><span class="sxs-lookup"><span data-stu-id="055d5-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





