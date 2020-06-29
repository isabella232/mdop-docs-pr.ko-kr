---
title: 클러스터 모드용 MED-V 서버 구성
description: 클러스터 모드용 MED-V 서버 구성
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826718"
---
# 클러스터 모드용 MED-V 서버 구성


클러스터 모드에서 MED-V 서버를 구성할 수 있습니다. 클러스터 모드에서는 두 개의 서버가 사용 되 고 두 서버 모두에 대해 상호 종속으로 식별 된 모든 파일이 파일 시스템에 배치 됩니다. 서버는 파일을 로컬로 저장 하는 대신 파일 시스템에서 파일에 액세스 합니다.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**클러스터 모드에서 MED-V 서버를 구성 하려면**

1.  서버 중 하나에 MED-V를 설치 하 고 구성 합니다.

2.  모든 서버에서 액세스할 수 있는 중앙 위치에서 공유 네트워크를 만듭니다.

3.  * &lt; InstallDir &gt; /Servers/ConfigurationServer* 폴더의 콘텐츠를 공유 네트워크에 복사 합니다.

4.  지정 된 모든 서버에 MED-V 서버를 설치 합니다.

5.  공유 네트워크에서 모든 MED-V 서버 시스템 계정에 대 한 모든 액세스 권한을 할당 합니다.

6.  각 서버에서 다음을 수행 합니다.

    1.  * &lt; InstallDir &gt; /Servers/ServerConfiguration.xml* 파일에서 * &lt; storepath &gt; * 의 값을 공유 네트워크 경로로 설정 합니다.

    2.  원본 서버에서 모든 MED-V 서버로 * &lt; 명령이 있는 salldir &gt; /Servers/KeyPair.xml* 파일을 복사 합니다.

    3.  MED-V 서비스를 다시 시작 합니다.

**참고**  모든 서버에 동일한 로컬 설정 (예: 수신 포트, IIS 서버, 관리 권한, 보고서 데이터베이스 등)이 있는 경우 * &lt; InstallDir &gt; /Servers/ServerSettings.xml* 모든 서버 에서도 공유할 수 있습니다.

 

## 관련 항목


[MED-V 인프라 계획 및 디자인](med-v-infrastructure-planning-and-design.md)

 

 





