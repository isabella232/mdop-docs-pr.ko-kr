---
title: App-V 5.1 Sequencer 및 Client 배포
description: App-V 5.1 Sequencer 및 Client 배포
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814569"
---
# App-V 5.1 Sequencer 및 Client 배포


Microsoft App-v (Application Virtualization) 5.1 시퀀서 및 클라이언트를 사용 하 여 관리자가 가상화 된 응용 프로그램을 가상화 하 고 실행할 수 있습니다.

## 클라이언트 배포


앱-V 5.1 클라이언트는 대상 컴퓨터에서 가상화 된 응용 프로그램을 실행 하는 구성 요소입니다. 클라이언트를 통해 사용자는 아이콘과 상호 작용 하 고 파일 형식을 두 번 클릭 하 여 가상화 된 응용 프로그램을 시작할 수 있습니다. 클라이언트는 관리 서버에서 가상 응용 프로그램 콘텐츠를 가져올 수도 있습니다.

[App-V Client 배포 방법](how-to-deploy-the-app-v-client-51gb18030.md)

[App-V 5.1 Client 제거 방법](how-to-uninstall-the-app-v-51-client.md)

[앱-V 4.6 및 앱-V 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## 클라이언트 구성 설정


앱-V 5.1 클라이언트는 레지스트리에 구성을 저장 합니다. 레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다. 레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.

[클라이언트 구성 설정 정보](about-client-configuration-settings51.md)

## ADMX 템플릿 및 그룹 정책을 사용 하 여 클라이언트 구성


Microsoft ADMX 서식 파일을 사용 하 여 App-v 5.1 클라이언트 및 원격 데스크톱 서비스 클라이언트에 대 한 클라이언트 설정을 구성할 수 있습니다. ADMX 템플릿은 기존 그룹 정책 인프라를 사용 하 여 일반적인 클라이언트 구성을 관리 하며 App-v 5.1 클라이언트 구성에 대 한 설정을 포함 합니다.

**중요**  Microsoft 다운로드 센터에서 앱-V 5.1 ADMX 서식 파일을 얻을 수 있습니다.

 

ADMX 서식 파일을 다운로드 하 여 설치한 후에는 그룹 정책을 관리 하는 데 사용할 컴퓨터에서 다음 단계를 수행 합니다. 일반적으로 도메인 컨트롤러입니다.

1.  다음 디렉터리에 **admx** 파일을 저장 합니다. **Windows \ \ policydefinitions**

2.  **Adml** 파일을 다음 디렉터리에 저장: **Windows \ \ policydefinitions \ \ &lt; 언어 디렉터리 &gt; **

앞의 단계를 완료 한 후에는 **그룹 정책 관리** 콘솔을 사용 하 여 app-v 5.1 클라이언트 구성 설정을 관리할 수 있습니다.

또한 App-v 5.1 클라이언트는 해당 구성을 레지스트리에 저장 합니다. 레지스트리의 데이터 형식을 이해 하면 클라이언트에 대 한 몇 가지 유용한 정보를 수집할 수 있습니다. 레지스트리 항목을 변경 하 여 여러 클라이언트 작업을 구성할 수도 있습니다.

[ADMX 템플릿 및 그룹 정책을 사용하여 App-V 5.1 Client 구성을 수정하는 방법](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## 공유 콘텐츠 저장소 모드를 사용 하 여 클라이언트 배포


App-v 5.1 공유 콘텐츠 저장소 (SCS) 모드에서는 연결 된 패키지 데이터를 로컬에 저장 하지 않고 SCS App-v 5.1 클라이언트가 가상화 된 응용 프로그램을 실행할 수 있습니다. 필요한 모든 가상화 된 패키지 데이터는 네트워크를 통해 전송 됩니다. 따라서 빠른 연결 환경 에서만 SCS 모드를 사용 해야 합니다. RDS (원격 데스크톱 서비스) 및 표준 버전의 App-v 5.1 클라이언트는 모두 SCS 모드에서 지원 됩니다.

**중요**  앱-V 5.1 클라이언트가 SCS 모드에서 실행 되도록 구성 된 경우 App-v 5.1 패키지를 스트리밍하는 위치를 사용할 수 있어야 하 고, 그렇지 않으면 가상화 된 패키지가 실패 하 게 됩니다. 또한, 인터넷을 통해 SCS 모드에서 App-v 5.1 클라이언트를 실행 하는 컴퓨터에는 가상화 된 응용 프로그램을 배포 하지 않는 것이 좋습니다.

 

또한 SCS는 가상화 된 패키지가 포함 된 실제 위치가 아닙니다. 이 모드는 App-v 5.1 클라이언트를 사용 하 여 네트워크에서 필요한 가상화 된 패키지 데이터를 스트리밍할 수 있습니다.

SCS 모드는 다음과 같은 시나리오에서 유용 합니다.

-   VDI (가상 데스크톱 인프라) 배포

-   RDS (원격 데스크톱 서비스) 배포

환경에서 SCS를 사용 하려면 SCS 모드에서 실행할 App-v 5.1 클라이언트를 사용 하도록 설정 해야 합니다. 설치 중에이 설정을 지정 해야 합니다. 기본적으로 클라이언트는 SCS 모드를 사용 하도록 구성 되지 않습니다. SCS를 사용할 계획인 경우 제안 된 절차를 사용 하 여 클라이언트를 설치 해야 합니다. 그러나 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 다음 PowerShell 명령을 입력 하 여 SCS 모드에서 실행 되도록 기존 App-v 5.1 클라이언트를 구성할 수 있습니다.

**set-AppvClientConfiguration-SharedContentStoreMode 1**

관리자가 SCS 모드 5.1 클라이언트를 실행 하는 컴퓨터에서 일부 가상 응용 프로그램을 미리 로드 하는 경우가 있을 수 있습니다. 패키지를 추가, 게시 및 탑재 하는 PowerShell 명령을 사용 하 여이 작업을 수행할 수 있습니다. 예를 들어 패키지가 모든 컴퓨터에 미리 로드 된 경우 관리자는 PowerShell 명령을 사용 하 여 패키지를 추가, 게시 및 탑재할 수 있습니다. 패키지는 로컬로 저장 되므로 네트워크를 통해 스트리밍할 수 없습니다.

[공유 콘텐츠 저장소 모드에서 App-V 5.1 Client를 설치하는 방법](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## Sequencer 배포


시퀀서는 표준 응용 프로그램을 배포용 가상 패키지로 (App-v 5.1 클라이언트를 실행 하는 컴퓨터) 변환 하는 데 사용 되는 도구입니다. 시퀀서는 이전 시퀀싱 워크플로를 최소한으로 변경 하 여 간단 하 고 예측 가능한 변환 프로세스를 제공할 수 있도록 합니다. 또한 시퀀서를 사용 하 여 가상화 된 응용 프로그램의 연결을 가능 하 게 하는 응용 프로그램을 보다 쉽게 구성할 수 있습니다.

App-v 5.1 Sequencer의 변경 목록은 [앱-v 5.1 정보](about-app-v-51.md)를 참조 하세요.

[Sequencer 설치 방법](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> 앱-V 5.1 클라이언트 및 Sequencer 로그


App-v 5.1를 사용 하는 동안 시퀀서 설치 및 작동 이벤트 문제를 해결 하는 데 도움이 되는 앱-V 5.1 Sequencer 로그 정보를 사용할 수 있습니다. **이벤트 뷰어**를 사용 하 여 Sequencer 관련 로그 정보를 검토할 수 있습니다. 다음 줄에는 시퀀서 관련 이벤트의 특정 경로가 표시 됩니다.

**이벤트 뷰어 \ \ 응용 프로그램 및 서비스 로그 \ \ Microsoft \\ App V**. Sequencer 관련 이벤트에는 **AppV \ _Sequencer**이 앞에 붙습니다. 클라이언트 관련 이벤트는 **AppV \ _Client**앞에 붙습니다.

## 시퀀서 및 클라이언트 배포에 대 한 기타 리소스


[App-V 5.1 배포](deploying-app-v-51.md)

[App-V 5.1 계획](planning-for-app-v-51.md)






 

 





