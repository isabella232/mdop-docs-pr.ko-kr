---
title: MED-V 설치 필수 구성 요소
description: MED-V 설치 필수 구성 요소
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824968"
---
# MED-V 설치 필수 구성 요소


MED-V를 설치 하기 위한 전제 조건은 다음과 같습니다.

[Active Directory 요구 사항](#bkmk-activedirectoryrequirements)

[보고서 데이터베이스](#bkmk-howtoinstallthereportdatabase)

[바이러스 백신/백업 소프트웨어 구성](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 SP1](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Active Directory 요구 사항


MED-V 서버를 구성할 때 사용자가 서버가 속한 도메인의 일부가 아닌 경우 도메인 간에 신뢰를 설정 해야 합니다.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>보고서 데이터베이스를 설치 하는 방법


모든 MED-V 작업 영역 로그를 저장 하려면 보고서 데이터베이스가 필요 합니다. 로그 데이터베이스는 MED-V 보고서를 생성 하는 데 사용 됩니다. 보고서에 대 한 자세한 내용은 [Med-v 보고](med-v-reporting.md)를 참조 하세요.

SQL Server는 MED-V 서버와 같은 서버나 원격 서버에 설치할 수 있습니다. 원격 서버에 설치 하는 경우 [원격 서버에 SQL Server 설치](#bkmk-installingsqlserveronaremoteserver)를 참조 하세요.

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>원격 서버에 SQL Server 설치

**원격 서버에 SQL Server를 설치 하려면**

1.  원격 서버에서 다음을 구성 합니다.

    -   인스턴스 이름-기본 인스턴스

    -   인증 모드-혼합 모드

    -   사용자 — 기본적으로 생성 되는 사용자는 "sa"입니다.

    -   비밀 번호-원하는 비밀 번호

    -   데이터 정렬 설정-기본값

    -   사용 현황 보고서 설정 오류-기본값

2.  MED-V 서버에 다음 파일을 설치 합니다.

    -   Microsoft SQL Server2008 용 관리 팩 개체 컬렉션에 대 한 필수 구성 요소를 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server2008 네이티브 클라이언트](https://go.microsoft.com/fwlink/?LinkId=164039) 를 다운로드 하세요.

    -   Microsoft SQL Server2005 용 관리 팩 개체 컬렉션에 대 한 필수 구성 요소를 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server2005 네이티브 클라이언트](https://go.microsoft.com/fwlink/?LinkId=164038) 를 다운로드 하세요.

    -   Microsoft SQL Server2008에 필요한 dll 파일을 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server 2008 Management Objects 컬렉션](https://go.microsoft.com/fwlink/?LinkId=164041) 을 다운로드 하세요.

    -   Microsoft SQL Server2005에 필요한 dll 파일을 설치 하려면 microsoft 다운로드 센터에서 [MICROSOFT Sql Server2005 Management 개체](https://go.microsoft.com/fwlink/?LinkId=164040) 를 다운로드 하세요.

    -   SQL Server2008에 대 한 추가 값을 제공 하는 독립 실행형 설치 패키지를 설치 하려면 Microsoft 다운로드 센터에서 [MICROSOFT SQL Server2008 기능 팩](https://go.microsoft.com/fwlink/?LinkId=163960) 을 다운로드 하세요.

    -   SQL Server2005에 대 한 추가 값을 제공 하는 독립 실행형 설치 패키지를 설치 하려면 Microsoft 다운로드 센터에서 [MICROSOFT SQL Server2005의 기능 팩]( https://go.microsoft.com/fwlink/?LinkId=163961) 을 다운로드 하세요.

    이러한 파일에 대 한 자세한 내용은 microsoft 다운로드 센터에서 microsoft [Sql Server2008 기능 팩](https://go.microsoft.com/fwlink/?LinkId=163960) (또는 Microsoft https://go.microsoft.com/fwlink/?LinkId=163960) 다운로드 센터의 [microsoft sql Server2005에 대 한 기능 팩](https://go.microsoft.com/fwlink/?LinkId=163961) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>바이러스 백신/백업 소프트웨어 구성


바이러스 백신 활동이 가상 데스크톱의 성능에 영향을 주지 않도록 하려면 호스트에서 실행 되는 바이러스 백신 또는 백업 처리에서 다음 가상 머신 파일 형식을 제외 하는 것이 좋습니다.

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Microsoft Virtual PC2007 SP1을 설치 하 고 구성 하는 방법


**중요**  Windows 용 가상 PC가 호스트 컴퓨터에 있는 경우 Virtual PC2007 SP1을 설치 하기 전에 제거 합니다.

 

**Microsoft Virtual PC2007 SP1을 설치 하려면**

1.  Microsoft 다운로드 센터 [가상 PC 2007 sp1](https://go.microsoft.com/fwlink/?LinkId=142994)에서 VIRTUAL PC2007 SP1을 다운로드 합니다.

2.  호스트 컴퓨터에서 설치 파일을 실행 하 고 마법사의 지시를 따릅니다.

3.  관리자 모드의 호스트 컴퓨터에 Virtual PC2007 SP1 업데이트를 설치 합니다.

    자세한 내용은 [가상 PC 2007 SP1의 핫픽스 패키지](https://go.microsoft.com/fwlink/?LinkId=150575)에 대 한 설명을 참조 하세요.

    **참고**  Virtual PC2007 SP1을 실행 하려면 Virtual PC2007 SP1 업데이트가 필요 합니다.

     

## 관련 항목


[지원되는 구성](supported-configurationsmedv-orientation.md)

 

 





