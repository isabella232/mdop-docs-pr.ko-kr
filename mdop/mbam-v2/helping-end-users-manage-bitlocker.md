---
title: 최종 사용자의 BitLocker 관리 지원
description: 최종 사용자의 BitLocker 관리 지원
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824778"
---
# <span data-ttu-id="76745-103">최종 사용자의 BitLocker 관리 지원</span><span class="sxs-lookup"><span data-stu-id="76745-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="76745-104">분실 하거나 도난당 한 컴퓨터의 콘텐츠는 무단 액세스에 취약해 지 며 사용자와 회사 모두에 게 보안 위험을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="76745-105">Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker를 사용 하 여 악의적인 사용자 로부터 중요 한 데이터를 보호 하기 위해 컴퓨터를 잠가 무단 액세스를 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="76745-106">BitLocker 란?</span><span class="sxs-lookup"><span data-stu-id="76745-106">What is BitLocker?</span></span>


<span data-ttu-id="76745-107">BitLocker 드라이브 암호화는 드라이브를 암호화 하 여 운영 체제 드라이브, 데이터 드라이브 및 이동식 드라이브 (USB 엄지 드라이브 등)에 대 한 보호 기능을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="76745-108">BitLocker 구성 방법에 따라 사용자가 암호화 된 드라이브에 저장 된 정보를 잠금 해제 하는 키 (암호 또는 PIN)를 제공 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="76745-109">BitLocker를 사용 하 여 암호화 된 드라이브에 새 파일을 추가 하면 BitLocker는 자동으로 암호를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="76745-110">암호화 된 드라이브에 저장 된 파일은 암호화 된 상태로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76745-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="76745-111">다른 드라이브나 컴퓨터로 복사 되는 파일의 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="76745-112">네트워크 등의 다른 사용자와 파일을 공유 하는 경우 이러한 파일은 암호화 된 드라이브에 저장 되는 동안 암호화 되지만 권한이 있는 사용자가 일반적으로 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="76745-113">운영 체제 드라이브를 암호화 하는 경우 BitLocker는 시작 하는 동안 컴퓨터에 보안 위험 (예: BIOS 변경 또는 시작 파일 변경 등)을 나타낼 수 있는 조건을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="76745-114">잠재적인 보안 위험이 감지 되 면 BitLocker에서 운영 체제 드라이브를 잠그고, 잠금을 해제 하는 데 특별 한 BitLocker 복구 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="76745-115">BitLocker를 처음으로 켤 때이 복구 키를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="76745-116">그렇지 않으면 파일에 영구적으로 액세스할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76745-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="76745-117">데이터 드라이브 (수정 또는 이동식)를 암호화 하는 경우 암호 또는 스마트 카드를 사용 하 여 암호화 된 드라이브의 잠금을 해제 하거나 컴퓨터에 로그온 할 때 자동으로 잠금을 해제 하도록 드라이브를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="76745-118">BitLocker는 암호 및 Pin 외에도 많은 최신 컴퓨터에 제공 되는 TPM (신뢰할 수 있는 플랫폼 모듈) 칩셋을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="76745-119">TPM 칩은 BitLocker에서 운영 체제 드라이브의 잠금을 해제 하기 전에 컴퓨터가 훼손 되지 않았음을 확인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="76745-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="76745-120">암호화 프로세스가 진행 되는 동안 TPM 칩을 사용 하도록 설정 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="76745-121">컴퓨터를 시작 하면 BitLocker에서 해당 키에 대 한 TPM을 드라이브에 요청 하 고 잠금을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="76745-122">TPM 칩을 사용 하도록 설정 하려면 컴퓨터를 다시 시작한 다음 BIOS에서 컴퓨터 소프트웨어의 Windows 이전 계층으로 설정을 변경 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="76745-123">TPM에 대 한 자세한 내용은 [컴퓨터 TPM 칩 정보](about-the-computer-tpm-chip.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76745-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="76745-124">컴퓨터가 BitLocker로 보호 되는 경우 최대 절전 모드에서 절전 모드를 해제 하거나 시작할 때마다 PIN 또는 암호를 입력 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="76745-125">사용자의 PIN 이나 비밀 번호를 잊어버린 경우 회사나 조직의 지원 센터에 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="76745-126">BitLocker를 일시 중지 하거나 드라이브의 암호를 해독 하 여 일시적으로 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="76745-127">**참고**  BitLocker는 개별 파일 자체가 아니라 전체 드라이브를 암호화 하기 때문에 드라이브 간에 중요 한 데이터를 이동 하는 경우 주의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="76745-128">BitLocker 보호 드라이브에서 암호화 되지 않은 드라이브로 파일을 이동 하면 해당 파일이 더 이상 암호화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="76745-129">BitLocker 암호화 옵션 응용 프로그램 정보</span><span class="sxs-lookup"><span data-stu-id="76745-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="76745-130">컴퓨터에서 하드 디스크 드라이브의 잠금을 해제 하 고 PIN 및 암호를 관리 하려면 Windows 제어판의 BitLocker 암호화 옵션 응용 프로그램을 사용 하 여 여기에 설명 된 절차를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="76745-131">암호를 입력 하 여 보호 된 드라이브의 잠금을 해제 하 고이 응용 프로그램을 사용 하 여 연결 된 드라이브의 BitLocker 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="76745-132">BitLocker 암호화 옵션 응용 프로그램을 열려면</span><span class="sxs-lookup"><span data-stu-id="76745-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="76745-133">**시작**을 클릭 하 고 **제어판**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="76745-134">제어판이 새 창에서 열립니다.</span><span class="sxs-lookup"><span data-stu-id="76745-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="76745-135">**제어판**에서 **시스템 및 보안**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="76745-136">Bitlocker **암호화 옵션을 선택 하** 여 Bitlocker 암호화 옵션 응용 프로그램을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="76745-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="76745-137">사용할 수 있는 옵션에 대 한 설명은 다음 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76745-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="76745-138">BitLocker 암호화 옵션 응용 프로그램의 옵션</span><span class="sxs-lookup"><span data-stu-id="76745-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="76745-139">제어판의 BitLocker 암호화 옵션 응용 프로그램을 사용 하면 BitLocker에서 컴퓨터를 보호 하는 데 사용 하는 PIN 및 암호를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="76745-140">BitLocker 드라이브 암호화 – 고정 디스크 드라이브:</span><span class="sxs-lookup"><span data-stu-id="76745-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="76745-141">이 섹션에서는 컴퓨터에 연결 된 하드 디스크 드라이브와 현재 BitLocker 암호화 상태에 대 한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="76745-142">**PIN 관리** -BitLocker에서 사용 하는 pin이 변경 되어 운영 체제 드라이브의 잠금을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="76745-143">**비밀 번호 관리** -BitLocker에서 다른 내부 드라이브의 잠금을 해제 하는 데 사용 하는 암호를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="76745-144">BitLocker 드라이브 암호화-외부 드라이브:</span><span class="sxs-lookup"><span data-stu-id="76745-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="76745-145">이 섹션에서는 컴퓨터에 연결 된 외장 드라이브 (예: USB 엄지 드라이브)와 현재 BitLocker 암호화 상태에 대 한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="76745-146">**비밀 번호 관리** -BitLocker에서 다른 내부 드라이브의 잠금을 해제 하는 데 사용 하는 암호를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="76745-147">높은</span><span class="sxs-lookup"><span data-stu-id="76745-147">Advanced:</span></span>**

-   <span data-ttu-id="76745-148">**Tpm 관리** -tpm 관리 도구를 별도의 창에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="76745-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="76745-149">여기서는 일반적인 TPM 작업을 구성 하 고 TPM 칩셋에 대 한 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="76745-150">이 도구에 액세스 하려면 컴퓨터에 대 한 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="76745-151">**디스크 관리** -디스크 관리 도구를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="76745-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="76745-152">여기에서 컴퓨터에 연결 된 모든 하드 드라이브에 대 한 정보를 보고 파티션과 드라이브 옵션을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76745-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="76745-153">이 도구에 액세스 하려면 컴퓨터에 대 한 관리자 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76745-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





