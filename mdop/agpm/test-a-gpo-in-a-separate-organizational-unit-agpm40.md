---
title: 별도 조직 구성 단위에서 GPO 테스트
description: 별도 조직 구성 단위에서 GPO 테스트
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818258"
---
# 별도 조직 구성 단위에서 GPO 테스트


프로덕션 환경에 배포 하기 전에 OU (조직 구성 단위)를 사용 하 여 동일한 도메인 내에서 Gpo (그룹 정책 개체)를 테스트 하는 경우 테스트 OU에 액세스 하는 데 필요한 권한이 있어야 합니다. 테스트 OU를 사용 하는 것은 선택 사항입니다.

**테스트 OU를 사용 하려면**

1.  편집할 GPO를 체크 아웃 했지만 **그룹 정책 관리 콘솔**에서 gpo를 관리 하는 포리스트와 도메인의 **그룹 정책 개체** 를 클릭 합니다.

2.  테스트할 GPO의 체크 아웃 된 복사본을 클릭 합니다. 이름은 **\ [AGPM \]이 (가)** 앞에 옵니다. (나열 되지 않은 경우 **작업**을 클릭 한 다음 **새로 고침**). 이름을 알파벳순으로 정렬 하면 **\ [AGPM \]** gpo가 일반적으로 목록 맨 위에 표시 됩니다.

3.  GPO를 테스트 OU로 끌어 옵니다.

4.  테스트 OU에서 GPO에 대 한 링크를 만들지 여부를 묻는 대화 상자에서 **확인** 을 클릭 합니다.

### 추가 고려 사항

-   테스트가 완료 되 면 GPO를 체크 인하면 GPO의 체크 아웃 된 복사본에 대 한 링크가 자동으로 삭제 됩니다.

### 추가 참조

-   [테스트 환경 사용](using-a-test-environment.md)

 

 





