---
title: MBAM 2.5 그룹 정책 요구 사항 계획
description: MBAM 2.5 그룹 정책 요구 사항 계획
author: dansimp
ms.assetid: 82d545dc-3fbf-4b46-b62f-47fe178a7c44
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4beeb9f88f16e7d48d145861c398a90fa29f3491
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823768"
---
# <span data-ttu-id="04db9-103">MBAM 2.5 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="04db9-103">Planning for MBAM 2.5 Group Policy Requirements</span></span>


<span data-ttu-id="04db9-104">다음 정보를 사용 하 여 엔터프라이즈에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트 컴퓨터를 관리 하는 데 사용할 수 있는 BitLocker 프로텍터 유형을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-104">Use the following information to determine the types of BitLocker protectors that you can use to manage the Microsoft BitLocker Administration and Monitoring (MBAM) client computers in your enterprise.</span></span>

## <span data-ttu-id="04db9-105">MBAM이 지 원하는 BitLocker 프로텍터 종류</span><span class="sxs-lookup"><span data-stu-id="04db9-105">Types of BitLocker protectors that MBAM supports</span></span>


<span data-ttu-id="04db9-106">MBAM은 다음 유형의 BitLocker 보호기를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-106">MBAM supports the following types of BitLocker protectors.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-107">드라이브 또는 볼륨 종류</span><span class="sxs-lookup"><span data-stu-id="04db9-107">Type of drive or volume</span></span></th>
<th align="left"><span data-ttu-id="04db9-108">지원 되는 BitLocker 프로텍터</span><span class="sxs-lookup"><span data-stu-id="04db9-108">Supported BitLocker protectors</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-109">운영 체제 볼륨</span><span class="sxs-lookup"><span data-stu-id="04db9-109">Operating system volumes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="04db9-110">TPM(신뢰할 수 있는 플랫폼 모듈)</span><span class="sxs-lookup"><span data-stu-id="04db9-110">Trusted Platform Module (TPM)</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04db9-111">TPM + PIN</span><span class="sxs-lookup"><span data-stu-id="04db9-111">TPM + PIN</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04db9-112">TPM + USB 키 </strong> – MBAM이 설치 되기 전에 운영 체제 볼륨을 암호화 한 경우에만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-112">TPM + USB key</strong> – supported only when the operating system volume is encrypted before MBAM is installed</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-113"></strong> - 컴퓨터 운영 체제 볼륨이 mbam이 설치 되기 전에 암호화 된 경우에만 지원 되는 TPM + PIN + USB 키</span><span class="sxs-lookup"><span data-stu-id="04db9-113">TPM + PIN + USB key</strong> - supported only when the operating system volume is encrypted before MBAM is installed</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-114">TPM이 없는 </strong> - Windows to Go 장치, 고정 데이터 드라이브, windows 8, windows 8.1 및 windows 10 장치 에서만 지원 되는 암호</span><span class="sxs-lookup"><span data-stu-id="04db9-114">Password</strong> - supported only for Windows To Go devices, fixed data drives, and Windows 8, Windows 8.1, and Windows 10 devices that do not have a TPM</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-115">숫자 암호는 </strong> - 볼륨 암호화의 일부로 자동 적용 되며 Windows 7에서 FIPS 모드를 제외 하 고 구성할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-115">Numerical password</strong> - applied automatically as part of volume encryption and does not need to be configured except in FIPS mode on Windows 7</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-116">DRA (Data recovery agent)</span><span class="sxs-lookup"><span data-stu-id="04db9-116">Data recovery agent (DRA)</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-117">고정 데이터 드라이브</span><span class="sxs-lookup"><span data-stu-id="04db9-117">Fixed data drives</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="04db9-118">암호</span><span class="sxs-lookup"><span data-stu-id="04db9-118">Password</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04db9-119">자동 잠금 해제</span><span class="sxs-lookup"><span data-stu-id="04db9-119">Auto-unlock</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04db9-120">숫자 암호는 </strong> - 볼륨 암호화의 일부로 자동 적용 되며 Windows 7에서 FIPS 모드를 제외 하 고 구성할 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-120">Numerical password</strong> - applied automatically as part of volume encryption and does not need to be configured except in FIPS mode on Windows 7</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-121">DRA (Data recovery agent)</span><span class="sxs-lookup"><span data-stu-id="04db9-121">Data recovery agent (DRA)</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-122">이동식 드라이브</span><span class="sxs-lookup"><span data-stu-id="04db9-122">Removable drives</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="04db9-123">암호</span><span class="sxs-lookup"><span data-stu-id="04db9-123">Password</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04db9-124">자동 잠금 해제</span><span class="sxs-lookup"><span data-stu-id="04db9-124">Auto-unlock</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="04db9-125">숫자 암호는 </strong> - 볼륨 암호화의 일부로 자동 적용 되며 구성할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-125">Numerical password</strong> - applied automatically as part of volume encryption and does not need to be configured</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-126">DRA (Data recovery agent)</span><span class="sxs-lookup"><span data-stu-id="04db9-126">Data recovery agent (DRA)</span></span></strong></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="04db9-127">사용 된 공간 암호화 BitLocker 정책에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="04db9-127">Support for the Used Space Encryption BitLocker policy</span></span>

<span data-ttu-id="04db9-128">MBAM 2.5 SP1에서 BitLocker 그룹 정책을 통해 사용 하는 공간 암호화를 사용 하도록 설정 하면 MBAM 클라이언트가이를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-128">In MBAM 2.5 SP1, if you enable Used Space Encryption via BitLocker Group policy, the MBAM Client honors it.</span></span>

<span data-ttu-id="04db9-129">이 그룹 정책 설정을 **운영 체제 드라이브에 드라이브 암호화 유형 강제 적용** 이라고 하며, **컴퓨터 구성** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **BitLocker 드라이브 암호화** &gt; **운영 체제 드라이브**에는 다음과 같은 GPO 노드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-129">This Group Policy setting is called **Enforce drive encryption type on operating system drives** and is located in the following GPO node: **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **Operating System Drives**.</span></span> <span data-ttu-id="04db9-130">이 정책을 사용 하 고 **사용 된 공간만 암호화**로 암호화 유형을 선택 하는 경우, mbam은 정책을 인식 하 고 BitLocker는 볼륨에 사용 되는 디스크 공간만 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-130">If you enable this policy and select the encryption type as **Used Space Only encryption**, MBAM will honor the policy and BitLocker will only encrypt disk space that is used on the volume.</span></span>

## <span data-ttu-id="04db9-131">MBAM 그룹 정책 템플릿을 가져오고 설정을 편집 하는 방법</span><span class="sxs-lookup"><span data-stu-id="04db9-131">How to get the MBAM Group Policy Templates and edit the settings</span></span>


<span data-ttu-id="04db9-132">원하는 MBAM 그룹 정책 설정을 구성할 준비가 되었으면 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-132">When you are ready to configure the MBAM Group Policy settings you want, do the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-133">팔 로우 단계</span><span class="sxs-lookup"><span data-stu-id="04db9-133">Steps to follow</span></span></th>
<th align="left"><span data-ttu-id="04db9-134">지침을 받을 위치</span><span class="sxs-lookup"><span data-stu-id="04db9-134">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-135">MBAM 그룹 정책 서식 파일을 복사 하 여 <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> </a> GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 실행할 수 있는 컴퓨터에 설치 하는 방법에서 MDOP 그룹 정책 (Admx) 서식 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-135">Copy the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and install them on a computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="04db9-136">MBAM 2.5 그룹 정책 템플릿 복사</span><span class="sxs-lookup"><span data-stu-id="04db9-136">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-137">엔터프라이즈에서 사용할 그룹 정책 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-137">Configure the Group Policy settings that you want to use in your enterprise.</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="04db9-138">MBAM 2.5 그룹 정책 설정 편집</span><span class="sxs-lookup"><span data-stu-id="04db9-138">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="04db9-139">MBAM 그룹 정책 설정에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="04db9-139">Descriptions of the MBAM Group Policy settings</span></span>


