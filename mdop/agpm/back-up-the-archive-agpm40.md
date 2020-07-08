---
title: 아카이브 백업
description: 아카이브 백업
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819213"
---
# 아카이브 백업


AGPM (고급 그룹 정책 관리)의 보관을 복구 하는 데 도움이 되도록 재해가 발생 한 경우 AGPM 관리자 (모든 권한)가 보관을 자주 백업 해야 합니다. 기본적으로 보관 파일 은%ProgramData%\\Microsoft\\AGPM.에 만들어집니다. 그러나 Microsoft 고급 그룹 정책 관리-서버를 설정 하는 동안 다른 경로를 지정할 수 있습니다.

이 절차를 완료 하려면 agpm 서비스를 설치 하는 컴퓨터를 비롯 하 여 사용자 계정에 대 한 액세스 권한이 있고 보관 파일이 들어 있는 폴더를 사용 해야 합니다.

**보관 저장소를 백업 하려면**

1.  AGPM 서비스를 중지 합니다. 자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm40.md)를 참조 하세요.

2.  Windows 탐색기, Xcopy, Windows Server® 백업 또는 다른 백업 도구를 사용 하 여 보관 폴더를 백업 합니다. 숨겨진, 시스템, 읽기 전용 파일을 백업 해야 합니다.

3.  보관 백업을 안전한 위치에 저장 합니다.

4.  AGPM 서비스를 다시 시작 합니다. 자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm40.md)를 참조 하세요.

**참고**  AGPM 관리자가 보관 저장소를 자주 백업 하지 않으면 보관 백업에 있는 Gpo (그룹 정책 개체)가 최신 상태가 되지 않습니다. 보관 백업이 최신 상태 인지 확인 하려면 조직의 일일 백업 전략의 일부로 아카이브를 백업 합니다.

 

### 추가 참조

-   [백업에서 아카이브 복원](restore-the-archive-from-a-backup-agpm40.md)

-   [AGPM 서버 및 아카이브 이동](move-the-agpm-server-and-the-archive-agpm40.md)

-   [아카이브 관리](managing-the-archive-agpm40.md)

 

 





