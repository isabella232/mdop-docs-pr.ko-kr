---
title: Application Virtualization Client의 사용자 액세스 권한
description: Application Virtualization Client의 사용자 액세스 권한
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815118"
---
# Application Virtualization Client의 사용자 액세스 권한


응용 프로그램 가상화 클라이언트 관리 콘솔에서 **응용 프로그램 가상화** 노드를 마우스 오른쪽 단추로 클릭 하 여 액세스할 수 있는 **속성** 대화 상자에 있는 **사용 권한** 탭에서 관리자는 다양 한 클라이언트 함수를 사용 하는 데 필요한 권한을 사용자에 게 부여할 수 있습니다.

**참고**  사용자 권한을 변경 하기 전에 모든 사용 권한 변경이 조직의 사용자 권한 부여에 대 한 지침과 일치 해야 합니다.

 

다음 표에서는 사용자에 게 부여할 수 있는 사용 권한을 나열 하 고 설명 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용 권한 이름</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>응용 프로그램 추가</p></td>
<td align="left"><p>sfttray.exe, sftmime.exe 또는 MMC를 사용 하 여 새 OSD 파일을 클라이언트에 전달 하 여 새 응용 프로그램을 등록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>파일 시스템 캐시 크기 변경</p></td>
<td align="left"><p>파일 시스템 캐시의 크기를 늘립니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>파일 시스템 드라이브 변경</p></td>
<td align="left"><p>파일 시스템에 대해 다른 기본 설정 드라이브 문자를 선택 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>로그 설정 변경</p></td>
<td align="left"><p>클라이언트 로그 파일의 로그 수준 또는 로그 경로를 변경 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OSD 파일 변경</p></td>
<td align="left"><p>등록 된 응용 프로그램의 OSD 파일을 수정 하 여 클라이언트에 게 전달 합니다. 이는 게시 새로 고침에 영향을 주지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램 설정 지우기</p></td>
<td align="left"><p>현재 사용자의 파일 형식, 바로 가기 및 구성을 삭제 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>응용 프로그램 삭제</p></td>
<td align="left"><p>컴퓨터의 모든 사용자에 대 한 파일 시스템 및 OSD 캐시에서 응용 프로그램에 대 한 참조를 모두 제거 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램을 캐시로 가져오기</p></td>
<td align="left"><p>지정 된 SFT 파일에서 파일 시스템 캐시로 직접 응용 프로그램 데이터를 로드 합니다. 이는 모든 사용자에 게 영향을 줍니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>캐시에 응용 프로그램 로드</p></td>
<td align="left"><p>앱-V 스트리밍 서버와 같이 구성 된 원본에서 응용 프로그램의 SFT 파일 로드를 시작 합니다. 이렇게 하면 컴퓨터의 모든 사용자에 대해 응용 프로그램이 로드 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>캐시에서 응용 프로그램 잠금 및 잠금 해제</p></td>
<td align="left"><p>파일 시스템 캐시에서 응용 프로그램을 언로드하는 것을 금지 하거나 허용 합니다. 이는 컴퓨터의 모든 사용자에 게 영향을 줍니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>파일 형식 연결 관리</p></td>
<td align="left"><p>현재 사용자의 파일 형식 연결만 추가, 수정 또는 삭제 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>게시 새로 고침 설정 관리</p></td>
<td align="left"><p>컴퓨터의 모든 사용자에 대 한 게시 새로 고침 타이밍을 제어 하는 설정을 변경 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>게시 서버 관리</p></td>
<td align="left"><p>컴퓨터의 모든 사용자에 대 한 게시 서버를 추가, 수정 또는 삭제 합니다. 이 권한에는 암시적으로 게시 새로 고침 설정을 관리할 수 있는 사용 권한이 포함 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>바로 가기 게시</p></td>
<td align="left"><p>등록 된 응용 프로그램에 대 한 바로 가기를 새로 만듭니다. 또한 사용자는 로컬 파일 시스템에서 파일을 만들 수 있는 권한도 있어야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>응용 프로그램 복구</p></td>
<td align="left"><p>바로 가기 또는 파일 형식 연결을 제거 하지 않고 현재 사용자의 응용 프로그램 관련 구성을 제거 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>게시 새로 고침 시작</p></td>
<td align="left"><p>현재 사용자에 대해 예약 되지 않은 게시 새로 고침을 시작 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>오프 라인 모드 전환</p></td>
<td align="left"><p>모든 사용자의 온라인에서 오프 라인 모드로 전체 클라이언트를 변경 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>캐시에서 응용 프로그램 언로드</p></td>
<td align="left"><p>사용자 관련 설정, 바로 가기 또는 파일 형식 연결을 제거 하지 않고 모든 사용자의 파일 시스템 캐시에서 응용 프로그램 데이터를 지웁니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>모든 응용 프로그램 보기</p></td>
<td align="left"><p>사용자가 컴퓨터에 등록 된 모든 사용자에 대 한 가상 응용 프로그램을 볼 수 있도록 허용 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[사용자 액세스 권한을 변경하는 방법](how-to-change-user-access-permissions.md)

 

 





