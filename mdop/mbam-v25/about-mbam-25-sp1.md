---
title: MBAM 2.5 SP1 정보
description: MBAM 2.5 SP1 정보
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823783"
---
# <span data-ttu-id="bc592-103">MBAM 2.5 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="bc592-103">About MBAM 2.5 SP1</span></span>


<span data-ttu-id="bc592-104">MBAM 2.5 SP1은 BitLocker 드라이브 암호화를 위한 간단한 관리 인터페이스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-104">MBAM 2.5 SP1 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="bc592-105">BitLocker는 분실 하거나 도난당 한 컴퓨터에 대 한 데이터 절도 또는 데이터 노출에 대 한 향상 된 보호 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="bc592-106">BitLocker는 Windows 운영 체제 및 드라이브 및 구성 된 데이터 드라이브에 저장 된 모든 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-106">BitLocker encrypts all data that is stored on the Windows operating system and drives and configured data drives.</span></span>

## <span data-ttu-id="bc592-107">MBAM 개요</span><span class="sxs-lookup"><span data-stu-id="bc592-107">Overview of MBAM</span></span>


<span data-ttu-id="bc592-108">MBAM 2.5 SP1에는 다음과 같은 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-108">MBAM 2.5 SP1 has the following features:</span></span>

-   <span data-ttu-id="bc592-109">관리자가 엔터프라이즈 전체의 클라이언트 컴퓨터에서 볼륨을 암호화 하는 프로세스를 자동화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="bc592-110">보안 관리자가 개별 컴퓨터 또는 엔터프라이즈 자체의 준수 상태를 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="bc592-111">Microsoft System Center Configuration Manager를 사용 하 여 중앙 집중식 보고 및 하드웨어 관리를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="bc592-112">최종 사용자에 게 BitLocker PIN 및 복구 키 요청을 지원 하기 위해 지원 센터의 작업량을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="bc592-113">셀프 서비스 포털을 사용 하 여 최종 사용자가 암호화 된 장치를 별도로 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="bc592-114">보안 책임자가 키 정보 복구에 대 한 액세스를 쉽게 감사할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="bc592-115">Windows Enterprise 사용자가 회사 데이터를 보호 한다는 보장으로 어디서 나 계속 작업 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="bc592-116">MBAM은 엔터프라이즈에 대해 설정한 BitLocker 암호화 정책 옵션을 적용 하 고, 해당 정책으로 클라이언트 컴퓨터의 준수 여부를 모니터링 하 고, 엔터프라이즈 및 개인 컴퓨터의 암호화 상태를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="bc592-117">또한, MBAM은 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="bc592-118">다음 그룹은 MBAM을 사용 하 여 BitLocker를 관리 하는 데 관심이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="bc592-119">권한 부여 없이 기밀 데이터가 공개 되지 않는지 확인 하는 관리자, IT 보안 전문가 및 규정 준수 책임자</span><span class="sxs-lookup"><span data-stu-id="bc592-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="bc592-120">원격 또는 지사에서 컴퓨터 보안을 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="bc592-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="bc592-121">Windows를 실행 하는 클라이언트 컴퓨터를 담당 하는 관리자</span><span class="sxs-lookup"><span data-stu-id="bc592-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="bc592-122">**참고**  이 MBAM 설명서에는 BitLocker에 대해 자세히 설명 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="bc592-123">자세한 내용은 [BitLocker 드라이브 암호화 개요](https://go.microsoft.com/fwlink/p/?LinkId=225013)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a><span data-ttu-id="bc592-124">MBAM 2.5 SP1의 새로운 기능</span><span class="sxs-lookup"><span data-stu-id="bc592-124">What’s new in MBAM 2.5 SP1</span></span>


<span data-ttu-id="bc592-125">이 섹션에서는 MBAM 2.5 SP1의 새로운 기능에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-125">This section describes the new features in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="bc592-126">MBAM 2.5 SP1 클라이언트에 대해 새로 지원 되는 언어</span><span class="sxs-lookup"><span data-stu-id="bc592-126">Newly Supported Languages for the MBAM 2.5 SP1 Client</span></span>

