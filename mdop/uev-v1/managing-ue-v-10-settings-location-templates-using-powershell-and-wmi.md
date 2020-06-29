---
title: PowerShell 및 WMI를 사용하여 UE-V 1.0 설정 위치 템플릿 관리
description: PowerShell 및 WMI를 사용하여 UE-V 1.0 설정 위치 템플릿 관리
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812492"
---
# <span data-ttu-id="484e5-103">PowerShell 및 WMI를 사용하여 UE-V 1.0 설정 위치 템플릿 관리</span><span class="sxs-lookup"><span data-stu-id="484e5-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="484e5-104">Microsoft UE-V (User Experience Virtualization)는 사용자 환경 가상화에 의해 캡처되고 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="484e5-105">UE-V는 표준 설정 위치 템플릿 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="484e5-106">또한 사용자 지정 설정 위치 템플릿을 만드는 데 사용할 수 있는 UE-V 생성기 도구가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="484e5-107">설정 위치 템플릿을 만들고 배포한 후에는 PowerShell 또는 WMI를 사용 하 여 해당 템플릿을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="484e5-108">WMI 및 PowerShell을 사용 하 여 설정 위치 템플릿 관리</span><span class="sxs-lookup"><span data-stu-id="484e5-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="484e5-109">UE-V의 WMI 및 PowerShell 기능에는 설정 위치 템플릿을 사용, 사용 안 함, 등록, 업데이트 및 등록 취소 하는 기능이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="484e5-110">이러한 기능을 사용 하 여 UE-V agent를 사용 하 여 서식 파일을 등록, 업데이트 또는 등록 취소 하는 프로세스를 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="484e5-111">또한 WMI 및 PowerShell 명령을 사용 하 여 수동으로 템플릿을 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="484e5-112">이러한 기능을 전자 소프트웨어 배포 솔루션, 그룹 정책 또는 스크립트와 같은 다른 자동화 된 배포 방법과 함께 사용 하면 해당 프로세스를 더 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="484e5-113">설정 위치 템플릿을 업데이트, 등록 또는 등록 취소 하려면 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="484e5-114">템플릿을 사용 하거나 사용 하지 않도록 설정 하는 데는 관리자 권한이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="484e5-115">PowerShell을 사용 하 여 설정 위치 템플릿을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="484e5-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="484e5-116">관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="484e5-117">**MICROSOFT Ue-v PowerShell** 모듈을 가져오려면 PowerShell 명령 프롬프트에서 다음 명령을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="484e5-118">다음 PowerShell cmdlet을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="484e5-119">PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="484e5-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="484e5-120">설명</span><span class="sxs-lookup"><span data-stu-id="484e5-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-121">가져오기-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-122">컴퓨터에 등록 된 모든 설정 위치 서식 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-123">등록-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-124">UE-V를 사용 하 여 설정 위치 템플릿을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="484e5-125">템플릿이 등록 되 면 UE-V는 등록 된 템플릿이 있는 컴퓨터 간에 템플릿에서 정의 된 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-126">등록 취소-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-127">UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="484e5-128">서식 파일이 등록 취소 되 면 UE-V는 더 이상 해당 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-129">업데이트 UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-130">최신 버전의 서식 파일을 사용 하 여 설정 위치 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="484e5-131">새 서식 파일에는 기존 버전이 이전 버전 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-132">사용 안 함-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-133">컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-134">사용-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-135">컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-136">테스트 UevTemplate</span><span class="sxs-lookup"><span data-stu-id="484e5-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-137">지정 된 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="484e5-138">UE-V PowerShell 기능을 사용 하 여 엔터프라이즈에 배포 된 설정 서식 파일 그룹을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="484e5-139">PowerShell을 사용 하 여 서식 파일 그룹을 관리 하려면 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="484e5-140">PowerShell을 사용 하 여 설정 위치 템플릿의 그룹을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="484e5-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="484e5-141">원하는 설정 위치 템플릿을 수정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="484e5-142">로컬 컴퓨터에서 액세스할 수 있는 폴더에 원하는 설정 위치 템플릿을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="484e5-143">로컬 컴퓨터에서 관리자 권한이 있는 Windows PowerShell 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="484e5-144">다음 명령을 입력 하 여 Microsoft UE-V PowerShell 모듈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="484e5-145">다음 명령을 입력 하 여 이전에 등록 된 모든 버전의 템플릿을 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="484e5-146">이렇게 하면 컴퓨터의 모든 활성 서식 파일이 등록 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="484e5-147">다음 명령을 입력 하 여 업데이트 된 서식 파일을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="484e5-148">이렇게 하면 지정 된 서식 파일 폴더에 있는 모든 설정 위치 템플릿이 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="484e5-149">사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="484e5-150">관리자는 이러한 인터페이스를 사용 하 여 Windows PowerShell에서 설정 위치 템플릿을 관리 하 고 템플릿 관리 작업을 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="484e5-151">WMI를 사용 하 여 설정 위치 템플릿을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="484e5-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="484e5-152">관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="484e5-153">다음 WMI 명령을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="484e5-154">PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="484e5-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="484e5-155">설명</span><span class="sxs-lookup"><span data-stu-id="484e5-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-156">WmiObject-네임 스페이스 root\Microsoft\UEV SettingsLocationTemplate | 선택-개체 TemplateId, TemplateName, 서식 버전, Enabled | 형식-테이블-Autosize</span><span class="sxs-lookup"><span data-stu-id="484e5-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-157">컴퓨터에 대해 등록 된 모든 설정 위치 서식 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-158">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name 레지스터-ArgumentList &lt; 템플릿 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="484e5-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-159">UE-V를 사용 하 여 설정 위치 템플릿을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-160">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; 템플릿 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="484e5-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-161">UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="484e5-162">서식 파일이 등록 취소 되 면 UE-V는 더 이상 해당 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-163">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; 템플릿 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="484e5-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-164">UE-V를 사용 하 여 설정 위치 템플릿을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-165">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; 템플릿 ID&gt;</span><span class="sxs-lookup"><span data-stu-id="484e5-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-166">UE-V를 사용 하 여 설정 위치 템플릿 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="484e5-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="484e5-167">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name 업데이트-ArgumentList &lt; 서식 파일 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="484e5-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-168">UE-V를 사용 하 여 설정 위치 템플릿을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="484e5-169">새 서식 파일에는 기존 버전 보다 높은 버전이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="484e5-170">WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name 유효성 검사-ArgumentList &lt; 서식 파일 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="484e5-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="484e5-171">지정 된 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="484e5-172">PowerShell을 사용 하 여 UE-V 에이전트를 배포 하는 방법</span><span class="sxs-lookup"><span data-stu-id="484e5-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="484e5-173">액세스 가능한 네트워크 공유에서 UE-V 설치 관리자 파일을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="484e5-174">**참고**  AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="484e5-175">각 아키텍처에 대해 Windows Installer 파일 버전, AgentSetupx86.msi 및 AgentSetupx64.msi를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="484e5-176">나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="484e5-177">다음 PowerShell 명령 중 하나를 사용 하 여 에이전트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="484e5-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="484e5-178">관련 항목</span><span class="sxs-lookup"><span data-stu-id="484e5-178">Related topics</span></span>


[<span data-ttu-id="484e5-179">PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리</span><span class="sxs-lookup"><span data-stu-id="484e5-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="484e5-180">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="484e5-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="484e5-181">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="484e5-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





