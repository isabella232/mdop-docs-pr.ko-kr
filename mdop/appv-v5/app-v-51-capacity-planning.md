---
title: App-V 5.1 용량 계획
description: App-V 5.1 용량 계획
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814785"
---
# App-V 5.1 용량 계획


다음 권장 사항은 조직의 App-v 5.1 인프라에 적합 한 용량 계획 정보를 결정 하는 데 도움이 되는 기준으로 사용할 수 있습니다.

**중요**  이 섹션의 정보는 App-v 5.1 배포 계획을 위한 일반적인 가이드로만 사용 하세요. 시스템 용량 요구 사항은 하드웨어 및 응용 프로그램 환경의 특정 정보에 따라 달라 집니다. 또한이 문서에 표시 되는 성과 번호는 예제 이며 결과는 다를 수 있습니다.

 

## 프로젝트 범위 결정


App-v 5.1 인프라를 디자인 하기 전에 프로젝트의 범위를 결정 해야 합니다. 범위는 사실상 사용할 수 있는 응용 프로그램을 결정 하 고 대상 사용자 및 해당 위치를 식별 하는 데에도 사용 됩니다. 이 정보는 구현 해야 하는 App-v 5.1 인프라 유형을 결정 하는 데 도움이 됩니다. 프로젝트 범위에 대 한 결정은 조직의 특정 요구 사항에 근거 해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>응용 프로그램 범위 결정</p></td>
<td align="left"><p>가상화 할 응용 프로그램에 따라 App-v 5.1 인프라를 다양 한 방식으로 설정할 수 있습니다. 첫 번째 작업은 가상화 하려는 응용 프로그램을 정의 하는 것입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>위치 범위 결정</p></td>
<td align="left"><p>위치 범위는 가상 응용 프로그램을 실행할 계획인 실제 위치 (예: enterprise 전체 또는 특정 지리적 위치)를 나타냅니다. 또한 가상 응용 프로그램을 실행 하는 사용자 집단 (예: 단일 부서)을 참조할 수 있습니다. 연결 경로 뿐만 아니라 각 위치에 대 한 사용 가능한 대역폭과 가상화 된 응용 프로그램을 사용 하는 사용자 수 및 WAN 연결 속도를 포함 하는 네트워크 맵을 구해야 합니다.</p></td>
</tr>
</tbody>
</table>

 

## 어떤 App-v 5.1 인프라가 필요 하다는 것을 확인 합니다.


**중요**  다음 두 모델에서는 가상 응용 프로그램을 실행 하려는 컴퓨터에 App-v 5.1 클라이언트를 설치 해야 합니다.

Microsoft 시스템 센터 구성 관리자와 같은 ESD (전자 소프트웨어 배포) 솔루션을 사용 하 여 App-v 5.1 환경을 관리할 수도 있습니다. 자세한 내용은 [전자 소프트웨어 배포를 사용 하 여 app-v 5.1 패키지를 배포 하는 방법을](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md)참조 하세요.

 

-   **독립 실행형 모델** -독립 실행형 모델을 통해 가상 응용 프로그램을 Windows Installer로 설정 하 여 스트리밍 없이 배포할 수 있습니다. 독립 실행형 모드의 app-v 5.1는 시퀀서 및 클라이언트로 구성 됩니다. 추가 구성 요소가 필요 하지 않습니다. 시퀀싱 이라는 프로세스를 사용 하 여 응용 프로그램의 가상화를 준비 합니다. 자세한 내용은 [앱-V 5.1 시퀀서 및 클라이언트 배포 계획](planning-for-the-app-v-51-sequencer-and-client-deployment.md)을 참조 하세요. 다음과 같은 시나리오에는 독립 실행형 모델을 사용할 것을 권장 합니다.

    -   앱-V 5.1 인프라에 연결할 수 없는 연결이 끊긴 원격 사용자

    -   소프트웨어 관리 시스템을 실행 중인 경우 (예: 구성 관리자 2012)

    -   네트워크 대역폭 제한으로 인해 전자 소프트웨어 배포가 금지 되는 경우

