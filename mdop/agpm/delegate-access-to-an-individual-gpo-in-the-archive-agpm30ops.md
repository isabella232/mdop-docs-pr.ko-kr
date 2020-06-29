---
title: 아카이브의 개별 GPO에 대한 액세스 권한 위임
description: 아카이브의 개별 GPO에 대한 액세스 권한 위임
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818768"
---
# <span data-ttu-id="2584f-103">아카이브의 개별 GPO에 대한 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="2584f-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="2584f-104">AGPM 관리자 (모든 권한)로, 선택 된 그룹 정책 개체 (GPO)의 관리를 해당 저장소에서 위임 하 여 선택한 그룹과 편집자에 게 편집할 수 있으며, 검토자는이를 검토 하 고 승인자가 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="2584f-105">이 절차를 완료 하려면 AGPM 관리자 (전체 제어) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 AGPM (고급 그룹 정책 관리)에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="2584f-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="2584f-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2584f-107">제어 된 GPO의 관리를 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="2584f-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="2584f-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2584f-109">세부 정보 창의 **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 한 다음 gpo를 클릭 하 여 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="2584f-110">사용자 또는 그룹에 대 한 액세스 권한을 추가 하려면 **추가** 단추를 클릭 하 고 사용자 또는 그룹을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="2584f-111">**그룹 또는 사용자 추가** 대화 상자에서 역할을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="2584f-112">사용자 또는 그룹에 대 한 액세스 권한을 제거 하려면 해당 사용자 또는 그룹을 선택 하 고 **제거** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="2584f-113">**참고**  사용자 또는 그룹이 도메인 전체 액세스를 상속 하는 경우 **제거** 단추를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="2584f-114">**도메인 위임** 탭에서 도메인 전체 액세스를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="2584f-115">사용자 또는 그룹에 게 위임 된 역할 및 사용 권한을 수정 하려면 **고급** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="2584f-116">**사용 권한** 대화 상자에서 사용자 또는 그룹을 선택 하 고 해당 사용자 또는 그룹에 지정할 각 역할에 대 한 확인란을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="2584f-117">**참고**  편집자 및 승인자는 검토자 권한을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="2584f-118">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="2584f-118">Additional considerations</span></span>

-   <span data-ttu-id="2584f-119">기본적으로이 절차를 수행 하려면 GPO 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2584f-120">특히 해당 도메인에 대 한 **콘텐츠 목록** 사용 권한과 GPO에 대 한 **보안 권한을 수정** 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="2584f-121">AGPM을 사용 하는 그룹 정책 관리자에 게 읽기 권한을 위임 하려면 **설정 읽기** 권한과 함께 **목록 콘텐츠** 를 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="2584f-122">이렇게 하면 AGPM의 **콘텐츠** 탭에서 gpo를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="2584f-123">다른 사용 권한은 명시적으로 위임 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="2584f-124">그룹 정책 소프트웨어 설치를 완전히 사용 하려면 편집자에 게 GPO의 배포 된 복사본에 대 한 **읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="2584f-125">그룹 정책 작성자 겸 소유자 그룹의 구성원은 제한 되어야 하며, Gpo에 대 한 액세스를 AGPM에서 관리 하는 데 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2584f-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="2584f-126">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="2584f-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="2584f-127">추가 참조</span><span class="sxs-lookup"><span data-stu-id="2584f-127">Additional references</span></span>

-   [<span data-ttu-id="2584f-128">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="2584f-128">Managing the Archive</span></span>](managing-the-archive.md)

 

 





