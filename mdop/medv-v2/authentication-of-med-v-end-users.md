---
title: MED-V 최종 사용자의 인증
description: MED-V 최종 사용자의 인증
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824888"
---
# <span data-ttu-id="d1d38-103">MED-V 최종 사용자의 인증</span><span class="sxs-lookup"><span data-stu-id="d1d38-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="d1d38-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 최종 사용자의 인증은 매우 중요 한 보안 문제입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="d1d38-105">이 컨텍스트에서 인증은 MED-V 최종 사용자의 id를 확인 하는 것을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="d1d38-106">다음 섹션에서는 MED-V의 최종 사용자 인증에 대 한 정보 및 지침을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="d1d38-107">MED-V의 사용자 인증</span><span class="sxs-lookup"><span data-stu-id="d1d38-107">User Authentication in MED-V</span></span>


<span data-ttu-id="d1d38-108">일반적으로 MED-V의 인증은 사용자가 MED-V에 액세스 하 고 암호를 변경할 때마다 두 가지 수준에서 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="d1d38-109">인증을 위해 MED-V 설정을 구성 하는 방법에 따라 일반적으로 MED-V가 시작 되는 경우 또는 게시 된 응용 프로그램을 처음으로 열려고 할 때 사용자에 게 암호를 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="d1d38-110">최종 사용자 인증에는 다음을 포함 하 여 제어할 수 있는 몇 가지 측면이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="d1d38-111">최종 사용자가 입력 한 자격 증명이 자격 증명 관리자에 저장 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="d1d38-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="d1d38-112">최종 사용자에 게 암호를 입력 하 고 저장 하는 옵션이 표시 되는 방식</span><span class="sxs-lookup"><span data-stu-id="d1d38-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="d1d38-113">회사의 최종 사용자 인증 관리에 대 한 기본 설정 프로세스에 따라 특정 MED-V 작업 영역에 대 한 자격 증명 캐싱이 발생할 지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="d1d38-114">최종 사용자의 자격 증명을 캐시 하는 것은 비밀 번호에 대해 한 번만 표시 되기 때문에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="d1d38-115">최종 사용자가 암호를 저장할 수 없는 경우 또는 새 MED-V 세션을 시작할 때마다 다시 입력 해야 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="d1d38-116">예를 들어, 사용자가 호스트에 로그온 할 때 MED-V가 시작 되도록 구성 되었지만 인증을 사용 하지 않도록 설정한 경우 최종 사용자는 로그온 중에 한 번만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="d1d38-117">이 경우 최종 사용자가 호스트에서 로그 오프할 때까지 자격 증명이 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="d1d38-118">필요한 경우 자격 증명 관리자를 사용 하 여 저장 된 최종 사용자 자격 증명을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="d1d38-119">기본적으로 자격 증명 저장은 사용 되지 않지만 다음 방법 중 하나를 통해이 설정을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="d1d38-120">**Med-v 작업 영역 패키지를 만드는 중**입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="d1d38-121">자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1d38-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="d1d38-122">**Med-v 작업 영역을 배포한 후**</span><span class="sxs-lookup"><span data-stu-id="d1d38-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="d1d38-123">MED-V cmdlet 매개 변수 UxCredentialCacheEnabled를 편집 하 여 터미널 서비스 레지스트리 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="d1d38-124">자세한 내용은 Windows PowerShell 도움말을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1d38-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="d1d38-125">MED-V 작업 영역 배포 후에는 DisablePasswordSaving 이라는 터미널 서비스 정책을 수정 하 여 최종 사용자 인증에 대 한 기본 설정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="d1d38-126">DisablePasswordSaving은 암호 저장 확인란이 RDP 클라이언트 대화 상자 창에 표시 되는지 여부와 MED-V 자격 증명 프롬프트가 표시 되는지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="d1d38-127">다음은 DisablePasswordSaving 이라는 터미널 서비스 정책에 대 한 정책 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="d1d38-128">차례로</span><span class="sxs-lookup"><span data-stu-id="d1d38-128">Regedit:</span></span>**

