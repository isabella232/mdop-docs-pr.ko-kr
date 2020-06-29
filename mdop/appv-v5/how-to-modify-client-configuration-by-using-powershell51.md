---
title: PowerShell을 사용하여 클라이언트 구성을 수정하는 방법
description: PowerShell을 사용하여 클라이언트 구성을 수정하는 방법
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813812"
---
# PowerShell을 사용하여 클라이언트 구성을 수정하는 방법


다음 절차를 사용 하 여 App-v 5.1 클라이언트 구성을 구성 합니다.

**PowerShell을 사용 하 여 App-v 5.1 클라이언트 구성을 수정 하려면**

1.  PowerShell을 사용 하 여 클라이언트 설정을 구성 하려면 **Set-AppvClientConfiguration** cmdlet을 사용 합니다. PowerShell을 설치 하는 방법에 대 한 자세한 내용과 cmdlet 목록에는 [Powershell cmdlet을 로드 하는 방법과 Cmdlet 도움말](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)을 참조 하세요.

2.  클라이언트 구성을 수정 하려면 PowerShell 명령 프롬프트를 열고 필요한 매개 변수를 사용 하 여 다음 cmdlet **Set-AppvClientConfiguration** 를 실행 합니다. 예:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)

 

 





