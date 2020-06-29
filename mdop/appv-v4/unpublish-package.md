---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815133"
---
# <span data-ttu-id="06cf3-103">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="06cf3-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="06cf3-104">전체 패키지에 대 한 바로 가기 및 파일 형식을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="06cf3-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="06cf3-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="06cf3-106">설명</span><span class="sxs-lookup"><span data-stu-id="06cf3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="06cf3-107">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="06cf3-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-108">패키지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="06cf3-109">/CLEAR</span><span class="sxs-lookup"><span data-stu-id="06cf3-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-110">표시 되 면 사용자 설정도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="06cf3-111">(자세한 내용은이 항목의 뒷부분에 있는 중요 참고를 참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="06cf3-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="06cf3-112">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="06cf3-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-113">있는 경우 패키지가이 컴퓨터의 모든 사용자에 대해 게시 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="06cf3-114">/LOG</span><span class="sxs-lookup"><span data-stu-id="06cf3-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-115">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="06cf3-116">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="06cf3-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-117">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="06cf3-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="06cf3-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="06cf3-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-119">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="06cf3-120">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="06cf3-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="06cf3-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="06cf3-122">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="06cf3-123">**중요**  **패키지 게시 취소** 명령을 실행 하려면 패키지가 Application Virtualization 클라이언트에 이미 추가 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="06cf3-124">**전역**을 사용 하려면 **게시 취소 패키지가** 로컬 관리자로 실행 되어야 합니다. 그렇지 않으면 **Clearapp** 권한만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="06cf3-125">**게시 취소 패키지** 를 사용 하 여 패키지의 모든 전역 파일 형식 및 바로 **가기를 제거 합니다** .</span><span class="sxs-lookup"><span data-stu-id="06cf3-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="06cf3-126">**CLEAR** 는 해당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="06cf3-127">**전역** 이 아닌 **패키지 게시 취소** 를 사용 하면 패키지의 사용자 바로 가기 키와 파일 형식이 제거 되 고, **CLEAR** 가 설정 된 경우 사용자의 컨텍스트 아래에 있는 백그라운드 로드도 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="06cf3-128">패키지 **게시 취소** 패키지를 **추가**, **편집**및 **게시**하기 위한 원본 ID로 사용 된 것과 동일한 패키지 이름 또는 GUID의 응용 프로그램에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="06cf3-129">**패키지 게시를 취소** 하면/clear 스위치 사용에 관계 없이 항상 모든 사용자 설정, 바로 가기 및 파일 형식이 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="06cf3-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="06cf3-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="06cf3-130">Related topics</span></span>


[<span data-ttu-id="06cf3-131">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="06cf3-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





