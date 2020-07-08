---
title: 제어된 GPO 명령
description: 제어된 GPO 명령
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821118"
---
# 제어된 GPO 명령


**제어** 탭:

-   AGPM (고급 그룹 정책 관리)에서 관리 하는 Gpo (그룹 정책 개체) 목록을 표시 합니다.

-   Gpo를 관리 하 고 Gpo에 대 한 기록 및 보고서를 표시 하는 명령이 포함 된 바로 가기 메뉴를 제공 합니다.

-   선택한 GPO에 대 한 액세스 권한이 있는 그룹 및 사용자의 목록을 표시 합니다.

이 탭에서 **그룹 정책 개체** 목록을 마우스 오른쪽 단추로 클릭 하면 바로 가기 메뉴가 표시 됩니다. 이 메뉴에는 다음 중 해당 되는 옵션이 포함 되어 있습니다.

## 제어 및 기록


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>새로운 제어 된 GPO</strong></p></td>
<td align="left"><p>AGPM에서 관리 되는 변경 컨트롤이 있는 새 GPO를 만들고이를 도메인의 프로덕션 환경에 배포 합니다. GPO를 만들 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다. (이 옵션은 다음을 마우스 오른쪽 단추로 클릭할 <strong> 때 GPO가 선택 되어 있지 않은 경우 표시 됩니다. 그룹 정책 개체 </strong> 목록.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>기록</strong></p></td>
<td align="left"><p>보관 함에 저장 된 선택한 GPO의 모든 버전이 나열 된 창을 엽니다. 기록에서 GPO 내의 설정에 대 한 보고서를 얻고, 두 버전의 GPO를 비교 하거나, GPO를 서식 파일과 비교 하거나, 이전 버전의 GPO로 롤백할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

## 보고


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>설정</strong></p></td>
<td align="left"><p>선택한 GPO 내의 설정을 표시 하는 HTML 기반 또는 XML 기반 보고서를 생성 하거나 GPO (들)가 최근에 제어, 가져오기 또는 체크 인 되었을 때의 조직 구성 단위에서 선택한 GPO에 대 한 링크를 표시 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>차이점</strong></p></td>
<td align="left"><p>선택한 두 Gpo 내의 설정과 선택한 GPO 및 서식 파일을 비교 하 여 HTML 기반 또는 XML 기반 보고서를 생성 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 편집


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Edit</strong></p></td>
<td align="left"><p><strong>그룹 정책 관리 편집기 창을 열어 </strong> 선택한 GPO를 변경 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>체크 아웃</strong></p></td>
<td align="left"><p>오프 라인으로 편집할 수 있도록 보관 저장소에서 선택한 GPO 복사본을 가져와 보관 저장소에 다시 체크 인 될 때까지 다른 사람이 GPO를 편집 하지 못하도록 합니다. 체크 아웃은 AGPM 관리자 (모든 권한)에 의해 재정의 될 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>체크인</strong></p></td>
<td align="left"><p>다른 승인 된 편집기에서 변경 하거나 승인자가 GPO를 도메인의 프로덕션 환경에 배포할 수 있도록 선택한 GPO의 편집 된 버전을 보관 함에 체크 인 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>체크 아웃 취소</strong></p></td>
<td align="left"><p>체크 아웃 된 GPO를 변경 하지 않고 보관 함으로 되돌립니다.</p></td>
</tr>
</tbody>
</table>

 

## 버전 관리


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>프로덕션에서 가져오기</strong></p></td>
<td align="left"><p>선택한 GPO에 대해 도메인의 프로덕션 환경에 있는 버전을 보관에 복사 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>파일에서 가져오기</strong></p></td>
<td align="left"><p>선택한 체크 아웃 된 GPO의 정책 설정을 GPO 백업 파일에서 해당 설정으로 바꿉니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>삭제</strong></p></td>
<td align="left"><p>선택한 GPO를 휴지통으로 이동 하 고 배포 된 버전 (있는 경우)을 프로덕션에 남길 것인지 아니면 아카이브의 버전 외에 배포 된 버전을 삭제할지를 지정 합니다. GPO를 삭제할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>배포</strong></p></td>
<td align="left"><p>선택한 GPO를 보관 함으로 체크 인 한 도메인의 프로덕션 환경으로 이동 합니다. 이 작업을 수행 하면 네트워크에서 활성화 되 고 이전에 GPO의 활성 버전 (있는 경우)이 덮어써집니다. GPO를 배포할 수 있는 권한이 없는 경우 요청을 제출 하 라는 메시지가 표시 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>다음으로 내보내기</strong></p></td>
<td align="left"><p>선택한 GPO를 다른 도메인에 복사할 수 있도록 백업 파일에 저장 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Label</strong></p></td>
<td align="left"><p>선택한 GPO에 설명 레이블 (예: &quot; 알려진 양호한 &quot; 레코드)과 기록 유지에 대 한 설명을 표시 합니다. 레이블은 <strong> 상태 열에 나타나며 </strong> <strong> 기록 창의 메모 열에 메모를 표시 </strong> <strong> </strong> 합니다. 또한 문제가 발생 하는 경우 롤백할 수 있도록 이전 버전의 GPO를 식별 하는 데 도움이 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>선택한 GPO의 이름을 변경 합니다. GPO가 이미 배포 된 경우 GPO를 재배포 하면 도메인의 프로덕션 환경에서 이름이 업데이트 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>서식 파일로 저장</strong></p></td>
<td align="left"><p>선택한 GPO의 설정을 기반으로 새 서식 파일을 만듭니다.</p></td>
</tr>
</tbody>
</table>

 

## 기타


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>새로 고침</strong></p></td>
<td align="left"><p>변경 내용을 통합 하기 위해 GPMC (그룹 정책 관리) 콘솔의 표시를 업데이트 합니다. 일부 변경 내용은 디스플레이를 새로 고칠 때까지 표시 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Help</strong></p></td>
<td align="left"><p>AGPM에 대 한 도움말을 표시 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

-   [내용 탭](contents-tab-agpm40.md)

-   [편집기 작업 수행](performing-editor-tasks-agpm40.md)

-   [승인자 작업 수행](performing-approver-tasks-agpm40.md)

-   [검토자 작업 수행](performing-reviewer-tasks-agpm40.md)

 

 





