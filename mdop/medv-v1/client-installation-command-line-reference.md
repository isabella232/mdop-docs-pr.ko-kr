---
title: 클라이언트 설치 명령줄 참조
description: 클라이언트 설치 명령줄 참조
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826728"
---
# 클라이언트 설치 명령줄 참조


**명령줄에서 MED-V를 설치 하려면**

1.  명령줄에서 다음 표에 설명 된 선택적 매개 변수를 모두 사용한 다음에 MED-V .msi 패키지를 실행 합니다.

2.  MED-V 패키지는 *MED-V\_x.msi*호출 되며 여기서 *x* 는 버전 번호입니다.

    예를 들어 *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">값</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/quiet</p></td>
<td align="left"><p></p></td>
<td align="left"><p>자동 설치</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;로그 파일의/log full 경로&gt;</p></td>
<td align="left"><p>로그 파일의 전체 경로입니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>설치 디렉터리의 전체 경로입니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>가상 컴퓨터 폴더의 전체 경로입니다.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>기본값: <strong> 0</strong></p></td>
<td align="left"><p>MED-V 관리 도구를 설치 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>기본값: <strong> 0</strong></p></td>
<td align="left"><p>사용자가 Windows에 로그온 할 때마다 MED-V 클라이언트가 자동으로 시작 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>호스트 이름 또는 IP</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>포트</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p><strong>https </strong> 또는 <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>기본값: <strong> 1</strong></p></td>
<td align="left"><p>MED-V 설치가 완료 되 면 MED-V가 시작 됩니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>MED-V가 시스템에 설치 되어 있는 경우를 대비 하 여 START_MEDV = 0을 설정 하는 것이 좋습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1, 0</strong></p>
<p>기본값: <strong> 1</strong></p></td>
<td align="left"><p>바탕 화면에 MED-V 클라이언트를 시작 하는 바로 가기를 만듭니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>RAM (MB)</p></td>
<td align="left"><p>MED-V를 설치 하는 경우 컴퓨터에 최소 크기의 RAM이 지정 되어 있는지 확인 합니다. 그렇지 않으면 설치가 중단 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1, 0</strong></p></td>
<td align="left"><p>운영 체제 유효성 검사를 생략 합니다.</p></td>
</tr>
</tbody>
</table>











