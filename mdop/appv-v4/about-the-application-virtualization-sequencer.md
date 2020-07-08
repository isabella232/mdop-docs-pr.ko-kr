---
title: Application Virtualization Sequencer 정보
description: Application Virtualization Sequencer 정보
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819998"
---
# Application Virtualization Sequencer 정보


Microsoft App-v (Application Virtualization) Sequencer는 응용 프로그램의 모든 설치 및 설정 프로세스를 모니터링 하 고 기록 하 고, **.ico**, **OSD**, **SFT**, **SPRJ**파일을 만듭니다. 이러한 파일에는 응용 프로그램에 대 한 모든 필수 정보가 포함 되어 있으므로 대상 컴퓨터의 가상 환경에서 응용 프로그램을 실행할 수 있습니다. Microsoft Application Virtualization (App-v) Sequencer를 사용 하 여 가상 응용 프로그램을 만들 수 있습니다. 응용 프로그램을 시퀀싱 한 후 대상 컴퓨터로 스트리밍할 수 있으며 가상 응용 프로그램 패키지의 콘텐츠를 다운로드 하 고 응용 프로그램을 로컬로 실행 하 여 대상 컴퓨터에서 가상 응용 프로그램을 실행할 수 있습니다.

**중요**  가상 응용 프로그램 패키지를 실행 하려면 대상 컴퓨터가 App-v 클라이언트의 적절 한 버전을 실행 해야 합니다.

 

가상 응용 프로그램 패키지는 각 응용 프로그램이 가상 환경에서 실행 되 고 대상 컴퓨터에 설치 되거나 실행 되는 다른 응용 프로그램과 격리 되므로 대상 컴퓨터의 기본 운영 체제와 상호 작용 하지 않고 대상 컴퓨터에서 실행 됩니다. 이러한 격리는 응용 프로그램 충돌을 줄일 수 있으며 필요한 응용 프로그램 사전 배포 테스트의 양을 줄이는 데 도움이 될 수 있습니다.

## Sequencer 용어


<a href="" id="application-virtualization-drive"></a>Application Virtualization 드라이브  
응용 프로그램 가상화 드라이브는 시퀀싱 된 응용 프로그램이 실행 되는 대상 컴퓨터의 기본 드라이브 (Q:\)입니다.

<a href="" id="ico-file"></a>.ICO 파일  
시퀀싱 된 응용 프로그램을 시작 하는 데 사용 되는 클라이언트 데스크톱의 아이콘 파일입니다.

<a href="" id="installation-directory"></a>설치 디렉터리  
설치 하는 동안 sequencer에서 설치 파일을 배치 하는 데 사용 되는 디렉터리입니다.

<a href="" id="open-software-descriptor--osd--file"></a>OSD (개방형 소프트웨어 설명자) 파일  
App-v 클라이언트에 app-v 스트리밍 서버에서 시퀀싱 된 응용 프로그램을 검색 하는 방법과 가상 환경에서 시퀀싱 된 응용 프로그램을 실행 하는 방법에 대해 설명 하는 XML 기반 파일입니다.

<a href="" id="package-root-directory"></a>패키지 루트 디렉터리  
시퀀싱 한 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지의 파일이 설치 된 디렉터리입니다. 이 디렉터리는 시퀀싱 된 응용 프로그램이 스트리밍되는 컴퓨터에도 사실상 존재 합니다.

<a href="" id="sequenced-application"></a>시퀀싱 응용 프로그램  
시퀀서에서 모니터링 하는 응용 프로그램을 기본 및 보조 기능 블록으로 분할 하 고, App-v 클라이언트 t를 실행 하는 대상 컴퓨터로 스트리밍 하 고, 가상 환경을 실행 합니다.

<a href="" id="sequenced-application-package"></a>시퀀싱 되는 응용 프로그램 패키지  
가상 응용 프로그램을 구성 하 고 가상 응용 프로그램을 실행할 수 있는 파일입니다. 이러한 파일은 시퀀싱, **sft**, **sprj**, **.ico** 파일을 순서 **대로 포함 하**여 생성 됩니다.

<a href="" id="sequencing"></a>시퀀스  
App-v 시퀀서를 사용 하 여 응용 프로그램 패키지를 만드는 프로세스입니다. 이 프로세스에서는 응용 프로그램이 모니터링 되 고 해당 바로 가기가 구성 되며 시퀀싱 된 응용 프로그램 패키지가 만들어집니다.

