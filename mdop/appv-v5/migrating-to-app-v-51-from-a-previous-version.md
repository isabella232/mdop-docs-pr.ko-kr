---
title: 이전 버전에서 App-V 5.1로 마이그레이션
description: 이전 버전에서 App-V 5.1로 마이그레이션
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813553"
---
# <span data-ttu-id="69a64-103">이전 버전에서 App-V 5.1로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="69a64-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="69a64-104">Microsoft Application Virtualization (App-v) 5.1를 사용 하 여 기존 App-v 4.6 또는 App-v 5.0 인프라를 보다 유연 하 고 통합 하 고 앱-v 5.1 인프라를 더 쉽게 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="69a64-105">그러나 앱-V 4. x에서 App-v 5.1으로 직접 마이그레이션할 수는 없으며 먼저 App-v 5.0로 마이그레이션해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="69a64-106">App-v 4. x에서 App-v 5.0으로 마이그레이션하는 방법에 대 한 자세한 내용은 [이전 버전에서 마이그레이션을](migrating-from-a-previous-version-app-v-50.md) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69a64-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="69a64-107">**참고**  App-v 5.1 패키지는 앱-v 5.0 패키지와 정확히 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="69a64-108">버전 간에 패키지 형식이 변경 되지 않았으므로 app-v 5.0 패키지를 App-v 5.1 패키지로 변환할 필요는 없습니다 .이 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="69a64-109">App-v 4.6 및 App-v 5.1 간의 차이점에 대 한 자세한 내용은 [app-v 5.0에 대 한](about-app-v-50.md)앱- **v 4.6 및 app-v 5.0 섹션의 차이점** 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69a64-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="69a64-110">앱-V 5.1 패키지 변환기의 향상 된 기능</span><span class="sxs-lookup"><span data-stu-id="69a64-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="69a64-111">이제 패키지 변환기를 사용 하 여 스크립트를 포함 하는 App-v 4.6 패키지를 변환할 수 있으며, 이제 원본 osd 파일의 레지스트리 정보와 스크립트가 패키지 변환기 출력에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="69a64-112">또한 cmdlet에 매개 변수를 사용 하 여 `–OSDsToIncludeInPackage` `ConvertFrom-AppvLegacyPackage` 변환 되는 osd 파일의 정보를 지정 하 고 새 패키지 내에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a64-113">앱의 새로운 기능-V 5.1</span><span class="sxs-lookup"><span data-stu-id="69a64-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="69a64-114">앱-V 5.1 이전</span><span class="sxs-lookup"><span data-stu-id="69a64-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-115">패키지와 연결 된 .osd 파일에 해당 하는 새 .xml 파일이 만들어집니다. 이러한 파일에는 다음 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="69a64-116">환경 변수</span><span class="sxs-lookup"><span data-stu-id="69a64-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="69a64-117">정의</span><span class="sxs-lookup"><span data-stu-id="69a64-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="69a64-118">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="69a64-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="69a64-119">레지스트리 정보</span><span class="sxs-lookup"><span data-stu-id="69a64-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="69a64-120">문자</span><span class="sxs-lookup"><span data-stu-id="69a64-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="69a64-121">이제 매개 변수를 사용 하 여 원본 디렉터리에 있는 .osd 파일의 하위 집합에 있는 정보를 패키지에 추가 하도록 선택할 수 있습니다 <code>-OSDsToIncludeInPackage</code> .</span><span class="sxs-lookup"><span data-stu-id="69a64-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a64-122">패키지와 연결 된 osd 파일에 포함 된 레지스트리 정보와 스크립트는 패키지 변환기 출력에 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="69a64-123">패키지 변환기는 원본 디렉터리에 있는 모든 .osd 파일의 정보로 새 패키지를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="69a64-124">예제 변환 문</span><span class="sxs-lookup"><span data-stu-id="69a64-124">Example conversion statement</span></span>