<span data-ttu-id="bc592-127">다음 추가 언어는 MBAM 2.5 SP1에서 셀프 서비스 포털을 포함 하 여이 클라이언트에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-127">The following additional languages are now supported in MBAM 2.5 SP1 for the MBAM Client only, including the Self-Service Portal:</span></span>

<span data-ttu-id="bc592-128">체코어 (체코 공화국) cs-CZ</span><span class="sxs-lookup"><span data-stu-id="bc592-128">Czech (Czech Republic) cs-CZ</span></span>

<span data-ttu-id="bc592-129">덴마크어 (덴마크) da-진한</span><span class="sxs-lookup"><span data-stu-id="bc592-129">Danish (Denmark) da-DK</span></span>

<span data-ttu-id="bc592-130">네덜란드어 (네덜란드) nl-NL</span><span class="sxs-lookup"><span data-stu-id="bc592-130">Dutch (Netherlands) nl-NL</span></span>

<span data-ttu-id="bc592-131">핀란드어 (핀란드) fi</span><span class="sxs-lookup"><span data-stu-id="bc592-131">Finnish (Finland) fi-FI</span></span>

<span data-ttu-id="bc592-132">그리스어 (그리스) el-GR</span><span class="sxs-lookup"><span data-stu-id="bc592-132">Greek (Greece) el-GR</span></span>

<span data-ttu-id="bc592-133">헝가리어 (헝가리) hu-hu&platform-HU-HU&PLATFORM</span><span class="sxs-lookup"><span data-stu-id="bc592-133">Hungarian (Hungary) hu-HU</span></span>

<span data-ttu-id="bc592-134">노르웨이어, 복말 (노르웨이) nb-아니요</span><span class="sxs-lookup"><span data-stu-id="bc592-134">Norwegian, Bokmål (Norway) nb-NO</span></span>

<span data-ttu-id="bc592-135">폴란드어 (폴란드) pl-PL</span><span class="sxs-lookup"><span data-stu-id="bc592-135">Polish (Poland) pl-PL</span></span>

<span data-ttu-id="bc592-136">포르투갈어 (포르투갈) pt-PT</span><span class="sxs-lookup"><span data-stu-id="bc592-136">Portuguese (Portugal) pt-PT</span></span>

<span data-ttu-id="bc592-137">슬로바키아어 (슬로바키아) a/.</span><span class="sxs-lookup"><span data-stu-id="bc592-137">Slovak (Slovakia) sk-SK</span></span>

<span data-ttu-id="bc592-138">슬로베니아어 (슬로베니아) sl-SI</span><span class="sxs-lookup"><span data-stu-id="bc592-138">Slovenian (Slovenia) sl-SI</span></span>

<span data-ttu-id="bc592-139">스웨덴 (스웨덴) sv-SE</span><span class="sxs-lookup"><span data-stu-id="bc592-139">Swedish (Sweden) sv-SE</span></span>

<span data-ttu-id="bc592-140">터키어 (터키) tr-TR</span><span class="sxs-lookup"><span data-stu-id="bc592-140">Turkish (Turkey) tr-TR</span></span>

