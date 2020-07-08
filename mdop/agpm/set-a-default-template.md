---
title: 기본 템플릿 설정
description: 기본 템플릿 설정
author: dansimp
ms.assetid: e0acf980-437f-4357-b237-298aaebe490d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 870c1d4c13049992509f6aa831966736e6ba25ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820228"
---
# 기본 템플릿 설정


편집기로, 새 Gpo (그룹 정책 개체)를 만드는 모든 그룹 정책 관리자가 사용할 수 있는 기본 서식 파일을 지정할 수 있습니다.

**참고**  서식 파일은 편집 가능한 새 Gpo를 만들기 위한 시작 점으로 사용할 수 있는 GPO의 정적 버전입니다.

 

이 절차를 완료 하려면 고급 그룹 정책 관리에서 편집기 또는 AGPM 관리자 (모든 권한) 역할 또는 필요한 권한이 있는 사용자 계정이 필요 합니다. 이 항목의 "추가 고려 사항"에서 세부 정보를 검토 하세요.

**새 Gpo를 만들 때 사용할 기본 서식 파일 설정**

1.  **그룹 정책 관리 콘솔** 트리에서 gpo를 관리 하려는 포리스트와 도메인의 **제어 변경을** 클릭 합니다.

2.  세부 정보 창의 **콘텐츠** 탭에서 **서식 파일** 탭을 클릭 하 여 사용 가능한 서식 파일을 표시 합니다.

3.  기본값으로 설정할 서식 파일을 마우스 오른쪽 단추로 클릭 한 다음 **기본값으로 설정을**클릭 합니다.

4.  **예** 를 클릭 하 여 확인 합니다.

5.  **진행률** 창에 전체 진행률이 완료 됨이 표시 되 면 **닫기를**클릭 합니다. 기본 서식 파일은 파란색 아이콘을 포함 하며, 상태 **는 서식 파일 탭의** **서식 파일 (기본값)** 으로 식별 됩니다.

### 추가 고려 사항

-   이 절차를 수행 하려면 기본적으로 편집기나 AGPM 관리자 (모든 권한) 여야 합니다. 특히, 도메인에 대 한 **목록 콘텐츠** 및 템플릿 사용 권한을 **만들어야** 합니다.

-   서식 파일을 기본값으로 설정 하면 그룹 정책 관리자가 새 Gpo를 만들 때 **새 제어 된 gpo** 대화 상자에서 처음에 선택 된 서식 파일이 됩니다. 그러나 모든 설정을 포함 하지 않는 ** &lt; 빈 gpo &gt; **를 포함 하 여 다른 gpo 템플릿을 선택 하는 옵션을 사용할 수 있습니다.

-   서식 파일의 이름을 바꾸거나 삭제 해도 해당 서식 파일에서 만든 Gpo에는 영향을 주지 않습니다.

-   서식 파일에는 변경할 수 없으므로 기록 내용이 없습니다.

### 추가 참조

-   [템플릿 만들기 및 기본 템플릿 설정](creating-a-template-and-setting-a-default-template.md)

-   [새 제어된 GPO 만들기 요청](request-the-creation-of-a-new-controlled-gpo.md)

 

 





