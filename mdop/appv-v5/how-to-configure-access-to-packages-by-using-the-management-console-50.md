---
title: 관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법
description: 관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814420"
---
# 관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법


App-v 5.0 가상화 된 패키지를 배포 하기 전에 응용 프로그램에 액세스 하 고 실행 하도록 허용 되는 AD DS (Active Directory 도메인 서비스) 보안 그룹을 구성 해야 합니다. 보안 그룹에는 컴퓨터 또는 사용자가 포함 될 수 있습니다. 패키지를 컴퓨터 그룹에 Entitling 그룹의 모든 컴퓨터에 패키지를 전역적으로 게시 합니다.

가상화 된 패키지에 대 한 액세스를 구성 하려면 다음 절차를 사용 합니다.

**앱-V 5.0 패키지에 대 한 액세스 권한을 부여 하려면**

1.  구성 하려는 패키지를 찾습니다.

    1.  App-v 5.0 관리 콘솔을 엽니다.

    2.  **광고 액세스** 페이지를 표시 하려면 구성할 패키지를 마우스 오른쪽 단추로 클릭 하 고 **Active directory ACCESS 편집**을 선택 합니다. 또는 패키지를 선택 하 고 **광고 액세스** 창에서 **편집** 을 클릭 합니다.

2.  패키지에 대 한 보안 그룹을 프로 비전 합니다.

    1.  **유효한 ACTIVE DIRECTORY 이름 찾기 및 액세스 권한 부여** 페이지로 이동 합니다.

    2.  **Mydomain**형식 그룹을 사용 하 여  \\  **groupname**Active Directory group 개체 이름의 이름 또는 일부를 입력 하 고 **확인**을 클릭 합니다.

        **참고**  검색할 그룹에 대 한 연결 된 도메인 이름을 제공 해야 합니다.

         

3.  패키지에 대 한 액세스 권한을 부여 하려면 원하는 그룹을 선택 하 고 **액세스 허용**을 클릭 합니다. 새로 추가 된 그룹이 **광고 엔터티에서 ACCESS** 창에 표시 됩니다.

4.  

    기본 구성 설정을 적용 하 고 **광고 액세스** 페이지를 닫으려면 **닫기를**클릭 합니다.

    특정 그룹에 대 한 구성을 사용자 지정 하려면 **할당 된 구성** 드롭다운을 클릭 하 고 **사용자 지정**을 선택 합니다. 사용자 지정 구성을 구성 하려면 **편집**을 클릭 합니다. 액세스 권한을 부여한 후 **닫기를**클릭 합니다.

**App-v 5.0 패키지에 대 한 액세스 권한을 제거 하려면**

1.  구성 하려는 패키지를 찾습니다.

    1.  App-v 5.0 관리 콘솔을 엽니다.

    2.  **광고 액세스** 페이지를 표시 하려면 구성할 패키지를 마우스 오른쪽 단추로 클릭 하 고 **Active directory ACCESS 편집**을 선택 합니다. 또는 패키지를 선택 하 고 **광고 액세스** 창에서 **편집** 을 클릭 합니다.

2.  제거 하려는 그룹을 선택 하 고 **삭제**를 클릭 합니다.

3.  **광고 액세스** 페이지를 닫으려면 **닫기를**클릭 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





