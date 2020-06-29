---
title: 특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법
description: 특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813884"
---
# <span data-ttu-id="576c9-103">특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="576c9-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>

<span data-ttu-id="576c9-104">**참고:** App-v 4.6에서 메인스트림 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="576c9-105">다음 절차를 사용 하 여 배포 구성 파일을 사용 하 여 앱-V 4.6 패키지의 확장 지점을 App-v 5.0 패키지로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-105">Use the following procedure to migrate extension points from an App-V4.6package to a App-V 5.0 package using the deployment configuration file.</span></span>

<span data-ttu-id="576c9-106">**참고**  다음 절차에서는 App-v 5.0 관리 서버가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-106">**Note** The following procedure does not require an App-V 5.0 management server.</span></span>

 

**<span data-ttu-id="576c9-107">배포 구성 파일을 사용 하 여 앱-V 4.6 패키지의 패키지에서 변환 된 앱 V 5.0 패키지로 확장 지점을 마이그레이션하려면</span><span class="sxs-lookup"><span data-stu-id="576c9-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.0 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="576c9-108">마이그레이션할 패키지에 대 한 배포 구성 파일이 포함 된 디렉터리를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="576c9-109">정책을 설정 하려면 **Userconfiguration** 섹션에 다음 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="576c9-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; 패키지 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="576c9-111">다음은 배포 구성 파일의 콘텐츠 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="576c9-112">&lt;? xml 버전 = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="576c9-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="576c9-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="576c9-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; Package ID &gt; DisplayName = &lt; 표시 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="576c9-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="576c9-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="576c9-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="576c9-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="576c9-118">PackageName = &lt; 패키지 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="576c9-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="576c9-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="576c9-121">앱-V 5.0 패키지를 추가 하려면 관리자 권한 PowerShell 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-121">To add the App-V 5.0 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="576c9-122">PS &gt; **$pkg AppvClientPackage** **–** &lt; 패키지 위치에 대 한 경로 경로 경로가 &gt;  - 배포 구성 파일에 대 한**dynamicdeploymentconfiguration** &lt; 경로입니다.&gt;</span><span class="sxs-lookup"><span data-stu-id="576c9-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="576c9-123">PS &gt; **게시-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="576c9-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="576c9-124">마이그레이션을 테스트 하려면 연결 된 FTAs 또는 바로 가기를 사용 하 여 가상 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="576c9-125">앱-V 5.0이 있는 응용 프로그램이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-125">The application opens with App-V 5.0.</span></span> <span data-ttu-id="576c9-126">두 가지 경우 모두 App-v 4.6 패키지와 변환 된 앱-V 5.0 패키지가 사용자에 게 게시 되지만, 응용 프로그램의 FTAs 및 바로 가기가 App-v 5.0 패키지로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-126">Both, the App-V 4.6 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="576c9-127">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="576c9-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="576c9-128">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="576c9-129">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="576c9-129">Got an App-V issue?</span></span>** <span data-ttu-id="576c9-130">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="576c9-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="576c9-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="576c9-131">Related topics</span></span>


[<span data-ttu-id="576c9-132">특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="576c9-132">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="576c9-133">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="576c9-133">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





