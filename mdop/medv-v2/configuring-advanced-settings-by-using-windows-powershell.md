---
title: Windows PowerShell을 사용하여 고급 설정 구성
description: Windows PowerShell을 사용하여 고급 설정 구성
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827393"
---
# <span data-ttu-id="3df27-103">Windows PowerShell을 사용하여 고급 설정 구성</span><span class="sxs-lookup"><span data-stu-id="3df27-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="3df27-104">사용자가 만드는 MED-V 작업 영역 패키지에는 MED-V 작업 영역 패키지를 테스트 하 고 배포 하기 전에 편집할 수 있는 Windows PowerShell 스크립트 (ps1) 파일이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="3df27-105">이 섹션에서는 MED-V 작업 영역을 배포 하기 전에 Windows PowerShell을 사용 하 여 MED-V 구성 설정을 관리 하는 데 도움이 되는 정보 및 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="3df27-106">MED-V에 Windows PowerShell Cmdlet 사용</span><span class="sxs-lookup"><span data-stu-id="3df27-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="3df27-107">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에서 다음 Windows PowerShell cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="3df27-108">새-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="3df27-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="3df27-109">내보내기-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="3df27-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="3df27-110">새 MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="3df27-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="3df27-111">내보내기-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="3df27-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="3df27-112">MED-V 용 Windows PowerShell cmdlet에 액세스 하려면 Windows PowerShell을 열고 다음 명령을 입력 하 여 MED-V 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="3df27-113">모듈을 가져온 후 표준 Windows PowerShell 도움말 명령, **매뉴얼** 또는 **도움말**을 사용 하 여 cmdlet에 대 한 인라인 도움말에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="3df27-114">예를 들어 사용할 수 있는 전체 매개 변수 목록을 비롯 하 여 **새 MedvConfiguration** cmdlet에 대 한 설명에 액세스 하려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="3df27-115">특정 매개 변수에 대 한 도움말을 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="3df27-116">예를 들어 VmMemory 매개 변수에 대 한 도움말을 보려면 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="3df27-117">모든 MED-V 구성 설정 및 기본값 목록을 보려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="3df27-118">모든 MED-V 구성 설정과 현재 값의 목록을 보려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="3df27-119">사용자 지정 설정을 사용 하 여 MED-V 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="3df27-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="3df27-120">MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역 패키지를 성공적으로 만든 후에는 포장기 파일을 저장 하기 위해 지정한 폴더에 Windows PowerShell 스크립트가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="3df27-121">이 스크립트의 내용에는 편집할 수 있는 사용 가능한 일부 MED-V 구성 설정이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="3df27-122">이러한 단계를 따라 Windows PowerShell에서 스크립트를 사용자 지정한 다음이를 실행 하 여 새 설정으로 MED-V 작업 영역을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="3df27-123">**중요**  관리 자격 증명으로 Windows PowerShell을 실행 하 고 Windows PowerShell 실행 정책이 스크립트 실행을 허용 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="3df27-124">MED-V 작업 영역 포장기에서 생성 한 Windows PowerShell 스크립트를 편집 하거나 원하는 구성 설정으로 새 스크립트를 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="3df27-125">관리 자격 증명을 사용 하 여 Windows PowerShell을 실행 하 고 명령 프롬프트에서 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="3df27-126">이 명령은 Windows PowerShell 스크립트를 실행 하 고 **새** med-v 작업 영역 cmdlet을 실행 하 여 새 med-v workspace 패키지를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="3df27-127">새 포장기 파일은 MED-V 작업 영역 포장기 파일을 저장 하기 위해 원래 지정 된 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="3df27-128">이 cmdlet에 대 한 추가 도움말은 Windows PowerShell 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3df27-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="3df27-129">레지스트리 파일에 MED-V 구성 내보내기</span><span class="sxs-lookup"><span data-stu-id="3df27-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="3df27-130">MED-V 작업 영역이 설치 된 후 MED-V 구성 설정을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="3df27-131">**새-MedvConfiguration** cmdlet을 사용 하 여 변경 하려는 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="3df27-132">예를 들어 가상 컴퓨터 메모리 설정을 변경 하는 레지스트리 파일을 만들려면 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="3df27-133">호스트 컴퓨터에서 MED-V 작업 영역으로 결과 레지스트리 파일을 가져와 새 구성 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3df27-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="3df27-134">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3df27-134">Related topics</span></span>


[<span data-ttu-id="3df27-135">MED-V 작업 영역 구성 설정 관리</span><span class="sxs-lookup"><span data-stu-id="3df27-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="3df27-136">MED-V 작업 영역 패키지 테스트 및 배포</span><span class="sxs-lookup"><span data-stu-id="3df27-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





