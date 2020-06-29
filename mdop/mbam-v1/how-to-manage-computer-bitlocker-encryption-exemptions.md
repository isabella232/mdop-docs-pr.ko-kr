---
title: 컴퓨터 BitLocker 암호화 예외를 관리하는 방법
description: 컴퓨터 BitLocker 암호화 예외를 관리하는 방법
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825678"
---
# 컴퓨터 BitLocker 암호화 예외를 관리하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 사용 하 여 특정 컴퓨터를 BitLocker 보호에서 제외할 수 있습니다. 예를 들어 조직은 컴퓨터 별로 BitLocker 예외를 제어 하도록 결정할 수 있습니다.

BitLocker 암호화에서 컴퓨터를 제외 하려면 컴퓨터 기반 BitLocker 보호 규칙을 무시 하려면 컴퓨터를 ActiveDirectoryDomainServices의 보안 그룹에 추가 해야 합니다.

**참고**  컴퓨터가 이미 BitLocker로 보호 되는 경우 컴퓨터 예외 정책이 적용 되지 않습니다.

 

**BitLocker 암호화에서 컴퓨터를 제외 하려면**

1.  ActiveDirectoryDomainServices의 보안 그룹에 제외 하려는 컴퓨터 계정을 추가 합니다. 이렇게 하면 모든 컴퓨터 기반 BitLocker 보호 규칙을 우회할 수 있습니다.

2.  MBAM 그룹 정책 템플릿을 사용 하 여 그룹 정책 개체를 만든 다음 이전 단계에서 만든 Active Directory 그룹과 그룹 정책 개체를 연결 합니다. 필요한 그룹 정책 개체를 만드는 방법에 대 한 자세한 내용은 [MBAM 1.0 그룹 정책 개체 배포](deploying-mbam-10-group-policy-objects.md)를 참조 하세요.

3.  제외 된 컴퓨터가 시작 되 면 MBAM 클라이언트는 컴퓨터 예외 정책 설정을 확인 하 고 컴퓨터가 BitLocker 예외 보안 그룹에 속해 있는지 여부에 따라 보호를 일시 중단 합니다.

## 관련 항목


[MBAM 1.0 기능 관리](administering-mbam-10-features.md)

 

 





