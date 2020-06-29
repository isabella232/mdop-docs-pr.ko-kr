---
title: App-V 4.6 릴리스 정보
description: App-V 4.6 릴리스 정보
author: dansimp
ms.assetid: a3eba129-edac-48bf-a933-3bf43a9873e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9eee3c309a927a72155dec707d8dd95f43e90fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822368"
---
# App-V 4.6 릴리스 정보


이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.

**중요**  이 릴리스 정보는 App-v (Microsoft Application Virtualization) 관리 시스템을 설치 하기 전에 자세히 읽어 보세요. 이러한 릴리스 정보에는 App-v (Application Virtualization) 4.6을 설치 하는 데 필요한 정보가 포함 되어 있습니다. 이 문서에는 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 노트와 다른 앱-V 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.

 

## 보안 취약점 및 바이러스 방지


보안 취약점과 바이러스 로부터 보호 하려면 설치 하는 새 소프트웨어에 대해 사용 가능한 최신 보안 업데이트를 설치 하는 것이 중요 합니다. 자세한 내용은 [Microsoft 보안 웹 사이트](https://go.microsoft.com/fwlink/?LinkId=3482) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=3482) .

## Application Virtualization 4.6의 알려진 문제점


이 섹션에서는 Microsoft Application Virtualization (App-v) 4.6 관련 문제에 대 한 최신 정보를 제공 합니다. 이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다. 이러한 문제는 가능한 경우 이후 릴리스에서 해결 될 것입니다.

### App-v 4.5 Sequencer에서 생성 된 Windows Installer 파일을 실행 하는 로드/설치 오류

App-v 4.5 Sequencer에서 생성 된 Windows Installer 파일을 실행 하면 App-v 4.6 클라이언트에서 실행 하려고 할 때 로드/설치 오류가 생성 됩니다. "이 패키지에는 Microsoft Application Virtualization 클라이언트 4.5 이상이 필요 합니다." 라는 메시지가 표시 됩니다. 다음 해결 방법을 사용해 주십시오.

App-v 4.5 SP1 Sequencer 또는 App-v 4.6 Sequencer를 사용 하 여 이전 패키지를 WORKAROUNDOpen 패키지에 대 한 새 .msi 파일을 생성 합니다.

**참고**  또는 명령 프롬프트에서 App-v 시퀀서는 */OPEN* 및 */MSI* 매개 변수를 사용 하 여 새 .msi 파일을 생성할 수 있습니다 (예:) `SFTSequencer /Open:”package.sprj” /MSI` . 자세한 내용은 [명령줄을 사용 하 여 가상 응용 프로그램을 업그레이드 하는 방법을](how-to-upgrade-a-virtual-application-by-using-the-command-line.md)참조 하세요.

 

### 릴리스 노트 저작권 정보

이 문서는 "있는 그대로" 제공 됩니다. URL 및 다른 인터넷 웹 사이트 참조를 포함한 이 문서의 내용과 관점은 예고 없이 변경될 수 있습니다. 이를 사용 하는 경우의 위험성을 고려해 야 합니다.

여기에 나와 있는 일부 예제는 설명을 돕기 위해 제공 되며 실제는 아닙니다.실제 연결 또는 연결이 의도 되지 않았거나 유추할 수 없습니다.

이 문서는 귀하에게 Microsoft 제품의 지적 재산에 대한 어떠한 법적 권리도 제공하지 않습니다. 내부 참조용으로 이 문서의 사본을 만들 수 있습니다. 내부 참조 목적으로이 문서를 수정할 수 있습니다.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, windows Vista는 Microsoft 회사 그룹의 상표입니다.

다른 모든 상표는 해당 소유자의 재산입니다.

 

 