<span data-ttu-id="69a64-125">새 프로세스를 이해 하려면 다음 예제 `ConvertFrom-AppvLegacyPackage` package converter 문을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="69a64-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="69a64-126">원본 디렉터리 (\\\\OldPkgStore\\ContosoApp)에 다음이 포함 된 경우:</span><span class="sxs-lookup"><span data-stu-id="69a64-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="69a64-127">ContosoApp. sft</span><span class="sxs-lookup"><span data-stu-id="69a64-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="69a64-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="69a64-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="69a64-129">ContosoApp.sprj</span><span class="sxs-lookup"><span data-stu-id="69a64-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="69a64-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="69a64-131">X. osd</span><span class="sxs-lookup"><span data-stu-id="69a64-131">X.osd</span></span>

-   <span data-ttu-id="69a64-132">Y osd</span><span class="sxs-lookup"><span data-stu-id="69a64-132">Y.osd</span></span>

-   <span data-ttu-id="69a64-133">Z. i a osd</span><span class="sxs-lookup"><span data-stu-id="69a64-133">Z.osd</span></span>

**<span data-ttu-id="69a64-134">다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="69a64-135">대상 디렉토리 (\\\\NewPkgStore\\ContosoApp)에서 다음이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="69a64-136">ContosoApp</span><span class="sxs-lookup"><span data-stu-id="69a64-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="69a64-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="69a64-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="69a64-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="69a64-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="69a64-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-140">X\_Config.xml</span></span>

-   <span data-ttu-id="69a64-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="69a64-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-142">Z\_Config.xml</span></span>

