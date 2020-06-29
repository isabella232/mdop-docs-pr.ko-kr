---
title: 가상 응용 프로그램 패키지를 편집하거나 업그레이드할지 여부를 결정하는 방법
description: 가상 응용 프로그램 패키지를 편집하거나 업그레이드할지 여부를 결정하는 방법
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817503"
---
# 가상 응용 프로그램 패키지를 편집하거나 업그레이드할지 여부를 결정하는 방법


다음 표를 사용 하 여 가상 응용 프로그램 패키지를 편집용으로 열 수 있는지 여부, 패키지의 새 버전을 만들어야 하는지 여부 또는 App-v Sequencer를 사용 하 여 어떤 옵션을 사용할 수 있는지 여부를 결정 하는 데 도움이 됩니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">편집용으로 열기</th>
<th align="left">업그레이드를 위해 열기</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>패키지 속성 보기.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 변경 내용 보기</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>연결 된 패키지 파일을 봅니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>레지스트리 설정을 편집 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>추가 패키지 설정 검토 (운영 체제 파일 속성 제외)</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>관련 Windows Installer (MSI)를 만듭니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OSD 파일을 수정 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지를 압축 및 압축 해제 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>파일 형식 연결을 추가 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>바로 가기 이름 바꾸기</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>가상화 된 레지스트리 키 상태 (재정의/병합)를 설정 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>가상화 된 폴더 상태를 설정 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>가상 파일 시스템 매핑 편집</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지에 대해 관련 된 모든 운영 체제 파일 속성을 검토 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>다른 서비스를 추가 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>다른 파일을 추가 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>연결 된 보안 설명자를 수집 하 고 구성 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>보안 업데이트를 적용 하거나 새 버전으로 업그레이드 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>다른 응용 프로그램을 추가 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p>응용 프로그램이 열리도록 업데이트를 적용 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터를 다시 시작 해야 하는 업데이트를 적용 합니다.</p></td>
<td align="left"><p>아니오</p></td>
<td align="left"><p>예</p></td>
</tr>
</tbody>
</table>

 

## 관련 항목


[기존 가상 응용 프로그램을 편집하는 방법](how-to-edit-an-existing-virtual-application.md)

[기존 가상 응용 프로그램을 업그레이드하는 방법](how-to-upgrade-an-existing-virtual-application.md)

 

 





