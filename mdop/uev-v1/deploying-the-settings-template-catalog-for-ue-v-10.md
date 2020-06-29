---
title: UE-V 1.0에 대한 설정 템플릿 카탈로그 배포
description: UE-V 1.0에 대한 설정 템플릿 카탈로그 배포
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826633"
---
# UE-V 1.0에 대한 설정 템플릿 카탈로그 배포


사용자 지정 설정 위치 템플릿은 Microsoft UE-V (User Experience Virtualization) 컴퓨터 또는 SMB (서버 메시지 블록) 네트워크 공유의 폴더 경로에 저장 될 수 있습니다. 컴퓨터의 예약 된 작업은이 위치에서 새 서식 파일이 나 업데이트 된 템플릿을 확인 합니다. 이 작업은 매일이 위치를 확인 하 고이 폴더의 서식 파일을 기반으로 동기화 동작을 업데이트 합니다. 마지막 검사 이후이 폴더에서 추가 되거나 업데이트 된 서식 파일은 UE-V agent에 의해 등록 됩니다. 이 폴더에서 제거 된 UE-V agent deregisters 템플릿입니다. 예약 된 작업이 시스템으로 실행 됩니다. 최소한 네트워크 공유는 Domain Computers 그룹에 대 한 사용 권한을 부여 해야 합니다. 또한 저장 된 서식 파일을 관리 하는 관리자에 게 네트워크 공유 폴더에 대 한 액세스 권한을 부여 합니다. 사용자 지정 설정 위치 서식 파일에 대 한 자세한 내용은 [ue-v 1.0에 대 한 사용자 지정 서식 파일 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)을 참조 하세요.

**UE-V 용 설정 템플릿 카탈로그를 구성 하려면**

1.  컴퓨터에서 UE-V 설정 템플릿 카탈로그를 저장할 새 폴더를 만듭니다.

2.  설정 템플릿 카탈로그 폴더에 대해 다음 SMB (공유 수준) 권한을 설정 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>사용자 계정</strong></th>
    <th align="left"><strong>권장 권한</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>모두</p></td>
    <td align="left"><p>권한 없음</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>도메인 컴퓨터</p></td>
    <td align="left"><p>읽기 사용 권한 수준</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>관리자</p></td>
    <td align="left"><p>읽기/쓰기 권한 수준</p></td>
    </tr>
    </tbody>
    </table>

     

3.  설정 서식 파일 카탈로그 폴더에 대해 다음 NTFS 사용 권한을 설정 합니다.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">사용자 계정</th>
    <th align="left">권장 되는 사용 권한</th>
    <th align="left">적용 대상</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>만든이/소유자</p></td>
    <td align="left"><p>모든 권한</p></td>
    <td align="left"><p>이 폴더, 하위 폴더 및 파일</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>도메인 컴퓨터</p></td>
    <td align="left"><p>폴더 내용 나열 및 읽기</p></td>
    <td align="left"><p>이 폴더, 하위 폴더 및 파일</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>모두</p></td>
    <td align="left"><p>권한 없음</p></td>
    <td align="left"><p>권한 없음</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>관리자</p></td>
    <td align="left"><p>모든 권한</p></td>
    <td align="left"><p>이 폴더, 하위 폴더 및 파일</p></td>
    </tr>
    </tbody>
    </table>

     

4.  **확인** 을 클릭 하 여 대화 상자를 닫습니다.

## 관련 항목


[UE-V 1.0 배포](deploying-ue-v-10.md)

[UE-V 1.0에 대한 사용자 지정 템플릿 배포 계획](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





