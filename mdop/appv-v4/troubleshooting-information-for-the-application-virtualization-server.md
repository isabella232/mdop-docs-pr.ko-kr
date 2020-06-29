---
title: Application Virtualization Server 문제 해결 정보
description: Application Virtualization Server 문제 해결 정보
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815188"
---
# Application Virtualization Server 문제 해결 정보


이 항목에는 Application Virtualization (App-v) 서버에 대 한 다양 한 문제를 해결 하는 데 사용할 수 있는 정보가 포함 되어 있습니다.

## 서버 설치 후 설정 로그의 경고 메시지 25017


설치 후 서버 설치 로그에 다음 메시지가 표시 될 수 있습니다.

*경고 25017. 설치 프로그램이 서버에 대 한 Active Directory marker 개체를 만들 수 없습니다. 설치 하는 데 사용 된 계정에 Active Directory 또는 Active Directory에 대 한 쓰기 권한이 없습니다.*

앱-V 관리 또는 스트리밍 서버 설치 관리자는 설치 관리자를 실행 하는 데 사용 되는 계정에 적절 한 권한이 있는 경우 서버가 설치 된 컴퓨터에 해당 하는 Active Directory 도메인 서비스 (추가)의 컴퓨터 개체 아래에 서비스 연결 지점의 항목을 만듭니다. 이 항목을 만들지 않으면 설치에 실패 하는 것이 아니므로 제품이 작동 하는 데는 영향을 주지 않습니다. 설치를 실행 하는 데 사용 되는 사용자 계정에 추가에 대 한 쓰기 권한이 충분 하지 않은 경우 오류가 발생할 수 있습니다. ADDS에 App-v server를 등록 하는 것은 선택 사항 이지만,이를 위해 중앙 집중화 된 관리 도구를 사용 하 여 재고 및 관리 목적에 맞게 App-v 서버를 찾을 수 있는 한 가지 이점이 있습니다.

## 관련 항목


[Application Virtualization Server](application-virtualization-server.md)

 

 





