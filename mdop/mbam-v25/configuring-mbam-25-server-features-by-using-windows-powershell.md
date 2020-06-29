---
title: Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성
description: Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822838"
---
# <span data-ttu-id="2ee08-103">Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="2ee08-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="2ee08-104">MBAM 2.5 서버 소프트웨어를 설치한 후에는 Windows PowerShell cmdlet 또는 MBAM 서버 구성 마법사를 사용 하 여 MBAM 2.5 서버 기능을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="2ee08-105">이 항목에서는 Windows PowerShell cmdlet을 사용 하 여 MBAM 2.5를 구성 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="2ee08-106">대신 마법사를 사용 하려면 [MBAM 2.5 서버 기능 구성을](configuring-the-mbam-25-server-features.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ee08-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="2ee08-107">이 항목의 내용</span><span class="sxs-lookup"><span data-stu-id="2ee08-107">In this topic</span></span>


<span data-ttu-id="2ee08-108">이 항목에는 Windows PowerShell을 사용 하 여 MBAM 구성에 대 한 다음 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="2ee08-109">MBAM 2.5에 대 한 Windows PowerShell 도움말을 로드 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2ee08-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="2ee08-110">MBAM Windows PowerShell cmdlet에 대 한 도움말을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="2ee08-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="2ee08-111">Windows PowerShell을 사용 하는 경우에만 수행할 수 있는 구성 및 MBAM 서버 구성 마법사를 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="2ee08-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="2ee08-112">Windows PowerShell을 사용 하 여 MBAM 서버 기능을 구성 하기 위한 필수 구성 요소 및 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ee08-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="2ee08-113">Windows PowerShell을 사용 하 여 원격 컴퓨터에 MBAM 구성</span><span class="sxs-lookup"><span data-stu-id="2ee08-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="2ee08-114">필수 계정 및 해당 Windows PowerShell cmdlet 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ee08-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="2ee08-115">MBAM을 관리 하는 데 사용 되는 **MbamBitLockerRecoveryKey** 및 **Get-MbamTPMOwnerPassword** windows powershell cmdlet에 대 한 자세한 내용은 [Windows powershell을 사용 하 여 mbam 2.5 관리](using-windows-powershell-to-administer-mbam-25.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ee08-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="2ee08-116">MBAM 2.5에 대 한 Windows PowerShell 도움말을 로드 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2ee08-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="2ee08-117">TechNet의 Windows PowerShell cmdlet 목록은 [Windows powershell을 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화](https://go.microsoft.com/fwlink/?LinkId=392816)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ee08-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="2ee08-118">MBAM 서버 소프트웨어를 설치한 후 Windows PowerShell cmdlet에 대 한 MBAM 2.5 도움말을 로드 하려면</span><span class="sxs-lookup"><span data-stu-id="2ee08-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="2ee08-119">Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="2ee08-120">Type **Update-도움말-Microsoft \* MBAM**.</span><span class="sxs-lookup"><span data-stu-id="2ee08-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="2ee08-121">MBAM Windows PowerShell cmdlet에 대 한 도움말을 가져오는 방법</span><span class="sxs-lookup"><span data-stu-id="2ee08-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="2ee08-122">MBAM에 대 한 Windows PowerShell 도움말은 다음 형식으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ee08-123">Windows PowerShell 도움말 형식</span><span class="sxs-lookup"><span data-stu-id="2ee08-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="2ee08-124">추가 정보</span><span class="sxs-lookup"><span data-stu-id="2ee08-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-125">Windows PowerShell 명령 프롬프트에서 <strong> get-help </strong> &lt; <em> cmdlet을 입력 합니다.</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="2ee08-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-126">최신 Windows PowerShell cmdlet을 업로드 하려면, MBAM에 대 한 Windows PowerShell 도움말을 로드 하는 방법에 대 한 이전 섹션의 지침을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-127">웹 페이지로 TechNet에서</span><span class="sxs-lookup"><span data-stu-id="2ee08-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-128">다운로드 센터에서 Word .docx 파일로</span><span class="sxs-lookup"><span data-stu-id="2ee08-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-129">.Pdf 파일로 다운로드 센터에서</span><span class="sxs-lookup"><span data-stu-id="2ee08-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="2ee08-130">Windows PowerShell을 사용 하는 경우에만 수행할 수 있는 구성 및 MBAM 서버 구성 마법사를 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="2ee08-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ee08-131">Windows PowerShell을 사용 하 여 수행할 수 있는 구성</span><span class="sxs-lookup"><span data-stu-id="2ee08-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="2ee08-132">세부 정보</span><span class="sxs-lookup"><span data-stu-id="2ee08-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-133">웹 응용 프로그램에서 웹 서비스를 별도의 컴퓨터에 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-134">마법사를 사용 하 여 웹 서비스와 웹 응용 프로그램을 같은 컴퓨터에 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-135">모든 Configuration Manager 개체를 설치 하지 않고 별도의 보고 서비스에 대 한 보고서를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-136">Configuration Manager에서 모든 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-137">에서 개체를 삭제 하면 구성 관리자에서 모든 준수 데이터가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-138">데이터베이스에 대 한 사용자 지정 연결 문자열을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-139">예: 미러링 작업을 수행 하도록 웹 응용 프로그램을 구성 하려면 <strong> Enable-MbamWebApplication cmdlet을 사용 하 여 </strong> 연결 문자열에 적절 한 장애 조치 파트너 구문을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-140">필수 구성 요소 검사에 실패 한 경우에도 유효성 검사를 건너뛰고 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2ee08-141">**참고**  Windows PowerShell cmdlet 또는 MBAM 서버 구성 마법사를 사용 하 여 MBAM 데이터베이스를 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="2ee08-142">준수 및 감사 데이터가 실수로 제거 되는 것을 방지 하기 위해 데이터베이스 관리자는 데이터베이스를 수동으로 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="2ee08-143">Windows PowerShell을 사용 하 여 MBAM 서버 기능을 구성 하기 위한 필수 구성 요소 및 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2ee08-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="2ee08-144">구성을 시작 하기 전에 다음 필수 구성 요소를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="2ee08-145">계정 관련 필수 조건</span><span class="sxs-lookup"><span data-stu-id="2ee08-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ee08-146">요소일</span><span class="sxs-lookup"><span data-stu-id="2ee08-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="2ee08-147">세부 정보 또는 추가 정보</span><span class="sxs-lookup"><span data-stu-id="2ee08-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-148">필요한 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-149"><strong> </strong> 이 항목의 뒷부분에 나오는 필수 계정 및 해당 Windows PowerShell cmdlet 매개 변수 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ee08-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-150">Windows PowerShell cmdlet에 매개 변수로 전달 하는 사용자 계정 및 그룹은 도메인에서 유효한 계정 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-151">로컬 계정은 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-152">하위 수준 형식으로 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-153">예제:</span><span class="sxs-lookup"><span data-stu-id="2ee08-153">Examples:</span></span></p>
<p><span data-ttu-id="2ee08-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="2ee08-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2ee08-155">사용 권한 관련 필수 조건</span><span class="sxs-lookup"><span data-stu-id="2ee08-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ee08-156">요소일</span><span class="sxs-lookup"><span data-stu-id="2ee08-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="2ee08-157">세부 정보 또는 추가 정보</span><span class="sxs-lookup"><span data-stu-id="2ee08-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-158">MBAM 기능을 구성 하는 로컬 컴퓨터의 관리자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-159">관리자 권한 Windows PowerShell 명령 프롬프트를 사용 하 여 모든 Windows PowerShell cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-160"><strong>사용-MbamDatabase cmdlet에 </strong> 만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="2ee08-161">&quot; &quot; 대상 Microsoft SQL Server 데이터베이스의 인스턴스에 대 한 데이터베이스 사용 권한을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="2ee08-162">이 사용자 계정은 로컬 관리자 그룹에 속해 있거나, MBAM 볼륨 섀도 복사본 서비스 (VSS) 기록기를 등록 하는 Backup Operators 그룹의 일부 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ee08-163">기본적으로 데이터베이스 관리자 또는 시스템 관리자는 필요한 &quot; 모든 데이터베이스 권한을 만들어야 합니다 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2ee08-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="2ee08-164">VSS 기록기에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> 볼륨 섀도 복사본 서비스를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="2ee08-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-165"><strong>System Center Configuration Manager 통합 기능에 </strong> 만 해당:</span><span class="sxs-lookup"><span data-stu-id="2ee08-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="2ee08-166">이 기능을 사용 하도록 설정 하는 사용자에 게는 구성 관리자에서 다음 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ee08-167">Configuration Manager의 권한 유형</span><span class="sxs-lookup"><span data-stu-id="2ee08-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="2ee08-168">필요한 권한</span><span class="sxs-lookup"><span data-stu-id="2ee08-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-169">Configuration Manager 사이트 권한:</span><span class="sxs-lookup"><span data-stu-id="2ee08-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="2ee08-170">Read</span><span class="sxs-lookup"><span data-stu-id="2ee08-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ee08-171">Configuration Manager 수집 권한:</span><span class="sxs-lookup"><span data-stu-id="2ee08-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="2ee08-172">만들기-삭제-읽기-변경-배포 구성 항목</span><span class="sxs-lookup"><span data-stu-id="2ee08-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ee08-173">Configuration Manager 구성 항목 권한:</span><span class="sxs-lookup"><span data-stu-id="2ee08-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="2ee08-174">만들기-삭제-읽기</span><span class="sxs-lookup"><span data-stu-id="2ee08-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="2ee08-175">Windows PowerShell을 사용 하 여 원격 컴퓨터에 MBAM 구성</span><span class="sxs-lookup"><span data-stu-id="2ee08-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ee08-176">이 접근 권한 값을 사용 하는 경우</span><span class="sxs-lookup"><span data-stu-id="2ee08-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ee08-177">원격 컴퓨터에서 MBAM 2.5 서버 기능을 구성 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="2ee08-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="2ee08-178">Windows PowerShell cmdlet이 한 컴퓨터에서 실행 되 고 있으며 다른 원격 컴퓨터에서 기능을 구성 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ee08-179">수행 해야 할 작업</span><span class="sxs-lookup"><span data-stu-id="2ee08-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ee08-180">Windows PowerShell을 사용 하 여 원격 컴퓨터에서 MBAM 2.5 서버 기능을 구성 하려면 다음을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="2ee08-181">MBAM 2.5 서버 소프트웨어가 원격 컴퓨터에 설치 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="2ee08-182">CredSSP (자격 증명 보안 지원 공급자) 프로토콜을 사용 하 여 Windows PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="2ee08-183">WinRM (Windows Remote Management)을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="2ee08-184">WinRM을 사용 하도록 설정 하는 데 실패 하 고 올바르게 구성 하는 경우 <strong> </strong> 이 표에 설명 된 새 PSSession cmdlet에 오류가 표시 되 고 문제를 해결 하는 방법에 대 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="2ee08-185">WinRM에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> Windows Remote Management 사용을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="2ee08-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ee08-186">수행 해야 하는 이유</span><span class="sxs-lookup"><span data-stu-id="2ee08-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ee08-187">이 프로토콜은 사용자의 관리 자격 증명을 사용 하 여 Windows PowerShell cmdlet이 Active Directory 도메인 서비스에 연결할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="2ee08-188">이 프로토콜을 사용 하지 않고 Windows PowerShell 세션을 시작 하는 경우 유효성 검사 오류가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ee08-189">CredSSP 프로토콜을 사용 하 여 Windows PowerShell 세션을 시작 하는 방법</span><span class="sxs-lookup"><span data-stu-id="2ee08-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ee08-190">Windows PowerShell 프롬프트에서 다음 코드를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="2ee08-191">다음 코드에서는 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="2ee08-192">필수 계정 및 해당 Windows PowerShell cmdlet 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ee08-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="2ee08-193">다음 표에서는 MBAM 2.5 서버 기능을 구성 하는 데 필요한 계정에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="2ee08-194">또한 구성 중에 계정을 지정 해야 하는 해당 Windows PowerShell cmdlet 및 매개 변수도 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="2ee08-195">Cmdlet 매개 변수 형식 (사용자 또는 그룹) 설명-MBAMDatabase 사용</span><span class="sxs-lookup"><span data-stu-id="2ee08-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="2ee08-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="2ee08-196">AccessAccount</span></span>

