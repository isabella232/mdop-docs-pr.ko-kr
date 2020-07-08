---
title: 설치 파일 페이지
description: 설치 파일 페이지
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816343"
---
# 설치 파일 페이지


**설치 파일** 페이지를 사용 하 여이 마법사의 **패키지 선택** 페이지에 지정 된 가상 응용 프로그램 패키지를 만드는 데 사용 된 설치 파일을 지정 합니다. 여러 응용 프로그램을 포함 하는 가상 응용 프로그램 패키지를 만든 경우에는 Microsoft Application Virtualization Sequencer를 실행 하는 컴퓨터의 단일 폴더에 필요한 모든 설치 파일을 복사 해야 합니다.

이 페이지에는 다음 요소가 포함 되어 있습니다.

<a href="" id="original-installation-files"></a>**원본 설치 파일**  
**찾아보기를** 클릭 하 여 가상 응용 프로그램 패키지를 만드는 데 사용 된 원래 설치 파일을 지정 합니다. 지정 하는 부모 디렉터리는 시퀀서를 실행 하는 컴퓨터에 로컬로 저장 해야 하며, 설치 파일을 포함 하는 필수 설치 파일 또는 하위 폴더가 모두 포함 되어 있어야 합니다. 설치 파일은 상위 폴더 또는 지정 된 상위 폴더의 하위 폴더에 포함 될 수 있습니다.

<a href="" id="files-installed-on-local-system"></a>**로컬 시스템에 설치 된 파일**  
**찾아보기를** 클릭 하 여 Sequencer를 실행 하는 컴퓨터에 로컬로 설치 된 설치 파일을 지정 합니다. 응용 프로그램 설치 파일이 응용 프로그램의 기본 위치에 설치 되어 있는 경우에만이 옵션을 선택할 수 있습니다.

**참고**  제공 하는 기본 설치 위치는 다음 조건에 따라 달라 집니다.

 

-   패키지를 처음 만들었을 때 지정 된 패키지 루트입니다.

-   패키지를 처음 만들었을 때 Windows Installer에 지정 된 설치 위치입니다.

-   기본 응용 프로그램 설치 경로입니다.

예를 들어 지정 된 패키지 루트가 **Q:\\Office12** 설치 하는 동안 기본 설치 위치가 **C:\\program files Files\\Office12** 에서 **Q:\\Office12**로 변경 되 면 디하이드레이션 중에 지정 된 경로가 **c:\\program files Files\\Office 12**여야 합니다.

지정 된 패키지 루트가 **Q:\\Microsoft** 설치 하는 동안 기본 설치 위치가 **C:\\program files Files\\Office12** 에서 **Q:\\Microsoft\\Office12**로 변경 된 경우 디하이드레이션 중에 지정 된 경로는 **c:\\program files 파일**이어야 합니다.

패키지 가속기를 사용 하 여 패키지를 만들 때 패키지 루트 **Q:\\Office12** 를 패키지 가속기를 만들 때 지정 된 기본 위치 (예: **c:\\program files Files\\Office12**)로 대체 하 여 로컬 컴퓨터에서 **Q:\\Office12\\file.txt** 있습니다. 앞의 예제에서 파일은 **c:\\program files Files\\Office12\\file.txt**에 위치 해야 합니다.

## 관련 항목


[패키지 가속기 만들기 마법사(App-V 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





