---
title: OSD 파일 요소
description: OSD 파일 요소
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816108"
---
# OSD 파일 요소


Sequencer 설치 디렉터리에는 OSD (개방형 소프트웨어 설명자) 파일의 유효한 구조를 정의 하는 XML 스키마 파일인 **Softricity**이 포함 되어 있습니다. 다음은 자주 사용 하는 OSD 요소 중 일부입니다.

<a href="" id="softpkg"></a>SOFTPKG  
소프트웨어 패키지를 정의 하는 모든 요소가 포함 된 OSD 파일의 루트 요소입니다.

<a href="" id="codebase"></a>CODEBASE  
이 패키지의 sft 파일에 대 한 정보 (HREF, FILENAME, GUID 특성 포함)입니다. 이 특정 패키지의 배포 지점을 변경 하는 경우 HREF 특성을 편집할 수 있습니다.

<a href="" id="os"></a>OS  
시퀀싱 마법사에서 초기에 설정 된 값을 기준으로이 응용 프로그램을 실행할 수 있는 운영 체제를 정의 합니다. 이 값에는 **Softricity**에 정의 된 값만 포함 될 수 있습니다.

<a href="" id="local-interaction-allowed"></a>지역 \ _INTERACTION \ _ALLOWED  
TRUE로 설정 하면 특정 가상 환경 내에서 격리 되지 않고 전역 네임 스페이스의 명명 된 개체 (이벤트, 뮤텍스, 세마포, 파일 매핑 및 mailslots) 및 COM 개체를 만들 수 있으며,이는 가상 응용 프로그램이 호스트 운영 체제의 응용 프로그램과 상호 작용할 수 있도록 합니다.

예: &lt; SOFTPKG &gt; &lt; 구현&gt;

&lt;VIRTUALENV &gt; &lt; 정책&gt;

&lt;로컬 \ _INTERACTION \ _ALLOWED &gt; TRUE

&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;

&lt;/REE &gt; &lt; /정책/VIRTUALENV&gt;

&lt;/구현 &gt; &lt; /SOFTPKG&gt;

<a href="" id="dependencies"></a>항목  
다른 패키지의 CODEBASE 태그를 사용 하 여 동적 도구 모음 컴퍼지션 (다른 패키지에 대 한 종속성)을 정의 합니다.

예: &lt; 종속성 &gt; &lt; CODEBASE HREF = "rtsps:/server/package.sft" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "installer.pkg" "SIZE =" osguard "필수 =" FALSE "/ &gt; &lt; /종속성&gt;

<a href="" id="package-name"></a>패키지 이름  
시퀀싱 마법사 **패키지 정보** 페이지에 입력 한 패키지의 일반 이름으로, 여러 응용 프로그램을 포함 하는 시퀀싱 된 응용 프로그램에 사용 되는 단일 이름을 지정할 수 있습니다.

<a href="" id="title"></a>타이틀이  
시퀀싱 하는 응용 프로그램의 선택적 설명적인 이름입니다.

<a href="" id="abstract"></a>이론적인  
시퀀싱 마법사 **패키지 정보** 페이지의 **설명** 필드에 입력 된 소프트웨어 패키지에 대 한 간략 한 설명입니다. 모범 사례는 운영 체제 및 Sequencer workstation 서비스 팩 수준, Sequencer 버전, 시퀀싱 엔지니어의 이름 등의 정보를 지정 하는 것입니다.

<a href="" id="script"></a>스크립팅할  
시작, 종료 또는 스트리밍 중 발생할 특정 스크립팅된 이벤트를 정의 합니다.

<a href="" id="mgmt-shortcutlist"></a>관리 \ _SHORTCUTLIST  
마법사에 정의 된 모든 바로 가기 목록입니다.

<a href="" id="mgmt-fileassociations"></a>관리 \ _FILEASSOCIATIONS  
마법사에 지정 된 파일 형식 목록입니다.

## 관련 항목


[OSD 탭 정보](about-the-osd-tab.md)

 

 





