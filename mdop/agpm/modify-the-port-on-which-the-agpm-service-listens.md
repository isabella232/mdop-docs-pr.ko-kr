---
title: AGPM 서비스를 수신할 포트 수정
description: AGPM 서비스를 수신할 포트 수정
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820488"
---
# AGPM 서비스를 수신할 포트 수정


AGPM 서비스는 보관 및 프로덕션 환경의 Gpo (그룹 정책 개체)에 대 한 클라이언트 액세스를 관리 하는 보안 프록시 역할을 하는 Windows 서비스입니다. 기본적으로 AGPM 서비스는 포트 4600에서 수신 대기 합니다. 각 아카이브의 용 AGPM (고급 그룹 정책 관리) 보관 인덱스 파일을 수정 하 여이 포트를 변경할 수 있습니다.

**참고**  AGPM 서비스가 수신 대기 하는 포트를 수정 하기 전에, AGPM 보관 인덱스 파일 (gpostate.xml)을 백업 하는 것이 좋습니다. 이 파일은 고급 그룹 정책 관리-서버를 설치 하는 동안 보관 경로로 입력 된 폴더에 있습니다. 기본적으로이 파일의이 위치는 AGPM 서버의% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml입니다. 보관 파일을 호스트 하는 컴퓨터를 모르는 경우 보관 경로를 수정 하는 절차에 따라 현재 보관 경로를 표시할 수 있습니다. 자세한 내용은 [보관 경로 수정을](modify-the-archive-path.md)참조 하세요.

 

이 절차를 완료 하려면 AGPM 서버 (AGPM 서비스가 설치 되어 있는 컴퓨터)에 대 한 액세스 권한이 있는 사용자 계정이 고 보관 인덱스 파일을 사용 해야 합니다.

**AGPM 서비스가 수신 대기 하는 포트를 수정 하려면**

1.  보관 파일을 호스트 하는 컴퓨터에서 텍스트 편집기에 보관 인덱스 파일 (gpostate.xml)을 엽니다.

2.  파일에서 **agpm: port = "4600"** 를 검색 합니다.

3.  **4600** 를 AGPM 서비스가 수신 대기할 포트로 바꿉니다. 그런 다음 파일을 저장 하 고 닫습니다.

4.  AGPM 서버에서 AGPM 서비스를 다시 시작 합니다. (자세한 내용은 [AGPM 서비스 시작 및 중지](start-and-stop-the-agpm-service.md)를 참조 하세요.)

5.  각 그룹 정책 관리자에 대해 AGPM 서버 연결의 포트를 수정 합니다. (자세한 내용은 [AGPM 서버 연결 구성을](configure-the-agpm-server-connection.md)참조 하세요.)

6.  각 보관 및 AGPM 서버에 대해 반복 합니다.

### 추가 참조

-   [AGPM 서비스 관리](managing-the-agpm-service.md)

 

 





