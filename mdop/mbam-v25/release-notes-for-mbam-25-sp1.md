---
title: MBAM 2.5 SP1 릴리스 정보
description: MBAM 2.5 SP1 릴리스 정보
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824988"
---
# <span data-ttu-id="26aef-103">MBAM 2.5 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="26aef-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="26aef-104">이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="26aef-105">이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 SP1을 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="26aef-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="26aef-106">이 릴리스 노트에는 MBAM을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있으며 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="26aef-107">이러한 릴리스 노트가 다른 MBAM 2.5 SP1 설명서와 다를 경우 신뢰할 수 있는 최신 변경 사항을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="26aef-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="26aef-109">MBAM 2.5 SP1의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="26aef-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="26aef-110">이 섹션에는 MBAM 2.5 SP1에 대 한 릴리스 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="26aef-111">PowerShell 읽기-AD \ \* cmdlet은 사용자에 게 충분 한 권한이 없는 경우 피드백을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="26aef-112">MBAM 서버에 대 한 PowerShell Read AD \ \* cmdlet을 사용 하려는 사용자에 게 Active Directory 복구 정보를 읽거나 TPM 정보를 읽을 수 있는 사용자 권한이 없는 경우에는 cmdlet이 사용자에 게 오류 또는 경고를 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="26aef-113">**해결 방법:** 필요한 사용자 권한이 있는 경우 PowerShell 읽기-AD \ \* cmdlet만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="26aef-114">MBAM Active Directory (AD) 마이그레이션 cmdlet이 볼륨 복구 정보를 검색 하지 않음</span><span class="sxs-lookup"><span data-stu-id="26aef-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="26aef-115">MBAM Active Directory (AD) 마이그레이션 cmdlet은 슬래시 문자 (/)가 OU 이름의 일부인 경우 조직 구성 단위 (Ou)의 컴퓨터에 대 한 볼륨 복구 정보를 검색 하지 못합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="26aef-116">이 오류가 발생 했을 때 파이프라인 종료 오류로 인해 반복 되는 광고를 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="26aef-117">**기술 정보:** 명령을 실행할 때 다음 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="26aef-118">또한 예외 스택 추적도 `Error[0].Exception.StackTrace` 다음과 같이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="26aef-119">**해결 방법:** 이 문제를 해결 하려면 다음 작업 중 하나를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="26aef-120">OU의 이름을 변경 하 여 슬래시 문자를 제거 하 고 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="26aef-121">백업 프로세스에서 문제가 있는 OU를 제외 하려면 이름에 슬래시 문자가 포함 되지 않은 Ou 목록을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="26aef-122">이러한 Ou에 대해 한 번에 하나의 OU에 대해 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="26aef-123">H/pc에서 TPM + PIN 보호기를 설정한 경우 MBAM이 볼륨을 암호화 하는 데 실패 하 고 오류를 보고 함</span><span class="sxs-lookup"><span data-stu-id="26aef-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="26aef-124">최종 사용자가 태블릿 장치에서 TPM + PIN 보호기를 설정 하려고 하면 MBAM이 암호화에 실패 하 고 오류를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="26aef-125">이 문제는 태블릿 장치에 부팅 전 환경 키보드가 없기 때문에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="26aef-126">**해결 방법:** **태블릿에서 부팅 가능 키보드 입력이 필요한 BitLocker 인증 사용** 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="26aef-127">이 설정은 BitLocker 그룹 정책 설정 이며, MBAM 그룹 정책 템플릿에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="26aef-128">모든 서비스 계정에 대해 사용자 계정 이름이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="26aef-129">모든 서비스 계정에 대해 UPN (사용자 계정 이름)을 MBAM으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="26aef-130">계정에 대 한 UPN을 만들지 못한 경우 구성 프로세스 중에 사용자 또는 그룹을 Active Directory에서 찾을 수 없음을 나타내는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="26aef-131">**해결 방법:** UPN을 서비스 계정에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="26aef-132">IIS를 .NET Framework 4.5으로 업그레이드 한 후 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않음</span><span class="sxs-lookup"><span data-stu-id="26aef-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="26aef-133">IIS (인터넷 정보 서비스)를 Microsoft .NET Framework 4.5으로 업그레이드 하면 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="26aef-134">**해결 방법:** [.Net Framework 4.0을 설치 하면 "system.servicemodel: HttpModule '을 로드할 수 없습니다. 라는 문서 오류 메시지](https://go.microsoft.com/fwlink/?LinkId=393568)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26aef-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="26aef-135">보고서가 구성 되지 않은 경우 관리 및 모니터링 웹 사이트에 "보고서를 찾을 수 없음" 오류 메시지가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="26aef-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="26aef-136">관리 및 모니터링 웹 사이트를 구성한 다음 보고서 기능을 먼저 구성 하지 않고 보고서를 보려고 하면 오류 메시지에 해당 보고서를 찾을 수 없음을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="26aef-137">**해결 방법:** 웹 응용 프로그램을 구성 하기 전에 보고서 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="26aef-138">SSL이 SSRS에 구성 되어 있지 않은 경우 관리 및 모니터링 웹 사이트의 보고서에 경고가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="26aef-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="26aef-139">SQL Server Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 구성할 때 보고서 기능에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="26aef-140">그런 다음 관리 및 모니터링 웹 사이트를 열고 보고서를 선택 하면 "보안 콘텐츠만 표시 됨"과 같은 오류 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="26aef-141">**해결 방법:** 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="26aef-142">이 문제를 해결 하려면 SQL Server Reporting Services가 설치 되어 있는 MBAM 컴퓨터로 이동한 다음 **Reporting Services 구성 관리자**를 실행 하 고 **웹 서비스 URL**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="26aef-143">서버에 대 한 적절 한 SSL 인증서를 선택 하 고 적절 한 SSL 포트 (기본 포트 443)를 입력 한 다음 **적용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="26aef-144">BitLocker 준수 요약 보고서에서 "뒤로"를 클릭 하면 오류가 발생 하는 경우</span><span class="sxs-lookup"><span data-stu-id="26aef-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="26aef-145">BitLocker 준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="26aef-146">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="26aef-146">**Workaround:** None.</span></span>

