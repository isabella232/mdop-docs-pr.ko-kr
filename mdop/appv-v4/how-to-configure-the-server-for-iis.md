---
title: IIS용 서버를 구성하는 방법
description: IIS용 서버를 구성하는 방법
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817743"
---
# IIS용 서버를 구성하는 방법


가상 응용 프로그램을 응용 프로그램 가상화 데스크톱 클라이언트로 스트림 하 고 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 클라이언트로 스트림할 수 있으려면 먼저 IIS 서버를 구성 해야 합니다. 서버를 구성할 때 SFT 파일이 로드 되 고 저장 되는 콘텐츠 디렉터리를 설정 하 게 됩니다. SFT 파일에는 가상 응용 프로그램 (또는 응용 프로그램)이 포함 됩니다.

**IIS 서버에서 콘텐츠 디렉터리를 구성 하려면**

1.  IIS를 실행 하는 서버에서 콘텐츠 디렉터리로 사용할 디렉터리를 찾거나 디렉터리가 없는 경우 디렉터리를 만듭니다. 이 디렉터리를 표준 파일 공유로 구성 합니다.

2.  IIS를 실행 하는 서버에서 **Iis 관리자**를 열고 기본 웹 사이트에서 서버에서 만든 콘텐츠 디렉터리에 해당 하는 가상 디렉터리를 만듭니다. **읽기가** 선택 되어 있는지 확인 합니다.

3.  새로 만든 가상 디렉터리에 별칭 **콘텐츠**를 지정 합니다.

4.  이 가상 디렉터리의 다른 모든 기본 설정을 그대로 적용 합니다.

5.  이전에 정의한 Active Directory 도메인 서비스의 보안 그룹을 사용 하 여 콘텐츠 디렉터리 아래의 콘텐츠 디렉터리와 패키지 폴더에 대 한 NTFS 파일 시스템 사용 권한을 구성 합니다.

**참고**  IIS를 사용 하 여 .ICO 및 OSD 파일을 게시 하는 경우 OSD = TXT에 대 한 MIME 형식을 구성 해야 합니다. 그렇지 않으면 IIS는 .ICO 및 OSD 파일을 클라이언트에 제공 하지 않습니다. IIS를 사용 하 여 패키지 (SFT 파일)를 게시 하는 경우 SFT = Binary에 대 한 MIME 형식을 구성 해야 합니다. 그렇지 않으면 IIS가 클라이언트에 SFT 파일을 제공 하지 않습니다.

 

## 관련 항목


[Application Virtualization Server 기반 시나리오](application-virtualization-server-based-scenario.md)

[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[Application Virtualization Management Server 구성 방법](how-to-configure-the-application-virtualization-management-servers.md)

[Application Virtualization Streaming Server 구성 방법](how-to-configure-the-application-virtualization-streaming-servers.md)

[파일 서버를 구성하는 방법](how-to-configure-the-file-server.md)

 

 





