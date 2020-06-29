---
title: MBAM 2.0 그룹 정책 요구 사항 계획
description: MBAM 2.0 그룹 정책 요구 사항 계획
author: dansimp
ms.assetid: f5e19dcb-eb15-4722-bb71-0734b3799eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6092507996fe6f0234178c8b1abae5cea7bf836
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812828"
---
# <span data-ttu-id="5b11b-103">MBAM 2.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="5b11b-103">Planning for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="5b11b-104">MBAM (Microsoft BitLocker 관리 및 모니터링) 클라이언트 컴퓨터를 관리 하려면 조직에서 지원할 BitLocker 프로텍터 유형을 고려해 야 하며, 적용할 해당 그룹 정책 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-104">To manage Microsoft BitLocker Administration and Monitoring (MBAM) client computers, you need to consider the types of BitLocker protectors that you want to support in your organization, and then configure the corresponding Group Policy settings that you want to apply.</span></span> <span data-ttu-id="5b11b-105">이 항목에서는 Microsoft BitLocker 관리 및 모니터링을 사용 하 여 엔터프라이즈의 BitLocker 드라이브 암호화를 관리 하는 데 사용할 수 있는 그룹 정책 설정에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-105">This topic describes the Group Policy settings that are available for use when you are using Microsoft BitLocker Administration and Monitoring to manage BitLocker Drive Encryption in the enterprise.</span></span>

<span data-ttu-id="5b11b-106">MBAM은 운영 체제 드라이브에 대해 TPM (신뢰할 수 있는 플랫폼 모듈), TPM + PIN, TPM + USB 키, TPM + PIN + USB 키, 암호, 숫자 암호, 데이터 복구 에이전트의 BitLocker 보호기 유형을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-106">MBAM supports the following types of BitLocker protectors for operating system drives: Trusted Platform Module (TPM), TPM + PIN, TPM + USB key, and TPM + PIN + USB key, password, numerical password, and Data Recovery Agent.</span></span> <span data-ttu-id="5b11b-107">암호 보호기는 Windows To Go 장치 및 TPM이 없는 Windows 8 장치에만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-107">The password protector is supported only for Windows To Go devices and for Windows 8 devices that do not have a TPM.</span></span> <span data-ttu-id="5b11b-108">MBAM은 운영 체제 볼륨이 MBAM이 설치 되기 전에 암호화 된 경우에만 TPM + USB 키 및 TPM + PIN + USB 키 보호기를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-108">MBAM supports the TPM + USB key and the TPM + PIN + USB key protectors only when the operating system volume is encrypted before MBAM is installed.</span></span>

<span data-ttu-id="5b11b-109">MBAM은 고정 데이터 드라이브에 대 한 다음과 같은 유형의 BitLocker 보호기 인 암호, 자동 잠금 해제, 숫자 암호, 데이터 복구 에이전트를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-109">MBAM supports the following types of BitLocker protectors for fixed data drives: password, auto-unlock, numerical password, and Data Recovery Agent.</span></span>

<span data-ttu-id="5b11b-110">숫자 암호 보호기는 볼륨 암호화의 일부로 자동 적용 되며 구성할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-110">The numeric password protector is applied automatically as part of volume encryption and does not need to be configured.</span></span>

**<span data-ttu-id="5b11b-111">중요</span><span class="sxs-lookup"><span data-stu-id="5b11b-111">Important</span></span>**  
<span data-ttu-id="5b11b-112">기본 Windows BitLocker 드라이브 암호화 GPO (그룹 정책 개체) 설정은 MBAM에서 사용 되지 않으며 사용 하도록 설정 된 경우 충돌 하는 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-112">The default Windows BitLocker drive encryption Group Policy Object (GPO) settings are not used by MBAM and can cause conflicting behavior if they are enabled.</span></span> <span data-ttu-id="5b11b-113">MBAM이 BitLocker를 관리 하도록 설정 하려면 mbam 그룹 정책 템플릿을 설치한 후에만 MBAM 그룹 정책 설정을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-113">To enable MBAM to manage BitLocker, you must define the MBAM Group Policy settings only after installing the MBAM Group Policy template.</span></span>



