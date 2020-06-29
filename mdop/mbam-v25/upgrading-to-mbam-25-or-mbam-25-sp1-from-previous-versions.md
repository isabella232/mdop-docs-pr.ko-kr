---
title: 이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드
description: 이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812753"
---
# 이전 버전에서 MBAM 2.5 또는 MBAM 2.5 SP1으로 업그레이드


이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 서버 및 이전 버전의 MBAM 클라이언트를 업그레이드 하는 프로세스에 대해 설명 합니다.

**참고**  이전 버전의 MBAM에서 MBAM 2.5 또는 MBAM 2.5 SP1로 직접 업그레이드할 수 있습니다.

 

## 업그레이드를 시작 하기 전에


업그레이드를 시작 하기 전에 다음 정보를 검토 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시작 하기 전에 알아야 할 사항</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>한 서버에 MBAM 웹 사이트를 설치 하는 경우 다른 서버의 웹 서비스에 Windows PowerShell cmdlet을 사용 하 여 구성 해야 합니다.</p></td>
<td align="left"><p>MBAM 서버 구성 마법사는 한 서버에서 웹 사이트를 구성 하는 작업과 다른 서버의 웹 서비스는 지원 하지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2에서 MBAM 2.0 또는 2.0 SP1에서 MBAM 2.5 또는 2.5 SP1로 업그레이드 하는 경우:</p>
<p>IIS (인터넷 정보 서비스)가 이미 설치 된 후 필요한 .NET Framework 4.5 소프트웨어를 설치 하는 경우 관리 및 모니터링 웹 사이트와 셀프 서비스 포털이 작동 하지 않습니다.</p>
<p>이 문제는 IIS가 이미 설치 된 후 .NET Framework가 설치 된 경우 ASP.NET에서 IIS에 올바르게 등록할 수 없기 때문에 발생 합니다.</p></td>
<td align="left"><p><strong>이 문제를 해결 하려면 다음을 수행 합니다.</strong></p>
<p><strong>다음 위치에서 aspnet_regiis 실행 – i </strong> :</p>
<p>C:\windows\microsoft.net\Framework\v4.0.30319</p>
<p>자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.NET IIS 등록 도구를 참조 </a> 하세요.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>다음이 모두 참일 경우 응용 프로그램 풀 계정에 SPN을 등록 합니다.</p>
<ul>
<li><p>이전 버전의 MBAM에서 업그레이드 하 고 있습니다.</p></li>
<li><p>현재 부하 분산 또는 분산 구성에서 MBAM 웹 사이트를 실행 하 고 있지는 않지만, MBAM 2.5 또는 2.5 SP1으로 업그레이드 하는 경우에도 마찬가지입니다.</p></li>
</ul></td>
<td align="left"><p>지침은 <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> MBAM 웹 사이트 보안 방법 계획을 참조 하세요 </a> .</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>권장 사항</strong></p></td>
<td align="left"><p>컴퓨터 계정에 대 한 Spn (서비스 사용자 이름)을 이미 등록 한 경우에도 해당 계정을 해당 계정에 등록할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>추천 이유</strong></p></td>
<td align="left"><p>부하 분산 또는 분산 구성에서 웹 사이트를 구성 하려면 응용 프로그램 풀 계정에 SPN을 등록 해야 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Spn이 컴퓨터 계정에 이미 구성 되어 있는 경우 어떻게 되나요?</strong></p></td>
<td align="left"><p>MBAM은 이미 등록 한 Spn을 사용 하지만 추가 Spn을 구성할 필요는 없지만 부하 분산 또는 분산 구성에서 웹 사이트를 구성할 수는 없습니다.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## MBAM 서버 인프라를 업그레이드 하는 단계


다음 섹션의 단계를 사용 하 여 독립 실행형 토폴로지 또는 System Center Configuration Manager 통합 토폴로지에 대해 MBAM을 업그레이드 합니다.

**독립 실행형 토폴로지에 대해 MBAM 서버 인프라를 업그레이드 하려면**

1.  이전 버전의 MBAM을 **프로그램 및 기능** , 웹 서버에서 제거 하 여 정보가 mbam 클라이언트에서 mbam 인프라로 기록 되지 않도록 합니다. 지침은 [MBAM 서버 기능 또는 소프트웨어 제거](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures)를 참조 하세요.

2.  데이터베이스를 백업 합니다.

3.  Sql Server Reporting Services를 통해 MBAM 보고서를 호스팅하는 SQL server를 비롯 하 여 **프로그램 및 기능**을 사용 하 여 이전 버전의 mbam을 제거 합니다. 데이터베이스 서버 및 reporting services에서 남아 있는 MBAM 서버 임시 파일 또는 폴더를 제거 합니다.

    **참고**  데이터베이스는 제거 되지 않으며 모든 준수 및 복구 데이터는 데이터베이스에서 유지 관리 됩니다.

     

