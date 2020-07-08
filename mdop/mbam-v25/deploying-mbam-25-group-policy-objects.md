---
title: MBAM 2.5 그룹 정책 개체 배포
description: MBAM 2.5 그룹 정책 개체 배포
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824388"
---
# MBAM 2.5 그룹 정책 개체 배포


MBAM을 배포 하려면 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 하는 그룹 정책 설정을 설정 해야 합니다. 이 작업을 완료 하려면 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)를 실행할 수 있는 서버 또는 워크스테이션에 MBAM 그룹 정책 템플릿을 복사한 다음 설정을 편집 해야 합니다.

**중요**  **BitLocker 드라이브 암호화** 노드에서 그룹 정책 설정을 변경 하지 마세요 또는 mbam이 제대로 작동 하지 않습니다. **MDOP mbam (BitLocker Management)** 노드에서 그룹 정책 설정을 구성 하면 mbam이 자동으로 **bitlocker 드라이브 암호화** 설정을 구성 합니다.

 

## MBAM 2.5 그룹 정책 템플릿 복사


MBAM 클라이언트를 설치 하기 전에, 관리 워크스테이션에 MBAM Gpo (그룹 정책 개체)를 복사 해야 합니다. 이러한 Gpo는 BitLocker 드라이브 암호화에 대 한 MBAM 구현 설정을 정의 합니다. 그룹 정책 템플릿을 지원 되는 Windows server 또는 클라이언트 컴퓨터인 모든 서버 또는 워크스테이션에 복사 하 여 GPMC (그룹 정책 관리 콘솔) 또는 AGPM (고급 그룹 정책 관리)을 실행할 수 있습니다.

[MBAM 2.5 그룹 정책 템플릿 복사](copying-the-mbam-25-group-policy-templates.md)

## MBAM 2.0 GPO 설정 편집


필요한 Gpo를 만든 후에는 조직의 클라이언트 컴퓨터에 MBAM 그룹 정책 설정을 배포 해야 합니다. Gpo를 보고 만들려면 GPMC (그룹 정책 관리) 콘솔 또는 AGPM (고급 그룹 정책 관리)이 설치 되어 있어야 합니다.

[MBAM 2.5 그룹 정책 설정 편집](editing-the-mbam-25-group-policy-settings.md)

## Windows 제어판에서 MBAM 제어판 표시 또는 숨기기


MBAM은 기본 Windows BitLocker 제어판을 바꿀 수 있는 사용자 지정 된 MBAM 제어판을 제공 하므로 그룹 정책 설정을 사용 하 여 최종 사용자의 기본 BitLocker 제어판을 표시 하거나 숨길 수도 있습니다.

[제어판에서 기본 BitLocker 드라이브 암호화 항목 숨기기](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## MBAM 2.0 그룹 정책 개체 배포에 대 한 기타 리소스


[MBAM 2.5 배포](deploying-mbam-25.md)

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.

 

 





