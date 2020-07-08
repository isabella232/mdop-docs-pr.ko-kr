---
ms.reviewer: ''
title: 특정 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
description: 특정 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813740"
---
# 특정 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법

*참고:** app-v 4.6에는 메인스트림 지원이 종료 되었습니다.

다음 절차를 사용 하 여 사용자 구성 파일을 사용 하 여 app-v 5.0 패키지를 App-v 파일 형식으로 되돌립니다.

**패키지 되돌리기**

1.  앱-V 4.6 패키지가 사용자에 게 게시 되어 있지만 다음 마이그레이션 방법을 사용 하 여 FTAs 및 바로 가기가 앱-v 5.0 패키지에 의해 간주 되는 것을 확인 합니다. [앱-v 4.6 패키지의 확장 지점을 특정 사용자를 위한 app-v 5.0로 마이그레이션하는 방법을 설명](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)합니다.

    변환 된 패키지에 대 한 배포 구성 파일의 **userconfiguration** 섹션에서 정책을 설정 하려면 **userconfiguration** 섹션: **ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSE" PackageName = &lt; package ID &gt; ** 에 대해 다음 업데이트를 수행 합니다.

2.  관리자 권한 명령 프롬프트에서 다음을 입력 합니다.

    PS &gt; **게시-AppVClientPackage $pkg –** &lt; 사용자 구성 파일에 대 한 DynamicUserConfigurationPath 경로&gt;

3.  게시 새로 고침을 수행 하거나 App-v 4.6에 대해 예정 된 다음 게시 새로 고침을 기다립니다. FTAs 또는 바로 가기를 사용 하 여 응용 프로그램을 엽니다. 이제 응용 프로그램이 app-v 4.6 SP2를 사용 하 여 열립니다.

    **참고**  
    App-v 5.0 패키지가 더 이상 필요 하지 않은 경우 App-v 5.0 패키지의 게시를 취소 하면 확장 지점이 자동으로 App-v 4.6로 다시 전환 됩니다.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)












