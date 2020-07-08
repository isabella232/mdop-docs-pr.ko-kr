---
title: UE-V 1.0에 대한 설정 저장소 위치 배포
description: UE-V 1.0에 대한 설정 저장소 위치 배포
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826638"
---
# UE-V 1.0에 대한 설정 저장소 위치 배포


Microsoft UE-V (User Experience Virtualization) 배포에는 사용자 설정이 설정 패키지 파일에 저장 되어 있는 설정 저장소 위치가 필요 합니다. 설정 저장소 위치는 다음 두 가지 방법 중 하나로 구성할 수 있습니다.

-   **Active directory home directory** – active directory에서 사용자에 대해 홈 디렉터리가 정의 된 경우 ue-v agent가이 위치를 사용 하 여 설정 위치 패키지를 저장 합니다. UE-V agent가 홈 디렉터리의 루트 아래에 있는 사용자 관련 저장소 폴더를 동적으로 만듭니다. 설정 저장소 위치가 정의 되지 않은 경우 에이전트는 Active Directory의 홈 디렉터리만 사용 합니다.

-   **설정 저장소 공유 만들기** – 설정 저장소 공유는 ue-v 사용자가 액세스할 수 있는 표준 네트워크 공유입니다.

## UE-V 설정 저장소 공유 배포


설정 저장소 공유를 만들 때 액세스가 필요한 사용자 에게만 액세스를 제한 해야 합니다. 필요한 사용 권한은 아래 표에 나와 있습니다.

**UE-V 네트워크 공유를 배포 하려면**

1.  UE-V 사용자에 대 한 새 보안 그룹을 만듭니다.

2.  중앙에서 찾은 컴퓨터에 UE-V 설정 패키지를 저장할 새 폴더를 만든 다음이 폴더에 대 한 그룹 권한이 있는 UE-V 사용자에 게이를 부여 합니다. UE-V를 지 원하는 관리자는이 공유 폴더에 대 한 사용 권한이 필요 합니다.

3.  설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>사용자 계정</strong></th>
    <th align="left"><strong>권장 되는 사용 권한</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>모두</p></td>
    <td align="left"><p>권한 없음</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UE-V 사용자의 보안 그룹</p></td>
    <td align="left"><p>모든 권한</p></td>
    </tr>
    </tbody>
    </table>

     

4.  설정 저장소 위치 폴더에 대해 다음 NTFS 사용 권한을 설정 합니다.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>사용자 계정</strong></th>
    <th align="left"><strong>권장 되는 사용 권한</strong></th>
    <th align="left"><strong>Folder</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>만든이/소유자</p></td>
    <td align="left"><p>모든 권한</p></td>
    <td align="left"><p>하위 폴더 및 파일만</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>UE-V 사용자의 보안 그룹</p></td>
    <td align="left"><p>폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</p></td>
    <td align="left"><p>이 폴더만</p></td>
    </tr>
    </tbody>
    </table>

     

5.  **확인** 을 클릭 하 여 대화 상자를 닫습니다.

이 사용 권한 구성에서는 사용자가 설정 저장소에 대 한 폴더를 만들 수 있습니다. UE-V agent는 `settingspackage` 사용자 컨텍스트에서 실행 되는 동안 폴더를 만들고 보호 합니다. 사용자가 해당 폴더에 대 한 모든 권한을 받습니다 `settingspackage` . 다른 사용자는이 폴더에 대 한 액세스 권한을 상속 받지 않습니다. 사용자의 컨텍스트에서 실행 되는 에이전트에 의해 자동으로 수행 되므로 개별 사용자 디렉터리를 만들고 보안 하지 않아도 됩니다.

**참고**  Windows server가 설정 저장소 공유에 사용 되는 경우 추가 보안을 구성할 수 있습니다. 로컬 관리자의 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 하도록 UE-V를 구성할 수 있습니다. 추가 보안을 사용 하도록 설정 하려면 다음을 완료 합니다.

1.  "RepositoryOwnerCheckEnabled" 이라는 **REG \ _DWORD** 레지스트리 키를 **HKEY \ _LOCAL \ _MACHINE** 에 추가 합니다. \\software\\microsoft\\uev\\agent\\configuration.

2.  레지스트리 키 값을 1로 설정 합니다.

 

## 관련 항목


[UE-V 1.0 배포](deploying-ue-v-10.md)

[UE-V 1.0에 지원되는 구성](supported-configurations-for-ue-v-10.md)

[Ue-v 생성기를 설치 하는](installing-the-ue-v-generator.md) 사용자 환경 가상화 설정 템플릿 및 설정 패키지에 대 한 중앙 저장소 배포

[UE-V 에이전트 배포](deploying-the-ue-v-agent.md)

 

 





