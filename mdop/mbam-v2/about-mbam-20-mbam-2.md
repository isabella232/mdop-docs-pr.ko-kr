---
title: MBAM 2.0 정보
description: MBAM 2.0 정보
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824318"
---
# <span data-ttu-id="9f36b-103">MBAM 2.0 정보</span><span class="sxs-lookup"><span data-stu-id="9f36b-103">About MBAM 2.0</span></span>


<span data-ttu-id="9f36b-104">Microsoft BitLockerAdministration 및 모니터링 (MBAM) 2.0은 BitLocker 드라이브 암호화에 간소화 된 관리 인터페이스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface to BitLocker drive encryption.</span></span> <span data-ttu-id="9f36b-105">BitLocker는 분실 하거나 도난당 한 컴퓨터에 대 한 데이터 절도 또는 데이터 노출에 대 한 향상 된 보호 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="9f36b-106">BitLocker는 Windows 운영 체제 볼륨 및 구성 된 데이터 볼륨에 저장 되어 있는 모든 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-106">BitLocker encrypts all data that is stored on the Windows operating system volume and configured data volumes.</span></span>

## <span data-ttu-id="9f36b-107">MBAM 2.0 정보</span><span class="sxs-lookup"><span data-stu-id="9f36b-107">About MBAM2.0</span></span>


<span data-ttu-id="9f36b-108">BitLockerAdministration 및 모니터링 2.0은 사용자의 엔터프라이즈에 대해 설정한 BitLocker 암호화 정책 옵션을 적용 하 고, 해당 정책으로 클라이언트 컴퓨터의 준수 여부를 모니터링 하 고, 엔터프라이즈 및 개별 컴퓨터의 암호화 상태를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-108">BitLockerAdministration and Monitoring2.0 enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of both the enterprise and the individual computers.</span></span> <span data-ttu-id="9f36b-109">또한, MBAM은 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-109">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot record changes.</span></span>

<span data-ttu-id="9f36b-110">**참고**  BitLocker에 대 한 자세한 내용은이 가이드에서 설명 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-110">**Note** BitLocker is not covered in detail in this guide.</span></span> <span data-ttu-id="9f36b-111">BitLocker에 대 한 개요는 [Bitlocker 드라이브 암호화 개요](https://go.microsoft.com/fwlink/p/?LinkId=225013)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f36b-111">For an overview of BitLocker, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

<span data-ttu-id="9f36b-112">다음 그룹은 MBAM을 사용 하 여 BitLocker를 관리 하는 데 관심이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-112">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="9f36b-113">권한 부여 없이 기밀 데이터가 공개 되지 않는지 확인 하는 관리자, IT 보안 전문가 및 규정 준수 책임자</span><span class="sxs-lookup"><span data-stu-id="9f36b-113">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="9f36b-114">원격 또는 지사에서 컴퓨터 보안을 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="9f36b-114">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="9f36b-115">Windows를 실행 하는 클라이언트 컴퓨터를 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="9f36b-115">Administrators who are responsible for client computers that are running Windows</span></span>

## <a href="" id="what-s-new-in-mbam-2-0"></a><span data-ttu-id="9f36b-116">MBAM 2.0의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="9f36b-116">What’s New in MBAM2.0</span></span>


<span data-ttu-id="9f36b-117">MBAM 2.0은 다음과 같은 새로운 기능과 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-117">MBAM2.0 provides the following new features and functionality.</span></span>

### <span data-ttu-id="9f36b-118">시스템 센터 구성 관리자와 MBAM의 통합</span><span class="sxs-lookup"><span data-stu-id="9f36b-118">Integration of System Center Configuration Manager with MBAM</span></span>

<span data-ttu-id="9f36b-119">이제 MBAM은 System Center Configuration Manager와의 통합을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-119">MBAM now supports integration with System Center Configuration Manager.</span></span> <span data-ttu-id="9f36b-120">이 통합은 MBAM 준수 인프라를 구성 관리자의 기본 환경으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-120">This integration moves the MBAM compliance infrastructure into the native environment of Configuration Manager.</span></span> <span data-ttu-id="9f36b-121">엔터프라이즈에서 Configuration Manager를 사용 하는 IT 관리자는 이제 Microsoft Management Console에서 엔터프라이즈의 준수 상태를 보고, 보고서로 드릴 다운 하 여 개별 컴퓨터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-121">IT administrators who use Configuration Manager in their enterprise can now view the compliance status of their enterprise in the Microsoft Management Console and drill into reports to view individual computers.</span></span>

