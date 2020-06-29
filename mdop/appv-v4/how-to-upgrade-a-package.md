---
title: 패키지를 업그레이드하는 방법
description: 패키지를 업그레이드하는 방법
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816503"
---
# 패키지를 업그레이드하는 방법


자동 업그레이드 프로세스는 응용 프로그램 가상화 서버 관리 콘솔에서 패키지 버전을 추가 하는 것과 동일 합니다. 기존 패키지에 응용 프로그램을 resequence 때 자동 업그레이드가 수행 됩니다. 그런 다음 스트리밍을 위해 서버에 새 버전을 추가할 수 있습니다.

새 버전을 사용 하 여 패키지를 업그레이드 하는 경우 기존 버전을 현재 위치에 그대로 두거나 삭제 하 고 최신 버전만 남길 수 있습니다. 기존 문서와의 호환성을 위해 이전 버전을 그대로 두거나, 모든 사용자가 사용할 수 있게 하기 전에 새 버전을 테스트할 수 있도록 할 수 있습니다.

**패키지를 자동으로 업그레이드 하려면**

1.  새 SFT 파일을 Application Virtualization Server의 content 폴더에 복사 합니다.

    **참고**  다시 시퀀싱 했을 때 OSD (Open Software Descriptor), icon (.ICO) 또는 Sequencer 프로젝트 (SPRJ) 파일을 변경한 기능이 추가 되지 않은 경우에는 복사 하지 않아도 됩니다. 이러한 파일을 모두 같은 날짜로 표시 하려면 이러한 파일을 포함할 수 있습니다.

     

2.  Application Virtualization Server 관리 콘솔의 왼쪽 창에서 **패키지**를 확장 합니다.

3.  업그레이드 하려는 패키지를 마우스 오른쪽 단추로 클릭 하 고 **버전 추가**를 선택 합니다.

4.  **패키지 버전 추가** 대화 상자에서 **파일 필드에 대 한 전체 경로** 에 있는 새 응용 프로그램 버전의 전체 경로 이름을 찾아보거나 입력 합니다. SFT 파일 이어야 합니다.

5.  **다음**을 클릭합니다.

6.  **요약** 대화 상자에서 파일 위치를 표시 하 고 아직 파일을 복사 하지 않은 경우이를 복사할 것인지 묻습니다. 정보를 확인 한 후 **마침을** 클릭 합니다.

    이제 새 버전이 완성 되어 스트리밍할 준비가 되었습니다.

## 관련 항목


[Server Management Console에서 패키지를 관리하는 방법](how-to-manage-packages-in-the-server-management-console.md)

 

 





