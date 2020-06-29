---
title: System Center Configuration Manager 2012에서 UE-V 2. x 구성
description: System Center Configuration Manager 2012에서 UE-V 2. x 구성
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824408"
---
# <span data-ttu-id="43eca-103">System Center Configuration Manager 2012에서 UE-V 2. x 구성</span><span class="sxs-lookup"><span data-stu-id="43eca-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="43eca-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1과 필요한 기능을 설치한 후에는 UE-V를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="43eca-105">UE-V 구성 팩은 관리자가 System Center Configuration Manager 2012 SP1 이상의 규정 준수 설정 기능을 사용 하 여 UE-V 및 Configuration Manager가 설치 된 사이트에서 일관 된 구성을 적용할 수 있는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="43eca-106">UE-V 구성 팩 지원 되는 기능</span><span class="sxs-lookup"><span data-stu-id="43eca-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="43eca-107">UE-V 구성 팩에는 다음 작업을 수행 하는 도구가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="43eca-108">UE-V 설정 위치 템플릿 배포 기준을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="43eca-109">등록 또는 등록이 취소 되도록 UE-V 템플릿 정의</span><span class="sxs-lookup"><span data-stu-id="43eca-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="43eca-110">서식 파일이 추가 되거나 업데이트 될 때 UE-V 템플릿 구성 항목 및 초기 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="43eca-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="43eca-111">표준 구성 항목 수정을 사용 하 여 UE-V 템플릿 배포 및 등록</span><span class="sxs-lookup"><span data-stu-id="43eca-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="43eca-112">이 설정을 설정 하거나 해제 하려면 UE-V 에이전트 정책 구성 항목을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="43eca-113">최대 패키지 크기</span><span class="sxs-lookup"><span data-stu-id="43eca-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-114">Windows 앱 동기화 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="43eca-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-115">응용 프로그램 시작 시 동기화 대기</span><span class="sxs-lookup"><span data-stu-id="43eca-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="43eca-116">가져오기 지연 설정</span><span class="sxs-lookup"><span data-stu-id="43eca-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-117">목록에 없는 Windows 앱 동기화</span><span class="sxs-lookup"><span data-stu-id="43eca-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-118">로그온 할 때 동기화 대기</span><span class="sxs-lookup"><span data-stu-id="43eca-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="43eca-119">설정 가져오기 알림</span><span class="sxs-lookup"><span data-stu-id="43eca-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-120">IT 연락처 URL</span><span class="sxs-lookup"><span data-stu-id="43eca-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-121">동기화 시간 초과 대기</span><span class="sxs-lookup"><span data-stu-id="43eca-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="43eca-122">설정 저장소 경로</span><span class="sxs-lookup"><span data-stu-id="43eca-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-123">설명 텍스트에 문의</span><span class="sxs-lookup"><span data-stu-id="43eca-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-124">설정 서식 파일 카탈로그 경로</span><span class="sxs-lookup"><span data-stu-id="43eca-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="43eca-125">동기화 방법</span><span class="sxs-lookup"><span data-stu-id="43eca-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-126">트레이 아이콘 사용</span><span class="sxs-lookup"><span data-stu-id="43eca-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-127">UE-V agent 서비스 시작/중지</span><span class="sxs-lookup"><span data-stu-id="43eca-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="43eca-128">Sync 메서드</span><span class="sxs-lookup"><span data-stu-id="43eca-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-129">첫 번째 사용 알림</span><span class="sxs-lookup"><span data-stu-id="43eca-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="43eca-130">설정을 로밍할 Windows 앱 정의</span><span class="sxs-lookup"><span data-stu-id="43eca-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="43eca-131">동기화 시간 제한</span><span class="sxs-lookup"><span data-stu-id="43eca-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="43eca-132">UE-V가 실행 되 고 있는지 확인 하 여 준수 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="43eca-133">UE-V 에이전트 정책 구성 항목 생성</span><span class="sxs-lookup"><span data-stu-id="43eca-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="43eca-134">모든 UE-V Agent 정책 및 구성은 UevAgentPolicyGenerator.exe 도구를 사용 하 여 생성 된 단일 구성 항목을 통해 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="43eca-135">이 도구는 XML 구성 파일에서 원하는 구성을 읽고 컴퓨터를 준수 하도록 하는 데 필요한 검색 및 업데이트 관리 설정을 포함 하는 CI를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="43eca-136">UE-V Agent 정책 구성 항목 CAB 파일은 다음 매개 변수를 포함 하는 UevTemplateBaselineGenerator.exe 명령줄 도구를 사용 하 여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="43eca-137">사이트 &lt; 사이트 코드&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="43eca-138">PolicyName &lt; name &gt; 선택 사항: "Ue-v Agent 정책"이 없는 경우 기본값을</span><span class="sxs-lookup"><span data-stu-id="43eca-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="43eca-139">PolicyDescription &lt; description &gt; (선택 사항): 설명이 없는 경우 설명을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="43eca-140">CabFilePath &lt; 구성 항목에 대 한 전체 경로입니다. CAB 파일&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="43eca-141">&lt;에이전트 구성 XML 파일의 configurationfile 전체 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="43eca-142">**참고**  이 스크립트를 환경에서 실행할 수 있도록 PowerShell 실행 정책을 변경 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="43eca-143">Configuration Manager 콘솔에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="43eca-144">**관리 &gt; 클라이언트 설정 &gt; 속성** 선택</span><span class="sxs-lookup"><span data-stu-id="43eca-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="43eca-145">**사용자 에이전트** 탭에서 **PowerShell 실행 정책을** **Bypass** 으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="43eca-146">첫 번째 UE-V-V 정책 구성 항목 만들기</span><span class="sxs-lookup"><span data-stu-id="43eca-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="43eca-147">UE-V Config Pack 설치 디렉터리의 기본 설정 구성 파일을 ConfigMgr 관리 콘솔에 표시 되는 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="43eca-148">기본 구성 파일에는 다음 5 개 섹션이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="43eca-149">컴퓨터 정책</span><span class="sxs-lookup"><span data-stu-id="43eca-149">Computer Policy</span></span>**  
    <span data-ttu-id="43eca-150">모든 UE-V 컴퓨터 수준 설정</span><span class="sxs-lookup"><span data-stu-id="43eca-150">All UE-V machine level settings.</span></span> <span data-ttu-id="43eca-151">DesiredState 특성은 다음이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="43eca-152">레지스트리에 값이 할당 되도록 **설정**</span><span class="sxs-lookup"><span data-stu-id="43eca-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="43eca-153">설정을 제거 하 여 **지우기**</span><span class="sxs-lookup"><span data-stu-id="43eca-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="43eca-154">**관리 되지 않는** 경우 구성 항목이 현재 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="43eca-155">이 섹션에서는 줄을 제거 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="43eca-155">Do not remove lines from this section.</span></span> <span data-ttu-id="43eca-156">대신, Configuration Manager에서 현재 값 또는 기본값을 변경 하지 않도록 하려면 DesiredState를 ' 관리 되지 않음 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="43eca-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="43eca-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="43eca-158">모든 UE-V 사용자 수준 설정</span><span class="sxs-lookup"><span data-stu-id="43eca-158">All UE-V user level settings.</span></span> <span data-ttu-id="43eca-159">이러한 항목은 사용자의 컴퓨터 설정 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="43eca-160">DesiredState 특성은 다음이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="43eca-161">레지스트리에 값이 할당 되도록 **설정**</span><span class="sxs-lookup"><span data-stu-id="43eca-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="43eca-162">설정을 제거 하 여 **지우기**</span><span class="sxs-lookup"><span data-stu-id="43eca-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="43eca-163">**관리 되지 않는** 경우 구성 항목이 현재 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="43eca-164">이 섹션에서는 줄을 제거 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="43eca-164">Do not remove lines from this section.</span></span> <span data-ttu-id="43eca-165">대신, Configuration Manager에서 현재 값 또는 기본값을 변경 하지 않도록 하려면 DesiredState를 ' 관리 되지 않음 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="43eca-166">서비스</span><span class="sxs-lookup"><span data-stu-id="43eca-166">Services</span></span>**  
    <span data-ttu-id="43eca-167">이 섹션의 항목은 서비스 작업을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-167">Entries in this section control service operation.</span></span> <span data-ttu-id="43eca-168">기본 구성 파일에는 UevAgentService에 대 한 단일 항목이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="43eca-169">DesiredState 특성을 **실행** 또는 **중지**로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="43eca-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="43eca-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="43eca-171">모든 컴퓨터 수준 Windows 앱 동기화 설정</span><span class="sxs-lookup"><span data-stu-id="43eca-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="43eca-172">이 섹션에 나열 된 각 PackageFamilyName에는 DesiredState를 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="43eca-173">설정을 로밍할 수 **있도록 설정 됨**</span><span class="sxs-lookup"><span data-stu-id="43eca-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="43eca-174">설정을 로밍 하는 것을 방지 하려면 **사용 안 함**</span><span class="sxs-lookup"><span data-stu-id="43eca-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="43eca-175">UE-V 컨트롤에서 항목을 제거 하도록 **선택 취소**</span><span class="sxs-lookup"><span data-stu-id="43eca-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="43eca-176">PowerShell cmdlet GetAppxPackage를 사용 하 여 볼 수 있는 설치 된 Windows 앱의 목록을 기반으로이 섹션에 추가 줄을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="43eca-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="43eca-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="43eca-178">개별 사용자에 대 한 컴퓨터 설정을 재정의 하는 설정이 있는 Windows8AppsComputerPolicy와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="43eca-179">원하는 상태 및 값 필드를 변경 하 여 구성 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="43eca-180">ConfigMgr 관리 콘솔을 실행 하는 컴퓨터에서이 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="43eca-181">ConfigMgr 콘솔 또는 PowerShell Import를 사용 하 여 CAB 파일 가져오기-CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="43eca-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="43eca-182">UE-V 정책 구성 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="43eca-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="43eca-183">원하는 상태 및 값 필드를 변경 하 여 구성 파일을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="43eca-184">3 단계의 명령을 실행 하 여 [첫 번째 ue-v-V 정책 구성 항목 만들기](#create)</span><span class="sxs-lookup"><span data-stu-id="43eca-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="43eca-185">PolicyName 매개 변수를 사용 하 여 이름을 변경한 경우 동일한 이름을 입력 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="43eca-186">CAB 파일을 다시 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-186">Reimport the CAB file.</span></span> <span data-ttu-id="43eca-187">ConfigMgr의 버전이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="43eca-188">UE-V 템플릿 기준선 생성</span><span class="sxs-lookup"><span data-stu-id="43eca-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="43eca-189">UE-V 템플릿은 여러 구성 항목이 포함 된 기준을 사용 하 여 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="43eca-190">각 구성 항목에는 하나의 UE-V 템플릿을 설치 하는 데 필요한 검색 및 재구성 스크립트가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="43eca-191">실제 UE-V 템플릿은 표준 구성 항목 기능을 사용 하 여 배포 하기 위한 업데이트 관리 스크립트에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="43eca-192">UE-V 템플릿 기준선은 다음 매개 변수를 포함 하는 UevTemplateBaselineGenerator.exe 명령줄 도구를 사용 하 여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="43eca-193">사이트 &lt; 사이트 코드&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="43eca-194">BaselineName &lt; 이름 &gt; (선택 사항: "Ue-v Template 배포 기준"이 없는 경우 기본값 "으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="43eca-195">BaselineDescription &lt; 설명 &gt; (선택 사항: 설명이 없는 경우 제공 됨)</span><span class="sxs-lookup"><span data-stu-id="43eca-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="43eca-196">서식 &lt; 파일 폴더 ue-v 템플릿 폴더&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="43eca-197">&lt;서식 파일 목록을 쉼표로 구분 하 여 등록&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="43eca-198">&lt;쉼표로 구분 된 서식 파일 목록 등록 취소&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="43eca-199">CabFilePath &lt; 생성할 기준선 CAB 파일의 전체 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="43eca-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="43eca-200">결과는 구성 관리자로 가져올 준비가 된 기준 CAB 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="43eca-201">나중에 서식 파일을 업데이트 하거나 추가 하는 경우 동일한 기준 이름을 사용 하 여 명령을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="43eca-202">CAB 파일을 가져오면 변경 된 서식 파일의 CI 버전 업데이트 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="43eca-203">첫 번째 UE-V 템플릿 기준선 만들기</span><span class="sxs-lookup"><span data-stu-id="43eca-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="43eca-204">ConfigMgr 관리 콘솔을 실행 하는 컴퓨터에 표시 되는 안정적인 폴더 위치에 UE-V 서식 파일의 "마스터" 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="43eca-205">서식 파일이 추가 되거나 업데이트 되 면이 폴더에 배포할 수 있는 위치가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="43eca-206">템플릿의 초기 목록은 UE-V가 설치 된 컴퓨터에서 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="43eca-207">기본 서식 파일 위치는 C:\\program files Files\\Microsoft 사용자 환경 Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="43eca-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="43eca-208">템플릿 생성기 명령을 추가할 수 있는 text.bat 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="43eca-209">이는 선택 사항 이지만 명령 매개 변수를 저장 하는 경우 재생성 하기가 쉽습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="43eca-210">베이스 라인을 생성 하는 .bat 파일에 명령 및 매개 변수를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="43eca-211">다음 예제에서는 메모장과 계산기를 배포 하는 초기 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="43eca-212">.Bat 파일을 실행 하 여 Configuration Manager로 가져오기 위해 준비 UevTemplateBaseline.cab 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="43eca-213">UE-V 템플릿 기준선 업데이트</span><span class="sxs-lookup"><span data-stu-id="43eca-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="43eca-214">템플릿 생성기는 템플릿 버전을 사용 하 여 템플릿을 업데이트 해야 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="43eca-215">서식 파일을 변경 하 고 버전을 업데이트 하는 경우 기준선 생성기는 마스터 폴더의 템플릿을 ConfigMgr 서버의 CI에 포함 된 템플릿과 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="43eca-216">차이점을 발견 하면 생성 된 기준 및 수정한 CI 버전이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="43eca-217">새 메모장 템플릿을 배포 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="43eca-218">템플릿의 버전 요소에 있는 템플릿 및 템플릿 버전을 업데이트 &lt; &gt; 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="43eca-219">마스터 서식 파일 디렉터리에 서식 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="43eca-220">3 단계에서 만든 .bat 파일에서 [첫 번째 Ue-v 템플릿 기준선 만들기](#create2)로 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="43eca-221">콘솔 또는 PowerShell 가져오기-CMBaseline를 사용 하 여 생성 된 CAB 파일을 ConfigMgr로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="43eca-222">UE-V 구성 팩 다운로드</span><span class="sxs-lookup"><span data-stu-id="43eca-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="43eca-223">Configuration Manager 2012 SP1 이상 버전에 대 한 UE-V 구성 팩을 [여기](https://go.microsoft.com/fwlink/?LinkId=317263)에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43eca-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="43eca-224">관련 항목</span><span class="sxs-lookup"><span data-stu-id="43eca-224">Related topics</span></span>


[<span data-ttu-id="43eca-225">UE-V 2.x에 대한 구성 관리</span><span class="sxs-lookup"><span data-stu-id="43eca-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





