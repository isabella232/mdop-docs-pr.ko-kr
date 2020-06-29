---
title: 분산 서버에서 MBAM을 설치 및 구성하는 방법
description: 분산 서버에서 MBAM을 설치 및 구성하는 방법
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824058"
---
# 분산 서버에서 MBAM을 설치 및 구성하는 방법


이 항목의 절차에서는 분산 서버의 독립 실행형 토폴로지에 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0을 설치 하는 방법에 대해 설명 합니다. 권장 아키텍처의 다이어그램을 보려면 데이터베이스 및 기능에 대 한 설명과 함께 [MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)를 참조 하세요. Configuration Manager 토폴로지를 사용 하 여 Microsoft BitLocker 관리 및 모니터링을 설치 하려면 [Configuration manager를 사용 하 여 MBAM 배포](deploying-mbam-with-configuration-manager-mbam2.md)를 참조 하세요.

각 서버 기능에는 특정 필수 구성 요소가 있습니다. 필수 구성 요소 및 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 확인 하려면 [mbam 2.0 배포 필수 구성 요소](mbam-20-deployment-prerequisites-mbam-2.md) 및 [Mbam 2.0 지원 되는 구성을](mbam-20-supported-configurations-mbam-2.md)참조 하세요. 또한 일부 기능을 설치 하는 동안 특정 정보를 제공 해야 기능을 성공적으로 배포할 수 있습니다. MBAM 배포를 시작 하기 전에 [mbam 2.0 서버 배포에 대 한 계획](planning-for-mbam-20-server-deployment-mbam-2.md) 도 검토 해야 합니다.

**참고**  
설치 로그 파일을 얻으려면 Msiexec 패키지와 **/l** 위치 옵션을 사용 하 여 &lt; &gt; mbam을 설치 해야 합니다. 로그 파일은 사용자가 지정한 위치에 만들어집니다.

추가 설치 로그 파일은 MBAM을 설치 하는 사용자 서버의% temp% 폴더에 만들어집니다.



## <a href="" id="deploying-mbam-server-features-"></a>MBAM 서버 기능 배포


다음 단계에서는 일반 MBAM 기능을 설치 하는 방법을 설명 합니다.

**MBAM 서버 설치 마법사 시작**

1.  Microsoft BitLocker 관리 및 모니터링을 설치 하려는 서버에서 **MBAMSetup.exe** 를 실행 하 여 mbam 설치 마법사를 시작 합니다.

2.  **시작** 페이지에서 **사용자 환경 개선 프로그램**을 선택적으로 선택한 다음 **시작**을 클릭 합니다.

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

4.  **토폴로지 선택** 페이지에서 **독립 실행형** 토폴로지를 선택 하 고 **다음**을 클릭 합니다.

    **참고**  
    Configuration Manager 통합 토폴로지에 MBAM을 설치 하려면 [Configuration manager를 사용 하 여 Mbam 배포](deploying-mbam-with-configuration-manager-mbam2.md)를 참조 하세요.



5.  설치 하려는 기능을 선택 합니다. 기본적으로 모든 MBAM 기능이 설치 되도록 선택 되어 있습니다. 다른 곳에 설치 하려는 기능을 선택 취소 합니다. 같은 컴퓨터에 설치 되는 기능은 동시에 함께 설치 해야 합니다. 다음과 같은 순서로 MBAM 기능을 설치 해야 합니다.

    -   복구 데이터베이스

    -   준수 및 감사 데이터베이스

    -   규정 준수 및 감사 보고서

    -   셀프 서비스 포털

    -   관리 및 모니터링 서버

    -   MBAM 그룹 정책 서식 파일

    **참고**  
    설치 마법사가 설치의 필수 구성 요소를 확인 하 고 누락 된 필수 구성 요소를 표시 합니다. 모든 필수 조건이 충족 되는 경우 설치가 계속 됩니다. 누락 된 필수 구성 요소를 발견 하면 누락 된 필수 구성 요소를 해결 한 다음 **필수 구성 요소 다시 확인**을 클릭 해야 합니다. 이 시간에 모든 선행 조건이 충족 되는 경우 설치가 다시 시작 됩니다.



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**복구 데이터베이스를 설치 하려면**

1.  **복구 데이터베이스 구성** 페이지에서 관리 및 모니터링 서버 기능을 실행 하는 컴퓨터의 이름을 지정 합니다. 관리 및 모니터링 서버 기능을 배포한 후에는 해당 도메인 계정을 사용 하 여 데이터베이스에 연결 합니다.

2.  **Next**(다음)를 클릭하여 계속합니다.

