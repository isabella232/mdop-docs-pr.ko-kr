---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815148"
---
# <span data-ttu-id="96f98-103">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="96f98-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="96f98-104">파일 시스템 캐시에서 패키지를 언로드합니다.</span><span class="sxs-lookup"><span data-stu-id="96f98-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96f98-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="96f98-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="96f98-106">설명</span><span class="sxs-lookup"><span data-stu-id="96f98-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96f98-107">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="96f98-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="96f98-108">언로드할 패키지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96f98-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96f98-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="96f98-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="96f98-110">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96f98-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96f98-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="96f98-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="96f98-112">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="96f98-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96f98-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="96f98-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="96f98-114">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96f98-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="96f98-115">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="96f98-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96f98-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="96f98-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="96f98-117">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96f98-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="96f98-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="96f98-118">Related topics</span></span>


[<span data-ttu-id="96f98-119">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="96f98-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





