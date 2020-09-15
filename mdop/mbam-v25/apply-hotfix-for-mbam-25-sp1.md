---
title: MBAM 2.5 SP1에 핫픽스 적용
description: MBAM 2.5 SP1에 핫픽스 적용
ms.author: dansimp
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: ea564d93a3eec6a46ec7d4c1be0f794abba9c93e
ms.sourcegitcommit: 8ecbf818a6ff2ddafd80b93614c01256484737ad
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/14/2020
ms.locfileid: "11014992"
---
# <span data-ttu-id="cdbb4-103">MBAM 2.5 SP1에 핫픽스 적용</span><span class="sxs-lookup"><span data-stu-id="cdbb4-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="cdbb4-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) Server 2.5 SP1 용 핫픽스를 적용 하는 프로세스에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="cdbb4-105">시작 하기 전에 Microsoft BitLocker 관리 및 모니터링 (MBAM) Server 2.5 SP1의 최신 핫픽스를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="cdbb4-106">데스크톱 최적화 팩</span><span class="sxs-lookup"><span data-stu-id="cdbb4-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="cdbb4-107">핫픽스 릴리스에 대 한 자세한 내용은 [Mbam 버전 차트](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="cdbb4-108">기존 MBAM 환경에 대 한 MBAM 서버를 업데이트 하는 단계</span><span class="sxs-lookup"><span data-stu-id="cdbb4-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="cdbb4-109">Mbam 서버 구성 도구를 열고 기능 제거를 선택 하 여이 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="cdbb4-110">제어판에서 MDOP MBAM 제거 | 프로그램 및 기능.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="cdbb4-111">MBAM 2.5 SP1 RTM 서버 구성 요소를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="cdbb4-112">최신 MBAM 2.5 SP1 핫픽스 롤업을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="cdbb4-113">MBAM 서버 구성자를 사용 하 여 MBAM 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="cdbb4-114">새 MBAM 2.5 SP1 서버 핫픽스를 설치 하는 단계</span><span class="sxs-lookup"><span data-stu-id="cdbb4-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="cdbb4-115">[새 서버 설치](deploying-the-mbam-25-server-infrastructure.md)에 대 한 문서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdbb4-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
