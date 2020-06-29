---
title: PowerShell 및 WMI를 사용하여 UE-V 1.0 설정 위치 템플릿 관리
description: PowerShell 및 WMI를 사용하여 UE-V 1.0 설정 위치 템플릿 관리
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812492"
---
# PowerShell 및 WMI를 사용하여 UE-V 1.0 설정 위치 템플릿 관리


Microsoft UE-V (User Experience Virtualization)는 사용자 환경 가상화에 의해 캡처되고 적용 되는 설정을 정의 하는 설정 위치 템플릿 (XML 파일)을 사용 합니다. UE-V는 표준 설정 위치 템플릿 집합을 포함 합니다. 또한 사용자 지정 설정 위치 템플릿을 만드는 데 사용할 수 있는 UE-V 생성기 도구가 포함 됩니다. 설정 위치 템플릿을 만들고 배포한 후에는 PowerShell 또는 WMI를 사용 하 여 해당 템플릿을 관리할 수 있습니다.

## WMI 및 PowerShell을 사용 하 여 설정 위치 템플릿 관리


UE-V의 WMI 및 PowerShell 기능에는 설정 위치 템플릿을 사용, 사용 안 함, 등록, 업데이트 및 등록 취소 하는 기능이 포함 됩니다. 이러한 기능을 사용 하 여 UE-V agent를 사용 하 여 서식 파일을 등록, 업데이트 또는 등록 취소 하는 프로세스를 자동화할 수 있습니다. 또한 WMI 및 PowerShell 명령을 사용 하 여 수동으로 템플릿을 등록할 수 있습니다. 이러한 기능을 전자 소프트웨어 배포 솔루션, 그룹 정책 또는 스크립트와 같은 다른 자동화 된 배포 방법과 함께 사용 하면 해당 프로세스를 더 자동화할 수 있습니다.

설정 위치 템플릿을 업데이트, 등록 또는 등록 취소 하려면 관리자 권한이 있어야 합니다. 템플릿을 사용 하거나 사용 하지 않도록 설정 하는 데는 관리자 권한이 필요 하지 않습니다.

**PowerShell을 사용 하 여 설정 위치 템플릿을 관리 하려면**

1.  관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다. **MICROSOFT Ue-v PowerShell** 모듈을 가져오려면 PowerShell 명령 프롬프트에서 다음 명령을 입력 합니다.

    ``` syntax
    Import-module UEV
    ```

2.  다음 PowerShell cmdlet을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>PowerShell 명령</strong></th>
    <th align="left"><strong>설명</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>가져오기-UevTemplate</p></td>
    <td align="left"><p>컴퓨터에 등록 된 모든 설정 위치 서식 파일을 나열 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>등록-UevTemplate</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 등록 합니다. 템플릿이 등록 되 면 UE-V는 등록 된 템플릿이 있는 컴퓨터 간에 템플릿에서 정의 된 설정을 동기화 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>등록 취소-UevTemplate</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다. 서식 파일이 등록 취소 되 면 UE-V는 더 이상 해당 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>업데이트 UevTemplate</p></td>
    <td align="left"><p>최신 버전의 서식 파일을 사용 하 여 설정 위치 템플릿을 업데이트 합니다. 새 서식 파일에는 기존 버전이 이전 버전 이어야 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>사용 안 함-UevTemplate</p></td>
    <td align="left"><p>컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 비활성화 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>사용-UevTemplate</p></td>
    <td align="left"><p>컴퓨터의 현재 사용자에 대 한 설정 위치 템플릿을 사용 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>테스트 UevTemplate</p></td>
    <td align="left"><p>지정 된 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

UE-V PowerShell 기능을 사용 하 여 엔터프라이즈에 배포 된 설정 서식 파일 그룹을 관리할 수 있습니다. PowerShell을 사용 하 여 서식 파일 그룹을 관리 하려면 다음을 실행 합니다.

**PowerShell을 사용 하 여 설정 위치 템플릿의 그룹을 관리 하려면**

1.  원하는 설정 위치 템플릿을 수정 하거나 업데이트 합니다.

