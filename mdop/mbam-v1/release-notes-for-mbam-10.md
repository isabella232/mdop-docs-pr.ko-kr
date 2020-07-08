---
title: MBAM 1.0 릴리스 정보
description: MBAM 1.0 릴리스 정보
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826028"
---
# MBAM 1.0 릴리스 정보


**이러한 릴리스 노트에서 특정 문제를 검색 하려면 CTRL + F를 누릅니다.**

이 릴리스 정보는 Microsoft BitLocker 관리 및 모니터링 (MBAM)을 설치 하기 전에 자세히 읽어 보세요.

이 릴리스 정보에는 MBAM을 성공적으로 설치 하는 데 필요한 정보가 포함 되어 있습니다. 릴리스 노트에는 제품 설명서에서 사용할 수 없는 정보도 들어 있습니다. 이러한 릴리스 정보와 다른 MBAM 설명서 사이에 차이가 있는 경우 최신 변경 내용을 신뢰할 수 있는 것으로 간주 해야 합니다. 이러한 릴리스 정보는이 제품에 포함 된 콘텐츠를 대체 합니다.

## 제품 설명서 정보


MBAM 설명서에 대 한 자세한 내용은 Microsoft TechNet의 MBAM 홈페이지 홈 페이지를 참조 하세요.

MBAM 설명서의 다운로드 가능한 복사본을 얻으려면 <https://go.microsoft.com/fwlink/p/?LinkId=225356> Microsoft 다운로드 센터를 참조 하세요.

## 피드백 제공


귀하는 MBAM의 피드백에 관심이 있습니다. 귀하의 의견을 보낼 수 있습니다 <mdopdocs@microsoft.com> .

**참고**  이 이메일 주소는 지원 채널이 아니지만, 귀하의 문서와 제품 릴리스에서 향후에 변경 사항을 계획 하는 데 도움이 될 것입니다.

 

