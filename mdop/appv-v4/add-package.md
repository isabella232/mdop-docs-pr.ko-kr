---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822398"
---
# <span data-ttu-id="732aa-103">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="732aa-103">ADD PACKAGE</span></span>


<span data-ttu-id="732aa-104">패키지 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-104">Adds a package record.</span></span> <span data-ttu-id="732aa-105">패키지가 이미 있는 경우이 명령을 통해 기존 패키지의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="732aa-106">매개 변수</span><span class="sxs-lookup"><span data-stu-id="732aa-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="732aa-107">설명</span><span class="sxs-lookup"><span data-stu-id="732aa-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-108">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="732aa-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-109">패키지에 대해 사용자에 게 표시 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-110">/PMANIFEST &lt; 매니페스트-경로&gt;</span><span class="sxs-lookup"><span data-stu-id="732aa-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-111">패키지에 포함 된 응용 프로그램과 모든 게시 정보를 나열 하는 매니페스트 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-112">/OVERRIDEURL &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="732aa-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-113">패키지의 SFT 파일 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="732aa-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-115">게시 새로 고침 후 백그라운드 로드를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="732aa-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-117">사용자가 로그인 할 때 백그라운드 로드가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="732aa-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-119">백그라운드 로드는 사용자가 패키지에서 응용 프로그램을 시작한 후 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-120">/AUTOLOADTARGET 대상</span><span class="sxs-lookup"><span data-stu-id="732aa-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-121">패키지에서 자동으로 로드 되는 응용 프로그램을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-122">않아야</span><span class="sxs-lookup"><span data-stu-id="732aa-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-123">/AUTOLOADONxxx 플래그에 관계 없이 autoloading 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-124">모든</span><span class="sxs-lookup"><span data-stu-id="732aa-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-125">Autoload trigger를 사용 하는 경우 패키지의 모든 응용 프로그램은 이전에 시작 되었는지 여부에 관계 없이 캐시로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="732aa-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-127">Autoload trigger를 사용 하는 경우 이전에 사용자가이 패키지의 응용 프로그램을 시작한 경우 패키지가 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-128">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="732aa-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-129">설치 되어 있는 경우이 컴퓨터의 모든 사용자가 패키지를 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-130">/LOG</span><span class="sxs-lookup"><span data-stu-id="732aa-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-131">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-132">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="732aa-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-133">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="732aa-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="732aa-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="732aa-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-135">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="732aa-136">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="732aa-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="732aa-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="732aa-138">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="732aa-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="732aa-139">관련 항목</span><span class="sxs-lookup"><span data-stu-id="732aa-139">Related topics</span></span>


[<span data-ttu-id="732aa-140">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="732aa-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





