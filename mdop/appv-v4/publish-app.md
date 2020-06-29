---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815818"
---
# <span data-ttu-id="a470c-103">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="a470c-103">PUBLISH APP</span></span>


<span data-ttu-id="a470c-104">사용자의 시작 메뉴, 바탕 화면 또는 기타 지정 된 위치에 응용 프로그램 바로 가기를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a470c-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a470c-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a470c-106">설명</span><span class="sxs-lookup"><span data-stu-id="a470c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a470c-107">응용 프로그램: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="a470c-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-108">응용 프로그램의 이름 및 버전 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="a470c-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a470c-109">/DESKTOP</span><span class="sxs-lookup"><span data-stu-id="a470c-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-110">사용자의 바탕 화면에 바로 가기를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a470c-111">/START</span><span class="sxs-lookup"><span data-stu-id="a470c-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-112">시작 메뉴의 프로그램 폴더에 있는 Application Virtualization 응용 프로그램 폴더에 대 한 바로 가기를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a470c-113">/TARGET &lt; 대상 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="a470c-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-114">바로 가기를 게시할 절대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a470c-115">/아이콘 &lt; 아이콘-pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="a470c-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-116">아이콘 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a470c-117">/DISPLAY &lt; 표시 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="a470c-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-118">바로 가기의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a470c-119">/인수 &lt; 명령-인수&gt;</span><span class="sxs-lookup"><span data-stu-id="a470c-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-120">매개 변수를 응용 프로그램에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a470c-121">/LOG</span><span class="sxs-lookup"><span data-stu-id="a470c-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-122">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a470c-123">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="a470c-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-124">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="a470c-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a470c-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="a470c-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-126">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a470c-127">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a470c-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a470c-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a470c-129">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a470c-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a470c-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a470c-130">Related topics</span></span>


[<span data-ttu-id="a470c-131">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="a470c-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





