---
title: MBAM 보고서 이해
description: MBAM 보고서 이해
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823813"
---
# MBAM 보고서 이해


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치할 때 독립 실행형 토폴로지를 선택한 경우 MBAM에서 다른 보고서를 실행 하 여 BitLocker 사용 및 준수를 모니터링할 수 있습니다. MBAM은 관리자가 관리 하는 모든 컴퓨터 및 장치에 대 한 규정 준수 및 기타 정보를 보고 합니다. 이 항목의 정보는 엔터프라이즈 및 개별 컴퓨터 준수 및 키 복구 작업에 대 한 Microsoft BitLocker 관리 및 모니터링 보고서를 이해 하는 데 도움이 될 수 있습니다.

**참고**  Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치할 때 구성 관리자 토폴로지를 선택 하면 보고서가 MBAM이 아닌 Configuration Manager에서 생성 됩니다. Configuration Manager에서 실행 되는 보고서에 대 한 자세한 내용은 [구성 관리자에서 MBAM 보고서 이해](understanding-mbam-reports-in-configuration-manager.md)를 참조 하세요.

 

## 보고서 이해


Microsoft BitLocker 관리 및 모니터링의 보고서 기능에 액세스 하려면 웹 브라우저를 열고 관리 및 모니터링 웹 사이트를 엽니다. 왼쪽 메뉴 모음에서 **보고서** 를 선택한 다음 위쪽 메뉴 모음에서 선택 합니다. 생성 하려는 보고서 종류

### 엔터프라이즈 준수 보고서

조직의 전반적인 BitLocker 준수에 대 한 정보를 수집 하려면이 보고서 형식을 사용 합니다. 여러 필터를 사용 하 여 검색 결과를 준수 상태 및 오류 상태로 좁힐 수 있습니다. 보고서 정보는 6 시간 마다 업데이트 됩니다.

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
<td align="left"><p>MBAM으로 관리 되는 사용자 지정 DNS 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>도메인 이름</p></td>
<td align="left"><p>클라이언트 컴퓨터가 상주 하 고 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>컴퓨터에 대해 지정 된 정책에 따라 컴퓨터를 준수 하는 상태입니다. 상태는 비규격이 고 규격입니다. 준수 상태를 해석 하는 방법에 대 한 자세한 내용은 엔터프라이즈 준수 보고서 준수 상태 테이블을 참조 하세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>마지막 연락처</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 대화 상대 주파수를 구성할 수 있습니다 (MBAM 정책 설정 참조).</p></td>
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
<td align="left"><p>지정 된 정책에 따라 컴퓨터가 비규격입니다.</p></td>
<td align="left"><p><strong>컴퓨터 이름을 클릭 하 </strong> 고 각 드라이브의 상태가 지정 된 정책을 따르는지 확인 하 여 컴퓨터 준수 보고서 세부 정보를 확장 합니다. 암호화 상태에 컴퓨터가 암호화 되지 않은 것으로 표시 되는 경우 암호화가 진행 중이거나 컴퓨터에 오류가 있는 것입니다. 오류가 없는 경우에는 컴퓨터가 여전히 암호화 상태를 연결 하거나 설정 하는 과정에서 발생 하는 것일 수 있습니다. 나중에 다시 확인 하 여 상태가 변경 되었는지 확인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기준</p></td>
<td align="left"><p>예외 아님</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터가 규격입니다.</p></td>
<td align="left"><p>작업이 필요 하지 않습니다. 컴퓨터의 상태는 컴퓨터 준수 보고서를 확인 하 여 확인할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### 컴퓨터 준수 보고서

컴퓨터 또는 사용자와 관련 된 정보를 수집 하려면이 보고서 형식을 사용 합니다.

이 보고서는 엔터프라이즈 준수 보고서에서 컴퓨터 이름을 클릭 하거나 컴퓨터 준수 보고서에 컴퓨터 이름을 입력 하 여 볼 수 있습니다. 컴퓨터 준수 보고서는 컴퓨터의 각 드라이브 (운영 체제 및 고정 데이터 드라이브)에 대 한 자세한 암호화 정보를 제공 하 고 컴퓨터의 각 드라이브 유형에 적용 되는 정책을 나타냅니다. 각 드라이브의 세부 정보를 보려면 컴퓨터 이름 항목을 확장 합니다.

