---
title: System Center Configuration Manager 2012에서 UE-V 2. x 구성
description: System Center Configuration Manager 2012에서 UE-V 2. x 구성
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824408"
---
# System Center Configuration Manager 2012에서 UE-V 2. x 구성


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 또는 2.1 SP1과 필요한 기능을 설치한 후에는 UE-V를 구성 해야 합니다. UE-V 구성 팩은 관리자가 System Center Configuration Manager 2012 SP1 이상의 규정 준수 설정 기능을 사용 하 여 UE-V 및 Configuration Manager가 설치 된 사이트에서 일관 된 구성을 적용할 수 있는 방법을 제공 합니다.

## UE-V 구성 팩 지원 되는 기능


UE-V 구성 팩에는 다음 작업을 수행 하는 도구가 포함 되어 있습니다.

-   UE-V 설정 위치 템플릿 배포 기준을 만들거나 업데이트 합니다.

    -   등록 또는 등록이 취소 되도록 UE-V 템플릿 정의

    -   서식 파일이 추가 되거나 업데이트 될 때 UE-V 템플릿 구성 항목 및 초기 계획 업데이트

    -   표준 구성 항목 수정을 사용 하 여 UE-V 템플릿 배포 및 등록

-   이 설정을 설정 하거나 해제 하려면 UE-V 에이전트 정책 구성 항목을 만들거나 업데이트 합니다.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>최대 패키지 크기</p></td>
    <td align="left"><p>Windows 앱 동기화 사용/사용 안 함</p></td>
    <td align="left"><p>응용 프로그램 시작 시 동기화 대기</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>가져오기 지연 설정</p></td>
    <td align="left"><p>목록에 없는 Windows 앱 동기화</p></td>
    <td align="left"><p>로그온 할 때 동기화 대기</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>설정 가져오기 알림</p></td>
    <td align="left"><p>IT 연락처 URL</p></td>
    <td align="left"><p>동기화 시간 초과 대기</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>설정 저장소 경로</p></td>
    <td align="left"><p>설명 텍스트에 문의</p></td>
    <td align="left"><p>설정 서식 파일 카탈로그 경로</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>동기화 방법</p></td>
    <td align="left"><p>트레이 아이콘 사용</p></td>
    <td align="left"><p>UE-V agent 서비스 시작/중지</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sync 메서드</p></td>
    <td align="left"><p>첫 번째 사용 알림</p></td>
    <td align="left"><p>설정을 로밍할 Windows 앱 정의</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>동기화 시간 제한</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   UE-V가 실행 되 고 있는지 확인 하 여 준수 여부를 확인 합니다.

## UE-V 에이전트 정책 구성 항목 생성


모든 UE-V Agent 정책 및 구성은 UevAgentPolicyGenerator.exe 도구를 사용 하 여 생성 된 단일 구성 항목을 통해 배포 됩니다. 이 도구는 XML 구성 파일에서 원하는 구성을 읽고 컴퓨터를 준수 하도록 하는 데 필요한 검색 및 업데이트 관리 설정을 포함 하는 CI를 만듭니다.

UE-V Agent 정책 구성 항목 CAB 파일은 다음 매개 변수를 포함 하는 UevTemplateBaselineGenerator.exe 명령줄 도구를 사용 하 여 만듭니다.

-   사이트 &lt; 사이트 코드&gt;

-   PolicyName &lt; name &gt; 선택 사항: "Ue-v Agent 정책"이 없는 경우 기본값을

-   PolicyDescription &lt; description &gt; (선택 사항): 설명이 없는 경우 설명을 제공 합니다.

-   CabFilePath &lt; 구성 항목에 대 한 전체 경로입니다. CAB 파일&gt;

-   &lt;에이전트 구성 XML 파일의 configurationfile 전체 경로&gt;

**참고**  이 스크립트를 환경에서 실행할 수 있도록 PowerShell 실행 정책을 변경 해야 할 수 있습니다. Configuration Manager 콘솔에서 다음 단계를 수행 합니다.

1.  **관리 &gt; 클라이언트 설정 &gt; 속성** 선택

2.  **사용자 에이전트** 탭에서 **PowerShell 실행 정책을** **Bypass** 으로 설정 합니다.

