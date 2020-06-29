---
title: 로깅 및 추적 설정
description: 로깅 및 추적 설정
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820588"
---
# 로깅 및 추적 설정


AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하면 이러한 설정의 GPO (그룹 정책 개체)가 적용 되는 AGPM 서버 및 클라이언트에 대 한 로깅 및 추적 옵션을 중앙에서 구성할 수 있습니다.

GPMC (그룹 정책 관리 콘솔)에서 GPO를 편집할 때 **그룹 정책 개체 편집기** 의 컴퓨터 Configuration\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다. 이 경로가 표시 되지 않으면 **관리 서식 파일**을 마우스 오른쪽 단추로 클릭 하 고 agpm 또는 agpm 템플릿을 추가 합니다.

**추적 파일 위치**:

-   클라이언트:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   서버:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>AGPM 로깅</strong></p></td>
<td align="left"><p>이 설정을 사용 하면 추적 설정 여부와 세부 정보 수준을 구성 합니다. 이 설정은 AGPM의 클라이언트 및 서버 구성 요소 모두에 영향을 줍니다.</p>
<p>이 설정을 사용 하지 않거나 구성 하지 않으면이 설정이 적용 되지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

-   [관리 템플릿 설정](administrative-template-settings.md)

 

 





