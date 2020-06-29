---
title: MBAM 2.5 설치 문제 해결
description: MBAM 설치 문제를 해결 하는 방법을 소개 합니다.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812865"
---
# <span data-ttu-id="a5131-103">MBAM 2.5 설치 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a5131-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="a5131-104">이 문서에서는 독립 실행형 구성에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 설치 문제를 해결 하는 방법을 소개 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="a5131-105">문제 해결을 위해 MBAM 로그 파일을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="a5131-106">MBAM에는 서버 설치, 클라이언트 설치 및 이벤트에 대 한 로깅이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="a5131-107">문제 해결을 위해이 로깅을 참조 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="a5131-108">MBAM 서버 설치 로그 파일</span><span class="sxs-lookup"><span data-stu-id="a5131-108">MBAM server installation log files</span></span>

<span data-ttu-id="a5131-109">MBAMServerSetup.exe는 MBAM 설치 중 사용자 의% temp% 폴더에 다음 로그 파일을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="a5131-110">Microsoft_BitLocker_Administration_and_Monitoring_<14> 번호를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="a5131-111">MBAMServerSetup.exe는 MBAM 설정 및 MBAM 서버 기능 설치 중 취한 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="a5131-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. 로그</span><span class="sxs-lookup"><span data-stu-id="a5131-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="a5131-113">MBAMServerSetup.exe 설치 하는 동안 취한 추가 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="a5131-114">MBAM 클라이언트 설치 로그 파일</span><span class="sxs-lookup"><span data-stu-id="a5131-114">MBAM client installation log file</span></span>

<span data-ttu-id="a5131-115">클라이언트 설치 는% temp% 폴더의 다음 로그 파일 또는 클라이언트 설치 방법에 따라 사용자 지정 위치에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="a5131-116">MSI \<five random characters\> . 로그</span><span class="sxs-lookup"><span data-stu-id="a5131-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="a5131-117">이 로그는 MBAM 클라이언트 설치 중 수행 되는 작업을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="a5131-118">MBAM 클라이언트 이벤트-로깅 채널</span><span class="sxs-lookup"><span data-stu-id="a5131-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="a5131-119">MBAM에는 별도의 이벤트 로깅 채널이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="a5131-120">관리자, 분석 및 운영 로그 파일은 이벤트 뷰어에 있으며, **응용 프로그램 및 서비스 로그**에서  >  **Microsoft**  >  **Windows**  >  **mbam**을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="a5131-121">다음 표에는 각 이벤트 로그에 대 한 간략 한 설명이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="a5131-122">이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="a5131-122">Event log</span></span>| <span data-ttu-id="a5131-123">설명</span><span class="sxs-lookup"><span data-stu-id="a5131-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="a5131-124">Microsoft-Windows-MBAM/관리자</span><span class="sxs-lookup"><span data-stu-id="a5131-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="a5131-125">오류 메시지 포함</span><span class="sxs-lookup"><span data-stu-id="a5131-125">Contains error messages</span></span>|
|<span data-ttu-id="a5131-126">Microsoft-Windows-MBAM/분석</span><span class="sxs-lookup"><span data-stu-id="a5131-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="a5131-127">고급 로깅 정보 포함</span><span class="sxs-lookup"><span data-stu-id="a5131-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="a5131-128">Microsoft-Windows-MBAM/작동</span><span class="sxs-lookup"><span data-stu-id="a5131-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="a5131-129">성공 메시지 포함</span><span class="sxs-lookup"><span data-stu-id="a5131-129">Contains success messages</span></span>|

