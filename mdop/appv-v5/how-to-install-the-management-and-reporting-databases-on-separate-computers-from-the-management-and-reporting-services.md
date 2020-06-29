---
title: 관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법
description: 관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814025"
---
# 관리 및 보고 서비스에서 개별 컴퓨터에 관리 및 보고 데이터베이스를 설치하는 방법


다음 절차를 사용 하 여 데이터베이스 서버와 관리 서버를 서로 다른 컴퓨터에 설치 합니다. 데이터베이스 서버를 설치 하려는 컴퓨터에서 지원 되는 Microsoft SQL 버전을 실행 하 고 있어야 하며 설치에 실패 하 게 됩니다.

**참고**  
배포를 완료 한 후 관리자가 서비스를 설치 하 여 해당 데이터베이스에 연결할 수 있으려면 **MICROSOFT SQL Server 이름**, **인스턴스 이름** 및 **데이터베이스 이름이** 필요 합니다.



**관리 데이터베이스와 관리 서버를 별도의 컴퓨터에 설치 하려면**

1.  설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다. App-v 5.0 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다. **설치**를 클릭합니다.

2.  **시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.

3.  **Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다. Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다. **다음**을 클릭합니다.

4.  **기능 선택** 페이지에서 **관리 서버 데이터베이스** 확인란을 선택 하 여 설치 하려는 구성 요소를 선택 하 고 **다음**을 클릭 합니다.

5.  **설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.

6.  초기 **새 관리 서버 데이터베이스 만들기 페이지**에서 필요에 따라 기본 선택 항목을 적용 하 고 **다음**을 클릭 합니다.

    사용자 지정 SQL Server 인스턴스를 사용 하는 경우 **사용자 지정 인스턴스 사용** 을 선택 하 고 인스턴스 이름을 입력 합니다.

    사용자 지정 데이터베이스 이름을 사용 하는 경우 **사용자 지정 구성을** 선택 하 고 데이터베이스 이름을 입력 합니다.

7.  다음 **새 관리 서버 데이터베이스 만들기** 페이지에서 **원격 컴퓨터 사용**을 선택 하 고 다음 형식을 사용 하 여 원격 컴퓨터 계정을 입력 합니다. **Domain\\MachineAccount**.

    **참고**  
    동일한 컴퓨터에 관리 서버를 배포 하려는 경우 **이 로컬 컴퓨터 사용**을 선택 해야 합니다.



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. 설치를 시작 하려면 **설치**를 클릭 합니다.

**보고 데이터베이스와 보고 서버를 별도의 컴퓨터에 설치 하려면**

1.  설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다. App-v 5.0 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다. **설치**를 클릭합니다.

2.  **시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.

3.  **Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다. Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다. **다음**을 클릭합니다.

4.  **기능 선택** 페이지에서 **보고 서버 데이터베이스** 확인란을 선택 하 여 설치 하려는 구성 요소를 선택 하 고 **다음**을 클릭 합니다.

5.  **설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.

6.  초기 **새 보고 서버 데이터베이스 만들기** 페이지에서 필요에 따라 기본 선택 항목을 적용 하 고 **다음**을 클릭 합니다.

    사용자 지정 SQL Server 인스턴스를 사용 하는 경우 **사용자 지정 인스턴스 사용** 을 선택 하 고 인스턴스 이름을 입력 합니다.

    사용자 지정 데이터베이스 이름을 사용 하는 경우 **사용자 지정 구성을** 선택 하 고 데이터베이스 이름을 입력 합니다.

7.  다음 **새 보고 서버 데이터베이스 만들기** 페이지에서 **원격 컴퓨터 사용**을 선택 하 고 다음 형식을 사용 하 여 원격 컴퓨터 계정을 입력 합니다. **Domain\\MachineAccount**.

    **참고**  
    같은 컴퓨터에 보고 서버를 배포 하려는 경우 **이 로컬 컴퓨터 사용**을 선택 해야 합니다.



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. 설치를 시작 하려면 **설치**를 클릭 합니다.

**앱-V 5.0 데이터베이스 스크립트를 사용 하 여 관리 및 보고 데이터베이스를 설치 하려면**

1.  설치 하려는 컴퓨터에 App-v 5.0 서버 설치 파일을 복사 합니다.

2.  App-v 5.0 데이터베이스 스크립트의 압축을 풀려면 명령 프롬프트를 열고 설치 파일이 저장 되는 위치를 지정 하 고 다음 명령을 실행 합니다.

    **appv\_server\_setup.exe** **/LAYOUT** **/Layoutdir = "설치 extractionlocation" "** 입니다.

3.  추출이 완료 된 후 App-v 5.0 데이터베이스 스크립트 및 지침 추가 정보 파일에 액세스 하려면 다음을 수행 합니다.

    -   앱-V 5.0 관리 데이터베이스 스크립트 및 지침 추가 정보는 **설치 extractionlocation**  \\  **데이터베이스 스크립트**  \\  **관리 데이터베이스**폴더에 있습니다.

    -   앱-V 5.0 보고 데이터베이스 스크립트 및 지침 추가 정보는 **설치 extractionlocation**  \\  **데이터베이스 스크립트**  \\  **보고 데이터베이스**폴더에 있습니다.

4.  각 데이터베이스에 대해 스크립트를 공유에 복사 하 고 추가 정보 파일의 지침에 따라 수정 합니다.

    **참고**  
    스크립트에 포함 된 필수 Sid를 수정 하는 방법에 대 한 자세한 내용은 [App-v 데이터베이스를 설치 하는 방법 및 PowerShell을 사용 하 여 연결 된 보안 식별자를 변환](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md)하는 방법을 참조 하세요.



5.  Microsoft SQL Server를 실행 하는 컴퓨터에서 스크립트를 실행 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 배포](deploying-app-v-50.md)









