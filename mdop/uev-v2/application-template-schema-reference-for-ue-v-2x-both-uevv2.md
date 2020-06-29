---
title: UE-V 2. x에 대 한 응용 프로그램 템플릿 스키마 참조
description: UE-V 2. x에 대 한 응용 프로그램 템플릿 스키마 참조
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827408"
---
# <span data-ttu-id="db088-103">UE-V 2. x에 대 한 응용 프로그램 템플릿 스키마 참조</span><span class="sxs-lookup"><span data-stu-id="db088-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="db088-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1은 XML 설정 위치 템플릿을 사용 하 여 UE-V를 통해 캡처 및 적용 되는 데스크톱 응용 프로그램 설정 및 Windows 설정을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="db088-105">UE-V는 기본 설정 위치 템플릿 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="db088-106">UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="db088-107">고급 사용자는 설정 위치 템플릿의 XML 파일을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="db088-108">이 항목에서는 UE-V 2.1 (SP1) 및 2.0 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고 이러한 파일 편집을 위한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="db088-109">UE-V 2.1 및 2.1 SP1 응용 프로그램 템플릿 스키마 참조</span><span class="sxs-lookup"><span data-stu-id="db088-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="db088-110">이 섹션에서는 UE-V 2.1 및 2.1 SP1 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고이 파일 편집에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="db088-111">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="db088-111">In This Section</span></span>

-   [<span data-ttu-id="db088-112">XML 선언 및 인코딩 특성</span><span class="sxs-lookup"><span data-stu-id="db088-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="db088-113">네임 스페이스 및 루트 요소</span><span class="sxs-lookup"><span data-stu-id="db088-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="db088-114">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="db088-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="db088-115">Name 요소</span><span class="sxs-lookup"><span data-stu-id="db088-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="db088-116">ID 요소</span><span class="sxs-lookup"><span data-stu-id="db088-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="db088-117">버전 요소</span><span class="sxs-lookup"><span data-stu-id="db088-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="db088-118">Author 요소</span><span class="sxs-lookup"><span data-stu-id="db088-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="db088-119">프로세스 및 프로세스 요소</span><span class="sxs-lookup"><span data-stu-id="db088-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="db088-120">응용 프로그램 요소</span><span class="sxs-lookup"><span data-stu-id="db088-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="db088-121">공통 요소</span><span class="sxs-lookup"><span data-stu-id="db088-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="db088-122">SettingsLocationTemplate 요소</span><span class="sxs-lookup"><span data-stu-id="db088-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="db088-123">부록: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="db088-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="db088-124">XML 선언 및 인코딩 특성</span><span class="sxs-lookup"><span data-stu-id="db088-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="db088-125">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-125">Mandatory: True</span></span>**

**<span data-ttu-id="db088-126">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-126">Type: String</span></span>**

<span data-ttu-id="db088-127">XML 선언에서는 XML 버전 1.0 특성 ( &lt; ? XML 버전 = "1.0")을 지정 해야 합니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="db088-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="db088-128">UE-V 생성기에서 만든 설정 위치 템플릿은 해당 인코딩이 명시적으로 지정 되어 있지 않지만 UTF-8 인코딩으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="db088-129">이 요소에 encoding = "UTF-8" 특성을 가장 좋은 방법으로 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="db088-130">제품에 포함 된 모든 서식 파일은이 태그를 지정 합니다 (참조용%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\Templates 문서 참조).</span><span class="sxs-lookup"><span data-stu-id="db088-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="db088-131">예:</span><span class="sxs-lookup"><span data-stu-id="db088-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="db088-132">네임 스페이스 및 루트 요소</span><span class="sxs-lookup"><span data-stu-id="db088-132">Namespace and Root Element</span></span>

**<span data-ttu-id="db088-133">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-133">Mandatory: True</span></span>**

**<span data-ttu-id="db088-134">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-134">Type: String</span></span>**

<span data-ttu-id="db088-135">UE-V는 https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate 모든 응용 프로그램에 대 한 네임 스페이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="db088-136">SettingsLocationTemplate은 루트 요소 이며 다른 모든 요소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="db088-137">이 태그를 사용 하 여 모든 템플릿의 Reference SettingsLocationTemplate:</span><span class="sxs-lookup"><span data-stu-id="db088-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="db088-138">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="db088-138">Data types</span></span>

<span data-ttu-id="db088-139">다음은 UE-V 응용 프로그램 템플릿 스키마에 대 한 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="db088-140">**GUID** GUID는 "\\ {\ [a-fA-F0-9 \]-\ [a-fA-F0-9 \] 형식으로 된 표준 전역 고유 식별자 정규식을 설명 합니다. {8} {4} [a-Fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \\}".</span><span class="sxs-lookup"><span data-stu-id="db088-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="db088-141">Filesetting\\Root\\KnownFolder 요소에서 잘 알려진 폴더의 서식을 확인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="db088-142">**FilenameString** FilenameString는 모니터링할 프로세스의 파일 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="db088-143">해당 값은 regex \ [^ \\ \ \\? \ \ \ \* \ \ | &lt; &gt; 에 의해 제한 됩니다. /: \] +, (백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 문자를 포함 하지 않을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="db088-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="db088-144">**Idstring** IDString은 응용 프로그램 요소의 ID 값, SettingsLocationTemplate, 공통 요소 (공통 설정을 공유 하는 응용 프로그램 제품군을 설명 하는 데 사용 됨)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="db088-145">FilenameString (\\ [^ \\? \\ | &lt; &gt; )와 동일한 regex로 제한 됩니다. /:\]+).</span><span class="sxs-lookup"><span data-stu-id="db088-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="db088-146">**서식 버전** 서식 파일 버전은 설정 위치 템플릿의 수정을 설명 하는 데 사용 되는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="db088-147">값의 범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="db088-148">**비어 있음** Empty는 null 값을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="db088-149">이는 처리할 프로세스가 없다는 것을 나타내기 위해 Process\\ShellProcess에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="db088-150">이 값은 응용 프로그램 템플릿에서 사용해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="db088-151">**만든이** Author 데이터 형식은 서식 파일의 작성자를 식별 하는 복잡 한 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="db088-152">여기에는 **이름** 및 **전자 메일**이라는 두 개의 자식 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="db088-153">Author 데이터 형식 내에서 Name 요소는 필수 항목이 며 전자 메일 요소는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="db088-154">이 형식은 SettingsLocationTemplate 요소 아래에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="db088-155">**범위** 범위는 **최소** 및 **최대**의 두 자식 요소로 구성 된 integer 클래스를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="db088-156">이 데이터 형식은 ProcessVersion 데이터 형식에서 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="db088-157">지정 된 경우 최소 및 최대 값을 모두 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="db088-158">**Processversion** ProcessVersion은 **주**, **부**, **빌드**, **패치**등 네 가지 자식 요소를 사용 하 여 형식을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="db088-159">이 데이터 형식은 Process 요소에서 ProductVersion 및 FileVersion 값을 채우는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="db088-160">이 유형의 데이터는 범위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-160">The data for this type is a Range value.</span></span> <span data-ttu-id="db088-161">주요 자식 요소는 필수 이며 나머지는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="db088-162">**아키텍처가** 아키텍처에는 두 가지 가능 값 ( **Win32** 및 **Win64**)이 열거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="db088-163">이러한 값은 프로세스 아키텍처를 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="db088-164">**공정** 프로세스 데이터 형식은 UE-V를 통해 모니터링할 프로세스를 설명 하는 데 사용 되는 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="db088-165">여기에는 **파일 이름**, **아키텍처**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**의 여섯 가지 하위 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="db088-166">이 표에서는 각 요소의 해당 데이터 형식에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="db088-167">요소</span><span class="sxs-lookup"><span data-stu-id="db088-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="db088-168">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="db088-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="db088-169">Mandatory</span><span class="sxs-lookup"><span data-stu-id="db088-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-170">이름이</span><span class="sxs-lookup"><span data-stu-id="db088-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-171">FilenameString</span><span class="sxs-lookup"><span data-stu-id="db088-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-172">True</span><span class="sxs-lookup"><span data-stu-id="db088-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-173">아키텍처</span><span class="sxs-lookup"><span data-stu-id="db088-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-174">아키텍처</span><span class="sxs-lookup"><span data-stu-id="db088-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-175">False</span><span class="sxs-lookup"><span data-stu-id="db088-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="db088-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-177">문자열</span><span class="sxs-lookup"><span data-stu-id="db088-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-178">False</span><span class="sxs-lookup"><span data-stu-id="db088-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="db088-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-180">문자열</span><span class="sxs-lookup"><span data-stu-id="db088-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-181">False</span><span class="sxs-lookup"><span data-stu-id="db088-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="db088-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="db088-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-184">False</span><span class="sxs-lookup"><span data-stu-id="db088-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-185">FileVersion</span><span class="sxs-lookup"><span data-stu-id="db088-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="db088-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-187">False</span><span class="sxs-lookup"><span data-stu-id="db088-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="db088-188">**프로세스** 프로세스 데이터 형식은 하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="db088-189">프로세스 시퀀스 형식에서 처리 되는 두 개의 자식 요소에는 **process** 와 **shellprocess**지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="db088-190">프로세스는 유형 프로세스의 요소이 고 ShellProcess는 데이터 형식이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="db088-191">순서에서 하나 이상의 항목을 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="db088-192">**경로** RegistrySetting 및 FileSetting에서 Path를 사용 하 여 레지스트리와 파일 경로를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="db088-193">이 요소는 선택적 특성 두 개를 지원 합니다. **재귀** 및 **Deletfnota가 발견**되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="db088-194">두 값 모두 default = "False"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="db088-195">Recursive는 경로 및 모든 하위 폴더가 파일 설정에 포함 되거나 모든 하위 레지스트리 키가 레지스트리 설정에 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="db088-196">두 경우 모두 현재 수준의 모든 항목이 캡처한 데이터에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="db088-197">FileSettings 개체의 경우 지정 된 폴더 내의 모든 파일이 UE-V를 통해 캡처한 데이터에 포함 되지만 폴더는 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="db088-198">레지스트리 경로의 경우 현재 경로에 있는 모든 값이 캡처되고 자식 레지스트리 키가 캡처되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="db088-199">두 경우 모두 대규모 데이터 집합 또는 많은 수의 항목을 캡처하는 것을 방지 하기 위해 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="db088-200">DeleteIfNotFound 특성은 사용자의 설정 저장소 경로 데이터에서 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="db088-201">이는 패키지에서 이러한 설정을 제거 하 여 설정 저장소 경로 파일 서버에 많은 양의 디스크 공간이 저장 되는 경우에 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="db088-202">**FileMask** FileMask는 Path로 정의 된 폴더에 대 한 특정 파일 형식만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="db088-203">예를 들어 Path는 `C:\users\username\files` `*.txt` 텍스트 파일만 포함 하 고 FileMask 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="db088-204">**RegistrySetting** RegistrySetting는 레지스트리 키 및 값에 대 한 컨테이너와 UE-V 에이전트의 부분에 대 한 연결 된 원하는 동작을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="db088-205">**Path**, **Name**, **Exclude**, 값 **경로** 및 **이름의**시퀀스를 포함 하 여 네 개의 자식 요소가이 형식으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="db088-206">**Filesetting** FileSetting에는 파일 및 파일 경로와 연결 된 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="db088-207">**루트**, **경로**, **FileMask**및 **Exclude**의 네 가지 자식 요소가 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="db088-208">Root는 필수 이며 나머지는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="db088-209">**설정** 설정은 특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="db088-210">여기에는 앞에서 설명한 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="db088-211">또한 다음과 같은 동작이 포함 된 다음 자식 요소도 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="db088-212">요소</span><span class="sxs-lookup"><span data-stu-id="db088-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="db088-213">설명</span><span class="sxs-lookup"><span data-stu-id="db088-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-214">비동기</span><span class="sxs-lookup"><span data-stu-id="db088-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-215">비동기 설정 패키지는 응용 프로그램 시작을 차단 하지 않고 적용 되므로 설정이 계속 적용 되는 동안 응용 프로그램을 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="db088-216">이 방법은 SystemParameterSetting과 같이 API를 통해 비동기적으로 적용할 수 있는 설정에 유용 <code>get/set</code> 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="db088-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-218">기본적으로 UE-V는 템플릿을 사용 하는 응용 프로그램의 마지막 인스턴스가 닫혀 있을 때만 응용 프로그램에 대 한 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="db088-219">이 요소를 ' f l l e '로 설정 하면 UE-V가 응용 프로그램의 다른 인스턴스가 실행 되는 경우에도 설정을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="db088-220">적합 한 서식 파일 – UE-V를 사용 하 여 제공 되는 공용 요소 섹션이 포함 된 경우이 플래그를 사용 하 여 마지막 인스턴스가 닫힐 때까지 응용 프로그램 관련 설정이 내보내기 되지 않도록 하 여 응용 프로그램을 닫을 때 공유 설정을 항상 내보낼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="db088-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-222">(2.1에서 도입 되었습니다.)</span><span class="sxs-lookup"><span data-stu-id="db088-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="db088-223">이 매개 변수는 패키지와 응용 프로그램의 현재 상태 간에 차이점이 없는 경우에도 가져온 설정 패키지를 적용 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="db088-224">이 매개 변수는 설정 가져오기가 느려질 수 있으므로 특별 한 경우에만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="db088-225">Name 요소</span><span class="sxs-lookup"><span data-stu-id="db088-225">Name Element</span></span>

