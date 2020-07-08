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
# MBAM 1.0 기능을 다른 컴퓨터로 이동하는 방법


이 항목에서는 하나 이상의 Microsoft BitLocker 관리 및 모니터링 (MBAM) 기능을 다른 컴퓨터로 이동 하는 데 필요한 단계에 대해 설명 합니다. 두 개 이상의 MBAM 기능을 다른 컴퓨터로 이동 하는 경우 다음 순서로 이동 해야 합니다.

1.  복구 및 하드웨어 데이터베이스

2.  준수 및 감사 데이터베이스

3.  규정 준수 및 감사 보고서

4.  관리 및 모니터링

## 복구 및 하드웨어 데이터베이스를 이동 하려면


다음 절차를 사용 하 여 MBAM 복구 및 하드웨어 데이터베이스를 다른 컴퓨터로 이동할 수 있습니다 (이 MBAM 서버 기능을 서버 A에서 서버 B로 이동할 수 있음).

****

1.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.

2.  서버 B에서 MBAM 설정을 실행 합니다.

3.  서버 A에서 MBAM 복구 및 하드웨어 데이터베이스를 백업 합니다.

4.  MBAM 복구 및 서버 A에서 B로의 하드웨어 데이터베이스

5.  서버 B에서 MBAM 복구 및 하드웨어 데이터베이스 복원

6.  서버 B에서 MBAM 복구 및 하드웨어 데이터베이스에 대 한 액세스를 구성 합니다.

7.  MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터 업데이트

8.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작

**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 하려면**

1.  IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 MBAM 웹 사이트를 중지 합니다. MBAM 웹 사이트는 **Microsoft BitLocker 관리 및 모니터링**이라고 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령 프롬프트에서 명령을 사용할 수 있습니다.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **참고**  
    이 PowerShell 명령 프롬프트를 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다. 또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.



**서버 B에서 MBAM 설정 실행**

1.  서버 B에서 MBAM 설정을 실행 하 고 설치할 복구 및 하드웨어 데이터베이스를 선택 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령 프롬프트에서 명령을 사용할 수 있습니다.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **참고**  
    위의 예제에서 다음 값을 환경과 일치 하는 항목으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스가 이동 되는 서버와 인스턴스 이름을 입력 합니다.

    -   $DOMAIN $ \\ $SERVERNAME $-복구 및 하드웨어 데이터베이스에 연결 될 각 MBAM 응용 프로그램과 모니터링 서버의 도메인 및 서버 이름을 입력 합니다. 도메인 및 서버 이름이 여러 개인 경우에는 세미콜론을 사용 하 여 목록에서 각각을 구분 합니다. 예를 들어 $DOMAIN \\SERVERNAME $; $DOMAIN \\ $SERVERNAME $ $). 또한 각 서버 이름 뒤에는가와 야 합니다 **$** . 예를 들어 MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.



**서버 A의 데이터베이스를 백업 하려면**

1.  서버 A에서 복구 및 하드웨어 데이터베이스를 백업 하려면 SQL Server Management Studio를 사용 하 고 **백업**이라는 작업을 시작 합니다. 기본적으로 데이터베이스 이름은 **Mbam 복구 및 하드웨어 데이터베이스**입니다.

2.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

    MBAM 복구와 하드웨어 데이터베이스를 수정 하 여 full 복구 모드를 사용 합니다.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    MBAM 복구와 하드웨어 데이터베이스 데이터 및 MBAM 복구 논리 백업 장치를 만듭니다.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    전체 MBAM 복구 및 하드웨어 데이터베이스를 백업 합니다.

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

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $PASSWORD $-개인 키 파일을 암호화 하는 데 사용 되는 암호를 입력 합니다.



3.  다음과 유사한 SQL Server PowerShell 및 명령을 사용 하 여 SQL 파일을 실행 합니다.

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스를 백업 하는 서버와 인스턴스의 이름을 입력 합니다.



**데이터베이스 및 인증서를 서버 A에서 B로 이동 하려면**

1.  Windows 탐색기를 사용 하 여 MBAM 복구 및 하드웨어 데이터베이스 데이터 .bak를 서버 A에서 서버 B로 이동 합니다.

