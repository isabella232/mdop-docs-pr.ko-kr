---
title: 아카이브 경로 수정
description: 아카이브 경로 수정
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820493"
---
# 아카이브 경로 수정


보관 경로는 AGPM 서버에 상대적인 보관 파일의 위치입니다. 보관 경로는 AGPM 서버나 같은 포리스트의 다른 서버에 있는 폴더를 가리킬 수 있습니다.

보관 경로 및 AGPM 서비스 계정은 AGPM 서버를 설치 하는 동안 구성 되며, 나중에 AGPM 서버에서 **프로그램 추가/제거** 를 통해 변경할 수 있습니다.

이 절차를 완료 하려면 Domain Admins 그룹의 구성원이 며 AGPM 서버 (Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터)에 대 한 액세스 권한이 있는 사용자 계정 이어야 합니다.

**보관 경로를 수정 하려면**

1.  Microsoft 고급 그룹 정책 관리-서버가 설치 된 컴퓨터에서 **시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **프로그램 추가/제거**를 클릭 합니다.

2.  **Microsoft 고급 그룹 정책 관리-서버**를 클릭 한 다음 **변경을**클릭 합니다.

3.  **다음**을 클릭 한 다음 **수정을**클릭 합니다.

4.  화면 설명에 따라 AGPM 서비스에 대 한 설정을 구성 합니다.

    1.  보관 경로의 새 보관 위치를 AGPM 서버와 비교 하 여 입력 합니다. 보관 경로는 AGPM 서버 또는 다른 위치에 있는 폴더를 가리킬 수 있지만,이 위치에는이 AGPM 서버에서 관리 하는 모든 Gpo 및 기록 데이터를 저장할 충분 한 공간이 있어야 합니다.

    2.  AGPM 서비스 계정에 대 한 자격 증명을 입력 합니다.

        **중요**  설치를 수정 하면 AGPM 서비스 계정에 대 한 자격 증명이 지워집니다. 자격 증명을 다시 입력 해야 하지만, 원본 설치 중 사용 되는 자격 증명과 일치 하는 경우에는 필요 하지 않습니다.

        AGPM 서비스 계정에는 관리할 Gpo에 대 한 모든 권한이 있어야 합니다. 단일 도메인에서 Gpo를 관리 하는 경우 기본 도메인 컨트롤러에 대 한 로컬 시스템 계정을 AGPM 서비스 계정으로 설정할 수 있습니다.

        여러 도메인의 Gpo를 관리 하는 경우 또는 구성원 서버가 AGPM 서버인 경우 한 도메인 컨트롤러의 로컬 시스템 계정이 다른 도메인의 Gpo에 액세스할 수 없으므로 AGPM 서비스 계정으로 다른 계정을 구성 해야 합니다.

         

    3.  보관 소유자의 경우 AGPM 관리자의 자격 증명 (모든 권한)을 입력 합니다.

5.  **변경을**클릭 하 고 설치가 완료 되 면 **마침을**클릭 합니다.

### 추가 참조

-   [AGPM 서비스 관리](managing-the-agpm-service.md)

 

 





