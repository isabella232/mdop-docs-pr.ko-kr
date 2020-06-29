---
title: 아카이브 백업
description: 아카이브 백업
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819208"
---
# <span data-ttu-id="7c2f9-103">아카이브 백업</span><span class="sxs-lookup"><span data-stu-id="7c2f9-103">Back Up the Archive</span></span>


<span data-ttu-id="7c2f9-104">AGPM (고급 그룹 정책 관리)의 보관을 복구 하는 데 도움이 되도록 재해가 발생 한 경우 AGPM 관리자 (모든 권한)가 보관을 자주 백업 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="7c2f9-105">기본적으로 보관 파일 은%ProgramData%\\Microsoft\\AGPM.에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="7c2f9-106">그러나 Microsoft 고급 그룹 정책 관리-서버를 설정 하는 동안 다른 경로를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="7c2f9-107">이 절차를 완료 하려면 agpm 서비스를 설치 하는 컴퓨터를 비롯 하 여 사용자 계정에 대 한 액세스 권한이 있고 보관 파일이 들어 있는 폴더를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="7c2f9-108">보관 저장소를 백업 하려면</span><span class="sxs-lookup"><span data-stu-id="7c2f9-108">To back up the archive</span></span>**

1.  <span data-ttu-id="7c2f9-109">AGPM 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-109">Stop the AGPM Service.</span></span> <span data-ttu-id="7c2f9-110">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="7c2f9-111">Windows 탐색기, Xcopy, Windows Server® 백업 또는 다른 백업 도구를 사용 하 여 보관 폴더를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="7c2f9-112">숨겨진, 시스템, 읽기 전용 파일을 백업 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="7c2f9-113">보관 백업을 안전한 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="7c2f9-114">AGPM 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-114">Restart the AGPM Service.</span></span> <span data-ttu-id="7c2f9-115">자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

<span data-ttu-id="7c2f9-116">**참고**  AGPM 관리자가 보관 저장소를 자주 백업 하지 않으면 보관 백업에 있는 Gpo (그룹 정책 개체)가 최신 상태가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="7c2f9-117">보관 백업이 최신 상태 인지 확인 하려면 조직의 일일 백업 전략의 일부로 아카이브를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2f9-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="7c2f9-118">추가 참조</span><span class="sxs-lookup"><span data-stu-id="7c2f9-118">Additional references</span></span>

-   [<span data-ttu-id="7c2f9-119">백업에서 아카이브 복원</span><span class="sxs-lookup"><span data-stu-id="7c2f9-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup.md)

-   [<span data-ttu-id="7c2f9-120">AGPM 서버 및 아카이브 이동</span><span class="sxs-lookup"><span data-stu-id="7c2f9-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="7c2f9-121">아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="7c2f9-121">Managing the Archive</span></span>](managing-the-archive.md)

 

 