**<span data-ttu-id="69a64-143">위의 예제에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a64-144">다음 원본 디렉터리 파일 ...</span><span class="sxs-lookup"><span data-stu-id="69a64-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="69a64-145">... 이러한 대상 디렉터리 파일로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="69a64-146">... 그리고 다음 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="69a64-147">설명</span><span class="sxs-lookup"><span data-stu-id="69a64-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="69a64-148">X. osd</span><span class="sxs-lookup"><span data-stu-id="69a64-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="69a64-149">Y osd</span><span class="sxs-lookup"><span data-stu-id="69a64-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="69a64-150">Z. i a osd</span><span class="sxs-lookup"><span data-stu-id="69a64-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="69a64-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="69a64-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="69a64-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="69a64-154">환경 변수</span><span class="sxs-lookup"><span data-stu-id="69a64-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="69a64-155">정의</span><span class="sxs-lookup"><span data-stu-id="69a64-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="69a64-156">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="69a64-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="69a64-157">레지스트리 정보</span><span class="sxs-lookup"><span data-stu-id="69a64-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="69a64-158">스크립트</span><span class="sxs-lookup"><span data-stu-id="69a64-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="69a64-159">각 .osd 파일은 앱-V 5.1 배포 구성 형식에 나열 된 항목을 포함 하는 별도의 해당 .xml 파일로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="69a64-160">이러한 항목은 이러한 .xml 파일에서 복사 하 여 원하는 대로 배포 구성 또는 사용자 구성 파일에 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="69a64-161">이 예제에는 원본 디렉터리에 있는 세 개의 .osd 파일에 해당 하는 세 개의 .xml 파일이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="69a64-162">각 .xml 파일에는 환경 변수, 바로 가기, 파일 형식 연결, 레지스트리 정보 및 해당 .osd 파일의 스크립트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="69a64-163">X. osd</span><span class="sxs-lookup"><span data-stu-id="69a64-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="69a64-164">Y osd</span><span class="sxs-lookup"><span data-stu-id="69a64-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="69a64-165">ContosoApp</span><span class="sxs-lookup"><span data-stu-id="69a64-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="69a64-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="69a64-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="69a64-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="69a64-168">환경 변수</span><span class="sxs-lookup"><span data-stu-id="69a64-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="69a64-169">정의</span><span class="sxs-lookup"><span data-stu-id="69a64-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="69a64-170">파일 형식 연결</span><span class="sxs-lookup"><span data-stu-id="69a64-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="69a64-171">매개 변수에 지정 된 .osd 파일의 정보는 <code>-OSDsToIncludeInPackage</code> 변환 되어 패키지 내에 배치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="69a64-172">그런 다음 새 패키지를 시퀀싱 하는 경우 앱-V 시퀀서와 마찬가지로 배포 구성 파일과 사용자 구성 파일을 패키지의 내용으로 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="69a64-173">이 예제에서는 X. osd 및 Y osd에 포함 된 환경 변수, 바로 가기 및 파일 형식 연결을 변환 하 여 App-v 패키지에 배치 했으며 이러한 정보 중 일부는 배포 구성 및 사용자 구성 파일에도 포함 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="69a64-174">이 매개 변수는 인수로 포함 되기 때문에 X. osd 및 Y osd가 사용 되었습니다 <code>-OSDsToIncludeInPackage</code> .</span><span class="sxs-lookup"><span data-stu-id="69a64-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="69a64-175">이 인수 중 하나로 포함 되지 않았으므로 Z.e.n.works의 정보는 패키지에 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="69a64-176">이전 버전의 App-v를 사용 하 여 만든 패키지 변환</span><span class="sxs-lookup"><span data-stu-id="69a64-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="69a64-177">패키지 변환기 유틸리티를 사용 하 여 앱-V 5.0 이전 버전의 app-v를 사용 하 여 만든 가상 응용 프로그램 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="69a64-178">패키지 변환기는 PowerShell을 사용 하 여 패키지를 변환 하며 변환이 필요한 패키지가 여러 개 있는 경우 프로세스를 자동화 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="69a64-179">**중요**  기존 패키지를 변환한 후에는 패키지를 배포 하기 전에 패키지를 테스트 하 여 변환 프로세스가 성공적으로 수행 되었는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="69a64-180">기존 패키지를 변환 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="69a64-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a64-181">문제</span><span class="sxs-lookup"><span data-stu-id="69a64-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="69a64-182">해결 방법</span><span class="sxs-lookup"><span data-stu-id="69a64-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-183">DSC를 사용 하는 가상 패키지는 변환 후 연결 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a64-184">연결 그룹을 사용 하 여 패키지를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-184">Link the packages using connection groups.</span></span> <span data-ttu-id="69a64-185"><a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">연결 그룹 관리를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="69a64-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a64-186">환경 변수 충돌은 변환 중에 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a64-187">관련 된 .osd 파일의 모든 충돌을 해결 <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-188">변환 하는 동안 하드 코드 된 경로가 감지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a64-189">하드 코드 된 경로는 제대로 변환 하기가 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="69a64-190">패키지 변환기는 하드 코드 된 경로가 들어 있는 파일을 사용 하 여 패키지를 감지 하 고 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="69a64-191">하드 코드 된 경로를 사용 하 여 파일을 보고 패키지에 파일이 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="69a64-192">그렇다면 패키지를 다시 시퀀싱 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="69a64-193">패키지를 변환할 때 파일 또는 바로 가기가 실패 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="69a64-194">앱-V 4.6 패키지에서 항목을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="69a64-195">하드 코딩 된 경로일 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="69a64-196">경로를 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-196">Convert the path.</span></span>

