---
title: 독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법
description: 독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813972"
---
# 독립 실행형 컴퓨터에 보고 서버를 설치하고 데이터베이스에 연결하는 방법

다음 절차를 사용 하 여 독립 실행형 컴퓨터에 보고 서버를 설치 하 고 데이터베이스에 연결 합니다.

**중요** 다음 절차를 수행 하기 전에 [app-v 5.1 보고에 대해](about-app-v-51-reporting.md)읽고 이해 해야 합니다.

## 독립 실행형 컴퓨터에 보고 서버를 설치 하 고 데이터베이스에 연결 하려면

1. 설치 하려는 컴퓨터에 App-v 5.1 서버 설치 파일을 복사 합니다. App-v 5.1 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다. **설치**를 클릭합니다.

2. **시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.

3. **Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다. Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다. **다음**을 클릭합니다.

4. **기능 선택** 페이지에서 **보고 서버** 확인란을 선택 하 고 **다음**을 클릭 합니다.

5. **설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.

6. **기존 보고 데이터베이스 구성** 페이지에서 **원격 SQL server 사용**을 선택 하 고 Microsoft SQL server를 실행 하는 컴퓨터의 컴퓨터 이름 (예: **SqlServerMachine**을 입력 합니다.

    > [!NOTE]
    > Microsoft SQL Server가 같은 서버에 배포 된 경우 **로컬 Sql Server 사용**을 선택 합니다.

    SQL Server 인스턴스의 경우 **기본 인스턴스 사용**을 선택 합니다. 사용자 지정 Microsoft SQL Server 인스턴스를 사용 하는 경우 **사용자 지정 인스턴스 사용** 을 선택한 다음 인스턴스의 이름을 입력 해야 합니다.

    이 보고 서버에서 사용할 **SQL Server 데이터베이스 이름** (예: **AppvReporting**)을 지정 합니다.

7. " **보고 서버 구성 구성** " 페이지

   - 보고 서비스에 사용할 웹 사이트 이름을 지정 합니다. 사용자 지정 이름이 없는 경우 기본값을 변경 하지 않고 그대로 둡니다.

   - **포트 바인딩에**대해 app-v 5.1 (예: **55555**)에서 사용 되는 고유 포트 번호를 지정 합니다. 또한 지정한 포트를 다른 웹 사이트에서 사용 하 고 있지 않은지 확인 해야 합니다.

8. **설치**를 클릭합니다.

**App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목

[App-V 5.1 보고 정보](about-app-v-51-reporting.md)

[App-V 5.1 배포](deploying-app-v-51.md)

[PowerShell을 사용하여 App-V 5.1 Client에서 보고를 사용하도록 설정하는 방법](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
