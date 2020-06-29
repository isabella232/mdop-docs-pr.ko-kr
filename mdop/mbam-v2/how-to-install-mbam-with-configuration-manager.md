---
title: Configuration Manager를 사용하여 MBAM을 설치하는 방법
description: Configuration Manager를 사용하여 MBAM을 설치하는 방법
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825128"
---
# Configuration Manager를 사용하여 MBAM을 설치하는 방법


이 섹션에서는 구성 관리자 [와 함께 MBAM을 사용 하](getting-started---using-mbam-with-configuration-manager.md)여 표시 되는 권장 구성을 사용 하 여 구성 관리자에 mbam을 설치 하는 단계에 대해 설명 합니다. 단계는 다음 작업으로 나뉘어 있습니다.

-   Configuration Manager 서버에 MBAM 설치 및 구성

-   데이터베이스 서버에 복구 및 감사 데이터베이스 설치

-   관리 및 모니터링 서버에 관리 및 모니터링 서버 기능 설치

설치를 시작 하기 전에 필요한 mof 파일을 편집 하거나 만들었는지 확인 합니다. 자세한 내용은 [Mof 파일을 만들거나 편집 하는 방법을](how-to-create-or-edit-the-mof-files.md)참조 하세요.

**중요**  기본이 아닌 SQL Server Reporting Services (SSRS) 인스턴스를 사용 하는 경우 다음 명령줄을 사용 하 여 MBAM 설정을 시작 해야 SSRS 명명 인스턴스를 지정할 수 있습니다.

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**Configuration Manager 서버에 MBAM 설치**

1.  Configuration Manager 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.

    **참고**  설치 로그 파일을 얻으려면 Msiexec 패키지와 **/l** 위치 옵션을 사용 하 여 &lt; &gt; Configuration Manager를 설치 해야 합니다. 로그 파일은 사용자가 지정한 위치에 만들어집니다.

    추가 설치 로그 파일은 Configuration Manager를 설치 하는 사용자의 컴퓨터에 있는% temp% 폴더에 만들어집니다.

     

2.  **시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

4.  **토폴로지 선택** 페이지에서 **System Center Configuration Manager 통합**을 선택 하 고 **다음**을 클릭 합니다.

5.  **설치할 기능 선택** 페이지에서 **System Center Configuration Manager 통합**을 선택 합니다.

    **참고**  **필수 구성 요소 확인** 페이지에서 설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 것이 없는지 여부를 클릭 하 여 **다음** 을 클릭 합니다. 누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인** 을 클릭 해야 합니다.

     

6.  Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다. Microsoft 업데이트를 사용 해도 Windows의 자동 업데이트는 설정 되지 않습니다.

7.  **Next**(다음)를 클릭하여 계속합니다.

8.  **설치 요약** 페이지에서 설치할 기능 목록을 검토 하 고 **설치** 를 클릭 하 여 mbam 기능 설치를 시작 합니다. 설치 설정을 검토 하거나 변경 해야 하는 경우 **뒤로** 를 클릭 하 여 마법사를 뒤로 이동 하거나 **취소** 를 클릭 하 여 설치를 종료 합니다. 설치 프로그램이 MBAM 기능을 설치 하 고 설치가 완료 되었음을 알려줍니다.

9.  **마침을** 클릭 하 여 마법사를 종료 합니다.

**데이터베이스 서버에 복구 및 감사 데이터베이스를 설치 하려면**

1.  데이터베이스 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.

2.  **시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

4.  **토폴로지 선택** 페이지에서 **System Center Configuration Manager 통합** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.

5.  설치할 기능 목록에서 **복구 데이터베이스** 와 **감사 데이터베이스**를 선택 하 고 나머지 기능을 지웁니다.

    **참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다. 모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다. 누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다. 이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.

     

6.  **복구 데이터베이스 구성** 페이지에서 관리 및 모니터링 서버 기능을 실행 하는 컴퓨터의 이름을 지정 합니다. 관리 및 모니터링 서버 기능을 배포한 후에는 해당 도메인 계정을 사용 하 여 데이터베이스에 연결 합니다.

7.  **Next**(다음)를 클릭하여 계속합니다.

8.  SQL Server 인스턴스 이름과 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다. 또한 데이터베이스를 찾을 위치와 로그 정보 위치를 지정 해야 합니다.

9.  MBAM 설정 설치 마법사를 계속 하려면 **다음** 을 클릭 합니다.

10. **감사 데이터베이스 구성** 페이지에서 보고서 데이터베이스에 액세스 하는 데 사용 될 사용자 계정을 지정 합니다.

11. 관리 및 모니터링 서버와 감사 보고서를 실행 하는 컴퓨터의 컴퓨터 이름을 지정 합니다. 관리 및 모니터링 및 감사 보고서 기능을 배포한 후에는 해당 도메인 계정이 데이터베이스에 연결 하는 데 사용 됩니다.

    **참고**  감사 보고서 기능 없이 감사 데이터베이스를 설치 하는 경우 감사 데이터베이스 컴퓨터에 예외를 추가 하 여 Microsoft SQL Server 포트에서 인바운드 트래픽을 사용 하도록 설정 해야 합니다. 기본 포트 번호는 1433입니다.

     

12. SQL Server 인스턴스 이름과 감사 데이터를 저장 하는 데이터베이스의 이름을 지정 합니다. 또한 데이터베이스 및 로그 정보의 위치를 지정 해야 합니다.

13. 설치 **를 클릭 하** 여 설치를 시작 하 고 **마침을** 클릭 하 여 설치를 완료 합니다.

**관리 및 모니터링 서버에 관리 및 모니터링 서버 기능을 설치 하려면**

1.  관리 및 모니터링 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.

2.  **시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

4.  **토폴로지 선택** 페이지에서 **System Center Configuration Manager 통합** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.

5.  설치할 기능 목록에서 **관리 및 모니터링 서버** 및 **셀프 서비스 포털**을 선택 하 고 나머지 기능을 지웁니다.

    **참고**  설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다. 모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다. 누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다. 이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.

     

6.  [분산 서버에 MBAM을 설치 하 고 구성 하는 방법](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md)에 대 한 **셀프 서비스 포털 설치** 섹션의 단계에 따라 셀프 서비스 포털을 설치 합니다.

    **참고**  클라이언트 컴퓨터에 CDN (Microsoft Content Delivery Network)에 대 한 액세스 권한이 없는 경우 특정 JavaScript 파일에 대 한 필수 액세스를 셀프 서비스 포털에 제공 하는 **경우, 최종 사용자가 Microsoft 콘텐츠 배달 네트워크 섹션에 액세스할 수 없는 경우 셀프 서비스 포털을 구성** 하려면 다음 단계를 완료 하세요. 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 하기 위해 [분산 된 서버에 Mbam을 설치 하 고 구성 하는 방법에 대해](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) 설명 합니다.

     

7.  [분산 서버에 MBAM을 설치 하 고 구성 하는 방법](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md)의 **관리 및 모니터링 서버 기능 설치** 방법 섹션에 나와 있는 단계를 따라 관리 및 모니터링 서버 기능을 설치 합니다.

8.  **마침을** 클릭 하 여 설치를 완료 합니다.

## 관련 항목


[Configuration Manager를 사용하여 MBAM 설치의 유효성을 검사하는 방법](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[Configuration Manager에서 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





