---
title: 그룹 정책 개체를 사용하여 UE-V 구성
description: 그룹 정책 개체를 사용하여 UE-V 구성
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826698"
---
# <span data-ttu-id="4ca97-103">그룹 정책 개체를 사용하여 UE-V 구성</span><span class="sxs-lookup"><span data-stu-id="4ca97-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="4ca97-104">일부 Microsoft UE-V (사용자 환경 가상화) 그룹 정책 설정은 컴퓨터에 대해 정의 될 수 있으며 다른 사용자를 위해 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="4ca97-105">컴퓨터 또는 사용자에 대해 UE-V 에이전트 구성 정책 설정을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="4ca97-106">UE-V 그룹 정책 ADMX 파일을 설치 하는 방법에 대 한 자세한 내용은 [Ue-v 그룹 정책 Admx 템플릿 설치](installing-the-ue-v-group-policy-admx-templates.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ca97-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="4ca97-107">UE-V에 대해 다음 정책 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4ca97-108">정책 설정 이름</span><span class="sxs-lookup"><span data-stu-id="4ca97-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="4ca97-109">대상</span><span class="sxs-lookup"><span data-stu-id="4ca97-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="4ca97-110">정책 설정 설명</span><span class="sxs-lookup"><span data-stu-id="4ca97-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="4ca97-111">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="4ca97-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4ca97-112">사용자 환경 가상화 사용 (UE-V)</span><span class="sxs-lookup"><span data-stu-id="4ca97-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-113">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="4ca97-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-114">이 정책 설정을 통해 UE-V (User Experience Virtualization)를 사용 하거나 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-115">이 정책 설정을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4ca97-116">설정 저장소 경로</span><span class="sxs-lookup"><span data-stu-id="4ca97-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-117">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="4ca97-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-118">이 정책 설정은 사용자 설정이 저장 되는 위치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-119">\Server\SettingsShare%username%.와 같은 UNC (범용 명명 규칙) 경로 및 변수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4ca97-120">설정 서식 파일 카탈로그 경로</span><span class="sxs-lookup"><span data-stu-id="4ca97-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-121">컴퓨터만</span><span class="sxs-lookup"><span data-stu-id="4ca97-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-122">이 정책 설정은 사용자 지정 설정 위치 템플릿이 저장 되는 위치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="4ca97-123">이 정책 설정은 또한 UE-V agent를 사용 하 여 설치 된 기본 Microsoft 템플릿을 바꾸는 데 카탈로그를 사용할지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-124">\Server\TemplateShare 또는 컴퓨터의 폴더 위치와 같은 UNC (범용 명명 규칙) 경로를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="4ca97-125">기본 Microsoft 서식 파일을 바꾸려면 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4ca97-126">오프 라인 파일을 사용 하지 않음</span><span class="sxs-lookup"><span data-stu-id="4ca97-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-127">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="4ca97-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-128">이 정책 설정을 통해 UE-V가 Windows 오프 라인 파일 기능을 사용할지 여부를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="4ca97-129">이 정책 설정을 사용 하면 사용자 설정 가져오기가 지연 되는 경우 알림을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-130">오프 라인 파일을 사용 하지 않도록 UE-V Agent를 구성 하려면이 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="4ca97-131">설정 가져오기가 지연 되는 경우 알림을 제공 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="4ca97-132">알림이 나타나기 전에 대기할 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4ca97-133">동기화 시간 제한</span><span class="sxs-lookup"><span data-stu-id="4ca97-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-134">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="4ca97-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-135">이 정책 설정은 원격 설정 위치에서 사용자 설정을 검색할 때 컴퓨터가 시간 초과 되기 전에 대기 하는 시간 (밀리초)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="4ca97-136">원격 저장소 위치를 사용할 수 없는 경우 응용 프로그램 시작이이 시간 (밀리초) 만큼 지연 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-137">기본 설정 동기화 시간 제한을 밀리초로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="4ca97-138">기본 값인 2000 밀리초입니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4ca97-139">패키지 크기 경고 임계값</span><span class="sxs-lookup"><span data-stu-id="4ca97-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-140">컴퓨터 및 사용자</span><span class="sxs-lookup"><span data-stu-id="4ca97-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-141">이 정책 설정을 통해 UE-V agent가 설정 패키지 파일 크기가 정의 된 임계값에 도달할 때 보고 하도록 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-142">설정 패키지 크기 (kb)에 대 한 기본 설정 임계값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="4ca97-143">기본적으로 UE-V agent에는 패키지 파일 크기 임계값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4ca97-144">로밍 응용 프로그램 설정</span><span class="sxs-lookup"><span data-stu-id="4ca97-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-145">사용자만</span><span class="sxs-lookup"><span data-stu-id="4ca97-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-146">이 정책 설정은 응용 프로그램의 사용자 설정 로밍을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-147">컴퓨터 간에 로밍 되는 Windows 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="4ca97-148">기본적으로 UE-V를 통해 설정 템플릿이 제공 하는 응용 프로그램의 사용자 설정은 컴퓨터 간에 roamed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4ca97-149">로밍 Windows 설정</span><span class="sxs-lookup"><span data-stu-id="4ca97-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-150">사용자만</span><span class="sxs-lookup"><span data-stu-id="4ca97-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-151">이 정책 설정은 Windows 설정의 로밍을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4ca97-152">컴퓨터 간에 로밍할 응용 프로그램을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="4ca97-153">기본적으로 Windows 테마는 동일한 운영 체제 버전의 컴퓨터 간에 roamed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="4ca97-154">Windows 데스크톱 설정 및 접근성 설정은 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="4ca97-155">컴퓨터 대상 정책을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="4ca97-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="4ca97-156">UE-V 컴퓨터에 대 한 그룹 정책을 관리 하는 도메인 컨트롤러 컴퓨터의 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="4ca97-157">**컴퓨터 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="4ca97-158">편집할 정책 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="4ca97-159">사용자 대상 정책을 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="4ca97-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="4ca97-160">UE-V (Microsoft 데스크톱 최적화 팩)의 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) 도구를 사용 합니다. i V m에 대 한 그룹 정책을 관리 하는 도메인 컨트롤러 컴퓨터의 MDOP</span><span class="sxs-lookup"><span data-stu-id="4ca97-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="4ca97-161">**사용자 구성**으로 이동 하 고, **정책을**선택 하 고, **관리 템플릿을**선택 하 고, **Windows 구성 요소**를 클릭 한 다음 **Microsoft 사용자 환경 가상화**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="4ca97-162">편집한 정책 설정을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-162">Select the policy setting edited.</span></span>

