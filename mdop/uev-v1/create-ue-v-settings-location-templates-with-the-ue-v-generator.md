---
title: UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 만들기
description: UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 만들기
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826643"
---
# <span data-ttu-id="fab8a-103">UE-V 생성기를 사용하여 UE-V 설정 위치 템플릿 만들기</span><span class="sxs-lookup"><span data-stu-id="fab8a-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="fab8a-104">Microsoft UE-V (User Experience Virtualization)는 *설정 위치 템플릿을* 사용 하 여 사용자 컴퓨터 간에 응용 프로그램 설정을 로밍 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="fab8a-105">일부 표준 설정 위치 템플릿은 사용자 환경 가상화에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="fab8a-106">UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들거나 편집 하거나 확인할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="fab8a-107">UE-V 생성기는 응용 프로그램이 해당 설정을 저장 하는 위치를 검색 하 고 캡처하는 응용 프로그램을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="fab8a-108">모니터링 되는 응용 프로그램은 일반 응용 프로그램 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="fab8a-109">UE-V 생성기는 다음 응용 프로그램 종류에서 설정 위치 템플릿을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="fab8a-110">가상화 된 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fab8a-110">Virtualized applications</span></span>

-   <span data-ttu-id="fab8a-111">터미널 서비스를 통해 제공 되는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fab8a-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="fab8a-112">Java 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fab8a-112">Java applications</span></span>

-   <span data-ttu-id="fab8a-113">Windows 8 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="fab8a-113">Windows 8 applications</span></span>

<span data-ttu-id="fab8a-114">**참고**  UE-V 템플릿은 가상화 된 응용 프로그램 또는 터미널 서비스 응용 프로그램에서 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="fab8a-115">그러나 서식 파일을 사용 하 여 동기화 된 설정은 해당 응용 프로그램에 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="fab8a-116">VDI (가상 데스크톱 인프라) 및 터미널 서비스 응용 프로그램을 지 원하는 템플릿을 만들려면 UE-V Generator를 사용 하 여 Windows Installer 파일 (.msi) 버전의 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="fab8a-117">제외 된 위치</span><span class="sxs-lookup"><span data-stu-id="fab8a-117">Excluded Locations</span></span>**

<span data-ttu-id="fab8a-118">검색 프로세스는 사용자 컴퓨터 또는 환경 간에 원활 하 게 로밍 되지 않는 응용 프로그램 소프트웨어 파일을 일반적으로 저장 하는 위치를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="fab8a-119">다음은 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-119">The following are excluded:</span></span>

-   <span data-ttu-id="fab8a-120">HKEY \ _CURRENT \ _USER 로그온 한 사용자가 값을 쓸 수 없는 레지스트리 키 및 파일</span><span class="sxs-lookup"><span data-stu-id="fab8a-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="fab8a-121">HKEY _CURRENT \ _USER Windows 운영 체제의 핵심 기능과 관련 된 레지스트리 키 및 파일</span><span class="sxs-lookup"><span data-stu-id="fab8a-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="fab8a-122">HKEY \ _LOCAL \ _MACHINE 하이브에 있는 모든 레지스트리 키</span><span class="sxs-lookup"><span data-stu-id="fab8a-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="fab8a-123">Program Files 디렉터리에 있는 파일</span><span class="sxs-lookup"><span data-stu-id="fab8a-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="fab8a-124">사용자 \\ [사용자 이름 \] \\ AppData에 있는 파일은 다음을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="fab8a-125">% Systemroot%에 위치한 Windows 운영 체제 파일</span><span class="sxs-lookup"><span data-stu-id="fab8a-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="fab8a-126">이러한 제외 위치에 저장 된 레지스트리 키 및 파일이 응용 프로그램 설정을 로밍 하기 위해 필요한 경우 관리자는 템플릿 만들기 프로세스 중에 설정 위치 템플릿에 위치를 수동으로 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="fab8a-127">UE-V 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="fab8a-127">Create UE-V templates</span></span>


