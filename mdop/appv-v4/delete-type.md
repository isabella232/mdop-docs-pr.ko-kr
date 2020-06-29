---
title: DELETE TYPE
description: DELETE TYPE
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821688"
---
# <span data-ttu-id="a4d2d-103">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="a4d2d-103">DELETE TYPE</span></span>


<span data-ttu-id="a4d2d-104">지정 된 파일 형식 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a4d2d-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a4d2d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a4d2d-106">설명</span><span class="sxs-lookup"><span data-stu-id="a4d2d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4d2d-107">유형: &lt; 파일 확장명&gt;</span><span class="sxs-lookup"><span data-stu-id="a4d2d-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4d2d-108">제거할 파일 이름 확장명입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a4d2d-109">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="a4d2d-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4d2d-110">지정 하는 경우 파일 이름 확장명에 대 한 전역 연결을 제거 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4d2d-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="a4d2d-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4d2d-112">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a4d2d-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="a4d2d-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4d2d-114">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="a4d2d-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4d2d-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="a4d2d-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4d2d-116">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a4d2d-117">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4d2d-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a4d2d-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4d2d-119">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2d-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a4d2d-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="a4d2d-120">Related topics</span></span>


[<span data-ttu-id="a4d2d-121">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="a4d2d-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