<a href="" id="create"></a>**첫 번째 UE-V-V 정책 구성 항목 만들기**

1.  UE-V Config Pack 설치 디렉터리의 기본 설정 구성 파일을 ConfigMgr 관리 콘솔에 표시 되는 위치에 복사 합니다.

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    기본 구성 파일에는 다음 5 개 섹션이 포함 됩니다.

    <a href="" id="computer-policy"></a>**컴퓨터 정책**  
    모든 UE-V 컴퓨터 수준 설정 DesiredState 특성은 다음이 될 수 있습니다.

    -   레지스트리에 값이 할당 되도록 **설정**

    -   설정을 제거 하 여 **지우기**

    -   **관리 되지 않는** 경우 구성 항목이 현재 상태로 유지 됩니다.

    이 섹션에서는 줄을 제거 하지 마세요. 대신, Configuration Manager에서 현재 값 또는 기본값을 변경 하지 않도록 하려면 DesiredState를 ' 관리 되지 않음 '으로 설정 합니다.

    <a href="" id="currentcomputeruserpolicy"></a>**CurrentComputerUserPolicy**  
    모든 UE-V 사용자 수준 설정 이러한 항목은 사용자의 컴퓨터 설정 보다 우선 합니다. DesiredState 특성은 다음이 될 수 있습니다.

    -   레지스트리에 값이 할당 되도록 **설정**

    -   설정을 제거 하 여 **지우기**

    -   **관리 되지 않는** 경우 구성 항목이 현재 상태로 유지 됩니다.

    이 섹션에서는 줄을 제거 하지 마세요. 대신, Configuration Manager에서 현재 값 또는 기본값을 변경 하지 않도록 하려면 DesiredState를 ' 관리 되지 않음 '으로 설정 합니다.

    <a href="" id="services"></a>**서비스**  
    이 섹션의 항목은 서비스 작업을 제어 합니다. 기본 구성 파일에는 UevAgentService에 대 한 단일 항목이 포함 되어 있습니다. DesiredState 특성을 **실행** 또는 **중지**로 설정할 수 있습니다.

    <a href="" id="windows8appscomputerpolicy"></a>**Windows8AppsComputerPolicy**  
    모든 컴퓨터 수준 Windows 앱 동기화 설정 이 섹션에 나열 된 각 PackageFamilyName에는 DesiredState를 할당할 수 있습니다.

    -   설정을 로밍할 수 **있도록 설정 됨**

    -   설정을 로밍 하는 것을 방지 하려면 **사용 안 함**

    -   UE-V 컨트롤에서 항목을 제거 하도록 **선택 취소**

    PowerShell cmdlet GetAppxPackage를 사용 하 여 볼 수 있는 설치 된 Windows 앱의 목록을 기반으로이 섹션에 추가 줄을 추가할 수 있습니다.

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**Windows8AppsCurrentComputerUserPolicy**  
    개별 사용자에 대 한 컴퓨터 설정을 재정의 하는 설정이 있는 Windows8AppsComputerPolicy와 동일 합니다.

2.  원하는 상태 및 값 필드를 변경 하 여 구성 파일을 편집 합니다.

3.  ConfigMgr 관리 콘솔을 실행 하는 컴퓨터에서이 명령을 실행 합니다.

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  ConfigMgr 콘솔 또는 PowerShell Import를 사용 하 여 CAB 파일 가져오기-CMConfigurationItem

**UE-V 정책 구성 항목 업데이트**

1.  원하는 상태 및 값 필드를 변경 하 여 구성 파일을 편집 합니다.

