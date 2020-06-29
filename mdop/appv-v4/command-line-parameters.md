---
title: 명령줄 매개 변수
description: 명령줄 매개 변수
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819403"
---
# 명령줄 매개 변수


다음 응용 프로그램 가상화 시퀀서 매개 변수를 사용 하 여 응용 프로그램을 시퀀싱 하 고 명령 프롬프트에서 시퀀싱 된 응용 프로그램 패키지를 업그레이드 합니다. Microsoft Application Virtualization Sequencer 디렉터리에서 **Sftsequencer**를 입력 한 다음 적절 한 매개 변수를 입력 합니다.

<a href="" id="-help-or---"></a>*/Help* 또는 */?*  
명령줄 시퀀싱에 사용할 수 있는 매개 변수 목록을 표시 하는 데 사용 합니다.

<a href="" id="-installpackage-or--i"></a>*/INSTALLPACKAGE* 또는 */i*  
시퀀싱 될 응용 프로그램의 배치 파일 또는 설치 관리자를 지정 하는 데 사용 합니다.

<a href="" id="-installpath-or--p"></a>*/INSTALLPATH* 또는 */p*  
패키지 루트 디렉터리를 지정 하는 데 사용 합니다.

<a href="" id="-outputfile-or--o"></a>*/OUTPUTFILE* 또는 */o*  
생성 되는 SPRJ 파일의 경로와 파일 이름을 지정 하는 데 사용 합니다.

**중요**  */OUTPUTFILE* 매개 변수는 업그레이드 하지 않으려는 패키지를 여는 경우에는 사용할 수 없습니다.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* 또는 */f*  
모든 것을 기본 기능 블록에 넣을지 여부를 지정 하는 데 사용 합니다.

<a href="" id="-packagename-or--k"></a>*/Packagename* 또는 */k*  
시퀀싱 된 응용 프로그램의 패키지 이름을 지정 하는 데 사용 합니다.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
패키지를 클라이언트 컴퓨터로 스트리밍하는 데 사용 되는 SFT 파일 블록 크기를 지정 합니다. 다음 값 중 하나를 선택할 수 있습니다.

-   4KB

-   16kb

-   32 KB

-   64 KB

블록 크기를 지정할 때 SFT 파일의 크기를 고려해 야 합니다. 더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다. 블록 크기가 더 많은 파일은 더 많은 네트워크 대역폭을 사용 합니다.

<a href="" id="-compression"></a>*/C압축*  
SFT 파일을 클라이언트로 스트리밍할 때 압축 하는 방법을 지정 하는 데 사용 합니다.

<a href="" id="-msi-or--m"></a>*/MSI* 또는 */m*  
시퀀싱 된 응용 프로그램에 대 한 Microsoft Windows Installer 패키지 생성을 지정 하는 데 사용 합니다.

<a href="" id="-default"></a>*/DEFAULT*  
가상 응용 프로그램 패키지를 만들 때 사용 되는 기본 SPRJ 파일을 지정 합니다. 이 파일은 응용 프로그램을 처음으로 시퀀싱 하는 경우 sprj 템플릿으로 사용 됩니다.

<a href="" id="-upgrade"></a>*/UPGRADE*  
업그레이드 될 SPRJ 파일의 경로와 파일 이름을 지정 합니다.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
시퀀싱 하는 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지와 관련 된 파일이 설치 된 디렉터리를 지정 합니다. 디렉터리를 지정할 때 다음 형식 중 하나를 사용 합니다.

-   /decodepath: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /decodepath: "Q:"

## 관련 항목


[Sequencer 명령줄 사용 정보](about-using-the-sequencer-command-line.md)

[명령줄을 사용하여 시퀀싱된 응용 프로그램을 여는 방법](how-to-open-a-sequenced-application-using-the-command-line.md)

[패키지 열기 명령을 사용하여 패키지를 업그레이드하는 방법](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