<span data-ttu-id="bc592-141">MBAM 2.5 및 MBAM 2.5 SP1의 클라이언트 및 서버에 대해 지원 되는 모든 언어 목록은 [mbam 2.5 지원 되는 구성을](mbam-25-supported-configurations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-141">For a list of all languages supported for client and server in MBAM 2.5 and MBAM 2.5 SP1, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

### <span data-ttu-id="bc592-142">Windows 10 지원</span><span class="sxs-lookup"><span data-stu-id="bc592-142">Support for Windows 10</span></span>

<span data-ttu-id="bc592-143">MBAM 2.5 SP1은 이전 버전의 MBAM에서 지원 되는 소프트웨어 외에도 Windows 10 및 Windows Server 2016에 대 한 지원을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-143">MBAM 2.5 SP1 adds support for Windows 10 and Windows Server 2016, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

<span data-ttu-id="bc592-144">Windows 10은 MBAM 2.5 및 MBAM 2.5 SP1 모두에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-144">Windows 10 is supported in both MBAM 2.5 and MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="bc592-145">Microsoft SQL Server 2014 SP1에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="bc592-145">Support for Microsoft SQL Server 2014 SP1</span></span>

<span data-ttu-id="bc592-146">MBAM 2.5 SP1에는 이전 버전의 MBAM에서 지원 되는 소프트웨어와 함께 Microsoft SQL Server 2014 SP1에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-146">MBAM 2.5 SP1 adds support for Microsoft SQL Server 2014 SP1, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <span data-ttu-id="bc592-147">MBAM은 더 이상 별도의 MSI와 함께 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-147">MBAM no longer ships with separate MSI</span></span>

<span data-ttu-id="bc592-148">MBAM 2.5 SP1 부터는 별도의 MSI가 MBAM 제품에 더 이상 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-148">Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="bc592-149">그러나 제품에 포함 된 실행 파일 (.exe)에서 MSI를 추출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-149">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

### <span data-ttu-id="bc592-150">MBAM은 TPM을 소유 하지 않고 정식 암호를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-150">MBAM can escrow OwnerAuth passwords without owning the TPM</span></span>

<span data-ttu-id="bc592-151">이전에는 MBAM이 TPM을 소유 하지 않은 경우 TPM 소유자 Auth를 MBAM 데이터베이스에 escrowed 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-151">Previously, if MBAM did not own the TPM, the TPM OwnerAuth could not be escrowed to the MBAM database.</span></span> <span data-ttu-id="bc592-152">TPM을 소유 하 고 암호를 저장 하도록 MBAM을 구성 하려면 TPM 자동 프로비저닝 기능을 사용 하지 않도록 설정 하 고 클라이언트 컴퓨터에서 TPM을 지워야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-152">To configure MBAM to own the TPM and to store the passwords, you had to disable TPM auto-provisioning and clear the TPM on the client computer.</span></span>

<span data-ttu-id="bc592-153">Windows 8 이상에서 MBAM 2.5 SP1은 이제 TPM을 소유 하지 않고 소유자 인증 암호를 에스크로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-153">In Windows 8 and higher, MBAM 2.5 SP1 can now escrow the OwnerAuth passwords without owning the TPM.</span></span> <span data-ttu-id="bc592-154">서비스를 시작 하는 동안 MBAM은 TPM이 이미 소유 되어 있는지 확인 하 고, 있다면 운영 체제에서 암호를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-154">During service startup, MBAM queries to see if the TPM is already owned and if so, it requests the passwords from the operating system.</span></span> <span data-ttu-id="bc592-155">그런 다음 MBAM 데이터베이스로 비밀 번호를 escrowed.</span><span class="sxs-lookup"><span data-stu-id="bc592-155">The passwords are then escrowed to the MBAM database.</span></span> <span data-ttu-id="bc592-156">또한 소유자 인증이 로컬로 삭제 되지 않도록 그룹 정책을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-156">In addition, Group Policy must be set to prevent the OwnerAuth from being deleted locally.</span></span>

<span data-ttu-id="bc592-157">Windows 7에서 MBAM은 MBAM 데이터베이스에서 자동으로 TPM 소유자 인증 정보를 받아야 하는 TPM을 소유 하 고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-157">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="bc592-158">MBAM이 TPM을 소유 하지 않거나 TPM의 AD (Active Directory) 백업이 그룹 정책을 통해 구성 되어 있으면 **Mbam directory (ad) 데이터 가져오기 cmdlet** 을 사용 하 여 AD에서 mbam 데이터베이스로 TPM 소유자 인증을 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-158">If MBAM does not own the TPM and Active Directory (AD) backup of the TPM is configured through Group Policy, you must use the **MBAM Active Directory (AD) Data Import cmdlets** to copy TPM OwnerAuth from AD into the MBAM database.</span></span> <span data-ttu-id="bc592-159">Active Directory에 저장 된 볼륨 복구 및 TPM 소유자 정보를 사용 하 여 MBAM 데이터베이스를 미리 채우는 5 개의 새 PowerShell cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-159">These are five new PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="bc592-160">자세한 내용은 [Mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-tpm)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-160">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

### <span data-ttu-id="bc592-161">MBAM은 잠금 이후 TPM을 자동으로 잠금 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-161">MBAM can automatically unlock the TPM after a lockout</span></span>

<span data-ttu-id="bc592-162">TPM 1.2를 실행 하는 컴퓨터에서 잠금을 설정 하는 경우 TPM을 자동으로 잠금 해제 하도록 MBAM을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-162">On computers running TPM 1.2, you can now configure MBAM to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="bc592-163">TPM 잠금 자동 재설정 기능을 사용 하도록 설정한 경우 MBAM은 사용자가 잠겨 있음을 감지 하 고 MBAM 데이터베이스에서 소유자 인증 암호를 받아 사용자의 TPM을 자동으로 잠금 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-163">If the TPM lockout auto reset feature is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span>

<span data-ttu-id="bc592-164">이 기능은 클라이언트 쪽의 서버 쪽 및 그룹 정책 모두에서 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-164">This feature must be enabled on both the server side and in Group Policy on the client side.</span></span> <span data-ttu-id="bc592-165">자세한 내용은 [Mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-autounlock)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-165">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-autounlock).</span></span>

