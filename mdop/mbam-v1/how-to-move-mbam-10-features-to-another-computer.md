---
title: MBAM 1.0 기능을 다른 컴퓨터로 이동하는 방법
description: MBAM 1.0 기능을 다른 컴퓨터로 이동하는 방법
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812948"
---
# <span data-ttu-id="8c3cc-103">MBAM 1.0 기능을 다른 컴퓨터로 이동하는 방법</span><span class="sxs-lookup"><span data-stu-id="8c3cc-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="8c3cc-104">이 항목에서는 하나 이상의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능을 다른 컴퓨터로 이동 하는 데 필요한 단계에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="8c3cc-105">두 개 이상의 MBAM 기능을 다른 컴퓨터로 이동 하는 경우 다음 순서로 이동 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="8c3cc-106">복구 및 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8c3cc-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="8c3cc-107">준수 및 감사 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8c3cc-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="8c3cc-108">규정 준수 및 감사 보고서</span><span class="sxs-lookup"><span data-stu-id="8c3cc-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="8c3cc-109">관리 및 모니터링</span><span class="sxs-lookup"><span data-stu-id="8c3cc-109">Administration and Monitoring</span></span>

## <span data-ttu-id="8c3cc-110">복구 및 하드웨어 데이터베이스를 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="8c3cc-111">다음 절차를 사용 하 여 MBAM 복구 및 하드웨어 데이터베이스를 다른 컴퓨터로 이동할 수 있습니다 (이 MBAM 서버 기능을 서버 A에서 서버 B로 이동할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="8c3cc-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="8c3cc-112">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="8c3cc-113">서버 B에서 MBAM 설정을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="8c3cc-114">서버 A에서 MBAM 복구 및 하드웨어 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="8c3cc-115">MBAM 복구 및 서버 A에서 B로의 하드웨어 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8c3cc-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="8c3cc-116">서버 B에서 MBAM 복구 및 하드웨어 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="8c3cc-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="8c3cc-117">서버 B에서 MBAM 복구 및 하드웨어 데이터베이스에 대 한 액세스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="8c3cc-118">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="8c3cc-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="8c3cc-119">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="8c3cc-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="8c3cc-120">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="8c3cc-121">IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 MBAM 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="8c3cc-122">MBAM 웹 사이트는 **Microsoft BitLocker 관리 및 모니터링**이라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="8c3cc-123">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령 프롬프트에서 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="8c3cc-124">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-124">Note</span></span>**  
    <span data-ttu-id="8c3cc-125">이 PowerShell 명령 프롬프트를 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="8c3cc-126">또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="8c3cc-127">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-128">서버 B에서 MBAM 설정을 실행 하 고 설치할 복구 및 하드웨어 데이터베이스를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="8c3cc-129">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령 프롬프트에서 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="8c3cc-130">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-130">Note</span></span>**  
    <span data-ttu-id="8c3cc-131">위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-132">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스가 이동 되는 서버와 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="8c3cc-133">$DOMAIN $ \\ $SERVERNAME $-복구 및 하드웨어 데이터베이스에 연결 될 각 MBAM 응용 프로그램과 모니터링 서버의 도메인 및 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="8c3cc-134">도메인 및 서버 이름이 여러 개인 경우에는 세미콜론을 사용 하 여 목록에서 각각을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="8c3cc-135">예를 들어 $DOMAIN \\SERVERNAME $; $DOMAIN \\ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="8c3cc-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="8c3cc-136">또한 각 서버 이름 뒤에는가와 야 합니다 **$** .</span><span class="sxs-lookup"><span data-stu-id="8c3cc-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="8c3cc-137">예를 들어 MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="8c3cc-138">서버 A의 데이터베이스를 백업 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="8c3cc-139">서버 A에서 복구 및 하드웨어 데이터베이스를 백업 하려면 SQL Server Management Studio를 사용 하 고 **백업**이라는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="8c3cc-140">기본적으로 데이터베이스 이름은 **Mbam 복구 및 하드웨어 데이터베이스**입니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="8c3cc-141">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="8c3cc-142">MBAM 복구와 하드웨어 데이터베이스를 수정 하 여 full 복구 모드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="8c3cc-143">MBAM 복구와 하드웨어 데이터베이스 데이터 및 MBAM 복구 논리 백업 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="8c3cc-144">전체 MBAM 복구 및 하드웨어 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-144">Back up the full MBAM Recovery and Hardware database.</span></span>

    ```sql
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

    **<span data-ttu-id="8c3cc-145">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-145">Note</span></span>**  
    <span data-ttu-id="8c3cc-146">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-147">$PASSWORD $-개인 키 파일을 암호화 하는 데 사용 되는 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="8c3cc-148">다음과 유사한 SQL Server PowerShell 및 명령을 사용 하 여 SQL 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="8c3cc-149">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-149">Note</span></span>**  
    <span data-ttu-id="8c3cc-150">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-151">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스를 백업 하는 서버와 인스턴스의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="8c3cc-152">데이터베이스 및 인증서를 서버 A에서 B로 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="8c3cc-153">Windows 탐색기를 사용 하 여 MBAM 복구 및 하드웨어 데이터베이스 데이터 .bak를 서버 A에서 서버 B로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="8c3cc-154">암호화 된 데이터베이스의 인증서를 이동 하려면 다음의 자동화 단계를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="8c3cc-155">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="8c3cc-156">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-156">Note</span></span>**  
    <span data-ttu-id="8c3cc-157">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-158">$SERVERNAME $-파일을 복사 하는 대상 서버의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="8c3cc-159">$DESTINATIONSHARE $-공유 이름과 파일을 복사할 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="8c3cc-160">서버 B에서 데이터베이스를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-161">SQL Server Management Studio와 **Restore database**라는 작업을 사용 하 여 서버 B의 복구 및 하드웨어 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="8c3cc-162">작업이 실행 되 면 **장치에서** 옵션을 선택 하 여 데이터베이스 백업 파일을 선택한 다음 **추가** 명령을 사용 하 여 Mbam 복구 및 하드웨어 데이터베이스 **데이터 .bak** 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="8c3cc-163">**확인** 을 선택 하 여 복원 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="8c3cc-164">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="8c3cc-165">MBAM 설정으로 만든 인증서를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="8c3cc-166">인증서 추가</span><span class="sxs-lookup"><span data-stu-id="8c3cc-166">Add certificate</span></span>

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    <span data-ttu-id="8c3cc-167">MBAM 복구와 하드웨어 데이터베이스 데이터 및 로그 파일을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="8c3cc-168">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-168">Note</span></span>**  
    <span data-ttu-id="8c3cc-169">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-170">$PASSWORD $-개인 키 파일을 암호화 하는 데 사용한 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="8c3cc-171">Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="8c3cc-172">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-172">Note</span></span>**  
    <span data-ttu-id="8c3cc-173">Receding 예제의 값을 해당 환경과 일치 하는 항목으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-174">$SERVERNAME $ \\ $SQLINSTANCENAME $-서버 이름과 복구 및 하드웨어 데이터베이스가 복원 되는 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="8c3cc-175">서버 B에서 데이터베이스에 대 한 액세스 구성</span><span class="sxs-lookup"><span data-stu-id="8c3cc-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-176">서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 복구 및 하드웨어 DB 액세스**라는 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="8c3cc-177">이 절차를 자동화 하려면 서버 B의 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="8c3cc-178">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-178">Note</span></span>**  
    <span data-ttu-id="8c3cc-179">이전 예제의 값을 해당 환경에 해당 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="8c3cc-180">$DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 이름과 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="8c3cc-181">서버 이름 뒤에는 a가와 야 합니다 **$** (예: MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="8c3cc-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="8c3cc-182">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="8c3cc-183">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 웹 사이트에서 호스팅되는 다음 응용 프로그램에 대 한 연결 문자열 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="8c3cc-184">MBAM 관리 서비스</span><span class="sxs-lookup"><span data-stu-id="8c3cc-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="8c3cc-185">MBAM 복구 및 하드웨어 서비스</span><span class="sxs-lookup"><span data-stu-id="8c3cc-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="8c3cc-186">각 응용 프로그램을 선택 하 고 **기능 뷰의** **관리** 섹션에 있는 **구성 편집기** 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="8c3cc-187">섹션 목록 컨트롤에서 **Configurationstrings** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="8c3cc-188">**(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="8c3cc-189">**컬렉션 편집기**에서 ' MBAMAdministrationService ' 응용 프로그램에 대 한 구성을 업데이트할 때 **keyrecoveryconnectionstring** 이라는 행을 선택 하거나 <strong> Microsoft RecoveryAndHardwareDataStore </strong> 라는 행을 선택 합니다. ' MBAMRecoveryAndHardwareService '에 대 한 구성을 업데이트 하는 경우 ConnectionString.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="8c3cc-190">서버 이름과 복구 및 하드웨어 데이터베이스가 이동 된 인스턴스를 나열 하도록 **Configurationstrings** 속성에 대 한 **데이터 원본 =** 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="8c3cc-191">예를 들어 $ \\ \ $SQLINSTANCENAME $를 $SERVERNAME 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="8c3cc-192">이 절차를 자동화 하려면 각 관리 및 모니터링 서버에서 Windows PowerShell을 사용 하 여 다음과 유사한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="8c3cc-193">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-193">Note</span></span>**  
   <span data-ttu-id="8c3cc-194">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="8c3cc-195">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="8c3cc-196">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="8c3cc-197">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="8c3cc-198">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="8c3cc-199">준수 상태 데이터베이스 기능을 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="8c3cc-200">서버 A에서 서버 B와 같이 컴퓨터 간에 MBAM 준수 상태 데이터베이스 기능을 이동 하려면 다음 절차를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="8c3cc-201">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="8c3cc-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="8c3cc-202">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="8c3cc-203">서버 A에서 데이터베이스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="8c3cc-204">데이터베이스를 서버 A에서 B로 이동</span><span class="sxs-lookup"><span data-stu-id="8c3cc-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="8c3cc-205">서버 B에서 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="8c3cc-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="8c3cc-206">서버 B에서 데이터베이스에 대 한 액세스 권한 구성</span><span class="sxs-lookup"><span data-stu-id="8c3cc-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="8c3cc-207">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="8c3cc-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="8c3cc-208">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="8c3cc-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="8c3cc-209">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="8c3cc-210">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="8c3cc-211">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="8c3cc-212">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-212">Note</span></span>**  
    <span data-ttu-id="8c3cc-213">이 명령을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="8c3cc-214">또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="8c3cc-215">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-216">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 준수 상태 데이터베이스 기능을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="8c3cc-217">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="8c3cc-218">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-218">Note</span></span>**  
    <span data-ttu-id="8c3cc-219">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-220">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 이동 될 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="8c3cc-221">$DOMAIN $ \\ $SERVERNAME $-준수 상태 데이터베이스에 연결 되는 각 MBAM 응용 프로그램과 모니터링 서버의 도메인 이름과 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="8c3cc-222">여러 도메인 이름과 서버 이름이 있는 경우 세미콜론을 사용 하 여 목록에서 각각을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="8c3cc-223">예를 들어 $DOMAIN \\SERVERNAME $; $DOMAIN \\ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="8c3cc-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="8c3cc-224">각 서버 이름 뒤에는이 예제에 나와 있는 a가와 야 합니다 **$** .</span><span class="sxs-lookup"><span data-stu-id="8c3cc-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="8c3cc-225">예를 들어 MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="8c3cc-226">$DOMAIN $ \\ $USERNAME $-규정 준수 및 감사 보고서 기능에서 준수 상태 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="8c3cc-227">서버 A의 규정 준수 데이터베이스를 백업 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="8c3cc-228">서버 A에서 규정 준수 데이터베이스를 백업 하려면 SQL Server Management Studio를 사용 하 고 **백업**이라는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="8c3cc-229">기본적으로 데이터베이스 이름은 **Mbam 준수 상태 데이터베이스**입니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="8c3cc-230">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  <span data-ttu-id="8c3cc-231">SQL Server PowerShell을 사용 하 여 다음과 유사한 명령을 사용 하 여 SQL 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="8c3cc-232">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-232">Note</span></span>**  
    <span data-ttu-id="8c3cc-233">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-234">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 백업 될 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="8c3cc-235">데이터베이스를 서버 A에서 B로 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="8c3cc-236">Windows 탐색기를 사용 하 여 서버 A에서 서버 B로 다음 파일을 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="8c3cc-237">MBAM 준수 상태 데이터베이스 데이터 .bak</span><span class="sxs-lookup"><span data-stu-id="8c3cc-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="8c3cc-238">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="8c3cc-239">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-239">Note</span></span>**  
    <span data-ttu-id="8c3cc-240">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-241">$SERVERNAME $-파일이 복사 될 서버 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="8c3cc-242">$DESTINATIONSHARE $-파일이 복사 될 공유 이름과 경로를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="8c3cc-243">서버 B에서 데이터베이스를 복원 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-244">SQL Server Management Studio와 " **복원 데이터베이스**" 작업을 사용 하 여 서버 B의 준수 상태 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="8c3cc-245">작업이 실행 되 면 장치에서 옵션을 선택 하 여 데이터베이스 백업 파일을 선택 하 고 추가 명령을 사용 하 여 MBAM 준수 상태 데이터베이스 데이터 .bak 파일을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="8c3cc-246">확인을 클릭 하 여 복원 프로세스를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="8c3cc-247">이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="8c3cc-248">SQL Server PowerShell을 사용 하 여 다음과 유사한 명령을 사용 하 여 SQL 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="8c3cc-249">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-249">Note</span></span>**  
    <span data-ttu-id="8c3cc-250">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-251">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 복원 될 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="8c3cc-252">서버 B에서 데이터베이스에 대 한 액세스를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-253">서버 B에서는 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 준수 상태 DB 액세스**라는 로컬 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="8c3cc-254">이 절차를 자동화 하려면 서버 B에서 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="8c3cc-255">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-255">Note</span></span>**  
    <span data-ttu-id="8c3cc-256">이전 예제의 값을 해당 환경에 해당 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="8c3cc-257">$DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="8c3cc-258">서버 이름 뒤에는가와 야 합니다 **$** . 예를 들어 MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="8c3cc-259">$DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="8c3cc-260">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="8c3cc-261">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 웹 사이트에서 호스팅되는 다음 응용 프로그램에 대 한 연결 문자열 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="8c3cc-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="8c3cc-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="8c3cc-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="8c3cc-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="8c3cc-264">각 응용 프로그램을 선택 하 고 **기능 뷰의** **관리** 섹션에 있는 **구성 편집기** 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="8c3cc-265">섹션 목록 컨트롤에서 **Configurationstrings** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="8c3cc-266">**(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 컬렉션 편집기를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="8c3cc-267">**컬렉션 편집기**에서 MBAMAdministrationService 응용 프로그램에 대 한 구성을 업데이트 하는 경우 **ComplianceStatusConnectionString**이라는 행을 선택 하 고, MBAMComplianceStatusService에 대 한 구성을 업데이트 하는 경우에는 **Windows 용 데이터 저장소 ConnectionString**이라는 이름의 행 또는 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="8c3cc-268">서버 이름과 인스턴스 이름을 나열 하도록 **Configurationstrings** 속성에 대 한 **데이터 원본 =** 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="8c3cc-269">예를 들어 복구 및 하드웨어 데이터베이스가 이동 된 $SERVERNAME $ \\ $SQLINSTANCENAME.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="8c3cc-270">이 절차를 자동화 하기 위해 Windows PowerShell을 사용 하 여 각 관리 및 모니터링 서버에서 다음과 유사한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="8c3cc-271">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-271">Note</span></span>**  
    <span data-ttu-id="8c3cc-272">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-273">$SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스가 있는 서버 이름과 인스턴스 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="8c3cc-274">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="8c3cc-275">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="8c3cc-276">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="8c3cc-277">PS C:\\ &gt; 시작-웹 사이트 "Microsoft BitLocker 관리 및 모니터링"</span><span class="sxs-lookup"><span data-stu-id="8c3cc-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="8c3cc-278">규정 준수 및 감사 보고서를 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="8c3cc-279">컴퓨터 간에 MBAM 준수 및 감사 보고서를 이동 하도록 선택 하면 (특히, 서버 A에서 서버 B로 이동 하는 경우) 다음 절차와 단계를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="8c3cc-280">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="8c3cc-281">서버 B의 준수 및 감사 보고서에 대 한 액세스 구성</span><span class="sxs-lookup"><span data-stu-id="8c3cc-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="8c3cc-282">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지</span><span class="sxs-lookup"><span data-stu-id="8c3cc-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="8c3cc-283">MBAM 관리 및 모니터링 서버에서 보고서 연결 데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="8c3cc-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="8c3cc-284">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="8c3cc-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="8c3cc-285">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-286">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 준수 및 감사 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="8c3cc-287">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="8c3cc-288">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-288">Note</span></span>**  
    <span data-ttu-id="8c3cc-289">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-290">$SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="8c3cc-291">$DOMAIN $ \\ $USERNAME $-규정 준수 및 감사 보고서 기능에서 준수 상태 데이터베이스에 연결 하는 데 사용할 도메인 이름과 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="8c3cc-292">$PASSWORD $-준수 상태 데이터베이스에 연결 하는 데 사용 되는 사용자 계정의 암호를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="8c3cc-293">서버 B의 준수 및 감사 보고서에 대 한 액세스를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-294">서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 규정 준수 및 감사 보고서에 액세스할 수 있는 사용자 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="8c3cc-295">"MBAM 보고서 사용자" 라는 로컬 그룹에 사용자 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="8c3cc-296">이 절차를 자동화 하려면 서버 B에서 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="8c3cc-297">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-297">Note</span></span>**  
    <span data-ttu-id="8c3cc-298">앞의 예제에서 다음 값을 환경에 적용할 수 있는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="8c3cc-299">$DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="8c3cc-300">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="8c3cc-301">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="8c3cc-302">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="8c3cc-303">MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="8c3cc-304">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 준수 보고서 URL을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="8c3cc-305">**Microsoft BitLocker 관리 및 모니터링** 웹 사이트를 선택 하 고 **기능 보기**의 **관리** 섹션에서 찾을 수 있는 **구성 편집기** 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="8c3cc-306">섹션 목록 컨트롤에서 **appSettings** 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="8c3cc-307">여기에서 **(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="8c3cc-308">**컬렉션 편집기**에서 "Microsoft. m l. Reports." 라는 행을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="8c3cc-309">서버 B에 대 한 서버 이름을 반영 하도록 Microsoft Mbam. u m l의 값을 업데이트 합니다. 규정 준수 및 감사 보고서 기능이 명명 된 SQL Reporting Services 인스턴스에 설치 되어 있는 경우 해당 URL에 대 한 인스턴스의 이름을 추가 하거나 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="8c3cc-310">예를 들어 http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....</span><span class="sxs-lookup"><span data-stu-id="8c3cc-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="8c3cc-311">이 절차를 자동화 하기 위해 Windows PowerShell을 사용 하 여 각 관리 및 모니터링 서버에서 다음과 유사한 명령을 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="8c3cc-312">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-312">Note</span></span>**  
   <span data-ttu-id="8c3cc-313">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="8c3cc-314">$SERVERNAME $-규정 준수 및 감사 보고서가 설치 된 서버의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="8c3cc-315">$SRSINSTANCENAME $-규정 준수 및 감사 보고서가 설치 된 SQL Reporting Services 인스턴스의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="8c3cc-316">MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="8c3cc-317">MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="8c3cc-318">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="8c3cc-319">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-319">Note</span></span>**  
    <span data-ttu-id="8c3cc-320">이 명령을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="8c3cc-321">또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="8c3cc-322">관리 및 모니터링 기능을 이동 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="8c3cc-323">MBAM 관리 및 모니터링 보고서 기능을 한 컴퓨터에서 다른 컴퓨터로 이동 하도록 선택 하면 (서버 A에서 서버 B로 기능을 이동 하는 경우) 다음 절차를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="8c3cc-324">프로세스에는 다음 단계가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="8c3cc-325">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="8c3cc-326">서버 B에서 데이터베이스에 대 한 액세스 권한 구성</span><span class="sxs-lookup"><span data-stu-id="8c3cc-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="8c3cc-327">서버 B에서 MBAM 설정 실행</span><span class="sxs-lookup"><span data-stu-id="8c3cc-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="8c3cc-328">서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 관리 기능만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="8c3cc-329">이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="8c3cc-330">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-330">Note</span></span>**  
    <span data-ttu-id="8c3cc-331">이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="8c3cc-332">$SERVERNAME $ \\ $SQLINSTANCENAME $-COMPLIDB \ _SQLINSTANCE 매개 변수에 대해 준수 상태 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="8c3cc-333">RECOVERYANDHWDB \ _SQLINSTANCE 매개 변수에 대해 복구 및 하드웨어 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="8c3cc-334">$DOMAIN $ \\ $USERNAME $-규정 준수 및 감사 보고서 기능에서 준수 상태 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="8c3cc-335">$ REPORTSSERVERURL $-SQL Reporting Service 웹 사이트의 홈 위치에 대 한 URL을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="8c3cc-336">보고서를 기본 SRS 인스턴스에 설치 하는 경우 URL 형식에 "http://$SERVERNAME $/ReportServer" 형식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="8c3cc-337">보고서가 기본 SRS 인스턴스에 설치 되어 있는 경우 URL 형식이 "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $"으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="8c3cc-338">데이터베이스에 대 한 액세스를 구성 하려면</span><span class="sxs-lookup"><span data-stu-id="8c3cc-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="8c3cc-339">복구와 하드웨어가 있는 서버나 서버에서 및 준수 및 감사 데이터베이스가 배포 되는 경우 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 "MBAM 복구 및 하드웨어 DB (복구 및 하드웨어 DB Server)" 라는 로컬 그룹에 추가 하 고 "MBAM 준수 상태 DB 액세스" (준수 및 감사 DB 서버)를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="8c3cc-340">이 절차를 자동화 하려면 준수 및 감사 데이터베이스가 배포 된 서버에서 Windows PowerShell을 사용 하 여 다음과 유사한 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="8c3cc-341">복구 및 하드웨어 데이터베이스가 배포 된 서버에서 Windows PowerShell을 사용 하 여 다음과 유사한 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="8c3cc-342">참고</span><span class="sxs-lookup"><span data-stu-id="8c3cc-342">Note</span></span>**  
    <span data-ttu-id="8c3cc-343">이전 예제의 값을 해당 환경에 해당 하는 값으로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="8c3cc-344">$DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="8c3cc-345">서버 이름 뒤에는가와 야 합니다 **$** .</span><span class="sxs-lookup"><span data-stu-id="8c3cc-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="8c3cc-346">예를 들어 MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="8c3cc-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="8c3cc-347">$DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c3cc-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="8c3cc-348">관련 항목</span><span class="sxs-lookup"><span data-stu-id="8c3cc-348">Related topics</span></span>


[<span data-ttu-id="8c3cc-349">MBAM 1.0 기능 관리</span><span class="sxs-lookup"><span data-stu-id="8c3cc-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









