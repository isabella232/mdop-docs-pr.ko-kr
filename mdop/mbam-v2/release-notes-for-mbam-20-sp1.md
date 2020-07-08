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
# MBAM 2.0 SP1 릴리스 정보


이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.

이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)을 설치 하기 전에 자세히 읽어 보세요. 이 릴리스 정보에는 BitLocker 관리 및 모니터링 2.0 SP1을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있으며, 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 정보와 다른 MBAM 2.0 SP1 설명서 사이에 차이가 있는 경우 최신 변경 내용을 신뢰할 수 있는 것으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> MBAM 2.0 SP1의 알려진 문제점


이 섹션에는 MBAM 2.0 SP1에 대 한 알려진 문제가 포함 되어 있습니다.

### Mbam 2.0 SP1에 대 한 Configuration Manager 통합 토폴로지로 MBAM을 업그레이드 하려면 Configuration Manager 개체의 수동 제거 필요

구성 관리자에서 MBAM을 사용 하는 경우 MBAM 2.0 SP1으로 업그레이드 하려면 MBAM 설치의 일부로 Configuration Manager에 설치 된 모든 Configuration Manager 개체를 수동으로 제거 해야 합니다. 수동으로 제거 해야 하는 개체는 MBAM 보고서, MBAM 지원 컴퓨터 모음, BitLocker 보호 구성 기준 및 연결 된 구성 항목입니다.

**해결 방법**: 다음 단계를 완료 하 여 Configuration Manager 개체를 업그레이드 합니다.

1.  다음 단계에 설명 된 대로 기존 준수 데이터를 외부 파일에 백업 합니다.

    **참고**  Configuration Manager에서 기존 기준을 삭제 하면 기존의 모든 BitLocker 준수 데이터가 삭제 됩니다. 데이터는 시간에 따라 다시 생성 되지만, 규정 준수 데이터를 다시 생성 하기 전에 특정 컴퓨터에 대 한 규정 준수 데이터가 필요한 경우에 대비 하 여 데이터 복사본을 저장 하는 것이 좋습니다.

     

    1.  BitLocker 준수 데이터 기록을 저장 하려면 **Bitlocker 엔터프라이즈 준수 정보** 보고서를 엽니다.

    2.  보고서에서 **저장** 아이콘을 클릭 하 고 **Excel**을 선택 합니다.

        저장 된 보고서에는 컴퓨터 이름, 도메인 이름, 준수 상태, 예외, 장치 사용자, 준수 상태 정보, 마지막 연락 날짜/시간 등의 데이터가 포함 됩니다. 자세한 볼륨 정보 및 암호화 강도와 같은 일부 정보는 저장 되지 않습니다.

2.  **Mbam** 설치 관리자를 사용 하 여 서버에서 **mbam** 을 제거 합니다.

3.  Configuration Manager에서 다음 개체를 수동으로 삭제 합니다.

    -   MBAM 지원 컴퓨터 모음

    -   BitLocker Protection 기준

    -   BitLocker 운영 체제 드라이브 보호 구성 항목

    -   BitLocker 고정 데이터 드라이브 보호 구성 항목

