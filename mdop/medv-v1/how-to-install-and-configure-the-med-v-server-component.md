---
title: MED-V 서버 구성 요소를 설치 및 구성하는 방법
description: MED-V 서버 구성 요소를 설치 및 구성하는 방법
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826978"
---
# MED-V 서버 구성 요소를 설치 및 구성하는 방법


이 섹션에서는 MED-V 서버를 [설치](#bkmk-howtoinstallthemedvserver) 하 고 [구성](#bkmk-howtoconfigurethemedvserver) 하는 방법에 대해 설명 합니다.

## <a href="" id="bkmk-howtoinstallthemedvserver"></a>MED-V 서버를 설치 하는 방법


**MED-V 서버를 설치 하려면**

1.  MED-V 서버 .msi 패키지를 설치 합니다.

    MED-V 서버 .msi 패키지는 *MED-V\_Server\_x.msi*호출 되며 여기서 x는 버전 번호입니다.

    예를 들어 *MED-V\_Server\_1.0.65.msi*.

2.  **InstallShield 마법사 시작** 화면이 나타나면 **다음**을 클릭 합니다.

3.  **사용권 계약** 화면에서 사용권 계약을 **읽고 동의 함을 클릭 한**후 **다음**을 클릭 합니다.

    기본 설치 폴더가 표시 된 **대상 폴더** 화면이 표시 됩니다.

    기본 설치 폴더는 *%Systemdrive%\\Program Files\\Microsoft Enterprise 데스크톱 Virtualization\\*입니다.

    -   MED-V가 설치 될 폴더를 변경 하려면 **변경을** 클릭 하 고 기존 폴더를 찾습니다.

4.  **다음**을 클릭합니다.

5.  **프로그램 설치 준비 완료** 화면에서 **설치**를 클릭 합니다.

    MED-V 서버 설치가 시작 됩니다. 이 경우 몇 분 정도 걸릴 수 있으며 화면에 텍스트가 표시 되지 않을 수 있습니다. 설치 중에 몇 가지 진행 화면이 표시 됩니다. 메시지가 표시 되 면 제공 된 지침을 따릅니다.

6.  **InstallShield 마법사 완료** 화면이 나타나면 **마침을** 클릭 하 여 마법사를 완료 합니다.

**참고**  
Microsoft 원격 데스크톱을 통해 MED-V 서버를 설치 하는 경우 다음 구문을 사용 합니다. **mstsc/admin**. RDP 세션이 콘솔로 연결 되어 있는지 확인 합니다.



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a>MED-V 서버를 구성 하는 방법


다음 서버 설정을 구성할 수 있습니다.

-   [연결](#bkmk-configuringconnections)

-   [이미지](#bkmk-configuringimages)

-   [사용 권한](#bkmk-configuringpermissions)

-   [보고](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a>연결 구성

**연결을 구성 하려면**

1.  Windows 시작 메뉴에서 **모든 프로그램 ( &gt; med-v &gt; Med-v-v 서버 구성 관리자**)을 선택 합니다.

    **참고**  
    참고: 서버 설치 중에 **Med-v 서버 구성 관리자 시작** 확인란을 선택한 경우 서버 설치가 완료 되 면 med-v 서버 구성 관리자가 자동으로 시작 됩니다.



~~~
The MED-V Server Configuration Manager appears.
~~~

2. **연결** 탭에서 다음 클라이언트 연결 설정을 구성 합니다.

   -   **포트를 사용 하 여 암호화 되지 않은 연결 (http) 사용**-지정 된 포트를 사용 하 여 암호화 되지 않은 연결을 설정 하려면이 확인란을 선택 합니다. 포트 상자에 암호화 되지 않은 연결 (http)을 수락할 서버 포트를 입력 합니다.

   -   **포트를 사용 하 여 암호화 된 연결 (https) 사용**-지정 된 포트를 사용 하 여 암호화 된 연결을 사용 하도록 설정 하려면이 확인란을 선택 합니다. 포트 상자에 암호화 된 연결을 수락할 서버 포트 (https)를 입력 합니다.

       Https는 MED-V 서버와 MED-V 클라이언트 간의 보안 트랜잭션을 보장 하도록 설정할 수 있는 선택적 구성입니다. Https를 구성 하려면 다음 절차를 수행 해야 합니다.

       -   서버에서 인증서를 구성 합니다.

       -   Netsh를 사용 하 여 서버 인증서를 지정 된 포트와 연결 합니다. 자세한 내용은 다음을 참조 하세요.

           -   [하이퍼텍스트 전송 프로토콜 (HTTP) 용 Netsh 명령](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [방법: SSL 인증서를 사용 하 여 포트 구성](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [방법: SSL 인증서를 사용 하 여 포트 구성](https://msdn.microsoft.com/library/ms733791.aspx)

3. **확인**을 클릭합니다.

### <a href="" id="bkmk-configuringimages"></a>이미지 구성

**이미지를 구성 하려면**

1.  **이미지** 탭을 클릭 합니다.

2.  다음과 같은 이미지 관리 설정을 구성 합니다.

    -   **Vm 디렉터리**-가상 컴퓨터 디렉터리 (이미지가 저장 되는 디렉터리) 이 필드에는 MED-V 서버에서 액세스할 수 있어야 하는 image 배포 서버의 이미지 디렉터리에 대 한 UNC 경로가 있습니다.

    -   **VM URL**-이미지가 저장 된 서버의 위치입니다.

3.  **확인**을 클릭합니다.

### <a href="" id="bkmk-configuringpermissions"></a>사용 권한 구성

**사용 권한을 구성 하려면**

1.  **사용 권한** 탭을 클릭 합니다.

2.  로그인 할 수 있는 모든 사용자의 목록이 제공 됩니다. 사용자에 게 읽기 및 쓰기 권한을 적용 하려면 사용자 옆에 있는 확인란을 선택 합니다. 사용자에 게 읽기 전용 권한을 적용 하려면 확인란의 선택을 취소 합니다.

3.  도메인 사용자 또는 그룹을 추가 하려면 **추가**를 클릭 합니다.

    **사용자 또는 그룹 이름 입력** 대화 상자가 나타납니다.

    1.  다음 중 하나를 수행 하 여 도메인 사용자 또는 그룹을 선택 합니다.

        -   **사용자 또는 그룹 이름 입력** 필드에 도메인에 존재 하는 사용자 또는 그룹을 입력 하거나 컴퓨터의 로컬 사용자 또는 그룹으로 존재 합니다. 그런 다음 **이름 확인** 을 클릭 하 여 기존 이름으로 확인 합니다.

        -   **찾기를** 클릭 하 여 표준 **사용자 또는 그룹 선택** 대화 상자를 엽니다. 그런 다음 도메인 사용자 또는 그룹을 선택 합니다.

    2.  **확인**을 클릭합니다.

4.  도메인 사용자 또는 그룹을 제거 하려면 사용자 또는 그룹을 선택 하 고 **제거**를 클릭 합니다.

5.  **확인**을 클릭합니다.

### <a href="" id="bkmk-configuringreports"></a>보고서 구성

**보고서를 구성 하려면**

1.  **보고서** 탭을 클릭 합니다.

2.  보고서를 지원 하려면 **보고서 사용**을 선택 합니다.

3.  **연결 문자열** 상자에 MSSQL 데이터베이스에 대 한 연결 문자열을 입력 합니다.

    -   원격 서버에 SQL Server가 설치 되어 있는 경우 다음 연결 문자열을 사용 합니다.

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **참고**  
        참고: SQL Express에 연결 하려면 다음을 사용 합니다. `Data Source=<ServerName>\sqlexpress.`



4.  데이터베이스를 만들려면 **데이터베이스 만들기**를 클릭 합니다.

5.  연결을 테스트 하려면 **연결 테스트**를 클릭 합니다.

6.  데이터베이스 지우기 옵션을 구성 하려면 **지우기 옵션**을 클릭 합니다.

    **데이터베이스 옵션 지우기** 대화 상자가 나타납니다.

    1.  다음 옵션 중 하나를 선택 합니다.

        -   다음 **보다 오래 된 데이터 지우기**— 지정한 날짜 수보다 이전의 모든 데이터를 지웁니다. 번호 상자에 일 수를 입력 합니다.

        -   **데이터베이스에서 모든 데이터 지우기**-데이터베이스에서 존재 하는 모든 데이터를 지웁니다.

        -   **데이터베이스 놓기**-데이터베이스를 삭제 합니다.

    2.  **확인** 을 클릭 하 여 변경 내용을 적용 하 고 대화 상자를 닫습니다.

7.  **확인** 을 클릭 하 여 변경 내용을 저장 하거나 **취소** 를 클릭 하 여 변경 내용을 저장 하지 않고 대화 상자를 닫습니다.

8.  메시지가 표시 되 면 MED-V 서버 서비스를 다시 시작 하 여 네트워크 설정에 변경 내용을 적용 합니다.

## 관련 항목


[지원되는 구성](supported-configurationsmedv-orientation.md)

[MED-V 서버 인프라 디자인](design-the-med-v-server-infrastructure.md)