<span data-ttu-id="2ee08-197">사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="2ee08-197">User or Group</span></span>

<span data-ttu-id="2ee08-198">이 데이터베이스의 데이터 및 보고서에 대 한 액세스 권한을 웹 응용 프로그램에 제공 하기 위해이 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="2ee08-199">값이 도메인 사용자 인 경우 **Enable-MbamWebApplication** cmdlet을 실행 하는 데 사용 되는 **Webserviceapplicationpoolcredential** 매개 변수는 동일한 사용자 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="2ee08-200">값이 도메인 사용자 그룹인 경우 **Webserviceapplicationpoolcredential** 매개 변수에서 사용 하는 도메인 계정이이 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="2ee08-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="2ee08-201">ReportAccount</span></span>

<span data-ttu-id="2ee08-202">사용자 또는 그룹</span><span class="sxs-lookup"><span data-stu-id="2ee08-202">User or Group</span></span>

<span data-ttu-id="2ee08-203">이 데이터베이스에 대 한 읽기 전용 권한이 있는 도메인 사용자 또는 사용자 그룹을 지정 하 여 정책 준수 및 감사 데이터에 대 한 MBAM 보고서 액세스를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="2ee08-204">값이 도메인 사용자 이면 **Enable-MbamReport** Cmdlet의 **ComplianceAndAuditDBCredential** 매개 변수는 동일한 사용자 계정을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="2ee08-205">값이 도메인 사용자 그룹인 경우 **ComplianceAndAuditDBCredential** 매개 변수에 사용 되는 도메인 계정이이 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="2ee08-206">사용-MbamReport</span><span class="sxs-lookup"><span data-stu-id="2ee08-206">Enable-MbamReport</span></span>

