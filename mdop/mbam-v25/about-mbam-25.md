---
title: MBAM 2.5 정보
description: MBAM 2.5 정보
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824213"
---
# MBAM 2.5 정보


Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5은 BitLocker 드라이브 암호화를 위한 간단한 관리 인터페이스를 제공 합니다. BitLocker는 분실 하거나 도난당 한 컴퓨터에 대 한 데이터 절도 또는 데이터 노출에 대 한 향상 된 보호 기능을 제공 합니다. BitLocker는 Windows 운영 체제 볼륨 및 드라이브 및 구성 된 데이터 드라이브에 저장 된 모든 데이터를 암호화 합니다.

## MBAM 개요


MBAM 2.5에는 다음과 같은 기능이 있습니다.

-   관리자가 엔터프라이즈 전체의 클라이언트 컴퓨터에서 볼륨을 암호화 하는 프로세스를 자동화할 수 있습니다.

-   보안 관리자가 개별 컴퓨터 또는 엔터프라이즈 자체의 준수 상태를 빠르게 확인할 수 있습니다.

-   Microsoft System Center Configuration Manager를 사용 하 여 중앙 집중식 보고 및 하드웨어 관리를 제공 합니다.

-   최종 사용자에 게 BitLocker PIN 및 복구 키 요청을 지원 하기 위해 지원 센터의 작업량을 줄입니다.

-   셀프 서비스 포털을 사용 하 여 최종 사용자가 암호화 된 장치를 별도로 복구할 수 있도록 합니다.

-   보안 책임자가 키 정보 복구에 대 한 액세스를 쉽게 감사할 수 있도록 합니다.

-   Windows Enterprise 사용자가 회사 데이터를 보호 한다는 보장으로 어디서 나 계속 작업 하도록 합니다.

MBAM은 엔터프라이즈에 대해 설정한 BitLocker 암호화 정책 옵션을 적용 하 고, 해당 정책으로 클라이언트 컴퓨터의 준수 여부를 모니터링 하 고, 엔터프라이즈 및 개인 컴퓨터의 암호화 상태를 보고 합니다. 또한, MBAM은 사용자가 PIN 또는 암호를 잊어버린 경우 또는 해당 BIOS 또는 부팅 레코드가 변경 될 때 복구 키 정보에 액세스할 수 있도록 합니다.

다음 그룹은 MBAM을 사용 하 여 BitLocker를 관리 하는 데 관심이 있을 수 있습니다.

-   권한 부여 없이 기밀 데이터가 공개 되지 않는지 확인 하는 관리자, IT 보안 전문가 및 규정 준수 책임자

-   원격 또는 지사에서 컴퓨터 보안을 담당 하는 관리자

-   Windows를 실행 하는 클라이언트 컴퓨터를 담당 하는 관리자

