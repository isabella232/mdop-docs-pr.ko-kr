---
title: UE-V 1.0에 지원되는 구성
description: UE-V 1.0에 지원되는 구성
author: dansimp
ms.assetid: d90ab83e-741f-48eb-b1d8-a64cb9259f7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a84514317de8a4cfd9df9c94a9a130933b00874a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825553"
---
# UE-V 1.0에 지원되는 구성


Microsoft UE-V (User Experience Virtualization)는 다음의 설명 된 구성을 지원 합니다.

**참고**  Microsoft는 현재 서비스 팩 및 일부 경우에는 이전 서비스 팩에 대 한 지원을 제공 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.

 

## UE-V 에이전트 및 UE-V 생성기에 대해 지원 되는 구성


다음 표에는 사용자 환경 가상화 생성기 및 사용자 환경 가상화 에이전트를 지 원하는 운영 체제가 나와 있습니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>운영 체제</strong></th>
<th align="left"><strong>버전</strong></th>
<th align="left"><strong>서비스 팩</strong></th>
<th align="left"><strong>시스템 아키텍처</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate, Enterprise 또는 Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>.NET Framework 3.5 SP1</p>
<p>.NET Framework 4 (생성기)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>.NET Framework 3.5 SP1</p>
<p>.NET Framework 4 (생성기)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>엔터프라이즈 또는 전문가 판</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>.NET Framework 4 또는 .NET Framework 3.5 SP1 (에이전트)</p>
<p>.NET Framework 4 (생성기)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>.NET Framework 4 또는 .NET Framework 3.5 SP1 (에이전트)</p>
<p>.NET Framework 4 (생성기)</p></td>
</tr>
</tbody>
</table>

 

UE-V와 관련 된 특수 한 RAM 요구 사항은 없습니다.

UE-V agent를 설치 하려면 관리자 권한이 필요 하며, UE-V 에이전트를 실행 하려면 먼저 컴퓨터를 다시 시작 해야 합니다.

**중요**  UE-V가 올바르게 작동할 수 있도록 Windows 8의 설정 동기화 기능을 사용 하지 않도록 설정 해야 합니다. Windows 8 및 UE-V를 사용 하 여 설정을 동기화 하면 예기치 않은 동기화 동작이 발생 합니다.

 

### <a href="" id="requirements-for-the-offline-files-feature-"></a>오프 라인 파일 기능에 대 한 요구 사항

UE-V 에이전트는 VDI (가상 데스크톱 인터페이스) 세션을 호스트 하는 Windows 서버와 같이 엔터프라이즈 네트워크에 항상 연결 되는 컴퓨터와 같이 엔터프라이즈 네트워크에 항상 연결 되어 있지 않은 컴퓨터 (예: 랩톱 컴퓨터 또는 원격 사무실에 있는 컴퓨터)에 대 한 사용자 설정을 동기화 할 수 있습니다.

UE-V 기본 구성은 Windows 오프 라인 파일 기능을 사용 하 여 설정을 동기화 합니다. 오프 라인 파일은 컴퓨터에서 엔터프라이즈 네트워크를 떠날 때도 사용자의 설정을 사용할 수 있는지 확인 합니다. 설정에 대 한 변경 내용은 엔터프라이즈 네트워크에 대 한 연결을 다시 설정할 때 설정 저장소 위치와 자동으로 동기화 됩니다. 또한 오프 라인 파일은 연결이 느리거나 제한 된 원격 사무실에 있는 컴퓨터에 대해 사용자의 설정을 사용할 수 있도록 보장 합니다.

가끔 엔터프라이즈 네트워크를 종료 하는 컴퓨터의 설정을 동기화 하려면 오프 라인 파일 기능을 사용 하도록 설정 하 고 UE-V 에이전트 배포가 시작 되기 전에 시작 해야 합니다. Windows7에서 오프 라인 파일 기능은 기본적으로 사용 하도록 설정 되어 있습니다. Windows Server2008R2, Windows Server 2012 및 Windows 8에서는 기본적으로이 기능을 사용할 수 없습니다. 오프 라인 파일 기능을 사용 하도록 설정 하지 않은 경우 UE-V 설정 동기화가 실패 합니다.

