---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819378"
---
# <span data-ttu-id="45722-103">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="45722-103">CONFIGURE APP</span></span>


<span data-ttu-id="45722-104">사용자가 응용 프로그램에 연결 된 아이콘을 변경할 수 있지만 기존 바로 가기 또는 파일 형식 연결에서는 아이콘을 업데이트 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45722-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45722-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="45722-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="45722-106">설명</span><span class="sxs-lookup"><span data-stu-id="45722-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45722-107">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="45722-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="45722-108">응용 프로그램의 이름 및 버전 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="45722-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45722-109">/아이콘 &lt; 아이콘-pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="45722-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="45722-110">아이콘 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="45722-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45722-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="45722-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="45722-112">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45722-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45722-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="45722-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="45722-114">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="45722-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45722-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="45722-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="45722-116">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45722-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="45722-117">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="45722-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45722-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="45722-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="45722-119">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45722-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="45722-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="45722-120">Related topics</span></span>


[<span data-ttu-id="45722-121">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="45722-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





