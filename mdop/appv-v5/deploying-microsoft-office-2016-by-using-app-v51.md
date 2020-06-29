---
title: App-V를 사용하여 Microsoft Office 2016 배포
description: App-V를 사용하여 Microsoft Office 2016 배포
author: dansimp
ms.assetid: e0f4876-da99-4b89-977e-2fb6e89ea3d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: b47fd46c8dc368bbce819b24f18fa30328fbbaf0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814609"
---
# <span data-ttu-id="b82dc-103">App-V를 사용하여 Microsoft Office 2016 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-103">Deploying Microsoft Office 2016 by Using App-V</span></span>


<span data-ttu-id="b82dc-104">Microsoft Application Virtualization (App-v) 5.1 이상 버전을 사용 하 여 조직의 컴퓨터에 Microsoft Office 2016을 가상화 된 응용 프로그램으로 제공 하려면이 문서의 정보를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2016 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="b82dc-105">Office 2013를 제공 하기 위해 App-v를 사용 하는 방법에 대 한 자세한 내용은 [app-v를 사용 하 여 Microsoft Office 2013 배포](deploying-microsoft-office-2013-by-using-app-v51.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-105">For information about using App-V to deliver Office 2013, see [Deploying Microsoft Office 2013 by Using App-V](deploying-microsoft-office-2013-by-using-app-v51.md).</span></span> <span data-ttu-id="b82dc-106">Office 2010를 제공 하기 위해 App-v를 사용 하는 방법에 대 한 자세한 내용은 [app-v를 사용 하 여 Microsoft Office 2010 배포](deploying-microsoft-office-2010-by-using-app-v51.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-106">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span>

<span data-ttu-id="b82dc-107">이 항목의 섹션:</span><span class="sxs-lookup"><span data-stu-id="b82dc-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b82dc-108">시작 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="b82dc-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="b82dc-109">Office 배포 도구를 사용 하 여 App-v 용 Office 2016 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="b82dc-109">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="b82dc-110">앱에 대 한 Office 패키지 게시-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b82dc-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="b82dc-111">Office 앱-V 패키지 사용자 지정 및 관리</span><span class="sxs-lookup"><span data-stu-id="b82dc-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="b82dc-112">시작 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="b82dc-112">What to know before you start</span></span>


<span data-ttu-id="b82dc-113">App-v를 사용 하 여 Office 2016를 배포 하기 전에 다음 계획 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-113">Before you deploy Office 2016 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="b82dc-114">지원 되는 Office 버전 및 Office 공존</span><span class="sxs-lookup"><span data-stu-id="b82dc-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="b82dc-115">다음 표를 사용 하 여 지원 되는 Office 버전에 대 한 정보를 확인 하 고 공존할 수 있는 Office 버전을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-116">검토할 정보</span><span class="sxs-lookup"><span data-stu-id="b82dc-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="b82dc-117">설명</span><span class="sxs-lookup"><span data-stu-id="b82dc-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="b82dc-118">지원 되는 Microsoft Office 버전</span><span class="sxs-lookup"><span data-stu-id="b82dc-118">Supported versions of Microsoft Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b82dc-119">지원 되는 Office 버전</span><span class="sxs-lookup"><span data-stu-id="b82dc-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="b82dc-120">지원 되는 배포 유형 (예: 데스크톱, VDI (개인용 가상 데스크톱 인프라), 풀링된 VDI)</span><span class="sxs-lookup"><span data-stu-id="b82dc-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="b82dc-121">Office 라이선스 옵션</span><span class="sxs-lookup"><span data-stu-id="b82dc-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="b82dc-122">동시 버전의 Office를 사용 하 여 App-v 사용 계획</span><span class="sxs-lookup"><span data-stu-id="b82dc-122">Planning for Using App-V with coexisting versions of Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="b82dc-123">같은 컴퓨터에 여러 버전의 Office를 설치할 때의 고려 사항</span><span class="sxs-lookup"><span data-stu-id="b82dc-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="b82dc-124">패키징, 게시 및 배포 요구 사항</span><span class="sxs-lookup"><span data-stu-id="b82dc-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="b82dc-125">App-v를 사용 하 여 Office를 배포 하기 전에 다음 요구 사항을 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-126">작업</span><span class="sxs-lookup"><span data-stu-id="b82dc-126">Task</span></span></th>
<th align="left"><span data-ttu-id="b82dc-127">요구 사항</span><span class="sxs-lookup"><span data-stu-id="b82dc-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-128">패키징</span><span class="sxs-lookup"><span data-stu-id="b82dc-128">Packaging</span></span></p></td>
<td align="left">
<ul>
<li><p><span data-ttu-id="b82dc-129">사용자에 게 배포 하려는 모든 Office 응용 프로그램은 단일 패키지에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-130">App-v 5.1 이상에서는 Office 배포 도구를 사용 하 여 패키지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="b82dc-131">Sequencer는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-132">Office와 함께 Microsoft Visio 2016 및 Microsoft Project 2016을 배포 하는 경우 Office와 동일한 패키지에 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-132">If you are deploying Microsoft Visio 2016 and Microsoft Project 2016 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="b82dc-133">자세한 내용은 <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> Office를 사용 하 여 Visio 2016 및 Project 2016 배포를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="b82dc-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2016 and Project 2016 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b82dc-134">게시</span><span class="sxs-lookup"><span data-stu-id="b82dc-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b82dc-135">각 클라이언트 컴퓨터에 하나의 Office 패키지만 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-136">Office 패키지를 전역적으로 게시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-136">You must publish the Office package globally.</span></span> <span data-ttu-id="b82dc-137">사용자에 게 게시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-138">예를 들어 원격 데스크톱 서비스를 사용 하 여 다음 제품을 공유 컴퓨터에 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="b82dc-139">엔터프라이즈 용 Microsoft 365 앱</span><span class="sxs-lookup"><span data-stu-id="b82dc-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="b82dc-140">Visio Pro for Office 365</span><span class="sxs-lookup"><span data-stu-id="b82dc-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="b82dc-141">Project Pro for Office 365</span><span class="sxs-lookup"><span data-stu-id="b82dc-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="b82dc-142">공유 컴퓨터 정품 인증을 사용 하도록 설정 해야 합니다 <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="b82dc-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
</td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b82dc-143">패키지에서 Office 응용 프로그램 제외</span><span class="sxs-lookup"><span data-stu-id="b82dc-143">Excluding Office applications from a package</span></span>

<span data-ttu-id="b82dc-144">다음 표에서는 패키지에서 특정 Office 응용 프로그램을 제외 하기 위해 권장 되는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-144">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-145">작업</span><span class="sxs-lookup"><span data-stu-id="b82dc-145">Task</span></span></th>
<th align="left"><span data-ttu-id="b82dc-146">세부 정보</span><span class="sxs-lookup"><span data-stu-id="b82dc-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-147"><strong> </strong> Office 배포 도구를 사용 하 여 패키지를 만들 때 excludeapp 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-147">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b82dc-148">Office 배포 도구가 패키지를 만들 때 패키지에서 특정 Office 응용 프로그램을 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-148">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="b82dc-149">예를 들어이 설정을 사용 하 여 Microsoft 단어만 포함 된 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-149">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-150">자세한 내용은 <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> excludeapp 요소를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="b82dc-150">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b82dc-151">DeploymentConfig.xml 파일 수정</span><span class="sxs-lookup"><span data-stu-id="b82dc-151">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b82dc-152">패키지를 만든 후 DeploymentConfig.xml 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-152">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="b82dc-153">이 파일에는 App-v 클라이언트를 실행 하는 컴퓨터의 모든 사용자에 대 한 기본 패키지 설정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-153">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-154">자세한 내용은 <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> Office 2016 응용 프로그램 사용 안 함을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="b82dc-154">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)">Disabling Office 2016 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="b82dc-155">Office 배포 도구를 사용 하 여 App-v 용 Office 2016 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="b82dc-155">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="b82dc-156">App-v 5.1 이상 버전의 Office 2016 패키지를 만들려면 다음 단계를 완료 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-156">Complete the following steps to create an Office 2016 package for App-V 5.1 or later.</span></span>

