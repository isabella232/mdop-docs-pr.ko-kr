---
title: 서버 로깅 수준 및 데이터베이스 매개 변수를 변경하는 방법
description: 서버 로깅 수준 및 데이터베이스 매개 변수를 변경하는 방법
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818033"
---
# 서버 로깅 수준 및 데이터베이스 매개 변수를 변경하는 방법


다음 절차를 사용 하 여 응용 프로그램 가상화 서버 관리 콘솔에서 로그 수준과 데이터베이스 로그 매개 변수를 변경할 수 있습니다.

다음과 같은 로깅 수준을 사용할 수 있습니다.

-   트랜잭션만

-   치명적 오류

-   오류

-   경고/오류

-   Info/경고/오류

-   자세한 정보 표시

**참고**  **Verbose** 모드를 사용할 때 생성 되는 로그 파일의 크기 때문에이 수준의 로깅 설정으로 프로덕션 서버를 실행 하지 않는 것이 좋습니다.

 

데이터베이스 로깅 매개 변수는 데이터베이스 드라이버 형식, 액세스 자격 증명 및 로깅 데이터베이스의 위치를 결정 합니다.

**관리 서버에 대 한 로깅 수준을 변경 하려면**

1.  서버 **그룹** 노드를 클릭 하 여 서버 그룹을 표시 합니다.

2.  서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.

3.  **속성** 대화 상자에서 **로깅** 탭을 선택 합니다.

4.  **서버 그룹 속성** 대화 상자에서 서버를 선택한 다음 **편집**을 클릭 합니다.

5.  **로그 모듈 추가/편집** 대화 상자의 **이벤트 유형** 드롭다운 목록에서 로깅 수준을 선택 합니다.

6.  **확인**을 클릭합니다.

7.  **서버 그룹 속성** 대화 상자에서 **확인** 또는 **적용**을 클릭 합니다.

**스트리밍 서버의 로깅 수준을 변경 하려면**

1.  다음 레지스트리 키 값을 편집 하 여 로깅 수준을 변경 합니다.

    -   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel

2.  다음 값 중 하나를 선택 하 여 로깅 수준을 설정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">값</th>
    <th align="left">로깅 수준</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>0</p></td>
    <td align="left"><p>트랜잭션만</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>raid-1</p></td>
    <td align="left"><p>치명적 오류</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>2</p></td>
    <td align="left"><p>오류</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>3-4</p></td>
    <td align="left"><p>경고/오류</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>4(tcp/ipv4)</p></td>
    <td align="left"><p>정보/경고/오류</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>5mb</p></td>
    <td align="left"><p>자세한 정보 표시</p></td>
    </tr>
    </tbody>
    </table>

     

**데이터베이스 로그 매개 변수를 변경 하려면**

1.  서버 **그룹** 노드를 클릭 하 여 서버 그룹을 표시 합니다.

2.  서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.

3.  **속성** 대화 상자에서 **로깅** 탭을 선택 합니다.

4.  **서버 그룹 속성** 대화 상자에서 서버를 선택한 다음 **편집**을 클릭 합니다.

5.  **로그 모듈 추가/편집** 대화 상자의 **데이터베이스 드라이버** 드롭다운 목록에서 데이터베이스 드라이버를 선택 합니다.

6.  **DNS 호스트 이름을**입력 합니다.

7.  **동적으로 포트 결정** 확인란을 클릭 하거나 포트 필드에 포트 번호를 입력 **합니다.**

8.  해당 필드에 **서비스 이름을** 입력 합니다.

9.  **확인**을 클릭합니다.

10. **서버 그룹 속성** 대화 상자에서 **확인** 또는 **적용**을 클릭 합니다.

## 관련 항목


[Server Management Console에서 Application Virtualization 시스템을 사용자 지정하는 방법](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





