---
title: MED-V 작업 영역에 대한 자동 업데이트 관리
description: MED-V 작업 영역에 대한 자동 업데이트 관리
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825293"
---
# MED-V 작업 영역에 대한 자동 업데이트 관리


MED-V 작업 영역은 자동 소프트웨어 업데이트 프로세스가 엔터프라이즈의 실제 컴퓨터와 같이 관리 되어야 하는 별도의 운영 체제를 포함 하는 가상 컴퓨터입니다. 호스트 운영 체제를 실행할 때 항상 게스트 운영 체제가 실행 되는 것은 아니지만, 필요한 경우 게스트 운영 체제에 소프트웨어 업데이트를 적용할 수 있도록 MED-V 가상 컴퓨터가 구성 되어 있는지 확인 해야 합니다. Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 솔루션은 MED-V 작업 영역에서 자동 소프트웨어 업데이트가 처리 되는 방식을 결정할 수 있는 기능을 제공 합니다.

## MED-V 작업 영역 절전 모드 해제 정책 관리


MED-V 작업 영역 깨우기 정책은 med-v 구성 설정에서 지정 하는 시간 동안 MED-V 가상 컴퓨터를 업데이트할 수 있도록 보장 합니다. 이는 바이러스 백신 응용 프로그램과 같은 Microsoft 이외의 솔루션에서 배포 하 고 제어 하는 Windows Update 및 업데이트를 Microsoft에서 게시 한 두 가지 업데이트에 모두 적용 됩니다.

**중요**  MED-V 작업 영역 절전 모드 해제 정책은 Microsoft 업데이트 인프라에 최적화 되어 있습니다. Microsoft System Center Configuration Manager를 사용 하 여 타사 업데이트를 배포 하는 경우 Microsoft Update와 동일한 인프라를 활용 하는 System Center 업데이트 게시자를 사용 하는 것이 좋으며, 따라서 MED-V 작업 영역 웨이크업 정책의 혜택을 참조 하세요. 자세한 내용은 [System Center 업데이트 Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=200035) .

 

MED-V 작업 영역 패키지를 만들 때 최종 사용자가 로그온 할 때 (**빠른 시작**) 또는 최종 사용자가 게시 된 응용 프로그램 (**정상 시작**)을 처음으로 열 때 시작 되는 시간과 방법을 구성한 경우 또는 최종 사용자가이 설정을 제어할 수 있도록 하는 옵션을 설정 합니다.

어느 경우 든 **빠른 시작** 옵션을 선택 하면 Med-v 호스트가 사용자로 로그온 한 경우에만 가상 컴퓨터가 계속 실행 됩니다. 이 구성에서 호스트가 활성 상태일 때 MED-V가 활성화 되어 있으므로 MED-V에서 추가 처리를 요구 하지 않고 자동 업데이트가 적용 됩니다.

그러나 **빠른 시작** 이 지정 되지 않았거나 가상 컴퓨터가 최대 절전 모드 또는 중단 되는 경우 med-v는 med-v가 정기적으로 사용 되지 않더라도 게스트 운영 체제가 정기적으로 업데이트 되는 med-v 작업 영역의 절전 모드 해제 정책을 통해 보장 합니다. MED-V는 사용자가 지정 하는 구성 설정에 따라 가상 컴퓨터를 정기적으로 시작 하 여이 함수를 수행 합니다. 이렇게 하면 가상 컴퓨터의 자동 업데이트 클라이언트가 해당 구성에 따라 실행 될 수 있습니다.MED-V 구성 설정에 의해 정의 된 기간이 경과한 후에는 MED-V가 가상 컴퓨터를 이전 상태로 되돌립니다.

**참고**  최종 사용자가 업데이트 기간 동안 게시 된 응용 프로그램을 열면 필요한 업데이트가 적용 되지만 MED-V는 업데이트 기간이 종료 된 후 자동으로 hibernated 또는 종료 되지 않습니다. 대신 MED-V가 계속 실행 됩니다.

 

MED-V 작업 영역 절전 모드 해제 정책에는 다음과 같은 세 가지 기본 구성 요소가 포함 됩니다.

**게스트 업데이트 관리자**

