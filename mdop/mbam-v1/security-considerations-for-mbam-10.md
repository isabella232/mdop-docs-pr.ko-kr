---
title: MBAM 1.0에 대한 보안 고려 사항
description: MBAM 1.0에 대한 보안 고려 사항
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826193"
---
# MBAM 1.0에 대한 보안 고려 사항


이 항목에서는 계정 및 그룹, 로그 파일, Microsoft BitLocker 관리 및 모니터링 (MBAM)에 대 한 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 다룹니다. 자세한 내용은이 문서의 링크를 따르세요.

## 일반 보안 고려 사항


**보안 위험을 파악 합니다.** MBAM의 가장 심각한 위험은 BitLocker 암호화를 다시 구성 하 고 MBAM 클라이언트에서 BitLocker 암호화 키 데이터를 얻을 수 있는 권한이 없는 사용자가 해당 기능을 도용 했을 수 있다는 것입니다. 그러나 서비스 거부 공격으로 인해 짧은 시간 동안에는 MBAM 기능이 손실 되는 것은 일반적으로 치명적인 영향을 받지 않습니다.

**컴퓨터를 물리적으로 보호**합니다. 보안이 완전 하지 않음 (물리적 보안 없음). MBAM 서버에 대 한 실제 액세스 권한이 있는 사용자는 모두 클라이언트 기반을 공격할 수 있습니다. 모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다. MBAM 서버는 제어 된 액세스 권한이 있는 물리적으로 안전한 서버 방에 저장 되어야 합니다. 운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.

**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다. 보안 알림 서비스 ()에 가입 하 여 운영 체제, Microsoft SQL Server 및 MBAM에 대 한 새 업데이트에 대 한 정보를 지속적으로 유지 <https://go.microsoft.com/fwlink/p/?LinkId=28819> 합니다.

**강력한 암호 또는 암호 문구를 사용**합니다. 항상 모든 MBAM 및 MBAM 관리자 계정에 대해 15 개 이상의 문자로 강력한 암호를 사용 합니다. 빈 암호를 사용 하지 마세요. 암호 개념에 대 한 자세한 내용은 TechNet ()의 "계정 암호 및 정책" 백서를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=30009> .

## MBAM의 계정 및 그룹


사용자 계정 관리에 대 한 모범 사례는 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다. 그런 다음 MBAM 서버의 필요한 MBAM 로컬 그룹에 도메인 글로벌 계정을 추가 합니다.

### ActiveDirectoryDomainServices 그룹

MBAM 설정 중 그룹이 자동으로 만들어지지 않습니다. 그러나 MBAM 작업을 관리 하려면 다음 ActiveDirectoryDomainServices 전역 그룹을 만들어야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 이름</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>이 그룹을 만들어 MBAM 설정 중에 만든 MBAM 고급 헬프 데스크 사용자 로컬 그룹의 구성원을 관리할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 준수 감사 DB 액세스</p></td>
<td align="left"><p>MBAM 설정 중에 만든 MBAM 준수 감사 DB 액세스 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 하드웨어 사용자</p></td>
<td align="left"><p>MBAM 설정 중에 만든 MBAM 하드웨어 사용자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>MBAM 설정 중에 만든 MBAM 헬프데스크 사용자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 복구 및 하드웨어 DB 액세스</p></td>
<td align="left"><p>MBAM 설정 중에 만든 MBAM 복구 및 하드웨어 DB 액세스 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 보고서 사용자</p></td>
<td align="left"><p>MBAM 설정 중에 만든 MBAM 보고서 사용자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 시스템 관리자</p></td>
<td align="left"><p>MBAM 설정 중에 만든 MBAM 시스템 관리자 로컬 그룹의 구성원을 관리 하려면이 그룹을 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker 암호화 예외</p></td>
<td align="left"><p>이 그룹을 만들어 로그온 하는 컴퓨터에서 시작 하는 BitLocker 암호화에서 제외 해야 하는 사용자 계정을 관리할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### MBAM 서버 로컬 그룹

MBAM 설치는 MBAM 작업을 지 원하는 로컬 그룹을 만듭니다. ActiveDirectoryDomainServices 글로벌 그룹을 해당 MBAM 로컬 그룹에 추가 하 여 MBAM 보안 및 데이터 액세스 권한을 구성 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 이름</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 헬프데스크 기능에 대 한 액세스를 확장 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 준수 감사 DB 액세스</p></td>
<td align="left"><p>이 그룹에는 MBAM 준수 감사 데이터베이스에 액세스할 수 있는 컴퓨터가 포함 되어 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 하드웨어 사용자</p></td>
<td align="left"><p>이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 몇 가지 하드웨어 기능 기능에 액세스할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 일부 헬프 데스크 기능에 액세스할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 복구 및 하드웨어 DB 액세스</p></td>
<td align="left"><p>이 그룹에는 MBAM 복구 및 하드웨어 데이터베이스에 액세스할 수 있는 컴퓨터가 포함 되어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 보고서 사용자</p></td>
<td align="left"><p>이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 규정 준수 및 감사 보고서에 액세스할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 시스템 관리자</p></td>
<td align="left"><p>이 그룹의 구성원은 Microsoft BitLocker 관리 및 모니터링의 모든 기능에 액세스할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### SSRS 보고서 액세스 계정

