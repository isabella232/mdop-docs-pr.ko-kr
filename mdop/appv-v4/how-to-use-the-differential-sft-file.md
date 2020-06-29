---
title: Differential SFT 파일을 사용하는 방법
description: Differential SFT 파일을 사용하는 방법
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816388"
---
# Differential SFT 파일을 사용하는 방법


응용 프로그램을 시퀀싱 할 때 Microsoft App-v (Application Virtualization) 시퀀서는 모든 가상 응용 프로그램 파일 콘텐츠 및 구성 정보를 저장 하기 위해 SFT 파일 (sft)을 만듭니다. App-v 버전 4.5에서는 차등 SFT (dsft) 파일이 도입 되었습니다. 시퀀서를 사용 하 여 기존 패키지에 대 한 업그레이드를 만든 후에는이 파일을 생성 하 여 원래 시퀀싱 된 응용 프로그램 패키지와 새 버전 간의 차이점만 저장 하도록 선택할 수 있습니다. 따라서 전체 SFT 파일은 새 버전의 응용 프로그램에 비해 훨씬 크기 때문에 낮은 대역폭 네트워크 연결을 통해 패키지 업데이트를 보내는 것이 미치는 영향을 줄일 수 있습니다. 그러나 해당 사용은 특정 제한 된 상황 에서만 지원 됩니다. 이 기능은 낮은 대역폭 연결을 통해 로컬 파일 서버를 사용 하는 사용자 그룹을 관리 하 고 App-v 스트리밍 서버를 사용 하지 않는 경우에 특별히 사용 하기 위한 것입니다.

Configuration Manager에서 사용자를 관리 하는 경우에는 이미 기본으로 제공 되는 낮은 대역폭 배포에 대 한 지원이 필요 하므로 차등 SFT 파일을 사용 하지 않는 것이 Manager2007. 또한 응용 프로그램 가상화 (App-v) 관리 또는 활성 업그레이드로 스트리밍 서버를 사용 하는 경우 클라이언트가 이전 버전과 새 패키지 버전의 차이만을 검색 하기 때문에 필요 하지 않습니다.

다음 절차에서는 virtual application 패키지의 업그레이드를 완료 하 고 차등 SFT 파일을 배포 하는 경우 Sequencer 설치에 포함 된 mkdiffpkg.exe를 사용 하 여 차등 SFT 파일을 만드는 방법을 보여 줍니다. 이 절차를 완료 하면 패키지가 클라이언트 컴퓨터에서 언로드될 때 다음에 사용자가 응용 프로그램을 실행 하려고 할 때 클라이언트는 로컬 파일 공유에서 전체 패키지 V2를 스트림할 수 있도록 설정 된 재정의 URL로 다시 대체 됩니다. 이렇게 하면 응용 프로그램을 시작할 때 사용자에 대 한 오류가 발생 하지 않습니다. 전체 클라이언트가 손상 되거나 제거 되는 경우 업그레이드 된 패키지 (Chapv2)의 정식 버전을 클라이언트에 배포 하도록 ESD 시스템을 구성 하는 것이 좋습니다.

패키지 업그레이드에 대 한 자세한 내용은 App-V 4.5 Operations 가이드의 "기존 가상 응용 프로그램을 업그레이드 하는 방법"을 참조 하세요. <https://go.microsoft.com/fwlink/?LinkId=133129>

**참고**  필수 구성 요소를 사용 하는 경우 ESD에서 대상으로 하는 모든 사용자 컴퓨터는 해당 로컬 캐시에 완전히 로드 된 V1 sft 파일을 포함 해야 하며, 모든 컴퓨터에서 파일 스트리밍을 사용할 수 있어야 합니다.

 

**차등 SFT 파일을 사용 하려면**

1.  관리자 권한이 있는 계정을 사용 하 여 Sequencer 컴퓨터에 로그온 합니다. Sequencer에서 업그레이드할 원본 패키지 (V1)를 연 다음 패키지를 새 버전 (V2)으로 업그레이드 하 고 새로운 V2 sft로 저장 합니다.

2.  App-V 4.5 Sequencer 설치 폴더에서 명령 창을 열고 다음 명령을 실행 합니다.

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  ESD 시스템 또는 기타 파일 복사 프로세스를 사용 하 여 완전 한 V2 패키지 콘텐츠 파일 V2를 잘 연결 된 네트워크 연결의 사용자 컴퓨터에 액세스할 수 있는 로컬 파일 공유에 복사 합니다.

4.  ESD 시스템을 사용 하 여 각 사용자 컴퓨터에 차등 SFT 파일인 V2 ft의 복사본을 배치 합니다.

5.  V2 ft 파일을 가져오려면 각 사용자 컴퓨터에서 다음 SFTMIME 명령을 실행 합니다.

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  각 사용자 컴퓨터에서 다음 SFTMIME 명령을 실행 하 여 재정의 URL을 V2. sft 파일을 가리키도록 설정 합니다.

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**참고**  
-   차등 SFT 파일을 올바른 순서로 클라이언트에 적용 해야 합니다. 예를 들어 V2 ft는 V3. dsft가 적용 되기 전에 V1 응용 프로그램에 적용 해야 합니다.

-   Sequencer의 **MSI (Microsoft Windows Installer) 패키지** 기능은 차등 SFT 파일과 함께 사용할 수 없습니다.

 

## 관련 항목


[앱-V 시퀀서를 사용 하 여 가상 응용 프로그램을 만들거나 업그레이드 하는 방법](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





