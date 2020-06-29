---
title: AGPM 기술 개요
description: AGPM 기술 개요
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818298"
---
# AGPM 기술 개요


Microsoft AGPM (고급 그룹 정책 관리)는 클라이언트/서버 응용 프로그램입니다. AGPM 서버는 AGPM이 서버의 파일 시스템에서 만든 보관 저장소에 오프 라인으로 Gpo (그룹 정책 개체)를 저장 합니다. 그룹 정책 관리자는 GPMC (그룹 정책 관리 콘솔) 용 AGPM 스냅인을 사용 하 여 보관 파일을 호스팅하는 서버의 Gpo와 함께 작업 합니다. AGPM 및 관련 항목의 부분, 파일 시스템에 Gpo를 저장 하는 방법, 사용 권한이 각 사용자 역할에서 사용할 수 있는 작업을 제어 하는 방법에 대 한 이해는 AGPM에서 그룹 정책 관리자의 효율성을 향상 시킬 수 있습니다.

## 용어


다음은 기본 AGPM 약관에 대해 설명 합니다.

-   **AGPM 클라이언트:** GPMC (그룹 정책 관리 콘솔) 용 AGPM 스냅인을 실행 하 고 그룹 정책 관리자가 Gpo를 관리 하는 컴퓨터입니다.

-   **AGPM 스냅인:** 사용자가 Gpo를 관리할 수 있도록 AGPM 클라이언트에 설치 되어 있는 AGPM의 소프트웨어 구성 요소입니다.

-   **AGPM 서버:** AGPM 서비스를 실행 하 고 보관 파일을 관리 하는 서버입니다. 각 AGPM 서버는 하나의 보관 파일만 관리할 수 있지만 하나의 AGPM 서버에서 하나의 보관 파일에 있는 여러 도메인에 대 한 보관 데이터를 관리할 수 있습니다. AGPM 서버 이외의 컴퓨터에서 보관 파일을 호스트할 수 있습니다.

-   **AGPM 서비스:** AGPM 서버에서 서비스로 실행 되는 AGPM의 소프트웨어 구성 요소입니다. 서비스는 해당 포리스트의 저장소와 프로덕션 환경에서 Gpo를 관리 합니다.

-   **보관:** AGPM에서 관련 AGPM 서버에서 관리 하는 제어 된 Gpo와 해당 Gpo 각각에 대 한 기록을 포함 하는 중앙 저장소입니다. 여기에는 각 GPO의 모든 이전 제어 버전이 포함 됩니다. 아카이브는 여러 도메인의 Gpo에 대 한 데이터를 포함할 수 있는 보관 인덱스 파일 및 관련 보관 데이터로 구성 됩니다. AGPM 서버 이외의 컴퓨터에서 보관 파일을 호스트할 수 있습니다.

-   **제어 GPO:** AGPM에서 관리 하는 GPO입니다. AGPM은 보관 저장소에 저장 되어 있는 제어 된 Gpo의 기록 및 사용 권한을 관리 합니다.

-   **미제어 GPO:** 도메인에 대 한 프로덕션 환경의 GPO로, AGPM에서 관리 되지 않습니다.

## AGPM 설치, 생성 및 영향


Agpm 서버에서 AGPM 설치 프로그램이 AGPM 서비스를 설치 합니다. AGPM은 Active Directory® 디렉터리 서비스 또는 스키마를 변경 하지 않습니다. 기본적으로 AGPM 서버 프로그램 파일 은%ProgramFiles%\\Microsoft\\AGPM\\Server.에 설치 됩니다. 필요 하면 도메인 컨트롤러에 AGPM 서비스를 설치할 수 있습니다. 그러나, 구성원 서버에 AGPM 서비스를 설치 하는 것이 좋습니다.

Agpm 클라이언트에서 AGPM 설치 프로그램은 AGPM 스냅인을 설치 하 고 GPMC에 표시 되는 각 도메인에 **변경 제어** 폴더를 추가 합니다. 기본적으로 AGPM 클라이언트 프로그램 파일 은%ProgramFiles%\\Microsoft\\AGPM\\Client.에 설치 됩니다.

