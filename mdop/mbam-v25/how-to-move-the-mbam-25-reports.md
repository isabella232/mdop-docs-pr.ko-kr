---
title: MBAM 2.5 보고서를 이동하는 방법
description: MBAM 2.5 보고서를 이동하는 방법
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812393"
---
# MBAM 2.5 보고서를 이동하는 방법


이 절차를 사용 하 여 보고서 기능을 한 컴퓨터에서 다른 컴퓨터로 이동 (즉, 보고서 기능을 서버 A에서 서버 B로 이동) 할 수 있습니다.

보고서 기능을 이동 하는 상위 수준 단계는 다음과 같습니다.

1.  MBAM 관리 및 모니터링 웹 사이트의 모든 인스턴스를 중지 합니다.

2.  서버 B에 MBAM 2.5 서버 소프트웨어를 설치 하 고 서버 B에서 보고서 기능을 구성 합니다.

3.  MBAM 관리 및 모니터링 서버에서 보고서 연결 데이터를 업데이트 합니다.

4.  MBAM 관리 및 모니터링 웹 사이트의 인스턴스를 다시 시작 합니다.

**참고**  이 항목의 예제 Windows PowerShell 스크립트를 실행 하려면 스크립트를 실행할 수 있도록 Windows PowerShell 실행 정책을 업데이트 해야 합니다. 자세한 내용은 [Windows PowerShell 스크립트 실행](https://technet.microsoft.com/library/ee176949.aspx) 을 참조 하세요.

 

**MBAM 관리 및 모니터링 웹 사이트를 중지 합니다.**

-   관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 중지 합니다.

    이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 입력할 수 있습니다.

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**MBAM 서버 소프트웨어를 설치 하 고 서버 B에서 MBAM 서버 구성 마법사 실행**

1.  서버 B에 MBAM 서버 소프트웨어를 설치 합니다. 지침은 [MBAM 2.5 서버 소프트웨어 설치](installing-the-mbam-25-server-software.md)를 참조 하세요.

2.  서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **보고서** 기능만 선택 합니다.

    또는 **Enable-MbamReport** Windows PowerShell cmdlet을 사용 하 여 보고서를 구성할 수 있습니다.

    보고서를 구성 하는 방법에 대 한 지침은 [MBAM 2.5 보고서를 구성](how-to-configure-the-mbam-25-reports.md)하는 방법을 참조 하세요.

**관리 및 모니터링 서버에서 보고서 연결 데이터 업데이트**

1.  보고서 기능을 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 보고서 URL을 업데이트 합니다.

2.  **Microsoft BitLocker 관리 및 모니터링**을 확장 한 다음 **헬프데스크** 노드를 선택 합니다.

3.  **기능 보기**의 **관리** 섹션에서 **구성 편집기**를 선택 합니다.

4.  **섹션** 필드에서 **appSettings**를 선택 합니다.

5.  **컬렉션** 행을 선택한 다음 창의 맨 오른쪽에 있는 "줄임표" 단추 **(...)** 를 클릭 하 여 **컬렉션 편집기**를 엽니다.

6.  **컬렉션 편집기**에서 **microsoft. r**e m. e a l. e a m .에 대 한 값을 업데이트 하 고 서버 B에 대 한 서버 이름을 반영 하는 url을 선택 합니다 **.**

    이전에 SQL Server Reporting Services의 명명 된 인스턴스에서 보고서 기능을 구성한 경우에는 다음과 같이 인스턴스의 이름을 URL에 추가 하거나 업데이트 합니다.

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 관리 및 모니터링 서버에서 다음 코드 예제와 유사한 명령을 실행할 수 있습니다.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    다음 표의 설명을 사용 하 여 코드 예제의 값을 환경과 일치 하는 값으로 바꿉니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">매개 변수</th>
    <th align="left">설명</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$SERVERNAME $</p></td>
    <td align="left"><p>보고서를 이동한 서버의 이름입니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>보고서가 이동 된 SQL Server Reporting Services 인스턴스의 이름입니다.</p></td>
    </tr>
    </tbody>
    </table>

     

**관리 및 모니터링 웹 사이트 인스턴스 다시 시작**

1.  관리 및 모니터링 웹 사이트를 실행 하는 서버에서 IIS (인터넷 정보 서비스) 관리자 콘솔을 사용 하 여 관리 및 모니터링 웹 사이트를 시작 합니다.

2.  이 절차를 자동화 하려면 Windows PowerShell을 사용 하 여 다음과 비슷한 명령을 실행할 수 있습니다.

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **참고**  이 명령을 실행 하려면 windows powershell 용 IIS 모듈을 현재 Windows PowerShell 인스턴스에 추가 해야 합니다.

     



## 관련 항목


[MBAM 2.5 보고서를 구성하는 방법](how-to-configure-the-mbam-25-reports.md)

[Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[다른 서버로 MBAM 2.5 기능 이동](moving-mbam-25-features-to-another-server.md)

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.
 





