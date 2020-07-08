---
title: App-V 4.6 SP1 릴리스 정보
description: App-V 4.6 SP1 릴리스 정보
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819838"
---
# App-V 4.6 SP1 릴리스 정보


이 릴리스 정보를 검색 하려면 CTRL + F를 누릅니다.

**중요**  이 릴리스 정보는 App-v (Microsoft Application Virtualization) 관리 시스템을 설치 하기 전에 자세히 읽어 보세요. 이 릴리스 정보에는 Application Virtualization (App-v) 4.6 SP1을 성공적으로 설치 하는 데 도움이 되는 정보가 포함 되어 있습니다. 이 문서에는 제품 설명서에서 사용할 수 없는 정보가 포함 되어 있습니다. 이러한 릴리스 노트와 다른 App-v 설명서 사이에 차이가 있는 경우 최신 변경 내용을 정식으로 간주 해야 합니다.

 

## 보안 취약점 및 바이러스 방지


보안 취약점과 바이러스 로부터 보호 하려면 설치 하는 새 소프트웨어에 대해 사용 가능한 최신 보안 업데이트를 설치 하는 것이 중요 합니다. 자세한 내용은 [Microsoft 보안 웹 사이트](https://go.microsoft.com/fwlink/?LinkId=3482) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=3482) .

## Application Virtualization 4.6 SP1의 알려진 문제점


이 섹션에서는 Microsoft App-v (Application Virtualization) 4.6 SP1 관련 문제에 대 한 최신 정보를 제공 합니다. 이러한 문제는 제품 설명서에 나타나지 않으며, 경우에 따라 기존 제품 설명서에 일치 하지 않을 수 있습니다. 가능 하면 이후 릴리스에서 문제가 해결 될 것입니다.

### 슬래시 (/)로 끝나지 않으면 SPRT의 경로가 손실 됩니다.

프로젝트 템플릿에서 HREF의 경로가 슬래시 ()로 끝나지 않는 경우 **/** 생성 된 HREF에는 경로가 포함 되지 않습니다. 이는 사용자가 **sprt** 파일을 수동으로 조작 하는 경우에 발생 합니다. 시퀀서를 사용 하는 경우 경로 뒤에 항상 슬래시 ()를 추가 합니다 **/** .

해결 방법 HREF에 역슬래시 ()가 있는지 확인 **/** 합니다.

### 사용자 폴더 이름이 패키지 이름에 해당 하지 않습니다.

사용자 및 전역 installer.pkg 파일을 포함 하는 폴더에는 더 이상 패키지 이름이 포함 되지 않습니다. 이전에는 패키지 루트 폴더 8.3 약식 이름을 폴더 이름의 일부로 사용 하는 데 사용 되는 App-v 클라이언트입니다. 이를 통해 쉽게 식별할 수 있습니다. App-v 4.6 SP1 sequencer를 사용 하는 경우 패키지 루트 폴더 8.3 짧은 이름은 이제 임의의 문자열입니다. 이렇게 하면 App-v 클라이언트를 실행 하는 컴퓨터에서 패키지의 **installer.pkg** 파일이 포함 된 폴더를 식별 하기가 어렵습니다.

해결 방법 다음 방법 중 하나를 사용 하 여 이러한 패키지 폴더를 보다 쉽게 식별 합니다.

1.  Sequencer를 사용 하 여 패키지를 만들 때 기본 응용 프로그램 폴더의 8.3 명명 규칙을 따르는 폴더 이름을 지정 합니다. 이 이름은 App-v 4.6의 경우 처럼 사용자 폴더 이름의 일부로 사용 됩니다.

2.  이제 sprj 파일에 사용자 폴더 이름의 시작 부분으로 사용 되는 문자열을 표시 하는 태그가 포함 되어 있습니다. **PACKAGEROOTFOLDER** 요소의 **SHORTNAME** 요소를 사용 하 여 이름을 확인할 수 있습니다.

### 64 개 이상의 프로세서가 있는 컴퓨터에서 App-v 4.6 SP1 실행

64 개 이상의 프로세서가 설치 된 컴퓨터에서 App-v 4.6 SP1을 실행 하면 App-v 클라이언트가 실패 합니다.

해결 방법 없음 이 구성은 지원 되지 않습니다. 64 보다 적은 수의 프로세서가 있는 App-v 4.6 SP1on 컴퓨터를 실행 해야 합니다.

### Microsoft 업데이트를 사용 하는 일부 로캘에서는 Application Virtualization 4.6 SP1 업데이트가 제공 되지 않음

Microsoft 업데이트를 사용 하는 경우 다음 언어 로캘에서 App-v 4.6 SP1 업데이트를 사용할 수 없습니다.

-   카자흐어

-   힌디어

-   세르비아어-키릴 자모

해결 방법 Microsoft Windows Server Update Services (WSUS)를 사용 하는 경우 영어 버전의 업데이트를 사용 하거나 Microsoft 업데이트 카탈로그에서 업데이트를 다운로드 합니다.

### 부모 패키지를 확장 한 후 나란히 구성 요소를 사용 하 여 플러그 인을 시퀀싱 할 수 없습니다.

**도구**를 사용 하 여 부모 패키지를 확장 하면  /  app-v Sequencer 콘솔에서**로컬 시스템으로 패키지 확장** 하 고 나란히 구성 요소를 사용 하 여 플러그 인을 시퀀싱 하면 설치 오류가 반환 됩니다. 예:

-   **HRESULT 0x80073712**

이 문제는 sequencer가 side-by-side 구성 요소를 레지스트리에 기록 하지만 다음 레지스트리 키의 값은 지우지 않는 경우에 발생 합니다.

HKEY _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

해결 방법 sequencer를 실행 하는 컴퓨터에서 부모 패키지를 확장 한 후 다음 레지스트리 키에 대 한 값을 삭제 해야 합니다.

HKEY _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

값을 삭제 한 후 플러그 인을 순서 대로 시퀀싱 합니다.

### 릴리스 노트 저작권 정보

이 문서는 "있는 그대로" 제공 됩니다. 이 문서에 표시 된 URL 및 기타 인터넷 웹 사이트 참조와 같은 정보 및 보기는 예 고 없이 변경 될 수 있습니다. 이를 사용 하는 경우의 위험성을 고려해 야 합니다.

여기에 나와 있는 일부 예제는 설명을 돕기 위해 제공 되며 실제는 아닙니다. 실제 연결 또는 연결이 의도 되지 않았거나 유추할 수 없습니다.

이 문서는 귀하에게 Microsoft 제품의 지적 재산에 대한 어떠한 법적 권리도 제공하지 않습니다. 내부 참조용으로 이 문서의 사본을 만들 수 있습니다. 내부 참조 목적으로이 문서를 수정할 수 있습니다.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, windows Vista는 Microsoft 회사 그룹의 상표입니다.

다른 모든 상표는 해당 소유자의 재산입니다.

 

 





