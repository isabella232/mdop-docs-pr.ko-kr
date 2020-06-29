---
title: 다른 SQL Server로 App-V SQL 데이터베이스를 마이그레이션하는 방법
description: 다른 SQL Server로 App-V SQL 데이터베이스를 마이그레이션하는 방법
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817073"
---
# 다른 SQL Server로 App-V SQL 데이터베이스를 마이그레이션하는 방법


다음 절차에서는 App-v (Microsoft Application Virtualization) 관리 서버의 SQL 데이터베이스를 다른 SQL Server로 마이그레이션하는 방법에 대해 자세히 설명 합니다.

**중요**  이 절차를 수행 하려면 App-v 서버 서비스가 중지 되어 최종 사용자가 해당 응용 프로그램을 사용 하지 못하게 됩니다.

 

**App-v SQL 데이터베이스를 백업 하려면**

1.  서비스 .msc 프로그램을 열고 마이그레이션할 데이터베이스를 사용 하는 모든 관리 서버에서 App-v 관리 서버 서비스를 중지 합니다.

2.  App-v 데이터베이스가 있는 컴퓨터에서 SQL Server Management Studio를 엽니다.

3.  **데이터베이스** 노드를 확장 하 여 app-v 데이터베이스를 찾습니다 (기본 이름은 APPVIRT입니다).

4.  데이터베이스를 마우스 오른쪽 단추로 클릭 하 고 **작업** 을 선택한 다음 **백업을**선택 합니다.

5.  **복구 모델이** **SIMPLE** 으로 설정 되어 있고 **백업 유형이** **Full**로 설정 되어 있는지 확인 합니다. 필요한 경우 **백업 집합과** **대상** 설정을 변경 합니다.

6.  **확인** 을 클릭 하 여 데이터베이스를 백업 합니다. 백업이 성공적으로 완료 되 면 **확인**을 클릭 합니다.

7.  Windows 탐색기를 열고 데이터베이스 백업 파일 (예: APPVIRT)이 포함 된 폴더를 찾습니다. K. 데이터베이스 백업 파일을 SQL Server를 실행 하는 대상 컴퓨터에 복사 합니다.

**대상 컴퓨터로 App-v SQL 데이터베이스 복원**

1.  대상 컴퓨터에서 SQL Server Management Studio를 열고 **데이터베이스** 노드를 마우스 오른쪽 단추로 클릭 하 고 **데이터베이스 복원을**선택 합니다.

2.  **복원할 원본**에서 **장치에서** 를 선택한 다음 "**...**"를 클릭 합니다. 단추를 선택합니다.

3.  **백업 지정** 대화 상자에서 **백업 미디어가** **파일로** 설정 되어 있는지 확인 한 다음 **추가**를 클릭 합니다.

4.  SQL Server를 실행 하는 원래 컴퓨터에서 복사한 백업 파일을 선택한 다음 **확인을**클릭 합니다.

5.  **확인** 을 클릭 한 다음 복원에 대 한 백업 집합을 클릭 하 여 선택 합니다.

