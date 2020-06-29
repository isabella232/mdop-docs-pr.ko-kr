---
title: 개별 GPO에 대한 액세스 권한 위임
description: 개별 GPO에 대한 액세스 권한 위임
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818733"
---
# <span data-ttu-id="fd9da-103">개별 GPO에 대한 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="fd9da-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="fd9da-104">AGPM 관리자 (모든 권한)로, 선택 된 그룹 정책 개체 (GPO)의 관리를 위임 하 여 선택한 그룹과 편집기가 편집할 수 있도록 하 고 검토자가 검토 하 고 승인자가 승인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="fd9da-105">이 절차를 완료 하려면 AGPM 관리자 (모든 권한) 역할이 있는 사용자 계정, GPO를 만든 승인자의 사용자 계정 또는 고급 그룹 정책 관리에서 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="fd9da-106">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="fd9da-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="fd9da-107">제어 된 GPO의 관리를 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="fd9da-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="fd9da-108">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="fd9da-109">세부 정보 창의 **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 한 다음 gpo를 클릭 하 여 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="fd9da-110">**추가** 단추를 클릭 하 고 액세스를 허용할 사용자 또는 그룹을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="fd9da-111">각 사용자 또는 그룹에 대 한 사용 권한을 사용자 지정 하려면 **콘텐츠** 탭에서 **고급** 단추를 클릭 하 고 역할 권한이 허용 또는 거부 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="fd9da-112">자세한 컨트롤은 **사용 권한** 대화 상자에서 **고급** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="fd9da-113">**적용**을 클릭 한 다음 **사용 권한** 대화 상자에서 **확인** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="fd9da-114">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="fd9da-114">Additional considerations</span></span>

-   <span data-ttu-id="fd9da-115">기본적으로이 절차를 수행 하려면 GPO 또는 AGPM 관리자 (모든 권한)를 만들거나 제어 하는 승인자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="fd9da-116">특히 해당 도메인에 대 한 **콘텐츠 목록** 사용 권한과 GPO에 대 한 **보안 권한을 수정** 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="fd9da-117">AGPM을 사용 하는 그룹 정책 관리자에 게 읽기 권한을 위임 하려면 **설정 읽기** 권한과 함께 **목록 콘텐츠** 를 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="fd9da-118">이렇게 하면 AGPM의 **콘텐츠** 탭에서 gpo를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="fd9da-119">**이 개체 및 중첩 된 개체**에 적용할 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="fd9da-120">다른 사용 권한은 명시적으로 위임 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="fd9da-121">그룹 정책 소프트웨어 설치를 완전히 사용 하려면 편집자에 게 GPO의 배포 된 복사본에 대 한 **읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="fd9da-122">Gpo에 대 한 액세스의 AGPM 관리를 우회 하는 데 사용 되지 않도록 그룹 정책 작성자 겸 소유자 그룹의 구성원을 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd9da-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="fd9da-123">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="fd9da-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="fd9da-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="fd9da-124">Additional references</span></span>

-   [<span data-ttu-id="fd9da-125">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fd9da-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