2.  로컬 컴퓨터에서 액세스할 수 있는 폴더에 원하는 설정 위치 템플릿을 배포 합니다.

3.  로컬 컴퓨터에서 관리자 권한이 있는 Windows PowerShell 창을 엽니다.

4.  다음 명령을 입력 하 여 Microsoft UE-V PowerShell 모듈을 가져옵니다.

    ``` syntax
    Import-module UEV
    ```

5.  다음 명령을 입력 하 여 이전에 등록 된 모든 버전의 템플릿을 등록 취소 합니다.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    이렇게 하면 컴퓨터의 모든 활성 서식 파일이 등록 취소 됩니다.

6.  다음 명령을 입력 하 여 업데이트 된 서식 파일을 등록 합니다.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    이렇게 하면 지정 된 서식 파일 폴더에 있는 모든 설정 위치 템플릿이 등록 됩니다.

사용자 환경 가상화는 다음과 같은 WMI 명령 집합을 제공 합니다. 관리자는 이러한 인터페이스를 사용 하 여 Windows PowerShell에서 설정 위치 템플릿을 관리 하 고 템플릿 관리 작업을 자동화할 수 있습니다.

**WMI를 사용 하 여 설정 위치 템플릿을 관리 하려면**

1.  관리자 권한이 있는 계정을 사용 하 여 Windows PowerShell 창을 열 수 있습니다.

2.  다음 WMI 명령을 사용 하 여 UE-V 설정 위치 템플릿을 등록 하 고 관리 합니다.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>PowerShell 명령</strong></p></td>
    <td align="left"><p><strong>설명</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>WmiObject-네임 스페이스 root\Microsoft\UEV SettingsLocationTemplate | 선택-개체 TemplateId, TemplateName, 서식 버전, Enabled | 형식-테이블-Autosize</p></td>
    <td align="left"><p>컴퓨터에 대해 등록 된 모든 설정 위치 서식 파일을 나열 합니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name 레지스터-ArgumentList &lt; 템플릿 경로&gt;</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 등록 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; 템플릿 ID&gt;</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿의 등록을 취소 합니다. 서식 파일이 등록 취소 되 면 UE-V는 더 이상 해당 서식 파일에 정의 된 설정을 컴퓨터 간에 동기화 하지 않습니다.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; 템플릿 ID&gt;</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 사용 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; 템플릿 ID&gt;</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿 사용 안 함</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name 업데이트-ArgumentList &lt; 서식 파일 경로&gt;</p></td>
    <td align="left"><p>UE-V를 사용 하 여 설정 위치 템플릿을 업데이트 합니다. 새 서식 파일에는 기존 버전 보다 높은 버전이 있어야 합니다.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>WmiMethod-네임 스페이스 root\Microsoft\UEV-Class SettingsLocationTemplate-Name 유효성 검사-ArgumentList &lt; 서식 파일 경로&gt;</p></td>
    <td align="left"><p>지정 된 설정 위치 템플릿이 해당 XML 스키마를 따르는지 여부를 결정 합니다.</p></td>
    </tr>
    </tbody>
    </table>

     

**PowerShell을 사용 하 여 UE-V 에이전트를 배포 하는 방법**

1.  액세스 가능한 네트워크 공유에서 UE-V 설치 관리자 파일을 준비 합니다.

    **참고**  AgentSetup.exe를 사용 하 여 32 비트 및 64 비트 버전의 UE-V Agent를 모두 배포 합니다. 각 아키텍처에 대해 Windows Installer 파일 버전, AgentSetupx86.msi 및 AgentSetupx64.msi를 사용할 수 있습니다. 나중에 설치 파일을 사용 하 여 UE-V 에이전트를 제거 하려면 동일한 파일 형식을 사용 해야 합니다.

     

2.  다음 PowerShell 명령 중 하나를 사용 하 여 에이전트를 설치 합니다.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## 관련 항목


[PowerShell 및 WMI를 사용하여 UE-V 1.0 에이전트 및 패키지 관리](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[UE-V 1.0 관리](administering-ue-v-10.md)

[UE-V 1.0 작업](operations-for-ue-v-10.md)

 

 





