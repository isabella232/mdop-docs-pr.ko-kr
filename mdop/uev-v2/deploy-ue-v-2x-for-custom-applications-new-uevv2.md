---
title: 사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포
description: 사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824403"
---
# <span data-ttu-id="1a3d7-103">사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포</span><span class="sxs-lookup"><span data-stu-id="1a3d7-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="1a3d7-104">Microsoft UE-V (User Experience Virtualization) 2.0.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="1a3d7-105">2.1 및 2.1 SP1에서는 **설정 위치 템플릿** 이라는 XML 파일을 사용 하 여 데스크톱 응용 프로그램 설정 및 사용자 컴퓨터 간에 Windows 데스크톱 설정을 모니터링 하 고 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="1a3d7-106">기본적으로 일부 설정 위치 템플릿은 UE-V에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="1a3d7-107">그러나 기본 템플릿에 포함 되지 않은 데스크톱 응용 프로그램의 설정을 동기화 하려는 경우 UE-V 생성기를 사용 하 여 고유한 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="1a3d7-108">[Ue-v 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md) 에서 계획 자료를 읽고 사용자 지정 응용 프로그램 (타사, lob 등)에 대 한 설정을 동기화 하도록 결정 한 경우이 항목에 설명 된 대로 ue-v의 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="1a3d7-109">시작 하려면 사용자 지정 응용 프로그램의 설정을 동기화 하는 데 필요한 주요 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="1a3d7-110">UEV 생성기 설치</span><span class="sxs-lookup"><span data-stu-id="1a3d7-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="1a3d7-111">UEV 생성기를 사용 하 여 사용자 지정 XML 설정 위치 서식 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="1a3d7-112">UE-V 설정 템플릿 카탈로그 구성</span><span class="sxs-lookup"><span data-stu-id="1a3d7-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="1a3d7-113">사용자 지정 설정 위치 템플릿이 저장 되는 위치를이 경로를 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="1a3d7-114">사용자 지정 설정 위치 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="1a3d7-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="1a3d7-115">이러한 사용자 지정 서식 파일을 통해 사용자는 사용자 지정 응용 프로그램의 설정을 동기화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="1a3d7-116">사용자 지정 설정 위치 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="1a3d7-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="1a3d7-117">사용자 지정 서식 파일을 테스트 하 여 설정이 올바르게 동기화 되었는지 확인 한 후 다음 방법 중 하나로 해당 템플릿을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="1a3d7-118">기존 배포 인프라 (예: 구성 관리자)</span><span class="sxs-lookup"><span data-stu-id="1a3d7-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="1a3d7-119">그룹 정책 기본 설정을 사용 하 여</span><span class="sxs-lookup"><span data-stu-id="1a3d7-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="1a3d7-120">UE-V 설정 서식 파일 카탈로그 배포</span><span class="sxs-lookup"><span data-stu-id="1a3d7-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="1a3d7-121">**참고**  ESD 또는 그룹 정책을 사용 하 여 배포한 서식 파일은 UE-V WMI (Windows Management Instrumentation) 또는 Windows PowerShell에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="1a3d7-122">사용자 지정 응용 프로그램에 대 한 UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="1a3d7-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="1a3d7-123">사용자 지정 응용 프로그램을 처리 하는 UE-V 기능 배포를 시작 하기 전에 몇 가지 검토 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="1a3d7-124">UE-V 생성기</span><span class="sxs-lookup"><span data-stu-id="1a3d7-124">The UE-V Generator</span></span>

<span data-ttu-id="1a3d7-125">UE-V 생성기는 응용 프로그램이 해당 설정을 저장 하는 위치를 검색 하 고 캡처하는 응용 프로그램을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="1a3d7-126">모니터링 되는 응용 프로그램은 일반 응용 프로그램 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="1a3d7-127">UE-V 생성기를 사용 하 여 설정 위치 템플릿을 만들지만 다음 응용 프로그램 유형에 서 설정 위치 템플릿을 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="1a3d7-128">가상화 된 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="1a3d7-128">Virtualized applications</span></span>

-   <span data-ttu-id="1a3d7-129">터미널 서비스를 통해 제공 되는 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="1a3d7-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="1a3d7-130">Java 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="1a3d7-130">Java applications</span></span>

-   <span data-ttu-id="1a3d7-131">Windows 앱  </span><span class="sxs-lookup"><span data-stu-id="1a3d7-131">Windows apps</span></span>

