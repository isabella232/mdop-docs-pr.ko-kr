---
title: 바로 가기 및 파일 형식 연결 동작을 구성하는 방법
description: 바로 가기 및 파일 형식 연결 동작을 구성하는 방법
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817913"
---
# 바로 가기 및 파일 형식 연결 동작을 구성하는 방법


바로 가기 및 파일 형식 연결 (FTA) 게시 정책은 게시 새로 고침 작업을 수행 하는 동안 게시 서버에 의해 클라이언트로 전송 되는 게시 XML 파일에 의해 정의 및 제어 됩니다. 클라이언트는이 정보를 받을 때 아이콘과 FTAs와 같은 응용 프로그램에 대 한 새로 게시 된 데이터를 추가 합니다. 그런 다음 오래 된 게시 데이터를 제거 합니다.

App-v 버전 4.6에서 관리자가이 동작을 제어할 수 있도록 두 개의 레지스트리 키 값이 정의 되었습니다. 기본적으로 클라이언트 콘솔을 사용 하 여 로컬로 만든 바로 가기가 이제 유지 됩니다.

## 바로 가기 및 FTA 동작을 변경 하는 방법


클라이언트 구성 레지스트리 키, "FileTypePolicy" 및 "ShortcutPolicy"에 대해 새로운 DWORD 레지스트리 값 두 개가 정의 되었습니다. 이러한 DWORD 레지스트리 값은 기본적으로 제공 되지 않지만 수동으로 추가할 수 있습니다. 구성 레지스트리 키는 HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.에 있습니다.

다음 표에는 4 개의 정책 값이 정의 되어 있으며,이는 두 레지스트리 키 값에 모두 적용 됩니다. 다음 목록에는 레지스트리 설정에 대 한 숫자 값과 게시 새로 고침 작업의 파일 형식 또는 바로 가기에 적용 되는 동작이 나와 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>이름</p></td>
<td align="left"><p>유형</p></td>
<td align="left"><p>데이터 (예제)</p></td>
<td align="left"><p>설명</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileTypePolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0x2 (App-V 4.6)</p></td>
<td align="left"><p>(0x0) – 동일한 게시 정보 원본에서 기존 항목을 제거 하 고 로컬에 추가 된 항목만 유지</p>
<p>(0x1) – "ServerOnly"-동일한 게시 정보 원본 및 로컬에 추가 된 모든 항목에서 오래 된 항목을 제거 하 고 새 항목을 추가 합니다.</p>
<p>(0x2)-"ClientAndServer"-동일한 게시 정보 원본에서 오래 된 항목을 제거 하 고, 로컬에 추가 된 항목을 유지 하 고, 새 항목을 추가 합니다 (App-v 4.6 용이 없는 경우 기본값).</p>
<p>(0x3) – "NoChange"-파일 형식 또는 바로 가기를 변경 하지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ShortcutPolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>기본값 = 0x2</p></td>
<td align="left"><p>(0x0) – 동일한 게시 정보 원본에서 기존 항목을 제거 하 고 로컬에 추가 된 항목만 유지</p>
<p>(0x1) – "ServerOnly"-동일한 게시 정보 원본에 있는 오래 된 항목 및 로컬로 추가 된 항목을 제거 하 고 새 항목을 추가 합니다.</p>
<p>(0x2)-"ClientAndServer"-동일한 게시 정보 원본에서 오래 된 항목을 제거 하 고, 로컬로 추가 된 항목을 유지 하 고, 새 항목을 추가 합니다 (기본값은 없는 경우).</p>
<p>(0x3) – "NoChange"-파일 형식 또는 바로 가기를 변경 하지 않습니다.</p></td>
</tr>
</tbody>
</table>

 

**참고**  텍스트 값은 게시 XML 파일의 XML 특성에 대 한 값을 참조 합니다.사용자 지정 HTTP 게시 솔루션을 구현한 경우 이러한 값을 수동으로 설정할 수 있습니다.

 

 

 





