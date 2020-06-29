---
title: 특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법
description: 특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813884"
---
# 특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법

**참고:** App-v 4.6에서 메인스트림 지원이 종료 되었습니다.

다음 절차를 사용 하 여 배포 구성 파일을 사용 하 여 앱-V 4.6 패키지의 확장 지점을 App-v 5.0 패키지로 마이그레이션합니다.

**참고**  다음 절차에서는 App-v 5.0 관리 서버가 필요 하지 않습니다.

 

**배포 구성 파일을 사용 하 여 앱-V 4.6 패키지의 패키지에서 변환 된 앱 V 5.0 패키지로 확장 지점을 마이그레이션하려면**

1. 마이그레이션할 패키지에 대 한 배포 구성 파일이 포함 된 디렉터리를 찾습니다. 정책을 설정 하려면 **Userconfiguration** 섹션에 다음 업데이트를 수행 합니다.

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; 패키지 ID&gt;**

   다음은 배포 구성 파일의 콘텐츠 예제입니다.

   &lt;? xml 버전 = "1.0"?&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; Package ID &gt; DisplayName = &lt; 표시 이름&gt;

   &lt;MachineConfiguration/&gt;

   &lt;UserConfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; 패키지 ID&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. 앱-V 5.0 패키지를 추가 하려면 관리자 권한 PowerShell 명령 프롬프트에서 다음을 입력 합니다.

   PS &gt; **$pkg AppvClientPackage** **–** &lt; 패키지 위치에 대 한 경로 경로 경로가 &gt;  - 배포 구성 파일에 대 한**dynamicdeploymentconfiguration** &lt; 경로입니다.&gt;

   PS &gt; **게시-AppVClientPackage $pkg**

3. 마이그레이션을 테스트 하려면 연결 된 FTAs 또는 바로 가기를 사용 하 여 가상 응용 프로그램을 엽니다. 앱-V 5.0이 있는 응용 프로그램이 열립니다. 두 가지 경우 모두 App-v 4.6 패키지와 변환 된 앱-V 5.0 패키지가 사용자에 게 게시 되지만, 응용 프로그램의 FTAs 및 바로 가기가 App-v 5.0 패키지로 간주 됩니다.

   **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





