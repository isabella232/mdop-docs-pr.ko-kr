---
title: 사용자에게 더 많은 셀프 서비스 포털 정보를 가리키는 "HelpdeskText" 명령문을 지역화하는 방법
description: 사용자에게 더 많은 셀프 서비스 포털 정보를 가리키는 "HelpdeskText" 명령문을 지역화하는 방법
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823423"
---
# 사용자에게 더 많은 셀프 서비스 포털 정보를 가리키는 "HelpdeskText" 명령문을 지역화하는 방법


셀프 서비스 포털을 사용 하는 경우 추가 도움말을 가져오는 방법에 대 한 최종 사용자에 게 해당 하는 ' HelpdeskText "문의 지역화 된 버전을 구성할 수 있습니다. 문에 대해 지역화 된 텍스트를 구성 하는 경우 다음 지침에 설명 된 대로 MBAM에는 지역화 버전이 표시 됩니다. MBAM이 지역화 된 버전을 찾지 못하면 **HelpdeskText** 매개 변수에 있는 값이 표시 됩니다.

**참고**  다음 지침에서는 *SelfService* 가 셀프 서비스 포털의 기본 가상 디렉터리 이름입니다. 셀프 서비스 포털을 구성할 때 다른 이름을 사용 했을 수 있습니다.

 

**HelpdeskText 문의 지역화 된 버전을 표시 하려면**

1.  셀프 서비스 **포털을 구성한** 서버에서 &gt; **Microsoft BitLocker 관리 및 모니터링** &gt; **SelfService** &gt; **응용 프로그램 설정**으로 이동 합니다.

2.  **작업** 창에서 **추가** 를 클릭 하 여 **응용 프로그램 설정 추가** 대화 상자를 엽니다.

3.  **이름** 필드에 **HelpdeskText**\ _ &lt; *언어* &gt; 를 입력 &lt; *Language* &gt; 합니다. 여기서 해당 언어는 텍스트에 적합 한 언어 코드입니다.

    예를 들어, 스페인어로 지역화 된 HelpdeskText 문을 만들려면 매개 변수의 이름을 **HelpdeskText \ _es로**이름에 붙여넣습니다.

    언어 폴더의 이름은 **es**대신 언어 **중립 이름을 사용할** 수도 있습니다. 최종 사용자의 브라우저가 **es** 로 설정 되 고 해당 폴더가 존재 하지 않는 경우, .net에서 정의 된 부모 로캘을 재귀적으로 검색 하 고 확인 하 여 &lt; &gt; 기본 Notice.txt 파일이 되기 전에\\SelfServiceWebsite\\es\\Notice.txt Mbam 서비스 설치 디렉터리를 확인 합니다. 이 재귀적 대체는 .NET 리소스 로딩 규칙을 모방 합니다.

    사용할 수 있는 유효한 언어 코드 목록은 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947)를 참조 하세요.

4.  **값** 필드에 최종 사용자에 게 표시 하려는 지역화 된 텍스트를 입력 합니다.



## 관련 항목


[조직에 대한 셀프 서비스 포털 사용자 지정](customizing-the-self-service-portal-for-your-organization.md)

 

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.



