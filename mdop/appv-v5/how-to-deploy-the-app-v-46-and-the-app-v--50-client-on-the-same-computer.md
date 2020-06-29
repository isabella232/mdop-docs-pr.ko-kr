---
title: 앱-V 4.6 및 앱-V 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법
description: 앱-V 4.6 및 앱-V 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814180"
---
# <span data-ttu-id="e6927-103">앱-V 4.6 및 앱-V 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="e6927-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="e6927-104">**참고:** App-v 4.6에서 메인스트림 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="e6927-105">다음은 App-v 4.6 SP3 클라이언트가 이미 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="e6927-106">다음 정보를 사용 하 여 앱-V 5.0 클라이언트 (가능에 따라 최신 서비스 팩 및 핫픽스 사용)와 동일한 컴퓨터에 App-v 4.6 SP3 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="e6927-107">지원 되는 버전, 요구 사항 및 기타 계획 정보는 [이전 버전의 app-v에서 마이그레이션 계획](planning-for-migrating-from-a-previous-version-of-app-v.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6927-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="e6927-108">동일한 컴퓨터에 App-v 5.0 클라이언트 및 App-v 4.6 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="e6927-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="e6927-109">앱-v 4.6 버전의 클라이언트를 실행 하는 컴퓨터에 App-v 5.0 SP3 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="e6927-110">최상의 결과를 위해서는 App-v 5.0 SP3 클라이언트에 사용할 수 있는 모든 업데이트를 설치 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="e6927-111">패키지를 점차적으로 변환 또는 다시 시퀀싱 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="e6927-112">패키지를 변환 하려면 App-v 5.0 패키지 변환기를 사용 하 여 필수 패키지를 App-v 5.0 (**appv**) 파일 형식으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="e6927-113">패키지를 다시 시퀀싱 하려면 최신 버전의 시퀀서를 사용 하 여 최상의 결과를 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6927-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="e6927-114">패키지 게시에 대 한 자세한 내용은 [관리 콘솔을 사용 하 여 패키지를 게시 하는 방법을](how-to-publish-a-package-by-using-the-management-console-50.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6927-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="e6927-115">패키지를 클라이언트 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="e6927-116">필요에 따라 확장명 점을 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-116">Convert extension points, as needed.</span></span> <span data-ttu-id="e6927-117">자세한 내용은 다음 리소스를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e6927-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="e6927-118">특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="e6927-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="e6927-119">특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="e6927-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="e6927-120">이전 버전의 App-V에서 만든 패키지를 변환하는 방법</span><span class="sxs-lookup"><span data-stu-id="e6927-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="e6927-121">App-v 5.0 패키지가 성공적으로 실행 되었는지 테스트 한 다음 4.6 패키지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="e6927-122">클라이언트 컴퓨터의 사용자 상태를 확인 하려면 [사용자 환경 가상화](https://technet.microsoft.com/library/dn458947.aspx) 또는 다른 사용자 환경 관리 도구를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="e6927-123">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="e6927-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e6927-124">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e6927-125">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="e6927-125">Got an App-V issue?</span></span>** <span data-ttu-id="e6927-126">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6927-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e6927-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e6927-127">Related topics</span></span>


[<span data-ttu-id="e6927-128">App-V의 이전 버전에서 마이그레이션 계획</span><span class="sxs-lookup"><span data-stu-id="e6927-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="e6927-129">App-V 5.0 Sequencer 및 Client 배포</span><span class="sxs-lookup"><span data-stu-id="e6927-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





