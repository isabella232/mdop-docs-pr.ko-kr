---
title: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
description: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822588"
---
# DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법


문제가 발생 하는 최종 사용자 컴퓨터에 컴퓨터를 설치 하는 경우 다음 지침을 사용 하 여 컴퓨터를 복구 합니다.

**DaRT 복구 이미지를 사용 하 여 로컬 컴퓨터를 복구 하는 방법**

1.  Microsoft 진단 및 복구 도구 집합 (DaRT) 10 복구 이미지를 사용 하 여 최종 사용자 컴퓨터를 부팅 합니다.

    컴퓨터가 DaRT 10 복구 이미지로 부팅 될 때 **Netstart** 대화 상자가 나타납니다.

2.  네트워크 서비스를 초기화할 것인지 묻는 메시지가 표시 되 면 다음 중 하나를 선택 합니다.

    **Yes** -DHCP 서버가 네트워크에 있고 서버에서 IP 주소를 가져오려고 시도 하는 것으로 가정 합니다. 네트워크에서 DHCP 대신 고정 IP 주소를 사용 하는 경우, 나중에 DaRT의 **Tcp/ip 구성** 도구를 사용 하 여 고정 ip 주소를 지정할 수 있습니다.

    **No** -네트워크 초기화 프로세스를 건너뜁니다.

3.  드라이브 문자를 다시 매핑할 것인지 여부를 나타냅니다. Windows online을 실행 하는 경우 시스템 볼륨은 일반적으로 C 드라이브에 매핑됩니다. 그러나 Windows를 오프 라인으로 WinRE에서 실행 하면 원래 시스템 볼륨이 다른 드라이브에 매핑될 수 있으며이로 인해 혼란이 발생할 수 있습니다. 다시 매핑하려는 경우 DaRT는 온라인 드라이브 문자와 일치 하도록 오프 라인 드라이브 문자를 매핑하려고 시도 합니다. 나중에 시작 프로세스에서 오프 라인 운영 체제를 선택한 경우에만 다시 매핑 처리가 수행 됩니다.

4.  **시스템 복구 옵션** 대화 상자에서 키보드 레이아웃을 선택 합니다.

5.  표시 된 시스템 루트 디렉터리, 설치 된 운영 체제 종류, 파티션 크기를 확인 합니다. 운영 체제가 나열 되지 않고 드라이버 부족으로 문제가 발생할 수 있다고 의심 되는 경우 **드라이버 로드** 를 클릭 하 여 의심 되는 드라이버를 로드 한 다음 장치에 대 한 설치 미디어를 삽입 하 고 드라이버를 선택 합니다.

6.  복구 하거나 진단 하려는 설치를 선택 하 고 **다음**을 클릭 합니다.

    **참고**  
    Windows 10 복구 환경 (WinRE)에서 마지막으로 시도 했을 때 Windows 10이 올바르게 시작 되지 않았다는 것을 감지 하거나 의심 되는 경우 **시동 복구가** 자동으로 실행 될 수 있습니다.



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. **시스템 복구 옵션** 창에서 **Microsoft 진단 및 복구 도구 집합**을 클릭 합니다.

   **진단 및 복구 도구 집합** 창이 열립니다. 이제 DaRT 복구 이미지를 만들 때 포함 된 개별 도구 또는 마법사를 실행할 수 있습니다.

**진단 및 복구 도구 집합** 창에서 **도움말** 을 클릭 하 여 개별 DaRT 도구를 실행 하는 데 필요한 자세한 지침과 정보를 제공 하는 클라이언트 도움말 파일을 열 수 있습니다. **진단 및 복구 도구 집합** 창에서 **솔루션 마법사** 를 클릭 하 여 마법사가 제공 하는 간략 한 인터뷰에 따라 상황에 가장 적합 한 도구를 선택할 수도 있습니다.

DaRT 도구에 대 한 일반적인 정보는 [dart 10의 도구 개요](overview-of-the-tools-in-dart-10.md)를 참조 하세요.

**명령 프롬프트에서 DaRT를 실행 하는 방법**

- 명령 프롬프트에서 DaRT를 실행 하려면 **netstart.exe** 명령을 지정 하 고 다음 매개 변수 중 하나를 사용 합니다.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong>매개 변수</strong></p></td>
  <td align="left"><p><strong>설명</strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-네트워크</p></td>
  <td align="left"><p>네트워크 서비스를 초기화 합니다.</p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p>-탑재</p></td>
  <td align="left"><p>드라이브 문자를 다시 매핑합니다.</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-프롬프트</p></td>
  <td align="left"><p>최종 사용자에 게 네트워크 초기화 및 드라이브 다시 매핑 여부를 지정 하도록 요청 하는 메시지를 표시 합니다.</p>
  <div class="alert">
  <strong>Warning</strong><br/><p>프롬프트에 대 한 최종 사용자의 응답은 – network 및 – 다시 탑재 스위치 보다 우선 합니다.</p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## 관련 항목


[DaRT 10 작업](operations-for-dart-10.md)

[DaRT 10을 사용하여 컴퓨터 복구](recovering-computers-using-dart-10.md)









