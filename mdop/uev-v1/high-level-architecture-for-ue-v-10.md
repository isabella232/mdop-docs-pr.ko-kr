---
title: UE-V 1.0의 개략적인 아키텍처
description: UE-V 1.0의 개략적인 아키텍처
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827098"
---
# <span data-ttu-id="3dee7-103">UE-V 1.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="3dee7-103">High-Level Architecture for UE-V 1.0</span></span>


<span data-ttu-id="3dee7-104">이 항목에서는 Microsoft UE-V (User Experience Virtualization) 설정 로밍 솔루션의 상위 수준 아키텍처 요소에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-104">This topic describes high-level architectural elements of the Microsoft User Experience Virtualization (UE-V) settings roaming solution.</span></span> <span data-ttu-id="3dee7-105">다음 요소는 표준 UE-V 배포의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-105">The following elements are part of a standard UE-V deployment.</span></span>

![ue-v agent 아키텍처 다이어그램](images/ue-vagentarchitecturaldiagram.gif)

<span data-ttu-id="3dee7-107">UE-V Agent는 UE-V 설정 위치 템플릿에서 식별 되는 응용 프로그램 및 운영 체제 프로세스를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-107">The UE-V Agent monitors the applications and the operating system processes as they are identified in the UE-V settings location templates.</span></span> <span data-ttu-id="3dee7-108">응용 프로그램이 나 운영 체제가 시작 되 면 설정 패키지에서 설정을 읽고 컴퓨터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-108">When the application or operating system starts, the settings are read from the settings package and applied to the computer.</span></span> <span data-ttu-id="3dee7-109">응용 프로그램이 닫히거나 운영 체제가 잠그거나 종료 되 면 설정 저장소 위치의 UE-V settings 패키지에 설정이 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-109">When the application closes or when the operating system is locked or shut down, settings are saved in a UE-V settings package in the settings storage location.</span></span>

## <span data-ttu-id="3dee7-110">설정 저장소 위치</span><span class="sxs-lookup"><span data-stu-id="3dee7-110">Settings storage location</span></span>