-   **전체 인프라 모델** -전체 인프라 모델은 소프트웨어 배포, 관리 및 보고 기능을 제공 합니다. 또한 네트워크를 통해 응용 프로그램의 스트리밍을 포함 합니다. App-v 5.1 전체 인프라 모델은 하나 이상의 App-v 5.1 관리 서버로 구성 됩니다. 관리 서버를 사용 하 여 모든 클라이언트에 응용 프로그램을 게시할 수 있습니다. 게시 프로세스에는 가상 응용 프로그램 아이콘과 바로 가기가 대상 컴퓨터에 배치 됩니다. 또한 응용 프로그램을 로컬 사용자에 게 스트리밍할 수 있습니다. 관리 서버를 설치 하는 방법에 대 한 자세한 내용은 [app-v 5.1 서버 배포 계획](planning-for-the-app-v-51-server-deployment.md)을 참조 하세요. 전체 인프라 모델은 다음과 같은 시나리오에 적합 합니다.

    **중요**  앱-V 5.1 전체 인프라 모델에는 Microsoft SQL Server가 구성 데이터를 저장 해야 합니다. 자세한 내용은 [앱-V 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.

     

    -   관리 서버를 사용 하 여 대상 컴퓨터에 응용 프로그램을 게시 하려는 경우

    -   대상 컴퓨터에 응용 프로그램을 신속 하 게 프로 비전 합니다.

    -   App-v 5.1 보고 기능을 사용 하려는 경우

## 엔드 투 엔드 서버 크기 조정 지침


다음 섹션에서는 종단간 앱-V 5.1 크기 조정 및 계획에 대 한 정보를 제공 합니다. 자세한 내용은 후속 섹션을 참조 하세요.

**참고**  클라이언트의 라운드트립 응답 시간은 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 게시 서버 로부터 성공적으로 알림을 수신 하는 데 걸리는 시간입니다. 게시 서버의 라운드트립 응답 시간은 게시 서버를 실행 하는 컴퓨터에서 관리 서버 로부터 성공적인 패키지 메타 데이터 업데이트를 수신 하는 데 걸리는 시간입니다.

 

-   2만 클라이언트는 단일 게시 서버를 대상으로 하 여 적절 한 라운드트립 시간에 패키지 새로 고침을 얻을 수 있습니다. ( &lt; 3 초)

-   단일 관리 서버는 허용 되는 라운드트립 시간에 패키지 메타 데이터 새로 고침에 대 한 최대 50 게시 서버를 지원할 수 있습니다. ( &lt; 5 초)

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> 앱-V 5.1 관리 서버 용량 계획 권장 사항


앱-V 5.1 게시 서버는 패키지 새로 고침 요청과 패키지 새로 고침 응답을 위한 관리 서버가 필요 합니다. 그런 다음 관리 서버에서 정보를 검색 하기 위해 관리 데이터베이스로 정보를 보냅니다. 앱-V 5.1 관리 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.

**참고**  App-v 5.1 게시 서버의 기본 새로 고침 시간은 10 분입니다.

 

여러 동시 게시 서버가 패키지 메타 데이터 새로 고침을 위해 단일 관리 서버에 연결 되 면 다음 세 가지 요소가 게시 서버의 라운드트립 응답 시간에 영향을 줍니다.

1.  동시 요청을 보내는 게시 서버 수입니다.

2.  관리 서버에 구성 된 연결 그룹의 수입니다.

3.  관리 서버에 구성 된 액세스 그룹의 수입니다.

다음 표에서는 라운드트립 시간에 영향을 주는 각 요소에 대 한 자세한 정보를 보여 줍니다.

**참고**  라운드트립 응답 시간은 관리 서버에서 성공적인 패키지 메타 데이터 업데이트를 받기 위해 App-v 5.1 게시 서버를 실행 하는 컴퓨터에 걸리는 시간입니다.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">라운드트립 응답 시간에 영향을 주는 요인</th>
<th align="left">추가 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>동시에 패키지 메타 데이터 새로 고침을 요청 하는 게시 서버 수입니다.</p></td>
<td align="left"><p></p>
<ul>
<li><p>단일 관리 서버는 게시 메타 데이터를 동시에 요청 하는 최대 320 게시 서버에 응답할 수 있습니다.</p></li>
<li><p>320 pub 서버에 대 한 라운드트립 응답 시간은 ~ 40 초입니다.</p></li>
<li><p>&lt;메타 데이터를 동시에 요청 하는 50 게시 서버의 경우 라운드트립 응답 시간은 &lt; 5 초입니다.</p></li>
<li><p>50에서 320 게시 서버로 응답 시간이 선형적으로 증가 합니다 (약 2x).</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>관리 서버에 구성 된 연결 그룹의 수입니다.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>최대 100 개의 연결 그룹에 대해 게시 서버의 라운드트립 응답 시간이 크게 변경 되지 않습니다.</p></li>
<li><p>100-400 연결 그룹의 경우 라운드트립 응답 시간에 약간의 선형 증가를 갖습니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>관리 서버에 구성 된 액세스 그룹의 수입니다.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>최대 40 액세스 그룹의 경우 게시 서버의 라운드트립 응답 시간에 선형 (약 3/3)이 증가 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

다음 표에는 각 이전 요인에 대 한 예제 값이 표시 되어 있습니다. 각 변형에서 120 패키지는 App-v 5.1 관리 서버에서 새로 고쳐집니다.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">변형</th>
<th align="left">연결 그룹 수</th>
<th align="left">액세스 그룹 수</th>
<th align="left">게시 서버 수</th>
<th align="left">네트워크 연결 형식 게시 서버/관리 서버</th>
<th align="left">게시 서버에서 라운드트립 응답 시간 (초)</th>
<th align="left">관리 서버의 CPU 이용률</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>게시 서버는 메타 데이터 게시를 위해 관리 서버에 동시에 연결 합니다.</p></td>
<td align="left"><p>게시 서버 수</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>300</p></li>
<li><p>315</p></li>
<li><p>320</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>5mb</p></li>
<li><p>1천만</p></li>
<li><p>인치</p></li>
<li><p>32</p></li>
<li><p>30</p></li>
<li><p>37</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>17</p></li>
<li><p>17</p></li>
<li><p>~</p></li>
<li><p>17</p></li>
<li><p>~</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>게시 메타 데이터에 연결 그룹 포함</p></td>
<td align="left"><p>연결 그룹 수</p></td>
<td align="left"><p></p>
<ul>
<li><p>1천만</p></li>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>150</p></li>
<li><p>300</p></li>
<li><p>400</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1천만</p></li>
<li><p>mb</p></li>
<li><p>mb</p></li>
<li><p>16</p></li>
<li><p>khz</p></li>
<li><p>km</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>인치</p></li>
<li><p>khz</p></li>
<li><p>인치</p></li>
<li><p>명</p></li>
<li><p>명</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>게시 메타 데이터에 액세스 그룹 포함</p></td>
<td align="left"><p>액세스 그룹 수</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>1천만</p></li>
<li><p>명</p></li>
<li><p>40</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1천만</p></li>
<li><p>43</p></li>
<li><p>153</p></li>
<li><p>535</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>kbps</p></li>
<li><p>fps</p></li>
<li><p>fps</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

관리 서버를 실행 하는 컴퓨터의 CPU 사용률이이를 대상으로 하는 게시 서버 수에 관계 없이 25%입니다. Microsoft SQL Server 데이터베이스 트랜잭션/초, 일괄 처리 요청/초 및 사용자 연결은 게시 서버 수에 관계 없이 동일 합니다. 예를 들어, 초당 거래 수는 ~ 30, 일괄 처리 요청 ~ 200, 사용자 연결 ~ 6이 있습니다.

관리 서버 & 게시 서버는 서로 느린 연결 네트워크를 사용 하는 지리적 분산 배포를 통해 &lt; 단일 관리 서버에 대 한 100 동시 요청에도 게시 서버의 라운드트립 응답 시간이 허용 되는 시간 제한 (5 초) 내에 있습니다.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">변형</th>
<th align="left">연결 그룹 수</th>
<th align="left">액세스 그룹 수</th>
<th align="left">게시 서버 수</th>
<th align="left">네트워크 연결 형식 게시 서버/관리 서버</th>
<th align="left">게시 서버에서 라운드트립 응답 시간 (초)</th>
<th align="left">관리 서버의 CPU 이용률</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>게시 서버와 관리 서버 간의 네트워크 연결</p></td>
<td align="left"><p>1.5 Mbps 느린 연결 네트워크</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1.5 mbps 케이블 DSL</p></li>
<li><p>1.5 mbps 케이블 DSL</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>4(tcp/ipv4)</p></li>
<li><p>5mb</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>게시 서버와 관리 서버 간의 네트워크 연결</p></td>
<td align="left"><p>LAN/WIFI 네트워크</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>raid-1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Wifi</p></li>
<li><p>Wifi</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>mb</p></li>
<li><p>명</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>~</p></li>
<li><p>17</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

관리 서버와 게시 서버가 느린 연결 네트워크 또는 고속 네트워크를 통해 연결 되어 있는지 여부에 관계 없이 관리 서버는 약 15000 패키지 새로 고침 요청을 30 분 내에 처리할 수 있습니다.

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> 앱-V 5.1 보고 서버 용량 계획 권장 사항


App-v 5.1 클라이언트 보고 데이터를 보고 서버로 보냅니다. 그러면 보고 서버는 Microsoft SQL Server 데이터베이스에 정보를 기록 하 고 App-v 5.1 클라이언트를 실행 하는 컴퓨터에 성공적으로 다시 알림을 보냅니다. 앱-V 5.1 보고 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.

**참고**  라운드트립 응답 시간은 reporting server에 보고 정보를 보내고 보고 서버에서 성공적으로 알림을 받기 위해 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 수행 되는 시간입니다.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">요약</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>여러 App-v 5.1 클라이언트는 보고 정보를 보고 서버에 동시에 보냅니다.</p></td>
<td align="left"><p></p>
<ul>
<li><p>보고 서버의 라운드트립 응답 시간은 500 클라이언트에 2.6 초입니다.</p></li>
<li><p>보고 서버의 라운드트립 응답 시간은 1000 클라이언트에 5.65 초입니다.</p></li>
<li><p>라운드 트립 응답 시간은 클라이언트 수에 따라 선형적으로 증가 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>보고 서버에서 처리 한 초당 요청 수입니다.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>단일 보고 서버와 단일 데이터베이스는 초당 최대 139 개의 요청을 처리할 수 있습니다. 평균은 121 요청/초입니다.</p></li>
<li><p>동일한 Microsoft SQL Server 데이터베이스에 보고 하는 두 개의 보고 서버를 사용 하는 경우 평균 요청/초는 단일 보고 서버 = ~ 127와 비슷하지만 최대 278 요청 수는 초입니다.</p></li>
<li><p>단일 보고 서버는 500 동시/활성 연결을 처리할 수 있습니다.</p></li>
<li><p>단일 보고 서버는 최대 1500 동시 연결을 처리할 수 있습니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>보고 데이터베이스.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Microsoft SQL Server를 실행 하는 컴퓨터의 잠금 경합은 초당 요청에 대 한 제한 요소입니다.</p></li>
<li><p>처리량 및 응답 시간은 데이터베이스 크기와 무관 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**임의 지연 계산**:

임의 지연은 보고 서버로 전송 되는 데이터의 최대 지연 시간 (분)을 지정 합니다. 예약 된 작업이 시작 되 면 클라이언트는 **0** 과 **ReportingRandomDelay** 사이의 임의 지연 시간을 생성 하 고 데이터를 보내기 전에 지정 된 기간 동안 대기 합니다.

임의 지연 = 4 \ * 클라이언트 수/초 당 평균 요청

예: 500 클라이언트의 경우 초당 120 요청이 있는 경우 임의 지연은 4 \ * 500/120 = ~ 17 분입니다.

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> 앱-V 5.1 게시 서버 용량 계획 권장 사항


App-v 5.1 클라이언트를 실행 하는 컴퓨터는 앱 V 5.1 게시 서버에 연결 하 여 게시 새로 고침 요청을 보내고 응답을 받습니다. 라운드 트립 응답 시간은 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 측정 됩니다. 프로세서 시간은 게시 서버에서 측정 됩니다. 앱-V 5.1 게시 서버 지원 구성에 대 한 자세한 내용은 [app-v 5.1 지원 되는 구성을](app-v-51-supported-configurations.md)참조 하세요.

**중요**  다음 목록에는 App-v 5.1 게시 서버를 설정할 때 고려해 야 하는 주요 요소가 표시 됩니다.

-   단일 게시 서버에 동시에 연결 하는 클라이언트 수입니다.

-   각 새로 고침의 패키지 수입니다.

-   클라이언트와 App-v 5.1 게시 서버 간의 환경에서 사용할 수 있는 네트워크 대역폭입니다.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">요약</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>여러 App-v 5.1 클라이언트는 단일 게시 서버에 동시에 연결 됩니다.</p></td>
<td align="left"><p></p>
<ul>
<li><p>듀얼 코어 프로세서를 실행 하는 게시 서버는 동시에 새로 고침을 요청 하는 최대 5000 클라이언트에 응답할 수 있습니다.</p></li>
<li><p>5000-10000 클라이언트의 경우 게시 서버에는 최소 쿼드 코어가 필요 합니다.</p></li>
<li><p>10000-20000 클라이언트의 경우 더 효율적인 응답 시간을 위해 게시 서버에 듀얼 쿼드 코어를 사용 해야 합니다.</p></li>
<li><p>쿼드 코어를 사용 하는 게시 서버는 3 초 내에 1만 패키지를 새로 고칠 수 있습니다. (1만 동시 클라이언트 지원)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>새로 고칠 때마다 패키지의 수입니다.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>패키지 수를 늘리면 응답 시간이 ~ 40% (최대 1000 패키지)로 증가 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 5.1 클라이언트와 게시 서버 간의 네트워크.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>느린 네트워크 (1.5 Mbps 대역폭)에서 LAN (최대 1000 명의 사용자)과 비교 하 여 응답 시간이 97% 증가 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**참고**  게시 서버 CPU 사용은 동시 요청 ( &gt; 대부분의 경우 90%)을 처리 해야 하는 시간 간격 동안 항상 높습니다. 게시 서버는 1 초에 ~ 1500 클라이언트 요청을 처리할 수 있습니다.

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">변형</th>
<th align="left">앱-V 5.1 클라이언트 수</th>
<th align="left">패키지 수</th>
<th align="left">게시 서버의 프로세서 구성</th>
<th align="left">네트워크 연결 형식 게시 서버/App-v 5.1 클라이언트</th>
<th align="left">App-v 5.1 클라이언트 (초)에 대 한 왕복 시간</th>
<th align="left">게시 서버의 CPU 사용률 (%)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 5.1 클라이언트에서 게시 새로 고침 요청이 &amp; 응답을 수신 하 고, 각 요청이 120 패키지를 포함 하 고 있습니다.</p></td>
<td align="left"><p>클라이언트 수</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>1000</p></li>
<li><p>5000</p></li>
<li><p>1만</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>듀얼 코어</p></li>
<li><p>듀얼 코어</p></li>
<li><p>쿼드 코어</p></li>
<li><p>쿼드 코어</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>raid-1</p></li>
<li><p>2</p></li>
<li><p>2</p></li>
<li><p>3-4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>99</p></li>
<li><p>89</p></li>
<li><p>77</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>각 새로 고침의 여러 패키지</p></td>
<td align="left"><p>패키지 수</p></td>
<td align="left"><p></p>
<ul>
<li><p>1000</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>쿼드 코어</p></li>
<li><p>쿼드 코어</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>2</p></li>
<li><p>3-4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>92</p></li>
<li><p>91</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>클라이언트와 게시 서버 간의 네트워크</p></td>
<td align="left"><p>1.5 Mbps 느린 연결 네트워크</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>쿼드 코어</p></li>
<li><p>쿼드 코어</p></li>
<li><p>쿼드 코어</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1.5 Mbps 내 대륙과 네트워크</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3-4</p></li>
<li><p>10 (0.2% 실패 율)</p></li>
<li><p>17 (1% 실패 율 사용)</p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> 앱-V 5.1 스트리밍 용량 계획 권장 사항


앱-V 5.1 클라이언트를 실행 하는 컴퓨터는 스트리밍 서버에서 가상 응용 프로그램 패키지를 스트리밍합니다. 라운드트립 응답 시간은 App-v 5.1 클라이언트를 실행 하는 컴퓨터에서 측정 되며 전체 패키지를 스트리밍하는 데 걸리는 시간입니다.

**중요**  다음 목록에서는 App-v 5.1 스트리밍 서버를 설정할 때 고려해 야 하는 주요 요인을 식별 합니다.

-   단일 스트리밍 서버에서 응용 프로그램 패키지를 동시에 스트리밍하는 클라이언트 수입니다.

-   스트리밍 중인 패키지의 크기입니다.

-   클라이언트와 스트리밍 서버 간의 환경에서 사용할 수 있는 네트워크 대역폭입니다.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">요약</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>여러 App-v 5.1 클라이언트는 단일 스트리밍 서버에서 동시에 응용 프로그램을 스트리밍합니다.</p></td>
<td align="left"><p></p>
<ul>
<li><p>동일한 서버에서 동시에 스트리밍하는 클라이언트 수가 늘어나면 패키지 다운로드/스트리밍 시간에 대 한 선형 관계가 있는 것입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>스트리밍 중인 패키지의 크기입니다.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>패키지 크기는 크기가 ~ 1GB 인 대용량 패키지에 대해서만 스트리밍/다운로드 시간에 영향을 줍니다. 3 MB에서 100 MB 까지의 패키지 크기에 대 한 스트리밍 시간은 20 초에서 100 초로, 100 동시 클라이언트를 포함 합니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>App-v 5.1 클라이언트와 스트리밍 서버 간의 네트워크.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>느린 네트워크 (1.5 Mbps 대역폭)에서 LAN (최대 100 명의 사용자)과 비교 하 여 응답 시간이 70-80% 증가 합니다.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

다음 표에는 이전 목록의 각 요소에 대 한 예제 값이 표시 되어 있습니다.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">변형</th>
<th align="left">앱-V 5.1 클라이언트 수</th>
<th align="left">각 패키지의 크기</th>
<th align="left">네트워크 연결 형식 스트리밍 서버/App-v 5.1 클라이언트</th>
<th align="left">App-v 5.1 클라이언트 (초)에 대 한 왕복 시간</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>여러 앱-V 5.1 클라이언트는 스트리밍 서버에서 가상 응용 프로그램 패키지를 스트리밍 합니다.</p></td>
<td align="left"><p>클라이언트 수입니다.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3.5MB</p></li>
<li><p>3.5MB</p></li>
<li><p>3.5MB</p></li>
<li><p></p></li>
<li><p>5mb</p></li>
<li><p>5mb</p></li>
<li><p>5mb</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>개가</p></li>
<li><p>39</p></li>
<li><p>391</p></li>
<li><p></p></li>
<li><p>35</p></li>
<li><p>68</p></li>
<li><p>461</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>스트리밍된 각 패키지의 크기입니다.</p></td>
<td align="left"><p>각 패키지의 크기입니다.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>21MB</p></li>
<li><p>21MB</p></li>
<li><p></p></li>
<li><p>109</p></li>
<li><p>109</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<p>33</p>
<p>83</p>
<p></p>
<p>100</p>
<p>160</p></td>
</tr>
<tr class="odd">
<td align="left"><p>클라이언트와 App-v 5.1 스트리밍 서버 간의 네트워크 연결.</p></td>
<td align="left"><p>1.5 Mbps 느린 연결 네트워크.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p></p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3.5MB</p></li>
<li><p></p></li>
<li><p>5mb</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1.5 Mbps 내 대륙과 네트워크</p></li>
</ul></td>
<td align="left"><p></p>
<p>102</p>
<p></p>
<p>121</p></td>
</tr>
</tbody>
</table>

 

각 App-v 5.1 스트리밍 서버는 가상화 된 응용 프로그램을 동시에 스트리밍하는 최소 200 클라이언트를 처리할 수 있어야 합니다.

**참고**  실제로 스트림 하는 데 걸리는 실제 시간은 동시 스트리밍 클라이언트 수, 패키지 수, 패키지 크기, 서버의 네트워크 활동 및 네트워크 상태에 따라 결정 됩니다.

 

예를 들어, 100 동시 클라이언트가 서버에서 스트리밍하는 경우 평균 사용자는 2 분 이내에 100 MB 패키지를 스트리밍할 수 있습니다. 그러나 크기가 1 GB 인 패키지는 최대 30 분까지 걸릴 수 있습니다. 대부분의 실제 환경에서는 스트리밍 요구가 일관 되 게 분산 되지 않으며, 필요한 스트리밍 서버 수의 크기를 적절히 조정 하기 위해 해당 환경에 존재 하는 대략적인 최대 스트리밍 요구 사항을 이해 하는 것이 필요 합니다.

스트리밍 서버가 지원할 수 있는 클라이언트 수가 현저 하 게 늘어나고, 응용 프로그램을 미리 캐시 하는 경우 최대 스트리밍 요구 사항이 줄어들 수 있습니다. 또한 요청에 따라 스트리밍 서버에서 지원 되는 클라이언트 수를 늘리면 최적화 된 패키지를 스트리밍할 수 있습니다.

## 앱-V 5.1 서버 역할 결합


확장 및 내결함성 요구 사항을 Discounting Active Directory에 연결 된 위치에 필요한 최소 서버 수가 하나입니다. 이 서버는 관리 서버, 관리 서버 서비스 및 Microsoft SQL Server 역할을 호스팅합니다. 따라서 서버 역할은 서로 충돌 하지 않으므로 원하는 조합으로 정렬할 수 있습니다.

크기 조정 요구 사항을 무시 하 여 오류 허용 구현을 제공 하는 데 필요한 최소 서버 수는 4 개입니다. 관리 서버 및 Microsoft SQL Server 역할은 내결함성이 있는 구성에서 지원 됩니다. 관리 서버 서비스를 역할 중 하 나와 결합할 수 있지만, 단일 오류 지점이 남아 있습니다.

내결함성이 많은 전략과 기술이 제공 되는 것은 아니지만, 제공 되는 서비스에는 적용 되지 않습니다. 또한 App-v 5.1 역할이 결합 된 경우 비 호환성으로 인해 특정 내결함성 옵션이 더 이상 적용 되지 않을 수 있습니다.






## 관련 항목


[App-V 5.1 지원되는 구성](app-v-51-supported-configurations.md)

[App-V 5.1을 사용한 고가용성 계획](planning-for-high-availability-with-app-v-51.md)

[App-V 배포 계획](planning-to-deploy-app-v51.md)

 

 





