---
title: Configuration Manager 통합 토폴로지에 대한 MBAM 2.5 보고서 보기
description: Configuration Manager 통합 토폴로지에 대한 MBAM 2.5 보고서 보기
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824043"
---
# Configuration Manager 통합 토폴로지에 대한 MBAM 2.5 보고서 보기


이 항목에서는 Configuration Manager 통합 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 구성할 때 사용할 수 있는 보고서에 대해 설명 합니다. 이 보고서에는 엔터프라이즈 및 MBAM이 관리 하는 개별 컴퓨터 및 장치에 대 한 BitLocker 호환성이 표시 됩니다. 보고서는 테이블 형식 정보와 차트를 제공 하며 다양 한 관점에서 데이터를 볼 수 있는 필터를 포함 합니다.

Configuration Manager 통합 토폴로지에서 관리 및 모니터링 웹 사이트에서 계속 표시 되는 **복구 감사 보고서**를 제외 하 고는 관리 및 모니터링 웹 사이트 대신 configuration manager에서 보고서를 볼 수 있습니다.

독립 실행형 토폴로지에 대 한 MBAM 보고서에 대 한 자세한 내용은 [독립 실행형 토폴로지에 대 한 mbam 2.5 보고서 보기](viewing-mbam-25-reports-for-the-stand-alone-topology.md)를 참조 하세요.

## Configuration Manager에서 보고서에 액세스


Configuration Manager에서 보고서 기능에 액세스 하려면 다음을 수행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">버전의 Configuration Manager</th>
<th align="left">보고서를 보는 방법</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SystemCenter2012 ConfigurationManager</p></td>
<td align="left"><ol>
<li><p>왼쪽 창에서 <strong> 모니터링 작업 영역을 선택 합니다 </strong> .</p></li>
<li><p>트리에서 " <strong> 개요 </strong> &gt; <strong> 보고 </strong> &gt; <strong> 보고서" </strong> &gt; <strong> mbam을 확장 </strong> 합니다.</p></li>
<li><p>보고서를 표시할 언어를 나타내는 폴더를 선택한 다음 오른쪽 창에서 보고서를 선택 합니다.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007</p></td>
<td align="left"><ol>
<li><p>왼쪽 창에서 <strong> 컴퓨터 관리 </strong> &gt; <strong> 보고 </strong> &gt; <strong> reporting Services </strong> &gt; <strong> &lt; 서버 이름 &gt; </strong> &gt; <strong> 보고서 폴더를 확장 </strong> &gt; <strong> </strong> 합니다.</p></li>
<li><p>보고서를 표시할 언어를 나타내는 폴더를 선택한 다음 오른쪽 창에서 보고서를 선택 합니다.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## Configuration Manager의 보고서에 대 한 설명


Configuration Manager 통합 토폴로지와 독립 실행형 토폴로지에 대 한 보고서에는 몇 가지 사소한 차이점이 있습니다. 다음 섹션에서는 Configuration Manager 통합 토폴로지에 대 한 MBAM 보고서의 데이터에 대해 설명 합니다.

