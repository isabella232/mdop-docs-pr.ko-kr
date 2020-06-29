---
title: MBAM 1.0 평가
description: MBAM 1.0 평가
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825253"
---
# MBAM 1.0 평가


Microsoft BitLocker 관리 및 모니터링 (MBAM)을 프로덕션 환경에 배포 하기 전에 랩 환경에서 평가 해야 합니다. 이 항목의 정보를 사용 하 여 평가 목적 으로만 단일 서버 랩 환경에서 MBAM을 설정할 수 있습니다.

실제 배포 단계는 [단일 서버에서 MBAM을 설치 하 고 구성](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)하는 방법에 설명 된 시나리오와 매우 유사 하지만이 항목에는 최소 시간 동안 mbam 평가 환경을 설정 하는 데 사용할 수 있는 추가 정보가 포함 되어 있습니다.

## 랩 환경 설정


랩 환경에서 평가할 MBAM의 비프로덕션 인스턴스를 설정 하는 경우에도 배포 선행 조건과 하드웨어 및 소프트웨어 요구 사항이 충족 되었는지 여전히 확인 해야 합니다. 자세한 내용은 [mbam 1.0 배포 필수 구성 요소](mbam-10-deployment-prerequisites.md) 및 [Mbam 1.0 지원 되는 구성을](mbam-10-supported-configurations.md)참조 하세요. MBAM 평가 배포를 시작 하기 전에 [mbam 1.0에 대 한 환경 준비](preparing-your-environment-for-mbam-10.md) 도 검토 해야 합니다.

### MBAM 평가 배포 계획

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">작업</th>
<th align="left">참조</th>
<th align="left">참고</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM에 대 한 시작 정보를 검토 하 여 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 지식을 얻으십시오.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">MBAM 1.0 시작</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>MBAM 설치에 대 한 컴퓨팅 환경을 준비 합니다. 이렇게 하려면 MBAM 데이터베이스를 호스트 하는 SQL Server 인스턴스에서 TDE (투명 한 데이터 암호화)를 사용 하도록 설정 해야 합니다. 랩 환경에서 TDE를 사용 하도록 설정 하려면 MBAM이 사용 하는 SQL Server 인스턴스에서 호스팅되는 마스터 데이터베이스에 대해 실행할 .sql 파일을 만들 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>다음 예제를 사용 하 여 MBAM 데이터베이스를 호스팅할 SQL Server 인스턴스에서 TDE를 빠르게 사용 하도록 설정 하는 랩 환경의 .sql 파일을 만들 수 있습니다. 이러한 SQL Server 명령은 로컬 서명 된 SQL Server 인증서를 사용 하 여 TDE를 사용 합니다. TDE 인증서 및 관련 암호화 키를 C:\Backup의 로컬 백업 경로 예제에 백업 해야 합니다 <em> </em> . 데이터베이스를 복구 하거나 인증서와 키를 입력 하는 다른 서버로 이동 하는 경우 TDE 인증서와 키가 필요 합니다.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">MBAM 1.0 배포 필수 구성 요소</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">SQL Server 2008 Enterprise Edition의 데이터베이스 암호화</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 그룹 정책 요구 사항 계획 및 구성</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">MBAM 1.0 그룹 정책 요구 사항 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>필요한 Active Directory 도메인 서비스 보안 그룹을 계획 하 고 만들고 MBAM 로컬 보안 그룹 구성원 요구 사항에 대 한 계획을 수립 합니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">MBAM 1.0 관리자 역할 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 서버 기능 배포 계획.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">MBAM 1.0 서버 배포 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 배포 계획.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">MBAM 1.0 클라이언트 배포 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### MBAM 평가 배포 수행

MBAM 설치에 대 한 컴퓨팅 환경을 준비 하는 데 필요한 계획 및 소프트웨어 필수 구성 요소 설치를 완료 한 후에는 MBAM 평가 배포를 시작할 수 있습니다.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 지원 구성 정보를 검토 하 여 선택한 클라이언트 및 서버 컴퓨터가 MBAM 기능 설치에 대해 지원 되는지 확인 합니다.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">MBAM 1.0 지원되는 구성</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>평가판을 위해 MBAM 설치를 실행 하 여 단일 서버에 MBAM 서버 기능을 배포 합니다.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">단일 서버에서 MBAM을 설치 및 구성하는 방법</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>계획 단계 중에 만든 Active Directory 도메인 서비스 보안 그룹을 새 MBAM 서버의 적절 한 로컬 MBAM 서버 기능 로컬 그룹에 추가 합니다.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">MBAM 1.0 관리자 역할 </a> 및 <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Mbam 관리자 역할을 관리 하는 방법에 대 한 계획</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>필요한 MBAM 그룹 정책 개체를 만들고 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">MBAM 1.0 그룹 정책 개체 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>MBAM 클라이언트 소프트웨어를 배포 합니다.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">MBAM 1.0 클라이언트 배포</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## MBAM 평가에 대 한 Lab 컴퓨터 구성


레지스트리 편집기를 사용 하 여 MBAM 클라이언트 상태 보고의 빈도 설정을 변경할 수 있습니다. 그러나 이러한 수정은 테스트 목적 으로만 사용 해야 합니다.

**Warning**  
이 항목에서는 레지스트리 편집기를 사용 하 여 Windows 레지스트리를 변경 하는 방법에 대해 설명 합니다. Windows 레지스트리를 잘못 변경 하면 Windows를 다시 설치 해야 할 수 있는 심각한 문제가 발생할 수 있습니다. 레지스트리를 변경 하려면 먼저 레지스트리 파일 (시스템. .dat 및 사용자)의 백업 복사본을 만들어야 합니다. Microsoft는 레지스트리를 변경할 때 발생할 수 있는 문제를 해결 하는 것을 보증 하지 않습니다. 레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>MBAM 클라이언트 상태 보고에서 주파수 설정 수정

그룹 정책을 사용 하도록 설정 하는 경우 MBAM 클라이언트 웨이크업 및 상태 보고 주파수는 최소 90 분의 값을 갖습니다. Windows 레지스트리를 더 낮은 값으로 편집 하 여 MBAM 클라이언트 컴퓨터에서 이러한 주파수를 변경할 수 있으며,이 경우 테스트 속도가 빨라집니다. MBAM 클라이언트 상태 보고에서 주파수 설정을 수정 하려면 레지스트리 편집기를 사용 하 여 **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**를 탐색 하 고 **ClientWakeupFrequency** 및 **StatusReportingFrequency** 의 값을 최소 클라이언트 지원 **값으로 변경한** 다음 BitLocker 관리 클라이언트 서비스를 다시 시작 합니다. 이 설정을 변경 하면 MBAM 클라이언트가 1 분 마다 보고 됩니다. 이 값을 레지스트리에서 수동으로 설정할 수 있습니다.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>MBAM 클라이언트 서비스에서 시작 지연 수정

Mbam 클라이언트 웨이크업 및 상태 보고 빈도 외에도 클라이언트 컴퓨터에서 MBAM 클라이언트 에이전트 서비스가 시작 될 때 최대 90 분의 지연이 있습니다. 임의 지연을 원하지 않으면 **HKLM\\Software\\Microsoft\\MBAM**에서 a 2의 **DWORD** 값을 만들고 해당 **NoStartupDelay** 값을 **1**로 설정한 다음 BitLocker 관리 클라이언트 서비스를 다시 시작 합니다.

## 관련 항목


[MBAM 1.0 시작](getting-started-with-mbam-10.md)









