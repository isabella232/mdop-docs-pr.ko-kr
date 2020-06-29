---
title: 사용자 지정 UE-V 2. x 템플릿 및 UE-V 2 .x 생성기 사용
description: 사용자 지정 UE-V 2. x 템플릿 및 UE-V 2 .x 생성기 사용
author: dansimp
ms.assetid: f0bb4920-0132-472c-a564-abf06a884275
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a8d863896e4ccfa92161f8a8f5e2b8955f139872
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819293"
---
# <span data-ttu-id="2b214-103">사용자 지정 UE-V 2. x 템플릿 및 UE-V 2 .x 생성기 사용</span><span class="sxs-lookup"><span data-stu-id="2b214-103">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="2b214-104">사용자 컴퓨터 간에 응용 프로그램 설정을 동기화 하려면 Microsoft 사용자 환경 가상화 (UE-V) 2.0, 2.1 및 2.1 SP1에서 *설정 위치 템플릿을*사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-104">To synchronize application settings between user computers, Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use *settings location templates*.</span></span> <span data-ttu-id="2b214-105">일부 설정 위치 템플릿은 사용자 환경 가상화에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-105">Some settings location templates are included in User Experience Virtualization.</span></span> <span data-ttu-id="2b214-106">UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들거나 편집 하거나 유효성을 검사할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-106">You can also create, edit, or validate custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="2b214-107">UE-V 생성기는 Windows 데스크톱 응용 프로그램을 모니터링 하 여 응용 프로그램에서 해당 설정을 저장 하는 위치를 검색 하 고 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-107">The UE-V Generator monitors Windows desktop applications to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="2b214-108">모니터링 되는 응용 프로그램은 데스크톱 응용 프로그램 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-108">The application that is monitored must be a desktop application.</span></span> <span data-ttu-id="2b214-109">UE-V 생성기는 다음 응용 프로그램 종류에 대 한 설정 위치 템플릿을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-109">The UE-V Generator cannot create a settings location template for the following application types:</span></span>

-   <span data-ttu-id="2b214-110">가상화 된 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="2b214-110">Virtualized applications</span></span>

-   <span data-ttu-id="2b214-111">터미널 서비스를 통해 제공 되는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="2b214-111">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="2b214-112">Java 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="2b214-112">Java applications</span></span>

-   <span data-ttu-id="2b214-113">Windows 앱  </span><span class="sxs-lookup"><span data-stu-id="2b214-113">Windows apps</span></span>

<span data-ttu-id="2b214-114">이 항목</span><span class="sxs-lookup"><span data-stu-id="2b214-114">This topic</span></span>

<span data-ttu-id="2b214-115">**표준 및 비표준 설정 위치:** UE-V 생성기는 응용 프로그램이 설정 정보를 저장 하는 데 사용 하는 설정 파일 및 레지스트리 설정을 검색 하는 위치를 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-115">**Standard and Nonstandard settings locations:** The UE-V Generator helps you identify where applications search for settings files and registry settings that applications use to store settings information.</span></span> <span data-ttu-id="2b214-116">생성기는 표준 사용자가 액세스할 수 있는 위치 에서만 설정을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-116">The generator only discovers settings in locations that are accessible to a standard user.</span></span> <span data-ttu-id="2b214-117">다른 위치에 저장 된 설정은 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-117">Settings that are stored in other locations are excluded.</span></span> <span data-ttu-id="2b214-118">검색 된 설정은 **표준** 및 비표준 **의**두 범주로 그룹화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-118">Discovered settings are grouped into two categories: **Standard** and **Non-standard**.</span></span> <span data-ttu-id="2b214-119">동기화에는 표준 설정이 권장 되며 UE-V를 통해 쉽게 캡처 및 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-119">Standard settings are recommended for synchronization, and UE-V can readily capture and apply them.</span></span> <span data-ttu-id="2b214-120">비 표준 설정은 잠재적으로 설정을 동기화 할 수 있지만, UE-V를 사용 하는 규칙 때문에 이러한 설정이 일관 되지 않거나 dependably 설정이 동기화 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-120">Non-standard settings can potentially synchronize settings but, because of the rules that UE-V uses, these settings might not consistently or dependably synchronize settings.</span></span> <span data-ttu-id="2b214-121">이러한 설정은 임시 파일에 따라 달라 지 며, 동기화 되지 않는 경우에는 그렇지 않거나, 도움이 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-121">These settings might depend on temporary files, result in unreliable synchronization, or might not be useful.</span></span> <span data-ttu-id="2b214-122">이러한 설정 위치는 UE-V 생성기에서 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-122">These settings locations are presented in the UE-V Generator.</span></span> <span data-ttu-id="2b214-123">대/소문자를 구분 하 여 포함 하거나 제외 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-123">You can choose to include or exclude them on a case-by-case basis.</span></span>

