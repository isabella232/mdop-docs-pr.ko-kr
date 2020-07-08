---
title: 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법
description: 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813876"
---
# 특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법

*참고:** app-v 4.6에는 메인스트림 지원이 종료 되었습니다.

다음 절차를 사용 하 여 사용자 구성 파일을 사용 하 여 App-v로 만든 패키지를 마이그레이션합니다.

**패키지를 변환 하려면**

1. 변환 하려는 패키지의 사용자 구성 파일을 찾습니다. 정책을 설정 하려면 **Userconfiguration** 섹션: **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGENAME = &lt; Package ID &gt; **에서 다음 업데이트를 수행 합니다.

   다음은 사용자 구성 파일의 예입니다.

   &lt;? xml 버전 = "1.0"?&gt;

   &lt;UserConfiguration PackageId = &lt; 패키지 ID &gt; DisplayName = &lt; 패키지의 이름입니다.&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; 패키지 ID&gt;

   &lt;/UserConfiguration&gt;

2. 앱-V 5.0 패키지를 추가 하려면 관리자 권한 PowerShell 명령 프롬프트에서 다음을 입력 합니다.

   PS &gt; **$Pkg = AppvClientPackage-** &lt; 패키지 위치의 경로 경로&gt;

   PS &gt; **게시-AppVClientPackage $pkg-** &lt; 사용자 구성 파일에 대 한 DynamicUserConfiguration 경로&gt;

3. FTAs 또는 지금 바로 가기 키를 사용 하 여 응용 프로그램을 엽니다. 응용 프로그램은 App-v 5.0를 사용 하 여 열어야 합니다.

   App-v SP2 패키지와 변환 된 앱-V 5.0 패키지가 사용자에 게 게시 되지만, 응용 프로그램의 FTAs 및 바로 가기가 App-v 5.0 패키지에 의해 간주 됩니다.

   **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





