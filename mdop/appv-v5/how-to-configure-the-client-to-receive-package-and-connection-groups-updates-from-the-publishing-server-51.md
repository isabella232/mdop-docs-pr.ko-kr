---
title: 클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법
description: 클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법
author: dansimp
ms.assetid: 23b2d03a-20ce-4973-99ee-748f3b682207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 034cf5255d75bbaf6a5e65357bd5b3d472344f03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814393"
---
# 클라이언트가 게시 서버에서 패키지 및 연결 그룹 업데이트를 받도록 구성하는 방법


App-v 5.1 게시 서버를 사용 하 여 패키지 및 연결 그룹을 배포 하면 단일 위치 관리와 높은 확장성을 제공 하기 때문에 유용 합니다.

게시 서버에서 업데이트를 받도록 App-v 5.1 클라이언트를 구성 하려면 다음 단계를 사용 합니다.

**참고**  다음 절차에서는 관리 서버가 **MyMgmtSrv**이라는 컴퓨터에 설치 되었고 게시 서버는 **MyPubSrv**라는 컴퓨터에 설치 되어 있습니다.

 

**게시 서버에서 업데이트를 받도록 App-v 5.1 클라이언트를 구성 하려면**

1.  앱-V 5.1 관리 및 게시 서버를 배포 하 고 필요한 패키지 및 연결 그룹을 추가 합니다. 패키지 및 연결 그룹을 추가 하는 방법에 대 한 자세한 내용은 [관리 콘솔을 사용 하 여 패키지를 추가 하거나 업그레이드 하는 방법과](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) [연결 그룹을 만드는](how-to-create-a-connection-group51.md)방법을 참조 하세요.

2.  관리 콘솔을 열려면 다음 링크를 클릭 하 고 브라우저를 열고 다음을 입력 합니다. http://MyMgmtSrv/AppvManagement/Console.html 웹 브라우저에서 특정 사용자 집합에 필요한 모든 패키지 및 연결 그룹을 가져오고, 게시 하 고, entitle.

3.  App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 관리자 권한 PowerShell 명령 프롬프트를 열고 다음 명령을 실행 합니다.

    **추가-AppvPublishingServer-이름 ABC-URL http://MyPubSrv/AppvPublishing**

    이 명령은 지정 된 게시 서버를 구성 합니다. 다음과 유사한 출력이 표시 됩니다.

    Id: 1

    SetByGroupPolicy: False

    이름: ABC

    URL: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: False

    GlobalRefreshOnLogon: False

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: 일

    UserRefreshEnabled: True

    UserRefreshOnLogon: True

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: 일

    반환 되는 Id-이 경우 1

4.  App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 PowerShell 명령 프롬프트를 열고 다음 명령을 입력 합니다.

    **Sync-AppvPublishingServer-ServerId 1**

    이 명령은 관리 서버에 구성 된 패키지 및 연결 그룹에 대 한 권리를 기반으로 해당 클라이언트에 대해 추가 또는 제거 해야 하는 패키지 및 연결 그룹에 대 한 게시 서버를 쿼리 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

 

 