<span data-ttu-id="2ee08-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="2ee08-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="2ee08-208">사용자</span><span class="sxs-lookup"><span data-stu-id="2ee08-208">User</span></span>

<span data-ttu-id="2ee08-209">로컬 SSRS 인스턴스가 MBAM 준수 및 감사 데이터베이스에 연결 하는 데 사용 하는 관리 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="2ee08-210">관리 자격 증명의 도메인 사용자는 **Enable-MbamDatabase** cmdlet을 실행 하는 동안 사용 되는 **reportaccount** 매개 변수에 사용 되는 사용자 계정과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="2ee08-211">Domain Users 그룹을 **Reportaccount** 매개 변수와 함께 사용 하는 경우이 계정은 해당 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="2ee08-212">**중요**  관리 자격 증명에 지정 된 계정에는 보안이 향상 되는 사용자 권한이 제한 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="2ee08-213">또한 계정의 암호가 만료 되지 않도록 설정 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="2ee08-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="2ee08-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="2ee08-215">Group</span><span class="sxs-lookup"><span data-stu-id="2ee08-215">Group</span></span>

<span data-ttu-id="2ee08-216">보고서에 대 한 읽기 권한이 있는 도메인 사용자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="2ee08-217">지정 된 그룹은 **Enable-MbamWebApplication** Cmdlet의 **ReportsReadOnlyAccessGroup** 매개 변수에 사용 되는 그룹과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="2ee08-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="2ee08-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="2ee08-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="2ee08-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="2ee08-220">Group</span><span class="sxs-lookup"><span data-stu-id="2ee08-220">Group</span></span>

