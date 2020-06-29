---
title: App-V 5.0 Server 배포 방법
description: App-V 5.0 Server 배포 방법
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814177"
---
# App-V 5.0 Server 배포 방법


다음 절차를 사용 하 여 App-v 5.0 서버를 설치 합니다. App-v 5.0 SP3 서버 배포에 대 한 자세한 내용은 [앱-v 5.0 sp3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3)정보를 참조 하세요.

**시작 하기 전에:**

-   필수 구성 요소 소프트웨어를 설치 했는지 확인 합니다. [앱-V 5.0 필수 구성 요소](app-v-50-prerequisites.md)를 참조 하세요.

-   [App-V 5.0 보안 고려](app-v-50-security-considerations.md)사항의 서버 섹션을 검토 합니다.

-   각 구성 요소를 호스트할 포트를 지정 합니다.

-   들어오는 요청에 대해 지정 된 포트에 액세스 하도록 허용 하는 방화벽 규칙을 추가 합니다.

-   Windows Installer 대신 SQL 스크립트를 사용 하 여 관리 데이터베이스 또는 보고 데이터베이스를 설정 하는 경우 관리 서버 또는 보고 서버를 설치 하기 전에 SQL 스크립트를 실행 해야 합니다. [SQL 스크립트를 사용 하 여 App-v 데이터베이스를 배포 하는 방법을](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)참조 하세요.

**App-v 5.0 서버를 설치 하려면**

1. 설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.

2. 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 고 실행 하 여 app-v 5.0 서버 설치를 시작 하 고 **설치**를 클릭 합니다.

3. 사용 조건을 검토 하 고 동의한 다음 Microsoft 업데이트를 사용할지 여부를 선택 합니다.

4. **기능 선택** 페이지에서 다음 구성 요소를 모두 선택 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">구성 요소</th>
   <th align="left">설명</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>관리 서버</p></td>
   <td align="left"><p>App-v 인프라에 대 한 전반적인 관리 기능을 제공 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>관리 데이터베이스</p></td>
   <td align="left"><p>앱-V 관리를 위한 데이터베이스 사전 배포를 용이 하 게 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>게시 서버</p></td>
   <td align="left"><p>가상 응용 프로그램에 대 한 호스팅 및 스트리밍 기능을 제공 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>보고 서버</p></td>
   <td align="left"><p>앱-V 5.0 reporting services를 제공 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>보고 데이터베이스</p></td>
   <td align="left"><p>앱-V reporting에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.</p></td>
   </tr>
   </tbody>
   </table>

     

5. **설치 위치** 페이지에서 선택한 구성 요소가 설치 될 기본 위치를 적용 하거나 **설치 위치** 줄에 새 경로를 입력 하 여 위치를 변경 합니다.

6. 초기 **새 관리 데이터베이스 만들기** 페이지에서 아래에서 적절 한 옵션을 선택 하 여 **Microsoft SQL Server 인스턴스** 및 **관리 서버 데이터베이스** 를 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">메서드</th>
   <th align="left">수행 해야 할 작업</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>사용자 지정 Microsoft SQL Server 인스턴스를 사용 하 고 있습니다.</p></td>
   <td align="left"><p><strong>사용자 지정 인스턴스 사용 </strong> 을 선택 하 고 인스턴스 이름을 입력 합니다.</p>
   <p>형식 인스턴스를 <strong> 사용 </strong> 합니다. 가정 된 설치 위치는 로컬 컴퓨터입니다.</p>
   <p>지원 되지 않음: ServerName의 strong format 인스턴스를 사용 하는 서버 이름 <strong> </strong> &lt; &gt; </strong> 입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>사용자 지정 데이터베이스 이름을 사용 하 고 있습니다.</p></td>
   <td align="left"><p><strong>사용자 지정 구성을 선택 </strong> 하 고 데이터베이스 이름을 입력 합니다.</p>
   <p>데이터베이스 이름은 고유 해야 하며 설치 되지 않습니다.</p></td>
   </tr>
   </tbody>
   </table>

     

7. **구성** 페이지에서 기본 값인 **이 로컬 컴퓨터 사용**을 그대로 적용 합니다.

   **참고**  
   관리 서버 및 관리 데이터베이스를 나란히 설치 하는 경우에는이 페이지의 일부 옵션을 사용할 수 없습니다. 이 경우 적절 한 옵션이 기본적으로 선택 되어 있으며 변경할 수 없습니다.

     

