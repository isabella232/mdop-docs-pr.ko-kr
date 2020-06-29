---
title: 백업에서 아카이브 복원
description: 백업에서 아카이브 복원
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818363"
---
# <span data-ttu-id="e256d-103">백업에서 아카이브 복원</span><span class="sxs-lookup"><span data-stu-id="e256d-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="e256d-104">재해가 발생 하 고 AGPM (고급 그룹 정책 관리)에 대 한 보관 파일이 손상 되거나 제거 되는 경우, AGPM 관리자 (모든 권한)가 미리 준비 된 백업 복사본에서 보관 파일을 복원 하 고 보관에 속하지 않은 Gpo (그룹 정책 개체) 또는 프로덕션 환경의 버전이 보관 저장소에 있는 것 보다 더 최신 버전 인지 여부를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="e256d-105">보관 백업을 다른 서버로 복원 하는 방법에 대 한 자세한 내용은 [AGPM 서버 및 보관 파일 이동을](move-the-agpm-server-and-the-archive.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e256d-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md).</span></span>

<span data-ttu-id="e256d-106">이 절차를 완료 하려면 AGPM 서버 (AGPM 서비스가 설치 되어 있는 컴퓨터)와 보관 파일이 포함 된 폴더에 액세스할 수 있는 사용자 계정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="e256d-107">백업에서 보관 파일을 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="e256d-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="e256d-108">AGPM 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-108">Stop the AGPM Service.</span></span> <span data-ttu-id="e256d-109">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e256d-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="e256d-110">기존 아카이브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-110">Remove the existing archive.</span></span> <span data-ttu-id="e256d-111">기본적으로 보관 폴더 는%ProgramData%\\Microsoft\\AGPM, Microsoft 고급 그룹 정책 관리를 설치한 AGPM 관리자가 설치 중에 다른 위치를 입력 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="e256d-112">보관 경로, AGPM 서비스 계정, 보관 소유자, 수신 대기 포트를 구성 하 여 보관 폴더를 다시 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="e256d-113">원래 설치 중에 사용 되는 것과 동일한 값을 사용 하는 것은 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="e256d-114">자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm30ops.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e256d-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

4.  <span data-ttu-id="e256d-115">보관 백업 내용을 보관 폴더에 복사 하 여 하위 폴더와 파일을 복사 하 여 각 하위 폴더와 파일이 보관 폴더의 사용 권한을 상속 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="e256d-116">보관 폴더를 덮어쓰지 않도록 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="e256d-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="e256d-117">보관 백업의 GPO가 프로덕션의 해당 GPO 복사본 보다 최신 인지 확실 하지 않은 경우 차이점 보고서를 생성 하 고 해당 설정을 비교 합니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="e256d-118">자세한 내용은 [gpo, Gpo 버전 또는 템플릿 간의 차이점 확인](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e256d-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).</span></span>

6.  <span data-ttu-id="e256d-119">AGPM 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e256d-119">Restart the AGPM Service.</span></span> <span data-ttu-id="e256d-120">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e256d-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

### <span data-ttu-id="e256d-121">추가 참조</span><span class="sxs-lookup"><span data-stu-id="e256d-121">Additional references</span></span>

-   [<span data-ttu-id="e256d-122">아카이브 백업</span><span class="sxs-lookup"><span data-stu-id="e256d-122">Back Up the Archive</span></span>](back-up-the-archive.md)

-   [<span data-ttu-id="e256d-123">AGPM 서버 및 아카이브 이동</span><span class="sxs-lookup"><span data-stu-id="e256d-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="e256d-124">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="e256d-124">Managing the Archive</span></span>](managing-the-archive.md)

 

 





