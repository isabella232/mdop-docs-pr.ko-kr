---
title: 셀프 서비스 포털 알림 텍스트를 지역화하는 방법
description: 셀프 서비스 포털 알림 텍스트를 지역화하는 방법
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826713"
---
# 셀프 서비스 포털 알림 텍스트를 지역화하는 방법


셀프 서비스 포털에서 기본적으로 최종 사용자에 게 표시 되도록 지역화 된 알림 텍스트를 구성할 수 있습니다. 알림 텍스트를 표시 하는 Notice.txt 파일의 루트 디렉터리는 다음과 같습니다.

&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

지역화 된 알림 텍스트를 표시 하려면 지역화 Notice.txt 파일을 만든 후 다음 예제 디렉터리의 특정 언어 폴더 아래에 저장 합니다.

&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

**참고**  **응용 프로그램 설정**에서 **NoticeTextPath** 항목을 사용 하 여 경로를 구성할 수 있습니다.

 

MBAM은 다음 규칙에 따라 알림 텍스트를 표시 합니다.

-   해당 언어 폴더에서 지역화 된 **Notice.txt** 파일을 만드는 경우 기본 **Notice.txt** 파일이 있으면 mbam에 지역화 된 알림 텍스트가 표시 됩니다. 기본 **Notice.txt** 파일이 없으면 기본 파일이 없음을 나타내는 메시지가 표시 됩니다.

-   MBAM이 Notice.txt 파일의 지역화 된 버전을 찾지 못하면 기본 Notice.txt 파일에 텍스트를 표시 합니다.

-   MBAM이 기본 Notice.txt 파일을 찾지 못하면 셀프 서비스 포털에 기본 텍스트가 표시 됩니다.

**참고**  최종 사용자의 브라우저가 해당 언어 하위 폴더 또는 Notice.txt 없는 언어로 설정 된 경우에는 다음 루트 디렉터리의 Notice.txt 파일에 있는 텍스트가 표시 됩니다.

&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

 

**지역화 된 Notice.txt 파일을 만들려면**

1.  셀프 서비스 포털을 구성한 서버에서 &lt; *Language* &gt; 다음 예제 디렉터리에 언어 폴더를 만들고 여기서 &lt; *언어* 는 &gt; 지역화 된 언어의 이름을 나타냅니다.

    &lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

    **참고**  일부 언어 폴더가 이미 있으므로 폴더를 만들 필요가 없을 수 있습니다. 언어 폴더를 만들어야 하는 경우 언어 폴더에 사용할 수 있는 유효한 이름 목록에 대 한 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947) 를 참조 하세요 &lt; *Language* &gt; .

     

2.  지역화 된 알림 텍스트를 포함 하는 Notice.txt 파일을 만듭니다.

3.  Notice.txt 파일을 &lt; *언어* &gt; 폴더에 저장 합니다. 예를 들어 스페인어로 지역화 된 Notice.txt 파일을 만들려면 다음 예제 디렉터리에 지역화 된 Notice.txt 파일을 저장 합니다.

    &lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\Es-es

    언어 폴더의 이름은 **es**대신 언어 **중립 이름을 사용할** 수도 있습니다. 최종 사용자의 브라우저가 **es** 로 설정 되 고 해당 폴더가 존재 하지 않는 경우, .net에서 정의 된 부모 로캘을 재귀적으로 검색 하 고 확인 하 여 &lt; &gt; 기본 Notice.txt 파일이 되기 전에\\SelfServiceWebsite\\es\\Notice.txt Mbam 서비스 설치 디렉터리를 확인 합니다. 이 재귀적 대체는 .NET 리소스 로딩 규칙을 모방 합니다.



## 관련 항목


[조직에 대한 셀프 서비스 포털 사용자 지정](customizing-the-self-service-portal-for-your-organization.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





