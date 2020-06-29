---
title: 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.1로 확장 지점을 마이그레이션하는 방법
description: 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.1로 확장 지점을 마이그레이션하는 방법
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813868"
---
# <span data-ttu-id="26a9c-103">특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.1로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="26a9c-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>


<span data-ttu-id="26a9c-104">다음 절차를 사용 하 여 사용자 구성 파일을 사용 하 여 App-v로 만든 패키지를 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-104">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

<span data-ttu-id="26a9c-105">**참고**  이 절차에서는 최신 버전의 App-v 4.6를 실행 하 고 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="26a9c-106">패키지를 변환 하려면</span><span class="sxs-lookup"><span data-stu-id="26a9c-106">To convert a package</span></span>**

1. <span data-ttu-id="26a9c-107">변환 하려는 패키지의 사용자 구성 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="26a9c-108">정책을 설정 하려면 **Userconfiguration** 섹션: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGENAME = &lt; Package ID &gt; \*\*에서 다음 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="26a9c-109">다음은 사용자 구성 파일의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="26a9c-110">&lt;? xml 버전 = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="26a9c-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="26a9c-111">&lt;UserConfiguration PackageId = &lt; 패키지 ID &gt; DisplayName = &lt; 패키지의 이름입니다.&gt;</span><span class="sxs-lookup"><span data-stu-id="26a9c-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="26a9c-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="26a9c-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="26a9c-113">PackageName = &lt; 패키지 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="26a9c-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="26a9c-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="26a9c-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="26a9c-115">App-v 5.1 패키지를 추가 하려면 관리자 권한 PowerShell 명령 프롬프트 창에 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-115">To add the App-V 5.1 package, type the following in an elevated PowerShell command prompt window:</span></span>

   <span data-ttu-id="26a9c-116">PS &gt; **$Pkg = AppvClientPackage-** &lt; 패키지 위치의 경로 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="26a9c-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="26a9c-117">PS &gt; **게시-AppVClientPackage $pkg-** &lt; 사용자 구성 파일에 대 한 DynamicUserConfiguration 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="26a9c-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="26a9c-118">FTAs 또는 지금 바로 가기 키를 사용 하 여 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="26a9c-119">응용 프로그램은 App-v 5.1를 사용 하 여 열어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-119">The application should open using App-V 5.1.</span></span>

   <span data-ttu-id="26a9c-120">App-v 4.6 패키지와 변환 된 앱-V 5.1 패키지는 사용자에 게 게시 되지만, 응용 프로그램의 FTAs 및 바로 가기가 App-v 5.1 패키지에 의해 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-120">The App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="26a9c-121">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="26a9c-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="26a9c-122">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="26a9c-123">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="26a9c-123">Got an App-V issue?</span></span>** <span data-ttu-id="26a9c-124">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26a9c-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="26a9c-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="26a9c-125">Related topics</span></span>


[<span data-ttu-id="26a9c-126">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="26a9c-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="26a9c-127">특정 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="26a9c-127">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





