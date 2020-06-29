---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822383"
---
# <span data-ttu-id="75145-103">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="75145-103">ADD TYPE</span></span>


<span data-ttu-id="75145-104">지정 된 파일 형식 연결을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="75145-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="75145-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="75145-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="75145-106">설명</span><span class="sxs-lookup"><span data-stu-id="75145-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-107">유형: &lt; 파일 확장명&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-108">지정 된 응용 프로그램과 연결 되는 파일 이름 확장명입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-109">/APP &lt; 응용 프로그램&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-110">응용 프로그램의 이름 및 버전 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="75145-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-111">/아이콘 &lt; 아이콘-pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-112">아이콘 파일의 경로 또는 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-113">/설명 &lt; 형식-desc&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-114">파일 형식에 대 한 사용자에 게 친숙 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="75145-115">&quot;확장명 파일이 기본값으로 설정 됩니다.&quot;</span><span class="sxs-lookup"><span data-stu-id="75145-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-116">/CONTENT-TYPE &lt; 콘텐츠-형식&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-117">파일의 콘텐츠 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-117">The content type of the file.</span></span> <span data-ttu-id="75145-118">기본적으로 &quot; application/softricity를 확장 합니다.&quot;</span><span class="sxs-lookup"><span data-stu-id="75145-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-119">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="75145-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-120">설치 되어 있는 경우이 컴퓨터의 모든 사용자가 패키지를 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75145-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-121">/PERCEIVED-TYPE &lt; 인식 형&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-122">파일의 인식 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-122">The perceived type of the file.</span></span> <span data-ttu-id="75145-123">기본적으로 없음이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75145-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-124">/PROGID &lt; progid&gt;</span><span class="sxs-lookup"><span data-stu-id="75145-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-125">파일 형식에 대 한 프로그래밍 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="75145-126">기본적으로 App Virt.</span><span class="sxs-lookup"><span data-stu-id="75145-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="75145-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-128">이 형식의 파일을 다운로드 하는 사용자에 게 파일을 열지 아니면 저장할지 묻는 메시지가 표시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75145-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="75145-129">기본값은 YES입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="75145-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-131">사용자가 모든 확장을 숨기도록 요청한 경우에도 파일의 확장명을 항상 표시할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75145-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="75145-132">기본값은 NO입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="75145-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-134">셸에서 새 메뉴에 항목을 추가할지 여부를 나타냅니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="75145-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="75145-135">기본값은 NO입니다.</span><span class="sxs-lookup"><span data-stu-id="75145-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-136">/LOG</span><span class="sxs-lookup"><span data-stu-id="75145-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-137">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75145-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-138">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="75145-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-139">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="75145-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="75145-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="75145-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-141">지정 된 경우 Windows 대화 상자에 출력이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75145-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="75145-142">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="75145-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="75145-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="75145-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="75145-144">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75145-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="75145-145">관련 항목</span><span class="sxs-lookup"><span data-stu-id="75145-145">Related topics</span></span>


[<span data-ttu-id="75145-146">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="75145-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





