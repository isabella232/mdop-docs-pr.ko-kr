---
title: UNLOCK APP
description: UNLOCK APP
author: dansimp
ms.assetid: 91fc8ceb-b4f5-4a06-8193-05189f830943
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ea47191450014856b4a9823728e3e275c7fb4cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815143"
---
# <span data-ttu-id="980bf-103">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="980bf-103">UNLOCK APP</span></span>


<span data-ttu-id="980bf-104">파일 시스템 캐시에 지정 된 응용 프로그램의 잠금을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="980bf-104">Unlocks the application specified in the file system cache.</span></span>

`SFTMIME UNLOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="980bf-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="980bf-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="980bf-106">설명</span><span class="sxs-lookup"><span data-stu-id="980bf-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="980bf-107">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="980bf-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="980bf-108">잠금을 해제할 응용 프로그램의 이름과 버전 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="980bf-108">The name and version (optional) of the application to unlock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="980bf-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="980bf-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="980bf-110">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="980bf-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="980bf-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="980bf-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="980bf-112">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="980bf-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="980bf-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="980bf-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="980bf-114">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="980bf-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="980bf-115">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="980bf-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="980bf-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="980bf-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="980bf-117">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="980bf-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="980bf-118">관련 항목</span><span class="sxs-lookup"><span data-stu-id="980bf-118">Related topics</span></span>


[<span data-ttu-id="980bf-119">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="980bf-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





