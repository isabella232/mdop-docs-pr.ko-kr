---
title: Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 설정 위치 템플릿 관리
description: Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 설정 위치 템플릿 관리
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812881"
---
# <span data-ttu-id="c6094-103">Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 설정 위치 템플릿 관리</span><span class="sxs-lookup"><span data-stu-id="c6094-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="c6094-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1은 XML 설정 위치 템플릿을 사용 하 여 사용자 환경 가상화가 캡처 및 적용 하는 설정을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="c6094-105">UE-V는 표준 설정 위치 템플릿 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="c6094-106">또한 사용자 지정 설정 위치 템플릿을 만드는 데 사용할 수 있는 UE-V 생성기 도구가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="c6094-107">설정 위치 템플릿을 만들고 배포한 후에는 Windows PowerShell 및 WMI (Windows Management Instrumentation)를 사용 하 여 해당 템플릿을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="c6094-108">UE-V PowerShell cmdlet의 전체 목록은 [ue-v 2 Cmdlet 참조](https://go.microsoft.com/fwlink/p/?LinkId=393495) ()를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="c6094-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="c6094-109">Windows PowerShell을 사용 하 여 UE-V 2 설정 위치 템플릿 관리</span><span class="sxs-lookup"><span data-stu-id="c6094-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="c6094-110">UE-V의 WMI 및 Windows PowerShell 기능에는 설정 위치 템플릿을 사용, 사용 안 함, 등록, 업데이트 및 등록 취소 하는 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="c6094-111">이러한 기능을 사용 하 여 UE-V Agent를 사용 하 여 서식 파일을 등록, 업데이트 또는 등록 취소 하는 프로세스를 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="c6094-112">또한 WMI 및 Windows PowerShell 명령을 사용 하 여 수동으로 템플릿을 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="c6094-113">이러한 기능을 전자 소프트웨어 배포 솔루션, 그룹 정책 또는 스크립트와 같은 다른 자동화 된 배포 방법과 함께 사용 하면 해당 프로세스를 더 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="c6094-114">설정 위치 템플릿을 업데이트, 등록 또는 등록 취소 하려면 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="c6094-115">관리자 권한은 서식 파일을 사용, 사용 안 함 또는 나열할 때 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="c6094-116">Windows PowerShell을 사용 하 여 설정 위치 템플릿을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="c6094-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="c6094-117">관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="c6094-118">다음 Windows PowerShell cmdlet을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c6094-119">Windows PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="c6094-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="c6094-120">설명</span><span class="sxs-lookup"><span data-stu-id="c6094-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-121">컴퓨터에 등록 된 모든 설정 위치 템플릿을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-122">응용 프로그램 이름 또는 서식 파일 이름에 문자열이 포함 된 컴퓨터에 등록 되어 있는 모든 설정 위치 템플릿을 &lt; 나열 &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-123">서식 파일 ID에 문자열이 포함 된 컴퓨터에 등록 되어 있는 모든 설정 위치 템플릿을 나열 &lt; 합니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="c6094-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-124">응용 프로그램 또는 서식 파일 이름 또는 서식 파일 ID에 문자열이 포함 된 컴퓨터에 등록 되어 있는 모든 설정 위치 템플릿을 &lt; 나열 &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-125">서식 파일 ID에 따라 달라 지는 프로그램의 이름과 버전 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-126">Windows 앱의 유효 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-127">컴퓨터에 대해 구성 된 Windows 앱 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-128">현재 사용자에 대해 구성 된 Windows 앱 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-129">파일 경로에 상대 경로 및/또는 와일드 카드 문자를 사용 하 여 UE-V를 사용 하 여 하나 이상의 설정 위치 템플릿을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="c6094-130">템플릿을 등록 한 후에는 UE-V가 등록 된 템플릿이 있는 컴퓨터 간에 서식 파일에 정의 된 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-131">문자를 와일드 카드 문자로 해석할 수 없는 리터럴 경로를 사용 하 여 UE-V를 사용 하 여 하나 이상의 설정 위치 템플릿을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="c6094-132">템플릿을 등록 한 후에는 UE-V가 등록 된 템플릿이 있는 컴퓨터 간에 서식 파일에 정의 된 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-133">UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="c6094-134">템플릿이 등록 취소 되 면 UE-V는 더 이상 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-135">UE-V를 사용 하 여 모든 설정 위치 템플릿의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="c6094-136">템플릿이 등록 취소 되 면 UE-V는 더 이상 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-137">하나 이상의 설정 위치 템플릿을 최신 버전의 템플릿으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="c6094-138">파일 경로에 상대 경로 및/또는 와일드 카드 문자를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="c6094-139">새 서식 파일은 기존 서식 파일 보다 최신 버전 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-140">하나 이상의 설정 위치 템플릿을 최신 버전의 템플릿으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="c6094-141">문자를 와일드 카드 문자로 해석할 수 없는 경우 서식 파일의 전체 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="c6094-142">새 서식 파일은 기존 서식 파일 보다 최신 버전 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-143">컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-144">현재 사용자 Windows 앱 목록에서 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-145">컴퓨터 Windows 앱 목록에서 모든 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-146">현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-147">현재 사용자 Windows 앱 목록에서 모든 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-148">컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-149">컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-150">현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-151">컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-152">컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-153">현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-154">하나 이상의 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="c6094-155">상대 경로와 와일드 카드 문자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-156">하나 이상의 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="c6094-157">경로는 서식 파일에 대 한 전체 경로 여야 하지만 와일드 카드 문자는 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="c6094-158">UE-V Windows PowerShell 기능을 사용 하면 엔터프라이즈에 배포 된 설정 서식 파일 그룹을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="c6094-159">Windows PowerShell을 사용 하 여 서식 파일 그룹을 관리 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="c6094-160">Windows PowerShell을 사용 하 여 설정 위치 템플릿의 그룹을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="c6094-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c6094-161">원하는 설정 위치 템플릿을 수정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="c6094-162">설정 위치 템플릿을 수정 하거나 업데이트 하려는 경우 해당 설정 위치 템플릿을 로컬 컴퓨터에서 액세스할 수 있는 폴더에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="c6094-163">로컬 컴퓨터에서 관리자 권한이 있는 Windows PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="c6094-164">다음 명령을 입력 하 여 이전에 등록 된 모든 버전의 템플릿을 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="c6094-165">이 명령은 컴퓨터에 있는 모든 활성 서식 파일의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="c6094-166">다음 명령을 입력 하 여 업데이트 된 서식 파일을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="c6094-167">이 명령은 지정 된 서식 파일 폴더에 있는 모든 설정 위치 템플릿을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="c6094-168">Windows 앱 목록</span><span class="sxs-lookup"><span data-stu-id="c6094-168">Windows app list</span></span>

