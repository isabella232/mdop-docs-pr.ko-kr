---
title: 백업에서 아카이브 복원
description: 백업에서 아카이브 복원
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818398"
---
# 백업에서 아카이브 복원


재해가 발생 하 고 AGPM (고급 그룹 정책 관리)에 대 한 보관 파일이 손상 되거나 제거 되는 경우 AGPM 관리자 (모든 권한)가 미리 준비 된 백업 복사본에서 보관을 복원한 다음 보관 저장소에 없는 Gpo (그룹 정책 개체)에 속한 도메인의 프로덕션 환경에서 가져오기 또는 프로덕션의 버전이 아카이브에 대 한 최신 버전 인지 여부를 확인할 수 있습니다. 보관 백업을 다른 서버로 복원 하는 방법에 대 한 자세한 내용은 [AGPM 서버 및 보관 파일 이동을](move-the-agpm-server-and-the-archive-agpm40.md)참조 하세요.

이 절차를 완료 하려면 AGPM 서버 (AGPM 서비스가 설치 되어 있는 컴퓨터)와 보관 파일이 포함 된 폴더에 액세스할 수 있는 사용자 계정이 필요 합니다.

**백업에서 보관 파일을 복원 하려면**

1.  AGPM 서비스를 중지 합니다. 자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm40.md)를 참조 하세요.

2.  기존 아카이브를 제거 합니다. 기본적으로 보관 폴더 는%ProgramData%\\Microsoft\\AGPM, Microsoft 고급 그룹 정책 관리를 설치한 AGPM 관리자가 설치 중에 다른 위치를 입력 했을 수 있습니다.

3.  보관 경로, AGPM 서비스 계정, 보관 소유자, 수신 대기 포트를 구성 하 여 보관 폴더를 다시 만듭니다. 원래 설치 중에 사용 되는 것과 동일한 값을 사용 하는 것은 필요 하지 않습니다. 자세한 내용은 [AGPM 서비스 수정을](modify-the-agpm-service-agpm40.md)참조 하세요.

4.  보관 백업 내용을 보관 폴더에 복사 하 여 하위 폴더와 파일을 복사 하 여 각 하위 폴더와 파일이 보관 폴더의 사용 권한을 상속 하는지 확인 합니다. 보관 폴더를 덮어쓰지 않도록 주의 하세요.

5.  보관 백업의 GPO가 프로덕션의 해당 GPO 복사본 보다 최신 인지 확실 하지 않은 경우 차이점 보고서를 생성 하 고 해당 설정을 비교 합니다. 자세한 내용은 [gpo, Gpo 버전 또는 템플릿 간의 차이점 확인](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md)을 참조 하세요.

6.  AGPM 서비스를 다시 시작 합니다. 자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service-agpm40.md)를 참조 하세요.

### 추가 참조

-   [아카이브 백업](back-up-the-archive-agpm40.md)

-   [AGPM 서버 및 아카이브 이동](move-the-agpm-server-and-the-archive-agpm40.md)

-   [아카이브 관리](managing-the-archive-agpm40.md)

 

 





