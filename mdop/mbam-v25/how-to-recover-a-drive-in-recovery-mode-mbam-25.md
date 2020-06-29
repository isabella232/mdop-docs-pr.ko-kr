---
title: 복구 모드에서 드라이브를 복구하는 방법
description: 복구 모드에서 드라이브를 복구하는 방법
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823368"
---
# <span data-ttu-id="f510d-103">복구 모드에서 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f510d-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="f510d-104">이 항목에서는 관리 및 모니터링 웹 사이트 (지원 데스크 라고도 함)를 사용 하 여 BitLocker로 보호 된 드라이브가 복구 모드로 전환 되는 경우 최종 사용자에 게 제공 하는 복구 암호를 가져오는 방법을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="f510d-105">사용자가 PIN 또는 암호를 분실 하거나 잊어버린 경우 또는 TPM (신뢰할 수 있는 모듈 플랫폼) 칩에서 컴퓨터의 BIOS 또는 시작 파일의 변경 내용을 감지 하는 경우 드라이브는 복구 모드로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="f510d-106">복구 암호를 얻으려면 관리 및 모니터링 웹 사이트의 **드라이브 복구** 영역을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="f510d-107">웹 사이트의이 영역에 액세스 하려면 MBAM 헬프데스크 사용자 역할 또는 MBAM 헬프데스크 사용자 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="f510d-108">참고</span><span class="sxs-lookup"><span data-stu-id="f510d-108">Note</span></span>**  
<span data-ttu-id="f510d-109">이러한 역할을 만들 때 서로 다른 이름을 지정 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="f510d-110">자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f510d-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="f510d-111">중요</span><span class="sxs-lookup"><span data-stu-id="f510d-111">Important</span></span>**  
<span data-ttu-id="f510d-112">복구 암호는 한 번 사용 후 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="f510d-113">운영 체제 드라이브 및 고정 데이터 드라이브에서는 단일 사용 규칙이 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="f510d-114">이동식 드라이브를 관리 하는 데 사용할 수 있는 그룹 정책 설정이 활성화 된 컴퓨터에서 드라이브를 제거 하 고 다시 삽입 한 후 잠금이 해제 되는 경우에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="f510d-115">복구 모드에서 드라이브를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="f510d-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="f510d-116">웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="f510d-117">왼쪽 창에서 **드라이브 복구** 를 선택 하 여 암호화 된 **드라이브에 대 한 액세스 복구** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="f510d-118">최종 사용자의 Windows 로그온 도메인 및 사용자 이름을 입력 하 여 복구 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="f510d-119">참고</span><span class="sxs-lookup"><span data-stu-id="f510d-119">Note</span></span>**  
    <span data-ttu-id="f510d-120">MBAM 헬프데스크 사용자 그룹에 속한 사용자 도메인 및 사용자 ID 필드는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="f510d-121">복구 키 ID의 처음 8 자리를 입력 하 여 일치 하는 복구 키 목록을 확인 하거나 전체 복구 키 ID를 입력 하 여 정확한 복구 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="f510d-122">**드라이브 잠금 해제 이유** 목록에서 미리 정의 된 옵션 중 하나를 선택한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="f510d-123">MBAM은 다음을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="f510d-124">일치 하는 복구 암호를 찾을 수 없는 경우 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="f510d-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="f510d-125">사용자에 게 일치 하는 복구 암호가 여러 개 있는 경우 일치 하는 항목 수</span><span class="sxs-lookup"><span data-stu-id="f510d-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="f510d-126">제출 된 사용자의 복구 암호 및 복구 패키지</span><span class="sxs-lookup"><span data-stu-id="f510d-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="f510d-127">참고</span><span class="sxs-lookup"><span data-stu-id="f510d-127">Note</span></span>**  
        <span data-ttu-id="f510d-128">손상 된 드라이브를 복구 하는 경우 복구 패키지 옵션은 드라이브를 복구 하는 데 필요한 중요 한 정보를 BitLocker에 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="f510d-129">암호를 복사 하려면 **키 복사**를 클릭 한 다음 복구 암호를 전자 메일 메시지에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="f510d-130">또는 **저장** 을 클릭 하 여 복구 암호를 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="f510d-131">사용자가 시스템에 복구 암호를 입력 하거나 복구 패키지를 사용 하는 경우 드라이브의 잠금이 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="f510d-132">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f510d-132">Related topics</span></span>


[<span data-ttu-id="f510d-133">MBAM 2.5를 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="f510d-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="f510d-134">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="f510d-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f510d-135">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f510d-136">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f510d-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





