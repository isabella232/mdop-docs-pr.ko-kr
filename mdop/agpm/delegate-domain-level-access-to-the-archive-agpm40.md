---
title: 아카이브에 대한 도메인 수준 액세스 권한 위임
description: 아카이브에 대한 도메인 수준 액세스 권한 위임
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818723"
---
# <span data-ttu-id="c0d1b-103">아카이브에 대한 도메인 수준 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="c0d1b-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="c0d1b-104">그룹 정책 관리자가 보관 저장소의 Gpo (그룹 정책 개체)에 대 한 적절 한 액세스 및 제어권을 가질 수 있도록 환경에 대 한 위임을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="c0d1b-105">작업을 보다 효율적으로 만들기 위해 적용할 수 있는 기본 사용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="c0d1b-106">조직의 요구 사항에 맞는 방식으로 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="c0d1b-107">이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="c0d1b-108">이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c0d1b-109">사용자 및 그룹에 게 도메인 전체의 모든 Gpo에 대 한 적절 한 사용 권한을 부여 하도록 액세스 권한을 위임 하려면</span><span class="sxs-lookup"><span data-stu-id="c0d1b-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="c0d1b-110">**그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c0d1b-111">**도메인 위임** 탭을 클릭 하 고 도메인의 모든 gpo에 대 한 액세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="c0d1b-112">사용자 또는 그룹에 대 한 액세스 권한을 추가 하려면 **추가** 단추를 클릭 하 고 사용자 또는 그룹을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="c0d1b-113">**그룹 또는 사용자 추가** 대화 상자에서 역할을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="c0d1b-114">사용자 또는 그룹에 대 한 액세스 권한을 제거 하려면 해당 사용자 또는 그룹을 선택 하 고 **제거** 단추를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="c0d1b-115">사용자 또는 그룹에 게 위임 된 역할 및 사용 권한을 수정 하려면 **고급** 단추를 클릭 합니다 .를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="c0d1b-116">**사용 권한** 대화 상자에서 사용자 또는 그룹을 선택 하 고 해당 사용자 또는 그룹에 지정할 각 역할에 대 한 확인란을 선택한 다음 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="c0d1b-117">**참고**  편집자 및 승인자는 검토자 권한을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="c0d1b-118">추가 고려 사항</span><span class="sxs-lookup"><span data-stu-id="c0d1b-118">Additional considerations</span></span>

-   <span data-ttu-id="c0d1b-119">기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="c0d1b-120">특히, 도메인에 대 한 **보안 수정** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="c0d1b-121">AGPM을 사용 하는 그룹 정책 관리자에 게 읽기 권한을 위임 하려면 **설정 읽기** 권한과 함께 **목록 콘텐츠** 를 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="c0d1b-122">이렇게 하면 AGPM의 **콘텐츠** 탭에서 gpo를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="c0d1b-123">다른 사용 권한은 명시적으로 위임 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="c0d1b-124">그룹 정책 소프트웨어 설치를 완전히 사용 하려면 편집자에 게 GPO의 배포 된 복사본에 대 한 **읽기** 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="c0d1b-125">그룹 정책 작성자 겸 소유자 그룹의 구성원은 제한 되어야 하며, Gpo에 대 한 액세스를 AGPM에서 관리 하는 데 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="c0d1b-126">( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)</span><span class="sxs-lookup"><span data-stu-id="c0d1b-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="c0d1b-127">추가 참조</span><span class="sxs-lookup"><span data-stu-id="c0d1b-127">Additional references</span></span>

-   [<span data-ttu-id="c0d1b-128">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="c0d1b-128">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