<span data-ttu-id="2ee08-221">보고서 영역을 제외한 관리 및 모니터링 웹 사이트의 모든 영역에 액세스할 수 있는 도메인 사용자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="2ee08-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="2ee08-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="2ee08-223">Group</span><span class="sxs-lookup"><span data-stu-id="2ee08-223">Group</span></span>

<span data-ttu-id="2ee08-224">관리 및 모니터링 웹 사이트의 **TPM 관리** 및 **드라이브 복구** 영역에 대 한 액세스 권한이 있는 도메인 사용자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="2ee08-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="2ee08-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="2ee08-226">Group</span><span class="sxs-lookup"><span data-stu-id="2ee08-226">Group</span></span>

<span data-ttu-id="2ee08-227">관리 및 모니터링 웹 사이트의 **보고서** 영역에 대 한 읽기 권한이 있는 domain Users 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="2ee08-228">지정 된 그룹은 **Enable-MbamReport** Cmdlet의 **ReportsReadOnlyAccessGroup** 매개 변수에 사용 되는 그룹과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="2ee08-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="2ee08-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="2ee08-230">사용자</span><span class="sxs-lookup"><span data-stu-id="2ee08-230">User</span></span>

<span data-ttu-id="2ee08-231">이 (가) MBAM 웹 응용 프로그램에 사용할 도메인 사용자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="2ee08-232">이 계정은 **Enable-MbamDatabase** Cmdlet의 **accessaccount** 매개 변수에 지정 된 것과 동일한 도메인 사용자 계정 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="2ee08-233">**사용-MbamDatabase** cmdlet을 실행할 때 **accessaccount** 매개 변수에서 도메인 사용자 그룹을 사용 하는 경우 여기에 지정 된 도메인 사용자는 해당 그룹의 구성원 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="2ee08-234">관리 자격 증명을 지정 하지 않으면 이전에 사용 하도록 설정 된 웹 응용 프로그램에서 지정한 관리 자격 증명이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="2ee08-235">모든 웹 응용 프로그램에서 동일한 응용 프로그램 풀 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="2ee08-236">여러 번 지정 된 경우에는 가장 최근에 지정 된 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="2ee08-237">**중요**  보안 향상을 위해 관리 자격 증명에 지정 된 계정을 제한 된 사용자 권한으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="2ee08-238">또한 계정 암호가 만료 되지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="2ee08-239">기본 제공 IIS \ _IUSRS 계정 또는 **Webserviceapplicationpoolcredential** 매개 변수에 사용 되는 계정이 인증 로컬 보안 설정 **이후에 클라이언트 가장** 에 추가 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="2ee08-240">로컬 보안 설정을 보려면 **로컬 보안 정책 편집기**를 열고, **로컬 정책** 노드를 확장 하 고, **사용자 권한 할당** 노드를 선택한 다음 **인증 후 클라이언트로 가장** 을 두 번 클릭 하 고 세부 정보 창에서 **일괄 작업으로 로그온** 그룹 정책 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="2ee08-241">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2ee08-241">Related topics</span></span>


[<span data-ttu-id="2ee08-242">MBAM 2.5 서버 기능 구성</span><span class="sxs-lookup"><span data-stu-id="2ee08-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="2ee08-243">MBAM 2.5 서버 기능 구성의 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="2ee08-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="2ee08-244">Windows PowerShell을 사용하여 MBAM 2.5 관리</span><span class="sxs-lookup"><span data-stu-id="2ee08-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="2ee08-245">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="2ee08-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2ee08-246">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2ee08-247">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ee08-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





