---
title: 명령줄을 사용하여 패키지를 제거하는 방법
description: 명령줄을 사용하여 패키지를 제거하는 방법
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816823"
---
# 명령줄을 사용하여 패키지를 제거하는 방법


다음 명령줄 프로시저를 사용 하 여 특정 컴퓨터의 App-v (Application Virtualization) 클라이언트에서 가상 응용 프로그램 패키지를 삭제할 수 있습니다.

**모든 사용자의 가상 응용 프로그램 패키지를 삭제 하려면**

-   이전에/CGLOBAL 스위치를 사용 하 여 모든 사용자에 대해 패키지가 추가 된 경우 다음 명령을 사용 하 여 패키지와 전역 파일 형식 및 바로 가기를 삭제 합니다. 관리자 권한이 필요 합니다. 이 명령은 항상 패키지의 전역 삭제를 수행 하므로이 경우/TGLOBAL 스위치가 필요 하지 않습니다.

    `SFTMIME DELETE PACKAGE:”name”`

**개별 사용자에 대해 이전에 추가 된 패키지를 삭제 하려면**

1.  이전에 개별 사용자에 대해 패키지가 추가 된 경우 여러 가지 옵션을 사용할 수 있습니다.

    패키지가 게시 된 각 사용자의 사용자 계정에서 다음 명령을 한 번 실행 합니다. 이렇게 하면 사용자가 다른 컴퓨터로 로밍 하는 경우 응용 프로그램에 대 한 액세스가 거부 됩니다. 프로필에서 특정 사용자의 설정, 바로 가기 및 파일 형식을 삭제 하 고 사용자의 컨텍스트 아래에서 백그라운드 로드를 중지 합니다.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  또는 패키지가 게시 된 각 사용자의 사용자 계정에서 다음 명령을 실행 합니다.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    그런 다음 패키지에 대해이 명령을 실행 합니다.

    `SFTMIME DELETE PACKAGE:”name”`

    이렇게 하면 패키지가 완전히 제거 되 고 해당 프로필에서 모든 사용자 설정, 바로 가기 및 파일 형식이 삭제 됩니다. 이후 패키지가 다시 추가 되는 경우 사용자는 해당 설정을 다시 지정 해야 합니다. 이 명령을 실행 하려면 "응용 프로그램 삭제" (**Deleteapp**) 권한만 필요 합니다.

3.  세 번째 방법으로 **패키지 게시 취소** 명령을 사용 하지 않고 **패키지 삭제** 명령을 간단히 실행할 수 있습니다. 이 경우 각 사용자의 파일 형식 및 바로 가기가 삭제 되지 않고 숨겨지고 사용자 설정이 유지 됩니다. 즉, 나중에 사용자를 위해 패키지가 다시 추가 되 면 파일 형식 및 바로 가기가 복원 되 고 사용자 설정이 다시 적용 됩니다.

## 관련 항목


[명령줄을 사용하여 패키지를 추가하는 방법](how-to-add-a-package-by-using-the-command-line.md)

[명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





