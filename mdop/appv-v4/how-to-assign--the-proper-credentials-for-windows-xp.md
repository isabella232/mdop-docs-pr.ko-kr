---
title: Windows XP에 적합 한 자격 증명을 할당 하는 방법
description: Windows XP에 적합 한 자격 증명을 할당 하는 방법
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819323"
---
# Windows XP에 적합 한 자격 증명을 할당 하는 방법


적절 한 WindowsXP 자격 증명을 사용 하도록 앱-V 데스크톱 클라이언트를 구성 하려면 다음 절차를 수행 합니다.

**참고**  이 절차를 완료 한 후 도메인에 가입 되지 않은 클라이언트는 도메인에 가입 하지 않고 게시 새로 고침을 수행할 수 있습니다.

 

**WindowsXP를 실행 하는 App-v 클라이언트에 대 한 적절 한 자격 증명을 할당 하려면**

1.  WindowsXP를 실행 하는 App-v 클라이언트에 대 한 관리자 권한이 있으면 **사용자 계정** 제어판의 클래식 제어판을 엽니다.

2.  **고급 탭**을 클릭 하 고 **암호 관리**를 선택 합니다.

3.  저장 된 **사용자 이름 및 암호** 화면에서 **추가**를 클릭 합니다.

4.  **로그온 정보 속성** 화면에서 app-v 인프라의 정보로 다음 필드를 입력 합니다.

    1.  **서버:** 게시 서버 외부 이름의 이름입니다.

    2.  **사용자 이름:** 양식 Domain\\username. 외부 사용자의 사용자 이름

    3.  **비밀 번호:** **사용자 이름** 필드에 입력 한 사용자 계정의 암호입니다.

5.  **확인**을 클릭합니다. 자격 증명이 클라이언트에 저장 됩니다.

## 관련 항목


[도메인 가입 및 도메인에 가입되지 않은 클라이언트](domain-joined-and-non-domain-joined-clients.md)

[Windows Vista에 적합 한 자격 증명을 할당 하는 방법](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





