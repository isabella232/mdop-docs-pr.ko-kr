---
title: GPO의 배포 요청
description: GPO의 배포 요청
author: dansimp
ms.assetid: 9aa9af29-4754-4f72-b624-bb3e1087cbe1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a9e5fdbbd352adb6d542932c7180c513cfac8b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820378"
---
# <span data-ttu-id="dd120-103">GPO의 배포 요청</span><span class="sxs-lookup"><span data-stu-id="dd120-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="dd120-104">GPO (그룹 정책 개체)를 수정 하 고 체크 인 한 후에는 프로덕션 환경에 적용 되도록 GPO를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-104">After you have modified and checked in a Group Policy object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="dd120-105">이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집자 역할이 있거나 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="dd120-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd120-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="dd120-107">프로덕션 환경에 GPO 배포를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="dd120-107">To request the deployment of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="dd120-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="dd120-109">세부 정보 창의 **내용** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="dd120-110">배포할 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **배포**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="dd120-111">승인자 또는 AGPM 관리자 이거나 Gpo를 배포 하기 위한 특별 한 권한이 없는 경우 배포 요청을 제출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="dd120-112">요청의 복사본을 받으려면 **참조** 필드에 전자 메일 주소를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="dd120-113">GPO의 **기록** 에 표시할 메모를 입력 한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="dd120-114">**진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="dd120-115">GPO가 **보류** 탭의 gpo 목록에 표시 됩니다. 승인자가 요청을 승인 하면 해당 GPO가 **보류 중** 탭에서 **제어** 탭으로 이동 하 고 배포 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="dd120-116">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="dd120-116">Additional considerations</span></span>

-   <span data-ttu-id="dd120-117">기본적으로이 절차를 수행 하려면 편집기 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="dd120-118">특히 GPO에 대 한 **목록 콘텐츠** 및 **설정 편집** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="dd120-119">승인 되기 전에 요청을 철회 하려면 **보류 중** 탭을 클릭 합니다. GPO를 마우스 오른쪽 단추로 클릭 한 다음 **회수**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="dd120-120">GPO가 **제어** 탭으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd120-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="dd120-121">추가 참조</span><span class="sxs-lookup"><span data-stu-id="dd120-121">Additional references</span></span>

-   [<span data-ttu-id="dd120-122">GPO 편집</span><span class="sxs-lookup"><span data-stu-id="dd120-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





