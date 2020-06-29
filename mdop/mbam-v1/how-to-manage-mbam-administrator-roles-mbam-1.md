---
title: MBAM 관리자 역할을 관리하는 방법
description: MBAM 관리자 역할을 관리하는 방법
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812969"
---
# <span data-ttu-id="f1929-103">MBAM 관리자 역할을 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="f1929-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="f1929-104">모든 서버 기능에 대해 Microsoft BitLocker 관리 및 모니터링 (MBAM) 설치가 완료 된 후에는 관리 사용자에 게 이러한 서버 기능에 대 한 액세스 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="f1929-105">가장 좋은 방법으로, MBAM 서버 기능을 관리 하거나 사용 하는 관리자는 Active Directory 보안 그룹에 할당 한 다음 해당 그룹을 해당 MBAM 관리 로컬 그룹에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="f1929-106">MBAM 관리자 역할 구성원 자격을 관리 하려면</span><span class="sxs-lookup"><span data-stu-id="f1929-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="f1929-107">ActiveDirectoryDomain 서비스의 보안 그룹에 관리 사용자를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="f1929-108">ActiveDirectoryDomain 서비스 보안 그룹을 해당 기능에 대 한 Microsoft BitLocker 관리 및 모니터링 서버의 MBAM 관리 로컬 그룹 역할에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="f1929-109">사용자 역할은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="f1929-110">**Mbam 시스템 관리자** 는 mbam 관리 웹 사이트의 모든 Microsoft BitLocker 관리 및 모니터링 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="f1929-111">**Mbam 하드웨어 사용자** 는 mbam 관리 웹 사이트의 하드웨어 호환성 기능에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="f1929-112">**Mbam 헬프데스크 사용자** 는 mbam 관리 웹 사이트의 TPM 관리 및 드라이브 복구 옵션에 액세스할 수 있지만, 두 옵션 중 하나를 사용 하는 경우 모든 필드를 채워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="f1929-113">**Mbam 보고서 사용자** 는 mbam 관리 웹 사이트의 규정 준수 및 감사 보고서에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="f1929-114">**Mbam Advanced 헬프데스크** 는 mbam 관리 웹 사이트의 TPM 관리 및 드라이브 복구 옵션에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="f1929-115">이러한 사용자는 두 옵션 중 하나를 사용할 때 모든 필드를 입력할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f1929-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="f1929-116">Microsoft BitLocker 관리 및 모니터링에 대 한 역할에 대 한 자세한 내용은 [MBAM 1.0 관리자 역할 계획](planning-for-mbam-10-administrator-roles.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1929-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="f1929-117">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f1929-117">Related topics</span></span>


[<span data-ttu-id="f1929-118">MBAM 1.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="f1929-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





