---
title: MBAM 2.0 SP1 정보
description: MBAM 2.0 SP1 정보
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823553"
---
# MBAM 2.0 SP1 정보

이 항목에서는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)의 변경 사항에 대해 설명 합니다. MBAM에 대 한 일반적인 설명은 [mbam 2.0 시작](getting-started-with-mbam-20-mbam-2.md)을 참조 하세요.

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>MBAM 2.0 SP1의 새로운 기능

이 MBAM 버전은 다음과 같은 새로운 기능과 기능을 제공 합니다.

### Windows 8.1, Windows Server 2012 R2 및 System Center 2012 R2 구성 관리자에 대 한 지원

Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 SP1(서비스 팩 1)은 Windows 8.1, Windows Server 2012 R2 및 System Center 2012 R2 구성 관리자에 대 한 지원을 추가 합니다.

### Microsoft SQL Server 2008 R2 SP2에 대 한 지원

Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 서비스 팩 1(sp1)은 Microsoft SQL Server 2008 R2 SP2에 대 한 지원을 추가 합니다. Microsoft System Center Configuration Manager 2007 R2를 실행 하는 경우 Microsoft SQL Server 2008 R2 이상을 사용 해야 합니다.

### 고객 의견 롤업

MBAM 2.0 SP1에는 Microsoft BitLocker 관리 및 모니터링 (MBAM) 2.0 출시 이후 발견 된 문제를 해결 하기 위한 해결 방법에 대 한 롤업을 포함 하 고 있습니다. 이러한 변경 사항으로 인해 Microsoft System Center Configuration Manager 2007에서 MBAM을 실행 하면 컴퓨터 이름 필드가 BitLocker 컴퓨터 준수 및 BitLocker 엔터프라이즈 준수 세부 정보 보고서에 표시 됩니다.

### 셀프 서비스 포털의 포트와 관리 및 모니터링 웹 사이트에 대 한 방화벽 예외를 설정 해야 합니다.

셀프 서비스 포털 및 관리 및 모니터링 웹 사이트를 구성 하는 경우 지정 된 포트를 통해 통신을 사용 하도록 방화벽 예외를 설정 해야 합니다. 이전에는 MBAM 서버 설치가 Windows 방화벽에서 자동으로 포트를 열었습니다.

### Configuration Manager에서 MBAM 보고서의 위치가 변경 됨

이제 MBAM 노드 내의 하위 폴더에서 Configuration Manager 통합 토폴로지에 대 한 MBAM 보고서를 사용할 수 있습니다. 하위 폴더 이름은 하위 폴더 내의 보고서 언어를 나타냅니다.

### Configuration Manager에서 MBAM을 설치할 때 기본 사이트 서버에 MBAM을 설치할 수 있는 기능

Configuration Manager 통합 토폴로지로 MBAM을 설치할 때 기본 사이트 서버나 중앙 관리 사이트 서버에 MBAM을 설치할 수 있습니다. 이전에는 중앙 관리 사이트 서버에 MBAM을 설치 해야 했습니다.

**중요**  
MBAM을 설치 하는 서버는 계층 구조의 최상위 계층 서버 여야 합니다.



MBAM 설치는 다음과 같이 Microsoft System Center Configuration Manager 2007 및 Microsoft System Center 2012 Configuration Manager에 대해 다르게 작동 합니다.

-   **구성 관리자 2007** : 크기가 더 크고, 중앙 사이트 상위 서버가 있는 주 사이트 서버에 mbam을 설치 하는 경우, mbam은 중앙 사이트 상위 서버를 확인 하 고 해당 상위 서버의 모든 설치 작업을 수행 합니다. 설치 작업에는 필수 조건을 확인 하 고 Configuration Manager 개체 및 보고서를 설치 하는 작업이 포함 됩니다. 예를 들어, 중앙 사이트 상위 서버의 자식인 주 사이트 서버에 MBAM을 설치 하는 경우 MBAM은 상위 서버에 모든 Configuration Manager 개체와 보고서를 설치 합니다. 부모 서버에 MBAM을 설치 하는 경우 MBAM은 해당 상위 서버의 모든 설치 작업을 수행 합니다.