### <span data-ttu-id="9f36b-122">하드웨어 호환성은 Configuration Manager 통합 토폴로지에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-122">Hardware Compatibility is Available Only in the Configuration Manager Integration Topology</span></span>

<span data-ttu-id="9f36b-123">구성 관리자와 MBAM을 통합 하면 MBAM에서 특정 하드웨어 종류의 사용을 허용 하거나 금지 하 고 MBAM 1.0에서 제공 하는 하드웨어 호환성 보다 더 많은 유연성을 제공 하는 Configuration Manager 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-123">Integrating Configuration Manager with MBAM enables Configuration Manager capabilities that allow or prohibit the use of certain hardware types with MBAM and provides more flexibility than the hardware compatibility that was available in MBAM 1.0.</span></span> <span data-ttu-id="9f36b-124">IT 관리자는 고유한 컬렉션을 만들어 하드웨어를 제한 하 고 해당 컬렉션에 MBAM 구성 기준을 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-124">IT administrators can create their own collections to limit hardware and can deploy the MBAM configuration baseline to those collections.</span></span> <span data-ttu-id="9f36b-125">MBAM 1.0에 있는 MBAM 하드웨어 호환성은 이제 MBAM 구성 관리자 토폴로지에서만 사용할 수 있으며,이는 구성 관리자에서 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-125">The MBAM hardware compatibility that was present in MBAM 1.0 is now available only in the MBAM Configuration Manager topology and is administered from Configuration Manager.</span></span>

### <span data-ttu-id="9f36b-126">보호기 유연성 정책</span><span class="sxs-lookup"><span data-stu-id="9f36b-126">Protectors Flexible Policy</span></span>

<span data-ttu-id="9f36b-127">보호기 (예: TPM + PIN 또는 자동 잠금 해제 및 암호)를 사용 하 여 이미 암호화 된 컴퓨터와 해당 암호화의 하위 집합 (예: TPM 또는 자동 잠금 해제)이 필요한 MBAM 정책을 수신 하는 경우에는 규격으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-127">Computers that are already encrypted with a protector (for example, TPM + PIN or Auto-Unlock and password) and that receive an MBAM policy that requires a subset of that encryption (for example, TPM or Auto-Unlock) are considered compliant.</span></span> <span data-ttu-id="9f36b-128">위 예제에서는 IT 관리자가 이러한 기능을 더 이상 허용 되지 않는 것으로 특별히 정의 하지 않는 한, PIN 및 암호가 자동으로 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-128">In the example above, PIN and password would not be removed automatically unless the IT administrator specifically defines these features as no longer allowed.</span></span>

<span data-ttu-id="9f36b-129">암호화 되지 않고 MBAM 정책 (예: TPM 또는 자동 잠금 해제)을 수신 하는 컴퓨터는 적절 하 게 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-129">Computers that are not encrypted and that receive an MBAM policy (for example, TPM or Auto-Unlock) are encrypted accordingly.</span></span> <span data-ttu-id="9f36b-130">로컬 관리자 인 사용자는 BitLocker 도구 (제어판 항목 BitLocker 드라이브 암호화 또는 manage-bde)를 사용 하 여 기존 보호기를 추가 하거나 수정할 수 있습니다 (예: TPM + PIN 또는 자동 잠금 해제 및 암호).</span><span class="sxs-lookup"><span data-stu-id="9f36b-130">Users who are local administrators are allowed to use the BitLocker tools (Control Panel item BitLocker Drive Encryption or Manage-bde) to add or modify the existing protectors (for example, TPM + PIN or Auto-Unlock and password).</span></span> <span data-ttu-id="9f36b-131">MBAM 정책에서 구체적으로 정의 하지 않는 한 규격은 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-131">They remain compliant unless MBAM policies specifically define them.</span></span>

### <span data-ttu-id="9f36b-132">MBAM 클라이언트를 업그레이드 하는 기능</span><span class="sxs-lookup"><span data-stu-id="9f36b-132">Ability to Upgrade the MBAM Client</span></span>

<span data-ttu-id="9f36b-133">MBAM 2.0 클라이언트 Windows Installer는 기존 클라이언트 버전을 감지 하 고 이전 버전에서 MBAM 2.0 클라이언트로 업그레이드 하는 데 필요한 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-133">The MBAM2.0 Client Windows Installer detects the version of the existing client and performs the required steps to upgrade to the MBAM2.0 Client from previous versions.</span></span>

### <span data-ttu-id="9f36b-134">이전 버전에서 MBAM 서버를 업그레이드 하는 기능</span><span class="sxs-lookup"><span data-stu-id="9f36b-134">Ability to Upgrade the MBAM Server from Previous Versions</span></span>

