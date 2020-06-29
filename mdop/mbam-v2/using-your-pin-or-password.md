---
title: PIN 또는 암호 사용
description: PIN 또는 암호 사용
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823793"
---
# <span data-ttu-id="1f14e-103">PIN 또는 암호 사용</span><span class="sxs-lookup"><span data-stu-id="1f14e-103">Using Your PIN or Password</span></span>


<span data-ttu-id="1f14e-104">BitLocker는 PIN (개인 식별 번호) 또는 암호를 요구 하 여 컴퓨터에 저장 된 정보를 잠금 해제 하 여 컴퓨터를 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-104">BitLocker helps secure your computer by requiring a personal identification number (PIN) or password to unlock the information that is stored on your computer.</span></span> <span data-ttu-id="1f14e-105">PIN 또는 암호 요구 사항은 조직에서 설정 하며 암호화 되는 드라이브의 종류에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-105">The PIN or password requirements are set by your organization and depend on the kind of drive being encrypted.</span></span> <span data-ttu-id="1f14e-106">암호화 된 드라이브의 데이터는 PIN 또는 암호를 입력 해야만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-106">Data on the encrypted drives cannot be viewed without entering the PIN or password.</span></span> <span data-ttu-id="1f14e-107">컴퓨터 하드웨어에 TPM (신뢰할 수 있는 플랫폼 모듈)이 포함 되어 있는 경우 TPM 칩에 Windows가 컴퓨터에서 시작 되기 전에 PIN을 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-107">If your computer hardware includes an enabled Trusted Platform Module (TPM), the TPM chip prompts you for your PIN before Windows starts on your computer.</span></span>

## <span data-ttu-id="1f14e-108">BitLocker PIN 및 암호 정보</span><span class="sxs-lookup"><span data-stu-id="1f14e-108">About Your BitLocker PIN and Passwords</span></span>


<span data-ttu-id="1f14e-109">귀하의 회사는 PIN 또는 비밀 번호에 필요한 복잡성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-109">Your company specifies the complexity required for your PIN or password.</span></span> <span data-ttu-id="1f14e-110">PIN 또는 암호에 대 한 이러한 요구 사항은 BitLocker 설치 프로세스 중에 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-110">These requirements for your PIN or password are explained during the BitLocker setup process.</span></span>

<span data-ttu-id="1f14e-111">암호는 컴퓨터에서 운영 체제를 포함 하지 않는 드라이브의 잠금을 해제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-111">The password is used to unlock drives on your computer that do not contain the operating system.</span></span> <span data-ttu-id="1f14e-112">BitLocker는 시작 하는 동안 PIN을 요청한 후 비밀 번호를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-112">BitLocker will ask for your password after the PIN is requested during startup.</span></span> <span data-ttu-id="1f14e-113">컴퓨터의 각 BitLocker 보호 하드 디스크에는 고유한 암호가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-113">Each BitLocker protected hard disk on your computer has its own unique password.</span></span> <span data-ttu-id="1f14e-114">비밀 번호를 입력할 때까지 BitLocker 보호 드라이브의 잠금을 해제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-114">You cannot unlock a BitLocker protected drive until you provide your password.</span></span>

<span data-ttu-id="1f14e-115">**참고**  지원 센터에서 자동으로 잠금 해제 되도록 드라이브를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-115">**Note** Your Help Desk may set drives to unlock automatically.</span></span> <span data-ttu-id="1f14e-116">이렇게 하면 드라이브에 대 한 정보를 볼 수 있는 PIN 또는 암호를 제공할 필요가 없어집니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-116">This eliminates the need to provide a PIN or password to view the information on the drives.</span></span>

 

## <span data-ttu-id="1f14e-117">PIN 또는 암호를 잊어버린 경우 컴퓨터 잠금 해제</span><span class="sxs-lookup"><span data-stu-id="1f14e-117">Unlocking Your Computer if You Forget Your PIN or Password</span></span>


<span data-ttu-id="1f14e-118">PIN 이나 비밀 번호를 잊어버린 경우 지원 센터에서 BitLocker 보호 드라이브의 잠금을 해제할 수 있도록 도와 드립니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-118">If you forget your PIN or password, your Help Desk can help you unlock BitLocker protected drives.</span></span> <span data-ttu-id="1f14e-119">BitLocker로 보호 되는 드라이브의 잠금을 해제 하려면 도움이 필요한 경우 지원 센터에 문의 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f14e-119">To unlock a drive protected with BitLocker, contact your Help Desk if you need help.</span></span>

**<span data-ttu-id="1f14e-120">PIN 또는 암호를 잊어버린 경우 컴퓨터 잠금을 해제 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1f14e-120">How to unlock your computer if you forget your PIN or password</span></span>**

