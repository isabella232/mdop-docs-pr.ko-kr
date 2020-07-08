---
title: 배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법
description: 배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826443"
---
# 배포된 MED-V 작업 영역에서 URL 리디렉션 정보를 추가하거나 제거하는 방법


배포 된 MED-V 작업 영역의 URL 리디렉션 정보를 편집 하려면 그룹 정책을 사용 하 여 시스템 레지스트리를 업데이트 하는 것이 좋습니다. 권장 하는 것은 아니지만 업데이트 된 URL 리디렉션 정보를 사용 하 여 MED-V 작업 영역을 다시 빌드하고 배포할 수도 있습니다.

레지스트리 키는 일반적으로 다음 위치에 있습니다.

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

다음과 같은 다중 문자열 값이 있어야 합니다. `RedirectUrls`

값 데이터는 `RedirectUrls` **Med-v 작업 영역 포장기**를 사용 하 여 med-v 작업 영역 패키지를 빌드할 때 리디렉션에 대해 지정한 모든 url의 목록입니다. 자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.

다음 작업 중 하나를 수행 하 여 URL 리디렉션 정보를 추가 하 고 제거할 수 있습니다.

-   [URL 리디렉션 레지스트리 키를 편집 하 고 그룹 정책을 사용 하 여 배포](#bkmk-editreg)

-   [URL 리디렉션 텍스트 파일을 편집 하 고 MED-V 작업 영역을 다시 빌드합니다.](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**그룹 정책을 사용 하 여 URL 리디렉션 정보를 업데이트 하려면**

1.  이름이 지정 된 레지스트리 키 다중 문자열 값을 편집 `RedirectUrls` 합니다. 이 값은 일반적으로 다음 위치에 있습니다.

    Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

    레지스트리 키에 Url을 추가 하는 경우에는 MED-V 작업 영역 패키지를 빌드할 때 필요 했던 대로 한 줄에 하나씩 입력 합니다. 자세한 내용은 [Med-v 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)를 참조 하세요.

2.  그룹 정책을 사용 하 여 업데이트 된 레지스트리 키를 배포 합니다. 그룹 정책을 사용 하는 방법에 대 한 자세한 내용은 [그룹 정책 소프트웨어 설치](https://go.microsoft.com/fwlink/?LinkId=195931) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195931) .

**참고**  이 방법으로 URL 리디렉션 정보를 편집 하는 방법은 MED-V 모범 사례입니다.

 

<a href="" id="bkmk-edittext"></a>**업데이트 된 URL 텍스트 파일을 사용 하 여 MED-V 작업 영역을 다시 작성 하려면**

-   리디렉션 목록에서 Url을 추가 하 고 제거 하는 또 다른 방법은 URL 리디렉션 텍스트 파일을 업데이트 한 다음이를 사용 하 여 새 MED-V 작업 영역을 빌드하는 것입니다. 그런 다음, ESD 시스템 등의 표준 배포 프로세스를 사용 하 여 MED-V 작업 영역을 이전 처럼 다시 배포할 수 있습니다.

    **중요**  URL 리디렉션 정보를 편집 하는 방법은이 방법을 권장 하지 않습니다. 또한 MED-V 작업 영역을 다시 실행할 때마다 엔터프라이즈에 다시 설치 해야 하는 경우를 제외 하 고 가상 컴퓨터에 저장 된 모든 데이터가 손실 됩니다.

     

## 관련 항목


[URL 리디렉션을 테스트하는 방법](how-to-test-url-redirection.md)

[MED-V 작업 영역에 배포된 응용 프로그램 관리](managing-applications-deployed-to-med-v-workspaces.md)

[MED-V 작업 영역 패키지 만들기](create-a-med-v-workspace-package.md)

 

 





