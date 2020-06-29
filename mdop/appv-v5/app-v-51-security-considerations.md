---
title: App-V 5.1 보안 고려 사항
description: App-V 5.1 보안 고려 사항
author: dansimp
ms.assetid: 6bc6c1fc-f813-47d4-b763-06fd4faf6a72
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a5606b3e0ba5e6fb8c62f14e2ed8d93ea2cf134
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814764"
---
# App-V 5.1 보안 고려 사항


이 항목에서는 계정 및 그룹, 로그 파일, Microsoft Application Virtualization (App-v) 5.1에 대 한 기타 보안 관련 고려 사항에 대 한 간략 한 개요를 다룹니다.

**중요**  
App-v 5.1는 보안 제품이 아니므로 보안 환경에 대 한 보증을 제공 하지 않습니다.



## PackageStoreAccessControl (PSAC) 기능은 더 이상 사용 되지 않습니다.


유효 6 월, 2014, Microsoft Application Virtualization (App-v) 5.0 서비스 팩 2(SP2)에 도입 된 PackageStoreAccessControl (PSAC) 기능은 단일 사용자 및 다중 사용자 환경에서 더 이상 사용 되지 않습니다.

## 일반 보안 고려 사항


**보안 위험을 파악 합니다.** App-v 5.1의 가장 심각한 위험은 앱 V 5.1 클라이언트에서 키 데이터를 다시 구성할 수 있는 권한이 없는 사용자가 해당 기능을 도용 했을 수 있다는 것입니다. 서비스 거부 공격으로 인해 짧은 기간 동안 App-v 5.1 기능이 손실 되는 것은 일반적으로 치명적이 지 않습니다.

**컴퓨터를 물리적으로 보호**합니다. 보안이 완전 하지 않음 (물리적 보안 없음). App-v 5.1 서버에 대 한 실제 액세스 권한이 있는 사람은 누구나 전체 클라이언트 기반을 공격할 수 있습니다. 모든 잠재 물리적 공격은 높은 위험 수준으로 간주 되 고 적절 하 게 완화 되어야 합니다. App-v 5.1 서버는 제어 된 액세스 권한이 있는 물리적으로 안전한 서버 방에 저장 되어야 합니다. 운영 체제에서 컴퓨터를 잠그거나 보안 된 화면 보호기를 사용 하 여 관리자가 실제로 제공 되지 않는 경우 이러한 컴퓨터를 보호 하세요.

**모든 컴퓨터에 최신 보안 업데이트를 적용**합니다. 운영 체제, Microsoft SQL Server 및 App-v 5.1 최신 업데이트에 대 한 정보를 확인 하려면 보안 알림 서비스 ()를 구독 합니다 <https://go.microsoft.com/fwlink/p/?LinkId=28819> .

**강력한 암호 또는 암호 문구를 사용**합니다. 모든 App-v 5.1 및 App-v 5.1 administrator 계정에는 항상 15 개 이상의 문자로 강력한 암호를 사용 합니다. 빈 암호를 사용 하지 마세요. 암호 개념에 대 한 자세한 내용은 TechNet ()의 "계정 암호 및 정책" 백서를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=30009> .

## 앱-V 5.1의 계정 및 그룹


사용자 계정 관리에 대 한 모범 사례는 도메인 글로벌 그룹을 만들고 사용자 계정을 추가 하는 것입니다. 그런 다음 App-v 5.1 서버의 필수 App-v 5.1 로컬 그룹에 도메인 글로벌 계정을 추가 합니다.

**참고**  
게시 서버에 연결 해야 하는 app-v 클라이언트 컴퓨터 계정은 게시 서버의 **사용자** 로컬 그룹의 일부 여야 합니다. 기본적으로 도메인의 모든 컴퓨터는 **사용자** 로컬 그룹의 일부인 **승인 된 사용자** 그룹의 일부입니다.



### <a href="" id="-------------app-v-5-1-server-security"></a> 앱-V 5.1 서버 보안