-   **System Center 2012 구성 관리자** : 주 사이트 서버나 중앙 관리 서버에 mbam을 설치 하는 경우 mbam은 해당 사이트 서버에서 모든 설치 작업을 수행 합니다.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> MBAM 서버를 설치 하는 컴퓨터에 Configuration Manager 콘솔을 설치 해야 함

Configuration Manager 통합 토폴로지로 MBAM을 설치 하는 경우 MBAM이 설치 될 컴퓨터에 Configuration Manager 콘솔을 설치 해야 합니다. [구성 관리자에서 MBAM을 사용 하 여 시작](getting-started---using-mbam-with-configuration-manager.md)하는 데 권장 되는 아키텍처를 사용 하는 경우 Configuration Manager 기본 사이트 서버에 mbam을 설치 합니다.

### Configuration Manager 통합 토폴로지의 새 설정 명령줄 매개 변수

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">명령줄 매개 변수</th>
<th align="left">설명</th>
<th align="left">예</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>MBAM이 설치 된 것과 동일한 Configuration Manager 사이트의 일부인 원격 SQL Server Reporting Services (SSRS) 서버에 Configuration Manager 보고서를 설치할 수 있도록 합니다. 값을 원격 SSRS 지점간 역할 서버의 정규화 된 도메인 이름으로 설정할 수 있습니다.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME ssrsServer =. m a c.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>기준, 컬렉션 및 구성 항목과 같은 다른 Configuration Manager 개체 없이 Configuration Manager 보고서만 설치할 수 있습니다.</p>
<div class="alert">
<strong>참고</strong><br/><p>이 매개 변수를 CM_REPORTS_COLLECTION_ID 매개 변수와 결합 해야 합니다.</p>
</div>
<div>

</div>
<p>유효한 매개 변수 값:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul>
<p>이 매개 변수를 CM_SSRS_REMOTE_SERVER_NAME 매개 변수와 결합 하 여 원격 SSRS 요점 역할 서버에만 보고서를 설치할 수 있습니다.</p>
<p>매개 변수를 설정 하지 않거나 False로 설정한 경우 MBAM 설정에서는 보고서를 포함 하 여 모든 Configuration Manager 개체를 설치 합니다.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = True</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>보고 준수 데이터를 표시할 컬렉션을 식별 하는 기존 컬렉션 ID입니다. 모든 컬렉션 ID를 지정할 수 있습니다. "MBAM 지원 컴퓨터" 컬렉션 ID를 사용할 필요는 없습니다.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = True</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### 셀프 서비스 포털 알림 텍스트를 설정 또는 해제 하는 기능

MBAM 2.0 SP1에서는 셀프 서비스 포털에서 알림 텍스트를 해제할 수 있습니다. 이전에는 기본적으로 표시 되는 알림 텍스트 이므로 해제할 수 없습니다.

**알림 텍스트를 해제 하려면**

1.  셀프 서비스 포털을 설치한 서버에서 IIS (인터넷 정보 서비스)를 열고 ** &gt; Microsoft BitLocker 관리 및 모니터링 &gt; SelfService &gt; 응용 프로그램 설정을**찾습니다.

2.  **이름** 열에서 **displaynotice**a를 선택 하 고 값을 **false**로 설정 합니다.

### 사용자에 게 셀프 서비스 포털 정보를 가리키는 HelpdeskText 문을 지역화 하는 기능

최종 사용자가 셀프 서비스 포털을 사용 하는 경우 추가 도움말을 가져오는 방법을 알려 주는 셀프 서비스 포털 "HelpdeskText" 문의 지역화 된 버전을 구성할 수 있습니다. 문에 대해 지역화 된 텍스트를 구성 하는 경우 다음 지침에 설명 된 대로 MBAM에는 지역화 버전이 표시 됩니다. MBAM이 지역화 된 버전을 찾지 못하면 **HelpdeskText** 매개 변수에 있는 값이 표시 됩니다.

**HelpdeskText 문의 지역화 된 버전을 표시 하려면**