<span data-ttu-id="1a3d7-132">**참고**  UE-V 설정 위치 템플릿은 가상화 된 응용 프로그램 또는 터미널 서비스 응용 프로그램에서 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="1a3d7-133">그러나 서식 파일을 사용 하 여 동기화 되는 설정은 해당 응용 프로그램에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="1a3d7-134">VDI (가상 데스크톱 인프라) 및 터미널 서비스 응용 프로그램을 지 원하는 템플릿을 만들려면 UE-V 생성기를 사용 하 여 응용 프로그램의 Windows Installer (.msi) 패키지 버전을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="1a3d7-135">가상 응용 프로그램에 대 한 설정을 동기화 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 응용 프로그램을 사용 하 여 ue-v 2. x](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="1a3d7-136">**제외 된 위치:** 검색 프로세스는 일반적으로 사용자 컴퓨터 또는 컴퓨팅 환경과 효과적으로 설정을 동기화 하지 않는 응용 프로그램 소프트웨어 파일을 저장 하는 위치를 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="1a3d7-137">기본적으로 다음 항목이 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="1a3d7-138">HKEY \ _CURRENT \ _USER 로그온 한 사용자가 값을 쓸 수 없는 레지스트리 키 및 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="1a3d7-139">HKEY _CURRENT \ _USER Windows 운영 체제의 핵심 기능과 연결 된 레지스트리 키 및 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="1a3d7-140">HKEY \ _LOCAL \ _MACHINE 하이브에 있는 모든 레지스트리 키</span><span class="sxs-lookup"><span data-stu-id="1a3d7-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="1a3d7-141">Program Files 디렉터리에 있는 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="1a3d7-142">사용자 \\ [사용자 이름 \] \\ AppData에 있는 파일은 다음을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="1a3d7-143">% Systemroot%에 있는 Windows 운영 체제 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="1a3d7-144">응용 프로그램 설정을 동기화 하는 데 제외 위치에 저장 된 레지스트리 키 및 파일이 필요한 경우 서식 파일 만들기 프로세스 중에 수동으로 설정 위치 템플릿에 위치를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="1a3d7-145">그러나 HKEY _CURRENT \ _USER 하이브가 변경 되는 경우에만 동기화-ed를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="1a3d7-146">기본 Microsoft 서식 파일 바꾸기</span><span class="sxs-lookup"><span data-stu-id="1a3d7-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="1a3d7-147">UE-V Agent는 일반적인 Microsoft 응용 프로그램 및 Windows 설정에 대 한 기본 설정 위치 템플릿 그룹을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="1a3d7-148">이러한 템플릿을 사용자 지정 하거나 설정 위치 템플릿을 만들어 사용자 지정 응용 프로그램의 설정을 동기화 하는 경우에는 설정 템플릿 카탈로그를 사용 하 여 템플릿을 저장 하도록 UE-V 에이전트를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="1a3d7-149">이 경우에는 기본 서식 파일을 설정 템플릿 카탈로그의 사용자 지정 템플릿과 함께 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="1a3d7-150">[Ue-v agent를 배포](https://technet.microsoft.com/library/dn458891.aspx#agent)하는 경우 명령줄 매개 변수를 사용 `RegisterMSTemplates` 하 여 기본 Microsoft 템플릿의 등록을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="1a3d7-151">그룹 정책을 사용 하 여 설정 템플릿 카탈로그 경로를 구성 하는 경우 기본 Microsoft 서식 파일을 바꾸도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="1a3d7-152">기본 Microsoft 서식 파일을 바꾸기 위해 정책 설정을 구성한 경우 UE-V Agent에 의해 설치 된 모든 기본 Microsoft 템플릿이 삭제 되 고 설정 서식 파일 카탈로그에 있는 템플릿만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="1a3d7-153">기본 Microsoft 서식 파일을 재정의 하려면 UE-V 에이전트 구성 설정 매개 변수를 `RegisterMSTemplates` *true* 로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="1a3d7-154">**참고**  사용 하도록 설정 된 후이 정책 설정을 사용 하지 않도록 설정 하면 UE-V Agent가 기본 Microsoft 템플릿을 복원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="1a3d7-155">기본 Microsoft 서식 파일과 동일한 ID를 사용 하는 사용자 지정 서식 파일 카탈로그에 UE-V Agent가 기본 Microsoft 서식 파일을 바꾸도록 구성 되어 있지 않은 경우 Microsoft 서식 파일은 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="1a3d7-156">UE-V Windows PowerShell 기능을 사용 하 여 기본 템플릿을 바꿀 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="1a3d7-157">기본 Microsoft 템플릿을 Windows PowerShell로 바꾸려면 기본 Microsoft 서식 파일을 모두 등록 취소 한 다음 사용자 지정 된 서식 파일을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="1a3d7-158">**참고**  이전 설정 패키지는 응용 프로그램에 대 한 새 설정 위치 템플릿을 배포 하는 경우에도 설정 저장소 위치에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="1a3d7-159">에이전트에서 이러한 패키지를 읽지는 않지만, 자동으로 삭제 되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="1a3d7-160">UEV 2. x 생성기 설치</span><span class="sxs-lookup"><span data-stu-id="1a3d7-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="1a3d7-161">사용자 지정 설정 위치 템플릿을 만드는 데 사용할 수 있는 Microsoft UE-V (User Experience Virtualization) 2.0 생성기를 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="1a3d7-162">이 컴퓨터에는 사용자 지정 설정 위치 템플릿이 생성 되는 응용 프로그램이 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="1a3d7-163">UE-V 생성기를 설치 하려면</span><span class="sxs-lookup"><span data-stu-id="1a3d7-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="1a3d7-164">로컬 관리자 권한이 있는 사용자는 UE-V 소프트웨어를 사용 하 여 제공 되는 **ToolSetup.exe** ue-v 생성기 설치 파일을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="1a3d7-165">또는 컴퓨터 아키텍처를 알고 있는 경우 적절 한 Windows Installer (.msi) 파일, **ToolsSetupx64.msi** 또는 **ToolsSetupx86.msi**를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="1a3d7-166">설치 파일을 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-166">Double-click the installation file.</span></span> <span data-ttu-id="1a3d7-167">사용자 환경 가상화 생성기 설정 마법사가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="1a3d7-168">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="1a3d7-169">Microsoft 소프트웨어 사용 조건에 동의 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="1a3d7-170">Microsoft 업데이트 및 사용자 환경 개선 프로그램에 대 한 옵션을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="1a3d7-171">UE-V 생성기를 설치할 대상 폴더를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="1a3d7-172">설치를 **클릭 하 여 설치를 시작** 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="1a3d7-173">**참고**  응용 프로그램을 설치 하기 전에 **사용자 계정 컨트롤** 에 대 한 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="1a3d7-174">UE-V 생성기를 설치 하려면 권한이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="1a3d7-175">설치가 완료 되 면 **마침을** 클릭 하 여 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="1a3d7-176">사용자가 컴퓨터를 다시 시작 해야 UE-V 생성기를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="1a3d7-177">성공적으로 설치 되었는지 확인 하려면 **시작**, **모든 프로그램**, **Microsoft 사용자 환경 가상화**, **microsoft 사용자**환경 가상화 생성기를 차례로 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="1a3d7-178">**참고**  Ue-v 2 생성기는 UE-V 2 에이전트에 대 한 템플릿을 만드는 데만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="1a3d7-179">UE-V 1.0 에이전트 및 UE-V 2 에이전트의 혼합 배포에서는 모든 UE-V agent를 업그레이드할 때까지 UE-V 1.0 생성기를 계속 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="1a3d7-180">설정 서식 파일 카탈로그 배포</span><span class="sxs-lookup"><span data-stu-id="1a3d7-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="1a3d7-181">사용자 환경 가상화 설정 템플릿 카탈로그는 UE-V 컴퓨터 또는 모든 사용자 지정 설정 위치 템플릿을 저장 하는 SMB (서버 메시지 블록) 네트워크 공유의 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="1a3d7-182">UE-V Agent의 예약 된 작업은이 위치를 하루에 한 번 확인 하 고이 폴더의 서식 파일을 기반으로 동기화 동작을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="1a3d7-183">UE-V Agent는 폴더를 마지막으로 확인 한 후에이 폴더에서 추가 또는 업데이트 된 서식 파일을 등록 하 고 제거 된 템플릿을 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="1a3d7-184">기본적으로 서식 파일은 매일 오전 3:30에 한 번씩 등록 되 고 등록이 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="1a3d7-185">작업 스케줄러 및 시스템 시작에의 한 현지 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="1a3d7-186">예약 된 작업의 빈도를 사용자 지정 하려면 [ue-v-V 2. x 예약 된 작업의 빈도 변경을](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="1a3d7-187">설치 명령줄 옵션, 그룹 정책, WMI 또는 Windows PowerShell을 사용 하 여 설정 템플릿 카탈로그 경로를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="1a3d7-188">설정 서식 파일 카탈로그 경로에 저장 된 서식 파일은 예약 된 작업에 의해 자동으로 등록 및 등록 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="1a3d7-189">UE-V 2. x에 대 한 설정 템플릿 카탈로그를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="1a3d7-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="1a3d7-190">UE-V 설정 템플릿 카탈로그를 저장 하는 컴퓨터에서 새 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="1a3d7-191">설정 템플릿 카탈로그 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="1a3d7-192">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="1a3d7-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="1a3d7-193">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1a3d7-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1a3d7-194">모두</span><span class="sxs-lookup"><span data-stu-id="1a3d7-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-195">권한 없음</span><span class="sxs-lookup"><span data-stu-id="1a3d7-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1a3d7-196">도메인 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1a3d7-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-197">읽기 사용 권한 수준</span><span class="sxs-lookup"><span data-stu-id="1a3d7-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1a3d7-198">관리자</span><span class="sxs-lookup"><span data-stu-id="1a3d7-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-199">읽기/쓰기 권한 수준</span><span class="sxs-lookup"><span data-stu-id="1a3d7-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="1a3d7-200">설정 템플릿 카탈로그 폴더에 대해 다음 NTFS 파일 시스템 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="1a3d7-201">사용자 계정</span><span class="sxs-lookup"><span data-stu-id="1a3d7-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="1a3d7-202">권장 되는 사용 권한</span><span class="sxs-lookup"><span data-stu-id="1a3d7-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="1a3d7-203">적용 대상</span><span class="sxs-lookup"><span data-stu-id="1a3d7-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1a3d7-204">만든이/소유자</span><span class="sxs-lookup"><span data-stu-id="1a3d7-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-205">모든 권한</span><span class="sxs-lookup"><span data-stu-id="1a3d7-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-206">이 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1a3d7-207">도메인 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="1a3d7-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-208">폴더 내용 나열 및 읽기</span><span class="sxs-lookup"><span data-stu-id="1a3d7-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-209">이 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="1a3d7-210">모두</span><span class="sxs-lookup"><span data-stu-id="1a3d7-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-211">권한 없음</span><span class="sxs-lookup"><span data-stu-id="1a3d7-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-212">권한 없음</span><span class="sxs-lookup"><span data-stu-id="1a3d7-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="1a3d7-213">관리자</span><span class="sxs-lookup"><span data-stu-id="1a3d7-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-214">모든 권한</span><span class="sxs-lookup"><span data-stu-id="1a3d7-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="1a3d7-215">이 폴더, 하위 폴더 및 파일</span><span class="sxs-lookup"><span data-stu-id="1a3d7-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="1a3d7-216">**확인** 을 클릭 하 여 대화 상자를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="1a3d7-217">최소한 네트워크 공유는 Domain Computers 그룹에 대 한 사용 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="1a3d7-218">또한 저장 된 서식 파일을 관리 하는 관리자에 게 네트워크 공유 폴더에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="1a3d7-219">사용자 지정 설정 위치 서식 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="1a3d7-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="1a3d7-220">UE-V 생성기를 사용 하 여 lob (기간 업무) 응용 프로그램 또는 기타 사용자 지정 응용 프로그램에 대 한 설정 위치 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="1a3d7-221">응용 프로그램의 템플릿을 만든 후에는 해당 응용 프로그램에 대 한 설정이 동기화 되도록 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="1a3d7-222">UE-V 생성기를 사용 하 여 UE-V 설정 위치 템플릿을 만들려면</span><span class="sxs-lookup"><span data-stu-id="1a3d7-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="1a3d7-223">**시작**을 클릭 하 고 **모든 프로그램**, **microsoft 사용자 환경 가상화**를 차례로 클릭 한 다음 **microsoft 사용자 환경 가상화 생성기**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="1a3d7-224">**설정 위치 서식 파일 만들기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="1a3d7-225">응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-225">Specify the application.</span></span> <span data-ttu-id="1a3d7-226">설정 위치 템플릿을 만들려는 응용 프로그램 (.exe) 또는 응용 프로그램 바로 가기 (.lnk)의 파일 경로를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="1a3d7-227">명령줄 인수 (있는 경우) 및 작업 디렉터리 (있는 경우)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="1a3d7-228">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="1a3d7-229">**참고**  응용 프로그램이 시작 되기 전에 시스템에서 **사용자 계정 컨트롤**을 확인 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="1a3d7-230">사용 권한은 응용 프로그램이 설정을 저장 하는 데 사용 하는 레지스트리와 파일 위치를 모니터링 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="1a3d7-231">응용 프로그램이 시작 되 면 응용 프로그램을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-231">After the application starts, close the application.</span></span> <span data-ttu-id="1a3d7-232">UE-V 생성기는 응용 프로그램에서 해당 설정을 저장 하는 위치를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="1a3d7-233">프로세스가 완료 되 면 **다음** 을 클릭 하 여 계속 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="1a3d7-234">이 응용 프로그램에 대해 동기화 할 적절 한 레지스트리 설정 위치 및 설정 파일 위치 옆에 있는 확인란을 검토 하 고 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="1a3d7-235">목록에는 설정 위치에 대 한 다음 두 가지 범주가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="1a3d7-236">**표준**: HKEY \ _CURRENT \ _USER 키 또는 \\ **사용자** \\ [사용자 이름 \ \ **AppData**  \\  **로밍**아래에 있는 파일 폴더에 저장 된 응용 프로그램 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="1a3d7-237">UE-V 생성기에는 이러한 설정이 기본적으로 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="1a3d7-238">**비표준**: 위치 외부에 저장 되는 응용 프로그램 설정은 설정 데이터 저장소에 대 한 모범 사례에 명시 되어 있습니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="1a3d7-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="1a3d7-239">여기에는 **사용자** \\ [사용자 이름 \ \ \ \ **AppData**의 파일 및 폴더가 포함 됩니다  \\  **Local**.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="1a3d7-240">이러한 위치를 검토 하 여 설정 위치 템플릿에 포함할 것인지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="1a3d7-241">위치 확인란을 선택 하 여 해당 항목을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="1a3d7-242">**Next**(다음)를 클릭하여 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="1a3d7-243">설정 위치 템플릿의 **속성**, **레지스트리** 위치 및 **파일** 위치를 검토 하 고 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="1a3d7-244">**속성** 탭에서 다음 속성을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="1a3d7-245">**응용 프로그램 이름**: program files 속성에 대 한 설명으로 작성 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="1a3d7-246">**프로그램 이름**: 프로그램 파일 속성에서 가져온 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="1a3d7-247">일반적으로이 이름은 .exe 파일 이름 확장명을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="1a3d7-248">**제품 버전**: 응용 프로그램의 .exe 파일에 대 한 제품 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="1a3d7-249">이 속성은 **파일 버전과**함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="1a3d7-250">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-250">This property accepts a major version number.</span></span> <span data-ttu-id="1a3d7-251">이 속성이 비어 있으면 설정 위치 템플릿이 모든 제품 버전에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="1a3d7-252">**파일 버전**: 응용 프로그램의 .exe 파일에 대 한 파일 버전 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="1a3d7-253">이 속성은 **제품 버전과**함께 설정 위치 템플릿에서 대상으로 하는 응용 프로그램을 확인 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="1a3d7-254">이 속성은 주 버전 번호를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-254">This property accepts a major version number.</span></span> <span data-ttu-id="1a3d7-255">이 속성이 비어 있으면 설정 위치 템플릿이 모든 버전의 프로그램에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="1a3d7-256">**서식 파일 만든이 이름** (선택 사항): 설정 위치 템플릿 작성자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="1a3d7-257">**서식 파일 저자 전자 메일** (선택 사항): 설정 위치 템플릿 작성자의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="1a3d7-258">**레지스트리** 탭에는 설정 위치 템플릿에 포함 된 레지스트리 위치의 **키** 와 **범위가** 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="1a3d7-259">**작업** 드롭다운 메뉴를 사용 하 여 레지스트리 위치를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="1a3d7-260">작업을 사용 하 여 새 키를 추가 하 고, 기존 키의 이름 또는 범위를 편집 하 고, 키를 삭제 하 고, 키가 있는 레지스트리를 찾아볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="1a3d7-261">**모든 설정** 범위를 사용 하 여 지정 된 키의 모든 레지스트리 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="1a3d7-262">**모든 설정 및 하위 키** 를 사용 하 여 지정 된 키, 하위 키 및 하위 키 설정의 모든 레지스트리 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="1a3d7-263">**파일** 탭에는 설정 위치 템플릿에 포함 된 파일 위치의 파일 경로 및 파일 마스크가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="1a3d7-264">**작업** 드롭다운 메뉴를 사용 하 여 파일 위치를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="1a3d7-265">파일 위치에 대 한 작업을 사용 하 여 새 파일 또는 폴더 위치를 추가 하 고, 기존 파일 또는 폴더의 범위를 편집 하 고, 파일이 나 폴더를 삭제 하 고, Windows 탐색기에서 선택한 위치를 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="1a3d7-266">지정 된 폴더의 모든 파일을 포함 하려면 파일 마스크를 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="1a3d7-267">**만들기**를 클릭 한 다음 **저장** 을 클릭 하 여 설정 위치 템플릿을 컴퓨터에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="1a3d7-268">**닫기를** 클릭 하 여 설정 템플릿 마법사를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="1a3d7-269">UE-V 생성기 응용 프로그램을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="1a3d7-270">응용 프로그램에 대 한 설정 위치 템플릿을 만든 후에는 해당 템플릿을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="1a3d7-271">엔터프라이즈에서 프로덕션에 배치 하기 전에 먼저 템플릿을 랩 환경에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="1a3d7-272">[Ue-v에 대 한 응용 프로그램 서식 파일 스키마 참조](https://technet.microsoft.com/library/dn763947.aspx) ue-v 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고 이러한 파일을 편집 하기 위한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="1a3d7-273">사용자 지정 설정 위치 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="1a3d7-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="1a3d7-274">UE-V 생성기를 사용 하 여 설정 위치 템플릿을 만든 후에는이를 테스트 하 여 응용 프로그램 설정이 올바르게 동기화 되었는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="1a3d7-275">그러면 설정 위치 템플릿을 엔터프라이즈의 컴퓨터에 안전 하 게 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="1a3d7-276">설정 위치 템플릿은 다음 방법 중 하나를 사용 하 여 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="1a3d7-277">System Center Configuration Manager와 같은 ESD (엔터프라이즈 소프트웨어 배포) 시스템</span><span class="sxs-lookup"><span data-stu-id="1a3d7-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="1a3d7-278">그룹 정책 기본 설정</span><span class="sxs-lookup"><span data-stu-id="1a3d7-278">Group Policy preferences</span></span>

-   <span data-ttu-id="1a3d7-279">UE-V 설정 템플릿 카탈로그</span><span class="sxs-lookup"><span data-stu-id="1a3d7-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="1a3d7-280">ESD 시스템 또는 그룹 정책 개체를 사용 하 여 배포 된 템플릿은 UE-V WMI (Windows Management Instrumentation) 또는 Windows PowerShell을 통해 등록 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="1a3d7-281">설정 서식 파일 카탈로그 위치에 저장 된 서식 파일은 UE-V Agent에서 자동으로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="1a3d7-282">설정 서식 파일 카탈로그 경로를 사용 하 여 UE-V 설정 위치 템플릿을 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="1a3d7-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="1a3d7-283">설정 템플릿 카탈로그로 정의 된 네트워크 공유 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="1a3d7-284">UE-V 컴퓨터에 사용할 UE-V 에이전트 템플릿 구성을 반영 하도록 설정 템플릿 카탈로그에서 설정 위치 템플릿을 추가, 제거 또는 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="1a3d7-285">**참고**  컴퓨터의 서식 파일은 매일 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="1a3d7-286">업데이트는 설정 서식 파일 카탈로그에 대 한 변경 내용을 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="1a3d7-287">UE-V Agent를 실행 하는 컴퓨터에서 템플릿을 수동으로 업데이트 하려면 관리자 권한 명령 프롬프트를 열고 \*\*% Program filesws Microsoft 사용자 환경 가상화 \\ 에이전트 \ \ &lt; x86 또는 x64 &gt; \*\*로 이동한 다음 **ApplySettingsTemplateCatalog.exe**를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="1a3d7-288">**참고**  이 프로그램은 컴퓨터 시작 시와 매일 3:30 ~ M 시에 자동으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="1a3d7-289">최근에 카탈로그에 추가 된 새 서식 파일을 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a3d7-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="1a3d7-290">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1a3d7-290">Related topics</span></span>


[<span data-ttu-id="1a3d7-291">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="1a3d7-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="1a3d7-292">UE-V 2.x에 대한 필수 기능 배포</span><span class="sxs-lookup"><span data-stu-id="1a3d7-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





