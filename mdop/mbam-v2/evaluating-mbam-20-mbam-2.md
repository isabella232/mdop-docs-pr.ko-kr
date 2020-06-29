---
title: MBAM 2.0 평가
description: MBAM 2.0 평가
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824738"
---
# <span data-ttu-id="79194-103">MBAM 2.0 평가</span><span class="sxs-lookup"><span data-stu-id="79194-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="79194-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 프로덕션 환경에 배포 하기 전에 테스트 환경에서 평가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="79194-105">이 항목의 정보를 사용 하 여 평가 목적 으로만 단일 서버 테스트 환경에서 독립 실행형 토폴로지로 Microsoft BitLocker 관리 및 모니터링을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="79194-106">단일 서버 토폴로지는 프로덕션 환경에는 권장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="79194-107">테스트 환경에서 MBAM을 배포 하는 방법에 대 한 지침은 [단일 서버에서 MBAM을 설치 하 고 구성 하는 방법을](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79194-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="79194-108">테스트 환경 설정</span><span class="sxs-lookup"><span data-stu-id="79194-108">Setting up the Test Environment</span></span>


<span data-ttu-id="79194-109">테스트 환경에서 평가할 MBAM의 비프로덕션 인스턴스를 설정 하는 경우에도 필수 구성 요소와 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 여전히 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="79194-110">설치를 시작 하기 전에 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md), [Mbam 2.0 지원 되는 구성](mbam-20-supported-configurations-mbam-2.md), 그리고 [mbam 2.0에 대 한 환경 준비](preparing-your-environment-for-mbam-20-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79194-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="79194-111">MBAM 평가 배포 계획</span><span class="sxs-lookup"><span data-stu-id="79194-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="79194-112">작업</span><span class="sxs-lookup"><span data-stu-id="79194-112">Task</span></span></th>
<th align="left"><span data-ttu-id="79194-113">참조</span><span class="sxs-lookup"><span data-stu-id="79194-113">References</span></span></th>
<th align="left"><span data-ttu-id="79194-114">참고</span><span class="sxs-lookup"><span data-stu-id="79194-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-115">MBAM에 대 한 시작 정보를 검토 하 여 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 지식을 얻으십시오.</span><span class="sxs-lookup"><span data-stu-id="79194-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="79194-116">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="79194-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-117">MBAM 2.0 배포 필수 구성 요소를 계획 하 고 컴퓨팅 환경을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="79194-118">MBAM 2.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="79194-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-119">MBAM 그룹 정책 요구 사항 계획 및 구성</span><span class="sxs-lookup"><span data-stu-id="79194-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="79194-120">MBAM 2.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="79194-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-121">필요한 ActiveDirectoryDomainServices 보안 그룹을 계획 하 고 만들고 MBAM 로컬 보안 그룹 구성원 요구 사항에 대 한 계획을 수립 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="79194-122">MBAM 2.0 관리자 역할 계획</span><span class="sxs-lookup"><span data-stu-id="79194-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-123">MBAM 서버 기능 배포를 배포 하기 위한 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="79194-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="79194-124">MBAM 2.0 서버 배포 계획</span><span class="sxs-lookup"><span data-stu-id="79194-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-125">MBAM 클라이언트 배포 배포 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="79194-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="79194-126">MBAM 2.0 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="79194-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="79194-127">MBAM 평가 배포 수행</span><span class="sxs-lookup"><span data-stu-id="79194-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="79194-128">MBAM 설치에 대 한 컴퓨팅 환경을 준비 하기 위해 필요한 계획 및 소프트웨어 필수 구성 요소 설치를 완료 한 후 MBAM 평가판 배포를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-129">MBAM 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치를 지원 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="79194-130">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="79194-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-131">평가판을 위해 MBAM 설치를 실행 하 여 단일 서버에 MBAM 서버 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="79194-132">단일 서버에서 MBAM을 설치 및 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="79194-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-133">계획 단계 중에 만든 ActiveDirectoryDomainServices 보안 그룹을 새 MBAM 서버의 적절 한 로컬 MBAM 서버 기능 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="79194-134">MBAM 2.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="79194-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-135">필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="79194-136">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="79194-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="79194-137">MBAM 클라이언트 소프트웨어를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="79194-138">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="79194-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="79194-139">MBAM 평가에 대 한 Lab 컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="79194-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="79194-140">이 섹션에는 MBAM 클라이언트 상태 보고 속도를 향상 하는 데 사용할 수 있는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="79194-141">그러나 이러한 수정은 테스트 목적 으로만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="79194-142">**참고**  다음 섹션의 정보는 Windows 레지스트리를 수정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="79194-143">레지스트리 편집기를 잘못 사용 하면 심각한 문제가 발생할 수 있으며,이 경우 Windows를 다시 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="79194-144">Microsoft는 레지스트리 편집기의 잘못 된 사용으로 인해 발생 하는 문제에 대 한 해결을 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="79194-145">레지스트리 편집기 사용에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="79194-146">MBAM 클라이언트 상태 보고 빈도 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="79194-147">그룹 정책을 사용 하 여 설정 하는 경우 MBAM 클라이언트 웨이크업 및 상태 보고 빈도는 최소 90 분입니다.</span><span class="sxs-lookup"><span data-stu-id="79194-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="79194-148">Windows 레지스트리를 사용 하 여 테스트 속도를 향상 시킬 수 있도록 MBAM 클라이언트 컴퓨터에서 이러한 주파수를 더 낮은 값으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="79194-149">MBAM 클라이언트 상태 보고 빈도 설정을 수정 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="79194-150">레지스트리 편집기를 사용 하 여 **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="79194-151">**ClientWakeupFrequency** 및 **StatusReportingFrequency** 의 값을 클라이언트에서 지원 되는 최소 값으로 **1** 로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="79194-152">이 변경으로 인해 MBAM 클라이언트가 분 단위로 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79194-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="79194-153">**BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="79194-154">**참고**  낮은 값을 설정 하려면 레지스트리에서 수동으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="79194-155">MBAM 클라이언트 서비스 시작 지연 수정</span><span class="sxs-lookup"><span data-stu-id="79194-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="79194-156">Mbam 클라이언트 웨이크업 및 상태 보고 빈도 외에도 클라이언트 컴퓨터에서 MBAM 클라이언트 에이전트 서비스가 시작 될 때 최대 90 분의 지연이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79194-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="79194-157">임의 지연을 원하지 않으면 **HKLM\\Software\\Microsoft\\MBAM**에서 a 2의 **DWORD** 값을 만들고 해당 **NoStartupDelay** 값을 **1**로 설정한 다음 **BitLocker 관리 클라이언트 서비스**를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="79194-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="79194-158">관련 항목</span><span class="sxs-lookup"><span data-stu-id="79194-158">Related topics</span></span>


[<span data-ttu-id="79194-159">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="79194-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





