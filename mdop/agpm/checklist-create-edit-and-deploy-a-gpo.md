---
title: 검사 목록 GPO 만들기, 편집 및 배포
description: 검사 목록 GPO 만들기, 편집 및 배포
author: dansimp
ms.assetid: 614e2d9a-c18b-4f62-99fd-e17a2ac8559d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c79fefaa65c138372ebee00b769ccc5243142e22
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819113"
---
# <span data-ttu-id="3e717-103">검사 목록: GPO 만들기, 편집 및 배포</span><span class="sxs-lookup"><span data-stu-id="3e717-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="3e717-104">여러 사용자가 Gpo (그룹 정책 개체)를 변경 하는 환경에서 AGPM 관리자 (모든 권한)가 편집자, 승인자, 검토자에 게 권한을 그룹 또는 개인으로 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-104">In an environment where multiple people make changes to Group Policy objects (GPOs), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="3e717-105">다음은 편집기 및 승인자에 대 한 일반적인 GPO 개발 프로세스입니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3e717-106">작업</span><span class="sxs-lookup"><span data-stu-id="3e717-106">Task</span></span></th>
<th align="left"><span data-ttu-id="3e717-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="3e717-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e717-108">편집자 새 GPO 만들기를 요청 하거나 승인자가 새 GPO를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)"><span data-ttu-id="3e717-109">새 제어된 GPO 만들기 요청</span><span class="sxs-lookup"><span data-stu-id="3e717-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)"><span data-ttu-id="3e717-110">새 제어된 GPO 만들기</span><span class="sxs-lookup"><span data-stu-id="3e717-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3e717-111">승인자는 편집자에 의해 요청 된 GPO 만들기를 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="3e717-112">보류 중인 작업 승인 또는 거부</span><span class="sxs-lookup"><span data-stu-id="3e717-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e717-113">편집자는 보관 저장소에서 GPO 복사본을 체크 아웃 하므로 아무도 GPO를 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="3e717-114">편집기에서 GPO를 변경한 다음 수정 된 GPO를 보관 함으로 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)"><span data-ttu-id="3e717-115">오프라인에서 GPO 편집</span><span class="sxs-lookup"><span data-stu-id="3e717-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3e717-116">편집자-GPO를 프로덕션 환경에 배포 하도록 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)"><span data-ttu-id="3e717-117">GPO의 배포 요청</span><span class="sxs-lookup"><span data-stu-id="3e717-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3e717-118">검토자 (예: 승인자 또는 편집자)가 GPO를 분석 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)"><span data-ttu-id="3e717-119">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="3e717-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3e717-120">승인자는 GPO를 승인 하 고 프로덕션 환경으로 배포 하거나 GPO를 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e717-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="3e717-121">보류 중인 작업 승인 또는 거부</span><span class="sxs-lookup"><span data-stu-id="3e717-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