**<span data-ttu-id="db088-226">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-226">Mandatory: True</span></span>**

**<span data-ttu-id="db088-227">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-227">Type: String</span></span>**

<span data-ttu-id="db088-228">Name은 설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-229">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-230">일반적으로 버전 정보를 참조 하지 않도록 하는 것은 ProductVersion 요소와는 다른 것이 될 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="db088-231">예를 들어, `<Name>My Application</Name>` 대신를 지정 `<Name>My Application 1.1</Name>` 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="db088-232">**참고**  UE-V는 외부 Dtd를 참조 하지 않으므로 설정 위치 템플릿에서 명명 된 엔터티를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="db088-233">예를 들어 &reg; 등록 된 무역 표시 기호®를 참조 하는 데 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="db088-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="db088-234">대신 정식 번호 매기기 참조를 사용 하 여 이러한 유형의 특수 문자를 포함 합니다 (예:® 문자에 대 한 & \ #174).</span><span class="sxs-lookup"><span data-stu-id="db088-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="db088-235">이 규칙은이 문서의 모든 문자열 값에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="db088-236"><http://www.w3.org/TR/xhtml1/dtds.html>전체 문자 엔터티 목록을 보려면을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db088-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="db088-237">U t f-8로 인코딩된 문서에는 유니코드 문자가 직접 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="db088-238">UE-V 생성기를 통해 템플릿을 저장 하면 문자 엔터티가 해당 유니코드 표현으로 자동 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="db088-239">ID 요소</span><span class="sxs-lookup"><span data-stu-id="db088-239">ID Element</span></span>

**<span data-ttu-id="db088-240">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-240">Mandatory: True</span></span>**

**<span data-ttu-id="db088-241">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-241">Type: String</span></span>**

<span data-ttu-id="db088-242">ID는 특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-243">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다 (예: Get-help Evtemplate 및 가져오기-Uevtemplate 파일 프로그램 PowerShell cmdlet의 출력 참조).</span><span class="sxs-lookup"><span data-stu-id="db088-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="db088-244">규칙에 따라이 태그에는 모든 공백을 포함할 수 없으며 스크립팅이 간단해 집니다.</span><span class="sxs-lookup"><span data-stu-id="db088-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="db088-245">또는 등의 템플릿을 쉽게 식별할 수 있도록이 요소에 응용 프로그램의 버전 번호를 지정 해야 합니다 `<ID>MicrosoftCalculator6</ID>` `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="db088-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="db088-246">버전 요소</span><span class="sxs-lookup"><span data-stu-id="db088-246">Version Element</span></span>

**<span data-ttu-id="db088-247">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-247">Mandatory: True</span></span>**

**<span data-ttu-id="db088-248">유형: Integer</span><span class="sxs-lookup"><span data-stu-id="db088-248">Type: Integer</span></span>**

