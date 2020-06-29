---
title: Windows Vista에 적합 한 자격 증명을 할당 하는 방법
description: Windows Vista에 적합 한 자격 증명을 할당 하는 방법
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821368"
---
# Windows Vista에 적합 한 자격 증명을 할당 하는 방법


다음 절차를 사용 하 여 올바른 WindowsVista 자격 증명을 사용할 수 있도록 App-v 데스크톱 클라이언트를 구성 합니다.

**참고**  이 절차는 비도메인에 연결 된 각 컴퓨터에서 완료 되어야 합니다. 환경에서 도메인에 연결 되지 않은 컴퓨터 수에 따라 매우 지루한 작업을 할 수 있습니다. 스크립트와 자격 증명 관리자의 명령줄 인터페이스를 사용 하 여 관리자가이 프로세스를 자동화 하는 데 도움을 줄 수 있습니다.

 

**Windows Vista를 실행 하는 App-v 클라이언트에 대 한 적절 한 자격 증명을 할당 하려면**

1.  Windows Vista를 실행 하는 App-v 데스크톱 클라이언트에 대 한 관리자 권한이 있으면 **사용자 계정** 제어판의 클래식 제어판을 엽니다.

2.  왼쪽 작업 창의 **사용자 계정** 에서 **네트워크 암호 관리** 를 선택 합니다.

3.  **저장 된 사용자 이름 및 암호** 화면에서 **추가** 를 선택 합니다.

4.  **저장 된 자격 증명 속성** 화면에서 앱-V 인프라에 대 한 정보를 제공 합니다.

    1.  **로그온 대상:** 게시 서버의 외부 이름입니다.

    2.  **사용자 이름:** 양식 Domain\\Username. 외부 사용자의 사용자 이름

    3.  **비밀 번호:** **사용자 이름** 필드에 입력 한 사용자 계정의 암호입니다.

    4.  **자격 증명 유형** 유지를 선택 하 고 **확인**을 클릭 합니다.

5.  **닫기**를 클릭합니다. 자격 증명은 앱 V 인프라에 대 한 적절 한 인증을 위해 자격 증명 저장소에 저장 됩니다.

## 관련 항목


[도메인 가입 및 도메인에 가입되지 않은 클라이언트](domain-joined-and-non-domain-joined-clients.md)

[Windows XP에 적합 한 자격 증명을 할당 하는 방법](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





