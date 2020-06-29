---
title: MBAM 1.0 그룹 정책 요구 사항 계획
description: MBAM 1.0 그룹 정책 요구 사항 계획
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812436"
---
# <span data-ttu-id="92dda-103">MBAM 1.0 그룹 정책 요구 사항 계획</span><span class="sxs-lookup"><span data-stu-id="92dda-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="92dda-104">Microsoft BitLocker 관리 및 모니터링 (MBAM) 클라이언트 관리에서 사용자 지정 그룹 정책 설정을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="92dda-105">이 항목에서는 MBAM을 사용 하 여 엔터프라이즈의 BitLocker 드라이브 암호화를 관리 하는 경우 GPO (그룹 정책 개체)에 사용할 수 있는 정책 옵션에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="92dda-106">중요</span><span class="sxs-lookup"><span data-stu-id="92dda-106">Important</span></span>**  
<span data-ttu-id="92dda-107">MBAM은 Windows BitLocker 드라이브 암호화에 대 한 기본 GPO 설정을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="92dda-108">기본 설정을 사용 하도록 설정 하면 충돌 하는 동작이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="92dda-109">MBAM이 BitLocker를 관리 하도록 설정 하려면 MBAM 그룹 정책 템플릿을 설치한 후 GPO 정책 설정을 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="92dda-110">MBAM 그룹 정책 템플릿을 설치한 후에는 MBAM에서 엔터프라이즈 BitLocker 암호화를 관리 하는 데 사용 가능한 사용자 지정 MBAM GPO 정책 설정을 보고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="92dda-111">MBAM 그룹 정책 템플릿은 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) MDOP 기술을 실행할 수 있는 컴퓨터에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="92dda-112">다음으로 해당 GPO를 편집 하려면 GPMC 또는 AGPM을 열고 다음 GPO 노드로 이동 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP (BitLocker 관리)**.</span><span class="sxs-lookup"><span data-stu-id="92dda-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="92dda-113">MDOP (BitLocker Management) GPO 노드에는 각각 4 개의 전역 정책 설정과 네 개의 자식 GPO 설정 노드가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="92dda-114">4 개의 GPO 전역 정책 설정은 클라이언트 관리, 고정 드라이브, 운영 체제 드라이브 및 이동식 드라이브입니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="92dda-115">다음 섹션에서는 MBAM GPO 정책 설정 요구 사항을 계획 하는 데 도움이 되는 정책 정의 및 제안 된 정책 설정을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="92dda-116">참고</span><span class="sxs-lookup"><span data-stu-id="92dda-116">Note</span></span>**  
<span data-ttu-id="92dda-117">MBAM이 BitLocker 암호화를 관리 하도록 허용 하도록 최소 추천 GPO 설정을 구성 하는 방법에 대 한 자세한 내용은 [mbam 1.0 GPO 설정을 편집 하는 방법을](how-to-edit-mbam-10-gpo-settings.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="92dda-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="92dda-118">전역 정책 정의</span><span class="sxs-lookup"><span data-stu-id="92dda-118">Global policy definitions</span></span>


<span data-ttu-id="92dda-119">이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 mbam 전역 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)**.</span><span class="sxs-lookup"><span data-stu-id="92dda-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92dda-120">정책 이름</span><span class="sxs-lookup"><span data-stu-id="92dda-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="92dda-121">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-122">드라이브 암호화 방법 및 암호화 수준 선택</span><span class="sxs-lookup"><span data-stu-id="92dda-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-123">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-124">특정 암호화 방법 및 암호화 강도를 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="92dda-125">이 정책이 구성 되어 있지 않으면, BitLocker는 AES 128 비트의 기본 암호화 방법으로 디퓨저 또는 설정 스크립트에 의해 지정 된 암호화 방법을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-126">다시 시작할 때 메모리 덮어쓰기 방지</span><span class="sxs-lookup"><span data-stu-id="92dda-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-127">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-128">다시 시작 시 메모리의 BitLocker 비밀을 덮어쓰지 않고 다시 시작 성능을 향상 시키려면이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="92dda-129">이 정책이 구성 되어 있지 않으면 컴퓨터가 다시 시작 될 때 BitLocker 비밀이 메모리에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-130">스마트 카드 인증서 용도 규칙 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="92dda-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-131">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-132">스마트 카드 인증서 기반 BitLocker 보호를 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="92dda-133">이 정책이 구성 되지 않은 경우에는 기본 개체 식별자 1.3.6.1.4.1.311.67.1.1를 사용 하 여 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-134">조직의 고유 식별자를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-135">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-136">인증서 기반 데이터 복구 에이전트 또는 BitLocker To Go 읽기 프로그램을 사용 하도록이 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="92dda-137">이 정책이 구성 되어 있지 않으면 <strong> 식별 </strong> 필드가 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="92dda-138">회사에서 더 높은 수준의 보안을 요구 하는 경우 id 필드를 구성 하 여 <strong> </strong> 모든 USB 장치에이 필드 집합을 포함 하 고이 그룹 정책 설정에 맞출지 여부를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="92dda-139">클라이언트 관리 정책 정의</span><span class="sxs-lookup"><span data-stu-id="92dda-139">Client Management policy definitions</span></span>