3.  SQL Server 인스턴스 이름과 복구 데이터를 저장할 데이터베이스의 이름을 지정 합니다. 또한 데이터베이스를 찾을 위치와 로그 정보 위치를 지정 해야 합니다.

4.  MBAM 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.

**준수 및 감사 데이터베이스를 설치 하려면**

1.  **준수 및 감사 데이터베이스 구성** 페이지에서 보고서 데이터베이스에 액세스 하는 데 사용 될 사용자 계정을 지정 합니다.

2.  관리 및 모니터링 서버를 실행 하는 컴퓨터의 컴퓨터 이름과 준수 및 감사 보고서를 지정 합니다. 관리 및 모니터링과 규정 준수 및 감사 보고서 서버는 배포 된 후 도메인 계정을 사용 하 여 데이터베이스에 연결 합니다.

    **참고**  
    준수 및 감사 보고서 기능 없이 준수 및 감사 데이터베이스를 설치 하는 경우 준수 및 감사 데이터베이스 컴퓨터에 예외를 추가 하 여 Microsoft SQL Server 포트에서 인바운드 트래픽을 사용 하도록 설정 해야 합니다. 기본 포트 번호는 1433입니다.



3.  SQL Server 인스턴스 이름과 규정 준수 및 감사 데이터를 저장할 데이터베이스 이름을 지정 합니다. 또한 데이터베이스 및 로그 정보의 위치를 지정 해야 합니다.

4.  Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.

**준수 및 감사 보고서를 설치 하려면**

1.  **준수 및 감사 보고서 구성** 페이지에서 &lt; &gt; 규정 준수 및 감사 데이터베이스가 설치 된 원격 SQL Server 인스턴스 이름 (예: ServerName)을 지정 합니다.

    **참고**  
    관리 및 모니터링 서버 없이 규정 준수 및 감사 보고서를 설치 하는 경우 준수 및 감사 보고서 컴퓨터에 예외를 추가 하 여 보고 서버 포트에서 인바운드 트래픽을 사용할 수 있도록 설정 해야 합니다 (기본 포트는 80).



2.  준수 및 감사 데이터베이스의 이름을 지정 합니다. 데이터베이스 이름은 기본적으로 MBAM 준수 상태 이지만, 준수 및 감사 데이터베이스를 설치할 때 이름을 변경할 수 있습니다.

3.  **Next**(다음)를 클릭하여 계속합니다.

4.  준수 및 감사 보고서가 설치 될 SQL Server Reporting Services 인스턴스를 선택 합니다. 준수 및 감사 데이터베이스에 액세스 하려면 도메인 사용자 계정 및 암호를 제공 합니다. 이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다. 사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.

5.  Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.

**셀프 서비스 포털을 설치 하려면**

1.  **셀프 서비스 포털 구성** 페이지에서 셀프 서비스 포털 및 관리 및 모니터링 서버 간의 통신을 선택적으로 암호화할 수 있습니다. 통신을 암호화 하는 옵션을 선택 하면 암호화에 사용할 인증 기관 프로 비전 된 인증서를 선택 하 라는 메시지가 표시 됩니다.

2.  **Next**(다음)를 클릭하여 계속합니다.

3.  준수 및 감사 데이터베이스가 설치 된 SQL Server (예: * &lt; ServerName &gt; *)의 원격 인스턴스를 지정 합니다.

4.  준수 및 감사 데이터베이스의 이름을 지정 합니다. 기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다. 그러나 준수 및 감사 데이터베이스를 설치할 때 이름을 변경할 수 있습니다.

5.  **Next**(다음)를 클릭하여 계속합니다.

6.  복구 데이터베이스가 설치 된 SQL Server (예: * &lt; ServerName &gt; *)의 원격 인스턴스를 지정 합니다.

7.  복구 데이터베이스의 이름을 지정 합니다. 기본적으로 데이터베이스 이름은 **Mbam 복구 및 하드웨어**입니다. 그러나 복구 데이터베이스 기능을 설치할 때 이름을 변경할 수 있습니다.

8.  **Next**(다음)를 클릭하여 계속합니다.

9.  **포트 번호**, **호스트 이름** (선택 사항), Mbam 관리 및 모니터링 서버의 **설치 경로** 를 입력 합니다.

    **참고**  
    고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다. Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.



