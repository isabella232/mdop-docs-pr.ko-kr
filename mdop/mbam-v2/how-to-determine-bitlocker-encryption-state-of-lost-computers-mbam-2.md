---
title: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
description: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
author: dansimp
ms.assetid: dbd23b64-dff3-4913-9acd-affe67b9462e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9ea4afd6dd08f2040b9e2bd1e1a8998181d1e60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824613"
---
# <span data-ttu-id="5b121-103">분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="5b121-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="5b121-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-104">You can use Microsoft BitLocker Administration and Monitoring (MBAM) to determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span> <span data-ttu-id="5b121-105">다음 절차에서는 컴퓨터의 볼륨이 손실 되거나 도난당 한 경우 암호화 되는지 여부를 확인 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-105">The following procedure explains how to determine whether the volumes on a computer are encrypted if there is a loss or theft.</span></span>

**<span data-ttu-id="5b121-106">손실 된 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인 하려면</span><span class="sxs-lookup"><span data-stu-id="5b121-106">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="5b121-107">웹 브라우저를 열고 관리 및 모니터링 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-107">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

    <span data-ttu-id="5b121-108">**참고**  참고: 관리 및 모니터링 웹 사이트의 기본 주소는 http://\* &lt; computername &gt; \*입니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-108">**Note** Note: The default address for the Administration and Monitoring website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="5b121-109">정규화 된 서버 이름을 사용 하면 검색 결과가 더 빠르게 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-109">Using the fully qualified server name will yield faster browsing results.</span></span>

     

2.  <span data-ttu-id="5b121-110">탐색 창에서 **보고서** 노드를 선택 하 고 **컴퓨터 준수 보고서**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-110">Selects the **Report** node from the navigation pane, and select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="5b121-111">오른쪽 창의 필터 필드를 사용 하 여 검색 결과의 범위를 좁히고 **검색**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-111">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="5b121-112">검색 쿼리 아래에 결과가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-112">Results are shown below your search query.</span></span>

4.  <span data-ttu-id="5b121-113">장치 손실에 대 한 정책에 따라 적절 한 조치를 취해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-113">Take the appropriate action, as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="5b121-114">**참고**  디바이스 준수는 엔터프라이즈에서 배포한 BitLocker 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-114">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="5b121-115">장치의 BitLocker 암호화 상태를 확인 하기 전에 배포 된 정책을 확인 하려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b121-115">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="5b121-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5b121-116">Related topics</span></span>


[<span data-ttu-id="5b121-117">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="5b121-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





