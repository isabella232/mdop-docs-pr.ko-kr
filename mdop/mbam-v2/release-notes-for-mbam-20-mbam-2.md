---
title: MBAM 2.0 릴리스 정보
description: MBAM 2.0 릴리스 정보
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825588"
---
# <span data-ttu-id="b9bc1-103">MBAM 2.0 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="b9bc1-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="b9bc1-104">이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="b9bc1-105">Microsoft BitLockerAdministration 및 모니터링 (MBAM) 2.0을 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="b9bc1-106">이 릴리스 정보에는 Bits Locker관리 및 모니터링 2.0을 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="b9bc1-107">이러한 릴리스 정보와 다른 MBAM 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="b9bc1-108">이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="b9bc1-109">MBAM 2.0 알려진 문제</span><span class="sxs-lookup"><span data-stu-id="b9bc1-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="b9bc1-110">이 섹션에서는 MBAM 2.0에 대 한 릴리스 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="b9bc1-111">Microsoft System Center Configuration Manager 2007에서 MBAM을 실행할 때 BitLocker 컴퓨터 준수 및 BitLocker 엔터프라이즈 준수 세부 정보 보고서에 컴퓨터 이름 필드가 표시 되지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="b9bc1-112">컴퓨터 이름 필드는 구성 관리자 2007에서 MBAM을 사용할 때 BitLocker 컴퓨터 규정 준수 및 BitLocker 엔터프라이즈 준수 세부 정보 보고서에서 비어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="b9bc1-113">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="b9bc1-114">독립 실행형 MBAM 서버 인프라를 업그레이드 한 후 엔터프라이즈 호환 보고서가 업데이트 되지 않음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="b9bc1-115">MBAM 독립 실행형 토폴로지를 사용 하는 경우 서버 인프라를 버전 1.0에서 2.0로 업그레이드 하면 엔터프라이즈 준수 보고서가 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="b9bc1-116">해결 방법: 업그레이드 한 후 준수 및 감사 데이터베이스에서 다음 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### <span data-ttu-id="b9bc1-117">SSL이 SSRS에 구성 되어 있지 않은 경우 지원 센터 포털의 보고서에 경고가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="b9bc1-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="b9bc1-118">SQL Server Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 설치할 때 보고서에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="b9bc1-119">그런 다음 지원 센터 포털로 이동한 다음 보고서를 선택 하면 "보안 콘텐츠만 표시 됨" 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="b9bc1-120">해결 방법: 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="b9bc1-121">이 문제를 해결 하려면 SQL Server Reporting Services가 설치 되어 있는 MBAM 컴퓨터로 이동 하 여 **Reporting Services 구성 관리자**를 실행 한 다음 **웹 서비스 URL**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="b9bc1-122">서버에 대 한 적절 한 SSL 인증서를 선택 하 고 적절 한 SSL 포트 (기본 포트 443)를 입력 한 다음 **적용**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="b9bc1-123">Configuration Manager 데이터베이스의 기본 인스턴스가 아닌 인스턴스는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="b9bc1-124">MBAM은 Configuration Manager 2007 및 SystemCenter2012 ConfigurationManager에서 Configuration Manager 데이터베이스의 기본 인스턴스만 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="b9bc1-125">비기본 인스턴스를 사용 하는 경우 MBAM을 설치할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="b9bc1-126">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="b9bc1-127">준수 요약 보고서에서 "뒤로"를 클릭 하면 오류가 발생 하는 경우</span><span class="sxs-lookup"><span data-stu-id="b9bc1-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="b9bc1-128">준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="b9bc1-129">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="b9bc1-130">사용 된 공간만 암호화가 올바르게 작동 하지 않음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="b9bc1-131">MBAM 클라이언트를 설치한 후 처음으로 컴퓨터를 암호화 하 고 사용 된 공간만 암호화를 구현 하도록 그룹 정책 개체를 설정한 경우, MBAM이 디스크의 사용 된 공간만 암호화 하는 대신 전체 디스크를 잘못 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="b9bc1-132">MBAM 클라이언트를 설치할 때 컴퓨터가 이미 암호화 되어 있고 동일한 그룹 정책 개체를 설정한 경우 암호화가 올바르게 작동 하 고 컴퓨터에서 사용 된 디스크 공간만 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="b9bc1-133">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="b9bc1-134">컴퓨터 준수 보고서에서 암호화 강도가 잘못 표시 됨</span><span class="sxs-lookup"><span data-stu-id="b9bc1-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="b9bc1-135">**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 수준을 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 컴퓨터 준수 보고서에 항상 암호화 강도로 "unknown"이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="b9bc1-136">그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="b9bc1-137">해결 방법: **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="b9bc1-138">드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨</span><span class="sxs-lookup"><span data-stu-id="b9bc1-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="b9bc1-139">SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="b9bc1-140">해결 방법: 없음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-140">WORKAROUND: None.</span></span> <span data-ttu-id="b9bc1-141">MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="b9bc1-142">보안 강화 구성으로 인해 보고서가 올바르게 표시 되지 않을 수 있음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="b9bc1-143">Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 메시지가 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="b9bc1-144">웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 기본적으로 ESC가 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="b9bc1-145">해결 방법: MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 메시지가 나타나는 경우 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="b9bc1-146">또는 ESC가 설정 되지 않은 다른 컴퓨터에서 보고서를 볼 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="b9bc1-147">SQL Server 2008에서 SQL Server 2012로 업그레이드할 때 MBAM 서버 설치가 실패 함</span><span class="sxs-lookup"><span data-stu-id="b9bc1-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="b9bc1-148">SQL Server 2008에서 SQL Server 2012으로 업그레이드 한 다음 준수 및 감사 데이터베이스 또는 복구 데이터베이스를 설치 하려고 하면 설치가 실패 하 고 롤백됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="b9bc1-149">SQL 업그레이드 중 필요한 SQLCMD.exe 파일이 제거 되었고 MBAM 설치 관리자에서 찾을 수 없기 때문에 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="b9bc1-150">MSI 로그 파일 줄은 다음과 유사 하 게 표시 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="b9bc1-151">RunDbInstallScript Recovery Db CA: BinDir E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exe-RunDbInstallScript 복구 Db CA: dbInstance-xxxxxx\\I01RunDbInstallScript 복구 Db CA: sqlScript-C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript 복구 Db CA: defaultFileName-MBAM \ _Recovery \ _and 복구 Db CA: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery Db CA: 복구 데이터베이스 설치 scriptRunDbInstallScript 복구 Db CA를 실행 하는 중: Sqlcmd 로그 파일이 C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript 복구 Db CA 예외: 설치 복구 데이터베이스 사용자 지정 작업 명령 명령줄 출력 예외: 시스템에서 지정 된 파일을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="b9bc1-152">MBAM 서버 Windows Installer는 HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. 레지스트리에서 Path 문자열 값을 찾아 SQLCMD.exe 경로를 찾기 위해 하드 코드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="b9bc1-153">Sql Server 2008에서 SQL Server 2012로 마이그레이션하는 동안 키가 계속 표시 되지만, SQL 업그레이드 프로세스에서 해당 파일을 제거 했으므로 데이터 값이 참조 하는 경로에 SQLCMD.exe 파일이 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="b9bc1-154">해결 방법: HKLM\\Software\\Microsoft\\Microsoft SQL Server\\1000tool\clientsetup 경로 문자열 값을 **Path \ _old**로 바꾼 다음 Mbam Server Windows Installer를 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="b9bc1-155">설치가 성공적으로 완료 되 고 SQL Server 2012에서 데이터베이스를 만드는 경우 **경로 \ _old** 값을 **path**로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="b9bc1-156">MBAM 2.0 용 핫픽스와 기술 자료 문서</span><span class="sxs-lookup"><span data-stu-id="b9bc1-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="b9bc1-157">이 섹션에는 MBAM 2.0 용 핫픽스와 KB에 대 한 문서가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="b9bc1-158">기술 자료 문서</span><span class="sxs-lookup"><span data-stu-id="b9bc1-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="b9bc1-159">제목</span><span class="sxs-lookup"><span data-stu-id="b9bc1-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="b9bc1-160">Link</span><span class="sxs-lookup"><span data-stu-id="b9bc1-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-161">2831166</span><span class="sxs-lookup"><span data-stu-id="b9bc1-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-162">&quot;System CENTER CM 개체가 이미 설치 된 상태에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 설치 실패&quot;</span><span class="sxs-lookup"><span data-stu-id="b9bc1-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="b9bc1-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-164">2870849</span><span class="sxs-lookup"><span data-stu-id="b9bc1-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-165">사용자가 MBAM 2.0 셀프 서비스 포털을 사용 하 여 BitLocker 복구 키를 검색할 수 없음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="b9bc1-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-167">2756402</span><span class="sxs-lookup"><span data-stu-id="b9bc1-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-168">MBAM 클라이언트가 이벤트 ID 4 및 오류 코드 0x8004100E와 함께 실패 함 이벤트 설명</span><span class="sxs-lookup"><span data-stu-id="b9bc1-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="b9bc1-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-170">2620287</span><span class="sxs-lookup"><span data-stu-id="b9bc1-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-171">MBAM에서 보고서 탭을 클릭 하면 "/Reports ' 응용 프로그램에서 오류 메시지" 서버 오류 발생 "</span><span class="sxs-lookup"><span data-stu-id="b9bc1-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="b9bc1-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-173">2639518</span><span class="sxs-lookup"><span data-stu-id="b9bc1-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-174">MBAM 엔터프라이즈 또는 컴퓨터 준수 보고서 열기 오류</span><span class="sxs-lookup"><span data-stu-id="b9bc1-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="b9bc1-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-176">2620269</span><span class="sxs-lookup"><span data-stu-id="b9bc1-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-177">MBAM Enterprise 보고서가 업데이트 되지 않음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="b9bc1-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-179">2712461</span><span class="sxs-lookup"><span data-stu-id="b9bc1-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-180">도메인 컨트롤러에 MBAM을 설치 하는 것은 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="b9bc1-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-182">2876732</span><span class="sxs-lookup"><span data-stu-id="b9bc1-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-183">MBAM 2.0의 독립 실행형 또는 Configuration Manager 통합 설정 중에 오류 코드 0x80071a90이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="b9bc1-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-185">2754259</span><span class="sxs-lookup"><span data-stu-id="b9bc1-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-186">MBAM 및 보안 네트워크 통신</span><span class="sxs-lookup"><span data-stu-id="b9bc1-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="b9bc1-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-188">2870842</span><span class="sxs-lookup"><span data-stu-id="b9bc1-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-189">Configuration Manager 통합 시나리오에서 SQL Server 2008와 함께 MBAM 2.0 설치가 실패 함</span><span class="sxs-lookup"><span data-stu-id="b9bc1-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="b9bc1-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-191">2668533</span><span class="sxs-lookup"><span data-stu-id="b9bc1-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-192">SQL SSRS가 올바르게 구성 되어 있지 않으면 MBAM이 실패 함</span><span class="sxs-lookup"><span data-stu-id="b9bc1-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="b9bc1-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-194">2870847</span><span class="sxs-lookup"><span data-stu-id="b9bc1-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-195">MBAM 2.0 &quot; &#39;Reporting Services 가리키기&#39; 역할에 대 한 Configuration Manager 서버 역할 설정을 검색 하는 동안 오류가 발생 하 여 설치에 실패 함&quot;</span><span class="sxs-lookup"><span data-stu-id="b9bc1-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="b9bc1-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-197">2870839</span><span class="sxs-lookup"><span data-stu-id="b9bc1-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-198">MBAM 2.0 Enterprise Reports는 SQL 작업 CreateCache 오류로 인해 MBAM 2.0 독립 실행형 토폴로지에서 새로 고쳐지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bc1-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="b9bc1-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-200">2620269</span><span class="sxs-lookup"><span data-stu-id="b9bc1-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-201">MBAM Enterprise 보고서가 업데이트 되지 않음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="b9bc1-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9bc1-203">2935997</span><span class="sxs-lookup"><span data-stu-id="b9bc1-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-204">MBAM 지원 컴퓨터 규정 준수 보고에 지원 되지 않는 제품이 포함 되어 있지 않음</span><span class="sxs-lookup"><span data-stu-id="b9bc1-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="b9bc1-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9bc1-206">2612822</span><span class="sxs-lookup"><span data-stu-id="b9bc1-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9bc1-207">컴퓨터 레코드가 MBAM에서 거부 됨</span><span class="sxs-lookup"><span data-stu-id="b9bc1-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="b9bc1-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="b9bc1-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b9bc1-209">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b9bc1-209">Related topics</span></span>


[<span data-ttu-id="b9bc1-210">MBAM 2.0 정보</span><span class="sxs-lookup"><span data-stu-id="b9bc1-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 