2.  암호화 된 데이터베이스의 인증서를 이동 하려면 다음의 자동화 단계를 사용 해야 합니다. 이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $-파일을 복사 하는 대상 서버의 이름을 입력 합니다.

    -   $DESTINATIONSHARE $-공유 이름과 파일을 복사할 경로를 입력 합니다.



**서버 B에서 데이터베이스를 복원 하려면**

1.  SQL Server Management Studio와 **Restore database**라는 작업을 사용 하 여 서버 B의 복구 및 하드웨어 데이터베이스를 복원 합니다.

2.  작업이 실행 되 면 **장치에서** 옵션을 선택 하 여 데이터베이스 백업 파일을 선택한 다음 **추가** 명령을 사용 하 여 Mbam 복구 및 하드웨어 데이터베이스 **데이터 .bak** 파일을 선택 합니다.

3.  **확인** 을 선택 하 여 복원 프로세스를 완료 합니다.

4.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    MBAM 설정으로 만든 인증서를 삭제 합니다.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    인증서 추가

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

    MBAM 복구와 하드웨어 데이터베이스 데이터 및 로그 파일을 복원 합니다.

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $PASSWORD $-개인 키 파일을 암호화 하는 데 사용한 암호를 입력 합니다.



5.  Windows PowerShell을 사용 하 여 다음과 같은 명령줄을 입력 합니다.

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **참고**  
    Receding 예제의 값을 해당 환경과 일치 하는 항목으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-서버 이름과 복구 및 하드웨어 데이터베이스가 복원 되는 인스턴스를 입력 합니다.



**서버 B에서 데이터베이스에 대 한 액세스 구성**

1.  서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 복구 및 하드웨어 DB 액세스**라는 로컬 그룹에 추가 합니다.

2.  이 절차를 자동화 하려면 서버 B의 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **참고**  
    이전 예제의 값을 해당 환경에 해당 하는 값으로 바꿉니다.

    -   $DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 이름과 컴퓨터 이름을 입력 합니다. 서버 이름 뒤에는 a가와 야 합니다 **$** (예: MyDomain\\MyServerName1 $).



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 하려면**

1. MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 웹 사이트에서 호스팅되는 다음 응용 프로그램에 대 한 연결 문자열 정보를 업데이트 합니다.

   -   MBAM 관리 서비스

   -   MBAM 복구 및 하드웨어 서비스

2. 각 응용 프로그램을 선택 하 고 **기능 뷰의** **관리** 섹션에 있는 **구성 편집기** 기능을 사용 합니다.

3. 섹션 목록 컨트롤에서 **Configurationstrings** 옵션을 선택 합니다.

4. **(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.

5. **컬렉션 편집기**에서 ' MBAMAdministrationService ' 응용 프로그램에 대 한 구성을 업데이트할 때 **keyrecoveryconnectionstring** 이라는 행을 선택 하거나 <strong> Microsoft RecoveryAndHardwareDataStore </strong> 라는 행을 선택 합니다. ' MBAMRecoveryAndHardwareService '에 대 한 구성을 업데이트 하는 경우 ConnectionString.

6. 서버 이름과 복구 및 하드웨어 데이터베이스가 이동 된 인스턴스를 나열 하도록 **Configurationstrings** 속성에 대 한 **데이터 원본 =** 값을 업데이트 합니다. 예를 들어 $ \\ \ $SQLINSTANCENAME $를 $SERVERNAME 합니다.

7. 이 절차를 자동화 하려면 각 관리 및 모니터링 서버에서 Windows PowerShell을 사용 하 여 다음과 유사한 명령을 사용할 수 있습니다.

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **참고**  
   이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

   -   $SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.



**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## 준수 상태 데이터베이스 기능을 이동 하려면


서버 A에서 서버 B와 같이 컴퓨터 간에 MBAM 준수 상태 데이터베이스 기능을 이동 하려면 다음 절차를 사용 해야 합니다.

1.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지

2.  서버 B에서 MBAM 설정 실행

3.  서버 A에서 데이터베이스를 백업 합니다.

4.  데이터베이스를 서버 A에서 B로 이동

5.  서버 B에서 데이터베이스 복원

6.  서버 B에서 데이터베이스에 대 한 액세스 권한 구성

7.  MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터 업데이트

8.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작

**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **참고**  
    이 명령을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다. 또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.



**서버 B에서 MBAM 설정 실행**

1.  서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 준수 상태 데이터베이스 기능을 선택 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 이동 될 서버 이름과 인스턴스를 입력 합니다.

    -   $DOMAIN $ \\ $SERVERNAME $-준수 상태 데이터베이스에 연결 되는 각 MBAM 응용 프로그램과 모니터링 서버의 도메인 이름과 서버 이름을 입력 합니다. 여러 도메인 이름과 서버 이름이 있는 경우 세미콜론을 사용 하 여 목록에서 각각을 구분 합니다. 예를 들어 $DOMAIN \\SERVERNAME $; $DOMAIN \\ $SERVERNAME $ $). 각 서버 이름 뒤에는이 예제에 나와 있는 a가와 야 합니다 **$** . 예를 들어 MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.

    -   $DOMAIN $ \\ $USERNAME $-규정 준수 및 감사 보고서 기능에서 준수 상태 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.