표 1에서는 AGPM에서 설치 하거나 만드는 항목 및 AGPM 작업에 영향을 주는 운영 체제 부분에 대해 설명 합니다.

**표 1: AGPM에서 설치, 생성 또는 영향을 받는 항목**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">항목</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AGPM 서비스</p></td>
<td align="left"><p>AGPM 서비스는 AGPM 서버에서 실행 됩니다. 서비스는 프로덕션 환경에서 오프 라인 Gpo와 제어 된 Gpo가 포함 된 보관 파일을 관리 합니다. AGPM 서비스의 기본 구성은 다음과 같습니다.</p>
<ul>
<li><p><strong>서비스 이름: </strong> AGPM 서비스</p></li>
<li><p><strong>표시 이름: </strong> AGPM 서비스</p></li>
<li><p><strong>실행 파일 경로: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</p></li>
<li><p><strong>시작: </strong> 자동</p></li>
<li><p><strong>다음 계정으로 로그온: </strong> <strong> 제어판에서 프로그램 및 기능을 사용 하 여 변경할 수 있는 agpm 서버를 설치 하는 동안 지정 된 Agpm 서비스 계정 </strong> <strong> </strong> 입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>AGPM 보관</p></td>
<td align="left"><p>기본적으로 AGPM은 AGPM 서버 에서%ProgramData%\Microsoft\AGPM에 아카이브를 만듭니다. 보관 파일은 오프 라인 Gpo에 대 한 저장소를 제공 하며 각 GPO의 여러 버전을 저장할 수 있습니다. AGPM 관리자 또는 승인자가 GPO를 프로덕션 환경에 배포 하 고 GPO를 OU (조직 구성 단위)에 연결 하는 경우에만이 아카이브에 있는 Gpo에 대 한 변경 내용이 프로덕션 환경에 영향을 주지 않습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 방화벽</p></td>
<td align="left"><p>설치 중에 AGPM은 AGPM 클라이언트가 AGPM 서버와 통신할 수 있도록 허용 하는 인바운드 Windows 방화벽 규칙을 사용 하도록 설정 합니다. 기본 Windows 방화벽 규칙은 다음과 같습니다.</p>
<ul>
<li><p><strong>Name: </strong> AGPM 서비스</p></li>
<li><p><strong>작업: </strong> 연결을 허용 합니다.</p></li>
<li><p><strong>프로그램: </strong> 지정 된 조건을 충족 하는 모든 프로그램</p></li>
<li><p><strong>프로토콜 종류: </strong> TCP</p></li>
<li><p><strong>로컬 포트: </strong> 4600</p></li>
<li><p><strong>원격 포트: </strong> 모든 포트</p></li>
<li><p><strong>로컬 IP 주소: </strong> 모두</p></li>
<li><p><strong>원격 IP 주소: </strong> 모두</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>전자 메일 서버</p></td>
<td align="left"><p>AGPM은 SMTP (Simple Mail Transfer Protocol)를 사용 하 여 도메인 위임 탭에서 구성한 주소로 전자 메일 요청을 보냅니다 <strong> </strong> . 예를 들어 편집기에서 새 GPO를 만들도록 요청할 때 AGPM은 도메인 위임 탭에 지정 된 각 전자 메일 주소를 알려 줍니다 <strong> </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AGPM 스냅인</p></td>
<td align="left"><p>GPMC의 AGPM 스냅인은 AGPM 클라이언트에서 실행 되며 그룹 정책 관리자가 Gpo를 관리 하는 데 사용 됩니다. 이 스냅인은 <strong> 각 도메인의 변경 제어 폴더로 GPMC에 표시 됩니다 </strong> .</p></td>
</tr>
</tbody>
</table>

 

### 추가 참조