1.  <span data-ttu-id="1f14e-121">지원 센터에 문의할 때 다음과 같은 정보를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-121">When you contact your Help Desk, you will need to provide them with the following information:</span></span>

    -   <span data-ttu-id="1f14e-122">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="1f14e-122">Your user name</span></span>

    -   <span data-ttu-id="1f14e-123">도메인</span><span class="sxs-lookup"><span data-stu-id="1f14e-123">Your domain</span></span>

    -   <span data-ttu-id="1f14e-124">복구 키 ID의 처음 8 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-124">The first eight digits of your recovery key ID.</span></span> <span data-ttu-id="1f14e-125">PIN 또는 암호를 잊어버린 경우 BitLocker에서 표시 하는 32 자리 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-125">This is a 32-digit code that BitLocker will display if you forget your PIN or password.</span></span>

        -   <span data-ttu-id="1f14e-126">PIN을 잊어버린 경우에는 BitLocker 복구 콘솔에 표시 되는 복구 키 ID의 처음 8 자리 숫자를 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-126">If you forget your PIN, you will have to enter the first eight digits of the recovery key ID, which will appear in the BitLocker Recovery console.</span></span> <span data-ttu-id="1f14e-127">BitLocker 복구 콘솔은 올바른 PIN을 입력 하지 않은 경우 표시 되는 Windows 이전 화면입니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-127">The BitLocker Recovery console is a pre-Windows screen that will be displayed if you do not enter the correct PIN.</span></span>

        -   <span data-ttu-id="1f14e-128">암호를 잊어버린 경우 BitLocker 암호화 옵션 제어판의 응용 프로그램에서 복구 키 ID를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-128">If you forget your password, look for the recovery key ID in the BitLocker Encryption Options Control Panel application.</span></span> <span data-ttu-id="1f14e-129">**드라이브 잠금 해제** 를 선택 하 고 **암호를 저장할 수 없음을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-129">Select **Unlock Drive** and then click **I cannot remember my password**.</span></span> <span data-ttu-id="1f14e-130">그러면 BitLocker 암호화 옵션 응용 프로그램에서 지원 센터에 제공 하는 복구 키 ID가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-130">The BitLocker Encryption Options application will then display a recovery key ID that you provide to Help Desk.</span></span>

2.  <span data-ttu-id="1f14e-131">지원 센터에서 필요한 정보를 받으면 휴대폰 이나 전자 메일을 통해 복구 키를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-131">Once your Help Desk receives the necessary information, it will provide you with a recovery key over the phone or through e-mail.</span></span>

    -   <span data-ttu-id="1f14e-132">PIN을 잊어버린 경우 BitLocker 복구 콘솔에 복구 키를 입력 하 여 컴퓨터 잠금을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-132">If you forgot your PIN, enter the recovery key in the BitLocker Recovery console to unlock your computer.</span></span>

    -   <span data-ttu-id="1f14e-133">비밀 번호를 잊은 경우, BitLocker 암호화 옵션 제어판의 응용 프로그램에서 복구 키를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-133">If you forgot your password, enter the recovery key in the BitLocker Encryption Options Control Panel application, in the same location where you found the recovery key ID earlier.</span></span> <span data-ttu-id="1f14e-134">이렇게 하면 보호 된 하드 드라이브의 잠금이 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-134">This will unlock the protected hard drive.</span></span>

## <span data-ttu-id="1f14e-135">PIN 또는 비밀 번호 변경</span><span class="sxs-lookup"><span data-stu-id="1f14e-135">Changing your PIN or Password</span></span>


<span data-ttu-id="1f14e-136">BitLocker 보호 드라이브의 암호를 변경 하려면 먼저 드라이브의 잠금을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-136">Before you can change the password on a BitLocker protected drive, you must unlock the drive.</span></span> <span data-ttu-id="1f14e-137">드라이브가 잠기지 않은 경우 **드라이브 잠금 해제**를 선택한 다음 현재 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-137">If the drive is not unlocked, select **Unlock Drive**, and then enter your current password.</span></span> <span data-ttu-id="1f14e-138">드라이브 잠금이 해제 되는 즉시 **암호 관리** 를 선택 하 여 현재 암호를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-138">As soon as the drive is unlocked, you can select **Manage your Password** to change your current password.</span></span>

**<span data-ttu-id="1f14e-139">PIN 또는 암호를 변경 하는 방법</span><span class="sxs-lookup"><span data-stu-id="1f14e-139">How to Change your PIN or password</span></span>**

1.  <span data-ttu-id="1f14e-140">**시작**을 클릭 한 다음 **제어판**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-140">Click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="1f14e-141">새 창에서 제어판이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-141">Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="1f14e-142">**시스템 및 보안**을 선택한 다음 **BitLocker 암호화 옵션**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-142">Select **System and Security**, and then select **BitLocker Encryption Options**.</span></span>

    -   <span data-ttu-id="1f14e-143">PIN을 변경 하려면 **Pin 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-143">To change your PIN, select **Manage Your PIN**.</span></span> <span data-ttu-id="1f14e-144">두 필드에 새 PIN을 입력 하 고 **PIN 다시 설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-144">Type your new PIN into both fields and select **Reset PIN**.</span></span>

    -   <span data-ttu-id="1f14e-145">비밀 번호를 변경 하려면 **비밀 번호 관리**를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-145">To change your password, select **Manage Your Password**.</span></span> <span data-ttu-id="1f14e-146">두 필드에 새 비밀 번호를 입력 하 고 **암호 재설정**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f14e-146">Enter your new password into both fields and select **Reset Password**.</span></span>

 

 