**서버 A의 규정 준수 데이터베이스를 백업 하려면**

1.  서버 A에서 규정 준수 데이터베이스를 백업 하려면 SQL Server Management Studio를 사용 하 고 **백업**이라는 작업을 시작 합니다. 기본적으로 데이터베이스 이름은 **Mbam 준수 상태 데이터베이스**입니다.

2.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

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

3.  SQL Server PowerShell을 사용 하 여 다음과 유사한 명령을 사용 하 여 SQL 파일을 실행 합니다.

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 백업 될 서버 이름과 인스턴스를 입력 합니다.



**데이터베이스를 서버 A에서 B로 이동 하려면**

1.  Windows 탐색기를 사용 하 여 서버 A에서 서버 B로 다음 파일을 이동 합니다.

    -   MBAM 준수 상태 데이터베이스 데이터 .bak

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $-파일이 복사 될 서버 이름을 입력 합니다.

    -   $DESTINATIONSHARE $-파일이 복사 될 공유 이름과 경로를 입력 합니다.



**서버 B에서 데이터베이스를 복원 하려면**

1.  SQL Server Management Studio와 " **복원 데이터베이스**" 작업을 사용 하 여 서버 B의 준수 상태 데이터베이스를 복원 합니다.

2.  작업이 실행 되 면 장치에서 옵션을 선택 하 여 데이터베이스 백업 파일을 선택 하 고 추가 명령을 사용 하 여 MBAM 준수 상태 데이터베이스 데이터 .bak 파일을 선택 합니다. 확인을 클릭 하 여 복원 프로세스를 완료 합니다.

3.  이 절차를 자동화 하려면 다음 SQL 스크립트를 포함 하는 SQL 파일 (.sql)을 만듭니다.

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  SQL Server PowerShell을 사용 하 여 다음과 유사한 명령을 사용 하 여 SQL 파일을 실행 합니다.

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 복원 될 서버 이름과 인스턴스를 입력 합니다.



**서버 B에서 데이터베이스에 대 한 액세스를 구성 하려면**

1.  서버 B에서는 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 **Mbam 준수 상태 DB 액세스**라는 로컬 그룹에 추가 합니다.

2.  이 절차를 자동화 하려면 서버 B에서 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **참고**  
    이전 예제의 값을 해당 환경에 해당 하는 값으로 바꿉니다.

    -   $DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다. 서버 이름 뒤에는가와 야 합니다 **$** . 예를 들어 MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 Microsoft BitLocker 관리 및 모니터링 웹 사이트에서 호스팅되는 다음 응용 프로그램에 대 한 연결 문자열 정보를 업데이트 합니다.

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  각 응용 프로그램을 선택 하 고 **기능 뷰의** **관리** 섹션에 있는 **구성 편집기** 기능을 사용 합니다.

3.  섹션 목록 컨트롤에서 **Configurationstrings** 옵션을 선택 합니다.

