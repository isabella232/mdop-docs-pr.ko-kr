---
title: 고급 그룹 정책 관리 문제 해결
description: 고급 그룹 정책 관리 문제 해결
author: dansimp
ms.assetid: f7ece97c-e9f8-4b18-8c7a-a615c98d5c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4815378a17a7c083501cfd7772e62415ec285237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820178"
---
# <span data-ttu-id="e7334-103">고급 그룹 정책 관리 문제 해결</span><span class="sxs-lookup"><span data-stu-id="e7334-103">Troubleshooting Advanced Group Policy Management</span></span>


<span data-ttu-id="e7334-104">이 섹션에는 AGPM (고급 그룹 정책 관리)를 사용 하 여 Gpo (그룹 정책 개체)를 관리할 때 발생할 수 있는 일반적인 문제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-104">This section lists common issues that you may encounter when you use Advanced Group Policy Management (AGPM) to manage Group Policy Objects (GPOs).</span></span> <span data-ttu-id="e7334-105">여기에 나와 있지 않은 문제를 진단 하려면 AGPM 관리자 (모든 권한)에서 로깅 및 추적을 사용 하는 것이 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-105">To diagnose issues not listed here, it may be helpful for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="e7334-106">자세한 내용은 [로깅 및 추적 구성을](configure-logging-and-tracing-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm30ops.md).</span></span>

