---
title: MBAM 1.0 GPO 설정을 편집하는 방법
description: MBAM 1.0 GPO 설정을 편집하는 방법
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824283"
---
# MBAM 1.0 GPO 설정을 편집하는 방법


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 성공적으로 배포 하려면 먼저 Microsoft BitLocker 관리 및 모니터링 구현에서 사용할 그룹 정책을 결정 해야 합니다. 사용할 수 있는 다양 한 정책에 대 한 자세한 내용은 [MBAM 1.0 그룹 정책 요구 사항 계획](planning-for-mbam-10-group-policy-requirements.md)을 참조 하세요. 사용할 정책을 결정 한 후에는 MBAM 정책 설정을 포함 하는 하나 이상의 GPO (그룹 정책 개체)를 수정 해야 합니다.

다음 단계에서는 MBAM이 조직의 클라이언트 컴퓨터에 대 한 BitLocker 암호화를 관리할 수 있도록 기본 GPO (권장 그룹 정책 개체) 설정을 구성 하는 방법을 설명 합니다.

**MBAM 클라이언트 GPO 설정을 편집 하려면**

1.  MBAM 그룹 정책 템플릿이 설치 된 컴퓨터에서 MBAM 서비스를 사용할 수 있는지 확인 합니다.

2.  그룹 정책 관리 콘솔 (GPMC) 또는 AGPM (고급 그룹 정책 관리) MDOP 제품을 사용 하 여 다음 작업을 수행 합니다. **컴퓨터 구성**선택, **정책**, **관리 템플릿**, **Windows 구성 요소**를 차례로 선택한 다음 **MDOP mbam (BitLocker Management)** 을 클릭 합니다.

3.  클라이언트 컴퓨터에서 MBAM 클라이언트 서비스를 사용 하도록 설정 하는 데 필요한 그룹 정책 개체 설정을 편집 합니다. 다음 표의 각 정책에 대해 **정책 그룹**을 선택 하 고 **정책을**클릭 한 다음 **설정을**구성 합니다.

    정책 그룹

    정책

    설정

    클라이언트 관리

    MBAM 서비스 구성

    활성화. **Mbam 복구 및 하드웨어 서비스 끝점** 을 설정 하 고 **저장할 BitLocker 복구 정보를 선택**합니다.

    **Mbam 준수 서비스 끝점** 을 설정 하 고 **상태 보고서 빈도를 (분)에 입력**합니다.

    하드웨어 호환성 검사 허용

    사용하지 않도록 설정됩니다. 이 정책은 기본적으로 사용 하도록 설정 되어 있지만 기본 MBAM 구현에는 필요 하지 않습니다.

    운영 체제 드라이브

    운영 체제 드라이브 암호화 설정

    활성화. **운영 체제 드라이브에 대 한 선택 보호 기능을**설정 합니다. 이는 운영 체제 드라이브 데이터를 MBAM 키 복구 서버에 저장 하는 데 필요 합니다.

    이동식 드라이브

    이동식 드라이브에서 BitLocker 사용 제어

    활성화. 이는 MBAM이 이동식 드라이브 데이터를 Mbam 복구 서버에 저장 하는 경우 필요 합니다.

    고정식 드라이브

    고정 드라이브의 BitLocker 사용 제어

    활성화. 이는 MBAM이 고정 드라이브 데이터를 Mbam 복구 서버에 저장 하는 경우에 필요 합니다.

    설정 **BitLocker로 보호 되는 드라이브를 복구 하** 고 **데이터 복구 에이전트를 허용**하는 방법을 선택 합니다.



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## 관련 항목


[MBAM 1.0 그룹 정책 개체 배포](deploying-mbam-10-group-policy-objects.md)









