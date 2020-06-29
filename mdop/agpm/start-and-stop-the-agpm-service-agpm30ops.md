---
title: AGPM 서비스 시작 및 중지
description: AGPM 서비스 시작 및 중지
author: dansimp
ms.assetid: b9d26920-c439-4992-9a78-73e4fba8309d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2be1c2386bedd5888c0ed032479bf1237ce8289c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820218"
---
# <span data-ttu-id="bc638-103">AGPM 서비스 시작 및 중지</span><span class="sxs-lookup"><span data-stu-id="bc638-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="bc638-104">AGPM 서비스는 보관 및 프로덕션 환경의 Gpo (그룹 정책 개체)에 대 한 클라이언트 액세스를 관리 하는 보안 프록시 역할을 하는 Windows 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="bc638-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="bc638-105">**중요**  AGPM 서비스를 중지 하거나 사용 하지 않도록 설정 하면 AGPM 클라이언트가 서버를 통해 Gpo 나열 또는 편집과 같은 작업을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc638-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM Clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="bc638-106">이 절차를 완료 하려면 AGPM 서버 (AGPM 서비스가 설치 되어 있는 컴퓨터)에 대 한 액세스 권한이 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc638-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="bc638-107">AGPM 서비스를 시작 하거나 중지 하려면</span><span class="sxs-lookup"><span data-stu-id="bc638-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="bc638-108">Microsoft 고급 그룹 정책 관리-서버 (따라서 AGPM 서비스)가 설치 되어 있는 컴퓨터에서 **시작**, **제어판**, **관리 도구**를 차례로 클릭 한 다음 **서비스**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc638-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="bc638-109">서비스 목록에서 **AGPM 서비스** 를 마우스 오른쪽 단추로 클릭 하 고 **시작**, **다시 시작**또는 **중지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc638-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="bc638-110">**주의**  사항 운영 체제의 **관리 도구** 및 **서비스** 를 통해 AGPM 서비스에 대 한 설정을 수정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="bc638-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="bc638-111">이렇게 하면 AGPM 서비스를 시작 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc638-111">Doing so can prevent the AGPM Service from starting.</span></span>

     

### <span data-ttu-id="bc638-112">추가 참조</span><span class="sxs-lookup"><span data-stu-id="bc638-112">Additional references</span></span>

-   [<span data-ttu-id="bc638-113">AGPM 서비스 관리</span><span class="sxs-lookup"><span data-stu-id="bc638-113">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





