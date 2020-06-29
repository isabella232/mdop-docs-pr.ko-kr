---
title: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
description: 셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826078"
---
# <span data-ttu-id="b2fb7-103">셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법</span><span class="sxs-lookup"><span data-stu-id="b2fb7-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="b2fb7-104">최종 사용자가 암호나 PIN을 잊었거나, 운영 체제 파일을 변경 하거나, BIOS 또는 TPM (신뢰할 수 있는 플랫폼 모듈)을 변경 하 였 기 때문에 Windows에서 BitLocker를 통해 잠긴 경우 셀프 서비스 포털을 사용 하 여 지원 부서에 도움을 요청 하지 않고 Windows에 다시 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="b2fb7-105">**참고**  IT 관리자가 IIS 세션 상태 시간 초과를 구성한 경우에는 시간 초과 전에 60 초 후에 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="b2fb7-106">**참고**  이러한 지침은 최종 사용자의 관점에서 작성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="b2fb7-107">셀프 서비스 포털을 사용 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻으려면</span><span class="sxs-lookup"><span data-stu-id="b2fb7-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="b2fb7-108">**복구 KeyId** 필드에 컴퓨터의 BitLocker 복구 화면에 표시 되는 32 자리 BITLOCKER 키 ID 중 최소 8 개를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="b2fb7-109">**참고**  첫 8 자리가 여러 키와 일치 하는 경우 복구 키 ID의 모든 32 자릿수를 입력 해야 한다는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="b2fb7-110">**이유** 필드에서 복구 키에 대 한 요청 이유를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="b2fb7-111">**키 가져오기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-111">Click **Get Key**.</span></span> <span data-ttu-id="b2fb7-112">BitLocker 복구 키가 "BitLocker 복구 키" 필드에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="b2fb7-113">컴퓨터의 BitLocker 복구 화면에 48 자리 코드를 입력 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2fb7-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="b2fb7-114">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b2fb7-114">Related topics</span></span>


[<span data-ttu-id="b2fb7-115">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="b2fb7-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





