---
title: MBAM 2.0에 대한 고가용성
description: MBAM 2.0에 대한 고가용성
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824728"
---
# <span data-ttu-id="ee856-103">MBAM 2.0에 대한 고가용성</span><span class="sxs-lookup"><span data-stu-id="ee856-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="ee856-104">이 항목에서는 사용 가능한 Microsoft BitLocker 관리 및 모니터링 (MBAM) 설치에 대 한 기본 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="ee856-105">고가용성 시나리오는이 버전의 MBAM에서 완전 하 게 지원 되지 않으므로 여기에서 설명 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="ee856-106">관련 블로그 및 포럼을 검색 하는 것이 좋습니다. 여기서 사용자는 해당 환경에서 MBAM에 대해 높은 가용성을 성공적으로 구성한 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="ee856-107">MBAM에 대 한 고가용성 시나리오</span><span class="sxs-lookup"><span data-stu-id="ee856-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="ee856-108">Microsoft BitLocker 관리 및 모니터링은 결함을 허용 하도록 설계 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="ee856-109">서버를 사용할 수 없게 되 면 사용자에 게 부정적인 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="ee856-110">예를 들어 MBAM 에이전트를 MBAM 웹 서버에 연결할 수 없는 경우 사용자에 게 작업을 묻는 메시지가 표시 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="ee856-111">MBAM 설치를 계획 하는 경우 다음 항목을 고려 하 여 MBAM 서비스의 사용 가능성에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="ee856-112">드라이브 암호화 및 복구 암호-복구 암호를 escrowed 수 없는 경우 클라이언트 컴퓨터에서 암호화가 시작 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="ee856-113">준수 상태 데이터 업로드 – 준수 상태 보고서 서비스를 호스팅하는 서버를 사용할 수 없는 경우 준수 데이터는 현재 상태로 유지 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="ee856-114">지원 센터 복구 키 액세스-지원 센터에서 MBAM 데이터베이스 정보에 액세스할 수 없는 경우 지원 센터에서 사용자에 게 복구 키를 제공할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="ee856-115">보고서의 사용 가능성 – 규정 준수 및 감사 보고서를 호스팅하는 서버를 사용할 수 없는 경우 보고서를 사용할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="ee856-116">MBAM 백업이 VSS (볼륨 섀도 복사본 서비스)를 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="ee856-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="ee856-117">MBAM 2.0은 Microsoft BitLocker 관리 및 관리 작성자 라고 하는 VSS (볼륨 섀도 복사본 서비스) 기록기를 제공 하 여 규정 준수 및 감사 데이터베이스와 복구 데이터베이스를 쉽게 백업할 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="ee856-118">MBAM 서버 Windows Installer는 MBAM VSS 기록기를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="ee856-119">VSS 기록기를 등록 하는 동안 오류가 발생 하면 MBAM 서버 설치가 롤백됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="ee856-120">준수 및 감사 데이터베이스와 복구 데이터베이스가 서로 다른 서버에 설치 되어 있는 토폴로지에서는 각각의 MBAM VSS 기록기 인스턴스가 각 서버에 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="ee856-121">MBAM VSS 기록기는 SQL Server VSS 기록기에 종속적입니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="ee856-122">SQL Server VSS 기록기는 Microsoft SQL Server 설치의 일부로 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="ee856-123">백업을 수행 하기 위해 VSS 기록기를 사용 하는 모든 백업 기술은 MBAM VSS 기록기를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee856-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="ee856-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ee856-124">Related topics</span></span>


[<span data-ttu-id="ee856-125">MBAM 2.0 유지 관리</span><span class="sxs-lookup"><span data-stu-id="ee856-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 





