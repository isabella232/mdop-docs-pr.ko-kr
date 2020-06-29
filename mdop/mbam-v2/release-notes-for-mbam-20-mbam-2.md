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
# MBAM 2.0 릴리스 정보


이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.

Microsoft BitLockerAdministration 및 모니터링 (MBAM) 2.0을 설치 하기 전에이 릴리스 노트를 철저히 읽어 보세요. 이 릴리스 정보에는 Bits Locker관리 및 모니터링 2.0을 설치 하는 데 필요한 정보와 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 정보와 다른 MBAM 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## <a href="" id="---------mbam-2-0-known-issues"></a> MBAM 2.0 알려진 문제


이 섹션에서는 MBAM 2.0에 대 한 릴리스 정보를 포함 합니다.

### Microsoft System Center Configuration Manager 2007에서 MBAM을 실행할 때 BitLocker 컴퓨터 준수 및 BitLocker 엔터프라이즈 준수 세부 정보 보고서에 컴퓨터 이름 필드가 표시 되지 않을 수 있음

컴퓨터 이름 필드는 구성 관리자 2007에서 MBAM을 사용할 때 BitLocker 컴퓨터 규정 준수 및 BitLocker 엔터프라이즈 준수 세부 정보 보고서에서 비어 있을 수 있습니다.

해결 방법: 없음

### 독립 실행형 MBAM 서버 인프라를 업그레이드 한 후 엔터프라이즈 호환 보고서가 업데이트 되지 않음

MBAM 독립 실행형 토폴로지를 사용 하는 경우 서버 인프라를 버전 1.0에서 2.0로 업그레이드 하면 엔터프라이즈 준수 보고서가 업데이트 되지 않습니다.

해결 방법: 업그레이드 한 후 준수 및 감사 데이터베이스에서 다음 스크립트를 실행 합니다.

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

### SSL이 SSRS에 구성 되어 있지 않은 경우 지원 센터 포털의 보고서에 경고가 표시 됨

SQL Server Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 설치할 때 보고서에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다. 그런 다음 지원 센터 포털로 이동한 다음 보고서를 선택 하면 "보안 콘텐츠만 표시 됨" 메시지가 표시 됩니다.

해결 방법: 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다. 이 문제를 해결 하려면 SQL Server Reporting Services가 설치 되어 있는 MBAM 컴퓨터로 이동 하 여 **Reporting Services 구성 관리자**를 실행 한 다음 **웹 서비스 URL**을 클릭 합니다. 서버에 대 한 적절 한 SSL 인증서를 선택 하 고 적절 한 SSL 포트 (기본 포트 443)를 입력 한 다음 **적용**을 클릭 합니다.

### Configuration Manager 데이터베이스의 기본 인스턴스가 아닌 인스턴스는 지원 되지 않습니다.

MBAM은 Configuration Manager 2007 및 SystemCenter2012 ConfigurationManager에서 Configuration Manager 데이터베이스의 기본 인스턴스만 찾습니다. 비기본 인스턴스를 사용 하는 경우 MBAM을 설치할 수 없습니다.

해결 방법: 없음

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>준수 요약 보고서에서 "뒤로"를 클릭 하면 오류가 발생 하는 경우

준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.

해결 방법: 없음

### 사용 된 공간만 암호화가 올바르게 작동 하지 않음

MBAM 클라이언트를 설치한 후 처음으로 컴퓨터를 암호화 하 고 사용 된 공간만 암호화를 구현 하도록 그룹 정책 개체를 설정한 경우, MBAM이 디스크의 사용 된 공간만 암호화 하는 대신 전체 디스크를 잘못 암호화 합니다. MBAM 클라이언트를 설치할 때 컴퓨터가 이미 암호화 되어 있고 동일한 그룹 정책 개체를 설정한 경우 암호화가 올바르게 작동 하 고 컴퓨터에서 사용 된 디스크 공간만 암호화 합니다.

해결 방법: 없음

### 컴퓨터 준수 보고서에서 암호화 강도가 잘못 표시 됨

**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 수준을 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 컴퓨터 준수 보고서에 항상 암호화 강도로 "unknown"이 표시 됩니다. 그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.

해결 방법: **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.

### 드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨

SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.

해결 방법: 없음 MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.

### 보안 강화 구성으로 인해 보고서가 올바르게 표시 되지 않을 수 있음

Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 메시지가 표시 될 수 있습니다. 웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 기본적으로 ESC가 설정 됩니다.

해결 방법: MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 메시지가 나타나는 경우 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다. 또는 ESC가 설정 되지 않은 다른 컴퓨터에서 보고서를 볼 수도 있습니다.

