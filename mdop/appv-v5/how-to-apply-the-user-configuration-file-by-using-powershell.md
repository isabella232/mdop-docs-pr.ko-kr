---
title: PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법
description: PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814436"
---
# PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법


패키지를 특정 사용자에 게 게시 하 고 패키지가 실행 되는 방식을 결정 하는 경우 동적 사용자 구성 파일이 적용 됩니다.

다음 절차를 사용 하 여 사용자 관련 구성 파일을 지정 합니다. 다음 절차는 예제를 기반으로 합니다.

**c:\\Packages\\Contoso\\MyApp.appv**

**사용자 구성 파일을 적용 하려면**

1.  PowerShell 콘솔을 사용 하 여 패키지를 컴퓨터에 추가 하려면 다음 명령을 입력 합니다.

    **추가-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.

2.  다음 명령을 사용 하 여 패키지를 사용자에 게 게시 하 고 업데이트 된 동적 사용자 구성 파일을 지정 합니다.

    **게시-AppVClientPackage $pkg – DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





