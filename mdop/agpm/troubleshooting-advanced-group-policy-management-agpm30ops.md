---
title: 고급 그룹 정책 관리 문제 해결
description: 고급 그룹 정책 관리 문제 해결
author: dansimp
ms.assetid: f7ece97c-e9f8-4b18-8c7a-a615c98d5c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4815378a17a7c083501cfd7772e62415ec285237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820178"
---
# 고급 그룹 정책 관리 문제 해결


이 섹션에는 AGPM (고급 그룹 정책 관리)를 사용 하 여 Gpo (그룹 정책 개체)를 관리할 때 발생할 수 있는 일반적인 문제가 나와 있습니다. 여기에 나와 있지 않은 문제를 진단 하려면 AGPM 관리자 (모든 권한)에서 로깅 및 추적을 사용 하는 것이 유용할 수 있습니다. 자세한 내용은 [로깅 및 추적 구성을](configure-logging-and-tracing-agpm30ops.md)참조 하세요.

**참고**  
-   문제가 있는 경우 이전 버전의 GPO로 롤백하는 방법에 대 한 자세한 내용은 [이전 버전의 gpo로 롤백을](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)참조 하세요.

-   백업에서 전체 보관 파일을 복원 하 여 재난 으로부터 복구 하는 방법에 대 한 자세한 내용은 [백업에서 보관 파일 복원을](restore-the-archive-from-a-backup.md)참조 하세요.

 

## 어떤 문제가 있나요?