8. 초기 **새 보고 데이터베이스 만들기** 페이지에서 아래에서 적절 한 옵션을 선택 하 여 **Microsoft SQL Server 인스턴스** 및 **보고 서버 데이터베이스** 를 구성 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">메서드</th>
   <th align="left">수행 해야 할 작업</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>사용자 지정 Microsoft SQL Server 인스턴스를 사용 하 고 있습니다.</p></td>
   <td align="left"><p><strong>사용자 지정 인스턴스 사용 </strong> 을 선택 하 고 인스턴스 이름을 입력 합니다.</p>
   <p>형식 인스턴스를 <strong> 사용 </strong> 합니다. 가정 된 설치 위치는 로컬 컴퓨터입니다.</p>
   <p>지원 되지 않음: ServerName의 strong format 인스턴스를 사용 하는 서버 이름 <strong> </strong> &lt; &gt; </strong> 입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>사용자 지정 데이터베이스 이름을 사용 하 고 있습니다.</p></td>
   <td align="left"><p><strong>사용자 지정 구성을 선택 </strong> 하 고 데이터베이스 이름을 입력 합니다.</p>
   <p>데이터베이스 이름은 고유 해야 하며 설치 되지 않습니다.</p></td>
   </tr>
   </tbody>
   </table>

     

9. **구성** 페이지에서 기본값을 적용 합니다. **이 로컬 컴퓨터를 사용**합니다.

   **참고**  
   관리 서버 및 관리 데이터베이스를 나란히 설치 하는 경우에는이 페이지의 일부 옵션을 사용할 수 없습니다. 이 경우 적절 한 옵션이 기본적으로 선택 되어 있으며 변경할 수 없습니다.

     

10. **구성** (관리 서버 구성) 페이지에서 다음을 지정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">구성할 항목</th>
    <th align="left">설명 및 예제</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>앱-V 환경을 관리할 수 있는 권한이 있는 광고 그룹을 입력 합니다.</p></td>
    <td align="left"><p>예: MyDomain\MyUser</p>
    <p>설치 후 관리 콘솔을 사용 하 여 다른 사용자 또는 그룹을 추가할 수 있습니다. 그러나 전역 보안 그룹과 AD DS (Active Directory 도메인 서비스) 메일 그룹은 지원 되지 않습니다. <strong> </strong> <strong> </strong> 이 작업을 수행 하려면 도메인 로컬 또는 유니버설 그룹을 사용 해야 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>웹 사이트 이름 </strong> : 게시 서비스를 실행 하는 데 사용 되는 사용자 지정 이름을 지정 합니다.</p></td>
    <td align="left"><p>사용자 지정 이름이 없는 경우에는 변경 하지 마세요.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>포트 바인딩 </strong> : app-v에 사용 되는 고유한 포트 번호를 지정 합니다.</p></td>
    <td align="left"><p>예: <strong> 12345</strong></p>
    <p>지정 된 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

11. **게시 서버 구성** **구성** 페이지에서 다음을 지정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">구성할 항목</th>
    <th align="left">설명 및 예제</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>관리 서비스의 URL을 지정 합니다.</p></td>
    <td align="left"><p>예<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>웹 사이트 이름 </strong> : 게시 서비스를 실행 하는 데 사용 되는 사용자 지정 이름을 지정 합니다.</p></td>
    <td align="left"><p>사용자 지정 이름이 없는 경우에는 변경 하지 마세요.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>포트 바인딩 </strong> : app-v에 사용 되는 고유한 포트 번호를 지정 합니다.</p></td>
    <td align="left"><p>예: 54321</p>
    <p>지정 된 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

12. **보고 서버** 페이지에서 다음을 지정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">구성할 항목</th>
    <th align="left">설명 및 예제</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>웹 사이트 이름 </strong> : 보고 서비스를 실행 하는 데 사용 되는 사용자 지정 이름을 지정 합니다.</p></td>
    <td align="left"><p>사용자 지정 이름이 없는 경우에는 변경 하지 마세요.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>포트 바인딩 </strong> : app-v에 사용 되는 고유한 포트 번호를 지정 합니다.</p></td>
    <td align="left"><p>예: 55555</p>
    <p>지정 된 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

13. 설치를 시작 하려면 **준비** 페이지에서 **설치** 를 클릭 한 다음 **완료** 페이지에서 **닫기를** 클릭 합니다.

14. 설치가 성공적으로 완료 되었는지 확인 하려면 웹 브라우저를 열고 다음 URL을 입력 합니다.

    **http:// &lt; 관리 서버 컴퓨터 이름 &gt; : &lt; 관리 서비스 포트 번호 &gt; /Console.html**.

    예: **http://localhost:12345/console.html** . 설치가 완료 되 면 앱에 오류 없이 App-v 관리 콘솔이 표시 됩니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 배포](deploying-app-v-50.md)

[관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[원격 컴퓨터에 게시 서버를 설치하는 방법](how-to-install-the-publishing-server-on-a-remote-computer.md)

[스크립트를 사용하여 App-V 5.0 Server를 배포하는 방법](how-to-deploy-the-app-v-50-server-using-a-script.md)

[PowerShell을 사용하여 App-V 5.0 Client에서 보고를 사용하도록 설정하는 방법](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





