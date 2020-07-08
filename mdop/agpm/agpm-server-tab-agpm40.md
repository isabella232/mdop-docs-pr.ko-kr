---
title: AGPM 서버 탭
description: AGPM 서버 탭
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819283"
---
# AGPM 서버 탭


**변경 컨트롤** 창의 **agpm server** 탭에서 정규화 된 컴퓨터 이름 및 포트를 입력 하 여 agpm 서버를 선택 하 고 보관 저장소에서 이전 버전의 Gpo (그룹 정책 개체)를 삭제 하 여 agpm 서버의 디스크 공간을 절약할 수 있습니다.

## AGPM 서버 지정


AGPM 서버를 선택 하면 **콘텐츠** 탭에서 사용자에 게 표시 되는 보관 파일과 **도메인 위임** 설정이 적용 되는 위치를 결정할 수 있습니다. AGPM (고급 그룹 정책 관리)의 기본 포트는 포트 4600입니다.

AGPM 서버 연결이 관리 템플릿 설정을 사용 하 여 중앙에서 구성 되는 경우이 탭에서 연결을 구성 하기 위한 옵션을 사용할 수 없습니다. 자세한 내용은 [AGPM 서버 연결 구성을](configure-agpm-server-connections-agpm40.md)참조 하세요.

## 이전 GPO 버전 삭제


기본적으로 모든 제어 된 GPO의 모든 버전이 보관 저장소에 보존 됩니다. 그러나 각 GPO에 대해 보존 되는 버전 수를 제한 하도록 AGPM 서비스를 구성 하 고 해당 제한이 초과 되는 경우 가장 오래 된 버전을 자동으로 삭제할 수 있습니다. **기록** 창의 **고유 버전** 탭에 표시 되는 GPO 버전만이 제한에 따라 계산 됩니다.

**참고**  각 GPO에 대해 저장할 고유 버전의 최대 수에는 현재 버전이 포함 되지 않으므로 0을 입력 하면 현재 버전만 유지 됩니다. 제한은 999 버전 보다 크지 않아야 합니다.

GPO 버전이 삭제 되 면 해당 버전의 기록은 GPO의 기록에 남아 있지만 GPO 버전 자체는 보관 저장소에서 삭제 됩니다. 삭제할 수 없는 것으로 표시 하 여 GPO 버전이 삭제 되는 것을 방지 합니다.

 

### 추가 참조

-   [사용자 인터페이스: 고급 그룹 정책 관리](user-interface-advanced-group-policy-management-agpm40.md)

-   [AGPM 관리자 작업 수행](performing-agpm-administrator-tasks-agpm40.md)

-   [검토자 작업 수행](performing-reviewer-tasks-agpm40.md)

 

 





