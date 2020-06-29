---
title: 이전 버전의 App-V에서 만든 패키지를 변환하는 방법
description: 이전 버전의 App-V에서 만든 패키지를 변환하는 방법
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814361"
---
# <span data-ttu-id="f2175-103">이전 버전의 App-V에서 만든 패키지를 변환하는 방법</span><span class="sxs-lookup"><span data-stu-id="f2175-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="f2175-104">패키지 변환기 유틸리티를 사용 하 여 이전 버전의 App-v로 만든 가상 응용 프로그램 패키지를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="f2175-105">참고</span><span class="sxs-lookup"><span data-stu-id="f2175-105">Note</span></span>**  
<span data-ttu-id="f2175-106">64 비트 아키텍처로 컴퓨터를 실행 하는 경우 x86 버전의 PowerShell을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="f2175-107">Package converter는 App-v 4.5 sequencer 또는 이후 버전을 사용 하 여 만든 패키지만 직접 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="f2175-108">App-V 4.5 이전 버전을 사용 하 여 만든 패키지는 변환 전에 App-v 4.5 또는 App-v 4.6 형식으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="f2175-109">다음 정보는 기존 가상 응용 프로그램 패키지를 변환 하는 방향을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="f2175-110">중요</span><span class="sxs-lookup"><span data-stu-id="f2175-110">Important</span></span>**  
<span data-ttu-id="f2175-111">패키지 원료 파일을 항상 안전한 위치 및 디렉터리에 저장 하도록 패키지 변환기를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="f2175-112">보안 위치에는 관리자만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="f2175-113">또한 패키지를 배포 하는 경우 안전한 위치에 패키지를 저장 하거나 변환 프로세스 중에 로그인 할 수 있는 다른 사용자가 없는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="f2175-114">시작</span><span class="sxs-lookup"><span data-stu-id="f2175-114">Getting started</span></span>**

1.  <span data-ttu-id="f2175-115">환경에서 컴퓨터에 App-v 시퀀서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-115">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="f2175-116">Sequencer를 설치 하는 방법에 대 한 자세한 내용은 [sequencer를 설치](how-to-install-the-sequencer-beta-gb18030.md)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2175-116">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2. <span data-ttu-id="f2175-117">필요한 Powershell 모듈 가져오기</span><span class="sxs-lookup"><span data-stu-id="f2175-117">Import the required Powershell Module</span></span>

```powershell
Import-Module AppVPkgConverter
```

3. <span data-ttu-id="f2175-118">다음 cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-118">The following cmdlets are available:</span></span>

   -   <span data-ttu-id="f2175-119">테스트-AppvLegacyPackage-이 cmdlet은 패키지를 검사 하도록 디자인 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-119">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="f2175-120">**Sft** 파일 누락, 잘못 된 원본, **osd** 파일 오류 또는 잘못 된 패키지 버전 등 패키지 오류에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-120">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="f2175-121">이 cmdlet은 **sft** 파일을 구문 분석 하거나 깊이 유효성 검사를 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-121">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="f2175-122">PowerShell cmdline을 사용 하 여이 cmdlet에 대 한 옵션 및 기본 기능에 대 한 자세한 내용은을 입력 `Test-AppvLegacyPackage -?` 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2175-122">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

   -   <span data-ttu-id="f2175-123">ConvertFrom-AppvLegacyPackage – 기존 패키지를 변환 하려면를 입력 `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-123">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="f2175-124">이 명령은 `c:\contentStore` 기존 패키지의 위치를 나타내고 `c:\convertedPackages` 결과 app-v 5.0 가상 응용 프로그램 패키지 파일이 저장 되는 출력 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-124">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.0 virtual application package file will be saved.</span></span> <span data-ttu-id="f2175-125">새 이름을 지정 하지 않으면 기본적으로 이전 패키지 이름이 App-V 5.0 파일 이름에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-125">By default, if you do not specify a new name, the old package name will be used for the App-V 5.0 filename.</span></span>

       <span data-ttu-id="f2175-126">또한 패키지 변환기는 패키지를 App-v 패키지의 스트림으로 설정 하 여 App-v 5.0 패키지의 성능을 최적화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-126">Additionally, the package converter optimizes performance of packages in App-V 5.0 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="f2175-127">이는 기본 기능 블록 보다 성능이 더 복잡 하며 패키지를 완전히 다운로드 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-127">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="f2175-128">플래그 **Downloadfullpackageonfirstlaunch** 를 사용 하 여 패키지를 변환 하 고 기본적으로 패키지가 완전히 다운로드 되도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-128">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

       **<span data-ttu-id="f2175-129">참고</span><span class="sxs-lookup"><span data-stu-id="f2175-129">Note</span></span>**  
       <span data-ttu-id="f2175-130">출력 디렉터리를 지정 하기 전에 출력 디렉터리를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2175-130">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="f2175-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f2175-131">Related topics</span></span>


[<span data-ttu-id="f2175-132">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="f2175-132">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









