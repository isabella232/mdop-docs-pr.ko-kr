---
title: 이전 버전의 App-V에서 만든 패키지를 변환하는 방법
description: 이전 버전의 App-V에서 만든 패키지를 변환하는 방법
author: dansimp
ms.assetid: 3366d399-2891-491d-8de1-f8cfdf39bbab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 402e64e3bdbc55eea1edb91d070bb7ebb11c912b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814356"
---
# 이전 버전의 App-V에서 만든 패키지를 변환하는 방법


패키지 변환기 유틸리티를 사용 하 여 이전 버전의 App-v로 만든 가상 응용 프로그램 패키지를 업그레이드할 수 있습니다.

**참고**  
64 비트 아키텍처로 컴퓨터를 실행 하는 경우 x86 버전의 PowerShell을 사용 해야 합니다.



Package converter는 App-v 4.5 sequencer 또는 이후 버전을 사용 하 여 만든 패키지만 직접 변환할 수 있습니다. App-V 4.5 이전 버전을 사용 하 여 만든 패키지는 변환 전에 App-v 4.5 또는 App-v 4.6 형식으로 업그레이드 해야 합니다.

다음 정보는 기존 가상 응용 프로그램 패키지를 변환 하는 방향을 제공 합니다.

**중요**  
패키지 원료 파일을 항상 안전한 위치 및 디렉터리에 저장 하도록 패키지 변환기를 구성 해야 합니다. 보안 위치에는 관리자만 액세스할 수 있습니다. 또한 패키지를 배포 하는 경우 안전한 위치에 패키지를 저장 하거나 변환 프로세스 중에 로그인 할 수 있는 다른 사용자가 없는지 확인 해야 합니다.



**앱-V 4.6 설치 폴더가 가상 파일 시스템 루트로 리디렉션 됨**

앱-V 4.6에서 5.1로 패키지를 변환할 때 앱-V 5.1 패키지는 4.6 패키지를 만들 때 사용 하는 데 필요한 하드 코드 된 드라이브에 액세스할 수 있습니다. 드라이브 문자는 4.6 시퀀싱 시스템에서 설치 드라이브로 선택한 드라이브입니다. (기본 드라이브 문자는 Q:\\.)

App-v 5.1 이전에는 4.6 루트 폴더가 인식 되지 않고 App-v 5.0 패키지에서 액세스할 수 없었습니다. 이제 App-v 5.1 패키지는 전체 경로로 하드 코드 된 파일에 액세스 하거나 App-v 4.6 설치 루트 아래의 파일을 프로그래밍 방식으로 열거할 수 있습니다.

**기술 정보:** App-v 5.1 패키지 변환기는 Filesystem 요소의 FilesystemMetadata.xml 파일에 App-v 4.6 설치 루트 폴더와 짧은 폴더 이름을 저장 합니다. App-v 5.1 클라이언트는 가상 프로세스를 만들 때 앱-V 4.6 설치 루트의 요청을 가상 파일 시스템 루트에 매핑합니다.

**시작**

1.  환경에서 컴퓨터에 App-v 시퀀서를 설치 합니다. Sequencer를 설치 하는 방법에 대 한 자세한 내용은 [sequencer를 설치](how-to-install-the-sequencer-51beta-gb18030.md)하는 방법을 참조 하세요.

2.  

    다음 cmdlet을 사용할 수 있습니다.

    -   테스트-AppvLegacyPackage-이 cmdlet은 패키지를 검사 하도록 디자인 되었습니다. **Sft** 파일 누락, 잘못 된 원본, **osd** 파일 오류 또는 잘못 된 패키지 버전 등 패키지 오류에 대 한 정보를 반환 합니다. 이 cmdlet은 **sft** 파일을 구문 분석 하거나 깊이 유효성 검사를 수행 하지 않습니다. PowerShell cmdline을 사용 하 여이 cmdlet에 대 한 옵션 및 기본 기능에 대 한 자세한 내용은을 입력 `Test-AppvLegacyPackage -?` 하세요.

    -   ConvertFrom-AppvLegacyPackage – 기존 패키지를 변환 하려면를 입력 `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` 합니다. 이 명령은 `c:\contentStore` 기존 패키지의 위치를 나타내고 `c:\convertedPackages` 결과 app-v 5.1 가상 응용 프로그램 패키지 파일이 저장 되는 출력 디렉터리입니다. 새 이름을 지정 하지 않으면 기본적으로 이전 패키지 이름이 App-V 5.1 파일 이름에 사용 됩니다.

        또한 패키지 변환기는 패키지를 App-v 패키지의 스트림으로 설정 하 여 App-v 5.1 패키지의 성능을 최적화 합니다.  이는 기본 기능 블록 보다 성능이 더 복잡 하며 패키지를 완전히 다운로드 하는 것입니다. 플래그 **Downloadfullpackageonfirstlaunch** 를 사용 하 여 패키지를 변환 하 고 기본적으로 패키지가 완전히 다운로드 되도록 설정할 수 있습니다.

        **참고**  
        출력 디렉터리를 지정 하기 전에 출력 디렉터리를 만들어야 합니다.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.1 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## 관련 항목


[App-V 5.1 작업](operations-for-app-v-51.md)









