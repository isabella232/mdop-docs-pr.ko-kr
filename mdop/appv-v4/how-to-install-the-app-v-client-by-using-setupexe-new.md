---
title: Setup.exe를 사용하여 App-V Client를 설치하는 방법
description: Setup.exe를 사용하여 App-V Client를 설치하는 방법
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817338"
---
# Setup.exe를 사용하여 App-V Client를 설치하는 방법


이 항목에서는 setup.exe 프로그램을 사용 하 여 앱 V 클라이언트를 설치 하는 방법에 대해 설명 합니다. setup.exe 프로그램을 사용 하 여 App-v 클라이언트를 설치 하는 경우 설치 관리자는 필요한 필수 구성 요소 소프트웨어를 확인 하 고 클라이언트를 설치 하기 전에 자동으로 설치 합니다.

**Setup.exe를 사용 하 여 응용 프로그램 가상화 클라이언트 설치**

1.  컴퓨터에 대 한 관리자 권한이 있는 계정으로 로그온 했는지 확인 합니다.

2.  명령 프롬프트 창을 열고 설치 파일이 들어 있는 폴더로 디렉터리를 변경 합니다. App-v 클라이언트의 버전 4.6 또는 이후 버전을 설치할 때 컴퓨터의 운영 체제 32 비트 또는 64 비트에 대 한 올바른 설치 관리자를 사용 해야 합니다. 설치에 실패 하 고 잘못 된 설치 관리자를 사용 하는 경우 오류 메시지가 표시 됩니다.

3.  명령 프롬프트에 설치 명령 문자열을 입력 합니다. 또는 명령 파일을 만들어 명령 프롬프트에서 실행할 수 있습니다. VBScript 또는 Windows PowerShell 같은 스크립트 언어를 사용 하 여 명령을 실행할 수도 있습니다.

4.  다음 명령줄 예제에서는 여러 개의 선택적 매개 변수를 사용 하 여 setup.exe를 사용할 수 있는 방법을 보여 줍니다. 이러한 매개 변수에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요.

    **"setup.exe"/s/v "/qn SWICACHESIZE = \\" 10240 \\ "SWIPUBSVRDISPLAY = \\" 프로덕션 System\\ "SWIPUBSVRTYPE = \\" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \\ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \\" D:\\AppVirt\\Global\\ "SWIUSERDATA = \" "^% LOCALAPPDATA = \\" ^ Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""**

    **중요**  
    -   "**/V**" 섹션에 표시 되는 인용 부호는 특수 문자로 처리 하 고 앞에 ""를 입력 해야 합니다 **\\** . 큰따옴표는 값에 공백이 포함 된 경우에만 필요 합니다. 그러나 일관성을 위해 이전 예제의 모든 인스턴스가 인용 부호로 표시 됩니다.

    -   " **%** **% HomeDrive%**"의 "" 문자는 "" 이스케이프 문자 앞에와 야 합니다 **^** . 그렇지 않으면 Windows 명령 셸에서는 설치를 수행 하는 사용자의 값을 설정 합니다.

    -   자동 설치를 위해 **InstallShield** 스위치 **/s** 및 **/qn** 이 필요 합니다. **/Qn** 스위치는 **/v** 스위치 뒤에 공백이 없는 인용 문자로 구분 해야 합니다.

    -   **SWIGLOBALDATA** 값에 지정 된 폴더가 이미 존재 해야 합니다.

     

5.  설치가 완료 되 면 Microsoft 업데이트 검사를 실행 하 여 최신 업데이트가 설치 되어 있는지 확인 하는 것이 좋습니다.

## 관련 항목


[명령줄을 사용하여 클라이언트를 설치하는 방법](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