<span data-ttu-id="9f36b-135">아래와 같이 이전 버전의 MBAM에서 MBAM 2.0 서버 인프라를 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-135">You can upgrade the MBAM2.0 Server infrastructure from previous versions of MBAM as follows:</span></span>

<span data-ttu-id="9f36b-136">**수동 현재 위치 서버 대체** – 기존 mbam 서버 인프라를 수동으로 제거한 다음 mbam 2.0 서버 인프라를 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-136">**Manual in-place server replacement** – You must manually uninstall the existing MBAM server infrastructure, and then install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="9f36b-137">업그레이드를 수행 하기 위해 데이터베이스를 제거할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-137">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="9f36b-138">대신, 이전 버전의 MBAM 클라이언트가 생성 하는 기존 데이터베이스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-138">Instead, you select the existing databases, which the previous version of the MBAM Client created.</span></span> <span data-ttu-id="9f36b-139">MBAM 2.0 업그레이드 설치는 기존 데이터베이스를 MBAM 2.0로 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-139">The MBAM2.0 upgrade installation then migrates the existing databases to MBAM 2.0.</span></span>

<span data-ttu-id="9f36b-140">**분산 클라이언트 업그레이드** -단독 mbam 토폴로지를 사용 하는 경우 mbam 2.0 서버 인프라를 설치한 후에 Mbam 클라이언트를 점차적으로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-140">**Distributed client upgrade** – If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="9f36b-141">MBAM 2.0 서버는 기존 클라이언트의 버전을 감지 하 고 2.0 클라이언트로 업그레이드 하는 데 필요한 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-141">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

<span data-ttu-id="9f36b-142">MBAM 2.0 서버 인프라를 업그레이드 한 후에는 mbam 1.0 클라이언트가 MBAM 2.0 서버에 성공적으로 보고 하지만 복구 데이터를 escrowing, 준수는 MBAM 1.0의 정책에 기반 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-142">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="9f36b-143">클라이언트 컴퓨터가 MBAM 2.0 정책에 대 한 준수를 정확 하 게 보고 하도록 클라이언트를 MBAM 2.0으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-143">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="9f36b-144">이전 클라이언트를 제거 하지 않고 MBAM 2.0 클라이언트로 클라이언트를 업그레이드 하면 클라이언트가 MBAM 2.0 정책을 적용 하 고 보고 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-144">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

<span data-ttu-id="9f36b-145">구성 관리자에서 MBAM을 사용 하는 경우 mbam 클라이언트를 MBAM 2.0으로 업그레이드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-145">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a><span data-ttu-id="9f36b-146">Windows 8 플랫폼에서의 BitLocker 엔터프라이즈 시나리오에 대 한 MBAM 지원</span><span class="sxs-lookup"><span data-stu-id="9f36b-146">MBAM Support for BitLocker’s Enterprise Scenarios on the Windows 8 Platform</span></span>

<span data-ttu-id="9f36b-147">MBAM 클라이언트 설치의 대상 플랫폼으로 Windows 8 운영 체제를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-147">MBAM supports the Windows 8 operating system as a target platform for the MBAM Client installation.</span></span> <span data-ttu-id="9f36b-148">이 지원으로 IT 관리자는 MBAM 에이전트를 설치 하 고, Windows 8 운영 체제 드라이브를 암호화 하 고, 컴퓨터를 준수 하는 데 보고할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-148">This support enables IT administrators to install the MBAM agent, to encrypt Windows 8 operating system drives, and to report on the compliance of the computers.</span></span> <span data-ttu-id="9f36b-149">MBAM은 Windows 7 운영 체제와 마찬가지로 Windows 8 운영 체제를 관리 하는 데 TPM 및 TPM + PIN 보호기를 활용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-149">MBAM leverages the TPM and TPM+PIN protectors to manage the Windows 8 operating system just as it does the Windows 7 operating system.</span></span> <span data-ttu-id="9f36b-150">또한 MBAM 2.0은 Windows To Go 클라이언트로의 암호화 지원도 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-150">MBAM2.0 also adds support for encrypting Windows To Go clients.</span></span>

### <span data-ttu-id="9f36b-151">셀프 서비스 포털 추가</span><span class="sxs-lookup"><span data-stu-id="9f36b-151">Addition of the Self-Service Portal</span></span>

