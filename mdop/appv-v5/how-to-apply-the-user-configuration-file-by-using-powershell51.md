---
title: PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법
description: PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법
author: dansimp
ms.assetid: 986e638c-4a0c-4a7e-be73-f4615e8b8000
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97b3db253993d6d855384ee5d9771a7f9ff5b64d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814428"
---
# <span data-ttu-id="be885-103">PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법</span><span class="sxs-lookup"><span data-stu-id="be885-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="be885-104">패키지를 특정 사용자에 게 게시 하 고 패키지가 실행 되는 방식을 결정 하는 경우 동적 사용자 구성 파일이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="be885-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="be885-105">다음 절차를 사용 하 여 사용자 관련 구성 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be885-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="be885-106">다음 절차는 예제를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="be885-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="be885-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="be885-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="be885-108">사용자 구성 파일을 적용 하려면</span><span class="sxs-lookup"><span data-stu-id="be885-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="be885-109">PowerShell 콘솔을 사용 하 여 패키지를 컴퓨터에 추가 하려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="be885-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="be885-110">**추가-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span><span class="sxs-lookup"><span data-stu-id="be885-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="be885-111">다음 명령을 사용 하 여 패키지를 사용자에 게 게시 하 고 업데이트 된 동적 사용자 구성 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be885-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="be885-112">게시-AppVClientPackage $pkg – DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="be885-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="be885-113">**App-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="be885-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="be885-114">[여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="be885-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="be885-115">App-v 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="be885-115">Got an App-V issue?</span></span>** <span data-ttu-id="be885-116">[App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be885-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="be885-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="be885-117">Related topics</span></span>


[<span data-ttu-id="be885-118">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="be885-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