MED-V 호스트에 거주 하는이 독립 실행형 실행 프로그램은 미리 정의 된 구성 가능한 일정에 따라 가상 컴퓨터의 절전 모드를 해제 하는 역할을 합니다. 업데이트 관리자가 매일 가상 컴퓨터를 종료 해야 하는 시간을 나타내는 구성 설정을 지정 하 고, 업데이트를 적용할 수 있도록 가상 컴퓨터를 활성 상태로 유지 해야 하는 기간 (분)을 표시 합니다. 지정 된 시간 (분)에 도달 하면 게스트 업데이트 관리자가 다음에 사용할 수 있도록 준비 되어 가상 컴퓨터를 최대 절전 모드로 전환 합니다. Windows 작업 관리자를 통해이 실행 프로그램의 실행을 예약할 수 있습니다.

**게스트 다시 시작 관리 서비스**

MED-V 호스트에 거주 하는이 서비스에는 세 가지 주요 책임이 있습니다. 게스트 업데이트 관리자와 함께 필요한 경우 사용자 로그온 시 가상 컴퓨터의 재시작을 관리 합니다. 업데이트 설치로 인해 가상 컴퓨터 다시 시작이 필요한 경우를 감지 합니다. 그러면 구성에 따라 게스트 업데이트 관리자의 작업이 항상 예약 됩니다.

**게스트 업데이트 서비스**

이 Windows 서비스는 MED-V 가상 컴퓨터에 설치 된 업데이트를 다시 시작 해야 하는 경우 모니터링을 담당 합니다. 서비스에서 다시 시작에 대 한 요구 사항이 발견 되 면 호스트에서 게스트 다시 시작 관리 서비스에 알립니다.

### MED-V 작업 영역 깨우기 정책에 대 한 구성 설정

레지스트리에 다음 두 가지 구성 값을 정의 하 여 가상 컴퓨터가 자동 업데이트를 수신 하는 시기 및 기간을 제어 합니다. awakens 이러한 값은 모두 HKLM\\Software\\Microsoft\\MEDV\\v2\\VM 키 아래에 있습니다.

**GuestUpdateTime** – 24 시간 시계 표준에 따라, med-v가 가상 컴퓨터를 업데이트 하기 위해 절전 모드를 해제 해야 하는 시간 및 분을 구성 합니다. HH: MM 형식으로 시간을 지정 합니다. 기본값은 00:00 (자정)입니다.

**GuestUpdateDuration** – med-v가 업데이트를 위해 가상 컴퓨터를 활성 상태로 유지 해야 하는 시간 (분)을 구성 합니다. GuestUpdateTime 구성 설정에 지정 된 시점부터 시작 합니다. 기본값은 240 (4 시간)입니다. 이 값을 0으로 설정 하면 MED-V 작업 영역 웨이크업 정책을 사용할 수 없습니다.

MED-V 구성 값을 정의 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)를 참조 하세요.

**참고**  MED-V 모범 사례는 MED-V 가상 컴퓨터가 정기적으로 업데이트 되도록 계획 되는 시간과 일치 하도록 절전 모드 종료 간격을 설정 하는 것입니다. 또한 호스트 컴퓨터의 동작과 비슷하게 이러한 설정을 구성 하는 것이 좋습니다.

 

### ESD 시스템을 사용한 재부팅 알림

자동 업데이트를 적용 한 후에 MED-V 작업 영역에 다시 시작이 필요할 때마다 사용자가 MED-V에 알리려면 ESD 시스템을 구성할 수 있습니다. ESD 시스템을 통해 다시 시작 해야 하는 자동 업데이트를 적용 하는 경우에는 MED-V 작업 영역에서 다음과 같은 전역 이벤트에 신호를 보내는 스크립트를 작성 해야 합니다.

**중요**  수정 전용 권한을 사용 하 여 이벤트를 열고 신호를 보내는 것이 필요 합니다. 올바른 사용 권한으로 열지 않은 경우에는 작동 하지 않습니다.

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

이 이벤트를 신호 하면 MED-V가 캡처를 캡처하여 가상 컴퓨터에 다시 시작이 필요 하다는 것을 알립니다.

## 관련 항목


[MED-V 작업 영역에 대한 소프트웨어 업데이트 관리](managing-software-updates-for-med-v-workspaces.md)

 

 





