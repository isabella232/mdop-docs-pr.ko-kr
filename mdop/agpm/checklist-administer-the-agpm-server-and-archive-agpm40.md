---
title: 검사 목록 AGPM 서버 및 보관 파일 관리
description: 검사 목록 AGPM 서버 및 보관 파일 관리
author: dansimp
ms.assetid: d9c60203-90c2-48a7-9318-197e0ec5038b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e464dafa68b9d93c5a1051c986a0efde4702c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819123"
---
# <span data-ttu-id="db613-103">검사 목록: AGPM 서버 및 아카이브 관리</span><span class="sxs-lookup"><span data-stu-id="db613-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="db613-104">AGPM (고급 그룹 정책 관리)에서 agpm 서비스와 보관이 모두 AGPM 관리자 (모든 권한)에 의해 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db613-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="db613-105">다음은 AGPM 관리자의 일반적인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="db613-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db613-106">자주 수행 하는 작업</span><span class="sxs-lookup"><span data-stu-id="db613-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="db613-107">참고자료</span><span class="sxs-lookup"><span data-stu-id="db613-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db613-108">보관 저장소의 Gpo (그룹 정책 개체)에 대 한 액세스를 위임 합니다.</span><span class="sxs-lookup"><span data-stu-id="db613-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm40.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md)"><span data-ttu-id="db613-109">아카이브에 대한 도메인 수준 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="db613-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)"><span data-ttu-id="db613-110">아카이브의 개별 GPO에 대한 액세스 권한 위임</span><span class="sxs-lookup"><span data-stu-id="db613-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db613-111">보관 저장소를 백업 하 여 재해 복구를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db613-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive-agpm40.md" data-raw-source="[Back Up the Archive](back-up-the-archive-agpm40.md)"><span data-ttu-id="db613-112">아카이브 백업</span><span class="sxs-lookup"><span data-stu-id="db613-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db613-113">드문 작업</span><span class="sxs-lookup"><span data-stu-id="db613-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="db613-114">참고자료</span><span class="sxs-lookup"><span data-stu-id="db613-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db613-115">재해 복구를 위해 백업에서 보관 파일을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db613-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup-agpm40.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md)"><span data-ttu-id="db613-116">백업에서 아카이브 복원</span><span class="sxs-lookup"><span data-stu-id="db613-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db613-117">AGPM 서비스, 보관 파일 또는 둘 다를 다른 서버로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="db613-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive-agpm40.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md)"><span data-ttu-id="db613-118">AGPM 서버 및 아카이브 이동</span><span class="sxs-lookup"><span data-stu-id="db613-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db613-119">보관 경로, AGPM 서비스 계정 또는 AGPM 서비스가 수신 대기 하는 포트를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="db613-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm40.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm40.md)"><span data-ttu-id="db613-120">AGPM 서비스 수정</span><span class="sxs-lookup"><span data-stu-id="db613-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db613-121">AGPM 서버의 일반적인 문제를 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="db613-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-agpm-agpm40.md" data-raw-source="[Troubleshooting AGPM](troubleshooting-agpm-agpm40.md)"><span data-ttu-id="db613-122">AGPM 문제 해결</span><span class="sxs-lookup"><span data-stu-id="db613-122">Troubleshooting AGPM</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm40.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md)"><span data-ttu-id="db613-123">로깅 및 추적 구성</span><span class="sxs-lookup"><span data-stu-id="db613-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="db613-124">추가 참조</span><span class="sxs-lookup"><span data-stu-id="db613-124">Additional references</span></span>

-   [<span data-ttu-id="db613-125">고급 그룹 정책 관리 4.0</span><span class="sxs-lookup"><span data-stu-id="db613-125">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





