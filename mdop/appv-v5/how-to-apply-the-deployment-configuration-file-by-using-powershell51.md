---
title: PowerShell을 사용하여 배포 구성 파일을 적용하는 방법
description: PowerShell을 사용하여 배포 구성 파일을 적용하는 방법
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814441"
---
# <span data-ttu-id="c434e-103">PowerShell을 사용하여 배포 구성 파일을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="c434e-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="c434e-104">패키지를 게시 하기 전에 앱-V 5.1 클라이언트를 실행 하는 컴퓨터에 패키지를 추가 하거나 설정할 때 동적 배포 구성 파일이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.1 client before the package has been published.</span></span> <span data-ttu-id="c434e-105">파일은 App-v 5.1 클라이언트를 실행 하는 컴퓨터의 모든 사용자에 대 한 패키지의 기본 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-105">The file configures the default settings for package for all users on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="c434e-106">이 섹션에서는 배포 구성 파일을 사용 하는 데 필요한 단계에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="c434e-107">이 절차는 다음 예제를 기반으로 하며 컴퓨터에 다음과 같은 패키지 및 구성 파일이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="c434e-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="c434e-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="c434e-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="c434e-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="c434e-110">PowerShell을 사용 하 여 배포 구성 파일을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="c434e-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="c434e-111">특정 컴퓨터에서 패키지를 실행 하는 모든 사용자에 대해 새 기본 구성 집합을 지정 하려면 PowerShell 콘솔을 사용 하 여 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="c434e-112">추가-AppVClientPackage – 경로 c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="c434e-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="c434e-113">참고</span><span class="sxs-lookup"><span data-stu-id="c434e-113">Note</span></span>**  
    <span data-ttu-id="c434e-114">이 명령은 결과 개체를 $pkg에 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="c434e-115">패키지가 컴퓨터에 이미 있는 경우 **Set AppVclientPackage** cmdlet을 사용 하 여 배포 구성 문서를 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c434e-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="c434e-116">Set-AppVClientPackage-Name Myapp – Path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="c434e-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="c434e-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c434e-117">Related topics</span></span>


[<span data-ttu-id="c434e-118">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="c434e-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









