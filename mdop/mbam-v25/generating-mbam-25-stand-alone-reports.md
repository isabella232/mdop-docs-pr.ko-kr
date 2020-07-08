---
title: MBAM 2.5 독립 실행형 보고서 생성
description: MBAM 2.5 독립 실행형 보고서 생성
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823123"
---
# MBAM 2.5 독립 실행형 보고서 생성


독립 실행형 토폴로지로 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 구성할 때 BitLocker 드라이브 암호화 사용 및 준수를 모니터링 하는 보고서를 생성할 수 있습니다. 이 항목에서는 다음 절차에 대해 설명 합니다.

-   [관리 및 모니터링 웹 사이트를 열려면](#bkmk-openadmin)

-   [엔터프라이즈 준수 보고서를 생성 하려면](#bkmk-enterprise)

-   [컴퓨터 준수 보고서를 생성 하려면](#bkmk-computercomp)

-   [복구 키 감사 보고서를 생성 하려면](#bkmk-recoverykey)

독립 실행형 보고서에 대 한 설명은 [MBAM 2.5 독립 실행형 보고서 이해](understanding-mbam-25-stand-alone-reports.md)를 참조 하세요.

**참고**  보고서를 실행 하려면 Active Directory 도메인 서비스에서 구성한 **Mbam 보고서 사용자** 그룹의 구성원 이어야 합니다. 자세한 내용은 [MBAM 2.5 그룹 및 계정 계획](planning-for-mbam-25-groups-and-accounts.md)을 참조 하세요.

 

<a href="" id="bkmk-openadmin"></a>**관리 및 모니터링 웹 사이트를 열려면**

1.  웹 브라우저를 열고 관리 및 모니터링 웹 사이트로 이동 합니다. 관리 및 모니터링 웹 사이트의 기본 URL은 다음과 같습니다.

    *http (s)// &lt; MBAMAdministrationServerName &gt; : &lt; 포트 &gt; /helpdesk*

2.  왼쪽 창에서 **보고서**를 클릭 합니다. 위쪽 메뉴 모음에서 실행할 보고서를 선택 합니다.

    MBAM 클라이언트 데이터는 컴퓨터를 분실 하거나 도난당 한 경우 기록 참조에 대 한 준수 및 감사 데이터베이스에 유지 됩니다. Enterprise 보고서를 실행할 때 적절 한 시작 및 종료 날짜를 사용 하 여 보고서 데이터의 정확성을 높이기 위해 1 ~ 2 주 동안 보고 하는 시간 프레임의 범위를 지정 하는 것이 좋습니다.

    보고서를 생성 한 후에는 HTML, Microsoft Word, Microsoft Excel 등의 다양 한 형식으로 결과를 저장할 수 있습니다.

    **참고**  관리 및 모니터링 웹 사이트를 구성 하기 전에 SSL (Secure Sockets layer)을 사용 하도록 SSRS (SQL Server Reporting Services)를 구성 합니다. 어떤 이유로 든 지 SSRS가 SSL을 사용 하도록 구성 되어 있지 않은 경우, 관리 및 모니터링 웹 사이트를 구성할 때 보고서의 URL이 HTTPS 대신 HTTP로 설정 됩니다. 그런 다음 관리 및 모니터링 웹 사이트로 이동 하 여 보고서를 선택 하면 "보안 콘텐츠만 표시 됩니다." 라는 메시지가 표시 됩니다. 보고서를 표시 하려면 **모든 콘텐츠 표시**를 클릭 합니다.

     

<a href="" id="bkmk-enterprise"></a>**엔터프라이즈 준수 보고서를 생성 하려면**

1.  관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택 하 고 **엔터프라이즈 준수 보고서**를 선택한 다음 사용할 필터를 선택 합니다. 엔터프라이즈 준수 보고서에 사용할 수 있는 필터는 다음과 같습니다.

    -   **준수 상태**. 이 필터를 사용 하 여 보고서의 준수 상태 유형을 지정 합니다 (예: 규격 또는 비규격).

    -   **오류 상태**입니다. 이 필터를 사용 하 여 보고서의 오류 상태 유형을 지정 합니다 (예: 오류 또는 오류 없음).

2.  **보고서 보기** 를 클릭 하 여 선택한 보고서를 표시 합니다.

3.  컴퓨터 이름을 선택 하 여 컴퓨터 준수 보고서에 컴퓨터에 대 한 정보를 표시 합니다.

4.  컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.

<a href="" id="bkmk-computercomp"></a>**컴퓨터 준수 보고서를 생성 하려면**

1.  관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택한 다음 **컴퓨터 준수 보고서**를 선택 합니다. 컴퓨터 준수 보고서를 사용 하 여 **사용자 이름** 또는 **컴퓨터 이름을**검색 합니다.

2.  **보고서 보기** 를 클릭 하 여 컴퓨터 준수 보고서를 봅니다.

3.  컴퓨터 이름을 선택 하 여 컴퓨터 준수 보고서에 컴퓨터에 대 한 추가 정보를 표시 합니다.

4.  컴퓨터 이름 옆에 있는 더하기 기호 (+)를 선택 하 여 컴퓨터에 있는 볼륨에 대 한 정보를 확인 합니다.

    **참고**  컴퓨터가 MBAM 그룹 정책 설정의 요구 사항을 충족 하거나 초과 하는 경우 MBAM 클라이언트 컴퓨터는 규격으로 간주 됩니다.

<a href="" id="bkmk-recoverykey"></a>**복구 키 감사 보고서를 생성 하려면**

1.  관리 및 모니터링 웹 사이트의 왼쪽 탐색 창에서 **보고서** 노드를 선택한 다음 **복구 감사 보고서**를 선택 합니다. 복구 키 감사 보고서에 대 한 필터를 선택 합니다. 복구 키 감사에 사용할 수 있는 필터는 다음과 같습니다.

    -   **헬프데스크 사용자**. 이 필터는 사용자가 요청자의 사용자 이름을 지정할 수 있도록 합니다. 요청자는 최종 사용자를 대신 하 여 키에 액세스 한 지원 센터의 사용자입니다.

    -   **최종 사용자**. 이 필터는 사용자가 requestee의 사용자 이름을 지정할 수 있도록 합니다. Requestee는 지원 센터를 호출 하 여 복구 키를 획득 하는 최종 사용자입니다.

    -   **요청 결과**. 이 필터는 사용자가 보고서의 기반으로 사용할 요청 결과 형식 (예: 성공 또는 실패)을 지정할 수 있도록 합니다. 예를 들어 사용자가 실패 한 키 액세스 시도를 보려고 할 수 있습니다.

    -   **키 유형**입니다. 이 필터는 사용자가 보고서의 기반으로 사용할 키 유형 (예: 복구 키 암호 또는 TPM 암호 해시)을 지정할 수 있도록 합니다.

    -   **시작 날짜**입니다. 이 필터는 사용자가 보고 하려는 날짜 범위의 시작 날짜 부분을 정의 하는 데 사용 됩니다.

    -   **종료 날짜**입니다. 이 필터는 사용자가 보고 하려는 날짜 범위의 끝 날짜 부분을 정의 하는 데 사용 됩니다.

2.  보고서 **보기** 를 클릭 하 여 보고서를 봅니다.



## 관련 항목


[MBAM 2.5로 BitLocker 규정 준수 모니터링 및 보고](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[MBAM 2.5 독립 실행형 보고서 이해](understanding-mbam-25-stand-alone-reports.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