<span data-ttu-id="5b11b-114">향상 된 시작 Pin에는 대 문자와 소문자, 숫자 등의 문자를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-114">Enhanced startup PINs can contain characters, such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="5b11b-115">BitLocker와 달리 MBAM은 향상 된 Pin에 대 한 기호 및 공백 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-115">Unlike BitLocker, MBAM does not support the use of symbols and spaces for enhanced PINs.</span></span>

<span data-ttu-id="5b11b-116">GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) MDOP 기술을 실행할 수 있는 컴퓨터에 MBAM 그룹 정책 템플릿을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-116">Install the MBAM Group Policy template on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="5b11b-117">Mbam 기능을 사용 하도록 설정 하는 GPO 설정을 편집 하려면 먼저 mbam 그룹 정책 템플릿을 설치 하 고 GPMC 또는 AGPM을 열고 해당 gpo를 편집한 후 다음 GPO 노드로 이동 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker 관리).**</span><span class="sxs-lookup"><span data-stu-id="5b11b-117">To edit the GPO settings that enable MBAM functionality, you must first install the MBAM Group Policy template, open the GPMC or AGPM to edit the applicable GPO, and then navigate to the following GPO node: **Computer Configuration**\\**Policies**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management).**</span></span>

<span data-ttu-id="5b11b-118">MDOP (BitLocker 관리) GPO 노드에는 4 개의 글로벌 정책 설정과 클라이언트 관리, 고정 드라이브, 운영 체제 드라이브, 이동식 드라이브의 네 가지 하위 GPO 설정 노드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-118">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO settings nodes: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="5b11b-119">다음 섹션에서는 MBAM GPO 정책 설정 요구 사항에 대 한 계획을 수립할 수 있도록 정책 정의 및 제안 된 정책 설정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-119">The following sections provide policy definitions and suggested policy settings to assist you in planning for MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="5b11b-120">참고</span><span class="sxs-lookup"><span data-stu-id="5b11b-120">Note</span></span>**  
<span data-ttu-id="5b11b-121">MBAM이 BitLocker 암호화를 관리 하도록 설정 하는 데 권장 되는 최소 GPO 설정을 구성 하는 방법에 대 한 자세한 내용은 [mbam 2.0 GPO 설정을 편집 하는 방법을](how-to-edit-mbam-20-gpo-settings-mbam-2.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b11b-121">For more information about configuring the minimum, recommended GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 2.0 GPO Settings](how-to-edit-mbam-20-gpo-settings-mbam-2.md).</span></span>



## <span data-ttu-id="5b11b-122">전역 정책 정의</span><span class="sxs-lookup"><span data-stu-id="5b11b-122">Global Policy Definitions</span></span>


<span data-ttu-id="5b11b-123">이 섹션에서는 다음과 같은 GPO 노드에서 볼 수 있는 mbam 글로벌 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker 관리)**.</span><span class="sxs-lookup"><span data-stu-id="5b11b-123">This section describes MBAM Global policy definitions found at the following GPO node: **Computer Configuration**\\**Policies**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b11b-124">정책 이름</span><span class="sxs-lookup"><span data-stu-id="5b11b-124">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="5b11b-125">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-125">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-126">드라이브 암호화 방법 및 암호화 수준 선택</span><span class="sxs-lookup"><span data-stu-id="5b11b-126">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-127">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-128">특정 암호화 방법 및 암호화 강도를 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-128">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="5b11b-129">이 정책이 구성 되어 있지 않으면, BitLocker는 AES 128 비트의 기본 암호화 방법으로 디퓨저 또는 설정 스크립트에 의해 지정 된 암호화 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-129">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-130">다시 시작할 때 메모리 덮어쓰기 방지</span><span class="sxs-lookup"><span data-stu-id="5b11b-130">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-131">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-132">다시 시작 시 메모리의 BitLocker 비밀을 덮어쓰지 않고 다시 시작 성능을 향상 시키려면이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-132">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="5b11b-133">이 정책이 구성 되어 있지 않으면 컴퓨터가 다시 시작 될 때 BitLocker 비밀이 메모리에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-133">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-134">스마트 카드 인증서 용도 규칙 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="5b11b-134">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-135">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-136">스마트 카드 인증서 기반 BitLocker 보호를 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-136">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="5b11b-137">이 정책이 구성 되지 않은 경우에는 기본 개체 식별자 1.3.6.1.4.1.311.67.1.1를 사용 하 여 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-137">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-138">조직의 고유 식별자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-138">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-139">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-139">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-140">인증서 기반 데이터 복구 에이전트 또는 BitLocker To Go 읽기 프로그램을 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-140">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="5b11b-141">이 정책이 구성 되어 있지 않으면 <strong> 식별 </strong> 필드가 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-141">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="5b11b-142">회사에서 더 높은 수준의 보안을 요구 하는 경우 id 필드를 구성 하 여 <strong> </strong> 모든 USB 장치에이 필드 집합을 포함 하 고이 그룹 정책 설정에 맞출지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-142">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5b11b-143">클라이언트 관리 정책 정의</span><span class="sxs-lookup"><span data-stu-id="5b11b-143">Client Management Policy Definitions</span></span>


