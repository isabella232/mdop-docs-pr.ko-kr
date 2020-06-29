---
title: DELETE OBJ
description: DELETE OBJ
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821703"
---
# <span data-ttu-id="a7a88-103">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="a7a88-103">DELETE OBJ</span></span>


<span data-ttu-id="a7a88-104">모든 응용 프로그램 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-104">Removes all of your application records.</span></span>

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7a88-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7a88-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a7a88-106">설명</span><span class="sxs-lookup"><span data-stu-id="a7a88-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7a88-107">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="a7a88-107">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7a88-108">지정 된 경우 모든 응용 프로그램이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-108">If specified, all applications are removed.</span></span> <span data-ttu-id="a7a88-109">기본적으로 현재 사용자가 액세스할 수 있는 응용 프로그램만 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-109">By default, only applications the current user has access to are removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7a88-110">/LOG</span><span class="sxs-lookup"><span data-stu-id="a7a88-110">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7a88-111">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-111">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7a88-112">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="a7a88-112">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7a88-113">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="a7a88-113">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7a88-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="a7a88-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7a88-115">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a7a88-116">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7a88-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a7a88-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7a88-118">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7a88-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a7a88-119">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a7a88-119">Related topics</span></span>


[<span data-ttu-id="a7a88-120">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="a7a88-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





