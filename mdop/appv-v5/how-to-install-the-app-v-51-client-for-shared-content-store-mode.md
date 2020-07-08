---
title: 공유 콘텐츠 저장소 모드에서 App-V 5.1 Client를 설치하는 방법
description: 공유 콘텐츠 저장소 모드에서 App-V 5.1 Client를 설치하는 방법
author: dansimp
ms.assetid: 6f3ecb1b-b5b5-4ae0-8de9-b4ffdfd2c216
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7ce8114a44762180bf9bb0240913dca50c55d31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814052"
---
# 공유 콘텐츠 저장소 모드에서 App-V 5.1 Client를 설치하는 방법


앱-V 5.1 공유 콘텐츠 저장소 (SCS) 모드를 사용 하도록 Microsoft Application Virtualization (App-v) 5.1 클라이언트를 설치 하려면 다음 절차를 사용 합니다. 설치 하려는 컴퓨터에 필수 구성 요소가 모두 설치 되어 있는지 확인 해야 합니다. [앱-V 5.1 필수 조건을](app-v-51-prerequisites.md)보려면 다음 링크를 사용 합니다.

**참고**  필요한 경우이 절차를 수행 하기 전에 앱-V 5.1 클라이언트의 기존 버전을 제거 합니다.

 

SCS 모드에 대 한 자세한 내용은 Microsoft App-v 5.0 ()에서 (() [백그라운드에서 공유 콘텐츠 저장소](https://go.microsoft.com/fwlink/?LinkId=316879) 를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=316879) .

**SCS 모드에 대 한 App-v 5.1 클라이언트 설치 및 구성**

1.  앱-V 5.1 클라이언트 설치 파일을 설치할 컴퓨터에 복사 합니다. 명령줄을 열고 설치 파일이 저장 된 디렉터리에서 설치 중인 클라이언트 버전에 따라 다음 옵션 중 하나를 입력 합니다.

    -   RDS 버전의 App-v 5.1 클라이언트 형식을 설치 하려면 다음을 수행 합니다. **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   App-v 5.1 클라이언트 유형의 표준 버전을 설치 하려면: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **중요**  자동 설치를 수행 해야 하며 설치에 실패 하 게 됩니다.

         

2.  설치를 완료 한 후에는 클라이언트를 실행 하는 컴퓨터에 패키지를 배포 하 고 모든 패키지 내용이 네트워크를 통해 스트리밍되 게 할 수 있습니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V 5.1 Sequencer 및 Client 배포](deploying-the-app-v-51-sequencer-and-client.md)

 

 





