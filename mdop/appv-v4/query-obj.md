---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815738"
---
# <span data-ttu-id="ffaa6-103">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="ffaa6-103">QUERY OBJ</span></span>


<span data-ttu-id="ffaa6-104">현재 응용 프로그램, 패키지, 파일 형식 연결 또는 게시 서버의 탭으로 구분 된 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ffaa6-105">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ffaa6-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="ffaa6-106">설명</span><span class="sxs-lookup"><span data-stu-id="ffaa6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffaa6-107">내</span><span class="sxs-lookup"><span data-stu-id="ffaa6-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-108">응용 프로그램 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffaa6-109">패키지할</span><span class="sxs-lookup"><span data-stu-id="ffaa6-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-110">패키지 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffaa6-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="ffaa6-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-112">파일 형식 연결 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffaa6-113">SERVER</span><span class="sxs-lookup"><span data-stu-id="ffaa6-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-114">게시 서버 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffaa6-115">/간단히</span><span class="sxs-lookup"><span data-stu-id="ffaa6-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-116">각에 대 한 전체 속성을 표시 하지 않고 응용 프로그램 이름, 패키지, 연결 또는 서버 이름 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffaa6-117">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="ffaa6-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-118">응용 프로그램의 경우 현재 사용자가 액세스할 수 있는 모든 알려진 응용 프로그램을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="ffaa6-119">패키지의 경우 현재 사용자가 액세스할 수 있는 패키지를 제외한 모든 알려진 패키지만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="ffaa6-120">연결에 대해 사용자가 아닌 모든 사용자에 게 적용 되는 연결만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="ffaa6-121">서버에 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffaa6-122">/LOG</span><span class="sxs-lookup"><span data-stu-id="ffaa6-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-123">지정 된 경우 출력이 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffaa6-124">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="ffaa6-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-125">지정 된 경우 출력이 활성 콘솔 창에 표시 됩니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="ffaa6-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ffaa6-126">버전 4.6의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffaa6-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="ffaa6-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-128">지정 된 경우 출력이 유니코드 형식의 지정 된 경로 이름에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ffaa6-129">**참고**  버전 4.6에서 SFTMIME 쿼리 OBJ: APP \ [/GLOBAL\]의 출력에 새 열이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="ffaa6-130">출력의 마지막 열은 응용 프로그램이 게시 되었는지 여부를 나타내는 숫자 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="ffaa6-131">게시 됨 = 1은 응용 프로그램을 게시 서버 새로 고침을 사용 하 여 응용 프로그램을 게시 한 후 Windows Installer 파일 (. MSI) 또는 패키지 매니페스트를 사용 하 여 SFTMIME 패키지 추가, 패키지 구성 또는 패키지 게시 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="ffaa6-132">게시 됨 = 0은 응용 프로그램이 게시 되지 않았거나 지우기 작업을 수행 하거나 SFTMIME 게시 취소 명령을 실행 하는 등의 결과로 더 이상 게시 되지 않았음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="ffaa6-133">/CGLOBAL 매개 변수를 사용 하는 경우 게시 된 상태는 전역으로 게시 된 응용 프로그램의 경우 1이 고, 사용자 컨텍스트에 게시 된 응용 프로그램에 대해서는 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="ffaa6-134">/GLOBAL 매개 변수가 없으면 명령을 실행 하는 사용자의 컨텍스트에서 게시 된 응용 프로그램에 대해 게시 된 상태 1이 반환 되 고, 전역으로 게시 되는 응용 프로그램에 대해 0 상태가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="ffaa6-135">SFTMIME 쿼리 OBJ 명령을 사용 하 여 위에 표시 된 모든 개체 (응용 프로그램, 패키지, 파일 형식 연결, 서버)에 대 한 정보를 쿼리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="ffaa6-136">일반 작업 작업에서 SFTMIME 쿼리 OBJ 명령을 사용 하는 방법을 표시 하려면 다음 예제에서는 특정 패키지에 대 한 OVERRIDEURL 매개 변수 값을 설정 하 여 패키지 콘텐츠의 새 경로를 지정 하려는 경우 수행할 프로세스를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="ffaa6-137">구성 하고자 하는 패키지를 찾으려면 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="ffaa6-138">이 명령은 검색 된 각 패키지 이름을 출력의 첫 번째 열에 GUID로 반환 합니다 (예: {AF78ABE1-57D4-4297-89DE-C308684AEDD6}).</span><span class="sxs-lookup"><span data-stu-id="ffaa6-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="ffaa6-139">OVERRIDEURL 매개 변수 값을 설정 하려면 SFTMIME [패키지 구성](configure-package.md) 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="ffaa6-140">예를 들어이 패키지에 대 한 OVERRIDEURL 값을 *\\\\server\\share\\mypackage.sft*값으로 설정 하려면 다음과 같이 SFTMIME 패키지 구성 명령을 사용 하 고, 1 단계에서 SFTMIME 쿼리 OBJ 명령의 출력에서 선택한 패키지 GUID를 지정 하 고, overrideurl 매개 변수와 새 값을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="ffaa6-141">버전 4.6 SP2의 경우 다음 옵션이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffaa6-142">/NO-UPDATE-FTA-SHORTCUT 가기</span><span class="sxs-lookup"><span data-stu-id="ffaa6-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffaa6-143">/NO-UPDATE-FTAI 바로 가기 플래그의 현재 상태를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ffaa6-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ffaa6-144">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ffaa6-144">Related topics</span></span>


[<span data-ttu-id="ffaa6-145">SFTMIME 명령 참조</span><span class="sxs-lookup"><span data-stu-id="ffaa6-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