<a href="" id="sequencing-computer"></a>시퀀싱 컴퓨터  
응용 프로그램을 시퀀싱 하는 데 사용 되는 컴퓨터입니다.

<a href="" id="virtual-application"></a>가상 응용 프로그램  
시퀀서에 의해 패키지 된 응용 프로그램을 자체 포함 가상 환경에서 실행 합니다. 가상 환경에는 응용 프로그램을 로컬로 설치 하지 않고 클라이언트에서 응용 프로그램을 실행 하는 데 필요한 정보가 포함 됩니다.

<a href="" id="primary-feature-block"></a>기본 기능 블록  
대상 컴퓨터에서 응용 프로그램을 실행 하는 데 필요한 가상 응용 프로그램 패키지의 최소 콘텐츠입니다. 기본 기능 블록의 콘텐츠는 시퀀싱 하는 응용 프로그램 단계에서 식별 되며 일반적으로 사용 되는 응용 프로그램 기능에 대 한 콘텐츠로 구성 됩니다.

## <a href="" id="sequencing-applications-"></a>시퀀싱 응용 프로그램


환경에서 가상 응용 프로그램 패키지를 만들고 수정 하는 방법에는 두 가지가 있습니다. 첫 번째 방법은 **시퀀싱** 마법사를 사용 하는 것입니다. **시퀀싱** 마법사를 사용 하 여 새로 만들거나 기존 가상 응용 프로그램 패키지를 수정할 수 있습니다. **시퀀싱** 마법사를 사용 하는 방법에 대 한 자세한 내용은 [새 응용 프로그램을 시퀀싱 하는 방법](how-to-sequence-a-new-application.md)을 참조 하세요. 두 번째 방법은 명령줄을 사용 하는 것입니다. 명령줄에서 명령 프롬프트를 사용 하 여 새를 만들거나 기존 가상 응용 프로그램 패키지를 수정할 수 있습니다. 명령줄을 사용 하는 방법에 대 한 자세한 내용은 [명령줄을 사용 하 여 가상 응용 프로그램을 관리 하는 방법](how-to-manage-virtual-applications-using-the-command-line.md)을 참조 하세요.

**시퀀싱** 마법사는 가상 응용 프로그램 패키지를 만들기 위해 다음과 같은 함수를 제공 합니다.

1.  **패키지 구성**: **시퀀싱** 마법사는 시퀀싱 된 응용 프로그램 패키지를 시작 하는 데 필요한 파일인 OSD (Open Software Descriptor) 파일을 완료 하는 데 필요한 패키지 구성 정보에 대 한 메시지를 표시 합니다.

2.  **응용 프로그램 설치**: **시퀀싱** 마법사는 응용 프로그램의 설치 및 시작 구성에 대 한 정보를 수집 합니다. 이 프로그램은 응용 프로그램과 관련 된 설치 및 시작 정보를 모니터링 하 고 기록 하 여 가상 응용 프로그램 패키지에 필요한 파일을 만듭니다.

3.  **응용 프로그램 시작**: **시퀀싱** 마법사는 대상 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지의 초기 시작을 수행 하는 데 필요한 코드 블록을 컴파일하고 정렬 하기 위한 정보를 수집 합니다. 코드 블록의 컴파일은 기본 기능 블록 이라고 합니다.

## Application Virtualization Sequencer 보안 고려 사항


App-v Sequencer는 로컬 시스템 계정을 사용 하 여 시퀀싱 시간에 검색 된 모든 서비스를 실행 하 고 서비스 제어 요청에 보안 설명자를 적용 하지 않습니다. 다른 사용자 계정을 사용 하 여 서비스를 설치 했거나 보안 설명자가 다른 사용자 그룹 특정 서비스 권한을 부여 하려는 경우 서비스를 가상화 해야 하는지 신중히 고려해 야 합니다. 의도 하지 않은 서비스 보안이 유지 되도록 서비스를 로컬로 설치 해야 하는 경우도 있습니다.

**중요**  가상 응용 프로그램 패키지는 항상 안전한 위치에 저장 해야 합니다.

 

## 관련 항목


[Application Virtualization Sequencer 개요](application-virtualization-sequencer-overview.md)

 

 





