---
title: UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 편집
description: UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 편집
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827113"
---
# <span data-ttu-id="77bf8-103">UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 편집</span><span class="sxs-lookup"><span data-stu-id="77bf8-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="77bf8-104">Microsoft UE-V (User Experience Virtualization) 생성기를 사용 하 여 설정 위치 템플릿을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="77bf8-105">UE-V 생성기를 사용 하 여 수정 된 설정을 템플릿에 추가 하면 해당 서식 파일의 버전 정보가 자동으로 업데이트 되어 엔터프라이즈에 배포 된 기존 서식 파일이 올바르게 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="77bf8-106">UE-V 생성기를 사용 하 여 UE-V 설정 위치 템플릿을 편집 하는 방법</span><span class="sxs-lookup"><span data-stu-id="77bf8-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="77bf8-107">**시작**을 클릭 하 고 **모든 프로그램**, **microsoft 사용자 환경 가상화**를 차례로 클릭 한 다음 **microsoft 사용자 환경 가상화 생성기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="77bf8-108">**설정 위치 서식 파일 편집을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="77bf8-109">최근에 사용한 서식 파일 목록에서 편집할 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="77bf8-110">또는 설정 템플릿 파일을 **찾습니다** .</span><span class="sxs-lookup"><span data-stu-id="77bf8-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="77bf8-111">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="77bf8-112">설정 템플릿의 **속성**, **레지스트리** 위치 및 **파일** 위치를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="77bf8-113">필요에 따라 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-113">Edit as needed.</span></span>

    -   <span data-ttu-id="77bf8-114">**속성** 탭에서 다음 속성을 보고 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="77bf8-115">**응용 프로그램 이름**: 프로그램 파일 속성에 대 한 설명으로 작성 된 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="77bf8-116">**프로그램 이름**: 프로그램 파일 속성에서 가져온 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="77bf8-117">이 이름에는 일반적으로 .exe 확장명이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="77bf8-118">**제품 버전**: 응용 프로그램의 .exe 파일에 대 한 제품 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="77bf8-119">이 속성은 **파일 버전과**함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="77bf8-120">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-120">This property accepts a major version number.</span></span> <span data-ttu-id="77bf8-121">이 속성이 비어 있으면 설정 위치 템플릿이 모든 제품 버전에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="77bf8-122">**파일 버전**: 응용 프로그램의 the.exe 파일에 대 한 파일 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="77bf8-123">이 속성은 **제품 버전과**함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="77bf8-124">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-124">This property accepts a major version number.</span></span> <span data-ttu-id="77bf8-125">이 속성이 비어 있으면 설정 위치 템플릿이 모든 버전의 프로그램에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="77bf8-126">**서식 파일 만든이 이름** (선택 사항): 설정 서식 파일 작성자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="77bf8-127">**서식 파일 저자 전자 메일** (선택 사항): 설정 위치 템플릿 작성자의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="77bf8-128">**레지스트리** 탭에는 설정 위치 템플릿에 포함 된 레지스트리 위치의 **키** 와 **범위가** 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="77bf8-129">**작업** 드롭다운 메뉴를 사용 하 여 레지스트리 위치를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="77bf8-130">작업에는 새 키 추가, 기존 키의 이름 또는 범위 편집, 키 삭제, 키가 있는 레지스트리 찾아보기 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="77bf8-131">레지스트리의 범위를 정의할 때 **모든 설정** 범위를 사용 하 여 지정 된 키 아래에 모든 레지스트리 설정을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="77bf8-132">**모든 설정** 및 **하위 키** 를 사용 하 여 지정 된 키, 하위 키 및 하위 키 설정의 모든 레지스트리 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="77bf8-133">**파일** 탭에는 설정 위치 템플릿에 포함 된 파일 위치의 파일 경로와 파일 마스크가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="77bf8-134">**작업** 드롭다운 메뉴를 사용 하 여 파일 위치를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="77bf8-135">파일 위치에 대 한 작업에는 새 파일 또는 폴더 위치 추가, 기존 파일 또는 폴더의 범위 편집, 파일 또는 폴더 삭제, Windows 탐색기에서 선택한 위치 열기 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="77bf8-136">지정 된 폴더의 모든 파일을 포함 하려면 파일 마스크를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="77bf8-137">**저장** 을 클릭 하 여 설정 위치 템플릿에 대 한 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="77bf8-138">**닫기를** 클릭 하 여 설정 템플릿 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="77bf8-139">UE-V 생성기 응용 프로그램을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="77bf8-140">응용 프로그램의 설정 위치 템플릿을 편집한 후에는 서식 파일을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="77bf8-141">수정 된 설정 위치 템플릿을 엔터프라이즈의 프로덕션에 배치 하기 전에 랩 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="77bf8-142">설정 위치 템플릿을 수동으로 편집 하는 방법</span><span class="sxs-lookup"><span data-stu-id="77bf8-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="77bf8-143">설정 위치 템플릿 (.xml 파일)의 로컬 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="77bf8-144">UE-V 설정 위치 템플릿은 응용 프로그램이 설정 값을 저장 하는 위치를 식별 하는 .xml 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="77bf8-145">XML 편집기를 사용 하 여 설정 위치 템플릿 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="77bf8-146">설정 위치 템플릿 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-146">Edit the settings location template file.</span></span> <span data-ttu-id="77bf8-147">모든 변경 내용은 SettingsLocationTempate에 정의 된 UE-V 스키마 파일을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="77bf8-148">.Xsd 파일의 복사본은 `\ProgramData\Microsoft\UEV\Templates` 기본적으로 위치 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="77bf8-149">설정 위치 템플릿 파일을 저장 하 고 XML 편집기를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="77bf8-150">UE-V 생성기를 사용 하 여 수정 된 설정 위치 템플릿 파일의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="77bf8-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="77bf8-151">UE-V 생성기를 사용 하 여 유효성을 검사 하는 방법에 대 한 자세한 내용은 ue-v [생성기를 사용 하 여 Ue-v 설정 위치 템플릿 유효성 검사](validate-ue-v-settings-location-templates-with-ue-v-generator.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77bf8-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="77bf8-152">관련 항목</span><span class="sxs-lookup"><span data-stu-id="77bf8-152">Related topics</span></span>


[<span data-ttu-id="77bf8-153">사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업</span><span class="sxs-lookup"><span data-stu-id="77bf8-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="77bf8-154">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="77bf8-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