**<span data-ttu-id="e7334-107">참고</span><span class="sxs-lookup"><span data-stu-id="e7334-107">Note</span></span>**  
-   <span data-ttu-id="e7334-108">문제가 있는 경우 이전 버전의 GPO로 롤백하는 방법에 대 한 자세한 내용은 [이전 버전의 gpo로 롤백을](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-108">For information about rolling back to an earlier version of a GPO if there are problems, see [Roll Back to a Previous Version of a GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).</span></span>

-   <span data-ttu-id="e7334-109">백업에서 전체 보관 파일을 복원 하 여 재난 으로부터 복구 하는 방법에 대 한 자세한 내용은 [백업에서 보관 파일 복원을](restore-the-archive-from-a-backup.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-109">For information about how to recover from a disaster by restoring the complete archive from a backup, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup.md).</span></span>

 

## <span data-ttu-id="e7334-110">어떤 문제가 있나요?</span><span class="sxs-lookup"><span data-stu-id="e7334-110">What problems are you having?</span></span>


-   [<span data-ttu-id="e7334-111">보관 파일에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-111">I am unable to access an archive</span></span>](#bkmk-access-an-archive)

-   [<span data-ttu-id="e7334-112">GPO 상태는 그룹 정책 관리자에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-112">The GPO state varies for different Group Policy administrators</span></span>](#bkmk-state-varies)

-   [<span data-ttu-id="e7334-113">AGPM 서버 연결을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-113">I am unable to modify the AGPM Server connection</span></span>](#bkmk-modify-archive-location)

-   [<span data-ttu-id="e7334-114">기본 서식 파일을 변경 하거나, Gpo를 보거나, 만들거나, 편집 하거나, 이름을 바꾸거나, 배포 하거나, 삭제할 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="e7334-114">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>](#bkmk-perform-task)

-   [<span data-ttu-id="e7334-115">특정 GPO 이름을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-115">I am unable to use a particular GPO name</span></span>](#bkmk-use-particular-name)

-   [<span data-ttu-id="e7334-116">AGPM 전자 메일 알림을 받지 못하는 경우</span><span class="sxs-lookup"><span data-stu-id="e7334-116">I am not receiving AGPM e-mail notifications</span></span>](#bkmk-email)

-   [<span data-ttu-id="e7334-117">AGPM 서비스에 대해 포트 4600을 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="e7334-117">I cannot use port 4600 for the AGPM Service</span></span>](#bkmk-port)

-   [<span data-ttu-id="e7334-118">AGPM 서비스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-118">The AGPM Service will not start</span></span>](#bkmk-not-start)

-   [<span data-ttu-id="e7334-119">그룹 정책 소프트웨어 설치가 소프트웨어 설치에 실패 함</span><span class="sxs-lookup"><span data-stu-id="e7334-119">Group Policy Software Installation fails to install software</span></span>](#bkmk-software-installation)

-   [<span data-ttu-id="e7334-120">보관 파일을 새 AGPM 서버로 복원 하는 동안 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-120">An error occurred when I restored the archive to a new AGPM Server</span></span>](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a><span data-ttu-id="e7334-121">보관 파일에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-121">I am unable to access an archive</span></span>

-   <span data-ttu-id="e7334-122">**원인**: 올바른 서버와 아카이브의 포트를 선택 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-122">**Cause**: You have not selected the correct server and port for the archive.</span></span>

-   <span data-ttu-id="e7334-123">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-123">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-124">AGPM 관리자 인 경우: [Agpm 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-124">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="e7334-125">AGPM 관리자가 아닌 경우: AGPM 관리자가 AGPM 서버에 대 한 연결 세부 정보를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-125">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="e7334-126">[AGPM 서버 연결 구성을](configure-an-agpm-server-connection-reviewer-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-126">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

-   <span data-ttu-id="e7334-127">**원인**: AGPM 서비스가 실행 되 고 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-127">**Cause**: The AGPM Service is not running.</span></span>

-   <span data-ttu-id="e7334-128">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-128">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-129">AGPM 관리자 인 경우 다음을 수행 합니다. AGPM 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-129">If you are an AGPM Administrator: Start the AGPM Service.</span></span> <span data-ttu-id="e7334-130">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-130">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

    -   <span data-ttu-id="e7334-131">AGPM 관리자가 아닌 경우: AGPM 관리자에 게 도움을 요청 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-131">If you are not an AGPM Administrator: Contact an AGPM Administrator for assistance.</span></span>

### <a href="" id="bkmk-state-varies"></a><span data-ttu-id="e7334-132">GPO 상태는 그룹 정책 관리자에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-132">The GPO state varies for different Group Policy administrators</span></span>

-   <span data-ttu-id="e7334-133">**원인**: 다른 그룹 정책 관리자가 동일한 보관에 대해 다른 AGPM 서버를 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-133">**Cause**: Different Group Policy administrators have selected different AGPM Servers for the same archive.</span></span>

-   <span data-ttu-id="e7334-134">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-134">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-135">AGPM 관리자 인 경우: [Agpm 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-135">If you are an AGPM Administrator: See [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="e7334-136">AGPM 관리자가 아닌 경우: AGPM 관리자가 AGPM 서버에 대 한 연결 세부 정보를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-136">If you are not an AGPM Administrator: Request connection details for the AGPM Server from an AGPM Administrator.</span></span> <span data-ttu-id="e7334-137">[AGPM 서버 연결 구성을](configure-an-agpm-server-connection-reviewer-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-137">See [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

### <a href="" id="bkmk-modify-archive-location"></a><span data-ttu-id="e7334-138">AGPM 서버 연결을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-138">I am unable to modify the AGPM Server connection</span></span>

-   <span data-ttu-id="e7334-139">**원인**: **agpm 서버** 탭의 설정을 사용할 수 없는 경우 agpm 서버가 관리 템플릿을 사용 하 여 중앙에서 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-139">**Cause**: If the settings on the **AGPM Server** tab are unavailable, the AGPM Server has been centrally configured using an Administrative template.</span></span>

-   <span data-ttu-id="e7334-140">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-140">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-141">AGPM 관리자 인 경우: **Agpm 서버** 탭의 설정을 사용할 수 없는 경우 [Agpm 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-141">If you are an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

    -   <span data-ttu-id="e7334-142">AGPM 관리자가 아닌 경우: **Agpm 서버** 탭의 설정을 사용할 수 없는 경우 agpm 서버를 수정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-142">If you are not an AGPM Administrator: If the settings on the **AGPM Server** tab are unavailable, you do not need to modify the AGPM Server.</span></span>

### <a href="" id="bkmk-perform-task"></a><span data-ttu-id="e7334-143">기본 서식 파일을 변경 하거나, Gpo를 보거나, 만들거나, 편집 하거나, 이름을 바꾸거나, 배포 하거나, 삭제할 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="e7334-143">I am unable to change the default template or view, create, edit, rename, deploy, or delete GPOs</span></span>

-   <span data-ttu-id="e7334-144">**원인**: 작업을 수행 하는 데 필요한 권한 역할을 지정 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-144">**Cause**: You have not been assigned a role with the permissions required to perform the task or tasks.</span></span>

-   <span data-ttu-id="e7334-145">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-145">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-146">AGPM 관리자 인 경우: [아카이브에 대 한 도메인 수준 액세스 위임](delegate-domain-level-access-to-the-archive-agpm30ops.md) 및 [보관 저장소의 개별 GPO에 대 한 액세스 권한 위임](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-146">If you are an AGPM Administrator: See [Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm30ops.md) and [Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md).</span></span> <span data-ttu-id="e7334-147">AGPM 권한은 도메인에서 현재 보관에 있는 모든 Gpo로 종속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-147">AGPM permissions will cascade from the domain to all GPOs currently in the archive.</span></span> <span data-ttu-id="e7334-148">작업을 수행할 수 있는 역할과 작업을 수행 하는 데 필요한 사용 권한을 확인 하는 방법에 대 한 자세한 내용은 해당 작업의 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-148">For details about which roles can perform a task and which permissions are necessary to perform a task, refer to the help for that task.</span></span>

    -   <span data-ttu-id="e7334-149">AGPM 관리자가 아닌 경우 추가 역할 또는 권한이 필요한 경우 AGPM 관리자에 게 도움을 요청 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-149">If you are not an AGPM Administrator and you require additional roles or permissions: Contact an AGPM Administrator for assistance.</span></span> <span data-ttu-id="e7334-150">편집자 인 경우 GPO를 만들거나, GPO를 배포 하거나, 프로덕션 환경에서 GPO를 삭제 하는 프로세스를 시작할 수 있지만 승인자 또는 AGPM 관리자가 요청을 승인 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-150">Be aware that if you are an Editor, you can begin the process of creating a GPO, deploying a GPO, or deleting a GPO from the production environment, but an Approver or AGPM Administrator must approve your request.</span></span>

### <a href="" id="bkmk-use-particular-name"></a><span data-ttu-id="e7334-151">특정 GPO 이름을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-151">I am unable to use a particular GPO name</span></span>

-   <span data-ttu-id="e7334-152">**원인**: gpo 이름이 이미 사용 중이거나 gpo를 나열할 수 있는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-152">**Cause**: Either the GPO name is already in use or you lack permission to list the GPO.</span></span>

-   <span data-ttu-id="e7334-153">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-153">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-154">GPO 이름이 **제어**됨, **제어**되지 않음 또는 **보류 중** 탭에 표시 되는 경우 다른 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-154">If the GPO name appears on the **Controlled**, **Uncontrolled**, or **Pending** tab, choose another name.</span></span> <span data-ttu-id="e7334-155">배포 된 GPO의 이름은 바뀌었지만 아직 배포 되지 않은 경우 프로덕션 환경의 이전 이름 아래에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-155">If a GPO that was deployed is renamed but not yet redeployed, it will be displayed under its old name in the production environment.</span></span> <span data-ttu-id="e7334-156">따라서 이전 이름은 여전히 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-156">Therefore, the old name is still being used.</span></span> <span data-ttu-id="e7334-157">GPO를 다시 배포 하 여 프로덕션 환경에서 해당 이름을 업데이트 하 고 다른 GPO에서 사용할 수 있도록 해당 이름을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-157">Redeploy the GPO to update its name in the production environment and release that name for use by another GPO.</span></span>

    -   <span data-ttu-id="e7334-158">**제어** **, 제어**되지 않음 또는 **보류 중** 탭에 gpo 이름이 표시 되지 않으면 gpo를 나열할 권한이 부족할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-158">If the GPO name does not appear on the **Controlled**, **Uncontrolled**, or **Pending** tab, you may lack permission to list the GPO.</span></span> <span data-ttu-id="e7334-159">권한을 요청 하려면 AGPM 관리자에 게 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-159">To request permission, contact an AGPM Administrator.</span></span>

### <a href="" id="bkmk-email"></a><span data-ttu-id="e7334-160">AGPM 전자 메일 알림을 받지 못하는 경우</span><span class="sxs-lookup"><span data-stu-id="e7334-160">I am not receiving AGPM e-mail notifications</span></span>

-   <span data-ttu-id="e7334-161">**원인**: 올바른 SMTP 전자 메일 서버 및 전자 메일 주소가 제공 되지 않았거나 전자 메일 알림을 생성 하는 작업이 수행 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-161">**Cause**: A valid SMTP e-mail server and e-mail address has not been provided, or no action has been taken that generates an e-mail notification.</span></span>

-   <span data-ttu-id="e7334-162">**해결 방법**:</span><span class="sxs-lookup"><span data-stu-id="e7334-162">**Solution**:</span></span>

    -   <span data-ttu-id="e7334-163">AGPM 관리자 인 경우: agpm에서 보낼 보류 중인 작업에 대 한 전자 메일 알림을 보려면 AGPM 관리자가 **도메인 위임** 탭에서 승인자를 위한 올바른 SMTP 전자 메일 서버와 전자 메일 주소를 제공 해야 합니다. 자세한 내용은 [전자 메일 알림 구성을](configure-e-mail-notification-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-163">If you are an AGPM Administrator: For e-mail notifications about pending actions to be sent by AGPM, an AGPM Administrator must provide a valid SMTP e-mail server and e-mail addresses for Approvers on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

    -   <span data-ttu-id="e7334-164">전자 메일 알림은 해당 GPO를 만들거나, 배포 하거나, 삭제 하는 데 필요한 권한이 없는 편집기, 검토자 또는 다른 그룹 정책 관리자가 이러한 작업 중 하나에 대 한 요청을 제출 하는 경우에만 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-164">E-mail notifications are generated only when an Editor, Reviewer, or other Group Policy administrator who lacks the permission necessary to create, deploy, or delete a GPO submits a request for one of those actions to occur.</span></span> <span data-ttu-id="e7334-165">요청 승인 또는 거부에 대 한 자동 알림은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-165">There is no automatic notification of approval or rejection of a request.</span></span>

### <a href="" id="bkmk-port"></a><span data-ttu-id="e7334-166">AGPM 서비스에 대해 포트 4600을 사용할 수 없음</span><span class="sxs-lookup"><span data-stu-id="e7334-166">I cannot use port 4600 for the AGPM Service</span></span>

-   <span data-ttu-id="e7334-167">**원인**: AGPM 서비스가 수신 대기 하는 포트는 기본적으로 포트 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-167">**Cause**: By default, the port on which the AGPM Service listens is port 4600.</span></span>

-   <span data-ttu-id="e7334-168">**해결 방법**: agpm 서비스에 대해 포트 4600을 사용할 수 없는 경우, 다른 포트를 사용 하도록 agpm 서버의 포트 구성을 수정한 다음 agpm 클라이언트에 대 한 agpm 서버 연결의 포트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-168">**Solution**: If port 4600 is not available for the AGPM Service, modify the port configuration on the AGPM Server to use another port and then update the port in the AGPM Server connection for AGPM Clients.</span></span> <span data-ttu-id="e7334-169">자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-169">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

### <a href="" id="bkmk-not-start"></a><span data-ttu-id="e7334-170">AGPM 서비스가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-170">The AGPM Service will not start</span></span>

-   <span data-ttu-id="e7334-171">**원인**: 운영 체제의 **관리 도구** 및 **서비스**에서 AGPM 서비스에 대 한 설정을 수정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-171">**Cause**: You have modified settings for the AGPM Service in the operating system under **Administrative Tools** and **Services**.</span></span>

-   <span data-ttu-id="e7334-172">**해결**방법: 제어판의 **프로그램 및 기능** 에서 **Microsoft 고급 그룹 정책 관리 서버** 에 대 한 설정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-172">**Solution**: Modify the settings for **Microsoft Advanced Group Policy Management - Server** under **Programs and Features** in Control Panel.</span></span> <span data-ttu-id="e7334-173">자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-173">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

### <a href="" id="bkmk-software-installation"></a><span data-ttu-id="e7334-174">그룹 정책 소프트웨어 설치가 소프트웨어 설치에 실패 함</span><span class="sxs-lookup"><span data-stu-id="e7334-174">Group Policy Software Installation fails to install software</span></span>

-   <span data-ttu-id="e7334-175">**원인**: AGPM은 그룹 정책 소프트웨어 설치 패키지의 무결성을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-175">**Cause**: AGPM preserves the integrity of Group Policy Software Installation packages.</span></span> <span data-ttu-id="e7334-176">Gpo가 오프 라인으로 편집 되기는 하지만 캐시 된 클라이언트 정보 외에 패키지 간 링크도 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-176">Although GPOs are edited offline, links between packages in addition to cached client information are preserved.</span></span> <span data-ttu-id="e7334-177">이것은 의도적입니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-177">This is by design.</span></span>

-   <span data-ttu-id="e7334-178">**해결 방법**: AGPM을 사용 하 여 오프 라인으로 GPO를 편집 하는 경우 다른 gpo의 패키지에 대 한 그룹 정책 소프트웨어 설치 업그레이드를 구성 하 여 체크 아웃 된 복사본이 아닌 배포 된 gpo를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-178">**Solution**: When you edit a GPO offline with AGPM, configure any Group Policy Software Installation upgrade of a package in another GPO to reference the deployed GPO, not the checked-out copy.</span></span> <span data-ttu-id="e7334-179">편집기에는 배포 된 GPO에 대 한 **읽기** 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-179">The Editor must have **Read** permission for the deployed GPO.</span></span>

### <a href="" id="bkmk-error-on-restore"></a><span data-ttu-id="e7334-180">보관 파일을 새 AGPM 서버로 복원 하는 동안 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-180">An error occurred when I restored the archive to a new AGPM Server</span></span>

-   <span data-ttu-id="e7334-181">**원인**: 보안 상의 이유로 **도메인 위임** 탭에 입력 한 암호를 보호 하면 보관 파일이 다른 컴퓨터로 이동 하는 경우 암호에 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7334-181">**Cause**: For security reasons, the encryption protecting the password entered on the **Domain Delegation** tab causes the password to fail if the archive is moved to another computer.</span></span>

-   <span data-ttu-id="e7334-182">**해결**방법: **도메인 위임** 탭에서 암호를 다시 입력 하 고 확인 합니다. 자세한 내용은 [전자 메일 알림 구성을](configure-e-mail-notification-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7334-182">**Solution**: Re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

 

 





