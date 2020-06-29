---
title: 아카이브 관리
description: 아카이브 관리
author: dansimp
ms.assetid: b11a3d71-74ea-4dd7-b243-6f2880b7af2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 682d720b4095dbfa6a7cc4d868109f57c4f54641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820558"
---
# <span data-ttu-id="fb38d-103">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="fb38d-103">Managing the Archive</span></span>


<span data-ttu-id="fb38d-104">Agpm (고급 그룹 정책 관리)의 AGPM 관리자 (모든 권한)는 보관 파일에 대 한 액세스를 관리 하 고 보관 저장소에 저장 된 각 GPO (그룹 정책 개체)의 버전 수를 제한 하는 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb38d-104">In Advanced Group Policy Management (AGPM), as an AGPM Administrator (Full Control), you manage access to the archive and have the option to limit the number of versions of each Group Policy Object (GPO) stored in the archive.</span></span> <span data-ttu-id="fb38d-105">도메인 수준 또는 GPO 수준에서 보관 파일의 Gpo에 대 한 액세스 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb38d-105">You can delegate access to GPOs in the archive at the domain level or GPO level.</span></span> <span data-ttu-id="fb38d-106">또한 재해가 발생 하는 경우 복구할 수 있도록 보관 파일을 백업할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb38d-106">Additionally, you can back up the archive so that you may be able to recover it if a disaster occurs.</span></span>

<span data-ttu-id="fb38d-107">AGPM 관리자는 GPO를 파일로 내보내고, 파일을 다른 포리스트에 복사한 다음, GPO를 해당 포리스트의 도메인으로 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb38d-107">As an AGPM Administrator, you can export a GPO to a file, copy the file to another forest, and then import the GPO into a domain in that forest.</span></span> <span data-ttu-id="fb38d-108">편집기와 달리 GPO를 만들 때 새 제어 된 GPO로 바로 정책 설정을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb38d-108">Unlike an Editor, you can import policy settings from a GPO backup directly into a new controlled GPO when you create it.</span></span> <span data-ttu-id="fb38d-109">GPO를 내보내는 방법에 대 한 자세한 내용은 [파일로 Gpo 내보내기를](export-a-gpo-to-a-file.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb38d-109">For information about how to export a GPO, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

-   [<span data-ttu-id="fb38d-110">아카이브에 대한 도메인 수준 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="fb38d-110">Delegate Domain-Level Access to the Archive</span></span>](delegate-domain-level-access-to-the-archive-agpm40.md)

-   [<span data-ttu-id="fb38d-111">아카이브의 개별 GPO에 대한 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="fb38d-111">Delegate Access to an Individual GPO in the Archive</span></span>](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)

-   [<span data-ttu-id="fb38d-112">저장된 GPO 버전 제한</span><span class="sxs-lookup"><span data-stu-id="fb38d-112">Limit the GPO Versions Stored</span></span>](limit-the-gpo-versions-stored-agpm40.md)

-   [<span data-ttu-id="fb38d-113">파일에서 GPO 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb38d-113">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-agpmadmin.md)

-   [<span data-ttu-id="fb38d-114">아카이브 백업</span><span class="sxs-lookup"><span data-stu-id="fb38d-114">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="fb38d-115">백업에서 아카이브 복원</span><span class="sxs-lookup"><span data-stu-id="fb38d-115">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

### <span data-ttu-id="fb38d-116">추가 참조</span><span class="sxs-lookup"><span data-stu-id="fb38d-116">Additional references</span></span>

-   <span data-ttu-id="fb38d-117">프로덕션 환경에서 Gpo에 대 한 액세스를 위임 하는 방법에 대 한 자세한 내용은 [프로덕션 환경에 대 한 대리인 액세스](delegate-access-to-the-production-environment-agpm40.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb38d-117">For information about how to delegate access to GPOs in the production environment, see [Delegate Access to the Production Environment](delegate-access-to-the-production-environment-agpm40.md).</span></span>

-   <span data-ttu-id="fb38d-118">보관 파일을 이동 하는 방법에 대 한 자세한 내용은 [AGPM 서버 및 보관 파일 이동을](move-the-agpm-server-and-the-archive-agpm40.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb38d-118">For information about how to move the archive, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

-   [<span data-ttu-id="fb38d-119">AGPM 관리자 작업 수행</span><span class="sxs-lookup"><span data-stu-id="fb38d-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