MDOP 및 추가 학습 리소스에 대 한 최신 정보는 [Mdop 정보 경험](https://go.microsoft.com/fwlink/p/?LinkId=236032) 페이지를 참조 하세요.

새 업데이트 또는 피드백을 제공 하는 방법에 대 한 자세한 내용은 [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) 또는 [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447)를 참조 하세요.

## MBAM 1.0의 알려진 문제점


이 섹션에서는 MBAM 설정 및 설치의 알려진 문제점에 대 한 릴리스 정보를 포함 합니다.

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a>설치 중에 "인증서를 사용 하 여 네트워크 통신 암호화" 옵션을 선택 하면 기존 데이터베이스 연결 및 종속 응용 프로그램이 작동을 중지할 수 있습니다.

복구 및 하드웨어 데이터베이스 또는 준수 상태 데이터베이스 기능을 설치한 후 **암호화 된 네트워크 통신용** 으로 mbam을 구성할 수 있습니다. 암호화 된 네트워크 통신을 위해 MBAM을 구성 하기로 선택 하면 해당 데이터베이스와 관리 및 모니터링 서버 간 통신을 위해 SSL (Secure Sockets layer)을 사용 하도록 SQL Server 데이터베이스 엔진의 인스턴스를 구성 하 고 준수 및 감사 보고서 서버 기능을 설정 합니다.

-   SQL Server 데이터베이스 엔진의 인스턴스가 SSL을 사용 하도록 아직 구성 되어 있지 않은 경우 MBAM 설치에서이를 수행 하도록 구성 합니다. 이렇게 하면 SQL Server 데이터베이스 엔진 인스턴스에서 비 MBAM 데이터베이스를 사용 하 여 데이터베이스와 통신 하지 못하도록 하는 응용 프로그램에 문제가 있을 수 있습니다.

-   SQL Server 데이터베이스 엔진의 인스턴스가 SSL을 사용 하도록 이미 구성 되어 있는 경우 설치 중에 사용자가 선택한 인증서를 사용 하도록 구성 됩니다. 이 인증서가 이미 사용 중인 것과 다른 경우 SQL Server 데이터베이스 엔진의 인스턴스에서 SQL Server 데이터베이스를 사용 하는 응용 프로그램이 실행 되지 않도록 할 수 있습니다.

**해결 방법:** 않아야

### 로컬 관리자 계정을 사용 하는 경우 설치 중에 MBAM 설치가 실패 함

로컬 관리자 계정을 사용 하는 경우 MBAM 설정이 실패 합니다. 로그 파일에는 다음 정보가 포함 되어 있습니다.

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

**해결 방법:** MBAM을 설치할 때 서버 컴퓨터에서 관리 자격 증명이 있는 도메인 계정을 사용 합니다.

### MBAM 설정 "네트워크 통신을 암호화 하지 않음"을 선택 하면 SQL Server 데이터베이스 엔진의 인스턴스가 SSL을 사용 하지 않도록 재구성 됩니다.

복구 및 하드웨어 데이터베이스 또는 준수 상태 데이터베이스를 설치 하는 경우 설치 프로그램을 사용 하 여 **암호화 된 네트워크 통신**을 선택 하 여 mbam을 구성할 수 있습니다. 네트워크 통신을 암호화 하지 않기로 결정 한 경우, MBAM Setup이 SSL을 사용 하지 않도록 SQL Server 데이터베이스 엔진의 인스턴스를 재구성 합니다.

-   SQL Server 데이터베이스 엔진의 인스턴스가 이미 SSL을 사용 하도록 구성 된 경우 MBAM 설치는 SQL Server 데이터베이스 엔진 인스턴스에서 SSL을 사용 하지 않도록 설정 합니다. 이렇게 하면 SQL Server 데이터베이스 엔진 인스턴스의 MBAM 데이터베이스에 연결 되지 않은 데이터베이스를 사용 하는 응용 프로그램 간의 통신 보안이 변경 됩니다.

**해결 방법:** 않아야

### IIS (인터넷 정보 서비스) 관리 스크립트 및 도구 웹 서버 기능에 대 한 필수 구성 요소가 없음

MBAM 설정에는 IIS 관리 스크립트와 도구 웹 서버 기능에 종속 되어 있지만, 필수 구성 요소는 적용 되지 않습니다. 이 기능이 누락 되 면 서버 설치를 통해 MBAM을 설치할 수 있습니다. 그러나이 경우 Windows Management Instrumentation (WMI) 및 IIS (인터넷 정보 서비스) 공급자를 찾을 수 없기 때문에 백업 서비스 MBAM 기록기가 시작 된 후 중지 됩니다. 이벤트 로그에서 발생 하는 경우를 제외 하 고이 조건에 대 한 오류 메시지가 없습니다. IIS 관리 스크립트와 도구 없이 MBAM을 설치 하면 MBAM에 대해 백업 작업이 실행 되지 않습니다.

**해결 방법:** MBAM 설정을 시작 하기 전에 IIS 관리 스크립트와 도구 웹 서버 기능이 설치 되어 있는지 확인 합니다.

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a>설치 프로그램이 인증서를 사용 하도록 구성 된 경우 MBAM 설정이 "선택한 기능 설치 중" 단계에서 응답을 중지 함

MBAM 설치의 **선택 된 기능을 설치** 하는 동안 설치 프로그램이 응답을 중지 합니다. 이는 **인증서를 사용 하 여 네트워크 통신 옵션을 암호화 하** 는 경우 복구 및 하드웨어 데이터베이스 또는 준수 상태 데이터베이스를 설치 하는 동안에 발생 합니다. 또한, SQL Server 데이터베이스 엔진의 인스턴스가 설치 중에 지정 된 인증서에 액세스할 수 없는 경우 MBAM 설정이 응답을 중지 합니다.

**해결 방법:** 해당 SQL Server 데이터베이스 엔진의 해당 인스턴스에 대 한 Windows 서비스에서 인증서에 액세스할 수 있도록 인증서의 사용 권한을 업데이트 합니다. 또한 SQL Server 데이터베이스 엔진의 인스턴스가 실행 되는 계정을 변경 하 여 데이터베이스 엔진이 인증서를 사용할 수 있습니다. 인증서에 대 한 사용 권한을 확인 하려면 명령 프롬프트에 다음 명령을 입력 합니다. **certutil-v-MY store**

### SQL Server Reporting Services를 설치 하면 MBAM 설정이 일시 중지 됨

MBAM 설치 중에 SQL Server Reporting Services (SSRS) 인스턴스를 선택 하거나 SSRS 인스턴스를 사용할 수 없거나 잘못 구성 된 경우 MBAM 설정이 SSRS 인스턴스와 통신 하는 데 1 분까지 일시 중지 될 수 있습니다.

**해결 방법:** 설치 프로그램이 SSRS 인스턴스에 접속 하려고 시도 하는 동안 MBAM 설정이 1 분 이상 일시 중단 될 때까지 기다립니다.

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a>설치 후 관리 및 모니터링 서버가 실행 되지 않음

MBAM 설정이 관리 및 모니터링 서버 기능을 성공적으로 설치 하면 MBAM 관리자 웹 사이트에 액세스 하려고 할 때 오류 메시지가 표시 됩니다. 이 문제는 다음 이유 중 하나로 인해 발생 합니다.

-   MBAM 설치 후 관리 및 모니터링 서버에서 하나 이상의 필수 조건이 제거 되었습니다.

-   하나 이상의 필수 구성 요소가 서버에 설치 되어 있으며 MBAM 설정을 실행 하기 전에 제거 되었습니다.

**해결 방법:** MBAM 설명서를 검토 하 고 모든 MBAM 필수 조건이 설치 되어 있는지 확인 합니다.

### 설치 중에 설명서 링크를 클릭 하면 설치가 완료 된 후 응용 프로그램 오류가 발생 합니다.

설치 중에 설명서 링크를 클릭 한 다음 설치를 완료 한 후 **취소** 또는 **마침을** 클릭 하 여 설치 프로그램을 닫으면 응용 프로그램 오류 메시지가 나타납니다. 이 문제는 Windows 작업 스케줄러의 액세스 위반 오류로 인해 발생 합니다.

**해결 방법:** 않아야. 이 오류는 무시할 수 있습니다.

### MBAM 설치는 새 데이터베이스를 제거 하지 않습니다.

MBAM 설정이 실패 하는 경우 설치 프로그램이 새로 만든 데이터베이스를 제거 하지 못할 수 있습니다. 이로 인해 후속 설치가 실패할 수 있습니다.

**해결 방법:** 후속 설치 중에 데이터베이스 인스턴스의 다른 이름을 선택 합니다.

### MBAM 설정에서 유효한 네트워크 부하 분산 클러스터 인증서를 인식 하지 못합니다.

MBAM 관리 및 모니터링 서버 설치 중 네트워크 암호화 옵션이 선택 되어 있으면 클러스터 인증서가 유효한 인증서로 인식 되지 않습니다. 데이터베이스와 통신 하기 위한 인증서가 설치 되어 있지만 부하 분산 클러스터의 통신에 대해 거부 되는 경우 유효한 것으로 인식 됩니다.

**해결 방법:** 인증서와 연결 된 CRL (인증서 해지 목록)에 액세스할 수 있는지 확인 하거나 CRL을 사용 하 여 유효성 검사가 필요 하지 않은 인증서를 사용 합니다.

## 릴리스 노트 저작권 정보


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune 및 WindowsPowerShell는 Microsoft의 회사 그룹의 상표입니다. 다른 모든 상표는 해당 소유자의 재산입니다.



## 관련 항목


[MBAM 1.0 정보](about-mbam-10.md)

 

 





