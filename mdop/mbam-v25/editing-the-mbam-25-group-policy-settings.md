---
title: MBAM 2.5 그룹 정책 설정 편집
description: MBAM 2.5 그룹 정책 설정 편집
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812596"
---
# MBAM 2.5 그룹 정책 설정 편집


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 다음을 수행 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 2.5 그룹 정책 템플릿을 복사 합니다.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">MBAM 2.5 그룹 정책 템플릿 복사</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 구현에 사용 하려는 Gpo (그룹 정책 개체)를 결정 합니다. 조직의 요구 사항에 따라 추가 그룹 정책 설정을 구성 해야 할 수 있습니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">MBAM 2.5 그룹 정책 요구 사항 계획 </a> – gpo에 대 한 설명이 포함 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>조직의 그룹 정책 설정을 설정 합니다.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다. **MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.

 

**MBAM 클라이언트 그룹 정책 설정을 편집 하려면**

1.  MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 MBAM 서비스를 사용할 수 있는지 확인 합니다.

2.  Mbam 그룹 정책 템플릿이 설치 된 컴퓨터에서 GPMC (그룹 정책 관리 콘솔) 또는 Microsoft 고급 그룹 정책 관리 MDOP 제품을 사용 하 여 **컴퓨터 구성** &gt; **정책** &gt; **관리 템플릿** , &gt; **Windows 구성 요소** &gt; **MDOP mbam (BitLocker 관리)** 을 선택 합니다.

3.  클라이언트 컴퓨터에서 MBAM 클라이언트 서비스를 사용 하도록 설정 하는 데 필요한 그룹 정책 설정을 편집 합니다. 다음 표의 각 정책에 대해 **정책 그룹**을 선택 하 고 원하는 **정책을** 클릭 한 다음 설정을 구성 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">정책 그룹</th>
    <th align="left">정책</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>클라이언트 관리</p></td>
    <td align="left"><p>MBAM 서비스 구성</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>운영 체제 드라이브</p></td>
    <td align="left"><p>운영 체제 드라이브 암호화 설정</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>이동식 드라이브</p></td>
    <td align="left"><p>이동식 드라이브에서 BitLocker 사용 제어</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>고정식 드라이브</p></td>
    <td align="left"><p>고정 드라이브의 BitLocker 사용 제어</p></td>
    </tr>
    </tbody>
    </table>

     

## 관련 항목


[MBAM 2.5 그룹 정책 요구 사항 계획](planning-for-mbam-25-group-policy-requirements.md)

[MBAM 2.5 그룹 정책 템플릿 복사](copying-the-mbam-25-group-policy-templates.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