**<span data-ttu-id="db088-249">최 솟 값: 0</span><span class="sxs-lookup"><span data-stu-id="db088-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="db088-250">최 댓 값: 2147483647</span><span class="sxs-lookup"><span data-stu-id="db088-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="db088-251">버전은 변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="db088-252">UE-V 생성기는 템플릿이 저장 될 때마다이 번호를 하나씩 자동으로 증가 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="db088-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="db088-253">이 필드에 정수 (integer) 값이 있어야 합니다. 같은 소수 값 `<Version>2.5</Version>` 은 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="db088-254">**힌트:** 다음과 같은 XML 주석 태그를 사용 하 여 버전 변경에 대 한 노트를 저장할 수 있습니다 `<!-- -->` .</span><span class="sxs-lookup"><span data-stu-id="db088-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="db088-255">**중요**  이 값을 쿼리하여 다음 인스턴스의 기존 서식 파일에 새 버전의 서식 파일을 적용 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="db088-256">예약 된 서식 파일 자동 업데이트 작업이 실행 되는 경우</span><span class="sxs-lookup"><span data-stu-id="db088-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="db088-257">업데이트 UevTemplate PowerShell cmdlet이 실행 되는 경우</span><span class="sxs-lookup"><span data-stu-id="db088-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="db088-258">Microsoft\\uev: SettingsLocationTemplate Update 메서드가 WMI를 통해 호출 되는 경우</span><span class="sxs-lookup"><span data-stu-id="db088-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="db088-259">Author 요소</span><span class="sxs-lookup"><span data-stu-id="db088-259">Author Element</span></span>

**<span data-ttu-id="db088-260">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-260">Mandatory: False</span></span>**

**<span data-ttu-id="db088-261">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-261">Type: String</span></span>**

<span data-ttu-id="db088-262">만든이는 설정 위치 템플릿의 작성자를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="db088-263">**이름** 및 **전자 메일**이라는 두 개의 선택적 자식 요소가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="db088-264">두 특성은 모두 선택 사항 이지만, 전자 메일 자식 요소가 지정 된 경우 Name 요소와 함께 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="db088-265">만든이는 설정 위치 서식 파일에 대 한 연락처의 전체 이름을 나타내고, 전자 메일은 작성자의 전자 메일 주소를 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="db088-266">이 정보는 [Ue-v 템플릿 갤러리](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)와 같이 공개적으로 게시 된 서식 파일에 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="db088-267">프로세스 및 프로세스 요소</span><span class="sxs-lookup"><span data-stu-id="db088-267">Processes and Process Element</span></span>

**<span data-ttu-id="db088-268">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-268">Mandatory: True</span></span>**

**<span data-ttu-id="db088-269">Type: Element</span><span class="sxs-lookup"><span data-stu-id="db088-269">Type: Element</span></span>**

<span data-ttu-id="db088-270">프로세스에는 적어도 하나 이상의 요소가 포함 되어 `<Process>` 있으며, 여기에는 **Filename**, **Architecture**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**이라는 자식 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="db088-271">Filename 하위 요소는 필수 이며 나머지는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="db088-272">완전히 채워진 요소에는 다음 예제와 유사한 태그가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="db088-273">이름이</span><span class="sxs-lookup"><span data-stu-id="db088-273">Filename</span></span>

**<span data-ttu-id="db088-274">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-274">Mandatory: True</span></span>**

**<span data-ttu-id="db088-275">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-275">Type: String</span></span>**

<span data-ttu-id="db088-276">Filename은 파일 시스템에 표시 되는 실행 파일의 실제 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="db088-277">이 요소는 템플릿이 프로세스에 적용 되는지 여부를 평가 하기 위해 UE-V에서 사용 하는 기본 조건을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="db088-278">이 요소는 설정 위치 템플릿 XML에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="db088-279">올바른 파일 이름은 정규식 \ [^ \\? \ \? \ \ | &lt; &gt; 와 일치 하지 않아야 합니다. /: \] +, 즉 백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 (\\?)이 포함 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="db088-280">\* | &lt; &gt; /또는: 문자.</span><span class="sxs-lookup"><span data-stu-id="db088-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="db088-281">**힌트:** 이 정규식에 대해 문자열을 테스트 하려면 PowerShell 명령 창을 사용 하 여 **해당 파일 이름에 대 한**실행 파일의 이름을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="db088-282">**True** 값은 문자열에 잘못 된 문자가 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="db088-283">다음은 잘못 된 값의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="db088-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="db088-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="db088-285">프로그램 \ \* .exe</span><span class="sxs-lookup"><span data-stu-id="db088-285">Program\*.exe</span></span>