4.  MBAM 또는 2.5 SP1 데이터베이스, 보고서, 웹 응용 프로그램을 순서 대로 설치 하 고 구성 합니다. 데이터베이스가 현재 위치에서 업그레이드 됩니다.

5.  MBAM 2.5 서식 파일을 사용 하 여 Gpo (그룹 정책 개체)를 업데이트 하 여 mbam 암호화와 같은 새로운 기능을 활용 합니다. Gpo와 MBAM 클라이언트를 MBAM 2.5으로 업데이트 하지 않으면 이전 버전의 MBAM 클라이언트는 기능 제한으로 현재 Gpo에 대해 계속 보고 합니다. 최신 ADMX 서식 파일을 다운로드 하려면 [MDOP 그룹 정책 (admx) 서식 파일을 가져오는 방법을](https://www.microsoft.com/download/details.aspx?id=41183) 참조 하세요.

    MBAM 서버 인프라를 업그레이드 하면 기존 클라이언트 컴퓨터가 여전히 MBAM 2.5 또는 2.5 SP1 서버에 성공적으로 보고 하 고 복구 데이터는 계속 저장 됩니다.

6.  최신 MBAM 2.5 또는 2.5 SP1 클라이언트를 설치 합니다. 배포 후 클라이언트 컴퓨터를 다시 부팅할 필요가 없습니다.

**System Center Configuration Manager 통합 토폴로지에 대해 MBAM 인프라를 업그레이드 하려면**

1.  이전 버전의 MBAM을 **프로그램 및 기능** , 웹 서버에서 제거 하 여 정보가 mbam 클라이언트에서 mbam 인프라로 기록 되지 않도록 합니다. 지침은 [MBAM 서버 기능 또는 소프트웨어 제거](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures)를 참조 하세요.

2.  데이터베이스를 백업 합니다.

3.  Sql Server Reporting Services를 통해 MBAM 보고서를 호스팅하는 SQL server를 비롯 하 여 **프로그램 및 기능**을 사용 하 여 이전 버전의 mbam을 제거 합니다. 데이터베이스 서버 및 reporting services에서 남아 있는 MBAM 서버 임시 파일 또는 폴더를 제거 합니다.

4.  Configuration Manager 서버에서 MBAM을 제거 합니다.

    **참고**  데이터베이스 및 Configuration Manager 개체 (기준, MBAM 지원 컴퓨터 모음 및 보고서)는 제거 되지 않으며 모든 준수 및 복구 데이터는 데이터베이스에서 유지 관리 됩니다.

     

5.  .Mof 파일을 업데이트 합니다.

6.  MBAM 또는 2.5 SP1 데이터베이스, 보고서, 웹 응용 프로그램, 구성 관리자 통합을 순서 대로 설치 하 고 구성 합니다. 데이터베이스 및 구성 관리자 개체가 현재 위치에서 업그레이드 됩니다.

7.  선택적으로, Gpo (그룹 정책 개체)를 업데이트 하 고 암호화를 적용 하는 등의 새 기능을 MBAM에 구현 하려는 경우 설정을 편집 합니다. Gpo를 업데이트 하지 않으면 MBAM은 현재 Gpo에 대해 계속 보고 합니다. 최신 ADMX 서식 파일을 다운로드 하려면 [MDOP 그룹 정책 (admx) 서식 파일을 가져오는 방법을](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) 참조 하세요.

    MBAM 서버 인프라를 업그레이드 하면 기존 클라이언트 컴퓨터가 여전히 MBAM 2.5 또는 2.5 SP1 서버에 성공적으로 보고 하 고 복구 데이터는 계속 저장 됩니다.

8.  최신 MBAM 2.5 또는 2.5 SP1 클라이언트를 설치 합니다. 배포 후 클라이언트 컴퓨터를 다시 부팅할 필요가 없습니다.

## MBAM 클라이언트에 대 한 업그레이드 지원


MBAM은 모든 이전 버전의 MBAM 클라이언트에서 MBAM 2.5 클라이언트로의 업그레이드를 지원 합니다.

**MBAM 클라이언트를 설치 하는 방법:**

-   Mbam 클라이언트를 실행 하는 컴퓨터를 모두 한 번에 업그레이드 하거나 MBAM 2.5 서버 인프라를 설치한 후 점진적으로 업그레이드할 수 있습니다.

-   전자 소프트웨어 배포 시스템을 통해 MBAM 클라이언트를 설치 하거나 Active Directory 도메인 서비스 또는 System Center Configuration Manager 등의 도구를 통해 가상으로 설정 합니다.



## 관련 항목


[MBAM 2.5 배포](deploying-mbam-25.md)

[MBAM 2.5 클라이언트 배포](deploying-the-mbam-25-client.md)

[MBAM 2.5 서버 기능 구성](configuring-the-mbam-25-server-features.md)

 

## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다. 





