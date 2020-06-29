---
title: MIT Kerberos 영역 지원에 대한 클라이언트를 구성하는 방법
description: MIT Kerberos 영역 지원에 대한 클라이언트를 구성하는 방법
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817813"
---
# MIT Kerberos 영역 지원에 대한 클라이언트를 구성하는 방법


Application Virtualization (App-v) 4.5 SP1에서는 MIT Kerberos 영역에 대 한 지원이 추가 되었습니다. 이 항목에서는 해당 지원을 사용 하도록 설정 하는 방법에 대 한 자세한 정보를 제공 합니다.

**MIT Kerberos 영역에 대 한 지원을 사용 하도록 설정 하려면**

-   다음과 같이 DWORD 형식의 **UseMitKerberos** 이라는 새 레지스트리 키를 만든 다음 값을 1로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos

 

 





