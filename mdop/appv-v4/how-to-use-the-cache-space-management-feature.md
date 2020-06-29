---
title: 캐시 공간 관리 기능을 사용하는 방법
description: 캐시 공간 관리 기능을 사용하는 방법
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816408"
---
# 캐시 공간 관리 기능을 사용하는 방법


파일 시스템 캐시 공간 관리 기능은 LRU (최근에 사용 되지 않은) 알고리즘을 사용 하며 기본적으로 사용 하도록 설정 되어 있습니다. 새 패키지에 필요한 공간이 캐시의 사용 가능한 공간을 초과 하는 경우 Application Virtualization (App-v) 클라이언트는이 기능을 사용 하 여 새 패키지에 대 한 공간을 만들기 위해 캐시에서 삭제할 수 있는 기존 패키지를 결정 합니다. 클라이언트가 MinPkgAge 레지스트리 값에 지정 된 값 보다 오래 된 경우 가장 오래 된 마지막으로 액세스 한 날짜를 사용 하 여 패키지를 삭제 합니다. 파일 시스템 캐시 공간 관리 기능을 사용 하면 캐시 공간 문제를 방지 하는 데에도 도움이 될 수 있습니다.

필요한 경우 두 개 이상의 패키지를 삭제 합니다. 잠긴 패키지는 삭제 되지 않습니다.

**참고**  캐시에 배포할 수 있는 모든 패키지에 대해 충분 한 공간이 할당 되었는지 확인 하려면 필요에 따라 캐시를 확장할 수 있도록 클라이언트를 구성할 때 사용 **가능한 디스크 공간 임계값** 설정을 사용 합니다. 또는, App-v 캐시에 필요한 디스크 공간을 미리 결정 하 고 설치 시간에 캐시 크기를 적절 하 게 설정 합니다.

 

캐시 공간 관리 기능은 UnloadLeastRecentlyUsed 레지스트리 값으로 제어 됩니다. 값 1은 해당 기능을 사용 하도록 설정 하 고 0 이면 값을 사용 하지 않습니다.

**캐시 공간 관리 기능을 사용 하거나 사용 하지 않도록 설정 하려면**

-   다음 레지스트리 값을 1로 설정 하 여 LRU 알고리즘을 사용 합니다. 이 기능을 사용 하지 않으려면 0으로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed

**삭제할 수 있는 패키지를 제어 하려면**

-   패키지를 취소 하도록 선택할 수 있는 시간을 결정 하려면 다음 레지스트리 값을 패키지를 마지막으로 액세스 한 이후 경과 되는 최소 날짜 수와 동일 하 게 설정 합니다. 최근에 사용한 패키지는 삭제 되지 않습니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge

    **주의**  사항 이 레지스트리 키의 최대 값은 0x00011111입니다. 값이 클수록 캐시 공간 관리 기능이 제대로 작동 하지 않습니다.

     

## 관련 항목


[명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