<span data-ttu-id="5b11b-144">이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 클라이언트 관리 정책 정의 ( **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)** \\ **클라이언트 관리**)에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-144">This section describes Client Management policy definitions for Microsoft BitLocker Administration and Monitoring found at the following GPO node: **Computer Configuration**\\**Policies**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**\\**Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b11b-145">정책 이름</span><span class="sxs-lookup"><span data-stu-id="5b11b-145">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="5b11b-146">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-146">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-147">MBAM 서비스 구성</span><span class="sxs-lookup"><span data-stu-id="5b11b-147">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-148">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="5b11b-148">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="5b11b-149">MBAM 복구 및 하드웨어 서비스 끝점 </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-149">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="5b11b-150">이 설정을 사용 하 여 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-150">Use this setting to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="5b11b-151">다음 예제와 유사한 끝점 위치를 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스를/MBAMRecoveryAndHardwareService/CoreService.svc에 연결 &gt; </em><strong> </strong> 하는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-151">Enter an endpoint location that is similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="5b11b-152">저장할 BitLocker 복구 정보를 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-152">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="5b11b-153">이 정책 설정을 통해 BitLocker 복구 정보를 백업 하도록 키 복구 서비스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-153">This policy setting lets you configure the key recovery service to back up BitLocker recovery information.</span></span> <span data-ttu-id="5b11b-154">또한 준수 및 감사 보고서를 수집 하는 상태 보고 서비스도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-154">It also lets you configure status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="5b11b-155">이 정책은 키 정보가 부족 하 여 데이터 손실을 방지 하기 위해 BitLocker에서 암호화 한 데이터를 복구 하는 관리 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-155">The policy provides an administrative method of recovering data encrypted by BitLocker to prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="5b11b-156">상태 보고서 및 키 복구 작업이 구성 된 보고서 서버 위치에 자동으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-156">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="5b11b-157">이 정책 설정을 구성 하지 않거나 사용 하지 않도록 설정 하면 키 복구 정보가 저장 되지 않으며 상태 보고서 및 키 복구 작업이 서버에 보고 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-157">If you do not configure or if you disable this policy setting, the Key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="5b11b-158">이 설정이 <strong> 복구 암호 및 키 패키지로 설정 되어 있으면 </strong> 복구 암호와 키 패키지가 자동으로 구성 된 키 복구 서버 위치에 백업 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-158">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="5b11b-159">클라이언트 검사 상태 빈도를 분 단위로 입력 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-159">Enter client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="5b11b-160">이 정책 설정은 클라이언트가 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하는 빈도를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-160">This policy setting manages how frequently the client checks the BitLocker protection policies and status on the client computer.</span></span> <span data-ttu-id="5b11b-161">또한이 정책은 클라이언트 준수 상태가 서버에 저장 되는 빈도를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-161">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="5b11b-162">클라이언트는 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하 고 구성 된 빈도로 클라이언트 복구 키를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-162">The client checks the BitLocker protection policies and status on the client computer and also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="5b11b-163">회사에서 설정한 요구 사항에 따라 컴퓨터의 준수 상태를 확인 하는 빈도 및 클라이언트 복구 키를 백업 하는 빈도를 기준으로이 빈도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-163">Set this frequency based on the requirement set by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="5b11b-164">MBAM 상태 보고 서비스 끝점 </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-164">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="5b11b-165">이 설정을 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-165">You must configure this setting to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="5b11b-166">다음 예제와 유사한 끝점 위치를 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스를/MBAMComplianceStatusService/StatusReportingService.svc에 연결 &gt; </em><strong> </strong> 하는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-166">Enter an endpoint location that is similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-167">사용자 예외 정책 구성</span><span class="sxs-lookup"><span data-stu-id="5b11b-167">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-168">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-168">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-169">이 정책 설정을 통해 사용자에 게 BitLocker 암호화 예외를 요청 하도록 지시할 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-169">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="5b11b-170">이 정책 설정을 사용 하 고 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 제공 하면 사용자에 게 BitLocker 보호에서 예외를 적용 하는 방법에 대 한 지침을 제공 하는 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-170">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog that gives them instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="5b11b-171">사용자의 BitLocker 암호화 예외를 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)"> 사용자 Bitlocker 암호화 예외를 관리 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="5b11b-171">For more information about enabling BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="5b11b-172">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 예외 요청 지침이 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-172">If you either disable or do not configure this policy setting, the exemption request instructions will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="5b11b-173">참고</span><span class="sxs-lookup"><span data-stu-id="5b11b-173">Note</span></span></strong><br/><p><span data-ttu-id="5b11b-174">사용자 예외는 컴퓨터당만 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-174">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="5b11b-175">여러 사용자가 같은 컴퓨터에 로그온 하 고 한 사용자가 제외 되지 않은 경우 컴퓨터는 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-175">If multiple users log on to the same computer and any one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-176">사용자 환경 개선 프로그램 구성</span><span class="sxs-lookup"><span data-stu-id="5b11b-176">Configure customer experience improvement program</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-177">이 정책 설정을 사용 하면 사용자 환경 개선 프로그램에 MBAM이 참여할 수 있는 기간을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-177">This policy setting lets you configure how MBAM users can join the Customer Experience Improvement Program.</span></span> <span data-ttu-id="5b11b-178">이 프로그램은 컴퓨터 하드웨어와 사용자가 작업을 중단 하지 않고 MBAM을 사용 하는 방법에 대 한 정보를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-178">This program collects information about computer hardware and how users use MBAM without interrupting their work.</span></span> <span data-ttu-id="5b11b-179">이 정보는 Microsoft가 향상 시킬 MBAM 기능을 식별 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-179">The information helps Microsoft to identify which MBAM features to improve.</span></span> <span data-ttu-id="5b11b-180">Microsoft는이 정보를 사용 하 여 MBAM 사용자를 식별 하거나 연락 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-180">Microsoft will not use this information to identify or contact MBAM users.</span></span></p>
<p><span data-ttu-id="5b11b-181">이 정책 설정을 사용 하도록 설정 하면 사용자가 고객 환경 개선 프로그램에 참가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-181">If you enable this policy setting, users will be able to join the Customer Experience Improvement Program.</span></span></p>
<p><span data-ttu-id="5b11b-182">이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자가 고객 환경 개선 프로그램에 참여할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-182">If you disable this policy setting, users will not be able to join the Customer Experience Improvement Program.</span></span></p>
<p><span data-ttu-id="5b11b-183">이 정책 설정을 구성 하지 않으면 사용자 환경 개선 프로그램에 참가할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-183">If you do not configure this policy setting, users will have the option to join the Customer Experience Improvement Program.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5b11b-184">고정 드라이브 정책 정의</span><span class="sxs-lookup"><span data-stu-id="5b11b-184">Fixed Drive Policy Definitions</span></span>


