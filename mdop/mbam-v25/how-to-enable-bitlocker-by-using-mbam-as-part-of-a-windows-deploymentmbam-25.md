---
title: Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법
description: Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626185"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a><span data-ttu-id="eddcd-103">Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법</span><span class="sxs-lookup"><span data-stu-id="eddcd-103">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eddcd-104">이러한 지침은 Configuration Manager BitLocker 관리와는 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-104">These instructions do not pertain to Configuration Manager BitLocker Management.</span></span> <span data-ttu-id="eddcd-105">`Invoke-MbamClientDeployment.ps1`PowerShell 스크립트는 Configuration Manager의 BitLocker 관리에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-105">The `Invoke-MbamClientDeployment.ps1` PowerShell script is not supported for use with BitLocker Management in Configuration Manager.</span></span> <span data-ttu-id="eddcd-106">여기에는 Configuration Manager 작업 순서 중에 BitLocker 복구 키의 에스크로킹이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-106">This includes escrowing of BitLocker recovery keys during a Configuration Manager task sequence.</span></span> <span data-ttu-id="eddcd-107">또한 Configuration Manager Current Branch 2103부터 Configuration Manager BitLocker Management는 더 이상 MBAM 키 복구 서비스 사이트를 사용하여 에스클로 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-107">Furthermore, starting with Configuration Manager Current Branch 2103, Configuration Manager BitLocker Management no longer uses the MBAM key recovery services site to escrow keys.</span></span> <span data-ttu-id="eddcd-108">Configuration Manager 현재 분기 2103 이상에서 PowerShell 스크립트를 사용하려고 시도하면 Configuration Manager 사이트에 심각한 문제가 `Invoke-MbamClientDeployment.ps1` 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-108">Attempting to use the `Invoke-MbamClientDeployment.ps1` PowerShell script with Configuration Manager Current Branch 2103 or newer can result in serious problems with the Configuration Manager site.</span></span> <span data-ttu-id="eddcd-109">알려진 문제로는 정책 폭주를 일으킬 수 있는 모든 장치를 대상으로 하는 많은 양의 정책 생성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-109">Known problems include creation of a large amount of policy targeted to all devices which can cause policy storms.</span></span> <span data-ttu-id="eddcd-110">이로 인해 Configuration Manager의 성능 저하는 주로 관리 지점에서 SQL 저하될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-110">This will lead to severe degradation of performance in Configuration Manager primarily in SQL and with Management Points.</span></span>

