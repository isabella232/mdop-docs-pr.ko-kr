---
title: MED-V에 대한 Windows 가상 PC 이미지 만들기
description: MED-V에 대한 Windows 가상 PC 이미지 만들기
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812684"
---
# MED-V에 대한 Windows 가상 PC 이미지 만들기


MED-V 작업 영역을 사용자에 게 제공 하기 전에 MED-V (Microsoft 엔터프라이즈 데스크톱 가상화) 2.0에 대 한 MED-V 작업 영역 설치 관리자 패키지를 빌드하는 데 사용 하는 가상 하드 디스크를 먼저 준비 해야 합니다. 필요한 가상 하드 디스크를 준비 하려면 나중에 응용 프로그램 및 URL 리디렉션 정보를 사용자에 게 배포할 수 있도록 필요한 운영 체제, 업데이트 및 소프트웨어를 포함 하는 Windows 가상 PC 이미지를 만들어야 합니다. 이 섹션에서는 가상 하드 디스크를 만드는 방법에 대 한 지침을 제공 합니다.

MED-V에 대 한 가상 이미지를 만들려면 다음 단계를 수행 해야 합니다.

1.  [Windows 가상 PC 이미지 만들기](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [이미지에 Windows XP 설치](#bkmk-installingwindowsxpontovpc)

3.  [이미지에 .NET Framework 설치](#bkmk-installingnet)

4.  [이미지에 업데이트 적용](#bkmk-applypatchestovpc)

5.  [통합 구성 요소 설치](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Windows 가상 PC 이미지 만들기


Windows 가상 PC 이미지를 만들려면 Windows 가상 PC 설명서를 참조 하세요.

-   [Windows 가상 PC 홈 페이지](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .

-   [Windows 가상 PC 도움말](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

또는 가상 이미지의 기준으로 사용할 Windows Imaging (WIM) 파일이 이미 있는 경우이를 MED-V 작업 영역을 빌드하는 데 사용 하는 VHD로 변환할 수 있습니다. WIM을 가상 하드 디스크로 변환 하는 방법에 대 한 자세한 내용은 [Windows 7 ()의 기본 VHD 지원](https://go.microsoft.com/fwlink/?LinkId=195922) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195922) .

**중요**  MED-V는 가상 컴퓨터당 하나의 가상 하드 디스크만 지원 하 고 각 가상 디스크에는 하나의 파티션만 있습니다.

 

가상 하드 디스크를 만들었으면 이미지에 Windows XP를 설치 합니다.

## <a href="" id="bkmk-installingwindowsxpontovpc"></a>Windows 가상 PC 이미지에 Windows XP 설치


MED-V를 사용 하려면 MED-V 작업 영역을 빌드하기 전에 windows XP SP3이 Windows 가상 PC 이미지에 설치 되어 있어야 합니다.

Windows XP를 설치 하는 방법에 대 한 자세한 내용은 [가상 컴퓨터 만들기 및 게스트 운영 체제 설치](https://go.microsoft.com/fwlink/?LinkId=182379) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=182379) .

## <a href="" id="bkmk-installingnet"></a>Windows 가상 PC 이미지에 .NET Framework 3.5 SP1 설치


.NET Framework 3.5 SP1 및 업데이트 KB959209을 MED-V와 함께 사용 하기 위해 준비 하는 Windows 가상 PC 이미지에 수동으로 설치 해야 합니다. 업데이트 [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) 알려진 여러 응용 프로그램 호환성 문제를 해결 합니다.

## <a href="" id="bkmk-applypatchestovpc"></a>Windows 가상 PC 이미지에 업데이트 적용


가상 컴퓨터에 Windows XP를 설치한 후에는 SP3 등의 이미지에 필요한 Windows XP 업데이트를 설치 합니다. 더 나은 성능을 위해 특정 선택적 업데이트를 설치할 수도 있습니다.

**중요**  MED-V를 사용 하려면 게스트 운영 체제에서 Windows XP SP3을 실행 해야 합니다.

 

**경고가**  Windows XP에 대 한 업데이트를 설치 하는 경우 MED-V 작업 영역에서 사용 하려는 게스트의 Internet Explorer 버전에 남아 있는지 확인 합니다. 예를 들어 MED-V 작업 영역에서 Internet Explorer 6을 실행 하려는 경우 지금 설치 하는 업데이트에는 Internet Explorer 7 또는 Internet Explorer 8이 포함 되어 있지 않은지 확인 합니다. 또한 자동 업데이트가 Internet Explorer를 업그레이드 하지 못하도록 레지스트리를 구성 하는 것이 좋습니다.

 

### 선택적 성능 업데이트 설치

이 기능은 선택 사항 이지만 [핫픽스 KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ()에 대해 다음 업데이트를 설치 하는 것이 좋습니다 https://go.microsoft.com/fwlink/?LinkId=201077) . 이 업데이트는 터미널 서비스 세션에서 공유 폴더의 성능을 향상 시킵니다.

**참고**  업데이트를 공개적으로 사용할 수 있습니다. 그러나 Microsoft 서비스에 대 한 계약을 수락 하 라는 메시지가 표시 될 수 있습니다. 후속 웹 페이지의 메시지에 따라이 핫픽스를 검색 합니다.

 

### 그룹 정책 성능 업데이트 구성

기본적으로 그룹 정책은 한 번에 1 바이트씩 컴퓨터에 다운로드 됩니다. 이로 인해 MED-V가 도메인에 가입 되어 있는 동안 지연이 발생할 수 있습니다. 그룹 정책의 성능을 높이려면 다음 레지스트리 키 값을 레지스트리로 설정 합니다.

레지스트리 하위 키: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

진입: BufferPolicyReads

형식: DWORD

값: 1

## <a href="" id="bkmk-installintegration"></a>통합 구성 요소 설치


Windows 가상 PC에는 통합 구성 요소 패키지가 포함 됩니다. 가상 환경과 물리적 컴퓨터 간의 상호 작용을 개선 하는 기능을 제공 합니다. 예를 들어 통합 구성 요소 패키지는 마우스를 호스트와 게스트 컴퓨터 간에 이동할 수 있도록 합니다.

**중요**  MED-V는 통합 구성 요소 패키지를 설치 해야 합니다.

 

MED-V와 함께 작동 하도록 가상 이미지를 구성 하는 경우 게스트 운영 체제에 통합 구성 요소 패키지를 수동으로 설치 하 여 통합 기능을 사용할 수 있도록 해야 합니다.

통합 구성 요소 패키지를 설치 하 고 사용 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.

-   [통합 구성 요소 패키지 설치 또는 업그레이드](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .

-   [통합 기능](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .

### RemoteApp 업데이트 설치

통합 구성 요소 패키지를 설치한 후 다음 업데이트를 설치 하 라는 메시지가 표시 됩니다. "Windows XP SP3 용 업데이트: RemoteApp 사용" 이는 MED-V에 필요한 구성 요소입니다.

**중요**  RemoteApp 업데이트를 설치 하 라는 메시지가 표시 되지 않는 경우 수동으로 다운로드 하 여 설치 해야 합니다. 이 업데이트를 다운로드 하는 방법에 대 한 자세한 내용과 지침은 [RemoteApp을 사용 하도록 설정 하는 WINDOWS XP SP3 업데이트](https://go.microsoft.com/fwlink/?LinkId=195925) (.)를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195925) .

 

### 원격 데스크톱 사용

통합 구성 요소 패키지를 설치한 후 원격 데스크톱이 기본적으로 사용 하도록 설정 됩니다. MED-V가 작동 하도록 하려면 원격 데스크톱을 사용 하도록 설정 하 고 사용 하지 않도록 설정 하는 그룹 정책을 배포 하지 않도록 해야 합니다.

원격 데스크톱을 사용 하도록 설정 하는 방법에 대 한 자세한 내용은 [원격 데스크톱 사용 또는 사용 안 함](https://go.microsoft.com/fwlink/?LinkId=201162) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=201162) .

## Internet Explorer 관리 키트를 사용 하 여 Internet Explorer 사용자 지정


원하는 경우 Internet Explorer 관리 키트를 사용 하 여 게스트 운영 체제에서 Internet Explorer를 사용자 지정할 수 있습니다. 자세한 내용은 [Internet Explorer 6 관리 키트 및 배포 가이드](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.microsoft.com/fwlink/?LinkId=200007)를 참조 하세요.

**경고가**  MED-V 작업 영역에서 Internet Explorer를 사용자 지정 하는 것과 관련 된 보안 문제를 고려해 야 합니다. 자세한 내용은 [Med-v 작업에 대 한 보안 모범 사례](security-best-practices-for-med-v-operations.md)를 참조 하세요.

 

가상 하드 디스크가 최신 게스트 운영 체제로 설치 되 면 이미지에 응용 프로그램을 설치할 수 있습니다.

## 관련 항목


[Windows 가상 PC 이미지에 응용 프로그램 설치](installing-applications-on-a-windows-virtual-pc-image.md)

[MED-V에 대한 Windows 가상 PC 이미지 구성](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