<span data-ttu-id="04db9-140">**MDOP (BitLocker 관리)** GPO 노드에는 4 개의 글로벌 정책 설정과 **클라이언트 관리**, **고정 드라이브**, **운영 체제 드라이브**, **이동식 드라이브**의 네 개의 자식 GPO 노드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-140">The **MDOP MBAM (BitLocker Management)** GPO node contains four global policy settings and four child GPO nodes: **Client Management**, **Fixed Drive**, **Operating System Drive**, and **Removable Drive**.</span></span> <span data-ttu-id="04db9-141">다음 섹션에서는 MBAM 그룹 정책 설정에 대 한 설정 및 제안 사항을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-141">The following sections describe and suggest settings for the MBAM Group Policy settings.</span></span>

**<span data-ttu-id="04db9-142">중요</span><span class="sxs-lookup"><span data-stu-id="04db9-142">Important</span></span>**  
<span data-ttu-id="04db9-143">**BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-143">Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="04db9-144">MBAM은 **MDOP mbam (BitLocker Management)** 노드에서 설정을 구성할 때이 노드의 설정을 자동으로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-144">MBAM automatically configures the settings in this node for you when you configure the settings in the **MDOP MBAM (BitLocker Management)** node.</span></span>



### <span data-ttu-id="04db9-145">글로벌 그룹 정책 정의</span><span class="sxs-lookup"><span data-stu-id="04db9-145">Global Group Policy definitions</span></span>

<span data-ttu-id="04db9-146">이 섹션에서는 다음과 같은 GPO 노드에서 mbam 전역 그룹 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)**.</span><span class="sxs-lookup"><span data-stu-id="04db9-146">This section describes MBAM Global Group Policy definitions at the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-147">정책 이름</span><span class="sxs-lookup"><span data-stu-id="04db9-147">Policy name</span></span></th>
<th align="left"><span data-ttu-id="04db9-148">개요 및 제안 된 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-148">Overview and suggested Group Policy settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-149">드라이브 암호화 방법 및 암호화 수준 선택</span><span class="sxs-lookup"><span data-stu-id="04db9-149">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-150">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-150">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-151">특정 암호화 방법 및 암호화 강도를 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-151">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="04db9-152">이 정책이 구성 되어 있지 않으면 BitLocker는 기본 암호화 방법 인 AES 128-디퓨저를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-152">When this policy is not configured, BitLocker uses the default encryption method: AES 128-bit with Diffuser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04db9-153">참고</span><span class="sxs-lookup"><span data-stu-id="04db9-153">Note</span></span></strong><br/><p><span data-ttu-id="04db9-154">BitLocker 컴퓨터 준수 보고서의 문제는 &quot; &quot; 기본값을 사용 하는 경우에도 암호화 강도에 대해 알 수 없는 것으로 표시 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-154">An issue with the BitLocker Computer Compliance report causes it to display &quot;unknown&quot; for the cipher strength, even if you are using the default value.</span></span> <span data-ttu-id="04db9-155">이 문제를 해결 하려면이 설정을 사용 하 고 암호화 수준에 대 한 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-155">To work around this issue, make sure you enable this setting and set a value for cipher strength.</span></span></p>
</div>
<div>

</div>
<ul>
<li><p><span data-ttu-id="04db9-156">AES 128-디퓨저-Windows 7 전용</span><span class="sxs-lookup"><span data-stu-id="04db9-156">AES 128-bit with Diffuser – for Windows 7 only</span></span></p></li>
<li><p><span data-ttu-id="04db9-157">Windows 8, Windows 8.1 및 Windows 10 용 AES 128</span><span class="sxs-lookup"><span data-stu-id="04db9-157">AES 128 for Windows 8, Windows 8.1, and Windows 10</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-158">다시 시작할 때 메모리 덮어쓰기 방지</span><span class="sxs-lookup"><span data-stu-id="04db9-158">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-159">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-159">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-160">다시 시작 시 메모리의 BitLocker 비밀을 덮어쓰지 않고 다시 시작 성능을 향상 시키려면이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-160">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="04db9-161">이 정책이 구성 되어 있지 않으면 컴퓨터가 다시 시작 될 때 BitLocker 비밀이 메모리에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-161">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-162">스마트 카드 인증서 용도 규칙 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="04db9-162">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-163">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-163">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-164">스마트 카드 인증서 기반 BitLocker 보호를 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-164">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="04db9-165">이 정책이 구성 되지 않은 경우에는 기본 개체 식별자 1.3.6.1.4.1.311.67.1.1를 사용 하 여 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-165">When this policy is not configured, the default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-166">조직의 고유 식별자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-166">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-167">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-167">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-168">인증서 기반 데이터 복구 에이전트 또는 BitLocker To Go 읽기 프로그램을 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-168">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="04db9-169">이 정책이 구성 되어 있지 않으면 <strong> 식별 </strong> 필드가 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-169">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="04db9-170">회사에서 더 높은 수준의 보안을 요구 하는 경우 <strong> id 필드를 구성 </strong> 하 여 모든 USB 장치에이 필드 집합을 포함 하 고이를이 그룹 정책 설정에 맞출지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-170">If your company requires higher security measurements, you can configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="04db9-171">클라이언트 관리 그룹 정책 정의</span><span class="sxs-lookup"><span data-stu-id="04db9-171">Client Management Group Policy definitions</span></span>

<span data-ttu-id="04db9-172">이 섹션에서는 다음 GPO 노드에서 mbam에 대 한 클라이언트 관리 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **클라이언트 관리**.</span><span class="sxs-lookup"><span data-stu-id="04db9-172">This section describes Client Management policy definitions for MBAM at the following GPO node: **Computer Configuration** &gt; **Policies** &gt;**Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Client Management**.</span></span>

