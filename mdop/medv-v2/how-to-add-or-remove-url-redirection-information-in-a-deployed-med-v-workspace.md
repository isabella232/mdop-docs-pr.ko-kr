---
title: 배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법
description: 배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826443"
---
# <span data-ttu-id="6e4f0-103">배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e4f0-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="6e4f0-104">배포 된 MED-V 작업 영역의 URL 리디렉션 정보를 편집 하려면 그룹 정책을 사용 하 여 시스템 레지스트리를 업데이트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="6e4f0-105">권장 하는 것은 아니지만 업데이트 된 URL 리디렉션 정보를 사용 하 여 MED-V 작업 영역을 다시 빌드하고 배포할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="6e4f0-106">레지스트리 키는 일반적으로 다음 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-106">The registry key is usually located at:</span></span>

<span data-ttu-id="6e4f0-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="6e4f0-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="6e4f0-108">다음과 같은 다중 문자열 값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="6e4f0-109">값 데이터는 `RedirectUrls` **Med-v 작업 영역 포장기**를 사용 하 여 med-v 작업 영역 패키지를 빌드할 때 리디렉션에 대해 지정한 모든 url의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="6e4f0-110">자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="6e4f0-111">다음 작업 중 하나를 수행 하 여 URL 리디렉션 정보를 추가 하 고 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="6e4f0-112">URL 리디렉션 레지스트리 키를 편집 하 고 그룹 정책을 사용 하 여 배포</span><span class="sxs-lookup"><span data-stu-id="6e4f0-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="6e4f0-113">URL 리디렉션 텍스트 파일을 편집 하 고 MED-V 작업 영역을 다시 빌드합니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="6e4f0-114">그룹 정책을 사용 하 여 URL 리디렉션 정보를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="6e4f0-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="6e4f0-115">이름이 지정 된 레지스트리 키 다중 문자열 값을 편집 `RedirectUrls` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="6e4f0-116">이 값은 일반적으로 다음 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-116">This value is typically located at:</span></span>

    <span data-ttu-id="6e4f0-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="6e4f0-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="6e4f0-118">레지스트리 키에 Url을 추가 하는 경우에는 MED-V 작업 영역 패키지를 빌드할 때 필요 했던 대로 한 줄에 하나씩 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="6e4f0-119">자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="6e4f0-120">그룹 정책을 사용 하 여 업데이트 된 레지스트리 키를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="6e4f0-121">그룹 정책을 사용 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="6e4f0-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="6e4f0-122">**참고**  이 방법으로 URL 리디렉션 정보를 편집 하는 방법은 MED-V 모범 사례입니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="6e4f0-123">업데이트 된 URL 텍스트 파일을 사용 하 여 MED-V 작업 영역을 다시 작성 하려면</span><span class="sxs-lookup"><span data-stu-id="6e4f0-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="6e4f0-124">리디렉션 목록에서 Url을 추가 하 고 제거 하는 또 다른 방법은 URL 리디렉션 텍스트 파일을 업데이트 한 다음이를 사용 하 여 새 MED-V 작업 영역을 빌드하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="6e4f0-125">그런 다음, ESD 시스템 등의 표준 배포 프로세스를 사용 하 여 MED-V 작업 영역을 이전 처럼 다시 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="6e4f0-126">**중요**  URL 리디렉션 정보를 편집 하는 방법은이 방법을 권장 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="6e4f0-127">또한 MED-V 작업 영역을 다시 실행할 때마다 엔터프라이즈에 다시 설치 해야 하는 경우를 제외 하 고 가상 컴퓨터에 저장 된 모든 데이터가 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e4f0-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="6e4f0-128">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6e4f0-128">Related topics</span></span>


[<span data-ttu-id="6e4f0-129">URL 리디렉션을 테스트하는 방법</span><span class="sxs-lookup"><span data-stu-id="6e4f0-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="6e4f0-130">MED-V 작업 영역에 배포된 응용 프로그램 관리</span><span class="sxs-lookup"><span data-stu-id="6e4f0-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="6e4f0-131">MED-V 작업 영역 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="6e4f0-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





