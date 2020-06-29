---
title: 고급 그룹 정책 관리 문제 해결
description: 고급 그룹 정책 관리 문제 해결
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818253"
---
# <span data-ttu-id="6e47c-103">고급 그룹 정책 관리 문제 해결</span><span class="sxs-lookup"><span data-stu-id="6e47c-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="6e47c-104">이 섹션에는 AGPM (고급 그룹 정책 관리)를 사용 하 여 Gpo (그룹 정책 개체)를 관리할 때 발생할 수 있는 몇 가지 일반적인 문제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-104">This section lists a few common issues you may encounter when using Advanced Group Policy Management (AGPM) to manage Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="6e47c-105">어떤 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="6e47c-105">What problems are you having?</span></span>


-   [<span data-ttu-id="6e47c-106">보관 파일에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-106">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="6e47c-107">GPO 상태는 그룹 정책 관리자에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-107">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="6e47c-108">AGPM 서버 연결을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-108">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="6e47c-109">기본 서식 파일을 변경 하거나, Gpo를 보거나, 만들거나, 편집 하거나, 이름을 바꾸거나, 배포 하거나, 삭제할 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="6e47c-109">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="6e47c-110">특정 GPO 이름을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-110">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="6e47c-111">AGPM 전자 메일 알림을 받지 못하는 경우</span><span class="sxs-lookup"><span data-stu-id="6e47c-111">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="6e47c-112">AGPM 서비스에 대해 포트 4600을 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="6e47c-112">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="6e47c-113">AGPM 서비스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-113">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="6e47c-114">그룹 정책 소프트웨어 설치가 소프트웨어 설치에 실패 함</span><span class="sxs-lookup"><span data-stu-id="6e47c-114">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="6e47c-115">보관 파일에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-115">I am unable to access an archive</span></span>

-   <span data-ttu-id="6e47c-116">**원인**: 올바른 서버와 아카이브의 포트를 선택 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-116">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="6e47c-117">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-117">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-118">AGPM 관리자 인 경우: [Agpm 서버 연결 구성을](configure-the-agpm-server-connection.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-118">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="6e47c-119">AGPM 관리자가 아닌 경우: AGPM 관리자가 AGPM 서버에 대 한 연결 세부 정보를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-119">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="6e47c-120">[AGPM 서버 연결 구성을](configure-the-agpm-server-connection-reviewer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-120">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

-   <span data-ttu-id="6e47c-121">**원인**: 고급 그룹 정책 관리 서비스가 실행 되 고 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-121">**Cause**: The Advanced Group Policy Management Service is not running.</span></span>

-   <span data-ttu-id="6e47c-122">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-122">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-123">AGPM 관리자 인 경우 다음을 수행 합니다. AGPM 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-123">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="6e47c-124">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-124">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).</span></span>

    -   <span data-ttu-id="6e47c-125">AGPM 관리자가 아닌 경우: AGPM 관리자에 게 도움을 요청 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-125">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="6e47c-126">GPO 상태는 그룹 정책 관리자에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-126">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="6e47c-127">**원인**: 다른 그룹 정책 관리자가 동일한 보관에 대해 다른 AGPM 서버를 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-127">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="6e47c-128">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-128">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-129">AGPM 관리자 인 경우: [Agpm 서버 연결 구성을](configure-the-agpm-server-connection.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-129">If you are an AGPM Administrator: See [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="6e47c-130">AGPM 관리자가 아닌 경우: AGPM 관리자가 AGPM 서버에 대 한 연결 세부 정보를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-130">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="6e47c-131">[AGPM 서버 연결 구성을](configure-the-agpm-server-connection-reviewer.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-131">See [Configure the AGPM Server Connection](configure-the-agpm-server-connection-reviewer.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="6e47c-132">AGPM 서버 연결을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-132">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="6e47c-133">**원인**: **agpm 서버** 탭의 설정을 사용할 수 없는 경우 agpm 서버가 관리 템플릿을 사용 하 여 중앙에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-133">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="6e47c-134">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-134">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-135">AGPM 관리자 인 경우: **Agpm 서버** 탭의 설정을 사용할 수 없는 경우 [Agpm 서버 연결 구성을](configure-the-agpm-server-connection.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-135">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).</span></span>

    -   <span data-ttu-id="6e47c-136">AGPM 관리자가 아닌 경우: **Agpm 서버** 탭의 설정을 사용할 수 없는 경우 agpm 서버를 수정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-136">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="6e47c-137">기본 서식 파일을 변경 하거나, Gpo를 보거나, 만들거나, 편집 하거나, 이름을 바꾸거나, 배포 하거나, 삭제할 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="6e47c-137">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="6e47c-138">**원인**: 작업을 수행 하는 데 필요한 권한 역할을 지정 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-138">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="6e47c-139">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-139">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-140">AGPM 관리자 인 경우: [도메인 수준 액세스 위임](delegate-domain-level-access.md) 및 [개별 GPO에 대 한 액세스 권한](delegate-access-to-an-individual-gpo.md)위임을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-140">If you are an AGPM Administrator: See [Delegate Domain-Level Access](delegate-domain-level-access.md) and [Delegate Access to an Individual GPO](delegate-access-to-an-individual-gpo.md).</span></span> <span data-ttu-id="6e47c-141">AGPM 권한은 도메인에서 현재 보관에 있는 모든 Gpo로 종속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-141">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="6e47c-142">새 그룹 정책 관리자가 도메인 수준에 추가 되 면 해당 사용 권한을 **이 개체 및 중첩 된 개체**에 적용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-142">As new Group Policy administrators are added at the domain level, their permissions must be set to apply to **This object and nested objects**.</span></span> <span data-ttu-id="6e47c-143">작업을 수행할 수 있는 역할과 작업을 수행 하는 데 필요한 사용 권한에 대 한 자세한 내용은 해당 작업의 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-143">For details about which roles can perform a task and what permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="6e47c-144">AGPM 관리자가 아닌 경우 추가 역할 또는 권한이 필요한 경우 AGPM 관리자에 게 도움을 요청 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-144">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="6e47c-145">편집자 인 경우 GPO를 만들거나, GPO를 배포 하거나, 프로덕션 환경에서 GPO를 삭제 하는 프로세스를 시작할 수 있지만 승인자 또는 AGPM 관리자가 요청을 승인 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-145">Note that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="6e47c-146">특정 GPO 이름을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-146">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="6e47c-147">**원인**: gpo 이름이 이미 사용 중이거나 gpo를 나열할 수 있는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-147">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="6e47c-148">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-148">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-149">GPO 이름이 **제어**됨, **제어**되지 않음 또는 **보류 중** 탭에 표시 되는 경우 다른 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-149">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="6e47c-150">배포 된 GPO의 이름은 바뀌었지만 아직 배포 되지 않은 경우 프로덕션 환경의 이전 이름 아래에 표시 되므로 이전 이름은 여전히 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-150">If a GPO that has been deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment—therefore, the old name is still in use.</span></span> <span data-ttu-id="6e47c-151">GPO를 다시 배포 하 여 프로덕션 환경에서 해당 이름을 업데이트 하 고 다른 GPO에서 사용할 수 있도록 해당 이름을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-151">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="6e47c-152">**제어** **, 제어**되지 않음 또는 **보류 중** 탭에 gpo 이름이 표시 되지 않으면 gpo를 나열할 권한이 부족할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-152">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="6e47c-153">권한을 요청 하려면 AGPM 관리자에 게 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-153">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="6e47c-154">AGPM 전자 메일 알림을 받지 못하는 경우</span><span class="sxs-lookup"><span data-stu-id="6e47c-154">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="6e47c-155">**원인**: 올바른 SMTP 전자 메일 서버 및 전자 메일 주소가 제공 되지 않았거나 전자 메일 알림을 생성 하는 작업이 수행 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-155">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="6e47c-156">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="6e47c-156">**Solution**:</span></span>

    -   <span data-ttu-id="6e47c-157">AGPM 관리자 인 경우: agpm에서 보낼 보류 중인 작업에 대 한 전자 메일 알림을 보려면 AGPM 관리자가 **도메인 위임** 탭에서 승인자를 위한 올바른 SMTP 전자 메일 서버와 전자 메일 주소를 제공 해야 합니다. 자세한 내용은 [전자 메일 알림 구성을](configure-e-mail-notification.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-157">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification.md).</span></span>

    -   <span data-ttu-id="6e47c-158">전자 메일 알림은 해당 GPO를 만들거나, 배포 하거나, 삭제 하는 데 필요한 권한이 없는 편집기, 검토자 또는 다른 그룹 정책 관리자가 이러한 작업 중 하나에 대 한 요청을 제출 하는 경우에만 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-158">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="6e47c-159">요청 승인 또는 거부에 대 한 자동 알림은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-159">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="6e47c-160">AGPM 서비스에 대해 포트 4600을 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="6e47c-160">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="6e47c-161">**원인**: AGPM 서비스가 수신 대기 하는 포트는 기본적으로 포트 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-161">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="6e47c-162">**해결 방법**: AGPM 서비스에 대해 포트 4600을 사용할 수 없는 경우 각 보관 인덱스 파일을 수정 하 여 다른 포트를 사용 하 고 모든 그룹 정책 관리자 용 AGPM 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-162">**Solution**: If port 4600 is not available for the AGPM Service, modify each archive index file to use another port and then update the AGPM Server for all Group Policy administrators.</span></span> <span data-ttu-id="6e47c-163">자세한 내용은 [AGPM 서비스에서 수신 대기 하는 포트 수정을](modify-the-port-on-which-the-agpm-service-listens.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-163">For more information, see [Modify the Port on Which the AGPM Service Listens](modify-the-port-on-which-the-agpm-service-listens.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="6e47c-164">AGPM 서비스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-164">The AGPM Service will not start</span></span>

-   <span data-ttu-id="6e47c-165">**원인**: 운영 체제의 **관리 도구** 및 **서비스**에서 AGPM 서비스에 대 한 설정을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-165">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="6e47c-166">**해결**방법: **프로그램 추가/제거**에서 **Microsoft 고급 그룹 정책 관리 서버** 에 대 한 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-166">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Add or Remove Programs**.</span></span> <span data-ttu-id="6e47c-167">자세한 내용은 [AGPM 서비스 계정 수정을](modify-the-agpm-service-account.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e47c-167">For more information, see [Modify the AGPM Service Account](modify-the-agpm-service-account.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="6e47c-168">그룹 정책 소프트웨어 설치가 소프트웨어 설치에 실패 함</span><span class="sxs-lookup"><span data-stu-id="6e47c-168">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="6e47c-169">**원인**: AGPM은 그룹 정책 소프트웨어 설치 패키지의 무결성을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-169">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="6e47c-170">Gpo는 오프 라인으로 편집 되지만 패키지와 캐시 된 클라이언트 정보 간의 링크는 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-170">Although GPOs are edited offline, links between packages as well as cached client information are preserved.</span></span> <span data-ttu-id="6e47c-171">이것은 의도적입니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-171">This is by design.</span></span>

-   <span data-ttu-id="6e47c-172">**해결 방법**: AGPM을 사용 하 여 오프 라인으로 GPO를 편집할 때는 체크 아웃 된 복사본이 아닌 다른 gpo의 패키지에 대 한 그룹 정책 소프트웨어 설치 업그레이드를 구성 하 여 배포 된 gpo를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-172">**Solution**: When editing a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="6e47c-173">편집기에는 배포 된 GPO에 대 한 **읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e47c-173">The Editor must have **Read** permission for the deployed GPO.</span></span>

 

 





