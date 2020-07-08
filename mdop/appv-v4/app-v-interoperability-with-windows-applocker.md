---
title: Windows AppLocker에 대한 App-V 상호 운용성
description: Windows AppLocker에 대한 App-V 상호 운용성
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822313"
---
# Windows AppLocker에 대한 App-V 상호 운용성


Microsoft App-v (Application Virtualization) 클라이언트의 버전 4.5 SP1은 Windows 7의 AppLocker 기능을 지원 합니다. AppLocker 기능을 사용 하면 IT 관리자가 컴퓨터에서 실행이 제한 되는 응용 프로그램을 지정할 수 있습니다. 이 문서에서는 앱-V 가상 환경 및 가상화 된 응용 프로그램과 함께 사용할 수 있도록 AppLocker 규칙을 구성 하는 방법을 설명 합니다.

**참고**  가상 응용 프로그램에 대해 Windows AppLocker 규칙을 구성 하기 전에 먼저 windows AppLocker를 사용 하도록 설정 해야 합니다. Windows applocker를 사용 하는 방법에 대 한 자세한 내용은 [Windows applocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## 가상 응용 프로그램에 대 한 Windows AppLocker 규칙 구성


로컬 관리자는 프로그램 실행 파일 (.exe 파일), Windows Installer 파일 (.msi 및 .msp 파일), 스크립트 (.ps, .bat, .cmd, .vbs, .js 파일)를 제한 하는 Windows AppLocker 규칙을 만들 수 있습니다. 관리자는 App-v 클라이언트가 설치 되어 있고 클라이언트 캐시로 스트리밍된 관련 된 모든 가상 응용 프로그램이 있는 참조 컴퓨터를 사용 하 여이를 수행 합니다. 그런 다음 관리자는 참조 컴퓨터에서 로컬 보안 정책 MMC (Microsoft Management Console) 스냅인의 Windows AppLocker 섹션을 사용 하 여 규칙을 만듭니다.

규칙을 만들려는 디렉터리 경로 또는 특정 파일을 검색 하는 경우 숨겨진 공유 경로를 사용 하 여 App-v 드라이브에 액세스할 수 있습니다. 예를 들어, \\\\localhost\\Q $로 이동할 수 있습니다. 여기서 App-v 드라이브는 drive Q입니다. 그러나 규칙을 만들려면 경로를 편집 하 여 \\\\localhost\\Q $에 대 한 참조를 제거 하 고 대신 Q:\\를 사용 해야 합니다. 응용 프로그램의 파일에 액세스 하려면 참조 컴퓨터에서 각 응용 프로그램을 시작 하 고 \\\\localhost\\Q $를 찾아보려면 관리자 권한이 필요 합니다.

 

 





