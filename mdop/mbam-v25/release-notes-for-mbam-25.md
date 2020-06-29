---
title: MBAM 2.5 릴리스 정보
description: MBAM 2.5 릴리스 정보
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824983"
---
# <span data-ttu-id="78dc7-103">MBAM 2.5 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="78dc7-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="78dc7-104">이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="78dc7-105">이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="78dc7-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="78dc7-106">이 릴리스 노트에는 MBAM을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있으며 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="78dc7-107">이러한 릴리스 노트가 다른 MBAM 2.5 설명서와 다를 경우 신뢰할 수 있는 최신 변경 사항을 고려해 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="78dc7-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="78dc7-109">MBAM 2.5 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="78dc7-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="78dc7-110">이 섹션에서는 MBAM 2.5에 대 한 릴리스 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="78dc7-111">웹 브라우저가 의도 하지 않게 관리자 권한으로 실행</span><span class="sxs-lookup"><span data-stu-id="78dc7-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="78dc7-112">MBAM 서버 구성 도구의 도움말 링크를 사용 하면 브라우저 창을 관리자 권한으로 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="78dc7-113">**해결 방법:** 다른 사이트로 이동 하기 전에 Internet Explorer 보안 강화 구성 (IESC)을 사용 하거나 웹 브라우저를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="78dc7-114">**참고**  이 문제는 MBAM 2.5 SP1에서 해결 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="78dc7-115">MBAM은 AES 256 비트 암호화 키 및 디퓨저를 사용 하 여 암호화 된 클라이언트를 비규격으로 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="78dc7-116">컴퓨터에 MBAM 2.5 클라이언트가 설치 되어 있고, 디퓨저 암호화 강도의 AES 256 비트를 사용 하 여 암호화 되는 경우 MBAM 클라이언트는 mbam 준수 보고서에서 비규격으로 보고 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="78dc7-117">**해결 방법:** [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972)에서 핫픽스를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="78dc7-118">H/pc에서 TPM + PIN 보호기를 설정한 경우 MBAM이 볼륨을 암호화 하는 데 실패 하 고 오류를 보고 함</span><span class="sxs-lookup"><span data-stu-id="78dc7-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="78dc7-119">최종 사용자가 태블릿 장치에서 TPM + PIN 보호기를 설정 하려고 하면 MBAM이 암호화에 실패 하 고 오류를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="78dc7-120">이 문제는 태블릿 장치에 부팅 전 환경 키보드가 없기 때문에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="78dc7-121">**해결 방법:** **태블릿에서 부팅 가능 키보드 입력이 필요한 BitLocker 인증 사용** 그룹 정책 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="78dc7-122">이 설정은 BitLocker 그룹 정책 설정 이며, MBAM 그룹 정책 템플릿에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="78dc7-123">모든 서비스 계정에 대해 사용자 계정 이름이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="78dc7-124">모든 서비스 계정에 대해 UPN (사용자 계정 이름)을 MBAM으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="78dc7-125">계정에 대 한 UPN을 만들지 못한 경우 구성 프로세스 중에 사용자 또는 그룹을 Active Directory에서 찾을 수 없음을 나타내는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="78dc7-126">**해결 방법:** UPN을 서비스 계정에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="78dc7-127">클라이언트 컴퓨터가 Microsoft Ajax 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털에 추가 구성이 필요 함</span><span class="sxs-lookup"><span data-stu-id="78dc7-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="78dc7-128">클라이언트 컴퓨터에 Microsoft의 CDN (콘텐츠 배달 네트워크)에 액세스할 수 없는 경우 셀프 서비스 포털에 특정 JavaScript 파일에 대 한 액세스 권한이 부여 되는 경우 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="78dc7-129">클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하지 않으면 로그온 한 회사 이름과 계정만 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="78dc7-130">오류 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-130">No error message appears.</span></span>

