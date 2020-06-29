---
title: Sequencer 보안 계획
description: Sequencer 보안 계획
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815913"
---
# Sequencer 보안 계획


시퀀서 구현이 작동 하 고 더 안전 하 게 유지 되도록 Application Virtualization (App-v)을 구성할 때 권장 되는 구현 방법을 최대한 일찍 통합 합니다. 시퀀서를 이미 구성한 경우에는 다음 모범 사례 지침을 사용 하 여 디자인 결정을 다시 검토 하 고 보안 측면에서 분석 합니다.

**중요**  
App-v 시퀀서는 Sequencer를 실행 하는 컴퓨터에 기록 된 모든 응용 프로그램 정보를 수집 하 고 배포 합니다. 시퀀서를 실행 하는 컴퓨터에 액세스 하는 모든 사용자에 게 관리 자격 증명이 있는지 확인 해야 합니다. 사용자 계정 자격 증명을 사용 하는 사용자는 패키지 콘텐츠 및 패키지 파일을 제어 하는 데 액세스할 수 없습니다. 원격 데스크톱 서비스 (이전의 터미널 서비스)를 실행 하는 컴퓨터에서 시퀀싱 하는 경우 시퀀싱을 전담 하는 컴퓨터이 고 사용자 계정 자격 증명이 있는 사용자가 시퀀싱 중에 연결 되지 않았는지 확인 합니다.



## Sequencer 보안 모범 사례


App-v (Application Virtualization) Sequencer를 구현 하 고 사용할 때 다음과 같은 시나리오와 관련 모범 사례를 고려 하세요.

-   **Sequencer를 실행 하는 컴퓨터에서 바이러스를 검색**하는 경우, sequencer를 실행 하는 컴퓨터에서 바이러스를 검색 한 다음 시퀀싱 프로세스 중 시퀀서를 실행 하는 컴퓨터에서 모든 바이러스 백신 및 맬웨어 감지 소프트웨어를 사용 하지 않도록 설정 하는 것이 좋습니다. 이렇게 하면 시퀀싱 프로세스가 속도를 빠르게 하 고 바이러스 백신 및 맬웨어 방지 소프트웨어 구성 요소가 시퀀싱 프로세스를 방해 하지 않습니다. 다음으로 시퀀서를 실행 하지 않는 컴퓨터에 시퀀싱 된 패키지를 설치 하 고 설치가 완료 되 면 해당 컴퓨터에서 바이러스를 검사 합니다. 바이러스가 발견 되 면 감염 된 원본 파일을 알리기 위해 소프트웨어 제조업체에 문의 하 고 바이러스 없이 업데이트 된 설치 원본을 요청 해야 합니다. 선택적으로 설치 단계 후에 시퀀서를 검색할 수 있으며, 바이러스가 발견 되는 경우 소프트웨어 제조업체에는 위에서 설명한 대로 연락 해야 합니다.

    **참고**  
    응용 프로그램에서 바이러스가 검색 되는 경우 대상 컴퓨터에 응용 프로그램을 배포할 수 없습니다.



-   **Ntfs 파일에서 acl (액세스 제어 목록)을 캡처하**는 경우 App-v 시퀀서는 제품을 설치 하는 동안 모니터링 되는 파일에 대 한 ntfs 파일 시스템 권한을 캡처합니다. 이 접근 권한 값을 통해 응용 프로그램의 의도 된 동작을 로컬로 설치 하 고 가상화 되지 않은 것 처럼 정확 하 게 복제할 수 있습니다. 일부 시나리오에서는 응용 프로그램에서 사용자가 응용 프로그램 파일 내에서 액세스 하지 않은 정보를 저장할 수 있습니다. 예를 들어 응용 프로그램은 응용 프로그램 내의 파일에 자격 증명 정보를 저장할 수 있습니다. 패키지에 Acl이 적용 되지 않으면 사용자가 볼 수 있으며,이 정보를 응용 프로그램 외부에서 사용할 수도 있습니다.

    **참고**  
    암호 등의 암호화 되지 않은 보안 관련 정보를 저장 하는 응용 프로그램은 시퀀싱 하지 않아야 합니다.



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   **Sequencer는 레지스트리 acl을 캡처하지**않지만, 시퀀싱을 설치 하는 동안 NTFS 파일 시스템 acl을 캡처 하더라도 레지스트리에 대 한 acl을 캡처하지 않습니다. 사용자는 서비스를 제외 하 고 가상 응용 프로그램의 모든 레지스트리 키에 대 한 전체 액세스 권한을 갖습니다. 그러나 사용자가 가상 응용 프로그램의 레지스트리를 수정 하는 경우, 변경 내용이 특정 매장 (**uservol \ _v1 _sftfs installer.pkg**)에 저장 되며 다른 사용자에 게 영향을 주지 않습니다.

-   **응용 프로그램 서비스**-app-v는 가상화 된 응용 프로그램의 일부인 응용 프로그램 서비스에 대 한 지원을 제공 합니다. 그러나 가상 환경에서는 해당 환경이 실행 되는 보안 컨텍스트가 제한 됩니다. 가상 환경에서 지원 되는 유일한 보안 컨텍스트는 로컬 시스템, 로컬 서비스 및 네트워크 서비스입니다. 시퀀싱 하는 동안 3 가지 지원 되지 않는 응용 프로그램 서비스에 대해 보안 컨텍스트를 지정한 경우 로컬 시스템 보안 컨텍스트가 가상 환경에 적용 됩니다. 응용 프로그램 서비스가 로컬 서비스 또는 네트워크 서비스를 사용 하도록 구성 된 경우에는 가상 환경에서 허용 됩니다. 이 세 가지 보안 컨텍스트를 사용 하 여 시퀀싱 프로세스 중에 서비스 계정을 구성 하는 작업이 가능 합니다.

-   **유지 된 보안 정보**— 응용 프로그램을 시퀀싱 하는 경우 사용자가 응용 프로그램을 설치할 수 있으며, 모니터링 하는 동안 응용 프로그램을 설치 하기 위한 자동화 된 방법을 개발할 수 있습니다. 패키지에서 제외 되지 않는 모든 내용은 해당 패키지의 일부로 캡처 되어 응용 프로그램에 가상화 된 환경에서 실행 하는 데 필요한 자산을 포함 시킵니다. 일부 응용 프로그램은 설치 중에 중요 한 보안 정보 (예: 암호)를 저장 합니다. 보호 되지 않은 상태로 유지 되는 경우 해당 패키지에 대 한 액세스 권한이 있는 다른 사용자가이 보안 정보에 액세스할 수 있습니다. 설치 중에 응용 프로그램 설치가 암호 또는 기타 보안 관련 정보를 요청 하는 경우 설명서를 참조 하 여 유지 되지 않았거나 (설치 후 제거 됨), 유지 되는 경우 보호 (암호화) 되어 있는지 확인 합니다.

-   **가상 응용 프로그램 패키지 보안**-패키지가 무단으로 또는 손상 되는 것을 방지 하기 위해 항상 네트워크의 안전한 위치에 가상 응용 프로그램 패키지를 저장 합니다.

## 관련 항목


[보안 및 보호 계획](planning-for-security-and-protection.md)









