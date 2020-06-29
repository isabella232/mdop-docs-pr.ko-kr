---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819348"
---
# <span data-ttu-id="47c75-103">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="47c75-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="47c75-104">사용자가 패키지 매니페스트 파일, 패키지 원본, 로드 트리거 형식 또는 패키지에 대 한 로드 대상을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47c75-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="47c75-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="47c75-106">설명</span><span class="sxs-lookup"><span data-stu-id="47c75-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-107">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="47c75-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-108">패키지에 대해 사용자에 게 표시 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-109">/PMANIFEST &lt; 매니페스트-경로&gt;</span><span class="sxs-lookup"><span data-stu-id="47c75-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-110">패키지에 포함 된 응용 프로그램과 모든 게시 정보를 나열 하는 매니페스트 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-111">/OVERRIDEURL &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="47c75-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-112">패키지의 SFT 파일 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="47c75-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-114">패키지에 대해 백그라운드 로드가 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="47c75-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-116">게시 새로 고침 후 백그라운드 로드를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="47c75-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-118">사용자가 로그인 할 때 백그라운드 로드가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="47c75-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-120">백그라운드 로드는 사용자가 패키지에서 응용 프로그램을 시작한 후 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-121">/AUTOLOADTARGET &lt; 대상&gt;</span><span class="sxs-lookup"><span data-stu-id="47c75-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-122">패키지에서 자동으로 로드 되는 응용 프로그램을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-123">않아야</span><span class="sxs-lookup"><span data-stu-id="47c75-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-124">/AUTOLOADONxxx 플래그에 관계 없이 autoloading 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-125">모든</span><span class="sxs-lookup"><span data-stu-id="47c75-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-126">Autoload trigger를 사용 하는 경우 패키지의 모든 응용 프로그램이 실행 되었는지 여부에 관계 없이 캐시로 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="47c75-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-128">Autoload trigger를 사용 하는 경우 이전에 사용자가이 패키지의 응용 프로그램을 시작한 경우 패키지가 로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-129">/LOG</span><span class="sxs-lookup"><span data-stu-id="47c75-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-130">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-131">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="47c75-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-132">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="47c75-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="47c75-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-134">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="47c75-135">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="47c75-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-137">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="47c75-138">버전 4.6 SP2의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47c75-139">[/NO-UPDATE-FTA-SHORTCUT 가기 {TRUE | FALSE} {/GLOBAL}]</span><span class="sxs-lookup"><span data-stu-id="47c75-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-140">TRUE로 설정 하는 경우 사용자 당 또는/TGLOBAL 플래그가 지정 된 경우 패키지에 대 한 레지스트리 값이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="47c75-141">FALSE로 설정 되 면 레지스트리 값이 제거 되 고 패키지에 대 한 파일 형식 연결 (FTA)이 다시 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="47c75-142">지정 하지 않으면 일반 FTA 및 바로 가기 게시 동작이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="47c75-143">App-v 4.6 SP2 클라이언트에서 이후 게시 새로 고침 작업을 수행 하는 경우이 레지스트리 값이 설정 된 패키지에 대 한 바로 가기 및 FTAs 변경 되지 않으며, 플래그를 다시 설정 하지 않는 한 시스템 시작 또는 사용자 로그인에서 바로 가기 및 FTAs가 등록 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47c75-144">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="47c75-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="47c75-145">/NO-UPDATE-FTA-SHORTCUT 가기 플래그와 함께 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="47c75-146">/GLOBAL 플래그가 있으면 모든 사용자에 대해 해당 패키지에 대 한 레지스트리 값이 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="47c75-147">기본적으로이 사용자에 대해서만 레지스트리 값이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="47c75-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="47c75-148">관련 항목</span><span class="sxs-lookup"><span data-stu-id="47c75-148">Related topics</span></span>


[<span data-ttu-id="47c75-149">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="47c75-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





