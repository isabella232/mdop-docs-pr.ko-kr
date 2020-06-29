---
title: 캐시 크기 및 드라이브 문자 지정을 변경하는 방법
description: 캐시 크기 및 드라이브 문자 지정을 변경하는 방법
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818038"
---
# 캐시 크기 및 드라이브 문자 지정을 변경하는 방법


응용 프로그램 가상화 클라이언트 관리 콘솔의 **응용 프로그램 가상화** 노드에서 직접 캐시 크기 및 드라이브 문자 지정을 변경할 수 있습니다.

**참고**  
캐시 크기를 설정한 후에는 더 작게 만들 수 없습니다.



**캐시 크기를 변경 하려면**

1.  **Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.

2.  **속성** 대화 상자에서 **파일 시스템** 탭을 선택 합니다. **클라이언트 캐시 구성 설정** 섹션에서 다음 라디오 단추 중 하나를 클릭 하 여 캐시 공간을 관리 하는 방법을 선택 합니다.

    **중요**  
    **사용 가능한 디스크 공간 임계값** 설정을 선택 하면 입력 하는 값에 의해 캐시 크기가 총 디스크 크기에서 입력 한 빈 디스크 공간 임계값을 뺀 수로 설정 됩니다. 그런 다음 **최대 캐시 크기 사용** 설정을 사용 하 여 되돌리려는 경우 기존 캐시 크기 보다 큰 값을 지정 해야 합니다. 그렇지 않으면 "새 크기는 기존 캐시 크기 보다 커야 합니다." 오류가 표시 됩니다.



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. **확인** 또는 **적용** 을 클릭 하 여 설정을 변경 합니다.

**드라이브 문자 지정을 변경 하려면**

1.  **Application Virtualization** 노드를 마우스 오른쪽 단추로 클릭 하 고 팝업 메뉴에서 **속성** 을 선택 합니다.

2.  **속성** 대화 상자의 **파일 시스템** 탭에 있는 **사용할 드라이브** 필드에서 사용 가능한 드라이브 문자 드롭다운 목록에서 원하는 드라이브 문자를 선택 합니다. 이 설정은 컴퓨터를 다시 부팅할 때 적용 됩니다.

3.  **확인** 또는 **적용** 을 클릭 하 여 설정을 변경 합니다.

## 관련 항목


[Application Virtualization Client Management Console에서 클라이언트를 구성하는 방법](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