<span data-ttu-id="5b11b-185">이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 고정 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 서식 파일** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)** \\ **고정 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="5b11b-185">This section describes Fixed Drive policy definitions for Microsoft BitLocker Administration and Monitoring found at the following GPO node: **Computer Configuration**\\**Policies**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**\\**Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b11b-186">정책 이름</span><span class="sxs-lookup"><span data-stu-id="5b11b-186">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="5b11b-187">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-187">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-188">고정 데이터 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-188">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-189">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="5b11b-189">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="5b11b-190">이 정책 설정을 통해 고정 드라이브를 암호화 해야 하는지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-190">This policy setting let you manage whether fixed drives must be encrypted.</span></span></p>
<p><span data-ttu-id="5b11b-191">운영 체제 볼륨을 암호화 해야 하는 경우에는 <strong> 고정 데이터 드라이브 자동 잠금 해제 옵션을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-191">If the operating system volume is required to be encrypted, select the <strong>Enable auto-unlock fixed data drive</strong> option.</span></span></p>
<p><span data-ttu-id="5b11b-192">이 정책을 사용 하는 경우 <strong> </strong> 고정 데이터 드라이브에 대 한 자동 잠금 해제를 허용 하거나 요구 하지 않는 한 고정 데이터 드라이브에 대 한 암호 사용 구성 정책을 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-192">When enabling this policy, you must not disable the <strong>Configure use of password for fixed data drives</strong> policy unless the use of Auto-Unlock for fixed data drives is allowed or required.</span></span></p>
<p><span data-ttu-id="5b11b-193">고정 데이터 드라이브에 대 한 자동 잠금 해제를 사용 해야 하는 경우 운영 체제 볼륨을 암호화 하도록 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-193">If you require the use of Auto-Unlock for fixed data drives, you must configure operating system volumes to be encrypted.</span></span></p>
<p><span data-ttu-id="5b11b-194">이 정책 설정을 사용 하면 사용자가 모든 고정 드라이브를 BitLocker 보호에 포함 해야 하며, 드라이브가 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-194">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, and the drives will be encrypted.</span></span></p>
<p><span data-ttu-id="5b11b-195">이 정책 설정을 구성 하지 않으면 사용자가 BitLocker 보호에 고정 드라이브를 추가할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-195">If you do not configure this policy setting, users are not required to put fixed drives under BitLocker protection.</span></span> <span data-ttu-id="5b11b-196">고정 데이터 드라이브가 암호화 된 후이 정책을 적용 하면 MBAM 에이전트는 암호화 된 고정 드라이브의 암호를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-196">If you apply this policy after fixed data drives are encrypted, the MBAM agent decrypts the encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="5b11b-197">이 정책 설정을 사용 하지 않으면 사용자가 고정 된 데이터 드라이브를 BitLocker 보호에 저장할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-197">If you disable this policy setting, users will not be able to put their fixed data drives under BitLocker protection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-198">BitLocker에 의해 보호되지 않는 고정 드라이브에 대한 쓰기 액세스 거부</span><span class="sxs-lookup"><span data-stu-id="5b11b-198">Deny write access to fixed drives not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-199">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-199">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-200">이 정책 설정은 컴퓨터에서 고정 드라이브를 쓰기 가능 하 게 하기 위해 BitLocker 보호가 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-200">This policy setting determines whether BitLocker protection is required for fixed drives to be writable on a computer.</span></span> <span data-ttu-id="5b11b-201">이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-201">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="5b11b-202">정책이 구성 되어 있지 않으면 컴퓨터의 모든 고정 데이터 드라이브가 읽기 및 쓰기 액세스 권한으로 탑재 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-202">When the policy is not configured, all fixed data drives on the computer are mounted with read and write access.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-203">이전 버전의 Windows에서 BitLocker로 보호 되는 고정 드라이브에 대 한 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="5b11b-203">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-204">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-204">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-205">Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 고정 드라이브를 잠금 해제 하 고 볼 수 있도록 하려면이 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-205">Enable this policy to let fixed drives with the FAT file system be unlocked and viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="5b11b-206">정책을 사용 하거나 구성 하지 않으면 FAT 파일 시스템으로 포맷 한 고정 드라이브는 잠금을 해제할 수 있으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-206">When the policy is enabled or not configured, fixed drives formatted with the FAT file system can be unlocked and their content can be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span> <span data-ttu-id="5b11b-207">이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-207">These operating systems have read-only access to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="5b11b-208">정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 된 고정 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-208">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-209">고정 드라이브의 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="5b11b-209">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-210">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-210">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-211">이 정책을 사용 하 여 BitLocker로 보호 된 고정 데이터 드라이브의 잠금을 해제 하는 데 암호가 필요한 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-211">Use this policy to specify whether a password is required to unlock BitLocker-protected fixed data drives.</span></span></p>
<p><span data-ttu-id="5b11b-212">이 정책 설정을 사용 하면 사용자가 정의한 요구 사항에 맞는 암호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-212">If you enable this policy setting, users can configure a password that meets the requirements you define.</span></span> <span data-ttu-id="5b11b-213">BitLocker는 사용자가 드라이브에서 사용할 수 있는 모든 보호기를 사용 하 여 드라이브 잠금을 해제할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-213">BitLocker will allow users to unlock a drive with any of the protectors that are available on the drive.</span></span></p>
<p><span data-ttu-id="5b11b-214">이러한 설정은 볼륨을 잠금 해제 하는 경우를 제외 하 고는 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-214">These settings are enforced when turning on BitLocker, not when unlocking a volume.</span></span></p>
<p><span data-ttu-id="5b11b-215">이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-215">If you disable this policy setting, users are not allowed to use a password.</span></span></p>
<p><span data-ttu-id="5b11b-216">정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-216">When the policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and which require only eight characters.</span></span></p>
<p><span data-ttu-id="5b11b-217">보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 고정 데이터 드라이브에 대해 암호 필요를 선택 하 고 </strong> , <strong> 암호 복잡도 필요를 선택 하 </strong> 고, 원하는 <strong> 최소 암호 길이를 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-217">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p>
<p><span data-ttu-id="5b11b-218">이 정책 설정을 사용 하지 않도록 설정 하는 경우 사용자는 암호를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-218">If you disable this policy setting, users are not allowed to use a password.</span></span></p>
<p><span data-ttu-id="5b11b-219">이 정책 설정을 구성 하지 않으면 암호가 복잡 한 요구 사항과 8 자만 포함 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-219">If you do not configure this policy setting, passwords will be supported with the default settings, which do not include password complexity requirements and which require only eight characters.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-220">BitLocker로 보호 되는 고정 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="5b11b-220">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-221">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-221">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-222">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-222">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="5b11b-223">정책이 구성 되어 있지 않으면 BitLocker 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-223">When the policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="5b11b-224">MBAM에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-224">MBAM does not require recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5b11b-225">운영 체제 드라이브 정책 정의</span><span class="sxs-lookup"><span data-stu-id="5b11b-225">Operating System Drive Policy Definitions</span></span>


