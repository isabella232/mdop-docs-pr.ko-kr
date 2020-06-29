---
title: FileSystem 캐시의 크기를 변경하는 방법
description: FileSystem 캐시의 크기를 변경하는 방법
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818003"
---
# FileSystem 캐시의 크기를 변경하는 방법


명령줄을 사용 하 여 파일 시스템 캐시의 크기를 변경할 수 있습니다. 이 작업을 수행 하려면 캐시를 완전히 다시 설정 해야 하며, 관리 권한이 필요 합니다.

**파일 시스템 캐시의 크기를 변경 하려면**

1.  다음 레지스트리 값을 0 (영)으로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  다음 레지스트리 값을 패키지를 보유 하는 데 필요한 최대 캐시 크기인 MB (예: 8192 MB)로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize

3.  컴퓨터를 다시 시작 합니다.

## 관련 항목


[명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





