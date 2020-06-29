---
title: MED-V 1.0 SP1 업그레이드 검사 목록
description: MED-V 1.0 SP1 업그레이드 검사 목록
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827268"
---
# MED-V 1.0 SP1 업그레이드 검사 목록


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 1.0을 MED-V 1.0 SP1(서비스 Pack1)으로 업그레이드 하려면 클라이언트를 업그레이드 해야 합니다. 서버는 선택적으로 업그레이드할 수 있습니다.

## 서버 업그레이드


**MED-V 1.0 서버를 MED-V 1.0 SP1로 업그레이드 하려면**

1.  * &lt; InstallDir &gt; /Servers/configurationserver* 디렉터리에 있는 다음 파일을 백업 합니다.

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  * &lt; InstallDir &gt; /Servers/ServerSettings.xml* 파일을 백업 합니다.

3.  MED-V 1.0 서버를 제거 합니다.

4.  MED-V 1.0 SP1 서버를 설치 합니다.

5.  백업 파일을 적절 한 디렉터리로 복원 합니다.

6.  MED-V 서버 서비스를 다시 시작 합니다.

**참고**  서버 구성이 기본값에서 변경 된 경우 파일이 다른 위치에 저장 될 수 있습니다.

 

## 클라이언트 업그레이드


Med-v 1.0 클라이언트를 MED-V 1.0 SP1로 업그레이드 하려면 MED-V 1.0 클라이언트에 .msp 파일을 설치 합니다. 클라이언트와 MED-V는 자동으로 업그레이드 됩니다.

 

 





