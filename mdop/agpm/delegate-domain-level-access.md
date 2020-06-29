---
title: 도메인 수준 액세스 권한 위임
description: 도메인 수준 액세스 권한 위임
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820998"
---
# <span data-ttu-id="fc2d6-103">도메인 수준 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="fc2d6-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="fc2d6-104">그룹 정책 관리자가 Gpo (그룹 정책 개체)에 대 한 적절 한 액세스 및 제어권을 가질 수 있도록 환경에 대 한 위임을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="fc2d6-105">AGPM (고급 그룹 정책 관리)의 작업을 보다 효율적으로 수행 하기 위해 적용할 수 있는 기본 사용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="fc2d6-106">조직의 요구 사항에 맞는 방식으로 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="fc2d6-107">이 절차를 완료 하려면 AGPM 관리자 (모든 권한) 역할 또는 고급 그룹 정책 관리의 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="fc2d6-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="fc2d6-109">사용자 및 그룹에 게 도메인 전체의 모든 Gpo에 대 한 적절 한 사용 권한이 있도록 액세스 권한을 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="fc2d6-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="fc2d6-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="fc2d6-111">**도메인 위임** 탭을 클릭 한 다음 **고급** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="fc2d6-112">**사용 권한** 대화 상자에서 개인에 게 할당할 각 역할의 확인란을 클릭 한 다음 **고급** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="fc2d6-113">**참고**  편집자 및 승인자는 검토자 권한을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="fc2d6-114">**고급 보안 설정** 대화 상자에서 그룹 정책 관리자를 선택 하 고 **편집**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="fc2d6-115">**적용 대상**에서 **이 개체 및 중첩 된 개체**를 선택 하 고 표준 AGPM 역할을 벗어나는 특정 권한을 구성한 다음 **사용 권한** **항목** 대화 상자에서 **확인** 을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="fc2d6-116">**고급 보안 설정** 대화 상자에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="fc2d6-117">**사용 권한** 대화 상자에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="fc2d6-118">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="fc2d6-118">Additional considerations</span></span>

-   <span data-ttu-id="fc2d6-119">기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="fc2d6-120">특히, 도메인에 대 한 **보안 수정** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="fc2d6-121">AGPM을 사용 하는 그룹 정책 관리자에 게 읽기 권한을 위임 하려면 **설정 읽기** 권한과 함께 **목록 콘텐츠** 를 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="fc2d6-122">이렇게 하면 AGPM의 **콘텐츠** 탭에서 gpo를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="fc2d6-123">**이 개체 및 중첩 된 개체**에 적용할 사용 권한을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="fc2d6-124">다른 사용 권한은 명시적으로 위임 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="fc2d6-125">그룹 정책 소프트웨어 설치를 완전히 사용 하려면 편집자에 게 GPO의 배포 된 복사본에 대 한 **읽기** 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="fc2d6-126">Gpo에 대 한 액세스의 AGPM 관리를 우회 하는 데 사용 되지 않도록 그룹 정책 작성자 겸 소유자 그룹의 구성원을 제한 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2d6-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="fc2d6-127">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="fc2d6-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="fc2d6-128">추가 참조</span><span class="sxs-lookup"><span data-stu-id="fc2d6-128">Additional references</span></span>

-   [<span data-ttu-id="fc2d6-129">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fc2d6-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





