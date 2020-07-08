---
title: 연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법
description: 연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817818"
---
# 연결이 끊긴 작업 모드에 대한 클라이언트를 구성하는 방법


연결이 끊긴 작업 모드는 응용 프로그램 가상화 (App-v) 데스크톱 클라이언트 또는 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 Application Virtualization (App-v) 클라이언트를 사용 하 여 클라이언트가 App-v 관리 서버에 연결할 수 없는 경우 클라이언트의 파일 시스템 캐시에 저장 된 응용 프로그램을 실행 합니다.

**중요**  여러 사용자를 지원 하기 위해 RD ° (원격 데스크톱 세션 호스트) 서버 (이전의 터미널 서버)가 팜에 연결 된 대규모 조직의 경우 단일 App-v 관리 서버를 사용 하 여 팜 지원의 단일 지점 실패를 나타냅니다. RDSession Host 팜을 지원 하기 위해 고가용성을 제공 하려면 두 개 이상의 App-v 관리 서버를 연결 하 여 동일한 데이터베이스를 사용 하는 것이 좋습니다.

 

**연결이 끊긴 작업 모드를 사용 하도록 설정 하려면**

-   연결 되지 않은 작동 모드를 사용 하도록 다음 레지스트리 키 값을 1로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

**연결이 끊긴 작업 모드 사용에 시간 제한을 설정 하려면**

1.  다음 레지스트리 키 값을 1로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

2.  다음 레지스트리 키 값을 연결이 끊긴 작업 모드를 제한 하는 데 사용할 시간 (분)으로 설정 합니다. 유효한 값의 범위는 1 – 999999입니다. 기본값은 90 일 또는 129600 분입니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes

**연결이 끊긴 작업 모드에 대해 원격 데스크톱 서비스에 맞게 클라이언트를 구성 하려면**

1.  연결 되지 않은 작동 모드를 사용 하도록 다음 레지스트리 키 값을 1로 설정 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

2.  다음 레지스트리 키 값을 0 (영)으로 설정 하 여 연결이 끊긴 작업 모드의 무제한 사용을 허용 합니다.

    HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

3.  성능을 개선 하기 위해 모든 패키지가 캐시에 미리 로드 되었는지 확인 합니다.

## 관련 항목


[연결이 끊긴 작업 모드](disconnected-operation-mode.md)

[명령줄을 사용하여 App-V Client 레지스트리 설정을 구성하는 방법](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