<span data-ttu-id="3dee7-111">설정 저장소 위치는 사용자 환경 가상화 에이전트에서 읽기 및 쓰기 설정에 액세스 하는 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-111">The settings storage location is a file share that the User Experience Virtualization agent accesses to read and write settings.</span></span> <span data-ttu-id="3dee7-112">이 위치는 Active Directory home 디렉터리 이거나 UE-V 설치 중에 정의 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-112">This location is either the Active Directory home directory or defined during the UE-V installation.</span></span> <span data-ttu-id="3dee7-113">UE-V 에이전트를 설치 하는 동안 위치를 설정 하거나 그룹 정책, WMI 또는 PowerShell을 사용 하 여 나중에 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-113">You can set the location during the installation of the UE-V agent, or you can set it later with Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="3dee7-114">위치는 사용자가 액세스할 수 있는 모든 공용 파일 공유에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-114">The location can be on any common file share that users can access.</span></span> <span data-ttu-id="3dee7-115">설치 하는 동안 설정 저장소 위치를 설정할 수 없는 경우에는 UE-V가 Active Directory에서 홈 디렉터리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-115">If no setting storage location is set during installation then UE-V will use the home directory in Active Directory.</span></span> <span data-ttu-id="3dee7-116">UE-V agent는 위치를 확인 하 고 사용자 설정을 저장 하 고 액세스 하는 사용자에 게 숨겨진 시스템 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-116">The UE-V agent verifies the location and creates a system folder that is hidden from the user in which to store and access the user settings.</span></span> <span data-ttu-id="3dee7-117">설정 저장소에 대 한 자세한 내용은 [ue-v 용 환경 준비](preparing-your-environment-for-ue-v.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dee7-117">For more information about settings storage, see [Preparing Your Environment for UE-V](preparing-your-environment-for-ue-v.md).</span></span>

## <span data-ttu-id="3dee7-118">UE-V 에이전트</span><span class="sxs-lookup"><span data-stu-id="3dee7-118">UE-V Agent</span></span>


<span data-ttu-id="3dee7-119">UE-V agent가 사용자 환경 가상화에 의해 동기화 되는 설정을 사용 하 여 각 컴퓨터에 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-119">The UE-V agent is installed on each computer with settings that are synchronized by User Experience Virtualization.</span></span> <span data-ttu-id="3dee7-120">에이전트는 등록 된 응용 프로그램 및 운영 체제를 모니터링 하 여 설정에 대 한 변경 내용을 적용 하 고 해당 설정을 컴퓨터 간에 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-120">The agent monitors the registered applications and the operating system for any changes to that are made to settings, and it synchronizes those settings between computers.</span></span> <span data-ttu-id="3dee7-121">설정은 응용 프로그램이 시작 될 때 설정 저장소 위치에서 응용 프로그램으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-121">Settings are applied from the settings storage location to the application when the application is started.</span></span> <span data-ttu-id="3dee7-122">그러면 해당 설정이 응용 프로그램을 닫을 때 설정 저장소 위치로 다시 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-122">The settings are then saved back to the settings storage location when the application closes.</span></span> <span data-ttu-id="3dee7-123">운영 체제 설정은 사용자가 로그온 하거나, 컴퓨터를 잠금 해제 하거나, 사용자가 RDP (원격 데스크톱 프로토콜)을 사용 하 여 컴퓨터에 원격으로 연결할 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-123">The operating system settings are applied when the user logs on, when the computer is unlocked, or when the user connects remotely to the computer by using remote desktop protocol (RDP).</span></span> <span data-ttu-id="3dee7-124">에이전트는 사용자가 로그 오프할 때, 컴퓨터가 잠겨 있거나 원격 연결이 끊어질 때 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-124">The agent saves settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="3dee7-125">UE-V 에이전트에 대 한 자세한 내용은 [ue-v 용 환경 준비](preparing-your-environment-for-ue-v.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dee7-125">For more information about the UE-V Agent, see [Preparing Your Environment for UE-V](preparing-your-environment-for-ue-v.md).</span></span>

## <a href="" id="bkmk-settingslocationtemplate"></a><span data-ttu-id="3dee7-126">설정 위치 템플릿</span><span class="sxs-lookup"><span data-stu-id="3dee7-126">Settings location templates</span></span>


<span data-ttu-id="3dee7-127">설정 위치 템플릿은 사용자 환경 가상화를 통해 모니터링할 설정 위치를 정의 하는 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-127">The settings location template is an XML file that defines the settings locations to be monitored by User Experience Virtualization.</span></span> <span data-ttu-id="3dee7-128">이러한 설정 템플릿에 정의 된 설정 위치만 UE-V Agent를 실행 하는 컴퓨터에서 캡처 또는 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-128">Only the settings locations defined in these settings templates are captured or applied on computers running the UE-V Agent.</span></span> <span data-ttu-id="3dee7-129">설정 위치 템플릿은 값이 컴퓨터에 저장 된 위치만 포함 하 고 설정 값으로 구성 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-129">The settings location template does not contain settings values, only the locations where values are stored on the computer.</span></span>

<span data-ttu-id="3dee7-130">UE-V는 일부 Microsoft 응용 프로그램 및 Windows 설정에 대 한 설정 위치를 지정 하는 설정 위치 템플릿의 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-130">UE-V includes a set of settings location templates that specify settings locations for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="3dee7-131">관리자는 UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-131">An administrator can create custom settings location templates by using the UE-V Generator.</span></span>

[<span data-ttu-id="3dee7-132">UE-V 1.0과 동기화할 응용 프로그램 계획</span><span class="sxs-lookup"><span data-stu-id="3dee7-132">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="3dee7-133">UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획</span><span class="sxs-lookup"><span data-stu-id="3dee7-133">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="3dee7-134">사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업</span><span class="sxs-lookup"><span data-stu-id="3dee7-134">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## <span data-ttu-id="3dee7-135">설정 패키지</span><span class="sxs-lookup"><span data-stu-id="3dee7-135">Settings packages</span></span>


<span data-ttu-id="3dee7-136">응용 프로그램 설정 및 Windows 설정은 UE-V Agent에서 만든 설정 패키지에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-136">Application settings and Windows settings are stored in settings packages, which are created by the UE-V Agent.</span></span> <span data-ttu-id="3dee7-137">설정 패키지는 설정 위치 템플릿에 표시 되는 설정의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-137">A settings package is a collection of the settings that are represented in the settings location templates.</span></span> <span data-ttu-id="3dee7-138">이러한 설정 패키지는 빌드, 로컬 저장, 설정 저장소 위치에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-138">These settings packages are built, locally stored, and then copied to the settings storage location.</span></span> <span data-ttu-id="3dee7-139">"마지막 쓰기 wins"는 단일 사용자가 두 대 이상의 컴퓨터를 저장소 위치로 동기화 할 때 유지 되는 설정을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-139">“Last write wins” determines which settings are preserved when a single user synchronizes the more than one computer to a storage location.</span></span> <span data-ttu-id="3dee7-140">한 컴퓨터에서 실행 되는 에이전트는 다른 컴퓨터에서 실행 되는 에이전트와 독립적으로 설정 위치를 읽고 씁니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-140">The agent that runs on one computer reads and writes to the settings location independent of agents that run on other computers.</span></span> <span data-ttu-id="3dee7-141">다음 에이전트가 설정 저장소 위치에서 읽을 때 가장 최근에 쓰여진 설정 및 값이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-141">The most recently written settings and values are applied when the next agent reads from the settings storage location.</span></span>

![ue-v 생성자 프로세스](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="3dee7-143">설정 서식 파일 카탈로그</span><span class="sxs-lookup"><span data-stu-id="3dee7-143">Settings template catalog</span></span>


<span data-ttu-id="3dee7-144">설정 템플릿 카탈로그는 UE-V 컴퓨터 또는 모든 사용자 지정 설정 위치 템플릿을 저장 하는 SMB (서버 메시지 블록) 네트워크 공유의 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-144">The settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="3dee7-145">UE-V agent가이 위치에서 새 서식 파일 또는 업데이트 된 템플릿을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-145">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="3dee7-146">UE-V agent는 매일이 위치를 확인 하 고이 폴더의 템플릿을 기반으로 동기화 동작을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-146">The UE-V agent checks this location once each day and it updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="3dee7-147">마지막 검사 이후이 폴더에서 추가 되거나 업데이트 된 서식 파일이 UE-V agent에 의해 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-147">The templates that were added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="3dee7-148">UE-V agent가이 폴더에서 제거 된 템플릿을 deregisters.</span><span class="sxs-lookup"><span data-stu-id="3dee7-148">The UE-V agent deregisters the templates that were removed from this folder.</span></span> <span data-ttu-id="3dee7-149">작업 스케줄러에서 서식 파일을 하루에 한 번씩 등록 하 고 등록 취소 했습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-149">Templates are registered and unregistered one time per day by the task scheduler.</span></span> <span data-ttu-id="3dee7-150">UE-V와 함께 제공 되는 기본 설정 위치 템플릿만 사용 하는 경우 설정 템플릿 카탈로그는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-150">If you will use only the default settings location templates that are included with UE-V, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="3dee7-151">설정 배포 카탈로그에 대 한 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획 수립](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dee7-151">For more information about settings deployment catalogs, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

## <span data-ttu-id="3dee7-152">사용자 환경 가상화 생성기</span><span class="sxs-lookup"><span data-stu-id="3dee7-152">User Experience Virtualization Generator</span></span>


<span data-ttu-id="3dee7-153">사용자 환경 가상화 생성기를 사용 하 여 엔터프라이즈에 사용 되 고 로밍 설정 솔루션에 포함 하려는 응용 프로그램의 설정 위치를 저장할 사용자 지정 설정 위치 템플릿을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-153">The User Experience Virtualization Generator enables you to create custom settings location templates which will store the settings locations of the applications that are used in the enterprise and that you want to include in the roaming settings solution.</span></span> <span data-ttu-id="3dee7-154">UE-V 생성기는 레지스트리 값의 위치와 응용 프로그램에 대 한 설정 파일을 검색 한 다음 설정 위치 템플릿 XML 파일에 해당 위치를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-154">The UE-V Generator will seek to discover the locations of registry values and the settings files for applications and then it will record those locations in a settings location template XML file.</span></span> <span data-ttu-id="3dee7-155">그런 다음 이러한 설정 위치 템플릿을 사용자 컴퓨터에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-155">You can then distribute these settings location templates to the user computers.</span></span> <span data-ttu-id="3dee7-156">또한 UE-V 생성기를 사용 하면 관리자가 기존 서식 파일을 편집 하거나 다른 XML 편집기를 사용 하 여 만든 서식 파일의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-156">The UE-V Generator also allows an administrator to edit an existing template or validate a template that was created with another XML editor.</span></span>

<span data-ttu-id="3dee7-157">UE-V 생성기는 응용 프로그램을 모니터링 하 여 설정을 저장 하는 위치를 검색 하 고 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-157">The UE-V Generator monitors an application to discover and record where it stores its settings.</span></span> <span data-ttu-id="3dee7-158">이렇게 하려면 HKEY \ _CURRENT \ _USER 레지스트리 또는 **사용자** \\ \ [사용자 이름 \ \ \ **AppData**  \\  **로밍 및 사용자** \\ \ \ \ \ **AppData**  \\  **Local**)의 파일 폴더에서 응용 프로그램이 읽거나 쓰는 위치를 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-158">To do this, it monitors where the application reads or writes in the HKEY\_CURRENT\_USER registry or in the file folders under **Users** \\ \[User name\] \\ **AppData** \\ **Roaming and Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span>

<span data-ttu-id="3dee7-159">검색 프로세스는 로그인 한 사용자가 값을 쓸 수 없는 레지스트리 키와 파일을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-159">The discovery process excludes registry keys and files to which the logged-in user cannot write values.</span></span> <span data-ttu-id="3dee7-160">이러한 항목이 XML 파일에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-160">None of these will be included in the XML file.</span></span> <span data-ttu-id="3dee7-161">또한 검색 프로세스는 Windows 운영 체제의 핵심 기능과 연결 된 레지스트리 키와 파일을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dee7-161">The discovery process also excludes registry keys and files that are associated with the core functionality of the Windows operating system.</span></span>

<span data-ttu-id="3dee7-162">UE-V 생성기에 대 한 자세한 내용은 [Ue-v 생성기 설치](installing-the-ue-v-generator.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dee7-162">For more information about the UE-V Generator, see [Installing the UE-V Generator](installing-the-ue-v-generator.md).</span></span>

## <span data-ttu-id="3dee7-163">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3dee7-163">Related topics</span></span>


[<span data-ttu-id="3dee7-164">Microsoft User Experience Virtualization(UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="3dee7-164">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="3dee7-165">User Experience Virtualization 1.0 시작</span><span class="sxs-lookup"><span data-stu-id="3dee7-165">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="3dee7-166">User Experience Virtualization 1.0 정보</span><span class="sxs-lookup"><span data-stu-id="3dee7-166">About User Experience Virtualization 1.0</span></span>](about-user-experience-virtualization-10.md)

[<span data-ttu-id="3dee7-167">사용자 지정 UE-V 템플릿 및 UE-V 생성기 작업</span><span class="sxs-lookup"><span data-stu-id="3dee7-167">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