### <span data-ttu-id="bc592-166">FIPS 규격 BitLocker 숫자 암호 보호기에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="bc592-166">Support for FIPS-compliant BitLocker numerical password protectors</span></span>

<span data-ttu-id="bc592-167">MBAM 2.5에서는 Windows 8.1 운영 체제를 실행 하는 디바이스의 FIPS (연방 정보 처리 표준) 규격 BitLocker 복구 키에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-167">In MBAM2.5, support was added for Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices running the Windows 8.1 operating system.</span></span> <span data-ttu-id="bc592-168">그러나 windows 7에서 FIPS 규격 복구 키를 구현 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-168">However, Windows did not implement FIPS-compliant recovery keys in Windows 7.</span></span> <span data-ttu-id="bc592-169">따라서 Windows 7 및 Windows 8 장치에는 복구를 위한 DRA (데이터 복구 에이전트) 보호기가 계속 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-169">Therefore, Windows 7 and Windows 8 devices still required a Data Recovery Agent (DRA) protector for recovery.</span></span>

<span data-ttu-id="bc592-170">Windows 팀에는 핫픽스가 포함 된 FIPS 호환 복구 키가 포함 되어 있으며, MBAM 2.5 SP1에도이에 대 한 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-170">The Windows team has backported FIPS-compliant recovery keys with a hotfix, and MBAM 2.5 SP1 has added support for them as well.</span></span>