<span data-ttu-id="2b214-124">UE-V 생성기가 검색 프로세스의 일부로 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-124">The UE-V Generator opens the application as part of the discovery process.</span></span> <span data-ttu-id="2b214-125">생성자는 다음 위치에서 설정을 캡처할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-125">The generator can capture settings in the following locations:</span></span>

-   <span data-ttu-id="2b214-126">**레지스트리 설정** – **HKEY \ _CURRENT \ _USER** 아래의 레지스트리 위치</span><span class="sxs-lookup"><span data-stu-id="2b214-126">**Registry Settings** – Registry locations under **HKEY\_CURRENT\_USER**</span></span>

-   <span data-ttu-id="2b214-127">**응용 프로그램 설정 파일** – \\ **사용자** \\ [사용자 이름 \ \ **AppData**  \\  **로밍** '에 저장 되는 파일</span><span class="sxs-lookup"><span data-stu-id="2b214-127">**Application Settings Files** – Files that are stored under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**</span></span>

<span data-ttu-id="2b214-128">UE-V 생성기는 일반적으로 응용 프로그램 소프트웨어 파일을 저장 하지만 사용자 컴퓨터와 환경 간에는 동기화 되지 않는 위치를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-128">The UE-V Generator excludes locations, which commonly store application software files, but do not synchronize well between user computers or environments.</span></span> <span data-ttu-id="2b214-129">UE-V 생성기는 이러한 위치를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-129">The UE-V Generator excludes these locations.</span></span> <span data-ttu-id="2b214-130">제외 된 위치는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-130">Excluded locations are as follows:</span></span>

-   <span data-ttu-id="2b214-131">HKEY \ _CURRENT \ _USER 로그온 한 사용자가 값을 쓸 수 없는 레지스트리 키 및 파일</span><span class="sxs-lookup"><span data-stu-id="2b214-131">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="2b214-132">HKEY _CURRENT \ _USER Windows 운영 체제의 핵심 기능과 연결 된 레지스트리 키 및 파일</span><span class="sxs-lookup"><span data-stu-id="2b214-132">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="2b214-133">HKEY \ _LOCAL \ _MACHINE hive에 있는 모든 레지스트리 키 (관리자 권한이 필요 하며 UAC (사용자 계정 컨트롤) 계약을 설정 해야 할 수 있음)</span><span class="sxs-lookup"><span data-stu-id="2b214-133">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive, which requires administrator rights and might require to set a User Account Control (UAC) agreement</span></span>

-   <span data-ttu-id="2b214-134">관리자 권한이 필요 하며 UAC 규약을 설정 해야 할 수 있는 Program Files 디렉터리에 있는 파일</span><span class="sxs-lookup"><span data-stu-id="2b214-134">Files that are located in Program Files directories, which requires administrator rights and might require to set a UAC agreement</span></span>

-   <span data-ttu-id="2b214-135">사용자 \\ [사용자 이름 \] \\ AppData에 있는 파일에는 다음이 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-135">Files that are located under Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="2b214-136">관리자 권한이 필요 하며 UAC 계약을 설정 해야 하는 경우% Systemroot%에 있는 Windows 운영 체제 파일</span><span class="sxs-lookup"><span data-stu-id="2b214-136">Windows operating system files that are located in %Systemroot%, which requires administrator rights and might require to set a UAC agreement</span></span>

<span data-ttu-id="2b214-137">이러한 위치에 저장 된 레지스트리 키 및 파일이 응용 프로그램 설정을 동기화 하는 데 필요한 경우 템플릿 만들기 프로세스 중에 제외 된 위치를 설정 위치 템플릿에 수동으로 추가할 수 있습니다 (HKEY \ _LOCAL \ _MACHINE hive의 레지스트리 항목 제외).</span><span class="sxs-lookup"><span data-stu-id="2b214-137">If registry keys and files that are stored in these locations are required to synchronize application settings, you can manually add the excluded locations to the settings location template during the template creation process (except for registry entries in the HKEY\_LOCAL\_MACHINE hive).</span></span>

## <a href="" id="edit"></a><span data-ttu-id="2b214-138">UE-V 생성기를 사용 하 여 설정 위치 템플릿 편집</span><span class="sxs-lookup"><span data-stu-id="2b214-138">Edit Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="2b214-139">UE-V 생성기를 사용 하 여 설정 위치 템플릿을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-139">Use the UE-V Generator to edit settings location templates.</span></span> <span data-ttu-id="2b214-140">UE-V 생성기를 사용 하 여 수정 된 설정이 서식 파일에 추가 되 면 해당 서식 파일의 버전 정보가 자동으로 업데이트 되어 엔터프라이즈에 배포 된 기존 서식 파일이 제대로 업데이트 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-140">When the revised settings are added to the templates by using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates that are deployed in the enterprise are updated correctly.</span></span>

<span data-ttu-id="2b214-141">**참고**  Ue-v 2 생성기를 사용 하 여 UE-V 1.0 서식 파일을 편집 하는 경우에는 템플릿이 UE-V 2 템플릿으로 자동 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-141">**Note** If you edit a UE-V 1.0 template by using the UE-V 2 Generator, the template is automatically converted to a UE-V 2 template.</span></span> <span data-ttu-id="2b214-142">UE-V 1.0 에이전트는 편집 된 템플릿을 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-142">UE-V 1.0 Agents can no longer use the edited template.</span></span>

 

**<span data-ttu-id="2b214-143">UE-V 생성기를 사용 하 여 UE-V 설정 위치 템플릿을 편집 하려면</span><span class="sxs-lookup"><span data-stu-id="2b214-143">To edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="2b214-144">**시작**을 클릭 하 고 **모든 프로그램**, **microsoft 사용자 환경 가상화**를 차례로 클릭 한 다음 **microsoft 사용자 환경 가상화 생성기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-144">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="2b214-145">**설정 위치 서식 파일 편집을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-145">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="2b214-146">최근에 사용한 서식 파일 목록에서 편집할 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-146">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="2b214-147">또는 **찾아보기를** 클릭 하 여 설정 템플릿 파일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-147">Alternatively, click **Browse** to search for the settings template file.</span></span> <span data-ttu-id="2b214-148">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-148">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="2b214-149">설정 템플릿의 **속성**, **레지스트리** 위치 및 **파일** 위치를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-149">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="2b214-150">필요에 따라 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-150">Edit as required.</span></span>

    -   <span data-ttu-id="2b214-151">**속성** 탭에서 다음 속성을 보고 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-151">On the **Properties** tab, you can view and edit the following properties:</span></span>

        -   <span data-ttu-id="2b214-152">**응용 프로그램 이름**: 프로그램 파일 속성에 대 한 설명으로 작성 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-152">**Application name**: The application name that is written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="2b214-153">**프로그램 이름**: 프로그램 파일 속성에서 가져온 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-153">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="2b214-154">일반적으로이 이름은 .exe 파일 이름 확장명을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-154">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="2b214-155">**제품 버전**: 응용 프로그램의 .exe 파일에 대 한 제품 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-155">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="2b214-156">이 속성은 **파일 버전과**함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-156">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="2b214-157">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-157">This property accepts a major version number.</span></span> <span data-ttu-id="2b214-158">이 속성이 비어 있으면 설정 위치 템플릿이 모든 제품 버전에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-158">If this property is empty, then the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="2b214-159">**파일 버전**: 응용 프로그램의 .exe 파일에 대 한 파일 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-159">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="2b214-160">이 속성은 **제품 버전과**함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-160">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="2b214-161">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-161">This property accepts a major version number.</span></span> <span data-ttu-id="2b214-162">이 속성이 비어 있으면 설정 위치 템플릿이 모든 버전의 프로그램에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-162">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="2b214-163">**서식 파일 만든이 이름** (선택 사항): 설정 서식 파일 작성자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-163">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="2b214-164">**서식 파일 저자 전자 메일** (선택 사항): 설정 위치 템플릿 작성자의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-164">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="2b214-165">**레지스트리** 탭에는 설정 위치 템플릿에 포함 된 레지스트리 위치의 **키** 와 **범위가** 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-165">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="2b214-166">**작업** 드롭다운 메뉴를 사용 하 여 레지스트리 위치를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-166">You can edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="2b214-167">작업 메뉴에서 새 키를 추가 하 고, 기존 키의 이름 또는 범위를 편집 하 고, 키를 삭제 하 고, 키가 있는 레지스트리를 찾아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-167">In the Tasks menu, you can add new keys, edit the name or scope of existing keys, delete keys, and browse the registry in which the keys are located.</span></span> <span data-ttu-id="2b214-168">레지스트리의 범위를 정의할 때 **모든 설정** 범위를 사용 하 여 지정 된 키 아래에 모든 레지스트리 설정을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-168">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="2b214-169">**모든 설정** 및 **하위 키** 를 사용 하 여 지정 된 키, 하위 키 및 하위 키 설정의 모든 레지스트리 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-169">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="2b214-170">**파일** 탭에는 설정 위치 템플릿에 포함 된 파일 위치의 파일 경로 및 파일 마스크가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-170">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="2b214-171">**작업** 드롭다운 메뉴를 사용 하 여 파일 위치를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-171">You can edit the file locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="2b214-172">파일 위치에 대 한 **작업** 메뉴에서 새 파일 또는 폴더 위치를 추가 하 고, 기존 파일 또는 폴더의 범위를 편집 하 고, 파일이 나 폴더를 삭제 하 고, Windows 탐색기에서 선택한 위치를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-172">In the **Tasks** menu for file locations, you can add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="2b214-173">지정 된 폴더의 모든 파일을 포함 하려면 파일 마스크를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-173">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="2b214-174">**저장** 을 클릭 하 여 설정 위치 템플릿에 대 한 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-174">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="2b214-175">**닫기를** 클릭 하 여 설정 템플릿 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-175">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="2b214-176">UE-V 생성기 응용 프로그램을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-176">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="2b214-177">응용 프로그램의 설정 위치 템플릿을 편집한 후에는 서식 파일을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-177">After you edit the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="2b214-178">엔터프라이즈에서 프로덕션에 배치 하기 전에 먼저 랩 환경에서 수정 된 설정 위치 템플릿을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-178">Deploy the revised settings location template in a lab environment before you put it into production in the enterprise.</span></span>

**<span data-ttu-id="2b214-179">설정 위치 템플릿을 수동으로 편집 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2b214-179">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="2b214-180">설정 위치 템플릿 .xml 파일의 로컬 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-180">Create a local copy of the settings location template .xml file.</span></span> <span data-ttu-id="2b214-181">UE-V 설정 위치 템플릿은 응용 프로그램에서 설정 값을 저장 하는 위치를 식별 하는 .xml 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-181">UE-V settings location templates are .xml files that identify the locations where application store settings values.</span></span>

    <span data-ttu-id="2b214-182">**참고**  서식 파일 **ID**때문에 설정 위치 템플릿이 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-182">**Note** A settings location template is unique because of the template **ID**.</span></span> <span data-ttu-id="2b214-183">서식 파일을 복사 하 고 .xml 파일의 이름을 바꾸면 UE-V 파일에서 서식 파일 **ID** 태그를 읽어 .xml 파일의 이름이 아닌 이름을 확인 하기 때문에 서식 파일 등록이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-183">If you copy the template and rename the .xml file, template registration fails because UE-V reads the template **ID** tag in the .xml file to determine the name, not the file name of the .xml file.</span></span> <span data-ttu-id="2b214-184">또한 UE-V는 변경 내용이 있는지 확인 하기 위해 **버전** 번호를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-184">UE-V also reads the **Version** number to know if anything has changed.</span></span> <span data-ttu-id="2b214-185">버전 번호가 더 상위 이면 UE-V가 서식 파일을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-185">If the version number is higher, UE-V updates the template.</span></span>

     

2.  <span data-ttu-id="2b214-186">XML 편집기를 사용 하 여 설정 위치 템플릿 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-186">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="2b214-187">설정 위치 템플릿 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-187">Edit the settings location template file.</span></span> <span data-ttu-id="2b214-188">모든 변경 내용은 [Settingslocationtempate](https://technet.microsoft.com/library/dn763947.aspx)에 정의 된 ue-v 스키마 파일을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-188">All changes must conform to the UE-V schema file that is defined in [SettingsLocationTempate.xsd](https://technet.microsoft.com/library/dn763947.aspx).</span></span> <span data-ttu-id="2b214-189">기본적으로 .xsd 파일의 복사본은 \\ProgramData\\Microsoft\\UEV\\Templates.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-189">By default, a copy of the .xsd file is located in \\ProgramData\\Microsoft\\UEV\\Templates.</span></span>

4.  <span data-ttu-id="2b214-190">설정 위치 템플릿의 **버전** 번호를 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-190">Increment the **Version** number for the settings location template.</span></span>

5.  <span data-ttu-id="2b214-191">설정 위치 템플릿 파일을 저장 한 다음 XML 편집기를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-191">Save the settings location template file, and then close the XML editor.</span></span>

6.  <span data-ttu-id="2b214-192">UE-V 생성기를 사용 하 여 수정 된 설정 위치 템플릿 파일의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-192">Validate the modified settings location template file by using the UE-V Generator.</span></span>

7.  <span data-ttu-id="2b214-193">클라이언트 컴퓨터 간 설정을 동기화 하려면 먼저 편집 된 UE-V 설정 위치 템플릿을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-193">You must register the edited UE-V settings location template before it can synchronize settings between client computers.</span></span> <span data-ttu-id="2b214-194">템플릿을 등록 하려면 Windows PowerShell을 열고 다음 cmdlet을 실행 합니다 `update-uevtemplate [templatefilename]` .</span><span class="sxs-lookup"><span data-stu-id="2b214-194">To register a template, open Windows PowerShell, and then run the following cmdlet: `update-uevtemplate [templatefilename]`.</span></span> <span data-ttu-id="2b214-195">그런 다음 설정 저장소 카탈로그에 파일을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-195">You can then copy the file to the settings storage catalog.</span></span> <span data-ttu-id="2b214-196">그러면 사용자의 컴퓨터에 대 한 UE-V Agent가 예약 된 작업에서 일정 대로 업데이트 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-196">The UE-V Agent on users’ computers should then update as scheduled in the scheduled task.</span></span>

## <a href="" id="validate"></a><span data-ttu-id="2b214-197">UE-V 생성기를 사용 하 여 설정 위치 템플릿 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2b214-197">Validate Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="2b214-198">UE-V 생성기를 사용 하지 않고 XML 편집기에서 설정 위치 템플릿을 만들거나 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-198">It is possible to create or edit settings location templates in an XML editor without using the UE-V Generator.</span></span> <span data-ttu-id="2b214-199">이렇게 하는 경우 UE-V 생성기를 사용 하 여 새 XML 또는 수정 된 XML이 서식 파일에 대해 정의 된 스키마와 일치 하는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-199">If you do, you can use the UE-V Generator to validate that the new or revised XML matches the schema that has been defined for the template.</span></span>

**<span data-ttu-id="2b214-200">UE-V 생성기를 사용 하 여 UE-V 설정 위치 템플릿의 유효성을 검사 하려면</span><span class="sxs-lookup"><span data-stu-id="2b214-200">To validate a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="2b214-201">**시작**을 클릭 하 고 **모든 프로그램**을 가리킨 다음 **microsoft 사용자 환경 가상화**를 클릭 하 고 **microsoft 사용자 환경 가상화 생성기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-201">Click **Start**, point to **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="2b214-202">**설정 위치 서식 파일의 유효성 검사를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-202">Click **Validate a settings location template**.</span></span>

3.  <span data-ttu-id="2b214-203">최근에 사용한 서식 파일 목록에서 편집할 서식 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-203">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="2b214-204">또는 설정 템플릿 파일을 **탐색할** 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-204">Alternatively, you can **Browse** to the settings template file.</span></span> <span data-ttu-id="2b214-205">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-205">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="2b214-206">**확인** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-206">Click **Validate** to continue.</span></span>

5.  <span data-ttu-id="2b214-207">**닫기를** 클릭 하 여 설정 템플릿 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-207">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="2b214-208">UE-V 생성기 응용 프로그램을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-208">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="2b214-209">응용 프로그램에 대 한 설정 위치 템플릿의 유효성을 검사 한 후에는 서식 파일을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-209">After you validate the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="2b214-210">엔터프라이즈의 프로덕션 환경에 배치 하기 전에 먼저 템플릿을 랩 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-210">Deploy the template in a lab environment before you put it into a production environment in enterprise.</span></span>

## <a href="" id="share"></a><span data-ttu-id="2b214-211">서식 파일 갤러리를 사용 하 여 설정 위치 서식 파일 공유</span><span class="sxs-lookup"><span data-stu-id="2b214-211">Share Settings Location Templates with the Template Gallery</span></span>


<span data-ttu-id="2b214-212">Microsoft UE-V (User Experience Virtualization) 2.0 서식 파일 갤러리를 통해 관리자는 UE-V 설정 위치 템플릿을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-212">The Microsoft User Experience Virtualization (UE-V) 2.0 template gallery enables administrators to share their UE-V settings location templates.</span></span> <span data-ttu-id="2b214-213">갤러리에서 다른 사용자가 사용할 수 있도록 설정 위치 템플릿을 업로드 하 고 다른 사용자가 만든 서식 파일을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-213">In the gallery, you can upload your settings location templates for other users to use, and you can download templates that other users have created.</span></span> <span data-ttu-id="2b214-214">UE-V 서식 파일 갤러리는 [Microsoft TechNet에 있습니다.](https://go.microsoft.com/fwlink/p/?LinkId=246589)</span><span class="sxs-lookup"><span data-stu-id="2b214-214">The UE-V template gallery is located on Microsoft TechNet [here](https://go.microsoft.com/fwlink/p/?LinkId=246589).</span></span>

<span data-ttu-id="2b214-215">UE-V 템플릿 갤러리에서 설정 위치 템플릿을 공유 하기 전에 개인 정보나 회사 정보가 포함 되어 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-215">Before you share a settings location template on the UE-V template gallery, ensure it does not contain any personal or company information.</span></span> <span data-ttu-id="2b214-216">XML 뷰어를 사용 하 여 설정 위치 템플릿 파일의 내용을 열고 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-216">You can use any XML viewer to open and view the contents of a settings location template file.</span></span> <span data-ttu-id="2b214-217">서식 파일을 회사 외부의 모든 사용자와 공유 하기 전에 다음 서식 파일 값을 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-217">The following template values should be reviewed before you share a template with anyone outside your company.</span></span>

-   <span data-ttu-id="2b214-218">서식 파일 작성자 이름-서식 파일 작성자 이름에 대해 식별 되지 않는 일반 이름을 지정 하거나 템플릿에서이 데이터를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-218">Template Author Name – Specify a general, non-identifying name for the template author name or exclude this data from the template.</span></span>

-   <span data-ttu-id="2b214-219">서식 파일 저자 전자 메일 – 식별이 불가능 한 일반 서식 파일 작성 전자 메일을 지정 하거나 템플릿에서이 데이터를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-219">Template Author Email – Specify a general, non-identifying template author email or exclude this data from the template.</span></span>

<span data-ttu-id="2b214-220">UE-V 갤러리에서 다운로드 한 설정 위치 서식 파일을 배포 하기 전에 먼저 템플릿을 테스트 하 여 응용 프로그램 설정이 테스트 환경에서 올바르게 설정 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b214-220">Before you deploy any settings location template that you have downloaded from the UE-V gallery, you should first test the template to ensure that the application settings synchronize settings correctly in a test environment.</span></span>






## <span data-ttu-id="2b214-221">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2b214-221">Related topics</span></span>


[<span data-ttu-id="2b214-222">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="2b214-222">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="2b214-223">사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포</span><span class="sxs-lookup"><span data-stu-id="2b214-223">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





