---
title: 동일한 컴퓨터에 App-V 4.6 및 App-V 5.0 클라이언트를 배포하는 방법
description: 동일한 컴퓨터에 App-V 4.6 및 App-V 5.0 클라이언트를 배포하는 방법
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.prod: w10
ms.openlocfilehash: f10f3d159c4724f3b486215b1169825bb029316d
ms.sourcegitcommit: 0132cd232b9c030820d95d91b71c4def0184400a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/19/2021
ms.locfileid: "11907231"
---
# <a name="how-to-deploy-the-app-v-46-and-the-app-v-50-client-on-the-same-computer"></a>동일한 컴퓨터에 App-V 4.6 및 App-V 5.0 클라이언트를 배포하는 방법

**참고:** App-V 4.6에서 기본 지원을 종료했습니다. 다음에서는 App-V 4.6 SP3 클라이언트가 이미 설치되어 있는 것으로 가정합니다.

다음 정보를 사용하여 동일한 컴퓨터에 App-V 5.0 클라이언트(최신 서비스 팩 및 핫픽스 사용) 및 App-V 4.6 SP3 클라이언트를 설치합니다. 지원되는 버전, 요구 사항 및 기타 계획 정보는 [Planning for Migrating from a Previous Version of App-V을 참조하십시오.](planning-for-migrating-from-a-previous-version-of-app-v.md)

**동일한 컴퓨터에 App-V 5.0 클라이언트 및 App-V 4.6 클라이언트를 배포하려면**

1.  App-V 4.6 버전의 클라이언트를 실행하는 컴퓨터에 App-V 5.0 SP3 클라이언트를 설치합니다. 최상의 결과를 얻기 위해 App-V 5.0 SP3 클라이언트에 사용 가능한 모든 업데이트를 설치하는 것이 좋습니다.

2.  패키지를 점진적으로 변환하거나 다시 시퀀스화합니다.

    -   패키지를 변환하려면 App-V 5.0 패키지 변환기 를 사용하여 필요한 패키지를 App-V 5.0(**.appv)** 파일 형식으로 변환합니다.

    -   패키지를 다시 시퀀서하기 위해 최상의 결과를 위해 최신 버전의 Sequencer를 사용하는 것이 고려됩니다.

    패키지 게시에 대한 자세한 내용은 관리 콘솔을 사용하여 패키지를 [게시하는 방법을 참조하세요.](how-to-publish-a-package-by-using-the-management-console-50.md)

3.  클라이언트 컴퓨터에 패키지를 배포합니다.

4.  필요한 경우 확장 지점을 변환합니다. 자세한 내용은 다음 리소스를 참조하세요.

    -   [특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [이전 버전의 App-V에서 만든 패키지를 변환하는 방법](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  App-V 5.0 패키지가 성공적이지 테스트한 다음 4.6 패키지를 제거합니다. 클라이언트 컴퓨터의 사용자 상태를 확인하려면 [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) 또는 다른 사용자 환경 관리 도구를 사용하는 것이 좋습니다.

    **App-V에 대한 제안이 있나요?** 여기에 제안을 추가하거나 [투표합니다.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **App-V 문제가 있나요?** [App-V TechNet 포럼을 사용하세요.](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)

## <a name="related-topics"></a>관련 항목


[App-V의 이전 버전에서 마이그레이션 계획](planning-for-migrating-from-a-previous-version-of-app-v.md)

[App-V 5.0 Sequencer 및 Client 배포](deploying-the-app-v-50-sequencer-and-client.md)

 

 





