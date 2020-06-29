---
title: DELETE PACKAGE
description: DELETE PACKAGE
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821698"
---
# <span data-ttu-id="b2840-103">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="b2840-103">DELETE PACKAGE</span></span>


<span data-ttu-id="b2840-104">패키지 레코드 및 연결 된 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b2840-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2840-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b2840-106">설명</span><span class="sxs-lookup"><span data-stu-id="b2840-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2840-107">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="b2840-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2840-108">제거할 패키지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2840-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="b2840-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2840-110">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2840-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="b2840-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2840-112">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="b2840-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2840-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="b2840-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2840-114">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b2840-115">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2840-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b2840-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2840-117">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b2840-118">**중요**  패키지 삭제 명령은 항상 패키지의 전역 삭제를 수행 하 고 전역 파일 형식 및 바로 가기만 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="b2840-119">전역 패키지 인 경우이 명령은 로컬 관리자로 실행 되어야 합니다. 그렇지 않으면 **Deleteapp** 권한만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2840-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="b2840-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b2840-120">Related topics</span></span>


[<span data-ttu-id="b2840-121">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="b2840-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