<span data-ttu-id="04db9-173">다음 표에 표시 된 대로 구성 관리자 통합 토폴로지를 사용 하는 경우 한 가지 예외를 제외 하 고 독립 실행형 및 System Center Configuration \*\* &gt; \*\* Manager 통합 토폴로지에 대해 동일한 그룹 정책 설정을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-173">You can set the same Group Policy settings for the Stand-alone and System Center Configuration Manager Integration topologies, with one exception: Disable the **Configure MBAM Services &gt; MBAM Status reporting service endpoint** setting if you are using the Configuration Manager Integration topology, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-174">정책 이름</span><span class="sxs-lookup"><span data-stu-id="04db9-174">Policy name</span></span></th>
<th align="left"><span data-ttu-id="04db9-175">개요 및 제안 된 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-175">Overview and suggested Group Policy settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-176">MBAM 서비스 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-176">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-177">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-177">Suggested configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="04db9-178">MBAM 복구 및 하드웨어 서비스 끝점 </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-178">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="04db9-179">이 설정을 사용 하 여 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-179">Use this setting to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="04db9-180">다음 예제와 유사한 끝점 위치를 입력 합니다. <strong> http (s)// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가/MBAMRecoveryAndHardwareService/CoreService.svc에 바인딩된 포트입니다 &gt; </em><strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="04db9-180">Enter an endpoint location that is similar to the following example: <strong>http(s)://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;the port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-181">저장할 BitLocker 복구 정보를 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-181">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="04db9-182">이 정책 설정을 통해 BitLocker 복구 정보를 백업 하도록 키 복구 서비스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-182">This policy setting lets you configure the key recovery service to back up BitLocker recovery information.</span></span> <span data-ttu-id="04db9-183">또한 보고서를 수집 하는 상태 보고 서비스도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-183">It also lets you configure a status reporting service for collecting reports.</span></span> <span data-ttu-id="04db9-184">이 정책은 키 정보가 부족 하 여 데이터 손실을 방지 하기 위해 BitLocker에서 암호화 한 데이터를 복구 하는 관리 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-184">The policy provides an administrative method of recovering data encrypted by BitLocker to prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="04db9-185">상태 보고서 및 키 복구 작업이 자동으로 구성 된 보고서 서버 위치에 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-185">The status report and key recovery activity are automatically and silently sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="04db9-186">이 정책 설정을 구성 하지 않거나 사용 하지 않도록 설정 하면 키 복구 정보가 저장 되지 않으며 상태 보고서 및 키 복구 작업이 서버에 보고 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-186">If you do not configure this policy setting or if you disable it, the key recovery information is not saved, and the status report and key recovery activity are not reported to the server.</span></span> <span data-ttu-id="04db9-187">이 설정이 <strong> 복구 암호 및 키 패키지로 설정 되어 있으면 </strong> 복구 암호와 키 패키지가 자동으로 구성 된 키 복구 서버 위치에 백업 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-187">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package are automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-188">클라이언트 검사 상태 빈도를 분 단위로 입력 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-188">Enter client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="04db9-189">이 정책 설정은 클라이언트가 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하는 빈도를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-189">This policy setting manages how frequently the client checks the BitLocker protection policies and status on the client computer.</span></span> <span data-ttu-id="04db9-190">또한이 정책은 클라이언트 준수 상태가 서버에 저장 되는 빈도를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-190">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="04db9-191">클라이언트는 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하 고 구성 된 빈도로 클라이언트 복구 키를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-191">The client checks the BitLocker protection policies and status on the client computer and also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="04db9-192">회사에서 설정한 요구 사항에 따라 컴퓨터의 준수 상태를 확인 하는 빈도 및 클라이언트 복구 키를 백업 하는 빈도를 기준으로이 빈도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-192">Set this frequency based on the requirement set by your company on how frequently to check the compliance status of the computer and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-193">MBAM 상태 보고 서비스 끝점:</span><span class="sxs-lookup"><span data-stu-id="04db9-193">MBAM Status reporting service endpoint:</span></span></strong></p>
<p><strong><span data-ttu-id="04db9-194">독립 실행형 토폴로지에서 MBAM </strong> : Mbam 클라이언트 BitLocker 암호화 관리를 설정 하려면이 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-194">For MBAM in a Stand-alone topology</strong>: You must configure this setting to enable MBAM Client BitLocker encryption management.</span></span></p>
<p><span data-ttu-id="04db9-195">다음 예와 비슷한 끝점 위치를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-195">Enter an endpoint location that is similar to the following example:</span></span></p>
<p><strong><span data-ttu-id="04db9-196">http (s)// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가/MBAMComplianceStatusService/StatusReportingService.svc에 바인딩된 포트입니다. &gt; </em><strong></span><span class="sxs-lookup"><span data-stu-id="04db9-196">http(s)://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;the port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.svc</span></span></strong></p>
<p><strong><span data-ttu-id="04db9-197">Configuration Manager 통합 토폴로지의 MBAM </strong> :이 설정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-197">For MBAM in the Configuration Manager Integration topology</strong>: Disable this setting.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-198">사용자 예외 정책 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-198">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-199">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-199">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-200">이 정책 설정을 통해 사용자가 BitLocker 암호화에서 예외를 요청 하도록 하는 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-200">This policy setting lets you configure a website address, email address, or phone number that instructs a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="04db9-201">이 정책 설정을 사용 하 고 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 제공 하는 경우, 사용자는 BitLocker 보호에서 예외를 적용 하는 방법에 대 한 지침이 있는 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-201">If you enable this policy setting and provide a website address, email address, or phone number, users see a dialog box with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="04db9-202">사용자의 BitLocker 암호화 예외를 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)"> 사용자 Bitlocker 암호화 예외를 관리 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="04db9-202">For more information about enabling BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-25.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="04db9-203">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 예외 요청 지침이 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-203">If you either disable or do not configure this policy setting, the exemption request instructions are not displayed to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04db9-204">참고</span><span class="sxs-lookup"><span data-stu-id="04db9-204">Note</span></span></strong><br/><p><span data-ttu-id="04db9-205">사용자 예외는 컴퓨터당만 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-205">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="04db9-206">여러 사용자가 같은 컴퓨터에 로그온 하 고 한 사용자가 제외 되지 않은 경우 컴퓨터는 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-206">If multiple users log on to the same computer and any one user is not exempt, the computer is encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-207">사용자 환경 개선 프로그램 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-207">Configure customer experience improvement program</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-208">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-208">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-209">이 정책 설정을 사용 하면 사용자 환경 개선 프로그램에 MBAM이 참여할 수 있는 기간을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-209">This policy setting lets you configure how MBAM users can join the Customer Experience Improvement Program.</span></span> <span data-ttu-id="04db9-210">이 프로그램은 컴퓨터 하드웨어와 사용자가 작업을 중단 하지 않고 MBAM을 사용 하는 방법에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-210">This program collects information about computer hardware and how users use MBAM without interrupting their work.</span></span> <span data-ttu-id="04db9-211">이 정보는 Microsoft가 향상 시킬 MBAM 기능을 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-211">The information helps Microsoft to identify which MBAM features to improve.</span></span> <span data-ttu-id="04db9-212">Microsoft는이 정보를 사용 하 여 MBAM 사용자를 식별 하거나 연락 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-212">Microsoft does not use this information to identify or contact MBAM users.</span></span></p>
<p><span data-ttu-id="04db9-213">이 정책 설정을 사용 하면 사용자 환경 개선 프로그램에 참가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-213">If you enable this policy setting, users can join the Customer Experience Improvement Program.</span></span></p>
<p><span data-ttu-id="04db9-214">이 정책을 사용 하지 않도록 설정 하면 사용자 환경 개선 프로그램에 참여할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-214">If you disable this policy setting, users cannot join the Customer Experience Improvement Program.</span></span></p>
<p><span data-ttu-id="04db9-215">이 정책 설정을 구성 하지 않으면 사용자 환경 개선 프로그램에 참가할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-215">If you do not configure this policy setting, users have the option to join the Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-216">보안 정책 링크의 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-216">Provide the URL for the Security Policy link</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-217">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-217">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-218">이 정책 설정을 사용 하 여 최종 사용자에 게 회사 보안 정책 이라는 링크로 표시 되는 URL을 지정 &quot; 합니다. &quot; 링크는 회사의 내부 보안 정책을 가리키고 최종 사용자에 게 암호화 요구 사항에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-218">Use this policy setting to specify a URL that is displayed to end users as a link named &quot;Company Security Policy.&quot; The link points to your company’s internal security policy and provides end users with information about encryption requirements.</span></span> <span data-ttu-id="04db9-219">드라이브를 암호화 하기 위해 사용자에 게 메시지를 표시 하는 경우에는 MBAM이 링크를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-219">The link appears when users are prompted by MBAM to encrypt a drive.</span></span></p>
<p><span data-ttu-id="04db9-220">이 정책 설정을 사용 하도록 설정 하는 경우 보안 정책 링크에 대 한 URL을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-220">If you enable this policy setting, you can configure the URL for the Security Policy link.</span></span></p>
<p><span data-ttu-id="04db9-221">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 보안 정책 링크가 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-221">If you disable or do not configure this policy setting, the Security Policy link is not displayed to users.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="04db9-222">고정 드라이브 그룹 정책 정의</span><span class="sxs-lookup"><span data-stu-id="04db9-222">Fixed Drive Group Policy definitions</span></span>

