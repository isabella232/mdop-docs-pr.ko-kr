---
title: MBAM 2.5 SP1에 핫픽스 적용
description: MBAM 2.5 SP1에 핫픽스 적용
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824188"
---
# <span data-ttu-id="6f170-103">MBAM 2.5 SP1에 핫픽스 적용</span><span class="sxs-lookup"><span data-stu-id="6f170-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="6f170-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) Server 2.5 SP1 용 핫픽스를 적용 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f170-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="6f170-105">시작 하기 전에 Microsoft BitLocker 관리 및 모니터링 (MBAM) Server 2.5 SP1의 최신 핫픽스를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f170-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="6f170-106">데스크톱 최적화 팩</span><span class="sxs-lookup"><span data-stu-id="6f170-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="6f170-107">핫픽스 릴리스에 대 한 자세한 내용은 [Mbam 버전 차트](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f170-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="6f170-108">기존 MBAM 환경에 대 한 MBAM 서버를 업데이트 하는 단계</span><span class="sxs-lookup"><span data-stu-id="6f170-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="6f170-109">Mbam 서버 구성 도구를 열고 기능 제거를 선택 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f170-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="6f170-110">제어판에서 MDOP MBAM 제거 | 프로그램 및 기능.</span><span class="sxs-lookup"><span data-stu-id="6f170-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="6f170-111">MBAM 2.5 SP1 RTM 서버 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f170-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="6f170-112">최신 MBAM 2.5 SP1 핫픽스 롤업을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f170-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="6f170-113">MBAM 서버 구성자를 사용 하 여 MBAM 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f170-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="6f170-114">새 MBAM 2.5 SP1 서버 핫픽스를 설치 하는 단계</span><span class="sxs-lookup"><span data-stu-id="6f170-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="6f170-115">[새 서버 설치](deploying-the-mbam-25-server-infrastructure.md)에 대 한 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f170-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
