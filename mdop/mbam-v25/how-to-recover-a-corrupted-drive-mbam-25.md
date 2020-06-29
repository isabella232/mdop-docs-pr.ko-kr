---
title: 손상된 드라이브를 복구하는 방법
description: 손상된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822553"
---
# <span data-ttu-id="3b7a4-103">손상된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="3b7a4-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="3b7a4-104">이 절차는 관리 및 모니터링 웹사이트 (지원 센터 라고도 함) 웹 사이트에서 BitLocker로 보호 되는 손상 된 드라이브를 복구 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="3b7a4-105">이렇게 하려면 다음 표에서 설명 하는 작업을 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3b7a4-106">작업</span><span class="sxs-lookup"><span data-stu-id="3b7a4-106">Task</span></span></th>
<th align="left"><span data-ttu-id="3b7a4-107">자세한 내용 및 추가 정보</span><span class="sxs-lookup"><span data-stu-id="3b7a4-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3b7a4-108"><strong> </strong> 관리 및 모니터링 웹 사이트의 드라이브 복구 영역에 액세스 하 여 복구 키 패키지 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b7a4-109"><strong>드라이브 복구 영역에 액세스 하려면 </strong> Mbam 헬프데스크 사용자 역할 또는 Mbam Advanced 헬프데스크 사용자 역할을 할당 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="3b7a4-110">이러한 역할을 만들 때 서로 다른 이름을 지정 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="3b7a4-111">자세한 내용은 <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> MBAM 2.5 그룹 및 계정 계획을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="3b7a4-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3b7a4-112">손상 된 드라이브를 포함 하는 컴퓨터에 패키지 파일을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3b7a4-113"><code>repair-bde</code>복구 프로세스를 완료 하려면 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="3b7a4-114">잠재적인 데이터 손실을 방지 하려면 <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> 사용 하기 전에 manage-bde 명령을 검토 하는 것이 좋습니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="3b7a4-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="3b7a4-115">손상 된 드라이브 복구</span><span class="sxs-lookup"><span data-stu-id="3b7a4-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="3b7a4-116">웹 브라우저를 열고 **관리 및 모니터링 웹 사이트로**이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="3b7a4-117">왼쪽 창에서 **드라이브 복구** 를 선택 하 여 암호화 된 **드라이브에 대 한 액세스 복구** 페이지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="3b7a4-118">최종 사용자의 Windows 로그온 도메인 및 사용자 이름, 드라이브 잠금 해제 이유, 최종 사용자의 복구 암호 ID를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="3b7a4-119">**참고**  고급 헬프데스크 사용자 액세스 그룹의 구성원 인 경우 사용자의 도메인 이름 또는 사용자 이름을 입력할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="3b7a4-120">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-120">Click **Submit**.</span></span> <span data-ttu-id="3b7a4-121">복구 키가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="3b7a4-122">**저장**을 클릭 한 다음 **복구 키 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="3b7a4-123">컴퓨터에 복구 키 패키지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="3b7a4-124">복구 키 패키지를 손상 된 드라이브가 있는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="3b7a4-125">관리자 권한 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-125">Open an elevated command prompt.</span></span> <span data-ttu-id="3b7a4-126">이렇게 하려면 **시작** 을 클릭 하 고 `cmd` **프로그램 및 파일 검색** 텍스트 상자에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="3b7a4-127">**cmd.exe**를 마우스 오른쪽 단추로 클릭 하 고 **관리자 권한으로 실행**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="3b7a4-128">명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="3b7a4-129">**참고**  손상 된 드라이브를 사용 하는 &lt; *fixed drive* &gt; 하드 디스크 드라이브 (드라이브의 데이터 보다 더 크거나 같은 여유 공간)로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="3b7a4-130">손상 된 드라이브의 데이터를 복구 하 여 지정한 하드 디스크 드라이브로 옮깁니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="3b7a4-131">관련 항목</span><span class="sxs-lookup"><span data-stu-id="3b7a4-131">Related topics</span></span>


[<span data-ttu-id="3b7a4-132">MBAM 2.5를 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="3b7a4-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="3b7a4-133">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="3b7a4-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3b7a4-134">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3b7a4-135">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7a4-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





