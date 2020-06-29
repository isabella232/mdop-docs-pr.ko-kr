---
title: AGPM 서비스 수정
description: AGPM 서비스 수정
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820503"
---
# <span data-ttu-id="c55e0-103">AGPM 서비스 수정</span><span class="sxs-lookup"><span data-stu-id="c55e0-103">Modify the AGPM Service</span></span>


<span data-ttu-id="c55e0-104">AGPM 서비스는 보관 및 프로덕션 환경의 Gpo (그룹 정책 개체)에 대 한 클라이언트 액세스를 관리 하는 보안 프록시 역할을 하는 Windows 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="c55e0-105">이 서비스를 중지 하거나 사용 하지 않도록 설정 하면 AGPM 클라이언트가 서버를 통해 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="c55e0-106">보관 경로, AGPM 서비스 계정 및 AGPM 서비스가 수신 대기 하는 포트를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="c55e0-107">**주의**  사항 운영 체제의 **관리 도구** 및 **서비스** 를 통해 AGPM 서비스에 대 한 설정을 수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c55e0-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="c55e0-108">이렇게 하면 AGPM 서비스를 시작 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="c55e0-109">이 절차를 완료 하려면 Domain Admins 그룹의 구성원이 며 AGPM 서버 (Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터)에 대 한 액세스 권한이 있는 사용자 계정 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="c55e0-110">또한이 절차를 완료 하려면 AGPM 서비스 계정에 대 한 자격 증명을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="c55e0-111">AGPM 서비스를 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="c55e0-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="c55e0-112">Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터에서 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed:</span></span>

    -   <span data-ttu-id="c55e0-113">WindowsServer2008의 경우 **시작**, **제어판**, **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-113">For WindowsServer2008, click **Start**, **Control Panel**, and **Programs and Features**.</span></span>

    -   <span data-ttu-id="c55e0-114">WindowsVista의 경우 **시작**, **제어판**, **프로그램**, **프로그램 및 기능**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-114">For WindowsVista, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="c55e0-115">**Microsoft 고급 그룹 정책 관리-서버**를 마우스 오른쪽 단추로 클릭 한 다음 **변경을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-115">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="c55e0-116">**다음**을 클릭 한 다음 **수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="c55e0-117">지침에 따라 AGPM 서비스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-117">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="c55e0-118">**보관 경로** 대화 상자에서 AGPM 서버와 관련 된 아카이브의 새 위치를 입력 하거나 현재 보관 경로를 확인 한 후 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-118">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="c55e0-119">**중요**  보관 경로는 AGPM 서버 또는 다른 위치에 있는 폴더를 가리킬 수 있지만,이 위치에는이 AGPM 서버에서 관리 하는 모든 Gpo 및 기록 데이터를 저장할 충분 한 공간이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-119">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="c55e0-120">Agpm 서비스 **계정** 대화 상자에서 agpm 서비스가 실행 될 서비스 계정에 대 한 자격 증명을 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-120">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="c55e0-121">**중요**  설치를 수정 하면 AGPM 서비스 계정에 대 한 자격 증명이 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-121">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="c55e0-122">자격 증명을 다시 입력 해야 하지만, 원본 설치 중 사용 되는 자격 증명과 일치 하는 경우에는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-122">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="c55e0-123">AGPM 서비스 계정에는 관리할 Gpo에 대 한 모든 권한이 있어야 하며 **서비스 권한으로 로그온** 이 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-123">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="c55e0-124">단일 도메인에서 Gpo를 관리 하는 경우 기본 도메인 컨트롤러에 대 한 로컬 시스템 계정을 AGPM 서비스 계정으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-124">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="c55e0-125">여러 도메인의 Gpo를 관리 하는 경우 또는 구성원 서버가 AGPM 서버인 경우 한 도메인 컨트롤러의 로컬 시스템 계정이 다른 도메인의 Gpo에 액세스할 수 없으므로 AGPM 서비스 계정으로 다른 계정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-125">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="c55e0-126">**보관 소유자** 대화 상자에서 agpm 관리자 (모든 권한) 또는 agpm 관리자 그룹의 사용자 이름을 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-126">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="c55e0-127">**참고**  설치를 수정 하면 보관 소유자의 자격 증명이 지워집니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-127">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="c55e0-128">자격 증명을 다시 입력 해야 하지만, 원본 설치 중 사용 되는 자격 증명과 일치 하는 경우에는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-128">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="c55e0-129">**포트 구성** 대화 상자에서 AGPM 서비스가 수신 대기 하거나 현재 선택 된 포트를 확인 해야 하는 새 포트를 입력 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-129">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="c55e0-130">**참고**  기본적으로 AGPM 서비스는 포트 4600에서 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-130">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="c55e0-131">수동으로 포트 예외를 구성 하거나 포트 예외를 구성 하는 규칙이 있는 경우 **방화벽에 포트 예외 추가** 확인란의 선택을 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-131">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="c55e0-132">**변경을**클릭 하 고 설치가 완료 되 면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-132">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="c55e0-133">AGPM 서비스가 수신 대기 하는 포트를 변경한 경우 각 그룹 정책 관리자에 대 한 AGPM 서버 연결의 포트를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-133">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="c55e0-134">(자세한 내용은 [AGPM 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.)</span><span class="sxs-lookup"><span data-stu-id="c55e0-134">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).)</span></span>

7.  <span data-ttu-id="c55e0-135">구성 변경 내용을 적용할 각 AGPM 서버에 대해이 작업을 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="c55e0-135">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="c55e0-136">추가 참조</span><span class="sxs-lookup"><span data-stu-id="c55e0-136">Additional references</span></span>

-   [<span data-ttu-id="c55e0-137">AGPM 서비스 관리</span><span class="sxs-lookup"><span data-stu-id="c55e0-137">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