10. 셀프 서비스 포털의 SPN (서비스 사용자 이름)을 선택적으로 등록 하려면 **Active Directory를 사용 하 여이 컴퓨터의 spn (서비스 사용자 이름) 등록 (Windows 인증에 필요)** 을 선택 합니다. 이 확인란을 선택 하면 MBAM 설정이 기존 Spn을 등록 하려고 시도 하지 않으며, MBAM 설치 전이나 후에 SPN을 수동으로 등록할 수 있습니다. 수동으로 SPN을 등록 하는 방법에 대 한 지침은 [수동 SPN 등록](https://go.microsoft.com/fwlink/?LinkId=286758)을 참조 하세요.

11. Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.

12. Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.

13. 선택한 MBAM 기능 정보가 완료 되 면 설치 마법사를 사용 하 여 MBAM 설치를 시작할 준비가 된 것입니다. 설치 설정을 검토 하거나 변경 해야 하는 경우 마법사를 이동 하려면 **뒤로** 를 클릭 합니다. 설치 **를 클릭 하** 여 설치를 시작 합니다. 마법사를 종료 하려면 **취소** 를 클릭 합니다. 설치 프로그램이 사용자가 선택한 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.

14. **마침을** 클릭 하 여 마법사를 종료 합니다.

    **참고**  
    셀프 서비스 포털을 설치한 후 구성 하려면 회사 이름과 기타 회사 관련 정보를 사용 하 여 셀프 서비스 포털을 브랜딩 하는 방법에 대 한 자세한 내용은 [셀프 서비스 포털을 브랜딩](how-to-brand-the-self-service-portal.md) 하는 방법에 대 한 지침을 참조 하세요.



15. 클라이언트 컴퓨터가 특정 JavaScript 파일에 대 한 필수 액세스를 셀프 서비스 포털에 제공 하는 Microsoft Content Delivery Network (CDN)에 액세스할 수 있는 경우 셀프 서비스 포털 설치를 완료 합니다. 클라이언트 컴퓨터에 Microsoft CDN에 대 한 액세스 권한이 없는 경우 다음 섹션의 단계를 완료 하 여 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 합니다.

**최종 사용자가 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하려면**

1. 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크 (CDN)에 액세스할 수 있는 경우 셀프 서비스 포털에 특정 JavaScript 파일에 대 한 필수 액세스를 제공 하는 경우 셀프 서비스 포털 설치가 완료 됩니다. 클라이언트 컴퓨터에 Microsoft CDN에 대 한 액세스 권한이 없는 경우이 섹션의 나머지 단계를 완료 하 여 접근성 있는 원본에서 JavaScript 파일을 참조 하도록 셀프 서비스 포털을 구성 합니다.

2. Microsoft CDN에서 4 개의 JavaScript 파일을 다운로드 합니다.

   -   jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)

   -   MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)

   -   MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)

   -   MicrosoftMvcValidation.js- <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. JavaScript 파일을 셀프 서비스 포털의 **Scripts** 디렉터리에 복사 합니다. 이 디렉터리는 <em> &lt; mbam 셀프 서비스 설치 디렉터리 &gt; \\ </em> 셀프 서비스 Website\\Scripts.에 있습니다.

4. **IIS (인터넷 정보 서비스) 관리자**를 엽니다.

5. **사이트** &gt; **Microsoft BitLocker 관리 및 모니터링**을 확장 하 고 **SelfService**를 강조 표시 합니다.

   **참고**  
   *SelfService* 는 기본 가상 디렉터리 이름입니다. 설치 중에이 디렉터리에 다른 이름을 선택한 경우에는이 지침의 나머지 부분에 있는 *SelfService* 을 선택한 이름으로 바꿉니다.



6. 가운데 창에서 **응용 프로그램 설정을**두 번 클릭 합니다.

7. 다음 목록에 있는 각 항목에 대해 &lt; 가상 디렉터리를 &gt; /SelfService/(또는 설치 중 선택한 이름)로 대체 하 여 새 위치를 참조 하는 응용 프로그램 설정을 편집 합니다. 예를 들어 가상 디렉터리 경로는/selfservice/scripts/jquery-1.7.2.min.js와 유사 합니다.

   -   jQueryPath:/ &lt; virtual directory &gt; /Scripts/jQuery-1.7.2.min.js

   -   MicrosoftAjaxPath:/ &lt; virtual directory &gt; /Scripts/MicrosoftAjax.js

   -   MicrosoftMvcAjaxPath:/ &lt; virtual directory &gt; /Scripts/MicrosoftMvcAjax.js

   -   MicrosoftMvcValidationPath:/ &lt; virtual directory &gt; /Scripts/MicrosoftMvcValidation.js

**관리 및 모니터링 서버 기능을 설치 하려면**

