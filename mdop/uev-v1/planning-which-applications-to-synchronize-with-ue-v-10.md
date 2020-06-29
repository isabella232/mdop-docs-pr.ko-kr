---
title: UE-V 1.0과 동기화할 응용 프로그램 계획
description: UE-V 1.0과 동기화할 응용 프로그램 계획
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812417"
---
# <span data-ttu-id="eea05-103">UE-V 1.0과 동기화할 응용 프로그램 계획</span><span class="sxs-lookup"><span data-stu-id="eea05-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="eea05-104">Microsoft UE-V (User Experience Virtualization)는 UE-V를 통해 캡처 및 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="eea05-105">UE-V는 미리 정의 된 설정 위치 템플릿의 집합을 포함 하며, 관리자는 엔터프라이즈에서 사용 되는 타사 또는 lob (기간 업무) 응용 프로그램에 대 한 사용자 지정 설정 위치 서식 파일을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="eea05-106">관리자는 UE-V 솔루션에 포함할 응용 프로그램을 고려할 때 사용자가 지정할 수 있는 설정과 응용 프로그램이 해당 설정을 저장 하는 방법 및 위치를 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="eea05-107">일부 응용 프로그램에는 사용자 지정할 수 있는 설정이 포함 되어 있지 않거나 정기적으로 사용자 지정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="eea05-108">또한 일부 응용 프로그램 설정은 여러 컴퓨터 또는 환경에서 안전 하 게 로밍할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="eea05-109">다음 조건에 맞는 설정을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="eea05-110">사용자가 액세스할 수 있는 위치에 저장 되는 설정</span><span class="sxs-lookup"><span data-stu-id="eea05-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="eea05-111">예를 들어 system32 또는 레지스트리의 외부 HKCU 섹션에 저장 된 설정을 동기화 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="eea05-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="eea05-112">특정 컴퓨터에 국한 되지 않는 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="eea05-113">예를 들어 네트워크 또는 하드웨어 구성을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="eea05-114">데이터 손상 위험 없이 컴퓨터 간에 동기화 될 수 있는 설정</span><span class="sxs-lookup"><span data-stu-id="eea05-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="eea05-115">예를 들어 데이터베이스 파일에 저장 된 설정을 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="eea05-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="eea05-116">UE-V에 포함 된 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="eea05-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="eea05-117">UE-V 응용 프로그램 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="eea05-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="eea05-118">UE-V 에이전트 설치 소프트웨어는 에이전트를 설치 하 고 공통 Microsoft 응용 프로그램에 대 한 기본 설정 위치 템플릿 그룹을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="eea05-119">이러한 설정 위치 템플릿은 다음 응용 프로그램에 대 한 설정 값을 캡처합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="eea05-120">응용 프로그램 범주</span><span class="sxs-lookup"><span data-stu-id="eea05-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="eea05-121">설명</span><span class="sxs-lookup"><span data-stu-id="eea05-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eea05-122">Microsoft Office 2010 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="eea05-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="eea05-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="eea05-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="eea05-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="eea05-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="eea05-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="eea05-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="eea05-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="eea05-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="eea05-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="eea05-133">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="eea05-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="eea05-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eea05-135">브라우저 옵션 (Internet Explorer 8, Internet Explorer 9 및 Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="eea05-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-136">즐겨찾기, 홈 페이지, 탭, 도구 모음</span><span class="sxs-lookup"><span data-stu-id="eea05-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eea05-137">Windows 액세서리</span><span class="sxs-lookup"><span data-stu-id="eea05-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-138">계산기, 메모장, 워드 패드</span><span class="sxs-lookup"><span data-stu-id="eea05-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="eea05-139">응용 프로그램은 응용 프로그램을 시작할 때 응용 프로그램에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="eea05-140">응용 프로그램이 닫힐 때 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="eea05-141">UE-V Windows 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="eea05-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="eea05-142">사용자 환경 가상화에는 다음 Windows 설정에 대 한 설정 값을 캡처하는 설정 위치 템플릿이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eea05-143">Windows 설정</span><span class="sxs-lookup"><span data-stu-id="eea05-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="eea05-144">설명</span><span class="sxs-lookup"><span data-stu-id="eea05-144">Description</span></span></th>
<th align="left"><span data-ttu-id="eea05-145">적용 기준</span><span class="sxs-lookup"><span data-stu-id="eea05-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="eea05-146">기본 상태</span><span class="sxs-lookup"><span data-stu-id="eea05-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eea05-147">바탕 화면 배경</span><span class="sxs-lookup"><span data-stu-id="eea05-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-148">현재 활성 상태인 바탕 화면 배경입니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-149">로그온, 잠금 해제, 원격 연결</span><span class="sxs-lookup"><span data-stu-id="eea05-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-150">설정됨</span><span class="sxs-lookup"><span data-stu-id="eea05-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eea05-151">접근성</span><span class="sxs-lookup"><span data-stu-id="eea05-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-152">접근성 및 입력 설정, 돋보기, 내레이터, 화상 키보드</span><span class="sxs-lookup"><span data-stu-id="eea05-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-153">로그온, 잠금 해제, 원격 연결</span><span class="sxs-lookup"><span data-stu-id="eea05-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-154">해제됨</span><span class="sxs-lookup"><span data-stu-id="eea05-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eea05-155">바탕 화면 설정</span><span class="sxs-lookup"><span data-stu-id="eea05-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-156">시작 메뉴 및 작업 표시줄 설정, 폴더 옵션, 기본 바탕 화면 아이콘, 추가 시계, 지역 및 언어 설정</span><span class="sxs-lookup"><span data-stu-id="eea05-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-157">로그온만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="eea05-158">해제됨</span><span class="sxs-lookup"><span data-stu-id="eea05-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="eea05-159">Windows 데스크톱 배경과 접근성 설정은 사용자가 로그온 하거나 컴퓨터를 잠그거나, 원격으로 다른 컴퓨터에 연결할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="eea05-160">에이전트는 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있거나 원격 연결이 끊어질 때 이러한 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="eea05-161">기본적으로 Windows 바탕 화면 배경 설정은 동일한 운영 체제 버전의 컴퓨터 간에 roamed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="eea05-162">Windows 데스크톱과 접근성 설정은 데스크톱이 사용자에 게 표시 되기 전에 로그온 할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="eea05-163">로그온 환경을 최적화 하기 위해 이러한 설정은 기본적으로 roamed 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="eea05-164">데스크톱 및 접근성 설정은 그룹 정책, PowerShell, WMI를 사용 하 여 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="eea05-165">UE-V는 다른 언어의 운영 체제 간에 설정 로밍을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="eea05-166">예를 들어, 영어와 독일어 간의 동기화는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="eea05-167">UE-V를 로밍 하는 모든 컴퓨터의 언어는 사용자 설정에 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="eea05-168">**참고**  Microsoft에서 제공 하는 설정 위치 서식 파일을 변경 하는 경우 사용자 환경 가상화가 지정 된 응용 프로그램 또는 Windows 설정 그룹에 대해 제대로 작동 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="eea05-169">의도 하지 않은 사용자 설정 구성 방지</span><span class="sxs-lookup"><span data-stu-id="eea05-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="eea05-170">사용자 환경 가상화는 새 사용자 설정 정보를 확인 하 고 설정 저장소 위치에서 해당 정보를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="eea05-171">이렇게 하면 다음과 같은 경우 로컬 컴퓨터에 설정이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="eea05-172">등록 된 UE-V 템플릿이 있는 응용 프로그램이 시작 될 때마다</span><span class="sxs-lookup"><span data-stu-id="eea05-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="eea05-173">사용자가 컴퓨터에 로그온 하는 경우</span><span class="sxs-lookup"><span data-stu-id="eea05-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="eea05-174">사용자가 컴퓨터의 잠금을 해제 하는 경우</span><span class="sxs-lookup"><span data-stu-id="eea05-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="eea05-175">UE-V를 설치한 원격 데스크톱 컴퓨터에 연결 하는 경우</span><span class="sxs-lookup"><span data-stu-id="eea05-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="eea05-176">UE-V을 컴퓨터 A 및 컴퓨터 B에 설치 하 고 응용 프로그램에 대 한 원하는 설정이 컴퓨터 A에 있는 경우 컴퓨터 A가 먼저 응용 프로그램을 열고 닫아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="eea05-177">컴퓨터 B에서 응용 프로그램을 열고 닫은 경우 컴퓨터 A의 응용 프로그램 설정이 컴퓨터 B의 응용 프로그램 설정과 동일 하 게 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="eea05-178">이 시나리오는 Windows 설정에도 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="eea05-179">컴퓨터 B의 Windows 설정이 컴퓨터 A의 Windows 설정과 동일 해야 하는 경우 사용자는 먼저 컴퓨터 A에 로그온 하 고 로그 아웃 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="eea05-180">원하는 사용자 설정이 잘못 된 순서로 적용 되는 경우 설정을 덮어쓴 컴퓨터에서 특정 응용 프로그램 또는 Windows 구성에 대 한 복원 작업을 수행 하 여 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="eea05-181">자세한 내용은 [ue-v 1.0와 동기화 된 응용 프로그램 및 Windows 설정 복원을](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eea05-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="eea05-182">사용자 지정 UE-V 설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="eea05-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="eea05-183">UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="eea05-184">테스트 환경에서 사용자 지정 설정 위치 템플릿을 만들고 테스트 한 후 엔터프라이즈의 컴퓨터에 설정 위치 템플릿을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="eea05-185">사용자 지정 설정 위치 템플릿은 ESD (엔터프라이즈 소프트웨어 배포) 메서드, 기본 설정 또는 UE-V 설정 템플릿 카탈로그를 구성 하는 등 기존 배포 인프라와 함께 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="eea05-186">ESD 또는 그룹 정책을 사용 하 여 배포 된 서식 파일은 UE-V WMI 또는 PowerShell을 사용 하 여 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eea05-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="eea05-187">사용자 지정 설정 위치 서식 파일에 대 한 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eea05-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="eea05-188">Lob (기간 업무) 응용 프로그램을 동기화할지 여부에 대 한 지침은 [ue-v 1.0의 lob (기간 업무) 응용 프로그램 평가에 대 한 검사 목록을](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eea05-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="eea05-189">관련 항목</span><span class="sxs-lookup"><span data-stu-id="eea05-189">Related topics</span></span>


[<span data-ttu-id="eea05-190">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="eea05-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="eea05-191">UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획</span><span class="sxs-lookup"><span data-stu-id="eea05-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="eea05-192">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="eea05-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





