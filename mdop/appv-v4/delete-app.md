---
title: DELETE APP
description: DELETE APP
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821718"
---
# <span data-ttu-id="37a94-103">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="37a94-103">DELETE APP</span></span>


<span data-ttu-id="37a94-104">파일 시스템 캐시에서 응용 프로그램 레코드를 제거 하 여 더 이상 표시 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="37a94-105">사용자의 바로 가기 및 파일 형식 연결이 숨겨지며 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="37a94-106">사용자 설정은 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37a94-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="37a94-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="37a94-108">설명</span><span class="sxs-lookup"><span data-stu-id="37a94-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a94-109">앱: &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="37a94-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a94-110">제거할 응용 프로그램의 이름과 버전 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a94-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="37a94-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a94-112">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a94-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="37a94-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a94-114">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="37a94-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a94-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="37a94-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a94-116">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="37a94-117">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a94-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="37a94-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a94-119">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37a94-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="37a94-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="37a94-120">Related topics</span></span>


[<span data-ttu-id="37a94-121">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="37a94-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