-   **Windows 7**

    Windows 7에서 오프 라인 파일 기능은 기본적으로 사용 하도록 설정 되어 있습니다. 필요한 경우 관리자 권한 명령 프롬프트에서 다음 명령을 사용 하 여 오프 라인 파일을 사용 하도록 설정할 수 있습니다.

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows8**

    Windows 8 버전에서는 오프 라인 파일 기능이 기본적으로 비활성화 되어 있습니다. 관리자 권한 명령 프롬프트에서 다음 명령을 사용 하 여 Windows 8에서 오프 라인 파일을 사용 하도록 설정할 수 있습니다.

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows Server 2008 R2 및 Windows Server 2012**

    오프 라인 파일 기능은 Windows Server 2008 R2 또는 Windows Server 2012에 기본적으로 설치 되지 않습니다. 오프 라인 파일 기능을 사용 하도록 설정 하려면 데스크톱 경험 팩을 설치 해야 합니다. 오프 라인 파일 기능을 포함 하는 선택적 서버 구성 요소입니다. 설치 된 후에는 관리자 권한 명령 프롬프트에서 다음 명령을 사용 하 여 오프 라인 파일 기능을 시작 합니다.

    ``` syntax
    sc config csc start= system
    ```

    ``` syntax
    sc config cscservice start= auto
    ```

설정 동기화를 시작 하기 전에 컴퓨터를 다시 부팅 해야 합니다.

### 항상 사용 가능한 연결이 있는 컴퓨터 동기화

VDI 세션을 호스트 하는 Windows Server 컴퓨터와 같이 항상 엔터프라이즈 네트워크에 연결 된 컴퓨터에서 UE-V를 사용 하는 경우 오프 라인 파일을 사용 하지 않도록 설정 해야 합니다.

UE-V agent가 오프 라인 파일을 사용 하지 않고 설정을 동기화 하도록 구성 된 경우 설정 저장소 서버는 표준 네트워크 공유로 처리 됩니다. 네트워크를 사용할 수 있게 되 면 설정이 동기화 됩니다. 이 구성에서는 응용 프로그램 설정 가져오기가 지연 되는 경우 알림을 제공 하도록 UE-V agent를 구성할 수 있습니다.

오프 라인 파일 기능을 사용 하지 않을 경우 UE-V 에이전트 배포 전 또는 동안 UE-V 기본 동작을 사용 하지 않도록 설정 해야 합니다. UE-V의 오프 라인 파일을 사용 하지 않도록 설정 하려면 다음 중 하나를 수행 합니다.

-   UE-V agent를 배포 하기 전에 UE-V 그룹 정책 설정에서 "오프 라인 파일을 사용 하지 않음" 확인란을 표시 합니다.

-   UE-V를 설치 하는 동안 `SyncMethod = None` 명령 프롬프트나 배치 파일에서 AgentSetup.exe 매개 변수를 설정 합니다. 에이전트를 배포 하는 방법에 대 한 자세한 내용은 [Ue-v 에이전트 배포](deploying-the-ue-v-agent.md)를 참조 하세요.

UE-V에 대 한 오프 라인 파일 설정을 사용 하지 않도록 설정 하 고 설치 하는 동안 **Syncmethod** 매개 변수를 지정 하지 않으면 ue-v agent가 설치 되지 않습니다. 또한 PowerShell 또는 WMI를 사용 하 여 오프 라인 파일을 사용 하지 않도록 설정할 수 있습니다. WMI 및 PowerShell 명령에 대 한 자세한 내용은 [powershell 및 WMI를 사용 하 여 ue-v 1.0 에이전트 및 패키지 관리](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)를 참조 하세요.

설정 동기화를 시작 하기 전에 컴퓨터를 다시 부팅 해야 합니다.

### UE-V PowerShell 기능에 대 한 필수 조건

에이전트의 UE-V PowerShell 기능을 사용 하려면 .NET Framework 버전 3.5 SP1이 활성화 되 고 PowerShell 버전 2.0 이상이 필요 합니다.

### UE-V 생성기 지원에 대 한 필수 조건

사용자 지정 설정 위치 서식 파일을 만드는 데 사용 되는 컴퓨터에 UE-V 생성기를 설치 합니다. 이 컴퓨터에는 설정을 로밍할 수 있는 응용 프로그램이 설치 되어 있어야 합니다. UE-V 생성기 소프트웨어를 실행 하는 컴퓨터에서 관리자 그룹의 구성원 이어야 합니다. 또한, UE-V 생성기는 NTFS 파일 시스템을 사용 하는 컴퓨터에 설치 해야 합니다. UE-V 생성기 소프트웨어에는 .NET Framework 버전 4가 필요 합니다. 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.

## 관련 항목


[UE-V 1.0 계획](planning-for-ue-v-10.md)

[UE-V용 환경 준비](preparing-your-environment-for-ue-v.md)

[UE-V 1.0 배포](deploying-ue-v-10.md)

[Ue-v 1.0의 설정 저장소 위치를 배포 하는](deploying-the-settings-storage-location-for-ue-v-10.md) 사용자 환경 가상화에 대해 지원 되는 구성

[UE-V 생성기 설치](installing-the-ue-v-generator.md)

[UE-V 에이전트 배포](deploying-the-ue-v-agent.md)

 

 





