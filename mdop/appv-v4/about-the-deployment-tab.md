---
title: 배포 탭 정보
description: 배포 탭 정보
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819963"
---
# 배포 탭 정보


응용 프로그램 가상화 시퀀서 콘솔의 **배포** 탭을 사용 하 여 시퀀싱 하려는 응용 프로그램에 대 한 정보를 변경 합니다. 이 탭에는 다음 요소가 포함 되어 있습니다.

## 서버 URL


**서버 URL** 컨트롤을 사용 하 여 가상 응용 프로그램 서버 구성 설정을 지정 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">컨트롤</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>프로토콜</strong></p></td>
<td align="left"><p>가상 응용 프로그램 서버에서 응용 프로그램 가상화 데스크톱 클라이언트로 시퀀싱 된 응용 프로그램 패키지를 스트림할 프로토콜을 선택할 수 있습니다. 다음 프로토콜을 사용할 수 있습니다.</p>
<ul>
<li><p><strong>RTSP </strong> — 기본값은 실시간 스트리밍 프로토콜이 가상화 지원 응용 프로그램의 교환을 제어 하도록 지정 합니다.</p></li>
<li><p><strong>RTSPS </strong> -전송 계층 보안이 포함 된 실시간 스트리밍 프로토콜이 시퀀싱 된 응용 프로그램 패키지의 교환을 제어 하도록 지정 합니다.</p></li>
<li><p><strong>파일 </strong> -시퀀싱 된 응용 프로그램을 파일 공유에서 스트림할 것을 지정 합니다.</p></li>
<li><p><strong>HTTPS </strong> -보안 하이퍼텍스트 전송 프로토콜이 패키지의 교환을 제어 하도록 지정 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>이름의</strong></p></td>
<td align="left"><p>소프트웨어 패키지를 응용 프로그램 가상화 데스크톱 클라이언트로 스트리밍하는 가상 응용 프로그램 서버 그룹의 앞에 있는 가상 응용 프로그램 서버 또는 부하 분산 장치를 선택할 수 있습니다. 시퀀싱 된 응용 프로그램 패키지를 만들려면이 항목을 완료 해야 하지만 기본% SFT_SOFTGRIDSERVER% 환경 변수를 가상 응용 프로그램 서버의 실제 호스트 이름 또는 IP 주소로 변경할 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>정적 호스트 이름 또는 IP 주소를 지정 하지 않도록 선택한 경우 각 응용 프로그램 가상화 데스크톱 클라이언트에서 SFT_SOFTGRIDSERVER 라는 환경 변수를 설정 해야 합니다. 해당 값은이 클라이언트&#39;s 응용 프로그램 원본에 해당 하는 부하 분산 장치 또는 가상 응용 프로그램 서버의 호스트 이름 또는 IP 주소 여야 합니다. 이 환경 변수를 사용자 변수가 아닌 시스템 변수로 만들어야 합니다. 이 변수를 할당 하는 동안이 컴퓨터에서 실행 되는 모든 Application Virtualization Desktop 클라이언트 세션을 닫은 후 열어야 다시 시작 된 세션에서 새 응용 프로그램 원본을 인식 해야 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Port</strong></p></td>
<td align="left"><p>가상 응용 프로그램 서버 또는 부하 분산이 패키지에 대 한 응용 프로그램 가상화 데스크톱 클라이언트&#39;s 요청을 수신 대기 하는 포트를 지정할 수 있도록 합니다. 이 정보는 패키지를 만드는 데 필요 하지만 변경할 수 있습니다. 기본 포트는 554입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>경로</strong></p></td>
<td align="left"><p>소프트웨어 패키지가 저장 되 고 스트리밍되는 가상 응용 프로그램 서버의 상대 경로를 지정할 수 있도록 합니다. 이 정보는 SFT 파일을 콘텐츠의 하위 디렉터리에 저장 하는 경우 패키지를 만드는 데 필요 합니다. 그렇지 않은 경우에는이 정보가 필요 하지 않습니다.</p></td>
</tr>
</tbody>
</table>



## 운영 체제


**Os** 컨트롤을 사용 하 여 응용 프로그램의 운영 체제 요구 사항을 지정 합니다. Application Virtualization 데스크톱 클라이언트가 선택 된 운영 체제를 지원할 수 없는 경우에는 응용 프로그램이 시작 되지 않습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">컨트롤</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>사용할 수 있는 운영 체제</strong></p></td>
<td align="left"><p>패키지의 응용 프로그램을 지원할 수 있는 운영 체제 목록을 표시 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>선택한 운영 체제</strong></p></td>
<td align="left"><p>패키지의 응용 프로그램을 지 원하는 선택 된 운영 체제 목록을 표시 합니다.</p></td>
</tr>
</tbody>
</table>



## 출력 옵션


**출력 옵션** 컨트롤을 사용 하 여 설치할 응용 프로그램의 출력 옵션을 지정 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">컨트롤</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>압축 알고리즘</strong></p></td>
<td align="left"><p>네트워크를 통해 스트리밍하는 SFT 파일을 압축 하는 방법을 선택 하는 데 사용 합니다. 다음 압축 방법 중 하나를 선택 합니다.</p>
<ul>
<li><p><strong>압축 됨 </strong> -SFT 파일을 ZLIB 형식으로 압축 하도록 지정 합니다 <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> .</p></li>
<li><p><strong>압축 안 함 </strong> — 기본값은 SFT 파일이 압축 되지 않도록 지정 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>보안 설명자 적용</strong></p></td>
<td align="left"><p>클라이언트에 배포 된 후 패키지에 있는 응용 프로그램의 보안 설명자를 적용 하려면 선택 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Microsoft Windows Installer (MSI) 패키지 생성</strong></p></td>
<td align="left"><p>Windows Installer를 사용 하 여 시퀀싱 된 응용 프로그램 패키지를 설치 또는 배포 하려면 선택 합니다. 시퀀서를 사용 하 여 변경 하는 경우 변경 내용이 Windows Installer 파일에 포함 되지 않습니다. Windows Installer 파일은 항상 하드 디스크에 저장 된 sft 파일을 사용 하 여 생성 됩니다.</p></td>
</tr>
</tbody>
</table>



## 관련 항목


[배포 속성을 변경하는 방법](how-to-change-deployment-properties.md)

[Sequencer Console](sequencer-console.md)