<span data-ttu-id="04db9-223">이 섹션에서는 다음 GPO 노드에서 Microsoft BitLocker 관리 및 모니터링에 대 한 고정 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **고정식 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="04db9-223">This section describes Fixed Drive policy definitions for Microsoft BitLocker Administration and Monitoring at the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-224">정책 이름</span><span class="sxs-lookup"><span data-stu-id="04db9-224">Policy name</span></span></th>
<th align="left"><span data-ttu-id="04db9-225">개요 및 제안 된 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-225">Overview and suggested Group Policy settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-226">고정 데이터 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-226">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-227">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-227">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-228">이 정책 설정을 통해 고정 데이터 드라이브를 암호화할지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-228">This policy setting lets you manage whether fixed data drives must be encrypted.</span></span></p>
<p><span data-ttu-id="04db9-229">운영 체제 볼륨을 암호화 해야 하는 경우에는 <strong> 고정 데이터 드라이브 자동 잠금 해제 사용을 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-229">If the operating system volume is required to be encrypted, click <strong>Enable auto-unlock fixed data drive</strong>.</span></span></p>
<p><span data-ttu-id="04db9-230">이 정책을 사용 하는 경우 <strong> </strong> 고정 데이터 드라이브에 대 한 자동 잠금 해제를 사용 하도록 설정 하거나 요구 하지 않는 한 고정 데이터 드라이브에 대 한 암호 사용 구성을 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-230">When you enable this policy, you must not disable the <strong>Configure use of password for fixed data drives</strong> policy unless you are enabling or requiring the use of auto-unlock for fixed data drives.</span></span></p>
<p><span data-ttu-id="04db9-231">고정 데이터 드라이브에 대 한 자동 잠금 해제를 사용 해야 하는 경우 운영 체제 볼륨을 암호화 하도록 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-231">If you have to use auto-unlock for fixed data drives, you must configure operating system volumes to be encrypted.</span></span></p>
<p><span data-ttu-id="04db9-232">이 정책 설정을 사용 하면 사용자가 모든 고정 데이터 드라이브를 BitLocker 보호에 포함 해야 하며 데이터 드라이브는 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-232">If you enable this policy setting, users are required to put all fixed data drives under BitLocker protection, and the data drives are then encrypted.</span></span></p>
<p><span data-ttu-id="04db9-233">이 정책 설정을 구성 하지 않으면 사용자가 BitLocker 보호 아래에 고정 데이터 드라이브를 추가할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-233">If you do not configure this policy setting, users are not required to put fixed data drives under BitLocker protection.</span></span> <span data-ttu-id="04db9-234">고정 데이터 드라이브가 암호화 된 후이 정책을 적용 하면 MBAM 에이전트는 암호화 된 고정 데이터 드라이브의 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-234">If you apply this policy after fixed data drives are encrypted, the MBAM agent decrypts the encrypted fixed data drives.</span></span></p>
<p><span data-ttu-id="04db9-235">이 정책 설정을 사용 하지 않으면 사용자가 BitLocker 보호에 고정 데이터 드라이브를 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-235">If you disable this policy setting, users cannot put their fixed data drives under BitLocker protection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-236">BitLocker에 의해 보호되지 않는 고정 드라이브에 대한 쓰기 액세스 거부</span><span class="sxs-lookup"><span data-stu-id="04db9-236">Deny write access to fixed drives not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-237">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-237">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-238">이 정책 설정은 컴퓨터에서 고정 데이터 드라이브를 쓰기 가능 하 게 하기 위해 BitLocker 보호가 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-238">This policy setting determines whether BitLocker protection is required for fixed data drives to be writable on a computer.</span></span> <span data-ttu-id="04db9-239">이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-239">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="04db9-240">정책이 구성 되지 않은 경우 컴퓨터의 모든 고정 데이터 드라이브는 읽기/쓰기 권한으로 탑재 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-240">When the policy is not configured, all fixed data drives on the computer are mounted with read/write permission.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-241">이전 버전의 Windows에서 BitLocker로 보호 되는 고정 드라이브에 대 한 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="04db9-241">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-242">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-242">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-243">Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 수정 된 드라이브를 잠금 해제 하 고 볼 수 있도록이 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-243">Enable this policy so that fixed drives with the FAT file system can be unlocked and viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="04db9-244">정책을 사용 하거나 구성 하지 않으면 FAT 파일 시스템으로 포맷 된 고정 드라이브를 잠금 해제할 수 있으며 windows Server 2008, Windows Vista, Windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-244">When the policy is enabled or not configured, fixed drives that are formatted with the FAT file system can be unlocked and their content can be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span> <span data-ttu-id="04db9-245">이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-245">These operating systems have read-only permission to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="04db9-246">정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 된 고정 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-246">When the policy is disabled, fixed drives that are formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-247">고정 드라이브의 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-247">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-248">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-248">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-249">이 정책을 사용 하 여 BitLocker로 보호 된 고정 데이터 드라이브의 잠금을 해제 하는 데 암호가 필요한 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-249">Use this policy to specify whether a password is required to unlock BitLocker-protected fixed data drives.</span></span></p>
<p><span data-ttu-id="04db9-250">이 정책 설정을 사용 하면 사용자가 정의한 요구 사항을 충족 하는 암호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-250">If you enable this policy setting, users can configure a password that meets the requirements that you define.</span></span> <span data-ttu-id="04db9-251">BitLocker는 사용자가 드라이브에서 사용할 수 있는 모든 보호기를 사용 하 여 드라이브 잠금을 해제할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-251">BitLocker enables users to unlock a drive with any of the protectors that are available on the drive.</span></span></p>
<p><span data-ttu-id="04db9-252">이러한 설정은 볼륨을 잠금 해제할 때가 아닌 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-252">These settings are enforced when you turn on BitLocker, not when you unlock a volume.</span></span></p>
<p><span data-ttu-id="04db9-253">이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-253">If you disable this policy setting, users are not allowed to use a password.</span></span></p>
<p><span data-ttu-id="04db9-254">정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-254">When the policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and which require only eight characters.</span></span></p>
<p><span data-ttu-id="04db9-255">보안을 강화 하려면이 정책을 사용 하도록 설정한 다음 <strong> 고정 데이터 드라이브에 대해 암호 요구를 선택 하 고 </strong> <strong> 암호 복잡도 필요를 클릭 하 </strong> 고 <strong> 원하는 최소 암호 길이를 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-255">For higher security, enable this policy, and then select <strong>Require password for fixed data drive</strong>, click <strong>Require password complexity</strong>, and set the <strong>minimum password length</strong> that you want.</span></span></p>
<p><span data-ttu-id="04db9-256">이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-256">If you disable this policy setting, users are not allowed to use a password.</span></span></p>
<p><span data-ttu-id="04db9-257">이 정책 설정을 구성 하지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-257">If you do not configure this policy setting, passwords are supported with the default settings, which do not include password complexity requirements and which require only eight characters.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-258">BitLocker로 보호 되는 고정 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="04db9-258">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-259">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-259">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-260">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-260">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="04db9-261">정책이 구성 되어 있지 않으면 BitLocker 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-261">When the policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="04db9-262">MBAM에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-262">MBAM does not require recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-263">암호화 정책 적용 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-263">Encryption Policy Enforcement Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-264">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-264">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-265">이 정책 설정을 사용 하 여 고정 데이터 드라이브가 MBAM 정책에 부합 될 때까지 비규격으로 유지 될 수 있는 날짜 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-265">Use this policy setting to configure the number of days that fixed data drives can remain noncompliant until they are forced to comply with MBAM policies.</span></span> <span data-ttu-id="04db9-266">사용자는 필요한 작업을 연기 하거나 유예 기간 후에 예외를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-266">Users cannot postpone the required action or request an exemption from it after the grace period.</span></span> <span data-ttu-id="04db9-267">유예 기간은 고정 데이터 드라이브가 비규격 인 것으로 판단 되는 경우 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-267">The grace period starts when the fixed data drive is determined to be noncompliant.</span></span> <span data-ttu-id="04db9-268">그러나 고정 데이터 드라이브 정책은 운영 체제 드라이브가 호환 될 때까지 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-268">However, the fixed data drive policy is not enforced until the operating system drive is compliant.</span></span></p>
<p><span data-ttu-id="04db9-269">유예 기간이 만료 되 고 고정 데이터 드라이브가 여전히 호환 되지 않는 경우 사용자는 예외를 연기 하거나 요청 하는 옵션을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-269">If the grace period expires and the fixed data drive is still not compliant, users do not have the option to postpone or to request an exemption.</span></span> <span data-ttu-id="04db9-270">암호화 프로세스에 사용자 입력이 필요한 경우 필요한 정보를 제공할 때까지 사용자가 닫을 수 없는 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-270">If the encryption process requires user input, a dialog box appears that users cannot close until they provide the required information.</span></span></p>
<p><span data-ttu-id="04db9-271"><strong> </strong> <strong> </strong> 운영 체제 드라이브에 대 한 유예 기간이 만료 된 후 즉시 암호화 프로세스가 시작 되도록 하려면 0을 입력 하 여 고정 드라이브의 비 준수 유예 기간 일 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-271">Enter <strong>0</strong> in the <strong>Configure the number of noncompliance grace period days for fixed drives</strong> to force the encryption process to begin immediately after the grace period expires for the operating system drive.</span></span></p>
<p><span data-ttu-id="04db9-272">이 설정을 사용 하지 않거나 구성 하지 않으면 사용자가 MBAM 정책에 부합 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-272">If you disable or do not configure this setting, users are not forced to comply with MBAM policies.</span></span></p>
<p><span data-ttu-id="04db9-273">보호기를 추가 하기 위해 사용자 조작이 필요 하지 않은 경우, 유예 기간이 만료 된 후 백그라운드에서 암호화가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-273">If no user interaction is required to add a protector, encryption begins in the background after the grace period expires.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="04db9-274">운영 체제 드라이브 그룹 정책 정의</span><span class="sxs-lookup"><span data-stu-id="04db9-274">Operating System Drive Group Policy definitions</span></span>

