---
title: 특정 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
description: 특정 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813732"
---
# <span data-ttu-id="2311e-103">특정 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="2311e-103">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>


<span data-ttu-id="2311e-104">다음 절차를 사용 하 여 사용자 구성 파일을 사용 하 여 app-v 5.1 패키지를 App-v 파일 형식으로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-104">Use the following procedure to revert an App-V 5.1 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="2311e-105">패키지 되돌리기</span><span class="sxs-lookup"><span data-stu-id="2311e-105">To revert a package</span></span>**

1.  <span data-ttu-id="2311e-106">앱-V 4.6 패키지가 사용자에 게 게시 되어 있지만 다음 마이그레이션 방법을 사용 하 여 FTAs 및 바로 가기가 앱-v 5.1 패키지에 의해 간주 되는 것을 확인 합니다. [앱-v 4.6 패키지의 확장 지점을 특정 사용자를 위한 app-v 5.1로 마이그레이션하는 방법을 설명](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

    <span data-ttu-id="2311e-107">변환 된 패키지에 대 한 배포 구성 파일의 **userconfiguration** 섹션에서 정책을 설정 하려면 **userconfiguration** 섹션: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSE" PackageName = &lt; package ID &gt; \*\* 에 대해 다음 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="2311e-108">관리자 권한 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="2311e-109">PS &gt; **게시-AppVClientPackage $pkg –** &lt; 사용자 구성 파일에 대 한 DynamicUserConfigurationPath 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="2311e-109">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="2311e-110">게시 새로 고침을 수행 하거나 App-v 4.6에 대해 예정 된 다음 게시 새로 고침을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-110">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="2311e-111">FTAs 또는 바로 가기를 사용 하 여 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-111">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="2311e-112">이제 앱이 app-v 4.6를 사용 하 여 열립니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-112">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="2311e-113">참고</span><span class="sxs-lookup"><span data-stu-id="2311e-113">Note</span></span>**  
    <span data-ttu-id="2311e-114">App-v 5.1 패키지가 더 이상 필요 하지 않은 경우 App-v 5.1 패키지의 게시를 취소 하면 확장 지점이 자동으로 App-v 4.6로 다시 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2311e-114">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="2311e-115">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2311e-115">Related topics</span></span>


[<span data-ttu-id="2311e-116">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="2311e-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









