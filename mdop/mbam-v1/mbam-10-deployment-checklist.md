---
title: MBAM 1.0 배포 검사 목록
description: MBAM 1.0 배포 검사 목록
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812537"
---
# <span data-ttu-id="0e695-103">MBAM 1.0 배포 검사 목록</span><span class="sxs-lookup"><span data-stu-id="0e695-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="0e695-104">이 검사 목록은 Microsoft BitLocker 관리 및 모니터링 (MBAM) 배포를 용이 하 게 하기 위해 고안 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="0e695-105">참고</span><span class="sxs-lookup"><span data-stu-id="0e695-105">Note</span></span>**  
<span data-ttu-id="0e695-106">이 검사 목록에서는 권장 단계를 개략적으로 설명 하 고, MBAM 기능을 배포할 때 고려해 야 할 항목의 상위 수준 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="0e695-107">이 검사 목록을 스프레드시트 프로그램에 복사 하 여 특정 요구 사항에 맞게 사용자 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="0e695-108">작업</span><span class="sxs-lookup"><span data-stu-id="0e695-108">Task</span></span></th>
<th align="left"><span data-ttu-id="0e695-109">참조</span><span class="sxs-lookup"><span data-stu-id="0e695-109">References</span></span></th>
<th align="left"><span data-ttu-id="0e695-110">참고</span><span class="sxs-lookup"><span data-stu-id="0e695-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0e695-111">이 계획 단계를 완료 하 여 MBAM 배포에 대 한 컴퓨팅 환경을 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="0e695-112">MBAM 1.0 계획 검사 목록</span><span class="sxs-lookup"><span data-stu-id="0e695-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0e695-113">MBAM 지원 구성의 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치를 지원 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="0e695-114">MBAM 1.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="0e695-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0e695-115">MBAM 설치 프로그램을 실행 하 여 다음과 같은 순서로 MBAM 서버 기능을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="0e695-116">복구 및 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="0e695-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="0e695-117">준수 상태 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="0e695-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="0e695-118">준수 감사 및 보고서</span><span class="sxs-lookup"><span data-stu-id="0e695-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="0e695-119">관리 및 모니터링 서버</span><span class="sxs-lookup"><span data-stu-id="0e695-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="0e695-120">MBAM 그룹 정책 서식 파일</span><span class="sxs-lookup"><span data-stu-id="0e695-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="0e695-121">참고</span><span class="sxs-lookup"><span data-stu-id="0e695-121">Note</span></span></strong><br/><p><span data-ttu-id="0e695-122">각 기능이 설치 된 서버의 이름을 추적 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e695-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="0e695-123">이 정보는 설치 프로세스 전체에서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="0e695-124">MBAM 1.0 서버 인프라 배포</span><span class="sxs-lookup"><span data-stu-id="0e695-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0e695-125">계획 단계 중에 만든 Active Directory 도메인 서비스 보안 그룹을 적절 한 서버의 적절 한 로컬 MBAM 서버 기능 관리자 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="0e695-126">MBAM 1.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</span><span class="sxs-lookup"><span data-stu-id="0e695-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0e695-127">필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="0e695-128">MBAM 1.0 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="0e695-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0e695-129">MBAM 클라이언트 소프트웨어를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e695-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="0e695-130">MBAM 1.0 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="0e695-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="0e695-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0e695-131">Related topics</span></span>


[<span data-ttu-id="0e695-132">MBAM 1.0 배포</span><span class="sxs-lookup"><span data-stu-id="0e695-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









