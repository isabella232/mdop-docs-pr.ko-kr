---
title: 독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법
description: 독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814012"
---
# 독립 실행형 컴퓨터에 관리 서버를 설치하고 데이터베이스에 연결하는 방법


독립 실행형 컴퓨터에 관리 서버를 설치 하 고 데이터베이스에 연결 하려면 다음 절차를 사용 합니다.

**독립 실행형 컴퓨터에 관리 서버를 설치 하 고 데이터베이스에 연결 하려면**

1.  설치 하려는 컴퓨터에 App-v 5.1 서버 설치 파일을 복사 합니다. App-v 5.1 서버 설치를 시작 하려면 관리자로 **appv\_server\_setup.exe** 를 마우스 오른쪽 단추로 클릭 하 여 실행 합니다. **설치**를 클릭합니다.

2.  **시작** 페이지에서 사용 조건을 검토 하 고 수락 하 고 **다음**을 클릭 합니다.

3.  **Microsoft update를 사용 하 여 컴퓨터를 안전** 하 게 보호 하 고, microsoft 업데이트를 사용 하도록 설정 하려면 **업데이트 확인 시 microsoft Update 사용 (권장)** 을 선택 합니다. Microsoft 업데이트를 사용 하지 않도록 설정 하려면 **Microsoft 업데이트 사용**안 함을 선택 합니다. **다음**을 클릭합니다.

4.  **기능 선택** 페이지에서 **관리 서버** 확인란을 선택 하 고 **다음**을 클릭 합니다.

5.  **설치 위치** 페이지에서 기본 위치를 그대로 두고 **다음**을 클릭 합니다.

6.  **기존 관리 데이터베이스 구성** 페이지에서 **원격 SQL Server 사용**을 선택 하 고 Microsoft SQL sql을 실행 하는 컴퓨터의 컴퓨터 이름 (예: **SqlServerMachine**을 입력 합니다.

    **참고**  
    Microsoft SQL Server가 같은 서버에 배포 된 경우 **로컬 Sql Server 사용**을 선택 합니다.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. **관리 서버 구성 구성** 페이지에서 관리 콘솔에 연결할 AD 그룹 또는 계정 (예: **MyDomain\\MyUser** 또는 **MyDomain\\AdminGroup**)을 관리 하기 위해 지정 합니다. 지정 하는 계정이 나 광고 그룹이 관리 콘솔을 통해 서버를 관리 하도록 설정 됩니다. 설치 후 관리 콘솔을 사용 하 여 추가 사용자 또는 그룹을 추가할 수 있습니다.

   관리 서비스에 사용할 **웹 사이트 이름을** 지정 합니다. 사용자 지정 이름이 없는 경우 기본값을 그대로 사용 합니다. **포트 바인딩에서**사용할 고유 포트 번호 (예: **12345**)를 지정 합니다.

8. **설치**를 클릭합니다.

9. 설정이 성공적으로 완료 되었는지 확인 하려면 웹 브라우저를 열고 다음 URL을 입력 http://managementserver:portnumber/Console 합니다. 성공적으로 설치 되 면 오류 메시지 또는 경고가 표시 되지 않고 **관리 콘솔이** 나타날 것으로 표시 됩니다.

   **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 배포](deploying-app-v-51.md)