<span data-ttu-id="04db9-275">이 섹션에서는 다음 GPO 노드에서 Microsoft BitLocker 관리 및 모니터링에 대 한 운영 체제 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **운영 체제 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="04db9-275">This section describes Operating System Drive policy definitions for Microsoft BitLocker Administration and Monitoring at the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-276">정책 이름</span><span class="sxs-lookup"><span data-stu-id="04db9-276">Policy name</span></span></th>
<th align="left"><span data-ttu-id="04db9-277">개요 및 제안 된 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-277">Overview and suggested Group Policy settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-278">운영 체제 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-278">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-279">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-279">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-280">이 정책 설정을 통해 운영 체제 드라이브를 암호화 해야 하는지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-280">This policy setting lets you manage whether the operating system drive must be encrypted.</span></span></p>
<p><span data-ttu-id="04db9-281">보안을 강화 하려면 <strong> </strong> &gt; <strong> </strong> &gt; <strong> </strong> TPM + PIN 보호기를 사용 하 여 시스템 전원 관리 절전 모드 설정에서 다음 정책 설정을 해제 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-281">For higher security, consider disabling the following policy settings in <strong>System</strong> &gt; <strong>Power Management</strong> &gt; <strong>Sleep Settings</strong> when you enable them with TPM + PIN protector:</span></span></p>
<ul>
<li><p><span data-ttu-id="04db9-282">절전 모드에서 대기 상태 (S1-S3) 허용 (전원 사용)</span><span class="sxs-lookup"><span data-stu-id="04db9-282">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="04db9-283">절전 모드 시 대기 상태 (S1-S3) 허용 (배터리 사용)</span><span class="sxs-lookup"><span data-stu-id="04db9-283">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul>
<p><span data-ttu-id="04db9-284">Microsoft Windows 8 이상을 실행 중이 고 TPM이 없는 컴퓨터에서 BitLocker를 사용 하려는 경우 <strong> 호환 되는 tpm이 없는 bitlocker 허용 확인란을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-284">If you are running Microsoft Windows 8 or later, and you want to use BitLocker on a computer without a TPM, select the <strong>Allow BitLocker without a compatible TPM</strong> check box.</span></span> <span data-ttu-id="04db9-285">이 모드에서는 시작 하는 데 암호가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-285">In this mode, a password is required for startup.</span></span> <span data-ttu-id="04db9-286">암호를 잊어버린 경우 BitLocker 복구 옵션 중 하나를 사용 하 여 드라이브에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-286">If you forget the password, you have to use one of the BitLocker recovery options to access the drive.</span></span></p>
<p><span data-ttu-id="04db9-287">호환 되는 TPM이 있는 컴퓨터에서는 시작 시 암호화 된 데이터에 대 한 추가 보호를 제공 하기 위해 두 가지 유형의 인증 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-287">On a computer with a compatible TPM, two types of authentication methods can be used at startup to provide added protection for encrypted data.</span></span> <span data-ttu-id="04db9-288">컴퓨터가 시작 되 면 인증에 TPM만 사용 하거나 PIN (개인 식별 번호)을 입력 해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-288">When the computer starts, it can use only the TPM for authentication, or it can also require the entry of a personal identification number (PIN).</span></span></p>
<p><span data-ttu-id="04db9-289">이 정책 설정을 사용 하면 사용자가 BitLocker protection에 운영 체제 드라이브를 설치 하 고 드라이브가 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-289">If you enable this policy setting, users have to put the operating system drive under BitLocker protection, and the drive is then encrypted.</span></span></p>
<p><span data-ttu-id="04db9-290">이 정책을 사용 하지 않도록 설정 하는 경우 사용자는 BitLocker protection에 운영 체제 드라이브를 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-290">If you disable this policy, users cannot put the operating system drive under BitLocker protection.</span></span> <span data-ttu-id="04db9-291">운영 체제 드라이브를 암호화 한 후에이 정책을 적용 하면 드라이브의 암호가 해독 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-291">If you apply this policy after the operating system drive is encrypted, the drive is then decrypted.</span></span></p>
<p><span data-ttu-id="04db9-292">이 정책을 구성 하지 않으면, 운영 체제 드라이브를 BitLocker 보호 아래에 배치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-292">If you do not configure this policy, the operating system drive is not required to be placed under BitLocker protection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-293">시작 시 향상 된 Pin 허용</span><span class="sxs-lookup"><span data-stu-id="04db9-293">Allow enhanced PINs for startup</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-294">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-294">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-295">이 정책 설정을 사용 하 여 향상 된 시작 Pin을 BitLocker와 함께 사용할지 여부를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-295">Use this policy setting to configure whether enhanced startup PINs are used with BitLocker.</span></span> <span data-ttu-id="04db9-296">향상 된 시작 Pin에는 대/소문자, 기호, 숫자, 공백 등의 문자 사용이 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-296">Enhanced startup PINs permit the use of characters including uppercase and lowercase letters, symbols, numbers, and spaces.</span></span> <span data-ttu-id="04db9-297">이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-297">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="04db9-298">이 정책 설정을 사용 하면 모든 새 BitLocker 시작 Pin이 설정 되어 최종 사용자가 향상 된 Pin을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-298">If you enable this policy setting, all new BitLocker startup PINs set will enable end user to create enhanced PINs.</span></span> <span data-ttu-id="04db9-299">그러나 일부 컴퓨터는 사전 부팅 환경에서 향상 된 Pin을 지원할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-299">However, not all computers can support enhanced PINs in the pre-boot environment.</span></span> <span data-ttu-id="04db9-300">관리자가 사용 하도록 설정 하기 전에 해당 시스템이이 기능과 호환 되는지 여부를 평가 하도록 강력히 권장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-300">We strongly recommend that administrators evaluate whether their systems are compatible with this feature before enabling its use.</span></span></p>
<p><span data-ttu-id="04db9-301"><strong> </strong> 프리 부팅 환경에 입력할 수 있는 문자 종류 또는 수를 제한 하는 컴퓨터와 향상 된 pin을 더 호환 되도록 하려면 ASCII 전용 pin 필요 확인란을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-301">Select the <strong>Require ASCII-only PINs</strong> check box to help make enhanced PINs more compatible with computers that limit the type or number of characters that can be entered in the pre-boot environment.</span></span></p>
<p><span data-ttu-id="04db9-302">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 강화 된 Pin이 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-302">If you disable or do not configure this policy setting, enhanced PINs are not used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-303">BitLocker로 보호 되는 운영 체제 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="04db9-303">Choose how BitLocker-protected operating system drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-304">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-304">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-305">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-305">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="04db9-306">이 정책이 구성 되어 있지 않으면 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-306">When this policy is not configured, the data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="04db9-307">MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-307">MBAM operation does not require recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-308">운영 체제 드라이브에 대 한 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-308">Configure use of passwords for operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-309">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-309">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-310">BitLocker로 보호 되는 운영 체제 드라이브의 잠금을 해제 하는 데 사용 되는 암호에 대 한 제약 조건을 설정 하려면이 정책 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-310">Use this policy setting to set the constraints for passwords that are used to unlock BitLocker-protected operating system drives.</span></span> <span data-ttu-id="04db9-311">운영 체제 드라이브에서 TPM이 아닌 보호기를 사용할 수 있는 경우 암호를 프로 비전 하 고 암호에 복잡성 요구 사항을 적용 하 고 암호의 최소 길이를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-311">If non-TPM protectors are allowed on operating system drives, you can provision a password, enforce complexity requirements on the password, and configure a minimum length for the password.</span></span> <span data-ttu-id="04db9-312">복잡 한 요구 사항 설정을 적용 하려면 그룹 정책 설정 &quot; 암호가 &quot; 컴퓨터 구성 &gt; Windows 설정 &gt; 보안 설정 &gt; 계정 정책 &gt; 암호 정책에 있는 복잡성 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-312">For the complexity requirement setting to be effective, you must also enable the Group Policy setting &quot;Password must meet complexity requirements&quot; located in Computer Configuration &gt; Windows Settings &gt; Security Settings &gt; Account Policies &gt; Password Policy.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04db9-313">참고</span><span class="sxs-lookup"><span data-stu-id="04db9-313">Note</span></span></strong><br/><p><span data-ttu-id="04db9-314">이러한 설정은 볼륨을 잠금 해제할 때가 아닌 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-314">These settings are enforced when you turn on BitLocker, not when you unlock a volume.</span></span> <span data-ttu-id="04db9-315">BitLocker를 사용 하면 드라이브에서 사용할 수 있는 모든 보호기를 사용 하 여 드라이브 잠금을 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-315">BitLocker lets you unlock a drive with any of the protectors that are available on the drive.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="04db9-316">이 정책 설정을 사용 하면 사용자가 정의한 요구 사항을 충족 하는 암호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-316">If you enable this policy setting, users can configure a password that meets the requirements that you define.</span></span> <span data-ttu-id="04db9-317">비밀 번호에 복잡성을 적용 하려면 <strong> 비밀 번호 복잡성 요구를 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-317">To enforce complexity requirements on the password, click <strong>Require password complexity</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-318">BIOS 기반 펌웨어 구성에 대 한 TPM 플랫폼 유효성 검사 프로필 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-318">Configure TPM platform validation profile for BIOS-based firmware configurations</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-319">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-319">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-320">이 정책 설정을 통해 컴퓨터&#39;s TPM (신뢰할 수 있는 플랫폼 모듈) 보안 하드웨어에서 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-320">This policy setting allows you to configure how the computer&#39;s Trusted Platform Module (TPM) security hardware secures the BitLocker encryption key.</span></span> <span data-ttu-id="04db9-321">컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-321">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker has already been turned on with TPM protection.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04db9-322">중요</span><span class="sxs-lookup"><span data-stu-id="04db9-322">Important</span></span></strong><br/><p><span data-ttu-id="04db9-323">이 그룹 정책 설정은 BIOS 구성을 사용 하는 컴퓨터에만 적용 되 고 CSM (호환성 서비스 모듈)가 설정 된 UEFI 펌웨어가 있는 컴퓨터에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-323">This Group Policy setting applies only to computers with BIOS configurations or to computers with UEFI firmware with a Compatibility Service Module (CSM) enabled.</span></span> <span data-ttu-id="04db9-324">네이티브 UEFI 펌웨어 구성을 사용 하는 컴퓨터는 플랫폼 구성 레지스터 (PCRs)에 여러 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-324">Computers that use a native UEFI firmware configuration store different values into the Platform Configuration Registers (PCRs).</span></span> <span data-ttu-id="04db9-325">기본 uefi 펌웨어 구성 &quot; 에 tpm 플랫폼 유효성 검사 프로필 구성 &quot; 그룹 정책 설정을 사용 하 여 네이티브 uefi 펌웨어를 사용 하는 컴퓨터에 대 한 tpm PCR 프로필을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-325">Use the &quot;Configure TPM platform validation profile for native UEFI firmware configurations&quot; Group Policy setting to configure the TPM PCR profile for computers that use native UEFI firmware.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="04db9-326">BitLocker를 설정 하기 전에이 정책 설정을 사용 하도록 설정 하면 BitLocker로 암호화 된 운영 체제 드라이브에 대 한 액세스를 잠금 해제 하기 전에 TPM에서 유효성을 검사 하는 부팅 구성 요소를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-326">If you enable this policy setting before you turn on BitLocker, you can configure the boot components that the TPM validates before you unlock access to the BitLocker-encrypted operating system drive.</span></span> <span data-ttu-id="04db9-327">BitLocker 보호가 적용 되는 동안 이러한 구성 요소 중 하나라도 변경 되 면 TPM은 암호화 키를 해제 하 여 드라이브 잠금을 해제 하지 않으며, 컴퓨터는 BitLocker 복구 콘솔을 표시 하 고 복구 암호 또는 복구 키를 제공 하 여 드라이브 잠금을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-327">If any of these components change while BitLocker protection is in effect, the TPM does not release the encryption key to unlock the drive and the computer instead displays the BitLocker Recovery console and requires that you provide either the recovery password or recovery key to unlock the drive.</span></span></p>
<p><span data-ttu-id="04db9-328">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 BitLocker는 설치 스크립트에 지정 된 기본 플랫폼 유효성 검사 프로필 또는 플랫폼 유효성 검사 프로필을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-328">If you disable or do not configure this policy setting, BitLocker uses the default platform validation profile or the platform validation profile that is specified by the Setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-329">TPM 플랫폼 유효성 검사 프로필 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-329">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-330">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-330">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-331">이 정책 설정을 사용 하 여 컴퓨터&#39;s TPM (신뢰할 수 있는 플랫폼 모듈) 보안 하드웨어에서 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-331">This policy setting enables you to configure how the computer&#39;s Trusted Platform Module (TPM) security hardware secures the BitLocker encryption key.</span></span> <span data-ttu-id="04db9-332">컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-332">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker has already been turned on with TPM protection.</span></span></p>
<p><span data-ttu-id="04db9-333">BitLocker를 설정 하기 전에이 정책 설정을 사용 하도록 설정 하면 BitLocker로 암호화 된 운영 체제 드라이브에 대 한 액세스를 잠금 해제 하기 전에 TPM에서 유효성을 검사 하는 부팅 구성 요소를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-333">If you enable this policy setting before you turn on BitLocker, you can configure the boot components that the TPM validates before you unlock access to the BitLocker-encrypted operating system drive.</span></span> <span data-ttu-id="04db9-334">BitLocker 보호가 적용 되는 동안 이러한 구성 요소 중 하나라도 변경 되 면 TPM은 암호화 키를 해제 하 여 드라이브 잠금을 해제 하지 않으며, 컴퓨터는 BitLocker 복구 콘솔을 표시 하 고 복구 암호 또는 복구 키를 제공 하 여 드라이브 잠금을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-334">If any of these components change while BitLocker protection is in effect, the TPM does not release the encryption key to unlock the drive and the computer instead displays the BitLocker Recovery console and requires that you provide either the recovery password or recovery key to unlock the drive.</span></span></p>
<p><span data-ttu-id="04db9-335">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 BitLocker는 설치 스크립트에 지정 된 기본 플랫폼 유효성 검사 프로필 또는 플랫폼 유효성 검사 프로필을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-335">If you disable or do not configure this policy setting, BitLocker uses the default platform validation profile or the platform validation profile that is specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-336">기본 UEFI 펌웨어 구성에 대 한 TPM 플랫폼 유효성 검사 프로필 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-336">Configure TPM platform validation profile for native UEFI firmware configurations</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-337">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-337">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-338">이 정책 설정을 통해 컴퓨터&#39;s TPM (신뢰할 수 있는 플랫폼 모듈) 보안 하드웨어에서 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-338">This policy setting allows you to configure how the computer&#39;s Trusted Platform Module (TPM) security hardware secures the BitLocker encryption key.</span></span> <span data-ttu-id="04db9-339">컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-339">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker has already been turned on with TPM protection.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04db9-340">중요</span><span class="sxs-lookup"><span data-stu-id="04db9-340">Important</span></span></strong><br/><p><span data-ttu-id="04db9-341">이 그룹 정책 설정은 네이티브 UEFI 펌웨어 구성을 사용 하는 컴퓨터에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-341">This Group Policy setting applies only to computers with a native UEFI firmware configuration.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="04db9-342">BitLocker를 설정 하기 전에이 정책 설정을 사용 하면 BitLocker로 암호화 된 운영 체제 드라이브에 대 한 액세스를 잠금 해제 하기 전에 TPM에서 유효성을 검사 하는 부팅 구성 요소를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-342">If you enable this policy setting before you turn on BitLocker, you can configure the boot components that the TPM validates before unlocking access to the BitLocker-encrypted operating system drive.</span></span> <span data-ttu-id="04db9-343">BitLocker 보호가 적용 되는 동안 이러한 구성 요소 중 하나라도 변경 되 면 TPM은 암호화 키를 해제 하 여 드라이브 잠금을 해제 하지 않으며, 컴퓨터는 BitLocker 복구 콘솔을 표시 하 고 복구 암호 또는 복구 키를 제공 하 여 드라이브 잠금을 해제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-343">If any of these components change while BitLocker protection is in effect, the TPM does not release the encryption key to unlock the drive and the computer instead displays the BitLocker Recovery console and requires that you provide either the recovery password or recovery key to unlock the drive.</span></span></p>
<p><span data-ttu-id="04db9-344">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 BitLocker는 설치 스크립트에 지정 된 기본 플랫폼 유효성 검사 프로필 또는 플랫폼 유효성 검사 프로필을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-344">If you disable or do not configure this policy setting, BitLocker uses the default platform validation profile or the platform validation profile that is specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-345">BitLocker 복구 후 플랫폼 유효성 검사 데이터 다시 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-345">Reset platform validation data after BitLocker recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-346">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-346">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-347">BitLocker 복구 후 Windows를 시작할 때 플랫폼 유효성 검사 데이터를 새로 고칠지 여부를 제어 하려면이 정책 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-347">Use this policy setting to control whether platform validation data is refreshed when Windows is started after BitLocker recovery.</span></span></p>
<p><span data-ttu-id="04db9-348">이 정책 설정을 사용 하면 BitLocker 복구 후 Windows가 시작 될 때 플랫폼 유효성 검사 데이터가 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-348">If you enable this policy setting, platform validation data are refreshed when Windows is started after BitLocker recovery.</span></span> <span data-ttu-id="04db9-349">이 정책 설정을 사용 하지 않으면 BitLocker 복구 이후 Windows가 시작 될 때 플랫폼 유효성 검사 데이터가 새로 고쳐지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-349">If you disable this policy setting, platform validation data are not refreshed when Windows is started after BitLocker recovery.</span></span> <span data-ttu-id="04db9-350">이 정책 설정을 구성 하지 않으면 BitLocker 복구 후 Windows가 시작 될 때 플랫폼 유효성 검사 데이터가 새로 고쳐집니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-350">If you do not configure this policy setting, platform validation data are refreshed when Windows is started after BitLocker recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-351">향상 된 부팅 구성 데이터 유효성 검사 프로필 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-351">Use enhanced Boot Configuration Data validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-352">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-352">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-353">이 정책 설정을 통해 플랫폼 유효성 검사 중에 확인할 특정 BCD (부팅 구성 데이터) 설정을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-353">This policy setting allows you to choose specific Boot Configuration Data (BCD) settings to verify during platform validation.</span></span></p>
<p><span data-ttu-id="04db9-354">이 정책 설정을 사용 하면 다른 설정을 추가 하거나 기본 설정을 제거 하거나 둘 다 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-354">If you enable this policy setting, you can add additional settings, remove the default settings, or both.</span></span> <span data-ttu-id="04db9-355">이 정책 설정을 사용 하지 않으면 컴퓨터가 Windows 7에서 사용 하는 기본 BCD 프로필과 비슷한 BCD 프로필로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-355">If you disable this policy setting, the computer reverts to a BCD profile similar to the default BCD profile that is used by Windows 7.</span></span> <span data-ttu-id="04db9-356">이 정책 설정을 구성 하지 않으면 컴퓨터에서 기본 Windows BCD 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-356">If you do not configure this policy setting, the computer verifies the default Windows BCD settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04db9-357">참고</span><span class="sxs-lookup"><span data-stu-id="04db9-357">Note</span></span></strong><br/><p><span data-ttu-id="04db9-358">BitLocker에서 무결성 유효성 검사에 보안 부팅 허용 정책에 정의 된 대로 플랫폼 및 BCD (부팅 구성 데이터) 무결성 유효성 검사에 대 한 보안 부팅을 사용 하는 경우 &quot; &quot; 향상 된 &quot; 부팅 구성 데이터 유효성 검사 프로필 &quot; 정책 사용이 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-358">When BitLocker uses Secure Boot for platform and Boot Configuration Data (BCD) integrity validation, as defined by the &quot;Allow Secure Boot for integrity validation&quot; policy, the &quot;Use enhanced Boot Configuration Data validation profile&quot; policy is ignored.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="04db9-359">부팅 디버깅 (0x16000010)을 제어 하는 설정은 항상 유효성을 검사 하며 제공 된 필드에 포함 된 경우 아무런 영향도 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-359">The setting that controls boot debugging (0x16000010) is always validated and has no effect if it is included in the provided fields.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-360">암호화 정책 적용 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-360">Encryption Policy Enforcement Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-361">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-361">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-362">이 정책 설정을 사용 하 여 사용자가 운영 체제 드라이브에 대 한 MBAM 정책 준수를 연기할 수 있는 일 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-362">Use this policy setting to configure the number of days that users can postpone complying with MBAM policies for their operating system drive.</span></span> <span data-ttu-id="04db9-363">유예 기간은 비규격으로 운영 체제를 처음 검색할 때 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-363">The grace period begins when the operating system is first detected as noncompliant.</span></span> <span data-ttu-id="04db9-364">이 유예 기간이 만료 된 후에는 사용자가 필요한 작업을 연기 하거나 예외를 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-364">After this grace period expires, users cannot postpone the required action or request an exemption from it.</span></span></p>
<p><span data-ttu-id="04db9-365">암호화 프로세스에 사용자 입력이 필요한 경우 필요한 정보를 제공할 때까지 사용자가 닫을 수 없는 대화 상자가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-365">If the encryption process requires user input, a dialog box appears that users cannot close until they provide the required information.</span></span></p>
<p><span data-ttu-id="04db9-366">이 설정을 사용 하지 않거나 구성 하지 않으면 사용자가 MBAM 정책에 부합 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-366">If you disable or do not configure this setting, users are not forced to comply with MBAM policies.</span></span></p>
<p><span data-ttu-id="04db9-367">보호기를 추가 하기 위해 사용자 조작이 필요 하지 않은 경우, 유예 기간이 만료 된 후 백그라운드에서 암호화가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-367">If no user interaction is required to add a protector, encryption begins in the background after the grace period expires.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-368">사전 부팅 복구 메시지 및 URL 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-368">Configure pre-boot recovery message and URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-369">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-369">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-370">이 정책 설정을 사용 하 여 사용자 지정 복구 메시지를 구성 하거나 OS 드라이브가 잠길 때 사전 부팅 BitLocker 복구 화면에 표시 되는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-370">Enable this policy setting to configure a custom recovery message or to specify a URL that is then displayed on the pre-boot BitLocker recovery screen when the OS drive is locked.</span></span> <span data-ttu-id="04db9-371">이 설정은 Windows 10을 실행 하는 클라이언트 컴퓨터 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-371">This setting is only available on client computers running Windows 10.</span></span></p>
<p><span data-ttu-id="04db9-372">이 정책을 사용 하는 경우 사전 부팅 복구 메시지에 대해 다음 옵션 중 하나를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-372">When this policy is enabled, you can select one of these options for the pre-boot recovery message:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="04db9-373">사용자 지정 복구 메시지 사용 </strong> : 사전 부팅 BitLocker 복구 화면에 사용자 지정 메시지를 포함 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-373">Use custom recovery message</strong>: Select this option to include a custom message in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="04db9-374"><strong>사용자 지정 복구 메시지 옵션 </strong> 상자에 표시할 메시지를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-374">In the <strong>Custom recovery message option</strong> box, type the message that you want displayed.</span></span> <span data-ttu-id="04db9-375">복구 URL도 지정 하려는 경우에는 사용자 지정 복구 메시지의 일부로 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-375">If you also want to specify a recovery URL, include it as part of your custom recovery message.</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-376">사용자 지정 복구 URL 사용 </strong> : 사전 부팅 BitLocker 복구 화면에 표시 되는 기본 URL을 바꾸려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-376">Use custom recovery URL</strong>: Select this option to replace the default URL that is displayed in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="04db9-377"><strong>사용자 지정 복구 URL 옵션 </strong> 상자에 표시할 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-377">In the <strong>Custom recovery URL option</strong> box, type the URL that you want displayed.</span></span></p></li>
<li><p><strong><span data-ttu-id="04db9-378">기본 복구 메시지 및 URL 사용 </strong> : 사전 부팅 BitLocker 복구 화면에 기본 BitLocker 복구 메시지 및 url을 표시 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-378">Use default recovery message and URL</strong>: Select this option to display the default BitLocker recovery message and URL in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="04db9-379">이전에 사용자 지정 복구 메시지 또는 URL을 구성한 경우 기본 메시지로 돌아가려면이 정책을 사용 하도록 설정 하 고 <strong> 기본 복구 메시지 및 URL 사용 옵션을 선택 해야 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="04db9-379">If you previously configured a custom recovery message or URL and want to revert to the default message, you must enable this policy and select the <strong>Use default recovery message and URL</strong> option.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="04db9-380">참고</span><span class="sxs-lookup"><span data-stu-id="04db9-380">Note</span></span></strong><br/><p><span data-ttu-id="04db9-381">모든 문자 및 언어가 사전 부팅에서 지원 되는 것은 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-381">Not all characters and languages are supported in pre-boot.</span></span> <span data-ttu-id="04db9-382">사전 부팅 BitLocker 복구 화면에서 사용자 지정 메시지 또는 URL에 사용 하는 문자가 올바르게 표시 되는지 테스트 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-382">We recommend that you test that the characters you use for the custom message or URL appear correctly on the pre-boot BitLocker recovery screen.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="04db9-383">이동식 드라이브 그룹 정책 정의</span><span class="sxs-lookup"><span data-stu-id="04db9-383">Removable Drive Group Policy definitions</span></span>

