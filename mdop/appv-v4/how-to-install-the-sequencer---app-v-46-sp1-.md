---
title: Sequencer를 설치 하는 방법 (App-v 4.6 SP1)
description: Sequencer를 설치 하는 방법 (App-v 4.6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817273"
---
# Sequencer를 설치 하는 방법 (App-v 4.6 SP1)


Microsoft App-v (Application Virtualization) Sequencer는 응용 프로그램을 가상 응용 프로그램으로 실행할 수 있도록 응용 프로그램의 설치 및 설정 프로세스를 모니터링 하 고 기록 합니다. 운영 체제만 설치 되어 있는 컴퓨터에는 App-v Sequencer를 설치 해야 합니다. 또는 가상 환경 (예: 가상 컴퓨터)에서 실행 되는 컴퓨터에 시퀀서를 설치할 수 있습니다. 이 방법은 최소한의 추가 구성으로 다시 사용할 수 있는 깨끗 한 시퀀싱 환경을 유지 관리 하는 것이 더 쉽기 때문에 유용 합니다.

응용 프로그램을 시퀀싱 하는 데 사용 하는 컴퓨터에 대 한 관리자 자격 증명이 있어야 하 고, 컴퓨터는 모든 버전의 App-v 클라이언트를 실행 하지 않아야 합니다. App-v 시퀀서를 사용 하 여 가상 응용 프로그램을 만들려면 여러 작업을 수행 해야 하므로 [Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항을](application-virtualization-sequencer-hardware-and-software-requirements.md)충족 하거나 초과 하는 컴퓨터에 시퀀서를 설치 하는 것이 중요 합니다.

**참고**  
안전 모드에서 App-v 시퀀서를 실행 하는 것은 지원 되지 않습니다.



**Microsoft Application Virtualization Sequencer를 설치 하려면**

1.  설치 하려는 컴퓨터에 Microsoft Application Virtualization Sequencer 설치 파일을 복사 합니다.

2.  Microsoft Application Virtualization Sequencer 설치 마법사를 시작 하려면 **Setup.exe**를 두 번 클릭 합니다. 설치 전에 **Microsoft Visual c + + SP1 재배포 가능 패키지 (x86)** 가 검색 되지 않는 경우 **설치** 를 클릭 하 여 필수 구성 요소를 설치 합니다.

3.  설치를 계속 하려면 **시작** 페이지에서 **다음**을 클릭 합니다.

4.  **사용권 계약 페이지에서** 사용권 계약 약관에 동의 하는 경우 **동의**함을 클릭 하 고 **다음**을 클릭 합니다.

5.  **대상 폴더** 페이지에서 기본 설치 폴더를 그대로 사용 하려면 **다음**을 클릭 합니다. 다른 대상 폴더를 지정 하려면 **변경을** 클릭 하 고 설치에 사용 될 설치 폴더를 지정 합니다. **다음**을 클릭합니다.

6.  **가상 드라이브** 페이지에서 응용 프로그램 가상화 기본 드라이브 **Q:\\** (기본값)를 모든 시퀀싱 된 응용 프로그램이 실행 되는 드라이브로 구성 하려면 **다음**을 클릭 합니다. 다른 드라이브 문자를 지정 하려면 목록을 사용 하 고 적절 한 드라이브 문자를 선택 하 여 사용할 드라이브 문자를 선택한 후 **다음**을 클릭 합니다.

    **중요**  
    이 단계에서 지정 하는 Application Virtualization 드라이브 문자는 가상 응용 프로그램이 대상 컴퓨터에서 실행 되는 드라이브 문자입니다. 지정 된 드라이브 문자를 사용할 수 있어야 하며, 현재 App-v 클라이언트를 실행 하는 컴퓨터에서 사용 중이 아니어야 합니다. 지정 된 드라이브가 이미 사용 중인 경우 가상 응용 프로그램은 대상 컴퓨터에서 실패 합니다.



7.  **프로그램 설치 준비** 페이지에서 설치를 시작 하려면 **설치**를 클릭 합니다.

8.  **InstallShield 마법사 완료** 페이지에서 설치 마법사를 닫고 app-v Sequencer를 열려면 **마침을**클릭 합니다. Sequencer를 열지 않고 설치 마법사를 닫으려면 **프로그램 실행**을 선택 취소 하 고 **마침을**클릭 합니다.

    **참고**  
    가상 환경을 실행 하는 컴퓨터 (예: 가상 컴퓨터)에 App-v 시퀀서를 설치한 경우 이제 스냅숏을 만들어야 합니다. 응용 프로그램을 순서 대로 만들면 다음 응용 프로그램의 순서를 지정할 수 있도록이 이미지로 되돌릴 수 있습니다.



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## 관련 항목


[Application Virtualization Sequencer(App-V 4.6 SP1) 구성](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