2.  3 단계의 명령을 실행 하 여 [첫 번째 ue-v-V 정책 구성 항목 만들기](#create) PolicyName 매개 변수를 사용 하 여 이름을 변경한 경우 동일한 이름을 입력 했는지 확인 합니다.

3.  CAB 파일을 다시 가져옵니다. ConfigMgr의 버전이 업데이트 됩니다.

## UE-V 템플릿 기준선 생성
UE-V 템플릿은 여러 구성 항목이 포함 된 기준을 사용 하 여 배포 됩니다. 각 구성 항목에는 하나의 UE-V 템플릿을 설치 하는 데 필요한 검색 및 재구성 스크립트가 포함 되어 있습니다. 실제 UE-V 템플릿은 표준 구성 항목 기능을 사용 하 여 배포 하기 위한 업데이트 관리 스크립트에 포함 되어 있습니다.

UE-V 템플릿 기준선은 다음 매개 변수를 포함 하는 UevTemplateBaselineGenerator.exe 명령줄 도구를 사용 하 여 만듭니다.

-   사이트 &lt; 사이트 코드&gt;

-   BaselineName &lt; 이름 &gt; (선택 사항: "Ue-v Template 배포 기준"이 없는 경우 기본값 "으로 설정 됩니다.

-   BaselineDescription &lt; 설명 &gt; (선택 사항: 설명이 없는 경우 제공 됨)

-   서식 &lt; 파일 폴더 ue-v 템플릿 폴더&gt;

-   &lt;서식 파일 목록을 쉼표로 구분 하 여 등록&gt;

-   &lt;쉼표로 구분 된 서식 파일 목록 등록 취소&gt;

-   CabFilePath &lt; 생성할 기준선 CAB 파일의 전체 경로&gt;

결과는 구성 관리자로 가져올 준비가 된 기준 CAB 파일입니다. 나중에 서식 파일을 업데이트 하거나 추가 하는 경우 동일한 기준 이름을 사용 하 여 명령을 다시 실행할 수 있습니다. CAB 파일을 가져오면 변경 된 서식 파일의 CI 버전 업데이트 결과가 표시 됩니다.

### <a href="" id="create2"></a>첫 번째 UE-V 템플릿 기준선 만들기

1.  ConfigMgr 관리 콘솔을 실행 하는 컴퓨터에 표시 되는 안정적인 폴더 위치에 UE-V 서식 파일의 "마스터" 집합을 만듭니다. 서식 파일이 추가 되거나 업데이트 되 면이 폴더에 배포할 수 있는 위치가 제공 됩니다. 템플릿의 초기 목록은 UE-V가 설치 된 컴퓨터에서 복사할 수 있습니다. 기본 서식 파일 위치는 C:\\program files Files\\Microsoft 사용자 환경 Virtualization\\Templates.

2.  템플릿 생성기 명령을 추가할 수 있는 text.bat 파일을 만듭니다. 이는 선택 사항 이지만 명령 매개 변수를 저장 하는 경우 재생성 하기가 쉽습니다.

3.  베이스 라인을 생성 하는 .bat 파일에 명령 및 매개 변수를 추가 합니다. 다음 예제에서는 메모장과 계산기를 배포 하는 초기 계획을 만듭니다.

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  .Bat 파일을 실행 하 여 Configuration Manager로 가져오기 위해 준비 UevTemplateBaseline.cab 만들 수 있습니다.

### UE-V 템플릿 기준선 업데이트

템플릿 생성기는 템플릿 버전을 사용 하 여 템플릿을 업데이트 해야 하는지 여부를 결정 합니다. 서식 파일을 변경 하 고 버전을 업데이트 하는 경우 기준선 생성기는 마스터 폴더의 템플릿을 ConfigMgr 서버의 CI에 포함 된 템플릿과 비교 합니다. 차이점을 발견 하면 생성 된 기준 및 수정한 CI 버전이 업데이트 됩니다.

새 메모장 템플릿을 배포 하려면 다음 단계를 수행 합니다.

1.  템플릿의 버전 요소에 있는 템플릿 및 템플릿 버전을 업데이트 &lt; &gt; 합니다.

2.  마스터 서식 파일 디렉터리에 서식 파일을 복사 합니다.

3.  3 단계에서 만든 .bat 파일에서 [첫 번째 Ue-v 템플릿 기준선 만들기](#create2)로 명령을 실행 합니다.

4.  콘솔 또는 PowerShell 가져오기-CMBaseline를 사용 하 여 생성 된 CAB 파일을 ConfigMgr로 가져옵니다.

## UE-V 구성 팩 다운로드


Configuration Manager 2012 SP1 이상 버전에 대 한 UE-V 구성 팩을 [여기](https://go.microsoft.com/fwlink/?LinkId=317263)에서 다운로드할 수 있습니다.






## 관련 항목


[UE-V 2.x에 대한 구성 관리](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