**참고**  이 MBAM 설명서에는 BitLocker에 대해 자세히 설명 되어 있지 않습니다. 자세한 내용은 [BitLocker 드라이브 암호화 개요](https://go.microsoft.com/fwlink/p/?LinkId=225013)를 참조 하세요.

 

## <a href="" id="what-s-new-in-mbam-2-5"></a>MBAM 2.5의 새로운 기능


이 섹션에서는 MBAM 2.5의 새로운 기능에 대해 설명 합니다.

### Microsoft SQL Server 2014에 대 한 지원

MBAM은 이전 버전의 MBAM에서 지원 되는 소프트웨어 외에 Microsoft SQL Server 2014에 대 한 지원을 추가 합니다.

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> MBAM 그룹 정책 서식 파일을 별도로 다운로드

MBAM 그룹 정책 서식 파일은 MBAM 설치와 별도로 다운로드 해야 합니다. 이전 버전의 MBAM에는 mbam 설치 관리자에 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 필수 MBAM Gpo (그룹 정책 개체)가 포함 된 MBAM 정책 템플릿이 포함 되어 있습니다. 이러한 Gpo는 MBAM 설치 관리자에서 제거 되었습니다. 이제 MBAM 클라이언트 설치를 시작 하기 전에 [MDOP 그룹 정책 (admx) 템플릿을 가져오고](https://go.microsoft.com/fwlink/p/?LinkId=393941) 이를 서버 또는 워크스테이션에 복사 하는 방법에서 gpo를 다운로드 합니다. Windows Server 또는 Windows 운영 체제의 지원 되는 버전을 실행 하는 모든 서버 또는 워크스테이션에 그룹 정책 템플릿을 복사할 수 있습니다.

**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다. **MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 Bitlocker 드라이브 암호화 설정을 구성 합니다.

 

서버 또는 워크스테이션에 복사 해야 하는 서식 파일은 다음과 같습니다.

-   BitLockerManagement. adml

-   BitLockerManagement. admx

-   BitLockerUserManagement. adml

-   BitLockerUserManagement. admx

서식 파일을 사용자의 요구에 가장 잘 맞는 위치에 복사 합니다. 언어별 폴더에 복사 해야 하는 언어별 파일의 경우 해당 파일을 보려면 그룹 정책 관리 콘솔이 필요 합니다.

- 서버 또는 워크스테이션에 로컬로 서식 파일을 설치 하려면 다음 위치 중 하나에 파일을 복사 합니다.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">파일 형식</th>
  <th align="left">파일 위치</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>언어 중립 (admx)</p></td>
  <td align="left"><p><em>% \ systemroot% </em> \Policydefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>언어별 (adml)</p></td>
  <td align="left"><p><em>% systemroot% </em> \Policydefinitions [ <em> MUIculture </em> ] (예를 들어 미국 영어 언어 관련 파일이 <em> % systemroot% &lt; /em policydefinition\ \ u s에 저장 됩니다. \ n/ &gt; us)</p></td>
  </tr>
  </tbody>
  </table>

     

- 도메인에 있는 모든 그룹 정책 관리자가 서식 파일을 사용할 수 있도록 하려면 도메인 컨트롤러의 다음 위치 중 하나에 파일을 복사 합니다.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">파일 형식</th>
  <th align="left">도메인 컨트롤러 파일 위치</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>언어 중립 (admx)</p></td>
  <td align="left"><p><em>% systemroot% </em> sysvol\domain\policies\PolicyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>언어별 (adml)</p></td>
  <td align="left"><p><em>% systemroot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (예: 미국 영어 언어별 파일은 <em> % systemroot% \sysvol\domain\policies\PolicyDefinitions\en-us에 저장 됩니다. </em> )</p></td>
  </tr>
  </tbody>
  </table>

     

서식 파일에 대 한 자세한 내용은 [그룹 정책 ADMX 파일 관리 단계별 가이드](https://go.microsoft.com/fwlink/?LinkId=392818)를 참조 하세요.

### 운영 체제 및 고정 데이터 드라이브에 대 한 암호화 정책 적용 기능

MBAM 2.5를 사용 하 여 조직의 컴퓨터에 대 한 운영 체제 및 고정 데이터 드라이브에 대 한 암호화 정책을 적용 하 고 최종 사용자가 MBAM 암호화 정책을 준수 하기 위해 요구 사항에 대 한 postponement 요청 하는 일 수를 제한할 수 있습니다.

암호화 정책 적용을 구성할 수 있도록 하려면 운영 체제 드라이브 및 고정 데이터 드라이브에 대해 암호화 정책 적용 설정 이라는 새 그룹 정책 설정이 추가 되었습니다. 이 정책은 다음 표에 설명 되어 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 정책 설정</th>
<th align="left">설명</th>
<th align="left">이 설정을 구성 하는 데 사용 되는 그룹 정책 노드</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>암호화 정책 적용 설정 (운영 체제 드라이브)</p></td>
<td align="left"><p>이 설정을 사용 하는 경우 <strong> 운영 체제 드라이브에서 유예 기간을 구성할 수 있는 비 준수 유예 기간 (일)을 구성 하는 옵션을 사용 </strong> 합니다.</p>
<p>유예 기간은 드라이브가 비규격으로 검색 된 후 최종 사용자가 해당 운영 체제 드라이브에 대 한 MBAM 정책 준수를 연기할 수 있는 일 수를 지정 합니다.</p>
<p>구성 된 유예 기간이 만료 되 면 사용자는 필요한 작업을 연기 하거나 예외를 요청할 수 없습니다.</p>
<p>사용자 조작이 필요한 경우 (예: TPM (신뢰할 수 있는 플랫폼 모듈) + PIN을 사용 하거나 암호 보호기를 사용 하는 경우) 대화 상자가 나타나고 사용자가 필요한 정보를 제공할 때까지 닫을 수 없습니다. 보호기만 TPM 인 경우 사용자 입력 없이 백그라운드에서 암호화가 즉시 시작 됩니다.</p>
<p>사용자는 BitLocker 암호화 마법사를 통해 예외를 요청할 수 없습니다. 그 대신 지원 센터에 문의 하거나 조직에서 예외를 요청 하는 데 사용 하는 모든 프로세스를 사용 해야 합니다.</p></td>
<td align="left"><p>컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; Windows 구성 요소 &gt; MDOP Mbam (BitLocker Management) &gt; 운영 체제 드라이브</p></td>
</tr>
<tr class="even">
<td align="left"><p>암호화 정책 적용 설정 (고정 데이터 드라이브)</p></td>
<td align="left"><p>이 설정에 대해 옵션을 사용 하 여 <strong> 유예 기간을 구성할 고정 드라이브의 비 준수 유예 기간 일 수를 구성 </strong> 합니다.</p>
<p>유예 기간은 드라이브가 비규격으로 검색 된 후 최종 사용자가 해당 고정 드라이브에 대 한 MBAM 정책 준수를 연기할 수 있는 일 수를 지정 합니다.</p>
<p>유예 기간은 고정 드라이브를 비규격으로 결정할 때 시작 됩니다. 자동 잠금 해제를 사용 하는 경우 운영 체제 드라이브가 호환 될 때까지 정책이 적용 되지 않습니다. 그러나 자동 잠금 해제를 사용 하지 않는 경우에는 운영 체제 드라이브가 완전히 암호화 되기 전에 고정 데이터 드라이브의 암호화가 시작 될 수 있습니다.</p>
<p>구성 된 유예 기간이 만료 되 면 사용자는 필요한 작업을 연기 하거나 예외를 요청할 수 없습니다. 사용자 조작이 필요한 경우 대화 상자가 나타나고 사용자가 필요한 정보를 제공할 때까지 닫을 수 없습니다.</p></td>
<td align="left"><p>컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; Windows 구성 요소 &gt; MDOP Mbam (BitLocker Management) &gt; 고정 드라이브</p></td>
</tr>
</tbody>
</table>

 

### BitLocker 드라이브 암호화 마법사에서 보안 정책을 가리키는 URL을 제공 하는 기능

새 그룹 정책 설정을 사용 하 여 **보안 정책 링크에 대 한 url을 제공**하면 최종 사용자에 게 표시 되는 Url을 **회사 보안 정책**이라는 링크로 구성할 수 있습니다. 이 링크는 MBAM이 볼륨을 암호화 하도록 사용자에 게 메시지를 표시 하는 경우에 나타납니다.

이 정책 설정을 사용 하면 **회사 보안 정책** 링크에 대 한 URL을 구성할 수 있습니다. 이 정책 설정을 사용 하지 않거나 구성 하지 않으면 **회사 보안 정책** 링크가 사용자에 게 표시 되지 않습니다.

새 그룹 정책 설정은 다음 GPO 노드에 있습니다. **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker Management) &gt; 클라이언트 관리**

### FIPS 규격 복구 키 지원

MBAM 2.5는 Windows 8.1 운영 체제를 실행 하는 디바이스에서 FIPS (미국 정보 처리 표준) 규격 BitLocker 복구 키를 지원 합니다. 복구 키는 이전 버전의 Windows에서 FIPS 규격이 아닙니다. 이 향상 된 기능은 최종 사용자가 자체 서비스 포털 또는 관리 및 모니터링 웹 사이트 (지원 센터)를 사용 하 여 드라이브의 PIN 이나 암호를 잊었거나 컴퓨터를 잠근 경우 드라이브를 복구할 수 있도록 하기 때문에 FIPS 준수를 필요로 하는 조직의 드라이브 복구 프로세스를 개선 합니다. 새로운 FIPS 준수 기능은 암호 보호기로 확장 되지 않습니다.

조직에서 FIPS 준수를 사용 하도록 설정 하려면 연방 정보 처리 표준 (FIPS) 그룹 정책 설정을 구성 해야 합니다. 구성 방법에 대 한 자세한 내용은 [BitLocker 그룹 정책 설정을](https://go.microsoft.com/fwlink/?LinkId=393560)참조 하세요.

[설치 된 BitLocker 핫픽스](https://support.microsoft.com/kb/3015477)없이 Windows8 또는 Windows7 운영 체제를 실행 하는 클라이언트 컴퓨터의 경우 IT 관리자는 FIPS 규격 환경에서 계속 해 서 DRA (Data Recovery agent) 보호기를 사용 합니다. DRA에 대 한 자세한 내용은 [BitLocker를 사용 하 여 데이터 복구 에이전트 사용](https://go.microsoft.com/fwlink/?LinkId=393557)을 참조 하세요.

Windows 7 및 Windows 8 컴퓨터용 BitLocker 핫픽스를 다운로드 하 고 설치 하려면 [Bitlocker 관리 및 모니터링 2.5에 대 한 핫픽스 패키지 2](https://support.microsoft.com/kb/3015477) 를 참조 하세요.

### 고가용성 배포 지원

MBAM은 표준 2 서버 및 구성 관리자 통합 토폴로지와 함께 다음과 같은 고가용성 시나리오를 지원 합니다.

-   SQL Server AlwaysOn 가용성 그룹

-   SQL Server 클러스터링

-   NLB (네트워크 부하 분산)

-   SQL Server 미러링

-   VSS (볼륨 섀도 복사본 서비스) 백업

이러한 기능에 대 한 자세한 내용은 [MBAM 2.5 고가용성에 대 한 계획](planning-for-mbam-25-high-availability.md)을 참조 하세요.

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a>관리 및 모니터링 웹 사이트의 역할 관리 변경

MBAM 2.5에서는 관리 및 모니터링 웹 사이트에 대 한 액세스 권한을 제공 하는 역할을 관리 하기 위해 Active Directory 도메인 서비스 (추가)에서 보안 그룹을 만들어야 합니다. 역할을 사용 하면 특정 보안 그룹에 속한 사용자가 보고서 보기, 최종 사용자의 암호화 된 드라이브 복구 등의 다른 작업을 웹 사이트에서 수행할 수 있습니다. 이전 버전의 MBAM에서는 로컬 그룹을 사용 하 여 역할을 관리 했습니다.

MBAM 2.5에서 "역할" 이라는 용어는 이전 버전의 MBAM에 사용 된 "관리자 역할" 이라는 용어를 대체 합니다. 또한 MBAM 2.5에서는 "MBAM 시스템 관리자" 역할이 제거 되었습니다.

다음 표에는 AD DS에서 만들어야 하는 보안 그룹이 나와 있습니다. 보안 그룹의 모든 이름을 사용할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">역할</th>
<th align="left">관리 및 모니터링 웹 사이트의이 역할에 대 한 액세스 권한</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>MBAM 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 대 한 액세스를 제공 합니다. 이러한 영역에 대 한 액세스 권한이 있는 사용자는 두 영역 중 하나를 사용할 때 모든 필드를 채워야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 보고서 사용자</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 보고서에 대 한 액세스를 제공 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 모든 영역에 대 한 액세스를 제공 합니다. 최종 사용자가 드라이브를 복구 하는 데 도움이 되는 경우이 그룹의 사용자는 최종 사용자의 도메인 및 사용자 이름이 아닌 복구 키만 입력 해야 합니다. 사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 사용자 그룹 권한 보다 우선 합니다.</p></td>
</tr>
</tbody>
</table>

 

추가에서 보안 그룹을 만든 후 해당 보안 그룹에 사용자 및/또는 그룹을 지정 하 여 관리 및 모니터링 웹 사이트에 대 한 해당 수준의 액세스를 사용 하도록 설정 합니다. 각 역할의 사용자가 관리 및 모니터링 웹 사이트에 액세스할 수 있도록 하려면 관리 및 모니터링 웹 사이트를 구성할 때 각 보안 그룹도 지정 해야 합니다.

### MBAM 서버 기능을 구성 하기 위한 Windows PowerShell cmdlet

MBAM 2.5 용 Windows PowerShell cmdlet을 사용 하면 MBAM 서버 기능을 구성 하 고 관리할 수 있습니다. 각 기능에는 기능을 사용 하거나 사용 하지 않도록 설정 하거나 기능에 대 한 정보를 가져오는 데 사용할 수 있는 해당 Windows PowerShell cmdlet이 있습니다.

Windows PowerShell을 사용 하기 위한 필수 구성 요소 및 필수 구성 요소는 [Windows powershell을 사용 하 여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md)참조 하세요.

**MBAM 서버 소프트웨어를 설치한 후 Windows PowerShell cmdlet에 대 한 MBAM 2.5 도움말을 로드 하려면**

1.  Windows PowerShell 또는 Windows PowerShell ISE (통합 스크립팅 환경)를 엽니다.

2.  Type **Update-도움말-Microsoft * MBAM**.

MBAM에 대 한 Windows PowerShell 도움말은 다음 형식으로 제공 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Windows PowerShell 도움말 형식</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows PowerShell 명령 프롬프트에서 <strong> get-help </strong> &lt; <em> cmdlet을 입력 합니다.</em>&gt;</p></td>
<td align="left"><p>최신 Windows PowerShell cmdlet을 업로드 하려면, MBAM에 대 한 Windows PowerShell 도움말을 로드 하는 방법에 대 한 이전 섹션의 지침을 따릅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>웹 페이지로 TechNet에서</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>다운로드 센터에서 Word .docx 파일로</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>.Pdf 파일로 다운로드 센터에서</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### ASCII 전용 및 향상 된 Pin 및 순차적 및 반복 되는 문자 방지 기능 지원

**시작 그룹 정책 설정에 향상 된 Pin 허용**

그룹 정책 설정, **시작 Pin 허용**, BitLocker에 향상 된 시작 pin을 사용할지 여부를 구성할 수 있습니다. 향상 된 시작 Pin을 통해 사용자는 대/소문자, 기호, 숫자, 공백을 포함 하 여 전체 키보드에 키를 입력할 수 있습니다. 이 정책 설정을 사용 하면 설정 된 모든 새 BitLocker 시작 핀의 Pin이 향상 됩니다. 이 정책 설정을 사용 하지 않거나 구성 하지 않으면 강화 된 Pin을 사용할 수 없습니다.

일부 컴퓨터는 PXE (사전 부팅 실행 환경)에서 향상 된 Pin의 항목을 지원 하지 않습니다. 조직에 대해이 그룹 정책 설정을 사용 하도록 설정 하기 전에 BitLocker 설치 프로세스 중 시스템 검사를 실행 하 여 컴퓨터의 BIOS가 PXE의 전체 키보드 사용을 지원 하는지 확인 합니다. 자세한 내용은 [MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)을 참조 하세요.

**ASCII 전용 핀이 필요 함 확인란**

**시작에 향상 된 Pin 허용** 그룹 정책 설정에도 **ASCII 전용 pin 필요** 확인란이 있습니다. 조직의 컴퓨터에서 PXE의 전체 키보드 사용을 지원 하지 않는 경우 **시작 그룹에 대해 향상 된 Pin 허용** 확인란을 사용 하도록 설정한 다음 **Ascii 전용 pin 필요** 확인란을 선택 하 여 향상 된 PIN에 인쇄 가능한 ASCII 문자만 사용 하도록 할 수 있습니다.

**비순차 및 반복 되지 않는 문자의 강제 사용**

MBAM 2.5는 최종 사용자가 반복 되는 숫자 (예: 1111) 또는 순차적 번호 (예: 1234)로 구성 된 Pin을 만들 수 없도록 방지 합니다. 최종 사용자가 세 개 이상의 반복 또는 순차 번호를 포함 하는 암호를 입력 하려고 하면 Bitlocker 드라이브 암호화 마법사에 오류 메시지가 표시 되 고 사용자가 허용 되지 않은 문자가 있는 PIN을 입력할 수 없습니다.

### BitLocker 컴퓨터 준수 보고서에 DRA 인증서 추가

새 보호기 유형, DRA (데이터 복구 에이전트) 인증서가 구성 관리자의 BitLocker 컴퓨터 준수 보고서에 추가 되었습니다. 이 보호기 유형은 운영 체제 드라이브에 적용 되며, **보호 유형** 열의 **컴퓨터 볼륨 (s)** 섹션에 표시 됩니다.

### 다중 포리스트 지원 배포 지원

MBAM 2.5는 다음과 같은 유형의 다중 포리스트 배포를 지원 합니다.

-   단일 도메인이 있는 단일 포리스트

-   단일 트리 및 여러 도메인이 있는 단일 포리스트

-   여러 트리 및 분리 네임 스페이스가 있는 단일 포리스트

-   중앙 포리스트 토폴로지의 여러 포리스트

-   리소스 포리스트 토폴로지의 여러 포리스트

포리스트 마이그레이션에 대 한 지원 (단일에서 여러 개, 단일에서 single로, 여러 개의 포리스트를 통해 리소스 등으로) 또는 업그레이드 또는 다운 그레이드에 대 한 지원이 없습니다.

다중 포리스트 배포에서 MBAM을 배포 하기 위한 전제 조건은 다음과 같습니다.

-   포리스트는 지원 되는 버전의 Windows Server에서 실행 되어야 합니다.

-   양방향 또는 단방향 트러스트가 필요 합니다. 단방향 트러스트의 경우 서버의 도메인이 클라이언트의 도메인을 신뢰 해야 합니다. 즉, 서버의 도메인이 클라이언트의 도메인을 가리킵니다.

### 암호화 된 하드 드라이브에 대 한 MBAM 클라이언트 지원

MBAM은 오 팔에 대 한 TCG 사양 요구 사항 및 IEEE 1667 표준을 충족 하는 암호화 된 하드 드라이브에서 BitLocker를 지원 합니다. 이러한 디바이스에서 BitLocker를 사용 하도록 설정 하면 암호화 된 드라이브에서 키를 생성 하 고 관리 기능을 수행 합니다. 자세한 내용은 [암호화 된 하드 드라이브](https://technet.microsoft.com/library/hh831627.aspx) 를 참조 하세요.

## MDOP 기술을 활용 하는 방법


MBAM은 Microsoft 데스크톱 최적화 팩 (MDOP)의 일부입니다. MDOP는 Microsoft 소프트웨어 보증 프로그램의 일부입니다. Microsoft 소프트웨어 보증 프로그램 및 MDOP를 구입 하는 방법에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049)을 참조 하세요.

## <a href="" id="---------mbam-2-5-release-notes"></a> MBAM 2.5 릴리스 정보


이 설명서에 포함 되지 않은 최신 뉴스에 대 한 자세한 내용은 [MBAM 2.5에 대 한 릴리스 정보](release-notes-for-mbam-25.md)를 참조 하세요.

## MBAM에 대 한 제안이 있으십니까?
- [여기](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub)에서 여러분의 의견을 보내세요. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.

## 관련 항목


[Microsoft BitLocker 관리 및 모니터링 2.5](index.md)

[MBAM 2.5 시작](getting-started-with-mbam-25.md)

 

 





