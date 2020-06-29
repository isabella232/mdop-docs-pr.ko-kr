---
title: 로깅 및 추적 설정
description: 로깅 및 추적 설정
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820593"
---
# 로깅 및 추적 설정


AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하면 이러한 설정의 GPO (그룹 정책 개체)가 적용 되는 AGPM 서버 및 클라이언트에 대 한 로깅 및 추적 옵션을 중앙에서 구성할 수 있습니다.

GPO를 편집할 때 컴퓨터 Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다.

**추적 파일 위치**:

-   클라이언트:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   서버:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>AGPM: 로깅 구성</strong></p></td>
<td align="left"><p>이 정책 설정을 통해 AGPM에 대 한 로깅을 설정 하 고 구성할 수 있습니다. 이 설정은 AGPM의 클라이언트 및 서버 구성 요소 모두에 영향을 줍니다.</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

-   [관리 템플릿 폴더](administrative-templates-folder-agpm30ops.md)

 

 





