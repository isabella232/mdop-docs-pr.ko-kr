---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815813"
---
# <span data-ttu-id="4d8b8-103">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="4d8b8-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="4d8b8-104">전체 패키지의 콘텐츠를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4d8b8-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d8b8-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4d8b8-106">설명</span><span class="sxs-lookup"><span data-stu-id="4d8b8-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d8b8-107">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="4d8b8-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-108">패키지에 대해 사용자에 게 표시 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d8b8-109">/PMANIFEST &lt; 매니페스트-경로&gt;</span><span class="sxs-lookup"><span data-stu-id="4d8b8-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-110">패키지에 포함 된 응용 프로그램과 모든 게시 정보를 나열 하는 매니페스트 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d8b8-111">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="4d8b8-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-112">설치 되어 있는 경우이 컴퓨터의 모든 사용자가 패키지를 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d8b8-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="4d8b8-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-114">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d8b8-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4d8b8-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-116">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="4d8b8-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d8b8-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="4d8b8-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-118">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4d8b8-119">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d8b8-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4d8b8-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d8b8-121">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4d8b8-122">**중요**  패키지는 Application Virtualization 클라이언트에 이미 추가 되어 있어야 하 고 매니페스트 파일이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="4d8b8-123">**GLOBAL** 매개 변수를 사용 하려면 게시 패키지 명령을 로컬 관리자로 실행 해야 합니다. 그렇지 않으면 **ManageTypes** 및 # **바로 가기** 권한만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="4d8b8-124">**전역** 매개 변수 없이 게시 하면 패키지의 응용 프로그램에 대 한 액세스 권한이 사용자에 게 부여 되 고 매니페스트에 나열 된 파일 형식과 바로 가기가 사용자의 프로필에 게시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="4d8b8-125">**전역** 매개 변수를 사용 하 여 게시 하면 매니페스트에 나열 된 파일 형식과 바로 가기가 "모든 사용자" 프로필에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="4d8b8-126">호출이 시작 되기 전에 전역이 아니고 글로벌 매개 변수를 사용 **하는 경우** 에는 패키지가 전역으로 설정 되 고 모든 사용자가 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d8b8-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="4d8b8-127">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4d8b8-127">Related topics</span></span>


[<span data-ttu-id="4d8b8-128">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="4d8b8-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