### <span data-ttu-id="26aef-147">암호화 강도가 BitLocker 컴퓨터 준수 보고서에 잘못 표시 됨</span><span class="sxs-lookup"><span data-stu-id="26aef-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="26aef-148">**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 강도를 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 BitLocker 컴퓨터 준수 보고서에 항상 암호화 수준에 대 한 "unknown"이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="26aef-149">그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="26aef-150">**해결 방법:** **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="26aef-151">드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="26aef-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="26aef-152">SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="26aef-153">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="26aef-153">**Workaround:** None.</span></span> <span data-ttu-id="26aef-154">MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="26aef-155">보안 강화 구성으로 인해 보고서에 오류 메시지가 잘못 표시 될 수 있음</span><span class="sxs-lookup"><span data-stu-id="26aef-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="26aef-156">Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="26aef-157">웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 기본적으로 ESC가 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="26aef-158">**해결 방법:** MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타나면 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="26aef-159">또는 ESC가 설정 되지 않은 다른 컴퓨터에서 보고서를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="26aef-160">Bitlocker XTS 암호화 알고리즘에 대 한 지원</span><span class="sxs-lookup"><span data-stu-id="26aef-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="26aef-161">Windows 10 버전 1511의 XTS 암호화 알고리즘에 대 한 Bitlocker 추가 지원이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="26aef-162">HF02를 사용 하면이 Bitlocker 옵션 및 HF04에 대 한 클라이언트 지원이 추가 되어 서버 쪽 지원이 추가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="26aef-163">그러나, 다음과 같은 한 가지 알려진 제한 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="26aef-164">고객은 동일한 컴퓨터에서 OS와 데이터 볼륨에 대해 동일한 암호화 강도를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="26aef-165">다른 암호화 강도가 사용 되는 경우 MBAM은 컴퓨터를 **비규격**으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="26aef-166">셀프 서비스 포털이 키 ID 항목에 "-"를 자동으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="26aef-167">HF02에서 MBAM 셀프 서비스 포털은 키 ID 항목에 '-'를 자동으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="26aef-168">**참고:** Javascript를 적용 하려면 서버를 다시 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="26aef-169">MBAM 2.5 Sp1 보고서가 작동 하지 않거나 올바르게 렌더링 되지 않음</span><span class="sxs-lookup"><span data-stu-id="26aef-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="26aef-170">SQL Server 2016 edition에서 SSRS가 호스팅되는 경우 보고서 페이지가 올바르게 렌더링 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="26aef-171">예를 들어 헬프데스크 탐색 – 보고서를 클릭 하면 (강조 표시 된 부분에 "x"가 있음) Fiddler를 사용 하 여 더 많은 작업을 하 고, 보고서를 클릭 한 후에는, HTML 4.0 렌더링 형식을 사용 하 여 SSRS 페이지를 호출 하는 것 처럼 보입니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="26aef-172">**해결 방법:** 사이트 마스터 코드를 보고 X-UA 모드가 IE8으로 결정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="26aef-173">IE8은 수명이 만료 되는 방식이 고, 고객은 IE11를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="26aef-174">설정을 다음 코드로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-174">Update the setting to the below code.</span></span> <span data-ttu-id="26aef-175">이를 통해 사이트는 IE11 렌더링 기술을 활용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="26aef-176">원래 설정:</span><span class="sxs-lookup"><span data-stu-id="26aef-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="26aef-177">Chrome, Firefox 등의 다른 브라우저에 문제가 표시 되지 않는 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="26aef-178">관련 항목</span><span class="sxs-lookup"><span data-stu-id="26aef-178">Related topics</span></span>


[<span data-ttu-id="26aef-179">MBAM 2.5 정보</span><span class="sxs-lookup"><span data-stu-id="26aef-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="26aef-180">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="26aef-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="26aef-181">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="26aef-182">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26aef-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