1. MBAM은 웹 서비스와 관리 및 모니터링 서버 간의 통신을 암호화할 수 있습니다. 통신을 암호화 하는 옵션을 선택 하면 암호화에 사용할 인증 기관 프로 비전 된 인증서를 선택 하 라는 메시지가 표시 됩니다.

2. **Next**(다음)를 클릭하여 계속합니다.

3. 준수 및 감사 데이터베이스가 설치 된 SQL Server (예: * &lt; ServerName &gt; *)의 원격 인스턴스를 지정 합니다.

4. 준수 및 감사 데이터베이스의 이름을 지정 합니다. 기본적으로 데이터베이스 이름은 MBAM 준수 상태입니다. 그러나 준수 및 감사 데이터베이스를 설치할 때 이름을 변경할 수 있습니다.

5. **Next**(다음)를 클릭하여 계속합니다.

6. 복구 데이터베이스가 설치 된 SQL Server의 원격 인스턴스 (예: * &lt; ServerName &gt; *)를 지정 합니다.

7. 복구 데이터베이스의 이름을 지정 합니다. 기본적으로 데이터베이스 이름은 **Mbam 복구 및 하드웨어**입니다. 그러나 복구 데이터베이스 기능을 설치할 때 이름을 변경할 수 있습니다.

8. **Next**(다음)를 클릭하여 계속합니다.

9. SQL Server Reporting Services (SRS) 사이트의 "홈"에 대 한 URL을 지정 합니다. SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 다음과 같습니다.

   http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer

   **참고**  
   SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 http://* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; srsinstancename &gt; *과 유사 합니다.



10. **Next**(다음)를 클릭하여 계속합니다.

11. **포트 번호**, **호스트 이름** (선택 사항), Mbam 관리 및 모니터링 서버의 **설치 경로** 를 입력 합니다.

    **참고**  
    고유한 호스트 헤더 이름을 지정 하지 않는 한, 지정 하는 포트 번호는 관리 및 모니터링 서버에서 사용 되지 않는 포트 번호 여야 합니다. Windows 방화벽을 사용 하는 경우 포트가 자동으로 열립니다.



