---
title: MBAM 2.5 그룹 및 계정 계획
description: MBAM 2.5 그룹 및 계정 계획
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825803"
---
# MBAM 2.5 그룹 및 계정 계획


이 항목에서는 Microsoft AD DS (Active Directory 도메인 서비스)에서 보안 및 액세스 권한을 제공 하 고 (예, MBAM) 데이터베이스, 보고서, 웹 응용 프로그램을 위해 만들어야 하는 역할 및 계정을 나열 합니다. 각 역할 및 계정에 대해 MBAM 서버 구성 마법사의 해당 필드를 제공 합니다. 이러한 계정에 해당 하는 Windows PowerShell cmdlet 및 매개 변수 목록은 [Windows powershell을 사용 하 여 MBAM 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts)참조 하세요.

**참고**  
MBAM은 관리 서비스 계정 사용을 지원 하지 않습니다.



## 데이터베이스 계정


준수 및 감사 데이터베이스와 복구 데이터베이스에 대해 다음 계정을 만듭니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">계정 이름 및 용도</th>
<th align="left">계정 유형</th>
<th align="left">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드</th>
<th align="left">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드에 대 한 설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>준수 및 감사 데이터베이스 및 복구 데이터베이스 보고서에 대 한 사용자 또는 그룹 읽기/쓰기</p></td>
<td align="left"><p>사용자 또는 그룹</p></td>
<td align="left"><p>읽기/쓰기 액세스 도메인 사용자 또는 그룹</p></td>
<td align="left"><p>준수 및 감사 데이터베이스와 복구 데이터베이스에 대 한 읽기/쓰기 권한이 있는 도메인 사용자 또는 그룹으로, 웹 응용 프로그램에서 이러한 데이터베이스의 데이터 및 보고서에 액세스할 수 있습니다.</p>
<p>이 필드에 사용자 이름을 입력 하는 경우 <strong> </strong> <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값과 동일 해야 합니다 </strong> .</p>
<p>이 필드에 그룹 이름을 입력 하는 경우 <strong> 웹 응용 프로그램 구성 페이지의 웹 서비스 응용 프로그램 풀 도메인 계정 필드에 있는 값 </strong> <strong> </strong> 이이 필드에 입력 하는 그룹의 구성원 이어야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>보고서에 대 한 규정 준수 및 감사 데이터베이스 읽기 전용 사용자 또는 그룹</p></td>
<td align="left"><p>사용자 또는 그룹</p></td>
<td align="left"><p>읽기 전용 액세스 도메인 사용자 또는 그룹</p></td>
<td align="left"><p>규정 준수 및 감사 데이터베이스에 대 한 읽기 전용 액세스 권한을 가지는 사용자 또는 그룹의 이름으로, 보고서에서이 데이터베이스의 규정 준수 및 감사 데이터에 액세스할 수 있습니다.</p>
<p>이 필드에 사용자 이름을 입력 하는 경우 <strong> </strong> <strong> 보고서 구성 페이지의 규정 준수 및 감사 데이터베이스 도메인 계정 필드에 지정 하는 사용자와 동일 해야 합니다 </strong> .</p>
<p>이 필드에 그룹 이름을 입력 하는 경우 <strong> 보고서 구성 페이지의 규정 준수 및 감사 데이터베이스 도메인 계정 필드에 지정한 값 </strong> <strong> </strong> 이이 필드에서 지정 하는 그룹의 구성원 이어야 합니다.</p></td>
</tr>
</tbody>
</table>



## 보고 계정


보고서 기능에 대해 다음 계정을 만듭니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">계정 이름/용도</th>
<th align="left">계정 유형</th>
<th align="left">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드</th>
<th align="left">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드에 대 한 설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>읽기 전용 도메인 액세스 그룹 보고</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>보고 역할 도메인 그룹</p></td>
<td align="left"><p>관리 및 모니터링 웹 사이트의 보고서에 대 한 읽기 전용 액세스 권한이 있는 도메인 사용자 그룹을 지정 합니다. 지정 하는 그룹은 웹 앱을 사용할 수 있는 경우 보고서 읽기 전용 액세스 그룹 매개 변수에 대해 지정한 그룹과 동일 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>준수 및 감사 데이터베이스 도메인 사용자 계정</p></td>
<td align="left"><p>사용자</p></td>
<td align="left"><p>준수 및 감사 데이터베이스 도메인 계정</p></td>
<td align="left"><p>로컬 SQL Server Reporting Services 인스턴스에서 준수 및 감사 데이터베이스에 액세스 하는 데 사용 하는 도메인 사용자 계정 및 암호입니다. 이 계정에 <strong> </strong> 는 SQL Server Reporting Services 서버에 일괄 처리 권한으로 로그온이 필요 합니다.</p>
<p><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 하는 값이 </strong> <strong> </strong> 사용자 이름 이면이 필드에 같은 값을 입력 해야 합니다.</p>
<p><strong>데이터베이스 구성 페이지의 읽기 전용 액세스 도메인 사용자 또는 그룹 필드에 입력 하는 값이 </strong> <strong> </strong> 그룹 이름이 면이 필드에 입력 하는 값이 해당 그룹의 구성원 이어야 합니다.</p>
<p>이 계정에 대 한 암호가 만료 되지 않도록 구성 합니다. 사용자 계정은 MBAM 보고서 사용자 그룹에서 사용할 수 있는 모든 데이터에 액세스할 수 있어야 합니다.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a>관리 및 모니터링 웹 사이트 (지원 센터) 계정


