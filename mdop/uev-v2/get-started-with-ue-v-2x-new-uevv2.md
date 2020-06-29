---
title: UE-V 2.x 시작
description: UE-V 2.x 시작
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823288"
---
# UE-V 2.x 시작


이 가이드의 단계를 따라 작은 테스트 환경에서 Microsoft UE-V (User Experience Virtualization) 2.0 또는 2.1을 신속 하 게 배포 합니다. 이는 UE-V가 엔터프라이즈 내의 여러 장치에서 사용자 설정을 관리 하기 위한 올바른 솔루션 인지 여부를 확인 하는 데 도움이 됩니다.

**참고**  이 섹션의 정보는 설명서의 나머지 부분에 걸쳐 더 자세히 설명 되어 있습니다. 따라서 UE-V 2가 올바른 솔루션이 고이를 평가할 필요가 없는 경우에는 오른쪽으로 이동 하 여 [ue-v 2. x 배포를 준비할](prepare-a-ue-v-2x-deployment-new-uevv2.md)수 있습니다.

 

UE-V의 표준 설치는 기본 Microsoft Windows 및 Office 설정과 여러 Windows 앱 설정을 동기화 합니다. 테스트 환경에 네트워크 액세스를 공유 하는 두 명 이상의 사용자 컴퓨터가 포함 되어 있는지 확인 하 고 짧은 시간에 UE-V을 평가할 수 있습니다.

