---
title: 명령줄을 사용하여 패키지를 추가하는 방법
description: 명령줄을 사용하여 패키지를 추가하는 방법
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821408"
---
# 명령줄을 사용하여 패키지를 추가하는 방법


다음 절차에서는 가상 응용 프로그램 패키지를 특정 컴퓨터의 App-v (Application Virtualization) 클라이언트에 추가 하는 데 필요한 단계를 나열 합니다.

**특정 사용자에 대 한 가상 응용 프로그램 패키지를 추가 하려면**

-   패키지를 받을 사람의 사용자 계정에서 다음 명령을 실행 합니다. 이 명령은 해당 사용자의 패키지를 추가 하 고 게시 합니다.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**모든 사용자에 대 한 가상 응용 프로그램 패키지를 추가 하려면**

-   관리자 권한이 있는 계정으로 다음 명령을 실행 합니다. 컴퓨터의 모든 사용자에 대해 패키지가 추가 되 고 게시 됩니다.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**전자 소프트웨어 배포 시스템을 사용 하 여 패키지를 추가 하려면**

1.  컴퓨터의 **시스템** 계정에서 명령을 실행 하는 전자 소프트웨어 배포 시스템을 사용 하는 경우/tglobal 스위치를 사용 하지 않는 한 해당 계정에 대해서만 패키지가 게시 됩니다. 다음 명령을 실행 하 여 컴퓨터의 모든 사용자에 대 한 패키지를 추가 하 고 게시 합니다.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    특정 사용자에 대해서만 패키지를 추가 하려면 **패키지 추가** 명령을 실행 한 다음 각 사용자의 사용자 계정 아래에서 다음 **게시 패키지** 명령을 실행 하 여 각 사용자에 대 한 패키지를 명시적으로 게시 합니다.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    전역 매개 변수 없이 패키지를 게시 하면 패키지의 응용 프로그램에 대 한 액세스 권한이 사용자에 게 부여 되 고 매니페스트에 나열 된 파일 형식과 바로 가기가 사용자의 프로필에 게시 됩니다. 필요한 사용 권한은 "파일 형식 연결 관리" (**ManageTypes**) 및 "**바로 가기 게시" (게시**안 됨)입니다.

## 관련 항목


[명령줄을 사용하여 모든 가상 응용 프로그램을 삭제하는 방법](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[명령줄을 사용하여 패키지를 제거하는 방법](how-to-remove-a-package-by-using-the-command-line.md)

 

 





