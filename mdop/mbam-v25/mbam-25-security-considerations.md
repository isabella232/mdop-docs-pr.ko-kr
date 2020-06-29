---
title: MBAM 2.5 보안 고려 사항
description: MBAM 2.5 보안 고려 사항
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826838"
---
# <span data-ttu-id="ffd10-103">MBAM 2.5 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="ffd10-103">MBAM 2.5 Security Considerations</span></span>


<span data-ttu-id="ffd10-104">이 항목에는 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 보호 하는 방법에 대 한 다음 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-104">This topic contains the following information about how to secure Microsoft BitLocker Administration and Monitoring (MBAM):</span></span>

-   [<span data-ttu-id="ffd10-105">TPM을 에스크로 하기 위해 MBAM 구성 및 스토어 소유자 인증 암호</span><span class="sxs-lookup"><span data-stu-id="ffd10-105">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>](#bkmk-tpm)

-   [<span data-ttu-id="ffd10-106">잠금 후 자동으로 TPM 잠금을 해제 하도록 MBAM 구성</span><span class="sxs-lookup"><span data-stu-id="ffd10-106">Configure MBAM to automatically unlock the TPM after a lockout</span></span>](#bkmk-autounlock)

-   [<span data-ttu-id="ffd10-107">SQL Server에 대 한 보안 연결</span><span class="sxs-lookup"><span data-stu-id="ffd10-107">Secure connections to SQL Server</span></span>](#bkmk-secure-databases)

-   [<span data-ttu-id="ffd10-108">계정 및 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="ffd10-108">Create accounts and groups</span></span>](#bkmk-accts-groups)

-   [<span data-ttu-id="ffd10-109">MBAM 로그 파일 사용</span><span class="sxs-lookup"><span data-stu-id="ffd10-109">Use MBAM log files</span></span>](#bkmk-logfiles)

-   [<span data-ttu-id="ffd10-110">MBAM 데이터베이스 TDE 고려 사항 검토</span><span class="sxs-lookup"><span data-stu-id="ffd10-110">Review MBAM database TDE considerations</span></span>](#bkmk-tde)

-   [<span data-ttu-id="ffd10-111">일반 보안 고려 사항 이해</span><span class="sxs-lookup"><span data-stu-id="ffd10-111">Understand general security considerations</span></span>](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a><span data-ttu-id="ffd10-112">TPM을 에스크로 하기 위해 MBAM 구성 및 스토어 소유자 인증 암호</span><span class="sxs-lookup"><span data-stu-id="ffd10-112">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>

<span data-ttu-id="ffd10-113">**참고** Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-113">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="ffd10-114">또한 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-114">In addition, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="ffd10-115">자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-115">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="ffd10-116">구성에 따라 TPM (신뢰할 수 있는 플랫폼 모듈)은 잘못 된 암호를 너무 많이 입력 하 여 일정 기간 동안 잠금 상태로 유지 되는 경우와 같은 특정 상황에서 함에 의해 자동으로 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-116">Depending on its configuration, the Trusted Platform Module (TPM) will lock itself in certain situations ─ such as when too many incorrect passwords are entered ─ and can remain locked for a period of time.</span></span> <span data-ttu-id="ffd10-117">TPM 잠금을 사용 하는 동안 BitLocker는 사용자가 운영 체제 드라이브에 액세스 하기 위해 BitLocker 복구 키를 입력 하도록 요구 하는 잠금 해제 또는 암호 해독 작업을 수행 하기 위해 암호화 키에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-117">During TPM lockout, BitLocker cannot access the encryption keys to perform unlock or decryption operations, requiring the user to enter their BitLocker recovery key to access the operating system drive.</span></span> <span data-ttu-id="ffd10-118">TPM 잠금을 다시 설정 하려면 TPM 소유자 인증 암호를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-118">To reset TPM lockout, you must provide the TPM OwnerAuth password.</span></span>

<span data-ttu-id="ffd10-119">MBAM이 TPM을 소유 하거나 암호가 escrows 경우 MBAM 데이터베이스에 TPM 소유자 인증 암호를 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-119">MBAM can store the TPM OwnerAuth password in the MBAM database if it owns the TPM or if it escrows the password.</span></span> <span data-ttu-id="ffd10-120">그런 다음, TPM 잠금에서 복구 해야 하는 경우 관리 및 모니터링 웹 사이트에서 잠금이 자체적으로 확인 될 때까지 대기 해야 하는 경우에 대 한 접근성 암호를 쉽게 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-120">OwnerAuth passwords are then easily accessible on the Administration and Monitoring Website when you must recover from a TPM lockout, eliminating the need to wait for the lockout to resolve on its own.</span></span>

### <span data-ttu-id="ffd10-121">Windows 8 이상에서 Escrowing TPM 소유자 인증</span><span class="sxs-lookup"><span data-stu-id="ffd10-121">Escrowing TPM OwnerAuth in Windows 8 and higher</span></span>

<span data-ttu-id="ffd10-122">**참고** Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-122">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="ffd10-123">Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-123">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="ffd10-124">자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-124">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="ffd10-125">Windows 8 이상에서 로컬 컴퓨터에서 소유자 인증을 사용할 수 있는 경우에는 MBAM가 소유자 인증 암호를 저장할 수 있도록 TPM을 소유 하 고 있지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-125">In Windows 8 or higher, MBAM no longer must own the TPM to store the OwnerAuth password, as long as the OwnerAuth is available on the local machine.</span></span>

<span data-ttu-id="ffd10-126">MBAM을 에스크로으로 설정한 다음 TPM 소유자 인증 암호를 저장 하려면 이러한 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-126">To enable MBAM to escrow and then store TPM OwnerAuth passwords, you must configure these Group Policy settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ffd10-127">그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ffd10-127">Group Policy Setting</span></span></th>
<th align="left"><span data-ttu-id="ffd10-128">구성</span><span class="sxs-lookup"><span data-stu-id="ffd10-128">Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffd10-129">Active Directory 도메인 서비스에 대 한 TPM 백업 설정</span><span class="sxs-lookup"><span data-stu-id="ffd10-129">Turn on TPM backup to Active Directory Domain Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffd10-130">사용 안 함 또는 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="ffd10-130">Disabled or Not Configured</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffd10-131">운영 체제에서 사용할 수 있는 TPM 소유자 권한 부여 정보 수준 구성</span><span class="sxs-lookup"><span data-stu-id="ffd10-131">Configure the level of TPM owner authorization information available to the operating system</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffd10-132">대리인/없음 또는 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="ffd10-132">Delegated/None or Not Configured</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ffd10-133">이러한 그룹 정책 설정의 위치는 **컴퓨터 구성** &gt; **관리 템플릿** &gt; **시스템** 의 &gt; **신뢰할 수 있는 플랫폼 모듈 서비스**입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-133">The location of these Group Policy settings is **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="ffd10-134">**참고**  Windows는 MBAM이이 설정으로 성공적으로 escrows 후 소유자 인증을 로컬로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-134">**Note** Windows removes the OwnerAuth locally after MBAM successfully escrows it with these settings.</span></span>

 

### <span data-ttu-id="ffd10-135">Windows 7의 Escrowing TPM 소유자 인증</span><span class="sxs-lookup"><span data-stu-id="ffd10-135">Escrowing TPM OwnerAuth in Windows 7</span></span>

<span data-ttu-id="ffd10-136">Windows 7에서 MBAM은 MBAM 데이터베이스에서 자동으로 TPM 소유자 인증 정보를 받아야 하는 TPM을 소유 하 고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-136">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="ffd10-137">MBAM이 TPM을 소유 하 고 있지 않은 경우 AD (Active Directory) 데이터 가져오기 cmdlet을 사용 하 여 Active Directory에서 MBAM 데이터베이스로 TPM 소유자 인증을 복사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-137">If MBAM does not own the TPM, you must use the MBAM Active Directory (AD) Data Import cmdlets to copy TPM OwnerAuth from Active Directory into the MBAM database.</span></span>

### <span data-ttu-id="ffd10-138">MBAM Active Directory 데이터 가져오기 cmdlet</span><span class="sxs-lookup"><span data-stu-id="ffd10-138">MBAM Active Directory Data Import cmdlets</span></span>

<span data-ttu-id="ffd10-139">MBAM Active Directory 데이터 가져오기 cmdlet을 사용 하면 Active Directory에 저장 된 복구 키 패키지와 소유자 인증 암호를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-139">The MBAM Active Directory Data Import cmdlets let you retrieve recovery key packages and OwnerAuth passwords that are stored in Active Directory.</span></span>

<span data-ttu-id="ffd10-140">MBAM 2.5 SP1 서버는 볼륨 복구 및 Active Directory에 저장 된 TPM 소유자 정보를 사용 하 여 MBAM 데이터베이스를 미리 채우는 4 개의 PowerShell cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-140">The MBAM 2.5 SP1 server ships with four PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="ffd10-141">볼륨 복구 키 및 패키지:</span><span class="sxs-lookup"><span data-stu-id="ffd10-141">For Volume Recovery keys and packages:</span></span>

-   <span data-ttu-id="ffd10-142">읽기-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="ffd10-142">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="ffd10-143">읽기-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="ffd10-143">Write-MbamRecoveryInformation</span></span>

<span data-ttu-id="ffd10-144">TPM 소유자 정보:</span><span class="sxs-lookup"><span data-stu-id="ffd10-144">For TPM Owner Information:</span></span>

-   <span data-ttu-id="ffd10-145">읽기-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="ffd10-145">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="ffd10-146">읽기-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="ffd10-146">Write-MbamTpmInformation</span></span>

<span data-ttu-id="ffd10-147">사용자를 컴퓨터에 연결 하는 방법:</span><span class="sxs-lookup"><span data-stu-id="ffd10-147">For Associating Users to Computers:</span></span>

-   <span data-ttu-id="ffd10-148">쓰기-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="ffd10-148">Write-MbamComputerUser</span></span>

<span data-ttu-id="ffd10-149">읽기-광고 \ \* cmdlet은 Active Directory에서 정보를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-149">The Read-AD\* cmdlets read information from Active Directory.</span></span> <span data-ttu-id="ffd10-150">쓰기-Mbam \ \* cmdlet은 데이터를 MBAM 데이터베이스로 푸시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-150">The Write-Mbam\* cmdlets push the data into the MBAM databases.</span></span> <span data-ttu-id="ffd10-151">구문, 매개 변수, 예제 등의 이러한 cmdlet에 대 한 자세한 내용은 [Microsoft Bitlocker 관리 및 모니터링 2.5에 대 한 Cmdlet 참조](https://technet.microsoft.com/library/dn459018.aspx) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-151">See [Cmdlet Reference for Microsoft Bitlocker Administration and Monitoring 2.5](https://technet.microsoft.com/library/dn459018.aspx) for detailed information about these cmdlets, including syntax, parameters, and examples.</span></span>

<span data-ttu-id="ffd10-152">**사용자 대 컴퓨터 연결 만들기:** MBAM Active Directory 데이터 가져오기 cmdlet은 Active Directory에서 정보를 수집 하 고 MBAM 데이터베이스에 데이터를 삽입 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-152">**Create user-to-computer associations:** The MBAM Active Directory Data Import cmdlets gather information from Active Directory and insert the data into MBAM database.</span></span> <span data-ttu-id="ffd10-153">그러나 사용자를 볼륨에 연결 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-153">However, they do not associate users to volumes.</span></span> <span data-ttu-id="ffd10-154">Add-ComputerUser.ps1 PowerShell 스크립트를 다운로드 하 여 사용자 간 연결을 만들어 사용자가 관리 및 모니터링 웹 사이트를 통해 컴퓨터에 액세스 하거나 복구에 셀프 서비스 포털을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-154">You can download the Add-ComputerUser.ps1 PowerShell script to create user-to-machine associations, which let users regain access to a computer through the Administration and Monitoring Website or by using the Self-Service Portal for recovery.</span></span> <span data-ttu-id="ffd10-155">Add-ComputerUser.ps1 스크립트는 AD (Active Directory)의 **관리** 속성 또는 광고의 개체 소유자 또는 사용자 지정 CSV 파일에서 데이터를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-155">The Add-ComputerUser.ps1 script gathers data from the **Managed By** attribute in Active Directory (AD), the object owner in AD, or from a custom CSV file.</span></span> <span data-ttu-id="ffd10-156">그런 다음이 스크립트는 검색 된 사용자를 복구 정보 파이프라인 개체에 추가 하 여 복구 데이터베이스에 데이터를 삽입 하도록 MbamRecoveryInformation에 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-156">The script then adds the discovered users to the recovery information pipeline object, which must be passed to Write-MbamRecoveryInformation to insert the data into the recovery database.</span></span>

<span data-ttu-id="ffd10-157">[Microsoft 다운로드 센터](https://go.microsoft.com/fwlink/?LinkId=613122)에서 Add-ComputerUser.ps1 PowerShell 스크립트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-157">Download the Add-ComputerUser.ps1 PowerShell script from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122).</span></span>

<span data-ttu-id="ffd10-158">Cmdlet 및 스크립트를 사용 하는 방법에 대 한 예제를 포함 하 여 스크립트에 대 한 도움말을 제공 하는 **도움말 Add-ComputerUser.ps1** 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-158">You can specify **help Add-ComputerUser.ps1** to get help for the script, including examples of how to use the cmdlets and the script.</span></span>

<span data-ttu-id="ffd10-159">MBAM 서버를 설치한 후 사용자 간 연결을 만들려면 쓰기-MbamComputerUser PowerShell cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-159">To create user-to-computer associations after you have installed the MBAM server, use the Write-MbamComputerUser PowerShell cmdlet.</span></span> <span data-ttu-id="ffd10-160">이 cmdlet은 Add-ComputerUser.ps1 PowerShell 스크립트와 유사 하 게, 셀프 서비스 포털을 사용 하 여 지정 된 컴퓨터에 대 한 TPM 소유자 인증 정보 또는 볼륨 복구 암호를 가져올 수 있는 사용자를 지정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-160">Similar to the Add-ComputerUser.ps1 PowerShell script, this cmdlet lets you specify users that can use the Self-Service Portal to get TPM OwnerAuth information or volume recovery passwords for the specified computer.</span></span>

<span data-ttu-id="ffd10-161">**참고**  MBAM 에이전트는 컴퓨터에서 서버에 보고 하기 시작 하면 사용자 간 연결을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-161">**Note** The MBAM agent will override user-to-computer associations when that computer begins reporting up to the server.</span></span>

 

<span data-ttu-id="ffd10-162">**전제 조건:** 읽기-AD \ \* cmdlet은 도메인 관리자 등의 높은 권한이 있는 사용자 계정으로 실행 되거나 정보에 대 한 읽기 권한을 부여 받은 사용자 지정 보안 그룹의 계정으로 실행 되는 경우에만 AD에서 정보를 검색할 수 있습니다 (권장).</span><span class="sxs-lookup"><span data-stu-id="ffd10-162">**Prerequisites:** The Read-AD\* cmdlets can retrieve information from AD only if they are either run as a highly privileged user account, such as a Domain Administrator, or run as an account in a custom security group granted read access to the information (recommended).</span></span>

<span data-ttu-id="ffd10-163">[BitLocker 드라이브 암호화 작업 가이드: AD DS를 사용 하 여 암호화 된 볼륨 복구](https://technet.microsoft.com/library/cc771778(WS.10).aspx) 광고 정보에 대 한 읽기 권한이 있는 사용자 지정 보안 그룹 (또는 여러 그룹)을 만드는 방법에 대 한 세부 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-163">[BitLocker Drive Encryption Operations Guide: Recovering Encrypted Volumes with AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) provides details about creating a custom security group (or multiple groups) with read access to the AD information.</span></span>

<span data-ttu-id="ffd10-164">**Mbam 복구 및 하드웨어 웹 서비스 쓰기 권한:** 쓰기-Mbam \ \* cmdlet은 복구 또는 TPM 정보를 게시 하는 데 사용 되는 MBAM 복구 및 하드웨어 서비스의 URL을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-164">**MBAM Recovery and Hardware Web Service Write Permissions:** The Write-Mbam\* cmdlets accept the URL of the MBAM Recovery and Hardware Service, used to publish the recovery or TPM information.</span></span> <span data-ttu-id="ffd10-165">일반적으로 도메인 컴퓨터 서비스 계정만 MBAM 복구 및 하드웨어 서비스와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-165">Typically, only a domain computer service account can communicate with the MBAM Recovery and Hardware Service.</span></span> <span data-ttu-id="ffd10-166">MBAM 2.5 SP1에서는 구성원이 도메인 컴퓨터 서비스 계정 확인을 우회할 수 있는 DataMigrationAccessGroup 이라는 보안 그룹을 사용 하 여 MBAM 복구 및 하드웨어 서비스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-166">In MBAM 2.5 SP1, you can configure the MBAM Recovery and Hardware Service with a security group called DataMigrationAccessGroup whose members are allowed to bypass the domain computer service account check.</span></span> <span data-ttu-id="ffd10-167">이 구성 된 그룹에 속하는 사용자로 서 쓰기-Mbam \ \* cmdlet을 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-167">The Write-Mbam\* cmdlets must be run as a user belonging to this configured group.</span></span> <span data-ttu-id="ffd10-168">또는 쓰기-Mbam \ \* cmdlet에서 – Credential 매개 변수를 사용 하 여 구성 된 그룹에 있는 개별 사용자의 자격 증명을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-168">(Alternatively, the credentials of an individual user in the configured group can be specified by using the –Credential parameter in the Write-Mbam\* cmdlets.)</span></span>

<span data-ttu-id="ffd10-169">다음 방법 중 하나를 사용 하 여이 보안 그룹의 이름으로 MBAM 복구 및 하드웨어 서비스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-169">You can configure the MBAM Recovery and Hardware Service with the name of this security group in one of these ways:</span></span>

-   <span data-ttu-id="ffd10-170">사용-MbamWebApplication – AgentService Powershell cmdlet의-DataMigrationAccessGroup 매개 변수에 보안 그룹 또는 개인의 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-170">Provide the name of the security group (or individual) in the -DataMigrationAccessGroup parameter of the Enable-MbamWebApplication –AgentService Powershell cmdlet.</span></span>

-   <span data-ttu-id="ffd10-171">&lt;Inetpub &gt; \\Microsoft Bitlocker 관리 솔루션 \ 복구 및 하드웨어 Service\\ 폴더에서 web.config 파일을 편집 하 여 Mbam 복구 및 하드웨어 서비스를 설치한 후 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-171">Configure the group after the MBAM Recovery and Hardware Service has been installed by editing the web.config file in the &lt;inetpub&gt;\\Microsoft Bitlocker Management Solution\\Recovery and Hardware Service\\ folder.</span></span>

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    <span data-ttu-id="ffd10-172">여기서 &lt; groupName &gt; 이 Active Directory에서 데이터 마이그레이션을 허용 하는 데 사용 되는 도메인 및 그룹 이름 (또는 개별 사용자)으로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-172">where &lt;groupName&gt; is replaced with the domain and the group name (or the individual user) that will be used to allow data migration from Active Directory.</span></span>

-   <span data-ttu-id="ffd10-173">IIS 관리자의 구성 편집기를 사용 하 여이 appSetting을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-173">Use the Configuration Editor in IIS Manager to edit this appSetting.</span></span>

<span data-ttu-id="ffd10-174">다음 예에서는 ADRecoveryInformation 그룹 및 데이터 마이그레이션 사용자 그룹의 구성원으로 실행 될 때 명령으로 contoso.com 도메인의 워크스테이션 OU (조직 구성 단위)에 있는 컴퓨터의 볼륨 복구 정보를 가져와 mbam.contoso.com 서버에서 실행 되는 MBAM 복구 및 하드웨어 서비스를 사용 하 여 MBAM에 씁니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-174">In the following example, the command, when run as a member of both the ADRecoveryInformation group and the Data Migration Users group, will pull the volume recovery information from computers in the WORKSTATIONS organizational unit (OU) in the contoso.com domain and write them to MBAM by using the MBAM Recovery and Hardware Service running on the mbam.contoso.com server.</span></span>

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

<span data-ttu-id="ffd10-175">**읽기-AD \ \* cmdlet** 은 복구 또는 TPM 정보에 대해 쿼리할 Active Directory 호스팅 서버 컴퓨터의 이름 또는 IP 주소를 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-175">**Read-AD\* cmdlets** accept the name or IP address of an Active Directory hosting server machine to query for recovery or TPM information.</span></span> <span data-ttu-id="ffd10-176">컴퓨터 개체가 있는 AD 컨테이너의 고유 이름을 SearchBase 매개 변수의 값으로 제공 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-176">We recommend providing the distinguished names of the AD containers in which the computer object resides as the value of the SearchBase parameter.</span></span> <span data-ttu-id="ffd10-177">컴퓨터가 여러 Ou에 저장 되어 있는 경우 cmdlet에서 파이프라인 입력을 허용 하 여 각 컨테이너에 대해 한 번씩 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-177">If computers are stored across several OUs, the cmdlets can accept pipeline input to run once for each container.</span></span> <span data-ttu-id="ffd10-178">광고 컨테이너의 고유 이름은 OU = 기계, DC = contoso, DC = com과 유사 하 게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-178">The distinguished name of an AD container will look similar to OU=Machines,DC=contoso,DC=com.</span></span> <span data-ttu-id="ffd10-179">특정 컨테이너를 대상으로 하는 검색을 수행 하면 다음과 같은 혜택을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-179">Performing a search targeted to specific containers provides the following benefits:</span></span>

-   <span data-ttu-id="ffd10-180">컴퓨터 개체에 대 한 대규모 광고 데이터 집합을 쿼리 하는 동안 시간이 초과 될 위험을 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-180">Reduces the risk of timeout while querying a large AD dataset for computer objects.</span></span>

-   <span data-ttu-id="ffd10-181">백업 하는 것이 원하지 않거나 필요 하지 않은 데이터 센터 서버 또는 다른 종류의 컴퓨터를 포함 하는 Ou를 생략할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-181">Can omit OUs containing datacenter servers or other classes of computers for which the backup might not be desired or necessary.</span></span>

<span data-ttu-id="ffd10-182">또 다른 옵션은 지정 된 SearchBase 또는 전체 도메인 아래에 있는 모든 컨테이너에서 컴퓨터 개체를 검색 하는 – a i a i a i a i a i a i a i a i a i a i a i a i</span><span class="sxs-lookup"><span data-stu-id="ffd10-182">Another option is to provide the –Recurse flag with or without the optional SearchBase to search for computer objects across all containers under the specified SearchBase or the entire domain respectively.</span></span> <span data-ttu-id="ffd10-183">-A 재귀 플래그를 사용 하는 경우-MaxPageSize 매개 변수를 사용 하 여 쿼리를 처리 하는 데 필요한 로컬 및 원격 메모리의 양을 제어할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-183">When you use the -Recurse flag, you can also use the -MaxPageSize parameter to control the amount of local and remote memory required to service the query.</span></span>

<span data-ttu-id="ffd10-184">이러한 cmdlet은 PsObject 유형의 파이프라인 개체에 씁니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-184">These cmdlets write to the pipeline objects of type PsObject.</span></span> <span data-ttu-id="ffd10-185">각 PsObject 인스턴스에는 단일 볼륨 복구 키 또는 TPM 소유자 문자열 (관련 컴퓨터 이름, 타임 스탬프, 그리고 MBAM 데이터 저장소에 게시 하는 데 필요한 기타 정보)이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-185">Each PsObject instance contains a single volume recovery key or TPM owner string with its associated computer name, timestamp, and other information required to publish it to the MBAM data store.</span></span>

<span data-ttu-id="ffd10-186">**쓰기-Mbam \ \* cmdlet** 은 파이프라인의 복구 정보 매개 변수 값을 속성 이름으로 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-186">**Write-Mbam\* cmdlets** accept recovery information parameter values from the pipeline by property name.</span></span> <span data-ttu-id="ffd10-187">이렇게 하면 쓰기-Mbam \ \* cmdlet이 읽기-AD \ \* cmdlet의 파이프라인 출력을 수락할 수 있습니다 (예: 읽기-ADRecoveryInformation-Server contoso.com-재귀적 |). 쓰기-MbamRecoveryInformation-RecoveryServiceEndpoint mbam.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="ffd10-187">This allows the Write-Mbam\* cmdlets to accept the pipeline output of the Read-AD\* cmdlets (for example, Read-ADRecoveryInformation –Server contoso.com –Recurse | Write-MbamRecoveryInformation –RecoveryServiceEndpoint mbam.contoso.com).</span></span>

<span data-ttu-id="ffd10-188">**쓰기-Mbam \ \* cmdlet** 에는 내결함성, 자세한 로깅 및 WhatIf 및 확인에 대 한 기본 설정에 대 한 옵션을 제공 하는 선택적 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-188">The **Write-Mbam\* cmdlets** include optional parameters that provide options for fault tolerance, verbose logging, and preferences for WhatIf and Confirm.</span></span>

<span data-ttu-id="ffd10-189">**쓰기-Mbam \ \* cmdlet** 에는 값이 **DateTime** 개체인 선택적 *시간* 매개 변수도 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-189">The **Write-Mbam\* cmdlets** also include an optional *Time* parameter whose value is a **DateTime** object.</span></span> <span data-ttu-id="ffd10-190">이 개체에는, 또는으로 설정할 수 있는 *Kind* 특성이 포함 되어 있습니다 `Local` `UTC` `Unspecified` .</span><span class="sxs-lookup"><span data-stu-id="ffd10-190">This object includes a *Kind* attribute that can be set to `Local`, `UTC`, or `Unspecified`.</span></span> <span data-ttu-id="ffd10-191">*시간* 매개 변수가 Active Directory에서 가져온 데이터로 채워지면 시간이 UTC로 변환 되 고이 *Kind* 특성이 자동으로로 설정 됩니다 `UTC` .</span><span class="sxs-lookup"><span data-stu-id="ffd10-191">When the *Time* parameter is populated from data taken from the Active Directory, the time is converted to UTC and this *Kind* attribute is set automatically to `UTC`.</span></span> <span data-ttu-id="ffd10-192">그러나 텍스트 파일과 같은 다른 소스를 사용 하 여 *시간* 매개 변수를 채울 때는 *Kind* 특성을 해당 값으로 명시적으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-192">However, when populating the *Time* parameter using another source, such as a text file, you must explicitly set the *Kind* attribute to its appropriate value.</span></span>

<span data-ttu-id="ffd10-193">**참고**  읽기-광고 \ \* cmdlet에는 컴퓨터 사용자를 나타내는 사용자 계정을 검색 하는 기능이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-193">**Note** The Read-AD\* cmdlets do not have the ability to discover the user accounts that represent the computer users.</span></span> <span data-ttu-id="ffd10-194">사용자 계정 연결에는 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-194">User account associations are needed for the following:</span></span>

-   <span data-ttu-id="ffd10-195">셀프 서비스 포털을 사용 하 여 볼륨 암호/패키지를 복구 하는 사용자</span><span class="sxs-lookup"><span data-stu-id="ffd10-195">Users to recover volume passwords/packages by using the Self-Service portal</span></span>

-   <span data-ttu-id="ffd10-196">다른 사용자를 대신 하 여 설치 하는 동안 MBAM 헬프데스크 사용자의 보안 그룹에 정의 된 사용자를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-196">Users who are not in the MBAM Advanced Helpdesk Users security group as defined during installation, recovering on behalf of other users</span></span>

 

## <a href="" id="bkmk-autounlock"></a><span data-ttu-id="ffd10-197">잠금 후 자동으로 TPM 잠금을 해제 하도록 MBAM 구성</span><span class="sxs-lookup"><span data-stu-id="ffd10-197">Configure MBAM to automatically unlock the TPM after a lockout</span></span>


<span data-ttu-id="ffd10-198">잠금을 설정 하는 경우 자동으로 TPM 잠금을 해제 하도록 MBAM 2.5 SP1을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-198">You can configure MBAM 2.5 SP1 to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="ffd10-199">TPM 잠금 자동 재설정을 사용 하도록 설정한 경우 MBAM은 사용자가 잠겨 있음을 감지 하 고 MBAM 데이터베이스에서 소유자 인증 암호를 받아 사용자의 TPM을 자동으로 잠금 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-199">If TPM lockout auto reset is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span> <span data-ttu-id="ffd10-200">TPM 잠금 자동 재설정은 셀프 서비스 포털 또는 관리 및 모니터링 웹 사이트를 사용 하 여 해당 컴퓨터의 OS 복구 키를 검색 한 경우에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-200">TPM lockout auto reset is only available if the OS recovery key for that computer was retrieved by using the Self Service Portal or the Administration and Monitoring Website.</span></span>

<span data-ttu-id="ffd10-201">**중요**  TPM 잠금 자동 재설정을 사용 하도록 설정 하려면 클라이언트측에서 서버 쪽 및 그룹 정책 모두에이 기능을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-201">**Important** To enable TPM lockout auto reset, you must configure this feature on both the server side and in Group Policy on the client side.</span></span>

 

-   <span data-ttu-id="ffd10-202">클라이언트 쪽에서 TPM 잠금 자동 재설정을 사용 하도록 설정 하려면 **컴퓨터 구성** 관리 템플릿에 있는 그룹 정책 설정 "TPM 잠금 자동 재설정 구성"을 구성 합니다 &gt; **Administrative Templates** &gt; . **Windows 구성 요소** &gt; **MDOP mblaam** &gt; **클라이언트 관리**.</span><span class="sxs-lookup"><span data-stu-id="ffd10-202">To enable TPM lockout auto reset on the client side, configure the Group Policy setting "Configure TPM lockout auto reset" located at **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM** &gt; **Client Management**.</span></span>

-   <span data-ttu-id="ffd10-203">서버 쪽에서 TPM 잠금 자동 재설정을 사용 하도록 설정 하려면 설치 하는 동안 MBAM 서버 구성 마법사에서 "TPM 잠금 자동 재설정 사용"을 선택 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-203">To enable TPM lockout auto reset on the server side, you can check "Enable TPM lockout auto reset" in the MBAM Server Configuration wizard during setup.</span></span>

    <span data-ttu-id="ffd10-204">또한 에이전트 서비스 웹 구성 요소를 사용 하도록 설정 하는 동안 "-TPM 잠금 자동 재설정" 스위치를 지정 하 여 PowerShell에서 TPM 잠금 자동 재설정을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-204">You can also enable TPM lockout auto reset in PowerShell by specifying the "-TPM lockout auto reset" switch while enabling the agent service web component.</span></span>

<span data-ttu-id="ffd10-205">사용자가 셀프 서비스 포털 또는 관리 및 모니터링 웹 사이트에서 받은 BitLocker 복구 키를 입력 하면 MBAM 에이전트는 TPM이 잠겨 있는지 확인 합니다. 잠겨 있는 경우 MBAM 데이터베이스에서 컴퓨터에 대 한 TPM 소유자 인증을 검색 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-205">After a user enters the BitLocker recovery key they obtained from the Self Service Portal or the Administration and Monitoring Website, the MBAM agent will determine if the TPM is locked out. If it is locked out, it will attempt to retrieve the TPM OwnerAuth for the computer from the MBAM database.</span></span> <span data-ttu-id="ffd10-206">TPM 소유자 인증이 성공적으로 검색 되 면 TPM의 잠금을 해제 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-206">If the TPM OwnerAuth is successfully retrieved, it will be used to unlock the TPM.</span></span> <span data-ttu-id="ffd10-207">Tpm 잠금을 해제 하면 tpm이 완전히 작동 하므로 사용자는 TPM 잠금에서 이후 다시 부팅 하는 동안 복구 암호를 입력 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-207">Unlocking the TPM makes the TPM fully functional and the user will not be forced to enter the recovery password during subsequent reboots from a TPM lockout.</span></span>

<span data-ttu-id="ffd10-208">TPM 잠금 자동 재설정은 기본적으로 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-208">TPM lockout auto reset is disabled by default.</span></span>

<span data-ttu-id="ffd10-209">**참고**  Tpm 잠금 자동 재설정은 TPM 버전 1.2를 실행 하는 컴퓨터 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-209">**Note** TPM lockout auto reset is only supported on computers running TPM version 1.2.</span></span> <span data-ttu-id="ffd10-210">TPM 2.0는 기본 제공 잠금 자동 재설정 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-210">TPM 2.0 provides built-in lockout auto reset functionality.</span></span>

 

<span data-ttu-id="ffd10-211">**복구 감사 보고서** 에는 TPM 잠금 자동 재설정 관련 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-211">**The Recovery Audit Report** includes events related to TPM lockout auto reset.</span></span> <span data-ttu-id="ffd10-212">MBAM 클라이언트에서 TPM 소유자 인증 암호를 검색 하는 데 요청이 이루어지면 복구를 나타내기 위해 이벤트가 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-212">If a request is made from the MBAM client to retrieve a TPM OwnerAuth password, an event is logged to indicate recovery.</span></span> <span data-ttu-id="ffd10-213">감사 항목에는 다음 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-213">Audit entries will include the following events:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ffd10-214">엔트리에서</span><span class="sxs-lookup"><span data-stu-id="ffd10-214">Entry</span></span></th>
<th align="left"><span data-ttu-id="ffd10-215">값</span><span class="sxs-lookup"><span data-stu-id="ffd10-215">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffd10-216">감사 요청 원본</span><span class="sxs-lookup"><span data-stu-id="ffd10-216">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffd10-217">에이전트 TPM 잠금 해제</span><span class="sxs-lookup"><span data-stu-id="ffd10-217">Agent TPM unlock</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ffd10-218">키 유형</span><span class="sxs-lookup"><span data-stu-id="ffd10-218">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffd10-219">TPM 암호 해시</span><span class="sxs-lookup"><span data-stu-id="ffd10-219">TPM Password Hash</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ffd10-220">이유 설명</span><span class="sxs-lookup"><span data-stu-id="ffd10-220">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="ffd10-221">TPM 다시 설정</span><span class="sxs-lookup"><span data-stu-id="ffd10-221">TPM Reset</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a><span data-ttu-id="ffd10-222">SQL Server에 대 한 보안 연결</span><span class="sxs-lookup"><span data-stu-id="ffd10-222">Secure connections to SQL Server</span></span>


<span data-ttu-id="ffd10-223">MBAM은 sql server Reporting Services와 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털의 웹 서비스와 통신 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-223">In MBAM, SQL Server communicates with SQL Server Reporting Services and with the web services for the Administration and Monitoring Website and Self-Service Portal.</span></span> <span data-ttu-id="ffd10-224">SQL Server와 통신을 보호 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-224">We recommend that you secure the communication with SQL Server.</span></span> <span data-ttu-id="ffd10-225">자세한 내용은 [SQL Server에 대 한 연결 암호화](https://technet.microsoft.com/library/ms189067.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-225">For more information, see [Encrypting Connections to SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span></span>

<span data-ttu-id="ffd10-226">MBAM 웹 사이트 보안에 대 한 자세한 내용은 [MBAM 웹 사이트 보안 방법 계획](planning-how-to-secure-the-mbam-websites.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-226">For more information about securing the MBAM websites, see [Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md).</span></span>

## <a href="" id="bkmk-accts-groups"></a><span data-ttu-id="ffd10-227">계정 및 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="ffd10-227">Create accounts and groups</span></span>


<span data-ttu-id="ffd10-228">사용자 계정을 관리 하는 가장 좋은 방법은 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-228">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="ffd10-229">권장 계정 및 그룹에 대 한 설명은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-229">For a description of the recommended accounts and groups, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

## <a href="" id="bkmk-logfiles"></a><span data-ttu-id="ffd10-230">MBAM 로그 파일 사용</span><span class="sxs-lookup"><span data-stu-id="ffd10-230">Use MBAM log files</span></span>


<span data-ttu-id="ffd10-231">이 섹션에서는 MBAM 서버 및 MBAM 클라이언트 로그 파일에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-231">This section describes the MBAM Server and MBAM Client log files.</span></span>

**<span data-ttu-id="ffd10-232">MBAM 서버 설정 로그 파일</span><span class="sxs-lookup"><span data-stu-id="ffd10-232">MBAM Server Setup log files</span></span>**

<span data-ttu-id="ffd10-233">**MBAMServerSetup.exe** 파일은 mbam 설치 중 사용자의 **% temp%** 폴더에 다음 로그 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-233">The **MBAMServerSetup.exe** file generates the following log files in the user’s **%temp%** folder during the MBAM installation:</span></span>

-   **<span data-ttu-id="ffd10-234">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 개 번호 &gt; . 로그</span><span class="sxs-lookup"><span data-stu-id="ffd10-234">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14 numbers&gt;.log</span></span>**

    <span data-ttu-id="ffd10-235">MBAM 설정 및 MBAM 서버 기능 구성 중에 수행 된 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-235">Logs the actions taken during the MBAM setup and the MBAM Server feature configuration.</span></span>

-   **<span data-ttu-id="ffd10-236">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. .log</span><span class="sxs-lookup"><span data-stu-id="ffd10-236">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14\_numbers&gt;\_0\_MBAMServer.msi.log</span></span>**

    <span data-ttu-id="ffd10-237">설치 중에 수행한 추가 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-237">Logs additional action taken during installation.</span></span>

**<span data-ttu-id="ffd10-238">MBAM 서버 구성 로그 파일</span><span class="sxs-lookup"><span data-stu-id="ffd10-238">MBAM Server Configuration log files</span></span>**

-   **<span data-ttu-id="ffd10-239">응용 프로그램 및 서비스 로그/Microsoft Windows/MBAM-설정</span><span class="sxs-lookup"><span data-stu-id="ffd10-239">Applications and Services Logs/Microsoft Windows/MBAM-Setup</span></span>**

    <span data-ttu-id="ffd10-240">Windows Powershell cmdlet 또는 MBAM 서버 구성 마법사를 사용 하 여 MBAM 서버 기능을 구성할 때 발생 하는 오류를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-240">Logs the errors that occur when you are using Windows Powershell cmdlets or the MBAM Server Configuration wizard to configure the MBAM Server features.</span></span>

**<span data-ttu-id="ffd10-241">MBAM 클라이언트 설치 로그 파일</span><span class="sxs-lookup"><span data-stu-id="ffd10-241">MBAM Client setup log files</span></span>**

-   **<span data-ttu-id="ffd10-242">MSI &lt; 5 임의 문자 &gt; 로그</span><span class="sxs-lookup"><span data-stu-id="ffd10-242">MSI&lt;five random characters&gt;.log</span></span>**

    <span data-ttu-id="ffd10-243">MBAM 클라이언트 설치 중 수행 된 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-243">Logs the actions taken during the MBAM Client installation.</span></span>

**<span data-ttu-id="ffd10-244">MBAM-웹 로그 파일</span><span class="sxs-lookup"><span data-stu-id="ffd10-244">MBAM-Web log files</span></span>**

-   <span data-ttu-id="ffd10-245">웹 포털 및 서비스의 활동을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-245">Shows activity from the web portals and services.</span></span>

## <a href="" id="bkmk-tde"></a><span data-ttu-id="ffd10-246">MBAM 데이터베이스 TDE 고려 사항 검토</span><span class="sxs-lookup"><span data-stu-id="ffd10-246">Review MBAM database TDE considerations</span></span>


<span data-ttu-id="ffd10-247">SQL Server에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능은 MBAM 데이터베이스 기능을 호스팅하는 데이터베이스 인스턴스의 선택적 설치입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-247">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host the MBAM database features.</span></span>

<span data-ttu-id="ffd10-248">TDE를 사용 하 여 실시간 전체 데이터베이스 수준의 암호화를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-248">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="ffd10-249">TDE는 규정 준수 또는 기업 데이터 보안 표준을 충족 하기 위해 일괄 암호화를 위한 최적의 선택입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-249">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="ffd10-250">TDE는 파일 수준에서 작동 하며, 파일 시스템 암호화 (EFS)와 BitLocker 드라이브 암호화의 두 가지 Windows 기능과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-250">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption.</span></span> <span data-ttu-id="ffd10-251">또한 두 기능은 모두 하드 드라이브의 데이터를 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-251">Both features also encrypt data on the hard drive.</span></span> <span data-ttu-id="ffd10-252">TDE는 셀 수준 암호화, EFS 또는 BitLocker를 대체 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-252">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="ffd10-253">데이터베이스에서 TDE를 사용 하도록 설정 하면 모든 백업이 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-253">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="ffd10-254">따라서 데이터베이스 암호화 키를 보호 하는 데 사용 된 인증서가 데이터베이스 백업과 함께 백업 되 고 유지 되도록 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-254">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="ffd10-255">이 인증서 (또는 인증서)가 손실 되 면 데이터를 읽을 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-255">If this certificate (or certificates) is lost, the data will be unreadable.</span></span>

<span data-ttu-id="ffd10-256">데이터베이스와 인증서를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-256">Back up the certificate with the database.</span></span> <span data-ttu-id="ffd10-257">각 인증서 백업에는 두 개의 파일이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-257">Each certificate backup should have two files.</span></span> <span data-ttu-id="ffd10-258">이러한 파일은 모두 보관 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-258">Both of these files should be archived.</span></span> <span data-ttu-id="ffd10-259">보안을 위해 가장 적합 한 것은 데이터베이스 백업 파일과 별도로 백업 해야 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-259">Ideally for security, they should be backed up separately from the database backup file.</span></span> <span data-ttu-id="ffd10-260">또는 TDE에 사용 되는 키 저장소 및 유지 관리를 위해 EKM (확장할 수 있는 키 관리) 기능 (확장 가능한 키 관리)을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-260">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys that are used for TDE.</span></span>

<span data-ttu-id="ffd10-261">MBAM 데이터베이스 인스턴스의 TDE를 사용 하는 방법에 대 한 예제는 [투명 한 데이터 암호화 (tde) 이해](https://technet.microsoft.com/library/bb934049.aspx)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-261">For an example of how to enable TDE for MBAM database instances, see [Understanding Transparent Data Encryption (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span></span>

## <a href="" id="bkmk-general-security"></a><span data-ttu-id="ffd10-262">일반 보안 고려 사항 이해</span><span class="sxs-lookup"><span data-stu-id="ffd10-262">Understand general security considerations</span></span>


**<span data-ttu-id="ffd10-263">보안 위험을 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-263">Understand the security risks.</span></span>** <span data-ttu-id="ffd10-264">Microsoft BitLocker 관리 및 모니터링을 사용할 때 가장 심각한 위험은 BitLocker 드라이브 암호화를 다시 구성 하 고 MBAM 클라이언트에서 BitLocker 암호화 키 데이터를 얻을 수 있는 권한이 없는 사용자가 해당 기능을 손상 시킬 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-264">The most serious risk when you use Microsoft BitLocker Administration and Monitoring is that its functionality could be compromised by an unauthorized user who could then reconfigure BitLocker Drive Encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="ffd10-265">그러나 서비스 거부 공격으로 인해 짧은 시간 동안에는 MBAM 기능이 손실 되는 것은 일반적으로 전자 메일 이나 네트워크 통신이 손실 되는 등의 경우와 달리 심각한 영향을 미치지 않는다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-265">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, losing e-mail or network communications, or power.</span></span>

<span data-ttu-id="ffd10-266">**컴퓨터를 물리적으로 보호**합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-266">**Physically secure your computers**.</span></span> <span data-ttu-id="ffd10-267">물리적 보안 없이 보안이 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-267">There is no security without physical security.</span></span> <span data-ttu-id="ffd10-268">MBAM 서버에 물리적으로 액세스 하는 공격자는이를 사용 하 여 전체 클라이언트 기반을 공격할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-268">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="ffd10-269">모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-269">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="ffd10-270">MBAM 서버는 액세스 권한이 있는 안전한 서버 방에 저장 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-270">MBAM Servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="ffd10-271">운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-271">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="ffd10-272">**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-272">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="ffd10-273">[보안 TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819)에서 보안 알림 서비스에 가입 하 여 Windows 운영 체제, SQL SERVER 및 mbam에 대 한 새 업데이트에 대 한 정보를 지속적으로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-273">Stay informed about new updates for Windows operating systems, SQL Server, and MBAM by subscribing to the Security Notification service at the [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819).</span></span>

<span data-ttu-id="ffd10-274">**강력한 암호 또는 암호 문구를 사용**합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-274">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="ffd10-275">모든 MBAM 관리자 계정에 대해 15 개 이상의 문자로 강력한 암호를 항상 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-275">Always use strong passwords with 15 or more characters for all MBAM administrator accounts.</span></span> <span data-ttu-id="ffd10-276">빈 암호를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-276">Never use blank passwords.</span></span> <span data-ttu-id="ffd10-277">암호 개념에 대 한 자세한 내용은 [암호 정책을](https://technet.microsoft.com/library/hh994572.aspx)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffd10-277">For more information about password concepts, see [Password Policy](https://technet.microsoft.com/library/hh994572.aspx).</span></span>



## <span data-ttu-id="ffd10-278">관련 항목</span><span class="sxs-lookup"><span data-stu-id="ffd10-278">Related topics</span></span>


[<span data-ttu-id="ffd10-279">MBAM 2.5 배포 계획</span><span class="sxs-lookup"><span data-stu-id="ffd10-279">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 
## <span data-ttu-id="ffd10-280">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="ffd10-280">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ffd10-281">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-281">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="ffd10-282">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffd10-282">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





