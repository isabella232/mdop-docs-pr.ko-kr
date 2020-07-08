---
title: Windows PowerShell을 사용하여 고급 설정 구성
description: Windows PowerShell을 사용하여 고급 설정 구성
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827393"
---
# Windows PowerShell을 사용하여 고급 설정 구성


사용자가 만드는 MED-V 작업 영역 패키지에는 MED-V 작업 영역 패키지를 테스트 하 고 배포 하기 전에 편집할 수 있는 Windows PowerShell 스크립트 (ps1) 파일이 포함 되어 있습니다. 이 섹션에서는 MED-V 작업 영역을 배포 하기 전에 Windows PowerShell을 사용 하 여 MED-V 구성 설정을 관리 하는 데 도움이 되는 정보 및 지침을 제공 합니다.

## MED-V에 Windows PowerShell Cmdlet 사용


Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0에서 다음 Windows PowerShell cmdlet을 사용할 수 있습니다.

**새-MedvConfiguration**

**내보내기-MedvConfiguration**

**새 MedvWorkspace**

**내보내기-MedvWorkspace**

MED-V 용 Windows PowerShell cmdlet에 액세스 하려면 Windows PowerShell을 열고 다음 명령을 입력 하 여 MED-V 모듈을 가져옵니다.

``` syntax
Import-Module microsoft.medv
```

모듈을 가져온 후 표준 Windows PowerShell 도움말 명령, **매뉴얼** 또는 **도움말**을 사용 하 여 cmdlet에 대 한 인라인 도움말에 액세스할 수 있습니다. 예를 들어 사용할 수 있는 전체 매개 변수 목록을 비롯 하 여 **새 MedvConfiguration** cmdlet에 대 한 설명에 액세스 하려면 다음 명령을 입력 합니다.

``` syntax
get-help New-MedvConfiguration
```

특정 매개 변수에 대 한 도움말을 볼 수도 있습니다. 예를 들어 VmMemory 매개 변수에 대 한 도움말을 보려면 다음을 입력 합니다.

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

모든 MED-V 구성 설정 및 기본값 목록을 보려면 다음 명령을 입력 합니다.

``` syntax
New-MedvConfiguration -ForceDefaults
```

모든 MED-V 구성 설정과 현재 값의 목록을 보려면 다음 명령을 입력 합니다.

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## 사용자 지정 설정을 사용 하 여 MED-V 작업 영역 만들기


MED-V 작업 영역 포장기를 사용 하 여 MED-V 작업 영역 패키지를 성공적으로 만든 후에는 포장기 파일을 저장 하기 위해 지정한 폴더에 Windows PowerShell 스크립트가 생성 됩니다. 이 스크립트의 내용에는 편집할 수 있는 사용 가능한 일부 MED-V 구성 설정이 표시 됩니다.

이러한 단계를 따라 Windows PowerShell에서 스크립트를 사용자 지정한 다음이를 실행 하 여 새 설정으로 MED-V 작업 영역을 만들 수 있습니다.

**중요**  관리 자격 증명으로 Windows PowerShell을 실행 하 고 Windows PowerShell 실행 정책이 스크립트 실행을 허용 하는지 확인 합니다.

1.  MED-V 작업 영역 포장기에서 생성 한 Windows PowerShell 스크립트를 편집 하거나 원하는 구성 설정으로 새 스크립트를 작성 합니다.

2.  관리 자격 증명을 사용 하 여 Windows PowerShell을 실행 하 고 명령 프롬프트에서 다음 명령을 입력 합니다.

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    이 명령은 Windows PowerShell 스크립트를 실행 하 고 **새** med-v 작업 영역 cmdlet을 실행 하 여 새 med-v workspace 패키지를 생성 합니다. 새 포장기 파일은 MED-V 작업 영역 포장기 파일을 저장 하기 위해 원래 지정 된 폴더에 저장 됩니다. 이 cmdlet에 대 한 추가 도움말은 Windows PowerShell 도움말을 참조 하세요.

 

## 레지스트리 파일에 MED-V 구성 내보내기


MED-V 작업 영역이 설치 된 후 MED-V 구성 설정을 업데이트할 수 있습니다. **새-MedvConfiguration** cmdlet을 사용 하 여 변경 하려는 매개 변수를 지정 합니다. 예를 들어 가상 컴퓨터 메모리 설정을 변경 하는 레지스트리 파일을 만들려면 다음 명령을 입력 합니다.

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

호스트 컴퓨터에서 MED-V 작업 영역으로 결과 레지스트리 파일을 가져와 새 구성 설정을 적용할 수 있습니다.

## 관련 항목


[MED-V 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)

[MED-V 작업 영역 패키지 테스트 및 배포](test-and-deploy-the-med-v-workspace-package.md)

 

 