### SQL Server 2008에서 SQL Server 2012로 업그레이드할 때 MBAM 서버 설치가 실패 함

SQL Server 2008에서 SQL Server 2012으로 업그레이드 한 다음 준수 및 감사 데이터베이스 또는 복구 데이터베이스를 설치 하려고 하면 설치가 실패 하 고 롤백됩니다. SQL 업그레이드 중 필요한 SQLCMD.exe 파일이 제거 되었고 MBAM 설치 관리자에서 찾을 수 없기 때문에 오류가 발생 합니다. MSI 로그 파일 줄은 다음과 유사 하 게 표시 될 수 있습니다.

RunDbInstallScript Recovery Db CA: BinDir E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exe-RunDbInstallScript 복구 Db CA: dbInstance-xxxxxx\\I01RunDbInstallScript 복구 Db CA: sqlScript-C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript 복구 Db CA: defaultFileName-MBAM \ _Recovery \ _and 복구 Db CA: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery Db CA: 복구 데이터베이스 설치 scriptRunDbInstallScript 복구 Db CA를 실행 하는 중: Sqlcmd 로그 파일이 C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript 복구 Db CA 예외: 설치 복구 데이터베이스 사용자 지정 작업 명령 명령줄 출력 예외: 시스템에서 지정 된 파일을 찾을 수 없습니다.

MBAM 서버 Windows Installer는 HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. 레지스트리에서 Path 문자열 값을 찾아 SQLCMD.exe 경로를 찾기 위해 하드 코드 됩니다. Sql Server 2008에서 SQL Server 2012로 마이그레이션하는 동안 키가 계속 표시 되지만, SQL 업그레이드 프로세스에서 해당 파일을 제거 했으므로 데이터 값이 참조 하는 경로에 SQLCMD.exe 파일이 포함 되어 있지 않습니다.

해결 방법: HKLM\\Software\\Microsoft\\Microsoft SQL Server\\1000tool\clientsetup 경로 문자열 값을 **Path \ _old**로 바꾼 다음 Mbam Server Windows Installer를 다시 실행 합니다. 설치가 성공적으로 완료 되 고 SQL Server 2012에서 데이터베이스를 만드는 경우 **경로 \ _old** 값을 **path**로 바꿉니다.

## MBAM 2.0 용 핫픽스와 기술 자료 문서


이 섹션에는 MBAM 2.0 용 핫픽스와 KB에 대 한 문서가 포함 되어 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>기술 자료 문서</strong></th>
<th align="left">제목</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>&quot;System CENTER CM 개체가 이미 설치 된 상태에서 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 설치 실패&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>사용자가 MBAM 2.0 셀프 서비스 포털을 사용 하 여 BitLocker 복구 키를 검색할 수 없음</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>MBAM 클라이언트가 이벤트 ID 4 및 오류 코드 0x8004100E와 함께 실패 함 이벤트 설명</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>MBAM에서 보고서 탭을 클릭 하면 "/Reports ' 응용 프로그램에서 오류 메시지" 서버 오류 발생 "</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>MBAM 엔터프라이즈 또는 컴퓨터 준수 보고서 열기 오류</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM Enterprise 보고서가 업데이트 되지 않음</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>도메인 컨트롤러에 MBAM을 설치 하는 것은 지원 되지 않습니다.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>MBAM 2.0의 독립 실행형 또는 Configuration Manager 통합 설정 중에 오류 코드 0x80071a90이 표시 됩니다.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM 및 보안 네트워크 통신</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Configuration Manager 통합 시나리오에서 SQL Server 2008와 함께 MBAM 2.0 설치가 실패 함</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>SQL SSRS가 올바르게 구성 되어 있지 않으면 MBAM이 실패 함</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>MBAM 2.0 &quot; &#39;Reporting Services 가리키기&#39; 역할에 대 한 Configuration Manager 서버 역할 설정을 검색 하는 동안 오류가 발생 하 여 설치에 실패 함&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>MBAM 2.0 Enterprise Reports는 SQL 작업 CreateCache 오류로 인해 MBAM 2.0 독립 실행형 토폴로지에서 새로 고쳐지지 않습니다.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM Enterprise 보고서가 업데이트 되지 않음</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM 지원 컴퓨터 규정 준수 보고에 지원 되지 않는 제품이 포함 되어 있지 않음</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>컴퓨터 레코드가 MBAM에서 거부 됨</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 2.0 정보](about-mbam-20-mbam-2.md)

 

 