-   [1 단계: 선행 조건 확인](#step1): 지원 되는 구성에 대 한 세부 정보를 포함 하 여 사용자의 환경이 ue-v를 실행할 수 있는지 확인 합니다.

-   [2 단계: ue-v 2에 대 한 설정 저장소 위치 배포](#step2): 모든 ue-v 배포에는 동기화 된 설정 값이 포함 된 설정 패키지의 위치가 필요 합니다.

-   [3 단계:](#step3)ue-v를 사용 하 여 설정을 동기화 하려면 장치에 ue-v agent가 설치 되어 실행 중 이어야 합니다.

-   [4 단계:](#step4)ue-v agent가 설치 된 두 대의 컴퓨터에서 몇 가지 테스트를 실행 하 고 ue-v를 사용 하 여 작동 하는 방법을 확인 합니다.

그거에요! 이 단계를 수행 하 고 나면 엔터프라이즈에서 UE-V를 사용 하는 방법을 평가할 수 있게 됩니다.

**추가 평가:** 또한 [사용자 지정 응용 프로그램의 배포 ue-v](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)를 사용 하 여 설정을 동기화 하도록 일부 타사 및 lob (기간 업무) 응용 프로그램을 구성 하는 추가 단계를 수행할 수도 있습니다.

## <a href="" id="step1"></a>1 단계: 필수 구성 요소 확인


계속 하기 전에 UE-V를 실행 하기 위한 요구 사항이 환경에 포함 되어 있는지 확인 합니다.

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
<th align="left"><strong>운영 체제</strong></th>
<th align="left"><strong>버전</strong></th>
<th align="left"><strong>서비스 팩</strong></th>
<th align="left"><strong>시스템 아키텍처</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate, Enterprise 또는 Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4 이상</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>표준, 엔터프라이즈, 데이터 센터 또는 웹 서버</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4 이상</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>엔터프라이즈 또는 Pro</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 또는 Windows Server 2012 R2</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10, 1607 전 verison</p></td>
<td align="left"><p>엔터프라이즈 또는 Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32비트 또는 64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>표준 또는 데이터 센터</p></td>
<td align="left"><p>없음</p></td>
<td align="left"><p>64비트</p></td>
<td align="left"><p>Windows PowerShell 3.0 이상</p></td>
<td align="left"><p>.NET Framework 4.5</p></td>
</tr>
</tbody>
</table>

**참고:** Windows 10, 버전 1607, UE-V를 사용 하는 경우 [엔터프라이즈 용 windows 10](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) 에 포함 되어 있으며 더 이상 Microsoft 데스크톱 최적화 팩의 일부가 아닙니다.

또한

-   **MDOP 라이선스:** 이 기술은 MDOP (Microsoft 데스크톱 최적화 팩)의 일부입니다. 엔터프라이즈 고객은 Microsoft 소프트웨어 보증을 통해 MDOP를 받을 수 있습니다. Microsoft 소프트웨어 보증 및 MDOP 취득에 대 한 자세한 내용은 MDOP를 가져오는 방법 (을 참조 하세요 https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   설치할 컴퓨터에 대 한 **관리 자격 증명**

## <a href="" id="step2"></a>2 단계: UE-V 2에 대 한 설정 저장소 위치 배포


사용자 설정이 설정 패키지 파일에 저장 된 표준 네트워크 공유 인 설정 저장소 위치를 배포 해야 합니다. 설정 저장소 공유를 만들 때는이를 필요로 하는 사용자에 대 한 액세스를 제한 해야 합니다. [설정 저장소 위치 배포](https://technet.microsoft.com/library/dn458891.aspx#ssl) 더 자세한 정보를 제공 합니다.

**네트워크 공유 만들기**

1.  새 보안 그룹을 만들고 UE-V 사용자를 추가 합니다.

2.  UE-V 설정 패키지를 저장 하는 중앙 컴퓨터에서 새 폴더를 만든 다음이 폴더에 대 한 그룹 사용 권한을 사용 하 여 UE-V 사용자에 게 액세스 권한을 부여 합니다. UE-V를 지 원하는 관리자는이 공유 폴더에 대 한 사용 권한이 있어야 합니다.

3.  연결할 때 디렉터리를 만들 수 있는 권한을 UE-V users 사용자에 게 할당 합니다. 해당 디렉터리의 모든 하위 디렉터리에 대해 모든 권한을 부여 하 되, 위의 항목에 대 한 액세스를 차단 합니다.

    1.  설정 저장소 위치 폴더에 대해 다음 SMB (공유 수준 서버 메시지 블록) 사용 권한을 설정 합니다.

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>사용자 계정</strong></th>
        <th align="left"><strong>권장 되는 사용 권한</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>모두</p></td>
        <td align="left"><p>권한 없음</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>UE-V 사용자의 보안 그룹</p></td>
        <td align="left"><p>모든 권한</p></td>
        </tr>
        </tbody>
        </table>

         

    2.  설정 저장소 위치 폴더에 대해 다음 NTFS 파일 시스템 사용 권한을 설정 합니다.

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>사용자 계정</strong></th>
        <th align="left"><strong>권장 되는 사용 권한</strong></th>
        <th align="left"><strong>Folder</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>만든이/소유자</p></td>
        <td align="left"><p>모든 권한</p></td>
        <td align="left"><p>하위 폴더 및 파일만</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>UE-V 사용자의 보안 그룹</p></td>
        <td align="left"><p>폴더 목록/데이터 읽기, 폴더 만들기/데이터 추가</p></td>
        <td align="left"><p>이 폴더만</p></td>
        </tr>
        </tbody>
        </table>

         

**보안 참고:**

Windows Server 운영 체제를 실행 하는 컴퓨터에서 설정 저장소 공유를 만드는 경우 UE-V를 구성 하 여 로컬 관리자 그룹 또는 현재 사용자가 설정 패키지가 저장 된 폴더의 소유자 인지 확인 합니다. 이 추가 보안을 사용 하도록 설정 하려면 Windows Server 레지스트리 편집기에서 다음 설정을 지정 합니다.

1.  **"RepositoryOwnerCheckEnabled"** 이라는 **REG \ _DWORD** 레지스트리 키를 **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**에 추가 합니다.

2.  레지스트리 키 값을 *1*로 설정 합니다.

## <a href="" id="step3"></a>3 단계: UE-V 2 에이전트 배포


UE-V Agent는 사용자 컴퓨터와 장치 간에 응용 프로그램 및 Windows 설정을 동기화 합니다. 평가를 위해 테스트 환경에서 동일한 사용자에 속하는 적어도 두 대 이상의 컴퓨터에 에이전트를 설치 합니다.

명령줄에서 AgentSetup.exe 파일을 실행 하 여 UE-V 에이전트를 설치 합니다. 32 비트 및 64 비트 운영 체제 모두에 설치 합니다.

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

SettingsStoragePath 명령줄 매개 변수를 2 단계의 네트워크 공유로 지정 해야 합니다. [Ue-v Agent 배포는](https://technet.microsoft.com/library/dn458891.aspx#agent) 보다 자세한 정보를 제공 합니다.

## <a href="" id="step4"></a>4 단계: UE-V 2 평가판 배포 테스트


이제 UE-V 계산 배포에서 몇 가지 테스트를 실행 하 여 UE-V가 작동 하는 방식을 확인할 수 있습니다.

****

1.  첫 번째 컴퓨터 (컴퓨터 A)에 다음 중 하나 이상의 변경 작업을 수행 합니다.

    1.  Windows 데스크톱으로 열고 작업 표시줄을 창의 다른 위치로 이동 합니다.

    2.  기본 글꼴을 변경 합니다.

    3.  계산기를 열고 **공학용**으로 설정 합니다.

    4.  [Windows PowerShell 및 WMI를 사용 하 여 ue-v 2. x 설정 위치 템플릿을 관리 하는 방법](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)에 따라 windows 앱의 동작을 변경 합니다.

    5.  Microsoft 계정 설정 동기화 및 로밍 프로필을 사용 하지 않도록 설정 합니다.

2.  컴퓨터 A. 설정은 사용자가 응용 프로그램을 잠그거나 로그 오프 하거나 종료 하거나 동기화 공급자가 실행 될 때 (기본적으로 30 분 마다) UE-V 설정 패키지에 저장 됩니다.

3.  두 번째 컴퓨터 (컴퓨터 B)에 컴퓨터 A와 동일한 사용자로 로그인 합니다.

4.  Windows 데스크톱으로 열고 작업 표시줄 위치가 컴퓨터 A와 일치 하는지 확인 합니다. 기본 글꼴이 일치 하 고 계산기가 **공학용**으로 설정 되어 있는지 확인 합니다. 또한 Windows 앱에 대 한 변경 내용을 확인 합니다.

컴퓨터 B의 설정을 원래 컴퓨터의 설정으로 다시 변경할 수 있습니다. 그런 다음 컴퓨터 B를 로그 오프 하 고 컴퓨터 A에 로그인 하 여 변경 내용을 확인 합니다.

## 이 제품에 대 한 기타 리소스


-   [Microsoft UE-V (User Experience Virtualization) 2. x](index.md)

-   [UE-V 2. x 배포 준비](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [UE-V on-V 2. x 관리](administering-ue-v-2x-new-uevv2.md)

-   [UE-V 2. x 문제 해결](troubleshooting-ue-v-2x-both-uevv2.md)

-   [UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





