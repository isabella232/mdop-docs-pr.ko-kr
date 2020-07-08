---
title: AGPM 관리자 작업 수행
description: AGPM 관리자 작업 수행
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822418"
---
# AGPM 관리자 작업 수행


AGPM (고급 그룹 정책 관리)은 AGPM 관리자 (모든 권한)가 승인자, 편집자, 검토자, AGPM 관리자에 게 권한을 위임 하 고 도메인 전체 옵션을 구성할 수 있도록 합니다. 기본적으로 AGPM 관리자는 모든 권한이 있는 사용자 (모든 AGPM 권한)와 모든 역할에 연결 된 작업을 수행할 수 있는 사람을 말합니다.

여러 사용자가 Gpo (그룹 정책 개체)를 개발 하는 환경에서 모든 그룹 정책 관리자가 동일한 작업을 수행 하 고 동일한 수준의 액세스를 사용 하도록 선택할 수 있습니다. 또는 AGPM 관리자가 Gpo를 변경할 수 있는 편집자 및 프로덕션 환경에 Gpo를 배포 하는 승인자에 게 권한을 위임할 수 있도록 선택할 수도 있습니다. AGPM 관리자는 조직의 요구에 맞게 사용 권한을 구성할 수 있습니다.

-   [고급 그룹 정책 관리 구성](configuring-advanced-group-policy-management-agpm40.md): AGPM 서버 연결 및 전자 메일 알림을 구성 하 고, 프로덕션 환경의 gpo에 대 한 액세스를 위임 하 고, 문제 해결을 위해 로깅 및 추적을 구성 합니다.

-   [보관 파일 관리](managing-the-archive-agpm40.md): 보관 저장소의 gpo에 대 한 액세스를 위임 하 고, 각 gpo의 버전 수를 제한 하 고, 다른 도메인에서 gpo를 가져오고, 보관 저장소를 백업 및 복원 합니다.

-   [Agpm 서비스 관리](managing-the-agpm-service-agpm40.md): agpm 서비스를 중지 하 고 시작 하거나 보관 경로, Agpm 서비스 계정 또는 agpm 서비스가 수신 대기 하는 포트를 변경 합니다.

-   [Agpm 서버와 보관 파일 이동](move-the-agpm-server-and-the-archive-agpm40.md): agpm 서비스, 보관 또는 둘 다를 다른 서버로 이동 합니다.

**참고**  AGPM 관리자 역할에는 다른 모든 역할에 대 한 사용 권한이 포함 되므로 AGPM 관리자가 다른 역할과 일반적으로 연결 되는 작업을 수행할 수 있습니다.

Gpo 만들기, 배포 또는 삭제와 같은 [승인자 작업 수행](performing-approver-tasks-agpm40.md)

편집, 이름 바꾸기, 레이블 지정, Gpo 가져오기, 서식 파일 만들기 또는 기본 서식 파일 설정 등의 [편집자 작업 수행](performing-editor-tasks-agpm40.md)

설정 검토 및 Gpo 비교와 같은 [검토자 작업 수행](performing-reviewer-tasks-agpm40.md)

 

### 추가 고려 사항

기본적으로 AGPM 관리자 역할에는 모든 권한, 즉 모든 AGPM 권한이 있습니다.

-   콘텐츠 나열

-   설정 읽기

-   설정 편집

-   GPO 만들기

-   GPO 배포

-   GPO 삭제

-   GPO 내보내기

-   GPO 가져오기

-   서식 파일 만들기

-   옵션 수정

-   보안 수정

**수정 옵션** 및 **보안 수정** 권한은 AGPM 관리자의 역할에 고유 합니다.

 

 