<span data-ttu-id="c6094-169">Windows 앱 목록에 Windows 앱을 나열 하 여 설정 동기화를 위해 앱을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="c6094-170">앱은 패키지 패밀리 이름 및 해당 앱에 대 한 설정 동기화를 사용할지 여부를 기준으로 목록에서 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="c6094-171">목록에 없는 기본 동기화 동작 설정과 함께 이러한 설정을 사용 하면 Windows 앱이 동기화 되는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="c6094-172">설치 된 Windows 앱의 패키지 패밀리 이름을 표시 하려면 Windows PowerShell 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="c6094-173">Windows PowerShell 명령 프롬프트에서 컴퓨터의 설정을 동기화 할 수 있는 Windows 앱 목록 (패키지 패밀리 이름, 사용 상태 및 활성화 된 원본)을 표시 하려면 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="c6094-174">Get-UevAppxPackage 속성 정의</span><span class="sxs-lookup"><span data-stu-id="c6094-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="c6094-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6094-175">DisplayName</span></span>**  
<span data-ttu-id="c6094-176">회사 설정 센터 응용 프로그램에서 사용자에 게 표시 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="c6094-177">속성이 `DisplayName` 속성에서 파생 됩니다 `PackageFamilyName` .</span><span class="sxs-lookup"><span data-stu-id="c6094-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="c6094-178">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="c6094-178">PackageFamilyName</span></span>**  
<span data-ttu-id="c6094-179">현재 사용자 용으로 설치 된 패키지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="c6094-180">설정됨</span><span class="sxs-lookup"><span data-stu-id="c6094-180">Enabled</span></span>**  
<span data-ttu-id="c6094-181">앱 설정이 동기화 되도록 구성 되었는지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="c6094-182">EnabledSource</span><span class="sxs-lookup"><span data-stu-id="c6094-182">EnabledSource</span></span>**  
<span data-ttu-id="c6094-183">앱을 사용 하거나 사용 하지 않도록 설정할 구성이 설정 된 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="c6094-184">사용할 수 있는 값은 *NotSet*, *LocalMachine*, *localuser*, *policymachine*, *policymachine*입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="c6094-185">NotSet</span><span class="sxs-lookup"><span data-stu-id="c6094-185">NotSet</span></span>**  
<span data-ttu-id="c6094-186">정책이이 앱을 동기화 하도록 구성 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="c6094-187">LocalMachine</span><span class="sxs-lookup"><span data-stu-id="c6094-187">LocalMachine</span></span>**  
<span data-ttu-id="c6094-188">사용 상태는 레지스트리의 로컬 컴퓨터 섹션에 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="c6094-189">LocalUser</span><span class="sxs-lookup"><span data-stu-id="c6094-189">LocalUser</span></span>**  
<span data-ttu-id="c6094-190">사용할 수 있는 상태는 레지스트리의 현재 사용자 섹션에 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="c6094-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="c6094-191">PolicyMachine</span></span>**  
<span data-ttu-id="c6094-192">사용 상태는 레지스트리의 로컬 컴퓨터 섹션의 정책 섹션에서 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="c6094-193">Windows 앱의 사용자 구성 목록을 가져오려면 Windows PowerShell 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="c6094-194">Windows 앱의 컴퓨터 구성 목록을 가져오려면 Windows PowerShell 명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="c6094-195">CurrentComputerUser 또는 컴퓨터 중 하나의 매개 변수를 사용 하는 경우 cmdlet은 사용자 또는 컴퓨터 수준에서 구성 된 Windows 앱 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="c6094-196">속성 정의</span><span class="sxs-lookup"><span data-stu-id="c6094-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="c6094-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6094-197">DisplayName</span></span>**  
<span data-ttu-id="c6094-198">회사 설정 센터 응용 프로그램에서 사용자에 게 표시 되는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="c6094-199">속성이 `DisplayName` 속성에서 파생 됩니다 `PackageFamilyName` .</span><span class="sxs-lookup"><span data-stu-id="c6094-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="c6094-200">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="c6094-200">PackageFamilyName</span></span>**  
<span data-ttu-id="c6094-201">현재 사용자 용으로 설치 된 패키지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="c6094-202">설정됨</span><span class="sxs-lookup"><span data-stu-id="c6094-202">Enabled</span></span>**  
<span data-ttu-id="c6094-203">지정 된 스위치 (즉, **사용자** 또는 **컴퓨터**)에 대해 앱 설정이 동기화 되도록 구성 되었는지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="c6094-204">설치됨</span><span class="sxs-lookup"><span data-stu-id="c6094-204">Installed</span></span>**  
<span data-ttu-id="c6094-205">현재 사용자에 대 한 PackageFamilyName가 설치 되어 있으면 True이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="c6094-206">WMI를 사용 하 여 UE-V 2 설정 위치 템플릿 관리</span><span class="sxs-lookup"><span data-stu-id="c6094-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="c6094-207">사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="c6094-208">관리자는 이러한 인터페이스를 사용 하 여 Windows PowerShell에서 설정 위치 템플릿을 관리 하 고 템플릿 관리 작업을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="c6094-209">WMI를 사용 하 여 설정 위치 템플릿을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="c6094-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="c6094-210">관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="c6094-211">다음 WMI 명령을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="c6094-212">설명</span><span class="sxs-lookup"><span data-stu-id="c6094-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-213">컴퓨터에 대해 등록 된 모든 설정 위치 템플릿을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-214">서식 파일 이름에 따라 달라 지는 프로그램의 이름과 버전 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-215">Windows 앱의 유효 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c6094-216">WmiObject-네임 스페이스 root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="c6094-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c6094-217">컴퓨터에 대해 구성 된 Windows 앱 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-218">현재 사용자에 대해 구성 된 Windows 앱 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-219">UE-V를 사용 하 여 설정 위치 템플릿을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-220">UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="c6094-221">서식 파일이 등록 취소 되 면 UE-V는 더 이상 컴퓨터 간에 서식 파일에 정의 된 설정을 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-222">UE-V를 사용 하 여 설정 위치 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="c6094-223">새 템플릿은 기존 버전과 최신 버전 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-224">컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-225">현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-226">UE-V를 사용 하 여 하나 이상의 설정 위치 템플릿을 사용할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-227">컴퓨터 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-228">현재 사용자 Windows 앱 목록에서 하나 이상의 Windows 앱을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-229">UE-V를 사용 하 여 설정 위치 템플릿을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-230">컴퓨터 Windows 앱 목록에서 Windows 앱을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-231">현재 사용자 Windows 앱 목록에서 Windows 앱을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c6094-232">지정 된 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="c6094-233">Windows PowerShell을 사용 하 여 UE-V 에이전트 배포</span><span class="sxs-lookup"><span data-stu-id="c6094-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="c6094-234">Windows PowerShell을 사용 하 여 UE-V 에이전트를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="c6094-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c6094-235">액세스 가능한 네트워크 공유에서 UE-V Agent 설치 패키지를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="c6094-236">참고</span><span class="sxs-lookup"><span data-stu-id="c6094-236">Note</span></span>**  
    <span data-ttu-id="c6094-237">AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="c6094-238">Windows Installer 패키지 AgentSetupx86.msi 및 AgentSetupx64.msi 각 아키텍처에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="c6094-239">나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="c6094-240">다음 Windows PowerShell 명령 중 하나를 사용 하 여 UE-V 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="c6094-241">**Ue-v에 대 한 제안이 있으십니까**?</span><span class="sxs-lookup"><span data-stu-id="c6094-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="c6094-242">[여기](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="c6094-243">**Ue-v 문제가**있나요?</span><span class="sxs-lookup"><span data-stu-id="c6094-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="c6094-244">[Ue-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6094-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="c6094-245">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c6094-245">Related topics</span></span>


[<span data-ttu-id="c6094-246">Windows PowerShell 및 WMI를 사용 하 여 UE-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="c6094-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="c6094-247">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="c6094-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









