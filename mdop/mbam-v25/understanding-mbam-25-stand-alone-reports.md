---
title: MBAM 2.5 독립 실행형 보고서 이해
description: MBAM 2.5 독립 실행형 보고서 이해
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812777"
---
# MBAM 2.5 독립 실행형 보고서 이해


이 항목에서는 독립 실행형 토폴로지에서 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 실행 하는 경우 사용할 수 있는 보고서에 대해 설명 합니다.

**참고**  
Configuration Manager 통합 토폴로지로 MBAM을 실행 중인 경우에는 MBAM이 아닌 Configuration Manager에서 보고서를 생성 합니다. 이러한 보고서에 대 한 자세한 내용은 [Configuration Manager 통합 토폴로지에 대 한 MBAM 2.5 보고서 보기](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) 를 참조 하세요.



## MBAM 독립 실행형 토폴로지 보고서 이해


MBAM은 BitLocker 준수를 위해 조직을 모니터링 하는 데 사용할 수 있는 세 가지 보고서 유형을 제공 합니다.

-   [엔터프라이즈 준수 보고서](#bkmk-enterprisecompliance)

-   [컴퓨터 준수 보고서](#bkmk-compliance)

-   [복구 감사 보고서](#bkmk-recovery)

독립 실행형 토폴로지에서 MBAM을 실행 중인 경우 MBAM 보고서에 액세스 하려면 웹 브라우저를 연 다음 관리 및 모니터링 웹 사이트를 엽니다. 왼쪽 메뉴 모음에서 **보고서** 를 선택 합니다. 최상위 메뉴 모음에서 생성 하려는 보고서 종류를 선택 합니다. 이러한 보고서를 생성 하는 방법에 대 한 자세한 내용은 [MBAM 2.5 독립 실행형 보고서 생성](generating-mbam-25-stand-alone-reports.md)을 참조 하세요.

### <a href="" id="bkmk-enterprisecompliance"></a>엔터프라이즈 준수 보고서

조직의 전반적인 BitLocker 준수에 대 한 정보를 수집 하려면이 보고서 형식을 사용 합니다. 필터를 사용 하 여 조직의 컴퓨터에 대 한 규정 준수 상태 및 오류 상태에 대 한 자세한 정보를 확인 하기 위해 검색 결과의 범위를 좁힐 수 있습니다.

**엔터프라이즈 준수 개요**

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
<td align="left"><p>% 예외</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 된 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% 비 면제</p></td>
<td align="left"><p>BitLocker 암호화 요구 사항에서 제외 되지 않은 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기준</p></td>
<td align="left"><p>기업에서 준수 하는 컴퓨터의 백분율입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>비호환</p></td>
<td align="left"><p>엔터프라이즈에서 비규격 컴퓨터의 백분율입니다.</p></td>
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



**엔터프라이즈 준수 컴퓨터 세부 정보**

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
<td align="left"><p>MBAM으로 관리 되는 사용자 지정 DNS 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>도메인 이름</p></td>
<td align="left"><p>클라이언트 컴퓨터가 상주 하 고 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>컴퓨터에 대해 지정 된 정책에 따라 컴퓨터를 준수 하는 상태입니다. 상태는 비규격이 고 규격입니다. 준수 상태를 해석 하는 방법에 대 한 자세한 내용은 다음 엔터프라이즈 준수 보고서 준수 상태 테이블을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외</p></td>
<td align="left"><p>이 컴퓨터가 BitLocker 정책에서 제외 되었는지 여부를 나타내는 상태입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>마지막 연락처</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 대화 상대 주파수를 구성할 수 있습니다. 자세한 내용은 MBAM 그룹 정책 설정을 참조 하세요.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a>컴퓨터 준수 보고서

컴퓨터 또는 사용자와 관련 된 정보를 수집 하려면이 보고서 형식을 사용 합니다.

엔터프라이즈 준수 보고서에서 컴퓨터 이름을 클릭 하거나 컴퓨터 준수 보고서에 컴퓨터 이름을 입력 하 여이 보고서를 봅니다. 이 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 보여 줍니다. 또한 컴퓨터의 각 드라이브 유형에 적용 되는 정책을 나타냅니다. 각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.

**참고**  
이 보고서에는 이동식 데이터 볼륨 암호화 상태가 표시 되지 않습니다.



**컴퓨터 준수 보고서 필드**

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
<td align="left"><p>클라이언트 컴퓨터가 상주 하 고 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 종류</p></td>
<td align="left"><p>컴퓨터의 유형입니다. 유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제</p></td>
<td align="left"><p>MBAM으로 관리 되는 클라이언트 컴퓨터에서 검색 된 운영 체제 유형입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다.</p>
<p>드라이브 (다음 표 참조)의 준수 상태가 서로 다른 준수 상태를 나타낼 수 있는지 확인 합니다. 그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>정책 암호화 수준</p></td>
<td align="left"><p>MBAM 정책 사양 중 관리자가 선택한 암호화 수준 (예: 128-디퓨저)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>정책 운영 체제 드라이브</p></td>
<td align="left"><p>운영 체제에 암호화가 필요한 경우 적절 한 보호기 형식을 보여 줍니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>정책 고정 데이터 드라이브</p></td>
<td align="left"><p>고정 데이터 드라이브에 대해 암호화가 필요한 경우에 표시 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>정책 이동식 데이터 드라이브</p></td>
<td align="left"><p>이동식 드라이브에 대 한 암호화가 필요한 경우에 표시 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>장치 사용자</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>제외</p></td>
<td align="left"><p>이 컴퓨터가 BitLocker 정책에서 제외 되었는지 여부를 나타내는 상태입니다.</p></td>
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
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>마지막 연락처</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 대화 상대 주파수를 구성할 수 있습니다. 자세한 내용은 MBAM 그룹 정책 설정을 참조 하세요.</p></td>
</tr>
</tbody>
</table>



**컴퓨터 준수 보고서 드라이브 필드**

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
<td align="left"><p>운영 체제 또는 고정 데이터 볼륨을 암호화 하는 데 사용 되는 그룹 정책 설정을 통해 선택한 보호기 유형입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>보호기 상태</p></td>
<td align="left"><p>MBAM으로 관리 되는 컴퓨터가 정책에 지정 된 보호기 형식을 사용 하도록 설정 했음을 나타냅니다. 유효한 상태는 ON 또는 OFF입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>암호화 상태</p></td>
<td align="left"><p>드라이브의 암호화 상태입니다. 유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>드라이브가 정책에 따라 사용 되는지 여부를 나타내는 상태입니다. 상태는 비규격이 고 준수 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a>복구 감사 보고서

BitLocker 복구 키에 대 한 액세스를 요청한 사용자를 감사 하려면이 보고서 형식을 사용 합니다. 보고서는 원하는 필터링 조건을 기준으로 여러 필터를 제공 합니다. 특정 유형의 사용자 (지원 센터 사용자 또는 최종 사용자)에 게 요청 실패 여부, 요청 된 특정 키 유형, 검색을 수행 하는 날짜 범위 등을 필터링 할 수 있습니다.

**복구 감사 보고서 필드**

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
<td align="left"><p>날짜 및 시간 요청</p></td>
<td align="left"><p>최종 사용자 또는 지원 센터 사용자가 키 검색 요청을 수행한 날짜 및 시간입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>감사 요청 원본</p></td>
<td align="left"><p>요청이 시작 된 사이트입니다. 이 항목에는 <strong> 셀프 서비스 포털 </strong> 또는 <strong> 헬프 데스크 두 가지 값 중 하나가 </strong> 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>요청 상태</p></td>
<td align="left"><p>요청 상태입니다. 유효한 상태가 성공적으로 (키 검색 됨) 또는 실패 했습니다 (키가 검색 되지 않음).</p></td>
</tr>
<tr class="even">
<td align="left"><p>헬프데스크 사용자</p></td>
<td align="left"><p>키 검색 요청을 시작한 지원 센터 사용자입니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>고급 헬프데스크 사용자가 최종 사용자를 지정 하지 않고 키를 복구 하는 경우 <strong> 최종 사용자 </strong> 필드는 비어 있게 됩니다. 표준 헬프데스크 사용자는 최종 사용자를 지정 해야 하며, 해당 사용자가이 필드에 표시 됩니다.</p>
<p>셀프 서비스 포털을 통한 복구에는이 필드와 최종 사용자 필드에 요청 하는 최종 사용자가 나열 됩니다 <strong> </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>최종 사용자</p></td>
<td align="left"><p>키 검색 요청을 시작한 최종 사용자입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>컴퓨터</p></td>
<td align="left"><p>복구 된 컴퓨터의 컴퓨터 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>키 유형</p></td>
<td align="left"><p>지원 센터 사용자 또는 최종 사용자가 요청한 키의 유형입니다. MBAM에서 수집 하는 세 가지 키 유형은 다음과 같습니다.</p>
<ul>
<li><p>복구 키 암호 (복구 모드에서 컴퓨터를 복구 하는 데 사용 됨)</p></li>
<li><p>복구 키 ID (다른 사용자 대신 복구 모드에서 컴퓨터를 복구 하는 데 사용 됨)</p></li>
<li><p>TPM 암호 해시 (TPM이 잠긴 컴퓨터를 복구 하는 데 사용 됨)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>이유 설명</p></td>
<td align="left"><p>지정 된 키 유형이 지원 센터 사용자 또는 최종 사용자에 의해 요청 된 이유입니다. 이유는 관리 및 모니터링 웹 사이트의 TPM 및 복구 기능을 관리 하는 방법에 명시 되어 있습니다. 유효한 항목은 사용자가 입력 한 텍스트 또는 다음 이유 코드 중 하나입니다.</p>
<ul>
<li><p>운영 체제 부팅 순서 변경 됨</p></li>
<li><p>BIOS 변경 됨</p></li>
<li><p>운영 체제 파일이 변경 됨</p></li>
<li><p>분실 한 시작 키</p></li>
<li><p>핀 분실</p></li>
<li><p>TPM 다시 설정</p></li>
<li><p>암호 손실</p></li>
<li><p>스마트 카드 분실</p></li>
<li><p>PIN 잠금 다시 설정</p></li>
<li><p>TPM 켜기</p></li>
<li><p>TPM 끄기</p></li>
<li><p>TPM 암호 변경</p></li>
<li><p>TPM 지우기</p></li>
</ul></td>
</tr>
</tbody>
</table>



**참고**  
**보고서 메뉴 모음** 에서 **내보내기** 단추를 클릭 하 여 결과를 파일에 저장할 수 있습니다.




## 관련 항목


[MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[MBAM 2.5 독립 실행형 보고서 생성](generating-mbam-25-stand-alone-reports.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





