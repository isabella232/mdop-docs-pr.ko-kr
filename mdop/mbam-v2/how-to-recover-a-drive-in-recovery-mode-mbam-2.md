---
title: 복구 모드에서 드라이브를 복구하는 방법
description: 복구 모드에서 드라이브를 복구하는 방법
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825058"
---
# <span data-ttu-id="f644f-103">복구 모드에서 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="f644f-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="f644f-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)의 암호화 된 드라이브 복구 기능을 통해 BitLocker가 복구 모드로 전환 될 때 BitLocker로 보호 된 볼륨에 액세스 하는 데 필요한 도구의 데이터 및 저장소 가용성을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="f644f-105">BitLocker로 보호 된 볼륨은 PIN 또는 암호를 분실 하거나 잊어버린 경우 또는 TPM (신뢰할 수 있는 모듈 플랫폼) 칩이 컴퓨터의 BIOS 또는 시작 파일의 변경 내용을 감지 하는 경우 복구 모드로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="f644f-106">복구 암호 ID 및 연결 된 사용자 식별자가 제공 되는 경우 복구 암호를 제공할 수 있는 중앙 집중화 된 키 복구 데이터 시스템에 액세스 하려면이 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="f644f-107">중요</span><span class="sxs-lookup"><span data-stu-id="f644f-107">Important</span></span>**  
<span data-ttu-id="f644f-108">Microsoft BitLocker 관리 및 모니터링은 사용할 때 만료 되는 단일 사용 복구 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="f644f-109">운영 체제 드라이브 및 고정 드라이브에는 복구 암호를 한 번만 사용 하 여 자동으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="f644f-110">이동식 드라이브를 관리 하기 위해 그룹 정책 설정이 활성화 된 컴퓨터에서 드라이브를 제거 하 고 다시 삽입 하 고 잠금을 해제 하는 경우에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="f644f-111">복구 모드에서 드라이브를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="f644f-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="f644f-112">웹 브라우저를 열고 관리 및 모니터링 웹 사이트로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="f644f-113">탐색 창에서 **드라이브 복구**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="f644f-114">"암호화 된 드라이브에 대 한 액세스 복구" 웹 페이지가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="f644f-115">Windows 로그온 도메인 및 사용자 이름을 입력 하 여 복구 정보를 확인 하 고 복구 키 ID의 처음 8 자리를 사용 하 여 일치 하는 복구 키 목록 또는 복구 키를 정확 하 게 받을 수 있는 복구 키의 전체 ID를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="f644f-116">**드라이브 잠금 해제 이유** 목록에서 미리 정의 된 옵션 중 하나를 선택한 다음 **제출을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="f644f-117">참고</span><span class="sxs-lookup"><span data-stu-id="f644f-117">Note</span></span>**  
    <span data-ttu-id="f644f-118">MBAM 고급 헬프 데스크 사용자는 사용자 도메인 및 사용자 ID 항목이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="f644f-119">암호를 복사 하려면 **키 복사**를 클릭 한 다음 복구 암호를 전자 메일 메시지에 붙여 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="f644f-120">또는 **저장** 을 클릭 하 여 복구 암호를 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="f644f-121">사용자가 시스템에 복구 암호를 입력 하거나 복구 패키지를 사용 하는 경우 드라이브의 잠금이 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f644f-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="f644f-122">관련 항목</span><span class="sxs-lookup"><span data-stu-id="f644f-122">Related topics</span></span>


[<span data-ttu-id="f644f-123">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="f644f-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









