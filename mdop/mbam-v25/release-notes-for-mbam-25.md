---
title: MBAM 2.5 릴리스 정보
description: MBAM 2.5 릴리스 정보
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824983"
---
# MBAM 2.5 릴리스 정보


이 릴리스 정보를 검색 하려면 Ctrl + F를 누릅니다.

이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5을 설치 하기 전에 자세히 읽어 보세요. 이 릴리스 노트에는 MBAM을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있으며 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 노트가 다른 MBAM 2.5 설명서와 다를 경우 신뢰할 수 있는 최신 변경 사항을 고려해 야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## <a href="" id="---------mbam-2-5-known-issues"></a> MBAM 2.5 알려진 문제


이 섹션에서는 MBAM 2.5에 대 한 릴리스 정보를 포함 합니다.

### 웹 브라우저가 의도 하지 않게 관리자 권한으로 실행

MBAM 서버 구성 도구의 도움말 링크를 사용 하면 브라우저 창을 관리자 권한으로 열 수 있습니다.

**해결 방법:** 다른 사이트로 이동 하기 전에 Internet Explorer 보안 강화 구성 (IESC)을 사용 하거나 웹 브라우저를 닫습니다.

**참고**  이 문제는 MBAM 2.5 SP1에서 해결 되었습니다.

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> MBAM은 AES 256 비트 암호화 키 및 디퓨저를 사용 하 여 암호화 된 클라이언트를 비규격으로 보고 합니다.

컴퓨터에 MBAM 2.5 클라이언트가 설치 되어 있고, 디퓨저 암호화 강도의 AES 256 비트를 사용 하 여 암호화 되는 경우 MBAM 클라이언트는 mbam 준수 보고서에서 비규격으로 보고 됩니다.

**해결 방법:** [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972)에서 핫픽스를 설치 합니다.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> H/pc에서 TPM + PIN 보호기를 설정한 경우 MBAM이 볼륨을 암호화 하는 데 실패 하 고 오류를 보고 함

최종 사용자가 태블릿 장치에서 TPM + PIN 보호기를 설정 하려고 하면 MBAM이 암호화에 실패 하 고 오류를 보고 합니다. 이 문제는 태블릿 장치에 부팅 전 환경 키보드가 없기 때문에 발생 합니다.

**해결 방법:** **태블릿에서 부팅 가능 키보드 입력이 필요한 BitLocker 인증 사용** 그룹 정책 설정을 사용 하도록 설정 합니다. 이 설정은 BitLocker 그룹 정책 설정 이며, MBAM 그룹 정책 템플릿에서 사용할 수 없습니다.

### 모든 서비스 계정에 대해 사용자 계정 이름이 필요 합니다.

모든 서비스 계정에 대해 UPN (사용자 계정 이름)을 MBAM으로 설정 해야 합니다. 계정에 대 한 UPN을 만들지 못한 경우 구성 프로세스 중에 사용자 또는 그룹을 Active Directory에서 찾을 수 없음을 나타내는 오류 메시지가 표시 됩니다.

**해결 방법:** UPN을 서비스 계정에 추가 합니다.

### 클라이언트 컴퓨터가 Microsoft Ajax 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털에 추가 구성이 필요 함

클라이언트 컴퓨터에 Microsoft의 CDN (콘텐츠 배달 네트워크)에 액세스할 수 없는 경우 셀프 서비스 포털에 특정 JavaScript 파일에 대 한 액세스 권한이 부여 되는 경우 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 해야 합니다. 클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하지 않으면 로그온 한 회사 이름과 계정만 표시 됩니다. 오류 메시지가 표시 되지 않습니다.

**해결 방법:** MBAM 2.5 SP1을 설치 합니다. 또는 다음 지침에 따라 셀프 서비스 포털을 구성 합니다. [클라이언트 컴퓨터가 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하는 방법을 설명](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)합니다.

### IIS를 .NET Framework 4.5으로 업그레이드 한 후 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않음

IIS (인터넷 정보 서비스)를 Microsoft .NET Framework 4.5으로 업그레이드 하면 셀프 서비스 포털 및 관리 및 모니터링 웹 사이트가 열리지 않습니다.

