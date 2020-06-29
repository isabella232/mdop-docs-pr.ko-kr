---
title: AGPM 서버 탭
description: AGPM 서버 탭
author: dansimp
ms.assetid: fb3b0265-53ed-4bf6-88a4-c409f5f1bed4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 335cad07691f914884583636cef01be8dbaa0266
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819288"
---
# <span data-ttu-id="0e213-103">AGPM 서버 탭</span><span class="sxs-lookup"><span data-stu-id="0e213-103">AGPM Server Tab</span></span>


<span data-ttu-id="0e213-104">**변경 컨트롤** 창의 **agpm server** 탭에서 정규화 된 컴퓨터 이름 및 포트를 입력 하 여 agpm 서버를 선택 하 고 보관 저장소에서 이전 버전의 Gpo (그룹 정책 개체)를 삭제 하 여 agpm 서버의 디스크 공간을 절약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="0e213-105">AGPM 서버 지정</span><span class="sxs-lookup"><span data-stu-id="0e213-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="0e213-106">AGPM 서버를 선택 하면 **콘텐츠** 탭에서 사용자에 게 표시 되는 보관 파일과 **도메인 위임** 설정이 적용 되는 위치를 결정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="0e213-107">AGPM (고급 그룹 정책 관리)의 기본 포트는 포트 4600입니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="0e213-108">AGPM 서버 연결이 관리 템플릿 설정을 사용 하 여 중앙에서 구성 되는 경우이 탭에서 연결을 구성 하기 위한 옵션을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="0e213-109">자세한 내용은 [AGPM 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e213-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

## <span data-ttu-id="0e213-110">이전 GPO 버전 삭제</span><span class="sxs-lookup"><span data-stu-id="0e213-110">Deleting old GPO versions</span></span>


<span data-ttu-id="0e213-111">기본적으로 모든 제어 된 GPO의 모든 버전이 보관 저장소에 보존 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="0e213-112">그러나 각 GPO에 대해 보존 되는 버전 수를 제한 하도록 AGPM 서비스를 구성 하 고 해당 제한이 초과 되는 경우 가장 오래 된 버전을 자동으로 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="0e213-113">**기록** 창의 **고유 버전** 탭에 표시 되는 GPO 버전만이 제한에 따라 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="0e213-114">**참고**  각 GPO에 대해 저장할 고유 버전의 최대 수에는 현재 버전이 포함 되지 않으므로 0을 입력 하면 현재 버전만 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="0e213-115">제한은 999 버전 보다 크지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="0e213-116">GPO 버전이 삭제 되 면 해당 버전의 기록은 GPO의 기록에 남아 있지만 GPO 버전 자체는 보관 저장소에서 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="0e213-117">삭제할 수 없는 것으로 표시 하 여 GPO 버전이 삭제 되는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e213-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="0e213-118">추가 참조</span><span class="sxs-lookup"><span data-stu-id="0e213-118">Additional references</span></span>

-   [<span data-ttu-id="0e213-119">사용자 인터페이스: 고급 그룹 정책 관리</span><span class="sxs-lookup"><span data-stu-id="0e213-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="0e213-120">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="0e213-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="0e213-121">검토자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="0e213-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





