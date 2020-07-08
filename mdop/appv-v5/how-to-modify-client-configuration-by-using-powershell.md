---
title: PowerShell을 사용하여 클라이언트 구성을 수정하는 방법
description: PowerShell을 사용하여 클라이언트 구성을 수정하는 방법
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813828"
---
# PowerShell을 사용하여 클라이언트 구성을 수정하는 방법


다음 절차를 사용 하 여 App-v 5.0 클라이언트 구성을 구성 합니다.

**PowerShell을 사용 하 여 App-v 5.0 클라이언트 구성을 수정 하려면**

1.  PowerShell을 사용 하 여 클라이언트 설정을 구성 하려면 **Set-AppvClientConfiguration** cmdlet을 사용 합니다.

2.  클라이언트 구성을 수정 하려면 PowerShell 명령 프롬프트를 열고 필요한 매개 변수를 사용 하 여 다음 cmdlet **Set-AppvClientConfiguration** 를 실행 합니다. 예:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





