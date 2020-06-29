---
title: AGPM 서버 및 아카이브 이동
description: AGPM 서버 및 아카이브 이동
author: dansimp
ms.assetid: 13cb83c4-bb42-4e81-8660-5b7540f473d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6ae5ba9c2346caf81f5aff9f57f6b9dc97127ad1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822518"
---
# <span data-ttu-id="b0240-103">AGPM 서버 및 아카이브 이동</span><span class="sxs-lookup"><span data-stu-id="b0240-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="b0240-104">AGPM 서버와 보관 파일이 호스팅되는 서버를 바꾸는 경우 AGPM 서비스 및 보관 파일을 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="b0240-105">원하는 경우, AGPM 서비스와 보관 파일을 개별적으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="b0240-106">참고</span><span class="sxs-lookup"><span data-stu-id="b0240-106">Note</span></span>**  
-   <span data-ttu-id="b0240-107">AGPM 서버는 AGPM 서비스와 Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터를 호스트 하는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="b0240-108">기본적으로 보관 파일은 AGPM 서버에서 호스팅되므로 보관 경로를 지정 하 여 대신 다른 서버에서 호스팅할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="b0240-109">이 절차를 완료 하려면 Domain Admins 그룹의 구성원이 며 이전 및 새 AGPM 서버에 대 한 액세스 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="b0240-110">또한이 절차를 완료 하려면 새 AGPM 서버에서 사용할 AGPM 서비스 계정에 대 한 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="b0240-111">AGPM 서비스 및 보관 파일을 다른 서버로 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="b0240-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="b0240-112">아카이브를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-112">Back up the archive.</span></span> <span data-ttu-id="b0240-113">자세한 내용은 [보관 파일 백업을](back-up-the-archive.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0240-113">For more information, see [Back Up the Archive](back-up-the-archive.md).</span></span>

2.  <span data-ttu-id="b0240-114">AGPM 서비스 이동:</span><span class="sxs-lookup"><span data-stu-id="b0240-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="b0240-115">AGPM 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-115">Stop the AGPM Service.</span></span> <span data-ttu-id="b0240-116">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0240-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

    2.  <span data-ttu-id="b0240-117">AGPM 서비스를 호스팅할 새 서버에 Microsoft 고급 그룹 정책 관리-서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="b0240-118">이 프로세스가 진행 되는 동안 AGPM 서버와 관련 하 여 보관 위치에 해당 하는 새 보관 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="b0240-119">자세한 내용은 microsoft 고급 그룹 정책 관리 3.0 ()에 대 한 단계별 가이드 <https://go.microsoft.com/fwlink/?LinkId=132706> 및 Microsoft 고급 그룹 정책 관리 ()에 대 한 계획 가이드를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=141871> .</span><span class="sxs-lookup"><span data-stu-id="b0240-119">For more information, see Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0 (<https://go.microsoft.com/fwlink/?LinkId=132706>) and Planning Guide for Microsoft Advanced Group Policy Management (<https://go.microsoft.com/fwlink/?LinkId=141871>).</span></span>

    3.  <span data-ttu-id="b0240-120">AGPM 관리자 (모든 권한)는 새 AGPM 서버를 사용 하는 모든 그룹 정책 관리자에 대해 AGPM 서버 연결을 구성 하 고, 이전 AGPM 서버에 대 한 연결을 제거 하 고, 각 그룹 정책 관리자가 새 AGPM 서버 연결을 수동으로 구성 하 고 컴퓨터의 AGPM 스냅인에 대 한 이전 AGPM 서버 연결을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="b0240-121">자세한 내용은 [AGPM 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0240-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

        <span data-ttu-id="b0240-122">**참고**  가장 좋은 방법은 이전 AGPM 서버에서 Microsoft 고급 그룹 정책 관리-서버를 제거 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="b0240-123">이렇게 하면 해당 서버에서 AGPM 서비스를 실수로 다시 시작할 수 없으며,이 사용자에 게 AGPM 서버 연결이 남아 있는 경우 혼란이 발생할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="b0240-124">백업에서 보관 파일을 호스트할 새 서버로 보관 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="b0240-125">자세한 내용은 [백업에서 보관 파일 복원을](restore-the-archive-from-a-backup.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0240-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup.md).</span></span>

    <span data-ttu-id="b0240-126">**중요**  지금 AGPM 서비스를 이동 하지 않고 보관을 이동한 경우:</span><span class="sxs-lookup"><span data-stu-id="b0240-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="b0240-127">AGPM 서버와 관련 하 여 아카이브의 새 위치를 가리키도록 보관 경로를 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0240-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="b0240-128">자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0240-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

    2.  <span data-ttu-id="b0240-129">**도메인 위임** 탭에서 암호를 다시 입력 하 고 확인 해야 합니다. 자세한 내용은 [전자 메일 알림 구성을](configure-e-mail-notification-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0240-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm30ops.md).</span></span>

     

### <span data-ttu-id="b0240-130">추가 참조</span><span class="sxs-lookup"><span data-stu-id="b0240-130">Additional references</span></span>

-   [<span data-ttu-id="b0240-131">아카이브 백업</span><span class="sxs-lookup"><span data-stu-id="b0240-131">Back Up the Archive</span></span>](back-up-the-archive.md)

-   [<span data-ttu-id="b0240-132">백업에서 아카이브 복원</span><span class="sxs-lookup"><span data-stu-id="b0240-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup.md)

-   [<span data-ttu-id="b0240-133">AGPM 서버 연결 구성</span><span class="sxs-lookup"><span data-stu-id="b0240-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm30ops.md)

-   [<span data-ttu-id="b0240-134">AGPM 서비스 수정</span><span class="sxs-lookup"><span data-stu-id="b0240-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm30ops.md)

-   <span data-ttu-id="b0240-135">Microsoft 고급 그룹 정책 관리 3.0 ()에 대 한 단계별 가이드 <https://go.microsoft.com/fwlink/?LinkId=132706></span><span class="sxs-lookup"><span data-stu-id="b0240-135">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0 (<https://go.microsoft.com/fwlink/?LinkId=132706>)</span></span>

-   <span data-ttu-id="b0240-136">Microsoft 고급 그룹 정책 관리 () 계획 가이드 <https://go.microsoft.com/fwlink/?LinkId=141871></span><span class="sxs-lookup"><span data-stu-id="b0240-136">Planning Guide for Microsoft Advanced Group Policy Management (<https://go.microsoft.com/fwlink/?LinkId=141871>)</span></span>

-   [<span data-ttu-id="b0240-137">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="b0240-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





