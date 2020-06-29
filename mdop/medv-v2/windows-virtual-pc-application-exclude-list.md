---
title: Windows 가상 PC 응용 프로그램 제외 목록
description: Windows 가상 PC 응용 프로그램 제외 목록
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823693"
---
# Windows 가상 PC 응용 프로그램 제외 목록


경우에 따라 MED-V 작업 영역에 설치 된 응용 프로그램을 호스트 컴퓨터의 **시작** 메뉴에 게시 하지 않는 것이 좋습니다. [Med-v 작업 영역에서 응용 프로그램을 게시](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)하는 방법에 대 한 지침에 따라 이러한 응용 프로그램의 게시를 취소할 수 있습니다. 그러나 프로그램이 자동으로 업데이트 되는 경우에도 자동으로 다시 게시 될 수 있습니다. 이렇게 하면 응용 프로그램을 다시 게시 취소 해야 합니다.

Windows 가상 PC에는 호스트 **시작** 메뉴에 게시 하지 않으려는 특정 설치 된 응용 프로그램을 지정할 수 있는 "제외 목록" 이라는 기능이 포함 되어 있습니다. "Exclude List"는 HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList 키의 게스트 레지스트리에 있으며 호스트 **시작** 메뉴에 게시 되지 않은 응용 프로그램을 나열 합니다. "제외 목록"이 표시 되는 응용 프로그램에 대 한 자동 업데이트 때문에 자동으로 다시 게시 되지 않으므로 지정 된 응용 프로그램을 영구적으로 게시 취소 하는 것으로 생각할 수 있습니다.

## Windows 가상 PC에서 제외 목록을 사용 하 여 응용 프로그램 관리


****

1.  전체 화면에서 MED-V 작업 영역을 엽니다.

    MED-V 관리 도구 키트를 사용 하 여 전체 화면 모드로 MED-V 작업 영역을 여는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 구성 보기](viewing-med-v-workspace-configurations.md#bkmk-fullscreen)를 참조 하세요. 또는 **시작**을 클릭 하 고 **모든 프로그램**, **Windows 가상 pc**, **windows 가상 pc**를 차례로 클릭 한 다음 med-v 작업 영역을 두 번 클릭 하 여 전체 화면으로 수동으로 열 수 있습니다.

2.  MED-V 작업 영역 Windows 가상 PC 창에서 레지스트리 편집기를 엽니다.

    **시작**을 클릭 하 고 **실행**을 클릭 한 다음 regedit를 입력 합니다. 그런 다음 **확인을**클릭 합니다.

3.  레지스트리 편집기에서 HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList 레지스트리 키를 찾습니다.

4.  호스트 컴퓨터 **시작** 메뉴에 게시 하지 않으려는 설치 된 응용 프로그램에 대 한 새 레지스트리 값을 만듭니다. 예를 들어 Microsoft Silverlight 자동으로 게시 된 프로그램의 게시를 취소 하려면 다음 단계를 따릅니다.

    1.  VPCVAppExcludeList 레지스트리 키가 강조 표시 된 상태에서 **편집**을 클릭 하 고 **새로 만들기**를 클릭 한 다음 **문자열 값**을 클릭 합니다.

    2.  새 레지스트리 값의 이름을 입력 합니다. 예를 들어 Microsoft Silverlight의 경우 sllauncher.exe를 입력할 수 있습니다.

    3.  새 레지스트리 값을 두 번 클릭 하 고 값 데이터를 입력 합니다.

        값 데이터는 게시 취소 하려는 명령의 전체 경로입니다. 게시 하지 않으려는 응용 프로그램의 **시작** 메뉴에서 바로 가기를 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 클릭 하 여 전체 경로를 찾을 수 있습니다. 전체 경로는 **바로 가기** 탭의 **대상**아래에 나열 됩니다.

        예를 들어 Microsoft Silverlight 프로그램의 전체 경로는 "C:\\program files Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe" 일 수 있습니다.

        **중요**  해당 하는 경우 값 데이터 필드에 입력할 때 전체 경로에서 따옴표를 제거 합니다.

         

5.  레지스트리 편집기를 닫고 MED-V 작업 영역 가상 컴퓨터를 다시 시작 합니다.

    응용 프로그램이 MED-V 작업 영역에 여전히 설치 되어 있지만 이제 호스트 컴퓨터 **시작** 메뉴에서 제거 됩니다.

VPCVAppExcludeList 키에서 해당 값을 삭제 하 여 제외 된 응용 프로그램을 호스트 **시작** 메뉴에 다시 게시할 수도 있습니다. 예를 들어 Microsoft Silverlight를 다시 게시 하려면 sllauncher.exe 레지스트리 값을 마우스 오른쪽 단추로 클릭 하 고 **삭제**를 선택 합니다.

## 관련 항목


[MED-V에 대한 기술 참조](technical-reference-for-med-v.md)

[MED-V 작업 영역에서 응용 프로그램을 게시 및 게시 취소하는 방법](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





