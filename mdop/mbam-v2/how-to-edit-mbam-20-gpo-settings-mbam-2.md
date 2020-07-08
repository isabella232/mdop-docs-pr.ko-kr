---
title: MBAM 2.0 GPO 설정을 편집하는 방법
description: MBAM 2.0 GPO 설정을 편집하는 방법
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824088"
---
# MBAM 2.0 GPO 설정을 편집하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 먼저 Microsoft BitLocker 관리 및 모니터링 구현에서 사용할 그룹 정책을 결정 해야 합니다. 사용할 수 있는 다양 한 정책에 대 한 자세한 내용은 [MBAM 2.0 그룹 정책 요구 사항 계획](planning-for-mbam-20-group-policy-requirements-mbam-2.md) 을 참조 하세요. 사용할 정책을 결정 한 후에는 MBAM에 대 한 정책 설정을 포함 하는 하나 이상의 GPO (그룹 정책 개체)를 수정 해야 합니다.

다음 단계를 사용 하 여 사용자 조직의 클라이언트 컴퓨터에 대 한 BitLocker 암호화를 관리 하기 위해 MBAM을 사용 하도록 기본 권장 GPO 설정을 구성할 수 있습니다.

**MBAM 클라이언트 GPO 설정을 편집 하려면**

1.  MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 MBAM 서비스를 사용할 수 있는지 확인 합니다.

2.  MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리) MDOP 제품을 사용 하 고, **컴퓨터 구성을**선택 하 고, **정책을**선택 하 고, **관리 템플릿을**클릭 하 고, **Windows 구성 요소**를 선택한 다음 **MDOP mbam (BitLocker Management)** 을 클릭 합니다.

3.  클라이언트 컴퓨터에서 MBAM 클라이언트 서비스를 사용 하도록 설정 하는 데 필요한 그룹 정책 개체 설정을 편집 합니다. 다음 표의 각 정책에 대해 **정책 그룹**을 선택 하 고 **정책을**클릭 한 다음 **설정을**구성 합니다.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">정책 그룹</th>
    <th align="left">정책</th>
    <th align="left">설정</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>클라이언트 관리</p></td>
    <td align="left"><p>MBAM 서비스 구성</p></td>
    <td align="left"><p>활성화. <strong>Mbam 복구 및 하드웨어 서비스 끝점 </strong> 을 설정 하 고 <strong> 저장할 BitLocker 복구 정보를 선택 </strong> 합니다. <strong>Mbam 준수 서비스 끝점 </strong> 을 설정 하 고 상태 보고서 빈도를 (분)에 입력 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>운영 체제 드라이브</p></td>
    <td align="left"><p>운영 체제 드라이브 암호화 설정</p></td>
    <td align="left"><p>활성화. <strong>운영 체제 드라이브에 대 한 선택 보호 기능을 설정 </strong> 합니다. 운영 체제 드라이브 데이터를 MBAMKey 복구 서버에 저장 하는 데 필요 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>이동식 드라이브</p></td>
    <td align="left"><p>이동식 드라이브에서 BitLocker 사용 제어</p></td>
    <td align="left"><p>활성화. MBAM이 MBAM 키 복구 서버에 이동식 드라이브 데이터를 저장 하는 경우 필요 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>고정식 드라이브</p></td>
    <td align="left"><p>고정 드라이브의 BitLocker 사용 제어</p></td>
    <td align="left"><p>활성화. MBAM은 고정 드라이브 데이터를 MBAM 키 복구 서버에 저장 하는 데 필요 합니다.</p>
    <p>설정 <strong> BitLocker로 보호 되는 드라이브를 복구 하 </strong> 고 <strong> 데이터 복구 에이전트를 허용 하는 방법을 선택 </strong> 합니다.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## 관련 항목


[MBAM 2.0 그룹 정책 개체 배포](deploying-mbam-20-group-policy-objects-mbam-2.md)









