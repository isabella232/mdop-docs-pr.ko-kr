---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816238"
---
# <span data-ttu-id="444ac-103">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="444ac-103">LOAD PACKAGE</span></span>


<span data-ttu-id="444ac-104">지정 된 패키지를 파일 시스템 캐시에 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="444ac-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="444ac-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="444ac-106">설명</span><span class="sxs-lookup"><span data-stu-id="444ac-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="444ac-107">패키지: &lt; 패키지 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="444ac-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="444ac-108">로드할 패키지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="444ac-109">/SFTPATH &lt; sft-경로 이름&gt;</span><span class="sxs-lookup"><span data-stu-id="444ac-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="444ac-110">지정 되는 경우 로드할 SFT 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="444ac-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="444ac-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="444ac-112">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="444ac-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="444ac-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="444ac-114">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="444ac-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="444ac-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="444ac-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="444ac-116">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="444ac-117">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="444ac-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="444ac-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="444ac-119">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="444ac-120">**참고**  SFTPATH가 지정 되지 않은 경우 클라이언트는 OSD 파일, ApplicationSourceRoot 레지스트리 키 값 또는 OverrideURL 설정을 기반으로 사용 하도록 구성 된 경로를 사용 하 여 패키지를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="444ac-121">**패키지 로드** 명령은 동기 로드를 수행 하며 패키지가 완전히 로드 되거나 오류 조건이 발생할 때까지 완료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="444ac-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="444ac-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="444ac-122">Related topics</span></span>


[<span data-ttu-id="444ac-123">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="444ac-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





