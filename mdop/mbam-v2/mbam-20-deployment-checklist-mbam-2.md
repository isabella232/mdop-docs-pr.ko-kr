---
title: MBAM 2.0 배포 검사 목록
description: MBAM 2.0 배포 검사 목록
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826438"
---
# <span data-ttu-id="c3e6c-103">MBAM 2.0 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="c3e6c-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="c3e6c-104">이 검사 목록을 사용 하 여 독립 실행형 토폴로지와 Microsoft BitLocker 관리 및 모니터링 (MBAM) 배포 중에 도움을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="c3e6c-105">참고</span><span class="sxs-lookup"><span data-stu-id="c3e6c-105">Note</span></span>**  
<span data-ttu-id="c3e6c-106">이 검사 목록에서는 Microsoft BitLocker 관리 및 모니터링 기능을 배포할 때 고려해 야 할 항목의 권장 단계 및 상위 수준 목록을 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="c3e6c-107">이 검사 목록을 스프레드시트 프로그램에 복사 하 여 사용을 위해 사용자 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="c3e6c-108">작업</span><span class="sxs-lookup"><span data-stu-id="c3e6c-108">Task</span></span></th>
<th align="left"><span data-ttu-id="c3e6c-109">참조</span><span class="sxs-lookup"><span data-stu-id="c3e6c-109">References</span></span></th>
<th align="left"><span data-ttu-id="c3e6c-110">참고</span><span class="sxs-lookup"><span data-stu-id="c3e6c-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c3e6c-111">이 계획 단계를 완료 하 여 MBAM 배포에 대 한 컴퓨팅 환경을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="c3e6c-112">MBAM 2.0 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="c3e6c-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c3e6c-113">MBAM 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치를 지원 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="c3e6c-114">MBAM 2.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="c3e6c-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c3e6c-115">MBAM 설치 프로그램을 실행 하 여 다음과 같은 순서로 MBAM 서버 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="c3e6c-116">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c3e6c-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="c3e6c-117">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c3e6c-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="c3e6c-118">준수 감사 및 보고서</span><span class="sxs-lookup"><span data-stu-id="c3e6c-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="c3e6c-119">셀프 서비스 서버</span><span class="sxs-lookup"><span data-stu-id="c3e6c-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="c3e6c-120">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="c3e6c-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="c3e6c-121">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="c3e6c-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="c3e6c-122">참고</span><span class="sxs-lookup"><span data-stu-id="c3e6c-122">Note</span></span></strong><br/><p><span data-ttu-id="c3e6c-123">각 기능이 설치 된 서버의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="c3e6c-124">이 정보는 설치 과정에서 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="c3e6c-125">MBAM 2.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="c3e6c-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c3e6c-126">계획 단계 중에 만든 Active Directory 도메인 서비스 보안 그룹을 적절 한 서버의 적절 한 로컬 MBAM 서버 기능 관리자 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="c3e6c-127">MBAM 2.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="c3e6c-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c3e6c-128">필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="c3e6c-129">MBAM 2.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="c3e6c-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="c3e6c-130">MBAM 클라이언트 소프트웨어를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="c3e6c-131">MBAM 2.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="c3e6c-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c3e6c-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c3e6c-132">Related topics</span></span>


[<span data-ttu-id="c3e6c-133">MBAM 2.0 배포</span><span class="sxs-lookup"><span data-stu-id="c3e6c-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









