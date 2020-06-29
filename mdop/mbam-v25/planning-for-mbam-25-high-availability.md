---
title: MBAM 2.5 고가용성 계획
description: MBAM 2.5 고가용성 계획
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826943"
---
# MBAM 2.5 고가용성 계획


Microsoft BitLocker 관리 및 모니터링 (MBAM)은 다음 섹션에서 설명 하는 다음 기술 중 하나 이상을 사용 하 여 고가용성을 유지할 수 있습니다.

-   [SQL Server AlwaysOn 가용성 그룹](#bkmk-alwayson)

-   [Microsoft SQL Server 클러스터링](#bkmk-sql-clustering)

-   [IIS 네트워크 부하 분산](#bkmk-load-balance)

-   [SQL Server의 데이터베이스 미러링](#bkmk-db-mirroring)

-   [VSS (볼륨 섀도 복사본 서비스)를 사용 하 여 MBAM 데이터베이스 백업](#bkmk-vss)

다음 섹션의 정보를 사용 하 여 항상 사용 가능한 구성에서 MBAM을 배포 하는 옵션을 이해할 수 있습니다.

## <a href="" id="bkmk-alwayson"></a>SQL Server AlwaysOn 가용성 그룹 지원


MBAM을 사용 하면 Microsoft SQL Server에서 데이터베이스에 대 한 가용성 그룹을 구성 하 고 관리할 수 있습니다. MBAM의 가용성 그룹은 규정 준수 및 감사 데이터베이스와 복구 데이터베이스가 개별적이 아니라 함께 작동 하지 않는 장애 조치 환경을 지원 합니다.

가용성 그룹은 읽기/쓰기 기본 데이터베이스 집합과 하나에서 네 개의 해당 보조 데이터베이스 집합을 지원 합니다. 선택적으로 보조 데이터베이스를 읽기 전용 권한, 일부 백업 작업 또는 둘 다에 사용할 수 있습니다.

가용성 그룹을 설정 하는 방법에 대 한 자세한 내용은 [AlwaysOn 가용성 그룹](https://go.microsoft.com/fwlink/?LinkId=393277)을 참조 하세요.

## <a href="" id="bkmk-sql-clustering"></a>Microsoft SQL Server 클러스터링


SQL Server 클러스터를 실행 하는 컴퓨터에서 MBAM 2.5 준수 및 감사 데이터베이스와 복구 데이터베이스를 실행할 수 있습니다.

## <a href="" id="bkmk-load-balance"></a>IIS 네트워크 부하 분산


네트워크 로드 균형 조정을 사용 하 여 관리 및 모니터링 웹 사이트 (지원 센터 라고도 함), 셀프 서비스 포털 및 IIS (인터넷 정보 서비스)를 통해 배포 되는 웹 서비스를 실행 하는 컴퓨터에 대해 항상 사용 가능한 환경을 구성할 수 있습니다.

### 필수 구성 요소

부하 분산을 구성 하기 전에 다음 필수 조건을 충족 하는지 확인 합니다.

-   부하 분산 장치를 사용할 수 있어야 합니다. Microsoft 또는 다른 회사의 부하 분산 장치를 사용할 수 있습니다. Microsoft 부하 분산 장치 기술에 대 한 자세한 내용은 [IIS 서버로 웹 팜 빌드](https://go.microsoft.com/fwlink/?LinkId=393326)를 참조 하세요.

-   적어도 두 대의 서버가 IIS를 실행 중이 고 ASP.NET MVC 4를 포함 하 여 웹 기능을 지원 하기 위해 모든 MBAM 전제 조건을 충족 했습니다.

-   MBAM 데이터베이스와 보고서는 서버에서 실행 됩니다.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> 부하 분산을 사용 하는 데 필요한 MBAM 관련 변경 사항

다음 작업을 완료 합니다.

1.  웹 응용 프로그램 풀에 사용 하는 도메인 계정 아래에 가상 호스트 이름에 대 한 SPN (서비스 사용자 이름)을 등록 합니다. 예를 들어 가상 호스트 이름이 mbamvirtual.contoso.com 웹 응용 프로그램 풀에 사용 되는 도메인 계정이 contoso\\mbamapppooluser 이면 다음 명령은 SPN을 적절 하 게 등록 합니다.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  다음 MBAM 웹 기능을 구성 합니다.

    -   MBAM 웹 기능을 호스트할 각 서버에서 응용 프로그램 풀 관리 자격 증명에 동일한 도메인 계정을 사용 합니다.

    -   부하 분산 클러스터의 가상 호스트 이름 (DNS 이름)과 일치 하는 호스트 이름을 지정 합니다. 예를 들어 가상 호스트 이름을 **mbamvirtual.contoso.com**로 "NLB1" 라는 서버에 mbam을 설치 하는 경우 Windows PowerShell cmdlet에서 지정 하는 호스트 이름이 **mbamvirtual.contoso.com**있는지 확인 합니다.

3.  부하 분산 장치를 사용 하 여 웹 팜에서 웹사이트를 구성 하는 경우에는 동일한 컴퓨터 키를 사용 하도록 웹사이트를 구성 해야 합니다.

    자세한 내용은 [MachineKey 요소 (ASP.NET Settings 스키마)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx)의 다음 섹션을 참조 하세요.

    -   컴퓨터 키 설명

    -   웹 팜 배포 고려 사항

    키를 자동으로 생성 하는 방법에 대 한 지침은 [컴퓨터 키 생성 (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx)을 참조 하세요.

부하 분산에 대 한 정보는 Windows Server 2012 또는 Windows Server2008R2의 IIS NLB (네트워크 부하 분산) 클러스터에도 적용 됩니다. Windows Server 2012의 IIS 네트워크 부하 분산 기능은 일반적으로 Windows Server2008R2에서와 동일 합니다. 그러나 일부 작업 세부 정보는 Windows Server 2012에서 다릅니다. 작업을 수행 하는 새로운 방법에 대 한 자세한 내용은 [Windows server 2012 R2 Preview 및 Windows server 2012의 일반적인 관리 작업 및 탐색](https://go.microsoft.com/fwlink/?LinkId=316371)을 참조 하세요.

## <a href="" id="bkmk-db-mirroring"></a>SQL Server의 데이터베이스 미러링


MBAM은 각 데이터베이스에 대해 두 개의 SQL Server 인스턴스를 사용 하 여 규정 준수 및 감사 데이터베이스와 복구 데이터베이스가 미러링 되는 SQL Server 미러링 사용을 지원 합니다. 미러링을 구현 하기 전에이 항목의 앞부분에서 설명한 가용성 그룹의 우선 미러링이 느리게 진행 되는 것에 유의 해야 합니다.

MBAM에 대 한 미러링을 구현 하려면 **Enable-MbamWebApplication** Windows PowerShell cmdlet을 사용 하 여 미러된 데이터베이스 구성에 대 한 적절 한 연결 문자열을 지정 해야 합니다. MBAM 2.5 Windows PowerShell cmdlet에 대 한 자세한 내용은 [Windows powershell을 사용 하 여 mbam 2.5 서버 기능 구성을](configuring-mbam-25-server-features-by-using-windows-powershell.md)참조 하세요.

### Windows PowerShell을 사용 하 여 SQL Server 미러링을 구현 하는 예제

다음 예제에서는 Windows PowerShell cmdlet을 사용 하 여 SQL Server 미러링을 구현 하는 방법을 보여 줍니다.

**예제 1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**예제 2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### SQL Server 미러링에 대 한 자세한 정보

다음 링크는 SQL Server 미러링 구성에 대 한 자세한 정보를 제공 합니다.

-   [방법: 미러링에 대 한 미러 데이터베이스 준비 (T-sql)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Windows 인증 (SQL Server Management Studio)을 사용 하 여 데이터베이스 미러링 세션 설정](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>VSS (볼륨 섀도 복사본 서비스)를 사용 하 여 MBAM 데이터베이스 백업


MBAM은 Microsoft BitLocker 관리 및 관리 작성자 라고 하는 VSS (볼륨 섀도 복사본 서비스) 기록기를 제공 합니다. 이 VSS 기록기는 준수 및 감사 데이터베이스와 복구 데이터베이스를 쉽게 백업할 수가 있습니다.

VSS 기록기는 MBAM 웹 응용 프로그램을 사용 하도록 설정 하는 모든 서버에 등록 되어 있습니다. MBAM VSS 기록기는 Microsoft SQL Server 설치의 일부로 등록 된 SQL Server VSS 기록기에 따라 달라 집니다. 백업을 수행 하기 위해 VSS 기록기를 사용 하는 모든 백업 기술은 MBAM VSS 기록기를 검색할 수 있습니다.



## 관련 항목


[MBAM 2.5 배포 계획](planning-to-deploy-mbam-25.md)

 

 
## MBAM에 대 한 제안이 있으십니까?
- [여기](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)에서 제안을 추가 하거나 투표 합니다.
- MBAM 문제의 경우 [Mbam TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)을 사용 합니다.




