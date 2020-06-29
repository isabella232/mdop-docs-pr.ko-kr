---
title: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
description: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826703"
---
# <span data-ttu-id="0c8b4-103">셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법</span><span class="sxs-lookup"><span data-stu-id="0c8b4-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="0c8b4-104">셀프 서비스 포털은 IT 관리자가 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 배포의 일부로 구성 하는 웹 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="0c8b4-105">웹 사이트를 사용 하면 Windows에서 잠긴 경우 최종 사용자가 자신의 컴퓨터에 개별적으로 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="0c8b4-106">셀프 서비스 포털에는 지원 센터 직원의 지원이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="0c8b4-107">다음 지침은 최종 사용자의 관점에서 작성 되었지만 IT 관리자가 이해 하는 데 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="0c8b4-108">**중요**  최종 사용자가 직접 컴퓨터에 로그온 해야 합니다 (원격이 아닌 경우). 셀프 서비스 포털을 사용 하 여 해당 키를 복구 하기 위해 적어도 한 번은 성공적으로 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="0c8b4-109">그렇지 않으면 키 복구를 위해 헬프 데스크 포털을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="0c8b4-110">다음과 같은 경우 최종 사용자가 잠금을 경험할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="0c8b4-111">암호 또는 PIN을 잊으셨습니까?</span><span class="sxs-lookup"><span data-stu-id="0c8b4-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="0c8b4-112">운영 체제 파일, BIOS 또는 TPM (신뢰할 수 있는 플랫폼 모듈) 변경</span><span class="sxs-lookup"><span data-stu-id="0c8b4-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="0c8b4-113">**참고**  IT 관리자가 IIS 세션 상태 시간을 구성한 경우 셀프 서비스 포털에는 시간 제한 보다 60 초 전에 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="0c8b4-114">셀프 서비스 포털을 사용 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻으려면</span><span class="sxs-lookup"><span data-stu-id="0c8b4-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="0c8b4-115">**복구 KeyId** 필드에 컴퓨터의 BitLocker 복구 화면에 표시 되는 32 자리 BITLOCKER 키 ID 중 최소 8 개를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="0c8b4-116">첫 8 자리가 여러 키와 일치 하는 경우 복구 키 ID의 모든 32 자릿수를 입력 해야 한다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="0c8b4-117">**이유** 필드에서 복구 키에 대 한 요청 이유를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="0c8b4-118">**키 가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-118">Click **Get Key**.</span></span> <span data-ttu-id="0c8b4-119">Bitlocker **복구 키 필드에** 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="0c8b4-120">컴퓨터의 BitLocker 복구 화면에 48 자리 코드를 입력 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="0c8b4-121">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0c8b4-121">Related topics</span></span>


[<span data-ttu-id="0c8b4-122">MBAM 2.5를 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="0c8b4-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="0c8b4-123">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="0c8b4-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0c8b4-124">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0c8b4-125">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8b4-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





