---
title: MBAM 1.0 언어 릴리스 업데이트 배포
description: MBAM 1.0 언어 릴리스 업데이트 배포
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812825"
---
# <span data-ttu-id="48548-103">MBAM 1.0 언어 릴리스 업데이트 배포</span><span class="sxs-lookup"><span data-stu-id="48548-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="48548-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 1.0 언어 릴리스는 MBAM에 대 한 업데이트 이며 새 언어에 대 한 지원을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="48548-105">새로운 언어는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="48548-105">The new languages are:</span></span>

-   <span data-ttu-id="48548-106">영어 (en-us)</span><span class="sxs-lookup"><span data-stu-id="48548-106">English (en-us)</span></span>

-   <span data-ttu-id="48548-107">프랑스어 (fr)</span><span class="sxs-lookup"><span data-stu-id="48548-107">French (fr)</span></span>

-   <span data-ttu-id="48548-108">이탈리아어 (it)</span><span class="sxs-lookup"><span data-stu-id="48548-108">Italian (it)</span></span>

-   <span data-ttu-id="48548-109">독일어 (de)</span><span class="sxs-lookup"><span data-stu-id="48548-109">German (de)</span></span>

-   <span data-ttu-id="48548-110">스페인어 (es)</span><span class="sxs-lookup"><span data-stu-id="48548-110">Spanish (es)</span></span>

-   <span data-ttu-id="48548-111">한국어 (ko-kr)</span><span class="sxs-lookup"><span data-stu-id="48548-111">Korean (ko)</span></span>

-   <span data-ttu-id="48548-112">일본어 (ja-jp)</span><span class="sxs-lookup"><span data-stu-id="48548-112">Japanese (ja)</span></span>

-   <span data-ttu-id="48548-113">포르투갈어 (브라질) (pt-br)</span><span class="sxs-lookup"><span data-stu-id="48548-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="48548-114">러시아어 (가)</span><span class="sxs-lookup"><span data-stu-id="48548-114">Russian (ru)</span></span>

-   <span data-ttu-id="48548-115">중국어 번체 (zh-cn-hy)</span><span class="sxs-lookup"><span data-stu-id="48548-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="48548-116">중국어 간체 (zh-cn-cn)</span><span class="sxs-lookup"><span data-stu-id="48548-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="48548-117">MBAM 1.0 언어 업데이트는 버전 번호를 MBAM 1.0.1237.1에서 MBAM 1.0.2001로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="48548-118">이러한 추가 언어를 추가 하기 위해 모든 MBAM 기능을 다시 설치할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="48548-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="48548-119">이 항목에서는 새로 지원 되는 언어를 추가 하는 데 필요한 단계를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="48548-120">MBAM 서버 기능에 MBAM 국제 릴리스 배포</span><span class="sxs-lookup"><span data-stu-id="48548-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="48548-121">시작 하려면 다음 MBAM 서버 기능을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="48548-122">준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="48548-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="48548-123">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="48548-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="48548-124">정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="48548-124">Policy Templates</span></span>

<span data-ttu-id="48548-125">그런 다음 동일한 서버에서 동시에 실행 되는 MBAM 기능을 업그레이드 하려면 **MbamSetup.exe** 를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="48548-126">단일 서버에서 MBAM 언어 업데이트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="48548-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="48548-127">분산 서버에 MBAM 언어 업데이트를 설치하는 방법</span><span class="sxs-lookup"><span data-stu-id="48548-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="48548-128">그룹 정책에 대해 MBAM 언어 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="48548-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="48548-129">MBAM 그룹 정책 서식 파일을 각 관리 워크스테이션에 설치 하거나 그룹 정책 중앙 저장소에 복사 하 여 모든 그룹 정책 관리자가 해당 템플릿을 사용할 수 있도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48548-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="48548-130">도메인 컨트롤러에는 정책 서식 파일을 직접 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="48548-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="48548-131">그룹 정책 중앙 저장소를 사용 하지 않는 경우에는 MBAM 그룹 정책을 관리 하는 각 도메인 컨트롤러에 정책을 수동으로 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="48548-132">MBAM 언어 정책 템플릿을 추가 하려면 "정책 템플릿" 역할이 설치 된 컴퓨터 의%SystemRoot%\\PolicyDefinitions에서 그룹 정책 언어 파일을 워크스테이션 컴퓨터의 동일한 위치에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="48548-133">다음은 그룹 정책 파일의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="48548-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="48548-134">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="48548-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="48548-135">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="48548-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="48548-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="48548-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="48548-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="48548-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="48548-138">fr-fr\\ BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="48548-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="48548-139">fr-fr\\ BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="48548-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="48548-140">(및 각각의 지원 되는 언어에 대해 유사)</span><span class="sxs-lookup"><span data-stu-id="48548-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="48548-141">MBAM 국제 릴리스의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="48548-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="48548-142">이 항목에서는 Microsoft BitLocker 관리 및 국제 릴리스의 알려진 문제점에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="48548-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="48548-143">MBAM 다국어 릴리스의 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="48548-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="48548-144">MBAM 1.0 언어 업데이트를 배포 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="48548-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="48548-145">MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="48548-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