><span data-ttu-id="b82dc-157">**Important** &nbsp; 중요 &nbsp; App-v 5.1 이상에서는 Office 배포 도구를 사용 하 여 패키지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-157">**Important**&nbsp;&nbsp;In App-V 5.1 and later, you must use the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="b82dc-158">Sequencer를 사용 하 여 패키지를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-158">You cannot use the Sequencer to create packages.</span></span>

### <span data-ttu-id="b82dc-159">Office 배포 도구를 사용 하기 위한 필수 구성 요소 검토</span><span class="sxs-lookup"><span data-stu-id="b82dc-159">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="b82dc-160">Office 배포 도구를 설치 하는 컴퓨터에는 다음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-160">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-161">요소일</span><span class="sxs-lookup"><span data-stu-id="b82dc-161">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="b82dc-162">설명</span><span class="sxs-lookup"><span data-stu-id="b82dc-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-163">필수 구성 요소 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="b82dc-163">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-164">.Net Framework 4</span><span class="sxs-lookup"><span data-stu-id="b82dc-164">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b82dc-165">지원되는 운영 체제</span><span class="sxs-lookup"><span data-stu-id="b82dc-165">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b82dc-166">64 비트 버전의 Windows 10</span><span class="sxs-lookup"><span data-stu-id="b82dc-166">64-bit version of Windows 10</span></span></p></li>
<li><p><span data-ttu-id="b82dc-167">64 비트 버전의 Windows 8 또는 8.1</span><span class="sxs-lookup"><span data-stu-id="b82dc-167">64-bit version of Windows 8 or 8.1</span></span></p></li>
<li><p><span data-ttu-id="b82dc-168">64 비트 버전의 Windows 7</span><span class="sxs-lookup"><span data-stu-id="b82dc-168">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


><span data-ttu-id="b82dc-169">**참고**  이 항목에서 "Office 2016 App-V 패키지" 라는 용어는 구독 라이선스를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-169">**Note**  In this topic, the term “Office 2016 App-V package” refers to subscription licensing.</span></span>


### <span data-ttu-id="b82dc-170">Office 배포 도구를 사용 하 여 Office 2016 앱-V 패키지 만들기</span><span class="sxs-lookup"><span data-stu-id="b82dc-170">Create Office 2016 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="b82dc-171">Office 배포 도구를 사용 하 여 Office 2016 앱-V 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-171">You create Office 2016 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="b82dc-172">다음 지침에서는 구독 라이선스를 사용 하 여 Office 2016 App-v 패키지를 만드는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-172">The following instructions explain how to create an Office 2016 App-V package with Subscription Licensing.</span></span>

<span data-ttu-id="b82dc-173">64 비트 Windows 컴퓨터에서 Office 2016 앱-V 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-173">Create Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="b82dc-174">Office 2016 앱-V 패키지는 일단 만들어지면 32 비트 및 64 비트 Windows 7, Windows 8.1 및 Windows 10 컴퓨터에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-174">Once created, the Office 2016 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="b82dc-175">Office 배포 도구 다운로드</span><span class="sxs-lookup"><span data-stu-id="b82dc-175">Download the Office Deployment Tool</span></span>

<span data-ttu-id="b82dc-176">Office 2016 앱-V 패키지는 office 2016 App-v 패키지를 생성 하는 Office 배포 도구를 사용 하 여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-176">Office 2016 App-V Packages are created using the Office Deployment Tool, which generates an Office 2016 App-V Package.</span></span> <span data-ttu-id="b82dc-177">앱-V 시퀀서를 통해 패키지를 만들거나 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-177">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="b82dc-178">패키지 만들기를 시작 하려면 다음을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-178">To begin package creation:</span></span>