-   <span data-ttu-id="db088-286">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="db088-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="db088-287">프로그램 &lt; 1 &gt; .exe</span><span class="sxs-lookup"><span data-stu-id="db088-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="db088-288">**참고**  UE-V 생성기는 각각 문자 보다 크거나 작은 값을 &gt; &lt; 각각 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="db088-289">드문 경우 지만 FileName 값에 .exe 확장명을 포함할 필요는 없지만 값의 일부로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="db088-290">예를 들어을 `<Filename>MyApplictication.exe</Filename>` 대신 지정 해야 합니다 `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="db088-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="db088-291">두 번째 예제에서는 실행 파일의 실제 이름이 "MyApplication.exe" 인 경우 템플릿을 프로세스에 적용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="db088-292">아키텍처</span><span class="sxs-lookup"><span data-stu-id="db088-292">Architecture</span></span>

**<span data-ttu-id="db088-293">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-293">Mandatory: False</span></span>**

**<span data-ttu-id="db088-294">Type: Architecture (String)</span><span class="sxs-lookup"><span data-stu-id="db088-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="db088-295">아키텍처는 대상 실행 파일이 컴파일된 프로세서 아키텍처를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="db088-296">유효한 값은 32 비트 응용 프로그램 또는 64 비트 응용 프로그램의 Win64에 대 한 Win32입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="db088-297">있는 경우이 태그는 설정 위치 템플릿의 적용 가능성을 특정 응용 프로그램 아키텍처로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="db088-298">예를 들어%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\templates\\ MicrosoftOffice2010Win32.xml 및 UE-V와 함께 포함 된 MicrosoftOffice2010Win64.xml 파일을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="db088-299">이는 여러 버전의 실행 파일에 대 한 상대 경로가 변경 되거나 프로세서 아키텍처 간에 전환할 때 설정이 추가 또는 제거 된 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="db088-300">이 요소가 없으면 설정 위치 템플릿은 프로세스의 아키텍처를 무시 하 고 파일 이름과 기타 특성이 적용 되는 경우 32 및 64 비트 프로세스에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="db088-301">**참고**  UE-V는이 버전의 ARM 프로세서를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="db088-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="db088-302">ProductName</span></span>

**<span data-ttu-id="db088-303">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-303">Mandatory: False</span></span>**

**<span data-ttu-id="db088-304">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-304">Type: String</span></span>**

<span data-ttu-id="db088-305">ProductName은 관리 목적 또는 보고를 위해 제품을 식별 하는 데 사용 되는 선택적 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="db088-306">ProductName은 해당 값에 정규식 제한이 없다는 점에서 Filename과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="db088-307">이를 통해 실행 파일 이름이 명확 하지 않을 수 있는 프로세스에 대 한 보다 쉽게 이해 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="db088-308">예:</span><span class="sxs-lookup"><span data-stu-id="db088-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="db088-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="db088-309">FileDescription</span></span>

**<span data-ttu-id="db088-310">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-310">Mandatory: False</span></span>**

**<span data-ttu-id="db088-311">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-311">Type: String</span></span>**

<span data-ttu-id="db088-312">FileDescription은 실행 파일의 관리 설명을 허용 하는 선택적 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="db088-313">자유 텍스트 필드 이며, 실행 파일의 기능을 식별 해야 하는 소프트웨어 패키지 내에서 여러 실행 파일을 구분 하는 데 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="db088-314">예를 들어 적합 한 응용 프로그램에서는 다음과 같이 두 실행 파일 (MyApplication.exe 및 MyApplicationHelper.exe)의 함수에 대 한 미리 알림을 제공 하는 것이 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="db088-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="db088-315">ProductVersion</span></span>

**<span data-ttu-id="db088-316">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-316">Mandatory: False</span></span>**

**<span data-ttu-id="db088-317">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-317">Type: String</span></span>**

<span data-ttu-id="db088-318">ProductVersion는 파일의 주 버전과 부 버전을 참조 하 고 빌드 및 패치 수준에도 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="db088-319">ProductVersion는 선택적 요소 이지만, 지정 하는 경우 적어도 주요 자식 요소를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="db088-320">값은 Minimum = "X" Maximum = "Y" 형식의 범위를 표현 해야 합니다. 여기서 X와 Y는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="db088-321">Minimum 및 Maximum 값은 동일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="db088-322">제품 및 파일 버전 요소는 지정 되지 않은 상태로 남아 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="db088-323">이렇게 하면 서식 파일을 "버전에 맞게 표시" 하 여 템플릿이 지정 된 실행 파일의 모든 버전에 적용 되는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="db088-324">예 1:</span><span class="sxs-lookup"><span data-stu-id="db088-324">Example 1:</span></span>**

<span data-ttu-id="db088-325">UE-V 생성기에 지정 된 제품 버전: 1.0는 다음과 같은 XML을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="db088-326">예 2:</span><span class="sxs-lookup"><span data-stu-id="db088-326">Example 2:</span></span>**

<span data-ttu-id="db088-327">파일 버전: UE-V 생성기에 지정 된 5.0.2.1000는 다음과 같은 XML을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="db088-328">잘못 된 예제 1-완전 하지 않은 범위:</span><span class="sxs-lookup"><span data-stu-id="db088-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="db088-329">최소 특성만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="db088-330">범위에도 Maximum을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="db088-331">잘못 된 예제 2 – 주요 요소 없이 Minor가 지정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="db088-332">Minor 요소만 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-332">Only the Minor element is present.</span></span> <span data-ttu-id="db088-333">주 버전도 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="db088-334">FileVersion</span><span class="sxs-lookup"><span data-stu-id="db088-334">FileVersion</span></span>

**<span data-ttu-id="db088-335">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-335">Mandatory: False</span></span>**

**<span data-ttu-id="db088-336">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-336">Type: String</span></span>**

<span data-ttu-id="db088-337">FileVersion은 게시 된 응용 프로그램의 릴리스 버전과 구성 요소 실행 파일의 내부 빌드 세부 정보를 구별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="db088-338">대부분의 상업용 응용 프로그램의 경우 이러한 번호는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="db088-339">변경 되는 파일의 제품 버전은 파일의 일반 버전 식별을 나타내고, 파일 버전은 파일의 특정 빌드를 나타냅니다 (핫픽스나 업데이트의 경우).</span><span class="sxs-lookup"><span data-stu-id="db088-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="db088-340">이렇게 하면 검색 논리가 손상 되지 않은 파일을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="db088-341">제품 버전과 특정 실행 파일 버전을 확인 하려면 Windows 탐색기에서 파일을 마우스 오른쪽 단추로 클릭 하 고 속성을 선택한 다음 세부 정보 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="db088-342">응용 프로그램에 FileVersion 요소를 포함 하면 더 세밀 하 게 조정할 수 있지만, 대부분의 응용 프로그램에서는 이러한 검색 논리가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="db088-343">ProductVersion 요소 설정이 먼저 검사 되 고 FileVersion이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="db088-344">더 제한적인 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="db088-345">FileVersion의 자식 요소 및 구문 규칙은 ProductVersion와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="db088-346">응용 프로그램 요소</span><span class="sxs-lookup"><span data-stu-id="db088-346">Application Element</span></span>

<span data-ttu-id="db088-347">응용 프로그램은 특정 응용 프로그램에 적용 되는 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="db088-348">다음 필드/형식의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="db088-349">필드/형식</span><span class="sxs-lookup"><span data-stu-id="db088-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="db088-350">설명</span><span class="sxs-lookup"><span data-stu-id="db088-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-351">이름</span><span class="sxs-lookup"><span data-stu-id="db088-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-352">설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-353">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-354">자세한 내용은 Name을 참조 <a href="#name21" data-raw-source="[Name](#name21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-355">ID</span><span class="sxs-lookup"><span data-stu-id="db088-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-356">특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-357">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="db088-358">자세한 내용은 ID를 참조 <a href="#id21" data-raw-source="[ID](#id21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-359">설명</span><span class="sxs-lookup"><span data-stu-id="db088-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-360">서식 파일에 대 한 설명입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="db088-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-361">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="db088-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-362">UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="db088-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-364">언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-365">버전</span><span class="sxs-lookup"><span data-stu-id="db088-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-366">변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="db088-367">자세한 내용은 버전을 참조 <a href="#version21" data-raw-source="[Version](#version21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="db088-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-369">이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="db088-370">컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="db088-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-372">MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="db088-373">설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-374">FixedProfile (2.1에서 도입 된)</span><span class="sxs-lookup"><span data-stu-id="db088-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-375">이 템플릿을이 요소에 지정 된 프로필에만 연결할 수 있으며 WMI 또는 PowerShell을 통해 변경할 수 없음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-376">프로세스</span><span class="sxs-lookup"><span data-stu-id="db088-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-377">하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="db088-378">자세한 내용은 프로세스를 참조 <a href="#processes21" data-raw-source="[Processes](#processes21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-379">설정</span><span class="sxs-lookup"><span data-stu-id="db088-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-380">특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="db088-381">여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="db088-382">자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data21" data-raw-source="[Data types](#data21)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="db088-383">공통 요소</span><span class="sxs-lookup"><span data-stu-id="db088-383">Common Element</span></span>

<span data-ttu-id="db088-384">일반적으로 응용 프로그램 요소와 유사 하지만 항상 둘 이상의 응용 프로그램 요소와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="db088-385">공용 섹션은 해당 응용 프로그램 인스턴스 간에 공유 되는 설정 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="db088-386">다음 필드/형식의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="db088-387">필드/형식</span><span class="sxs-lookup"><span data-stu-id="db088-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="db088-388">설명</span><span class="sxs-lookup"><span data-stu-id="db088-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-389">이름</span><span class="sxs-lookup"><span data-stu-id="db088-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-390">설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-391">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-392">자세한 내용은 Name을 참조 <a href="#name21" data-raw-source="[Name](#name21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-393">ID</span><span class="sxs-lookup"><span data-stu-id="db088-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-394">특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-395">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="db088-396">자세한 내용은 ID를 참조 <a href="#id21" data-raw-source="[ID](#id21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-397">설명</span><span class="sxs-lookup"><span data-stu-id="db088-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-398">서식 파일에 대 한 설명입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="db088-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-399">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="db088-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-400">UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="db088-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-402">언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-403">버전</span><span class="sxs-lookup"><span data-stu-id="db088-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-404">변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="db088-405">자세한 내용은 버전을 참조 <a href="#version21" data-raw-source="[Version](#version21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="db088-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-407">이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="db088-408">컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="db088-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-410">MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="db088-411">설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-412">FixedProfile (2.1에서 도입 된)</span><span class="sxs-lookup"><span data-stu-id="db088-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-413">이 템플릿을이 요소에 지정 된 프로필에만 연결할 수 있으며 WMI 또는 PowerShell을 통해 변경할 수 없음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-414">설정</span><span class="sxs-lookup"><span data-stu-id="db088-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-415">특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="db088-416">여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="db088-417">자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data21" data-raw-source="[Data types](#data21)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="db088-418">SettingsLocationTemplate 요소</span><span class="sxs-lookup"><span data-stu-id="db088-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="db088-419">이 요소는 단일 응용 프로그램 또는 응용 프로그램 집합에 대 한 설정을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="db088-420">필드/형식</span><span class="sxs-lookup"><span data-stu-id="db088-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="db088-421">설명</span><span class="sxs-lookup"><span data-stu-id="db088-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-422">이름</span><span class="sxs-lookup"><span data-stu-id="db088-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-423">설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-424">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-425">자세한 내용은 Name을 참조 <a href="#name21" data-raw-source="[Name](#name21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-426">ID</span><span class="sxs-lookup"><span data-stu-id="db088-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-427">특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-428">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="db088-429">자세한 내용은 ID를 참조 <a href="#id21" data-raw-source="[ID](#id21)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-430">설명</span><span class="sxs-lookup"><span data-stu-id="db088-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-431">서식 파일에 대 한 설명입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="db088-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-432">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="db088-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-433">UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="db088-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-435">언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="db088-436">부록: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="db088-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="db088-437">다음은 해당 요소, 자식 요소, 특성 및 매개 변수를 보여 주는 SettingsLocationTemplate .xsd 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="db088-438">UE-V 2.0 응용 프로그램 템플릿 스키마 참조</span><span class="sxs-lookup"><span data-stu-id="db088-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="db088-439">이 섹션에서는 UE-V 2.0 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고이 파일 편집에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="db088-440">이 섹션의 내용</span><span class="sxs-lookup"><span data-stu-id="db088-440">In This Section</span></span>

-   [<span data-ttu-id="db088-441">XML 선언 및 인코딩 특성</span><span class="sxs-lookup"><span data-stu-id="db088-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="db088-442">네임 스페이스 및 루트 요소</span><span class="sxs-lookup"><span data-stu-id="db088-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="db088-443">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="db088-443">Data types</span></span>](#data)

-   [<span data-ttu-id="db088-444">Name 요소</span><span class="sxs-lookup"><span data-stu-id="db088-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="db088-445">ID 요소</span><span class="sxs-lookup"><span data-stu-id="db088-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="db088-446">버전 요소</span><span class="sxs-lookup"><span data-stu-id="db088-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="db088-447">Author 요소</span><span class="sxs-lookup"><span data-stu-id="db088-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="db088-448">프로세스 및 프로세스 요소</span><span class="sxs-lookup"><span data-stu-id="db088-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="db088-449">응용 프로그램 요소</span><span class="sxs-lookup"><span data-stu-id="db088-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="db088-450">공통 요소</span><span class="sxs-lookup"><span data-stu-id="db088-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="db088-451">SettingsLocationTemplate 요소</span><span class="sxs-lookup"><span data-stu-id="db088-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="db088-452">부록: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="db088-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="db088-453">XML 선언 및 인코딩 특성</span><span class="sxs-lookup"><span data-stu-id="db088-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="db088-454">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-454">Mandatory: True</span></span>**

**<span data-ttu-id="db088-455">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-455">Type: String</span></span>**

<span data-ttu-id="db088-456">XML 선언에서는 XML 버전 1.0 특성 ( &lt; ? XML 버전 = "1.0")을 지정 해야 합니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="db088-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="db088-457">UE-V 생성기에서 만든 설정 위치 템플릿은 해당 인코딩이 명시적으로 지정 되어 있지 않지만 UTF-8 인코딩으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="db088-458">이 요소에 encoding = "UTF-8" 특성을 가장 좋은 방법으로 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="db088-459">제품에 포함 된 모든 서식 파일은이 태그를 지정 합니다 (참조용%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\Templates 문서 참조).</span><span class="sxs-lookup"><span data-stu-id="db088-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="db088-460">예:</span><span class="sxs-lookup"><span data-stu-id="db088-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="db088-461">네임 스페이스 및 루트 요소</span><span class="sxs-lookup"><span data-stu-id="db088-461">Namespace and Root Element</span></span>

**<span data-ttu-id="db088-462">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-462">Mandatory: True</span></span>**

**<span data-ttu-id="db088-463">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-463">Type: String</span></span>**

<span data-ttu-id="db088-464">UE-V는 https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate 모든 응용 프로그램에 대 한 네임 스페이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="db088-465">SettingsLocationTemplate은 루트 요소 이며 다른 모든 요소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="db088-466">이 태그를 사용 하 여 모든 템플릿의 Reference SettingsLocationTemplate:</span><span class="sxs-lookup"><span data-stu-id="db088-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="db088-467">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="db088-467">Data types</span></span>

<span data-ttu-id="db088-468">다음은 UE-V 응용 프로그램 템플릿 스키마에 대 한 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="db088-469">**GUID** GUID는 "\\ {\ [a-fA-F0-9 \]-\ [a-fA-F0-9 \] 형식으로 된 표준 전역 고유 식별자 정규식을 설명 합니다. {8} {4} [a-Fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \\}".</span><span class="sxs-lookup"><span data-stu-id="db088-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="db088-470">Filesetting\\Root\\KnownFolder 요소에서 잘 알려진 폴더의 서식을 확인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="db088-471">**FilenameString** FilenameString는 모니터링할 프로세스의 파일 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="db088-472">해당 값은 regex \ [^ \\ \ \\? \ \ \ \* \ \ | &lt; &gt; 에 의해 제한 됩니다. /: \] +, (백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 문자를 포함 하지 않을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="db088-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="db088-473">**Idstring** IDString은 응용 프로그램 요소의 ID 값, SettingsLocationTemplate, 공통 요소 (공통 설정을 공유 하는 응용 프로그램 제품군을 설명 하는 데 사용 됨)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="db088-474">FilenameString (\\ [^ \\? \\ | &lt; &gt; )와 동일한 regex로 제한 됩니다. /:\]+).</span><span class="sxs-lookup"><span data-stu-id="db088-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="db088-475">**서식 버전** 서식 파일 버전은 설정 위치 템플릿의 수정을 설명 하는 데 사용 되는 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="db088-476">값의 범위는 0 ~ 2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="db088-477">**비어 있음** Empty는 null 값을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="db088-478">이는 처리할 프로세스가 없다는 것을 나타내기 위해 Process\\ShellProcess에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="db088-479">이 값은 응용 프로그램 템플릿에서 사용해 서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="db088-480">**만든이** Author 데이터 형식은 서식 파일의 작성자를 식별 하는 복잡 한 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="db088-481">여기에는 **이름** 및 **전자 메일**이라는 두 개의 자식 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="db088-482">Author 데이터 형식 내에서 Name 요소는 필수 항목이 며 전자 메일 요소는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="db088-483">이 형식은 SettingsLocationTemplate 요소 아래에 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="db088-484">**범위** 범위는 **최소** 및 **최대**의 두 자식 요소로 구성 된 integer 클래스를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="db088-485">이 데이터 형식은 ProcessVersion 데이터 형식에서 구현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="db088-486">지정 된 경우 최소 및 최대 값을 모두 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="db088-487">**Processversion** ProcessVersion은 **주**, **부**, **빌드**, **패치**등 네 가지 자식 요소를 사용 하 여 형식을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="db088-488">이 데이터 형식은 Process 요소에서 ProductVersion 및 FileVersion 값을 채우는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="db088-489">이 유형의 데이터는 범위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-489">The data for this type is a Range value.</span></span> <span data-ttu-id="db088-490">주요 자식 요소는 필수 이며 나머지는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="db088-491">**아키텍처가** 아키텍처에는 두 가지 가능 값 ( **Win32** 및 **Win64**)이 열거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="db088-492">이러한 값은 프로세스 아키텍처를 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="db088-493">**공정** 프로세스 데이터 형식은 UE-V를 통해 모니터링할 프로세스를 설명 하는 데 사용 되는 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="db088-494">여기에는 **파일 이름**, **아키텍처**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**의 여섯 가지 하위 요소가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="db088-495">이 표에서는 각 요소의 해당 데이터 형식에 대해 자세히 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db088-496">요소</span><span class="sxs-lookup"><span data-stu-id="db088-496">Element</span></span></th>
<th align="left"><span data-ttu-id="db088-497">데이터 형식</span><span class="sxs-lookup"><span data-stu-id="db088-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="db088-498">Mandatory</span><span class="sxs-lookup"><span data-stu-id="db088-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-499">이름이</span><span class="sxs-lookup"><span data-stu-id="db088-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-500">FilenameString</span><span class="sxs-lookup"><span data-stu-id="db088-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-501">True</span><span class="sxs-lookup"><span data-stu-id="db088-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-502">아키텍처</span><span class="sxs-lookup"><span data-stu-id="db088-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-503">아키텍처</span><span class="sxs-lookup"><span data-stu-id="db088-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-504">False</span><span class="sxs-lookup"><span data-stu-id="db088-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="db088-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-506">문자열</span><span class="sxs-lookup"><span data-stu-id="db088-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-507">False</span><span class="sxs-lookup"><span data-stu-id="db088-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="db088-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-509">문자열</span><span class="sxs-lookup"><span data-stu-id="db088-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-510">False</span><span class="sxs-lookup"><span data-stu-id="db088-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="db088-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="db088-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-513">False</span><span class="sxs-lookup"><span data-stu-id="db088-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-514">FileVersion</span><span class="sxs-lookup"><span data-stu-id="db088-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="db088-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-516">False</span><span class="sxs-lookup"><span data-stu-id="db088-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="db088-517">**프로세스** 프로세스 데이터 형식은 하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="db088-518">프로세스 시퀀스 형식에서 처리 되는 두 개의 자식 요소에는 **process** 와 **shellprocess**지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="db088-519">프로세스는 유형 프로세스의 요소이 고 ShellProcess는 데이터 형식이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="db088-520">순서에서 하나 이상의 항목을 식별 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="db088-521">**경로** RegistrySetting 및 FileSetting에서 Path를 사용 하 여 레지스트리와 파일 경로를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="db088-522">이 요소는 선택적 특성 두 개를 지원 합니다. **재귀** 및 **Deletfnota가 발견**되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="db088-523">두 값 모두 default = "False"로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="db088-524">Recursive는 경로 및 모든 하위 폴더가 파일 설정에 포함 되거나 모든 하위 레지스트리 키가 레지스트리 설정에 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="db088-525">두 경우 모두 현재 수준의 모든 항목이 캡처한 데이터에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="db088-526">FileSettings 개체의 경우 지정 된 폴더 내의 모든 파일이 UE-V를 통해 캡처한 데이터에 포함 되지만 폴더는 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="db088-527">레지스트리 경로의 경우 현재 경로에 있는 모든 값이 캡처되고 자식 레지스트리 키가 캡처되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="db088-528">두 경우 모두 대규모 데이터 집합 또는 많은 수의 항목을 캡처하는 것을 방지 하기 위해 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="db088-529">DeleteIfNotFound 특성은 사용자의 설정 저장소 경로 데이터에서 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="db088-530">이는 패키지에서 이러한 설정을 제거 하 여 설정 저장소 경로 파일 서버에 많은 양의 디스크 공간이 저장 되는 경우에 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="db088-531">**FileMask** FileMask는 Path로 정의 된 폴더에 대 한 특정 파일 형식만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="db088-532">예를 들어 Path는 `C:\users\username\files` `*.txt` 텍스트 파일만 포함 하 고 FileMask 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="db088-533">**RegistrySetting** RegistrySetting는 레지스트리 키 및 값에 대 한 컨테이너와 UE-V 에이전트의 부분에 대 한 연결 된 원하는 동작을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="db088-534">**Path**, **Name**, **Exclude**, 값 **경로** 및 **이름의**시퀀스를 포함 하 여 네 개의 자식 요소가이 형식으로 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="db088-535">**Filesetting** FileSetting에는 파일 및 파일 경로와 연결 된 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="db088-536">**루트**, **경로**, **FileMask**및 **Exclude**의 네 가지 자식 요소가 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="db088-537">Root는 필수 이며 나머지는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="db088-538">**설정** 설정은 특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="db088-539">여기에는 앞에서 설명한 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="db088-540">또한 다음과 같은 동작이 포함 된 다음 자식 요소도 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db088-541">요소</span><span class="sxs-lookup"><span data-stu-id="db088-541">Element</span></span></th>
<th align="left"><span data-ttu-id="db088-542">설명</span><span class="sxs-lookup"><span data-stu-id="db088-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-543">비동기</span><span class="sxs-lookup"><span data-stu-id="db088-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-544">비동기 설정 패키지는 응용 프로그램 시작을 차단 하지 않고 적용 되므로 설정이 계속 적용 되는 동안 응용 프로그램을 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="db088-545">이 방법은 SystemParameterSetting과 같이 API를 통해 비동기적으로 적용할 수 있는 설정에 유용 <code>get/set</code> 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="db088-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-547">기본적으로 UE-V는 템플릿을 사용 하는 응용 프로그램의 마지막 인스턴스가 닫혀 있을 때만 응용 프로그램에 대 한 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="db088-548">이 요소를 ' f l l e '로 설정 하면 UE-V가 응용 프로그램의 다른 인스턴스가 실행 되는 경우에도 설정을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="db088-549">적합 한 서식 파일 – UE-V를 사용 하 여 제공 되는 공용 요소 섹션이 포함 된 경우이 플래그를 사용 하 여 마지막 인스턴스가 닫힐 때까지 응용 프로그램 관련 설정이 내보내기 되지 않도록 하 여 응용 프로그램을 닫을 때 공유 설정을 항상 내보낼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="db088-550">Name 요소</span><span class="sxs-lookup"><span data-stu-id="db088-550">Name Element</span></span>

**<span data-ttu-id="db088-551">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-551">Mandatory: True</span></span>**

**<span data-ttu-id="db088-552">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-552">Type: String</span></span>**

<span data-ttu-id="db088-553">Name은 설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-554">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-555">일반적으로 버전 정보를 참조 하지 않도록 하는 것은 ProductVersion 요소와는 다른 것이 될 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="db088-556">예를 들어, `<Name>My Application</Name>` 대신를 지정 `<Name>My Application 1.1</Name>` 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="db088-557">**참고**  UE-V는 외부 Dtd를 참조 하지 않으므로 설정 위치 템플릿에서 명명 된 엔터티를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="db088-558">예를 들어 &reg; 등록 된 무역 표시 기호®를 참조 하는 데 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="db088-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="db088-559">대신 정식 번호 매기기 참조를 사용 하 여 이러한 유형의 특수 문자를 포함 합니다 (예:® 문자에 대 한 & \ #174).</span><span class="sxs-lookup"><span data-stu-id="db088-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="db088-560">이 규칙은이 문서의 모든 문자열 값에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="db088-561"><http://www.w3.org/TR/xhtml1/dtds.html>전체 문자 엔터티 목록을 보려면을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db088-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="db088-562">U t f-8로 인코딩된 문서에는 유니코드 문자가 직접 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="db088-563">UE-V 생성기를 통해 템플릿을 저장 하면 문자 엔터티가 해당 유니코드 표현으로 자동 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="db088-564">ID 요소</span><span class="sxs-lookup"><span data-stu-id="db088-564">ID Element</span></span>

**<span data-ttu-id="db088-565">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-565">Mandatory: True</span></span>**

**<span data-ttu-id="db088-566">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-566">Type: String</span></span>**

<span data-ttu-id="db088-567">ID는 특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-568">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다 (예: Get-help Evtemplate 및 가져오기-Uevtemplate 파일 프로그램 PowerShell cmdlet의 출력 참조).</span><span class="sxs-lookup"><span data-stu-id="db088-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="db088-569">규칙에 따라이 태그에는 모든 공백을 포함할 수 없으며 스크립팅이 간단해 집니다.</span><span class="sxs-lookup"><span data-stu-id="db088-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="db088-570">또는 등의 템플릿을 쉽게 식별할 수 있도록이 요소에 응용 프로그램의 버전 번호를 지정 해야 합니다 `<ID>MicrosoftCalculator6</ID>` `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="db088-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="db088-571">버전 요소</span><span class="sxs-lookup"><span data-stu-id="db088-571">Version Element</span></span>