<span data-ttu-id="d1d38-129">HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="d1d38-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="d1d38-130">참고</span><span class="sxs-lookup"><span data-stu-id="d1d38-130">Note</span></span>**  
<span data-ttu-id="d1d38-131">DisablePasswordSaving에 대해 변경한 내용은 가상 컴퓨터에 대 한 RDP 프롬프트에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="d1d38-132">다음 표에서는 자격 증명 저장을 위한 설정을 구성할 수 있는 다양 한 방법과 여러 구성의 효과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d1d38-133">값</span><span class="sxs-lookup"><span data-stu-id="d1d38-133">Value</span></span></th>
<th align="left"><span data-ttu-id="d1d38-134">구성</span><span class="sxs-lookup"><span data-stu-id="d1d38-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="d1d38-135">결과</span><span class="sxs-lookup"><span data-stu-id="d1d38-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1d38-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="d1d38-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d1d38-137">해제됨</span><span class="sxs-lookup"><span data-stu-id="d1d38-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d1d38-138">MED-V 프롬프트가 표시 되며 수락 확인란을 사용할 수 있으며 선택이 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="d1d38-139">최종 사용자가 확인란을 선택 하면 나중에 사용할 수 있도록 자격 증명이 캐시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="d1d38-140">또한 최종 사용자는 암호가 만료 된 경우에만 메시지를 표시 하는 이점도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="d1d38-141">최종 사용자가 확인란을 선택 하지 않은 경우에는 MED-V 프롬프트 대신 RDC (원격 데스크톱 연결) 클라이언트 프롬프트가 표시 되 고 수락에 허용 되는 확인란의 선택이 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="d1d38-142">최종 사용자가 확인란을 선택 하면 나중에 사용할 수 있도록 RDC 클라이언트 자격 증명이 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d1d38-143">중요</span><span class="sxs-lookup"><span data-stu-id="d1d38-143">Important</span></span></strong><br/><p><span data-ttu-id="d1d38-144">RDC는 최종 사용자가 입력 한 자격 증명의 유효성을 검사 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="d1d38-145">최종 사용자가 RDC 프롬프트를 통해 자격 증명을 캐시 하는 경우 잘못 된 자격 증명이 저장 될 위험이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="d1d38-146">이 경우 Windows 자격 증명 관리자에서 잘못 된 자격 증명을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d1d38-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="d1d38-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d1d38-148">설정됨</span><span class="sxs-lookup"><span data-stu-id="d1d38-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="d1d38-149">참고</span><span class="sxs-lookup"><span data-stu-id="d1d38-149">Note</span></span></strong><br/><p><span data-ttu-id="d1d38-150">이 구성은 최종 사용자 자격 증명을 캐시할 수 없기 때문에 더욱 안전 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="d1d38-151">기본적으로 MED-V 설치는 게스트의 레지스트리 키를 설정 하 여 "암호 만료" 메시지를 표시 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="d1d38-152">최종 사용자에 게는 호스트의 암호 변경만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="d1d38-153">호스트에서 업데이트 되는 자격 증명이 게스트로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="d1d38-154">주의</span><span class="sxs-lookup"><span data-stu-id="d1d38-154">Caution</span></span>**  
<span data-ttu-id="d1d38-155">환경에서 그룹 정책을 사용 하는 경우 게스트의 암호 메시지가 나타나는 레지스트리 키를 재정의할 수 있다는 것을 알립니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="d1d38-156">인증에 대 한 보안 고려 사항</span><span class="sxs-lookup"><span data-stu-id="d1d38-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="d1d38-157">최종 사용자의 자격 증명을 캐시 하는 것이 최상의 사용자 환경을 제공 하는 경우에도 관련 된 위험에 대해 알고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="d1d38-158">자격 증명 캐싱이 사용 되는 경우 최종 사용자의 도메인 자격 증명이 Windows 자격 증명 관리자 내의 해독 가능한 형식으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="d1d38-159">결과적으로 공격자는 시스템 수준 프로세스나 최종 사용자 프로세스로 실행 되는 도구를 작성 하 고 최종 사용자의 자격 증명을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="d1d38-160">DisablePasswordSaving을 **사용**으로 설정 하 여이 위험을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="d1d38-161">MED-V 인증을 사용 하지 않도록 설정 했지만 터미널 서비스 정책 설정을 사용 하는 경우에도 동일한 문제가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d38-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="d1d38-162">관련 항목</span><span class="sxs-lookup"><span data-stu-id="d1d38-162">Related topics</span></span>


[<span data-ttu-id="d1d38-163">MED-V 작업의 보안 모범 사례</span><span class="sxs-lookup"><span data-stu-id="d1d38-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









