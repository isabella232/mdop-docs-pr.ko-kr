---
title: 프로덕션 환경에 대한 액세스 권한 위임
description: 프로덕션 환경에 대한 액세스 권한 위임
author: dansimp
ms.assetid: c1ebae2e-909b-4e64-b368-b7d3cc67b1eb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4667a23f1584d7aab6143860721e326da6407afb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821013"
---
# 프로덕션 환경에 대한 액세스 권한 위임


프로덕션 환경의 Gpo (그룹 정책 개체)에 대 한 액세스를 변경 하 여 해당 Gpo의 기존 사용 권한을 바꿀 수 있습니다. 사용자가 GPMC (그룹 정책 관리) 콘솔의 **변경 제어** 폴더를 사용 하지 않는 경우 프로덕션 환경에서 gpo의 보안을 편집, 삭제 또는 수정할 수 없도록 도메인 수준에서 사용 권한을 구성할 수 있습니다.

**참고**  
-   프로덕션 환경에 대 한 액세스 위임은 사용자의 Gpo 연결 기능에 영향을 주지 않습니다.

-   Gpo를 제어 하거나 배포 하는 경우 **읽기** 및 **적용** 권한이 있는 다른 계정에 대 한 액세스는 제거 됩니다.

 

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 필요한 사용 권한이 나 AGPM 관리자 (모든 권한)의 역할을 갖는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**프로덕션 환경의 Gpo에 대 한 액세스 권한 변경**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **프로덕션 위임** 탭을 클릭 합니다.

3.  프로덕션 환경에 액세스할 수 없는 사용자 또는 그룹에 대 한 사용 권한을 추가 하거나 액세스 권한이 있는 사용자 또는 그룹에 대 한 사용 권한을 바꾸려면 다음을 수행 합니다.

    1.  **추가**를 클릭 하 고 사용자 또는 그룹을 선택한 다음 **확인**을 클릭 합니다.

    2.  프로덕션 환경을 위해 해당 사용자 또는 그룹에 위임할 권한을 선택 하 고 **확인**을 클릭 합니다.

4.  사용자 또는 그룹의 프로덕션 환경에 대 한 모든 사용 권한을 제거 하려면 사용자 또는 그룹을 선택 하 고 **제거**를 클릭 한 다음 **확인**을 클릭 합니다.

### 추가 고려 사항

-   기본적으로이 절차를 수행 하려면 AGPM 관리자 (모든 권한) 여야 합니다. 특히, 도메인에 대 한 **보안 수정** 권한이 있어야 합니다.

-   AGPM 서비스 계정에 대 한 사용 권한은 **프로덕션 위임** 탭에서 변경할 수 없습니다.

-   기본적으로 다음 계정에는 프로덕션 환경의 Gpo에 대 한 사용 권한이 있습니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">계정</th>
    <th align="left">Gpo의 기본 사용 권한</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>&lt;AGPM 서비스 계정&gt;</p></td>
    <td align="left"><p>설정 편집, 삭제, 보안 수정</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>인증 된 사용자</p></td>
    <td align="left"><p>읽기, 적용</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>도메인 관리자</p></td>
    <td align="left"><p>설정 편집, 삭제, 보안 수정</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>엔터프라이즈 관리자</p></td>
    <td align="left"><p>설정 편집, 삭제, 보안 수정</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>엔터프라이즈 도메인 컨트롤러</p></td>
    <td align="left"><p>Read</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>시스템</p></td>
    <td align="left"><p>설정 편집, 삭제, 보안 수정</p></td>
    </tr>
    </tbody>
    </table>

     

-   그룹 정책 작성자 겸 소유자 그룹의 구성원은 제한 되어야 하며, Gpo에 대 한 액세스를 AGPM에서 관리 하는 데 사용 되지 않습니다. ( **그룹 정책 관리 콘솔**에서 gpo를 관리 하려는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 하 고 **위임을**클릭 한 다음 조직의 요구 사항에 맞게 설정을 구성 합니다.)

### 추가 참조

-   [고급 그룹 정책 관리 구성](configuring-advanced-group-policy-management.md)

 

 