6.  **복원할 대상**에서 **데이터베이스에** 대 한 드롭다운을 클릭 하 고 app-v 데이터베이스 이름 (예: APPVIRT을 선택 합니다.

7.  **확인** 을 클릭 하 여 복원을 시작 합니다. 복원이 성공적으로 완료 되 면 **확인**을 클릭 합니다.

8.  **보안** 노드를 확장 하 고 **로그인** 을 마우스 오른쪽 단추로 클릭 한 다음 **새 로그인**을 선택 합니다.

9.  **로그인 이름** 필드에 DOMAIN\\SERVERNAME $의 형식으로 App-v 관리 서버에 대 한 네트워크 서비스 계정 정보를 입력 합니다.

10. **기본 데이터베이스** 아래의 **일반** 페이지에서 app-v 데이터베이스 이름 (예: APPVIRT)을 선택한 다음 **확인**을 클릭 합니다.

11. **페이지 선택**에서 **사용자 매핑** 페이지를 클릭 하 여 선택 합니다. **이 로그인에 매핑된 사용자**에서 **지도** 열의 확인란을 클릭 하 여 app-v 데이터베이스를 선택 합니다.

12. **데이터베이스 역할 구성원: &lt; Appvdatabasename &gt; **에서 **SFTEveryone** 을 클릭 하 여 선택한 다음 **확인**을 클릭 합니다.

13. SQL Server를 실행 하는 새 컴퓨터의 Windows 방화벽이 App-v 관리 서버에서 시스템에 액세스할 수 있도록 구성 되어 있는지 확인 합니다. **관리 도구**아래에서 **고급 보안이 포함 된 Windows 방화벽** 프로그램을 사용 하 여 SQL Server에서 사용 되는 포트에 대 한 **인바운드 규칙** 을 만듭니다 (기본값은 포트 1433).

**App-v SQL Server 에이전트 작업을 마이그레이션하려면**

1.  SQL Server를 실행 하는 원래 컴퓨터의 SQL server Management Studio에서 **Sql Server 에이전트** 노드를 확장 한 다음 **작업** 노드를 확장 합니다.

2.  다음 4 개의 App-v 작업을 마우스 오른쪽 단추로 클릭 하 고 작업 스크립트를 선택 합니다. ** 만들기 | 파일**을 열고 각 스크립트를 폴더에 저장 하 고 각 스크립트에 설명적인 이름을 지정 합니다.

    -   **Appvdbname (Softgrid 데이터베이스) 사용 내역 확인**

    -   **Appvdbname (Softgrid 데이터베이스) 고아 세션 닫기**

    -   **Appvdbname (Softgrid 데이터베이스) 크기 제한 적용**

    -   **Appvdbname (Softgrid 데이터베이스)의 알림/작업 상태 모니터링**

3.  4 개의 스크립트 파일 (.sql)을 SQL Server를 실행 하는 대상 컴퓨터에 복사 하 고 SQL Server Management Studio를 엽니다.

4.  Windows 탐색기에서 각 .sql 파일을 마우스 오른쪽 단추로 클릭 한 다음 **실행**을 클릭 합니다. 각 스크립트는 SQL Server Management Studio의 쿼리 창에서 열립니다. 각 스크립트에 대해 **실행** 을 클릭 하 고 각 스크립트가 성공적으로 완료 되었는지 확인 합니다.

5.  **SQL Server 에이전트** 노드에서 **작업** 노드를 새로 고치고 4 개의 작업이 성공적으로 생성 되었는지 확인 합니다.

**App-v 관리 서버의 구성을 업데이트 하려면**

1.  App-v 관리 서버에서 다음 레지스트리 키를 수정 합니다.

    -   **Sqlservername**  =  &lt; newservername&gt;

    -   **SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;

    그런 다음 App-v 서버 서비스를 다시 시작 합니다.

2.  App-V 관리 서버 설치 디렉터리 아래에 있는 파일을 찾아서 찾습니다 (기본값은 C:\\program files Files\\Microsoft System Center App Virt Management Server\\App Virt 관리 서비스). 파일을 마우스 오른쪽 단추로 클릭 하 고 **열기**를 선택 합니다.

3.  **연결** 탭에서 SQL Server를 실행 하는 대상 컴퓨터의 이름을 입력 한 다음 **연결 테스트**를 클릭 합니다. 테스트에 성공 하면 **확인** 을 클릭 한 다음 **확인** 을 다시 클릭 합니다.

4.  4.5 SP2 이전의 App-v 관리 서버 버전의 경우 SQL 로깅 설정을 업데이트 해야 합니다. **서버 그룹**에서 서버가 구성원으로 속해 있는 서버 그룹을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택 합니다.

5.  **로깅** 탭에서 **SQL 데이터베이스** 항목을 클릭 하 여 선택한 다음 **편집**을 클릭 합니다.

6.  **DNS 호스트 이름을** SQL Server를 실행 하는 새 컴퓨터의 호스트 이름으로 변경한 다음 **확인**을 클릭 합니다. **확인** 을 두 번 클릭 한 다음 app-v 서버 서비스를 다시 시작 합니다.

7.  App-v 관리 콘솔을 열고 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 한 다음 **새로 고침**을 선택 합니다. 응용 프로그램 목록은 이전과 같이 표시 되어야 합니다.

 

 





