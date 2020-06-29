---
title: 복구 모드에서 드라이브를 복구하는 방법
description: 복구 모드에서 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812953"
---
# <span data-ttu-id="0a86b-103">복구 모드에서 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="0a86b-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="0a86b-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 암호화 된 드라이브 복구 기능을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="0a86b-105">이러한 기능을 통해 BitLocker가 볼륨을 복구 모드로 전환 했을 때 BitLocker 보호 볼륨에 액세스 하는 데 필요한 도구를 사용 하 고 데이터를 캡처하고 저장 하는 것을 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="0a86b-106">BitLocker로 보호 되는 볼륨은 PIN 또는 암호를 분실 하거나 잊어버린 경우 또는 TPM (신뢰할 수 있는 모듈 플랫폼) 칩이 컴퓨터의 BIOS 또는 시작 파일에 대 한 변경 내용을 검색 하는 경우 복구 모드에 들어갑니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="0a86b-107">복구 암호 ID 및 연결 된 사용자 식별자가 제공 된 경우 복구 암호를 제공할 수 있는 중앙 집중화 된 키 복구 데이터 시스템에 액세스 하려면이 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="0a86b-108">**중요**  MBAM은 단일 사용 복구 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="0a86b-109">이 제한에 따라 복구 키는 한 번만 사용할 수 있으며 더 이상 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="0a86b-110">운영 체제 드라이브 및 고정 드라이브에는 복구 암호를 한 번만 사용 하 여 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="0a86b-111">이동식 드라이브를 관리 하는 그룹 정책 설정이 활성화 된 컴퓨터에서 드라이브를 제거 하 고 다시 삽입 하 고 잠금 해제 한 경우 단일 사용이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="0a86b-112">복구 모드에서 드라이브를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="0a86b-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="0a86b-113">MBAM 웹 사이트를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="0a86b-114">탐색 창에서 **드라이브 복구**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="0a86b-115">**암호화 된 드라이브에 대 한 액세스 복구** 웹 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="0a86b-116">사용자의 Windows 로그온 도메인 및 사용자 이름과 복구 키 ID의 첫 8 자리 숫자를 입력 하 여 일치 하는 복구 키의 목록을 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="0a86b-117">또는 전체 복구 키 ID를 입력 하 여 정확한 복구 키를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="0a86b-118">**드라이브 잠금 해제 이유** 드롭다운 목록에서 미리 정의 된 옵션 중 하나를 선택 하 고 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="0a86b-119">**참고**  MBAM 고급 헬프 데스크 사용자는 사용자 도메인 및 사용자 ID 항목이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="0a86b-120">MBAM은 다음을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="0a86b-121">일치 하는 복구 암호를 찾을 수 없는 경우 오류 메시지</span><span class="sxs-lookup"><span data-stu-id="0a86b-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="0a86b-122">사용자에 게 일치 하는 복구 암호가 여러 개 있는 경우 일치 하는 항목 수</span><span class="sxs-lookup"><span data-stu-id="0a86b-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="0a86b-123">제출 된 사용자의 복구 암호 및 복구 패키지</span><span class="sxs-lookup"><span data-stu-id="0a86b-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="0a86b-124">**참고**  손상 된 드라이브를 복구 하는 경우 복구 패키지 옵션은 BitLocker에 복구를 시도 하는 데 필요한 중요 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="0a86b-125">복구 암호와 복구 패키지가 검색 되 고 나면 복구 암호가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="0a86b-126">암호를 복사 하려면 **키 복사**를 클릭 한 다음 복구 암호를 임시 저장소에 대 한 전자 메일 또는 기타 텍스트 파일에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="0a86b-127">또는 복구 암호를 파일에 저장 하려면 **저장**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="0a86b-128">사용자가 시스템에 복구 암호를 입력 하거나 복구 패키지를 사용 하는 경우 드라이브의 잠금이 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a86b-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="0a86b-129">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0a86b-129">Related topics</span></span>


[<span data-ttu-id="0a86b-130">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="0a86b-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





