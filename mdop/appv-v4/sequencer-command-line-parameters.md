---
title: Sequencer 명령줄 매개 변수
description: Sequencer 명령줄 매개 변수
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815553"
---
# Sequencer 명령줄 매개 변수


다음 Application Virtualization (App-v) Sequencer 매개 변수를 사용 하 여 응용 프로그램을 시퀀싱 하 고 명령줄을 사용 하 여 기존 가상 응용 프로그램을 업그레이드할 수 있습니다. 명령줄을 사용 하 여 응용 프로그램을 시퀀싱 하는 방법에 대 한 자세한 내용은 [명령줄을 사용 하 여 새 응용 프로그램을 시퀀스 하는 방법](how-to-sequence-a-new-application-by-using-the-command-line.md)을 참조 하세요.

## Sequencer 명령줄 매개 변수


<a href="" id="-help-or---"></a>**/HELP 또는/?**  
명령줄을 사용 하 여 응용 프로그램을 시퀀싱 하는 데 사용할 수 있는 매개 변수에 대 한 정보를 표시 합니다.

<a href="" id="-installpackage-or--i"></a>**/INSTALLPACKAGE 또는/I**  
시퀀싱 될 수 있도록 응용 프로그램을 설치 하는 데 사용 되는 Windows Installer 또는 배치 파일을 지정 합니다.

<a href="" id="-installpath-or--p"></a>**/INSTALLPATH 또는/P**  
응용 프로그램에 대 한 패키지 루트 디렉터리를 지정 합니다.

<a href="" id="-outputfile-or--o"></a>**/OUTPUTFILE 또는/O**  
생성 될 SPRJ 파일의 경로와 파일 이름을 지정 합니다.

<a href="" id="-fullload-or--f"></a>**/FULLLOAD 또는/F**  
모든 파일을 기본 기능 블록에 포함할 것인지 여부를 지정 합니다. 명령줄에 **/FULLLOAD** 매개 변수를 지정 하면 연결 된 모든 응용 프로그램 데이터가 기본 기능 블록에 추가 됩니다. 명령줄에서 **/FULLLOAD** 매개 변수를 지정 하지 않으면 연결 된 응용 프로그램 데이터가 기본 기능 블록에 모두 추가 되지 않습니다.

<a href="" id="-packagename-or--k"></a>**/PACKAGENAME 또는/K**  
시퀀싱 된 응용 프로그램에 할당 될 패키지 이름을 지정 합니다.

<a href="" id="-blocksize"></a>**/BLOCKSIZE**  
패키지를 클라이언트 컴퓨터로 스트리밍하는 데 사용 되는 SFT 파일 블록 크기를 지정 합니다. 다음 값 중 하나를 선택할 수 있습니다.

-   4KB

-   16kb

-   32 KB

-   64 KB

블록 크기를 지정할 때 SFT 파일의 크기를 고려해 야 합니다. 더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다. 블록 크기가 더 많은 파일은 더 많은 네트워크 대역폭을 사용 합니다.

<a href="" id="-compression"></a>**/C압축**  
클라이언트로 스트리밍할 SFT 파일을 압축 하는 방법을 지정 합니다.

<a href="" id="-msi-or--m"></a>**/MSI 또는/M**  
시퀀싱 된 응용 프로그램에 대 한 Windows Installer를 만들지 여부를 지정 합니다.

<a href="" id="-default"></a>**/DEFAULT**  
가상 응용 프로그램 패키지를 만들 때 사용 되는 기본 SPRJ 파일을 지정 합니다. 이 파일은 응용 프로그램을 처음으로 시퀀싱 하는 경우 sprj 템플릿으로 사용 됩니다.

<a href="" id="-upgrade"></a>**/UPGRADE**  
업그레이드 될 SPRJ 파일의 경로와 파일 이름을 지정 합니다.

<a href="" id="-decodepath"></a>**/DECODEPATH**  
시퀀싱 하는 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지와 관련 된 파일이 설치 된 디렉터리를 지정 합니다. 디렉터리를 지정할 때 다음 형식 중 하나를 사용 합니다.

-   /decodepath: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /decodepath: "Q:"

## 관련 항목


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Sequencer 명령줄 오류 코드](sequencer-command-line-error-codes.md)

 

 





