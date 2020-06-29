---
title: MBAM 보고서 이해
description: MBAM 보고서 이해
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822868"
---
# MBAM 보고서 이해


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 BitLocker 사용 및 준수 모니터링을 위해 다양 한 보고서를 생성 합니다. 이 항목에서는 엔터프라이즈 준수, 개별 컴퓨터, 하드웨어 호환성 및 키 복구 활동에 대 한 MBAM 보고서에 대해 설명 합니다.

## 보고서 이해


MBAM의 보고서 기능에 액세스 하려면 MBAM 관리 웹 사이트를 엽니다. 탐색 창에서 **보고서** 를 선택 합니다. 그런 다음 기본 콘텐츠 창에서 보고서 유형의 탭을 클릭 합니다. **엔터프라이즈 준수 보고서**, **컴퓨터 준수 보고서**, **하드웨어 감사 보고서**또는 **복구 감사**보고서.

### 엔터프라이즈 준수 보고서

엔터프라이즈 준수 보고서는 조직의 전반적인 BitLocker 준수에 대 한 정보를 제공 합니다. 이 보고서에 사용할 수 있는 필터를 통해 준수 상태 및 오류 상태에 따라 검색 결과를 좁힐 수 있습니다. 이 보고서는 6 시간 마다 실행 됩니다.

**엔터프라이즈 준수 보고서 필드**

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
<td align="left"><p>MBAM에서 관리 되는 사용자 지정 DNS 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>도메인 이름</p></td>
<td align="left"><p>클라이언트 컴퓨터가 상주 하 고 있으며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>컴퓨터에 대해 지정 된 정책에 따라 컴퓨터에 대 한 규정 준수 상태입니다. 사용할 수 있는 상태는 비규격이 고 준수입니다. 자세한 내용은이 항목의 엔터프라이즈 준수 보고서 준수 상태를 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>제외</p></td>
<td align="left"><p>하드웨어 종류 식별 및 컴퓨터가 정책에서 제외 되었는지 여부를 확인 하는 컴퓨터 하드웨어의 상태입니다. 하드웨어는 알려지지 않음 (하드웨어 종류는 MBAM으로 식별 되지 않음), 하드웨어 예외 (하드웨어 종류는 확인 되었으며, MBAM 정책에서 제외 된 것으로 표시 됨), 예외 (하드웨어 식별 됨 및 정책에서 제외 되지 않음) 등 세 가지 상태일 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>장치 사용자</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 알려진 사용자입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>마지막 연락처</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 이 시간은 구성할 수 있습니다. MBAM 정책 설정을 참조 하세요.</p></td>
</tr>
</tbody>
</table>

 

**엔터프라이즈 준수 보고서 준수 상태**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">준수 상태</th>
<th align="left">제외</th>
<th align="left">설명</th>
<th align="left">사용자 작업</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>맞지</p></td>
<td align="left"><p>예외 아님</p></td>
<td align="left"><p>컴퓨터가 지정 된 정책에 따라 비규격 이며 하드웨어 종류가 정책에서 제외로 표시 되지 않았습니다.</p></td>
<td align="left"><p>컴퓨터 <strong> 이름을 클릭 </strong> 하 여 컴퓨터 준수 보고서를 확장 하 고 각 드라이브의 상태가 지정 된 정책을 준수 하는지 확인 합니다. 암호화 상태에 컴퓨터가 암호화 되지 않은 것으로 표시 되는 경우 암호화가 계속 진행 중이거나 컴퓨터에 오류가 있는 것일 수 있습니다. 오류가 없는 경우에는 컴퓨터가 여전히 암호화 상태를 연결 하거나 설정 하는 과정에서 발생 하는 것일 수 있습니다. 나중에 다시 확인 하 여 상태가 변경 되었는지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기준</p></td>
<td align="left"><p>예외 아님</p></td>
<td align="left"><p>컴퓨터는 지정 된 정책에 따라 규격을 준수 합니다.</p></td>
<td align="left"><p>작업이 필요 하지 않습니다. 필요에 따라 컴퓨터 준수 보고서를 보고 컴퓨터의 상태를 확인할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>기준</p></td>
<td align="left"><p>하드웨어 예외</p></td>
<td align="left"><p>하드웨어 종류가 면제 인 경우 정책이 설정 되는 방법과 각 하드 드라이브의 개별 상태에 관계 없이 전체 상태는 규격으로 간주 됩니다.</p></td>
<td align="left"><p>작업이 필요 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기준</p></td>
<td align="left"><p>알 수 없는 하드웨어</p></td>
<td align="left"><p>MBAM은 하드웨어 유형을 인식 하지만, MBAM은 예외 또는 예외 인지 여부를 알 수 없습니다. 관리자가 하드웨어에 대해 호환 되는 상태를 설정 하지 않은 경우이 문제가 발생 합니다. 따라서 MBAM은 기본적으로 규격 상태로 되돌려집니다.</p></td>
<td align="left"><p>새로 배포 된 MBAM 클라이언트의 초기 상태입니다. 일반적으로 일시적인 상태입니다. 관리자가 하드웨어를 호환 되는 것으로 표시 했더라도 클라이언트 컴퓨터가 다시 보고 되기 전에 상당한 지연 또는 구성 가능한 대기 시간이 있을 수 있습니다. 마지막 대화 상대의 시간을 기록 하 고 지정 된 간격 후에 다시 체크 인 하 여 상태가 변경 되었는지 확인 합니다. 상태가 변경 되지 않은 경우이 컴퓨터 또는 하드웨어 종류에 오류가 있을 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### 컴퓨터 준수 보고서

