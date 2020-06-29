---
title: UNLOAD APP
description: UNLOAD APP
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815153"
---
# <span data-ttu-id="e961a-103">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="e961a-103">UNLOAD APP</span></span>


<span data-ttu-id="e961a-104">파일 시스템 캐시에서 응용 프로그램과 패키지의 다른 모든 응용 프로그램을 언로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e961a-104">Unloads the application and all other applications in the package from the file system cache.</span></span>

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e961a-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e961a-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e961a-106">설명</span><span class="sxs-lookup"><span data-stu-id="e961a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e961a-107">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="e961a-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e961a-108">언로드할 응용 프로그램의 이름 및 버전 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="e961a-108">The name and version (optional) of the application to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e961a-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="e961a-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="e961a-110">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e961a-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e961a-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="e961a-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="e961a-112">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="e961a-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e961a-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="e961a-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="e961a-114">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e961a-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e961a-115">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e961a-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e961a-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="e961a-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="e961a-117">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e961a-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e961a-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e961a-118">Related topics</span></span>


[<span data-ttu-id="e961a-119">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="e961a-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





