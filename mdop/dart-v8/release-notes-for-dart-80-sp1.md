---
title: DaRT 8.0 SP1 릴리스 정보
description: DaRT 8.0 SP1 릴리스 정보
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824773"
---
# <span data-ttu-id="658c7-103">DaRT 8.0 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="658c7-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="658c7-104">이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="658c7-105">Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0 서비스 팩 1 (SP1)을 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="658c7-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="658c7-106">이 릴리스 정보에는 진단 및 복구 도구 집합 8.0 SP1을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="658c7-107">릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="658c7-108">이러한 릴리스 정보와 기타 DaRT 설명서가 서로 다르면 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="658c7-109">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="658c7-110">제품 설명서 정보</span><span class="sxs-lookup"><span data-stu-id="658c7-110">About the product documentation</span></span>


<span data-ttu-id="658c7-111">DaRT 설명서에 대 한 자세한 내용은 Microsoft TechNet의 [DaRT 홈페이지](https://go.microsoft.com/fwlink/?LinkID=252096) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="658c7-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="658c7-112">DaRT 8.0 SP1의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="658c7-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="658c7-113">Locksmith 또는 레지스트리 편집기를 실행 하면 시스템 복원이 실패 함</span><span class="sxs-lookup"><span data-stu-id="658c7-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="658c7-114">Locksmith, 레지스트리 편집기 및 기타 도구를 실행 하면 시스템 복원이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="658c7-115">**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 시스템 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="658c7-116">Locksmith 또는 컴퓨터 관리를 시작 하 고 닫은 후 SFC scan이 실행 되지 않음</span><span class="sxs-lookup"><span data-stu-id="658c7-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="658c7-117">Locksmith 또는 컴퓨터 관리 도구를 시작 하 고 닫으면 시스템 파일 검사기가 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="658c7-118">**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 SFC를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="658c7-119">ADK가 설치 되지 않은 경우 DaRT 설치 프로그램이 실패 하지 않음</span><span class="sxs-lookup"><span data-stu-id="658c7-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="658c7-120">명령줄을 사용 하 여 MSI를 실행 하 고 설치 되어 있지 않은 DaRT 8.0 SP1을 설치 하는 경우 DaRT 설치는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="658c7-121">현재 DaRT 8.0 SP1 설치자는 DaRT 복구 이미지를 제외한 모든 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="658c7-122">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="658c7-122">**Workaround:** None.</span></span>

### <span data-ttu-id="658c7-123">Locksmith, RegEdit, 크래시 분석기, 컴퓨터 관리가 실행 된 후에는 Defender를 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="658c7-124">Locksmith, RegEdit, 충돌 분석기 및 컴퓨터 관리를 이미 실행 한 경우에는 Defender가 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="658c7-125">**해결 방법:** DaRT를 닫았다가 다시 시작 하 고 Defender를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="658c7-126">Defender가 시작 하는 데 오랜 시간이 걸릴 수 있음</span><span class="sxs-lookup"><span data-stu-id="658c7-126">Defender may be slow to launch</span></span>

<span data-ttu-id="658c7-127">Defender를 실행 하는 데 몇 분이 소요 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="658c7-128">진행률 표시줄에 현재 로드 상태가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="658c7-129">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="658c7-129">**Workaround:** None.</span></span>

## <span data-ttu-id="658c7-130">릴리스 노트 저작권 정보</span><span class="sxs-lookup"><span data-stu-id="658c7-130">Release notes copyright information</span></span>


<span data-ttu-id="658c7-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune 및 WindowsPowerShell는 Microsoft의 회사 그룹의 상표입니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="658c7-132">다른 모든 상표는 해당 소유자의 재산입니다.</span><span class="sxs-lookup"><span data-stu-id="658c7-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="658c7-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="658c7-133">Related topics</span></span>


[<span data-ttu-id="658c7-134">DaRT 8.0 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="658c7-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





