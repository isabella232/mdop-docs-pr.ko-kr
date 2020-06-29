---
title: UE-V 2. x에 대 한 회사 설정 센터 구성
description: UE-V 2. x에 대 한 회사 설정 센터 구성
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823293"
---
# UE-V 2. x에 대 한 회사 설정 센터 구성


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1에는 사용자가 동기화 할 설정을 관리 하는 데 도움이 되는 새 응용 프로그램 (예를 들어, 회사 설정 센터)이 포함 되어 있습니다. 회사 설정 센터는 UE-V Agent를 사용 하 여 설치 합니다. 사용자는 제어판, **시작** 메뉴 또는 **시작** 화면에서, ue-v 알림 영역 아이콘을 통해 회사 설정 센터에 액세스할 수 있습니다. 회사 설정 센터에서는 동기화 되는 설정을 표시 하 고 사용자가 UE-V의 동기화 상태를 볼 수 있도록 도와줍니다. 사용자는 회사 설정 센터를 사용 하 여 컴퓨터 간에 설정을 동기화 하는 응용 프로그램 또는 Windows 기능을 선택할 수 있습니다. **지금 동기화** 단추를 클릭 하 여 모든 설정을 즉시 동기화 할 수도 있습니다. 또한 관리자는 회사 설정 센터에 지원 링크를 포함할 수 있습니다.

## 회사 설정 센터 정보


회사 설정 센터 데스크톱 응용 프로그램은 사용자에 게 UE-V 설정 동기화에 대 한 정보를 제공 합니다. 회사 설정 센터에는 다양 한 방법으로 액세스할 수 있습니다.

-   알림 영역 아이콘 – **트레이 아이콘** 그룹 정책 설정 또는 Windows PowerShell 구성을 사용 하면 알림 영역에 ue-v 아이콘이 표시 됩니다. UE-V 아이콘을 클릭 하 여 회사 설정 센터를 엽니다.

    **참고**  다음 설정을 사용 하 여 알림 영역 아이콘을 사용 하지 않도록 설정할 수 있습니다.

    -   그룹 정책 설정: `Policy Tray Icon`

    -   Windows PowerShell cmdlet: `TrayIconEnabled`

    -   SystemCenter2012 ConfigurationManager에 대 한 UE-V 구성 팩의 구성 항목: `Tray icon enabled`

     

-   제어판의 응용 프로그램-제어판에서 **모양 및 개인**설정을 찾아본 다음, **회사 설정 센터**를 클릭 합니다.

-   첫 번째 사용 알림-비활성화 하지 않는 한, UE-V Agent가 사용자에 게 이제 UE-V agent가 컴퓨터에서 처음 실행 될 때 동기화를 설정 한다는 알림을 표시 합니다. 알림 대화 상자를 클릭 하 여 회사 설정 센터를 엽니다.

-   **시작** 화면 또는 **시작** 메뉴에는 회사 설정 센터 링크가 포함 되어 있습니다. 회사 설정 검색 센터에서 응용 프로그램을 찾습니다.

## 회사 설정 센터에서 지원 링크 구성


회사 설정 센터에는 사용자가 UE-V 설정 동기화 문제를 지원 하기 위해 클릭할 수 있는 하이퍼링크가 포함 될 수 있습니다. 이 링크는 웹 페이지나 mailto://의 http://같은 유효한 URL 프로토콜 (예: 전자 메일)을 열 수 있습니다. 지원 링크는 그룹 정책, Windows PowerShell 또는 System Center 2012 Configuration Manager UE-V 구성 팩을 사용 하 여 구성할 수 있습니다.

**회사 설정 센터 지원 링크를 구성 하는 방법**

1.  다음과 같이 원하는 관리 도구를 엽니다.

    -   **그룹 정책** -아직 [MDOP 관리 템플릿에서](https://go.microsoft.com/fwlink/p/?LinkId=393941)ue-v 2에 대 한 ADMX 서식 파일을 다운로드 하지 않은 경우이 작업을 수행 합니다.

    -   **Windows powershell** – ue-v agent가 설치 된 컴퓨터에서 **windows powershell**을 엽니다. Windows PowerShell을 사용 하 여 UE-V를 관리 하는 방법에 대 한 자세한 내용은 [Windows powershell 및 WMI에서 ue-v 2. x 관리](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)를 참조 하세요.

    -   **System Center 2012 MICROSOFT ue-v (User Experience Virtualization) 용 구성 팩** -Ue-v 구성 팩을 가져오고 구성 팩 문서를 따라 구성 항목을 만듭니다. UE-V 구성 팩에 대 한 자세한 내용은 [System Center Configuration Manager 2012에서 ue-v 2. x 구성을](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)참조 하세요.

2.  다음 정책에 대 한 설정을 편집 합니다.

    -   **It 담당자에 게 연결 텍스트** -이 설정은 회사 설정 센터에 있는 연락처 URL 하이퍼링크의 텍스트를 지정 합니다. 이 설정을 사용 하면 회사 설정 센터에 연락처 URL에 대 한 링크에 지정 된 텍스트가 표시 됩니다.

        -   그룹 정책 설정: `Contact IT Link Text`

        -   Windows PowerShell cmdlet: `ContactITDescription`

        -   구성 팩 구성 항목: `IT contact descriptive text`

    -   **IT URL에 문의** -이 설정은 전자 메일의 웹 페이지 또는 mailto://에 대 한 http://같은 유효한 URL 프로토콜에서 회사 설정 센터의 연락처 링크에 대 한 URL을 지정 합니다.

        -   그룹 정책 설정: `Contact IT URL`

        -   Windows PowerShell cmdlet: `ContactITUrl`

        -   구성 팩 구성 항목: `IT contact URL`

3.  관리 도구를 사용 하 여 사용자의 컴퓨터에 설정을 배포 합니다.






 

 





