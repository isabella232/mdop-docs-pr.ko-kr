---
title: 앱-V 4.6 및 앱-V 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법
description: 앱-V 4.6 및 앱-V 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814172"
---
# 앱-V 4.6 및 앱-V 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법

**참고:** App-v 4.6에서 메인스트림 지원이 종료 되었습니다.

다음 정보를 사용 하 여 Microsoft App-v (Application Virtualization) 5.1 클라이언트 (가능에 따라 최신 서비스 팩 및 핫픽스 사용) 및 App-v 4.6 SP2 클라이언트 또는 동일한 컴퓨터에 app-v 4.6 S3 클라이언트를 설치 합니다. 지원 되는 버전, 요구 사항 및 기타 계획 정보는 [이전 버전의 app-v에서 마이그레이션 계획](planning-for-migrating-from-a-previous-version-of-app-v51.md)을 참조 하세요.

**동일한 컴퓨터에 App-v 5.1 클라이언트 및 App-v 4.6 클라이언트 배포**

1.  App-v 4.6를 실행 하는 컴퓨터에 다음 버전의 App-v 클라이언트를 설치 합니다.

    -   [Microsoft Application Virtualization 4.6 서비스 팩 3](https://www.microsoft.com/download/details.aspx?id=41187)

2.  앱-v 4.6 SP3 버전의 클라이언트를 실행 하는 컴퓨터에 App-v 5.1 클라이언트를 설치 합니다. 최상의 결과를 위해서는 App-v 5.1 클라이언트에 사용할 수 있는 모든 업데이트를 설치 하는 것이 좋습니다.

3.  패키지를 점차적으로 변환 또는 다시 시퀀싱 합니다.

    -   패키지를 변환 하려면 App-v 5.1 패키지 변환기를 사용 하 여 필수 패키지를 App-v 5.1 (**appv**) 파일 형식으로 변환 합니다.

    -   패키지를 다시 시퀀싱 하려면 최신 버전의 시퀀서를 사용 하 여 최상의 결과를 고려 하세요.

    패키지 게시에 대 한 자세한 내용은 [관리 콘솔을 사용 하 여 패키지를 게시 하는 방법을](how-to-publish-a-package-by-using-the-management-console-51.md)참조 하세요.

4.  패키지를 클라이언트 컴퓨터에 배포 합니다.

5.  필요에 따라 확장명 점을 변환 합니다. 자세한 내용은 다음 리소스를 참조하세요.

    -   [특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.1 패키지로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.1로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [이전 버전의 App-V에서 만든 패키지를 변환하는 방법](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  App-v 5.1 패키지가 성공적으로 실행 되었는지 테스트 한 다음 4.6 패키지를 제거 합니다. 클라이언트 컴퓨터의 사용자 상태를 확인 하려면 [사용자 환경 가상화](https://technet.microsoft.com/library/dn458947.aspx) 또는 다른 사용자 환경 관리 도구를 사용 하는 것이 좋습니다.

    **App-v에 대 한 제안이 있으십니까**? [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다. **App-v 문제가 있나요?** [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 합니다.

## 관련 항목


[App-V의 이전 버전에서 마이그레이션 계획](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[App-V 5.1 Sequencer 및 Client 배포](deploying-the-app-v-51-sequencer-and-client.md)

 

 





