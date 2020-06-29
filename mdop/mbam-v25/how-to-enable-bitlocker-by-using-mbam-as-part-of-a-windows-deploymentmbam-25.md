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
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826228"
---
# <span data-ttu-id="b971d-103">Windows 배포의 일환으로 MBAM을 사용하여 BitLocker를 활성화하는 방법</span><span class="sxs-lookup"><span data-stu-id="b971d-103">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>


<span data-ttu-id="b971d-104">이 항목에서는 Windows 이미징 및 배포 프로세스의 일부로 MBAM을 사용 하 여 최종 사용자의 컴퓨터에서 BitLocker를 사용 하도록 설정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-104">This topic explains how to enable BitLocker on an end user's computer by using MBAM as part of your Windows imaging and deployment process.</span></span> <span data-ttu-id="b971d-105">컴퓨터를 다시 시작할 때 검정색 화면이 표시 되는 경우 (단계 종료 이후 설치 후) 드라이브의 잠금을 해제할 수 없음을 나타내는 windows [10, 버전 1511에서 BitLocker를 미리 프로 비전 하는 경우 "windows 및 Configuration Manager 설정" 단계를 참조 하 여 이전 Windows 버전이 시작 되지 않도록](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-105">If you see a black screen at restart (after Install phase concludes) indicating that the drive cannot be unlocked, see [Earlier Windows versions don't start after "Setup Windows and Configuration Manager" step if Pre-Provision BitLocker is used with Windows 10, version 1511](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).</span></span>

**<span data-ttu-id="b971d-106">필수 조건:</span><span class="sxs-lookup"><span data-stu-id="b971d-106">Prerequisites:</span></span>**

-   <span data-ttu-id="b971d-107">기존 Windows 이미지 배포 프로세스 – Microsoft 배포 툴킷 (MDT), Microsoft System Center Configuration Manager 또는 일부 다른 이미징 도구 또는 프로세스가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-107">An existing Windows image deployment process – Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager, or some other imaging tool or process – must be in place</span></span>

-   <span data-ttu-id="b971d-108">TPM을 BIOS에서 사용 하도록 설정 하 고 OS에 표시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-108">TPM must be enabled in the BIOS and visible to the OS</span></span>

-   <span data-ttu-id="b971d-109">MBAM 서버 인프라는 현재 위치에 있고 액세스할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-109">MBAM server infrastructure must be in place and accessible</span></span>

-   <span data-ttu-id="b971d-110">BitLocker에 필요한 시스템 파티션을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-110">The system partition required by BitLocker must be created</span></span>

-   <span data-ttu-id="b971d-111">컴퓨터는 MBAM에서 BitLocker를 완전히 사용 하도록 설정 하기 전에 이미징 중에 도메인에 가입 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-111">The machine must be domain joined during imaging before MBAM fully enables BitLocker</span></span>

**<span data-ttu-id="b971d-112">Windows 배포의 일부로 MBAM 2.5 SP1을 사용 하 여 BitLocker를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b971d-112">To enable BitLocker using MBAM 2.5 SP1 as part of a Windows deployment</span></span>**

1. <span data-ttu-id="b971d-113">MBAM 2.5 SP1에서는 Windows 배포 중에 PowerShell 스크립트를 사용 하 여 BitLocker를 사용 하는 것이 권장 되는 접근 방법입니다 `Invoke-MbamClientDeployment.ps1` .</span><span class="sxs-lookup"><span data-stu-id="b971d-113">In MBAM 2.5 SP1, the recommended approach to enable BitLocker during a Windows Deployment is by using the `Invoke-MbamClientDeployment.ps1` PowerShell script.</span></span>

   -   <span data-ttu-id="b971d-114">이 `Invoke-MbamClientDeployment.ps1` 스크립트는 이미징 프로세스 중에 BitLocker를 enacts.</span><span class="sxs-lookup"><span data-stu-id="b971d-114">The `Invoke-MbamClientDeployment.ps1` script enacts BitLocker during the imaging process.</span></span> <span data-ttu-id="b971d-115">BitLocker 정책에 따라 필요할 때, MBAM 에이전트는 도메인 사용자가 이미징 후 처음으로 로그온 할 때 PIN 또는 암호를 만들도록 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-115">When required by BitLocker policy, the MBAM agent immediately prompts the domain user to create a PIN or password when the domain user first logs on after imaging.</span></span>

   -   <span data-ttu-id="b971d-116">MDT, System Center Configuration Manager 또는 독립 실행형 이미징 프로세스에서 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-116">Easy to use with MDT, System Center Configuration Manager, or standalone imaging processes</span></span>

   -   <span data-ttu-id="b971d-117">PowerShell 2.0 이상과 호환 가능</span><span class="sxs-lookup"><span data-stu-id="b971d-117">Compatible with PowerShell 2.0 or higher</span></span>

   -   <span data-ttu-id="b971d-118">TPM 키 보호기를 사용 하 여 OS 볼륨 암호화</span><span class="sxs-lookup"><span data-stu-id="b971d-118">Encrypt OS volume with TPM key protector</span></span>

   -   <span data-ttu-id="b971d-119">BitLocker 사전 프로비저닝 완전 지원</span><span class="sxs-lookup"><span data-stu-id="b971d-119">Fully support BitLocker pre-provisioning</span></span>

   -   <span data-ttu-id="b971d-120">선택적으로 FDDs 암호화</span><span class="sxs-lookup"><span data-stu-id="b971d-120">Optionally encrypt FDDs</span></span>

   -   <span data-ttu-id="b971d-121">Windows 7에 대 한 에스크로 TPM 소유자 인증, MBAM은 에스크로를 발생 시킬 TPM을 소유 하 고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-121">Escrow TPM OwnerAuth For Windows 7, MBAM must own the TPM for escrow to occur.</span></span>
   <span data-ttu-id="b971d-122">Windows 8.1의 경우 Windows 10 RTM 및 Windows 10 버전 1511, TPM 소유자의 에스크로 인증이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-122">For Windows 8.1, Windows 10 RTM and Windows 10 version 1511, escrow of TPM OwnerAuth is supported.</span></span>
   <span data-ttu-id="b971d-123">Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-123">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="b971d-124">Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-124">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="b971d-125">자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b971d-125">See [TPM owner password](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

   -   <span data-ttu-id="b971d-126">에스크로 복구 키 및 복구 키 패키지</span><span class="sxs-lookup"><span data-stu-id="b971d-126">Escrow recovery keys and recovery key packages</span></span>

   -   <span data-ttu-id="b971d-127">즉시 암호화 상태 보고</span><span class="sxs-lookup"><span data-stu-id="b971d-127">Report encryption status immediately</span></span>

   -   <span data-ttu-id="b971d-128">새 WMI 공급자</span><span class="sxs-lookup"><span data-stu-id="b971d-128">New WMI providers</span></span>

   -   <span data-ttu-id="b971d-129">자세한 로깅</span><span class="sxs-lookup"><span data-stu-id="b971d-129">Detailed logging</span></span>

   -   <span data-ttu-id="b971d-130">강력한 오류 처리</span><span class="sxs-lookup"><span data-stu-id="b971d-130">Robust error handling</span></span>

   <span data-ttu-id="b971d-131">`Invoke-MbamClientDeployment.ps1` [Microsoft.com 다운로드 센터](https://www.microsoft.com/download/details.aspx?id=54439)에서 스크립트를 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-131">You can download the `Invoke-MbamClientDeployment.ps1` script from [Microsoft.com Download Center](https://www.microsoft.com/download/details.aspx?id=54439).</span></span> <span data-ttu-id="b971d-132">이는 배포 시스템에서 MBAM 서버를 사용 하 여 BitLocker 드라이브 암호화 및 레코드 복구 키를 구성 하기 위해 호출할 주 스크립트입니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-132">This is the main script that your deployment system will call to configure BitLocker drive encryption and record recovery keys with the MBAM Server.</span></span>

   <span data-ttu-id="b971d-133">**MBAM에 대 한 WMI 배포 방법:** 이 PowerShell 스크립트를 사용 하 여 BitLocker 사용을 지원 하기 위해 다음 WMI 메서드가 MBAM 2.5 SP1에 추가 되었습니다 `Invoke-MbamClientDeployment.ps1` .</span><span class="sxs-lookup"><span data-stu-id="b971d-133">**WMI deployment methods for MBAM:** The following WMI methods have been added in MBAM 2.5 SP1 to support enabling BitLocker by using the `Invoke-MbamClientDeployment.ps1` PowerShell script.</span></span>

   <a href="" id="mbam-machine-wmi-class"></a><span data-ttu-id="b971d-134">**Mbam \ _MACHINE WMI 클래스** 
    **PrepareTpmAndEscrowOwnerAuth:** TPM 소유자 인증을 읽고 MBAM 복구 서비스를 사용 하 여이를 MBAM 데이터베이스로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-134">**MBAM\_Machine WMI Class**
**PrepareTpmAndEscrowOwnerAuth:** Reads the TPM OwnerAuth and sends it to the MBAM recovery database by using the MBAM recovery service.</span></span> <span data-ttu-id="b971d-135">TPM이 소유 되지 않고 자동 프로비저닝이 켜져 있지 않으면 TPM 소유자 인증을 생성 하 고 소유권을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-135">If the TPM is not owned and auto-provisioning is not on, it generates a TPM OwnerAuth and takes ownership.</span></span> <span data-ttu-id="b971d-136">실패 하면 문제 해결을 위해 오류 코드가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-136">If it fails, an error code is returned for troubleshooting.</span></span>

   <span data-ttu-id="b971d-137">**참고** Windows 10 버전 1607 이상에서는 Windows만 TPM 소유권을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-137">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="b971d-138">Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-138">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="b971d-139">자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b971d-139">See [TPM owner password](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

| <span data-ttu-id="b971d-140">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b971d-140">Parameter</span></span> | <span data-ttu-id="b971d-141">설명</span><span class="sxs-lookup"><span data-stu-id="b971d-141">Description</span></span> |
| -------- | ----------- |
| <span data-ttu-id="b971d-142">RecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="b971d-142">RecoveryServiceEndPoint</span></span> | <span data-ttu-id="b971d-143">MBAM 복구 서비스 끝점을 지정 하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-143">A string specifying the MBAM recovery service endpoint.</span></span> |

<span data-ttu-id="b971d-144">일반적인 오류 메시지 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-144">Here are a list of common error messages:</span></span>

| <span data-ttu-id="b971d-145">일반적인 반환 값</span><span class="sxs-lookup"><span data-stu-id="b971d-145">Common return values</span></span> | <span data-ttu-id="b971d-146">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="b971d-146">Error message</span></span> |
| -------------------- | ------------- |
|  **<span data-ttu-id="b971d-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="b971d-147">S_OK</span></span>**<br /><span data-ttu-id="b971d-148">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="b971d-148">0 (0x0)</span></span> | <span data-ttu-id="b971d-149">메서드가 성공적으로 수행 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-149">The method was successful.</span></span> |
| **<span data-ttu-id="b971d-150">MBAM_E_TPM_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="b971d-150">MBAM_E_TPM_NOT_PRESENT</span></span>**<br /><span data-ttu-id="b971d-151">2147746304 (0x80040200)</span><span class="sxs-lookup"><span data-stu-id="b971d-151">2147746304 (0x80040200)</span></span> | <span data-ttu-id="b971d-152">TPM이 컴퓨터에 없거나 BIOS 구성에서 사용 하지 않도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-152">TPM is not present in the computer or is disabled in the BIOS configuration.</span></span> |
| **<span data-ttu-id="b971d-153">MBAM_E_TPM_INCORRECT_STATE</span><span class="sxs-lookup"><span data-stu-id="b971d-153">MBAM_E_TPM_INCORRECT_STATE</span></span>**<br /><span data-ttu-id="b971d-154">2147746305 (0x80040201)</span><span class="sxs-lookup"><span data-stu-id="b971d-154">2147746305 (0x80040201)</span></span> | <span data-ttu-id="b971d-155">TPM의 상태가 올바르지 않습니다 (사용 가능, 활성화 됨, 소유자 설치가 허용 됨).</span><span class="sxs-lookup"><span data-stu-id="b971d-155">TPM is not in the correct state (enabled, activated and owner installation allowed).</span></span> |
| **<span data-ttu-id="b971d-156">MBAM_E_TPM_AUTO_PROVISIONING_PENDING</span><span class="sxs-lookup"><span data-stu-id="b971d-156">MBAM_E_TPM_AUTO_PROVISIONING_PENDING</span></span>**<br /><span data-ttu-id="b971d-157">2147746306 (0x80040202)</span><span class="sxs-lookup"><span data-stu-id="b971d-157">2147746306 (0x80040202)</span></span> | <span data-ttu-id="b971d-158">MBAM은 자동 프로비저닝이 보류 중 이므로 TPM의 소유권을 가질 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-158">MBAM cannot take ownership of TPM because auto-provisioning is pending.</span></span> <span data-ttu-id="b971d-159">자동 프로비저닝이 완료 된 후 다시 시도해 주십시오.</span><span class="sxs-lookup"><span data-stu-id="b971d-159">Try again after auto-provisioning is completed.</span></span> |
| **<span data-ttu-id="b971d-160">MBAM_E_TPM_OWNERAUTH_READFAIL</span><span class="sxs-lookup"><span data-stu-id="b971d-160">MBAM_E_TPM_OWNERAUTH_READFAIL</span></span>**<br /><span data-ttu-id="b971d-161">2147746307 (0x80040203)</span><span class="sxs-lookup"><span data-stu-id="b971d-161">2147746307 (0x80040203)</span></span> | <span data-ttu-id="b971d-162">MBAM은 TPM 소유자 권한 부여 값을 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-162">MBAM cannot read the TPM owner authorization value.</span></span> <span data-ttu-id="b971d-163">성공적으로 에스크로 한 후에도 값이 제거 되었을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-163">The value might have been removed after a successful escrow.</span></span> <span data-ttu-id="b971d-164">Windows 7에서는 TPM을 다른 사용자가 소유한 경우 MBAM에서 값을 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-164">On Windows 7, MBAM cannot read the value if the TPM is owned by others.</span></span> |
| **<span data-ttu-id="b971d-165">MBAM_E_REBOOT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="b971d-165">MBAM_E_REBOOT_REQUIRED</span></span>**<br /><span data-ttu-id="b971d-166">2147746308 (0x80040204)</span><span class="sxs-lookup"><span data-stu-id="b971d-166">2147746308 (0x80040204)</span></span> | <span data-ttu-id="b971d-167">TPM을 올바른 상태로 설정 하려면 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-167">The computer must be restarted to set TPM to the correct state.</span></span> <span data-ttu-id="b971d-168">컴퓨터를 수동으로 다시 부팅 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-168">You might need to manually reboot the computer.</span></span> |
| **<span data-ttu-id="b971d-169">MBAM_E_SHUTDOWN_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="b971d-169">MBAM_E_SHUTDOWN_REQUIRED</span></span>**<br /><span data-ttu-id="b971d-170">2147746309 (0x80040205)</span><span class="sxs-lookup"><span data-stu-id="b971d-170">2147746309 (0x80040205)</span></span> | <span data-ttu-id="b971d-171">TPM을 올바른 상태로 설정 하려면 컴퓨터를 종료 하 고 다시 켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-171">The computer must be shut down and turned back on to set TPM to the correct state.</span></span> <span data-ttu-id="b971d-172">컴퓨터를 수동으로 다시 부팅 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-172">You might need to manually reboot the computer.</span></span> |
| **<span data-ttu-id="b971d-173">WS_E_ENDPOINT_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="b971d-173">WS_E_ENDPOINT_ACCESS_DENIED</span></span>**<br /><span data-ttu-id="b971d-174">2151481349 (0X800005)</span><span class="sxs-lookup"><span data-stu-id="b971d-174">2151481349 (0x803D0005)</span></span> | <span data-ttu-id="b971d-175">원격 끝점에 의해 액세스가 거부 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-175">Access was denied by the remote endpoint.</span></span> |
| **<span data-ttu-id="b971d-176">WS_E_ENDPOINT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b971d-176">WS_E_ENDPOINT_NOT_FOUND</span></span>**<br /><span data-ttu-id="b971d-177">2151481357 (0x803D000D)</span><span class="sxs-lookup"><span data-stu-id="b971d-177">2151481357 (0x803D000D)</span></span> | <span data-ttu-id="b971d-178">원격 끝점이 없거나 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-178">The remote endpoint does not exist or could not be located.</span></span> |
| <span data-ttu-id="b971d-179">\* \* WS_E_ENDPOINT_FAILURE</span><span class="sxs-lookup"><span data-stu-id="b971d-179">\*\*WS_E_ENDPOINT_FAILURE</span></span><br /><span data-ttu-id="b971d-180">2151481357 (0X80이상 000F)</span><span class="sxs-lookup"><span data-stu-id="b971d-180">2151481357 (0x803D000F)</span></span> | <span data-ttu-id="b971d-181">원격 끝점이 요청을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-181">The remote endpoint could not process the request.</span></span> |
| **<span data-ttu-id="b971d-182">WS_E_ENDPOINT_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="b971d-182">WS_E_ENDPOINT_UNREACHABLE</span></span>**<br /><span data-ttu-id="b971d-183">2151481360 (0X80이상 0010)</span><span class="sxs-lookup"><span data-stu-id="b971d-183">2151481360 (0x803D0010)</span></span> | <span data-ttu-id="b971d-184">원격 끝점에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-184">The remote endpoint was not reachable.</span></span> |
| **<span data-ttu-id="b971d-185">WS_E_ENDPOINT_FAULT_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="b971d-185">WS_E_ENDPOINT_FAULT_RECEIVED</span></span>**<br /><span data-ttu-id="b971d-186">2151481363 (0X80이상 0013)</span><span class="sxs-lookup"><span data-stu-id="b971d-186">2151481363 (0x803D0013)</span></span> | <span data-ttu-id="b971d-187">원격 끝점에서 오류가 포함 된 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-187">A message containing a fault was received from the remote endpoint.</span></span> <span data-ttu-id="b971d-188">올바른 서비스 끝점에 연결 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-188">Make sure you are connecting to the correct service endpoint.</span></span> |
| <span data-ttu-id="b971d-189">**WS_E_INVALID_ENDPOINT_URL** 2151481376 (0X80이상 0020)</span><span class="sxs-lookup"><span data-stu-id="b971d-189">**WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020)</span></span> | <span data-ttu-id="b971d-190">끝점 주소 URL이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-190">The endpoint address URL is not valid.</span></span> <span data-ttu-id="b971d-191">URL은 "http" 또는 "https"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-191">The URL must start with “http” or “https”.</span></span> |

   <span data-ttu-id="b971d-192">**보고서 상태:** 볼륨의 준수 상태를 읽고 MBAM 상태 보고 서비스를 사용 하 여이를 MBAM 준수 상태 데이터베이스로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-192">**ReportStatus:** Reads the compliance status of the volume and sends it to the MBAM compliance status database by using the MBAM status reporting service.</span></span> <span data-ttu-id="b971d-193">상태에는 암호화 수준, 보호기 유형, 보호기 상태 및 암호화 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-193">The status includes cipher strength, protector type, protector state and encryption state.</span></span> <span data-ttu-id="b971d-194">실패 하면 문제 해결을 위해 오류 코드가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-194">If it fails, an error code is returned for troubleshooting.</span></span>

   | <span data-ttu-id="b971d-195">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b971d-195">Parameter</span></span> | <span data-ttu-id="b971d-196">설명</span><span class="sxs-lookup"><span data-stu-id="b971d-196">Description</span></span> |
   | --------- | ----------- |
   | <span data-ttu-id="b971d-197">ReportingServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="b971d-197">ReportingServiceEndPoint</span></span> | <span data-ttu-id="b971d-198">MBAM 상태 보고 서비스 끝점을 지정 하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-198">A string specifying the MBAM status reporting service endpoint.</span></span> |

   <span data-ttu-id="b971d-199">일반적인 오류 메시지 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-199">Here are a list of common error messages:</span></span>

   | <span data-ttu-id="b971d-200">일반적인 반환 값</span><span class="sxs-lookup"><span data-stu-id="b971d-200">Common return values</span></span> | <span data-ttu-id="b971d-201">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="b971d-201">Error message</span></span> |
   | -------------------- | ------------- |
   | **<span data-ttu-id="b971d-202">S_OK</span><span class="sxs-lookup"><span data-stu-id="b971d-202">S_OK</span></span>**<br /> <span data-ttu-id="b971d-203">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="b971d-203">0 (0x0)</span></span> | <span data-ttu-id="b971d-204">메서드 성공</span><span class="sxs-lookup"><span data-stu-id="b971d-204">The method was successful</span></span> |
   | **<span data-ttu-id="b971d-205">WS_E_ENDPOINT_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="b971d-205">WS_E_ENDPOINT_ACCESS_DENIED</span></span>**<br /><span data-ttu-id="b971d-206">2151481349 (0X800005)</span><span class="sxs-lookup"><span data-stu-id="b971d-206">2151481349 (0x803D0005)</span></span> | <span data-ttu-id="b971d-207">원격 끝점에 의해 액세스가 거부 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-207">Access was denied by the remote endpoint.</span></span>|
   | **<span data-ttu-id="b971d-208">WS_E_ENDPOINT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b971d-208">WS_E_ENDPOINT_NOT_FOUND</span></span>**<br /><span data-ttu-id="b971d-209">2151481357 (0x803D000D)</span><span class="sxs-lookup"><span data-stu-id="b971d-209">2151481357 (0x803D000D)</span></span> | <span data-ttu-id="b971d-210">원격 끝점이 없거나 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-210">The remote endpoint does not exist or could not be located.</span></span> |
   | **<span data-ttu-id="b971d-211">WS_E_ENDPOINT_FAILURE</span><span class="sxs-lookup"><span data-stu-id="b971d-211">WS_E_ENDPOINT_FAILURE</span></span>**<br /> <span data-ttu-id="b971d-212">2151481357 (0X80이상 000F)</span><span class="sxs-lookup"><span data-stu-id="b971d-212">2151481357 (0x803D000F)</span></span> | <span data-ttu-id="b971d-213">원격 끝점이 요청을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-213">The remote endpoint could not process the request.</span></span> |
   | **<span data-ttu-id="b971d-214">WS_E_ENDPOINT_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="b971d-214">WS_E_ENDPOINT_UNREACHABLE</span></span>**<br /><span data-ttu-id="b971d-215">2151481360 (0X80이상 0010)</span><span class="sxs-lookup"><span data-stu-id="b971d-215">2151481360 (0x803D0010)</span></span> | <span data-ttu-id="b971d-216">원격 끝점에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-216">The remote endpoint was not reachable.</span></span> |
   | **<span data-ttu-id="b971d-217">WS_E_ENDPOINT_FAULT_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="b971d-217">WS_E_ENDPOINT_FAULT_RECEIVED</span></span>**<br /><span data-ttu-id="b971d-218">2151481363 (0X80이상 0013)</span><span class="sxs-lookup"><span data-stu-id="b971d-218">2151481363 (0x803D0013)</span></span> | <span data-ttu-id="b971d-219">원격 끝점에서 오류가 포함 된 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-219">A message containing a fault was received from the remote endpoint.</span></span> <span data-ttu-id="b971d-220">올바른 서비스 끝점에 연결 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-220">Make sure you are connecting to the correct service endpoint.</span></span> |
   | **<span data-ttu-id="b971d-221">WS_E_INVALID_ENDPOINT_URL</span><span class="sxs-lookup"><span data-stu-id="b971d-221">WS_E_INVALID_ENDPOINT_URL</span></span>**<br /><span data-ttu-id="b971d-222">2151481376 (0X80.0020)</span><span class="sxs-lookup"><span data-stu-id="b971d-222">2151481376 (0x803D0020)</span></span> | <span data-ttu-id="b971d-223">끝점 주소 URL이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-223">The endpoint address URL is not valid.</span></span> <span data-ttu-id="b971d-224">URL은 "http" 또는 "https"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-224">The URL must start with “http” or “https”.</span></span> |

   <a href="" id="mbam-volume-wmi-class"></a><span data-ttu-id="b971d-225">**Mbam \ _VOLUME WMI 클래스** **EscrowRecoveryKey:** 볼륨의 복구 숫자 암호와 키 패키지를 읽고 mbam 복구 서비스를 사용 하 여 mbam 복구 데이터베이스로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-225">**MBAM\_Volume WMI Class** **EscrowRecoveryKey:** Reads the recovery numerical password and key package of the volume and sends them to the MBAM recovery database by using the MBAM recovery service.</span></span> <span data-ttu-id="b971d-226">실패 하면 문제 해결을 위해 오류 코드가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-226">If it fails, an error code is returned for troubleshooting.</span></span>

   | <span data-ttu-id="b971d-227">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b971d-227">Parameter</span></span> | <span data-ttu-id="b971d-228">설명</span><span class="sxs-lookup"><span data-stu-id="b971d-228">Description</span></span> |
   | --------- | ----------- |
   | <span data-ttu-id="b971d-229">RecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="b971d-229">RecoveryServiceEndPoint</span></span> | <span data-ttu-id="b971d-230">MBAM 복구 서비스 끝점을 지정 하는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-230">A string specifying the MBAM recovery service endpoint.</span></span> |

   <span data-ttu-id="b971d-231">일반적인 오류 메시지 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-231">Here are a list of common error messages:</span></span>

   | <span data-ttu-id="b971d-232">일반적인 반환 값</span><span class="sxs-lookup"><span data-stu-id="b971d-232">Common return values</span></span> | <span data-ttu-id="b971d-233">오류 메시지</span><span class="sxs-lookup"><span data-stu-id="b971d-233">Error message</span></span> |
   | -------------------- | ------------- |
   | **<span data-ttu-id="b971d-234">S_OK</span><span class="sxs-lookup"><span data-stu-id="b971d-234">S_OK</span></span>**<br /><span data-ttu-id="b971d-235">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="b971d-235">0 (0x0)</span></span> | <span data-ttu-id="b971d-236">메서드 성공</span><span class="sxs-lookup"><span data-stu-id="b971d-236">The method was successful</span></span> |
   | **<span data-ttu-id="b971d-237">FVE_E_LOCKED_VOLUME</span><span class="sxs-lookup"><span data-stu-id="b971d-237">FVE_E_LOCKED_VOLUME</span></span>**<br /><span data-ttu-id="b971d-238">2150694912 (0x80310000)</span><span class="sxs-lookup"><span data-stu-id="b971d-238">2150694912 (0x80310000)</span></span> | <span data-ttu-id="b971d-239">볼륨이 잠겼습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-239">The volume is locked.</span></span> |
   | **<span data-ttu-id="b971d-240">FVE_E_PROTECTOR_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b971d-240">FVE_E_PROTECTOR_NOT_FOUND</span></span>**<br /><span data-ttu-id="b971d-241">2150694963 (0x80310033)</span><span class="sxs-lookup"><span data-stu-id="b971d-241">2150694963 (0x80310033)</span></span> | <span data-ttu-id="b971d-242">볼륨에 대 한 숫자 암호 보호기를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-242">A Numerical Password protector was not found for the volume.</span></span> |
   | **<span data-ttu-id="b971d-243">WS_E_ENDPOINT_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="b971d-243">WS_E_ENDPOINT_ACCESS_DENIED</span></span>**<br /><span data-ttu-id="b971d-244">2151481349 (0X800005)</span><span class="sxs-lookup"><span data-stu-id="b971d-244">2151481349 (0x803D0005)</span></span> | <span data-ttu-id="b971d-245">원격 끝점에 의해 액세스가 거부 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-245">Access was denied by the remote endpoint.</span></span> |
   | **<span data-ttu-id="b971d-246">WS_E_ENDPOINT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b971d-246">WS_E_ENDPOINT_NOT_FOUND</span></span>**<br /><span data-ttu-id="b971d-247">2151481357 (0x803D000D)</span><span class="sxs-lookup"><span data-stu-id="b971d-247">2151481357 (0x803D000D)</span></span> | <span data-ttu-id="b971d-248">원격 끝점이 없거나 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-248">The remote endpoint does not exist or could not be located.</span></span> |
   | **<span data-ttu-id="b971d-249">WS_E_ENDPOINT_FAILURE</span><span class="sxs-lookup"><span data-stu-id="b971d-249">WS_E_ENDPOINT_FAILURE</span></span>**<br /><span data-ttu-id="b971d-250">2151481357 (0X80이상 000F)</span><span class="sxs-lookup"><span data-stu-id="b971d-250">2151481357 (0x803D000F)</span></span> | <span data-ttu-id="b971d-251">원격 끝점이 요청을 처리할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-251">The remote endpoint could not process the request.</span></span> |
   | **<span data-ttu-id="b971d-252">WS_E_ENDPOINT_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="b971d-252">WS_E_ENDPOINT_UNREACHABLE</span></span>**<br /><span data-ttu-id="b971d-253">2151481360 (0X80이상 0010)</span><span class="sxs-lookup"><span data-stu-id="b971d-253">2151481360 (0x803D0010)</span></span> | <span data-ttu-id="b971d-254">원격 끝점에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-254">The remote endpoint was not reachable.</span></span> |
   | **<span data-ttu-id="b971d-255">WS_E_ENDPOINT_FAULT_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="b971d-255">WS_E_ENDPOINT_FAULT_RECEIVED</span></span>**<br /><span data-ttu-id="b971d-256">2151481363 (0X80이상 0013)</span><span class="sxs-lookup"><span data-stu-id="b971d-256">2151481363 (0x803D0013)</span></span> | <span data-ttu-id="b971d-257">원격 끝점에서 오류가 포함 된 메시지를 받았습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-257">A message containing a fault was received from the remote endpoint.</span></span> <span data-ttu-id="b971d-258">올바른 서비스 끝점에 연결 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-258">Make sure you are connecting to the correct service endpoint.</span></span> |
   | **<span data-ttu-id="b971d-259">WS_E_INVALID_ENDPOINT_URL</span><span class="sxs-lookup"><span data-stu-id="b971d-259">WS_E_INVALID_ENDPOINT_URL</span></span>**<br /><span data-ttu-id="b971d-260">2151481376 (0X80.0020)</span><span class="sxs-lookup"><span data-stu-id="b971d-260">2151481376 (0x803D0020)</span></span> | <span data-ttu-id="b971d-261">끝점 주소 URL이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-261">The endpoint address URL is not valid.</span></span> <span data-ttu-id="b971d-262">URL은 "http" 또는 "https"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-262">The URL must start with “http” or “https”.</span></span> |
     

2. **<span data-ttu-id="b971d-263">MDT (Microsoft Deployment Toolkit) 및 PowerShell을 사용 하 여 MBAM 배포</span><span class="sxs-lookup"><span data-stu-id="b971d-263">Deploy MBAM by using Microsoft Deployment Toolkit (MDT) and PowerShell</span></span>**

   1.  <span data-ttu-id="b971d-264">MDT에서 새 배포 공유를 만들거나 기존 배포 공유를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-264">In MDT, create a new deployment share or open an existing deployment share.</span></span>

       **<span data-ttu-id="b971d-265">참고</span><span class="sxs-lookup"><span data-stu-id="b971d-265">Note</span></span>**  
       <span data-ttu-id="b971d-266">`Invoke-MbamClientDeployment.ps1`PowerShell 스크립트는 모든 이미징 프로세스 또는 도구와 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-266">The `Invoke-MbamClientDeployment.ps1` PowerShell script can be used with any imaging process or tool.</span></span> <span data-ttu-id="b971d-267">이 섹션에서는 MDT를 사용 하 여 통합 하는 방법을 보여 주지만,이 단계는 다른 프로세스나 도구와 통합 하는 것과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-267">This section shows how to integrate it by using MDT, but the steps are similar to integrating it with any other process or tool.</span></span>

       **<span data-ttu-id="b971d-268">주의</span><span class="sxs-lookup"><span data-stu-id="b971d-268">Caution</span></span>**  
       <span data-ttu-id="b971d-269">WinPE (BitLocker 사전 프로비저닝)를 사용 하는 경우 TPM 소유자 권한 부여 값을 유지 관리 하려면 `SaveWinPETpmOwnerAuth.wsf` 설치가 전체 운영 체제로 다시 부팅 되기 바로 전에 WinPE에서 스크립트를 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-269">If you are using BitLocker pre-provisioning (WinPE) and want to maintain the TPM owner authorization value, you must add the `SaveWinPETpmOwnerAuth.wsf` script in WinPE immediately before the installation reboots into the full operating system.</span></span> **<span data-ttu-id="b971d-270">이 스크립트를 사용 하지 않으면 다시 부팅할 때 TPM 소유자 권한 부여 값이 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-270">If you do not use this script, you will lose the TPM owner authorization value on reboot.</span></span>**

   2.  <span data-ttu-id="b971d-271">`Invoke-MbamClientDeployment.ps1` \*\* &lt; Deploymentshare. &gt; \ \ 스크립트\*\*에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-271">Copy `Invoke-MbamClientDeployment.ps1` to **&lt;DeploymentShare&gt;\\Scripts**.</span></span> <span data-ttu-id="b971d-272">사전 배포를 사용 하는 경우 `SaveWinPETpmOwnerAuth.wsf` 파일을 \*\* &lt; deploymentshare &gt; \ 스크립트\*\*에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-272">If you are using pre-provisioning, copy the `SaveWinPETpmOwnerAuth.wsf` file into **&lt;DeploymentShare&gt;\\Scripts**.</span></span>

   3.  <span data-ttu-id="b971d-273">배포 공유의 응용 프로그램 노드에 MBAM 2.5 SP1 클라이언트 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-273">Add the MBAM 2.5 SP1 client application to the Applications node in the deployment share.</span></span>

       1.  <span data-ttu-id="b971d-274">**응용 프로그램** 노드에서 **새 응용 프로그램**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-274">Under the **Applications** node, click **New Application**.</span></span>

       2.  <span data-ttu-id="b971d-275">**원본 파일을 사용 하 여 응용 프로그램을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-275">Select **Application with Source Files**.</span></span> <span data-ttu-id="b971d-276">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-276">Click **Next**.</span></span>

       3.  <span data-ttu-id="b971d-277">**응용 프로그램 이름**에 "mbam 2.5 SP1 클라이언트"를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-277">In **Application Name**, type “MBAM 2.5 SP1 Client”.</span></span> <span data-ttu-id="b971d-278">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-278">Click **Next**.</span></span>

       4.  <span data-ttu-id="b971d-279">을 (를) 포함 하는 디렉터리로 이동 `MBAMClientSetup-<Version>.msi` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-279">Browse to the directory containing `MBAMClientSetup-<Version>.msi`.</span></span> <span data-ttu-id="b971d-280">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-280">Click **Next**.</span></span>

       5.  <span data-ttu-id="b971d-281">"MBAM 2.5 SP1 클라이언트"를 만들 디렉터리로 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-281">Type “MBAM 2.5 SP1 Client” as the directory to create.</span></span> <span data-ttu-id="b971d-282">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-282">Click **Next**.</span></span>

       6.  <span data-ttu-id="b971d-283">`msiexec /i MBAMClientSetup-<Version>.msi /quiet`명령줄에서 Enter 키를 누르십시오.</span><span class="sxs-lookup"><span data-stu-id="b971d-283">Enter `msiexec /i MBAMClientSetup-<Version>.msi /quiet` at the command line.</span></span> <span data-ttu-id="b971d-284">**다음**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-284">Click **Next**.</span></span>

       7.  <span data-ttu-id="b971d-285">나머지 기본값을 적용 하 여 새 응용 프로그램 마법사를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-285">Accept the remaining defaults to complete the New Application wizard.</span></span>

   4.  <span data-ttu-id="b971d-286">MDT에서 배포 공유의 이름을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-286">In MDT, right-click the name of the deployment share and click **Properties**.</span></span> <span data-ttu-id="b971d-287">**규칙** 탭을 클릭 합니다. 다음 줄을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-287">Click the **Rules** tab. Add the following lines:</span></span>

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       <span data-ttu-id="b971d-288">확인을 클릭 하 여 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-288">Click OK to close the window.</span></span>

   5.  <span data-ttu-id="b971d-289">작업 순서 노드에서 Windows 배포에 사용 되는 기존 작업 순서를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-289">Under the Task Sequences node, edit an existing task sequence used for Windows Deployment.</span></span> <span data-ttu-id="b971d-290">원하는 경우 **작업** 순서 노드를 마우스 오른쪽 단추로 클릭 하 고 **새 작업 순서**를 선택한 다음 마법사를 완료 하 여 새 작업 순서를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-290">If you want, you can create a new task sequence by right-clicking the **Task Sequences** node, selecting **New Task Sequence**, and completing the wizard.</span></span>

       <span data-ttu-id="b971d-291">선택한 작업 순서의 **작업 순서** 탭에서 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-291">On the **Task Sequence** tab of the selected task sequence, perform these steps:</span></span>

       1.  <span data-ttu-id="b971d-292">WinPE에서 BitLocker를 사용 하 여 사용 하는 공간만 암호화 하려면 **사전 설치** 폴더에서 선택적 작업 **(bitlocker 사용)** 을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-292">Under the **Preinstall** folder, enable the optional task **Enable BitLocker (Offline)** if you want BitLocker enabled in WinPE, which encrypts used space only.</span></span>

       2.  <span data-ttu-id="b971d-293">사전 프로비저닝을 사용할 때 TPM 소유자 인증을 유지 하 고, 나중에 MBAM에서 에스크로를 허용 하려면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-293">To persist TPM OwnerAuth when using pre-provisioning, allowing MBAM to escrow it later, do the following:</span></span>

           1.  <span data-ttu-id="b971d-294">**설치 운영 체제** 찾기 단계</span><span class="sxs-lookup"><span data-stu-id="b971d-294">Find the **Install Operating System** step</span></span>

           2.  <span data-ttu-id="b971d-295">새 **실행** 명령줄을 추가 하는 단계</span><span class="sxs-lookup"><span data-stu-id="b971d-295">Add a new **Run Command Line** step after it</span></span>

           3.  <span data-ttu-id="b971d-296">단계의 이름 **TPM 소유자 인증 유지**</span><span class="sxs-lookup"><span data-stu-id="b971d-296">Name the step **Persist TPM OwnerAuth**</span></span>

           4.  <span data-ttu-id="b971d-297">명령줄을 `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **참고:** windows 10, 버전 1607 이상에서는 windows만 TPM 소유권을 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-297">Set the command line to `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
**Note:** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="b971d-298">Addiiton에서 Windows는 TPM을 구축할 때 TPM 소유자 암호를 유지 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-298">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="b971d-299">자세한 내용은 [TPM 소유자 암호](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b971d-299">See [TPM owner password](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

       3.  <span data-ttu-id="b971d-300">**상태 복원** 폴더에서 **BitLocker 사용 가능** 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-300">In the **State Restore** folder, delete the **Enable BitLocker** task.</span></span>

       4.  <span data-ttu-id="b971d-301">**사용자 지정 작업**아래에 있는 **상태 복원** 폴더에서 새 **설치 응용 프로그램** 작업을 만들고 이름에 **mbam 에이전트를 설치**합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-301">In the **State Restore** folder under **Custom Tasks**, create a new **Install Application** task and name it **Install MBAM Agent**.</span></span> <span data-ttu-id="b971d-302">**단일 응용 프로그램 설치** 라디오 단추를 클릭 하 고 이전에 만든 mbam 2.5 SP1 클라이언트 응용 프로그램을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-302">Click the **Install Single Application** radio button and browse to the MBAM 2.5 SP1 client application created earlier.</span></span>

       5.  <span data-ttu-id="b971d-303">**사용자 지정 작업**아래에 있는 **상태 복원** 폴더에서 다음 설정을 사용 하 여 새 **실행 PowerShell 스크립트** 작업 (mbam 2.5 SP1 클라이언트 응용 프로그램 단계 이후)을 만듭니다 (환경에 맞게 매개 변수 업데이트).</span><span class="sxs-lookup"><span data-stu-id="b971d-303">In the **State Restore** folder under **Custom Tasks**, create a new **Run PowerShell Script** task (after the MBAM 2.5 SP1 Client application step) with the following settings (update the parameters as appropriate for your environment):</span></span>

           -   <span data-ttu-id="b971d-304">이름: MBAM에 대 한 BitLocker 구성</span><span class="sxs-lookup"><span data-stu-id="b971d-304">Name: Configure BitLocker for MBAM</span></span>

           -   <span data-ttu-id="b971d-305">PowerShell 스크립트:</span><span class="sxs-lookup"><span data-stu-id="b971d-305">PowerShell script:</span></span> `Invoke-MbamClientDeployment.ps1`

           -   <span data-ttu-id="b971d-306">변수</span><span class="sxs-lookup"><span data-stu-id="b971d-306">Parameters:</span></span>

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="b971d-307">-RecoveryServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b971d-307">-RecoveryServiceEndpoint</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-308">필수</span><span class="sxs-lookup"><span data-stu-id="b971d-308">Required</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-309">MBAM 복구 서비스 끝점</span><span class="sxs-lookup"><span data-stu-id="b971d-309">MBAM recovery service endpoint</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="b971d-310">-StatusReportingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b971d-310">-StatusReportingServiceEndpoint</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-311">선택 사항</span><span class="sxs-lookup"><span data-stu-id="b971d-311">Optional</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-312">MBAM 상태 보고 서비스 끝점</span><span class="sxs-lookup"><span data-stu-id="b971d-312">MBAM status reporting service endpoint</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="b971d-313">-. A 메서드</span><span class="sxs-lookup"><span data-stu-id="b971d-313">-EncryptionMethod</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-314">선택 사항</span><span class="sxs-lookup"><span data-stu-id="b971d-314">Optional</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-315">암호화 방법 (기본값: AES 128)</span><span class="sxs-lookup"><span data-stu-id="b971d-315">Encryption method (default: AES 128)</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="b971d-316">-EncryptAndEscrowDataVolume</span><span class="sxs-lookup"><span data-stu-id="b971d-316">-EncryptAndEscrowDataVolume</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-317">스위치</span><span class="sxs-lookup"><span data-stu-id="b971d-317">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-318">데이터 볼륨 및 에스크로 데이터 볼륨 복구 키를 암호화 하도록 지정 (s)</span><span class="sxs-lookup"><span data-stu-id="b971d-318">Specify to encrypt data volume(s) and escrow data volume recovery key(s)</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="b971d-319">-Waitforcomplete To완료</span><span class="sxs-lookup"><span data-stu-id="b971d-319">-WaitForEncryptionToComplete</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-320">스위치</span><span class="sxs-lookup"><span data-stu-id="b971d-320">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-321">암호화가 완료 될 때까지 대기 하도록 지정</span><span class="sxs-lookup"><span data-stu-id="b971d-321">Specify to wait for the encryption to complete</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="b971d-322">-DoNotResumeSuspendedEncryption</span><span class="sxs-lookup"><span data-stu-id="b971d-322">-DoNotResumeSuspendedEncryption</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-323">스위치</span><span class="sxs-lookup"><span data-stu-id="b971d-323">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-324">배포 스크립트가 일시 중단 된 암호화를 다시 시작 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-324">Specify that the deployment script will not resume suspended encryption</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="b971d-325">-IgnoreEscrowOwnerAuthFailure</span><span class="sxs-lookup"><span data-stu-id="b971d-325">-IgnoreEscrowOwnerAuthFailure</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-326">스위치</span><span class="sxs-lookup"><span data-stu-id="b971d-326">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-327">TPM 소유자 인증 에스크로 오류를 무시 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-327">Specify to ignore TPM owner-auth escrow failure.</span></span> <span data-ttu-id="b971d-328">이는 MBAM이 TPM 소유자 인증을 읽을 수 없는 시나리오 (예: TPM 자동 프로비저닝이 사용 되는 경우)에 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-328">It should be used in the scenarios where MBAM is not able to read the TPM owner-auth, e.g. if TPM auto provisioning is enabled</span></span></p></td>
               </tr>
               <tr class="even">
               <td align="left"><p><span data-ttu-id="b971d-329">-IgnoreEscrowRecoveryKeyFailure</span><span class="sxs-lookup"><span data-stu-id="b971d-329">-IgnoreEscrowRecoveryKeyFailure</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-330">스위치</span><span class="sxs-lookup"><span data-stu-id="b971d-330">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-331">볼륨 복구 키 에스크로 오류를 무시 하도록 지정</span><span class="sxs-lookup"><span data-stu-id="b971d-331">Specify to ignore volume recovery key escrow failure</span></span></p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p><span data-ttu-id="b971d-332">-IgnoreReportStatusFailure</span><span class="sxs-lookup"><span data-stu-id="b971d-332">-IgnoreReportStatusFailure</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-333">스위치</span><span class="sxs-lookup"><span data-stu-id="b971d-333">Switch</span></span></p></td>
               <td align="left"><p><span data-ttu-id="b971d-334">상태 보고 실패를 건너뛰도록 지정</span><span class="sxs-lookup"><span data-stu-id="b971d-334">Specify to ignore status reporting failure</span></span></p></td>
               </tr>
               </tbody>
               </table>

                 

**<span data-ttu-id="b971d-335">Windows 배포의 일부로 MBAM 2.5 또는 이전 버전을 사용 하 여 BitLocker를 사용 하도록 설정 하려면</span><span class="sxs-lookup"><span data-stu-id="b971d-335">To enable BitLocker using MBAM 2.5 or earlier as part of a Windows deployment</span></span>**

1.  <span data-ttu-id="b971d-336">MBAM 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-336">Install the MBAM Client.</span></span> <span data-ttu-id="b971d-337">지침은 [명령줄을 사용 하 여 MBAM 클라이언트를 배포 하는 방법을](how-to-deploy-the-mbam-client-by-using-a-command-line.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b971d-337">For instructions, see [How to Deploy the MBAM Client by Using a Command Line](how-to-deploy-the-mbam-client-by-using-a-command-line.md).</span></span>

2.  <span data-ttu-id="b971d-338">컴퓨터를 도메인에 가입 (권장)</span><span class="sxs-lookup"><span data-stu-id="b971d-338">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="b971d-339">컴퓨터가 도메인에 가입 되어 있지 않으면 복구 암호가 MBAM 키 복구 서비스에 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-339">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="b971d-340">복구 키를 저장할 수 없는 경우 기본적으로 MBAM은 암호화를 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-340">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="b971d-341">복구 키가 MBAM 서버에 저장 되기 전에 컴퓨터가 복구 모드에서 시작 되는 경우 복구 방법을 사용할 수 없으며 컴퓨터를 reimaged 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-341">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, no recovery method is available, and the computer has to be reimaged.</span></span>

3.  <span data-ttu-id="b971d-342">관리자 권한으로 명령 프롬프트를 열고 MBAM 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-342">Open a command prompt as an administrator, and stop the MBAM service.</span></span>

4.  <span data-ttu-id="b971d-343">다음 명령을 입력 하 여 **수동** 또는 **주문형** 으로 서비스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-343">Set the service to **Manual** or **On demand** by typing the following commands:</span></span>

    **<span data-ttu-id="b971d-344">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="b971d-344">net stop mbamagent</span></span>**

    **<span data-ttu-id="b971d-345">sc config mbamagent 시작 = 요청</span><span class="sxs-lookup"><span data-stu-id="b971d-345">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="b971d-346">MBAM 클라이언트가 그룹 정책 설정을 무시 하 고 대신 Windows가 해당 클라이언트 컴퓨터에 배포 되는 시간을 시작 하도록 암호화를 설정 하도록 레지스트리 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-346">Set the registry values so that the MBAM Client ignores the Group Policy settings and instead sets encryption to start the time Windows is deployed to that client computer.</span></span>

    <span data-ttu-id="b971d-347">**주의**  사항 이 단계에서는 Windows 레지스트리를 수정 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-347">**Caution** This step describes how to modify the Windows registry.</span></span> <span data-ttu-id="b971d-348">레지스트리 편집기를 잘못 사용 하면 심각한 문제가 발생할 수 있으며,이 경우 Windows를 다시 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-348">Using Registry Editor incorrectly can cause serious issues that can require you to reinstall Windows.</span></span> <span data-ttu-id="b971d-349">레지스트리 편집기의 잘못 된 사용으로 인해 발생 하는 문제는 확인할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-349">We cannot guarantee that issues resulting from the incorrect use of Registry Editor can be resolved.</span></span> <span data-ttu-id="b971d-350">레지스트리 편집기 사용에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-350">Use Registry Editor at your own risk.</span></span>

    1.  <span data-ttu-id="b971d-351">**운영 체제 전용 암호화**용 TPM을 설정 하 고, Regedit.exe을 실행 한 다음 C:\\program files Files\\Microsoft\\MDOP Mbam\\mbamdeploymentkeytemplate 파일에서 레지스트리 키 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-351">Set the TPM for **Operating system only encryption**, run Regedit.exe, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

    2.  <span data-ttu-id="b971d-352">Regedit.exe에서 HKLM\\SOFTWARE\\Microsoft\\MBAM으로 이동 하 여 다음 표에 나열 된 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-352">In Regedit.exe, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

        <span data-ttu-id="b971d-353">**참고**  여기에 MBAM과 관련 된 그룹 정책 설정 또는 레지스트리 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-353">**Note** You can set Group Policy settings or registry values related to MBAM here.</span></span> <span data-ttu-id="b971d-354">이러한 설정은 이전에 설정 값을 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-354">These settings will override previously set values.</span></span>

        <span data-ttu-id="b971d-355">레지스트리 항목 구성 설정</span><span class="sxs-lookup"><span data-stu-id="b971d-355">Registry entry Configuration settings</span></span>

        <span data-ttu-id="b971d-356">DeploymentTime</span><span class="sxs-lookup"><span data-stu-id="b971d-356">DeploymentTime</span></span>

        <span data-ttu-id="b971d-357">0 = 해제</span><span class="sxs-lookup"><span data-stu-id="b971d-357">0 = Off</span></span>

        <span data-ttu-id="b971d-358">1 = 배포 시간 정책 설정 사용 (기본값) – Windows가 클라이언트 컴퓨터에 배포 될 때 암호화를 사용 하도록 설정 하려면이 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-358">1 = Use deployment time policy settings (default) – use this setting to enable encryption at the time Windows is deployed to the client computer.</span></span>

        <span data-ttu-id="b971d-359">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="b971d-359">UseKeyRecoveryService</span></span>

        <span data-ttu-id="b971d-360">0 = key 에스크로를 사용 하지 않음 (이 경우 다음 두 레지스트리 항목은 필요 없음)</span><span class="sxs-lookup"><span data-stu-id="b971d-360">0 = Do not use key escrow (the next two registry entries are not required in this case)</span></span>

        <span data-ttu-id="b971d-361">1 = 키 복구 시스템에서 키 에스크로 사용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b971d-361">1 = Use key escrow in Key Recovery system (default)</span></span>

        <span data-ttu-id="b971d-362">이 설정은 MBAM이 복구 키를 저장할 수 있도록 하는 권장 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-362">This is the recommended setting, which enables MBAM to store the recovery keys.</span></span> <span data-ttu-id="b971d-363">컴퓨터는 MBAM 키 복구 서비스와 통신할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-363">The computer must be able to communicate with the MBAM Key Recovery service.</span></span> <span data-ttu-id="b971d-364">계속 하기 전에 컴퓨터가 서비스와 통신할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-364">Verify that the computer can communicate with the service before you proceed.</span></span>

        <span data-ttu-id="b971d-365">KeyRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="b971d-365">KeyRecoveryOptions</span></span>

        <span data-ttu-id="b971d-366">0 = 복구 키만 업로드</span><span class="sxs-lookup"><span data-stu-id="b971d-366">0 = Uploads Recovery Key only</span></span>

        <span data-ttu-id="b971d-367">1 = 복구 키 및 키 복구 패키지를 업로드 합니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="b971d-367">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

        <span data-ttu-id="b971d-368">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="b971d-368">KeyRecoveryServiceEndPoint</span></span>

        <span data-ttu-id="b971d-369">이 값을 키 복구 서비스를 실행 하는 서버의 URL (예: http:// &lt; computer name/MBAMRecoveryAndHardwareService/CoreService.svc.)으로 설정 합니다. &gt;</span><span class="sxs-lookup"><span data-stu-id="b971d-369">Set this value to the URL for the server running the Key Recovery service, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>


6.  <span data-ttu-id="b971d-370">MBAM 클라이언트는 MBAM 클라이언트 배포 중에 시스템을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-370">The MBAM Client will restart the system during the MBAM Client deployment.</span></span> <span data-ttu-id="b971d-371">이 작업을 다시 시작할 준비가 되 면 관리자 권한으로 명령 프롬프트에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-371">When you are ready for this restart, run the following command at a command prompt as an administrator:</span></span>

    **<span data-ttu-id="b971d-372">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="b971d-372">net start mbamagent</span></span>**

7.  <span data-ttu-id="b971d-373">컴퓨터가 다시 시작 되 고 BIOS에 메시지가 표시 되 면 TPM 변경 내용을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-373">When the computers restarts, and the BIOS prompts you, accept the TPM change.</span></span>

8.  <span data-ttu-id="b971d-374">Windows 클라이언트 운영 체제 이미징 프로세스 중에 암호화를 시작할 준비가 되 면 관리자 권한으로 명령 프롬프트를 열고 다음 명령을 입력 하 여 **자동** 시작을 설정 하 고 Mbam 클라이언트 에이전트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-374">During the Windows client operating system imaging process, when you are ready to start encryption, open a command prompt as an administrator, and type the following commands to set the start to **Automatic** and to restart the MBAM Client agent:</span></span>

    **<span data-ttu-id="b971d-375">sc config mbamagent 시작 = 자동</span><span class="sxs-lookup"><span data-stu-id="b971d-375">sc config mbamagent start= auto</span></span>**

    **<span data-ttu-id="b971d-376">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="b971d-376">net start mbamagent</span></span>**

9.  <span data-ttu-id="b971d-377">무시 레지스트리 값을 삭제 하려면 Regedit.exe를 실행 하 고 HKLM\\SOFTWARE\\Microsoft 레지스트리 항목으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-377">To delete the bypass registry values, run Regedit.exe, and go to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="b971d-378">**Mbam** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **삭제**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-378">Right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="b971d-379">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b971d-379">Related topics</span></span>

[<span data-ttu-id="b971d-380">MBAM 2.5 클라이언트 배포</span><span class="sxs-lookup"><span data-stu-id="b971d-380">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="b971d-381">MBAM 2.5 클라이언트 배포 계획</span><span class="sxs-lookup"><span data-stu-id="b971d-381">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <span data-ttu-id="b971d-382">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="b971d-382">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b971d-383">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-383">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="b971d-384">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b971d-384">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
