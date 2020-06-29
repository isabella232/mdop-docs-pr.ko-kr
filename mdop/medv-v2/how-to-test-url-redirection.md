---
title: URL 리디렉션을 테스트하는 방법
description: URL 리디렉션을 테스트하는 방법
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824448"
---
# <span data-ttu-id="52277-103">URL 리디렉션을 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="52277-103">How to Test URL Redirection</span></span>


<span data-ttu-id="52277-104">처음으로 설치를 완료 한 후에 다음 작업을 수행 하 여 URL 리디렉션 기능이 예상 대로 작동 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52277-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="52277-105">**중요**  MED-V 호스트 에이전트는 URL 리디렉션이 올바르게 작동 하려면 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="52277-106">URL 리디렉션을 테스트 하려면</span><span class="sxs-lookup"><span data-stu-id="52277-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="52277-107">호스트 컴퓨터에서 Internet Explorer 브라우저를 열고 리디렉션에 대해 지정한 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="52277-108">게스트 가상 컴퓨터의 Internet Explorer에서 웹 페이지가 열려 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="52277-109">테스트 하려는 각 URL에 대해이 과정을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="52277-110">URL을 추가 하거나 제거할 수 있는지 테스트 하려면</span><span class="sxs-lookup"><span data-stu-id="52277-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="52277-111">MED-V 작업 영역에서 URL을 추가 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="52277-112">MED-V 작업 영역의 리디렉션에 대 한 Url을 추가 하 고 제거 하는 방법에 대 한 자세한 내용은 [MED-V URL 리디렉션 관리](manage-med-v-url-redirection.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52277-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="52277-113">리디렉션 목록에 URL을 추가한 경우에는 [Url 리디렉션을 테스트 하](#bkmk-urlredir) 는 단계를 반복 하 여 새 URL이 의도 한 대로 리디렉션 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="52277-114">리디렉션 목록에서 URL을 제거한 경우 다음 단계를 따라 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="52277-115">호스트 컴퓨터에서 Internet Explorer 브라우저를 열고 리디렉션 목록에서 제거한 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="52277-116">게스트 가상 컴퓨터가 아닌 호스트 컴퓨터의 Internet Explorer에서 웹 페이지가 열려 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="52277-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="52277-117">**참고**  URL 리디렉션 변경 내용이 적용 되는 데 몇 초 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52277-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="52277-118">**참고**  URL 리디렉션 설정을 확인할 때 문제가 발생 하는 경우에는 [작업 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52277-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="52277-119">MED-V 작업 영역에서 URL 리디렉션 테스트를 완료 한 후 다른 구성을 테스트 하 여 의도 한 대로 작동 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52277-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="52277-120">MED-V 작업 영역 패키지 테스트를 완료 하 고 의도 한 대로 작동 하는지 확인 한 후에는 MED-V 작업 영역을 enterprise에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52277-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="52277-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="52277-121">Related topics</span></span>

[<span data-ttu-id="52277-122">응용 프로그램 게시를 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="52277-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="52277-123">처음 설치 설정을 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="52277-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="52277-124">MED-V 작업 영역 패키지 배포</span><span class="sxs-lookup"><span data-stu-id="52277-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





