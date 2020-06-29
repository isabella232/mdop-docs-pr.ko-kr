---
title: 특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
description: 특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813729"
---
# <span data-ttu-id="782a2-103">특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="782a2-103">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>

<span data-ttu-id="782a2-104">*참고:*\* app-v 4.6에는 메인스트림 지원이 종료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="782a2-105">다음은 App-v 4.6 SP3 클라이언트가 이미 설치 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="782a2-106">다음 절차를 사용 하 여 배포 구성 파일을 사용 하 여 앱-V 5.0 패키지의 확장 지점을 App-v 4.6 파일 형식으로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-106">Use the following procedure to revert extension points from an App-V 5.0 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="782a2-107">패키지 되돌리기</span><span class="sxs-lookup"><span data-stu-id="782a2-107">To revert a package</span></span>**

1.  <span data-ttu-id="782a2-108">앱-V 4.6 패키지가 사용자에 게 게시 되어 있지만 다음 마이그레이션 방법을 사용 하 여 FTAs 및 바로 가기가 앱-v 5.0 패키지에 의해 간주 되는 경우 [특정 컴퓨터의 모든 사용자에 대해 앱-v 4.6 패키지의 확장 지점을 변환 된 app-v 5.0 패키지로 마이그레이션하는 방법을](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-108">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="782a2-109">변환 된 패키지에 대 한 배포 구성 파일의 **userconfiguration** 섹션에서 정책을 설정 하려면 **userconfiguration** 섹션: \*\*ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSE" PackageName = &lt; package ID &gt; \*\* 에 대해 다음 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-109">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="782a2-110">관리자 권한 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-110">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="782a2-111">PS &gt; **Set-AppvClientPackage $pkg –** &lt; 배포 구성 파일에 대 한 dynamicdeploymentconfiguration 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="782a2-111">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="782a2-112">PS &gt; **게시-AppVClientPackage $Pkg – DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="782a2-112">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="782a2-113">게시 새로 고침을 수행 하거나 App-v 4.6 SP2 패키지에 예정 된 다음 게시 새로 고침을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-113">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 SP2 package.</span></span>

    <span data-ttu-id="782a2-114">FTAs 또는 바로 가기를 사용 하 여 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-114">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="782a2-115">이제 앱이 app-v 4.6를 사용 하 여 열립니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-115">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="782a2-116">참고</span><span class="sxs-lookup"><span data-stu-id="782a2-116">Note</span></span>**  
    <span data-ttu-id="782a2-117">App-v 5.0 패키지가 더 이상 필요 하지 않은 경우 App-v 5.0 패키지의 게시를 취소 하면 확장 지점이 자동으로 App-v 4.6로 다시 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="782a2-117">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="782a2-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="782a2-118">Related topics</span></span>


[<span data-ttu-id="782a2-119">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="782a2-119">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









