---
title: 패키지 속성을 변경하는 방법
description: 패키지 속성을 변경하는 방법
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818043"
---
# 패키지 속성을 변경하는 방법


다음 절차를 사용 하 여 응용 프로그램 가상화 패키지 이름과 관련 설명을 수정할 수 있습니다.

패키지를 처음으로 만든 경우 시퀀싱 된 응용 프로그램 패키지가 응용 프로그램 가상화 서버에서 응용 프로그램 가상화 데스크톱 클라이언트로 스트리밍되는 방법을 결정 하는 시퀀싱 매개 변수 블록 크기를 변경할 수도 있습니다.

**참고**  블록 크기를 선택할 때 SFT 파일과 네트워크 대역폭의 크기를 고려 합니다. 더 작은 블록 크기의 파일은 네트워크를 통해 스트리밍하는 데 더 오래 걸리므로 대역폭 사용량이 적습니다. 블록 크기가 더 많은 파일은 스트리밍할 수 있지만 더 많은 네트워크 대역폭을 사용 합니다. 실험을 통해 네트워크의 스트리밍 응용 프로그램에 대 한 최적의 블록 크기를 찾을 수 있습니다.

 

**속성** 탭의 나머지 패키지 속성은 자동으로 생성 되며이 탭에서 수정할 수 없습니다.

**패키지 이름 또는 설명을 변경 하려면**

1.  **속성** 탭을 클릭 합니다.

2.  **패키지 이름** 텍스트 상자에서 패키지에 사용 되는 단일 이름을 입력 하거나 편집 하 여 여러 응용 프로그램을 포함할 수 있습니다.

3.  **메모** 텍스트 상자에서 원하는 대로 메모를 입력 하거나 편집 합니다. 모범 사례는 패키지 및 시퀀싱에 대 한 자세한 정보를 제공 하는 것입니다.

4.  **파일** 메뉴에서 **저장**을 선택 합니다.

**블록 크기를 변경 하려면**

1.  **속성** 탭을 클릭 합니다.

2.  **블록 크기** 드롭다운 목록에서 4kb, **16kb**, **32 kb**또는 **64 KB** **를 선택 합니다**.

3.  **파일** 메뉴에서 **저장**을 선택 합니다.

## 관련 항목


[속성 탭 정보](about-the-properties-tab.md)

[Sequencer Console](sequencer-console.md)

 

 





