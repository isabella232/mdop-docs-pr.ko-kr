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
# MBAM 2.5 데이터베이스를 이동하는 방법

다음 절차를 사용 하 여 다음 데이터베이스를 한 컴퓨터에서 다른 컴퓨터로 이동 합니다. 서버 A에서 서버 B까지, 예를 들면 다음과 같습니다.

-   준수 및 감사 데이터베이스

-   복구 데이터베이스

>[!NOTE]
>MBAM 구성 마법사를 실행 하기 전에 데이터베이스를 시스템 B로 복원 하 여 업데이트/구성 하는 것이 중요 합니다.

데이터베이스가 없으면 구성 마법사가 비어 있는 새 데이터베이스를 만듭니다. 기존 데이터베이스가 복원 되 면이 프로세스는 MBAM 구성을 중단 합니다.

먼저 데이터베이스를 복원한 다음 MBAM 구성 마법사를 실행 하 고 데이터베이스 옵션을 선택 하면 구성 마법사가 복원한 데이터베이스에 "연결" 됩니다. 프로세스의 일부로 필요한 경우 업그레이드

**여러 기능을 이동 하는 경우 다음 순서 대로 이동 합니다.**

1.  복구 데이터베이스

2.  준수 및 감사 데이터베이스

3.  보고

4.  관리 및 모니터링 웹 사이트

5.  셀프 서비스 포털

