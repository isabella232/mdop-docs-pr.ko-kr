---
title: 위임을 위해 신뢰할 수 있는 서버를 구성하는 방법
description: 위임을 위해 신뢰할 수 있는 서버를 구성하는 방법
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817748"
---
# 위임을 위해 신뢰할 수 있는 서버를 구성하는 방법


Microsoft App-v (Application Virtualization) 관리 서버 소프트웨어를 설치할 때 분산 시스템 아키텍처를 사용 하 여 설치 하도록 선택할 수 있습니다. 콘솔, 관리 웹 서비스 및 데이터베이스를 다른 컴퓨터에 설치 하는 경우 위임용으로 신뢰할 수 있도록 IIS (인터넷 정보 서비스) 서버를 구성 해야 합니다. 이는 관리 웹 서비스가 콘솔을 사용 하는 App-v 관리자의 자격 증명을 사용 하 여 App-v 데이터 저장소에 연결 하려고 시도 하기 때문에 필요 합니다. IIS 서버를 위임용으로 신뢰 하도록 구성 하지 않은 경우 데이터 저장소가 설치 된 데이터베이스 서버에서 IIS 서버의 관리자 자격 증명을 받아들이지 않으므로 관리 웹 서비스에서 App-v 데이터 저장소에 연결할 수 없습니다.

**참고**  단일 서버에 App-v 관리 서버 소프트웨어를 설치 하 고 별도의 서버에 데이터 저장소를 배치 하는 경우 관리 웹 서비스 및 관리 콘솔이 동일한 서버에 있더라도 위임에 대해 신뢰할 수 있는 상태로 서버를 구성 해야 하는 경우가 있습니다. 이러한 상황은 **대체 자격 증명 사용** 옵션을 사용 하 여 콘솔의 관리 웹 서비스에 연결 해야 하는 경우에 발생 합니다.

 

사용할 수 있는 위임 유형은 Active Directory 도메인 서비스 (ADDS) 인프라에서 구성한 도메인 기능 수준에 따라 달라 집니다. 다음 표에는 App-v의 각 도메인 기능 수준에 대해 구성할 수 있는 위임 유형이 나와 있습니다. 자세한 지침은 표를 따르세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">도메인 기능 수준</th>
<th align="left">사용 가능한 위임 수준</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000 네이티브</p></td>
<td align="left"><ul>
<li><p>대리인 없음 (기본값)</p></li>
<li><p>무제한 위임</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2003, Windows Server 2008 또는 Windows Server 2008 R2</p></td>
<td align="left"><ul>
<li><p>대리인 없음 (기본값)</p></li>
<li><p>무제한 위임 ¹</p></li>
<li><p>제한 된 위임 (Kerberos 전용 프로토콜 사용)</p></li>
<li><p>제한 된 위임 (모든 인증 프로토콜 사용) ¹</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

¹ 권장 하지 않음.

## 도메인 기능 수준이 Windows 2000 네이티브 인 경우 무제한 위임을 구성 하려면


웹 서버의 도메인 컨트롤러에서 다음 단계를 완료 합니다.

****

1.  **시작**, **관리 도구**를 차례로 클릭 한 다음 **Active Directory 사용자 및 컴퓨터**를 클릭 합니다.

2.  도메인을 확장 한 다음 컴퓨터 폴더를 확장 합니다.

3.  오른쪽 창에서 웹 서버의 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 한 다음 **속성**을 클릭 합니다.

4.  **일반** 탭에서 **위임용으로 컴퓨터 트러스트** 확인란이 선택 되어 있는지 확인 합니다.

5.  **확인**을 클릭합니다.

## 도메인 기능 수준이 Windows Server 2003, Windows Server 2008 또는 Windows Server 2008 R2 인 경우 무제한 위임을 구성 하려면


웹 서버의 도메인 컨트롤러에서 다음 단계를 완료 합니다.

****

1.  **시작**을 클릭 하 고 **관리 도구**를 클릭 한 다음 **Active Directory 사용자 및 컴퓨터**를 클릭 합니다.

2.  도메인을 확장 하 고 컴퓨터 폴더를 확장 합니다.

3.  오른쪽 창에서 웹 서버의 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **위임** 탭을 클릭 합니다.

4.  **모든 서비스에 대 한 위임용으로이 컴퓨터 신뢰 (Kerberos만)** 를 클릭 하 여 선택 합니다.

5.  **확인**을 클릭합니다.

## 도메인 기능 수준이 Windows Server 2003, Windows Server 2008 또는 Windows Server 2008 R2 인 경우 제한 위임을 구성 하려면


웹 서버의 도메인 컨트롤러에서 다음 단계를 완료 합니다.

****

1.  **시작**을 클릭 하 고 **관리 도구**를 클릭 한 다음 **Active Directory 사용자 및 컴퓨터**를 클릭 합니다.

2.  도메인을 확장 한 다음 컴퓨터 폴더를 확장 합니다.

3.  오른쪽 창에서 웹 서버의 컴퓨터 이름을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 선택한 다음 **위임** 탭을 클릭 합니다.

4.  **지정 된 서비스에 대 한 위임용 으로만이 컴퓨터 신뢰**를 클릭 하 여 선택 합니다.

5.  **Kerberos만 사용** 이 선택 되어 있는지 확인 한 다음 **확인**을 클릭 합니다.

6.  **추가** 단추를 클릭합니다. **서비스 추가** 대화 상자에서 **사용자 또는 컴퓨터**를 클릭 한 다음 앱-V 데이터 저장소가 있는 Microsoft SQL server의 이름을 찾아보거나 입력 하 고 IIS에서 사용자 자격 증명을 받습니다. **확인**을 클릭합니다.

7.  **사용 가능한 서비스** 목록에서 Microsoft SQL Server가 app-v 데이터베이스에 대 한 연결을 허용 하는 포트 번호를 나열 하는 MSSQLSvc 서비스 (기본 포트는 1433)를 선택 합니다. **확인**을 클릭합니다.

### 제한 된 위임을 위해 IIS 7을 구성 하는 추가 단계

IIS 7 서버에서 관리 웹 서비스를 실행 하는 경우에는 다음 단계를 완료 하 여 IIS 7 *Useapppoolcredentials* 변수를 True로 설정 해야 합니다.

1.  관리자 권한 명령 프롬프트 창을 엽니다. 관리자 권한 명령 프롬프트 창을 열려면 **시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **보조 프로그램**을 클릭 하 고 **명령 프롬프트**를 마우스 오른쪽 단추로 클릭 한 다음 **관리자 권한으로 실행**을 클릭 합니다.

2.  %Windir%\\system32\\inetsrv.로 이동

3.  **appcmd.exe 설정 구성 섹션: system.webserver/security/authentication/windowsAuthentication-useAppPoolCredentials: true**를 입력 한 다음 enter 키를 누릅니다.

 

 





