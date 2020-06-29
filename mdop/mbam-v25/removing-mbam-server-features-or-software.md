---
title: MBAM 서버 기능 또는 소프트웨어 제거
description: MBAM 서버 기능 또는 소프트웨어 제거
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824978"
---
# MBAM 서버 기능 또는 소프트웨어 제거


이 지침에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM)에서 소프트웨어와 기능을 제거 하는 방법에 대해 설명 합니다. MBAM 서버 기능을 제거 하는 경우 구성 된 기능만 MBAM 서버 소프트웨어가 아닌 서버에서 제거 됩니다. MBAM 서버 소프트웨어를 제거 하면 해당 서버에서 구성한 소프트웨어와 모든 MBAM 서버 기능이 제거 됩니다.

**참고**  데이터가 실수로 제거 되는 것을 방지 하기 위해 MBAM은 데이터베이스를 제거 하는 메커니즘을 제공 하지 않습니다. 수동으로 작업을 수행 해야 합니다.

 

## <a href="" id="bkmk-removeserverfeatures"></a>MBAM 서버 기능 제거


다음 방법 중 하나를 사용 하 여 구성한 MBAM 서버 기능을 제거할 수 있습니다.

-   MBAM 서버 구성 마법사

-   Windows PowerShell cmdlet

### MBAM 서버 구성 마법사를 사용 하 여 기능 제거

이 지침에 따라 MBAM 서버 구성 마법사를 사용 하 여 서버에서 구성 된 MBAM 서버 기능을 제거 합니다.

**마법사를 사용 하 여 MBAM 기능을 제거 하려면**

1.  기능을 제거 하려는 서버에서 **Mbam 서버 구성을** 선택 하 여 구성 마법사를 엽니다.

2.  **기능 제거**를 클릭 하 고 제거할 기능을 선택한 후 **다음**을 클릭 합니다. 제거를 위해 선택한 기능이 **요약** 페이지에 표시 됩니다.

3.  **제거** 를 클릭 하 여 기능 제거를 시작 하 고 **닫기를**클릭 합니다.

### Windows PowerShell을 사용 하 여 기능 제거

Windows PowerShell cmdlet을 사용 하 여 MBAM 서버 기능을 제거 하는 일반적인 지침으로 다음 단계를 사용 합니다.

**Windows PowerShell을 사용 하 여 MBAM 기능을 제거 하려면**

1.  기능을 제거 하기 전에 windows powershell을 사용 하 여 Windows PowerShell을 사용 하기 위한 필수 구성 요소를 검토 하 [여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md) 참조 하세요.

2.  다음 cmdlet을 사용 하 여 MBAM 서버 기능을 제거 합니다.

    -   사용 안 함-MbamReport

    -   Disable-MbamWebApplication

    -   사용 안 함-MbamCMIntegration

    Windows powershell cmdlet에 대 한 도움말을 보려면 **get-help** &lt; *cmdlet* 을 입력 &gt; 하거나, mbam windows powershell cmdlet에 대해 [Windows PowerShell 페이지를 사용 하 여 Microsoft 데스크톱 최적화 팩 자동화](https://go.microsoft.com/fwlink/?LinkId=393498) 를 참조 하세요.

## MBAM 서버 소프트웨어 제거


다음 단계를 사용 하 여 MBAM 서버 소프트웨어와 해당 서버에서 구성한 모든 MBAM 서버 기능을 제거 합니다.

**MBAM 서버 소프트웨어를 제거 하려면**

1.  MBAM 서버 소프트웨어를 제거 하려는 서버에서 **MBAMserversetup.exe** 를 실행 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 시작 합니다.

2.  **제거**를 선택 하 고 나머지 메시지에 따라 Mbam 서버 소프트웨어 제거 프로세스를 완료 합니다.



## 관련 항목


[MBAM 2.5 배포](deploying-mbam-25.md)

 

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.



