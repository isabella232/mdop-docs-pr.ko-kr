---
title: MBAM 2.5 웹 사이트를 이동하는 방법
description: MBAM 2.5 웹 사이트를 이동하는 방법
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825748"
---
# MBAM 2.5 웹 사이트를 이동하는 방법


다음 절차를 사용 하 여 다음 MBAM 웹 사이트를 한 컴퓨터에서 다른 컴퓨터로 이동 하 여 서버 A에서 서버 B로 다음 기능을 이동 합니다.

-   관리 및 모니터링 웹 사이트

-   셀프 서비스 포털

**중요**  두 웹 사이트를 구성 하는 동안 같은 연결 문자열, 보고서 URL, 그룹 계정 및 웹 서비스 응용 프로그램 풀 도메인 계정을 현재 사용 중인 사용자와 함께 제공 해야 합니다. 같은 값을 사용 하지 않는 경우에는 일부 서버에 액세스할 수 없습니다. 현재 값을 가져오려면 **get-MbamWebApplication** Windows PowerShell cmdlet을 사용 합니다.

 

**관리 및 모니터링 웹 사이트를 다른 서버로 이동 하려면**

1.  서버 B에서 MBAM 2.5 서버 소프트웨어를 설치 합니다. 지침은 [MBAM 2.5 서버 소프트웨어 설치](installing-the-mbam-25-server-software.md)를 참조 하세요.

2.  서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **관리 및 모니터링 웹 사이트** 기능만 선택 합니다.

    또는 **Enable-MbamWebApplication** Windows PowerShell cmdlet을 사용 하 여 관리 및 모니터링 웹 사이트를 구성할 수 있습니다.

    관리 및 모니터링 웹 사이트를 구성 하는 방법에 대 한 지침은 [MBAM 2.5 웹 응용 프로그램을 구성](how-to-configure-the-mbam-25-web-applications.md)하는 방법을 참조 하세요.

**셀프 서비스 포털을 다른 서버로 이동 하려면**

1.  서버 B에서 MBAM 2.5 서버 소프트웨어를 설치 합니다. 지침은 [MBAM 2.5 서버 소프트웨어 설치](installing-the-mbam-25-server-software.md)를 참조 하세요.

2.  서버 B에서 MBAM 서버 구성 마법사를 시작 하 고 **새 기능 추가**를 클릭 한 다음 **셀프 서비스 포털** 기능만 선택 합니다.

    또는 **Enable-MbamWebApplication** Windows PowerShell cmdlet을 사용 하 여 셀프 서비스 포털을 구성할 수 있습니다.

    관리 및 모니터링 웹 사이트를 구성 하는 방법에 대 한 지침은 [MBAM 2.5 웹 응용 프로그램을 구성](how-to-configure-the-mbam-25-web-applications.md)하는 방법을 참조 하세요.

3.  조직의 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 JavaScript 파일도 이동 해야 합니다. 자세한 내용은 [클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하는 방법을](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) 참조 하세요.

4.  조직의 셀프 서비스 포털을 사용자 지정 합니다. [조직의 셀프 서비스 포털을 사용자 지정](customizing-the-self-service-portal-for-your-organization.md) 하는 지침을 사용 하 여 현재 사용자 지정을 검토 하 고 서버 B의 셀프 서버 포털에서 사용자 지정 설정을 구성 합니다.



## 관련 항목


[MBAM 2.5 웹 응용 프로그램을 구성하는 방법](how-to-configure-the-mbam-25-web-applications.md)

[Windows PowerShell을 사용하여 MBAM 2.5 서버 기능 구성](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[다른 서버로 MBAM 2.5 기능 이동](moving-mbam-25-features-to-another-server.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





