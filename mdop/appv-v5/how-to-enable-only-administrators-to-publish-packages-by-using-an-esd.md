---
title: ESD를 사용하여 관리자만 패키지를 게시할 수 있도록 하는 방법
description: ESD를 사용하여 관리자만 패키지를 게시할 수 있도록 하는 방법
author: dansimp
ms.assetid: 03367b26-83d5-4299-ad52-b9177b9cf9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 341e86ca806c5acc736c78cf8072aab6fb4286df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814108"
---
# ESD를 사용하여 관리자만 패키지를 게시할 수 있도록 하는 방법


App-v 5.0 SP3부터 앱-V 클라이언트를 구성 하 여 관리자 (최종 사용자가 아님)만 패키지를 게시 하거나 게시 취소할 수 있도록 할 수 있습니다. 이전 버전의 App-v에서는 최종 사용자가 이러한 작업을 수행 하는 것을 방지할 수 없었습니다.

**관리자만 패키지를 게시 하거나 게시 취소할 수 있도록 설정 하려면**

1.  다음 그룹 정책 개체 노드로 이동 합니다.

    **컴퓨터 구성 &gt; 정책 &gt; 관리 템플릿 &gt; 시스템 &gt; 앱-V &gt; 게시**.

2.  **관리자 권한으로 게시** 그룹 정책 설정을 사용 하도록 설정 합니다.

    또는 PowerShell을 사용 하 여이 항목을 설정 하려면 [powershell을 사용 하 여 독립 실행형 컴퓨터에서 실행 되는 app-v 5.0 패키지를 관리 하는 방법을](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)참조 하세요.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

 

 





