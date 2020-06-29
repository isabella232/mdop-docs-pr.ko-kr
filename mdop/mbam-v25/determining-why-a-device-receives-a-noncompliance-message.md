---
title: 장치에서 규정 미준수 메시지를 수신하는 이유 확인
description: 장치에서 규정 미준수 메시지를 수신하는 이유 확인
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824573"
---
# <span data-ttu-id="7ff0b-103">장치에서 규정 미준수 메시지를 수신하는 이유 확인</span><span class="sxs-lookup"><span data-stu-id="7ff0b-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="7ff0b-104">다음 비 호환성 코드는 WMI에서 제공 되며, 비규격으로 인해 특정 장치가 보고 되는 이유를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="7ff0b-105">선호 하는 방법을 사용 하 여 WMI를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="7ff0b-106">PowerShell을 사용 하는 경우 `gwmi -class mbam_volume -Namespace root\microsoft\mbam` powershell 프롬프트에서 실행 하 고 ReasonsForNoncompliance를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ff0b-107">비호환 코드</span><span class="sxs-lookup"><span data-stu-id="7ff0b-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="7ff0b-108">준수 하지 않는 이유</span><span class="sxs-lookup"><span data-stu-id="7ff0b-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-109">0</span><span class="sxs-lookup"><span data-stu-id="7ff0b-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-110">암호화 강도가 AES 256이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-111">raid-1</span><span class="sxs-lookup"><span data-stu-id="7ff0b-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-112">MBAM 정책은이 볼륨을 암호화 해야 하지만, 그렇지 않은 경우에는 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-113">2</span><span class="sxs-lookup"><span data-stu-id="7ff0b-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-114">MBAM 정책에서는이 볼륨을 암호화 하지 않아도 되지만,</span><span class="sxs-lookup"><span data-stu-id="7ff0b-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-115">3-4</span><span class="sxs-lookup"><span data-stu-id="7ff0b-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-116">MBAM 정책은이 볼륨에 TPM 보호기를 사용 해야 하지만, 그렇지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-117">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="7ff0b-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-118">이 볼륨에는이 볼륨이 TPM + PIN 보호기를 사용 해야 하지만 MBAM 정책이 필요 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-119">5mb</span><span class="sxs-lookup"><span data-stu-id="7ff0b-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-120">MBAM 정책은 비 TPM 컴퓨터를 규격으로 보고 하도록 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-121">26</span><span class="sxs-lookup"><span data-stu-id="7ff0b-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-122">볼륨에 TPM 보호기가 있지만 TPM이 표시 되지 않습니다 (BIOS에서 TPM을 사용 하지 않도록 설정한 후 복구 키로 부팅 됨).</span><span class="sxs-lookup"><span data-stu-id="7ff0b-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-123">7</span><span class="sxs-lookup"><span data-stu-id="7ff0b-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-124">이 볼륨에는 암호 보호기를 사용 해야 하지만 MBAM 정책에는 암호가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-125">20cm(8</span><span class="sxs-lookup"><span data-stu-id="7ff0b-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-126">MBAM 정책에 의해이 볼륨에는 암호 보호기가 사용 되지 않지만, 하나는 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-127">되었는지</span><span class="sxs-lookup"><span data-stu-id="7ff0b-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-128">이 볼륨에는이 볼륨이 자동 잠금 해제 보호 기능을 사용 하도록 요구 하지만 MBAM 정책에는 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-129">1천만</span><span class="sxs-lookup"><span data-stu-id="7ff0b-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-130">MBAM 정책에 의해이 볼륨에는 자동 잠금 해제 보호기가 사용 되지 않지만, 하나는 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-131">mb</span><span class="sxs-lookup"><span data-stu-id="7ff0b-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-132">정책 충돌이 감지 되어 MBAM이이 볼륨을 준수 하는 것으로 보고 하지 못하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-133">까지</span><span class="sxs-lookup"><span data-stu-id="7ff0b-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-134">시스템 볼륨이 OS 볼륨을 암호화 하는 데 필요 하지만 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-135">일자</span><span class="sxs-lookup"><span data-stu-id="7ff0b-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-136">볼륨에 대 한 보호가 일시 중단 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-137">13</span><span class="sxs-lookup"><span data-stu-id="7ff0b-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-138">OS 볼륨이 암호화 되지 않은 경우 AutoUnlock 안전 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff0b-139">~</span><span class="sxs-lookup"><span data-stu-id="7ff0b-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-140">정책에는 최소 cypher 강도가 XTS-AES-128 비트 이지만 실제 cypher 강도가 약한 것 보다 적습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff0b-141">16</span><span class="sxs-lookup"><span data-stu-id="7ff0b-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="7ff0b-142">정책에는 최소 cypher 강도가 XTS-AES-256 비트 이지만 실제 cypher 강도가 약한 것 보다 적습니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7ff0b-143">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7ff0b-143">Related topics</span></span>


[<span data-ttu-id="7ff0b-144">MBAM 2.5에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="7ff0b-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="7ff0b-145">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="7ff0b-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="7ff0b-146">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="7ff0b-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7ff0b-147">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="7ff0b-148">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





