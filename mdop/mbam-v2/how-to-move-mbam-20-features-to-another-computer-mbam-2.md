---
title: MBAM 2.0 기능을 다른 컴퓨터로 이동하는 방법
description: MBAM 2.0 기능을 다른 컴퓨터로 이동하는 방법
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825078"
---
# <span data-ttu-id="c6349-103">MBAM 2.0 기능을 다른 컴퓨터로 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="c6349-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="c6349-104">이 항목에서는 하나 이상의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능을 다른 컴퓨터로 이동 하는 데 필요한 단계에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="c6349-105">두 개 이상의 Microsoft BitLocker 관리 및 모니터링 기능을 이동 하는 경우 다음 순서로 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="c6349-106">복구 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c6349-106">Recovery Database</span></span>

2.  <span data-ttu-id="c6349-107">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c6349-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="c6349-108">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="c6349-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="c6349-109">관리 및 모니터링</span><span class="sxs-lookup"><span data-stu-id="c6349-109">Administration and Monitoring</span></span>

## <span data-ttu-id="c6349-110">복구 데이터베이스 이동</span><span class="sxs-lookup"><span data-stu-id="c6349-110">Moving the Recovery Database</span></span>


<span data-ttu-id="c6349-111">복구 데이터베이스를 한 컴퓨터에서 다른 컴퓨터로 이동 하려면 (예: 서버 A에서 서버 B로) 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="c6349-112">관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="c6349-113">서버 B에서 MBAM 설정을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="c6349-114">서버 A에서 MBAM 복구 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="c6349-115">MBAM 복구 데이터베이스를 서버 A에서 B로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="c6349-116">서버 B에서 MBAM 복구 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="c6349-117">서버 B에서 MBAM 복구 데이터베이스에 대 한 액세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="c6349-118">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="c6349-119">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="c6349-120">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="c6349-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="c6349-121">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="c6349-122">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="c6349-123">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-123">Note</span></span>**  
    <span data-ttu-id="c6349-124">이 PowerShell 명령줄을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="c6349-125">또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="c6349-126">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="c6349-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="c6349-127">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 **복구 데이터베이스** 만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="c6349-128">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="c6349-129">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-129">Note</span></span>**  
    <span data-ttu-id="c6349-130">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-131">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 데이터베이스를 이동할 서버와 인스턴스의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="c6349-132">$DOMAIN $ \\ $SERVERNAME $-복구 데이터베이스에 연결 될 각 MBAM 관리 및 모니터링 서버의 도메인 및 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="c6349-133">세미콜론을 사용 하 여 목록에서 각 도메인 및 서버 쌍을 구분 합니다 (예: $DOMAIN \\SERVERNAME $; $DOMAIN \\ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="c6349-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="c6349-134">각 서버 이름 뒤에는 다음 예제에 표시 된 대로 "$" 기호가와 야 합니다 (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="c6349-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="c6349-135">$X $-MBAM 독립 실행형 토폴로지를 설치 하는 경우 **0** 을 입력 하 고, Mbam 구성 관리자 토폴로지를 설치 하는 경우 **1** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="c6349-136">서버 A의 복구 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="c6349-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="c6349-137">서버 A에서 복구 데이터베이스를 백업 하려면 SQL Server Management Studio와 백업 이라는 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="c6349-138">기본적으로 데이터베이스 이름은 **Mbam 복구 데이터베이스**입니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="c6349-139">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="c6349-140">MBAM 복구 데이터베이스를 수정 하 여 full 복구 모드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

    ```sql
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

    **<span data-ttu-id="c6349-141">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-141">Note</span></span>**  
    <span data-ttu-id="c6349-142">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-143">$PASSWORD $-개인 키 파일을 암호화 하는 데 사용 되는 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="c6349-144">다음과 유사한 SQL Server PowerShell 및 명령줄을 사용 하 여 SQL 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="c6349-145">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-145">Note</span></span>**  
    <span data-ttu-id="c6349-146">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-147">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 데이터베이스를 백업할 서버와 인스턴스의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="c6349-148">복구 데이터베이스 및 인증서를 서버 A에서 서버 B로 이동</span><span class="sxs-lookup"><span data-stu-id="c6349-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="c6349-149">Windows 탐색기를 사용 하 여 서버 A에서 서버 B로 다음 파일을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="c6349-150">MBAM 복구 데이터베이스 데이터 .bak</span><span class="sxs-lookup"><span data-stu-id="c6349-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="c6349-151">암호화 된 데이터베이스의 인증서를 이동 하려면 다음과 같은 자동화 단계를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="c6349-152">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="c6349-153">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-153">Note</span></span>**  
    <span data-ttu-id="c6349-154">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-155">$SERVERNAME $-파일을 복사 하는 대상 서버의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="c6349-156">$DESTINATIONSHARE $-공유 이름과 파일을 복사할 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="c6349-157">서버 B에서 복구 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="c6349-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="c6349-158">SQL Server Management Studio와 ' **Restore database**' 라는 작업을 사용 하 여 서버 B의 복구 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="c6349-159">작업이 완료 되 면 **장치에서** 옵션을 선택한 다음 **추가** 명령을 사용 하 여 Mbam 복구 데이터베이스 **데이터 .bak** 파일을 선택 하 여 데이터베이스 백업 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="c6349-160">**확인** 을 선택 하 여 복원 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="c6349-161">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

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

    **<span data-ttu-id="c6349-162">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-162">Note</span></span>**  
    <span data-ttu-id="c6349-163">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-164">$PASSWORD $-개인 키 파일을 암호화 하는 데 사용한 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="c6349-165">Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="c6349-166">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-166">Note</span></span>**  
    <span data-ttu-id="c6349-167">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-168">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 데이터베이스가 복원 될 서버와 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="c6349-169">서버 B의 복구 데이터베이스에 대 한 액세스 구성</span><span class="sxs-lookup"><span data-stu-id="c6349-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="c6349-170">서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 복구 및 하드웨어 DB 액세스**라는 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="c6349-171">복원 된 데이터베이스의 SQL 로그인 **Mbam 및 하드웨어 Db 액세스가** 로그인 이름 **$MachineName $ \\Mbam 복구 및 하드웨어 db 액세스**에 매핑 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="c6349-172">설명 대로 매핑되지 않은 경우에는 유사한 그룹 구성원 자격을 사용 하 여 다른 로그인을 만들고이를 로그인 이름 **$MachineName $ \\MBAM 복구 및 하드웨어 DB 액세스**에 매핑하십시오.</span><span class="sxs-lookup"><span data-stu-id="c6349-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="c6349-173">이 절차를 자동화 하려면 서버 B의 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="c6349-174">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-174">Note</span></span>**  
    <span data-ttu-id="c6349-175">위의 예제에서 다음 값을 환경에 적합 한 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="c6349-176">$DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="c6349-177">예제에 표시 된 대로 서버 이름 뒤에 $가와 야 합니다 (예: MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="c6349-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="c6349-178">MBAM 관리 및 모니터링 서버에서 복구 데이터베이스 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6349-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="c6349-179">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트에서 호스팅되는 다음 응용 프로그램에 대 한 연결 문자열 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="c6349-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="c6349-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="c6349-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="c6349-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="c6349-182">각 응용 프로그램을 선택 하 고 **기능 뷰의** **관리** 섹션에 있는 **구성 편집기** 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="c6349-183">**섹션 목록** 컨트롤에서 **configurationstrings** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="c6349-184">**(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="c6349-185">**컬렉션 편집기**에서 MBAMAdministrationService 응용 프로그램의 구성을 업데이트할 때 **keyrecoveryconnectionstring** 또는 <strong> RecoveryAndHardwareDataStore </strong> 라는 행을 선택 합니다. MBAMRecoveryAndHardwareService에 대 한 구성을 업데이트할 때의 ConnectionString.</span><span class="sxs-lookup"><span data-stu-id="c6349-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="c6349-186">서버 이름 및 인스턴스 (예: $SERVERNAME $ \\ $SQLINSTANCENAME $)를 나열 하도록 **Configurationstrings** 속성에 대 한 **데이터 원본 =** 값을 업데이트 하 여 복구 데이터베이스를 이동한 위치에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="c6349-187">이 절차를 자동화 하려면 Windows를 사용 하 여 각 관리 및 모니터링 서버에서 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="c6349-188">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-188">Note</span></span>**  
   <span data-ttu-id="c6349-189">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="c6349-190">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="c6349-191">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c6349-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="c6349-192">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="c6349-193">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="c6349-194">준수 및 감사 데이터베이스 기능 이동</span><span class="sxs-lookup"><span data-stu-id="c6349-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="c6349-195">컴퓨터 간에 MBAM 준수 및 감사 데이터베이스를 이동 하려는 경우 (즉, 서버 A에서 서버 B로 데이터베이스를 이동 하려면 다음 절차를 사용 합니다.)</span><span class="sxs-lookup"><span data-stu-id="c6349-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="c6349-196">프로세스에는 다음과 같은 상위 수준 단계가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="c6349-197">관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="c6349-198">서버 B에서 MBAM 설정을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="c6349-199">서버 A의 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="c6349-200">데이터베이스를 서버 A에서 B로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="c6349-201">서버 B에서 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="c6349-202">서버 B에서 데이터베이스에 대 한 액세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="c6349-203">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="c6349-204">준수 및 감사 데이터베이스의 새 위치를 사용 하 여 SSRS 보고서 데이터 원본 연결 문자열을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="c6349-205">관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="c6349-206">관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="c6349-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="c6349-207">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="c6349-208">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="c6349-209">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-209">Note</span></span>**  
    <span data-ttu-id="c6349-210">이 명령줄을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="c6349-211">또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="c6349-212">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="c6349-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="c6349-213">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 **준수 및 감사 데이터베이스** 만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="c6349-214">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="c6349-215">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-215">Note</span></span>**  
    <span data-ttu-id="c6349-216">참고: 위의 예제에서 다음 값을 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-217">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 및 감사 데이터베이스가 이동 될 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="c6349-218">$DOMAIN $ \\ $SERVERNAME $-규정 준수 및 감사 데이터베이스에 연결 되는 각 MBAM 관리 및 모니터링 서버의 도메인 및 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="c6349-219">세미콜론을 사용 하 여 목록에서 각 도메인 및 서버 쌍을 구분 합니다 (예: $DOMAIN \\SERVERNAME $; $DOMAIN \\ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="c6349-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="c6349-220">각 서버 이름 뒤에는 다음 예제에 표시 된 대로 "$" 기호가와 야 합니다 (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="c6349-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="c6349-221">$DOMAIN $ \\ $USERNAME $-준수 및 감사 보고서 기능에서 준수 및 감사 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="c6349-222">$X $-MBAM 독립 실행형 토폴로지를 설치 하는 경우 **0** 을 입력 하 고, Mbam 구성 관리자 토폴로지를 설치 하는 경우 **1** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="c6349-223">서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="c6349-224">서버 A에서 준수 및 감사 데이터베이스를 백업 하려면 SQL Server Management Studio와 **백업**이라는 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="c6349-225">기본적으로 데이터베이스 이름은 **Mbam 준수 상태 데이터베이스**입니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="c6349-226">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

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

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  <span data-ttu-id="c6349-227">다음과 유사한 Windows PowerShell 명령줄을 사용 하 여 SQL 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="c6349-228">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-228">Note</span></span>**  
    <span data-ttu-id="c6349-229">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-230">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 및 감사 데이터베이스가 백업 되는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="c6349-231">서버 A에서 B로 규정 준수 및 감사 데이터베이스 이동</span><span class="sxs-lookup"><span data-stu-id="c6349-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="c6349-232">Windows 탐색기를 사용 하 여 서버 A에서 서버 B로 다음 파일을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="c6349-233">MBAM 준수 상태 데이터베이스 데이터 .bak</span><span class="sxs-lookup"><span data-stu-id="c6349-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="c6349-234">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="c6349-235">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-235">Note</span></span>**  
    <span data-ttu-id="c6349-236">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-237">$SERVERNAME $-파일이 복사 될 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="c6349-238">$DESTINATIONSHARE $-파일이 복사 될 공유 이름과 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="c6349-239">서버 B에서 규정 준수 및 감사 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="c6349-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="c6349-240">SQL Server Management Studio와 ' **Restore database**' 라는 작업을 사용 하 여 서버 B의 규정 준수 및 감사 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="c6349-241">작업이 완료 되 면 **장치에서** 옵션을 선택 하 여 데이터베이스 백업 파일을 선택한 다음 **추가** 명령을 사용 하 여 Mbam 준수 상태 데이터베이스 데이터 .bak 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="c6349-242">**확인** 을 선택 하 여 복원 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="c6349-243">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="c6349-244">다음과 유사한 Windows PowerShell 명령줄을 사용 하 여 SQL 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="c6349-245">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-245">Note</span></span>**  
    <span data-ttu-id="c6349-246">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-247">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 및 감사 데이터베이스가 복원 될 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="c6349-248">서버 B의 준수 및 감사 데이터베이스에 대 한 액세스 권한 구성</span><span class="sxs-lookup"><span data-stu-id="c6349-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="c6349-249">서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 준수 상태 DB 액세스**라는 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="c6349-250">복원 된 데이터베이스의 SQL 로그인 **Mbam 준수 감사 Db 액세스가** 로그인 이름 **$MachineName $ \\ MBAM 준수 감사 db 액세스**에 매핑 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="c6349-251">설명 대로 매핑되지 않은 경우에는 유사한 그룹 구성원 자격을 사용 하 여 다른 로그인을 만들고이를 로그인 이름 **$MachineName $ \\ MBAM 준수 감사 DB 액세스**에 매핑하십시오.</span><span class="sxs-lookup"><span data-stu-id="c6349-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="c6349-252">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 서버 B에 다음과 유사한 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="c6349-253">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-253">Note</span></span>**  
    <span data-ttu-id="c6349-254">위의 예제에서 다음 값을 환경에 적합 한 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="c6349-255">$DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="c6349-256">서버 이름 뒤에는 예제에 표시 된 대로 "$"가와 야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="c6349-257">(예: MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="c6349-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="c6349-258">$DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="c6349-259">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6349-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="c6349-260">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트에서 호스팅되는 다음 응용 프로그램에 대 한 연결 문자열 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="c6349-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="c6349-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="c6349-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="c6349-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="c6349-263">각 응용 프로그램을 선택 하 고 **기능 뷰의** **관리** 섹션에 있는 **구성 편집기** 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="c6349-264">**섹션 목록** 컨트롤에서 **configurationstrings** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="c6349-265">**(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="c6349-266">**컬렉션 편집기**에서 MBAMAdministrationService 응용 프로그램에 대 한 구성을 업데이트할 때 **ComplianceStatusConnectionString** 이라는 행을 선택 하거나 MBAMComplianceStatusService에 대 한 구성을 업데이트 하는 경우 **statusreportker** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="c6349-267">**Configurationstrings** 속성에 대 한 **데이터 원본 =** 값을 업데이트 하 여 복구 데이터베이스가 이동 된 서버 및 인스턴스 이름 (예: $SERVERNAME $ \\ $SQLINSTANCENAME)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="c6349-268">이 절차를 자동화 하려면 Windows를 사용 하 여 각 관리 및 모니터링 서버에 다음과 유사한 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="c6349-269">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-269">Note</span></span>**  
    <span data-ttu-id="c6349-270">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-271">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="c6349-272">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c6349-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="c6349-273">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="c6349-274">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="c6349-275">규정 준수 및 감사 보고서 이동</span><span class="sxs-lookup"><span data-stu-id="c6349-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="c6349-276">컴퓨터 간에 MBAM 준수 및 감사 보고서 (즉, 서버 A에서 서버 B로 보고서를 이동 하려는 경우)를 이동 하려면 다음과 같은 상위 수준의 단계를 포함 하는 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="c6349-277">서버 B에서 MBAM 설정을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="c6349-278">서버 B의 준수 및 감사 보고서에 대 한 액세스 권한을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="c6349-279">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="c6349-280">MBAM 관리 및 모니터링 서버에서 보고서 연결 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="c6349-281">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="c6349-282">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="c6349-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="c6349-283">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 **준수 및 감사 보고서** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="c6349-284">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="c6349-285">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-285">Note</span></span>**  
    <span data-ttu-id="c6349-286">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-287">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 및 감사 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="c6349-288">$DOMAIN $ \\ $USERNAME $-준수 및 감사 보고서 기능에서 준수 및 감사 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="c6349-289">$PASSWORD $-규정 준수 및 감사 데이터베이스에 연결 하는 데 사용 되는 사용자 계정의 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="c6349-290">$X $-MBAM 독립 실행형 토폴로지를 설치 하는 경우 **0** 을 입력 하 고, Mbam 구성 관리자 토폴로지를 설치 하는 경우 **1** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="c6349-291">서버 B의 준수 및 감사 보고서에 대 한 액세스 구성</span><span class="sxs-lookup"><span data-stu-id="c6349-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="c6349-292">서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 규정 준수 및 감사 보고서에 액세스할 수 있는 사용자 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="c6349-293">사용자 계정을 MBAM 보고서 사용자 라는 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="c6349-294">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 서버 B에 다음과 유사한 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="c6349-295">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-295">Note</span></span>**  
    <span data-ttu-id="c6349-296">위의 예제에서 다음 값을 환경에 적합 한 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="c6349-297">$DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="c6349-298">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="c6349-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="c6349-299">MBAM 관리 및 모니터링 서버 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="c6349-300">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="c6349-301">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="c6349-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="c6349-302">MBAM 관리 및 모니터링 서버 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 규정 준수 및 감사 보고서 URL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="c6349-303">**Microsoft BitLocker 관리 및 모니터링** 웹 사이트를 선택 하 고 **기능 뷰의** **관리** 섹션 아래에 있는 위치에 해당 하는 **구성 편집기** 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="c6349-304">**섹션 목록** 컨트롤에서 **appSettings** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="c6349-305">**(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="c6349-306">**컬렉션 편집기**에서 **Reports. u m l**이라는 이름의 행을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="c6349-307">서버 B에 대 한 서버 이름을 반영 하도록 **Microsoft Mbam. u m l** 의 값을 업데이트 합니다. 규정 준수 및 감사 보고서 기능이 명명 된 SQL Reporting Services 인스턴스에 설치 되어 있는 경우 URL에 대 한 인스턴스의 이름을 추가 하거나 업데이트 해야 합니다 (예: http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....).</span><span class="sxs-lookup"><span data-stu-id="c6349-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="c6349-308">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 각 관리 및 모니터링 서버에 다음과 유사한 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="c6349-309">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-309">Note</span></span>**  
   <span data-ttu-id="c6349-310">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="c6349-311">$SERVERNAME $-준수 및 감사 보고서가 설치 된 서버 이름의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="c6349-312">$SRSINSTANCENAME $-규정 준수 및 감사 보고서가 설치 된 SQL Reporting Services 인스턴스의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="c6349-313">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c6349-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="c6349-314">MBAM 관리 및 모니터링 서버 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="c6349-315">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="c6349-316">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-316">Note</span></span>**  
    <span data-ttu-id="c6349-317">이 명령줄을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="c6349-318">또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="c6349-319">관리 및 모니터링 기능 이동</span><span class="sxs-lookup"><span data-stu-id="c6349-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="c6349-320">MBAM 관리 및 모니터링 보고서 기능을 한 컴퓨터에서 다른 컴퓨터로 이동 하려면 (즉, 서버 A에서 서버 B로 기능을 이동 하는 경우) 다음과 같은 고급 단계를 포함 하는 다음 절차를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="c6349-321">서버 B에서 MBAM 설정을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="c6349-322">서버 B에서 데이터베이스에 대 한 액세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="c6349-323">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="c6349-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="c6349-324">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 **관리 및 모니터링 서버** 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="c6349-325">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="c6349-326">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-326">Note</span></span>**  
    <span data-ttu-id="c6349-327">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="c6349-328">$SERVERNAME $ \\ $SQLINSTANCENAME $-COMPLIDB \ _SQLINSTANCE 매개 변수에 대해 준수 및 감사 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="c6349-329">RECOVERYANDHWDB \ _SQLINSTANCE 매개 변수에 대해 복구 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="c6349-330">$DOMAIN $ \\ $USERNAME $-준수 및 감사 보고서 기능에서 준수 및 감사 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="c6349-331">$ REPORTSSERVERURL $-SQL Reporting Service 웹 사이트의 홈 위치에 대 한 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="c6349-332">보고서가 기본 SRS 인스턴스에 설치 되어 있는 경우 URL 형식에는 "http://$SERVERNAME $/ReportServer" 형식이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="c6349-333">보고서가 기본 SRS 인스턴스에 설치 되어 있는 경우 URL 형식에 "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $" 형식이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="c6349-334">$X $-MBAM 독립 실행형 토폴로지를 설치 하는 경우 **0** 을 입력 하 고, Mbam 구성 관리자 토폴로지를 설치 하는 경우 **1** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="c6349-335">데이터베이스에 대 한 액세스 권한 구성</span><span class="sxs-lookup"><span data-stu-id="c6349-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="c6349-336">복구 데이터베이스와 준수 및 감사 데이터베이스가 배포 되는 서버에서 서버 관리자에서 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 서버 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 복구 및 하드웨어 DB 액세스** (복구 DB 서버) 및 **Mbam 준수 상태 DB 액세스** (준수 및 감사 데이터베이스 서버)로 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="c6349-337">이 절차를 자동화 하기 위해 Windows PowerShell을 사용 하 여 규정 준수 및 감사 데이터베이스가 배포 된 서버에서 다음과 유사한 명령줄을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="c6349-338">복구 데이터베이스가 배포 된 서버에서 Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="c6349-339">참고</span><span class="sxs-lookup"><span data-stu-id="c6349-339">Note</span></span>**  
    <span data-ttu-id="c6349-340">위의 예제에서 다음 값을 환경에 적합 한 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="c6349-341">$DOMAIN $ \\ $SERVERNAME $ $-관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="c6349-342">서버 이름 뒤에는 예제에 표시 된 대로 "$" 기호가와 야 합니다 (예: MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="c6349-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="c6349-343">$DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6349-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="c6349-344">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c6349-344">Related topics</span></span>


[<span data-ttu-id="c6349-345">MBAM 2.0 유지 관리</span><span class="sxs-lookup"><span data-stu-id="c6349-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