컴퓨터 준수 보고서에 컴퓨터 또는 사용자와 관련 된 정보가 표시 됩니다.

컴퓨터 준수 보고서는 운영 체제 드라이브 및 고정 데이터 드라이브를 포함 하 여 컴퓨터의 각 드라이브에 대 한 자세한 암호화 정보 및 적용 가능한 정책을 제공 합니다. 이 보고서 유형을 보려면 엔터프라이즈 준수 보고서에서 컴퓨터 이름을 클릭 하거나 컴퓨터 준수 보고서에 컴퓨터 이름을 입력 합니다. 각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.

**참고**  이 보고서는 이동식 데이터 볼륨에 대 한 암호화 상태를 제공 하지 않습니다.

 

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
<td align="left"><p>MBAM에서 관리 되는 사용자 지정 DNS 컴퓨터 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>도메인 이름</p></td>
<td align="left"><p>클라이언트 컴퓨터가 상주 하 고 있으며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 종류</p></td>
<td align="left"><p>컴퓨터의 이식성 유형입니다. 유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제</p></td>
<td align="left"><p>MBAM 관리 클라이언트 컴퓨터에 설치 된 운영 체제 유형입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다. 동일한 컴퓨터에 규격 및 비규격 드라이브가 있을 수 있지만,이 필드에는 지정 된 정책에 따른 전반적인 컴퓨터 준수 여부가 표시 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>정책 Cypher 강도</p></td>
<td align="left"><p>MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다. 예를 들어 128 비트에 디퓨저</p></td>
</tr>
<tr class="odd">
<td align="left"><p>정책 운영 체제 드라이브</p></td>
<td align="left"><p>해당 되는 경우 O/S 및 보호기 유형에 대해 암호화가 필요한 지 여부를 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>정책 고정 데이터 드라이브</p></td>
<td align="left"><p>고정 드라이브에 대해 암호화가 필요한 지 여부를 나타냅니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>정책 이동식 데이터 드라이브</p></td>
<td align="left"><p>이동식 드라이브에 대해 암호화가 필요한 지 여부를 나타냅니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>장치 사용자</p></td>
<td align="left"><p>컴퓨터에서 알려진 사용자의 id를 제공 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>제외</p></td>
<td align="left"><p>컴퓨터 하드웨어 유형이 MBAM에서 인식 되는지, 알려진 경우 컴퓨터가 정책에서 제외로 지정 되었는지 여부를 나타냅니다. 하드웨어를 알 수 없음 (하드웨어 종류가 MBAM으로 식별 되지 않음) 이라는 세 가지 상태가 있습니다. 하드웨어 예외 (하드웨어 종류는 확인 되었으며, MBAM 정책에서 제외로 표시 됨), (하드웨어가 식별 되었으며 정책에서 제외 되지 않음).</p></td>
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
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. T</p></td>
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
<td align="left"><p>사용자가이 특정 드라이브에 할당 한 컴퓨터 드라이브 문자</p></td>
</tr>
<tr class="even">
<td align="left"><p>드라이브 종류</p></td>
<td align="left"><p>드라이브의 유형입니다. 올바른 값은 운영 체제 드라이브 및 고정 데이터 드라이브입니다. 이는 논리 볼륨이 아닌 실제 드라이브입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cypher 힘</p></td>
<td align="left"><p>MBAM 정책 사양 동안 관리자가 선택한 암호화 수준입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>보호 기능 유형</p></td>
<td align="left"><p>운영 체제 또는 고정 볼륨을 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다. 운영 체제 드라이브의 유효한 보호기 유형은 TPM 또는 TPM + PIN입니다. 고정 데이터 볼륨에 유효한 보호기 유형은 비밀 번호입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>보호기 상태</p></td>
<td align="left"><p>이 필드는 컴퓨터에서 정책에 지정 된 보호기 유형을 사용 하도록 설정 했는지 여부를 나타냅니다. 유효한 상태는 ON 또는 OFF입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>암호화 상태</p></td>
<td align="left"><p>드라이브의 현재 암호화 상태입니다. 유효한 상태는 암호화 되 고 암호화 되지 않고 암호화 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>드라이브가 정책에 따라 사용 되는지 여부를 나타냅니다. 상태는 비규격이 고 준수 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>컴퓨터의 준수 상태와 관련 된 오류 및 상태 메시지를 포함 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 하드웨어 감사 보고서

