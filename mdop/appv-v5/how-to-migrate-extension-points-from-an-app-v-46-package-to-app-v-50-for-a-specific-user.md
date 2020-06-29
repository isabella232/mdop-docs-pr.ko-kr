---
title: 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법
description: 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813876"
---
# <span data-ttu-id="63eaa-103">특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="63eaa-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>

<span data-ttu-id="63eaa-104">*참고:*\* app-v 4.6에는 메인스트림 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="63eaa-105">다음 절차를 사용 하 여 사용자 구성 파일을 사용 하 여 App-v로 만든 패키지를 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-105">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

**<span data-ttu-id="63eaa-106">패키지를 변환 하려면</span><span class="sxs-lookup"><span data-stu-id="63eaa-106">To convert a package</span></span>**

1. <span data-ttu-id="63eaa-107">변환 하려는 패키지의 사용자 구성 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="63eaa-108">정책을 설정 하려면 **Userconfiguration** 섹션: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGENAME = &lt; Package ID &gt; \*\*에서 다음 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="63eaa-109">다음은 사용자 구성 파일의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="63eaa-110">&lt;? xml 버전 = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="63eaa-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="63eaa-111">&lt;UserConfiguration PackageId = &lt; 패키지 ID &gt; DisplayName = &lt; 패키지의 이름입니다.&gt;</span><span class="sxs-lookup"><span data-stu-id="63eaa-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="63eaa-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="63eaa-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="63eaa-113">PackageName = &lt; 패키지 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="63eaa-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="63eaa-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="63eaa-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="63eaa-115">앱-V 5.0 패키지를 추가 하려면 관리자 권한 PowerShell 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-115">To add the App-V 5.0 package type the following in an elevated PowerShell command prompt:</span></span>

   <span data-ttu-id="63eaa-116">PS &gt; **$Pkg = AppvClientPackage-** &lt; 패키지 위치의 경로 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="63eaa-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="63eaa-117">PS &gt; **게시-AppVClientPackage $pkg-** &lt; 사용자 구성 파일에 대 한 DynamicUserConfiguration 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="63eaa-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="63eaa-118">FTAs 또는 지금 바로 가기 키를 사용 하 여 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="63eaa-119">응용 프로그램은 App-v 5.0를 사용 하 여 열어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-119">The application should open using App-V 5.0.</span></span>

   <span data-ttu-id="63eaa-120">App-v SP2 패키지와 변환 된 앱-V 5.0 패키지가 사용자에 게 게시 되지만, 응용 프로그램의 FTAs 및 바로 가기가 App-v 5.0 패키지에 의해 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-120">The App-V SP2 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="63eaa-121">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="63eaa-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="63eaa-122">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="63eaa-123">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="63eaa-123">Got an App-V issue?</span></span>** <span data-ttu-id="63eaa-124">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63eaa-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="63eaa-125">관련 항목</span><span class="sxs-lookup"><span data-stu-id="63eaa-125">Related topics</span></span>


[<span data-ttu-id="63eaa-126">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="63eaa-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