**<span data-ttu-id="db088-572">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-572">Mandatory: True</span></span>**

**<span data-ttu-id="db088-573">유형: Integer</span><span class="sxs-lookup"><span data-stu-id="db088-573">Type: Integer</span></span>**

**<span data-ttu-id="db088-574">최 솟 값: 0</span><span class="sxs-lookup"><span data-stu-id="db088-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="db088-575">최 댓 값: 2147483647</span><span class="sxs-lookup"><span data-stu-id="db088-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="db088-576">버전은 변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="db088-577">UE-V 생성기는 템플릿이 저장 될 때마다이 번호를 하나씩 자동으로 증가 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="db088-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="db088-578">이 필드에 정수 (integer) 값이 있어야 합니다. 같은 소수 값 `<Version>2.5</Version>` 은 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="db088-579">**힌트:** 다음과 같은 XML 주석 태그를 사용 하 여 버전 변경에 대 한 노트를 저장할 수 있습니다 `<!-- -->` .</span><span class="sxs-lookup"><span data-stu-id="db088-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="db088-580">**중요**  이 값을 쿼리하여 다음 인스턴스의 기존 서식 파일에 새 버전의 서식 파일을 적용 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="db088-581">예약 된 서식 파일 자동 업데이트 작업이 실행 되는 경우</span><span class="sxs-lookup"><span data-stu-id="db088-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="db088-582">업데이트 UevTemplate PowerShell cmdlet이 실행 되는 경우</span><span class="sxs-lookup"><span data-stu-id="db088-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="db088-583">Microsoft\\uev: SettingsLocationTemplate Update 메서드가 WMI를 통해 호출 되는 경우</span><span class="sxs-lookup"><span data-stu-id="db088-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="db088-584">Author 요소</span><span class="sxs-lookup"><span data-stu-id="db088-584">Author Element</span></span>