<span data-ttu-id="eddcd-111">이 항목에서는 MBAM을 이미징 및 배포 프로세스의 일부로 사용하여 최종 사용자 컴퓨터에서 BitLocker를 사용하도록 Windows 방법을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-111">This topic explains how to enable BitLocker on an end user's computer by using MBAM as part of your Windows imaging and deployment process.</span></span> <span data-ttu-id="eddcd-112">다시 시작 시(설치 단계가 종료된 후) 드라이브의 잠금을 해제할 수 없다는 검은색 화면이 표시될 경우 Windows 10 버전 [1511과](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)함께 사전 프로비전 BitLocker를 사용하는 경우 이전 Windows 버전이 "설치 Windows 및 Configuration Manager" 단계 후에 시작되지 않습니다를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-112">If you see a black screen at restart (after Install phase concludes) indicating that the drive cannot be unlocked, see [Earlier Windows versions don't start after "Setup Windows and Configuration Manager" step if Pre-Provision BitLocker is used with Windows 10, version 1511](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).</span></span>

**<span data-ttu-id="eddcd-113">필수 조건:</span><span class="sxs-lookup"><span data-stu-id="eddcd-113">Prerequisites:</span></span>**

-   <span data-ttu-id="eddcd-114">MDT(Microsoft Deployment Toolkit), Microsoft System Center Configuration Manager 또는 기타 이미징 도구 또는 프로세스인 기존 Windows 이미지 배포 프로세스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-114">An existing Windows image deployment process – Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager, or some other imaging tool or process – must be in place</span></span>

-   <span data-ttu-id="eddcd-115">BIOS에서 TPM을 사용하도록 설정하고 OS에 표시되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-115">TPM must be enabled in the BIOS and visible to the OS</span></span>

-   <span data-ttu-id="eddcd-116">MBAM 서버 인프라가 있으며 액세스 가능해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-116">MBAM server infrastructure must be in place and accessible</span></span>

-   <span data-ttu-id="eddcd-117">BitLocker에 필요한 시스템 파티션을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-117">The system partition required by BitLocker must be created</span></span>

-   <span data-ttu-id="eddcd-118">MBAM에서 BitLocker를 완전히 사용하려면 이미징 중에 컴퓨터 도메인에 가입되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-118">The machine must be domain joined during imaging before MBAM fully enables BitLocker</span></span>

**<span data-ttu-id="eddcd-119">MBAM 2.5 SP1을 배포의 일부로 사용하여 BitLocker를 사용하도록 Windows</span><span class="sxs-lookup"><span data-stu-id="eddcd-119">To enable BitLocker using MBAM 2.5 SP1 as part of a Windows deployment</span></span>**

1. <span data-ttu-id="eddcd-120">MBAM 2.5 SP1에서는 배포 중에 BitLocker를 사용하도록 설정하는 Windows `Invoke-MbamClientDeployment.ps1` PowerShell 스크립트를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-120">In MBAM 2.5 SP1, the recommended approach to enable BitLocker during a Windows Deployment is by using the `Invoke-MbamClientDeployment.ps1` PowerShell script.</span></span>

   -   <span data-ttu-id="eddcd-121">이 `Invoke-MbamClientDeployment.ps1` 스크립트는 이미징 프로세스 중에 BitLocker를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-121">The `Invoke-MbamClientDeployment.ps1` script enacts BitLocker during the imaging process.</span></span> <span data-ttu-id="eddcd-122">BitLocker 정책에 필요한 경우 MBAM 에이전트는 도메인 사용자가 이미징 후 처음 로그온할 때 PIN 또는 암호를 만들지 묻는 메시지를 도메인 사용자에게 즉시 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-122">When required by BitLocker policy, the MBAM agent immediately prompts the domain user to create a PIN or password when the domain user first logs on after imaging.</span></span>

   -   <span data-ttu-id="eddcd-123">MDT, System Center Configuration Manager 또는 독립 실행형 이미징 프로세스에서 사용하기 쉬운 경우</span><span class="sxs-lookup"><span data-stu-id="eddcd-123">Easy to use with MDT, System Center Configuration Manager, or standalone imaging processes</span></span>

   -   <span data-ttu-id="eddcd-124">PowerShell 2.0 이상과 호환</span><span class="sxs-lookup"><span data-stu-id="eddcd-124">Compatible with PowerShell 2.0 or higher</span></span>

   -   <span data-ttu-id="eddcd-125">TPM 키 보호기로 OS 볼륨 암호화</span><span class="sxs-lookup"><span data-stu-id="eddcd-125">Encrypt OS volume with TPM key protector</span></span>

   -   <span data-ttu-id="eddcd-126">BitLocker 사전 프로비전을 완전히 지원</span><span class="sxs-lookup"><span data-stu-id="eddcd-126">Fully support BitLocker pre-provisioning</span></span>

   -   <span data-ttu-id="eddcd-127">선택적으로 FDD 암호화</span><span class="sxs-lookup"><span data-stu-id="eddcd-127">Optionally encrypt FDDs</span></span>

   -   <span data-ttu-id="eddcd-128">Escrow TPM OwnerAuth Windows 7의 경우 에스로가 발생하려면 MBAM이 TPM을 소유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-128">Escrow TPM OwnerAuth For Windows 7, MBAM must own the TPM for escrow to occur.</span></span>
   <span data-ttu-id="eddcd-129">이 Windows 8.1 RTM Windows 10 Windows 10 버전 1511의 경우 TPM OwnerAuth의 에스로가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-129">For Windows 8.1, Windows 10 RTM and Windows 10 version 1511, escrow of TPM OwnerAuth is supported.</span></span>
   <span data-ttu-id="eddcd-130">Windows 10 버전 1607 이상의 경우 TPM의 Windows 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-130">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="eddcd-131">addiiton에서는 Windows 프로비전할 때 TPM 소유자 암호를 유지하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-131">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="eddcd-132">자세한 [내용은 TPM 소유자 암호를](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eddcd-132">See [TPM owner password](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

   -   <span data-ttu-id="eddcd-133">에스로 복구 키 및 복구 키 패키지</span><span class="sxs-lookup"><span data-stu-id="eddcd-133">Escrow recovery keys and recovery key packages</span></span>

   -   <span data-ttu-id="eddcd-134">즉시 암호화 상태 보고</span><span class="sxs-lookup"><span data-stu-id="eddcd-134">Report encryption status immediately</span></span>

   -   <span data-ttu-id="eddcd-135">새 WMI 공급자</span><span class="sxs-lookup"><span data-stu-id="eddcd-135">New WMI providers</span></span>

   -   <span data-ttu-id="eddcd-136">자세한 로깅</span><span class="sxs-lookup"><span data-stu-id="eddcd-136">Detailed logging</span></span>

   -   <span data-ttu-id="eddcd-137">강력한 오류 처리</span><span class="sxs-lookup"><span data-stu-id="eddcd-137">Robust error handling</span></span>

   <span data-ttu-id="eddcd-138">다운로드 센터에서 스크립트를 `Invoke-MbamClientDeployment.ps1` [다운로드할 Microsoft.com 있습니다.](https://www.microsoft.com/download/details.aspx?id=54439)</span><span class="sxs-lookup"><span data-stu-id="eddcd-138">You can download the `Invoke-MbamClientDeployment.ps1` script from [Microsoft.com Download Center](https://www.microsoft.com/download/details.aspx?id=54439).</span></span> <span data-ttu-id="eddcd-139">이 스크립트는 배포 시스템에서 BitLocker 드라이브 암호화를 구성하고 MBAM Server를 사용하여 복구 키를 기록하기 위해 호출하는 기본 스크립트입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-139">This is the main script that your deployment system will call to configure BitLocker drive encryption and record recovery keys with the MBAM Server.</span></span>

   <span data-ttu-id="eddcd-140">**MBAM에** 대한 WMI 배포 방법: PowerShell 스크립트를 사용하여 BitLocker 사용을 지원하기 위해 다음 WMI 메서드가 MBAM 2.5 SP1에 `Invoke-MbamClientDeployment.ps1` 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-140">**WMI deployment methods for MBAM:** The following WMI methods have been added in MBAM 2.5 SP1 to support enabling BitLocker by using the `Invoke-MbamClientDeployment.ps1` PowerShell script.</span></span>

   <a href="" id="mbam-machine-wmi-class"></a><span data-ttu-id="eddcd-141">**MBAM\_Machine WMI 클래스** 
    **PrepareTpmAndEscrowOwnerAuth:** TPM OwnerAuth를 읽고 MBAM 복구 서비스를 사용하여 MBAM 복구 데이터베이스로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-141">**MBAM\_Machine WMI Class**
**PrepareTpmAndEscrowOwnerAuth:** Reads the TPM OwnerAuth and sends it to the MBAM recovery database by using the MBAM recovery service.</span></span> <span data-ttu-id="eddcd-142">TPM이 소유되지 않은 경우 자동 프로비저닝이 사용되지 않는 경우 TPM OwnerAuth가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-142">If the TPM is not owned and auto-provisioning is not on, it generates a TPM OwnerAuth and takes ownership.</span></span> <span data-ttu-id="eddcd-143">오류가 발생하면 문제 해결을 위해 오류 코드가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-143">If it fails, an error code is returned for troubleshooting.</span></span>

   <span data-ttu-id="eddcd-144">**참고** Windows 10 버전 1607 이상의 경우 TPM의 Windows 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-144">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="eddcd-145">addiiton에서는 Windows 프로비전할 때 TPM 소유자 암호를 유지하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-145">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="eddcd-146">자세한 [내용은 TPM 소유자 암호를](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eddcd-146">See [TPM owner password](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

| <span data-ttu-id="eddcd-147">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eddcd-147">Parameter</span></span> | <span data-ttu-id="eddcd-148">설명</span><span class="sxs-lookup"><span data-stu-id="eddcd-148">Description</span></span> |
| -------- | ----------- |
| <span data-ttu-id="eddcd-149">RecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="eddcd-149">RecoveryServiceEndPoint</span></span> | <span data-ttu-id="eddcd-150">MBAM 복구 서비스 끝점을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-150">A string specifying the MBAM recovery service endpoint.</span></span> |

<span data-ttu-id="eddcd-151">다음은 일반적인 오류 메시지 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-151">Here are a list of common error messages:</span></span>

| <span data-ttu-id="eddcd-152">일반 반환 값</span><span class="sxs-lookup"><span data-stu-id="eddcd-152">Common return values</span></span> | <span data-ttu-id="eddcd-153">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="eddcd-153">Error message</span></span> |
| -------------------- | ------------- |
|  **<span data-ttu-id="eddcd-154">S_OK</span><span class="sxs-lookup"><span data-stu-id="eddcd-154">S_OK</span></span>**<br /><span data-ttu-id="eddcd-155">0(0x0)</span><span class="sxs-lookup"><span data-stu-id="eddcd-155">0 (0x0)</span></span> | <span data-ttu-id="eddcd-156">메서드가 성공했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-156">The method was successful.</span></span> |
| **<span data-ttu-id="eddcd-157">MBAM_E_TPM_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="eddcd-157">MBAM_E_TPM_NOT_PRESENT</span></span>**<br /><span data-ttu-id="eddcd-158">2147746304(0x80040200)</span><span class="sxs-lookup"><span data-stu-id="eddcd-158">2147746304 (0x80040200)</span></span> | <span data-ttu-id="eddcd-159">TPM이 컴퓨터에 존재하지 않는 경우 또는 BIOS 구성에서 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-159">TPM is not present in the computer or is disabled in the BIOS configuration.</span></span> |
| **<span data-ttu-id="eddcd-160">MBAM_E_TPM_INCORRECT_STATE</span><span class="sxs-lookup"><span data-stu-id="eddcd-160">MBAM_E_TPM_INCORRECT_STATE</span></span>**<br /><span data-ttu-id="eddcd-161">2147746305(0x80040201)</span><span class="sxs-lookup"><span data-stu-id="eddcd-161">2147746305 (0x80040201)</span></span> | <span data-ttu-id="eddcd-162">TPM이 올바른 상태(사용, 활성화 및 소유자 설치 허용)에 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-162">TPM is not in the correct state (enabled, activated and owner installation allowed).</span></span> |
| **<span data-ttu-id="eddcd-163">MBAM_E_TPM_AUTO_PROVISIONING_PENDING</span><span class="sxs-lookup"><span data-stu-id="eddcd-163">MBAM_E_TPM_AUTO_PROVISIONING_PENDING</span></span>**<br /><span data-ttu-id="eddcd-164">2147746306(0x80040202)</span><span class="sxs-lookup"><span data-stu-id="eddcd-164">2147746306 (0x80040202)</span></span> | <span data-ttu-id="eddcd-165">자동 프로비전이 보류 중이기 때문에 MBAM은 TPM의 소유권을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-165">MBAM cannot take ownership of TPM because auto-provisioning is pending.</span></span> <span data-ttu-id="eddcd-166">자동 프로비전이 완료된 후 다시 시도하십시오.</span><span class="sxs-lookup"><span data-stu-id="eddcd-166">Try again after auto-provisioning is completed.</span></span> |
| **<span data-ttu-id="eddcd-167">MBAM_E_TPM_OWNERAUTH_READFAIL</span><span class="sxs-lookup"><span data-stu-id="eddcd-167">MBAM_E_TPM_OWNERAUTH_READFAIL</span></span>**<br /><span data-ttu-id="eddcd-168">2147746307(0x80040203)</span><span class="sxs-lookup"><span data-stu-id="eddcd-168">2147746307 (0x80040203)</span></span> | <span data-ttu-id="eddcd-169">MBAM은 TPM 소유자 권한 부여 값을 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-169">MBAM cannot read the TPM owner authorization value.</span></span> <span data-ttu-id="eddcd-170">이 값은 에스크로에 성공한 후 제거된 것일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-170">The value might have been removed after a successful escrow.</span></span> <span data-ttu-id="eddcd-171">7 Windows TPM이 다른 사용자가 소유한 경우 MBAM은 값을 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-171">On Windows 7, MBAM cannot read the value if the TPM is owned by others.</span></span> |
| **<span data-ttu-id="eddcd-172">MBAM_E_REBOOT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="eddcd-172">MBAM_E_REBOOT_REQUIRED</span></span>**<br /><span data-ttu-id="eddcd-173">2147746308(0x80040204)</span><span class="sxs-lookup"><span data-stu-id="eddcd-173">2147746308 (0x80040204)</span></span> | <span data-ttu-id="eddcd-174">TPM을 올바른 상태로 설정하려면 컴퓨터를 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-174">The computer must be restarted to set TPM to the correct state.</span></span> <span data-ttu-id="eddcd-175">컴퓨터를 수동으로 다시 시작해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-175">You might need to manually reboot the computer.</span></span> |
| **<span data-ttu-id="eddcd-176">MBAM_E_SHUTDOWN_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="eddcd-176">MBAM_E_SHUTDOWN_REQUIRED</span></span>**<br /><span data-ttu-id="eddcd-177">2147746309(0x80040205)</span><span class="sxs-lookup"><span data-stu-id="eddcd-177">2147746309 (0x80040205)</span></span> | <span data-ttu-id="eddcd-178">TPM을 올바른 상태로 설정하려면 컴퓨터를 종료했다가 다시 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-178">The computer must be shut down and turned back on to set TPM to the correct state.</span></span> <span data-ttu-id="eddcd-179">컴퓨터를 수동으로 다시 시작해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-179">You might need to manually reboot the computer.</span></span> |
| **<span data-ttu-id="eddcd-180">WS_E_ENDPOINT_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="eddcd-180">WS_E_ENDPOINT_ACCESS_DENIED</span></span>**<br /><span data-ttu-id="eddcd-181">2151481349(0x803D0005)</span><span class="sxs-lookup"><span data-stu-id="eddcd-181">2151481349 (0x803D0005)</span></span> | <span data-ttu-id="eddcd-182">원격 끝점에서 액세스가 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-182">Access was denied by the remote endpoint.</span></span> |
| **<span data-ttu-id="eddcd-183">WS_E_ENDPOINT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eddcd-183">WS_E_ENDPOINT_NOT_FOUND</span></span>**<br /><span data-ttu-id="eddcd-184">2151481357(0x803D000D)</span><span class="sxs-lookup"><span data-stu-id="eddcd-184">2151481357 (0x803D000D)</span></span> | <span data-ttu-id="eddcd-185">원격 끝점이 존재하지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-185">The remote endpoint does not exist or could not be located.</span></span> |
| <span data-ttu-id="eddcd-186">\*\*WS_E_ENDPOINT_FAILURE</span><span class="sxs-lookup"><span data-stu-id="eddcd-186">\*\*WS_E_ENDPOINT_FAILURE</span></span><br /><span data-ttu-id="eddcd-187">2151481357(0x803D000F)</span><span class="sxs-lookup"><span data-stu-id="eddcd-187">2151481357 (0x803D000F)</span></span> | <span data-ttu-id="eddcd-188">원격 끝점에서 요청을 처리하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-188">The remote endpoint could not process the request.</span></span> |
| **<span data-ttu-id="eddcd-189">WS_E_ENDPOINT_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="eddcd-189">WS_E_ENDPOINT_UNREACHABLE</span></span>**<br /><span data-ttu-id="eddcd-190">2151481360(0x803D0010)</span><span class="sxs-lookup"><span data-stu-id="eddcd-190">2151481360 (0x803D0010)</span></span> | <span data-ttu-id="eddcd-191">원격 끝점에 도달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-191">The remote endpoint was not reachable.</span></span> |
| **<span data-ttu-id="eddcd-192">WS_E_ENDPOINT_FAULT_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="eddcd-192">WS_E_ENDPOINT_FAULT_RECEIVED</span></span>**<br /><span data-ttu-id="eddcd-193">2151481363(0x803D0013)</span><span class="sxs-lookup"><span data-stu-id="eddcd-193">2151481363 (0x803D0013)</span></span> | <span data-ttu-id="eddcd-194">원격 끝점에서 오류가 포함된 메시지를 수신했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-194">A message containing a fault was received from the remote endpoint.</span></span> <span data-ttu-id="eddcd-195">올바른 서비스 끝점에 연결하고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-195">Make sure you are connecting to the correct service endpoint.</span></span> |
| <span data-ttu-id="eddcd-196">**WS_E_INVALID_ENDPOINT_URL** 2151481376(0x803D0020)</span><span class="sxs-lookup"><span data-stu-id="eddcd-196">**WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020)</span></span> | <span data-ttu-id="eddcd-197">끝점 주소 URL이 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-197">The endpoint address URL is not valid.</span></span> <span data-ttu-id="eddcd-198">URL은 "http" 또는 "https"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-198">The URL must start with “http” or “https”.</span></span> |

   <span data-ttu-id="eddcd-199">**ReportStatus:** 볼륨의 준수 상태를 읽고 MBAM 상태 보고 서비스를 사용하여 MBAM 준수 상태 데이터베이스로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-199">**ReportStatus:** Reads the compliance status of the volume and sends it to the MBAM compliance status database by using the MBAM status reporting service.</span></span> <span data-ttu-id="eddcd-200">상태에는 암호화 강도, 보호기 유형, 보호기 상태 및 암호화 상태가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-200">The status includes cipher strength, protector type, protector state and encryption state.</span></span> <span data-ttu-id="eddcd-201">오류가 발생하면 문제 해결을 위해 오류 코드가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-201">If it fails, an error code is returned for troubleshooting.</span></span>

   | <span data-ttu-id="eddcd-202">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eddcd-202">Parameter</span></span> | <span data-ttu-id="eddcd-203">설명</span><span class="sxs-lookup"><span data-stu-id="eddcd-203">Description</span></span> |
   | --------- | ----------- |
   | <span data-ttu-id="eddcd-204">ReportingServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="eddcd-204">ReportingServiceEndPoint</span></span> | <span data-ttu-id="eddcd-205">MBAM 상태 보고 서비스 끝점을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-205">A string specifying the MBAM status reporting service endpoint.</span></span> |

   <span data-ttu-id="eddcd-206">다음은 일반적인 오류 메시지 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-206">Here are a list of common error messages:</span></span>

   | <span data-ttu-id="eddcd-207">일반 반환 값</span><span class="sxs-lookup"><span data-stu-id="eddcd-207">Common return values</span></span> | <span data-ttu-id="eddcd-208">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="eddcd-208">Error message</span></span> |
   | -------------------- | ------------- |
   | **<span data-ttu-id="eddcd-209">S_OK</span><span class="sxs-lookup"><span data-stu-id="eddcd-209">S_OK</span></span>**<br /> <span data-ttu-id="eddcd-210">0(0x0)</span><span class="sxs-lookup"><span data-stu-id="eddcd-210">0 (0x0)</span></span> | <span data-ttu-id="eddcd-211">메서드가 성공했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-211">The method was successful</span></span> |
   | **<span data-ttu-id="eddcd-212">WS_E_ENDPOINT_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="eddcd-212">WS_E_ENDPOINT_ACCESS_DENIED</span></span>**<br /><span data-ttu-id="eddcd-213">2151481349(0x803D0005)</span><span class="sxs-lookup"><span data-stu-id="eddcd-213">2151481349 (0x803D0005)</span></span> | <span data-ttu-id="eddcd-214">원격 끝점에서 액세스가 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-214">Access was denied by the remote endpoint.</span></span>|
   | **<span data-ttu-id="eddcd-215">WS_E_ENDPOINT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eddcd-215">WS_E_ENDPOINT_NOT_FOUND</span></span>**<br /><span data-ttu-id="eddcd-216">2151481357(0x803D000D)</span><span class="sxs-lookup"><span data-stu-id="eddcd-216">2151481357 (0x803D000D)</span></span> | <span data-ttu-id="eddcd-217">원격 끝점이 존재하지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-217">The remote endpoint does not exist or could not be located.</span></span> |
   | **<span data-ttu-id="eddcd-218">WS_E_ENDPOINT_FAILURE</span><span class="sxs-lookup"><span data-stu-id="eddcd-218">WS_E_ENDPOINT_FAILURE</span></span>**<br /> <span data-ttu-id="eddcd-219">2151481357(0x803D000F)</span><span class="sxs-lookup"><span data-stu-id="eddcd-219">2151481357 (0x803D000F)</span></span> | <span data-ttu-id="eddcd-220">원격 끝점에서 요청을 처리하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-220">The remote endpoint could not process the request.</span></span> |
   | **<span data-ttu-id="eddcd-221">WS_E_ENDPOINT_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="eddcd-221">WS_E_ENDPOINT_UNREACHABLE</span></span>**<br /><span data-ttu-id="eddcd-222">2151481360(0x803D0010)</span><span class="sxs-lookup"><span data-stu-id="eddcd-222">2151481360 (0x803D0010)</span></span> | <span data-ttu-id="eddcd-223">원격 끝점에 도달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-223">The remote endpoint was not reachable.</span></span> |
   | **<span data-ttu-id="eddcd-224">WS_E_ENDPOINT_FAULT_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="eddcd-224">WS_E_ENDPOINT_FAULT_RECEIVED</span></span>**<br /><span data-ttu-id="eddcd-225">2151481363(0x803D0013)</span><span class="sxs-lookup"><span data-stu-id="eddcd-225">2151481363 (0x803D0013)</span></span> | <span data-ttu-id="eddcd-226">원격 끝점에서 오류가 포함된 메시지를 수신했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-226">A message containing a fault was received from the remote endpoint.</span></span> <span data-ttu-id="eddcd-227">올바른 서비스 끝점에 연결하고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-227">Make sure you are connecting to the correct service endpoint.</span></span> |
   | **<span data-ttu-id="eddcd-228">WS_E_INVALID_ENDPOINT_URL</span><span class="sxs-lookup"><span data-stu-id="eddcd-228">WS_E_INVALID_ENDPOINT_URL</span></span>**<br /><span data-ttu-id="eddcd-229">2151481376(0x803D0020)</span><span class="sxs-lookup"><span data-stu-id="eddcd-229">2151481376 (0x803D0020)</span></span> | <span data-ttu-id="eddcd-230">끝점 주소 URL이 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-230">The endpoint address URL is not valid.</span></span> <span data-ttu-id="eddcd-231">URL은 "http" 또는 "https"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-231">The URL must start with “http” or “https”.</span></span> |

   <a href="" id="mbam-volume-wmi-class"></a><span data-ttu-id="eddcd-232">**MBAM\_Volume WMI** 클래스 **EscrowRecoveryKey:** 볼륨의 복구 숫자 암호 및 키 패키지를 읽고 MBAM 복구 서비스를 사용하여 MBAM 복구 데이터베이스로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-232">**MBAM\_Volume WMI Class** **EscrowRecoveryKey:** Reads the recovery numerical password and key package of the volume and sends them to the MBAM recovery database by using the MBAM recovery service.</span></span> <span data-ttu-id="eddcd-233">오류가 발생하면 문제 해결을 위해 오류 코드가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-233">If it fails, an error code is returned for troubleshooting.</span></span>

   | <span data-ttu-id="eddcd-234">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eddcd-234">Parameter</span></span> | <span data-ttu-id="eddcd-235">설명</span><span class="sxs-lookup"><span data-stu-id="eddcd-235">Description</span></span> |
   | --------- | ----------- |
   | <span data-ttu-id="eddcd-236">RecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="eddcd-236">RecoveryServiceEndPoint</span></span> | <span data-ttu-id="eddcd-237">MBAM 복구 서비스 끝점을 지정하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-237">A string specifying the MBAM recovery service endpoint.</span></span> |

   <span data-ttu-id="eddcd-238">다음은 일반적인 오류 메시지 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-238">Here are a list of common error messages:</span></span>

   | <span data-ttu-id="eddcd-239">일반 반환 값</span><span class="sxs-lookup"><span data-stu-id="eddcd-239">Common return values</span></span> | <span data-ttu-id="eddcd-240">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="eddcd-240">Error message</span></span> |
   | -------------------- | ------------- |
   | **<span data-ttu-id="eddcd-241">S_OK</span><span class="sxs-lookup"><span data-stu-id="eddcd-241">S_OK</span></span>**<br /><span data-ttu-id="eddcd-242">0(0x0)</span><span class="sxs-lookup"><span data-stu-id="eddcd-242">0 (0x0)</span></span> | <span data-ttu-id="eddcd-243">메서드가 성공했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-243">The method was successful</span></span> |
   | **<span data-ttu-id="eddcd-244">FVE_E_LOCKED_VOLUME</span><span class="sxs-lookup"><span data-stu-id="eddcd-244">FVE_E_LOCKED_VOLUME</span></span>**<br /><span data-ttu-id="eddcd-245">2150694912(0x80310000)</span><span class="sxs-lookup"><span data-stu-id="eddcd-245">2150694912 (0x80310000)</span></span> | <span data-ttu-id="eddcd-246">볼륨이 잠겨 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-246">The volume is locked.</span></span> |
   | **<span data-ttu-id="eddcd-247">FVE_E_PROTECTOR_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eddcd-247">FVE_E_PROTECTOR_NOT_FOUND</span></span>**<br /><span data-ttu-id="eddcd-248">2150694963(0x80310033)</span><span class="sxs-lookup"><span data-stu-id="eddcd-248">2150694963 (0x80310033)</span></span> | <span data-ttu-id="eddcd-249">볼륨에 대한 숫자 암호 보호를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-249">A Numerical Password protector was not found for the volume.</span></span> |
   | **<span data-ttu-id="eddcd-250">WS_E_ENDPOINT_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="eddcd-250">WS_E_ENDPOINT_ACCESS_DENIED</span></span>**<br /><span data-ttu-id="eddcd-251">2151481349(0x803D0005)</span><span class="sxs-lookup"><span data-stu-id="eddcd-251">2151481349 (0x803D0005)</span></span> | <span data-ttu-id="eddcd-252">원격 끝점에서 액세스가 거부됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-252">Access was denied by the remote endpoint.</span></span> |
   | **<span data-ttu-id="eddcd-253">WS_E_ENDPOINT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eddcd-253">WS_E_ENDPOINT_NOT_FOUND</span></span>**<br /><span data-ttu-id="eddcd-254">2151481357(0x803D000D)</span><span class="sxs-lookup"><span data-stu-id="eddcd-254">2151481357 (0x803D000D)</span></span> | <span data-ttu-id="eddcd-255">원격 끝점이 존재하지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-255">The remote endpoint does not exist or could not be located.</span></span> |
   | **<span data-ttu-id="eddcd-256">WS_E_ENDPOINT_FAILURE</span><span class="sxs-lookup"><span data-stu-id="eddcd-256">WS_E_ENDPOINT_FAILURE</span></span>**<br /><span data-ttu-id="eddcd-257">2151481357(0x803D000F)</span><span class="sxs-lookup"><span data-stu-id="eddcd-257">2151481357 (0x803D000F)</span></span> | <span data-ttu-id="eddcd-258">원격 끝점에서 요청을 처리하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-258">The remote endpoint could not process the request.</span></span> |
   | **<span data-ttu-id="eddcd-259">WS_E_ENDPOINT_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="eddcd-259">WS_E_ENDPOINT_UNREACHABLE</span></span>**<br /><span data-ttu-id="eddcd-260">2151481360(0x803D0010)</span><span class="sxs-lookup"><span data-stu-id="eddcd-260">2151481360 (0x803D0010)</span></span> | <span data-ttu-id="eddcd-261">원격 끝점에 도달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-261">The remote endpoint was not reachable.</span></span> |
   | **<span data-ttu-id="eddcd-262">WS_E_ENDPOINT_FAULT_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="eddcd-262">WS_E_ENDPOINT_FAULT_RECEIVED</span></span>**<br /><span data-ttu-id="eddcd-263">2151481363(0x803D0013)</span><span class="sxs-lookup"><span data-stu-id="eddcd-263">2151481363 (0x803D0013)</span></span> | <span data-ttu-id="eddcd-264">원격 끝점에서 오류가 포함된 메시지를 수신했습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-264">A message containing a fault was received from the remote endpoint.</span></span> <span data-ttu-id="eddcd-265">올바른 서비스 끝점에 연결하고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-265">Make sure you are connecting to the correct service endpoint.</span></span> |
   | **<span data-ttu-id="eddcd-266">WS_E_INVALID_ENDPOINT_URL</span><span class="sxs-lookup"><span data-stu-id="eddcd-266">WS_E_INVALID_ENDPOINT_URL</span></span>**<br /><span data-ttu-id="eddcd-267">2151481376(0x803D0020)</span><span class="sxs-lookup"><span data-stu-id="eddcd-267">2151481376 (0x803D0020)</span></span> | <span data-ttu-id="eddcd-268">끝점 주소 URL이 유효하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-268">The endpoint address URL is not valid.</span></span> <span data-ttu-id="eddcd-269">URL은 "http" 또는 "https"로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-269">The URL must start with “http” or “https”.</span></span> |
     

2. **<span data-ttu-id="eddcd-270">MDT(Microsoft Deployment Toolkit) 및 PowerShell을 사용하여 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="eddcd-270">Deploy MBAM by using Microsoft Deployment Toolkit (MDT) and PowerShell</span></span>**

   1.  <span data-ttu-id="eddcd-271">MDT에서 새 배포 공유를 만들거나 기존 배포 공유를 니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-271">In MDT, create a new deployment share or open an existing deployment share.</span></span>

       **<span data-ttu-id="eddcd-272">참고</span><span class="sxs-lookup"><span data-stu-id="eddcd-272">Note</span></span>**  
       <span data-ttu-id="eddcd-273">PowerShell 스크립트는 모든 이미징 프로세스 또는 `Invoke-MbamClientDeployment.ps1` 도구에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-273">The `Invoke-MbamClientDeployment.ps1` PowerShell script can be used with any imaging process or tool.</span></span> <span data-ttu-id="eddcd-274">이 섹션에서는 MDT를 사용하여 통합하는 방법을 보여 주지만 단계는 다른 프로세스 또는 도구와 통합하는 방법과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-274">This section shows how to integrate it by using MDT, but the steps are similar to integrating it with any other process or tool.</span></span>

       **<span data-ttu-id="eddcd-275">주의</span><span class="sxs-lookup"><span data-stu-id="eddcd-275">Caution</span></span>**  
       <span data-ttu-id="eddcd-276">WinPE(BitLocker 사전 프로비전)를 사용하는 경우 TPM 소유자 권한 부여 값을 유지하려면 설치가 전체 운영 체제로 다시 시작되기 직전에 WinPE에서 스크립트를 `SaveWinPETpmOwnerAuth.wsf` 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-276">If you are using BitLocker pre-provisioning (WinPE) and want to maintain the TPM owner authorization value, you must add the `SaveWinPETpmOwnerAuth.wsf` script in WinPE immediately before the installation reboots into the full operating system.</span></span> **<span data-ttu-id="eddcd-277">이 스크립트를 사용하지 않는 경우 다시 시작 시 TPM 소유자 권한 부여 값이 손실됩니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-277">If you do not use this script, you will lose the TPM owner authorization value on reboot.</span></span>**

   2.  <span data-ttu-id="eddcd-278">`Invoke-MbamClientDeployment.ps1` \*\* &lt; DeploymentShare &gt; \\Scripts에 복사합니다.\*\*</span><span class="sxs-lookup"><span data-stu-id="eddcd-278">Copy `Invoke-MbamClientDeployment.ps1` to **&lt;DeploymentShare&gt;\\Scripts**.</span></span> <span data-ttu-id="eddcd-279">사전 프로비전을 사용하는 경우 `SaveWinPETpmOwnerAuth.wsf` 파일을 \*\* &lt; DeploymentShare &gt; \\Scripts 에 복사합니다.\*\*</span><span class="sxs-lookup"><span data-stu-id="eddcd-279">If you are using pre-provisioning, copy the `SaveWinPETpmOwnerAuth.wsf` file into **&lt;DeploymentShare&gt;\\Scripts**.</span></span>

   3.  <span data-ttu-id="eddcd-280">배포 공유의 응용 프로그램 노드에 MBAM 2.5 SP1 클라이언트 응용 프로그램을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-280">Add the MBAM 2.5 SP1 client application to the Applications node in the deployment share.</span></span>

       1.  <span data-ttu-id="eddcd-281">응용 프로그램 **노드에서** 새 응용 **프로그램을 클릭합니다.**</span><span class="sxs-lookup"><span data-stu-id="eddcd-281">Under the **Applications** node, click **New Application**.</span></span>

       2.  <span data-ttu-id="eddcd-282">원본 **파일이 있는 응용 프로그램을 선택합니다.**</span><span class="sxs-lookup"><span data-stu-id="eddcd-282">Select **Application with Source Files**.</span></span> <span data-ttu-id="eddcd-283">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-283">Click **Next**.</span></span>

       3.  <span data-ttu-id="eddcd-284">응용 **프로그램 이름에**"MBAM 2.5 SP1 Client"를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-284">In **Application Name**, type “MBAM 2.5 SP1 Client”.</span></span> <span data-ttu-id="eddcd-285">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-285">Click **Next**.</span></span>

       4.  <span data-ttu-id="eddcd-286">를 포함하는 디렉터리로 `MBAMClientSetup-<Version>.msi` 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-286">Browse to the directory containing `MBAMClientSetup-<Version>.msi`.</span></span> <span data-ttu-id="eddcd-287">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-287">Click **Next**.</span></span>

       5.  <span data-ttu-id="eddcd-288">만들 디렉터리로 "MBAM 2.5 SP1 Client"를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-288">Type “MBAM 2.5 SP1 Client” as the directory to create.</span></span> <span data-ttu-id="eddcd-289">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-289">Click **Next**.</span></span>

       6.  <span data-ttu-id="eddcd-290">`msiexec /i MBAMClientSetup-<Version>.msi /quiet`명령줄에 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-290">Enter `msiexec /i MBAMClientSetup-<Version>.msi /quiet` at the command line.</span></span> <span data-ttu-id="eddcd-291">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-291">Click **Next**.</span></span>

       7.  <span data-ttu-id="eddcd-292">나머지 기본값을 적용하여 새 응용 프로그램 마법사를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-292">Accept the remaining defaults to complete the New Application wizard.</span></span>

   4.  <span data-ttu-id="eddcd-293">MDT에서 배포 공유의 이름을 마우스 오른쪽 단추로 클릭하고 속성을 **클릭합니다.**</span><span class="sxs-lookup"><span data-stu-id="eddcd-293">In MDT, right-click the name of the deployment share and click **Properties**.</span></span> <span data-ttu-id="eddcd-294">규칙 **탭을** 클릭합니다. 다음 줄을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-294">Click the **Rules** tab. Add the following lines:</span></span>

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       <span data-ttu-id="eddcd-295">확인을 클릭하여 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-295">Click OK to close the window.</span></span>

   5.  <span data-ttu-id="eddcd-296">Task Sequences 노드에서 Deployment에 사용되는 기존 작업 Windows 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-296">Under the Task Sequences node, edit an existing task sequence used for Windows Deployment.</span></span> <span data-ttu-id="eddcd-297">원하는 경우 Task **Sequences** 노드를 마우스 오른쪽 단추로 클릭하고 새 \*\*\*\* 작업 순서를 선택한 다음 마법사를 완료하여 새 작업 순서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-297">If you want, you can create a new task sequence by right-clicking the **Task Sequences** node, selecting **New Task Sequence**, and completing the wizard.</span></span>

       <span data-ttu-id="eddcd-298">선택한 **작업 순서의** 작업 순서 탭에서 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-298">On the **Task Sequence** tab of the selected task sequence, perform these steps:</span></span>

       1.  <span data-ttu-id="eddcd-299">**WinPE에서** **BitLocker를** 사용하도록 설정하려면 사전 설치 폴더에서 사용된 공간만 암호화하는 선택적 작업인 BitLocker(오프라인)를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-299">Under the **Preinstall** folder, enable the optional task **Enable BitLocker (Offline)** if you want BitLocker enabled in WinPE, which encrypts used space only.</span></span>

       2.  <span data-ttu-id="eddcd-300">사전 프로비저닝을 사용할 때 TPM OwnerAuth를 유지하여 MBAM이 나중에 에스로를 에버로 할 수 있도록 허용하기 위해 다음을 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-300">To persist TPM OwnerAuth when using pre-provisioning, allowing MBAM to escrow it later, do the following:</span></span>

           1.  <span data-ttu-id="eddcd-301">운영 체제 **설치 단계** 찾기</span><span class="sxs-lookup"><span data-stu-id="eddcd-301">Find the **Install Operating System** step</span></span>

           2.  <span data-ttu-id="eddcd-302">다음에 새 **실행 명령줄** 단계 추가</span><span class="sxs-lookup"><span data-stu-id="eddcd-302">Add a new **Run Command Line** step after it</span></span>

           3.  <span data-ttu-id="eddcd-303">**TPM OwnerAuth 유지 단계의 이름을 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="eddcd-303">Name the step **Persist TPM OwnerAuth**</span></span>

           4.  <span data-ttu-id="eddcd-304">명령줄을 참고로 `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **설정:** Windows 10 버전 1607 이상의 경우 TPM의 Windows 수만 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-304">Set the command line to `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
**Note:** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="eddcd-305">addiiton에서는 Windows 프로비전할 때 TPM 소유자 암호를 유지하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-305">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="eddcd-306">자세한 [내용은 TPM 소유자 암호를](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eddcd-306">See [TPM owner password](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

       3.  <span data-ttu-id="eddcd-307">State **Restore 폴더에서** **BitLocker** 사용 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-307">In the **State Restore** folder, delete the **Enable BitLocker** task.</span></span>

       4.  <span data-ttu-id="eddcd-308">사용자 **지정 작업 아래 상태 복원** 폴더에서 새 응용 프로그램 설치 작업을 만들고 이름을 \*\*\*\* \*\*\*\* **MBAM 에이전트 설치로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="eddcd-308">In the **State Restore** folder under **Custom Tasks**, create a new **Install Application** task and name it **Install MBAM Agent**.</span></span> <span data-ttu-id="eddcd-309">단일 **응용 프로그램 설치** 라디오 단추를 클릭하고 앞에서 만든 MBAM 2.5 SP1 클라이언트 응용 프로그램으로 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-309">Click the **Install Single Application** radio button and browse to the MBAM 2.5 SP1 client application created earlier.</span></span>

       5.  <span data-ttu-id="eddcd-310">사용자 지정 작업의 \*\*\*\* **상태 복원** 폴더에서 다음 설정(환경에 따라 매개 변수 업데이트)을 사용하여 새 **PowerShell** 스크립트 실행 작업(MBAM 2.5 SP1 클라이언트 응용 프로그램 단계 후)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-310">In the **State Restore** folder under **Custom Tasks**, create a new **Run PowerShell Script** task (after the MBAM 2.5 SP1 Client application step) with the following settings (update the parameters as appropriate for your environment):</span></span>

           -   <span data-ttu-id="eddcd-311">이름: MBAM에 대해 BitLocker 구성</span><span class="sxs-lookup"><span data-stu-id="eddcd-311">Name: Configure BitLocker for MBAM</span></span>

           -   <span data-ttu-id="eddcd-312">PowerShell 스크립트:</span><span class="sxs-lookup"><span data-stu-id="eddcd-312">PowerShell script:</span></span> `Invoke-MbamClientDeployment.ps1`

           -   <span data-ttu-id="eddcd-313">매개 변수:</span><span class="sxs-lookup"><span data-stu-id="eddcd-313">Parameters:</span></span>

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="eddcd-314">-RecoveryServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="eddcd-314">-RecoveryServiceEndpoint</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-315">필수</span><span class="sxs-lookup"><span data-stu-id="eddcd-315">Required</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-316">MBAM 복구 서비스 끝점</span><span class="sxs-lookup"><span data-stu-id="eddcd-316">MBAM recovery service endpoint</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="eddcd-317">-StatusReportingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="eddcd-317">-StatusReportingServiceEndpoint</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-318">선택 사항</span><span class="sxs-lookup"><span data-stu-id="eddcd-318">Optional</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-319">MBAM 상태 보고 서비스 끝점</span><span class="sxs-lookup"><span data-stu-id="eddcd-319">MBAM status reporting service endpoint</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="eddcd-320">-EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="eddcd-320">-EncryptionMethod</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-321">선택 사항</span><span class="sxs-lookup"><span data-stu-id="eddcd-321">Optional</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-322">암호화 방법(기본값: AES 128)</span><span class="sxs-lookup"><span data-stu-id="eddcd-322">Encryption method (default: AES 128)</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="eddcd-323">-EncryptAndEscrowDataVolume</span><span class="sxs-lookup"><span data-stu-id="eddcd-323">-EncryptAndEscrowDataVolume</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-324">스위치</span><span class="sxs-lookup"><span data-stu-id="eddcd-324">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-325">데이터 볼륨 및 에스로 데이터 볼륨 복구 키를 암호화하기 위해 지정</span><span class="sxs-lookup"><span data-stu-id="eddcd-325">Specify to encrypt data volume(s) and escrow data volume recovery key(s)</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="eddcd-326">-WaitForEncryptionToComplete</span><span class="sxs-lookup"><span data-stu-id="eddcd-326">-WaitForEncryptionToComplete</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-327">스위치</span><span class="sxs-lookup"><span data-stu-id="eddcd-327">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-328">암호화가 완료될 때까지 기다릴 지정</span><span class="sxs-lookup"><span data-stu-id="eddcd-328">Specify to wait for the encryption to complete</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="eddcd-329">-DoNotResumeSuspendedEncryption</span><span class="sxs-lookup"><span data-stu-id="eddcd-329">-DoNotResumeSuspendedEncryption</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-330">스위치</span><span class="sxs-lookup"><span data-stu-id="eddcd-330">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-331">배포 스크립트가 일시 중단된 암호화를 다시 시작하지 못하게 지정</span><span class="sxs-lookup"><span data-stu-id="eddcd-331">Specify that the deployment script will not resume suspended encryption</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="eddcd-332">-IgnoreEscrowOwnerAuthFailure</span><span class="sxs-lookup"><span data-stu-id="eddcd-332">-IgnoreEscrowOwnerAuthFailure</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-333">스위치</span><span class="sxs-lookup"><span data-stu-id="eddcd-333">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-334">TPM 소유자-에스크로 실패를 무시할지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-334">Specify to ignore TPM owner-auth escrow failure.</span></span> <span data-ttu-id="eddcd-335">MBAM이 TPM 소유자-auth를 읽을 수 없는 시나리오(예: TPM 자동 프로비저닝을 사용하도록 설정한 경우)에서 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-335">It should be used in the scenarios where MBAM is not able to read the TPM owner-auth, e.g. if TPM auto provisioning is enabled</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="eddcd-336">-IgnoreEscrowRecoveryKeyFailure</span><span class="sxs-lookup"><span data-stu-id="eddcd-336">-IgnoreEscrowRecoveryKeyFailure</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-337">스위치</span><span class="sxs-lookup"><span data-stu-id="eddcd-337">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-338">볼륨 복구 키 에스로 오류 무시를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-338">Specify to ignore volume recovery key escrow failure</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="eddcd-339">-IgnoreReportStatusFailure</span><span class="sxs-lookup"><span data-stu-id="eddcd-339">-IgnoreReportStatusFailure</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-340">스위치</span><span class="sxs-lookup"><span data-stu-id="eddcd-340">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="eddcd-341">상황 보고 실패를 무시하기 위해 지정</span><span class="sxs-lookup"><span data-stu-id="eddcd-341">Specify to ignore status reporting failure</span></span></p></td>
               </tr>
               </tbody>
               </table>

                 

**<span data-ttu-id="eddcd-342">MBAM 2.5 또는 이전 버전 배포의 일부로 BitLocker를 사용하도록 Windows</span><span class="sxs-lookup"><span data-stu-id="eddcd-342">To enable BitLocker using MBAM 2.5 or earlier as part of a Windows deployment</span></span>**

1.  <span data-ttu-id="eddcd-343">MBAM 클라이언트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-343">Install the MBAM Client.</span></span> <span data-ttu-id="eddcd-344">자세한 내용은 [How to Deploy the MBAM Client by Using a Command Line을 참조하십시오.](how-to-deploy-the-mbam-client-by-using-a-command-line.md)</span><span class="sxs-lookup"><span data-stu-id="eddcd-344">For instructions, see [How to Deploy the MBAM Client by Using a Command Line](how-to-deploy-the-mbam-client-by-using-a-command-line.md).</span></span>

2.  <span data-ttu-id="eddcd-345">컴퓨터를 도메인에 가입합니다(권장).</span><span class="sxs-lookup"><span data-stu-id="eddcd-345">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="eddcd-346">컴퓨터가 도메인에 가입되어 있지 않은 경우 복구 암호는 MBAM 키 복구 서비스에 저장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-346">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="eddcd-347">기본적으로 MBAM은 복구 키를 저장할 수 없는 경우 암호화가 발생하도록 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-347">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="eddcd-348">복구 키가 MBAM Server에 저장되기 전에 컴퓨터가 복구 모드로 시작되는 경우 복구 방법을 사용할 수 없는 것이 아니며 컴퓨터를 다시 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-348">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, no recovery method is available, and the computer has to be reimaged.</span></span>

3.  <span data-ttu-id="eddcd-349">관리자 권한으로 명령 프롬프트를 열고 MBAM 서비스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-349">Open a command prompt as an administrator, and stop the MBAM service.</span></span>

4.  <span data-ttu-id="eddcd-350">다음 명령을 입력하여 **서비스를 수동** 또는 On **demand로** 설정하십시오.</span><span class="sxs-lookup"><span data-stu-id="eddcd-350">Set the service to **Manual** or **On demand** by typing the following commands:</span></span>

    **<span data-ttu-id="eddcd-351">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="eddcd-351">net stop mbamagent</span></span>**

    **<span data-ttu-id="eddcd-352">sc config mbamagent start= demand</span><span class="sxs-lookup"><span data-stu-id="eddcd-352">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="eddcd-353">MBAM 클라이언트가 그룹 정책 설정을 무시하고 대신 암호화를 설정하여 해당 클라이언트 컴퓨터에 배포되는 Windows 수 있도록 레지스트리 값을 설정하십시오.</span><span class="sxs-lookup"><span data-stu-id="eddcd-353">Set the registry values so that the MBAM Client ignores the Group Policy settings and instead sets encryption to start the time Windows is deployed to that client computer.</span></span>

    **<span data-ttu-id="eddcd-354">주의</span><span class="sxs-lookup"><span data-stu-id="eddcd-354">Caution</span></span>**  
    <span data-ttu-id="eddcd-355">이 단계에서는 레지스트리를 수정하는 Windows 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-355">This step describes how to modify the Windows registry.</span></span> <span data-ttu-id="eddcd-356">레지스트리 편집기를 잘못 사용하면 레지스트리 편집기를 다시 설치해야 할 수 있는 심각한 문제가 Windows.</span><span class="sxs-lookup"><span data-stu-id="eddcd-356">Using Registry Editor incorrectly can cause serious issues that can require you to reinstall Windows.</span></span> <span data-ttu-id="eddcd-357">레지스트리 편집기가 잘못 사용되어 발생하는 문제를 해결할 수 있는 것은 보장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-357">We cannot guarantee that issues resulting from the incorrect use of Registry Editor can be resolved.</span></span> <span data-ttu-id="eddcd-358">레지스트리 편집기는 모든 위험에 노출될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-358">Use Registry Editor at your own risk.</span></span>

    1.  <span data-ttu-id="eddcd-359">운영 체제 전용 \*\*\*\* 암호화에 대한 TPM을 설정하고 Regedit.exe 실행한 다음 C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg에서 레지스트리 키 템플릿을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-359">Set the TPM for **Operating system only encryption**, run Regedit.exe, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

    2.  <span data-ttu-id="eddcd-360">이 Regedit.exe HKLM\\SOFTWARE\\Microsoft\\MBAM으로 이동하여 다음 표에 나와 있는 설정을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-360">In Regedit.exe, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

        **<span data-ttu-id="eddcd-361">참고</span><span class="sxs-lookup"><span data-stu-id="eddcd-361">Note</span></span>**  
        <span data-ttu-id="eddcd-362">여기에서 MBAM과 관련된 그룹 정책 설정 또는 레지스트리 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-362">You can set Group Policy settings or registry values related to MBAM here.</span></span> <span data-ttu-id="eddcd-363">이러한 설정은 이전에 설정한 값을 다시 정합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-363">These settings will override previously set values.</span></span>

        <span data-ttu-id="eddcd-364">레지스트리 항목 구성 설정</span><span class="sxs-lookup"><span data-stu-id="eddcd-364">Registry entry Configuration settings</span></span>

        <span data-ttu-id="eddcd-365">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="eddcd-365">DeploymentTime</span></span>

        <span data-ttu-id="eddcd-366">0 = 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-366">0 = Off</span></span>

        <span data-ttu-id="eddcd-367">1 = 배포 시간 정책 설정 사용(기본값) - 이 설정을 사용하여 클라이언트 컴퓨터에 배포할 Windows 암호화를 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-367">1 = Use deployment time policy settings (default) – use this setting to enable encryption at the time Windows is deployed to the client computer.</span></span>

        <span data-ttu-id="eddcd-368">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="eddcd-368">UseKeyRecoveryService</span></span>

        <span data-ttu-id="eddcd-369">0 = 키 에스로를 사용하지 않습니다(이 경우 다음 두 레지스트리 항목이 필요하지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="eddcd-369">0 = Do not use key escrow (the next two registry entries are not required in this case)</span></span>

        <span data-ttu-id="eddcd-370">1 = 키 복구 시스템에서 키 에스로 사용(기본값)</span><span class="sxs-lookup"><span data-stu-id="eddcd-370">1 = Use key escrow in Key Recovery system (default)</span></span>

        <span data-ttu-id="eddcd-371">이 설정은 MBAM이 복구 키를 저장할 수 있는 권장 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-371">This is the recommended setting, which enables MBAM to store the recovery keys.</span></span> <span data-ttu-id="eddcd-372">컴퓨터가 MBAM 키 복구 서비스와 통신할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-372">The computer must be able to communicate with the MBAM Key Recovery service.</span></span> <span data-ttu-id="eddcd-373">계속하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-373">Verify that the computer can communicate with the service before you proceed.</span></span>

        <span data-ttu-id="eddcd-374">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="eddcd-374">KeyRecoveryOptions</span></span>

        <span data-ttu-id="eddcd-375">0 = 복구 키만 업로드</span><span class="sxs-lookup"><span data-stu-id="eddcd-375">0 = Uploads Recovery Key only</span></span>

        <span data-ttu-id="eddcd-376">1 = 복구 키 및 키 복구 패키지 업로드(기본값)</span><span class="sxs-lookup"><span data-stu-id="eddcd-376">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

        <span data-ttu-id="eddcd-377">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="eddcd-377">KeyRecoveryServiceEndPoint</span></span>

        <span data-ttu-id="eddcd-378">키 복구 서비스를 실행하는 서버의 URL(예: http:// 컴퓨터 이름 &lt; &gt; /MBAMRecoveryAndHardwareService/CoreService.svc)으로 이 값을 설정하십시오.</span><span class="sxs-lookup"><span data-stu-id="eddcd-378">Set this value to the URL for the server running the Key Recovery service, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>


6.  <span data-ttu-id="eddcd-379">MBAM 클라이언트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-379">The MBAM Client will restart the system during the MBAM Client deployment.</span></span> <span data-ttu-id="eddcd-380">이 다시 시작할 준비가 되면 명령 프롬프트에서 관리자 권한으로 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-380">When you are ready for this restart, run the following command at a command prompt as an administrator:</span></span>

    **<span data-ttu-id="eddcd-381">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="eddcd-381">net start mbamagent</span></span>**

7.  <span data-ttu-id="eddcd-382">컴퓨터가 다시 시작될 때 BIOS에 메시지가 표시될 때 TPM 변경을 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-382">When the computers restarts, and the BIOS prompts you, accept the TPM change.</span></span>

8.  <span data-ttu-id="eddcd-383">Windows 클라이언트 운영 체제 이미징 프로세스 중에 암호화를 시작할 준비가 되면 관리자 권한으로 명령 프롬프트를 열고 \*\*\*\* 다음 명령을 입력하여 시작을 자동으로 설정하고 MBAM 클라이언트 에이전트를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="eddcd-383">During the Windows client operating system imaging process, when you are ready to start encryption, open a command prompt as an administrator, and type the following commands to set the start to **Automatic** and to restart the MBAM Client agent:</span></span>

    **<span data-ttu-id="eddcd-384">sc config mbamagent start= auto</span><span class="sxs-lookup"><span data-stu-id="eddcd-384">sc config mbamagent start= auto</span></span>**

    **<span data-ttu-id="eddcd-385">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="eddcd-385">net start mbamagent</span></span>**

9.  <span data-ttu-id="eddcd-386">무시 레지스트리 값을 삭제하려면 Regedit.exe 실행하고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목으로 이동하십시오.</span><span class="sxs-lookup"><span data-stu-id="eddcd-386">To delete the bypass registry values, run Regedit.exe, and go to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="eddcd-387">**MBAM 노드를 마우스** 오른쪽 단추로 클릭한 다음 삭제를 **클릭합니다.**</span><span class="sxs-lookup"><span data-stu-id="eddcd-387">Right-click the **MBAM** node, and then click **Delete**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eddcd-388">관련 항목</span><span class="sxs-lookup"><span data-stu-id="eddcd-388">Related topics</span></span>

[<span data-ttu-id="eddcd-389">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="eddcd-389">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="eddcd-390">MBAM 2.5 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="eddcd-390">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a><span data-ttu-id="eddcd-391">MBAM에 대한 제안이 있나요?</span><span class="sxs-lookup"><span data-stu-id="eddcd-391">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="eddcd-392">여기에 제안을 추가하거나 [투표합니다.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="eddcd-392">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="eddcd-393">MBAM 문제의 경우 [MBAM TechNet 포럼 을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)</span><span class="sxs-lookup"><span data-stu-id="eddcd-393">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