1.  셀프 서비스 포털을 설치한 서버에서 IIS를 열고 ** &gt; Microsoft BitLocker 관리 및 모니터링 &gt; SelfService &gt; 응용 프로그램 설정을**찾습니다.

2.  **작업** 창에서 **추가** 를 클릭 하 여 **응용 프로그램 설정 추가** 대화 상자를 엽니다.

3.  **이름** 필드에 **HelpdeskText**\ _ &lt; *언어* &gt; 를 입력 &lt; *language* &gt; 합니다. 여기서 해당 언어는 텍스트에 적합 한 언어 코드입니다. 예를 들어 스페인어로 지역화 된 HelpdeskText 문을 만들려면 HelpdeskText \ _es 매개 변수에 이름을 name으로 표시 합니다. 사용할 수 있는 유효한 언어 코드 목록은 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947)를 참조 하세요.

4.  **값** 필드에 최종 사용자에 게 표시 하려는 지역화 된 텍스트를 입력 합니다.

### 셀프 서비스 포털 HelpdeskURL를 지역화 하는 기능

최종 사용자에 게 기본적으로 표시 되도록 자체 서비스 포털 HelpdeskURL의 지역화 된 버전을 구성할 수 있습니다. 다음 지침에 설명 된 바와 같이 지역화 된 버전을 만드는 경우 MBAM에서 지역화 된 버전을 찾고 표시 합니다. MBAM이 지역화 된 버전을 찾지 못하면 HelpDeskURL 매개 변수에 대해 구성 된 URL이 표시 됩니다.

**지역화 된 HelpdeskURL를 표시 하려면**

1.  셀프 서비스 포털을 설치한 서버에서 IIS를 열고 ** &gt; Microsoft BitLocker 관리 및 모니터링 &gt; SelfService &gt; 응용 프로그램 설정을**찾습니다.

2.  **작업** 창에서 **추가** 를 클릭 하 여 **응용 프로그램 설정 추가** 대화 상자를 엽니다.

3.  **이름** 필드에 **HelpdeskURL**\ _ &lt; *언어* &gt; 를 입력 &lt; *language* &gt; 합니다. 여기서 해당 언어는 해당 URL에 대 한 언어 코드입니다. 예를 들어 스페인어로 지역화 된 HelpdeskURL를 만들려면 매개 변수의 이름을 HelpdeskURL \ _es로 표시 합니다. 사용할 수 있는 유효한 언어 코드 목록은 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947)를 참조 하세요.

4.  **값** 필드에 최종 사용자에 게 표시 하려는 지역화 된 HelpdeskURL를 입력 합니다.

### 셀프 서비스 포털 알림 텍스트를 지역화 하는 기능

셀프 서비스 포털에서 기본적으로 최종 사용자에 게 표시 되도록 지역화 된 알림 텍스트를 구성할 수 있습니다. 알림 텍스트를 표시 하는 notice.txt 파일은 다음 루트 디렉터리에 있습니다.

&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

지역화 된 알림 텍스트를 표시 하려면 지역화 notice.txt 파일을 만들고 다음 디렉터리의 특정 언어 폴더 아래에 저장 합니다.

&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

MBAM은 다음 규칙에 따라 알림 텍스트를 표시 합니다.

-   적절 한 언어 폴더에서 지역화 된 notice.txt 파일을 만드는 경우 MBAM은 지역화 된 알림 텍스트를 표시 합니다.

-   MBAM이 notice.txt 파일의 지역화 된 버전을 찾지 못하면 기본 notice.txt 파일에 텍스트를 표시 합니다.

-   MBAM이 기본 notice.txt 파일을 찾지 못하면 셀프 서비스 포털에 기본 텍스트가 표시 됩니다.

**참고**  
최종 사용자의 브라우저가 해당 언어 하위 폴더 또는 notice.txt 없는 언어로 설정 된 경우에는 다음 루트 디렉터리의 notice.txt 파일에 있는 텍스트가 표시 됩니다.

&lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\



**지역화 된 notice.txt 파일을 만들려면**

