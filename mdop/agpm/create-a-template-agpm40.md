---
title: 템플릿 만들기
description: 템플릿 만들기
author: dansimp
ms.assetid: b38423af-7d24-437a-98bc-01f1ae891127
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd50dd41863e383b931b8563854a8bbd4ee196d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821073"
---
# 템플릿 만들기


서식 파일을 만들면 새 Gpo를 만들기 위한 출발점으로 사용할 특정 버전의 GPO (그룹 정책 개체)에 대 한 모든 설정을 저장할 수 있습니다.

**참고**  서식 파일은 편집 가능한 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.

 

이 절차를 완료 하려면 AGPM (고급 그룹 정책 관리)에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**기존 GPO를 기반으로 서식 파일을 만들려면**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **내용** 탭에서 **제어** **또는 제어** 되지 않음 탭을 클릭 하 여 사용 가능한 gpo를 표시 합니다.

3.  서식 파일을 만들려는 GPO를 마우스 오른쪽 단추로 클릭 한 다음 **서식 파일로 저장**을 클릭 합니다.

4.  서식 파일과 메모의 이름을 입력 한 다음 **확인**을 클릭 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. **서식** 파일 탭에 새 서식 파일이 표시 됩니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다. 특히, 도메인에 대 한 **목록 콘텐츠** 및 템플릿 사용 권한을 **만들어야** 합니다.

-   서식 파일의 이름을 바꾸거나 삭제 해도 해당 서식 파일에서 만든 Gpo에는 영향을 주지 않습니다.

-   서식 파일에는 변경할 수 없으므로 기록 내용이 없습니다.

### 추가 참조

-   [템플릿 만들기 및 기본 템플릿 설정](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [새 제어된 GPO 만들기 요청](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