-   [BitLocker 엔터프라이즈 준수 대시보드](#bkmk-dashboard)

-   [BitLocker 엔터프라이즈 준수 세부 정보](#bkmk-compliancedetails)

-   [BitLocker Enterprise 규정 준수 요약](#bkmk-compliancesummary)

-   [BitLocker 컴퓨터 준수 보고서](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a>BitLocker 엔터프라이즈 준수 대시보드

BitLocker 엔터프라이즈 준수 대시보드는 엔터프라이즈 전체의 BitLocker 준수 상태를 보여 주는 다음과 같은 그래프를 제공 합니다.

-   준수 상태 배포

-   비 준수 오류 분포

-   드라이브 유형별 준수 상태 배포

**준수 상태 배포**

이 원형 차트는 엔터프라이즈 내의 컴퓨터에 대 한 준수 상태를 보여 줍니다. 또한 선택한 컬렉션의 총 컴퓨터 수와 해당 준수 상태가 있는 컴퓨터의 백분율이 표시 됩니다. 각 상태를 포함 하는 실제 컴퓨터 수도 표시 됩니다. 원형 차트에는 다음과 같은 준수 상태가 표시 됩니다.

-   기준

-   비 준수

-   사용자 예외

-   임시 사용자 예외

-   정책이 적용 되지 않음

-   없는. 이러한 컴퓨터는 상태 오류를 보고 했거나 컬렉션의 일부 이지만 준수 상태를 보고 하지 않았습니다. 컴퓨터가 조직 으로부터 연결이 끊어지면 준수 상태가 부족 하 게 될 수 있습니다.

**비 준수 오류 분포**

이 원형 차트는 엔터프라이즈에서 BitLocker 드라이브 암호화 정책과 호환 되지 않는 컴퓨터 범주를 표시 하 고 각 범주의 컴퓨터 수를 보여 줍니다. 각 범주 비율은 컬렉션에 있는 비규격 컴퓨터의 총 수를 기준으로 계산 됩니다.

-   사용자가 연기 한 암호화

-   호환 되는 TPM을 찾을 수 없음

-   시스템 파티션이 사용할 수 없는 경우 또는 충분히 큰 경우

-   정책 충돌

-   TPM 자동 프로 비전 대기 중

-   알 수 없는 오류가 발생 하였습니다.

-   정보가 없습니다. 이 컴퓨터에는 MBAM 클라이언트가 설치 되어 있지 않거나, MBAM 클라이언트가 설치 되었지만 정품 인증 되지 않은 경우 (예: 서비스가 작동 하지 않음).

**드라이브 유형별 준수 상태 배포**

이 막대 차트는 드라이브 유형별 현재 BitLocker 준수 상태를 보여 줍니다. 상태는 **규격** 이며 **준수 되지**않습니다. 고정 데이터 드라이브 및 운영 체제 드라이브에 대 한 막대가 표시 됩니다. 고정 데이터 드라이브가 없는 컴퓨터는 **운영 체제 드라이브** 표시줄에만 포함 되며 값이 표시 됩니다. 이 차트에는 BitLocker 드라이브 암호화 정책 또는 정책 없음 범주에서 예외를 허용한 사용자가 포함 되어 있지 않습니다.

### <a href="" id="bkmk-compliancedetails"></a>BitLocker 엔터프라이즈 준수 세부 정보

이 보고서는 엔터프라이즈 전체의 bitlocker 사용을 대상으로 하는 컴퓨터 컬렉션에 대 한 전반적인 BitLocker 준수에 대 한 정보를 보여 줍니다.

**BitLocker Enterprise 규정 준수 세부 정보 필드**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">열 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>관리 컴퓨터</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터 수입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% 규격</p></td>
<td align="left"><p>기업에서 준수 하는 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% 규격이 아닌%</p></td>
<td align="left"><p>엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% 알 수 없는 규정</p></td>
<td align="left"><p>준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% 예외</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% 비 면제</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 되지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>기준</p></td>
<td align="left"><p>기업에서 준수 하는 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>비호환</p></td>
<td align="left"><p>엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>알 수 없는 규정 준수</p></td>
<td align="left"><p>준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외 등급</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</p></td>
</tr>
<tr class="odd">
<td align="left"><p>비 예외</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</p></td>
</tr>
</tbody>
</table>

 

**BitLocker Enterprise 규정 준수 정보 상태**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">준수 상태</th>
<th align="left">제외</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>맞지</p></td>
<td align="left"><p>예외 아님</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터가 비규격입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기준</p></td>
<td align="left"><p>예외 아님</p></td>
<td align="left"><p>컴퓨터는 지정 된 정책에 따라 규격을 준수 합니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a>BitLocker Enterprise 규정 준수 요약

이 보고서 유형을 사용 하 여 엔터프라이즈 전체의 전반적인 BitLocker 준수에 대 한 정보를 표시 하 고 BitLocker 사용을 대상으로 하는 컴퓨터 컬렉션에 있는 개별 컴퓨터에 대 한 준수를 표시 합니다.

**BitLocker Enterprise 규정 준수 요약 필드**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">열 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>관리 컴퓨터</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터 수입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% 규격</p></td>
<td align="left"><p>기업에서 준수 하는 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% 규격이 아닌%</p></td>
<td align="left"><p>엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% 알 수 없는 규정</p></td>
<td align="left"><p>준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% 예외</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% 비 면제</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 되지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>기준</p></td>
<td align="left"><p>기업에서 준수 하는 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>비호환</p></td>
<td align="left"><p>엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>알 수 없는 규정 준수</p></td>
<td align="left"><p>준수 상태가 알려지지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외 등급</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 된 총 컴퓨터</p></td>
</tr>
<tr class="odd">
<td align="left"><p>비 예외</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 되지 않은 총 컴퓨터</p></td>
</tr>
</tbody>
</table>

 

**BitLocker Enterprise 규정 준수 요약 컴퓨터 세부 정보**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">열 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>컴퓨터 이름</p></td>
<td align="left"><p>MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>도메인 이름</p></td>
<td align="left"><p>클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다. 드라이브 (팔 로우 하는 다음 표 참조)에 대 한 준수 상태가 서로 다른 준수 상태를 나타내는 것을 확인할 수 있습니다. 그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외</p></td>
<td align="left"><p>사용자가 BitLocker 정책에서 제외 되었는지 또는 제외 되지 않았음을 나타내는 상태입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>장치 사용자</p></td>
<td align="left"><p>디바이스의 사용자입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>마지막 연락처</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 대화 상대 빈도는 그룹 정책 설정을 통해 구성할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a>BitLocker 컴퓨터 준수 보고서

이 보고서 유형을 사용 하 여 컴퓨터에 대 한 정보를 수집 합니다. BitLocker 컴퓨터 준수 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 제공 합니다. 또한 컴퓨터의 각 드라이브 유형에 적용 되는 정책의 표시를 제공 합니다. 각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.

**참고**  이동식 데이터 볼륨 암호화 상태는이 보고서에 표시 되지 않습니다.

 

**BitLocker 컴퓨터 준수 보고서: 컴퓨터 세부 정보 필드**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">열 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>컴퓨터 이름</p></td>
<td align="left"><p>MBAM으로 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>도메인 이름</p></td>
<td align="left"><p>클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 종류</p></td>
<td align="left"><p>컴퓨터의 유형입니다. 유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제</p></td>
<td align="left"><p>MBAM 관리 클라이언트 컴퓨터에서 찾을 수 있는 운영 체제 유형입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>전반적인 준수</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다. 드라이브 (팔 로우 하는 다음 표 참조)에 대 한 준수 상태가 서로 다른 준수 상태를 나타내는 것을 확인할 수 있습니다. 그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제 준수</p></td>
<td align="left"><p>MBAM으로 관리 되는 운영 체제의 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>고정 데이터 드라이브 준수</p></td>
<td align="left"><p>MBAM으로 관리 되는 고정 데이터 드라이브의 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>마지막 업데이트 날짜</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 대화 상대 빈도는 그룹 정책 설정을 통해 구성할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>제외</p></td>
<td align="left"><p>사용자가 BitLocker 정책에서 제외 되었는지 또는 제외 되지 않았음을 나타내는 상태입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외 사용자</p></td>
<td align="left"><p>BitLocker 정책에서 제외 된 사용자입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>면제 날짜</p></td>
<td align="left"><p>면제를 부여 받은 날짜입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>정책 암호화 수준</p></td>
<td align="left"><p>관리자가 MBAM 정책 명세 중에 선택한 암호화 수준 (예: 128--디퓨저)</p></td>
</tr>
<tr class="even">
<td align="left"><p>정책: 운영 체제 드라이브</p></td>
<td align="left"><p>운영 체제 및 적절 한 보호기 유형에 암호화가 필요한 경우에 표시 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>정책: 고정 데이터 드라이브</p></td>
<td align="left"><p>고정 데이터 드라이브에 대해 암호화가 필요한 경우에 표시 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제조업체</p></td>
<td align="left"><p>컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>모델</p></td>
<td align="left"><p>컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>장치 사용자</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</p></td>
</tr>
</tbody>
</table>

 

**BitLocker 컴퓨터 준수 보고서: 컴퓨터 볼륨 필드**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">열 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>드라이브 문자</p></td>
<td align="left"><p>사용자가 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</p></td>
</tr>
<tr class="even">
<td align="left"><p>드라이브 종류</p></td>
<td align="left"><p>드라이브의 유형입니다. 올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다. 이는 논리 볼륨이 아닌 실제 드라이브입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>암호화 수준</p></td>
<td align="left"><p>MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>보호 기능 유형</p></td>
<td align="left"><p>운영 체제 또는 고정 데이터 드라이브를 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다. 운영 체제의 유효한 보호기 유형은 TPM 또는 TPM + PIN입니다. 고정 데이터 드라이브의 유효한 보호기 유형은 비밀 번호입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>보호기 상태</p></td>
<td align="left"><p>MBAM으로 관리 되는 컴퓨터가 정책에 지정 된 보호기 형식을 사용 하도록 설정 했음을 나타냅니다. 유효한 상태는 ON 또는 OFF입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>암호화 상태</p></td>
<td align="left"><p>드라이브의 암호화 상태입니다. 유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