**참고**  이동식 데이터 볼륨 암호화 상태가 보고서에 표시 되지 않습니다.

 

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
<td align="left"><p>클라이언트 컴퓨터가 상주 하며 MBAM으로 관리 되는 정규화 된 도메인 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 종류</p></td>
<td align="left"><p>컴퓨터의 유형입니다. 유효한 형식은 이식할 수 없으며 이식 가능 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>운영 체제</p></td>
<td align="left"><p>MBAM 관리 클라이언트 컴퓨터에서 찾을 수 있는 운영 체제 유형.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태</p></td>
<td align="left"><p>MBAM이 관리 하는 컴퓨터의 전반적인 준수 상태입니다. 유효한 상태는 규격 및 비규격입니다. 드라이브 (다음 표 참조)의 준수 상태가 서로 다른 준수 상태를 나타낼 수 있는지 확인 합니다. 그러나이 필드는 지정 된 정책에 따라 준수 상태를 나타냅니다.</p></td>
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
<td align="left"><p>제조업체</p></td>
<td align="left"><p>컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>모델</p></td>
<td align="left"><p>컴퓨터 BIOS에 표시 되는 컴퓨터 제조업체 모델 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 상태 세부 정보</p></td>
<td align="left"><p>지정 된 정책에 따라 컴퓨터의 준수 상태에 대 한 오류 및 상태 메시지입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>마지막 연락처</p></td>
<td align="left"><p>컴퓨터가 호환성 상태를 보고 하기 위해 서버에 마지막으로 연결한 날짜 및 시간입니다. 대화 상대 주파수를 구성할 수 있습니다 (MBAM 정책 설정 참조).</p></td>
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
<td align="left"><p>운영 체제 또는 고정 데이터 볼륨을 암호화 하는 데 사용 되는 정책을 통해 선택한 보호기 유형입니다.</p></td>
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

 

### 복구 감사 보고서

이 보고서 유형을 사용 하 여 복구 키에 대 한 액세스를 요청한 사용자를 감사 합니다. 보고서는 원하는 필터링 조건을 기준으로 여러 필터를 제공 합니다. 사용자는 지원 센터 사용자 또는 최종 사용자, 요청 실패 여부, 요청 된 특정 키 형식, 검색을 수행 하는 날짜 범위 등 특정 유형의 사용자를 필터링 할 수 있습니다. 관리자는 필요에 따라 상황별 보고서를 만들 수 있습니다.

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
<td align="left"><p>요청 상태</p></td>
<td align="left"><p>요청 상태입니다. 유효한 상태는 성공적 (키 검색 됨) 또는 실패 (키가 검색 되지 않음) 중 하나입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>헬프데스크 사용자</p></td>
<td align="left"><p>키 검색 요청을 시작한 지원 센터 사용자입니다. 참고: 지원 센터 사용자가 최종 사용자에 게 해당 키를 대신 검색 하는 경우 최종 사용자 필드는 비어 있게 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자</p></td>
<td align="left"><p>키 검색 요청을 시작한 최종 사용자입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>키 유형</p></td>
<td align="left"><p>지원 센터 사용자 또는 최종 사용자가 요청한 키의 유형입니다. MBAM에는 복구 키 암호 (복구 모드에서 컴퓨터를 복구 하는 데 사용 됨), 복구 키 ID (다른 사용자 대신 복구 모드에서 컴퓨터를 복구 하는 데 사용 됨), TPM 암호 해시 (tpm이 잠겨 있는 컴퓨터를 복구 하는 데 사용 됨) 등 세 가지 키 유형이 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이유 설명</p></td>
<td align="left"><p>지정 된 키 유형이 지원 센터 사용자 또는 최종 사용자에 의해 요청 된 이유입니다. 이유는 관리 및 모니터링 웹 사이트의 TPM 및 복구 기능을 관리 하는 방법에 명시 되어 있습니다. 유효한 항목은 사용자가 입력 한 텍스트 이거나 다음 이유 코드 중 하나입니다.</p>
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

 

**참고**  보고서 메뉴 모음에서 **내보내기** 단추를 클릭 하 여 결과를 파일에 저장할 수 있습니다. MBAM 보고서를 실행 하는 방법에 대 한 자세한 내용은 [Mbam 보고서를 생성 하는 방법을](how-to-generate-mbam-reports-mbam-2.md)참조 하세요.

 

## 관련 항목


[MBAM 2.0으로 BitLocker 규정 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





