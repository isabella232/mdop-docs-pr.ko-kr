---
title: 손상된 드라이브를 복구하는 방법
description: 손상된 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812945"
---
# <span data-ttu-id="5fa0e-103">손상된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="5fa0e-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="5fa0e-104">BitLocker로 보호 되는 손상 된 드라이브를 복구 하려면 Microsoft BitLocker 관리 및 모니터링 (MBAM) 지원 센터 사용자가 복구 키 패키지 파일을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="5fa0e-105">손상 된 드라이브를 포함 하는 컴퓨터에이 패키지 파일을 복사한 다음 드라이브를 복구 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="5fa0e-106">이 작업을 수행 하려면 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="5fa0e-107">손상 된 드라이브 복구</span><span class="sxs-lookup"><span data-stu-id="5fa0e-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="5fa0e-108">MBAM 관리 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="5fa0e-109">탐색 창에서 **드라이브 복구** 를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="5fa0e-110">사용자의 도메인 이름과 사용자 이름, 드라이브 잠금 해제 이유, 사용자의 복구 암호 ID를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="5fa0e-111">**참고**  지원 센터 관리자 역할의 구성원 인 경우 사용자의 도메인 이름 또는 사용자 이름을 입력할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="5fa0e-112">**제출**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-112">Click **Submit**.</span></span> <span data-ttu-id="5fa0e-113">복구 키가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="5fa0e-114">**저장**을 클릭 한 다음 **복구 키 패키지**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="5fa0e-115">컴퓨터에 복구 키 패키지가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="5fa0e-116">복구 키 패키지를 손상 된 드라이브가 있는 컴퓨터에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="5fa0e-117">관리자 권한 명령 프롬프트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-117">Open an elevated command prompt.</span></span> <span data-ttu-id="5fa0e-118">이렇게 하려면 **시작** 을 클릭 하 고 `cmd` **프로그램 및 파일 검색** 상자에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="5fa0e-119">검색 결과 목록에서 **cmd.exe** 를 마우스 오른쪽 단추로 클릭 하 고 **관리자 권한으로 실행**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="5fa0e-120">명령 프롬프트에서 다음을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="5fa0e-121">**참고**  &lt;명령에 있는 고정 드라이브에는 &gt; 손상 된 드라이브의 데이터 보다 더 크거나 같은 여유 공간이 있는 사용 가능한 저장소 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="5fa0e-122">손상 된 드라이브의 데이터를 복구 하 고 지정한 고정식 드라이브로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fa0e-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="5fa0e-123">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5fa0e-123">Related topics</span></span>


[<span data-ttu-id="5fa0e-124">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="5fa0e-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





