---
title: 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법
description: 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824493"
---
# 클라이언트 컴퓨터에서 Microsoft 콘텐츠 배달 네트워크에 액세스할 수 없는 경우 셀프 서비스 포털을 구성하는 방법


조직의 클라이언트 컴퓨터에서 Microsoft 사용자 CDN (콘텐츠 배달 네트워크)에 액세스할 수 없는 경우 다음 지침을 따릅니다.

**구성 해야 하는 이유는 다음과 같습니다.**

클라이언트 컴퓨터는 특정 JavaScript 파일에 대 한 필수 액세스를 셀프 서비스 포털에 제공 하는 CDN에 대 한 액세스 권한이 필요 합니다. 클라이언트 컴퓨터가 CDN에 액세스할 수 없을 때 셀프 서비스 포털을 구성 하지 않은 경우에는 최종 사용자가 로그인 하는 회사 이름과 계정만 표시 됩니다. 오류 메시지가 표시 되지 않습니다.

**참고**  MBAM 2.5 SP1에는 JavaScript 파일이 제품에 포함 되어 있으므로이 섹션의 지침에 따라 인터넷에 액세스할 수 없는 클라이언트를 지원 하도록 SSP를 구성할 필요가 없습니다.

 

**클라이언트 컴퓨터가 CDN에 액세스할 수 없는 경우 셀프 서비스 포털을 구성 하는 방법**

1. CDN에서 다음 JavaScript 파일을 다운로드 합니다.

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. JavaScript 파일을 셀프 서비스 포털의 **Scripts** 디렉터리에 복사 합니다. 이 디렉터리는 <em> &lt; mbam 셀프 서비스 설치 디렉터리 &gt; \\ </em> 셀프 서비스 Website\\Scripts.에 있습니다.

3. IIS (인터넷 정보 서비스) 관리자를 엽니다.

4. **사이트** &gt; **Microsoft BitLocker 관리 및 모니터링**을 확장 하 고 **SelfService**를 강조 표시 합니다.

   **참고**  
   *SelfService* 는 기본 가상 디렉터리 이름입니다. 구성 중에이 디렉터리에 대해 다른 이름을 선택한 경우에는이 지침에서 *SelfService* 을 선택한 이름으로 바꿔야 한다는 점에 유의 하세요.

     

5. 가운데 창에서 **응용 프로그램 설정을**두 번 클릭 합니다.

6. 다음 목록에 있는 각 항목에 대해 &lt; *virtual directory* &gt; /SelfService/(또는 구성 중에 선택한 이름)을 사용 하 여 새 위치를 참조 하는 응용 프로그램 설정을 편집 합니다. 예를 들어 가상 디렉터리 경로는/selfservice/Scripts/jQuery-1.10.2.min.js와 유사 합니다.

   -   jQueryPath:/ &lt; *virtual directory* &gt; /Scripts/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *virtual directory* &gt; /Scripts/jQuery.validate.unobtrusive.min.js



## 관련 항목


[MBAM 2.5 웹 응용 프로그램을 구성하는 방법](how-to-configure-the-mbam-25-web-applications.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





