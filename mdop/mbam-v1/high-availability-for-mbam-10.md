---
title: MBAM 1.0에 대한 고가용성
description: MBAM 1.0에 대한 고가용성
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825363"
---
# MBAM 1.0에 대한 고가용성


이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM)의 고가용성 설치를 구성 하는 방법에 대해 설명 합니다.

## MBAM에 대 한 고가용성 시나리오


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 결함을 허용 하도록 설계 되었습니다. 서버를 사용할 수 없게 되 면 사용자는 부정적인 영향을 받지 않습니다. 예를 들어 MBAM 에이전트를 MBAM 웹 서버에 연결할 수 없는 경우 사용자에 게 작업을 묻는 메시지가 표시 되지 않아야 합니다.

MBAM 설치를 계획 하는 경우 MBAM 서비스의 사용 가능성에 영향을 줄 수 있는 다음 관심사를 고려 하세요.

-   드라이브 암호화 및 복구 암호-복구 암호를 escrowed 수 없는 경우 클라이언트 컴퓨터에서 암호화가 시작 되지 않습니다.

-   준수 상태 데이터 업로드 – 준수 상태 보고서 서비스를 호스팅하는 서버를 사용할 수 없는 경우 준수 데이터는 현재 상태로 유지 되지 않습니다.

-   지원 센터 복구 키 액세스-지원 센터에서 MBAM 데이터베이스 정보에 액세스할 수 없는 경우에는 사용자에 게 복구 키를 제공할 수 없습니다.

-   보고서의 가용성 – 준수 및 감사 보고서를 호스팅하는 서버를 사용할 수 없는 경우 보고서를 사용할 수 없습니다.

MBAM의 고가용성에 대 한 주요 관심사는 BitLocker 키 복구 가용성입니다. 지원 센터에서 복구 키를 제공할 수 없는 경우 잠긴 사용자는 컴퓨터의 잠금을 해제할 수 없습니다. 이 문제를 방지 하려면 고가용성을 보장 하기 위해 중복 웹 서버 및 데이터베이스를 구현 하는 것이 좋습니다.

MBAM 확장성 및 고가용성에 대 한 자세한 내용은 [Mbam 확장성 백서](https://go.microsoft.com/fwlink/p/?LinkId=229025) ()를 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=229025) .

Microsoft SQL Server의 고가용성에 대 한 일반적인 지침은 [고가용성 (()을 참조](https://go.microsoft.com/fwlink/p/?LinkId=221504) 하세요 https://go.microsoft.com/fwlink/p/?LinkId=221504) .

웹 서버의 가용성 및 확장성에 대 한 일반적인 지침은 [가용성 및 확장성](https://go.microsoft.com/fwlink/p/?LinkId=221503) (()을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=221503) .

## 관련 항목


[MBAM 1.0 유지 관리](maintaining-mbam-10.md)

 

 