<span data-ttu-id="4ca97-163">UE-V agent는 다음 우선 순위를 사용 하 여 동기화를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="4ca97-164">UE-V 설정의 우선 순위 순서</span><span class="sxs-lookup"><span data-stu-id="4ca97-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="4ca97-165">그룹 정책에서 관리 하는 사용자 대상 설정-이러한 구성 설정은 아래에 있는 그룹 정책에 의해 레지스트리 키에 저장 됩니다 `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4ca97-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="4ca97-166">그룹 정책에서 관리 하는 컴퓨터 대상 설정-이러한 구성 설정은 그룹 정책에 따라 레지스트리 키에 저장 됩니다 `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4ca97-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="4ca97-167">PowerShell 또는 WMI를 사용 하 여 현재 사용자가 정의한 구성 설정-이러한 구성 설정은 UE-V agent가 다음 레지스트리 위치에 저장 `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="4ca97-168">PowerShell 또는 WMI를 사용 하 여 컴퓨터에 대해 정의 된 구성 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4ca97-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="4ca97-169">이러한 구성 설정은의 UE-V agent에 저장 됩니다 `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4ca97-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="4ca97-170">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4ca97-170">Related topics</span></span>


[<span data-ttu-id="4ca97-171">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="4ca97-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="4ca97-172">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="4ca97-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





