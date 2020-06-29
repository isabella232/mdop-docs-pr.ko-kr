---
title: 제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기
description: 제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823098"
---
# <span data-ttu-id="ee61c-103">제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기</span><span class="sxs-lookup"><span data-stu-id="ee61c-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="ee61c-104">이 항목에서는 Windows 운영 체제의 일부로 제어판에 기본적으로 표시 되는 **BitLocker 드라이브 암호화** 제어판 항목을 숨기는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="ee61c-105">**참고**  Microsoft BitLocker 관리 및 모니터링 (MBAM)은 **BitLocker 암호화 옵션**이라는 추가 사용자 지정 제어판 항목을 만들어 최종 사용자가 PIN 및 암호를 관리 하 고, 드라이브의 BitLocker를 켜고, 암호화를 확인할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="ee61c-106">[제어판의 Bitlocker 암호화 옵션 및 Bitlocker 드라이브 암호화 항목 이해](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) 를 참조 하 여 다음 사항을 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="ee61c-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="ee61c-107">MBAM과 기본 제어판 항목의 차이점</span><span class="sxs-lookup"><span data-stu-id="ee61c-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="ee61c-108">Windows 탐색기에서 드라이브를 마우스 오른쪽 단추로 클릭할 때 표시 되는 BitLocker 바로 가기 메뉴 **관리**</span><span class="sxs-lookup"><span data-stu-id="ee61c-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="ee61c-109">**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ee61c-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="ee61c-110">이 경우 MBAM이 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="ee61c-111">**MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="ee61c-112">제어판에서 기본 BitLocker 드라이브 암호화 항목을 숨기려면</span><span class="sxs-lookup"><span data-stu-id="ee61c-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="ee61c-113">GPMC (그룹 정책 관리 콘솔) 또는 고급 그룹 정책 관리에서 **사용자 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **제어판**을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="ee61c-114">**세부 정보** 창에서 **지정 된 제어판 항목 숨기기**를 두 번 클릭 한 다음 **사용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="ee61c-115">**표시**를 클릭 하 고 **추가**를 클릭 한 다음 **Microsoft. bitlocker드라이브 암호화**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="ee61c-116">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ee61c-116">Related topics</span></span>


[<span data-ttu-id="ee61c-117">BitLocker 암호화 옵션 및 제어판의 BitLocker 드라이브 암호화 항목 이해</span><span class="sxs-lookup"><span data-stu-id="ee61c-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="ee61c-118">MBAM 2.5 그룹 정책 개체 배포</span><span class="sxs-lookup"><span data-stu-id="ee61c-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="ee61c-119">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="ee61c-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ee61c-120">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ee61c-121">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee61c-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