<span data-ttu-id="5b11b-226">이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 운영 체제 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)** \\ **운영 체제 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="5b11b-226">This section describes Operating System Drive policy definitions for Microsoft BitLocker Administration and Monitoring found at the following GPO node: **Computer Configuration**\\**Policies**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**\\**Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b11b-227">정책 이름</span><span class="sxs-lookup"><span data-stu-id="5b11b-227">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="5b11b-228">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-228">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-229">운영 체제 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-229">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-230">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="5b11b-230">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="5b11b-231">이 정책 설정을 통해 운영 체제 드라이브를 암호화 해야 하는지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-231">This policy setting lets you manage whether the operating system drive must be encrypted.</span></span></p>
<p><span data-ttu-id="5b11b-232">보안을 강화 하려면 <strong> </strong> TPM + PIN 보호기를 사용 하는 경우 시스템/전원 관리/절전 모드 설정에서 다음 정책 설정을 사용 하지 않도록 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-232">For higher security, consider disabling the following policy settings in <strong>System/Power Management/Sleep Settings</strong> when you enable them with TPM + PIN protector:</span></span></p>
<ul>
<li><p><span data-ttu-id="5b11b-233">절전 모드에서 대기 상태 (S1-S3) 허용 (전원 사용)</span><span class="sxs-lookup"><span data-stu-id="5b11b-233">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="5b11b-234">절전 모드 시 대기 상태 (S1-S3) 허용 (배터리 사용)</span><span class="sxs-lookup"><span data-stu-id="5b11b-234">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul>
<p><span data-ttu-id="5b11b-235">Microsoft Windows 8 이상을 실행 중이 고 TPM이 없는 컴퓨터에서 BitLocker를 사용 하려는 경우 <strong> 호환 되는 tpm이 없는 bitlocker 허용 확인란을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-235">If you are running Microsoft Windows 8 or later, and you want to use BitLocker on a computer without a TPM, select the <strong>Allow BitLocker without a compatible TPM</strong> check box.</span></span> <span data-ttu-id="5b11b-236">이 모드에서는 시작 하는 데 암호가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-236">In this mode, a password is required for startup.</span></span> <span data-ttu-id="5b11b-237">암호를 잊어버린 경우 BitLocker 복구 옵션 중 하나를 사용 하 여 드라이브에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-237">If you forget the password, you have to use one of the BitLocker recovery options to access the drive.</span></span></p>
<p><span data-ttu-id="5b11b-238">호환 되는 TPM이 있는 컴퓨터에서는 시작 시 암호화 된 데이터에 대 한 추가 보호를 제공 하기 위해 두 가지 유형의 인증 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-238">On a computer with a compatible TPM, two types of authentication methods can be used at startup to provide added protection for encrypted data.</span></span> <span data-ttu-id="5b11b-239">컴퓨터가 시작 되 면 인증에 TPM만 사용 하거나 PIN (개인 식별 번호)을 입력 해야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-239">When the computer starts, it can use only the TPM for authentication, or it can also require the entry of a personal identification number (PIN).</span></span></p>
<p><span data-ttu-id="5b11b-240">이 정책 설정을 사용 하면 사용자가 BitLocker protection에서 운영 체제 드라이브를 설치 하 고 드라이브가 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-240">If you enable this policy setting, users have to put the operating system drive under BitLocker protection, and the drive will be encrypted.</span></span></p>
<p><span data-ttu-id="5b11b-241">이 정책을 사용 하지 않도록 설정 하는 경우, 사용자는 운영 체제 드라이브를 BitLocker 보호 하에 둘 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-241">If you disable this policy, users will not be able to put the operating system drive under BitLocker protection.</span></span> <span data-ttu-id="5b11b-242">운영 체제 드라이브가 암호화 된 후이 정책을 적용 하면 드라이브의 암호가 해독 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-242">If you apply this policy after the operating system drive is encrypted, the drive will be decrypted.</span></span></p>
<p><span data-ttu-id="5b11b-243">이 정책을 구성 하지 않으면, 운영 체제 드라이브를 BitLocker 보호 아래에 배치할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-243">If you do not configure this policy, the operating system drive is not required to be placed under BitLocker protection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-244">TPM 플랫폼 유효성 검사 프로필 구성</span><span class="sxs-lookup"><span data-stu-id="5b11b-244">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-245">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-245">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-246">이 정책 설정을 통해 컴퓨터의 TPM 보안 하드웨어가 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-246">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="5b11b-247">컴퓨터에 호환 되는 TPM이 없거나 BitLocker가 이미 TPM 보호를 사용 하도록 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-247">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker has already been turned on with TPM protection.</span></span></p>
<p><span data-ttu-id="5b11b-248">이 정책 설정이 구성 되어 있지 않으면 TPM은 기본 플랫폼 유효성 검사 프로필 또는 설정 스크립트에 지정 된 플랫폼 유효성 검사 프로필을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-248">When this policy setting is not configured, the TPM uses the default platform validation profile or the platform validation profile that is specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-249">BitLocker로 보호 되는 운영 체제 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="5b11b-249">Choose how BitLocker-protected operating system drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-250">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-250">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-251">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-251">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="5b11b-252">이 정책이 구성 되어 있지 않으면 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-252">When this policy is not configured, the data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="5b11b-253">MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-253">MBAM operation does not require recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5b11b-254">이동식 드라이브 정책 정의</span><span class="sxs-lookup"><span data-stu-id="5b11b-254">Removable Drive Policy Definitions</span></span>


