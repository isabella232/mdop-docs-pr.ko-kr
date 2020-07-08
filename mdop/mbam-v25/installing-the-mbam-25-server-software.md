---
title: MBAM 2.5 서버 소프트웨어 설치
description: MBAM 2.5 서버 소프트웨어 설치
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823393"
---
# MBAM 2.5 서버 소프트웨어 설치


이 항목에서는 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하거나 명령줄 매개 변수를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.5 서버 소프트웨어를 설치 하는 방법에 대해 설명 합니다. MBAM 2.5 서버 기능을 구성 하는 각 서버에 대해 서버 설치 프로세스를 반복 합니다. 설치를 완료 한 후 서버 기능 구성 단계에 대해 [MBAM 2.5 서버 기능 구성을](configuring-the-mbam-25-server-features.md) 참조 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시작하기 전에</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM 2.5 계획 정보 검토</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">독립 실행형 및 Configuration Manager 통합 토폴로지용 MBAM 2.5 서버 필수 구성 요소</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 지원되는 구성</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">MBAM 2.5의 개략적인 아키텍처</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>로그 파일을 가져오는 방법 읽기</p></td>
<td align="left"><p>기본적으로 로그 파일은 로컬 컴퓨터 의% temp% 폴더에 만들어집니다. % Temp% 폴더가 아닌 특정 위치에 로그 파일을 쓰려면 <strong> </strong> <strong> /log </strong> &lt; <em> location 인수를 사용 </em> &gt; 합니다.</p>
<p>다른 이벤트가 <strong> mbam-설정 </strong> 또는 <strong> mbam- </strong> <strong> 응용 프로그램 및 서비스의 웹 노드에서 &gt; Microsoft Windows를 기록 &gt; </strong> 하는 이벤트 뷰어에 기록 될 수 있습니다. 예를 들어, MBAM을 제거 하면 제거 관리자가 EventViewer에서 MBAM-설정 및 MBAM 웹 로그를 제거 하기도 합니다.</p></td>
</tr>
</tbody>
</table>

 

## Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하 여 MBAM 2.5 서버 소프트웨어 설치


다음 단계를 사용 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 사용 하 여 MBAM 서버 소프트웨어를 설치 합니다.

**마법사를 사용 하 여 MBAM 2.5 서버 소프트웨어를 설치 하려면**

1.  MBAM을 설치 하려는 서버에서 **MBAMserversetup.exe** 를 실행 하 여 Microsoft BitLocker 관리 및 모니터링 설정 마법사를 시작 합니다.

2.  **시작** 페이지에서 **다음**을 클릭 합니다.

3.  Microsoft 소프트웨어 사용권 계약을 읽고 동의한 후 **다음** 을 클릭 하 여 설치를 계속 합니다.

4.  업데이트를 확인할 때 Microsoft 업데이트 사용 여부를 선택 하 고 **다음**을 클릭 합니다.

5.  사용자 환경 개선 프로그램 참여 여부를 선택 하 고 **다음**을 클릭 합니다.

6.  설치를 시작 하려면 **설치**를 클릭 합니다.

7.  MBAM 서버 소프트웨어 설치가 완료 된 후 서버 기능을 구성 하려면 **마법사를 닫은 후에 Mbam 서버 구성 실행** 확인란을 선택 합니다. 또는 서버 설치가 **시작** 메뉴에 생성 하는 **Mbam 서버 구성** 바로 가기를 사용 하 여 나중에 mbam을 구성할 수 있습니다.

8.  **마침**을 클릭합니다.

## 명령 프롬프트 창을 사용 하 여 MBAM 2.5 서버 소프트웨어 설치


명령 프롬프트에서 다음 명령과 비슷한 명령을 입력 하 여 MBAM 서버 소프트웨어를 설치 합니다.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

다음 표에서는 MBAM 2.5 서버 소프트웨어를 설치 하기 위한 명령줄 매개 변수를 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">매개 변수</th>
<th align="left">매개 변수 값</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>True False</p></td>
<td align="left"><p>True-향상 시킬 MBAM 기능을 확인 하는 데 도움이 되는 사용자 개선 경험 프로그램에 참여 합니다.</p>
<p>False-고객 개선 사항 프로그램에 참여 하지 마세요.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>True False</p></td>
<td align="left"><p>True-Microsoft Update를 사용 하 여 컴퓨터를 안전 하 게 보호 하 고 Windows 및 다른 Microsoft 제품 (MBAM 포함)을 최신 상태로 유지 합니다.</p>
<p>False-Microsoft 업데이트 사용 안 함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;경로&gt;</p></td>
<td align="left"><p>MBAM을 설치 하려는 위치입니다.</p>
<p>예:</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>True False</p></td>
<td align="left"><p>True-제거 되지 않은 기능이 있어도 MBAM을 제거 하는 프로세스를 계속 합니다.</p>
<p>False (기본값) 제거 사용자 지정 작업이 추가 된 MBAM 서버 기능을 제거 하지 못하면 제거에 실패 하 고 MBAM은 설치 된 상태로 유지 됩니다.</p>
<p>두 경우 모두 MBAM을 제거 하는 동안 성공적으로 제거한 기능은 제거 됩니다.</p></td>
</tr>
</tbody>
</table>

 



## 관련 항목


[MBAM 2.5 배포](deploying-mbam-25.md)

[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





