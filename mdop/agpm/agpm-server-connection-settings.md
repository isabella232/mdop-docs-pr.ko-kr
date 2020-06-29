---
title: AGPM 서버 연결 설정
description: AGPM 서버 연결 설정
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813020"
---
# AGPM 서버 연결 설정


AGPM (고급 그룹 정책 관리)의 관리 템플릿 설정을 사용 하 여 해당 설정의 GPO (그룹 정책 개체)가 적용 되는 그룹 정책 관리자에 대 한 AGPM 서버 연결을 중앙에서 구성할 수 있습니다.

GPO를 편집할 때 사용자 Configuration\\Administrative Templates\\Windows Components\\AGPM에서 다음 설정을 사용할 수 있습니다. 이 경로가 표시 되지 않으면 **관리 서식 파일**을 마우스 오른쪽 단추로 클릭 하 고 agpm 또는 agpm 템플릿을 추가 합니다.

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
<td align="left"><p><strong>AGPM 서버 (모든 도메인)</strong></p></td>
<td align="left"><p>이 설정을 사용 하면 모든 도메인에서 사용할 수 있도록 하나의 AGPM 서버 연결을 중앙에서 구성 하 고 <strong> </strong> 그룹 정책 관리자 용 agpm 서버 탭의 설정을 사용 하지 않도록 설정 합니다. 여러 AGPM 서버의 경우 기본 서버로이 설정을 구성한 다음 <strong> 관리 템플릿에서 AGPM 서버 설정을 구성 하 여 </strong> 다른 도메인에 대해이 서버를 재정의 합니다.</p>
<p>이 기능을 사용 하지 않거나 구성 하지 않으면 각 그룹 정책 관리자가 agpm <strong> 의 Agpm 서버 탭에서 각 도메인에 대해 표시할 Agpm 서버를 선택 해야 합니다 </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM 서버</strong></p></td>
<td align="left"><p>이 설정을 사용 하면 <strong> 관리 템플릿에서 AGPM 서버 (모든 도메인) 설정을 재정의 하 여 여러 도메인 관련 AGPM 서버를 중앙에서 구성 </strong> 합니다. 환경에 단일 AGPM 서버만 필요한 경우 <strong> 관리 템플릿에서 Agpm 서버 (모든 도메인) 설정만 사용 </strong> 합니다.</p>
<p>이 기능을 사용 하지 않거나 구성 하지 않으면 <strong> 관리 템플릿에서 Agpm 서버 (모든 도메인) </strong> 설정이 agpm 서버 연결을 구성 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

-   [관리 템플릿 설정](administrative-template-settings.md)

-   [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks.md)

 

 