1.  셀프 서비스 포털을 설치한 서버에서 &lt; *language* &gt; 다음 디렉터리에 언어 폴더를 만듭니다. 여기서 &lt; *언어* 는 &gt; 지역화 된 언어의 이름을 나타냅니다.

    &lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\

    **참고**  
    일부 언어 폴더가 이미 있으므로이를 만들 필요가 없을 수 있습니다. 언어 폴더를 만들어야 하는 경우 언어 폴더에 사용할 수 있는 유효한 이름 목록에 대 한 [NLS (국가별 언어 지원) API 참조](https://go.microsoft.com/fwlink/?LinkId=317947) 를 참조 하세요 &lt; *language* &gt; .



2.  지역화 된 알림 텍스트를 포함 하는 notice.txt 파일을 만듭니다.

3.  notice.txt 파일을 &lt; *언어* &gt; 폴더에 저장 합니다. 예를 들어 스페인어로 지역화 된 notice.txt 파일을 만들려면 다음 폴더에 지역화 된 notice.txt 파일을 저장 합니다.

    &lt;*Mbam 셀프 서비스 설치 디렉터리* &gt; \\Self 서비스 Website\\es-es

## MBAM 2.0 SP1으로 업그레이드


이전 버전의 MBAM에서 MBAM 2.0 SP1로 업그레이드할 수 있습니다.

### MBAM 인프라 업그레이드

다음과 같이 MBAM 서버 인프라를 mbam SP1로 업그레이드할 수 있습니다.

**수동 현재 위치 서버 대체**: 기존 Mbam 서버 인프라를 수동으로 제거한 다음 mbam 2.0 SP1 서버 인프라를 설치 해야 합니다. 업그레이드를 수행 하기 위해 데이터베이스를 제거할 필요는 없습니다. 대신 이전 버전의 MBAM이 생성 되는 기존 데이터베이스를 선택 합니다. MBAM 2.0 SP1 업그레이드 설치는 기존 데이터베이스를 MBAM 2.0 SP1로 마이그레이션합니다.

**분산 클라이언트 업그레이드**: 독립 실행형 mbam 토폴로지를 사용 하는 경우 mbam 2.0 SP1 서버 인프라를 설치한 후 Mbam 클라이언트를 점차적으로 업그레이드할 수 있습니다.

MBAM 서버 인프라를 업그레이드 하면 mbam 1.0 또는 2.0 클라이언트가 MBAM 2.0 SP1 서버에 성공적으로 보고 되지만 복구 데이터는 저장 되지만, 준수는 현재 설치 된 MBAM 클라이언트 버전에서 사용할 수 있는 정책에 따라 결정 됩니다. MBAM 2.0 SP1 정책에 대 한 보고 기능을 사용 하도록 설정 하려면 클라이언트 컴퓨터를 MBAM 2.0 SP1로 업그레이드 해야 합니다. 이전 클라이언트를 제거 하지 않고 MBAM 2.0 SP1 클라이언트로 클라이언트 컴퓨터를 업그레이드할 수 있으며, 클라이언트는 MBAM 2.0 SP1 정책에 따라 적용 하 고 보고 하기 시작 합니다.

MBAM 서버 업그레이드에 대 한 자세한 내용은 [이전 버전의 mbam에서 업그레이드](upgrading-from-previous-versions-of-mbam.md)를 참조 하세요.

### MBAM 클라이언트를 MBAM 2.0 SP1로 업그레이드

최종 사용자 컴퓨터를 MBAM 2.0 SP1 클라이언트로 업그레이드 하려면 각 클라이언트 컴퓨터에서 **MbamClientSetup.exe** 를 실행 합니다. 설치 관리자가 자동으로 MBAM 2.0 SP1 클라이언트로 클라이언트를 업데이트 합니다. 설치 후에는 클라이언트 컴퓨터를 다시 부팅할 필요가 없으며 mbam 2.0 SP1 클라이언트는 MBAM 2.0 SP1 정책에 대해 적용 하 고 보고 하기 시작 합니다.

구성 관리자에 MBAM을 사용 하는 경우 mbam 클라이언트 컴퓨터를 MBAM 2.0 SP1로 업그레이드 해야 합니다.

MBAM 클라이언트 컴퓨터를 업그레이드 하는 방법에 대 한 자세한 내용은 [이전 버전의 mbam에서 업그레이드](upgrading-from-previous-versions-of-mbam.md)를 참조 하세요.

## Configuration Manager에서 MBAM 2.0 SP1 설치 또는 업그레이드


이 섹션에서는 MBAM 2.0 SP1을 새 설치로 설치 하거나 이전의 MBAM 2.0 SP1 설치로 업그레이드할 때 요구 사항에 대해 설명 합니다.

### Configuration Manager에서 MBAM을 사용 하는 경우 MBAM 2.0 SP1을 설치 하는 데 필요한 파일

MBAM을 처음으로 설치 하 고 System Center Configuration Manager와 함께 MBAM 2.0 SP1을 사용 하는 경우, Configuration Manager에서 MBAM이 올바르게 작동 하도록 mof 파일을 만들거나 편집 해야 합니다.

-   **구성 .mof 파일**

    -   Configuration Manager 2007를 사용 하는 경우에는 항목에서 3 단계를 완료 하 여 configuration .mof 파일을 편집 해야 하며,이 항목 다음에 오는 **Configuration Manager 2007에서 MBAM을 사용 하는 2.0 경우**에만 구성 파일을 업데이트 합니다.

    -   System Center 2012 구성 관리자를 사용 하는 경우에는 [구성 .Mof 파일 편집](edit-the-configurationmof-file.md)의 지침에 따라 구성 .mof 파일을 편집 합니다.

-   **sms \ _def mof 파일** - [Sms \ _def 파일 만들기 또는 편집](create-or-edit-the-sms-defmof-file.md)의 지침을 따릅니다.

### MBAM 2.0 SP1로 업그레이드 하 고 Configuration Manager 2007에서 MBAM을 사용 하는 경우에는 구성 .mof 파일을 업데이트 합니다.

MBAM 2.0 SP1로 업그레이드 하는 경우 구성 관리자 2007에서 MBAM을 사용 하는 경우에는 MBAM 2.0 SP1이 올바르게 작동 하도록 구성 .mof 파일을 업데이트 해야 합니다.

**구성 .mof 파일을 업데이트 하려면 다음을 수행 합니다.**

1.  Configuration Manager 서버에서 Configuration .mof 파일의 위치로 이동 합니다.

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    기본 설치의 경우 설치 위치 는%systemdrive%\\Program Files (x86) \\Microsoft 구성 관리자입니다.

2.  구성 .mof 파일에 추가한 코드 블록을 검토 하 고 삭제 합니다. 코드 블록은 다음 단계에 표시 되는 것과 유사 합니다.

3.  다음 코드 블록을 복사한 다음이를 구성 .mof 파일에 추가 하 여 다음 필수 MBAM 클래스를 파일에 추가 합니다.

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### MBAM 2.0 SP1 번역

현재 MBAM 2.0 SP1은 다음 언어로 제공 됩니다.

-   영어 (미국) en-us-US
-   프랑스어 (프랑스) fr-fr
-   이탈리아어 (이탈리아) it
-   독일어 (독일) DE-DE
-   스페인어, 국제 정렬 (스페인-ES)
-   한국어 (대한민국) ko-kr-KR
-   일본어 (일본) ja-jp
-   포르투갈어 (브라질) pt-BR
-   러시아어 (러시아)의 기능
-   중국어 번체 zh-cn-hy 얕은 샘물 a
-   중국어 간체 zh-cn-CN

## MDOP 기술을 활용 하는 방법

MBAM 2.0 SP1은 Microsoft MDOP (데스크톱 최적화 팩)의 일부입니다. MDOP는 Microsoft 소프트웨어 보장의 일부입니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 [mdop를 가져오는 방법](https://go.microsoft.com/fwlink/?LinkId=322049) (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=322049) .

## 관련 항목

[MBAM 2.0 SP1 릴리스 정보](release-notes-for-mbam-20-sp1.md)