### <span data-ttu-id="a5131-130">MBAM 서버 이벤트-로깅 채널</span><span class="sxs-lookup"><span data-stu-id="a5131-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="a5131-131">로그 파일은 이벤트 뷰어에 있으며, **응용 프로그램 및 서비스 로그**에서  >  **Microsoft**  >  **Windows**  >  **mbam**을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="a5131-132">다음 표에는 MBAM 2.5에 도입 된 서버 이벤트 로그가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="a5131-133">이벤트 로그</span><span class="sxs-lookup"><span data-stu-id="a5131-133">Event log</span></span>| <span data-ttu-id="a5131-134">설명</span><span class="sxs-lookup"><span data-stu-id="a5131-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="a5131-135">Microsoft-Windows-MBAM/관리자</span><span class="sxs-lookup"><span data-stu-id="a5131-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="a5131-136">오류 메시지 포함</span><span class="sxs-lookup"><span data-stu-id="a5131-136">Contains error messages</span></span>|
|<span data-ttu-id="a5131-137">Microsoft-Windows-MBAM/분석</span><span class="sxs-lookup"><span data-stu-id="a5131-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="a5131-138">고급 로깅 정보 포함</span><span class="sxs-lookup"><span data-stu-id="a5131-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="a5131-139">Microsoft-Windows-MBAM/작동</span><span class="sxs-lookup"><span data-stu-id="a5131-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="a5131-140">성공 메시지 포함</span><span class="sxs-lookup"><span data-stu-id="a5131-140">Contains success messages</span></span>|

### <span data-ttu-id="a5131-141">MBAM 웹 서비스 로그</span><span class="sxs-lookup"><span data-stu-id="a5131-141">MBAM web service logs</span></span>

<span data-ttu-id="a5131-142">각 MBAM 웹 서비스 로그는 SVCLOG 파일에 로깅 정보를 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="a5131-143">기본적으로 각 웹 서비스는 C:\inetpub\Microsoft BitLocker 관리 솔루션 \ 로그 폴더에서 해당 이름을 사용 하는 폴더 아래에 추적 파일을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="a5131-144">서비스 추적 뷰어 도구 (Microsoft Visual Studio의 일부)를 사용 하 여 svclog 추적을 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="a5131-145">암호화 및 보고 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a5131-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="a5131-146">이 섹션에는 서버 기능, 클라이언트 기능, 구성 설정 및 알려진 문제에 대 한 문제 해결 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="a5131-147">MBAM 클라이언트 설치, 그룹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a5131-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="a5131-148">MBAM 에이전트가 클라이언트 컴퓨터에 설치 되어 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="a5131-149">MBAM이 설치 되 면 BitLocker 관리 클라이언트 서비스 라는 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="a5131-150">이 서비스는 자동으로 시작 되도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-150">This service is configured to start automatically.</span></span> <span data-ttu-id="a5131-151">서비스가 실행 중인지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-151">Determine whether the service is running.</span></span>

