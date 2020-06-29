---
title: UE-V 구성 방법 계획
description: UE-V 구성 방법 계획
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827093"
---
# <span data-ttu-id="870df-103">UE-V 구성 방법 계획</span><span class="sxs-lookup"><span data-stu-id="870df-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="870df-104">Microsoft UE-V (User Experience Virtualization) 구성은 엔터프라이즈 전체에서 설정을 동기화 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="870df-105">이 항목에서는 비즈니스 요구 사항에 가장 적합 한 구성 계획을 공식화 하는 데 도움이 되도록 UE-V 구성을 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="870df-106">UE-V 용 구성 방법</span><span class="sxs-lookup"><span data-stu-id="870df-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="870df-107">사용 하는 구성 방법에 따라 에이전트를 설치 하기 전이나 설치한 후에 UE-V를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="870df-108">**그룹 정책:** 기존 그룹 정책 인프라를 사용 하 여 ue-v 에이전트 배포 전 또는 후에 ue-v를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="870df-109">UE-V ADMX 서식 파일은 일반적인 UE-V Agent 구성 옵션의 중앙 관리를 가능 하 게 하며 UE-V 동기화를 구성 하는 설정을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="870df-110">그룹 정책을 사용 하는 네트워크 환경은 에이전트 배포에 대비 하 여 UE-V를 미리 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="870df-111">그룹 정책 개체를 사용하여 UE-V 구성</span><span class="sxs-lookup"><span data-stu-id="870df-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="870df-112">UE-V 그룹 정책 ADMX 템플릿 설치</span><span class="sxs-lookup"><span data-stu-id="870df-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="870df-113">**명령줄 또는 배치 스크립트 설치:** ue-v 에이전트 배포와 함께 사용 되는 매개 변수는 여러 ue-v 설정의 구성을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="870df-114">System Center Configuration Manager와 같은 전자 소프트웨어 배포 시스템에서는 UE-V 에이전트 소프트웨어를 배포 하 고 설치할 때 이러한 매개 변수를 사용 하 여 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="870df-115">설치 매개 변수 목록과 샘플 설치 스크립트는 [Ue-v 에이전트 배포](deploying-the-ue-v-agent.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="870df-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="870df-116">**Powershell 및 wmi:** POWERSHELL 또는 wmi를 사용 하는 스크립팅된 명령을 사용 하 여 ue-v agent가 설치 된 후 구성을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="870df-117">PowerShell 및 WMI 명령 목록은 [powershell 및 wmi를 사용 하 여 ue-v 1.0 에이전트 및 패키지 관리](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="870df-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="870df-118">**레지스트리 설정 편집:** UE-V 설정은 레지스트리에 저장 되며 RegEdit 등의 레지스트리 설정을 수정할 수 있는 도구를 사용 하 여 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="870df-119">**참고**  레지스트리를 수정 하면 데이터가 손실 되거나 컴퓨터가 응답 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="870df-120">다른 구성 메서드를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="870df-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="870df-121">UE-V 구성 설정</span><span class="sxs-lookup"><span data-stu-id="870df-121">UE-V configuration settings</span></span>

<span data-ttu-id="870df-122">다음은 UE-V 구성 설정의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="870df-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="870df-123">**저장소 경로 설정:** ue-v 설정을 저장 하는 파일 공유의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="870df-124">**설정 템플릿 카탈로그 경로:** 새 설정 위치 템플릿을 확인 한 위치를 정의 하는 UNC (범용 명명 규칙) 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="870df-125">**Microsoft 서식 파일 등록:** 설치 중에 기본 Microsoft 서식 파일을 등록할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="870df-126">**동기화 방법:** Windows 오프 라인 파일 기능을 오프 라인 지원에 사용 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="870df-127">**동기화 시간 제한:** 설정 저장소 위치에서 사용자 설정을 검색할 때 시간이 초과 되기 전에 컴퓨터가 대기 하는 시간 (밀리초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="870df-128">**동기화 사용:** ue-v 설정을 동기화 할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="870df-129">**최대 패키지 크기:** ue-v agent가 경고를 보고 하는 설정 패키지 파일 임계값 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="870df-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="870df-130">관련 항목</span><span class="sxs-lookup"><span data-stu-id="870df-130">Related topics</span></span>


[<span data-ttu-id="870df-131">UE-V 1.0 계획</span><span class="sxs-lookup"><span data-stu-id="870df-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="870df-132">UE-V 구성 계획</span><span class="sxs-lookup"><span data-stu-id="870df-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





