---
title: 설치 필수 구성 요소 구성
description: 설치 필수 구성 요소 구성
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819308"
---
# 설치 필수 구성 요소 구성


다음 지침에는 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 설치 및 사용에 대 한 전제 조건이 나와 있습니다.

[Windows 가상 PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Windows 가상 PC 업데이트](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[바이러스 백신/백업 소프트웨어 구성](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Windows 가상 PC를 설치 하 고 구성 하는 방법


**중요**  Windows 용 Virtual PC 버전이 호스트 컴퓨터에 이미 있는 경우 Windows 가상 PC를 설치 하기 전에 해당 버전을 제거 해야 합니다.

 

**Windows 가상 PC를 설치 하려면**

1.  Microsoft 다운로드 센터 ()에서 [Windows 가상 PC](https://go.microsoft.com/fwlink/?LinkId=195918) 를 다운로드 https://go.microsoft.com/fwlink/?LinkId=195918) 합니다.

2.  호스트 컴퓨터에서 설치 파일을 실행 하 고 마법사의 단계를 따릅니다.

**중요**  Windows 가상 PC에는 가상 환경과 물리적 컴퓨터 간의 상호 작용을 개선 하는 기능을 제공 하는 통합 구성 요소 패키지가 포함 되어 있습니다. 예를 들어 마우스를 호스트와 게스트 컴퓨터 간에 이동할 수 있습니다. MED-V는 통합 구성 요소 패키지를 설치 해야 합니다.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Windows 가상 PC 업데이트를 설치 하 고 구성 하는 방법


문서 KB977206에 연결 된 Microsoft 업데이트는 HAV (하드웨어 지원 가상화) 기술이 없는 컴퓨터에 Windows XP 모드를 사용 하도록 설정 합니다. 게스트 운영 체제의 통합 구성 요소 패키지가 호스트 컴퓨터에 설치 된 Windows 가상 PC 버전과 일치 하지 않는 경우 일부 통합 기능이 올바르게 작동 하지 않을 수 있으므로이 업데이트를 설치 하는 것이 좋습니다.

**중요**  Windows 7 서비스 팩 1을 실행 하는 호스트 컴퓨터에 MED-V를 설치 하는 경우에는이 업데이트를 설치할 필요가 없습니다.

 

**팁**  여기에 나열 된 업데이트 외에도 사용 가능한 모든 Windows 가상 PC 업데이트를 검토 하 고 해당 환경에 적합 하거나 필요한 업데이트를 적용 하는 것이 좋습니다.

 

**Windows 가상 PC 업데이트를 설치 하려면**

1.  Microsoft 다운로드 센터에서 필요한 Windows 가상 PC 업데이트를 다운로드 합니다.

    [32 비트 업데이트](https://go.microsoft.com/fwlink/?LinkId=195919) ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [64 비트 업데이트](https://go.microsoft.com/fwlink/?LinkId=195920) ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  관리자 모드의 호스트 컴퓨터에서 설치 파일을 실행 하 고 마법사의 단계를 따릅니다.

    Windows 가상 PC 용 핫픽스 패키지에 대 한 자세한 내용은 [기사 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>바이러스 백신/백업 소프트웨어를 구성 하는 방법


바이러스 백신 활동이 가상 데스크톱의 성능에 영향을 주지 않도록 하려면 호스트 컴퓨터에서 실행 중인 바이러스 백신 또는 백업 프로세스에서 다음 가상 컴퓨터 파일 형식을 제외 하는 것이 좋습니다.

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. .VHD

## 관련 항목


[환경 필수 구성 요소 구성](configure-environment-prerequisites.md)

[개략적인 아키텍처](high-level-architecturemedv2.md)

[MED-V 2.0 지원되는 구성](med-v-20-supported-configurations.md)

 

 