<span data-ttu-id="78dc7-131">**해결 방법:** MBAM 2.5 SP1을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="78dc7-132">또는 다음 지침에 따라 셀프 서비스 포털을 구성 합니다. [클라이언트 컴퓨터가 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하는 방법을 설명](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="78dc7-133">IIS를 .NET Framework 4.5으로 업그레이드 한 후 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않음</span><span class="sxs-lookup"><span data-stu-id="78dc7-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="78dc7-134">IIS (인터넷 정보 서비스)를 Microsoft .NET Framework 4.5으로 업그레이드 하면 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="78dc7-135">**해결 방법:** [.Net Framework 4.0을 설치 하면 "system.servicemodel: HttpModule '을 로드할 수 없습니다. 라는 문서 오류 메시지](https://go.microsoft.com/fwlink/?LinkId=393568)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="78dc7-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="78dc7-136">보고서가 구성 되지 않은 경우 관리 및 모니터링 웹 사이트에 "보고서를 찾을 수 없음" 오류 메시지가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="78dc7-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="78dc7-137">관리 및 모니터링 웹 사이트를 구성한 다음 보고서 기능을 먼저 구성 하지 않고 보고서를 보려고 하면 오류 메시지에 해당 보고서를 찾을 수 없음을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="78dc7-138">**해결 방법:** 웹 응용 프로그램을 구성 하기 전에 보고서 기능을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="78dc7-139">SSL이 SSRS에 구성 되어 있지 않은 경우 관리 및 모니터링 웹 사이트의 보고서에 경고가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="78dc7-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="78dc7-140">SQL Server Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 구성할 때 보고서 기능에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="78dc7-141">그런 다음 관리 및 모니터링 웹 사이트를 열고 보고서를 선택 하면 "보안 콘텐츠만 표시 됨"과 같은 오류 메시지가 나타납니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="78dc7-142">**해결 방법:** 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="78dc7-143">이 문제를 해결 하려면 SQL Server Reporting Services가 설치 되어 있는 MBAM 컴퓨터로 이동한 다음 **Reporting Services 구성 관리자**를 실행 하 고 **웹 서비스 URL**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="78dc7-144">서버에 대 한 적절 한 SSL 인증서를 선택 하 고 적절 한 SSL 포트 (기본 포트 443)를 입력 한 다음 **적용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="78dc7-145">BitLocker 준수 요약 보고서에서 "뒤로"를 클릭 하면 오류가 발생 하는 경우</span><span class="sxs-lookup"><span data-stu-id="78dc7-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="78dc7-146">BitLocker 준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="78dc7-147">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="78dc7-147">**Workaround:** None.</span></span>

### <span data-ttu-id="78dc7-148">사용 된 공간만 암호화가 올바르게 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="78dc7-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="78dc7-149">MBAM 클라이언트를 설치한 후 처음으로 컴퓨터를 암호화 하 고 사용 된 공간만 암호화를 구현 하도록 그룹 정책 설정을 구성한 경우에는 MBAM이 디스크의 사용 된 공간만 암호화 하는 대신 전체 디스크를 잘못 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="78dc7-150">컴퓨터는 MBAM 클라이언트를 설치 하는 경우에만 사용 된 공간으로 암호화 되 고 같은 그룹 정책 설정을 구성한 경우 MBAM은 드라이브가 올바르게 암호화 되었음을 보고 하 고 드라이브를 다시 암호화 하려고 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="78dc7-151">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="78dc7-151">**Workaround:** None.</span></span>

### <span data-ttu-id="78dc7-152">암호화 강도가 BitLocker 컴퓨터 준수 보고서에 잘못 표시 됨</span><span class="sxs-lookup"><span data-stu-id="78dc7-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="78dc7-153">**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 강도를 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 BitLocker 컴퓨터 준수 보고서에 항상 암호화 수준에 대 한 "unknown"이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="78dc7-154">그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="78dc7-155">**해결 방법:** **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="78dc7-156">드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="78dc7-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="78dc7-157">SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="78dc7-158">**해결 방법:** 않아야.</span><span class="sxs-lookup"><span data-stu-id="78dc7-158">**Workaround:** None.</span></span> <span data-ttu-id="78dc7-159">MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="78dc7-160">보안 강화 구성으로 인해 보고서에 오류 메시지가 잘못 표시 될 수 있음</span><span class="sxs-lookup"><span data-stu-id="78dc7-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="78dc7-161">Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="78dc7-162">웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 기본적으로 ESC가 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="78dc7-163">**해결 방법:** MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타나면 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="78dc7-164">또는 ESC가 설정 되지 않은 다른 컴퓨터에서 보고서를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="78dc7-165">MBAM 2.5에 대 한 핫픽스와 지식 기반 문서</span><span class="sxs-lookup"><span data-stu-id="78dc7-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="78dc7-166">이 표에는 MBAM 2.5에 대 한 핫픽스와 KB 아티클이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="78dc7-167">기술 자료 문서</span><span class="sxs-lookup"><span data-stu-id="78dc7-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="78dc7-168">제목</span><span class="sxs-lookup"><span data-stu-id="78dc7-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="78dc7-169">Link</span><span class="sxs-lookup"><span data-stu-id="78dc7-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78dc7-170">2975636</span><span class="sxs-lookup"><span data-stu-id="78dc7-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-171">Microsoft BitLocker 관리 및 모니터링 2.5 핫픽스 패키지 1</span><span class="sxs-lookup"><span data-stu-id="78dc7-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="78dc7-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="78dc7-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78dc7-173">3015477</span><span class="sxs-lookup"><span data-stu-id="78dc7-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-174">BitLocker 관리 및 모니터링 2.5 핫픽스 패키지 2</span><span class="sxs-lookup"><span data-stu-id="78dc7-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="78dc7-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="78dc7-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78dc7-176">3011022</span><span class="sxs-lookup"><span data-stu-id="78dc7-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-177">SSRS 인스턴스의 이름에 밑줄이 포함 되어 있으면 MBAM 2.5 설치 또는 구성 관리자 보고가 실패 함</span><span class="sxs-lookup"><span data-stu-id="78dc7-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="78dc7-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="78dc7-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78dc7-179">2756402</span><span class="sxs-lookup"><span data-stu-id="78dc7-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-180">MBAM 클라이언트가 이벤트 ID 4 및 오류 코드 0x8004100E와 함께 실패 함 이벤트 설명</span><span class="sxs-lookup"><span data-stu-id="78dc7-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="78dc7-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="78dc7-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78dc7-182">2639518</span><span class="sxs-lookup"><span data-stu-id="78dc7-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-183">MBAM 엔터프라이즈 또는 컴퓨터 준수 보고서 열기 오류</span><span class="sxs-lookup"><span data-stu-id="78dc7-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="78dc7-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="78dc7-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="78dc7-185">2870842</span><span class="sxs-lookup"><span data-stu-id="78dc7-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-186">MBAM 2.0 구성 관리자 통합 시나리오에서 SQL Server 2008을 사용 하 여 설치 실패</span><span class="sxs-lookup"><span data-stu-id="78dc7-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="78dc7-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="78dc7-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="78dc7-188">2975472</span><span class="sxs-lookup"><span data-stu-id="78dc7-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="78dc7-189">여러 MBAM 클라이언트가 MBAM 복구 데이터베이스에 연결 되는 경우의 SQL 교착 상태</span><span class="sxs-lookup"><span data-stu-id="78dc7-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="78dc7-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="78dc7-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="78dc7-191">관련 항목</span><span class="sxs-lookup"><span data-stu-id="78dc7-191">Related topics</span></span>


[<span data-ttu-id="78dc7-192">MBAM 2.5 정보</span><span class="sxs-lookup"><span data-stu-id="78dc7-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="78dc7-193">MBAM에 대 한 제안이 있으십니까?</span><span class="sxs-lookup"><span data-stu-id="78dc7-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="78dc7-194">[여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="78dc7-195">MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78dc7-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





