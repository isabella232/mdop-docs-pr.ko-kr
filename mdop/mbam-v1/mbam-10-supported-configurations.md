---
title: MBAM 1.0 지원되는 구성
description: MBAM 1.0 지원되는 구성
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825938"
---
# MBAM 1.0 지원되는 구성


이 항목에서는 사용자 환경에서 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하 고 실행 하는 데 필요한 요구 사항을 설명 합니다.

## <a href="" id="---------mbam-server-system-requirements"></a> MBAM 서버 시스템 요구 사항


### 서버 운영 체제 요구 사항

다음 표에는 Microsoft BitLocker 관리 및 모니터링 서버 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</p></td>
<td align="left"><p>SP2만 해당</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</p></td>
<td align="left"></td>
<td align="left"><p>64비트</p></td>
</tr>
</tbody>
</table>



**Warning**  
도메인 컨트롤러 컴퓨터에는 MBAM 서비스, 보고서 또는 데이터베이스를 설치 하는 기능이 지원 되지 않습니다.



### <a href="" id="server-random-access-memory--ram--requirements-"></a>서버 RAM (임의 액세스 메모리) 요구 사항

MBAM 서버 설치와 관련 된 RAM 요구 사항은 없습니다.

### <a href="" id="sql-server-database-requirements-"></a>SQL Server 데이터베이스 요구 사항

다음 표에는 MBAM 서버 기능 설치에 대해 지원 되는 SQL Server 버전이 나와 있습니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">MBAM 서버 기능</th>
<th align="left">SQL Server 버전</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>규정 준수 및 감사 보고서</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter 또는 Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>복구 및 하드웨어 데이터베이스</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Enterprise, Datacenter 또는 Developer Edition</p>
<div class="alert">
<strong>중요</strong><br/><p>MBAM 복구 및 하드웨어 데이터베이스 서버 기능 설치에는 SQL Server Standard Edition이 지원 되지 않습니다.</p>
</div>
<div>

</div></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="odd">
<td align="left"><p>준수 및 감사 데이터베이스</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p></td>
<td align="left"><p>R2, Standard, Enterprise, Datacenter 또는 Developer Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> MBAM 클라이언트 시스템 요구 사항


### 클라이언트 운영 체제 요구 사항

다음 표에는 MBAM 클라이언트 설치에 대해 지원 되는 운영 체제가 나와 있습니다.

**참고**  
Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다. 제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요. Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">시스템 아키텍처</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Enterprise 버전</p></td>
<td align="left"><p>없음, SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate Edition</p></td>
<td align="left"><p>없음, SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>클라이언트 RAM 요구 사항

MBAM 클라이언트 설치와 관련 된 RAM 요구 사항은 없습니다.

## 관련 항목


[MBAM 1.0 배포 계획](planning-to-deploy-mbam-10.md)

[MBAM 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md)









