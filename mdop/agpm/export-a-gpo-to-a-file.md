---
title: 파일로 GPO 내보내기
description: 파일로 GPO 내보내기
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820853"
---
# 파일로 GPO 내보내기


제어 된 GPO (그룹 정책 개체)를 CAB 파일로 내보내 다른 포리스트의 도메인에 복사 하 고 해당 도메인의 AGPM (고급 그룹 정책 관리)으로 GPO를 가져올 수 있습니다. GPO 설정을 새 또는 기존 GPO로 가져오는 방법에 대 한 자세한 내용은 [파일에서 Gpo 가져오기를](import-a-gpo-from-a-file-ed.md)참조 하세요.

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다.이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**GPO를 파일로 내보내기**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  **콘텐츠** 탭에서 **제어** 탭을 클릭 하 여 제어 된 gpo를 표시 합니다.

3.  GPO를 마우스 오른쪽 단추로 클릭 한 다음 **내보내기를**클릭 합니다.

4.  GPO를 내보낼 파일의 파일 이름을 입력 한 다음 **내보내기를**클릭 합니다. 파일이 없는 경우 생성 됩니다. 이미 존재 하는 경우에는 대체 됩니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다. 특히 GPO에 대 한 **콘텐츠 목록**보기, **설정 읽기**, **gpo 내보내기** 사용 권한이 있어야 합니다.

### 추가 참조

-   [테스트 환경 사용](using-a-test-environment.md)

 

 





