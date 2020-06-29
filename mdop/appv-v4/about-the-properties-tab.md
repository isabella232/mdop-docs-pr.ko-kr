---
title: 속성 탭 정보
description: 속성 탭 정보
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819923"
---
# 속성 탭 정보


**속성** 탭을 사용 하 여 시퀀싱 된 응용 프로그램 패키지에 대 한 기본 통계 정보를 볼 수 있습니다. 다른 언급이 없는 한 정보가 자동으로 생성 됩니다. 이 탭에는 다음 요소가 포함 되어 있습니다.

## 패키지 정보


<a href="" id="package-name"></a>**패키지 이름**  
하나 이상의 응용 프로그램을 포함할 수 있는 시퀀싱 된 응용 프로그램 패키지에 사용 되는 단일 이름 (예: Microsoft Office를 사용 하 여 동일한 가상 환경에서 실행 되는 Microsoft Word 및 Microsoft Excel 응용 프로그램을 포함 하는 시퀀싱 된 응용 프로그램 패키지에 레이블을 지정할 수 있음)

<a href="" id="comments"></a>**설명**  
OSD (Open Software Descriptor) 파일 추상 요소에 표시 되는 소프트웨어 패키지에 대 한 간략 한 설명을 표시 합니다. 이 항목은 선택 사항입니다.

<a href="" id="package-version"></a>**패키지 버전**  
시퀀싱 된 응용 프로그램 패키지 버전입니다.

<a href="" id="package-guid"></a>**패키지 GUID**  
시퀀싱 된 응용 프로그램 패키지를 스트리밍하는 컴퓨터에서 실행 될 수 있는 다른 시퀀싱 된 응용 프로그램 패키지와 구분 하기 위해 자동으로 순차적으로 지정 되는 전역 고유 식별자 (GUID)입니다.

<a href="" id="package-version-guid"></a>**패키지 버전 GUID**  
시퀀싱 된 응용 프로그램 패키지 버전 GUID입니다.

<a href="" id="root-directory"></a>**루트 디렉터리**  
시퀀싱 한 컴퓨터에서 시퀀싱 된 응용 프로그램 패키지의 파일이 설치 된 디렉터리입니다. 이 디렉터리는 또한 시퀀싱 된 응용 프로그램 패키지가 스트리밍되는 컴퓨터에서 생성 됩니다. 이전 버전과의 호환성을 위해 Q:\\MyApp.1\\.와 같은 Q 드라이브의 루트에 있는 8.3 형식 디렉터리 이름 이어야 하는 것이 좋습니다.

<a href="" id="created"></a>**만들어져야**  
시퀀싱 된 응용 프로그램 패키지를 만든 날짜와 시간입니다.

<a href="" id="modified"></a>**수정됨**  
시퀀싱 된 응용 프로그램 패키지가 마지막으로 수정 된 날짜 및 시간입니다.

<a href="" id="package-size"></a>**패키지 크기**  
패키지의 크기 (mb)입니다.

<a href="" id="launch-size"></a>**시작 크기**  
응용 프로그램을 시작 하는 데 필요한 SFT 파일 부분의 크기 (mb)입니다.

## 시퀀싱 매개 변수


<a href="" id="block-size"></a>**블록 크기**  
네트워크에서 스트리밍을 위해 SFT 파일을 나눌 기본 및 보조 기능 블록의 크기를 지정 합니다. 모든 블록은 지정 된 크기와 동일 합니다. 그러나 마지막 블록이 지정 된 것 보다 작을 수 있습니다. 다음 값 중 하나가 표시 됩니다.

-   4KB

-   16kb

-   32 KB

-   64 KB

**참고**  초기 패키지를 만든 후에는 블록 크기 값을 변경할 수 없습니다.

 

## 관련 항목


[패키지 속성을 변경하는 방법](how-to-change-package-properties.md)

[Sequencer Console](sequencer-console.md)

 

 





