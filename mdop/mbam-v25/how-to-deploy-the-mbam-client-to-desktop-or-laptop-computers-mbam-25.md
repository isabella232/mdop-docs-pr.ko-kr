---
title: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
description: 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824478"
---
# 데스크톱 또는 노트북 컴퓨터에 MBAM 클라이언트를 배포하는 방법


이 항목에서는 사용자의 컴퓨터에 MBAM 클라이언트를 배포 하는 방법에 대해 설명 합니다. Active Directory 도메인 서비스 또는 MicrosoftSystemCenterConfiguration Manager와 같은 전자 소프트웨어 배포 시스템을 통해 MBAM 클라이언트를 배포할 수 있습니다.

Windows 배포의 일부로 MBAM 클라이언트를 배포 하려면 [Windows 배포의 일부로 MBAM을 사용 하 여 BitLocker를 사용 하도록 설정 하는 방법을](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)참조 하세요.

MBAM 클라이언트 배포를 시작 하기 전에 [mbam에서 지원 되는 구성을](mbam-25-supported-configurations.md)검토 하세요.

**데스크톱 또는 랩톱 컴퓨터에 MBAM 클라이언트 배포**

1.  MBAM 소프트웨어와 함께 제공 되는 MBAM 클라이언트 설치 파일을 찾습니다.

2.  Active Directory 도메인 서비스 또는 MicrosoftSystemCenterConfiguration Manager와 같은 엔터프라이즈 소프트웨어 배포 도구를 사용 하 여 대상 컴퓨터에 Windows Installer 패키지를 배포 합니다.

3.  배포 설정 또는 그룹 정책 설정을 구성 하 여 MBAM 클라이언트 설치 파일을 실행 합니다.

    설치가 완료 되 면 MBAM 클라이언트는 도메인 컨트롤러에서 받은 그룹 정책 설정을 적용 하 여 BitLocker 드라이브 암호화 및 관리 기능을 시작 합니다.

    **중요**  원격 데스크톱 프로토콜 연결이 활성 상태인 경우 MBAM 클라이언트는 BitLocker 드라이브 암호화 작업을 시작 하지 않습니다. 모든 원격 콘솔 연결을 종료 해야 하며 사용자는 BitLocker 드라이브 암호화가 시작 되기 전에 물리적 콘솔 세션에 로그온 해야 합니다.

     


## 관련 항목
[MBAM 2.5 클라이언트 배포](deploying-the-mbam-25-client.md)

[MBAM 2.5 클라이언트 배포 계획](planning-for-mbam-25-client-deployment.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





