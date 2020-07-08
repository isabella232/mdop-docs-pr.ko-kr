---
title: MED-V 클라이언트를 설치하는 방법
description: MED-V 클라이언트를 설치하는 방법
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827193"
---
# MED-V 클라이언트를 설치하는 방법


배포 패키지 기반 시나리오에서 MED-V 클라이언트 설치는 배포 패키지에 포함 되어 패키지에서 직접 설치 됩니다.

**중요**  
이미지를 포함 하지 않는 배포 패키지를 사용 하는 경우 배포 패키지를 설치 하기 전에 이미지를 웹에 업로드 하거나 미리 스테이지 폴더로 푸시 해야 합니다.



**배포 패키지를 설치 하려면**

1.  다음 중 하나를 수행합니다.

    -   웹에서 MED-V 패키지를 다운로드 합니다.

    -   배포 USB 또는 DVD를 호스트 드라이브에 삽입 합니다.

2.  MED-V가 자동으로 실행 되지 않는 경우 MED-VAutoInstaller.exe를 두 번 클릭 합니다.

    이미 설치 된 구성 요소와 현재 설치 되 고 있는 항목을 나열 하는 대화 상자가 표시 됩니다.

    **참고**  
    지원 되지 않는 Microsoft 가상 PC 버전이 호스트 컴퓨터에 있는 경우 기존 버전을 제거 하 고 설치 관리자를 다시 실행 하 라는 메시지가 표시 됩니다.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. 필요한 경우 컴퓨터를 다시 부팅 합니다.

   설치가 완료 되 면 MED-V가 시작 되 고 설치가 완료 되었음을 알리는 메시지가 표시 됩니다.

4. 다음 사용자 이름 및 암호를 사용 하 여 MED-V에 로그인 합니다.

   -   도메인 이름 및 사용자 이름 뒤에 MED-V와 함께 작업할 수 있는 도메인 사용자의 암호를 입력 합니다.

       예: "domain \ _name \\user\ _name", "password"

## 관련 항목


[배포 패키지를 구성하는 방법](how-to-configure-a-deployment-package.md)

[서버에 MED-V 이미지를 업로드하는 방법](how-to-upload-a-med-v-image-to-the-server.md)

[클라이언트 설치 명령줄 참조](client-installation-command-line-reference.md)