**해결 방법:** [.Net Framework 4.0을 설치 하면 "system.servicemodel: HttpModule '을 로드할 수 없습니다. 라는 문서 오류 메시지](https://go.microsoft.com/fwlink/?LinkId=393568)를 참조 하세요.

### 보고서가 구성 되지 않은 경우 관리 및 모니터링 웹 사이트에 "보고서를 찾을 수 없음" 오류 메시지가 표시 됨

관리 및 모니터링 웹 사이트를 구성한 다음 보고서 기능을 먼저 구성 하지 않고 보고서를 보려고 하면 오류 메시지에 해당 보고서를 찾을 수 없음을 표시 합니다.

**해결 방법:** 웹 응용 프로그램을 구성 하기 전에 보고서 기능을 구성 합니다.

### SSL이 SSRS에 구성 되어 있지 않은 경우 관리 및 모니터링 웹 사이트의 보고서에 경고가 표시 됨

SQL Server Reporting Services (SSRS)가 보안 소켓 계층 (SSL)을 사용 하도록 구성 되지 않은 경우 MBAM 서버를 구성할 때 보고서 기능에 대 한 URL이 HTTPS 대신 HTTP로 설정 됩니다. 그런 다음 관리 및 모니터링 웹 사이트를 열고 보고서를 선택 하면 "보안 콘텐츠만 표시 됨"과 같은 오류 메시지가 나타납니다.

**해결 방법:** 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다. 이 문제를 해결 하려면 SQL Server Reporting Services가 설치 되어 있는 MBAM 컴퓨터로 이동한 다음 **Reporting Services 구성 관리자**를 실행 하 고 **웹 서비스 URL**을 클릭 합니다. 서버에 대 한 적절 한 SSL 인증서를 선택 하 고 적절 한 SSL 포트 (기본 포트 443)를 입력 한 다음 **적용**을 클릭 합니다.

### BitLocker 준수 요약 보고서에서 "뒤로"를 클릭 하면 오류가 발생 하는 경우

BitLocker 준수 요약 보고서로 드릴 다운 한 다음 SSRS 보고서의 **뒤로** 링크를 클릭 하면 오류가 발생할 수 있습니다.

**해결 방법:** 않아야.

### 사용 된 공간만 암호화가 올바르게 작동 하지 않음

MBAM 클라이언트를 설치한 후 처음으로 컴퓨터를 암호화 하 고 사용 된 공간만 암호화를 구현 하도록 그룹 정책 설정을 구성한 경우에는 MBAM이 디스크의 사용 된 공간만 암호화 하는 대신 전체 디스크를 잘못 암호화 합니다. 컴퓨터는 MBAM 클라이언트를 설치 하는 경우에만 사용 된 공간으로 암호화 되 고 같은 그룹 정책 설정을 구성한 경우 MBAM은 드라이브가 올바르게 암호화 되었음을 보고 하 고 드라이브를 다시 암호화 하려고 하지 않습니다.

**해결 방법:** 않아야.

### 암호화 강도가 BitLocker 컴퓨터 준수 보고서에 잘못 표시 됨

**드라이브 암호화 방법 선택 및 암호화 수준** 그룹 정책 개체에서 특정 암호화 강도를 설정 하지 않으면, 암호 강도가 기본값 128 비트 암호화를 사용 하는 경우에도 구성 관리자 통합 토폴로지의 BitLocker 컴퓨터 준수 보고서에 항상 암호화 수준에 대 한 "unknown"이 표시 됩니다. 그룹 정책 개체에서 특정 암호화 수준을 설정한 경우 보고서에 올바른 암호화 강도가 표시 됩니다.

**해결 방법:** **드라이브 암호화 방법 및 암호화 수준** 그룹 정책 개체를 선택 하 여 항상 특정 암호화 강도를 설정 합니다.

### 드라이브 유형별 준수 상태 배포 구성 항목을 업데이트 한 후에 이전 데이터가 표시 됨

SystemCenter2012 ConfigurationManager에서 MBAM 구성 항목을 업데이트 한 후에는 BitLocker Enterprise 준수 대시보드에 드라이브 유형별 차트를 통해 준수 상태 배포에 이전 버전의 구성 항목에 대 한 정보를 기반으로 하는 데이터가 표시 됩니다.

**해결 방법:** 않아야. MBAM 구성 항목을 수정 하는 것은 지원 되지 않으며, 보고서가 예상 대로 표시 되지 않을 수 있습니다.

### 보안 강화 구성으로 인해 보고서에 오류 메시지가 잘못 표시 될 수 있음

Internet Explorer 보안 강화 구성 (ESC)이 켜져 있는 경우 MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타날 수 있습니다. 웹 콘텐츠 및 응용 프로그램 스크립트를 통해 발생할 수 있는 잠재적인 공격에 대 한 서버의 노출을 줄여 서버를 보호 하기 위해 기본적으로 ESC가 설정 됩니다.

**해결 방법:** MBAM 서버에서 보고서를 보려고 할 때 "액세스 거부" 오류 메시지가 나타나면 그룹 정책 개체를 설정 하거나 이미지의 기본 설정을 수동으로 변경 하 여 보안 강화 구성을 사용 하지 않도록 설정할 수 있습니다. 또는 ESC가 설정 되지 않은 다른 컴퓨터에서 보고서를 볼 수도 있습니다.

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a>MBAM 2.5에 대 한 핫픽스와 지식 기반 문서


이 표에는 MBAM 2.5에 대 한 핫픽스와 KB 아티클이 나와 있습니다.

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
<td align="left"><p>2975636</p></td>
<td align="left"><p>Microsoft BitLocker 관리 및 모니터링 2.5 핫픽스 패키지 1</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)">support.microsoft.com/kb/2975636/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>3015477</p></td>
<td align="left"><p>BitLocker 관리 및 모니터링 2.5 핫픽스 패키지 2</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)">support.microsoft.com/kb/3015477</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3011022</p></td>
<td align="left"><p>SSRS 인스턴스의 이름에 밑줄이 포함 되어 있으면 MBAM 2.5 설치 또는 구성 관리자 보고가 실패 함</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)">support.microsoft.com/kb/3011022/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2756402</p></td>
<td align="left"><p>MBAM 클라이언트가 이벤트 ID 4 및 오류 코드 0x8004100E와 함께 실패 함 이벤트 설명</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>MBAM 엔터프라이즈 또는 컴퓨터 준수 보고서 열기 오류</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>MBAM 2.0 구성 관리자 통합 시나리오에서 SQL Server 2008을 사용 하 여 설치 실패</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2975472</p></td>
<td align="left"><p>여러 MBAM 클라이언트가 MBAM 복구 데이터베이스에 연결 되는 경우의 SQL 교착 상태</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)">support.microsoft.com/kb/2975472/EN-US</a></p></td>
</tr>
</tbody>
</table>

 


## 관련 항목


[MBAM 2.5 정보](about-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