1.  <span data-ttu-id="b82dc-179">[간편 실행을 위한 Office 2016 배포 도구](https://www.microsoft.com/download/details.aspx?id=49117)를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-179">Download the [Office 2016 Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span>

> <span data-ttu-id="b82dc-180">**중요** Office 2016 App-v 패키지를 만들려면 Office 2016 배포 도구를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-180">**Important** You must use the Office 2016 Deployment Tool to create Office 2016 App-V Packages.</span></span>
> 2. <span data-ttu-id="b82dc-181">.Exe 파일을 실행 하 고 원하는 위치에 해당 기능을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-181">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="b82dc-182">이 프로세스를 더 쉽게 하려면 기능을 저장할 공유 네트워크 폴더를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-182">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    Example: \\\\Server\\Office2016

3. <span data-ttu-id="b82dc-183">setup.exe 및 configuration.xml 파일이 존재 하며 지정한 위치에 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-183">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="b82dc-184">Office 2016 응용 프로그램 다운로드</span><span class="sxs-lookup"><span data-stu-id="b82dc-184">Download Office 2016 applications</span></span>

<span data-ttu-id="b82dc-185">Office 배포 도구를 다운로드 한 후에이를 사용 하 여 최신 Office 2016 응용 프로그램을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-185">After you download the Office Deployment Tool, you can use it to get the latest Office 2016 applications.</span></span> <span data-ttu-id="b82dc-186">Office 응용 프로그램을 가져온 후 Office 2016 App-v 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-186">After getting the Office applications, you create the Office 2016 App-V package.</span></span>

<span data-ttu-id="b82dc-187">Office 배포 도구에 포함 된 XML 파일은 포함 된 언어 및 Office 응용 프로그램과 같은 제품 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-187">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="b82dc-188">**예제 XML 구성 파일을 사용자 지정 합니다.** Office 배포 도구를 사용 하 여 다운로드 한 샘플 XML 구성 파일을 사용 하 여 Office 응용 프로그램을 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-188">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="b82dc-189">메모장 또는 즐겨 찾는 텍스트 편집기에서 샘플 XML 파일을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-189">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="b82dc-190">샘플 configuration.xml 파일을 열어 편집할 수 있는 상태에서 Office 2016 응용 프로그램을 저장 하는 제품, 언어, 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-190">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2016 applications.</span></span> <span data-ttu-id="b82dc-191">다음은 configuration.xml 파일의 기본 예입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-191">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      ><span data-ttu-id="b82dc-192">**참고**  구성 XML은 샘플 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-192">**Note**  The configuration XML is a sample XML file.</span></span> <span data-ttu-id="b82dc-193">파일에는 주석 처리 된 줄이 포함 됩니다. 이러한 줄을 "주석 처리" 하 여 파일에 대 한 추가 설정을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-193">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span> <span data-ttu-id="b82dc-194">이러한 줄을 "주석으로 처리" 하려면 "<!을 (를) 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-194">To “uncomment” these lines, remove the "<!</span></span> <span data-ttu-id="b82dc-195">--"줄의 시작 부분에 있고 줄 끝에서"--> "입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-195">- -" from the beginning of the line, and the "-- >" from the end of the line.</span></span>

      <span data-ttu-id="b82dc-196">위의 XML 구성 파일은 Visio ProPlus를 포함 하 여 Office 2016 ProPlus 32 비트 에디션을 영어로 다운로드 하 여 Office 응용 프로그램이 저장 되는 위치인 \\\\server\\Office 2016에이를 설치 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-196">The above XML configuration file specifies that Office 2016 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2016, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="b82dc-197">응용 프로그램의 제품 ID는 Office의 최종 라이선스에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-197">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="b82dc-198">이후 단계에서 라이선스를 지정 하 여 다양 한 라이선스를 포함 하는 Office 2016 앱-V 패키지를 같은 응용 프로그램에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-198">Office 2016 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="b82dc-199">아래 표에는 XML 파일의 사용자 지정 가능한 특성 및 요소가 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-199">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="b82dc-200">입력</span><span class="sxs-lookup"><span data-stu-id="b82dc-200">Input</span></span></th>
      <th align="left"><span data-ttu-id="b82dc-201">설명</span><span class="sxs-lookup"><span data-stu-id="b82dc-201">Description</span></span></th>
      <th align="left"><span data-ttu-id="b82dc-202">예</span><span class="sxs-lookup"><span data-stu-id="b82dc-202">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="b82dc-203">요소 추가</span><span class="sxs-lookup"><span data-stu-id="b82dc-203">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-204">패키지에 포함할 제품 및 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-204">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-205">해당 없음</span><span class="sxs-lookup"><span data-stu-id="b82dc-205">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="b82dc-206">OfficeClientEdition (Add 요소의 특성)</span><span class="sxs-lookup"><span data-stu-id="b82dc-206">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-207">사용할 Office 2016 제품 버전 (32 비트 또는 64-비트)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-207">Specifies the edition of Office 2016 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="b82dc-208"><strong>OfficeClientEdition </strong> 가 유효한 값으로 설정 되지 않은 경우 작업이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-208">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="b82dc-209">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="b82dc-209">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="b82dc-210">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="b82dc-210">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="b82dc-211">Product 요소</span><span class="sxs-lookup"><span data-stu-id="b82dc-211">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-212">응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-212">Specifies the application.</span></span> <span data-ttu-id="b82dc-213">여기에 프로젝트 2016 및 Visio 2016을 여기에 지정 하 여 응용 프로그램에 포함 시킬 추가 된 제품이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-213">Project 2016 and Visio 2016 must be specified here as an added product to be included in the applications.</span></span>

      <span data-ttu-id="b82dc-214">제품 Id에 대 한 자세한 내용은 <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> Office 배포 도구에서 간편 실행 용으로 지원 되는 제품 id를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-214">For more information about the product IDs, see <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)">Product IDs that are supported by the Office Deployment Tool for Click-to-Run</span></span></a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="b82dc-215">Language 요소</span><span class="sxs-lookup"><span data-stu-id="b82dc-215">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-216">응용 프로그램에서 지원 되는 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-216">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="b82dc-217">버전 (요소 추가의 특성)</span><span class="sxs-lookup"><span data-stu-id="b82dc-217">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-218">선택 사항.</span><span class="sxs-lookup"><span data-stu-id="b82dc-218">Optional.</span></span> <span data-ttu-id="b82dc-219">패키지에 사용할 빌드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-219">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="b82dc-220">Office 원본의 v32.CAB에 정의 된 최신 광고 빌드를 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-220">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="b82dc-221">SourcePath (Add 요소의 특성)</span><span class="sxs-lookup"><span data-stu-id="b82dc-221">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-222">응용 프로그램이 저장 되는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-222">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="b82dc-223">분기 (요소 추가의 특성)</span><span class="sxs-lookup"><span data-stu-id="b82dc-223">Branch (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="b82dc-224">선택 사항.</span><span class="sxs-lookup"><span data-stu-id="b82dc-224">Optional.</span></span> <span data-ttu-id="b82dc-225">다운로드 하거나 설치할 제품에 대 한 업데이트 분기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-225">Specifies the update branch for the product that you want to download or install.</span></span> </p><p><span data-ttu-id="b82dc-226">업데이트 분기에 대 한 자세한 내용은 엔터프라이즈 용 Microsoft 365 앱에 대 한 업데이트 분기 개요를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-226">For more information about update branches, see Overview of update branches for Microsoft 365 Apps for enterprise.</span></span></p></td>
      <td align="left"><p><code>Branch = &quot;Business&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="b82dc-227">원하는 제품, 언어, 그리고 Office 2016 응용 프로그램이 저장 되는 위치를 지정 하도록 configuration.xml 파일을 편집한 후에는 구성 파일 (예: Customconfig.xml)을 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-227">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2016 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="b82dc-228">**지정 된 위치에 응용 프로그램을 다운로드 합니다.** 관리자 권한 명령 프롬프트 및 64 비트 운영 체제를 사용 하 여 나중에 App-v 패키지로 변환 될 Office 2016 응용 프로그램을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-228">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2016 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="b82dc-229">다음은 세부 정보에 대 한 설명이 포함 된 예제 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-229">Below is an example command with a description of details:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   <span data-ttu-id="b82dc-230">예제:</span><span class="sxs-lookup"><span data-stu-id="b82dc-230">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-231">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="b82dc-231">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-232">은 Office 배포 도구와 사용자 지정 Configuration.xml 파일 Customconfig.xml 포함 하는 네트워크 공유 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-232">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b82dc-233">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b82dc-233">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-234">Office 배포 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-234">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-235">/download</span><span class="sxs-lookup"><span data-stu-id="b82dc-235">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-236">customConfig.xml 파일에서 지정 하는 Office 2016 응용 프로그램을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-236">downloads the Office 2016 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="b82dc-237">나중에 볼륨 라이선스를 사용 하 여 Office 2016 앱-V 패키지에서 이러한 비트를 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-237">These bits can be later converted in an Office 2016 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b82dc-238">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b82dc-238">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-239">다운로드 프로세스를 완료 하는 데 필요한 XML 구성 파일을 전달 합니다 (이 예제에서는 customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b82dc-239">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="b82dc-240">다운로드 명령을 사용한 후에는 구성 xml 파일에 지정 된 위치에서 Office 응용 프로그램을 찾을 수 있습니다 (이 예제에서는 \Server\Office2016.).</span><span class="sxs-lookup"><span data-stu-id="b82dc-240">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2016.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="b82dc-241">Office 응용 프로그램을 앱-V 패키지로 변환</span><span class="sxs-lookup"><span data-stu-id="b82dc-241">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="b82dc-242">Office 배포 도구를 통해 Office 2016 응용 프로그램을 다운로드 한 후 office 배포 도구를 사용 하 여 office 2016 App-v 패키지로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-242">After you download the Office 2016 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2016 App-V package.</span></span> <span data-ttu-id="b82dc-243">라이선스 모델에 해당 하는 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-243">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="b82dc-244">수행 해야 하는 작업에 대 한 요약:</span><span class="sxs-lookup"><span data-stu-id="b82dc-244">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="b82dc-245">64 비트 Windows 컴퓨터에서 Office 2016 앱-V 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-245">Create the Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="b82dc-246">그러나 패키지는 32 비트 및 64 비트 Windows 7, Windows 8 또는 8.1 및 Windows 10 컴퓨터에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-246">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8 or 8.1, and Windows 10 computers.</span></span>

-   <span data-ttu-id="b82dc-247">Office 배포 도구를 사용 하 여 구독 라이선스 패키지에 대 한 Office 앱-V 패키지를 만든 다음 CustomConfig.xml 구성 파일을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-247">Create an Office App-V package for Subscription Licensing package by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="b82dc-248">다음 표에는 사용 중인 라이선스 모델의 CustomConfig.xml 파일에 입력 해야 하는 값이 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-248">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="b82dc-249">표 다음에 나오는 섹션의 단계에서는 필요한 정확한 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-249">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

><span data-ttu-id="b82dc-250">**Note** &nbsp; 참고 &nbsp; Office 배포 도구를 사용 하 여 엔터프라이즈 용 Microsoft 365 앱에 대 한 앱 V 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-250">**Note**&nbsp;&nbsp;You can use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="b82dc-251">볼륨 라이선스 버전의 Office Professional Plus 또는 Office Standard에 대 한 패키지 만들기는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-251">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-252">제품 ID</span><span class="sxs-lookup"><span data-stu-id="b82dc-252">Product ID</span></span></th>
<th align="left"><span data-ttu-id="b82dc-253">구독 라이선스</span><span class="sxs-lookup"><span data-stu-id="b82dc-253">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b82dc-254">Office 2016</span><span class="sxs-lookup"><span data-stu-id="b82dc-254">Office 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b82dc-255">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="b82dc-255">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b82dc-256">Office 2016 (Visio 2016)</span><span class="sxs-lookup"><span data-stu-id="b82dc-256">Office 2016 with Visio 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b82dc-257">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="b82dc-257">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="b82dc-258">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="b82dc-258">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b82dc-259">Office 2016 (Visio 2016 및 Project 2016)</span><span class="sxs-lookup"><span data-stu-id="b82dc-259">Office 2016 with Visio 2016 and Project 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b82dc-260">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="b82dc-260">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="b82dc-261">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="b82dc-261">VisioProRetail</span></span></p>
<p><span data-ttu-id="b82dc-262">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="b82dc-262">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b82dc-263">Office 응용 프로그램을 앱-V 패키지로 변환 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b82dc-263">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="b82dc-264">메모장에서 CustomConfig.xml 파일을 다시 열고 파일을 다음과 같이 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-264">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="b82dc-265">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b82dc-265">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="b82dc-266">값을 변경할 대상</span><span class="sxs-lookup"><span data-stu-id="b82dc-266">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b82dc-267">SourcePath</span><span class="sxs-lookup"><span data-stu-id="b82dc-267">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-268">이전에 다운로드 한 Office 응용 프로그램을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-268">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b82dc-269">ProductID</span><span class="sxs-lookup"><span data-stu-id="b82dc-269">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-270">다음 예제에 표시 된 대로 구독 라이선스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-270">Specify Subscription licensing, as shown in the following example:</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="b82dc-271">이 예제에서는 구독 라이선스를 사용 하 여 패키지를 만들기 위해 다음과 같이 변경 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-271">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-272">SourcePath</span><span class="sxs-lookup"><span data-stu-id="b82dc-272">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-273">는 이전에 다운로드 된 Office 응용 프로그램을 가리키도록 변경 된 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-273">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b82dc-274">제품 ID</span><span class="sxs-lookup"><span data-stu-id="b82dc-274">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-275">(으)로 변경 되었습니다 <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="b82dc-275">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-276">제품 ID</span><span class="sxs-lookup"><span data-stu-id="b82dc-276">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-277">Visio는으로 변경 되었습니다 <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="b82dc-277">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b82dc-278">ExcludeApp (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b82dc-278">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-279">Office 배포 도구가 만드는 App-v 패키지에 포함 하지 않을 Office 프로그램을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-279">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="b82dc-280">예를 들어 Access 및 InfoPath는 제외할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-280">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b82dc-281">PACKAGEGUID (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="b82dc-281">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-282">기본적으로 Office 배포 도구에서 만든 모든 App-v 패키지는 동일한 App-v 패키지 ID를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-282">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="b82dc-283">PACKAGEGUID를 사용 하 여 각 패키지에 대해 다른 패키지 ID를 지정할 수 있으며,이를 통해 Office 배포 도구에서 만든 여러 App-v 패키지를 게시 하 고 App-v 서버를 사용 하 여 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-283">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="b82dc-284">이 매개 변수를 사용 하는 경우 사용자 마다 다른 패키지를 만드는 경우를 예로 들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-284">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="b82dc-285">예를 들어 일부 사용자를 위해 Office 2016만 사용 하 여 패키지를 만들고 다른 사용자 집합에 대해 Office 2016 및 Visio 2016을 사용 하 여 다른 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-285">For example, you can create a package with just Office 2016 for some users, and create another package with Office 2016 and Visio 2016 for another set of users.</span></span></p>

   <span data-ttu-id="b82dc-286">&gt;<strong>참고 </strong> 고유한 패키지 id를 사용 하는 경우에도 단일 장치에 하나의 앱 V 패키지만 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-286">&gt;<strong>Note</strong> Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span>
   </td>
   </tr>
   </tbody>
   </table>


2. <span data-ttu-id="b82dc-287">/Packager 명령을 사용 하 여 Office 응용 프로그램을 Office 2016 App-v 패키지로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-287">Use the /packager command to convert the Office applications to an Office 2016 App-V package.</span></span>

   <span data-ttu-id="b82dc-288">예:</span><span class="sxs-lookup"><span data-stu-id="b82dc-288">For example:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   <span data-ttu-id="b82dc-289">예제:</span><span class="sxs-lookup"><span data-stu-id="b82dc-289">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-290">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="b82dc-290">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-291">은 Office 배포 도구와 사용자 지정 Configuration.xml 파일 Customconfig.xml 포함 하는 네트워크 공유 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-291">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b82dc-292">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b82dc-292">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-293">Office 배포 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-293">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-294">/packager</span><span class="sxs-lookup"><span data-stu-id="b82dc-294">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-295">customConfig.xml 파일에 지정 된 라이선스 유형을 사용 하 여 Office 2016 앱-V 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-295">creates the Office 2016 App-V package with the type of licensing specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b82dc-296">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b82dc-296">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-297">패키징 단계에 대해 준비한 구성 XML 파일 (이 경우 customConfig)을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-297">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b82dc-298">\server\share\Office 2016AppV</span><span class="sxs-lookup"><span data-stu-id="b82dc-298">\server\share\Office 2016AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b82dc-299">새로 만든 Office App-v 패키지의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-299">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="b82dc-300">Office 2016 App-v 패키지가 올바르게 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-300">Verify that the Office 2016 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="b82dc-301">전역으로 만든 Office 2016 App-v 패키지를 테스트 컴퓨터에 게시 하 고 Office 2016 바로 가기가 표시 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-301">Publish the Office 2016 App-V package, which you created globally, to a test computer, and verify that the Office 2016 shortcuts appear.</span></span>

   2.  <span data-ttu-id="b82dc-302">Excel 또는 Word 등의 몇 가지 Office 2016 응용 프로그램을 시작 하 여 패키지가 예상 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-302">Start a few Office 2016 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="b82dc-303">App-v 용 Office 패키지 게시-V</span><span class="sxs-lookup"><span data-stu-id="b82dc-303">Publishing the Office package for App-V</span></span>


<span data-ttu-id="b82dc-304">다음 정보를 사용 하 여 Office 패키지를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-304">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="b82dc-305">Office 앱-V 패키지 게시 방법</span><span class="sxs-lookup"><span data-stu-id="b82dc-305">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="b82dc-306">다른 패키지에 사용 하는 것과 동일한 방법을 사용 하 여 Office 2016의 App-v 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-306">Deploy the App-V package for Office 2016 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="b82dc-307">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b82dc-307">System Center Configuration Manager</span></span>

-   <span data-ttu-id="b82dc-308">App-v Server</span><span class="sxs-lookup"><span data-stu-id="b82dc-308">App-V Server</span></span>

-   <span data-ttu-id="b82dc-309">독립 실행형-PowerShell 명령</span><span class="sxs-lookup"><span data-stu-id="b82dc-309">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="b82dc-310">필수 구성 요소 및 요구 사항 게시</span><span class="sxs-lookup"><span data-stu-id="b82dc-310">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-311">필수 구성 요소 또는 요구 사항</span><span class="sxs-lookup"><span data-stu-id="b82dc-311">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="b82dc-312">세부 정보</span><span class="sxs-lookup"><span data-stu-id="b82dc-312">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-313">App-v 클라이언트에서 PowerShell 스크립트 사용</span><span class="sxs-lookup"><span data-stu-id="b82dc-313">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-314">Office 2016 패키지를 게시 하려면 스크립트를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-314">To publish Office 2016 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="b82dc-315">앱-V 클라이언트에서는 패키지 스크립트를 기본적으로 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-315">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="b82dc-316">스크립팅을 사용 하도록 설정 하려면 다음 PowerShell 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-316">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b82dc-317">전체적으로 Office 2016 패키지 게시</span><span class="sxs-lookup"><span data-stu-id="b82dc-317">Publish the Office 2016 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-318">Office App-v 패키지의 확장 지점은 컴퓨터 수준에서 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-318">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="b82dc-319">컴퓨터 수준에서 게시 하는 경우 필수 작업 또는 재배포 가능이 필요 하지 않으며 Office 2016 패키지를 전역적으로 응용 프로그램이 기본적으로 설치 된 Office와 동일 하 게 작동 하므로 관리자가 패키지를 사용자 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-319">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2016 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b82dc-320">Office 패키지를 게시 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b82dc-320">How to publish an Office package</span></span>

<span data-ttu-id="b82dc-321">다음 명령을 실행 하 여 Office 패키지를 전역적으로 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-321">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="b82dc-322">App-v 서버의 웹 관리 콘솔에서 사용자 그룹을 사용 하는 대신 컴퓨터 그룹에 대 한 사용 권한을 추가 하 여 패키지를 해당 그룹의 컴퓨터에 전역으로 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-322">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="b82dc-323">Office 앱-V 패키지 사용자 지정 및 관리</span><span class="sxs-lookup"><span data-stu-id="b82dc-323">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="b82dc-324">Office App-v 패키지를 관리 하려면 다른 패키지에 대해 수행 하는 것과 동일한 작업을 사용 하지만 다음 섹션에서 설명 하는 몇 가지 예외가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-324">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="b82dc-325">연결 그룹을 사용 하 여 Office 플러그 인 사용</span><span class="sxs-lookup"><span data-stu-id="b82dc-325">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="b82dc-326">Office 2016 응용 프로그램을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="b82dc-326">Disabling Office 2016 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="b82dc-327">Office 2016 바로 가기를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="b82dc-327">Disabling Office 2016 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="b82dc-328">Office 2016 패키지 업그레이드 관리</span><span class="sxs-lookup"><span data-stu-id="b82dc-328">Managing Office 2016 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="b82dc-329">Visio 2016 및 Project 2016을 Office와 함께 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-329">Deploying Visio 2016 and Project 2016 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="b82dc-330">연결 그룹을 사용 하 여 Office 플러그 인 사용</span><span class="sxs-lookup"><span data-stu-id="b82dc-330">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="b82dc-331">이 섹션의 단계를 사용 하 여 office 플러그 인을 Office 패키지와 함께 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-331">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="b82dc-332">Office 플러그 인을 사용 하려면 App-v 시퀀서를 사용 하 여 플러그 인만 포함 된 별도의 패키지를 만들어야 합니다. Office 배포 도구를 사용 하 여 플러그 인 패키지를 만들 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-332">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="b82dc-333">그런 다음 다음 단계에 설명 된 대로 Office 패키지 및 플러그 인 패키지를 포함 하는 연결 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-333">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="b82dc-334">Office 앱-V 패키지에 대 한 플러그 인을 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b82dc-334">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="b82dc-335">App-v Server, System Center Configuration Manager 또는 PowerShell cmdlet을 통해 연결 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-335">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="b82dc-336">App-v 시퀀서를 사용 하 여 플러그 인을 순서 대로 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-336">Sequence your plug-ins using the App-V Sequencer.</span></span> <span data-ttu-id="b82dc-337">플러그 인을 시퀀싱 하는 데 사용 되는 컴퓨터에 Office 2016이 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-337">Ensure that Office 2016 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="b82dc-338">Office 2016 플러그 인을 순서 대로 시퀀싱 하는 컴퓨터에서 Microsoft 365 앱 (비가상)을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-338">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2016 plug-ins.</span></span>

3.  <span data-ttu-id="b82dc-339">원하는 플러그 인을 포함 하는 App-v 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-339">Create an App-V package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="b82dc-340">App-v server, System Center Configuration Manager 또는 PowerShell cmdlet을 통해 연결 그룹을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-340">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="b82dc-341">만든 연결 그룹에 Office 2016 앱-V 패키지와 시퀀싱 한 플러그 인 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-341">Add the Office 2016 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    ><span data-ttu-id="b82dc-342">**중요** 연결 그룹의 패키지 순서에 따라 패키지 콘텐츠가 병합 되는 순서가 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-342">**Important** The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="b82dc-343">연결 그룹 설명자 파일에서 Office 2016 App-v 패키지를 먼저 추가한 다음 플러그인 App-v 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-343">In your Connection group descriptor file, add the Office 2016 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="b82dc-344">두 패키지가 모두 대상 컴퓨터에 게시 되 고 게시 된 Office 2016 App-v 패키지의 전역 설정에 맞게 플러그 인 패키지가 전역으로 게시 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-344">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2016 App-V package.</span></span>

7.  <span data-ttu-id="b82dc-345">플러그 인 패키지의 배포 구성 파일에 Office 2016 App-v 패키지와 동일한 설정이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-345">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2016 App-V package has.</span></span>

    <span data-ttu-id="b82dc-346">Office 2016 App-v 패키지가 운영 체제와 통합 되어 있기 때문에 플러그 인 패키지 설정이 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-346">Since the Office 2016 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="b82dc-347">배포 구성 파일에서 "COM 모드"를 검색 하 고 플러그 인 패키지에 "통합 됨"으로 설정 되어 있는지 확인 하 고 "InProcessEnabled" 및 "OutOfProcessEnabled"이 모두 게시 한 Office 2016 App-v 패키지의 설정과 일치 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-347">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2016 App-V package you published.</span></span>

8.  <span data-ttu-id="b82dc-348">배포 구성 파일을 열고 **사용할 수 있는 개체** 값을 **false**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-348">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="b82dc-349">시퀀싱 한 후에 배포 구성 파일을 변경한 경우 플러그 인 패키지가 파일과 함께 게시 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-349">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="b82dc-350">만든 연결 그룹이 원하는 컴퓨터에 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-350">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="b82dc-351">연결 그룹을 사용 하는 경우 Office 2016 App-v 패키지를 사용 하는 경우 생성 되는 연결 그룹은 "보류" 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-351">The Connection Group created will likely “pend” if the Office 2016 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="b82dc-352">이 문제가 발생 하면 다시 부팅 하 여 연결 그룹을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-352">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="b82dc-353">두 패키지를 성공적으로 게시 하 고 연결 그룹을 사용 하도록 설정한 후에는 대상 Office 2016 응용 프로그램을 시작 하 고, 게시 하 고 추가한 플러그 인이 필요한 대로 작동 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-353">After you successfully publish both packages and enable the Connection Group, start the target Office 2016 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="b82dc-354">Office 2016 응용 프로그램을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="b82dc-354">Disabling Office 2016 applications</span></span>

<span data-ttu-id="b82dc-355">Office 앱-V 패키지에서 특정 응용 프로그램을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-355">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="b82dc-356">예를 들어 Access를 사용 하지 않도록 설정할 수 있지만 다른 모든 Office 응용 프로그램의 기본은 사용할 수 있는 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-356">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="b82dc-357">응용 프로그램을 사용 하지 않도록 설정 하면 최종 사용자가 더 이상 해당 응용 프로그램의 바로 가기를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-357">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="b82dc-358">응용 프로그램을 다시 시퀀싱 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-358">You do not have to re-sequence the application.</span></span> <span data-ttu-id="b82dc-359">Office 2016 앱-V 패키지를 게시 한 후 배포 구성 파일을 변경 하는 경우 변경 내용을 저장 하 고 Office 2016 App-v 패키지를 추가한 다음 새 배포 구성 파일을 사용 하 여 새 설정을 적용 하는 Office 2016 App-v 패키지 응용 프로그램에 다시 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-359">When you change the Deployment Configuration File after the Office 2016 App-V package has been published, you will save the changes, add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

><span data-ttu-id="b82dc-360">**참고** Office 배포 도구를 사용 하 여 앱-V 패키지를 만들 때 특정 Office 응용 프로그램 (예: Access 및 InfoPath)을 제외 하려면 **Excludeapp** 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-360">**Note** To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span>


**<span data-ttu-id="b82dc-361">Office 2016 응용 프로그램을 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b82dc-361">To disable an Office 2016 application</span></span>**

1.  <span data-ttu-id="b82dc-362">**메모장과** 같은 텍스트 편집기를 사용 하 여 배포 구성 파일을 열고 "응용 프로그램"을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-362">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="b82dc-363">사용 하지 않으려는 Office 응용 프로그램 (예: Access 2016)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-363">Search for the Office application you want to disable, for example, Access 2016.</span></span>

3.  <span data-ttu-id="b82dc-364">"사용" 값을 "true"에서 "false"로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-364">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="b82dc-365">배포 구성 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-365">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="b82dc-366">새 배포 구성 파일을 사용 하 여 Office 2016 App-v 패키지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-366">Add the Office 2016 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="b82dc-367">Office 2016 App-v 패키지를 다시 추가한 다음 새 배포 구성 파일을 사용 하 여 Office 2016 앱-V 패키지 응용 프로그램에 새 설정을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-367">Re-add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="b82dc-368">Office 2016 바로 가기를 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="b82dc-368">Disabling Office 2016 shortcuts</span></span>

<span data-ttu-id="b82dc-369">패키지를 게시 취소 하거나 제거 하는 대신 특정 Office 응용 프로그램의 바로 가기를 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-369">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="b82dc-370">다음 예제에서는 Microsoft Access의 바로 가기를 사용 하지 않도록 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-370">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="b82dc-371">Office 2016 응용 프로그램의 바로 가기를 사용 하지 않도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b82dc-371">To disable shortcuts for Office 2016 applications</span></span>**

1.  <span data-ttu-id="b82dc-372">메모장에서 배포 구성 파일을 열고 "바로 가기"를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-372">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="b82dc-373">특정 바로 가기를 사용 하지 않도록 설정 하려면 원하지 않는 특정 바로 가기를 삭제 하거나 주석으로 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-373">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="b82dc-374">하위 시스템을 표시 하 고 사용 하도록 유지 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-374">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="b82dc-375">예를 들어 아래 예제에서는 Microsoft Access 바로 가기를 삭제 하 고, 하위 시스템 바로 가기 &lt; &gt; &lt; /바로 가기는 &gt; 그대로 유지 하 여 microsoft access 바로 가기를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-375">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="b82dc-376">배포 구성 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-376">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="b82dc-377">새 배포 구성 파일을 사용 하 여 Office 2016 App-v 패키지를 다시 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-377">Republish Office 2016 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="b82dc-378">앱-V 패키지에 대 한 배포 구성 (예: 파일 형식 연결, 가상 파일 시스템 등)을 수정 하 여 다양 한 추가 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-378">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="b82dc-379">배포 구성 파일을 사용 하 여 App-v 패키지 설정을 변경 하는 방법에 대 한 자세한 내용은이 문서의 뒷부분에 나오는 추가 리소스 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82dc-379">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="b82dc-380">Office 2016 패키지 업그레이드 관리</span><span class="sxs-lookup"><span data-stu-id="b82dc-380">Managing Office 2016 package upgrades</span></span>

<span data-ttu-id="b82dc-381">Office 2016 패키지를 업그레이드 하려면 Office 배포 도구를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-381">To upgrade an Office 2016 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="b82dc-382">이전에 배포 된 Office 2016 패키지를 업그레이드 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-382">To upgrade a previously deployed Office 2016 package, perform the following steps.</span></span>

**<span data-ttu-id="b82dc-383">이전에 배포 된 Office 2016 패키지를 업그레이드 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b82dc-383">How to upgrade a previously deployed Office 2016 package</span></span>**

1. <span data-ttu-id="b82dc-384">최신 Office 2016 응용 프로그램 소프트웨어를 사용 하는 Office 배포 도구를 통해 새 Office 2016 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-384">Create a new Office 2016 package through the Office Deployment Tool that uses the most recent Office 2016 application software.</span></span> <span data-ttu-id="b82dc-385">가장 최근의 Office 2016 비트는 Office 2016 App-v 패키지를 만드는 다운로드 단계를 통해 언제 든 지 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-385">The most recent Office 2016 bits can always be obtained through the download stage of creating an Office 2016 App-V Package.</span></span> <span data-ttu-id="b82dc-386">새로 생성 된 Office 2016 패키지에는 최신 업데이트와 새 버전 ID가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-386">The newly created Office 2016 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="b82dc-387">Office 배포 도구를 사용 하 여 만든 모든 패키지에는 동일한 계보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-387">All packages created using the Office Deployment Tool have the same lineage.</span></span>

   > <span data-ttu-id="b82dc-388">**참고** Office 앱-V 패키지에는 두 가지 버전 Id가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-388">**Note** Office App-V packages have two Version IDs:</span></span>
   > <ul>
   > <li><span data-ttu-id="b82dc-389">Office 배포 도구를 사용 하 여 만든 모든 패키지에서 고유한 Office 2016 App-v 패키지 버전 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-389">An Office 2016 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span></li>
   > <li><span data-ttu-id="b82dc-390">새 버전의 Office가 있는 경우에만 변경 되는 두 번째 App-v 패키지 버전 ID, x.x. x 예: AppX 매니페스트</span><span class="sxs-lookup"><span data-stu-id="b82dc-390">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="b82dc-391">예를 들어 업그레이드 된 새 Office 2016 릴리스를 사용할 수 있고 이러한 업그레이드를 통합 하기 위해 Office 배포 도구를 통해 패키지를 만들면 X.x.x.x 버전 ID가 변경 되어 Office 버전 자체가 변경 되었음을 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-391">For example, if a new Office 2016 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="b82dc-392">App-v 서버는이 패키지를 구분 하는 데 x.x 버전 ID를 사용 하 고 이전에 게시 된 패키지에 대 한 새 업그레이드가 포함 되어 있음을 인식 하 고, 결과적으로 기존 Office 2016 패키지에 대 한 업그레이드로 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-392">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2016 package.</span></span></li>
   > </ul>


2. <span data-ttu-id="b82dc-393">새로 만든 Office 2016 App-v 패키지를 새 업데이트를 적용 하려는 컴퓨터에 전역적으로 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-393">Globally publish the newly created Office 2016 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="b82dc-394">새 패키지에는 이전 Office 2016 App-v 패키지의 계보가 있으므로 업데이트를 사용 하 여 새 패키지를 게시 하면 이전 패키지에 새 변경 내용만 적용 되므로 속도가 빠릅니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-394">Since the new package has the same lineage of the older Office 2016 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3. <span data-ttu-id="b82dc-395">업그레이드는 전역적으로 게시 된 모든 앱-V 패키지와 동일한 방식으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-395">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="b82dc-396">응용 프로그램을 사용 중일 수 있으므로 컴퓨터를 다시 부팅할 때까지 업그레이드가 지연 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-396">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>


### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="b82dc-397">Visio 2016 및 Project 2016을 Office와 함께 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-397">Deploying Visio 2016 and Project 2016 with Office</span></span>

<span data-ttu-id="b82dc-398">다음 표에서는 Visio 2016 및 Project 2016을 Office와 함께 배포 하기 위한 요구 사항 및 옵션에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-398">The following table describes the requirements and options for deploying Visio 2016 and Project 2016 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-399">작업</span><span class="sxs-lookup"><span data-stu-id="b82dc-399">Task</span></span></th>
<th align="left"><span data-ttu-id="b82dc-400">세부 정보</span><span class="sxs-lookup"><span data-stu-id="b82dc-400">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-401">Visio 2016 및 Project 2016을 Office와 함께 패키지 하 고 게시 하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="b82dc-401">How do I package and publish Visio 2016 and Project 2016 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-402">Visio 2016 및 Project 2016을 Office와 동일한 패키지에 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-402">You must include Visio 2016 and Project 2016 in the same package with Office.</span></span></p>
<p><span data-ttu-id="b82dc-403">Office를 배포 하지 않는 경우이 항목에서 설명 하는 패키징, 게시 및 배포 요구 사항에 따라 Visio 및/또는 프로젝트를 포함 하는 패키지를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-403">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow the packaging, publishing, and deployment requirements described in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b82dc-404">Visio 2016 및 Project 2016을 특정 사용자에 게 어떻게 배포할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="b82dc-404">How can I deploy Visio 2016 and Project 2016 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-405">다음 방법 중 하나를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-405">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b82dc-406">원하는 경우</span><span class="sxs-lookup"><span data-stu-id="b82dc-406">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="b82dc-407">... 그런 다음이 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-407">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b82dc-408">두 개의 다른 패키지를 만들어 각각 다른 사용자 그룹에 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-408">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-409">다음 패키지를 만들고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-409">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="b82dc-410">사용자가 Office만 필요로 하는 컴퓨터에는 Office 배포만 포함 된 패키지입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-410">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-411">사용자가 세 가지 응용 프로그램을 모두 필요로 하는 컴퓨터에 Office, Visio, 프로젝트 배포가 포함 된 패키지입니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-411">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b82dc-412">전체 조직에 대해 하나의 패키지만 사용 하려는 경우 또는 컴퓨터를 공유 하는 사용자가 있는 경우:</span><span class="sxs-lookup"><span data-stu-id="b82dc-412">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="b82dc-413">다음 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-413">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="b82dc-414">Office, Visio, 프로젝트를 포함 하는 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-414">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-415">패키지를 모든 사용자에 게 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-415">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="b82dc-416"><a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker </a> 를 사용 하 여 특정 사용자가 Visio 및 Project를 사용 하지 못하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b82dc-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>


## <span data-ttu-id="b82dc-417">추가 리소스</span><span class="sxs-lookup"><span data-stu-id="b82dc-417">Additional resources</span></span>


[<span data-ttu-id="b82dc-418">App-V를 사용하여 Microsoft Office 2013 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-418">Deploying Microsoft Office 2013 by Using App-V</span></span>](deploying-microsoft-office-2013-by-using-app-v.md)

[<span data-ttu-id="b82dc-419">App-V를 사용하여 Microsoft Office 2010 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-419">Deploying Microsoft Office 2010 by Using App-V</span></span>](deploying-microsoft-office-2010-by-using-app-v.md)

[<span data-ttu-id="b82dc-420">간편 실행을 위한 Office 2016 배포 도구</span><span class="sxs-lookup"><span data-stu-id="b82dc-420">Office 2016 Deployment Tool for Click-to-Run</span></span>](https://www.microsoft.com/download/details.aspx?id=49117)

**<span data-ttu-id="b82dc-421">연결 그룹</span><span class="sxs-lookup"><span data-stu-id="b82dc-421">Connection Groups</span></span>**

[<span data-ttu-id="b82dc-422">Microsoft App-V v5에 연결 그룹 배포</span><span class="sxs-lookup"><span data-stu-id="b82dc-422">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="b82dc-423">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="b82dc-423">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="b82dc-424">동적 구성</span><span class="sxs-lookup"><span data-stu-id="b82dc-424">Dynamic Configuration</span></span>**

[<span data-ttu-id="b82dc-425">App-V 5.1 동적 구성 정보</span><span class="sxs-lookup"><span data-stu-id="b82dc-425">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)





