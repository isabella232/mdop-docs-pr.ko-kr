---
title: UE-V 1.0 관리
description: UE-V 1.0 관리
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822698"
---
# <span data-ttu-id="7af15-103">UE-V 1.0 관리</span><span class="sxs-lookup"><span data-stu-id="7af15-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="7af15-104">Microsoft UE-V (사용자 환경 가상화)를 배포한 후에는 다양 한 지속적인 관리 작업을 수행할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="7af15-105">이러한 사후 설치 작업에 대해서는 다음 섹션에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="7af15-106">UE-V 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="7af15-106">Managing UE-V resources</span></span>


<span data-ttu-id="7af15-107">UE-V 수명 주기 과정에서 UE-V agent의 구성을 관리 하 고 설정 패키지와 같은 리소스의 저장소 위치를 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="7af15-108">손실 된 설정을 복구 하기 위해 UE-V-V를 설치 하기 전에 사용자 설정을 원래 상태로 복원 하는 등의 다른 작업을 수행 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="7af15-109">다음 항목에서는 UE-V 리소스 관리에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="7af15-110">UE-V 예약된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="7af15-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="7af15-111">UE-V가 설정 서식 파일 카탈로그에서 새 사용자 지정 설정 위치 템플릿, 업데이트 또는 제거 여부를 확인할 때 관리 되는 예약 된 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="7af15-112">UE-V 예약된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="7af15-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="7af15-113">UE-V 템플릿 갤러리와 설정 위치 템플릿 공유</span><span class="sxs-lookup"><span data-stu-id="7af15-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="7af15-114">UE-V 템플릿 갤러리를 통해 UE-V 설정 위치 템플릿의 공유를 쉽게 수행할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="7af15-115">갤러리를 통해 다른 사용자와 공유할 설정 위치 템플릿을 업로드 하 고 다른 사용자가 만든 서식 파일을 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="7af15-116">UE-V 템플릿 갤러리와 설정 위치 템플릿 공유</span><span class="sxs-lookup"><span data-stu-id="7af15-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="7af15-117">UE-V 1.0와 동기화 된 응용 프로그램 및 Windows 설정 복원</span><span class="sxs-lookup"><span data-stu-id="7af15-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="7af15-118">UE-V의 WMI 및 PowerShell 기능은 설정 패키지를 복원 하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="7af15-119">WMI 및 PowerShell 명령을 사용 하 여 UE-V agent가 시작 된 후 응용 프로그램을 처음 시작 했을 때 컴퓨터에 있던 설정 값으로 응용 프로그램 설정 및 Windows 설정을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="7af15-120">UE-V 1.0과 동기화된 응용 프로그램 및 Windows 설정 복원</span><span class="sxs-lookup"><span data-stu-id="7af15-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="7af15-121">그룹 정책 개체를 사용하여 UE-V 구성</span><span class="sxs-lookup"><span data-stu-id="7af15-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="7af15-122">그룹 정책을 사용 하 여 UE-V가 컴퓨터에서 설정을 동기화 하는 방식을 정의 하는 설정을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="7af15-123">그룹 정책 개체를 사용하여 UE-V 구성</span><span class="sxs-lookup"><span data-stu-id="7af15-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="7af15-124">PowerShell 및 WMI를 사용하여 UE-V 관리</span><span class="sxs-lookup"><span data-stu-id="7af15-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="7af15-125">PowerShell 및 WMI를 사용 하 여 UE-V가 컴퓨터에서 설정을 동기화 하는 방법을 정의 하는 설정을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="7af15-126">PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리</span><span class="sxs-lookup"><span data-stu-id="7af15-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="7af15-127">UE-V 설정 패키지 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="7af15-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="7af15-128">새 서버로 마이그레이션하거나 백업을 위해 사용자 설정 패키지를 재배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7af15-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="7af15-129">UE-V 설정 패키지 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="7af15-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="7af15-130">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="7af15-130">Other resources for this product</span></span>


[<span data-ttu-id="7af15-131">UE-V 1.0 작업</span><span class="sxs-lookup"><span data-stu-id="7af15-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





