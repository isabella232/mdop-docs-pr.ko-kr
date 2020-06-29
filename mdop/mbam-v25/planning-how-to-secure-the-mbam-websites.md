---
title: MBAM 웹 사이트를 보호하는 방법 계획
description: MBAM 웹 사이트를 보호하는 방법 계획
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825023"
---
# <span data-ttu-id="e8163-103">MBAM 웹 사이트를 보호하는 방법 계획</span><span class="sxs-lookup"><span data-stu-id="e8163-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="e8163-104">이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털을 보호 하기 위한 다음 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-105">메서드</span><span class="sxs-lookup"><span data-stu-id="e8163-105">Method</span></span></th>
<th align="left"><span data-ttu-id="e8163-106">필수 또는 선택 사항</span><span class="sxs-lookup"><span data-stu-id="e8163-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-107">인증서를 사용 하 여 MBAM 웹 사이트 보안</span><span class="sxs-lookup"><span data-stu-id="e8163-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-108">선택 사항 이지만 매우 좋음</span><span class="sxs-lookup"><span data-stu-id="e8163-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-109">응용 프로그램 풀 계정에 대 한 SPN (서비스 사용자 이름) 등록</span><span class="sxs-lookup"><span data-stu-id="e8163-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-110">필수</span><span class="sxs-lookup"><span data-stu-id="e8163-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e8163-111">MBAM 배포를 보호 하는 방법에 대 한 자세한 내용은 [mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8163-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="e8163-112">인증서를 사용 하 여 MBAM 웹 사이트 보안</span><span class="sxs-lookup"><span data-stu-id="e8163-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="e8163-113">인증서를 사용 하 여 다음 간의 통신을 보호 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="e8163-114">MBAM 클라이언트 및 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="e8163-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="e8163-115">브라우저 및 관리 및 모니터링 웹 사이트 및 셀프 서비스 포털 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="e8163-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="e8163-116">인증서 요청 및 설치에 대 한 자세한 내용은 [인터넷 서버 인증서 구성을](https://technet.microsoft.com/library/cc731977.aspx)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8163-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="e8163-117">참고</span><span class="sxs-lookup"><span data-stu-id="e8163-117">Note</span></span>**  
<span data-ttu-id="e8163-118">Windows PowerShell을 사용 하는 경우에만 다른 서버에서 웹 사이트 및 웹 서비스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="e8163-119">MBAM 서버 구성 마법사를 사용 하 여 웹 사이트를 구성 하는 경우에는 동일한 서버에서 웹 사이트 및 웹 서비스를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="e8163-120">웹 서비스와 데이터베이스 간의 통신을 보호 하려면 SQL Server에 암호화를 강제로 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="e8163-121">웹 서비스와 SQL Server 간의 통신을 비롯 하 여 SQL Server에 대 한 모든 연결을 보호 하는 방법에 대 한 자세한 내용은 [Mbam 2.5 보안 고려 사항을](mbam-25-security-considerations.md#bkmk-secure-databases)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8163-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="e8163-122">응용 프로그램 풀 계정에 대 한 Spn 등록</span><span class="sxs-lookup"><span data-stu-id="e8163-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="e8163-123">MBAM 서버에서 관리 및 모니터링 웹 사이트와 셀프 서비스 포털의 통신을 인증 하도록 설정 하려면 웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 호스트 이름에 대 한 SPN (서비스 사용자 이름)을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="e8163-124">이 항목에는 다음 유형의 호스트 이름에 대해 Spn을 등록 하는 방법에 대 한 지침이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="e8163-125">정규화 된 도메인 이름</span><span class="sxs-lookup"><span data-stu-id="e8163-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="e8163-126">NetBIOS 이름</span><span class="sxs-lookup"><span data-stu-id="e8163-126">NetBIOS name</span></span>

-   <span data-ttu-id="e8163-127">가상 이름</span><span class="sxs-lookup"><span data-stu-id="e8163-127">Virtual name</span></span>

### <span data-ttu-id="e8163-128">초기 MBAM 설치에 대 한 Spn을 만들기 전에</span><span class="sxs-lookup"><span data-stu-id="e8163-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="e8163-129">Spn 만들기를 시작 하기 전에 다음 표의 정보를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-130">작업 또는 항목</span><span class="sxs-lookup"><span data-stu-id="e8163-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="e8163-131">추가 정보</span><span class="sxs-lookup"><span data-stu-id="e8163-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-132">AD DS (Active Directory 도메인 서비스)에서 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-133">서비스 계정은 AD DS에서 만든 사용자 계정으로, MBAM 웹 사이트에 보안을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="e8163-134">MBAM 웹 사이트는 응용 프로그램 풀에서 실행 되며, 해당 id는 서비스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="e8163-135">그러면 Spn이 응용 프로그램 풀 계정에 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e8163-136">참고</span><span class="sxs-lookup"><span data-stu-id="e8163-136">Note</span></span></strong><br/><p><span data-ttu-id="e8163-137">모든 웹 서버에 같은 응용 프로그램 풀 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-138">IIS-IUSRS 그룹 계정 또는 응용 프로그램 풀 계정에 필요한 권한이 부여 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-139">이를 확인 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="e8163-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="e8163-140"><strong>로컬 보안 정책 편집기를 열고 </strong> <strong> 로컬 정책 노드를 확장 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="e8163-141"><strong>사용자 권한 할당 </strong> 노드를 선택 하 고 인증 후 클라이언트로 가장을 두 번 클릭 하 고 <strong> </strong> <strong> 오른쪽 창에서 일괄 작업으로 로그온 </strong> 그룹 정책 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-142">도메인 관리 계정을 사용 하 여 MBAM 웹 사이트를 구성 하는 경우 MBAM이 사용자를 위한 Spn을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-143">도메인 관리 계정을 사용 하 여 MBAM 웹 사이트를 구성 하는 경우 사용 중인 호스트 이름 유형에 Spn을 수동으로 등록 하려면이 항목의 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="e8163-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e8163-144">정규화 된 도메인 호스트 이름을 사용할 때 Spn 등록</span><span class="sxs-lookup"><span data-stu-id="e8163-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="e8163-145">MBAM을 구성할 때 정규화 된 도메인 호스트 이름을 사용 하는 경우 다음 예제에 표시 된 대로 SPN을 하나만 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-146">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="e8163-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e8163-147">예제 및 추가 정보</span><span class="sxs-lookup"><span data-stu-id="e8163-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-148">정규화 된 도메인 이름에 대 한 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e8163-149">정규화 된 호스트 이름이 <strong> mybitlockerrecovery.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e8163-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-150">응용 프로그램 풀 계정에 대해 등록 하는 SPN에 대해 제한 된 위임을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="e8163-151">제한 된 위임 구성</span><span class="sxs-lookup"><span data-stu-id="e8163-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="e8163-152">이 요구 사항은 MBAM 2.5에만 적용 됩니다. MBAM 2.5 SP1에서는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e8163-153">NetBIOS 호스트 이름을 사용할 때 Spn 등록</span><span class="sxs-lookup"><span data-stu-id="e8163-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="e8163-154">MBAM을 구성할 때 NetBIOS 호스트 이름을 사용 하는 경우 다음 예제와 같이 NetBIOS 이름에 대해 하나의 SPN 및 정규화 된 도메인 이름에 대 한 다른 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-155">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="e8163-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e8163-156">예제 및 추가 정보</span><span class="sxs-lookup"><span data-stu-id="e8163-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-157">NetBIOS 호스트 이름에 대 한 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e8163-158">NetBIOS 호스트 이름이 <strong> nbname01 </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e8163-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-159">정규화 된 도메인 이름에 대 한 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e8163-160">정규화 된 도메인 이름이 <strong> nbname01.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e8163-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-161">응용 프로그램 풀 계정에 대해 등록 하는 Spn에 대해 제한 된 위임을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="e8163-162">제한 된 위임 구성</span><span class="sxs-lookup"><span data-stu-id="e8163-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="e8163-163">이 요구 사항은 MBAM 2.5에만 적용 됩니다. MBAM 2.5 SP1에서는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="e8163-164">가상 호스트 이름을 사용할 때 Spn 등록</span><span class="sxs-lookup"><span data-stu-id="e8163-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="e8163-165">정규화 된 도메인 이름인 가상 호스트 이름으로 MBAM을 구성 하는 경우 가상 호스트 이름에 대해 SPN을 하나만 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="e8163-166">구성 하는 가상 호스트 이름이 정규화 된 도메인 이름이 아니면 다음 예제와 같이 정규화 된 도메인 이름을 지정 하는 두 번째 SPN을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-167">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="e8163-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e8163-168">예제 및 추가 정보</span><span class="sxs-lookup"><span data-stu-id="e8163-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-169">이 예제와 같이 가상 호스트 이름이 정규화 된 도메인 이름이 면 SPN을 하나만 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e8163-170">이 예제에서는 가상 호스트 이름이 <strong> mbamvirtual.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e8163-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-171">가상 호스트 이름이 정규화 된 도메인 이름이 아닌 경우이 추가 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e8163-172">이 예제에서 가상 호스트 이름은 <strong> mbamvirtual이 </strong> 고 웹 응용 프로그램 풀에 사용 되는 도메인 계정은 <strong> contoso\mbamapppooluser입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e8163-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-173">가상 호스트 이름이 정규화 된 도메인 이름이 아닌 경우이 추가 SPN을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="e8163-174">이 예제에서는 가상 호스트 이름이 <strong> mbamvirtual.contoso.com </strong> 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 <strong> contoso\mbamapppooluser입니다 </strong> .</span><span class="sxs-lookup"><span data-stu-id="e8163-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-175">DNS (도메인 이름 서버) 서버에서 사용자 지정 호스트 이름에 대해 "A record"를 만들고 웹 서버 또는 부하 분산 장치를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-176">DNS 호스트 레코드 구성에서 "DNS 호스트 A 레코드를 구성 하려면" 섹션을 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> </a> .</span><span class="sxs-lookup"><span data-stu-id="e8163-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="e8163-177">CNAMES 대신 레코드를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="e8163-178">도메인 주소를 가리키는 CNAMES을 사용 하는 경우 응용 프로그램 풀 계정에서 웹 서버 이름에 대 한 Spn도 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-179">응용 프로그램 풀 계정에 대해 등록 하는 Spn에 대해 제한 된 위임을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="e8163-180">제한 된 위임 구성</span><span class="sxs-lookup"><span data-stu-id="e8163-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="e8163-181">이 요구 사항은 MBAM 2.5에만 적용 됩니다. MBAM 2.5 SP1에서는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="e8163-182">이전 버전의 MBAM에서 업그레이드할 때 SPN 등록</span><span class="sxs-lookup"><span data-stu-id="e8163-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="e8163-183">다음과 같은 경우에만이 섹션의 단계를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="e8163-184">이전 버전의 MBAM에서 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="e8163-185">부하 분산 또는 분산 구성에서 MBAM 2.5에서 웹 사이트를 실행 하 고 현재 부하 분산 되지 않은 구성으로 실행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="e8163-186">응용 프로그램 풀 계정이 아닌 컴퓨터 계정에 Spn을 등록 한 경우, MBAM은 기존 Spn을 사용 하며 부하 분산 또는 분산 구성에서 웹 사이트를 구성할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-187">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="e8163-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="e8163-188">예제 및 추가 정보</span><span class="sxs-lookup"><span data-stu-id="e8163-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-189">AD DS (Active Directory 도메인 서비스)에 응용 프로그램 풀 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-190">현재 설치 된 웹 사이트 및 웹 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="e8163-191">MBAM 서버 기능 또는 소프트웨어 제거</span><span class="sxs-lookup"><span data-stu-id="e8163-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-192">컴퓨터 계정에서 Spn을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-193">응용 프로그램 풀 계정에 Spn을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-194"><a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">가상 호스트 이름을 사용할 때 spn을 등록 하는 단계를 따릅니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="e8163-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e8163-195">웹 응용 프로그램 및 웹 서비스를 다시 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="e8163-196">MBAM 2.5 웹 응용 프로그램을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="e8163-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e8163-197">구성에 사용 하는 방법에 따라 다음 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8163-198">메서드</span><span class="sxs-lookup"><span data-stu-id="e8163-198">Method</span></span></th>
<th align="left"><span data-ttu-id="e8163-199">세부 정보</span><span class="sxs-lookup"><span data-stu-id="e8163-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e8163-200">MBAM 서버 구성 마법사</span><span class="sxs-lookup"><span data-stu-id="e8163-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e8163-201"><strong>웹 서비스 응용 프로그램 풀 도메인 계정 필드에 응용 프로그램 풀 계정을 입력 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="e8163-202">Windows PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="e8163-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="e8163-203"><code>WebServiceApplicationPoolCredential</code>매개 변수에 계정을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="e8163-204">중요</span><span class="sxs-lookup"><span data-stu-id="e8163-204">Important</span></span></strong><br/><p><span data-ttu-id="e8163-205">입력 하는 호스트 이름은 Spn을 만드는 가상 호스트 이름과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="e8163-206">또한 웹 팜에서는 구성 하는 모든 서버에서 호스트 이름 및 응용 프로그램 풀 자격 증명이 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="e8163-207">MBAM이 웹 응용 프로그램을 구성 하는 경우 Spn을 등록 하려고 시도 하지만이 작업은 사용자가 MBAM을 설치 하는 서버에 대 한 도메인 관리자 권한이 있는 경우에만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="e8163-208">이러한 권한이 없는 경우 구성을 완료할 수 있지만, MBAM을 구성 하기 전이나 후에 Spn을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="e8163-209">필수 요청 필터링 설정</span><span class="sxs-lookup"><span data-stu-id="e8163-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="e8163-210">응용 프로그램이 정상적으로 작동 하려면 ' 나열 되지 않은 파일 이름 확장명 허용 '이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="e8163-211">이는 ' Microsoft BitLocker 관리 및 모니터링 ' > 요청 필터링-> 편집 기능 설정을 탐색 하 여 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="e8163-212">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e8163-212">Related topics</span></span>


[<span data-ttu-id="e8163-213">MBAM 2.5용 환경 준비</span><span class="sxs-lookup"><span data-stu-id="e8163-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="e8163-214">MBAM 2.5 배포 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="e8163-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="e8163-215">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="e8163-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e8163-216">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="e8163-217">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8163-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



