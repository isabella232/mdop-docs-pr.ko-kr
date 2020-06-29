---
title: UE-V on-V 2. x 관리
description: UE-V on-V 2. x 관리
author: dansimp
ms.assetid: 996e4797-8383-4627-b714-24a84c907798
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2674f6ace80672c1e89bb4f9c765b56f260c3bc0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825673"
---
# <span data-ttu-id="ef2f0-103">UE-V on-V 2. x 관리</span><span class="sxs-lookup"><span data-stu-id="ef2f0-103">Administering UE-V 2.x</span></span>


<span data-ttu-id="ef2f0-104">Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1을 배포한 후에는 UE-V Agent의 구성을 관리 하 고 손실 된 설정을 복구 하는 등 지속적인 다양 한 관리 작업을 수행할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-104">After you have deployed Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you must be able to perform various ongoing administrative tasks, such as managing the configuration of the UE-V Agent and recovering lost settings.</span></span> <span data-ttu-id="ef2f0-105">이러한 사후 설치 작업에 대해서는 다음 섹션에서 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="ef2f0-106">UE-V 2. x 구성 관리</span><span class="sxs-lookup"><span data-stu-id="ef2f0-106">Managing UE-V 2.x configurations</span></span>


<span data-ttu-id="ef2f0-107">UE-V 수명 주기 과정에서 UE-V Agent의 구성을 관리 하 고 설정 패키지 파일과 같은 리소스의 저장소 위치를 관리 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-107">In the course of the UE-V lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span>

[<span data-ttu-id="ef2f0-108">UE-V 2.x에 대한 구성 관리</span><span class="sxs-lookup"><span data-stu-id="ef2f0-108">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

## <span data-ttu-id="ef2f0-109">사용자 지정 UE-V 템플릿 및 UE-V 2. x 생성기 사용</span><span class="sxs-lookup"><span data-stu-id="ef2f0-109">Working with custom UE-V templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="ef2f0-110">이 항목에서는 UE-V 생성기를 사용 하 고 사용자 지정 설정 위치 템플릿을 관리 하는 방법에 대 한 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-110">This topic provides instructions for how to use the UE-V Generator and manage custom settings location templates.</span></span>

[<span data-ttu-id="ef2f0-111">사용자 지정 UE-V 2. x 템플릿 및 UE-V 2 .x 생성기 사용</span><span class="sxs-lookup"><span data-stu-id="ef2f0-111">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

## <span data-ttu-id="ef2f0-112">UE-V 2. x와 동기화 되는 응용 프로그램 및 Windows 설정 백업 및 복원</span><span class="sxs-lookup"><span data-stu-id="ef2f0-112">Backup and restore application and Windows settings that are synchronized with UE-V 2.x</span></span>


<span data-ttu-id="ef2f0-113">UE-V의 windows Management Instrumentation (WMI) 및 Windows PowerShell 기능은 설정 패키지를 복원할 수 있는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-113">Windows Management Instrumentation (WMI) and Windows PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="ef2f0-114">WMI 및 Windows PowerShell 명령을 사용 하 여 응용 프로그램 및 Windows 설정을 원래 상태로 복원 하 고 사용자가 새 장치를 사용할 때 추가 설정을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-114">By using WMI and Windows PowerShell commands, you can restore application and Windows settings to their original state and restore additional settings when a user adopts a new device.</span></span>

[<span data-ttu-id="ef2f0-115">UE-V 2. x에서 관리 백업 및 복원 관리</span><span class="sxs-lookup"><span data-stu-id="ef2f0-115">Manage Administrative Backup and Restore in UE-V 2.x</span></span>](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

## <span data-ttu-id="ef2f0-116">UE-V 2. x 예약 된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="ef2f0-116">Changing the frequency of UE-V 2.x scheduled tasks</span></span>


<span data-ttu-id="ef2f0-117">UE-V가 설정 서식 파일 카탈로그에서 업데이트 된 사용자 지정 설정 위치 템플릿 또는 업데이트 된 설정을 확인 하거나 새로 고칠 때 관리 되는 예약 작업을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-117">You can configure the scheduled tasks that manage when UE-V checks for new or updated settings or for updated custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="ef2f0-118">UE-V 2. x 예약 된 작업의 빈도 변경</span><span class="sxs-lookup"><span data-stu-id="ef2f0-118">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

## <span data-ttu-id="ef2f0-119">UE-V 2. x 설정 패키지 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="ef2f0-119">Migrating UE-V 2.x settings packages</span></span>


<span data-ttu-id="ef2f0-120">사용자 설정 패키지를 새 서버로 마이그레이션하거나 백업용으로 재배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-120">You can relocate the user settings packages either when they migrate to a new server or for backup purposes.</span></span>

[<span data-ttu-id="ef2f0-121">UE-V 2. x 설정 패키지 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="ef2f0-121">Migrating UE-V 2.x Settings Packages</span></span>](migrating-ue-v-2x-settings-packages-both-uevv2.md)

## <span data-ttu-id="ef2f0-122">UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ef2f0-122">Using UE-V 2.x with Application Virtualization applications</span></span>


<span data-ttu-id="ef2f0-123">Ue-v (Microsoft Application Virtualization)와 함께 ue-v를 사용 하 여 여러 컴퓨터에서 가상 응용 프로그램과 설치 된 응용 프로그램 간에 설정을 공유할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef2f0-123">You can use UE-V with Microsoft Application Virtualization (App-V) to share settings between virtual applications and installed applications across multiple computers.</span></span>

[<span data-ttu-id="ef2f0-124">UE-V 2. x를 사용 하 여 응용 프로그램 가상화 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="ef2f0-124">Using UE-V 2.x with Application Virtualization Applications</span></span>](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)

## <span data-ttu-id="ef2f0-125">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="ef2f0-125">Other resources for this product</span></span>


-   [<span data-ttu-id="ef2f0-126">Microsoft UE-V (User Experience Virtualization) 2. x</span><span class="sxs-lookup"><span data-stu-id="ef2f0-126">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="ef2f0-127">UE-V 2.x 시작</span><span class="sxs-lookup"><span data-stu-id="ef2f0-127">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="ef2f0-128">UE-V 2. x 배포 준비</span><span class="sxs-lookup"><span data-stu-id="ef2f0-128">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="ef2f0-129">UE-V 2. x 문제 해결</span><span class="sxs-lookup"><span data-stu-id="ef2f0-129">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="ef2f0-130">UE-V 2.x에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="ef2f0-130">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





