---
title: 검사 목록 GPO 만들기, 편집 및 배포
description: 검사 목록 GPO 만들기, 편집 및 배포
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819103"
---
# 검사 목록: GPO 만들기, 편집 및 배포


AGPM (고급 그룹 정책 관리)을 사용 하 여 여러 사용자가 Gpo (그룹 정책 개체)를 변경 하는 환경에서 AGPM 관리자 (모든 권한)가 편집자, 승인자 및 검토자에 게 권한을 그룹 또는 개인으로 위임 합니다. 다음은 편집기 및 승인자에 대 한 일반적인 GPO 개발 프로세스입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">참고자료</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>편집자 요청 새 GPO를 만들거나 승인자가 새 GPO를 만듭니다.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">새 제어된 GPO 만들기 요청</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">새 제어된 GPO 만들기</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>승인자는 편집자에 의해 요청 된 GPO 만들기를 승인 합니다.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">보류 중인 작업 승인 또는 거부</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>편집자는 다른 사람이 GPO를 수정할 수 없도록 저장소에서 GPO 복사본을 체크 아웃 합니다. 편집기에서 GPO를 변경한 다음 수정 된 GPO를 보관 함으로 확인 합니다.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">오프라인에서 GPO 편집</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>테스트 포리스트에서 개발 하는 경우, 편집자는 GPO를 파일로 내보내고, 파일을 프로덕션 포리스트로 전송 하 고, 파일을 가져옵니다. 또한 편집기는 테스트 컴퓨터 및 사용자가 포함 된 조직 구성 단위에 GPO를 연결할 수 있습니다.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">테스트 환경 사용</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>편집자-GPO를 도메인의 프로덕션 환경에 배포 하도록 요청 합니다.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">GPO의 배포 요청</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>검토자 (예: 승인자 또는 편집자)가 GPO를 분석 합니다.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">검토자 작업 수행</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>승인자는 GPO를 승인 하 고 도메인의 프로덕션 환경으로 배포 하거나 GPO를 거부 합니다.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">보류 중인 작업 승인 또는 거부</a></p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

[고급 그룹 정책 관리 4.0](advanced-group-policy-management-40.md)

 

 