<span data-ttu-id="a5131-152">MBAM 그룹 정책 설정이 클라이언트 컴퓨터에 적용 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="a5131-153">클라이언트 컴퓨터에 그룹 정책 설정이 적용 된 경우 다음 레지스트리 하위 키가 만들어집니다. **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="a5131-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="a5131-154">이 키가 존재 하며 그룹 정책 설정에 따라 값을 사용 하 여 채워졌는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="a5131-155">초기 지연 기간에는 MBAM 에이전트</span><span class="sxs-lookup"><span data-stu-id="a5131-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="a5131-156">MBAM 클라이언트는 설치 후 바로 작업을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="a5131-157">이 경우 MBAM 에이전트는 해당 작업을 시작 하기 전에 1 ~ 18 분의 초기 임의 지연 시간을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="a5131-158">초기 지연 외에 최소 90 분의 지연이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="a5131-159">지연 시간은 클라이언트 상태를 확인 하는 빈도에 대해 구성 된 그룹 정책 설정에 따라 달라 집니다. 따라서 클라이언트를 시작 하기 전의 총 지연은 *임의 시작 지연*  +  *클라이언트 검사 주파수 지연을 지연*합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="a5131-160">운영 및 관리 이벤트 로그가 비어 있는 경우에는 클라이언트가 작업을 아직 시작 하지 않고 앞에서 설명한 지연 기간에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="a5131-161">지연 되지 않도록 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="a5131-162">BitLocker 관리 클라이언트 서비스 서비스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="a5131-163">**HKEY_LOCAL_MACHINE \software\microsoft\mbam** 레지스트리 하위 키에서 **nostartupdelay** 레지스트리 값을 만들고 해당 형식을 **REG_DWORD**로 설정한 다음 해당 값을 **1**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="a5131-164">**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**에서 **ClientWakeupFrequency** 및 **StatusReportingFrequency** 값을 **1**로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="a5131-165">이러한 값은 컴퓨터에 그룹 정책 업데이트가 있는 경우 원래 설정으로 돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="a5131-166">BitLocker 관리 클라이언트 서비스 서비스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="a5131-167">서비스가 시작 된 후 컴퓨터에 로컬로 로그인 하 고 오류가 없는 경우 1 분 내에 컴퓨터를 암호화 하는 요청을 받아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="a5131-168">요청을 받지 못하는 경우에는 모든 오류 항목에 대 한 MBAM 관리자 로그를 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="a5131-169">컴퓨터에 TPM 장치가 없거나, BIOS에서 TPM 장치를 사용 하도록 설정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="a5131-170">MBAM 관리 이벤트 로그를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="a5131-171">MBAM 관리 이벤트 로그에 다음과 유사한 이벤트 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="a5131-172">TPM 관리 (tpm)를 열고 컴퓨터에 TPM 장치가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="a5131-173">Services.msc에 장치가 표시 되지 않으면 장치 관리자 (devmgmt.msc)를 열고 보안 장치 아래에서 신뢰할 수 있는 플랫폼 모듈을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="a5131-174">신뢰할 수 있는 플랫폼 모듈 장치가 표시 되지 않는 경우에는 다음 이유 중 하나에 해당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="a5131-175">시스템에 TPM/보안 (신뢰할 수 있는 플랫폼 모듈) 장치가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="a5131-176">TPM 장치를 BIOS에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="a5131-177">TPM 장치가 BIOS에서 사용 하도록 설정 되어 있지만 운영 체제 설정에서 TPM 장치 관리를 BIOS에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="a5131-178">TPM 장치에 대 한 Microsoft 드라이버를 사용 하 고 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="a5131-179">장치 관리자에 나열 된 장치를 검토 하 여 Microsoft TPM 장치 드라이버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="a5131-180">TPM 장치에서 C:\Windows\System32\tpm.sys 드라이버를 사용 하 고 있지 않은 경우에는 c \ \ \ \ \ \ \ \ c h i c 파일을 선택 하 여 드라이버를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="a5131-181">컴퓨터에 유효한 시스템 파티션이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="a5131-182">MBAM 관리 이벤트 로그를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="a5131-183">MBAM 관리 이벤트 로그에 다음과 유사한 이벤트 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="a5131-184">BitLocker에는 암호화를 사용 하도록 설정 하는 시스템 파티션이 필요 합니다 ([Windows 7에서 BitLocker 드라이브 암호화: 질문과 대답](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="a5131-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="a5131-185">MBAM은 자동으로 시스템 파티션을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="a5131-186">BitLocker 드라이브 준비 유틸리티 (bdehdcfg.exe)를 사용 하 여 시스템 파티션을 만들고 필요한 시작 파일을 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="a5131-187">예를 들어 드라이브를 암호화 하도록 MBAM을 배포 하기 전에 **% windir% \system32\bdeHdCfg.exe 대상 기본 크기 300 – quiet** 명령을 사용 하 여 드라이브를 자동으로 준비할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="a5131-188">이 경우 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-188">This requires a restart.</span></span> <span data-ttu-id="a5131-189">필요한 경우 작업을 스크립팅할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-189">You can also script the action if this is required.</span></span> <span data-ttu-id="a5131-190">다음 문서는 BitLocker 드라이브 준비 도구에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="a5131-191">BitLocker 드라이브 준비 도구에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="a5131-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="a5131-192">드라이브에 호환 되는 파일 시스템을 설정 하지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="a5131-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="a5131-193">[BitLocker에 대 한 파일 시스템 요구 사항은 TechNet 문서](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="a5131-194">그룹 정책 충돌</span><span class="sxs-lookup"><span data-stu-id="a5131-194">Group Policy conflict</span></span>

<span data-ttu-id="a5131-195">MBAM 관리 이벤트 로그에 다음과 유사한 이벤트 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="a5131-196">그룹 정책 설정을 확인 하 여 MBAM 그룹 정책 설정 간에 충돌 하는 설정이 없는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="a5131-197">BitLocker 드라이브 암호화 템플릿이 아니라 MDOP MBAM 템플릿을 사용 하 여 그룹 정책을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="a5131-198">예:</span><span class="sxs-lookup"><span data-stu-id="a5131-198">For example:</span></span>

<span data-ttu-id="a5131-199">운영 체제 드라이브 암호화 설정에서 TPM을 보호기로 선택 했으며, **시작에 대해 향상 된 Pin 허용**을 선택 했습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="a5131-200">TPM 전용 보호에는 PIN이 필요 하지 않으므로 설정이 충돌 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="a5131-201">따라서 향상 된 Pin 설정을 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="a5131-202">사용자가 예외를 요청 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-202">User may have requested an exemption</span></span>

<span data-ttu-id="a5131-203">컴퓨터 구성 \ 관리 템플릿 \ Components\MDOP MBSAM (BitLocker Management) \Client 관리 \ 사용자 예외 구성 정책 그룹 정책 설정을 사용 하도록 설정한 경우 사용자에 게 예외를 요청할 수 있는 옵션이 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="a5131-204">기본적으로 사용자가 예외를 요청 하는 경우 예외는 7 일 동안 유효 하며,이 기간 동안 사용자가 암호화할 것인지 묻는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="a5131-205">(정책 구성 중에 기본값을 늘리거나 줄일 수 있습니다.) 예외 기간이 끝나면 사용자에 게 암호를 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="a5131-206">컴퓨터가 사용자 예외를 발생 하는 경우 MBAM 관리 이벤트 로그에 다음 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="a5131-207">컴퓨터에 대 한 사용자 예외를 수동으로 다시 정의 하려면 다음 단계를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="a5131-208">다음 레지스트리 하위 키 아래에서 AllowUserExemption 값을 **0** 으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="a5131-209">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="a5131-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="a5131-210">다음 레지스트리 하위 키에서 **Agentversion**, **EncodedComputerName**및 **Installed**를 제외한 모든 레지스트리 값을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="a5131-211">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM</span><span class="sxs-lookup"><span data-stu-id="a5131-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="a5131-212">**참고** 변경 내용이 적용 되려면 MBAM 에이전트를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="a5131-213">컴퓨터에 그룹 정책을 적용 하면 이러한 값이 원래 설정으로 돌아갈 수 있다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="a5131-214">WMI 문제</span><span class="sxs-lookup"><span data-stu-id="a5131-214">WMI issue</span></span>

<span data-ttu-id="a5131-215">MBAM은 win32_encryptablevolume 클래스의 메서드를 사용 하 여 BitLocker를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="a5131-216">이 모듈이 등록 되지 않았거나 손상 된 경우 MBAM 클라이언트가 제대로 작동 하지 않으며 MBAM 관리 이벤트 로그에 다음 이벤트 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="a5131-217">또한 복구 및 하드웨어 정책이 오류 코드 0x8007007e에 적용 되지 않을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="a5131-218">"지정 된 모듈을 찾을 수 없습니다."로 변환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="a5131-219">이 문제를 해결 하려면 다음 명령을 사용 하 여 **win32_encryptablevolume** 클래스를 다시 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="a5131-220">MBAM 통신 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a5131-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="a5131-221">이 섹션에는 MBAM 에이전트 통신과 관련 된 다음과 같은 문제에 대 한 문제 해결 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="a5131-222">잘못 된 MBAM 서비스 URL</span><span class="sxs-lookup"><span data-stu-id="a5131-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="a5131-223">MBAM 준수 상태 서비스 또는 복구 및 하드웨어 서비스 값이 올바르지 않으면 클라이언트 컴퓨터의 MBAM 관리 이벤트 로그에 다음과 유사한 이벤트 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="a5131-224">클라이언트 컴퓨터의 다음 레지스트리 하위 키 아래에서 **KeyRecoveryServiceEndPoint** 및 **StatusReportingServiceEndpoint** 의 값을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="a5131-225">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="a5131-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="a5131-226">기본적으로 KeyRecoveryServiceEndPoint (MBAM 복구 및 하드웨어 서비스 끝점)의 URL은 다음과 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="a5131-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="a5131-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="a5131-228">기본적으로 StatusReportingServiceEndpoint (MBAM Status 보고 서비스 끝점)의 URL은 다음과 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="a5131-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="a5131-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="a5131-230">URL에 공백이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="a5131-231">서비스 URL이 잘못 된 경우 다음 그룹 정책 설정에서 서비스 URL을 수정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="a5131-232">**컴퓨터 구성**  >  **정책**  >  **관리 서식 파일**  >  **Windows 구성 요소**  >  **MDOP MBAM (BitLocker 관리)**  >  **클라이언트 관리**  >  **MBAM 서비스 구성**</span><span class="sxs-lookup"><span data-stu-id="a5131-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="a5131-233">MBAM 관리 서버에 영향을 주는 연결 문제</span><span class="sxs-lookup"><span data-stu-id="a5131-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="a5131-234">클라이언트 에이전트와 MBAM 관리 서버 간에 연결 문제가 있는 경우 MBAM 에이전트에서 데이터베이스에 대 한 업데이트를 게시할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="a5131-235">이 경우 클라이언트 컴퓨터의 MBAM 관리 이벤트 로그에 연결 실패 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="a5131-236">기본 검사:</span><span class="sxs-lookup"><span data-stu-id="a5131-236">Basic checks:</span></span>

* <span data-ttu-id="a5131-237">MBAM 관리 서버를 이름 및 IP로 ping 하 여 기본 연결을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="a5131-238">Telnet 또는 portqry를 사용 하 여 MBAM 관리 웹 사이트 또는 서비스 포트에 연결할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="a5131-239">MBAM 관리 및 모니터링 서버에서 IIS 서비스가 실행 중이 고 MBAM 웹 서비스가 MBAM 클라이언트 컴퓨터 ()에 구성 된 동일한 포트에서 수신 하 고 있는지 확인 `netstat –ano | find "portnumber"` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="a5131-240">MBAM 웹 사이트에 대해 구성 된 포트 번호가 IIS 관리자 (inetmgr)를 사용 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="a5131-241">포트 번호가 클라이언트가 수신 대기 하는 포트 번호와 같은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="a5131-242">다른 응용 프로그램에서 포트 번호를 공유 하 고 있지 않은지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="a5131-243">예를 들어 서버의 다른 응용 프로그램에서 동일한 포트를 사용 하 고 있지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="a5131-244">방화벽이 있는 경우 방화벽 또는 프록시 서버에 포트가 열려 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="a5131-245">클라이언트와 서버 간의 통신이 안전한 경우 유효한 SSL 인증서를 사용 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="a5131-246">웹 서버와 데이터를 삽입 하기 위해 전송 되는 데이터베이스 서버 간의 네트워크 연결을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="a5131-247">ODBC 데이터 원본 관리자를 사용 하 여 웹 서버에서 데이터베이스 서버로의 데이터베이스 연결을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="a5131-248">Sql [Server 데이터베이스 엔진 연결 문제를 해결 하는 방법에 대](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)한 자세한 sql Server 연결 문제 해결 정보를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="a5131-249">연결 문제 해결</span><span class="sxs-lookup"><span data-stu-id="a5131-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="a5131-250">클라이언트에 구성 되어 있는 서비스 URL이 올바른지 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="a5131-251">KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**)에 대 한 URL의 값을 레지스트리에서 복사한 다음 Internet Explorer에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="a5131-252">마찬가지로 StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**)에 대 한 URL의 값을 복사한 다음 Internet Explorer에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="a5131-253">클라이언트 컴퓨터에서 URL을 탐색할 수 없는 경우 클라이언트에서 IIS를 실행 하는 서버로의 기본 네트워크 연결을 테스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="a5131-254">이전 섹션의 포인트 1, 2, 3, 4를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="a5131-255">또한 관리 및 모니터링 서버에서 오류에 대 한 응용 프로그램 로그를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="a5131-256">클라이언트와 서버 간의 동시 네트워크 추적을 만들고 추적을 검토 하 여 클라이언트 에이전트와 MBAM 관리 서버 간의 연결 실패 원인을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="a5131-257">클라이언트 컴퓨터에서 서비스 Url을 탐색할 수 있고, MBAM 관리 이벤트 로그에 연결 오류 항목이 있는 경우 관리 서버와 데이터베이스 서버 간의 연결 오류 때문일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="a5131-258">두 서비스 Url을 성공적으로 탐색할 수 있으며 클라이언트와 실행 중인 서버가 연결 되어 있으면 IIS가 작동 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="a5131-259">그러나 IIS를 실행 하는 서버와 데이터베이스 서버 간에 통신 하는 데 문제가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="a5131-260">네트워크 문제 또는 잘못 된 데이터베이스 연결 문자열 설정으로 인해 MBAM 서비스가 데이터베이스 서버에 연결 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="a5131-261">관리 및 모니터링 서버에서 응용 프로그램 로그를 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="a5131-262">다음 로그 항목과 유사한 원본 ASP.NET 2.0.50727.0의 오류 항목 또는 경고가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="a5131-263">원인</span><span class="sxs-lookup"><span data-stu-id="a5131-263">Possible causes</span></span>

##### <span data-ttu-id="a5131-264">원인 1</span><span class="sxs-lookup"><span data-stu-id="a5131-264">Cause 1</span></span>

<span data-ttu-id="a5131-265">관리자가 관리 및 모니터링 서버 구성 요소를 설치 하는 동안 잘못 된 데이터베이스 인스턴스 이름/데이터베이스 이름을 지정 했을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="a5131-266">IIS 관리 콘솔을 사용 하 여 데이터베이스 연결 문자열을 확인 하 고 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="a5131-267">이렇게 하려면 IIS 관리자를 열고 Microsoft BitLocker 관리 및 모니터링으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="a5131-268">왼쪽에 나열 된 각 서비스에 대해 데이터베이스 연결 문자열을 변경 하려면 다음 단계를 따르세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="a5131-269">**기능 보기**에서 **연결 문자열**을 두 번 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="a5131-270">**연결 문자열** 페이지에서 변경 하려는 연결 문자열을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="a5131-271">**작업** 창에서 **편집**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="a5131-272">**연결 문자열 편집** 대화 상자에서 변경 하려는 속성을 변경 하 고 **확인**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="a5131-273">원인 2</span><span class="sxs-lookup"><span data-stu-id="a5131-273">Cause 2</span></span>

<span data-ttu-id="a5131-274">방화벽에서 SQL Server 포트가 차단 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="a5131-275">SQL Server가 수신 하도록 구성 된 포트 번호를 확인 하 고 관리 서버와 데이터베이스 서버 사이에 방화벽에 포트가 열려 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="a5131-276">원인 3</span><span class="sxs-lookup"><span data-stu-id="a5131-276">Cause 3</span></span>

<span data-ttu-id="a5131-277">SQL server TCP/IP 바인딩이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="a5131-278">데이터베이스 서버의 SQL Server 구성 관리자에서 SQL TCP/IP 바인딩을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="a5131-279">MBAM은 데이터베이스에 연결할 수 있도록 TCP/IP 및 명명 된 파이프 프로토콜을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="a5131-280">원인 4</span><span class="sxs-lookup"><span data-stu-id="a5131-280">Cause 4</span></span>

<span data-ttu-id="a5131-281">NT Authority\Network 서비스 계정 또는 MBAM 관리 서버의 컴퓨터 계정에는 SQL 데이터베이스에 연결 하는 데 필요한 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="a5131-282">데이터베이스 서버에 데이터베이스 구성 요소를 설치 하는 동안 설치 관리자는 MBAM 준수 감사 DB 액세스와 MBAM 복구 및 하드웨어 DB 액세스를 사용 하 여 두 개의 로컬 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="a5131-283">NT Authority\Network 서비스 계정, MBAM 관리 서버의 컴퓨터 계정, 그리고 데이터베이스 구성 요소를 설치 하는 사용자가 이러한 그룹에 자동으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="a5131-284">이러한 그룹에는 설치 중에 데이터베이스에 대해 필요한 권한이 부여 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="a5131-285">이 그룹에 속하는 모든 사용자는 데이터베이스에 대해 필요한 사용 권한을 자동으로 받습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="a5131-286">다음 조건 중 하나 이상에 해당 하는 경우 사용 권한 문제로 인해 웹 서비스가 데이터베이스 서버에 연결 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="a5131-287">앞에서 언급 한 그룹은 데이터베이스 서버의 로컬 그룹에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="a5131-288">NT Authority\Network 서비스 계정 및 MBAM 관리 서버의 컴퓨터 계정은 이러한 그룹의 구성원이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="a5131-289">이러한 그룹에는 데이터베이스에 대해 필요한 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="a5131-290">이전 조건 중 하나라도 충족 되는 경우 MBAM 관리 및 모니터링 서버의 응용 프로그램 로그에 사용 권한 관련 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="a5131-291">이 경우 NT Authority\Network 서비스 계정 및 MBAM 관리 서버의 컴퓨터 계정을 수동으로 추가 하 고 SQL Server Management Studio ()를 사용 하는 SQL 데이터베이스 서버에서 서버 차원의 공용 역할을 부여 해야 합니다 https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a5131-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="a5131-292">웹 서비스 로그 검토</span><span class="sxs-lookup"><span data-stu-id="a5131-292">Review the web service logs</span></span>

<span data-ttu-id="a5131-293">MBAM 관리 서버의 응용 프로그램 로그에 이벤트가 기록 되어 있지 않으면 MBAM 관리 및 모니터링 서버에서 호스트 되는 MBAM 웹 서비스의 웹 서비스 로그 (svclog)를 검토 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="a5131-294">로그 파일을 보려면 서비스 추적 뷰어 도구 (SvcTraceViewer.exe)를 사용 해야 https://msdn.microsoft.com/library/ms732023.aspx 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="a5131-295">RecoveryandHardwareService 및 ComplianceStatusService의 서비스 추적 로그를 주로 조사 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="a5131-296">기본적으로 웹 서비스 로그는 C:\inetpub\Microsoft BitLocker 관리 솔루션 \ 로그 폴더에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="a5131-297">각 서비스는 자신의 폴더 아래에 svclog 파일을 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="a5131-298">오류 또는 경고 항목에 대 한 서비스 추적 로그의 활동을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="a5131-299">기본적으로 오류 항목은 빨간색으로 강조 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="a5131-300">추적 뷰어의 오른쪽 창에 있는 오류 설명을 선택 하 여 오류 항목에 대 한 자세한 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="a5131-301">다음은 추적 로그의 샘플 오류 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="a5131-302">MBAM 인프라 다시 설치 또는 재구성</span><span class="sxs-lookup"><span data-stu-id="a5131-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="a5131-303">MBAM 인프라를 다시 설치 하거나 다시 구성 하려면 다음 사항을 알아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="a5131-304">응용 프로그램 풀 계정</span><span class="sxs-lookup"><span data-stu-id="a5131-304">Application Pool account</span></span>

* <span data-ttu-id="a5131-305">MBAM 그룹 (헬프데스크, 고급, 보고서 사용자 그룹)</span><span class="sxs-lookup"><span data-stu-id="a5131-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="a5131-306">MBAM 보고서 URL</span><span class="sxs-lookup"><span data-stu-id="a5131-306">MBAM Reports URL</span></span>

* <span data-ttu-id="a5131-307">SQL Server 이름 및 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="a5131-307">SQL Server name and database names</span></span>

* <span data-ttu-id="a5131-308">MBAM ReadWrite 및 ReadOnly 계정</span><span class="sxs-lookup"><span data-stu-id="a5131-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="a5131-309">응용 프로그램 풀 계정</span><span class="sxs-lookup"><span data-stu-id="a5131-309">Application Pool account</span></span>

<span data-ttu-id="a5131-310">응용 프로그램 풀 계정을 찾으려면 MBAM 웹 서버에 로그온 하 고 **IIS (인터넷 정보 서비스) 관리자**를 연 다음 **응용 프로그램 풀**을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![응용 프로그램 풀](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="a5131-312">이 계정에 SPN (서비스 사용자 이름)을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="a5131-313">이 설정은 MBAM의 기능에 매우 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="a5131-314">MBAM 그룹 (헬프데스크, 고급, 보고서 사용자 그룹 및 보고서 URL)</span><span class="sxs-lookup"><span data-stu-id="a5131-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![MBAM 그룹](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="a5131-316">헬프 데스크 그룹, 고급 헬프데스크 그룹, 보고서 사용자 그룹, MBAM 보고서 URL 등의 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="a5131-317">MBAM 보고서 URL은 MBAM 설정에서 제공 해야 하 고 http (s)://servername/ReportServer.로 읽어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="a5131-318">SQL Server 이름 및 데이터베이스 (DB) 이름</span><span class="sxs-lookup"><span data-stu-id="a5131-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="a5131-319">MBAM을 호스트 하는 SQL Server 이름 및 인스턴스를 찾으려면 MBAM 웹 (IIS) 서버에 로그온 하 고 folowing registry 하위 키를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="a5131-320">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web</span><span class="sxs-lookup"><span data-stu-id="a5131-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![차례로](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="a5131-322">강조 표시 된 부분은 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="a5131-323">여기에는 SQL Server 이름, 데이터베이스 이름 및 인스턴스 (명명 된 경우)가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="a5131-324">MBAM ReadWrite 및 ReadOnly 계정</span><span class="sxs-lookup"><span data-stu-id="a5131-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="a5131-325">이 정보는 SQL Server 데이터베이스에 있으며, 이미 웹 서버에서 해당 이름을 찾았습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="a5131-326">ReadWrite 계정</span><span class="sxs-lookup"><span data-stu-id="a5131-326">ReadWrite account</span></span>

1. <span data-ttu-id="a5131-327">SQL Management Studio에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="a5131-328">**Mbam 복구 및 하드웨어**를 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **사용 권한을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="a5131-329">예를 들어 랩 계정 이름은 **Mbamwrite**입니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="a5131-330">응용 프로그램 풀 및 ReadWrite 계정이 동일 하 게 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![DB 속성](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="a5131-333">SQL Management Studio에서 **보안** 을 탐색 한 다음 **로그인** 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="a5131-334">이전 스크린샷에 표시 된 계정으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-334">Browse to the account shown in the previous screenshot.</span></span>

![SQL 보안](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="a5131-336">계정을 마우스 오른쪽 단추로 클릭 하 고 **속성 사용자 매핑으로**이동한 다음 Mbam 복구 및 하드웨어 데이터베이스를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![사용자 매핑](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="a5131-338">읽기 전용 계정</span><span class="sxs-lookup"><span data-stu-id="a5131-338">ReadOnly account</span></span>

<span data-ttu-id="a5131-339">SSRS 서버에서 SQL Server Reporting Services 구성 관리자를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="a5131-340">**보고서 관리자 URL**을 선택한 다음 **url**을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![보고서 관리자](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="a5131-342">**Microsoft Bitlocker 관리 및 모니터링**선택:</span><span class="sxs-lookup"><span data-stu-id="a5131-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![Bitlocker 관리 및 모니터링](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="a5131-344">**MaltaDatasource**선택:</span><span class="sxs-lookup"><span data-stu-id="a5131-344">Select **MaltaDatasource**:</span></span>

![운영할](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="a5131-347">MaltaDataSource는 읽기 전용 계정 이름을 포함 해야 하며 MBAM 설정에 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5131-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="a5131-348">참고자료</span><span class="sxs-lookup"><span data-stu-id="a5131-348">Reference</span></span>

<span data-ttu-id="a5131-349">자세한 내용은 다음 문서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a5131-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="a5131-350">독립 실행형 구성에서 MBAM 2.5 배포</span><span class="sxs-lookup"><span data-stu-id="a5131-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="a5131-351">Microsoft BitLocker 관리 및 모니터링 2.5</span><span class="sxs-lookup"><span data-stu-id="a5131-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
