---
title: AGPM 관리자 작업 수행
description: AGPM 관리자 작업 수행
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820478"
---
# AGPM 관리자 작업 수행


AGPM 관리자 (모든 권한)는 도메인 전체 옵션을 구성 하 고 승인자, 편집자, 검토자 및 기타 AGPM 관리자에 게 권한을 위임 합니다. 기본적으로 AGPM 관리자는 모든 권한이 있는 개인 (모든 고급 그룹 정책 관리 \ [AGPM \] 권한) 이므로 역할에 연결 된 작업을 수행할 수도 있습니다.

여러 사용자가 Gpo (그룹 정책 개체)를 개발 하는 환경에서 모든 AGPM (고급 그룹 정책 관리) 사용자가 동일한 작업을 수행 하 고 동일한 수준의 액세스를가지고 있는지, 아니면 AGPM 관리자가 Gpo를 변경 하는 편집자와 프로덕션 환경에 Gpo를 배포 하는 승인자에 게 권한을 위임할 것인지 여부를 선택할 수 있습니다. AGPM 관리자는 조직의 요구에 맞게 사용 권한을 구성할 수 있습니다.

-   [AGPM 서버 연결 구성](configure-the-agpm-server-connection.md)

-   [전자 메일 알림 구성](configure-e-mail-notification.md)

-   [도메인 수준 액세스 권한 위임](delegate-domain-level-access.md)

-   [개별 GPO에 대한 액세스 권한 위임](delegate-access-to-an-individual-gpo.md)

-   [로깅 및 추적 구성](configure-logging-and-tracing.md)

-   [AGPM 서비스 관리](managing-the-agpm-service.md)

    -   [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service.md)

    -   [아카이브 경로 수정](modify-the-archive-path.md)

    -   [AGPM 서비스 계정 수정](modify-the-agpm-service-account.md)

    -   [AGPM 서비스를 수신할 포트 수정](modify-the-port-on-which-the-agpm-service-listens.md)

또한 AGPM 관리자 역할에 다른 모든 역할에 대 한 사용 권한이 포함 되기 때문에 AGPM 관리자가 다른 역할과 일반적으로 연결 되는 작업을 수행할 수 있습니다.

-   Gpo 만들기, 배포 또는 삭제와 같은 [승인자 작업 수행](performing-approver-tasks.md)

-   편집, 이름 바꾸기, 레이블 지정, Gpo 가져오기, 서식 파일 만들기 또는 기본 서식 파일 설정 등의 [편집자 작업 수행](performing-editor-tasks.md)

-   설정 검토 및 Gpo 비교와 같은 [검토자 작업 수행](performing-reviewer-tasks.md)

### 추가 고려 사항

기본적으로 AGPM 관리자 역할에는 모든 권한, 즉 모든 AGPM 권한이 있습니다.

-   콘텐츠 나열

-   설정 읽기

-   설정 편집

-   GPO 만들기

-   GPO 배포

-   GPO 삭제

-   옵션 수정

-   보안 수정

-   서식 파일 만들기

**수정 옵션** 및 **보안 수정** 권한은 AGPM 관리자의 역할에 고유 합니다.

 

 