<span data-ttu-id="04db9-384">이 섹션에서는 다음 GPO 노드에서 Microsoft BitLocker 관리 및 모니터링을 위한 이동식 드라이브 그룹 정책 정의에 대해 설명 합니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management)** &gt; **이동식 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="04db9-384">This section describes Removable Drive Group Policy definitions for Microsoft BitLocker Administration and Monitoring at the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04db9-385">정책 이름</span><span class="sxs-lookup"><span data-stu-id="04db9-385">Policy name</span></span></th>
<th align="left"><span data-ttu-id="04db9-386">개요 및 제안 된 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="04db9-386">Overview and suggested Group Policy settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-387">이동식 드라이브에서 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="04db9-387">Control use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-388">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="04db9-388">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="04db9-389">이 정책은 이동식 데이터 드라이브의 BitLocker 사용을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-389">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="04db9-390">사용자가 이동식 데이터 <strong> </strong> 드라이브에서 bitlocker 설치 마법사를 실행할 수 있도록 이동식 데이터 드라이브에 bitlocker 보호 적용 허용을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-390">Click <strong>Allow users to apply BitLocker protection on removable data drives</strong> to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="04db9-391">사용자가 <strong> 이동식 데이터 드라이브에서 bitlocker 드라이브 암호화를 제거 하거나 암호를 해독 하는 </strong> 동안 사용자가 암호화를 일시 중지할 수 있도록 허용을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-391">Click <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> to enable users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="04db9-392">이 정책을 사용 하도록 설정 하 고 <strong> 사용자가 이동식 데이터 드라이브에서 BitLocker 보호를 적용 하도록 허용을 클릭 하면 </strong> , Mbam 클라이언트는 이동식 드라이브에 대 한 복구 정보를 mbam 키 복구 서버에 저장 하 고, 사용자가 암호를 분실 한 경우 드라이브를 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-392">When this policy is enabled, and you click <strong>Allow users to apply BitLocker protection on removable data drives</strong>, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server and allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-393">BitLocker에 의해 보호되지 않는 이동식 드라이브에 대한 쓰기 액세스 거부</span><span class="sxs-lookup"><span data-stu-id="04db9-393">Deny write access to removable drives not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-394">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-394">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-395">이 정책을 사용 하 여 BitLocker 보호 드라이브에 대 한 쓰기 권한만 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-395">Enable this policy to allow only write permission to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="04db9-396">이 정책을 사용 하는 경우 쓰기 권한을 허용 하기 전에 컴퓨터의 모든 이동식 데이터 드라이브에 암호화가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-396">When this policy is enabled, all removable data drives on the computer require encryption before write permission is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-397">이전 버전의 Windows에서 BitLocker로 보호 된 이동식 드라이브에 대 한 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="04db9-397">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-398">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-398">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-399">Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 고정 드라이브를 잠금 해제 하 고 볼 수 있도록 하려면이 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-399">Enable this policy to allow fixed drives with the FAT file system to be unlocked and viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="04db9-400">이 정책이 구성 되어 있지 않으면 Windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템으로 포맷 된 이동식 드라이브를 잠금 해제 하 고 해당 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-400">When this policy is not configured, removable drives that are formatted with the FAT file system can be unlocked on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2, and their content can be viewed.</span></span> <span data-ttu-id="04db9-401">이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-401">These operating systems have read-only permission to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="04db9-402">정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 한 이동식 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-402">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04db9-403">이동식 데이터 드라이브에 대 한 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="04db9-403">Configure use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-404">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-404">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-405">이 정책을 사용 하 여 이동식 데이터 드라이브에서 암호 보호를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-405">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="04db9-406">이 정책이 구성 되어 있지 않은 경우 암호 복잡성 요구 사항이 포함 되지 않고 8 자만 필요로 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-406">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and which require only eight characters.</span></span></p>
<p><span data-ttu-id="04db9-407">보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 대해 암호 요구를 선택 하 고 </strong> , <strong> 암호 복잡도 필요를 클릭 하 </strong> 고, 기본 <strong> 최소 암호 길이를 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-407">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, click <strong>Require password complexity</strong>, and set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04db9-408">BitLocker로 보호 된 이동식 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="04db9-408">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="04db9-409">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="04db9-409">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="04db9-410">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-410">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="04db9-411">구성 되지 않음으로 설정 하는 경우 <strong> </strong> 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-411">When set to <strong>Not Configured</strong>, the data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="04db9-412">MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-412">MBAM operation does not require recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="04db9-413">관련 항목</span><span class="sxs-lookup"><span data-stu-id="04db9-413">Related topics</span></span>


[<span data-ttu-id="04db9-414">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="04db9-414">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="04db9-415">MBAM 2.5 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="04db9-415">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)


## <span data-ttu-id="04db9-416">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="04db9-416">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="04db9-417">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-417">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="04db9-418">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04db9-418">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