**<span data-ttu-id="db088-585">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-585">Mandatory: False</span></span>**

**<span data-ttu-id="db088-586">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-586">Type: String</span></span>**

<span data-ttu-id="db088-587">만든이는 설정 위치 템플릿의 작성자를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="db088-588">**이름** 및 **전자 메일**이라는 두 개의 선택적 자식 요소가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="db088-589">두 특성은 모두 선택 사항 이지만, 전자 메일 자식 요소가 지정 된 경우 Name 요소와 함께 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="db088-590">만든이는 설정 위치 서식 파일에 대 한 연락처의 전체 이름을 나타내고, 전자 메일은 작성자의 전자 메일 주소를 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="db088-591">이 정보는 [Ue-v 템플릿 갤러리](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)와 같이 공개적으로 게시 된 서식 파일에 포함 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="db088-592">프로세스 및 프로세스 요소</span><span class="sxs-lookup"><span data-stu-id="db088-592">Processes and Process Element</span></span>

**<span data-ttu-id="db088-593">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-593">Mandatory: True</span></span>**

**<span data-ttu-id="db088-594">Type: Element</span><span class="sxs-lookup"><span data-stu-id="db088-594">Type: Element</span></span>**

<span data-ttu-id="db088-595">프로세스에는 적어도 하나 이상의 요소가 포함 되어 `<Process>` 있으며, 여기에는 **Filename**, **Architecture**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**이라는 자식 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="db088-596">Filename 하위 요소는 필수 이며 나머지는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="db088-597">완전히 채워진 요소에는 다음 예제와 유사한 태그가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="db088-598">이름이</span><span class="sxs-lookup"><span data-stu-id="db088-598">Filename</span></span>

