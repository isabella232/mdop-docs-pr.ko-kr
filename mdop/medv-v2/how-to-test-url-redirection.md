---
title: URL 리디렉션을 테스트하는 방법
description: URL 리디렉션을 테스트하는 방법
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824448"
---
# URL 리디렉션을 테스트하는 방법


처음으로 설치를 완료 한 후에 다음 작업을 수행 하 여 URL 리디렉션 기능이 예상 대로 작동 하는지 확인할 수 있습니다.

**중요**  MED-V 호스트 에이전트는 URL 리디렉션이 올바르게 작동 하려면 실행 중 이어야 합니다.

<a href="" id="bkmk-urlredir"></a>**URL 리디렉션을 테스트 하려면**

1.  호스트 컴퓨터에서 Internet Explorer 브라우저를 열고 리디렉션에 대해 지정한 URL을 입력 합니다.

2.  게스트 가상 컴퓨터의 Internet Explorer에서 웹 페이지가 열려 있는지 확인 합니다.

3.  테스트 하려는 각 URL에 대해이 과정을 반복 합니다.

**URL을 추가 하거나 제거할 수 있는지 테스트 하려면**

1.  MED-V 작업 영역에서 URL을 추가 하거나 제거 합니다.

    MED-V 작업 영역의 리디렉션에 대 한 Url을 추가 하 고 제거 하는 방법에 대 한 자세한 내용은 [MED-V URL 리디렉션 관리](manage-med-v-url-redirection.md)를 참조 하세요.

2.  리디렉션 목록에 URL을 추가한 경우에는 [Url 리디렉션을 테스트 하](#bkmk-urlredir) 는 단계를 반복 하 여 새 URL이 의도 한 대로 리디렉션 되는지 확인 합니다.

3.  리디렉션 목록에서 URL을 제거한 경우 다음 단계를 따라 제거 되었는지 확인 합니다.

    1.  호스트 컴퓨터에서 Internet Explorer 브라우저를 열고 리디렉션 목록에서 제거한 URL을 입력 합니다.

    2.  게스트 가상 컴퓨터가 아닌 호스트 컴퓨터의 Internet Explorer에서 웹 페이지가 열려 있는지 확인 합니다.

        **참고**  URL 리디렉션 변경 내용이 적용 되는 데 몇 초 정도 걸릴 수 있습니다.

**참고**  URL 리디렉션 설정을 확인할 때 문제가 발생 하는 경우에는 [작업 문제 해결](operations-troubleshooting-medv2.md)을 참조 하세요.

MED-V 작업 영역에서 URL 리디렉션 테스트를 완료 한 후 다른 구성을 테스트 하 여 의도 한 대로 작동 하는지 확인할 수 있습니다.

MED-V 작업 영역 패키지 테스트를 완료 하 고 의도 한 대로 작동 하는지 확인 한 후에는 MED-V 작업 영역을 enterprise에 배포할 수 있습니다.

## 관련 항목

[응용 프로그램 게시를 테스트하는 방법](how-to-test-application-publishing.md)

[처음 설치 설정을 확인하는 방법](how-to-verify-first-time-setup-settings.md)

[MED-V 작업 영역 패키지 배포](deploying-the-med-v-workspace-package.md)

 

 





