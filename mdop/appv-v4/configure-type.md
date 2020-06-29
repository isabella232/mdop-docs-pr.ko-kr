---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821938"
---
# <span data-ttu-id="f5872-103">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="f5872-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="f5872-104">사용자가 파일 형식 연결에 대 한 설정을 변경할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5872-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5872-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f5872-106">설명</span><span class="sxs-lookup"><span data-stu-id="f5872-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-107">유형: &lt; 파일 확장명&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-108">구성할 파일 이름 확장명입니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-109">/APP &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-110">이 파일 형식을 연결할 응용 프로그램의 이름 및 버전 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="f5872-111">PROGID를 사용 하 여 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-112">/아이콘 &lt; 아이콘-pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-113">아이콘 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-114">/설명 &lt; 형식-desc&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-115">파일 형식에 대 한 사용자에 게 친숙 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-116">/CONTENT-TYPE &lt; 콘텐츠-형식&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-117">파일의 콘텐츠 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-118">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="f5872-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-119">있는 경우 모든 사용자에 게 적용 되는 연결을 편집 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-120">/PERCEIVED-TYPE &lt; 인식 형&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-121">파일의 인식 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-122">/PROGID &lt; progid&gt;</span><span class="sxs-lookup"><span data-stu-id="f5872-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-123">확장명을 다른 파일 형식과 연결 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="f5872-124">이전 파일 형식은 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-124">The previous file type is not deleted.</span></span> <span data-ttu-id="f5872-125">앱, 아이콘, 설명, CONFIRMOPEN 또는 SHOWEXT와 함께 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="f5872-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-127">이 형식의 파일을 다운로드 하는 사용자에 게 파일을 열지 아니면 저장할지 묻는 메시지가 표시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="f5872-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-129">사용자가 모든 확장을 숨기도록 요청한 경우에도 파일의 확장명을 항상 표시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="f5872-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-131">셸에서 새 메뉴에 항목을 추가할지 여부를 나타냅니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="f5872-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-132">/LOG</span><span class="sxs-lookup"><span data-stu-id="f5872-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-133">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-134">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="f5872-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-135">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="f5872-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5872-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="f5872-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-137">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f5872-138">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5872-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f5872-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5872-140">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5872-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f5872-141">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f5872-141">Related topics</span></span>


[<span data-ttu-id="f5872-142">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="f5872-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