SSRS (SQL Server Reporting Services) 보고서 서비스 계정은 보안 컨텍스트를 제공 하 여 SSRS를 통해 사용할 수 있는 MBAM 보고서를 실행 합니다. 이 계정은 MBAM 설정 중에 구성 됩니다.

## MBAM 로그 파일


MBAM 설정 중에 다음 MBAM 설정 로그 파일은 다음을 설치 하는 사용자 의% temp% 폴더에 만들어집니다.

**MBAM 서버 설정 로그 파일**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; 5 임의 문자 &gt; </em> 로그  
MBAM 설정 및 MBAM 서버 기능 설치 중 취한 동작을 기록 합니다.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase  
MBAM 준수 상태 데이터베이스 설정을 만들기 위해 수행한 작업을 기록 합니다.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase  
MBAM 복구 및 하드웨어 데이터베이스를 만들기 위해 수행한 작업을 기록 합니다.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers  
MBAM 준수 상태 데이터베이스에서 SQL Server 로그인을 만들기 위해 수행한 작업을 기록 하 고 보고서에 대 한 데이터베이스에 헬프데스크 웹 서비스를 승인 합니다.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers  
키 복구용으로 웹 서비스에 권한을 부여 하기 위해 수행한 작업을 로그 하 고 MBAM 복구 및 하드웨어 데이터베이스에 대 한 로그인을 만듭니다.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers  
웹 서비스를 준수 보고를 위해 MBAM 준수 상태 데이터베이스에 대 한 권한을 부여 하기 위해 수행한 작업을 기록 합니다.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers  
웹 서비스에 대 한 MBAM 및 키 복구에 대 한 하드웨어 데이터베이스 권한을 부여 하기 위해 수행한 작업을 기록 합니다.

**참고**  추가 MBAM 설치 로그 파일을 얻으려면 **msiexec** 패키지 및 **/l** 위치 옵션을 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 해야 합니다 &lt; &gt; . 로그 파일은 지정 된 위치에 만들어집니다.

 

**MBAM 클라이언트 설치 로그 파일**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; 5 임의 문자 &gt; </em> 로그  
MBAM 클라이언트 설치 중 수행 되는 작업을 기록 합니다.

## MBAM 데이터베이스 TDE 고려 사항


SQL Server 2008에서 사용할 수 있는 TDE (투명 한 데이터 암호화) 기능은 MBAM 데이터베이스 기능을 호스팅하는 데이터베이스 인스턴스의 필수 설치 필수 구성 요소입니다.

TDE를 사용 하 여 실시간 전체 데이터베이스 수준의 암호화를 수행할 수 있습니다. TDE는 규정 준수 또는 기업 데이터 보안 표준을 충족 하기 위해 일괄 암호화를 위해 적합 합니다. TDE는 파일 수준에서 작동 하며, EFS (암호화 파일 시스템) 및 BitLocker 드라이브 암호화 (둘 다 하드 드라이브의 데이터를 암호화 하는 두 가지 Windows 기능)와 유사 합니다. TDE는 셀 수준 암호화, EFS 또는 BitLocker를 대체 하지 않습니다.

데이터베이스에서 TDE를 사용 하도록 설정 하면 모든 백업이 암호화 됩니다. 따라서 데이터베이스 암호화 키 (DEK)를 보호 하는 데 사용 된 인증서가 데이터베이스 백업과 함께 백업 되 고 유지 되도록 주의를 기울여야 합니다. 인증서가 없으면 데이터를 읽을 수 없습니다. 데이터베이스와 함께 인증서를 백업 합니다. 각 인증서 백업에는 두 개의 파일이 있어야 합니다. 이러한 파일은 모두 보관 되어야 합니다. 보안을 위해 데이터베이스 백업 파일과 별도로 보관 하는 것이 좋습니다.

MBAM 데이터베이스 인스턴스의 TDE를 사용 하도록 설정 하는 방법에 대 한 예제는 [mbam 1.0 계산](evaluating-mbam-10.md)을 참조 하세요.

SQLServer 2008의 TDE에 대 한 자세한 내용은 [SQL Server 2008 Enterprise Edition에서 데이터베이스 암호화](https://go.microsoft.com/fwlink/?LinkId=269703)를 참조 하세요.

## 관련 항목


[MBAM 1.0에 대한 보안 및 개인 정보](security-and-privacy-for-mbam-10.md)

 

 





