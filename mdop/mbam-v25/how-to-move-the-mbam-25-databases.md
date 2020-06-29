---
title: MBAM 2.5 데이터베이스를 이동하는 방법
description: MBAM 2.5 데이터베이스를 이동하는 방법
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812401"
---
# <span data-ttu-id="f530c-103">MBAM 2.5 데이터베이스를 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="f530c-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="f530c-104">다음 절차를 사용 하 여 다음 데이터베이스를 한 컴퓨터에서 다른 컴퓨터로 이동 합니다. 서버 A에서 서버 B까지, 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="f530c-105">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f530c-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="f530c-106">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f530c-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="f530c-107">MBAM 구성 마법사를 실행 하기 전에 데이터베이스를 시스템 B로 복원 하 여 업데이트/구성 하는 것이 중요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="f530c-108">데이터베이스가 없으면 구성 마법사가 비어 있는 새 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="f530c-109">기존 데이터베이스가 복원 되 면이 프로세스는 MBAM 구성을 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="f530c-110">먼저 데이터베이스를 복원한 다음 MBAM 구성 마법사를 실행 하 고 데이터베이스 옵션을 선택 하면 구성 마법사가 복원한 데이터베이스에 "연결" 됩니다. 프로세스의 일부로 필요한 경우 업그레이드</span><span class="sxs-lookup"><span data-stu-id="f530c-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="f530c-111">여러 기능을 이동 하는 경우 다음 순서 대로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="f530c-112">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f530c-112">Recovery Database</span></span>

2.  <span data-ttu-id="f530c-113">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="f530c-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="f530c-114">보고</span><span class="sxs-lookup"><span data-stu-id="f530c-114">Reports</span></span>

