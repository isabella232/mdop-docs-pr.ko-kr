---
title: MED-V 이미지를 만들고 테스트하는 방법
description: MED-V 이미지를 만들고 테스트하는 방법
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827043"
---
# MED-V 이미지를 만들고 테스트하는 방법


MED-V 관리자가 med-v 이미지를 업로드 한 후에는 MED-V 작업 영역과 연결 하 고 웹을 통해 클라이언트에 배포 하거나 MED-V 패키지에 추가 하거나 타사 시스템을 사용 하 여 클라이언트에 다운로드할 수 있습니다. 먼저 테스트 이미지를 만들고이를 배포 하기 전에 MED-V 클라이언트에서 테스트 하는 것이 좋습니다.

MED-V 이미지를 만들 때 다음 단계를 거칩니다.

1.  **로컬 테스트 이미지**-로컬에서 테스트할 수 있는 기본 이미지입니다.

2.  **로컬 압축 이미지**-이미지를 테스트 한 후에는 테스트 하기 전에 있던 이미지가 압축 됩니다. 테스트 중에 발생 한 변경 내용은 압축 된 이미지에 포함 되어 있지 않습니다.

3.  **서버에서 압축 한 이미지**-압축 된 이미지가 서버에 업로드 됩니다.

## MED-V 테스트 이미지를 만드는 방법


**새 MED-V 테스트 이미지를 만들려면**

1.  **이미지** 관리 단추를 클릭 합니다.

    **이미지** 모듈을 표시 합니다.

    -   **Images** 모듈은 다음 창으로 구성 됩니다.

        -   **로컬 테스트 이미지**-로컬의 압축을 푼 이미지

        -   로컬 **압축 이미지**-로컬 컴퓨터에 압축 된 모든 이미지

        -   **서버에 압축 된 이미지**-압축 되어 서버에 업로드 한 모든 이미지

    -   서버 창의 **로컬 압축 이미지** 및 **압축 된 이미지** 에서 각 이미지의 최신 버전이 부모 노드로 표시 됩니다. 부모 노드를 클릭 하 여 다른 모든 기존 버전의 이미지를 표시 합니다.

2.  **로컬 테스트 이미지** 창에서 **새로 만들기**를 클릭 합니다.

3.  **테스트 이미지 만들기** 대화 상자에서 다음 중 하나를 수행 하 여 med-v 테스트 이미지로 구성 하려는 가상 컴퓨터 이미지를 선택 합니다.

    -   **기본 이미지** 파일 필드에 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리의 전체 경로를 입력 합니다.

    -   **찾아보기를** 클릭 하 여 med-v에 대해 준비 된 MICROSOFT 가상 PC 이미지가 있는 디렉터리로 이동 합니다.

4.  **이미지 이름** 필드에서 원하는 이름을 입력 하거나 선택 합니다.

    **참고**  Image 이름에는 다음 문자를 포함할 수 없습니다: space " &lt; &gt; | \\ / : \* ?

     

5.  **확인**을 클릭합니다.

    다음 표에 정의 된 속성을 사용 하 여 호스트 컴퓨터에 새 MED-V 테스트 이미지가 만들어집니다.

    MED-V 작업 영역 이미지를 구성 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 정책 구성을](configuring-med-v-workspace-policies.md)참조 하세요.

**로컬 테스트 이미지 속성**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">속성</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이미지 이름</p></td>
<td align="left"><p>관리자가 이미지를 만들었을 때 정의 된 테스트 이미지의 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>이미지 경로</p></td>
<td align="left"><p>테스트 이미지의 로컬 경로입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>만들어져야</p></td>
<td align="left"><p>테스트 이미지를 만든 날짜입니다.</p></td>
</tr>
</tbody>
</table>

 

## MED-V 클라이언트에서 MED-V 이미지를 테스트 하는 방법


MED-V 테스트 이미지를 만든 후 다음 절차를 사용 하 여 이미지를 로컬로 테스트 합니다.

**MED-V 이미지를 테스트 하려면**

1.  **정책** 관리 단추를 클릭 합니다.

2.  **정책** 모듈에서 다음 작업을 수행 하 여 med-v 테스트 이미지를 med-v 작업 영역에 할당 합니다.

    1.  **가상 컴퓨터** 탭을 클릭 합니다.

    2.  할당 된 **이미지** 필드에서 직접 만든 med-v 테스트 이미지를 선택 합니다. 테스트 이미지가 목록에 없으면 **새로 고침**을 클릭 합니다.

    3.  도구 모음에서 **변경 내용 저장**을 클릭 합니다.

3.  다른 MED-V 작업 영역 설정을 테스트 하도록 구성 합니다. 자세한 내용은 [Med-v 작업 영역 정책 구성을](configuring-med-v-workspace-policies.md)참조 하세요.

4.  MED-V 클라이언트를 시작 합니다.

5.  **테스트 실행 확인** 상자에서 **테스트 이미지 사용**을 클릭 합니다.

6.  MED-V 작업 영역 테스트 이미지를 테스트 합니다.

    MED-V 클라이언트를 시작 하 고 실행 하는 방법에 대 한 자세한 내용은 [Med-v 클라이언트 작업](med-v-client-operations.md)을 참조 하세요.

**참고**  이미지를 테스트 하는 동안 VPC를 열고 이미지를 변경 하지 마세요.

 

**참고**  이미지를 테스트 하는 경우 세션 간에 이미지에 변경 내용이 저장 되지 않습니다. 대신 별도의 임시 파일에 저장 됩니다. 이는 이미지가 프로덕션 환경에서 압축 및 실행 될 때 깨끗 한 원본 이미지입니다.

 

## 관련 항목


[MED-V에 대한 가상 PC 이미지 만들기](creating-a-virtual-pc-image-for-med-v.md)

[MED-V 작업 영역 만들기](creating-a-med-v-workspacemedv-10-sp1.md)

[MED-V 작업 영역 정책 구성](configuring-med-v-workspace-policies.md)

[MED-V 클라이언트 작업](med-v-client-operations.md)

 

 





