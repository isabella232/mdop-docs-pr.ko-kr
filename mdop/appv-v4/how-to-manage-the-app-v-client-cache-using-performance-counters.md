---
title: 성능 카운터를 사용하여 App-V Client 캐시를 관리하는 방법
description: 성능 카운터를 사용하여 App-V Client 캐시를 관리하는 방법
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817133"
---
# 성능 카운터를 사용하여 App-V Client 캐시를 관리하는 방법


성능 모니터를 사용 하 여 정보를 그래픽으로 표시 하면 다음 절차를 사용 하 여 Application Virtualization (App-v) 클라이언트 캐시에서 사용할 수 있는 사용 가능한 공간을 확인할 수 있습니다. 이 정보는 "App Virt Client Cache" 라는 성능 카운터를 통해 클라이언트 컴퓨터에서 캡처되고 "캐시 크기 (MB)," "캐시 여유 공간 (MB)" 및 "사용 가능한 공간" 카운터를 포함 합니다.

**클라이언트 캐시 공간 사용량을 확인 하려면**

1.  관리자 권한으로 명령 프롬프트를 열거나 **시작**, **실행**을 클릭 한 다음 **perfmon.exe**입력 하 고 **확인**을 클릭 합니다.

2.  사용 중인 Windows 운영 체제에 따라 MMC 창이 열린 후 성능 모니터 또는 시스템 모니터 도구를 클릭 합니다.

3.  카운터를 추가 하려면 그래프 영역을 마우스 오른쪽 단추로 클릭 하 고 **카운터 추가**를 선택 합니다.

4.  드롭다운을 클릭 하 여 사용 가능한 카운터 목록을 표시 하 고 스크롤하여 **App Virt 클라이언트 캐시**를 찾은 다음 세 개의 카운터를 추가 합니다.

    **중요**  App-v 성능 카운터는 32 비트 DLL에서 구현 되므로이를 확인 하려면 다음 명령을 사용 하 여 32 비트 버전의 성능 모니터 ( **mmc/32 perfmon.exe**)를 시작 해야 합니다. 이 명령은 모니터링할 컴퓨터에서 직접 실행 해야 하며 64 비트 운영 체제를 실행 하는 원격 컴퓨터를 모니터링 하는 데 사용할 수 없습니다.

     

## 관련 항목


[명령줄을 사용하여 가상 응용 프로그램을 관리하는 방법](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





