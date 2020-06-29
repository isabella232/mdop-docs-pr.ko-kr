---
title: 관리자만 연결 그룹을 사용 설정할 수 있도록 허용하는 방법
description: 관리자만 연결 그룹을 사용 설정할 수 있도록 허용하는 방법
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814460"
---
# 관리자만 연결 그룹을 사용 설정할 수 있도록 허용하는 방법


관리자 (최종 사용자가 아님)만 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있도록 App-v 클라이언트를 구성할 수 있습니다. 이전 버전의 App-v에서는 최종 사용자가 이러한 작업을 수행 하는 것을 방지할 수 없었습니다.

**참고** 
 **이 기능은 app-v 5.0 SP3에서 시작 하는 것으로 지원 됩니다.**

 

다음 방법 중 하나를 사용 하 여 관리자만 연결 그룹을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">메서드</th>
<th align="left">단계</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>그룹 정책 설정</p></td>
<td align="left"><p>다음 그룹 정책 개체 노드에 있는 "관리자로 게시 필요" 그룹 정책 설정을 사용 하도록 설정 합니다.</p>
<p><strong>컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell Cmdlet</p></td>
<td align="left"><p><strong> </strong> <strong> – RequireAppvClientConfiguration cmdlet 관리자 매개 변수를 사용 하 여 명령줄을 실행 합니다 </strong> .</p>
<p>매개 변수 값:</p>
<ul>
<li><p>0-거짓</p></li>
<li><p>1-참</p></li>
</ul>
<p><strong>예: </strong> : Set-AppvClientConfiguration-RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

**App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[연결 그룹 관리](managing-connection-groups.md)

 

 