4.  Configuration Manager SQL Server Reporting Services 사이트에서 MBAM 보고서 폴더를 수동으로 삭제 합니다. 이렇게 하려면 다음을 수행합니다.

    1.  Internet Explorer를 사용 하 여 보고 서비스 지점을 찾습니다 (예: http:// &lt; /reports. server). &gt;

    2.  적절 한 구성 관리자 사이트 코드 링크를 클릭 합니다.

    3.  MBAM 폴더를 삭제 합니다.

5.  MBAM 서버 설치 관리자를 사용 하 여 Configuration Manager 통합 개체를 다시 설치 합니다. 클라이언트 컴퓨터는 시간에 따라 BitLocker 준수 데이터를 다시 업로드 하기 시작 합니다.

### 셀프 서비스 포털의 제출 단추가 인터넷 Explorer10에서 작동 하지 않음

인터넷 Explorer10을 사용 하 여 관리 및 모니터링 웹 사이트에 액세스 하면 웹 사이트의 **제출** 단추가 작동 하지 않습니다.

**해결 방법**: 관리 및 모니터링 웹 사이트를 설치한 서버에서 [ASP.NET browser 정의 파일에 대 한 핫픽스](https://go.microsoft.com/fwlink/?LinkId=317798)를 설치 합니다.

### 국제 도메인 이름은 지원 되지 않음

MBAM 2.0 SP1은 국제 도메인 이름을 지원 하지 않습니다.

**해결 방법**: 없음

### SSL이 SSRS에 구성 되어 있지 않은 경우 관리 및 모니터링 웹 사이트의 보고서에 경고가 표시 됨

SQLServer Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 설치 하면 보고서의 URL이 HTTPS 대신 HTTP로 설정 됩니다. 그런 다음 관리 및 모니터링 웹 사이트로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 표시 됩니다.

**해결 방법**:이 문제를 해결 하려면 **Reporting services 구성 관리자** 에서 SQLServer reporting services가 설치 되어 있는 mbam 서버의 SSL을 구성 합니다. 관리 및 모니터링 서버 웹 사이트를 제거한 다음 다시 설치 합니다.

### 규정 준수 요약 보고서에서 뒤로를 클릭 하면 오류가 발생할

준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.

**해결 방법**: 없음

### 사용 된 공간만 암호화가 올바르게 작동 하지 않음

MBAM 클라이언트를 설치한 후 처음으로 컴퓨터를 암호화 하 고 사용 된 공간만 암호화를 구현 하도록 그룹 정책 개체를 설정한 경우, MBAM이 디스크의 사용 된 공간만 암호화 하는 대신 전체 디스크를 잘못 암호화 합니다. MBAM 클라이언트를 설치 하기 전에 사용 된 공간만 암호화로 컴퓨터를 암호화 하 고 동일한 사용 공간만 암호화 그룹 정책 개체를 설정한 경우 MBAM은 설정을 인식 하 고 준수 보고서에 암호화를 올바르게 보고 합니다.

**해결 방법**: 없음

### 컴퓨터 준수 보고서에 암호화 강도가 잘못 표시 됨

**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 수준을 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 컴퓨터 준수 **보고서에 항상 암호 강도가 표시 되지** 않습니다. 그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.

**해결 방법**: **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.

### 드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨

SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.

**해결 방법**: 없음 MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.

### 보안 강화 구성으로 인해 보고서가 올바르게 표시 되지 않을 수 있음

Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 **액세스 거부** 메시지가 나타날 수 있습니다. 기본적으로 보안 강화 구성은 웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 설정 됩니다.

**해결 방법**: Mbam 서버에서 보고서를 보려고 할 때 **액세스 거부** 메시지가 나타나면 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다. 또는 고급 보안 구성을 사용할 수 없는 다른 컴퓨터의 보고서를 볼 수도 있습니다.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> SQLServer2008에서 SQLServer2012로 업그레이드 하면 MBAM 설치가 실패 함

SQLServer2008에서 SQLServer2012로 업그레이드 한 다음 준수 및 감사 데이터베이스 또는 복구 데이터베이스를 설치 하려고 하면 설치가 실패 하 고 롤백됩니다. 이 오류는 SQLServer를 업그레이드 하는 동안 필요한 SQLCMD.exe 파일이 제거 되었고 MBAM 설치 관리자에서 찾을 수 없기 때문에 발생 합니다. MSI 로그 파일 줄은 다음과 유사 하 게 표시 될 수 있습니다.

RunDbInstallScript Recovery Db CA: BinDir E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exe-RunDbInstallScript 복구 Db CA: dbInstance-xxxxxx\\I01RunDbInstallScript 복구 Db CA: sqlScript-C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript 복구 Db CA: defaultFileName-MBAM \ _Recovery \ _and 복구 Db CA: defaultDataPath-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\program files Files\\Microsoft\\Microsoft BitLocker 관리 및 Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript Recovery Db CA: 복구 데이터베이스 설치 scriptRunDbInstallScript 복구 Db CA를 실행 하는 중: Sqlcmd 로그 파일이 C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript 복구 Db CA 예외: 설치 복구 데이터베이스 사용자 지정 작업 명령 명령줄 출력 예외: 시스템에서 지정 된 파일을 찾을 수 없습니다.

MBAM 서버 Windows Installer는 HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.에서 레지스트리의 경로 문자열 값을 검색 하 여 SQLCMD.exe 경로를 찾기 위해 하드 코드 됩니다. SQLServer2008에서 SQLServer2012으로 마이그레이션하는 동안 키가 계속 표시 되지만, SQLupgrade 프로세스가 파일을 제거 했으므로 데이터 값이 참조 하는 경로에 SQLCMD.exe 파일이 포함 되어 있지 않습니다.

**해결 방법**: HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path 문자열 값의 이름을 **\ _old 경로로**설정한 다음 Mbam 서버에서 Windows Installer를 다시 실행 합니다. 설치가 성공적으로 완료 되 고 SQLServer2012에서 데이터베이스를 만드는 경우 **경로 \ _old** 경로를 **경로로**바꿉니다.

## MBAM 2.0 SP1에 대 한 핫픽스 및 지식 기반 문서


이 섹션에는 MBAM 2.0 SP1에 대 한 핫픽스와 KB 문서가 포함 되어 있습니다.

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


[MBAM 2.0 SP1 정보](about-mbam-20-sp1.md)

 

 





