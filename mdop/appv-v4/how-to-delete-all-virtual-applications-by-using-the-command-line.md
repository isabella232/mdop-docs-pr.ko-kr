---
title: 명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법
description: 명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817538"
---
# 명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법


다음 절차를 사용 하 여 특정 컴퓨터에서 모든 가상 응용 프로그램을 삭제할 수 있습니다.

**참고**  모든 응용 프로그램이 패키지에서 삭제 되 면 Application Virtualization (App-v) 클라이언트 에서도 패키지를 삭제 합니다.

 

**모든 응용 프로그램을 삭제 하려면**

-   명령이 실행 되는 사용자 계정에 대 한 모든 응용 프로그램을 삭제 하려면 다음 명령을 실행 합니다. 선택/전역 스위치를 사용 하 여 명령을 실행 하는 경우 관리 권한이 있는 계정을 사용 하면 모든 응용 프로그램이 모든 사용자에 대해 삭제 됩니다.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **참고**  모든 응용 프로그램이 패키지에서 삭제 되 면 Application Virtualization (App-v) 클라이언트 에서도 패키지를 삭제 합니다.

     

## 관련 항목


[명령줄을 사용하여 패키지를 추가하는 방법](how-to-add-a-package-by-using-the-command-line.md)

[명령줄을 사용하여 패키지를 제거하는 방법](how-to-remove-a-package-by-using-the-command-line.md)

 

 





