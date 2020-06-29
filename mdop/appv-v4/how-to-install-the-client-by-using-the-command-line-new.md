---
title: 명령줄을 사용하여 클라이언트를 설치하는 방법
description: 명령줄을 사용하여 클라이언트를 설치하는 방법
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817323"
---
# 명령줄을 사용하여 클라이언트를 설치하는 방법


이 섹션의 항목에는 setup.exe 또는 setup.msi를 사용 하 여 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트 또는 Application Virtualization (App-v) 데스크톱 클라이언트를 설치 하는 절차가 포함 되어 있습니다. 설치 프로그램 중 하나를 실행 하려면 관리자 권한이 필요 합니다.

선택적 명령줄 매개 변수를 사용 하 여 설치 중에 앱-V 클라이언트에 특정 구성 설정을 적용할 수 있습니다. 매개 변수를 사용 하는 방법에 대 한 자세한 내용은 [응용 프로그램 가상화 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)를 참조 하세요. 클라이언트를 배포 하기 전에 컴퓨터에 레지스트리 설정을 적용 한 경우 (예: 그룹 정책을 사용 하는 경우) 이러한 설정이 유지 되 고 추가 명령줄 매개 변수가 적용 됩니다. 명령줄 매개 변수 값이 같은 설정의 기존 값을 바꿉니다.

**참고**  VDI 서버 구현과 같이 읽기 전용 캐시와 함께 사용 하기 위해 App-v 클라이언트를 설치 하는 경우에는 클라이언트가 읽기 전용일 때 응용 프로그램을 업데이트 하지 않도록 *Autoloadtarget* 매개 변수를 no로 설정 해야 합니다.

 

설치 후 이러한 매개 변수 값을 설정 하는 방법에 대 한 자세한 내용은 Application Virtualization (App-v) 운영 가이드에서 [명령줄을 사용 하 여 App-v 클라이언트 레지스트리 설정을 구성 하는 방법을](https://go.microsoft.com/fwlink/?LinkId=169355) 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=169355) .

**참고**  사용자 컴퓨터의 구성 설정이 클라이언트 설치 경로에 종속 되는 경우 Application Virtualization (App-v) 4.5 클라이언트는 해당 설치 파일을 이전 버전이 아닌 다른 폴더에 복사 한다는 점에 유의 하세요. 기본적으로 App-v 4.5 클라이언트의 새 설치는 설치 파일을 \\Program Files\\Microsoft Application 가상화 클라이언트 폴더에 복사 합니다. 이전 버전의 클라이언트가 이미 설치 되어 있는 경우 App-v 4.5 클라이언트 설치 관리자를 실행 하면 기존 설치 폴더를 사용 하 여 기존 클라이언트의 업그레이드를 수행 합니다.

 

\ [Template 토큰 값 \]

**참고**  App-v 버전 4.6 이상에서 App-v 클라이언트가 설치 되 면 SFTLDR.DLL Windows\\system32 디렉터리에 복사 됩니다. 64 비트 시스템에 App-v 클라이언트가 설치 되어 있으면 SFTLDR\_WOW64.DLL Windows\\SysWOW64 디렉터리에 복사 됩니다.

 

\ [Template 토큰 값 \]

## 이 섹션의 내용


다음 항목에서는 setup.exe 또는 setup.msi를 사용 하 여 원격 데스크톱 서비스 (이전의 터미널 서비스) 용 App-v 클라이언트, Application Virtualization (App-v) 데스크톱 클라이언트를 설치 하는 방법에 대해 설명 합니다.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[Setup.exe를 사용하여 App-V Client를 설치하는 방법](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
setup.exe 프로그램을 사용 하 여 App-v 클라이언트를 설치 하는 단계별 절차를 제공 합니다.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[Setup.msi를 사용하여 App-V Client를 설치하는 방법](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
setup.msi 프로그램을 사용 하 여 필수 구성 요소 소프트웨어를 설치 하는 단계별 절차와 앱 V 클라이언트도 제공 합니다.

## 관련 항목


[Application Virtualization Client 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md)

[Application Virtualization Client를 수동으로 설치하는 방법](how-to-manually-install-the-application-virtualization-client.md)

[클라이언트에 가상 응용 프로그램을 게시하는 방법](how-to-publish-a-virtual-application-on-the-client.md)

[App-V Client 제거 방법](how-to-uninstall-the-app-v-client.md)

 

 