<span data-ttu-id="9f36b-152">최종 사용자는 이제 셀프 서비스 포털을 사용 하 여 복구 키를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-152">End users can now use the Self-Service Portal to recover their recovery keys.</span></span> <span data-ttu-id="9f36b-153">셀프 서비스 포털은 다른 MBAM 기능을 사용 하 여 단일 서버에 배포 하거나, 필요한 경우 자체 서버 포털을 사용자에 게 제공할 수 있는 유연성을 IT 관리자에 게 제공 하는 별도의 서버에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-153">The Self-Service Portal can be deployed on a single server with the other MBAM features, or on a separate server that gives IT administrators the flexibility to expose the Self-Server Portal to users, as required.</span></span> <span data-ttu-id="9f36b-154">셀프 서비스 포털이 사용자를 인증 한 후에는 복구 키를 받을 수 있도록 복구 키 ID의 처음 여덟 자리만 입력 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-154">After the Self-Service Portal authenticates users, users have to enter only the first eight digits of the recovery key ID to receive their recovery key.</span></span>

<span data-ttu-id="9f36b-155">또한 MBAM은 사용자가 사용자 인 컴퓨터에 대 한 키만 복구할 수 있도록 하 여 다른 사용자가 무단으로 액세스 하는 위험을 줄여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-155">MBAM also secures the key by allowing users to recover keys only for those computers on which they are users, which reduces the risk that other users gain unauthorized access.</span></span>

### <span data-ttu-id="9f36b-156">일시 중단 상태에서 BitLocker 보호를 자동으로 다시 시작 하는 기능</span><span class="sxs-lookup"><span data-stu-id="9f36b-156">Ability to Automatically Resume BitLocker Protection from a Suspended State</span></span>

<span data-ttu-id="9f36b-157">MBAM은 더 이상 IT 관리자가 오랫동안 BitLocker를 일시 중단 상태로 유지할 수 있도록 허용 하지 않는 기간</span><span class="sxs-lookup"><span data-stu-id="9f36b-157">MBAM no longer allows IT administrators to keep BitLocker suspended and unprotected for prolonged periods of time.</span></span> <span data-ttu-id="9f36b-158">IT 관리자가 BitLocker를 일시 중지 하면 컴퓨터가 다시 부팅 될 때 자동으로 사용 하도록 설정 되므로 컴퓨터가 공격할 수 있는 위험이 줄어듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-158">If an IT administrator suspends BitLocker, MBAM re-enables it automatically when the computer is rebooted, which reduces the risk that the computer can be attacked.</span></span>

### <span data-ttu-id="9f36b-159">암호 없이 자동으로 잠금을 해제 하도록 고정 데이터 드라이브를 구성할 수 있음</span><span class="sxs-lookup"><span data-stu-id="9f36b-159">Fixed Data Drives Can Be Configured to Automatically Unlock Without a Password</span></span>

<span data-ttu-id="9f36b-160">이제 암호 없이 드라이브의 자동 잠금 해제를 허용 하도록 FDD (고정 데이터 드라이브) 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-160">A Fixed Data Drive (FDD) policy can now be configured to allow automatic unlocking of the drive without a password.</span></span> <span data-ttu-id="9f36b-161">FDD를 암호화 하기 전에 사용자에 게 암호를 입력 하 라는 메시지가 표시 되지 않으며, FDD는 운영 체제 드라이브를 사용 하 여 자동으로 잠금 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-161">Users are not prompted for a password before the FDD is encrypted, and the FDD will be secured and auto-unlocked with the operating system drive.</span></span>

## <a href="" id="---------mbam-2-0-release-notes"></a> <span data-ttu-id="9f36b-162">MBAM 2.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="9f36b-162">MBAM2.0 Release Notes</span></span>


<span data-ttu-id="9f36b-163">설명서에 포함 되어 있지 않은 최신 뉴스 및 자세한 내용은 [MBAM 2.0 릴리스 정보](release-notes-for-mbam-20-mbam-2.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f36b-163">For more information, and for late-breaking news that is not included in the documentation, see the [Release Notes for MBAM 2.0](release-notes-for-mbam-20-mbam-2.md).</span></span>

## <span data-ttu-id="9f36b-164">MBAM 2.0을 얻는 방법</span><span class="sxs-lookup"><span data-stu-id="9f36b-164">How to Get MBAM2.0</span></span>


<span data-ttu-id="9f36b-165">이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-165">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="9f36b-166">엔터프라이즈 고객은 Microsoft 소프트웨어 보증을 통해 MDOP를 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f36b-166">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="9f36b-167">Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/p/?LinkId=322049) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f36b-167">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)</span></span>

## <span data-ttu-id="9f36b-168">관련 항목</span><span class="sxs-lookup"><span data-stu-id="9f36b-168">Related topics</span></span>


[<span data-ttu-id="9f36b-169">MBAM 2.0 시작</span><span class="sxs-lookup"><span data-stu-id="9f36b-169">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





