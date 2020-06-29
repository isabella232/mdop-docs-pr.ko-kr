---
title: LOCK APP
description: LOCK APP
author: dansimp
ms.assetid: 30673433-4364-499f-8116-cb135fe2716f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 319271640c2550fc94479e876a59b30d3b2bf7ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816243"
---
# <span data-ttu-id="08d6f-103">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="08d6f-103">LOCK APP</span></span>


<span data-ttu-id="08d6f-104">파일 시스템 캐시에 지정 된 응용 프로그램을 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="08d6f-104">Locks the application specified in the file system cache.</span></span>

`SFTMIME LOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08d6f-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="08d6f-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="08d6f-106">설명</span><span class="sxs-lookup"><span data-stu-id="08d6f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08d6f-107">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="08d6f-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="08d6f-108">잠글 응용 프로그램의 이름과 버전 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="08d6f-108">The name and version (optional) of the application to lock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08d6f-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="08d6f-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="08d6f-110">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08d6f-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08d6f-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="08d6f-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="08d6f-112">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="08d6f-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08d6f-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="08d6f-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="08d6f-114">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08d6f-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="08d6f-115">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="08d6f-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08d6f-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="08d6f-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="08d6f-117">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="08d6f-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="08d6f-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="08d6f-118">Related topics</span></span>


[<span data-ttu-id="08d6f-119">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="08d6f-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





