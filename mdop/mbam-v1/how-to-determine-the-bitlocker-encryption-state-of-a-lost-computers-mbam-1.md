---
title: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
description: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824293"
---
# <span data-ttu-id="c15bd-103">분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="c15bd-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="c15bd-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하면 분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="c15bd-105">다음 절차를 사용 하 여 더 이상 소유 하지 않는 컴퓨터에서 볼륨이 암호화 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="c15bd-106">컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태 확인</span><span class="sxs-lookup"><span data-stu-id="c15bd-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="c15bd-107">MBAM 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-107">Open the MBAM website.</span></span>

    <span data-ttu-id="c15bd-108">**참고**  MBAM 웹 사이트의 기본 주소는 http://\* &lt; computername &gt; \*입니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="c15bd-109">더 빠른 검색 결과를 위해 정규화 된 서버 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="c15bd-110">탐색 창에서 **보고서** 노드를 선택한 다음 **컴퓨터 준수 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="c15bd-111">오른쪽 창의 필터 필드를 사용 하 여 검색 결과의 범위를 좁히고 **검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="c15bd-112">검색 쿼리 아래에 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="c15bd-113">장치 손실에 대 한 정책에 따라 적절 한 조치를 취할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="c15bd-114">**참고**  디바이스 준수는 배포 된 BitLocker 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="c15bd-115">장치의 BitLocker 암호화 상태를 확인 하려는 경우 이러한 배포 된 정책을 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15bd-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="c15bd-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c15bd-116">Related topics</span></span>


[<span data-ttu-id="c15bd-117">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="c15bd-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





