---
title: 클라이언트 이벤트 로그
description: 클라이언트 이벤트 로그
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824193"
---
# <span data-ttu-id="d0bba-103">클라이언트 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="d0bba-103">Client Event Logs</span></span>

<span data-ttu-id="d0bba-104">MBAM 클라이언트 이벤트 로그는 이벤트 뷰어에 있으며, 응용 프로그램 및 서비스 로그 – Microsoft – Windows – MBAM 작동 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-104">MBAM Client event logs are located in Event Viewer – Applications and Services Logs – Microsoft – Windows – MBAM - Operational path.</span></span>
<span data-ttu-id="d0bba-105">다음 표에는 MBAM 클라이언트에서 발생할 수 있는 이벤트 Id가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-105">The following table contains event IDs that can occur on the MBAM Client.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0bba-106">이벤트 ID</span><span class="sxs-lookup"><span data-stu-id="d0bba-106">Event ID</span></span></th>
<th align="left"><span data-ttu-id="d0bba-107">채널</span><span class="sxs-lookup"><span data-stu-id="d0bba-107">Channel</span></span></th>
<th align="left"><span data-ttu-id="d0bba-108">이벤트 기호</span><span class="sxs-lookup"><span data-stu-id="d0bba-108">Event symbol</span></span></th>
<th align="left"><span data-ttu-id="d0bba-109">메시지</span><span class="sxs-lookup"><span data-stu-id="d0bba-109">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="d0bba-110">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-111">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-111">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-112">VolumeEnactmentSuccessful</span><span class="sxs-lookup"><span data-stu-id="d0bba-112">VolumeEnactmentSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-113">MBAM 정책이 성공적으로 적용 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-113">The MBAM policies were applied successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-114">2</span><span class="sxs-lookup"><span data-stu-id="d0bba-114">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-115">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-115">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-116">VolumeEnactmentFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-116">VolumeEnactmentFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-117">MBAM 정책을 적용 하는 동안 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-117">An error occurred while applying MBAM policies.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-118">3-4</span><span class="sxs-lookup"><span data-stu-id="d0bba-118">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-119">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-119">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-120">TransferStatusDataSuccessful</span><span class="sxs-lookup"><span data-stu-id="d0bba-120">TransferStatusDataSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-121">암호화 상태 데이터가 성공적으로 전송 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-121">The encryption status data was sent successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-122">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="d0bba-122">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-123">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-123">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-124">전송 실패</span><span class="sxs-lookup"><span data-stu-id="d0bba-124">TransferStatusDataFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-125">암호화 상태 데이터를 보내는 동안 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-125">An error occurred while sending encryption status data.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-126">20cm(8</span><span class="sxs-lookup"><span data-stu-id="d0bba-126">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-127">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-127">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-128">SystemVolumeNotFound</span><span class="sxs-lookup"><span data-stu-id="d0bba-128">SystemVolumeNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-129">시스템 볼륨이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-129">The system volume is missing.</span></span> <span data-ttu-id="d0bba-130">운영 체제 드라이브를 암호화 하려면 SystemVolume이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-130">SystemVolume is needed to encrypt the operating system drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-131">되었는지</span><span class="sxs-lookup"><span data-stu-id="d0bba-131">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-132">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-132">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-133">TPMNotFound</span><span class="sxs-lookup"><span data-stu-id="d0bba-133">TPMNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-134">TPM 하드웨어가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-134">The TPM hardware is missing.</span></span> <span data-ttu-id="d0bba-135">Tpm은 TPM 보호기로 운영 체제 드라이브를 암호화 하는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-135">TPM is needed to encrypt the operating system drive with any TPM protector.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-136">1천만</span><span class="sxs-lookup"><span data-stu-id="d0bba-136">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-137">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-137">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-138">MachineHWExempted</span><span class="sxs-lookup"><span data-stu-id="d0bba-138">MachineHWExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-139">컴퓨터가 암호화에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-139">The computer is exempted from Encryption.</span></span> <span data-ttu-id="d0bba-140">컴퓨터의 하드웨어 상태: 제외</span><span class="sxs-lookup"><span data-stu-id="d0bba-140">Machine’s hardware status: Exempted</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-141">mb</span><span class="sxs-lookup"><span data-stu-id="d0bba-141">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-142">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-142">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-143">MachineHWUnknown</span><span class="sxs-lookup"><span data-stu-id="d0bba-143">MachineHWUnknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-144">컴퓨터가 암호화에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-144">The computer is exempted from encryption.</span></span> <span data-ttu-id="d0bba-145">컴퓨터의 하드웨어 상태: 알 수 없음</span><span class="sxs-lookup"><span data-stu-id="d0bba-145">Machine’s hardware status: Unknown</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-146">까지</span><span class="sxs-lookup"><span data-stu-id="d0bba-146">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-147">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-147">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-148">HWCheckFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-148">HWCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-149">하드웨어 예외 검사에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-149">Hardware exemption check failed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-150">일자</span><span class="sxs-lookup"><span data-stu-id="d0bba-150">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-151">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-151">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-152">UserIsExempted</span><span class="sxs-lookup"><span data-stu-id="d0bba-152">UserIsExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-153">사용자가 암호화에서 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-153">The user is exempt from encryption.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-154">13</span><span class="sxs-lookup"><span data-stu-id="d0bba-154">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-155">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-155">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-156">UserIsWaiting</span><span class="sxs-lookup"><span data-stu-id="d0bba-156">UserIsWaiting</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-157">사용자가 예외를 요청 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-157">The user requested an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-158">~</span><span class="sxs-lookup"><span data-stu-id="d0bba-158">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-159">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-159">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-160">UserExemptionCheckFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-160">UserExemptionCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-161">사용자 예외 검사에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-161">User exemption check failed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-162">16</span><span class="sxs-lookup"><span data-stu-id="d0bba-162">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-163">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-163">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-164">UserPostponed 됨</span><span class="sxs-lookup"><span data-stu-id="d0bba-164">UserPostponed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-165">사용자가 암호화 프로세스를 연기 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-165">The user postponed the encryption process.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-166">17</span><span class="sxs-lookup"><span data-stu-id="d0bba-166">17</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-167">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-167">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-168">TPMInitializationFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-168">TPMInitializationFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-169">TPM 초기화에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-169">TPM initialization failed.</span></span> <span data-ttu-id="d0bba-170">사용자가 BIOS 변경 내용을 거부 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-170">The user rejected the BIOS changes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-171">18</span><span class="sxs-lookup"><span data-stu-id="d0bba-171">18</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-172">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-172">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-173">CoreServiceDown</span><span class="sxs-lookup"><span data-stu-id="d0bba-173">CoreServiceDown</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-174">MBAM 복구 및 하드웨어 서비스에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-174">Unable to connect to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-175">인치</span><span class="sxs-lookup"><span data-stu-id="d0bba-175">19</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-176">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-176">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-177">CoreServiceUp</span><span class="sxs-lookup"><span data-stu-id="d0bba-177">CoreServiceUp</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-178">MBAM 복구 및 하드웨어 서비스에 연결 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-178">Successfully connected to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-179">명</span><span class="sxs-lookup"><span data-stu-id="d0bba-179">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-180">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-180">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-181">PolicyMismatch</span><span class="sxs-lookup"><span data-stu-id="d0bba-181">PolicyMismatch</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-182">MBAM 정책이 충돌 하거나 손상 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-182">The MBAM policy is in conflict or corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-183">mb</span><span class="sxs-lookup"><span data-stu-id="d0bba-183">21</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-184">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-184">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-185">ConflictingOSVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="d0bba-185">ConflictingOSVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-186">OS 볼륨 암호화 정책이 충돌 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-186">Detected OS volume encryption policies conflict.</span></span> <span data-ttu-id="d0bba-187">OS 드라이브 프로텍터와 관련 된 BitLocker 및 MBAM 정책을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-187">Check BitLocker and MBAM policies related to OS drive protectors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-188">khz</span><span class="sxs-lookup"><span data-stu-id="d0bba-188">22</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-189">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-189">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-190">ConflictingFDDVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="d0bba-190">ConflictingFDDVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-191">해결 됨 고정 데이터 드라이브 볼륨 암호화 정책이 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-191">Detected Fixed Data Drive volume encryption policies conflict.</span></span> <span data-ttu-id="d0bba-192">FDD 드라이브 프로텍터와 관련 된 BitLocker 및 MBAM 정책을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-192">Check BitLocker and MBAM policies related to FDD drive protectors.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-193">27</span><span class="sxs-lookup"><span data-stu-id="d0bba-193">27</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-194">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-194">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-195"># Failednodra</span><span class="sxs-lookup"><span data-stu-id="d0bba-195">EncryptionFailedNoDra</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-196">암호화 하는 동안 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-196">An error occurred while encrypting.</span></span> <span data-ttu-id="d0bba-197">Windows 사전 8.1 컴퓨터의 경우 DRA (데이터 복구 에이전트) 보호기가 FIPS 모드에서 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-197">A Data Recovery Agent (DRA) protector is required in FIPS mode for pre-Windows 8.1 machines.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-198">일까</span><span class="sxs-lookup"><span data-stu-id="d0bba-198">28</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-199">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-199">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-200">TpmOwnerAuthEscrowed</span><span class="sxs-lookup"><span data-stu-id="d0bba-200">TpmOwnerAuthEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-201">TPM 소유자 Auth가 escrowed 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-201">The TPM OwnerAuth has been escrowed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-202">개가</span><span class="sxs-lookup"><span data-stu-id="d0bba-202">29</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-203">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-203">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-204">RecoveryKeyEscrowed</span><span class="sxs-lookup"><span data-stu-id="d0bba-204">RecoveryKeyEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-205">볼륨에 대 한 BitLocker 복구 키가 escrowed 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-205">The BitLocker recovery key for the volume has been escrowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-206">30</span><span class="sxs-lookup"><span data-stu-id="d0bba-206">30</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-207">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-207">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-208">RecoveryKeyReset</span><span class="sxs-lookup"><span data-stu-id="d0bba-208">RecoveryKeyReset</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-209">볼륨에 대 한 BitLocker 복구 키가 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-209">The BitLocker recovery key for the volume has been updated.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-210">개</span><span class="sxs-lookup"><span data-stu-id="d0bba-210">31</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-211">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-211">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-212">EnforcePolicyDateSet</span><span class="sxs-lookup"><span data-stu-id="d0bba-212">EnforcePolicyDateSet</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-213"><em> &lt; &gt; 볼륨에 대해 적용 정책 날짜, 날짜를 </em> 설정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-213">The enforce policy date, <em>&lt;date&gt;</em>, has been set for the volume</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-214">32</span><span class="sxs-lookup"><span data-stu-id="d0bba-214">32</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-215">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-215">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-216">EnforcePolicyDateCleared</span><span class="sxs-lookup"><span data-stu-id="d0bba-216">EnforcePolicyDateCleared</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-217"><em> &lt; 볼륨에 대 한 적용 정책 날짜, 날짜 &gt; </em> 를 지웠습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-217">The enforce policy date, <em>&lt;date&gt;</em>, has been cleared for the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-218">33</span><span class="sxs-lookup"><span data-stu-id="d0bba-218">33</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-219">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-219">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-220">TpmLockOutResetSucceeded</span><span class="sxs-lookup"><span data-stu-id="d0bba-220">TpmLockOutResetSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-221">TPM 잠금을 다시 설정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-221">Successfully reset TPM lockout.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-222">34</span><span class="sxs-lookup"><span data-stu-id="d0bba-222">34</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-223">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-223">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-224">TpmLockOutResetFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-224">TpmLockOutResetFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-225">TPM 잠금을 다시 설정 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-225">Failed to reset TPM lockout.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-226">35</span><span class="sxs-lookup"><span data-stu-id="d0bba-226">35</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-227">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-227">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-228">TpmOwnerAuthRetrievalSucceeded</span><span class="sxs-lookup"><span data-stu-id="d0bba-228">TpmOwnerAuthRetrievalSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-229">MBAM 서비스에서 TPM 소유자 인증을 검색 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-229">Successfully retrieved TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-230">36</span><span class="sxs-lookup"><span data-stu-id="d0bba-230">36</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-231">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-231">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-232">TpmOwnerAuthRetrievalFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-232">TpmOwnerAuthRetrievalFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-233">MBAM 서비스에서 TPM 소유자 인증을 검색 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-233">Failed to retrieve TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-234">37</span><span class="sxs-lookup"><span data-stu-id="d0bba-234">37</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-235">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-235">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-236">WmiProviderDllSearchPathUpdateFailed</span><span class="sxs-lookup"><span data-stu-id="d0bba-236">WmiProviderDllSearchPathUpdateFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-237">WMI 공급자에 대 한 DLL 검색 경로를 업데이트 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-237">Failed to update the DLL search path for WMI provider.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-238">38</span><span class="sxs-lookup"><span data-stu-id="d0bba-238">38</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-239">Admin</span><span class="sxs-lookup"><span data-stu-id="d0bba-239">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-240">TimedOutWaitingForWmiProvider</span><span class="sxs-lookup"><span data-stu-id="d0bba-240">TimedOutWaitingForWmiProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-241">에이전트 중지 중-MBAM WMI 공급자 인스턴스를 기다리는 동안 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-241">Agent Stopping - Timed-out waiting for MBAM WMI Provider Instance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-242">39</span><span class="sxs-lookup"><span data-stu-id="d0bba-242">39</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-243">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-243">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-244">RemovableDriveMounted</span><span class="sxs-lookup"><span data-stu-id="d0bba-244">RemovableDriveMounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-245">이동식 드라이브를 탑재 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-245">Removable drive was mounted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-246">40</span><span class="sxs-lookup"><span data-stu-id="d0bba-246">40</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-247">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-247">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-248">Removable드라이브 분리 됨</span><span class="sxs-lookup"><span data-stu-id="d0bba-248">RemovableDriveDismounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-249">이동식 드라이브가 분리 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-249">Removable drive was unmounted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-250">41</span><span class="sxs-lookup"><span data-stu-id="d0bba-250">41</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-251">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-251">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-252">이 (가) FailedToEnactEndpointUnreachable 수 없음</span><span class="sxs-lookup"><span data-stu-id="d0bba-252">FailedToEnactEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-253">MBAM 복구 및 하드웨어 서비스에 연결 하지 못해 볼륨에 성공적으로 적용 되지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="d0bba-253">Failure to connect to the MBAM Recovery and Hardware service prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0bba-254">42</span><span class="sxs-lookup"><span data-stu-id="d0bba-254">42</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-255">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-255">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-256">FailedToEnactLockedVolume</span><span class="sxs-lookup"><span data-stu-id="d0bba-256">FailedToEnactLockedVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-257">볼륨 상태가 잠기면 MBAM 정책이 볼륨에 성공적으로 적용 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-257">Locked volume state prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0bba-258">43</span><span class="sxs-lookup"><span data-stu-id="d0bba-258">43</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-259">운용</span><span class="sxs-lookup"><span data-stu-id="d0bba-259">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-260">전송 불가능 한 전송 상태 Datafailedendpoint접근할 수 없음</span><span class="sxs-lookup"><span data-stu-id="d0bba-260">TransferStatusDataFailedEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0bba-261">MBAM 준수 및 상태 서비스에 연결 하지 못하면 암호화 상태 데이터를 전송할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-261">Failure to connect to the MBAM Compliance and Status service prevented the transfer of encryption status data.</span></span></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="d0bba-262">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d0bba-262">Related topics</span></span>
[<span data-ttu-id="d0bba-263">MBAM 2.5에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="d0bba-263">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="d0bba-264">서버 이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="d0bba-264">Server Event Logs</span></span>](server-event-logs.md)

 


## <span data-ttu-id="d0bba-265">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="d0bba-265">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d0bba-266">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-266">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="d0bba-267">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bba-267">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