<span data-ttu-id="69a64-197">**참고**  기능을 활용 해야 하는 중요 한 응용 프로그램 또는 응용 프로그램을 변환 하는 데 App-v 5.1 sequencer를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="69a64-198">[앱-V 5.1를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법을](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69a64-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="69a64-199">변환 후 변환 된 패키지가 열리지 않는 경우 App-v 5.1 sequencer를 사용 하 여 응용 프로그램을 다시 시퀀싱 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="69a64-200">이전 버전의 App-V에서 만든 패키지를 변환하는 방법</span><span class="sxs-lookup"><span data-stu-id="69a64-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="69a64-201">클라이언트 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="69a64-201">Migrating Clients</span></span>


<span data-ttu-id="69a64-202">다음 표에서는 클라이언트 업그레이드에 권장 되는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a64-203">작업</span><span class="sxs-lookup"><span data-stu-id="69a64-203">Task</span></span></th>
<th align="left"><span data-ttu-id="69a64-204">추가 정보</span><span class="sxs-lookup"><span data-stu-id="69a64-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-205">환경을 최신 버전의 App-V 4.6으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="69a64-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="69a64-206">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</span><span class="sxs-lookup"><span data-stu-id="69a64-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a64-207">공존을 사용 하도록 설정 된 App-v 5.1 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="69a64-208">앱-V 4.6 및 App-v 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법을 설명 </a> 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-209">앱-V 5.1 패키지 순서 및 롤아웃</span><span class="sxs-lookup"><span data-stu-id="69a64-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="69a64-210">필요에 따라 App-v 4.6 패키지의 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="69a64-211">앱-V 5.1를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법 </a></span><span class="sxs-lookup"><span data-stu-id="69a64-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="69a64-212">**중요**  공존 모드를 사용 하려면 최신 버전의 App-V 4.6을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="69a64-213">또한 패키지를 시퀀싱 하는 경우 **사용자 구성 섹션** **에 설정** 되어 있는 관리 권한 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="69a64-214">App-v 5.1 서버 전체 인프라 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="69a64-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="69a64-215">전체 App-v 5.1 인프라로 업그레이드 하는 직접적인 방법은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="69a64-216">App-v server를 업그레이드 하는 방법에 대 한 자세한 내용은 다음 섹션의 정보를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="69a64-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a64-217">작업</span><span class="sxs-lookup"><span data-stu-id="69a64-217">Task</span></span></th>
<th align="left"><span data-ttu-id="69a64-218">추가 정보</span><span class="sxs-lookup"><span data-stu-id="69a64-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-219">환경을 최신 버전인 App-v 4.6으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="69a64-220">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</span><span class="sxs-lookup"><span data-stu-id="69a64-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a64-221">앱-V 5.1 버전의 클라이언트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="69a64-222">App-v 클라이언트를 배포 하는 방법 </a></span><span class="sxs-lookup"><span data-stu-id="69a64-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a64-223">App-v 5.1 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="69a64-224">App-v 5.1 서버를 배포 하는 방법 </a></span><span class="sxs-lookup"><span data-stu-id="69a64-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a64-225">기존 패키지 마이그레이션.</span><span class="sxs-lookup"><span data-stu-id="69a64-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a64-226"><strong>이 문서의 이전 버전의 app-v 섹션을 사용 하 여 만든 패키지 변환을 참조 하세요 </strong> .</span><span class="sxs-lookup"><span data-stu-id="69a64-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="69a64-227">추가 마이그레이션 작업</span><span class="sxs-lookup"><span data-stu-id="69a64-227">Additional Migration tasks</span></span>


<span data-ttu-id="69a64-228">또한 끝점 재구성, 그리고 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 이전 버전을 사용 하 여 만든 패키지를 여는 등의 추가 마이그레이션 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="69a64-229">다음 링크는 이러한 작업을 수행 하는 방법에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="69a64-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="69a64-230">특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.1 패키지로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="69a64-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="69a64-231">특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.1로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="69a64-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="69a64-232">특정 컴퓨터의 모든 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="69a64-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="69a64-233">특정 사용자에 대해 App-V 5.1 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="69a64-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="69a64-234">앱-V 마이그레이션 작업을 수행 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="69a64-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="69a64-235">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="69a64-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="69a64-236">간단한 Microsoft App-v 5.1 관리 서버 업그레이드 절차</span><span class="sxs-lookup"><span data-stu-id="69a64-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