<span data-ttu-id="92dda-140">이 섹션에서는 다음 GPO 노드에서 볼 수 있는 mbam 클라이언트 관리 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mblaam (BitLocker Management)**  \\  **클라이언트 관리**</span><span class="sxs-lookup"><span data-stu-id="92dda-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92dda-141">정책 이름</span><span class="sxs-lookup"><span data-stu-id="92dda-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="92dda-142">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-143">MBAM 서비스 구성</span><span class="sxs-lookup"><span data-stu-id="92dda-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-144">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="92dda-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="92dda-145">MBAM 복구 및 하드웨어 서비스 끝점 </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="92dda-146">이는 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 구성 해야 하는 첫 번째 정책 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="92dda-147">이 설정에 대 한 끝점 위치를 다음 예제와 같이 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가/MBAMRecoveryAndHardwareService/CoreService.svc에 바인딩된 포트입니다 &gt; </em><strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="92dda-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="92dda-148">저장할 BitLocker 복구 정보를 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="92dda-149">이 정책 설정을 통해 BitLocker 복구 정보를 백업 하도록 키 복구 서비스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="92dda-150">또한 준수 및 감사 보고서를 수집 하는 상태 보고 서비스도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="92dda-151">이 정책은 키 정보가 부족 하 여 데이터 손실을 방지 하기 위해 BitLocker에서 암호화 한 데이터를 복구 하는 관리 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="92dda-152">상태 보고서 및 키 복구 작업이 구성 된 보고서 서버 위치에 자동으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="92dda-153">이 정책 설정을 구성 하지 않거나 사용 하지 않도록 설정 하면 키 복구 정보가 저장 되지 않으며 상태 보고서 및 키 복구 작업이 서버에 보고 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="92dda-154">이 설정이 <strong> 복구 암호 및 키 패키지로 설정 되어 있으면 </strong> 복구 암호와 키 패키지가 자동으로 구성 된 키 복구 서버 위치에 백업 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="92dda-155">클라이언트 검사 상태 빈도 (분)를 입력 합니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="92dda-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="92dda-156">이 정책 설정은 클라이언트가 BitLocker 보호 정책 및 클라이언트 컴퓨터의 상태를 확인 하는 빈도를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="92dda-157">또한이 정책은 클라이언트 준수 상태가 서버에 저장 되는 빈도를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="92dda-158">클라이언트는 클라이언트 컴퓨터의 BitLocker 보호 정책 및 상태를 확인 하 고 구성 된 주파수에서 클라이언트 복구 키를 백업 하기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="92dda-159">컴퓨터의 준수 상태를 확인 하는 빈도 및 클라이언트 복구 키를 백업 하는 빈도에 따라 회사에서 설정한 요구 사항을 기반으로이 빈도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="92dda-160">MBAM 상태 보고 서비스 끝점 </strong> 입니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="92dda-161">이는 MBAM 클라이언트 BitLocker 암호화 관리를 사용 하도록 구성 해야 하는 두 번째 정책 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="92dda-162">이 설정에 대해 다음 예제를 사용 하 여 끝점 위치를 입력 합니다. <strong> http:// </strong><em> &lt; mbam 관리 및 모니터링 서버 이름 &gt; </em><strong> : </strong><em> &lt; 웹 서비스가 &gt; /MBAMComplianceStatusService/StatusReportingService.에 바인딩된 포트 </em><strong></span><span class="sxs-lookup"><span data-stu-id="92dda-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="92dda-163">svc </strong> .</span><span class="sxs-lookup"><span data-stu-id="92dda-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-164">하드웨어 호환성 검사 허용</span><span class="sxs-lookup"><span data-stu-id="92dda-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-165">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="92dda-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="92dda-166">이 정책 설정을 사용 하면 MBAM 클라이언트 컴퓨터의 드라이브에서 BitLocker 보호 기능을 사용 하도록 설정 하기 전에 하드웨어 호환성 확인을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="92dda-167">엔터프라이즈에 TPM (신뢰할 수 있는 플랫폼 모듈)을 지원 하지 않는 이전 컴퓨터 하드웨어 또는 컴퓨터가 있는 경우이 정책 옵션을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="92dda-168">이러한 조건 중 하나라도 참이 면 하드웨어 호환성 확인을 사용 하 여 MBAM이 BitLocker를 지 원하는 컴퓨터 모델에만 적용 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="92dda-169">조직의 모든 컴퓨터에서 BitLocker를 지 원하는 경우 하드웨어 호환성을 배포할 필요가 없으며이 정책을 <strong> 구성 되지 않도록 설정할 수 있습니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="92dda-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="92dda-170">이 정책 설정을 사용 하면 컴퓨터 드라이브에서 BitLocker 보호 기능을 사용 하도록 설정 하기 전에 하드웨어 호환성 목록에 대해 모든 24 시간에 대 한 작업의 모델이 확인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92dda-171">참고</span><span class="sxs-lookup"><span data-stu-id="92dda-171">Note</span></span></strong><br/><p><span data-ttu-id="92dda-172">이 정책 설정을 사용 하기 전에 <strong> </strong> <strong> mbam 서비스 구성 옵션에서 mbam 복구 및 하드웨어 서비스 끝점 설정을 구성 했는지 확인 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="92dda-173">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 하드웨어 호환성 목록에 대해 컴퓨터 모델의 유효성을 검사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-174">사용자 예외 정책 구성</span><span class="sxs-lookup"><span data-stu-id="92dda-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-175">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-176">이 정책 설정을 통해 사용자에 게 BitLocker 암호화 예외를 요청 하도록 지시할 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="92dda-177">이 정책 설정을 사용 하 고 웹 사이트 주소, 전자 메일 주소 또는 전화 번호를 제공 하는 경우, 사용자에 게 BitLocker 보호에서 예외를 적용 하는 방법에 대 한 지침이 포함 된 대화 상자가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="92dda-178">사용자에 대 한 BitLocker 암호화 예외를 사용 하는 방법에 대 한 자세한 내용은 <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> 사용자 Bitlocker 암호화 예외를 관리 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="92dda-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="92dda-179">이 정책 설정을 사용 하지 않거나 구성 하지 않으면 예외 요청에 대해 적용 하는 방법에 대 한 지침이 사용자에 게 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="92dda-180">참고</span><span class="sxs-lookup"><span data-stu-id="92dda-180">Note</span></span></strong><br/><p><span data-ttu-id="92dda-181">사용자 예외는 컴퓨터당만 관리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="92dda-182">여러 사용자가 같은 컴퓨터에 로그온 하 고 한 사용자가 제외 되지 않은 경우 컴퓨터는 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="92dda-183">고정 드라이브 정책 정의</span><span class="sxs-lookup"><span data-stu-id="92dda-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="92dda-184">이 섹션에서는 다음 GPO 노드에서 찾을 수 있는 mbam에 대 한 고정 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mbam (BitLocker Management)**  \\  **고정 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="92dda-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92dda-185">정책 이름</span><span class="sxs-lookup"><span data-stu-id="92dda-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="92dda-186">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-187">고정 데이터 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-188">권장 구성: <strong> 사용 하도록 설정한 상태 </strong> 에서 <strong> 운영 체제 볼륨을 암호화 해야 하는 경우 자동으로 고정 데이터 드라이브 사용 확인란을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="92dda-189">이 정책 설정을 통해 고정 드라이브를 암호화할지 여부를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="92dda-190">이 정책을 사용 하도록 설정 하는 경우 <strong> 고정 데이터 드라이브에 대 한 암호 사용 구성 정책을 사용 하지 않도록 설정 하지 마세요 </strong> .</span><span class="sxs-lookup"><span data-stu-id="92dda-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="92dda-191"><strong>고정 데이터 드라이브 자동 잠금 해제 </strong> 확인란이 선택 되어 있으면 운영 체제 볼륨을 암호화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="92dda-192">이 정책 설정을 사용 하면 사용자가 모든 고정 드라이브를 BitLocker 보호 아래에 설치 하 여 드라이브를 암호화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="92dda-193">이 정책을 구성 하지 않거나이 정책을 사용 하지 않도록 설정 하는 경우 사용자는 BitLocker 보호에 고정 드라이브를 추가할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="92dda-194">이 정책을 사용 하지 않도록 설정 하는 경우 MBAM 에이전트는 암호화 된 모든 고정 드라이브를 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="92dda-195">운영 체제 볼륨을 암호화 하는 것이 필요 하지 않은 경우에는 <strong> 고정 데이터 드라이브 자동 잠금 해제 확인란의 선택을 취소 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-196">BitLocker로 보호 되지 않는 고정 드라이브에 대 한 "쓰기" 권한 거부</span><span class="sxs-lookup"><span data-stu-id="92dda-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-197">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-198">이 정책 설정은 컴퓨터의 고정 드라이브에 대해 BitLocker 보호가 필요한 지 여부를 결정 하 여 쓸 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="92dda-199">이 정책 설정은 BitLocker를 켤 때 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="92dda-200">정책이 구성 되어 있지 않으면 컴퓨터의 모든 고정 드라이브가 읽기/쓰기 권한으로 탑재 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-201">이전 버전의 Windows에서 BitLocker로 보호 되는 고정 드라이브에 대 한 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="92dda-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-202">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-203">이 정책을 사용 하 여 Windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 FAT (파일 할당 테이블) 파일 시스템으로 포맷 된 고정 드라이브를 잠금 해제 하 고 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="92dda-204">이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="92dda-205">정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 된 고정 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-206">고정 드라이브의 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="92dda-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-207">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-208">이 정책을 사용 하 여 고정 드라이브의 암호 보호를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="92dda-209">정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 사항을 포함 하지 않고 8 자만 요구 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="92dda-210">보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 고정 데이터 드라이브에 대해 암호 필요를 선택 하 고 </strong> , <strong> 암호 복잡도 필요를 선택 하 </strong> 고, 원하는 <strong> 최소 암호 길이를 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-211">BitLocker로 보호 되는 고정 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="92dda-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-212">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-213">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="92dda-214">이 정책이 구성 되어 있지 않으면 BitLocker 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="92dda-215">MBAM에는 AD DS에 백업 하는 복구 정보가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="92dda-216">운영 체제 드라이브 정책 정의</span><span class="sxs-lookup"><span data-stu-id="92dda-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="92dda-217">이 섹션에서는 **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP \ am (BitLocker Management)**  \\  **운영 체제 드라이브**에 있는 mbam의 운영 체제 드라이브 정책 정의에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92dda-218">정책 이름</span><span class="sxs-lookup"><span data-stu-id="92dda-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="92dda-219">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-220">운영 체제 드라이브 암호화 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-221">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="92dda-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="92dda-222">이 정책 설정은 운영 체제 드라이브를 암호화할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="92dda-223">이 정책을 구성 하 여 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="92dda-224">운영 체제 드라이브에 대해 BitLocker 보호를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="92dda-225">운영 체제 보호를 위해 TPM (신뢰할 수 있는 플랫폼 모듈) 핀을 사용 하도록 PIN 사용을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="92dda-226">대 문자와 소문자, 숫자 등의 문자를 허용 하는 향상 된 시작 Pin을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="92dda-227">MBAM은 기호 및 공백을 지원 하기에도 불구 하 고 향상 된 Pin에 대 한 기호 및 공백의 사용을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="92dda-228">이 정책 설정을 사용 하도록 설정 하는 경우 사용자는 BitLocker를 사용 하 여 운영 체제 드라이브를 보호 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="92dda-229">구성 하지 않거나 설정을 사용 하지 않도록 설정한 경우 사용자는 BitLocker를 사용 하 여 운영 체제 드라이브의 보안을 유지할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="92dda-230">이 정책을 사용 하지 않도록 설정 하면, MBAM 에이전트는 운영 체제 볼륨을 암호화 된 상태로 해독 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="92dda-231">이 정책 설정을 사용 하면 사용자가 BitLocker 보호를 사용 하 여 운영 체제를 보호 하 고 드라이브가 암호화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="92dda-232">암호화 요구 사항에 따라 운영 체제 드라이브에 대 한 보호 방법을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="92dda-233">보안 요구 사항이 더 높은 경우 TPM + PIN을 사용 하 고, 향상 된 Pin을 허용 하 고, 최소 PIN 길이를 8 자로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="92dda-234">TPM + PIN 보호기를 사용 하 여이 정책을 사용 하는 경우 <strong> 시스템 </strong>  /  <strong> 전원 관리 </strong>  /  <strong> 절전 모드 설정 </strong> 에서 다음 정책을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="92dda-235">절전 모드에서 대기 상태 (S1-S3) 허용 (전원 사용)</span><span class="sxs-lookup"><span data-stu-id="92dda-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="92dda-236">절전 모드 시 대기 상태 (S1-S3) 허용 (배터리 사용)</span><span class="sxs-lookup"><span data-stu-id="92dda-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-237">TPM 플랫폼 유효성 검사 프로필 구성</span><span class="sxs-lookup"><span data-stu-id="92dda-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-238">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-239">이 정책 설정을 통해 컴퓨터의 TPM 보안 하드웨어가 BitLocker 암호화 키를 보호 하는 방법을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="92dda-240">컴퓨터에 호환 되는 TPM이 없거나 BitLocker에 이미 TPM 보호가 설정 되어 있는 경우에는이 정책 설정이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="92dda-241">이 정책이 구성 되지 않은 경우 TPM은 기본 플랫폼 유효성 검사 프로필 또는 설정 스크립트에 지정 된 플랫폼 유효성 검사 프로필을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-242">BitLocker로 보호 되는 운영 체제 드라이브를 복구 하는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="92dda-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-243">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-244">BitLocker 데이터 복구 에이전트를 사용 하도록이 정책을 구성 하거나 AD DS (Active Directory 도메인 서비스)에 BitLocker 복구 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="92dda-245">이 정책이 구성 되어 있지 않으면 데이터 복구 에이전트를 사용할 수 있으며 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="92dda-246">MBAM 작업에서는 복구 정보를 AD DS에 백업할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="92dda-247">이동식 드라이브 정책 정의</span><span class="sxs-lookup"><span data-stu-id="92dda-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="92dda-248">이 섹션에서는 다음 GPO 노드에서 볼 수 있는 mbam의 이동식 드라이브 정책 정의에 대해 설명 합니다. **컴퓨터 구성** \\ **관리 템플릿** \\ **Windows 구성 요소** \\ **MDOP mblaam (BitLocker Management)**  \\  **이동식 드라이브**.</span><span class="sxs-lookup"><span data-stu-id="92dda-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92dda-249">정책 이름</span><span class="sxs-lookup"><span data-stu-id="92dda-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="92dda-250">개요 및 제안 된 정책 설정</span><span class="sxs-lookup"><span data-stu-id="92dda-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-251">이동식 드라이브에서 BitLocker 사용 제어</span><span class="sxs-lookup"><span data-stu-id="92dda-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-252">권장 구성: <strong> 사용</span><span class="sxs-lookup"><span data-stu-id="92dda-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="92dda-253">이 정책은 이동식 데이터 드라이브의 BitLocker 사용을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="92dda-254">사용자가 이동식 데이터 드라이브에서 <strong> bitlocker 설치 마법사를 실행할 수 있도록 허용 하기 위해 사용자에 게 bitlocker 보호를 적용할 수 있음 옵션을 사용 하도록 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="92dda-255">사용자가 <strong> 드라이브에서 bitlocker 드라이브 암호화를 제거 하거나 암호를 해독 하도록 허용 옵션을 사용 하도록 설정 하 여 </strong> 유지 관리 작업을 수행 하는 동안 암호화를 일시 중단 하거나, 암호를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="92dda-256">이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 BitLocker 보호 적용 허용 옵션을 </strong> 선택 하면 Mbam 클라이언트는 이동식 드라이브에 대 한 복구 정보를 mbam 키 복구 서버에 저장 하 고, 사용자가 암호를 분실 한 경우 드라이브를 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-257">BitLocker로 보호 되지 않는 이동식 드라이브에 대 한 "쓰기" 사용 권한 거부</span><span class="sxs-lookup"><span data-stu-id="92dda-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-258">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-259">이 정책을 사용 하 여 BitLocker 보호 드라이브에 대 한 쓰기 전용 권한을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="92dda-260">이 정책을 사용 하는 경우 쓰기 권한을 허용 하기 전에 컴퓨터의 모든 이동식 데이터 드라이브에 암호화가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-261">이전 버전의 Windows에서 BitLocker로 보호 된 이동식 드라이브에 대 한 액세스 허용</span><span class="sxs-lookup"><span data-stu-id="92dda-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-262">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-263">이 정책을 사용 하 여 Windows Server 2008, Windows Vista, Windows XP SP3 또는 Windows XP SP2를 실행 하는 컴퓨터에서 (FAT) 파일 시스템으로 포맷 된 고정 드라이브를 잠금 해제 하 고 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="92dda-264">이러한 운영 체제에는 BitLocker로 보호 되는 드라이브에 대 한 읽기 전용 권한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="92dda-265">정책을 사용 하지 않도록 설정 하면 FAT 파일 시스템으로 포맷 한 이동식 드라이브는 잠금을 해제할 수 없으며 Windows Server 2008, Windows Vista, windows XP SP3 또는 windows xp SP2를 실행 하는 컴퓨터에서 해당 콘텐츠를 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92dda-266">이동식 데이터 드라이브에 대 한 암호 사용 구성</span><span class="sxs-lookup"><span data-stu-id="92dda-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-267">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-268">이 정책을 사용 하 여 이동식 데이터 드라이브에서 암호 보호를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="92dda-269">이 정책이 구성 되어 있지 않으면 암호가 복잡 한 요구 조건을 포함 하지 않고 8 자만 요구 하는 기본 설정으로 암호가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="92dda-270">보안을 강화 하려면이 정책을 사용 하도록 설정 하 고 <strong> 이동식 데이터 드라이브에 대해 암호 필요를 선택 하 고 </strong> , <strong> 암호 복잡도 필요 </strong> 를 선택한 다음, 기본 사용 <strong> 최소 암호 길이를 설정 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92dda-271">BitLocker로 보호 된 이동식 드라이브를 복구할 수 있는 방법 선택</span><span class="sxs-lookup"><span data-stu-id="92dda-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="92dda-272">권장 구성: <strong> 구성 되지 않음</span><span class="sxs-lookup"><span data-stu-id="92dda-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="92dda-273">BitLocker 데이터 복구 에이전트를 사용 하도록 설정 하거나 BitLocker 복구 정보를 AD DS (Active Directory 도메인 서비스)에 저장 하도록이 정책을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="92dda-274">정책이 <strong> 구성 되지 않음으로 설정 되 면 </strong> 데이터 복구 에이전트는 허용 되 고 복구 정보는 AD DS에 백업 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="92dda-275">MBAM 작업에서는 복구 정보를 AD DS에 백업할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="92dda-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="92dda-276">관련 항목</span><span class="sxs-lookup"><span data-stu-id="92dda-276">Related topics</span></span>


[<span data-ttu-id="92dda-277">MBAM 1.0용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="92dda-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









