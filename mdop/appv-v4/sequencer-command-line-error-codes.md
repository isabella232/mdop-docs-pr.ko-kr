---
title: Sequencer 명령줄 오류 코드
description: Sequencer 명령줄 오류 코드
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815558"
---
# Sequencer 명령줄 오류 코드


명령줄을 사용 하 여 응용 프로그램 시퀀싱 관련 오류를 식별 하는 데 도움이 되는 다음 목록을 사용 합니다. 연결 된 App-v 시퀀서 로그 파일을 보고이 정보를 볼 수도 있습니다.

**참고**  시퀀싱 하는 동안 여러 오류가 발생할 수 있으며,이 경우 표시 되는 오류 코드는 두 오류 코드의 합이 될 수 있습니다. 예를 들어 */InstallPath* 및 */OutputFile* 매개 변수가 없는 경우 app-v 시퀀서는 두 오류 코드의 합계인 **96**를 반환 합니다.

 

<a href="" id="01"></a>01  
알 수 없는 오류가 발생 했습니다.

<a href="" id="02"></a>02  
지정 된 설치 디렉터리 (/INSTALLPACKAGE)가 유효 하지 않습니다.

<a href="" id="04"></a>월  
지정 된 패키지 루트 디렉터리 (/INSTALLPATH)가 유효 하지 않습니다.

<a href="" id="08"></a>2008  
지정 된 */OutputFile* 매개 변수가 잘못 되었습니다.

<a href="" id="16"></a>16  
설치 디렉터리 (/INSTALLPACKAGE)가 지정 되어 있지 않습니다.

<a href="" id="32"></a>32  
/INSTALLPATH (package root directory)가 지정 되지 않았습니다.

<a href="" id="64"></a>64  
*/OutputFile* 매개 변수를 지정 하지 않았습니다.

<a href="" id="128"></a>128  
지정 된 application virtualization 드라이브가 유효 하지 않습니다.

<a href="" id="256"></a>256  
설치 관리자가 실패 했습니다.

<a href="" id="512"></a>512  
응용 프로그램 시퀀싱에 실패 했습니다.

<a href="" id="1024"></a>1024  
설치 된 바로 가기를 계산 하지 못했습니다.

<a href="" id="2048"></a>2048  
시퀀싱 된 응용 프로그램 패키지를 저장할 수 없습니다.

<a href="" id="4096"></a>4096  
지정 된 패키지 이름 (/PACKAGENAME)이 유효 하지 않습니다.

<a href="" id="8192"></a>8192  
지정 된 블록 크기 (/BLOCKSIZE)가 유효 하지 않습니다.

<a href="" id="16384"></a>16384  
지정 된 압축 유형 (/CCOMPRESSION)이 잘못 되었습니다.

<a href="" id="32768"></a>32768  
지정 된 프로젝트 경로가 잘못 되었습니다.

<a href="" id="65536"></a>65536  
지정 된 업그레이드 매개 변수가 잘못 되었습니다.

<a href="" id="131072"></a>131072  
지정 된 업그레이드 프로젝트 매개 변수가 잘못 되었습니다.

<a href="" id="262144"></a>262144  
지정 된 디코드 경로 매개 변수가 잘못 되었습니다.

<a href="" id="525288"></a>525288  
패키지 이름이 지정 되지 않았습니다.

## 관련 항목


[Application Virtualization Sequencer 참조](application-virtualization-sequencer-reference.md)

[Sequencer 명령줄 매개 변수](sequencer-command-line-parameters.md)

 

 





