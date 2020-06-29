---
title: MED-V 2.0 모범 사례
description: MED-V 2.0 모범 사례
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826113"
---
# MED-V 2.0 모범 사례


엔터프라이즈에서 MED-V를 계획, 배포 및 관리 하는 경우 유용한 모범 사례를 찾을 수 있습니다.

### 자동으로 설치 프로그램을 실행 하도록 구성

원하는 설정을 지정할 수 있지만, 처음에는 설치 프로그램을 **무인** 모드로 실행할 수 있도록 sysprep.inf 파일을 만드는 것이 좋습니다. 이렇게 하려면 **설치 관리자** 마법사를 계속 진행할 때 필요한 모든 설정 정보를 제공 해야 합니다. MED-V 이미지를 구성 하는 방법에 대 한 자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.

### 가상 머신에서 복원 지점 사용 안 함

MED-V 작업 영역 패키지를 만들기 전에 가상 컴퓨터에서 복원 지점을 사용 하지 않도록 설정 하 여 차이점 보관용 디스크에 대 한 무제한 연결을 방지 하는 것이 좋습니다. 자세한 내용은 [WINDOWS XP ()에서 시스템 복원을 해제 하 고 설정 하는 방법](https://go.microsoft.com/fwlink/?LinkId=195927) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195927) .

### 로컬 프로필을 사용 하도록 MED-V 이미지 구성

Windows XP에 대 한 응용 프로그램 호환성 환경에 적합 한 정책만 적용 하는 것이 좋습니다. 예를 들어 데스크톱 사용자 지정 정책을 일반적으로 적용할 필요는 없으며 사용 하지 않도록 설정 해야 합니다. 로컬 프로필만 허용 하는 방법에 대 한 자세한 내용은 [로밍 사용자 프로필 ()에 대 한 그룹 정책 설정](https://go.microsoft.com/fwlink/?LinkId=205072) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=205072) .

### 그룹 정책 성능 업데이트 구성

기본적으로 그룹 정책은 한 번에 1 바이트씩 컴퓨터에 다운로드 됩니다. 이로 인해 MED-V가 도메인에 가입 되어 있는 경우 지연이 발생할 수 있습니다. 그룹 정책의 성능을 높이려면 다음 레지스트리 키 값을 레지스트리로 설정 하는 것이 좋습니다.

레지스트리 하위 키: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

진입: BufferPolicyReads

형식: DWORD

값: 1

### MED-V 이미지 대신 그룹 정책을 통해 법적 고 지 사항 배포

최종 사용자가 MED-V에 액세스 하기 전에 SLA (서비스 수준 계약)를 표시 하도록 하려면 나중에 그룹 정책을 통해 SLA를 적용 하 여 처음 설치 완료 후 최종 사용자에 게 SLA가 표시 되도록 하는 것이 좋습니다.

**주의**  사항 **무인** 모드에서 처음 설치를 실행 하는 것이 좋지만 이미지 (가상 하드 디스크)에 SLA를 포함 하도록 로컬 정책 또는 레지스트리 항목을 설정 하는 경우 첫 번째 설정이 **유인** 모드로 실행 되도록 하거나 처음 설치 하는 데 실패할 수 있는지도 지정 해야 합니다.

 

### 가상 하드 디스크 압축

가상 하드 디스크를 압축 하 여 빈 디스크 공간을 확보 하 고 가상 하드 디스크의 크기를 줄이는 것이 좋습니다. 가상 하드 디스크를 압축 하는 방법에 대 한 자세한 내용은 [Med-v 가상 하드 디스크 압축](compacting-the-med-v-virtual-hard-disk.md)을 참조 하세요.

### 파란색 화면 손상으로 다시 시작 하도록 가상 컴퓨터 구성

파란색 화면 충돌이 발생할 경우 MED-V 작업 영역 가상 컴퓨터를 자동으로 다시 시작 하도록 구성 하는 것이 좋습니다. 게스트에서이 설정을 구성 하려면 HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl 키의 AutoReboot 값을 "1"로 설정 합니다.

**시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **시스템**을 클릭 하 여이 설정을 구성할 수도 있습니다. 그런 다음 **고급** 탭의 **시작 및 복구** 영역에서 **설정을**클릭 합니다. **자동으로 다시 시작** 확인란을 선택 하 고 **확인**을 클릭 합니다.

### 밀봉 하기 전에 MED-V 이미지 백업

봉인 하기 전에 MED-V 이미지의 백업 복사본을 만드는 것이 좋습니다. MED-V 이미지를 봉인 하는 방법에 대 한 자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.

### 배치 파일에서 설치 하는 경우 마지막으로 Windows Virtual PC 설치

배치 파일을 사용 하 여 MED-V 구성 요소를 설치 하는 경우 MED-V 호스트 에이전트 및 MED-V 작업 영역 패키지 파일 뒤에 Windows 가상 PC 및 Windows 가상 PC 핫픽스가 설치 되도록 지정 합니다. 이렇게 하면 Windows Update는 다시 시작을 요구 하 여 설치 프로세스에 간섭이 발생 하지 않도록 할 수 있습니다.

### 로컬 폴더에서 MED-V 작업 영역 설치

네트워크 위치에서 MED-V를 설치할 때 발생할 수 있는 문제 때문에 MED-V 작업 영역 설정 파일을 로컬로 복사한 다음 setup.exe를 실행 하는 것이 좋습니다.

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a>한 가지 방법 으로만 프린터 리디렉션 관리

프린터가 MED-V 게스트 가상 컴퓨터에 수동으로 설치 되어 있고 나중에 호스트 컴퓨터에 동일한 프린터가 설치 되어 있으면 게스트에 두 번 설치 된 것입니다. 이 문제를 방지 하려면 리디렉션을 사용 하지 않도록 설정 하 고 게스트에 수동으로 프린터를 설치 하거나 리디렉션을 사용 하도록 설정 하거나 게스트에 수동으로 프린터를 설치 하지 않는 등 한 가지 방법 으로만 프린터 리디렉션을 관리 하는 것이 좋습니다.

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a>MED-V 게스트 패치 설정 구성

MED-V 가상 컴퓨터가 레지스트리에서 관련 구성 값을 정의 하 여 자동 업데이트를 수신 하는 시기와 기간을 제어할 수 있습니다. awakens MED-V 모범 사례는 MED-V 가상 컴퓨터에 대 한 정기 업데이트를 예약한 시간과 일치 하도록 절전 모드 해제 간격을 설정 하는 것입니다. 또한 호스트 컴퓨터의 동작과 비슷하게 이러한 설정을 구성 하는 것이 좋습니다.

MED-V 게스트 패치 설정을 구성 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역에 대 한 자동 업데이트 관리](managing-automatic-updates-for-med-v-workspaces.md)를 참조 하세요.

### 바이러스 백신/백업 소프트웨어 구성

바이러스 백신 활동이 가상 데스크톱의 성능에 영향을 주지 않도록 하려면, MED-V 호스트 컴퓨터에서 실행 중인 바이러스 백신 또는 백업 프로세스에서 다음 가상 컴퓨터 파일 형식을 제외 하는 것이 좋습니다.

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. .VHD

## 관련 항목


[MED-V에 대한 보안 및 보호](security-and-protection-for-med-v.md)

 

 