관리 및 모니터링 웹 사이트에 대해 다음 계정을 만듭니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">계정 이름/용도</th>
<th align="left">계정 유형</th>
<th align="left">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드</th>
<th align="left">이 계정에 해당 하는 MBAM 서버 구성 마법사 필드에 대 한 설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>웹 서비스 응용 프로그램 풀 도메인 계정</p></td>
<td align="left"><p>사용자</p></td>
<td align="left"><p>웹 서비스 응용 프로그램 풀 도메인 계정</p></td>
<td align="left"><p>웹 응용 프로그램의 응용 프로그램 풀에서 사용할 도메인 사용자 계정입니다.</p>
<p><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 사용자 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 같은 값을 입력 해야 합니다.</p>
<p><strong>데이터베이스 구성 페이지의 읽기/쓰기 도메인 사용자 또는 그룹 필드에 그룹 이름을 입력 하는 경우 </strong> <strong> </strong> 이 필드에 입력 하는 값은 해당 그룹의 구성원 이어야 합니다.</p>
<p>자격 증명을 지정 하지 않으면 이전에 사용 하도록 설정 된 웹 응용 프로그램에 대해 지정 된 자격 증명이 사용 됩니다. 모든 웹 응용 프로그램은 동일한 응용 프로그램 풀 자격 증명을 사용 해야 합니다. 여러 웹 응용 프로그램에 대해 다른 자격 증명을 지정 하는 경우 가장 최근에 지정 된 값이 사용 됩니다.</p>
<div class="alert">
<strong>중요</strong><br/><p>보안 향상을 위해 자격 증명에 지정 된 계정에 제한 된 사용자 권한을 설정 합니다.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 고급 헬프 데스크 사용자 액세스 그룹</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>구성원이 관리 및 모니터링 웹 사이트의 모든 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다. 이 역할을 사용 하는 사용자는 최종 사용자의 도메인 및 사용자 이름 대신 복구 키만 입력 해야 하는 데,이를 사용 하 여 엔드 사용자의 드라이브 복구를 도울 수 있습니다. 사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 그룹 사용 권한 보다 우선 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 헬프데스크 사용자 액세스 그룹</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>MBAM 헬프데스크 사용자</p></td>
<td align="left"><p>구성원이 MBAM 관리 및 모니터링 웹 사이트의 TPM 관리 및 드라이브 복구 영역에 액세스할 수 있는 도메인 사용자 그룹입니다. 이 역할이 있는 개인은 두 옵션 중 하나를 사용할 때 최종 사용자의 도메인 및 계정 이름을 포함 하 여 모든 필드를 채워야 합니다.</p>
<p>사용자가 MBAM 헬프데스크 사용자 그룹 및 Mbam 헬프데스크 사용자 그룹의 구성원 인 경우 MBAM 고급 헬프 데스크 사용자 그룹 권한이 MBAM 헬프데스크 그룹 사용 권한 보다 우선 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM 보고서 사용자 액세스 그룹</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>MBAM 보고서 사용자</p></td>
<td align="left"><p>구성원이 관리 및 모니터링 웹 사이트의 보고서 영역에 있는 보고서에 대 한 읽기 전용 액세스 권한을 갖는 도메인 사용자 그룹입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM 데이터 마이그레이션 사용자 그룹</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>MBAM 데이터 마이그레이션 사용자</p></td>
<td align="left"><p>구성원이 mbam 서버에서 실행 되는 MBAM 복구와 하드웨어 서비스를 사용 하 여 MBAM에 데이터를 쓸 수 있는 권한이 있는 도메인 사용자 그룹 (선택 사항). 이 계정은 일반적으로 Active Directory에서 MBAM 데이터베이스로 복구 및 TPM 데이터를 쓰는 데 비 Mbam * cmdlet과 함께 사용 됩니다.</p>
<p>자세한 내용은 <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> mbam 2.5 보안 고려 사항을 참조 하세요 </a> .</p></td>
</tr>
</tbody>
</table>




## 관련 항목


[MBAM 2.5용 환경 준비](preparing-your-environment-for-mbam-25.md)

[MBAM 2.5 배포 필수 구성 요소](mbam-25-deployment-prerequisites.md)



## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다. 
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