**<span data-ttu-id="db088-599">필수: True</span><span class="sxs-lookup"><span data-stu-id="db088-599">Mandatory: True</span></span>**

**<span data-ttu-id="db088-600">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-600">Type: String</span></span>**

<span data-ttu-id="db088-601">Filename은 파일 시스템에 표시 되는 실행 파일의 실제 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="db088-602">이 요소는 템플릿이 프로세스에 적용 되는지 여부를 평가 하기 위해 UE-V에서 사용 하는 기본 조건을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="db088-603">이 요소는 설정 위치 템플릿 XML에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="db088-604">올바른 파일 이름은 정규식 \ [^ \\? \ \? \ \ | &lt; &gt; 와 일치 하지 않아야 합니다. /: \] +, 즉 백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 (\\?)이 포함 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="db088-605">\* | &lt; &gt; /또는: 문자.</span><span class="sxs-lookup"><span data-stu-id="db088-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="db088-606">**힌트:** 이 정규식에 대해 문자열을 테스트 하려면 PowerShell 명령 창을 사용 하 여 **해당 파일 이름에 대 한**실행 파일의 이름을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="db088-607">**True** 값은 문자열에 잘못 된 문자가 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="db088-608">다음은 잘못 된 값의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="db088-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="db088-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="db088-610">프로그램 \ \* .exe</span><span class="sxs-lookup"><span data-stu-id="db088-610">Program\*.exe</span></span>

