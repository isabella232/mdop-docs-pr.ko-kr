---
title: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
description: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824473"
---
# <span data-ttu-id="652db-103">분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="652db-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="652db-104">관리 및 모니터링 웹 사이트에서이 절차를 사용 하 여 다음을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="652db-105">분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태</span><span class="sxs-lookup"><span data-stu-id="652db-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="652db-106">분실 하거나 도난당 한 컴퓨터의 볼륨을 암호화할지 여부</span><span class="sxs-lookup"><span data-stu-id="652db-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="652db-107">이 작업을 완료 하려면 관리 및 모니터링 웹 사이트의 **보고서** 영역에 대 한 액세스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="652db-108">이 영역에 대 한 액세스 권한을 얻으려면 MBAM 보고서 사용자 역할을 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="652db-109">이러한 역할을 만들 때 서로 다른 이름을 지정 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="652db-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="652db-110">자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="652db-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="652db-111">**참고**  디바이스 준수는 엔터프라이즈에서 배포한 BitLocker 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="652db-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="652db-112">장치의 BitLocker 암호화 상태를 확인 하기 전에 배포 된 정책을 확인 하려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="652db-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="652db-113">손실 된 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="652db-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="652db-114">웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="652db-115">왼쪽 창에서 **보고서** 를 선택 하 여 보고서 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="652db-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="652db-116">**컴퓨터 준수 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="652db-117">오른쪽 창의 필터 필드를 사용 하 여 검색 결과의 범위를 좁히고 **검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="652db-118">검색 쿼리에서 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="652db-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="652db-119">장치 손실에 대 한 정책에 따라 적절 한 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="652db-120">관련 항목</span><span class="sxs-lookup"><span data-stu-id="652db-120">Related topics</span></span>


[<span data-ttu-id="652db-121">MBAM 2.5를 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="652db-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="652db-122">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="652db-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="652db-123">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="652db-124">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="652db-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