<span data-ttu-id="bc592-171">**참고**  Windows8 운영 체제를 실행 하는 클라이언트 컴퓨터는 해당 OS에 핫픽스를 백 이식할 수 없기 때문에 DRA 보호기가 여전히 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-171">**Note** Client computers that are running the Windows8 operating system still require a DRA protector since the hotfix was not backported to that OS.</span></span> <span data-ttu-id="bc592-172">Windows 7 및 Windows 8 컴퓨터용 BitLocker 핫픽스를 다운로드 하 고 설치 하려면 [Bitlocker 관리 및 모니터링 2.5에 대 한 핫픽스 패키지 2](https://support.microsoft.com/kb/3015477) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-172">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span> <span data-ttu-id="bc592-173">DRA에 대 한 자세한 내용은 [BitLocker를 사용 하 여 데이터 복구 에이전트 사용](https://go.microsoft.com/fwlink/?LinkId=393557)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-173">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

 

<span data-ttu-id="bc592-174">조직에서 FIPS 준수를 사용 하도록 설정 하려면 연방 정보 처리 표준 (FIPS) 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-174">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="bc592-175">구성 방법에 대 한 자세한 내용은 [BitLocker 그룹 정책 설정을](https://go.microsoft.com/fwlink/?LinkId=393560)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-175">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

### <span data-ttu-id="bc592-176">새 그룹 정책 설정을 사용 하 여 사전 부팅 복구 메시지 및 URL 사용자 지정</span><span class="sxs-lookup"><span data-stu-id="bc592-176">Customize pre-boot recovery message and URL with new Group Policy setting</span></span>

<span data-ttu-id="bc592-177">새로운 그룹 정책 설정, **사전 부팅 복구 메시지 및 url을 구성**하면 OS 드라이브가 잠길 때 사전 부팅 BitLocker 복구 화면에 표시 되는 URL을 지정 하거나 사용자 지정 복구 메시지를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-177">A new Group Policy setting, **Configure pre-boot recovery message and URL**, lets you configure a custom recovery message or specify a URL that is then displayed on the pre-boot BitLocker recovery screen when the OS drive is locked.</span></span> <span data-ttu-id="bc592-178">이 설정은 Windows 10을 실행 하는 클라이언트 컴퓨터 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-178">This setting is only available on client computers running Windows 10.</span></span>

<span data-ttu-id="bc592-179">이 정책 설정을 사용 하도록 설정 하는 경우 사전 부팅 복구 메시지에 대해 다음 옵션 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-179">If you enable this policy setting, you can you can select one of these options for the pre-boot recovery message:</span></span>

-   <span data-ttu-id="bc592-180">**사용자 지정 복구 메시지 사용**: 사전 부팅 BitLocker 복구 화면에 사용자 지정 메시지를 포함 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-180">**Use custom recovery message**: Select this option to include a custom message in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="bc592-181">**사용자 지정 복구 URL 사용**: 사전 부팅 BitLocker 복구 화면에 표시 되는 기본 URL을 바꾸려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-181">**Use custom recovery URL**: Select this option to replace the default URL that is displayed in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="bc592-182">**기본 복구 메시지 및 Url 사용**: 사전 부팅 BitLocker 복구 화면에 기본 BitLocker 복구 메시지 및 url을 표시 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-182">**Use default recovery message and URL**: Select this option to display the default BitLocker recovery message and URL in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="bc592-183">이전에 사용자 지정 복구 메시지 또는 URL을 구성한 경우 기본 메시지로 돌아가려면이 정책을 사용 하도록 설정 하 고이 옵션을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-183">If you previously configured a custom recovery message or URL and want to revert to the default message, you must enable this policy and select this option.</span></span>

<span data-ttu-id="bc592-184">새 그룹 정책 설정은 다음 GPO 노드에 있습니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **운영 체제 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="bc592-184">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Operating System Drive**.</span></span> <span data-ttu-id="bc592-185">자세한 내용은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-185">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="bc592-186">사용 된 공간 암호화에 대 한 MBAM 추가 지원</span><span class="sxs-lookup"><span data-stu-id="bc592-186">MBAM added support for Used Space Encryption</span></span>

<span data-ttu-id="bc592-187">MBAM 2.5 SP1에서 BitLocker 그룹 정책을 통해 사용 하는 공간 암호화를 사용 하도록 설정 하면 MBAM 클라이언트가이를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-187">In MBAM 2.5 SP1, if you enable Used Space Encryption via BitLocker Group Policy, the MBAM Client honors it.</span></span>

<span data-ttu-id="bc592-188">이 그룹 정책 설정을 **운영 체제 드라이브에 드라이브 암호화 유형 강제 적용** 이라고 하며, **컴퓨터 구성** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **BitLocker 드라이브 암호화** &gt; **운영 체제 드라이브**에는 다음과 같은 GPO 노드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-188">This Group Policy setting is called **Enforce drive encryption type on operating system drives** and is located in the following GPO node: **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **Operating System Drives**.</span></span> <span data-ttu-id="bc592-189">이 정책을 사용 하 고 **사용 된 공간만 암호화**로 암호화 유형을 선택 하는 경우, mbam은 정책을 인식 하 고 BitLocker는 볼륨에 사용 되는 디스크 공간만 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-189">If you enable this policy and select the encryption type as **Used Space Only encryption**, MBAM will honor the policy and BitLocker will only encrypt disk space that is used on the volume.</span></span>

<span data-ttu-id="bc592-190">자세한 내용은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-190">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="bc592-191">암호화 된 하드 드라이브에 대 한 MBAM 클라이언트 지원</span><span class="sxs-lookup"><span data-stu-id="bc592-191">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="bc592-192">MBAM은 오 팔에 대 한 TCG 사양 요구 사항 및 IEEE 1667 표준을 충족 하는 암호화 된 하드 드라이브에서 BitLocker를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-192">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="bc592-193">이러한 디바이스에서 BitLocker를 사용 하도록 설정 하면 암호화 된 드라이브에서 키를 생성 하 고 관리 기능을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-193">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="bc592-194">자세한 내용은 [암호화 된 하드 드라이브](https://technet.microsoft.com/library/hh831627.aspx) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-194">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

### <span data-ttu-id="bc592-195">Spn을 등록할 때 더 이상 위임 구성이 필요 하지 않음</span><span class="sxs-lookup"><span data-stu-id="bc592-195">Delegation configuration no longer required when registering SPNs</span></span>

<span data-ttu-id="bc592-196">MBAM 2.5 SP1에서는 응용 프로그램 풀 계정에 대해 등록 하는 Spn에 대해 제한 위임을 구성 하는 요구 사항이 더 이상 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-196">The requirement to configure constrained delegation for SPNs that you register for the application pool account is no longer necessary in MBAM 2.5 SP1.</span></span> <span data-ttu-id="bc592-197">그러나이는 여전히 MBAM 2.5에 대 한 요구 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-197">However, it is still a requirement for MBAM 2.5.</span></span>

### <span data-ttu-id="bc592-198">Windows 배포의 일부로 MBAM을 사용 하 여 BitLocker 사용</span><span class="sxs-lookup"><span data-stu-id="bc592-198">Enable BitLocker using MBAM as Part of a Windows Deployment</span></span>

<span data-ttu-id="bc592-199">MBAM 2.5 SP1에서는 PowerShell 스크립트를 사용 하 여 BitLocker 드라이브 암호화 및 에스크로 복구 키를 MBAM 서버에 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-199">In MBAM 2.5 SP1, you can use a PowerShell script to configure BitLocker drive encryption and escrow recovery keys to the MBAM Server.</span></span>

<span data-ttu-id="bc592-200">자세한 내용은 [Windows 배포의 일부로 MBAM을 사용 하 여 BitLocker를 사용 하도록 설정 하는 방법](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-200">For more information, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span></span>

### <span data-ttu-id="bc592-201">PowerShell 또는 SSP 사용자 지정 마법사를 사용 하 여 셀프 서비스 포털을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-201">Self-Service Portal can be customized by using either PowerShell or the SSP customization wizard</span></span>

<span data-ttu-id="bc592-202">MBAM 2.5 SP1의 경우 PowerShell을 사용 하는 것 외에도 사용자 지정 마법사를 사용 하 여 셀프 서비스 포털을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-202">As of MBAM 2.5 SP1, the Self-Service Portal can be configured by using the customization wizard as well as by using PowerShell.</span></span> <span data-ttu-id="bc592-203">[MBAM 2.5 웹 응용 프로그램을 구성 하는 방법을](how-to-configure-the-mbam-25-web-applications.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-203">See [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

### <span data-ttu-id="bc592-204">웹 브라우저가 더 이상 관리자 권한으로 실행 되지 않음</span><span class="sxs-lookup"><span data-stu-id="bc592-204">Web browser no longer unintentionally runs as administrator</span></span>

<span data-ttu-id="bc592-205">MBAM 2.5의 문제는 서버 구성 도구에 대 한 도움말 링크를 통해 브라우저 창이 관리자 권한으로 열리도록 하는 데 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-205">An issue in MBAM 2.5 caused help links in the Server Configuration tool to cause browser windows to open with administrator rights.</span></span> <span data-ttu-id="bc592-206">이 문제는 MBAM 2.5 SP1에서 해결 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-206">This issue is fixed in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="bc592-207">CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하기 위해 더 이상 JavaScript 파일을 다운로드할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-207">No longer need to download the JavaScript files to configure the Self-Service Portal when the CDN is inaccessible</span></span>

<span data-ttu-id="bc592-208">MBAM 2.5이 하에서 셀프 서비스 포털에 액세스 하는 클라이언트가 인터넷에 액세스할 수 없는 경우 셀프 서비스 포털의 구성에 사용 되는 jQuery 파일을 미리 CDN에서 다운로드 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-208">In MBAM 2.5 and earlier, the jQuery files used for configuration of the Self-Service Portal had to be downloaded from the CDN in advance if clients accessing the Self-Service Portal did not have internet access.</span></span> <span data-ttu-id="bc592-209">MBAM 2.5 SP1에서는 모든 JavaScript 파일이 제품에 포함 되어 있으므로 다운로드할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-209">In MBAM 2.5 SP1, all JavaScript files are included in the product, so downloading them is unnecessary.</span></span>

### <span data-ttu-id="bc592-210">보고서 작성기 3.0에서 보고서를 열 수 있음</span><span class="sxs-lookup"><span data-stu-id="bc592-210">Reports can be opened in Report Builder 3.0</span></span>

<span data-ttu-id="bc592-211">MBAM 2.5 SP1에서는 보고서를 최신 보고서 정의 언어 스키마로 업데이트 하 여 사용자가 보고서 작성기 3.0에서 보고서를 열고 사용자 지정 하 고 보고서 파일을 손상 시 키 지 않고 즉시 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-211">In MBAM 2.5 SP1, the reports have been updated to the latest report definition language schema, allowing users to open and customize the reports in Report Builder 3.0 and save them immediately without corrupting the report file.</span></span>

### <span data-ttu-id="bc592-212">새 PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="bc592-212">New PowerShell cmdlets</span></span>

<span data-ttu-id="bc592-213">MBAM 2.5 SP1 용 새 PowerShell cmdlet을 사용 하면 데이터베이스, 보고서, 웹 응용 프로그램을 비롯 한 다양 한 MBAM 기능을 구성 하 고 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-213">New PowerShell cmdlets for MBAM 2.5 SP1 enable you to configure and manage different MBAM features, including databases, reports, and web applications.</span></span> <span data-ttu-id="bc592-214">각 기능에는 기능을 사용 하거나 사용 하지 않도록 설정 하거나 기능에 대 한 정보를 가져오는 데 사용할 수 있는 해당 PowerShell cmdlet이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-214">Each feature has a corresponding PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="bc592-215">MBAM 2.5 SP1에 대해 다음 cmdlet이 구현 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-215">The following cmdlets have been implemented for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="bc592-216">읽기-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="bc592-216">Write-MbamTpmInformation</span></span>

-   <span data-ttu-id="bc592-217">읽기-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="bc592-217">Write-MbamRecoveryInformation</span></span>

-   <span data-ttu-id="bc592-218">읽기-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="bc592-218">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="bc592-219">읽기-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="bc592-219">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="bc592-220">쓰기-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="bc592-220">Write-MbamComputerUser</span></span>

<span data-ttu-id="bc592-221">MBAM 2.5 SP1 용 Enable-MbamWebApplication 및 Test-MbamWebApplication cmdlet에 다음 매개 변수가 구현 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-221">The following parameters have been implemented in the Enable-MbamWebApplication and Test-MbamWebApplication cmdlets for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="bc592-222">DataMigrationAccessGroup</span><span class="sxs-lookup"><span data-stu-id="bc592-222">DataMigrationAccessGroup</span></span>

-   <span data-ttu-id="bc592-223">TpmAutoUnlock</span><span class="sxs-lookup"><span data-stu-id="bc592-223">TpmAutoUnlock</span></span>

<span data-ttu-id="bc592-224">Cmdlet에 대 한 자세한 내용은 [Mbam 2.5 보안 고려 사항](mbam-25-security-considerations.md) 및 [Microsoft Bitlocker 관리 및 모니터링 Cmdlet 도움말](https://technet.microsoft.com/library/dn720418.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-224">For information about the cmdlets, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md) and [Microsoft Bitlocker Administration and Monitoring Cmdlet Help](https://technet.microsoft.com/library/dn720418.aspx).</span></span>

### <span data-ttu-id="bc592-225">MBAM 에이전트는 프레젠테이션 모드를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-225">MBAM agent detects presentation mode</span></span>

<span data-ttu-id="bc592-226">MBAM 에이전트는 컴퓨터가 프레젠테이션 모드에 있을 때 검색 하 고 해당 시간에 MBAM UI를 호출 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-226">The MBAM agent can detect when the computer is in presentation mode and avoid invoking the MBAM UI at that time.</span></span>

### <span data-ttu-id="bc592-227">현재 MBAM 에이전트 서비스가 지연 된 시작을 사용 하도록 구성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-227">MBAM agent service now configured to use delayed start</span></span>

<span data-ttu-id="bc592-228">설치 후 서비스는 이제 Windows를 시작 하는 데 걸리는 시간을 줄임으로써 MBAM 에이전트 서비스를 지연 시작을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-228">After installation, the service will now set the MBAM agent service to use delayed start, decreasing the amount of time it takes to start Windows.</span></span>

### <span data-ttu-id="bc592-229">잠긴 고정 데이터 볼륨이 이제 규격으로 보고 됨</span><span class="sxs-lookup"><span data-stu-id="bc592-229">Locked Fixed Data volumes now report as Compliant</span></span>

<span data-ttu-id="bc592-230">"잠긴 고정 데이터" 볼륨에 대 한 규정 준수 계산 논리가 변경 되어 볼륨을 "규격"으로 보고 하지만, "알 수 없음"의 보호 상태와 "볼륨 잠김"의 준수 상태 세부 정보를 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="bc592-230">The compliance calculation logic for "Locked Fixed Data" volumes has been changed to report the volumes as "Compliant," but with a Protector State and Encryption State of "Unknown" and with a Compliance Status Detail of "Volume is locked".</span></span> <span data-ttu-id="bc592-231">이전에는 잠긴 볼륨이 "비규격", "암호화 됨"의 프로텍터 상태, "알 수 없음"의 암호화 상태, "알 수 없는 오류"에 대 한 준수 상태 세부 정보로 보고 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-231">Previously, locked volumes were reported as “Non-Compliant”, a Protector State of "Encrypted", an Encryption State of "Unknown", and a Compliance Status Detail of "An unknown error".</span></span>


## <span data-ttu-id="bc592-232">MDOP 기술을 활용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="bc592-232">How to Get MDOP Technologies</span></span>


<span data-ttu-id="bc592-233">MBAM은 Microsoft 데스크톱 최적화 팩 (MDOP)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-233">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="bc592-234">MDOP는 Microsoft 소프트웨어 보증 프로그램의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-234">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="bc592-235">Microsoft 소프트웨어 보증 프로그램 및 MDOP를 구입 하는 방법에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-235">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="bc592-236">MBAM 2.5 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="bc592-236">MBAM 2.5 SP1 Release Notes</span></span>


<span data-ttu-id="bc592-237">이 설명서에 포함 되지 않은 최신 뉴스에 대 한 자세한 내용은 [MBAM 2.5 SP1 릴리스 노트](release-notes-for-mbam-25-sp1.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc592-237">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5 SP1](release-notes-for-mbam-25-sp1.md).</span></span>

## <span data-ttu-id="bc592-238">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="bc592-238">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bc592-239">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-239">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="bc592-240">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc592-240">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="bc592-241">관련 항목</span><span class="sxs-lookup"><span data-stu-id="bc592-241">Related topics</span></span>


[<span data-ttu-id="bc592-242">Microsoft BitLocker 관리 및 모니터링 2.5</span><span class="sxs-lookup"><span data-stu-id="bc592-242">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="bc592-243">MBAM 2.5 시작</span><span class="sxs-lookup"><span data-stu-id="bc592-243">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





