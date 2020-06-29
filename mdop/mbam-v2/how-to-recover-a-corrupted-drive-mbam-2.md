---
title: 손상된 드라이브를 복구하는 방법
description: 손상된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822873"
---
# <span data-ttu-id="7e8c9-103">손상된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="7e8c9-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="7e8c9-104">BitLocker로 보호 되는 손상 된 드라이브를 복구 하기 위해 Microsoft BitLocker 관리 및 모니터링 (MBAM) 지원 센터 사용자는 복구 키 패키지 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="7e8c9-105">그런 다음이 패키지 파일을 손상 된 드라이브를 포함 하는 컴퓨터에 복사한 다음 드라이브를 복구 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="7e8c9-106">이 작업을 수행 하는 데 필요한 단계에 대해 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="7e8c9-107">**중요**  잠재적인 데이터 손실을 방지 하려면 다음 지침을 완료 하기 전에 "복구-manage-bde" 도움말을 읽고 명령을 사용 하는 방법을 명확히 이해 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="7e8c9-108">손상 된 드라이브 복구</span><span class="sxs-lookup"><span data-stu-id="7e8c9-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="7e8c9-109">손상 된 드라이브를 복구 하는 데 필요한 복구 키 패키지를 만들려면 웹 브라우저를 시작 하 고 MBAM 관리 및 모니터링 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="7e8c9-110">왼쪽 탐색 창에서 **드라이브 복구** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="7e8c9-111">사용자의 도메인 이름, 사용자 이름, 드라이브 잠금 이유, 사용자의 복구 암호 ID를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="7e8c9-112">**참고**  지원 센터 관리자 역할의 구성원 인 경우 사용자의 도메인 이름 또는 사용자 이름을 입력할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="7e8c9-113">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-113">Click **Submit**.</span></span> <span data-ttu-id="7e8c9-114">복구 키가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="7e8c9-115">**저장**을 클릭 한 다음 **복구 키 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="7e8c9-116">컴퓨터에 복구 키 패키지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="7e8c9-117">복구 키 패키지를 손상 된 드라이브가 있는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="7e8c9-118">관리자 권한 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-118">Open an elevated command prompt.</span></span> <span data-ttu-id="7e8c9-119">이렇게 하려면 **시작** 을 클릭 하 고 `cmd` **프로그램 및 파일 검색 상자**에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="7e8c9-120">**cmd.exe** 를 마우스 오른쪽 단추로 클릭 하 고 **관리자 권한으로 실행**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="7e8c9-121">명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="7e8c9-122">**참고**  손상 된 드라이브를 사용 하는 &lt; &gt; 하드 디스크 드라이브 (드라이브의 데이터 보다 더 크거나 같은 여유 공간)로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="7e8c9-123">손상 된 드라이브의 데이터를 복구 하 여 지정한 하드 디스크 드라이브로 옮깁니다.</span><span class="sxs-lookup"><span data-stu-id="7e8c9-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="7e8c9-124">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7e8c9-124">Related topics</span></span>


[<span data-ttu-id="7e8c9-125">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="7e8c9-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





