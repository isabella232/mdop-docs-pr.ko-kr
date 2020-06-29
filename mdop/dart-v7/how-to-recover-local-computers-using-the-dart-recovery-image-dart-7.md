---
title: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
description: DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823763"
---
# DaRT 복구 이미지를 사용하여 로컬 컴퓨터를 복구하는 방법


Microsoft 진단 및 복구 도구 집합 (DaRT) 7을 사용 하 여 로컬 컴퓨터를 복구 하려면 DaRT가 필요한 문제가 발생 하는 최종 사용자 컴퓨터에 실제로 설치 되어 있어야 합니다. [Dart 복구 이미지를 사용 하 여 원격 컴퓨터를 복구 하는 방법](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)에 대 한 지침을 따라 원격으로 dart를 실행할 수도 있습니다.

**DaRT를 사용 하 여 로컬 컴퓨터를 복구 하려면**

1.  컴퓨터를 DaRT 복구 이미지로 부팅 하면 **Netstart** 대화 상자가 나타납니다. 네트워크 서비스를 초기화할 것인지 묻는 메시지가 표시 됩니다. **예**를 클릭 하면 DHCP 서버가 네트워크에 있고 서버에서 IP 주소를 가져오려고 시도 하는 것으로 간주 됩니다. 네트워크에서 DHCP 대신 고정 IP 주소를 사용 하는 경우, 나중에 DaRT의 **Tcp/ip 구성** 도구를 사용 하 여 고정 ip 주소를 지정할 수 있습니다.

    네트워크 초기화 프로세스를 건너뛰려면 **아니요**를 클릭 합니다.

2.  네트워크 초기화 대화 상자를 팔 로우 하는 경우 드라이브 문자를 다시 매핑할 것인지 묻는 메시지가 표시 됩니다. Windows online을 실행 하는 경우 시스템 볼륨은 일반적으로 C 드라이브에 매핑됩니다. 그러나 Windows를 오프 라인으로 WinRE에서 실행 하면 원래 시스템 볼륨이 다른 드라이브에 매핑될 수 있으며이로 인해 혼란이 발생할 수 있습니다. 다시 매핑하려는 경우 DaRT는 온라인 드라이브 문자와 일치 하도록 오프 라인 드라이브 문자를 매핑하려고 시도 합니다. 나중에 시작 프로세스에서 오프 라인 운영 체제를 선택한 경우에만 다시 매핑 처리가 수행 됩니다.

3.  다시 매핑 대화 상자 다음에는 **시스템 복구 옵션** 대화 상자가 나타나고 키보드 레이아웃을 선택 하 라는 메시지가 표시 됩니다. 그러면 시스템 루트 디렉터리, 설치 된 운영 체제 종류 및 파티션 크기가 표시 됩니다. 운영 체제가 나열 되지 않고 드라이버 부족으로 문제가 발생할 수 있다고 의심 되는 경우 **드라이버 로드** 를 클릭 하 여 의심 되는 드라이버를 로드 합니다. 장치에 대 한 설치 미디어를 삽입 하 고 드라이버를 선택 하 라는 메시지가 표시 됩니다. 복구 하거나 진단 하려는 설치를 선택 하 고 **다음**을 클릭 합니다.

    **참고**  
    WinRE (Windows 복구 환경)에서 Windows 7을 마지막으로 시도 했을 때 올바르게 시작 되지 않았다는 것을 감지 하거나 의심 되는 경우 **시동 복구** 는 자동으로 실행 되기 시작 될 수 있습니다.



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. **시스템 복구 옵션** 창에서 **Microsoft 진단 및 복구 도구 집합**을 클릭 합니다.

   **진단 및 복구 도구 집합** 창이 열립니다. 이제 DaRT 복구 이미지를 만들 때 포함 된 개별 도구 또는 마법사를 실행할 수 있습니다.

**진단 및 복구 도구 집합** 창에서 **도움말** 을 클릭 하 여 개별 DaRT 도구를 실행 하는 데 필요한 자세한 지침과 정보를 제공 하는 클라이언트 도움말 파일을 열 수 있습니다. **진단 및 복구 도구 집합** 창에서 **솔루션 마법사** 를 클릭 하 여 마법사가 제공 하는 간략 한 인터뷰에 따라 상황에 가장 적합 한 도구를 선택할 수도 있습니다.

DaRT 도구에 대 한 일반적인 정보는 [dart 7.0의 도구 개요](overview-of-the-tools-in-dart-70-new-ia.md)를 참조 하세요.

**명령 프롬프트에서 DaRT를 실행 하려면**

1. 명령 프롬프트에서 **netstart.exe** 명령을 지정 하 고 다음 매개 변수를 사용 하 여 DaRT를 실행할 수 있습니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">매개 변수</th>
   <th align="left">설명</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>-네트워크</p></td>
   <td align="left"><p>네트워크 서비스를 초기화 합니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>-탑재</p></td>
   <td align="left"><p>드라이브 문자를 다시 매핑합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>-프롬프트</p></td>
   <td align="left"><p>최종 사용자에 게 네트워크 초기화 및 드라이브 다시 매핑 여부를 지정 하 라는 메시지를 표시 합니다.</p>
   <div class="alert">
   <strong>중요</strong><br/><p>메시지에 대 한 최종 사용자의 응답은-network 및-탑재 스위치를 재정의 합니다.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Dart로 부팅 하는 컴퓨터가 지원 센터와의 원격 연결을 설정 하는 데 사용 되는 **원격 연결** 도구를 자동으로 열려면 dart를 사용자 지정할 수 있습니다.

## 관련 항목


[DaRT 7.0를 사용하여 컴퓨터 복구](recovering-computers-using-dart-70-dart-7.md)









