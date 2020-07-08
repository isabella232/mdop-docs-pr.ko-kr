---
title: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
description: 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824293"
---
# 분실한 컴퓨터의 BitLocker 암호화 상태를 확인하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하면 분실 하거나 도난당 한 컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태를 확인할 수 있습니다. 다음 절차를 사용 하 여 더 이상 소유 하지 않는 컴퓨터에서 볼륨이 암호화 되었는지 확인 합니다.

**컴퓨터의 마지막으로 알려진 BitLocker 암호화 상태 확인**

1.  MBAM 웹 사이트를 엽니다.

    **참고**  MBAM 웹 사이트의 기본 주소는 http://* &lt; computername &gt; *입니다. 더 빠른 검색 결과를 위해 정규화 된 서버 이름을 사용 합니다.

     

2.  탐색 창에서 **보고서** 노드를 선택한 다음 **컴퓨터 준수 보고서**를 선택 합니다.

3.  오른쪽 창의 필터 필드를 사용 하 여 검색 결과의 범위를 좁히고 **검색**을 클릭 합니다. 검색 쿼리 아래에 결과가 표시 됩니다.

4.  장치 손실에 대 한 정책에 따라 적절 한 조치를 취할 것입니다.

    **참고**  디바이스 준수는 배포 된 BitLocker 정책에 따라 결정 됩니다. 장치의 BitLocker 암호화 상태를 확인 하려는 경우 이러한 배포 된 정책을 확인 해야 합니다.

     

## 관련 항목


[MBAM을 사용하여 BitLocker 관리 수행](performing-bitlocker-management-with-mbam.md)

 

 





