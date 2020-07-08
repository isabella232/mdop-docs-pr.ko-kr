---
title: 전자 소프트웨어 배포 시스템을 사용하여 App-V 5.0 배포 계획
description: 전자 소프트웨어 배포 시스템을 사용하여 App-V 5.0 배포 계획
author: dansimp
ms.assetid: 8cd3f1fb-b84e-4260-9e72-a14d01e7cadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ca441820be7e6759e65902aea18b2db7f989e8f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813404"
---
# 전자 소프트웨어 배포 시스템을 사용하여 App-V 5.0 배포 계획


전자 소프트웨어 배포 시스템을 사용 하 여 App-v 패키지를 배포 하는 경우 다음 계획 고려 사항을 검토 하세요. System Center Configuration Manager를 사용 하 여 App-v를 배포 하는 방법에 대 한 자세한 내용은 [구성 관리자의 응용 프로그램 관리 소개](https://go.microsoft.com/fwlink/?LinkId=281816)를 참조 하세요.

ESD를 사용 하 여 App-v 패키지를 배포할 때 적용 되는 다음 구성 요소 및 아키텍처 요구 사항 옵션을 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">배포 요구 사항 또는 옵션</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>앱-V 관리 서버, 관리 데이터베이스 및 게시 서버는 필요 하지 않습니다.</p></td>
<td align="left"><p>이러한 함수는 구현 된 ESD 솔루션에 의해 처리 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V 보고 서버와 보고 데이터베이스를 ESD와 나란히 배포할 수 있습니다.</p></td>
<td align="left"><p>Side-by-side 배포를 사용 하 여 데이터를 수집 하 고 보고서를 생성할 수 있습니다.</p>
<p>앱-V 클라이언트가 보고서 정보를 보낼 수 있도록 설정 하 고 App-v 보고서 서버를 사용 하지 않는 경우 보고 데이터는 관련 .xml 파일에 저장 됩니다.</p></td>
</tr>
</tbody>
</table>

 






 

 