AGPM에서 설치 하는 파일에 대 한 자세한 내용은 [Agpm 계획 가이드](https://go.microsoft.com/fwlink/?LinkId=160060)를 참조 하세요.

## Archive


기본적으로 AGPM 서버 설치 프로세스 는%ProgramData%\\Microsoft\\AGPM.에서 AGPM 서버의 로컬 하드 디스크에 아카이브를 만듭니다. 그러나 설치 하는 동안 경로를 변경 하거나 AGPM 서버 이외의 서버에서 보관 파일을 만들 수도 있습니다.

보관 파일에는 보관 파일에 포함 된 각 GPO의 각 버전에 대 한 하위 폴더가 포함 됩니다. 각 하위 폴더의 이름은 GPO의 버전을 식별 하는 GUID입니다.

gpostate.xml 파일은 아카이브에 있는 각 GPO의 상태를 기록 합니다. 파일은 아카이브의 콘텐츠를 설명 하는 매니페스트입니다. 예를 들어 GPO에는 여러 버전이 있을 수 있으며, 각 버전은 보관 저장소의 고유한 하위 폴더에 있습니다. gpostate.xml 파일은 서로 다른 버전의 단일 GPO를 포함 하는 하위 폴더를 나타냅니다. 또한 GPO 템플릿은 보관 파일에 하위 폴더를 포함 하지만, gpostate.xml는 해당 Gpo를 제어할 수 없습니다. 마찬가지로, 그룹 정책 관리자가 Gpo를 삭제 하면 AGPM이 해당 사용자의 상태를 gpostate.xml에서 변경 하 여 **휴지통** 에 있는 것을 나타내지만 실제로는 보관 함의 하위 폴더를 제거 하지 않습니다.

**주의**  사항 보관 파일에 포함 된 gpostate.xml 또는 Gpo를 수동으로 편집 하지 마세요. 이 정보는 AGPM 보관에 대 한 이해를 향상 시키기 위해 제공 됩니다. 대신 AGPM 스냅인을 사용 하 여 Gpo를 변경 합니다.

 

AGPM에서 보관 파일을 만들면 시스템, 관리자 및 agpm 서비스 계정 (AGPM 서버의 설정에 지정)에 모든 권한이 부여 됩니다. Agpm 스냅인에서 AGPM 사용자 인터페이스를 사용 하 여 사용 권한을 변경 해도 로그온 한 사용자를 대신 하 여 AGPM 서비스 계정이 모든 작업을 수행 하기 때문에 보관에 대 한 사용 권한은 변경 되지 않습니다.

### 추가 참조

보관 파일을 백업 하는 방법, 백업에서 보관 파일을 복원 하거나 AGPM 서버와 보관 파일을 모두 이동 하는 방법에 대 한 자세한 내용은 [agpm의 운영 가이드](https://go.microsoft.com/fwlink/?LinkId=160061)에 있는 "Agpm 관리자 작업 수행" 섹션을 참조 하세요.

## 역할 및 권한


역할은 위임을 간소화 합니다. AGPM 관리자는 그룹 정책 관리자에 대 한 자세한 사용 권한을 할당 하는 대신 그룹 정책 관리자에 게 다음 네 가지 역할 중 하나를 할당 하 여 해당 역할과 관련 된 작업을 수행할 수 있도록 합니다.

-   **AGPM 관리자:** AGPM 관리자 (모든 권한) 역할이 할당 한 그룹 정책 관리자는 AGPM에서 모든 작업을 수행할 수 있습니다. AGPM 관리자는 도메인 전체 옵션을 구성 하 고 다른 그룹 정책 관리자에 게 권한을 위임할 수 있습니다.

-   **승인자:** 승인자 역할에 할당 된 그룹 정책 관리자는 도메인의 프로덕션 환경에 Gpo를 배포할 수 있습니다. 또한 승인자는 Gpo를 만들고 삭제 하며 편집자의 요청을 승인 하거나 거부할 수 있습니다. 승인자는 도메인의 Gpo 목록을 보고 gpo의 정책 설정을 보고 GPO의 정책 설정에 대 한 보고서를 만들고 볼 수 있습니다. 편집자 역할을 할당 하지 않는 한 Gpo의 정책 설정은 편집할 수 없습니다.

-   **편집자:** 편집자 역할이 할당 한 그룹 정책 관리자는 도메인의 Gpo 목록을 보고, gpo의 정책 설정을 보고, gpo의 정책 설정을 편집 하 고, GPO의 정책 설정에 대 한 보고서를 만들고 볼 수 있습니다. 승인자 역할을 할당 하지 않는 한, 편집자는 Gpo를 만들거나 배포 하거나 삭제할 수 없습니다. 그러나 Gpo를 만들거나 배포 하거나 삭제 하도록 요청할 수 있습니다.

-   **검토자:** 검토자 역할이 지정 된 그룹 정책 관리자는 도메인의 Gpo 목록을 보고 GPO의 정책 설정에 대 한 보고서를 만들고 볼 수 있습니다. 편집기 역할에 할당 된 경우에만 GPO에서 정책 설정을 편집할 수 있습니다.

Agpm 관리자가 agpm 스냅인을 사용 하 여 역할 보다 더 세부적인 수준에서 권한을 구성할 수 있는 유연성을 제공 합니다. 표 2에서는 이러한 사용 권한에 대해 설명 하 고 기본적으로 각 역할에 부여 된 사용 권한을 나타냅니다.

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
<th align="left">권한</th>
<th align="left">설명</th>
<th align="left">AGPM 관리자</th>
<th align="left">승인자</th>
<th align="left">편집기</th>
<th align="left">구분</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>모든 권한</strong></p></td>
<td align="left"><p>모든 권한이 있어야 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO 만들기</strong></p></td>
<td align="left"><p>도메인에서 Gpo를 만듭니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>콘텐츠 나열</strong></p></td>
<td align="left"><p>도메인의 Gpo를 나열 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>설정 읽기</strong></p></td>
<td align="left"><p>GPO 내의 정책 설정을 읽습니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>설정 편집</strong></p></td>
<td align="left"><p>GPO의 정책 설정을 변경 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO 삭제</strong></p></td>
<td align="left"><p>GPO를 삭제 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>보안 수정</strong></p></td>
<td align="left"><p>도메인 수준 액세스를 위임 하 고, 단일 GPO에 대 한 액세스 권한을 위임 하 고, 프로덕션 환경에 대 한 액세스를 위임할 수 있습니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO 배포</strong></p></td>
<td align="left"><p>보관 저장소에서 프로덕션 환경으로 GPO를 배포 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>서식 파일 만들기</strong></p></td>
<td align="left"><p>AGPM에서 GPO 서식 파일을 만듭니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>옵션 수정</strong></p></td>
<td align="left"><p>AGPM 전자 메일 알림을 구성 하 고 보관 저장소에 저장 된 GPO 버전을 제한 합니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>GPO 내보내기</strong></p></td>
<td align="left"><p>GPO를 파일로 내보냅니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>GPO 가져오기</strong></p></td>
<td align="left"><p>파일에서 GPO를 가져옵니다.</p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
<td align="left"><p>예</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**참고** 
 AGPM 3.0 또는 2.5에서는 **Gpo 내보내기** 및 **gpo 가져오기** 권한을 사용할 수 없습니다.

도메인에 대 한 프로덕션 환경에서 Gpo에 대 한 액세스를 위임 하는 기능과 저장 된 GPO 버전의 수를 제한 하는 기능은 AGPM 2.5에서 사용할 수 없습니다.

 

### 추가 참조

특정 역할을 할당 하거나 특정 작업을 수행 하는 데 필요한 권한에 대해 그룹 정책 관리자가 수행할 수 있는 작업에 대 한 자세한 내용은 [AGPM의 운영 가이드](https://go.microsoft.com/fwlink/?LinkId=160061)를 참조 하세요.

 

 





