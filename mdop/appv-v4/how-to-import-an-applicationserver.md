---
title: 응용 프로그램을 가져오는 방법
description: 응용 프로그램을 가져오는 방법
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817403"
---
# 응용 프로그램을 가져오는 방법


일반적으로 응용 프로그램 가상화 관리 서버에서 스트림에 사용할 수 있도록 응용 프로그램을 가져옵니다. 수동으로 응용 프로그램을 추가할 수도 있지만 응용 프로그램에 대 한 자세한 정보를 제공 해야 합니다. 자세한 내용은 [응용 프로그램을 수동으로 추가 하는 방법을](how-to-manually-add-an-application.md)참조 하세요.

**참고**  응용 프로그램을 가져오려면 서버에서 사용할 수 있는 파일의 순차화 된 OSD (개방형 소프트웨어 설명자) 파일이 나 해당 Sequencer 프로젝트 (SPRJ) 파일이 있어야 합니다.

 

응용 프로그램을 가져올 때 서버는 **시스템 옵션** 대화 상자의 **일반** 탭에 있는 **기본 콘텐츠 경로** 필드의 값으로 구성 되었는지 확인 해야 합니다 (App-v server 콘솔의 **application Virtualization System** 노드를 마우스 오른쪽 단추로 클릭 하 여 액세스할 수 있음). 기본 콘텐츠 경로 값은 응용 프로그램을 가져올 위치를 정의 하 고, 가져오기 프로세스 중에이 값을 사용 하 여 SFT 파일과 아이콘 바로 가기의 OSD 파일에 정의 된 경로를 수정 합니다. OSD 파일에서 SFT 파일의 경로는 CODEBASE HREF 엔트리에 지정 되며 아이콘에 대 한 경로는 바로 가기 항목에 지정 되어 있습니다.

가져오기 프로세스가 진행 되는 동안 OSD 파일의 이러한 두 경로에 지정 된 프로토콜, 서버 및 포트가 기본 콘텐츠 경로의 값으로 바뀝니다. 다음 표에서는 가져오기 경로에 영향을 주는 방법의 예를 보여 줍니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">기본 콘텐츠 경로</th>
<th align="left">OSD 파일 코드 베이스 HREF</th>
<th align="left">결과 값</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**응용 프로그램을 가져오려면**

1.  왼쪽 창에서 **응용 프로그램** 노드를 마우스 오른쪽 단추로 클릭 하 고 **응용 프로그램 가져오기를**선택 합니다.

2.  **열기** 대화 상자에서 응용 프로그램의 SPRJ 또는 OSD 파일로 이동 합니다. 파일을 강조 표시 하 고 **열기**를 클릭 합니다.

3.  **새 응용 프로그램 마법사**에서 스트리밍할 응용 프로그램에 대해 **사용** 상자가 선택 되어 있는지 확인 합니다. 또한 설명을 입력 하 고 서버 및 파일 경로를 확인할 수도 있습니다. 또한 라이선스 및 서버 그룹을 설정한 경우 해당 사용자를 선택할 수 있습니다.

4.  **다음**을 클릭합니다.

5.  게시 된 **바로 가기** 화면에서 응용 프로그램 바로 가기를 클라이언트 컴퓨터에 표시할 위치에 해당 하는 확인란을 선택 합니다.

6.  **다음**을 클릭합니다.

7.  **파일 연결** 화면에서이 응용 프로그램에 새 파일 연결을 추가할 수 있습니다. 이렇게 하려면 **추가**를 클릭 하 고 확장명 (앞에 있는 점을 포함 하지 않음)을 입력 한 다음 설명을 입력 하 고 **확인**을 클릭 합니다.

    **참고**  Sequencer 4.0으로 시퀀싱 된 응용 프로그램은 관리 콘솔을 통해 가져오거나 만들 때 **파일 연결** 대화 상자를 채웁니다. 이전 Sequencer 버전 패키지를 사용 하는 응용 프로그램은 그렇지 않습니다.

     

8.  **다음**을 클릭합니다.

9.  **액세스 권한** 화면에서 **추가**를 클릭 합니다.

10. **그룹 선택** 대화 상자를 완료 합니다. 완료 되 면 **확인**을 클릭 합니다.

11. **다음**을 클릭합니다.

12. **요약** 화면에서 가져오기 설정을 검토할 수 있습니다. **마침을**클릭 하거나 **뒤로** 를 클릭 하 여 가져오기를 변경 하거나 **취소** 를 클릭 하 여 가져오기를 취소 합니다.

## 관련 항목


[Server Management Console에서 응용 프로그램 그룹을 관리하는 방법](how-to-manage-application-groups-in-the-server-management-console.md)

[Server Management Console에서 응용 프로그램을 관리하는 방법](how-to-manage-applications-in-the-server-management-console.md)

[수동으로 응용 프로그램을 추가하는 방법](how-to-manually-add-an-application.md)

 

 





