---
title: ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법
description: ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813841"
---
# ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.0 Client 구성을 수정하는 방법


앱-V 5.0 ADMX 템플릿을 사용 하 여 ADMX 템플릿 및 그룹 정책을 사용 하 여 App-v 5.0 클라이언트 설정을 구성 합니다.

**그룹 정책을 사용 하 여 앱-V 5.0 클라이언트 구성을 수정 하려면**

1.  App-v 5.0 클라이언트 구성을 수정 하려면 App-v 5.0와 함께 제공 되는 **ADMXTemplate** 파일을 찾습니다.

    **참고**  앱-V 5.0 **ADMX 서식 파일**을 다운로드 하려면 다음 링크를 사용 <https://go.microsoft.com/fwlink/p/?LinkId=393941> 합니다.

     

2.  그룹 정책을 관리 하는 컴퓨터 (일반적으로 도메인 컨트롤러)에서 다음 디렉터리에 **admx** 파일을 복사 합니다. ** &lt; 설치 드라이브 &gt; \ \ Windows \\ policydefinitions**.

    그 다음, 같은 컴퓨터에서 **adml** 파일을 다음 디렉터리에 복사 합니다. \ \ ** &lt; &gt; \ Windows \\ policydefinitions \ \ en-US**.

3.  파일을 복사한 후 그룹 정책 관리 콘솔을 열고, 앱-v 5.0 클라이언트와 연결 된 정책을 수정 하려면 **컴퓨터 구성**  /  **정책**  /  **관리 템플릿**  /  **시스템**  /  **app-v**로 이동 합니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.0 배포](deploying-app-v-50.md)

[클라이언트 구성 설정 정보](about-client-configuration-settings.md)

 

 