App-v 5.1를 설정 하는 동안 그룹이 자동으로 생성 되지 않습니다. App-v 5.1 서버 작업을 관리 하려면 다음 Active Directory 도메인 서비스 글로벌 그룹을 만들어야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">그룹 이름</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 관리 관리자 그룹</p></td>
<td align="left"><p>App-v 5.1 관리 서버를 관리 하는 데 사용 됩니다. 이 그룹은 App-v 5.1 관리 서버 설치 중에 만들어집니다.</p>
<div class="alert">
<strong>중요</strong><br/><p>설치를 완료 한 후 관리 콘솔을 사용 하 여 그룹을 만들 수 있는 방법은 없습니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>관리 서비스 계정에 대 한 데이터베이스 읽기/쓰기</p></td>
<td align="left"><p>관리 데이터베이스에 대 한 읽기/쓰기 액세스를 제공 합니다. 이 계정은 App-v 5.1 관리 데이터베이스 설치 중에 만들어야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>앱-V 관리 서비스 관리자 계정 설치</p>
<div class="alert">
<strong>참고</strong><br/><p>이는 관리 데이터베이스가 서비스와 별도로 설치 되는 경우에만 필요 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>관리 데이터베이스의 스키마 버전 테이블에 대 한 공용 액세스를 제공 합니다. 이 계정은 App-v 5.1 관리 데이터베이스 설치 중에 만들어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>앱-V Reporting Service 관리자 계정 설치</p>
<div class="alert">
<strong>참고</strong><br/><p>이는 보고 데이터베이스가 서비스와 별도로 설치 되는 경우에만 필요 합니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>보고 데이터베이스의 스키마 버전 테이블에 대 한 공용 액세스 이 계정은 App-v 5.1 reporting 데이터베이스 설치 중에 만들어야 합니다.</p></td>
</tr>
</tbody>
</table>



다음과 같은 추가 정보를 고려 합니다.

-   패키지 공유에 대 한 액세스-관리 서버와 같은 컴퓨터에 공유가 있는 경우 **네트워크** 서비스에서 공유에 대 한 읽기 권한이 필요 합니다. 또한 각 App-v 클라이언트 컴퓨터에는 패키지 공유에 대 한 읽기 권한이 있어야 합니다.

    **참고**  
    이전 버전의 App-v-V에서는 패키지 공유를 콘텐츠 공유 라고 합니다.



-   관리 서버에 게시 서버 등록-게시 서버는 관리 서버에 등록 되어 있어야 합니다. 예를 들어 게시 서버 컴퓨터 계정이 관리 서비스 API로 호출할 수 있도록 데이터베이스에 추가 해야 합니다.

### <a href="" id="-------------app-v-5-1-package-security"></a> 앱-V 5.1 패키지 보안

다음은 가상화 된 패키지의 안전성을 확인 하는 방법을 계획 하는 데 도움이 됩니다.

-   응용 프로그램 설치 관리자가 ACL (액세스 제어 목록)을 파일 또는 디렉터리에 적용 하는 경우 해당 ACL이 패키지에 유지 되지 않습니다. 패키지를 배포 하는 경우 사용자가 파일 또는 디렉터리를 수정 하는 경우 **% userprofile%** 의 acl을 상속 하거나 대상 컴퓨터의 acl을 상속 받습니다. 이전 경우는 파일 또는 디렉터리가 가상 파일 시스템 위치에 없는 경우에 발생 합니다. 후자의 경우 파일 또는 디렉터리가 가상 파일 시스템 위치 (예: **% windir%**)에 있는 경우에 발생 합니다.

## <a href="" id="---------app-v-5-1-log-files"></a> 앱-V 5.1 로그 파일


App-v 5.1 설정을 사용 하는 동안 설치 사용자의 **% temp%** 폴더에 설정 로그 파일이 만들어집니다.






## 관련 항목


[App-V 5.1용 환경 준비](preparing-your-environment-for-app-v-51.md)









