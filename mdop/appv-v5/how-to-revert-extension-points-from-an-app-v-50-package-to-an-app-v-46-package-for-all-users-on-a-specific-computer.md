---
title: 특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
description: 특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813729"
---
# 특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법

*참고:** app-v 4.6에는 메인스트림 지원이 종료 되었습니다. 다음은 App-v 4.6 SP3 클라이언트가 이미 설치 되어 있다고 가정 합니다.

다음 절차를 사용 하 여 배포 구성 파일을 사용 하 여 앱-V 5.0 패키지의 확장 지점을 App-v 4.6 파일 형식으로 되돌립니다.

**패키지 되돌리기**

1.  앱-V 4.6 패키지가 사용자에 게 게시 되어 있지만 다음 마이그레이션 방법을 사용 하 여 FTAs 및 바로 가기가 앱-v 5.0 패키지에 의해 간주 되는 경우 [특정 컴퓨터의 모든 사용자에 대해 앱-v 4.6 패키지의 확장 지점을 변환 된 app-v 5.0 패키지로 마이그레이션하는 방법을](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)확인 합니다.

    변환 된 패키지에 대 한 배포 구성 파일의 **userconfiguration** 섹션에서 정책을 설정 하려면 **userconfiguration** 섹션: **ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSE" PackageName = &lt; package ID &gt; ** 에 대해 다음 업데이트를 수행 합니다.

2.  관리자 권한 명령 프롬프트에서 다음을 입력 합니다.

    PS &gt; **Set-AppvClientPackage $pkg –** &lt; 배포 구성 파일에 대 한 dynamicdeploymentconfiguration 경로&gt;

    PS &gt; **게시-AppVClientPackage $Pkg – DynamicUserConfigurationType useDeploymentConfiguration**

3.  게시 새로 고침을 수행 하거나 App-v 4.6 SP2 패키지에 예정 된 다음 게시 새로 고침을 기다립니다.

    FTAs 또는 바로 가기를 사용 하 여 응용 프로그램을 엽니다. 이제 앱이 app-v 4.6를 사용 하 여 열립니다.

    **참고**  
    App-v 5.0 패키지가 더 이상 필요 하지 않은 경우 App-v 5.0 패키지의 게시를 취소 하면 확장 지점이 자동으로 App-v 4.6로 다시 전환 됩니다.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)