<span data-ttu-id="5b11b-255">이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 Microsoft BitLocker 관리 및 모니터링에 대 한 이동식 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **정책** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)**  \\  **이동식 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="5b11b-255">This section describes Removable Drive Policy definitions for Microsoft BitLocker Administration and Monitoring found at the following GPO node: **Computer Configuration**\\**Policies**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b11b-256">정책 이름</span><span class="sxs-lookup"><span data-stu-id="5b11b-256">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="5b11b-257">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="5b11b-257">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-258">이동식 드라이브에서 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="5b11b-258">Control use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-259">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="5b11b-259">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="5b11b-260">이 정책은 이동식 데이터 드라이브의 BitLocker 사용을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-260">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="5b11b-261">사용자가 이동식 데이터 드라이브에서 bitlocker <strong> 보호 기능을 적용할 수 있도록 허용 옵션을 사용 하도록 설정 </strong> 하 여 사용자가 이동식 데이터 드라이브에서 bitlocker 설치 마법사를 실행할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-261">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="5b11b-262">사용자가 <strong> 드라이브에서 bitlocker 드라이브 암호화를 제거 하거나 암호를 해독 하도록 허용 옵션을 사용 하도록 설정 하 여 </strong> 유지 관리 작업을 수행 하는 동안 암호화를 일시 중단 하거나, 암호를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-262">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="5b11b-263">이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 BitLocker 보호 적용 허용 옵션을 </strong> 선택 하면 Mbam 클라이언트는 이동식 드라이브에 대 한 복구 정보를 mbam 키 복구 서버에 저장 하 고 사용자가 암호를 잃어버린 경우 드라이브를 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-263">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server and allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-264">BitLocker에 의해 보호되지 않는 이동식 드라이브에 대한 쓰기 액세스 거부</span><span class="sxs-lookup"><span data-stu-id="5b11b-264">Deny write access to removable drives not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-265">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-265">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-266">이 정책을 사용 하 여 BitLocker 보호 드라이브에 대 한 쓰기 권한만 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-266">Enable this policy to allow only write access to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="5b11b-267">이 정책을 사용 하는 경우 쓰기 액세스를 허용 하기 전에 컴퓨터의 모든 이동식 데이터 드라이브에 암호화가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-267">When this policy is enabled, all removable data drives on the computer require encryption before write access is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-268">이전 버전의 Windows에서 BitLocker로 보호 된 이동식 드라이브에 대 한 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="5b11b-268">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-269">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-269">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-270">Windows Server 2008, Windows Vista, windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템을 사용 하는 고정 드라이브를 잠금 해제 하 고 볼 수 있도록 하려면이 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-270">Enable this policy to allow fixed drives with the FAT file system to be unlocked and viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="5b11b-271">이 정책이 구성 되어 있지 않은 경우, windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT 파일 시스템으로 포맷 된 이동식 데이터 드라이브의 잠금을 해제 하 고 해당 콘텐츠를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-271">When this policy is not configured, removable data drives formatted with the FAT file system can be unlocked on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2, and their content can be viewed.</span></span> <span data-ttu-id="5b11b-272">이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-272">These operating systems have read-only access to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="5b11b-273">정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 한 이동식 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-273">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b11b-274">이동식 데이터 드라이브에 대 한 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="5b11b-274">Configure use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-275">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-275">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-276">이 정책을 사용 하 여 이동식 데이터 드라이브에서 암호 보호를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-276">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="5b11b-277">이 정책이 구성 되어 있지 않은 경우 암호 복잡성 요구 사항이 포함 되지 않고 8 자만 필요로 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-277">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and which require only eight characters.</span></span></p>
<p><span data-ttu-id="5b11b-278">보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 대 한 암호 필요 </strong> 를 선택 하 고, <strong> 암호 복잡도 필요 </strong> , 기본 <strong> 최소 암호 길이를 설정 해야 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-278">For increased security, you may enable this policy and check <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b11b-279">BitLocker로 보호 된 이동식 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="5b11b-279">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b11b-280">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="5b11b-280">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="5b11b-281">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-281">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="5b11b-282">구성 되지 않음으로 설정 하는 경우 <strong> </strong> 데이터 복구 에이전트는 허용 되 고 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-282">When set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="5b11b-283">MBAM 작업에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b11b-283">MBAM operation does not require recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5b11b-284">관련 항목</span><span class="sxs-lookup"><span data-stu-id="5b11b-284">Related topics</span></span>


[<span data-ttu-id="5b11b-285">MBAM 2.0 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="5b11b-285">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)