>[!Note]
>이 항목에서 제공 하는 예제 Windows PowerShell 스크립트를 실행 하려면 스크립트를 실행할 수 있도록 Windows PowerShell 실행 정책을 업데이트 해야 합니다. 자세한 내용은 [Windows PowerShell 스크립트 실행](https://technet.microsoft.com/library/ee176949.aspx) 을 참조 하세요.

## 복구 데이터베이스 이동

복구 데이터베이스 이동에 대 한 상위 수준 단계는 다음과 같습니다.

1.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지

2.  서버 A의 복구 데이터베이스 백업

3.  복구 데이터베이스를 서버 A에서 서버 B로 이동

4.  서버 B에서 복구 데이터베이스 복원

5.  서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.

6.  MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행

7.  관리 및 모니터링 웹 사이트 인스턴스 다시 시작

### 복구 데이터베이스를 이동 하는 방법

**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.** MBAM 관리 및 모니터링 서버 웹 사이트를 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 중지 합니다.

이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>이 명령을 실행 하려면 windows powershell 용 IIS (인터넷 정보 서비스) 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.

### 서버 A의 복구 데이터베이스 백업

1.  SQL Server Management Studio의 **백업** 작업을 사용 하 여 서버 A의 복구 데이터베이스를 백업 합니다.  기본적으로 데이터베이스 이름은 **Mbam 복구 데이터베이스**입니다.

2.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만들고, 모든 복구 모드를 사용 하도록 MBAM 복구 데이터베이스를 변경 합니다.

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

3.  다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    **$PASSWORD $** -개인 키 파일을 암호화 하는 데 사용 하는 암호입니다.

4.  Windows PowerShell에서 다음 예와 유사 하 게 파일에 저장 된 스크립트를 실행 합니다.

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    **$SERVERNAME $ \ $SQLINSTANCENAME $** -복구 데이터베이스가 백업 되는 서버 이름 및 인스턴스.

### 복구 데이터베이스를 서버 A에서 서버 B로 이동

Windows 탐색기를 사용 하 여 **Mbam 복구 데이터베이스 데이터 .bak** 파일을 서버 a에서 서버 B로 이동 합니다.

이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
다음 표의 정보를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

| **매개 변수**        | **설명**  |
|----------------------|------------------|
| $SERVERNAME $       | 파일이 복사 되는 서버의 이름입니다. |
| $DESTINATIONSHARE $ | 파일이 복사 되는 공유 및 경로의 이름입니다. |


### 서버 B에서 복구 데이터베이스 복원

1.  SQL Server Management Studio에서 **데이터베이스 복원** 작업을 사용 하 여 서버 B의 복구 데이터베이스를 복원 합니다.

2.  이전 작업이 완료 되 면 **장치에서**를 선택한 다음 데이터베이스 백업 파일을 선택 합니다.

3.  **추가** 명령을 사용 하 여 **Mbam 복구 데이터베이스 데이터 .bak** 파일을 선택 하 고 **확인** 을 클릭 하 여 복원 프로세스를 완료 합니다.

4.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

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

5.  다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    **$PASSWORD $** -개인 키 파일을 암호화 하는 데 사용 하는 암호입니다.

6.  Windows PowerShell에서 다음 예와 유사 하 게 파일에 저장 된 스크립트를 실행 합니다.

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    **$SERVERNAME $ \ $SQLINSTANCENAME $** -복구 데이터베이스가 복원 될 서버 이름 및 인스턴스.

### 서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.

1. 복원 된 데이터베이스에서 복구 데이터베이스 액세스를 사용 하도록 설정 하는 Microsoft SQL Server 사용자 로그인이 구성 프로세스 중에 제공한 액세스 계정에 매핑 되었는지 확인 합니다.

   >[!NOTE]
   >로그인이 동일 하지 않으면 SQL Server Management Studio를 사용 하 여 로그인을 만들고 기존 데이터베이스 사용자에 매핑합니다.

2. 관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 MBAM 웹 사이트의 연결 문자열 정보를 업데이트 합니다.

3. 다음 레지스트리 키를 편집 합니다.

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. 복구 데이터베이스가 이동 된 서버 및 인스턴스 이름 (예: \ $SERVERNAME \ $ \\ \ $SQLINSTANCENAME)으로 **데이터 원본** 값을 업데이트 합니다.

5. 복구 된 데이터베이스 이름으로 **초기 카탈로그** 값을 업데이트 합니다.

6. 이 프로세스를 자동화 하려면 Windows PowerShell 명령 프롬프트를 사용 하 여 관리 및 모니터링 서버에 다음과 유사한 명령줄을 입력 하면 됩니다.

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
   >이 연결 문자열은 모든 로컬 MBAM 웹 응용 프로그램에서 공유 합니다. 따라서 서버 당 한 번만 업데이트 해야 합니다.


7. 다음 표를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

   |매개 변수|설명|
   |---------|-----------|
   |$SERVERNAME $/\ $SQLINSTANCENAME $|복구 데이터베이스가 있는 SQL Server의 서버 이름 및 인스턴스|
   |$DATABASE $|복구 데이터베이스의 이름입니다.|


### MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행

1.  서버 B에 MBAM 2.5 서버 소프트웨어를 설치 합니다. 자세한 내용은 [MBAM 2.5 서버 소프트웨어 설치](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)를 참조 하세요.

2.  서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **복구 데이터베이스** 기능만 선택 합니다. 데이터베이스를 구성 하는 방법에 대 한 자세한 내용은 [MBAM 2.5 데이터베이스를 구성](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)하는 방법을 참조 하세요.

    >[!TIP]
    >또는 **Enable-MbamDatabase** Windows PowerShell cmdlet을 사용 하 여 복구 데이터베이스를 구성할 수 있습니다.


### 관리 및 모니터링 웹 사이트 인스턴스 다시 시작

관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 시작 합니다.

이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>이 명령을 실행 하려면 windows powershell 용 IIS 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.

## 준수 및 감사 데이터베이스 이동

준수 및 감사 데이터베이스 이동에 대 한 상위 수준 단계는 다음과 같습니다.

1.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지

2.  서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다.

3.  서버 A에서 서버 B로 규정 준수 및 감사 데이터베이스 이동

4.  서버 B에서 규정 준수 및 감사 데이터베이스 복원

5.  서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.

6.  MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행

7.  관리 및 모니터링 웹 사이트 인스턴스 다시 시작

### 준수 및 감사 데이터베이스를 이동 하는 방법

**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.**  MBAM 관리 및 모니터링 서버 웹 사이트를 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 중지 합니다.

이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>이 명령을 실행 하려면 windows powershell 용 IIS (인터넷 정보 서비스) 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.

### 서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다.

1.  SQL Server Management Studio의 **백업** 작업을 사용 하 여 서버 A의 규정 준수 및 감사 데이터베이스를 백업 합니다. 기본적으로 데이터베이스 이름은 **Mbam 준수 상태 데이터베이스**입니다.

2.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

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

3.  다음과 유사한 Windows PowerShell 명령을 사용 하 여 .sql 파일에 저장 된 스크립트를 실행 합니다.

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    **$SERVERNAME $ \ $SQLINSTANCENAME $** -규정 준수 및 감사 데이터베이스가 백업 되는 서버 이름과 인스턴스.

### 준수 및 감사 데이터베이스를 서버 A에서 서버 B로 이동 * *

1.  Windows 탐색기를 사용 하 여 **Mbam 준수 상태 데이터베이스 데이터 .bak** 파일을 서버 A에서 서버 B로 이동 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  다음 표를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    | **매개 변수**        | **설명**                                               |
    |----------------------|---------------------------------------------------------------|
    | $SERVERNAME $       | 파일이 복사 되는 서버의 이름입니다.         |
    | $DESTINATIONSHARE $ | 파일이 복사 되는 공유 및 경로의 이름입니다. |


### 서버 B에서 규정 준수 및 감사 데이터베이스 복원

1.  SQL Server Management Studio에서 **데이터베이스 복원** 작업을 사용 하 여 서버 B의 규정 준수 및 감사 데이터베이스를 복원 합니다.

2.  이전 작업이 완료 되 면 **장치에서**를 선택한 다음 데이터베이스 백업 파일을 선택 합니다.

3.  **추가** 명령을 사용 하 여 **Mbam 준수 상태 데이터베이스 데이터 .bak** 파일을 선택 하 고 **확인** 을 클릭 하 여 복원 프로세스를 완료 합니다.

4.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  Windows PowerShell에서 다음 예와 유사 하 게 파일에 저장 된 스크립트를 실행 합니다.

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  다음 값을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    **$SERVERNAME $ \ $SQLINSTANCENAME $** -준수 및 감사 데이터베이스가 복원 될 서버 이름과 인스턴스.

### 서버 B에서 데이터베이스에 대 한 액세스를 구성 하 고 연결 데이터를 업데이트 합니다.

1. 복원 된 데이터베이스에서 준수 및 감사 데이터베이스 액세스를 사용 하도록 설정 하는 Microsoft SQL Server 사용자 로그인이 구성 프로세스 중에 제공한 액세스 계정에 매핑 되었는지 확인 합니다.

   >[!NOTE]
   >로그인이 동일 하지 않으면 SQL Server Management Studio를 사용 하 여 로그인을 만들고 기존 데이터베이스 사용자에 매핑합니다.

2. 관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 웹 사이트에 대 한 연결 문자열 정보를 업데이트 합니다.

3. 다음 레지스트리 키를 편집 합니다.

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. 복구 데이터베이스가 이동 된 서버 및 인스턴스 이름 (예: \ $SERVERNAME \ $ \\ \ $SQLINSTANCENAME)으로 **데이터 원본** 값을 업데이트 합니다.

5. 복구 된 데이터베이스 이름으로 **초기 카탈로그** 값을 업데이트 합니다.

6. 이 프로세스를 자동화 하려면 Windows PowerShell 명령 프롬프트를 사용 하 여 관리 및 모니터링 서버에 다음과 유사한 명령줄을 입력 하면 됩니다.

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >이 연결 문자열은 모든 로컬 MBAM 웹 응용 프로그램에서 공유 합니다. 따라서 서버 당 한 번만 업데이트 해야 합니다.


7. 다음 표를 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

   |매개 변수 | 설명 |
   |---------|------------|
   |$SERVERNAME $ \ $SQLINSTANCENAME $ | 복구 데이터베이스가 있는 SQL Server의 서버 이름 및 인스턴스|
   |$DATABASE $|복구 된 데이터베이스의 이름입니다.|

### MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행

1.  서버 B에 MBAM 2.5 서버 소프트웨어를 설치 합니다. 자세한 내용은 [MBAM 2.5 서버 소프트웨어 설치](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software)를 참조 하세요.

2.  서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **준수 및 감사 데이터베이스** 기능만 선택 합니다. 데이터베이스를 구성 하는 방법에 대 한 자세한 내용은 [MBAM 2.5 데이터베이스를 구성](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases)하는 방법을 참조 하세요.

    >[!TIP]
    >또는 **사용-MbamDatabase** Windows PowerShell cmdlet을 사용 하 여 규정 준수 및 감사 데이터베이스를 구성할 수 있습니다.


### 관리 및 모니터링 웹 사이트 인스턴스 다시 시작

관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 시작 합니다.

이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>이 명령을 실행 하려면 windows powershell 용 IIS 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.
