---
title: MBAM을 사용하여 BitLocker 관리 수행
description: MBAM을 사용하여 BitLocker 관리 수행
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826498"
---
# <span data-ttu-id="c001f-103">MBAM을 사용하여 BitLocker 관리 수행</span><span class="sxs-lookup"><span data-stu-id="c001f-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="c001f-104">Microsoft BitLocker 관리 및 모니터링 (MBAM)을 계획 하 고 배포한 후 엔터프라이즈 BitLocker 암호화를 관리 하는 데이를 구성 하 고 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="c001f-105">이 섹션의 정보는 Microsoft BitLocker 관리 및 모니터링을 사용 하 여 수행 되는 사후 설치 일일 BitLocker 암호화 관리 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="c001f-106">MBAM을 사용 하 여 TPM 잠금 다시 설정</span><span class="sxs-lookup"><span data-stu-id="c001f-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="c001f-107">TPM (신뢰할 수 있는 플랫폼 모듈)은 기본적으로 암호화 키를 포함 하는 기본 보안 관련 기능을 제공 하도록 설계 된 microchip입니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="c001f-108">일반적으로 TPM은 컴퓨터 또는 랩톱의 마더보드에 설치 되며 하드웨어 버스를 사용 하 여 시스템의 나머지 부분과 통신 합니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="c001f-109">TPM을 통합 하는 컴퓨터에는 암호화 키를 만들고이를 암호화 하 여 TPM 에서만 해독할 수 있도록 하는 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="c001f-110">사용자가 잘못 된 PIN을 너무 여러 번 입력 하는 경우 TPM 잠금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="c001f-111">TPM 잠금이 설정 되기 전에 사용자가 잘못 된 PIN을 입력할 수 있는 횟수는 제조업체 마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="c001f-112">컴퓨터 ID 및 연결 된 사용자 식별자를 제공할 때 TPM 소유자 암호 파일을 검색할 수 있는 관리 및 모니터링 웹 사이트에서 MBAM을 사용 하 여 중앙 집중화 된 키 복구 데이터 시스템에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="c001f-113">TPM 잠금을 다시 설정하는 방법</span><span class="sxs-lookup"><span data-stu-id="c001f-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="c001f-114">MBAM을 사용 하 여 드라이브 복구</span><span class="sxs-lookup"><span data-stu-id="c001f-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="c001f-115">특히 엔터프라이즈 환경에서 데이터 암호화를 처리 하는 경우 하드웨어 오류 발생 시 해당 데이터를 복구할 수 있는 방법, 인적 자원 변경 또는 암호화 키가 손실 될 수 있는 기타 상황을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="c001f-116">MBAM의 암호화 된 드라이브 복구 기능은 데이터를 캡처하고 저장할 수 있으며 BitLocker가 복구 모드로 전환 되거나 이동 되거나 손상 될 때 BitLocker로 보호 되는 볼륨에 액세스 하는 데 필요한 도구가 제공 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="c001f-117">복구 모드에서 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="c001f-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="c001f-118">이동된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="c001f-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="c001f-119">손상된 드라이브를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="c001f-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="c001f-120">MBAM을 사용 하 여 손실 된 컴퓨터의 BitLocker 암호화 상태 확인</span><span class="sxs-lookup"><span data-stu-id="c001f-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="c001f-121">MBAM을 사용 하면 분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="c001f-122">분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법</span><span class="sxs-lookup"><span data-stu-id="c001f-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="c001f-123">셀프 서비스 포털을 사용 하 여 컴퓨터에 다시 액세스</span><span class="sxs-lookup"><span data-stu-id="c001f-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="c001f-124">최종 사용자가 BitLocker로 Windows에서 잠긴 경우이 섹션의 지침에 따라 BitLocker 복구 키를 사용 하 여 컴퓨터에 대 한 액세스 권한을 다시 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c001f-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="c001f-125">셀프 서비스 포털을 사용하여 컴퓨터에 대한 액세스 권한을 다시 획득하는 방법</span><span class="sxs-lookup"><span data-stu-id="c001f-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="c001f-126">MBAM을 사용 하 여 BitLocker 관리를 수행 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="c001f-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="c001f-127">MBAM 2.0 작업</span><span class="sxs-lookup"><span data-stu-id="c001f-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





