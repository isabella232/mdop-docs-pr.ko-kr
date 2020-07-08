---
title: 가상 응용 프로그램 패키지 추가 구성 요소
description: 가상 응용 프로그램 패키지 추가 구성 요소
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815078"
---
# 가상 응용 프로그램 패키지 추가 구성 요소


App-v Sequencer에서 64 비트 및 32 비트 실행 파일 및/또는 side-by-side 어셈블리에 종속 된 dll (동적 연결 라이브러리) 파일이 포함 된 디렉터리를 검색 했습니다. 일반적으로 시퀀서는 패키지에 사용 되는 모든 공용 어셈블리에 대해 전용 side-by-side 어셈블리를 만듭니다. 그러나 동일한 디렉터리에 32 비트 및 64 비트 버전의 전용 어셈블리를 만들 수는 없습니다.

Sequencer가 단일 충돌을 감지 하면 다음 작업을 수행 합니다.

-   디렉터리에 충돌이 있는지 여부에 관계 없이 전체 패키지에서 기존의 모든 64 비트 전용 어셈블리를 제거 합니다.

-   전용 side-by-side 어셈블리의 32 비트 버전만 만듭니다.

시퀀서를 실행 하는 컴퓨터와 모든 App-v 클라이언트 컴퓨터에 필요한 모든 64 비트 어셈블리의 공용 버전을 기본적으로 설치 해야 합니다.

필요한 기존 공용 어셈블리를 찾으려면 패키지가 저장 된 디렉터리를 열고 **VFS** 폴더를 확인 합니다. 예를 들어 패키지 루트가 **Q:\\MyApp**경우 응용 프로그램을 시퀀싱 하는 경우 **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** 을 찾아 기존 공용 어셈블리를 모두 찾습니다. 이러한 파일의 64 비트 버전은 항상 매니페스트 이름의 시작 부분에서 다음 텍스트로 시작 **됩니다.** 어셈블리의 정확한 이름과 버전은 연결 된 매니페스트 파일에서 찾을 수 있습니다.

다음 링크 중 하나를 사용 하 여 올바른 버전의 필수 구성 요소를 다운로드 하 고 설치 합니다.

-   [Microsoft Visual c + + 2005 재배포 가능 패키지 (x64)](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x64)](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [Microsoft Visual c + + 2008 재배포 가능 패키지 (x64)](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [Microsoft Visual c + + 2008 SP1 재배포 가능 패키지 (x64)](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