-   <span data-ttu-id="db088-611">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="db088-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="db088-612">프로그램 &lt; 1 &gt; .exe</span><span class="sxs-lookup"><span data-stu-id="db088-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="db088-613">**참고**  UE-V 생성기는 각각 문자 보다 크거나 작은 값을 &gt; &lt; 각각 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="db088-614">드문 경우 지만 FileName 값에 .exe 확장명을 포함할 필요는 없지만 값의 일부로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="db088-615">예를 들어을 `<Filename>MyApplictication.exe</Filename>` 대신 지정 해야 합니다 `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="db088-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="db088-616">두 번째 예제에서는 실행 파일의 실제 이름이 "MyApplication.exe" 인 경우 템플릿을 프로세스에 적용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="db088-617">아키텍처</span><span class="sxs-lookup"><span data-stu-id="db088-617">Architecture</span></span>

**<span data-ttu-id="db088-618">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-618">Mandatory: False</span></span>**

**<span data-ttu-id="db088-619">Type: Architecture (String)</span><span class="sxs-lookup"><span data-stu-id="db088-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="db088-620">아키텍처는 대상 실행 파일이 컴파일된 프로세서 아키텍처를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="db088-621">유효한 값은 32 비트 응용 프로그램 또는 64 비트 응용 프로그램의 Win64에 대 한 Win32입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="db088-622">있는 경우이 태그는 설정 위치 템플릿의 적용 가능성을 특정 응용 프로그램 아키텍처로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="db088-623">예를 들어%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\templates\\ MicrosoftOffice2010Win32.xml 및 UE-V와 함께 포함 된 MicrosoftOffice2010Win64.xml 파일을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="db088-624">이는 여러 버전의 실행 파일에 대 한 상대 경로가 변경 되거나 프로세서 아키텍처 간에 전환할 때 설정이 추가 또는 제거 된 경우에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="db088-625">이 요소가 없으면 설정 위치 템플릿은 프로세스의 아키텍처를 무시 하 고 파일 이름과 기타 특성이 적용 되는 경우 32 및 64 비트 프로세스에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="db088-626">**참고**  UE-V는이 버전의 ARM 프로세서를 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="db088-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="db088-627">ProductName</span></span>

**<span data-ttu-id="db088-628">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-628">Mandatory: False</span></span>**

**<span data-ttu-id="db088-629">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-629">Type: String</span></span>**

<span data-ttu-id="db088-630">ProductName은 관리 목적 또는 보고를 위해 제품을 식별 하는 데 사용 되는 선택적 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="db088-631">ProductName은 해당 값에 정규식 제한이 없다는 점에서 Filename과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="db088-632">이를 통해 실행 파일 이름이 명확 하지 않을 수 있는 프로세스에 대 한 보다 쉽게 이해 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="db088-633">예:</span><span class="sxs-lookup"><span data-stu-id="db088-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="db088-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="db088-634">FileDescription</span></span>

**<span data-ttu-id="db088-635">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-635">Mandatory: False</span></span>**

**<span data-ttu-id="db088-636">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-636">Type: String</span></span>**

<span data-ttu-id="db088-637">FileDescription은 실행 파일의 관리 설명을 허용 하는 선택적 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="db088-638">자유 텍스트 필드 이며, 실행 파일의 기능을 식별 해야 하는 소프트웨어 패키지 내에서 여러 실행 파일을 구분 하는 데 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="db088-639">예를 들어 적합 한 응용 프로그램에서는 다음과 같이 두 실행 파일 (MyApplication.exe 및 MyApplicationHelper.exe)의 함수에 대 한 미리 알림을 제공 하는 것이 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="db088-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="db088-640">ProductVersion</span></span>

**<span data-ttu-id="db088-641">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-641">Mandatory: False</span></span>**

**<span data-ttu-id="db088-642">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-642">Type: String</span></span>**

<span data-ttu-id="db088-643">ProductVersion는 파일의 주 버전과 부 버전을 참조 하 고 빌드 및 패치 수준에도 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="db088-644">ProductVersion는 선택적 요소 이지만, 지정 하는 경우 적어도 주요 자식 요소를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="db088-645">값은 Minimum = "X" Maximum = "Y" 형식의 범위를 표현 해야 합니다. 여기서 X와 Y는 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="db088-646">Minimum 및 Maximum 값은 동일할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="db088-647">제품 및 파일 버전 요소는 지정 되지 않은 상태로 남아 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="db088-648">이렇게 하면 서식 파일을 "버전에 맞게 표시" 하 여 템플릿이 지정 된 실행 파일의 모든 버전에 적용 되는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="db088-649">예 1:</span><span class="sxs-lookup"><span data-stu-id="db088-649">Example 1:</span></span>**

<span data-ttu-id="db088-650">UE-V 생성기에 지정 된 제품 버전: 1.0는 다음과 같은 XML을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="db088-651">예 2:</span><span class="sxs-lookup"><span data-stu-id="db088-651">Example 2:</span></span>**

<span data-ttu-id="db088-652">파일 버전: UE-V 생성기에 지정 된 5.0.2.1000는 다음과 같은 XML을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="db088-653">잘못 된 예제 1-완전 하지 않은 범위:</span><span class="sxs-lookup"><span data-stu-id="db088-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="db088-654">최소 특성만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="db088-655">범위에도 Maximum을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="db088-656">잘못 된 예제 2 – 주요 요소 없이 Minor가 지정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="db088-657">Minor 요소만 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-657">Only the Minor element is present.</span></span> <span data-ttu-id="db088-658">주 버전도 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="db088-659">FileVersion</span><span class="sxs-lookup"><span data-stu-id="db088-659">FileVersion</span></span>

**<span data-ttu-id="db088-660">필수: False</span><span class="sxs-lookup"><span data-stu-id="db088-660">Mandatory: False</span></span>**

**<span data-ttu-id="db088-661">형식: 문자열</span><span class="sxs-lookup"><span data-stu-id="db088-661">Type: String</span></span>**

<span data-ttu-id="db088-662">FileVersion은 게시 된 응용 프로그램의 릴리스 버전과 구성 요소 실행 파일의 내부 빌드 세부 정보를 구별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="db088-663">대부분의 상업용 응용 프로그램의 경우 이러한 번호는 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="db088-664">변경 되는 파일의 제품 버전은 파일의 일반 버전 식별을 나타내고, 파일 버전은 파일의 특정 빌드를 나타냅니다 (핫픽스나 업데이트의 경우).</span><span class="sxs-lookup"><span data-stu-id="db088-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="db088-665">이렇게 하면 검색 논리가 손상 되지 않은 파일을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="db088-666">제품 버전과 특정 실행 파일 버전을 확인 하려면 Windows 탐색기에서 파일을 마우스 오른쪽 단추로 클릭 하 고 속성을 선택한 다음 세부 정보 탭을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="db088-667">응용 프로그램에 FileVersion 요소를 포함 하면 더 세밀 하 게 조정할 수 있지만, 대부분의 응용 프로그램에서는 이러한 검색 논리가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db088-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="db088-668">ProductVersion 요소 설정이 먼저 검사 되 고 FileVersion이 선택 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="db088-669">더 제한적인 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="db088-670">FileVersion의 자식 요소 및 구문 규칙은 ProductVersion와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="db088-671">응용 프로그램 요소</span><span class="sxs-lookup"><span data-stu-id="db088-671">Application Element</span></span>

<span data-ttu-id="db088-672">응용 프로그램은 특정 응용 프로그램에 적용 되는 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="db088-673">다음 필드/형식의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db088-674">필드/형식</span><span class="sxs-lookup"><span data-stu-id="db088-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="db088-675">설명</span><span class="sxs-lookup"><span data-stu-id="db088-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-676">이름</span><span class="sxs-lookup"><span data-stu-id="db088-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-677">설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-678">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-679">자세한 내용은 Name을 참조 <a href="#name" data-raw-source="[Name](#name)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-680">ID</span><span class="sxs-lookup"><span data-stu-id="db088-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-681">특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-682">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="db088-683">자세한 내용은 ID를 참조 <a href="#id" data-raw-source="[ID](#id)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-684">설명</span><span class="sxs-lookup"><span data-stu-id="db088-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-685">서식 파일에 대 한 설명입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="db088-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-686">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="db088-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-687">UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="db088-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-689">언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-690">버전</span><span class="sxs-lookup"><span data-stu-id="db088-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-691">변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="db088-692">자세한 내용은 버전을 참조 <a href="#version" data-raw-source="[Version](#version)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="db088-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-694">이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="db088-695">컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="db088-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-697">MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="db088-698">설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-699">프로세스</span><span class="sxs-lookup"><span data-stu-id="db088-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-700">하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="db088-701">자세한 내용은 프로세스를 참조 <a href="#processes" data-raw-source="[Processes](#processes)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-702">설정</span><span class="sxs-lookup"><span data-stu-id="db088-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-703">특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="db088-704">여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="db088-705">자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data" data-raw-source="[Data types](#data)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="db088-706">공통 요소</span><span class="sxs-lookup"><span data-stu-id="db088-706">Common Element</span></span>

<span data-ttu-id="db088-707">일반적으로 응용 프로그램 요소와 유사 하지만 항상 둘 이상의 응용 프로그램 요소와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="db088-708">공용 섹션은 해당 응용 프로그램 인스턴스 간에 공유 되는 설정 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="db088-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="db088-709">다음 필드/형식의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db088-710">필드/형식</span><span class="sxs-lookup"><span data-stu-id="db088-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="db088-711">설명</span><span class="sxs-lookup"><span data-stu-id="db088-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-712">이름</span><span class="sxs-lookup"><span data-stu-id="db088-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-713">설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-714">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-715">자세한 내용은 Name을 참조 <a href="#name" data-raw-source="[Name](#name)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-716">ID</span><span class="sxs-lookup"><span data-stu-id="db088-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-717">특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-718">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="db088-719">자세한 내용은 ID를 참조 <a href="#id" data-raw-source="[ID](#id)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-720">설명</span><span class="sxs-lookup"><span data-stu-id="db088-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-721">서식 파일에 대 한 설명입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="db088-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-722">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="db088-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-723">UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="db088-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-725">언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-726">버전</span><span class="sxs-lookup"><span data-stu-id="db088-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-727">변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="db088-728">자세한 내용은 버전을 참조 <a href="#version" data-raw-source="[Version](#version)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="db088-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-730">이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="db088-731">컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="db088-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-733">MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="db088-734">설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-735">설정</span><span class="sxs-lookup"><span data-stu-id="db088-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-736">특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="db088-737">여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="db088-738">자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data" data-raw-source="[Data types](#data)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="db088-739">SettingsLocationTemplate 요소</span><span class="sxs-lookup"><span data-stu-id="db088-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="db088-740">이 요소는 단일 응용 프로그램 또는 응용 프로그램 집합에 대 한 설정을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db088-741">필드/형식</span><span class="sxs-lookup"><span data-stu-id="db088-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="db088-742">설명</span><span class="sxs-lookup"><span data-stu-id="db088-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-743">이름</span><span class="sxs-lookup"><span data-stu-id="db088-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-744">설정 위치 템플릿의 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db088-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="db088-745">이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="db088-746">자세한 내용은 Name을 참조 <a href="#name" data-raw-source="[Name](#name)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-747">ID</span><span class="sxs-lookup"><span data-stu-id="db088-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-748">특정 서식 파일의 고유 식별자를 채웁니다.</span><span class="sxs-lookup"><span data-stu-id="db088-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="db088-749">이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db088-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="db088-750">자세한 내용은 ID를 참조 <a href="#id" data-raw-source="[ID](#id)"> 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="db088-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-751">설명</span><span class="sxs-lookup"><span data-stu-id="db088-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-752">서식 파일에 대 한 설명입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="db088-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db088-753">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="db088-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-754">UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db088-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="db088-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="db088-756">언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="db088-757">부록: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="db088-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="db088-758">다음은 해당 요소, 자식 요소, 특성 및 매개 변수를 보여 주는 SettingsLocationTemplate .xsd 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="db088-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="db088-759">관련 항목</span><span class="sxs-lookup"><span data-stu-id="db088-759">Related topics</span></span>


[<span data-ttu-id="db088-760">사용자 지정 UE-V 2. x 템플릿 및 UE-V 2 .x 생성기 사용</span><span class="sxs-lookup"><span data-stu-id="db088-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="db088-761">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="db088-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





