---
title: AGPM 서버 연결 설정
description: AGPM 서버 연결 설정
author: dansimp
ms.assetid: 5f03e397-b868-4c49-9cbf-a5f5d0ddcc39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ee1e67eb2c565bcf833314d82cdf611e2caa85
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812988"
---
# AGPM 서버 연결 설정


AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하 여 해당 설정의 GPO (그룹 정책 개체)가 적용 되는 그룹 정책 관리자에 대 한 AGPM 서버 연결을 중앙에서 구성할 수 있습니다.

GPO를 편집할 때 사용자 Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">설정</th>
<th align="left">효과</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM: 기본 AGPM 서버 (모든 도메인) 지정</strong></p></td>
<td align="left"><p>이 정책 설정을 통해 모든 도메인에 대 한 기본 AGPM 서버를 지정할 수 있습니다. 이는 AGPM 클라이언트 에서만 사용 되며 그룹 정책 관리자가 다른 보관 저장소에 연결 하는 것을 제한 합니다. <strong>Agpm: Agpm 서버 지정 설정을 사용 하 여 개별 도메인에 대해이 기본값을 재정의할 수 있습니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM: AGPM 서버 지정</strong></p></td>
<td align="left"><p>이 정책 설정을 통해 개별 도메인에 대해 AGPM 서버를 지정할 수 있습니다. 이는 AGPM 클라이언트 에서만 사용 되며 그룹 정책 관리자가 지정 된 도메인의 다른 아카이브에 연결 하는 것을 제한 합니다. 기본 AGPM 서버를 지정 하려면 <strong> agpm: 기본 Agpm 서버 (모든 도메인) 설정을 지정 하 </strong> 고이 정책 설정을 사용 하 여 도메인 별로 기본값을 재정의 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

-   [관리 템플릿 폴더](administrative-templates-folder-agpm30ops.md)

-   [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





