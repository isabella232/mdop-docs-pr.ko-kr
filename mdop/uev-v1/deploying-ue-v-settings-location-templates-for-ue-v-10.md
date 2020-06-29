---
title: UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포
description: UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827123"
---
# <span data-ttu-id="0ccf2-103">UE-V 1.0에 대한 UE-V 설정 위치 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="0ccf2-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="0ccf2-104">Microsoft UE-V (User Experience Virtualization)는 사용자 환경 가상화에 의해 캡처되고 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="0ccf2-105">UE-V는 사용자 지정 설정 위치 템플릿을 만들 수 있는 도구인 UE-V 생성기와 같은 표준 템플릿 집합을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="0ccf2-106">설정 위치 템플릿을 만든 후에는 테스트 환경에서 응용 프로그램 설정이 올바르게 로밍 되는지 확인 하도록 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="0ccf2-107">그러면 설정 위치 템플릿을 엔터프라이즈의 컴퓨터에 안전 하 게 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="0ccf2-108">설정 위치 템플릿은 엔터프라이즈 소프트웨어 배포 (ESD), 그룹 정책 기본 설정 또는 UE-V 설정 템플릿 카탈로그 구성을 사용 하 여 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="0ccf2-109">ESD 또는 그룹 정책을 사용 하 여 배포 된 서식 파일은 UE-V WMI 또는 PowerShell을 통해 등록 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="0ccf2-110">설정 서식 파일 카탈로그 위치에 저장 된 서식 파일은 UE-V agent에서 자동으로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="0ccf2-111">설정 템플릿 카탈로그 경로를 사용 하 여 설정 위치 템플릿 배포</span><span class="sxs-lookup"><span data-stu-id="0ccf2-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="0ccf2-112">UE-V 설정 위치 템플릿 카탈로그 경로는 그룹 정책, 에이전트 설치 명령줄 매개 변수, WMI 또는 PowerShell 등의 메서드를 사용 하 여 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="0ccf2-113">서식 파일 카탈로그 경로를 정의한 후에는 UE-V agent가이 위치에서 새 서식 파일 또는 업데이트 된 템플릿을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="0ccf2-114">UE-V agent는 하루에이 위치를 확인 하 고이 폴더에 있는 서식 파일을 기반으로 동기화 동작을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="0ccf2-115">마지막 검사 이후이 폴더에서 추가 되거나 업데이트 된 서식 파일이 UE-V agent에 의해 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="0ccf2-116">또한 UE-V agent는이 폴더에서 제거 된 템플릿의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="0ccf2-117">작업 스케줄러에서 서식 파일을 하루에 한 번씩 등록 하 고 등록 취소 했습니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="0ccf2-118">설정 템플릿 카탈로그 경로를 사용 하 여 UE-V 설정 위치 템플릿을 배포 하려면</span><span class="sxs-lookup"><span data-stu-id="0ccf2-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="0ccf2-119">설정 템플릿 카탈로그로 정의 된 네트워크 공유 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="0ccf2-120">UE-V 컴퓨터에 대 한 원하는 UE-V agent 템플릿 구성을 반영 하도록 설정 템플릿 카탈로그에서 설정 위치 템플릿을 추가, 제거 또는 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="0ccf2-121">컴퓨터의 서식 파일은 설정 템플릿 카탈로그에 대 한 변경 내용에 따라 매일 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="0ccf2-122">관리자 권한 명령 프롬프트를 열고 \*\*% program filesws Microsoft 사용자 환경 가상화 \\ 에이전트 \ \ &lt; x86 또는 x64 &gt; \*\*로 이동한 다음 **ApplySettingsTemplateCatalog.exe** 를 실행 하 여 ue-v Agent를 실행 하는 컴퓨터의 템플릿을 수동으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccf2-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="0ccf2-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0ccf2-123">Related topics</span></span>


[<span data-ttu-id="0ccf2-124">Microsoft User Experience Virtualization(UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="0ccf2-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="0ccf2-125">UE-V 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="0ccf2-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="0ccf2-126">UE-V 1.0과 동기화할 응용 프로그램 계획</span><span class="sxs-lookup"><span data-stu-id="0ccf2-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