12. 셀프 서비스 포털의 SPN (서비스 사용자 이름)을 선택적으로 등록 하려면 **Active Directory를 사용 하 여이 컴퓨터의 spn (서비스 사용자 이름) 등록 (Windows 인증에 필요)** 을 선택 합니다. 이 확인란을 선택 하면 MBAM 설정이 기존 Spn을 등록 하려고 시도 하지 않으며, MBAM 설치 전이나 후에 SPN을 수동으로 등록할 수 있습니다. 수동으로 SPN을 등록 하는 방법에 대 한 지침은 [수동 SPN 등록](https://go.microsoft.com/fwlink/?LinkId=286758)을 참조 하세요.

13. Microsoft BitLocker 관리 및 모니터링 설정 마법사를 계속 하려면 **다음** 을 클릭 합니다.

14. Microsoft 업데이트를 사용 하 여 컴퓨터 보안을 유지할 것인지 여부를 지정 하 고 **다음**을 클릭 합니다.

15. 선택한 MBAM 기능 정보가 완료 되 면 설치 마법사를 사용 하 여 MBAM 설치를 시작할 준비가 된 것입니다. 설치 설정을 검토 하거나 변경 해야 하는 경우 마법사를 이동 하려면 **뒤로** 를 클릭 합니다. 설치 하려면 **설치** 를 클릭 합니다. 마법사를 종료 하려면 **취소** 를 클릭 합니다. 설치 프로그램이 사용자가 선택한 MBAM 기능을 설치 하 고 설치가 완료 되었다는 알림을 표시 합니다.

16. **마침을** 클릭 하 여 마법사를 종료 합니다.

**설치 후 구성을 수행 하려면**

1.  관리 및 모니터링 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 및 모니터링 웹 사이트의 기능에 대 한 액세스 권한을 부여 합니다.

    -   **Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 액세스할 수 있습니다. 드라이브 복구 및 TPM 관리의 모든 필드는 헬프데스크 사용자를 위한 필수 필드입니다.

    -   **Mbam 헬프데스크 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트에서 드라이브 복구 및 TPM 관리 기능에 대 한 고급 액세스 권한을 갖습니다. 고급 헬프데스크 사용자의 경우 드라이브 복구에 키 ID 필드만 필요 합니다. **TPM 관리**에서 **컴퓨터 도메인** 필드 및 **컴퓨터 이름** 필드만 필요 합니다.

2.  관리 및 모니터링 서버와 준수 및 감사 데이터베이스를 호스트 하는 서버와 규정 준수 및 감사 보고서를 호스팅하는 서버에서 다음 로컬 그룹에 사용자를 추가 하 여 MBAM 관리 및 모니터링 웹 사이트의 보고서 기능에 대 한 액세스 권한을 부여 합니다.

    -   **Mbam 보고서 사용자**:이 로컬 그룹의 구성원은 Mbam 관리 및 모니터링 웹 사이트의 보고서에 액세스할 수 있습니다.

    **참고**  
    **Mbam 보고서** 의 동일한 사용자 또는 그룹 구성원 자격을 가진 모든 컴퓨터에서 Mbam 관리 및 모니터링 서버 기능, 준수 및 감사 데이터베이스, 규정 준수 및 감사 보고서가 설치 되어 있어야 합니다.



## MBAM 서버 기능 설치 유효성 검사


Microsoft BitLocker 관리 및 모니터링 서버 기능 설치가 완료 되 면 해당 설치가 MBAM에 대해 필요한 모든 기능을 성공적으로 설정 했는지 확인 하는 것이 좋습니다. 다음 절차를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 서비스가 작동 하는지 확인 합니다.

**MBAM 서버 설치의 유효성을 검사 하려면**

1. MBAM 기능이 배포 되는 각 서버에서 **제어판**을 열고 **프로그램**을 선택한 다음 **프로그램 및 기능**을 선택 합니다. **Microsoft BitLocker 관리 및 모니터링** 이 **프로그램 및 기능** 목록에 표시 되는지 확인 합니다.

   **참고**  
   MBAM 설치의 유효성을 검사 하려면 각 서버에서 로컬 컴퓨터 관리 자격 증명이 있는 도메인 계정을 사용 해야 합니다.



2. 복구 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 복구 및 하드웨어** 데이터베이스가 설치 되어 있는지 확인 합니다.

3. 준수 및 감사 데이터베이스가 설치 된 서버에서 SQL Server Management Studio를 열고 **Mbam 준수 상태 데이터베이스가** 설치 되어 있는지 확인 합니다.

4. 준수 및 감사 보고서가 설치 된 서버에서 관리 자격 증명으로 웹 브라우저를 열고 SQL Server Reporting Services 사이트의 "홈"을 찾습니다.

   SQL Server Reporting Services 사이트 인스턴스의 기본 홈 위치는 http://NameofMBAMReportsServer에서 찾을 수 있습니다 <em> &lt; &gt; </em> /Reports.aspx. 실제 URL을 찾으려면 Reporting Services 구성 관리자 도구를 사용 하 여 설치 중에 지정 된 인스턴스를 선택 합니다.

   **Microsoft BitLocker 관리 및 모니터링** 이라는 보고서 폴더에 **MaltaDataSource** 이라는 데이터 원본이 포함 되어 있고 **en-us** 폴더에 4 개의 보고서가 포함 되어 있는지 확인 합니다.

   **참고**  
   SQL Server Reporting Services가 명명 된 인스턴스로 구성 된 경우 URL은 다음과 유사 합니다. http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; srsinstancename &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. 관리 및 모니터링 기능이 설치 된 서버에서 **서버 관리자** 를 실행 하 고 **역할**을 찾습니다. **웹 서버 (iis)** 를 선택한 다음 **Iis (인터넷 정보 서비스) 관리자**를 클릭 합니다.

6. **연결**에서 * &lt; computername &gt; *으로 이동 하 여 **사이트**를 선택 하 고 **Microsoft BitLocker 관리 및 모니터링**을 선택 합니다. **MBAMAdministrationService**, **MBAMComplianceStatusService**및 **MBAMRecoveryAndHardwareService** 이 나열 되는지 확인 합니다.

7. 관리 및 모니터링 기능 및 셀프 서비스 포털이 설치 되어 있는 서버에서 관리 자격 증명을 사용 하는 웹 브라우저를 열고 다음 위치로 이동 하 여 성공적으로 로드 되었는지 확인 합니다.

   **참고**  
   ".Svc"로 끝나는 Url은 웹 사이트를 표시 하지 않습니다. 성공 여부는 "이 서비스에 대 한 메타 데이터 게시가 현재 사용 하지 않도록 설정 되었습니다." 메시지나 코드와 유사한 정보로 표시 됩니다. 다른 오류 메시지가 표시 되거나 페이지를 찾을 수 없는 경우 페이지가 제대로 로드 되지 않은 것입니다.



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. 각 웹 페이지가 성공적으로 로드 되었는지 확인 합니다.

## 관련 항목


[MBAM 2.0 서버 인프라 배포](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