4.  **(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 컬렉션 편집기를 엽니다.

5.  **컬렉션 편집기**에서 MBAMAdministrationService 응용 프로그램에 대 한 구성을 업데이트 하는 경우 **ComplianceStatusConnectionString**이라는 행을 선택 하 고, MBAMComplianceStatusService에 대 한 구성을 업데이트 하는 경우에는 **Windows 용 데이터 저장소 ConnectionString**이라는 이름의 행 또는 Microsoft.

6.  서버 이름과 인스턴스 이름을 나열 하도록 **Configurationstrings** 속성에 대 한 **데이터 원본 =** 값을 업데이트 합니다. 예를 들어 복구 및 하드웨어 데이터베이스가 이동 된 $SERVERNAME $ \\ $SQLINSTANCENAME.

7.  이 절차를 자동화 하기 위해 Windows PowerShell을 사용 하 여 각 관리 및 모니터링 서버에서 다음과 유사한 명령을 입력할 수 있습니다.

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-복구 및 하드웨어 데이터베이스가 있는 서버 이름과 인스턴스 이름을 입력 합니다.



**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.

    **PS C:\\ &gt; 시작-웹 사이트 "Microsoft BitLocker 관리 및 모니터링"**

## 규정 준수 및 감사 보고서를 이동 하려면


컴퓨터 간에 MBAM 준수 및 감사 보고서를 이동 하도록 선택 하면 (특히, 서버 A에서 서버 B로 이동 하는 경우) 다음 절차와 단계를 사용 해야 합니다.

1.  서버 B에서 MBAM 설정 실행

2.  서버 B의 준수 및 감사 보고서에 대 한 액세스 구성

3.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 중지

4.  MBAM 관리 및 모니터링 서버에서 보고서 연결 데이터 업데이트

5.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스 다시 시작

**서버 B에서 MBAM 설정 실행**

1.  서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 준수 및 감사 기능만 선택 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-준수 상태 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.

    -   $DOMAIN $ \\ $USERNAME $-규정 준수 및 감사 보고서 기능에서 준수 상태 데이터베이스에 연결 하는 데 사용할 도메인 이름과 사용자 이름을 입력 합니다.

    -   $PASSWORD $-준수 상태 데이터베이스에 연결 하는 데 사용 되는 사용자 계정의 암호를 입력 합니다.



**서버 B의 준수 및 감사 보고서에 대 한 액세스를 구성 하려면**

1.  서버 B에서 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 규정 준수 및 감사 보고서에 액세스할 수 있는 사용자 계정을 추가 합니다. "MBAM 보고서 사용자" 라는 로컬 그룹에 사용자 계정을 추가 합니다.

2.  이 절차를 자동화 하려면 서버 B에서 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **참고**  
    앞의 예제에서 다음 값을 환경에 적용할 수 있는 값으로 바꿉니다.

    -   $DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 중지 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**MBAM 관리 및 모니터링 서버에서 데이터베이스 연결 데이터를 업데이트 하려면**

1. MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 준수 보고서 URL을 업데이트 합니다.

2. **Microsoft BitLocker 관리 및 모니터링** 웹 사이트를 선택 하 고 **기능 보기**의 **관리** 섹션에서 찾을 수 있는 **구성 편집기** 기능을 사용 합니다.

3. 섹션 목록 컨트롤에서 **appSettings** 옵션을 선택 합니다.

4. 여기에서 **(Collection)** 이라는 행을 선택 하 고 행의 오른쪽에 있는 단추를 선택 하 여 **컬렉션 편집기** 를 엽니다.

5. **컬렉션 편집기**에서 "Microsoft. m l. Reports." 라는 행을 선택 합니다.

6. 서버 B에 대 한 서버 이름을 반영 하도록 Microsoft Mbam. u m l의 값을 업데이트 합니다. 규정 준수 및 감사 보고서 기능이 명명 된 SQL Reporting Services 인스턴스에 설치 되어 있는 경우 해당 URL에 대 한 인스턴스의 이름을 추가 하거나 업데이트 해야 합니다. 예를 들어 http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/Pages....

7. 이 절차를 자동화 하기 위해 Windows PowerShell을 사용 하 여 각 관리 및 모니터링 서버에서 다음과 유사한 명령을 입력할 수 있습니다.

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **참고**  
   이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

   -   $SERVERNAME $-규정 준수 및 감사 보고서가 설치 된 서버의 이름을 입력 합니다.

   -   $SRSINSTANCENAME $-규정 준수 및 감사 보고서가 설치 된 SQL Reporting Services 인스턴스의 이름을 입력 합니다.



**MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 다시 시작 하려면**

1.  MBAM 관리 및 모니터링 기능을 실행 하는 각 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 **Microsoft BitLocker 관리 및 모니터링**이라는 mbam 웹 사이트를 시작 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **참고**  
    이 명령을 실행 하려면 PowerShell 용 IIS 모듈을 현재 PowerShell 인스턴스에 추가 해야 합니다. 또한 스크립트를 실행할 수 있도록 PowerShell 실행 정책을 업데이트 해야 합니다.



## 관리 및 모니터링 기능을 이동 하려면


MBAM 관리 및 모니터링 보고서 기능을 한 컴퓨터에서 다른 컴퓨터로 이동 하도록 선택 하면 (서버 A에서 서버 B로 기능을 이동 하는 경우) 다음 절차를 사용 해야 합니다. 프로세스에는 다음 단계가 포함 됩니다.

1.  서버 B에서 MBAM 설정 실행

2.  서버 B에서 데이터베이스에 대 한 액세스 권한 구성

**서버 B에서 MBAM 설정 실행**

1.  서버 B에서 MBAM 설정을 실행 하 고 설치를 위해 관리 기능만 선택 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 사용할 수 있습니다.

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **참고**  
    이전 예제의 값을 해당 환경과 일치 하는 것으로 바꿉니다.

    -   $SERVERNAME $ \\ $SQLINSTANCENAME $-COMPLIDB \ _SQLINSTANCE 매개 변수에 대해 준수 상태 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다. RECOVERYANDHWDB \ _SQLINSTANCE 매개 변수에 대해 복구 및 하드웨어 데이터베이스가 있는 서버 이름과 인스턴스를 입력 합니다.

    -   $DOMAIN $ \\ $USERNAME $-규정 준수 및 감사 보고서 기능에서 준수 상태 데이터베이스에 연결 하는 데 사용 될 도메인 및 사용자 이름을 입력 합니다.

    -   $ REPORTSSERVERURL $-SQL Reporting Service 웹 사이트의 홈 위치에 대 한 URL을 입력 합니다. 보고서를 기본 SRS 인스턴스에 설치 하는 경우 URL 형식에 "http://$SERVERNAME $/ReportServer" 형식이 지정 됩니다. 보고서가 기본 SRS 인스턴스에 설치 되어 있는 경우 URL 형식이 "http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $"으로 지정 됩니다.



**데이터베이스에 대 한 액세스를 구성 하려면**

1.  복구와 하드웨어가 있는 서버나 서버에서 및 준수 및 감사 데이터베이스가 배포 되는 경우 서버 관리자의 로컬 사용자 및 그룹 스냅인을 사용 하 여 MBAM 관리 및 모니터링 기능을 실행 하는 각 서버의 컴퓨터 계정을 "MBAM 복구 및 하드웨어 DB (복구 및 하드웨어 DB Server)" 라는 로컬 그룹에 추가 하 고 "MBAM 준수 상태 DB 액세스" (준수 및 감사 DB 서버)를 선택 합니다.

2.  이 절차를 자동화 하려면 준수 및 감사 데이터베이스가 배포 된 서버에서 Windows PowerShell을 사용 하 여 다음과 유사한 명령을 사용할 수 있습니다.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  복구 및 하드웨어 데이터베이스가 배포 된 서버에서 Windows PowerShell을 사용 하 여 다음과 유사한 명령을 실행 합니다.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **참고**  
    이전 예제의 값을 해당 환경에 해당 하는 값으로 바꿉니다.

    -   $DOMAIN $ \\ $SERVERNAME $ $-MBAM 관리 및 모니터링 서버의 도메인 및 컴퓨터 이름을 입력 합니다. 서버 이름 뒤에는가와 야 합니다 **$** . 예를 들어 MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \\ $REPORTSUSERNAME $-규정 준수 및 감사 보고서에 대 한 데이터 원본을 구성 하는 데 사용 된 사용자 계정 이름을 입력 합니다.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## 관련 항목


[MBAM 1.0 기능 관리](administering-mbam-10-features.md)









