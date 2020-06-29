---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819898"
---
# <span data-ttu-id="b065b-103">ADD APP</span><span class="sxs-lookup"><span data-stu-id="b065b-103">ADD APP</span></span>


<span data-ttu-id="b065b-104">응용 프로그램 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b065b-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b065b-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b065b-106">설명</span><span class="sxs-lookup"><span data-stu-id="b065b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b065b-107">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="b065b-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-108">응용 프로그램의 이름 및 버전 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b065b-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b065b-109">/OSD &lt; osd-pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="b065b-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-110">OSD 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b065b-111">/아이콘 &lt; 아이콘-pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="b065b-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-112">아이콘 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b065b-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="b065b-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-114">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b065b-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="b065b-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-116">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="b065b-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b065b-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="b065b-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-118">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b065b-119">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b065b-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b065b-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b065b-121">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b065b-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b065b-122">**참고**  응용 프로그램의 결과 이름은 앱: 응용 프로그램에 제공 된 이름이 아니라 OSD 파일에서 가져옵니다 &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="b065b-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="b065b-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b065b-123">Related topics</span></span>


[<span data-ttu-id="b065b-124">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="b065b-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





