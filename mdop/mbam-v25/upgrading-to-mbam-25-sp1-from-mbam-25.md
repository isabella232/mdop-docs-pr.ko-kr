---
title: MBAM 2.5에서 MBAM 2.5 SP1으로 업그레이드
description: MBAM 2.5에서 MBAM 2.5 SP1으로 업그레이드
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812745"
---
# <span data-ttu-id="a1301-103">MBAM 2.5에서 MBAM 2.5 SP1으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="a1301-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="a1301-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 2.5 및 MBAM 클라이언트를 2.5에서 MBAM 2.5 SP1로 업그레이드 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="a1301-105">시작하기 전에</span><span class="sxs-lookup"><span data-stu-id="a1301-105">Before you begin</span></span>
#### <span data-ttu-id="a1301-106">2019 년 5 월 서비스 릴리스 다운로드</span><span class="sxs-lookup"><span data-stu-id="a1301-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="a1301-107">데스크톱 최적화 팩</span><span class="sxs-lookup"><span data-stu-id="a1301-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="a1301-108">설치 documentaion 확인</span><span class="sxs-lookup"><span data-stu-id="a1301-108">Verify the installation documentaion</span></span>
<span data-ttu-id="a1301-109">모든 서버 이름, 데이터베이스 이름, 서비스 계정 및 암호를 포함 하 여 현재 MBAM 환경에 대 한 문서가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-109">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="a1301-110">업그레이드 단계</span><span class="sxs-lookup"><span data-stu-id="a1301-110">Upgrade steps</span></span>
#### <span data-ttu-id="a1301-111">MBAM 데이터베이스를 업그레이드 하는 단계 (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="a1301-111">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="a1301-112">MBAM 구성자 사용 SQL server에서 또는 SSRS 데이터베이스가 호스팅되는 모든 위치에서 보고서 역할을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-112">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="a1301-113">환경에 따라 동일한 서버 또는 개별 항목 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-113">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="a1301-114">데이터베이스를 제거 하는 옵션이 표시 되지 않습니다. 이는 예상 되는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-114">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="a1301-115">볼륨 라이선스 서비스 센터 사이트의 MDOP-Microsoft 데스크톱 최적화 팩 2015에 있는 2.5 SP1을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-115">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="a1301-116">지금 구성 하지 않음</span><span class="sxs-lookup"><span data-stu-id="a1301-116">Do not configure it at this time</span></span> 
4. <span data-ttu-id="a1301-117">MBAM 구성자 사용 보고서 역할 다시 추가</span><span class="sxs-lookup"><span data-stu-id="a1301-117">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="a1301-118">MBAM 구성자 사용 SQL Server에서 SQL 데이터베이스 역할 다시 추가</span><span class="sxs-lookup"><span data-stu-id="a1301-118">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="a1301-119">마지막에는 해당 레코드가 이미 존재 하 고 생성 되지 않았다는 경고가 표시 되지만, 이것은 예상 되는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-119">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="a1301-120">이 프로세스는 기존 데이터베이스를 설치 중인 현재 버전으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-120">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="a1301-121">MBAM 서버를 업그레이드 하는 단계 (MBAM 및 IIS 실행)</span><span class="sxs-lookup"><span data-stu-id="a1301-121">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="a1301-122">MBAM 구성자 사용 IIS 서버에서 관리자 및 셀프 서비스 포털 제거</span><span class="sxs-lookup"><span data-stu-id="a1301-122">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="a1301-123">MBAM 2.5 SP1 설치</span><span class="sxs-lookup"><span data-stu-id="a1301-123">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="a1301-124">지금 구성 하지 않음</span><span class="sxs-lookup"><span data-stu-id="a1301-124">Do not configure it at this time</span></span>  
4. <span data-ttu-id="a1301-125">MBAM 구성자 사용 관리자 및 셀프 서비스 포털을 IIS 서버에 다시 추가</span><span class="sxs-lookup"><span data-stu-id="a1301-125">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="a1301-126">관리자 권한 명령 프롬프트를 열고 **IISRESET**을 입력 한 다음 enter 키를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-126">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="a1301-127">MBAM 클라이언트/끝점을 업그레이드 하는 단계</span><span class="sxs-lookup"><span data-stu-id="a1301-127">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="a1301-128">클라이언트 끝점에서 2.5 에이전트 제거</span><span class="sxs-lookup"><span data-stu-id="a1301-128">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="a1301-129">클라이언트 끝점에 2.5 SP1 에이전트 설치</span><span class="sxs-lookup"><span data-stu-id="a1301-129">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="a1301-130">2.5 SP1 에이전트를 실행 하는 클라이언트에 대 한 2019 롤업 클라이언트 업데이트를 푸시 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-130">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="a1301-131">5 월 2019 롤업을 설치 하기 전에 기존 클라이언트를 제거할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a1301-131">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
