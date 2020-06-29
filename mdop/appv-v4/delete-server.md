---
title: DELETE SERVER
description: DELETE SERVER
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821693"
---
# <span data-ttu-id="3c473-103">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="3c473-103">DELETE SERVER</span></span>


<span data-ttu-id="3c473-104">게시 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-104">Removes a publishing server.</span></span>

<span data-ttu-id="3c473-105">**참고**  이 명령은 서버에서 클라이언트에 게시 하는 응용 프로그램 또는 패키지를 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="3c473-106">각 응용 프로그램에 대해 클라이언트에서 해당 응용 프로그램 및 패키지를 완전히 제거 하기 위해 SFTMIME **지우기 앱** 명령 다음에 **패키지 삭제** 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c473-107">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3c473-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3c473-108">설명</span><span class="sxs-lookup"><span data-stu-id="3c473-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c473-109">서버: &lt; 서버 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="3c473-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c473-110">게시 서버의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c473-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="3c473-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c473-112">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c473-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="3c473-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c473-114">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="3c473-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c473-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="3c473-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c473-116">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3c473-117">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c473-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3c473-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3c473-119">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c473-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3c473-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3c473-120">Related topics</span></span>


[<span data-ttu-id="3c473-121">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="3c473-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