4.  <span data-ttu-id="f530c-115">관리 및 모니터링 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="f530c-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="f530c-116">셀프 서비스 포털</span><span class="sxs-lookup"><span data-stu-id="f530c-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="f530c-117">이 항목에서 제공 하는 예제 Windows PowerShell 스크립트를 실행 하려면 스크립트를 실행할 수 있도록 Windows PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="f530c-118">자세한 내용은 [Windows PowerShell 스크립트 실행](https://technet.microsoft.com/library/ee176949.aspx) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f530c-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="f530c-119">복구 데이터베이스 이동</span><span class="sxs-lookup"><span data-stu-id="f530c-119">Move the Recovery Database</span></span>

<span data-ttu-id="f530c-120">복구 데이터베이스 이동에 대 한 상위 수준 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="f530c-121">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="f530c-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="f530c-122">서버 A의 복구 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="f530c-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="f530c-123">복구 데이터베이스를 서버 A에서 서버 B로 이동</span><span class="sxs-lookup"><span data-stu-id="f530c-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="f530c-124">서버 B에서 복구 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="f530c-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="f530c-125">서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="f530c-126">MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행</span><span class="sxs-lookup"><span data-stu-id="f530c-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="f530c-127">관리 및 모니터링 웹 사이트 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f530c-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="f530c-128">복구 데이터베이스를 이동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f530c-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="f530c-129">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="f530c-130">MBAM 관리 및 모니터링 서버 웹 사이트를 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="f530c-131">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="f530c-132">이 명령을 실행 하려면 windows powershell 용 IIS (인터넷 정보 서비스) 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="f530c-133">서버 A의 복구 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="f530c-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="f530c-134">SQL Server Management Studio의 **백업** 작업을 사용 하 여 서버 A의 복구 데이터베이스를 백업 합니다.  기본적으로 데이터베이스 이름은 **Mbam 복구 데이터베이스**입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="f530c-135">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만들고, 모든 복구 모드를 사용 하도록 MBAM 복구 데이터베이스를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

3.  <span data-ttu-id="f530c-136">다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="f530c-137">**$PASSWORD $** -개인 키 파일을 암호화 하는 데 사용 하는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="f530c-138">Windows PowerShell에서 다음 예와 유사 하 게 파일에 저장 된 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="f530c-139">다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="f530c-140">**$SERVERNAME $ \ $SQLINSTANCENAME $** -복구 데이터베이스가 백업 되는 서버 이름 및 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="f530c-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="f530c-141">복구 데이터베이스를 서버 A에서 서버 B로 이동</span><span class="sxs-lookup"><span data-stu-id="f530c-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="f530c-142">Windows 탐색기를 사용 하 여 **Mbam 복구 데이터베이스 데이터 .bak** 파일을 서버 a에서 서버 B로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="f530c-143">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="f530c-144">다음 표의 정보를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="f530c-145">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f530c-145">Parameter</span></span>**        | **<span data-ttu-id="f530c-146">설명</span><span class="sxs-lookup"><span data-stu-id="f530c-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="f530c-147">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="f530c-147">$SERVERNAME$</span></span>       | <span data-ttu-id="f530c-148">파일이 복사 되는 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="f530c-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="f530c-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="f530c-150">파일이 복사 되는 공유 및 경로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="f530c-151">서버 B에서 복구 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="f530c-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="f530c-152">SQL Server Management Studio에서 **데이터베이스 복원** 작업을 사용 하 여 서버 B의 복구 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="f530c-153">이전 작업이 완료 되 면 **장치에서**를 선택한 다음 데이터베이스 백업 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="f530c-154">**추가** 명령을 사용 하 여 **Mbam 복구 데이터베이스 데이터 .bak** 파일을 선택 하 고 **확인** 을 클릭 하 여 복원 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="f530c-155">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

    FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

    DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

    FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

    WITH REPLACE
    ```

5.  <span data-ttu-id="f530c-156">다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="f530c-157">**$PASSWORD $** -개인 키 파일을 암호화 하는 데 사용 하는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="f530c-158">Windows PowerShell에서 다음 예와 유사 하 게 파일에 저장 된 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="f530c-159">다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="f530c-160">**$SERVERNAME $ \ $SQLINSTANCENAME $** -복구 데이터베이스가 복원 될 서버 이름 및 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="f530c-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="f530c-161">서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="f530c-162">복원 된 데이터베이스에서 복구 데이터베이스 액세스를 사용 하도록 설정 하는 Microsoft SQL Server 사용자 로그인이 구성 프로세스 중에 제공한 액세스 계정에 매핑 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="f530c-163">로그인이 동일 하지 않으면 SQL Server Management Studio를 사용 하 여 로그인을 만들고 기존 데이터베이스 사용자에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="f530c-164">관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 MBAM 웹 사이트의 연결 문자열 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="f530c-165">다음 레지스트리 키를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="f530c-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="f530c-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="f530c-167">복구 데이터베이스가 이동 된 서버 및 인스턴스 이름 (예: \ $SERVERNAME \ $ \\ \ $SQLINSTANCENAME)으로 **데이터 원본** 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="f530c-168">복구 된 데이터베이스 이름으로 **초기 카탈로그** 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="f530c-169">이 프로세스를 자동화 하려면 Windows PowerShell 명령 프롬프트를 사용 하 여 관리 및 모니터링 서버에 다음과 유사한 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   ><span data-ttu-id="f530c-170">이 연결 문자열은 모든 로컬 MBAM 웹 응용 프로그램에서 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="f530c-171">따라서 서버 당 한 번만 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="f530c-172">다음 표를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="f530c-173">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f530c-173">Parameter</span></span>|<span data-ttu-id="f530c-174">설명</span><span class="sxs-lookup"><span data-stu-id="f530c-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="f530c-175">$SERVERNAME $/\ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="f530c-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="f530c-176">복구 데이터베이스가 있는 SQL Server의 서버 이름 및 인스턴스</span><span class="sxs-lookup"><span data-stu-id="f530c-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="f530c-177">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="f530c-177">$DATABASE$</span></span>|<span data-ttu-id="f530c-178">복구 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="f530c-179">MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행</span><span class="sxs-lookup"><span data-stu-id="f530c-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="f530c-180">서버 B에 MBAM 2.5 서버 소프트웨어를 설치 합니다. 자세한 내용은 [MBAM 2.5 서버 소프트웨어 설치](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f530c-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="f530c-181">서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **복구 데이터베이스** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="f530c-182">데이터베이스를 구성 하는 방법에 대 한 자세한 내용은 [MBAM 2.5 데이터베이스를 구성](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f530c-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="f530c-183">또는 **Enable-MbamDatabase** Windows PowerShell cmdlet을 사용 하 여 복구 데이터베이스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="f530c-184">관리 및 모니터링 웹 사이트 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f530c-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="f530c-185">관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="f530c-186">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="f530c-187">이 명령을 실행 하려면 windows powershell 용 IIS 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="f530c-188">준수 및 감사 데이터베이스 이동</span><span class="sxs-lookup"><span data-stu-id="f530c-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="f530c-189">준수 및 감사 데이터베이스 이동에 대 한 상위 수준 단계는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="f530c-190">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="f530c-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="f530c-191">서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="f530c-192">서버 A에서 서버 B로 규정 준수 및 감사 데이터베이스 이동</span><span class="sxs-lookup"><span data-stu-id="f530c-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="f530c-193">서버 B에서 규정 준수 및 감사 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="f530c-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="f530c-194">서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="f530c-195">MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행</span><span class="sxs-lookup"><span data-stu-id="f530c-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="f530c-196">관리 및 모니터링 웹 사이트 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f530c-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="f530c-197">준수 및 감사 데이터베이스를 이동 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f530c-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="f530c-198">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="f530c-199">MBAM 관리 및 모니터링 서버 웹 사이트를 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="f530c-200">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="f530c-201">이 명령을 실행 하려면 windows powershell 용 IIS (인터넷 정보 서비스) 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="f530c-202">서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="f530c-203">SQL Server Management Studio의 **백업** 작업을 사용 하 여 서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다. 기본적으로 데이터베이스 이름은 **Mbam 준수 상태 데이터베이스**입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="f530c-204">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

    SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  <span data-ttu-id="f530c-205">다음과 유사한 Windows PowerShell 명령을 사용 하 여 .sql 파일에 저장 된 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="f530c-206">다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="f530c-207">**$SERVERNAME $ \ $SQLINSTANCENAME $** -규정 준수 및 감사 데이터베이스가 백업 되는 서버 이름과 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="f530c-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="f530c-208">준수 및 감사 데이터베이스를 서버 A에서 서버 B로 이동 \* \*</span><span class="sxs-lookup"><span data-stu-id="f530c-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="f530c-209">Windows 탐색기를 사용 하 여 **Mbam 준수 상태 데이터베이스 데이터 .bak** 파일을 서버 A에서 서버 B로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="f530c-210">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="f530c-211">다음 표를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="f530c-212">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f530c-212">Parameter</span></span>**        | **<span data-ttu-id="f530c-213">설명</span><span class="sxs-lookup"><span data-stu-id="f530c-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="f530c-214">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="f530c-214">$SERVERNAME$</span></span>       | <span data-ttu-id="f530c-215">파일이 복사 되는 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="f530c-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="f530c-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="f530c-217">파일이 복사 되는 공유 및 경로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="f530c-218">서버 B에서 규정 준수 및 감사 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="f530c-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="f530c-219">SQL Server Management Studio에서 **데이터베이스 복원** 작업을 사용 하 여 서버 B의 규정 준수 및 감사 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="f530c-220">이전 작업이 완료 되 면 **장치에서**를 선택한 다음 데이터베이스 백업 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="f530c-221">**추가** 명령을 사용 하 여 **Mbam 준수 상태 데이터베이스 데이터 .bak** 파일을 선택 하 고 **확인** 을 클릭 하 여 복원 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="f530c-222">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="f530c-223">Windows PowerShell에서 다음 예와 유사 하 게 파일에 저장 된 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="f530c-224">다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="f530c-225">**$SERVERNAME $ \ $SQLINSTANCENAME $** -준수 및 감사 데이터베이스가 복원 될 서버 이름과 인스턴스.</span><span class="sxs-lookup"><span data-stu-id="f530c-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="f530c-226">서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="f530c-227">복원 된 데이터베이스에서 준수 및 감사 데이터베이스 액세스를 사용 하도록 설정 하는 Microsoft SQL Server 사용자 로그인이 구성 프로세스 중에 제공한 액세스 계정에 매핑 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="f530c-228">로그인이 동일 하지 않으면 SQL Server Management Studio를 사용 하 여 로그인을 만들고 기존 데이터베이스 사용자에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="f530c-229">관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 웹 사이트에 대 한 연결 문자열 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="f530c-230">다음 레지스트리 키를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="f530c-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="f530c-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="f530c-232">복구 데이터베이스가 이동 된 서버 및 인스턴스 이름 (예: \ $SERVERNAME \ $ \\ \ $SQLINSTANCENAME)으로 **데이터 원본** 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="f530c-233">복구 된 데이터베이스 이름으로 **초기 카탈로그** 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="f530c-234">이 프로세스를 자동화 하려면 Windows PowerShell 명령 프롬프트를 사용 하 여 관리 및 모니터링 서버에 다음과 유사한 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="f530c-235">이 연결 문자열은 모든 로컬 MBAM 웹 응용 프로그램에서 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="f530c-236">따라서 서버 당 한 번만 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="f530c-237">다음 표를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="f530c-238">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f530c-238">Parameter</span></span> | <span data-ttu-id="f530c-239">설명</span><span class="sxs-lookup"><span data-stu-id="f530c-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="f530c-240">$SERVERNAME $ \ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="f530c-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="f530c-241">복구 데이터베이스가 있는 SQL Server의 서버 이름 및 인스턴스</span><span class="sxs-lookup"><span data-stu-id="f530c-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="f530c-242">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="f530c-242">$DATABASE$</span></span>|<span data-ttu-id="f530c-243">복구 된 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="f530c-244">MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행</span><span class="sxs-lookup"><span data-stu-id="f530c-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="f530c-245">서버 B에 MBAM 2.5 서버 소프트웨어를 설치 합니다. 자세한 내용은 [MBAM 2.5 서버 소프트웨어 설치](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f530c-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="f530c-246">서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **준수 및 감사 데이터베이스** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="f530c-247">데이터베이스를 구성 하는 방법에 대 한 자세한 내용은 [MBAM 2.5 데이터베이스를 구성](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)하는 방법을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f530c-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="f530c-248">또는 **사용-MbamDatabase** Windows PowerShell cmdlet을 사용 하 여 규정 준수 및 감사 데이터베이스를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="f530c-249">관리 및 모니터링 웹 사이트 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f530c-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="f530c-250">관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="f530c-251">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="f530c-252">이 명령을 실행 하려면 windows powershell 용 IIS 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f530c-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
