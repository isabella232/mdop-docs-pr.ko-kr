---
title: 클라이언트에 가상 응용 프로그램을 게시하는 방법
description: 클라이언트에 가상 응용 프로그램을 게시하는 방법
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816873"
---
# 클라이언트에 가상 응용 프로그램을 게시하는 방법


전자 소프트웨어 배포 시스템을 사용 하 여 응용 프로그램 가상화를 배포 하는 경우 다음 절차 중 하나를 사용 하 여 사용자에 게 응용 프로그램 패키지를 게시할 수 있습니다.

**독립 실행형 Windows Installer 파일을 사용 하 여 패키지를 게시 하려면**

1.  클라이언트는 *Requireauthorizationifcached* 매개 변수를 0 (영)으로 설정 하 여 설치 해야 합니다. 이 매개 변수를 설정 하는 방법에 대 한 자세한 내용은 [Application Virtualization 클라이언트 설치 관리자 명령줄 매개 변수](application-virtualization-client-installer-command-line-parameters.md) 를 참조 하세요.

2.  Windows Installer 파일 및 SFT 파일을 대상 컴퓨터의 동일한 폴더에 복사 합니다.

3.  컴퓨터에서 다음 명령을 실행 합니다.

    `Msiexec.exe /I "packagename.msi" /q`

**Windows Installer 및 패키지 매니페스트를 사용 하 여 패키지를 게시 하려면**

1.  Windows Installer 파일을 대상 컴퓨터와 SFT 파일을 스트리밍 서버의 콘텐츠 공유에 복사 합니다.

2.  각 사용자의 컴퓨터에서 다음 명령을 실행 합니다.

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **중요**  OVERRIDEURL의 경우 모든 백슬래시 문자는 앞의 백슬래시를 사용 하 여 이스케이프 되어야 하며, OVERRIDEURL 경로가 올바르게 구문 분석 되지 않습니다. 또한 값이 파일의 경로인 경우를 제외 하 고 속성 및 값을 대문자로 입력 해야 합니다.

     

**SFTMIME을 사용 하 여 패키지를 게시 하려면**

-   컴퓨터의 모든 사용자에 대해 응용 프로그램을 게시 하는 방법의 예는 사용자 컴퓨터에서 다음 명령을 실행 합니다.

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    이러한 및 다른 SFTMIME 명령에 대 한 자세한 내용은 [Sftmime 명령 참조](sftmime--command-reference.md)를 참조 하세요.

## 관련 항목


[게시 방법 결정](determine-your-publishing-method.md)

[전자 소프트웨어 배포 기반 시나리오](electronic-software-distribution-based-scenario.md)

[SFTMIME 명령 참조](sftmime--command-reference.md)

[Application Virtualization Client에 대한 독립 실행형 배달 시나리오](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





