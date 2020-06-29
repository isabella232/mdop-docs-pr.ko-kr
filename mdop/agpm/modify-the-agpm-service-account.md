---
title: AGPM 서비스 계정 수정
description: AGPM 서비스 계정 수정
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820523"
---
# <span data-ttu-id="c8eed-103">AGPM 서비스 계정 수정</span><span class="sxs-lookup"><span data-stu-id="c8eed-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="c8eed-104">AGPM 서비스는 보관 및 프로덕션 환경의 Gpo (그룹 정책 개체)에 대 한 클라이언트 액세스를 관리 하는 보안 프록시 역할을 하는 Windows 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="c8eed-105">이 서비스를 중지 하거나 사용 하지 않도록 설정 하면 AGPM 클라이언트가 서버를 통해 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="c8eed-106">보관 경로 및 AGPM 서비스 계정은 AGPM 서버를 설치 하는 동안 구성 되며, 나중에 AGPM 서버에서 **프로그램 추가/제거** 를 통해 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="c8eed-107">**주의**  사항 운영 체제의 **관리 도구** 및 **서비스** 를 통해 AGPM 서비스에 대 한 설정을 수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c8eed-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="c8eed-108">이렇게 하면 AGPM 서비스를 시작 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="c8eed-109">이 절차를 완료 하려면 Domain Admins 그룹의 구성원이 며 AGPM 서버 (Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터)에 대 한 액세스 권한이 있는 사용자 계정 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="c8eed-110">**중요**  AGPM 서비스 계정에는 관리할 Gpo에 대 한 모든 권한이 있어야 하며 **서비스 권한으로 로그온** 이 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="c8eed-111">단일 도메인에서 Gpo를 관리 하는 경우 기본 도메인 컨트롤러에 대 한 로컬 시스템 계정을 AGPM 서비스 계정으로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="c8eed-112">여러 도메인의 Gpo를 관리 하는 경우 또는 구성원 서버가 AGPM 서버인 경우 한 도메인 컨트롤러의 로컬 시스템 계정이 다른 도메인의 Gpo에 액세스할 수 없으므로 AGPM 서비스 계정으로 다른 계정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="c8eed-113">AGPM 서비스 계정을 수정 하려면</span><span class="sxs-lookup"><span data-stu-id="c8eed-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="c8eed-114">Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터에서 **시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **프로그램 추가/제거**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="c8eed-115">**Microsoft 고급 그룹 정책 관리-서버**를 클릭 한 다음 **변경을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="c8eed-116">**다음**을 클릭 한 다음 **수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="c8eed-117">화면 설명에 따라 AGPM 서비스에 대 한 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="c8eed-118">보관 경로의 위치를 확인 하거나이를 AGPM 서버와 관련 하 여 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="c8eed-119">보관 경로는 AGPM 서버 또는 다른 위치에 있는 폴더를 가리킬 수 있지만,이 위치에는이 AGPM 서버에서 관리 하는 모든 Gpo 및 기록 데이터를 저장할 충분 한 공간이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="c8eed-120">AGPM 서비스 계정에 대 한 새 자격 증명을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="c8eed-121">보관 소유자의 경우 AGPM 관리자의 자격 증명 (모든 권한)을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="c8eed-122">**변경을**클릭 하 고 설치가 완료 되 면 **마침을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8eed-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="c8eed-123">추가 참조</span><span class="sxs-lookup"><span data-stu-id="c8eed-123">Additional references</span></span>

-   [<span data-ttu-id="c8eed-124">AGPM 서비스 관리</span><span class="sxs-lookup"><span data-stu-id="c8eed-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





