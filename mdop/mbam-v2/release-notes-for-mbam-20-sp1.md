---
title: MBAM 2.0 SP1 릴리스 정보
description: MBAM 2.0 SP1 릴리스 정보
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825583"
---
# <span data-ttu-id="34e85-103">MBAM 2.0 SP1 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="34e85-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="34e85-104">이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="34e85-105">이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)을 설치 하기 전에 자세히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="34e85-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="34e85-106">이 릴리스 정보에는 BitLocker 관리 및 모니터링 2.0 SP1을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있으며, 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="34e85-107">이러한 릴리스 정보와 다른 MBAM 2.0 SP1 설명서 사이에 차이가 있는 경우 최신 변경 내용을 신뢰할 수 있는 것으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="34e85-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="34e85-109">MBAM 2.0 SP1의 알려진 문제점</span><span class="sxs-lookup"><span data-stu-id="34e85-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="34e85-110">이 섹션에는 MBAM 2.0 SP1에 대 한 알려진 문제가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="34e85-111">Mbam 2.0 SP1에 대 한 Configuration Manager 통합 토폴로지로 MBAM을 업그레이드 하려면 Configuration Manager 개체의 수동 제거 필요</span><span class="sxs-lookup"><span data-stu-id="34e85-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="34e85-112">구성 관리자에서 MBAM을 사용 하는 경우 MBAM 2.0 SP1으로 업그레이드 하려면 MBAM 설치의 일부로 Configuration Manager에 설치 된 모든 Configuration Manager 개체를 수동으로 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="34e85-113">수동으로 제거 해야 하는 개체는 MBAM 보고서, MBAM 지원 컴퓨터 모음, BitLocker 보호 구성 기준 및 연결 된 구성 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="34e85-114">**해결 방법**: 다음 단계를 완료 하 여 Configuration Manager 개체를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="34e85-115">다음 단계에 설명 된 대로 기존 준수 데이터를 외부 파일에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="34e85-116">**참고**  Configuration Manager에서 기존 기준을 삭제 하면 기존의 모든 BitLocker 준수 데이터가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="34e85-117">데이터는 시간에 따라 다시 생성 되지만, 규정 준수 데이터를 다시 생성 하기 전에 특정 컴퓨터에 대 한 규정 준수 데이터가 필요한 경우에 대비 하 여 데이터 복사본을 저장 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="34e85-118">BitLocker 준수 데이터 기록을 저장 하려면 **Bitlocker 엔터프라이즈 준수 정보** 보고서를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="34e85-119">보고서에서 **저장** 아이콘을 클릭 하 고 **Excel**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="34e85-120">저장 된 보고서에는 컴퓨터 이름, 도메인 이름, 준수 상태, 예외, 장치 사용자, 준수 상태 정보, 마지막 연락 날짜/시간 등의 데이터가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="34e85-121">자세한 볼륨 정보 및 암호화 강도와 같은 일부 정보는 저장 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="34e85-122">**Mbam** 설치 관리자를 사용 하 여 서버에서 **mbam** 을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="34e85-123">Configuration Manager에서 다음 개체를 수동으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="34e85-124">MBAM 지원 컴퓨터 모음</span><span class="sxs-lookup"><span data-stu-id="34e85-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="34e85-125">BitLocker Protection 기준</span><span class="sxs-lookup"><span data-stu-id="34e85-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="34e85-126">BitLocker 운영 체제 드라이브 보호 구성 항목</span><span class="sxs-lookup"><span data-stu-id="34e85-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="34e85-127">BitLocker 고정 데이터 드라이브 보호 구성 항목</span><span class="sxs-lookup"><span data-stu-id="34e85-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="34e85-128">Configuration Manager SQL Server Reporting Services 사이트에서 MBAM 보고서 폴더를 수동으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="34e85-129">이렇게 하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-129">To do this:</span></span>

    1.  <span data-ttu-id="34e85-130">Internet Explorer를 사용 하 여 보고 서비스 지점을 찾습니다 (예: http:// &lt; /reports. server). &gt;</span><span class="sxs-lookup"><span data-stu-id="34e85-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="34e85-131">적절 한 구성 관리자 사이트 코드 링크를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="34e85-132">MBAM 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="34e85-133">MBAM 서버 설치 관리자를 사용 하 여 Configuration Manager 통합 개체를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="34e85-134">클라이언트 컴퓨터는 시간에 따라 BitLocker 준수 데이터를 다시 업로드 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="34e85-135">셀프 서비스 포털의 제출 단추가 인터넷 Explorer10에서 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="34e85-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="34e85-136">인터넷 Explorer10을 사용 하 여 관리 및 모니터링 웹 사이트에 액세스 하면 웹 사이트의 **제출** 단추가 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="34e85-137">**해결 방법**: 관리 및 모니터링 웹 사이트를 설치한 서버에서 [ASP.NET browser 정의 파일에 대 한 핫픽스](https://go.microsoft.com/fwlink/?LinkId=317798)를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="34e85-138">국제 도메인 이름은 지원 되지 않음</span><span class="sxs-lookup"><span data-stu-id="34e85-138">International domain names are not supported</span></span>

<span data-ttu-id="34e85-139">MBAM 2.0 SP1은 국제 도메인 이름을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="34e85-140">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="34e85-140">**Workaround**: None.</span></span>

### <span data-ttu-id="34e85-141">SSL이 SSRS에 구성 되어 있지 않은 경우 관리 및 모니터링 웹 사이트의 보고서에 경고가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="34e85-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="34e85-142">SQLServer Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 설치 하면 보고서의 URL이 HTTPS 대신 HTTP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="34e85-143">그런 다음 관리 및 모니터링 웹 사이트로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="34e85-144">**해결 방법**:이 문제를 해결 하려면 **Reporting services 구성 관리자** 에서 SQLServer reporting services가 설치 되어 있는 mbam 서버의 SSL을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="34e85-145">관리 및 모니터링 서버 웹 사이트를 제거한 다음 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="34e85-146">규정 준수 요약 보고서에서 뒤로를 클릭 하면 오류가 발생할</span><span class="sxs-lookup"><span data-stu-id="34e85-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="34e85-147">준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="34e85-148">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="34e85-148">**Workaround**: None.</span></span>

### <span data-ttu-id="34e85-149">사용 된 공간만 암호화가 올바르게 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="34e85-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="34e85-150">MBAM 클라이언트를 설치한 후 처음으로 컴퓨터를 암호화 하 고 사용 된 공간만 암호화를 구현 하도록 그룹 정책 개체를 설정한 경우, MBAM이 디스크의 사용 된 공간만 암호화 하는 대신 전체 디스크를 잘못 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="34e85-151">MBAM 클라이언트를 설치 하기 전에 사용 된 공간만 암호화로 컴퓨터를 암호화 하 고 동일한 사용 공간만 암호화 그룹 정책 개체를 설정한 경우 MBAM은 설정을 인식 하 고 준수 보고서에 암호화를 올바르게 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="34e85-152">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="34e85-152">**Workaround**: None.</span></span>

### <span data-ttu-id="34e85-153">컴퓨터 준수 보고서에 암호화 강도가 잘못 표시 됨</span><span class="sxs-lookup"><span data-stu-id="34e85-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="34e85-154">**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 수준을 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 컴퓨터 준수 **보고서에 항상 암호 강도가 표시 되지** 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="34e85-155">그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="34e85-156">**해결 방법**: **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="34e85-157">드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="34e85-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="34e85-158">SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="34e85-159">**해결 방법**: 없음</span><span class="sxs-lookup"><span data-stu-id="34e85-159">**Workaround**: None.</span></span> <span data-ttu-id="34e85-160">MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="34e85-161">보안 강화 구성으로 인해 보고서가 올바르게 표시 되지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="34e85-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="34e85-162">Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 **액세스 거부** 메시지가 나타날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="34e85-163">기본적으로 보안 강화 구성은 웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="34e85-164">**해결 방법**: Mbam 서버에서 보고서를 보려고 할 때 **액세스 거부** 메시지가 나타나면 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="34e85-165">또는 고급 보안 구성을 사용할 수 없는 다른 컴퓨터의 보고서를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="34e85-166">SQLServer2008에서 SQLServer2012로 업그레이드 하면 MBAM 설치가 실패 함</span><span class="sxs-lookup"><span data-stu-id="34e85-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="34e85-167">SQLServer2008에서 SQLServer2012로 업그레이드 한 다음 준수 및 감사 데이터베이스 또는 복구 데이터베이스를 설치 하려고 하면 설치가 실패 하 고 롤백됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="34e85-168">이 오류는 SQLServer를 업그레이드 하는 동안 필요한 SQLCMD.exe 파일이 제거 되었고 MBAM 설치 관리자에서 찾을 수 없기 때문에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="34e85-169">MSI 로그 파일 줄은 다음과 유사 하 게 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="34e85-170">RunDbInstallScript Recovery Db CA: BinDir E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exe-RunDbInstallScript 복구 Db CA: dbInstance-xxxxxx\\I01RunDbInstallScript 복구 Db CA: sqlScript-C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript 복구 Db CA: defaultFileName-MBAM \ _Recovery \ _and 복구 Db CA: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery Db CA: 복구 데이터베이스 설치 scriptRunDbInstallScript 복구 Db CA를 실행 하는 중: Sqlcmd 로그 파일이 C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript 복구 Db CA 예외: 설치 복구 데이터베이스 사용자 지정 작업 명령 명령줄 출력 예외: 시스템에서 지정 된 파일을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="34e85-171">MBAM 서버 Windows Installer는 HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.에서 레지스트리의 경로 문자열 값을 검색 하 여 SQLCMD.exe 경로를 찾기 위해 하드 코드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="34e85-172">SQLServer2008에서 SQLServer2012으로 마이그레이션하는 동안 키가 계속 표시 되지만, SQLupgrade 프로세스가 파일을 제거 했으므로 데이터 값이 참조 하는 경로에 SQLCMD.exe 파일이 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="34e85-173">**해결 방법**: HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path 문자열 값의 이름을 **\ _old 경로로**설정한 다음 Mbam 서버에서 Windows Installer를 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="34e85-174">설치가 성공적으로 완료 되 고 SQLServer2012에서 데이터베이스를 만드는 경우 **경로 \ _old** 경로를 **경로로**바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="34e85-175">MBAM 2.0 SP1에 대 한 핫픽스 및 지식 기반 문서</span><span class="sxs-lookup"><span data-stu-id="34e85-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="34e85-176">이 섹션에는 MBAM 2.0 SP1에 대 한 핫픽스와 KB 문서가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="34e85-177">기술 자료 문서</span><span class="sxs-lookup"><span data-stu-id="34e85-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="34e85-178">제목</span><span class="sxs-lookup"><span data-stu-id="34e85-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="34e85-179">Link</span><span class="sxs-lookup"><span data-stu-id="34e85-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-180">2831166</span><span class="sxs-lookup"><span data-stu-id="34e85-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-181">&quot;System CENTER CM 개체가 이미 설치 된 상태에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 설치 실패&quot;</span><span class="sxs-lookup"><span data-stu-id="34e85-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="34e85-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-183">2870849</span><span class="sxs-lookup"><span data-stu-id="34e85-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-184">사용자가 MBAM 2.0 셀프 서비스 포털을 사용 하 여 BitLocker 복구 키를 검색할 수 없음</span><span class="sxs-lookup"><span data-stu-id="34e85-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="34e85-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-186">2756402</span><span class="sxs-lookup"><span data-stu-id="34e85-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-187">MBAM 클라이언트가 이벤트 ID 4 및 오류 코드 0x8004100E와 함께 실패 함 이벤트 설명</span><span class="sxs-lookup"><span data-stu-id="34e85-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="34e85-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-189">2620287</span><span class="sxs-lookup"><span data-stu-id="34e85-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-190">MBAM에서 보고서 탭을 클릭 하면 "/Reports ' 응용 프로그램에서 오류 메시지" 서버 오류 발생 "</span><span class="sxs-lookup"><span data-stu-id="34e85-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="34e85-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-192">2639518</span><span class="sxs-lookup"><span data-stu-id="34e85-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-193">MBAM 엔터프라이즈 또는 컴퓨터 준수 보고서 열기 오류</span><span class="sxs-lookup"><span data-stu-id="34e85-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="34e85-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-195">2620269</span><span class="sxs-lookup"><span data-stu-id="34e85-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-196">MBAM Enterprise 보고서가 업데이트 되지 않음</span><span class="sxs-lookup"><span data-stu-id="34e85-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="34e85-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-198">2712461</span><span class="sxs-lookup"><span data-stu-id="34e85-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-199">도메인 컨트롤러에 MBAM을 설치 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="34e85-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-201">2876732</span><span class="sxs-lookup"><span data-stu-id="34e85-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-202">MBAM 2.0의 독립 실행형 또는 Configuration Manager 통합 설정 중에 오류 코드 0x80071a90이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="34e85-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-204">2754259</span><span class="sxs-lookup"><span data-stu-id="34e85-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-205">MBAM 및 보안 네트워크 통신</span><span class="sxs-lookup"><span data-stu-id="34e85-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="34e85-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-207">2870842</span><span class="sxs-lookup"><span data-stu-id="34e85-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-208">Configuration Manager 통합 시나리오에서 SQL Server 2008와 함께 MBAM 2.0 설치가 실패 함</span><span class="sxs-lookup"><span data-stu-id="34e85-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="34e85-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-210">2668533</span><span class="sxs-lookup"><span data-stu-id="34e85-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-211">SQL SSRS가 올바르게 구성 되어 있지 않으면 MBAM이 실패 함</span><span class="sxs-lookup"><span data-stu-id="34e85-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="34e85-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-213">2870847</span><span class="sxs-lookup"><span data-stu-id="34e85-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-214">MBAM 2.0 &quot; &#39;Reporting Services 가리키기&#39; 역할에 대 한 Configuration Manager 서버 역할 설정을 검색 하는 동안 오류가 발생 하 여 설치에 실패 함&quot;</span><span class="sxs-lookup"><span data-stu-id="34e85-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="34e85-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-216">2870839</span><span class="sxs-lookup"><span data-stu-id="34e85-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-217">MBAM 2.0 Enterprise Reports는 SQL 작업 CreateCache 오류로 인해 MBAM 2.0 독립 실행형 토폴로지에서 새로 고쳐지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34e85-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="34e85-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-219">2620269</span><span class="sxs-lookup"><span data-stu-id="34e85-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-220">MBAM Enterprise 보고서가 업데이트 되지 않음</span><span class="sxs-lookup"><span data-stu-id="34e85-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="34e85-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34e85-222">2935997</span><span class="sxs-lookup"><span data-stu-id="34e85-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-223">MBAM 지원 컴퓨터 규정 준수 보고에 지원 되지 않는 제품이 포함 되어 있지 않음</span><span class="sxs-lookup"><span data-stu-id="34e85-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="34e85-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34e85-225">2612822</span><span class="sxs-lookup"><span data-stu-id="34e85-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="34e85-226">컴퓨터 레코드가 MBAM에서 거부 됨</span><span class="sxs-lookup"><span data-stu-id="34e85-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="34e85-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="34e85-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="34e85-228">관련 항목</span><span class="sxs-lookup"><span data-stu-id="34e85-228">Related topics</span></span>


[<span data-ttu-id="34e85-229">MBAM 2.0 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="34e85-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 





