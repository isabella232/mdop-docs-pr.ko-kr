---
title: App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법
description: App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817933"
---
# App-V용 Microsoft SQL Server 미러링 지원을 구성하는 방법


다음 절차를 사용 하 여 microsoft SQL Server 데이터베이스 미러링을 사용 하도록 Microsoft Application Virtualization (App-v) 환경을 구성할 수 있습니다. 데이터베이스 미러링을 구성 하면 재해 복구 및 장애 조치 시나리오에 도움이 될 수 있습니다. App-v 4.5 SP2는 현재 Microsoft SQL Server 2005 및 SQL Server 2008에서 사용할 수 있는 모든 데이터베이스 미러링 모드를 지원 합니다.

**참고**  
이 절차는 Microsoft SQL Server를 사용 하 여 SQL Server 데이터베이스 및 데이터베이스 미러링을 설정 하 고 구성 하는 데 익숙한 관리자를 위해 작성 되었으며, 따라서 App-v에 고유한 특정 구성 설정만 다룹니다.



**Microsoft SQL Server 데이터베이스 미러링을 사용 하도록 앱-V 환경을 구성 하려면**

1.  데이터베이스 미러링에 대 한 표준 비즈니스 지침에 따라 App-v 데이터베이스의 SQL Server 데이터베이스 미러링을 설정 합니다. Microsoft SQL Server 데이터베이스 미러링 구현에 대 한 일반적인 정보를 보려면 다음 링크를 사용 합니다.

    -   **MICROSOFT SQL 2005**—[데이터베이스 미러링 설정](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)

    -   **MICROSOFT SQL 2008**—[데이터베이스 미러링 설정](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)

    또한 최상의 방법 정보는 [데이터베이스 미러링 모범 사례 및 성능 고려 사항](https://go.microsoft.com/fwlink/?LinkId=190270) ()에서 확인할 수 있습니다 https://go.microsoft.com/fwlink/?LinkId=190270) .

2.  미러링이 설정 된 후에는 App-v 데이터베이스가 상태 **(주도자, 동기화 됨)** 를 표시 하 고 미러된 데이터베이스에 상태 **(미러, 동기화 됨/복원 중)** 가 표시 되는지 확인 합니다. 다음 단계를 진행 하기 전에 모든 미러링 문제를 해결 합니다. 상태 모니터링에 대 한 자세한 내용은 [미러링 상태 모니터링](https://go.microsoft.com/fwlink/?LinkId=190279) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=190279) .

3.  App-v 데이터베이스의 미러를 호스트 하는 sql server 컴퓨터에서 계정 이름 ** &lt; 도메인 &gt; \\ &lt; managementserverhostname &gt; $ **을 사용 하 여 app-v 관리 서버의 네트워크 서비스 계정에 대 한 SQL Server 로그인을 만듭니다.

4.  Microsoft SQL Server 네이티브 클라이언트를 App-v 관리 서버에 설치 하 고, 다른 컴퓨터에 설치 되어 있는 경우 App-v 관리 웹 서비스를 실행 하는 컴퓨터에 설치 합니다. 부하 분산을 위해 추가 App-v 관리 서버를 미러된 SQL 데이터베이스에 연결 하려는 경우 해당 컴퓨터에도 Microsoft SQL Server 기본 클라이언트를 설치 해야 합니다. Microsoft [sql server 2008 기능 팩](https://go.microsoft.com/fwlink/?LinkId=187479) 페이지의 Microsoft 다운로드 센터 ()에서 Microsoft Sql Server 기본 클라이언트를 다운로드할 수 있습니다 https://go.microsoft.com/fwlink/?LinkId=187479) .

5.  레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** 을 확인 하 고 SQL Server의 호스트 이름만 포함 하 고 있는지 확인 합니다. 인스턴스 이름 (예: *serverhostname\\instancename*을 포함 하는 경우 인스턴스 이름을 제거 해야 합니다.

    **중요**  
    데이터베이스 미러링이 사용 되는 경우 App-v 관리 서버는 TCP/IP 네트워킹 라이브러리를 사용 하 여 SQL Server와 통신 하므로 인스턴스 이름을 사용할 수 없습니다. 포트 번호는 대신 레지스트리 키에서 지정 해야 합니다.



6.  레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** 을 확인 하 고 sql Server 컴퓨터의 sql에 사용 되는 포트 번호가 포함 되어 있는지 확인 합니다. 명명 된 인스턴스를 사용 하는 경우이 키 값을 명명 된 인스턴스에 사용 되는 포트로 설정 해야 합니다.

7.  레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\MICROSOFT\\SOFTGRID\\4.5\\SERVER\\SQLFAILOVERSERVERNAME** REG \ _SZ으로 만든 다음 해당 값을 미러를 호스팅하는 SQL Server의 호스트 이름으로 설정 합니다.

8.  레지스트리 키 **HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\MICROSOFT\\SOFTGRID\\4.5\\SERVER\\SQLFAILOVERSERVERPORT** DWORD로 만든 다음 해당 값을 sql Server를 실행 하는 컴퓨터의 sql에서 미러를 호스팅하기 위해 사용 하는 포트 번호로 설정 합니다. 미러에 대해 명명 된 인스턴스를 사용 하는 경우이 키 값은 명명 된 인스턴스에 사용 되는 포트 번호로 설정 되어야 합니다.

9.  앱-V 관리 웹 서비스를 실행 하는 컴퓨터에서 UDL (유니버설 데이터 링크) 텍스트 파일을 구성 합니다. App-v가 설치 된 디렉터리에서 **Sftmgmt** 를 두 번 클릭 하 고 다음 값을 지정 합니다.

    -   **공급자** 탭에서 OLE DB 공급자 **SQL Server Native Client 10.0**를 선택 합니다.

    -   **다음** 을 클릭 하 여 **연결** 탭을 선택 합니다. **서버 이름** 상자에 SQL server의 서버 이름을 입력 합니다. 다음으로, **WINDOWS NT의 통합 보안 사용**을 선택 합니다. 마지막으로 목록을 클릭 하 여 **데이터베이스를 선택한**다음 app-v 데이터베이스 이름을 선택 합니다.

    -   **모두** 탭을 클릭 한 다음 항목 **장애 조치 파트너**를 선택 합니다. **값 편집**을 클릭 한 다음 장애 조치 SQL server의 서버 이름을 입력 합니다. **확인**을 클릭합니다.

    **중요**  
    App-v 시스템은 Kerberos 인증을 사용 합니다. 따라서 sql Server에서 Kerberos 인증을 사용 하도록 설정 하 고 도메인 사용자 계정에서 SQL Server 서비스를 실행 하는 SQL 미러링을 구성할 때는 수동으로 SPN을 구성 해야 합니다. 자세한 내용은 [분산 환경에 대 한 App-v 관리 구성](https://go.microsoft.com/fwlink/?LinkId=203186) () 문서의 "SQL 서비스에서 도메인 기반 계정을 사용 하는 경우"를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=203186) .



10. 데이터베이스 미러링이 제대로 실행 되 고 있는지 확인 하려면 장애 조치를 테스트 하 고 App-v 관리 서버가 계속 올바르게 작동 하는지 확인 합니다.

    **중요**  
    주의를 기울여, 표준 비즈니스 관행에 따라 오류가 발생 했을 때 시스템 작업이 중단 되지 않는지 확인 합니다.



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## 관련 항목


[Application Virtualization Server Management Console에서 관리 작업을 수행하는 방법](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