이 보고서는 특정 컴퓨터의 하드웨어 호환성 상태와 모델에 대 한 변경 사항을 감사 하는 데 도움이 됩니다. 검색 결과의 범위를 좁히는 데 도움이 되도록이 보고서에는 변경 유형 및 발생 시간 등의 기준에 대 한 필터링이 포함 됩니다. 각 상태 변경은 사용자 및 날짜 및 시간을 기준으로 추적 됩니다. 하드웨어 종류는 클라이언트 컴퓨터에서 실행 되는 MBAM 에이전트에 의해 자동으로 채워집니다. 이 보고서는 MBAM 관리 컴퓨터에서 직접 수집한 정보에 대 한 사용자 변경을 추적 합니다. 일반적인 관리 변경 내용이 호환 되지 않는 것으로 변경 됩니다. 그러나 관리자는 필드를 수정할 수도 있습니다.

**하드웨어 감사 보고서 필드**

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
<td align="left"><p>날짜 및 시간</p></td>
<td align="left"><p>하드웨어 종류를 변경한 날짜 및 시간입니다. 모든 고유 하드웨어 종류에는 적어도 하나 이상의 항목이 할당 되어 있다는 점에 유의 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자</p></td>
<td align="left"><p>특정 항목을 변경한 관리 사용자입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>유형 변경</p></td>
<td align="left"><p>하드웨어 종류 정보에 대 한 변경 유형입니다. 유효한 값은 더하기 (새 항목), 업데이트 (기존 항목 변경) 또는 삭제 (기존 항목 제거)입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>원래 값</p></td>
<td align="left"><p>변경 전의 하드웨어 종류 사양 값입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>현재 값</p></td>
<td align="left"><p>변경이 이루어진 후의 하드웨어 종류 사양 값입니다.</p></td>
</tr>
</tbody>
</table>

 

### 복구 감사 보고서

복구 감사 보고서는 복구 키에 대 한 액세스를 요청한 사용자를 감사 하는 데 도움이 될 수 있습니다. 이 보고서에 대 한 필터 조건에는 요청을 수행 하는 사용자 유형, 요청 된 키 유형, 성공 또는 실패, 발생 시간, 사용자 요청 (지원 센터, 최종 사용자)의 유형 등이 포함 됩니다. 이 보고서를 통해 관리자는 필요에 따라 상황별 보고서를 만들 수 있습니다.

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
<td align="left"><p>최종 사용자 또는 지원 센터 사용자가 키 검색 요청을 수행한 날짜와 시간입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>요청 상태</p></td>
<td align="left"><p>요청 상태입니다. 유효한 상태는 성공적 (키 검색 됨) 또는 실패 (키가 검색 되지 않음) 중 하나입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>헬프데스크 사용자</p></td>
<td align="left"><p>키 검색 요청을 시작한 지원 센터 사용자입니다. 지원 센터 사용자가 최종 사용자를 대신 하 여 키를 검색 하는 경우 최종 사용자 필드는 비어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자</p></td>
<td align="left"><p>키 검색 요청을 시작한 최종 사용자입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>키 유형</p></td>
<td align="left"><p>요청 된 키의 유형입니다. MBAM은 복구 키 암호 (복구 모드에서 컴퓨터 복구) 라는 세 가지 키 유형을 수집 합니다. 복구 키 ID (다른 사용자 대신 복구 모드로 컴퓨터를 복구 하는 경우) TPM (신뢰할 수 있는 플랫폼 모듈) 암호 해시 (TPM이 잠겨 있는 컴퓨터를 복구 하는 경우)</p></td>
</tr>
<tr class="even">
<td align="left"><p>이유 설명</p></td>
<td align="left"><p>지정 된 키 형식을 요청한 이유입니다. 이유는 관리 웹 사이트의 TPM (드라이브 복구) 및 TPM 관리 기능에 명시 되어 있습니다. 유효한 항목에는 사용자가 입력 한 텍스트 또는 다음 이유 코드 중 하나가 포함 됩니다.</p>
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
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

**참고**  보고서 결과를 파일에 저장 하려면 보고서 메뉴 모음에서 **내보내기** 단추를 클릭 합니다.

 

## 관련 항목


[MBAM 1.0으로 BitLocker 규정 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





