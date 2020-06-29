---
title: 응용 프로그램 게시를 테스트하는 방법
description: 응용 프로그램 게시를 테스트하는 방법
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826913"
---
# 응용 프로그램 게시를 테스트하는 방법


처음으로 설치를 완료 한 후에 다음 작업을 수행 하 여 응용 프로그램 게시 기능이 예상 대로 작동 하는지 확인할 수 있습니다.

<a href="" id="bkmk-apppub"></a>**응용 프로그램 게시를 테스트 하려면**

1.  게시에 대해 지정한 응용 프로그램이 표시 되는지 확인 합니다.

    **시작** 을 클릭 한 다음 **모든 프로그램** 을 클릭 하 고 지정 된 응용 프로그램을 검색 합니다.

    경우에 따라 호스트 컴퓨터에 같은 응용 프로그램을 두 번 설치 했을 때와 게스트에 한 번 사용할 수 있습니다. 동일한 이름을 가진 게시 된 응용 프로그램이 호스트 **시작** 메뉴의 동일한 위치에 게시 되는 경우 가상 컴퓨터 이름을 바로 가기 이름에 추가 하 여 호스트 응용 프로그램 바로 가기에서 구분 합니다. 예를 들어 "MEDVHost1" 이라는 가상 컴퓨터의 경우 호스트 응용 프로그램이 "Notepad"이 고 게시 된 응용 프로그램이 "Notepad (MEDVHost1)" 일 수 있습니다.

2.  응용 프로그램이 의도 한 대로 작동 하는지 확인 합니다.

    호스트 컴퓨터에서 게시 한 응용 프로그램을 시작 하 고 게스트의 Windows XP SP3에서 열려 있는지 확인 합니다. 응용 프로그램이 호스트 컴퓨터 데스크톱의 Windows XP 스타일 창에 표시 되어야 합니다.

3.  해당 하는 경우 문서 리디렉션이 의도 한 대로 작동 하는지 확인 합니다.

    게스트의 게시 된 응용 프로그램이 호스트 시스템 드라이브의 폴더를 열어야 하는 경우 지정 된 폴더를 열 수 있는지 확인 합니다.

    **중요**  Windows 가상 PC는 이미 공유 된 폴더에서 공유 만들기를 지원 하지 않으므로 네트워크에 있는 내 문서 폴더 등 공유 폴더에서 여는 문서에 대해서는 리디렉션이 발생 하지 않습니다. 자세한 내용은 [운영 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.

게시 된 응용 프로그램이 설치 되어 있고 제대로 작동 하는지 확인 한 후에는 MED-V 작업 영역에서 응용 프로그램을 추가 하거나 제거할 수 있는지 여부를 테스트할 수 있습니다.

**응용 프로그램을 추가 하거나 제거할 수 있는지 테스트 하려면**

1.  MED-V 작업 영역에서 응용 프로그램을 추가 하거나 제거 합니다.

    MED-V 작업 영역에서 응용 프로그램을 추가 하 고 제거 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역에 배포 된 응용 프로그램 관리](managing-applications-deployed-to-med-v-workspaces.md)를 참조 하세요.

2.  응용 프로그램을 추가한 경우에는의 단계를 반복 하 여 [응용 프로그램 게시를 테스트](#bkmk-apppub) 하 여 새 응용 프로그램이 의도 한 대로 작동 하는지 확인 합니다.

3.  응용 프로그램을 제거한 경우 **시작** 을 클릭 한 다음 **모든 프로그램** 을 클릭 하 고 제거한 모든 응용 프로그램이 더 이상 나열 되지 않는지 확인 합니다.

**참고**  응용 프로그램 게시 설정을 확인할 때 문제가 발생 하는 경우에는 [작업 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.

응용 프로그램 게시 테스트를 완료 한 후 다른 MED-V 작업 영역 구성을 테스트 하 여 의도 한 대로 작동 하는지 확인할 수 있습니다.

MED-V 작업 영역 패키지 테스트를 완료 하 고 의도 한 대로 작동 하는지 확인 한 후에는 MED-V 작업 영역을 enterprise에 배포할 수 있습니다.

## 관련 항목

[URL 리디렉션을 테스트하는 방법](how-to-test-url-redirection.md)

[처음 설치 설정을 확인하는 방법](how-to-verify-first-time-setup-settings.md)

[MED-V 작업 영역 패키지 배포](deploying-the-med-v-workspace-package.md)

 

 