-   [보관 파일에 액세스할 수 없습니다.](#bkmk-access-an-archive)

-   [GPO 상태는 그룹 정책 관리자에 따라 다릅니다.](#bkmk-state-varies)

-   [AGPM 서버 연결을 수정할 수 없습니다.](#bkmk-modify-archive-location)

-   [기본 서식 파일을 변경 하거나, Gpo를 보거나, 만들거나, 편집 하거나, 이름을 바꾸거나, 배포 하거나, 삭제할 수 없는 경우](#bkmk-perform-task)

-   [특정 GPO 이름을 사용할 수 없습니다.](#bkmk-use-particular-name)

-   [AGPM 전자 메일 알림을 받지 못하는 경우](#bkmk-email)

-   [AGPM 서비스에 대해 포트 4600을 사용할 수 없음](#bkmk-port)

-   [AGPM 서비스가 시작 되지 않습니다.](#bkmk-not-start)

-   [그룹 정책 소프트웨어 설치가 소프트웨어 설치에 실패 함](#bkmk-software-installation)

-   [보관 파일을 새 AGPM 서버로 복원 하는 동안 오류가 발생 했습니다.](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a>보관 파일에 액세스할 수 없습니다.

-   **원인**: 올바른 서버와 아카이브의 포트를 선택 하지 않았습니다.

-   **해결 방법**:

    -   AGPM 관리자 인 경우: [Agpm 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.

    -   AGPM 관리자가 아닌 경우: AGPM 관리자가 AGPM 서버에 대 한 연결 세부 정보를 요청 합니다. [AGPM 서버 연결 구성을](configure-an-agpm-server-connection-reviewer-agpm30ops.md)참조 하세요.

-   **원인**: AGPM 서비스가 실행 되 고 있지 않습니다.

-   **해결 방법**:

    -   AGPM 관리자 인 경우 다음을 수행 합니다. AGPM 서비스를 시작 합니다. 자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm30ops.md)를 참조 하세요.

    -   AGPM 관리자가 아닌 경우: AGPM 관리자에 게 도움을 요청 하세요.

### <a href="" id="bkmk-state-varies"></a>GPO 상태는 그룹 정책 관리자에 따라 다릅니다.

-   **원인**: 다른 그룹 정책 관리자가 동일한 보관에 대해 다른 AGPM 서버를 선택 했습니다.

-   **해결 방법**:

    -   AGPM 관리자 인 경우: [Agpm 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.

    -   AGPM 관리자가 아닌 경우: AGPM 관리자가 AGPM 서버에 대 한 연결 세부 정보를 요청 합니다. [AGPM 서버 연결 구성을](configure-an-agpm-server-connection-reviewer-agpm30ops.md)참조 하세요.

### <a href="" id="bkmk-modify-archive-location"></a>AGPM 서버 연결을 수정할 수 없습니다.

-   **원인**: **agpm 서버** 탭의 설정을 사용할 수 없는 경우 agpm 서버가 관리 템플릿을 사용 하 여 중앙에서 구성 되었습니다.

-   **해결 방법**:

    -   AGPM 관리자 인 경우: **Agpm 서버** 탭의 설정을 사용할 수 없는 경우 [Agpm 서버 연결 구성을](configure-agpm-server-connections-agpm30ops.md)참조 하세요.

    -   AGPM 관리자가 아닌 경우: **Agpm 서버** 탭의 설정을 사용할 수 없는 경우 agpm 서버를 수정할 필요가 없습니다.

### <a href="" id="bkmk-perform-task"></a>기본 서식 파일을 변경 하거나, Gpo를 보거나, 만들거나, 편집 하거나, 이름을 바꾸거나, 배포 하거나, 삭제할 수 없는 경우

-   **원인**: 작업을 수행 하는 데 필요한 권한 역할을 지정 하지 않았습니다.

-   **해결 방법**:

    -   AGPM 관리자 인 경우: [아카이브에 대 한 도메인 수준 액세스 위임](delegate-domain-level-access-to-the-archive-agpm30ops.md) 및 [보관 저장소의 개별 GPO에 대 한 액세스 권한 위임](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md)을 참조 하세요. AGPM 권한은 도메인에서 현재 보관에 있는 모든 Gpo로 종속 됩니다. 작업을 수행할 수 있는 역할과 작업을 수행 하는 데 필요한 사용 권한을 확인 하는 방법에 대 한 자세한 내용은 해당 작업의 도움말을 참조 하세요.

    -   AGPM 관리자가 아닌 경우 추가 역할 또는 권한이 필요한 경우 AGPM 관리자에 게 도움을 요청 하세요. 편집자 인 경우 GPO를 만들거나, GPO를 배포 하거나, 프로덕션 환경에서 GPO를 삭제 하는 프로세스를 시작할 수 있지만 승인자 또는 AGPM 관리자가 요청을 승인 해야 한다는 점에 유의 하세요.

### <a href="" id="bkmk-use-particular-name"></a>특정 GPO 이름을 사용할 수 없습니다.

-   **원인**: gpo 이름이 이미 사용 중이거나 gpo를 나열할 수 있는 권한이 없습니다.

-   **해결 방법**:

    -   GPO 이름이 **제어**됨, **제어**되지 않음 또는 **보류 중** 탭에 표시 되는 경우 다른 이름을 선택 합니다. 배포 된 GPO의 이름은 바뀌었지만 아직 배포 되지 않은 경우 프로덕션 환경의 이전 이름 아래에 표시 됩니다. 따라서 이전 이름은 여전히 사용 중입니다. GPO를 다시 배포 하 여 프로덕션 환경에서 해당 이름을 업데이트 하 고 다른 GPO에서 사용할 수 있도록 해당 이름을 해제 합니다.

    -   **제어** **, 제어**되지 않음 또는 **보류 중** 탭에 gpo 이름이 표시 되지 않으면 gpo를 나열할 권한이 부족할 수 있습니다. 권한을 요청 하려면 AGPM 관리자에 게 문의 하세요.

### <a href="" id="bkmk-email"></a>AGPM 전자 메일 알림을 받지 못하는 경우

-   **원인**: 올바른 SMTP 전자 메일 서버 및 전자 메일 주소가 제공 되지 않았거나 전자 메일 알림을 생성 하는 작업이 수행 되지 않았습니다.

-   **해결 방법**:

    -   AGPM 관리자 인 경우: agpm에서 보낼 보류 중인 작업에 대 한 전자 메일 알림을 보려면 AGPM 관리자가 **도메인 위임** 탭에서 승인자를 위한 올바른 SMTP 전자 메일 서버와 전자 메일 주소를 제공 해야 합니다. 자세한 내용은 [전자 메일 알림 구성을](configure-e-mail-notification-agpm30ops.md)참조 하세요.

    -   전자 메일 알림은 해당 GPO를 만들거나, 배포 하거나, 삭제 하는 데 필요한 권한이 없는 편집기, 검토자 또는 다른 그룹 정책 관리자가 이러한 작업 중 하나에 대 한 요청을 제출 하는 경우에만 생성 됩니다. 요청 승인 또는 거부에 대 한 자동 알림은 없습니다.

### <a href="" id="bkmk-port"></a>AGPM 서비스에 대해 포트 4600을 사용할 수 없음

-   **원인**: AGPM 서비스가 수신 대기 하는 포트는 기본적으로 포트 4600입니다.

-   **해결 방법**: agpm 서비스에 대해 포트 4600을 사용할 수 없는 경우, 다른 포트를 사용 하도록 agpm 서버의 포트 구성을 수정한 다음 agpm 클라이언트에 대 한 agpm 서버 연결의 포트를 업데이트 합니다. 자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm30ops.md)참조 하세요.

### <a href="" id="bkmk-not-start"></a>AGPM 서비스가 시작 되지 않습니다.

-   **원인**: 운영 체제의 **관리 도구** 및 **서비스**에서 AGPM 서비스에 대 한 설정을 수정 했습니다.

-   **해결**방법: 제어판의 **프로그램 및 기능** 에서 **Microsoft 고급 그룹 정책 관리 서버** 에 대 한 설정을 수정 합니다. 자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm30ops.md)참조 하세요.

### <a href="" id="bkmk-software-installation"></a>그룹 정책 소프트웨어 설치가 소프트웨어 설치에 실패 함

-   **원인**: AGPM은 그룹 정책 소프트웨어 설치 패키지의 무결성을 유지 합니다. Gpo가 오프 라인으로 편집 되기는 하지만 캐시 된 클라이언트 정보 외에 패키지 간 링크도 유지 됩니다. 이것은 의도적입니다.

-   **해결 방법**: AGPM을 사용 하 여 오프 라인으로 GPO를 편집 하는 경우 다른 gpo의 패키지에 대 한 그룹 정책 소프트웨어 설치 업그레이드를 구성 하 여 체크 아웃 된 복사본이 아닌 배포 된 gpo를 참조 합니다. 편집기에는 배포 된 GPO에 대 한 **읽기** 권한이 있어야 합니다.

### <a href="" id="bkmk-error-on-restore"></a>보관 파일을 새 AGPM 서버로 복원 하는 동안 오류가 발생 했습니다.

-   **원인**: 보안 상의 이유로 **도메인 위임** 탭에 입력 한 암호를 보호 하면 보관 파일이 다른 컴퓨터로 이동 하는 경우 암호에 오류가 발생 합니다.

-   **해결**방법: **도메인 위임** 탭에서 암호를 다시 입력 하 고 확인 합니다. 자세한 내용은 [전자 메일 알림 구성을](configure-e-mail-notification-agpm30ops.md)참조 하세요.

 

 