<span data-ttu-id="fab8a-128">UE-V 생성기를 사용 하 여 lob (기간 업무) 응용 프로그램 또는 다른 응용 프로그램에 대 한 설정 위치 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="fab8a-129">응용 프로그램의 템플릿을 만든 후에는 사용자가 해당 응용 프로그램에 대 한 설정을 로밍할 수 있도록 템플릿을 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="fab8a-130">UE-V 생성기를 사용 하 여 UE-V 설정 위치 템플릿을 만들려면</span><span class="sxs-lookup"><span data-stu-id="fab8a-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="fab8a-131">**시작**을 클릭 하 고 **모든 프로그램**, **microsoft 사용자 환경 가상화**를 차례로 클릭 한 다음 **microsoft 사용자 환경 가상화 생성기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="fab8a-132">**설정 위치 서식 파일 만들기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="fab8a-133">응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-133">Specify the application.</span></span> <span data-ttu-id="fab8a-134">설정 위치 템플릿을 만들려는 응용 프로그램 (.exe) 또는 응용 프로그램 바로 가기 (.lnk)의 파일 경로를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="fab8a-135">명령줄 인수 (있는 경우) 및 작업 디렉터리 (있는 경우)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="fab8a-136">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="fab8a-137">**참고**  응용 프로그램이 시작 되기 전에 시스템에서 **사용자 계정 컨트롤**을 확인 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="fab8a-138">사용 권한은 응용 프로그램이 설정을 저장 하는 데 사용 하는 레지스트리와 파일 위치를 모니터링 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="fab8a-139">응용 프로그램이 시작 되 면 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-139">After the application starts, close the application.</span></span> <span data-ttu-id="fab8a-140">UE-V 생성기는 응용 프로그램에서 해당 설정을 저장 하는 위치를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="fab8a-141">프로세스가 완료 되 면 **다음** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="fab8a-142">해당 레지스트리 설정 위치 및이 응용 프로그램에 대해 로밍할 적절 한 설정 파일 위치 옆에 있는 확인란을 검토 하 고 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="fab8a-143">목록에는 설정 위치에 대 한 다음 두 가지 범주가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="fab8a-144">**표준**: HKEY \ _CURRENT \ _USER 키 또는 \\ **사용자** \\ [사용자 이름 \ \ **AppData**  \\  **로밍**아래에 있는 파일 폴더에 저장 된 응용 프로그램 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="fab8a-145">UE-V 생성기에는 이러한 설정이 기본적으로 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="fab8a-146">**비표준**: 설정 데이터 저장소에 대 한 모범 사례에 지정 된 위치 외부에 저장 되는 응용 프로그램 설정 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="fab8a-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="fab8a-147">여기에는 **사용자** \\ [사용자 이름 \ \ \ \ **AppData**의 파일 및 폴더가 포함 됩니다  \\  **Local**.</span><span class="sxs-lookup"><span data-stu-id="fab8a-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="fab8a-148">이러한 위치를 검토 하 여 설정 위치 템플릿에 포함할 것인지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="fab8a-149">위치 확인란을 선택 하 여 해당 항목을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="fab8a-150">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="fab8a-151">설정 위치 템플릿의 **속성**, **레지스트리** 위치 및 **파일** 위치를 검토 하 고 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="fab8a-152">**속성** 탭에서 다음 속성을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="fab8a-153">**응용 프로그램 이름**: program files 속성에 대 한 설명으로 작성 된 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="fab8a-154">**프로그램 이름**: 프로그램 파일 속성에서 가져온 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="fab8a-155">이 이름에는 일반적으로 .exe 확장명이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="fab8a-156">**제품 버전**: 응용 프로그램의 .exe 파일에 대 한 제품 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="fab8a-157">이 속성은 파일 버전과 함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="fab8a-158">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-158">This property accepts a major version number.</span></span> <span data-ttu-id="fab8a-159">이 속성이 비어 있으면 설정 위치 템플릿이 모든 제품 버전에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="fab8a-160">**파일 버전**: 응용 프로그램의 the.exe 파일에 대 한 파일 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="fab8a-161">이 속성은 제품 버전과 함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="fab8a-162">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-162">This property accepts a major version number.</span></span> <span data-ttu-id="fab8a-163">이 속성이 비어 있으면 설정 위치 템플릿이 모든 버전의 프로그램에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="fab8a-164">**서식 파일 만든이 이름** (선택 사항): 설정 위치 템플릿 작성자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="fab8a-165">**서식 파일 저자 전자 메일** (선택 사항): 설정 위치 템플릿 작성자의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="fab8a-166">**레지스트리** 탭에는 설정 위치 템플릿에 포함 된 레지스트리 위치의 **키** 와 **범위가** 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="fab8a-167">**작업** 드롭다운 메뉴를 사용 하 여 레지스트리 위치를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="fab8a-168">작업에는 새 키 추가, 기존 키의 이름 또는 범위 편집, 키 삭제, 키가 있는 레지스트리 검색 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="fab8a-169">**모든 설정** 범위를 사용 하 여 지정 된 키의 모든 레지스트리 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="fab8a-170">**모든 설정 및 하위 키** 를 사용 하 여 지정 된 키, 하위 키 및 하위 키 설정의 모든 레지스트리 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="fab8a-171">**파일** 탭에는 설정 위치 템플릿에 포함 된 파일 위치의 파일 경로와 파일 마스크가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="fab8a-172">**작업** 드롭다운 메뉴를 사용 하 여 파일 위치를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="fab8a-173">파일 위치에 대 한 작업에는 새 파일 또는 폴더 위치 추가, 기존 파일 또는 폴더의 범위 편집, 파일 또는 폴더 삭제, Windows 탐색기에서 선택한 위치 열기 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="fab8a-174">지정 된 폴더의 모든 파일을 포함 하려면 파일 마스크를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="fab8a-175">컴퓨터에서 설정 위치 서식 파일 **만들기** 및 저장을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="fab8a-176">**닫기를** 클릭 하 여 설정 템플릿 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="fab8a-177">UE-V 생성기 응용 프로그램을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="fab8a-178">응용 프로그램에 대 한 설정 위치 템플릿을 만든 후에는 해당 템플릿을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="fab8a-179">엔터프라이즈에서 프로덕션에 게시 하기 전에 먼저 템플릿을 랩 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="fab8a-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="fab8a-180">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fab8a-180">Related topics</span></span>


[<span data-ttu-id="fab8a-181">사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업</span><span class="sxs-lookup"><span data-stu-id="fab8a-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="fab8a-182">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="fab8a-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





