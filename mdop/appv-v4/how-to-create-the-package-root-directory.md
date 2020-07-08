---
title: 패키지 루트 디렉터리를 만드는 방법
description: 패키지 루트 디렉터리를 만드는 방법
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817628"
---
# 패키지 루트 디렉터리를 만드는 방법


패키지 루트 디렉터리는 시퀀싱 된 응용 프로그램의 파일이 설치 된 App-v 시퀀서를 실행 하는 컴퓨터의 디렉터리입니다. 이 디렉터리는 시퀀싱 된 응용 프로그램이 스트리밍되는 컴퓨터에도 사실상 존재 합니다. 새 응용 프로그램의 설치를 모니터링 하기 전에 패키지 루트 디렉터리를 만들어야 합니다.

패키지 루트 디렉터리를 만든 후에는 응용 프로그램 시퀀싱을 시작할 수 있습니다. 새 응용 프로그램을 시퀀싱 하는 방법에 대 한 자세한 내용은 [Sequencer 설치 방법을](how-to-install-the-sequencer.md)참조 하세요.

**패키지 루트 디렉터리를 만들려면**

1.  패키지 루트 디렉터리를 만들려면 App-v Sequencer를 실행 하는 컴퓨터에서 Q:\\ 드라이브를 지정 된 네트워크 위치로 매핑합니다. 시퀀싱 하는 응용 프로그램을 저장할 충분 한 공간이 지정 된 위치입니다.

2.  새 가상 응용 프로그램에 사용할 수 있는 디렉터리를 만들려면 Q:\\ 드라이브에 폴더를 만들고 이름을 지정 합니다.

    **중요**  패키지 루트 디렉터리에 저장 되는 가상 응용 프로그램 파일에 할당 하는 이름은 8.3 명명 형식을 사용 해야 합니다. 파일 이름은 8 자 미만 이어야 하며, 파일 이름 확장명은 3 자로 제한 됩니다.

     

## 관련 항목


[Application Virtualization Sequencer에 대한 작업](tasks-for-the-application-virtualization-sequencer.md)

 

 





