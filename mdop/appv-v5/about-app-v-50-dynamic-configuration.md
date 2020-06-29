---
title: App-V 5.0 동적 구성 정보
description: App-V 5.0 동적 구성 정보
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815033"
---
# App-V 5.0 동적 구성 정보


동적 구성을 사용 하 여 사용자의 App-v 5.0 패키지를 사용자 지정할 수 있습니다. 다음 정보를 사용 하 여 기존 동적 구성 파일을 만들거나 편집 합니다.

동적 구성 파일을 편집 하는 경우 사용자 또는 그룹에 대해 App-v 5.0 패키지가 실행 되는 방법을 사용자 지정할 수 있습니다. 이렇게 하면 원하는 설정을 사용 하 여 패키지를 다시 시퀀싱 해야 하는 것을 제거 하 여 더 편리한 방법으로 패키지를 사용자 지정할 수 있으며 패키지 콘텐츠 및 사용자 지정 설정을 독립적으로 유지 하는 방법을 제공할 수 있습니다.

## 고급: 동적 구성


가상 응용 프로그램 패키지에는 패키지에 대 한 모든 핵심 정보를 제공 하는 매니페스트가 포함 되어 있습니다. 이 정보에는 패키지 설정의 기본값이 포함 되며 추가 사용자 지정 없이 가장 기본적인 양식의 설정이 결정 됩니다. 특정 사용자 또는 그룹에 대해 이러한 기본값을 조정 하려는 경우 다음 파일을 만들고 편집할 수 있습니다.

-   사용자 구성 파일

-   배포 구성 파일

이전의 .xml 파일은 패키지 설정을 지정 하 고 패키지에 직접적인 영향을 주지 않고 패키지를 사용자 지정할 수 있도록 허용 합니다. 패키지를 만들 때 시퀀서는 패키지 매니페스트 데이터를 사용 하 여 기본 배포 및 사용자 구성 파일을 자동으로 생성 합니다. 따라서 이러한 자동으로 생성 되는 구성 파일에는 패키지가 시퀀싱 중에 구성 되는 방법으로 innately 되는 기본 설정이 반영 됩니다. Sequencer에서 생성 된 형식의 패키지에 이러한 구성 파일을 적용 하는 경우 패키지는 해당 매니페스트에 제공 된 것과 동일한 기본 설정을 갖게 됩니다. 이렇게 하면 기본 설정을 변경 해야 하는 경우 패키지 관련 서식 파일을 통해 시작할 수 있습니다.

**참고**  다음 정보는 특정 사용자 또는 그룹 요구 사항을 충족 하도록 패키지를 사용자 지정 하는 시퀀서 생성 구성 파일을 수정 하는 데에만 사용할 수 있습니다.

 

### 동적 구성 파일 내용

구성 파일의 모든 추가, 삭제 및 업데이트는 패키지의 매니페스트 정보에 지정 된 기본값과 관련 하 여 수행 해야 합니다. 다음 표를 검토 합니다.

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 구성 .xml 파일</p></td>
</tr>
<tr class="even">
<td align="left"><p>배포 구성 .xml 파일</p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지 매니페스트</p></td>
</tr>
</tbody>
</table>

 

앞의 표는 파일을 읽는 방법을 나타냅니다. 첫 번째 항목은 마지막으로 읽을 항목을 나타내므로 콘텐츠의 우선 순위를 갖습니다. 따라서 모든 패키지는 기본적으로 패키지 매니페스트의 기본 설정을 포함 하 고 제공 합니다. 사용자 지정 설정이 있는 배포 구성 xml 파일이 적용 되는 경우 패키지 매니페스트 기본값이 재정의 됩니다. 사용자 지정 설정을 사용 하는 사용자 구성 xml 파일이 그 이전에 적용 되는 경우 배포 구성과 패키지 매니페스트 기본값이 모두 재정의 됩니다.

다음 목록에는 두 가지 파일 형식에 대 한 자세한 정보가 표시 됩니다.

-   **UserConfig (사용자 구성 파일)** -패키지에 대 한 사용자 지정 설정을 지정 하거나 수정할 수 있습니다. 이러한 설정은 패키지가 App-v 5.0 클라이언트를 실행 하는 컴퓨터에 배포 되는 경우 특정 사용자에 게 적용 됩니다.

-   **배포 구성 파일 (DeploymentConfig)** – 패키지에 대 한 기본 설정을 지정 하거나 수정할 수 있습니다. 이러한 설정은 앱-V 5.0 클라이언트를 실행 하는 컴퓨터에 패키지를 배포할 때 모든 사용자에 게 적용 됩니다.

컴퓨터에서 특정 사용자 집합의 패키지에 대 한 설정을 사용자 지정 하거나 HKCU와 같은 로컬 사용자 위치에 적용 되는 변경 작업을 수행 하려면 UserConfig 파일을 사용 해야 합니다. 컴퓨터의 모든 사용자에 대 한 패키지의 기본 설정을 수정 하거나 HKEY \ _LOCAL \ _MACHINE 및 모든 사용자 폴더와 같은 전역 위치에 적용 되는 변경 내용을 만들려면 DeploymentConfig 파일을 사용 해야 합니다.

UserConfig 파일은 클라이언트의 다른 사용자에 게 영향을 주지 않고 단일 사용자에 게 적용할 수 있는 구성 설정을 제공 합니다.

-   사용자 당 네이티브 시스템으로 통합할 확장:-바로 가기, 파일 형식 연결, URL 프로토콜, AppPaths, 소프트웨어 클라이언트, COM

-   가상 하위 시스템:-응용 프로그램 개체, 환경 변수, 레지스트리 수정, 서비스 및 글꼴

-   스크립트 (사용자 컨텍스트만)

-   기관 관리 (App-v 4.6를 사용 하 여 패키지 공존을 제어 하는 경우)

배포 구성 파일은 컴퓨터 컨텍스트에 따라 하나씩, 위의 UserConfig 목록에 나열 된 것과 동일한 기능을 제공 하는 사용자 컨텍스트에 상대적인 1 개의 섹션으로 구성 설정을 제공 합니다.

-   위의 모든 UserConfig 설정

-   모든 사용자에 대해 전역 으로만 적용 될 수 있는 확장

-   전역 컴퓨터 위치에 대해 구성할 수 있는 가상 하위 시스템 (예: 레지스트리)

-   제품 원본 URL

-   스크립트 (컴퓨터 컨텍스트만 해당)

-   하위 프로세스를 종료 하는 컨트롤

### 파일 구조

App-v 5.0 동적 구성 파일의 구조는 다음 섹션에서 설명 합니다.

### 동적 사용자 구성 파일

**Header** -동적 사용자 구성 파일의 헤더는 다음과 같습니다.

&lt;? xml 버전 = "1.0" 인코딩 = "utf-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> = "

**PackageId** 는 매니페스트 파일에 있는 것과 동일한 값입니다.

**본문** -동적 사용자 구성 파일의 본문에는 매니페스트 파일에 정의 된 모든 앱 확장 지점 및 가상 응용 프로그램을 구성 하는 데 사용할 수 있는 정보가 포함 됩니다. 본문에는 네 개의 하위 섹션이 허용 됩니다.

1. **응용 프로그램** -패키지 내의 매니페스트 파일에 포함 된 모든 앱-확장은 응용 프로그램 ID를 사용 하 여 할당 되며,이는 매니페스트 파일에도 정의 됩니다. 이를 통해 패키지 내에서 지정 된 응용 프로그램의 모든 확장을 사용 하거나 사용 하지 않도록 설정할 수 있습니다. **응용 프로그램 ID** 가 매니페스트 파일에 있어야 하며, 그렇지 않은 경우 무시 됩니다.

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> = "

   &lt;응용 프로그램&gt;

   &lt;정책에 새 응용 프로그램을 정의할 수!--. AppV 클라이언트가 매니페스트 파일에 없는 응용 프로그램 ID를 무시 합니다.&gt;

   &lt;Application Id = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/응용 프로그램&gt;

   …

   &lt;/UserConfiguration&gt;

2. **하위 시스템** -appextensions 및 기타 하위 시스템은 하위 시스템 아래에 노드로 정렬 됩니다 &lt; &gt; .

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> = "

   &lt;시스템과&gt;

   ..

   &lt;/Subsystems 시스템&gt;

   ..

   &lt;/UserConfiguration&gt;

   "**사용**" 특성을 사용 하 여 각 하위 시스템을 사용 하거나 사용 하지 않도록 설정할 수 있습니다. 다음은 다양 한 하위 시스템 및 사용 샘플입니다.

   **번호**

   일부 하위 시스템 (확장 하위 시스템) 컨트롤 확장 해당 하위 시스템:-바로 가기, 파일 형식 연결, URL 프로토콜, AppPaths, 소프트웨어 클라이언트 및 COM

   확장 하위 시스템은 콘텐츠와 별개로 사용 하거나 사용 하지 않도록 설정할 수 있습니다.  따라서 바로 가기 키를 사용 하도록 설정 하면 클라이언트가 기본적으로 매니페스트에 포함 된 바로 가기를 사용 하 게 됩니다. 각 확장 하위 시스템에는 확장 노드가 포함 될 수 있습니다 &lt; &gt; . 이 자식 요소가 있으면 클라이언트는 해당 하위 시스템의 매니페스트 파일에 있는 콘텐츠를 무시 하 고 구성 파일의 콘텐츠만 사용 합니다.

   바로 가기 하위 시스템을 사용 하는 예:

   1.  사용자가 동적 또는 배포 구성 파일 중 하나에서이를 정의한 경우:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  사용자가 다음만 정의한 경우:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  사용자가 다음을 정의 하는 경우

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   매니페스트 내의 모든 바로 가기는 계속 무시 됩니다. 통합 된 바로 가기가 제공 되지 않습니다.

   지원 되는 확장 하위 시스템은 다음과 같습니다.

   **바로 가기 키:** 이 컨트롤은 로컬 시스템에 통합 되는 바로 가기 키입니다. 다음은 두 개의 바로 가기가 포함 된 샘플입니다.

   &lt;시스템과&gt;

   &lt;바로 가기 사용 = "true"&gt;

     &lt;Extensions&gt;

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     &lt;/확장&gt;

     &lt;확장 범주 = "AppV 바로 가기"&gt;

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     &lt;/확장&gt;

    &lt;/확장&gt;

   &lt;/Shortcuts 가기 키&gt;

   **파일 형식 연결:** 파일 형식과 프로그램을 연결 하 여 상황에 맞는 메뉴 설정 및 기본으로 열기 (MIME 형식은이 susbsystem를 사용 하 여 설정할 수도 있습니다.) 샘플 파일 형식 연결이 아래에 있습니다.

   &lt;Fil과 Association 사용 = "true"&gt;

   &lt;Extensions&gt;

     &lt;확장 범주 = "AppV. 연결"&gt;

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      &lt;/확장&gt;

     &lt;/확장&gt;

     &lt;/Filassociation 연결&gt;

   **URL 프로토콜**: 이렇게 하면 클라이언트 컴퓨터의 로컬 레지스트리에 통합 된 url 프로토콜 (예: "mailto:")이 제어 됩니다.

   &lt;URLProtocols 사용 = "true"&gt;

   &lt;Extensions&gt;

   &lt;확장 범주 = "AppV (URLProtocol)"&gt;

   &lt;URLProtocol&gt;

     &lt;&gt;Mailto &lt; /name 이름&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /editflags&gt;

     &lt;설명은&gt;

     &lt;AppUserModelId&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;정보&gt;

   &lt;원본 필터/&gt;

     &lt;ShellFolder/&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;지닌&gt;

     &lt;ShellCommands&gt;

     &lt;DefaultCommand &gt; 열기 &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationid&gt;

     &lt;&gt;개방형 &lt; /name 이름&gt;

     &lt;명령줄 &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. 참고/m "%1" &lt; /명령줄&gt;

     &lt;DropTargetClassId/&gt;

     &lt;인&gt;

     &lt;확장 &gt; 0 &lt; /확장&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler/&gt;

     &lt;Application &gt; contosomail &lt; /Application&gt;

     &lt;항목 &gt; shellsystem &lt; /topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /Ifexec&gt;

     &lt;DdeCommand &gt; \ [setforeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/확장&gt;

     &lt;/확장&gt;

     &lt;/URLProtocols&gt;

   **소프트웨어 클라이언트**: 앱을 전자 메일 클라이언트, 뉴스 읽기 프로그램, 미디어 플레이어로 등록 하 고, 프로그램 액세스 및 컴퓨터 기본값 UI에서 앱을 볼 수 있도록 합니다. 대부분의 경우이 기능을 활성화 및 비활성화 하기만 하면 됩니다. 또한 해당 클라이언트를 제외한 다른 클라이언트가 아직 사용 하도록 설정 하려는 경우에만 전자 메일 클라이언트를 사용 하도록 설정 하 고 사용 하지 않도록 설정할 수 있습니다.

   &lt;사용할 수 있는 \Clients = "true"&gt;

     &lt;ClientConfiguration EmailEnabled = "false"/&gt;

   &lt;/Re\클라이언트&gt;

   AppPaths:-예를 들어 contoso.exe 응용 프로그램이 apppaths 이름 "myapp"로 등록 된 경우 실행 메뉴 아래에 "myapp"를 입력할 수 있으며 contoso.exe이 열립니다.

   &lt;AppPaths 사용 = "true"&gt;

   &lt;Extensions&gt;

   &lt;확장 범주 = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationid&gt;

     &lt;이름 &gt;contosomail.exe&lt; /name&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /Applicationpath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl/&gt;

   &lt;/AppPath&gt;

   &lt;/확장&gt;

   &lt;/확장&gt;

   &lt;/AppPaths&gt;

   **COM**: 응용 프로그램에서 로컬 COM 서버를 등록할 수 있습니다. 모드는 통합, 격리 또는 꺼짐이 될 수 있습니다. Isol.

   &lt;COM 모드 = "격리 됨"/&gt;

   **기타 설정**:

   확장 외에도 다른 하위 시스템을 사용 하거나 사용 하지 않도록 설정 하거나 편집할 수 있습니다.

   **가상 커널 개체**:

   &lt;사용할 수 있는 개체 = "false"/&gt;

   **가상 레지스트리**: HKCU 내의 가상 레지스트리에서 레지스트리를 설정 하려는 경우 사용 됩니다.

   &lt;Registry 사용 = "true"&gt;

   &lt;시&gt;

   &lt;키 경로 = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;값 형식 = "REG \ _SZ" Name = "Bar" Data = "NewValue"/&gt;

    &lt;/Ckey&gt;

     &lt;키 경로 = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;삭제&gt;

     &lt;/Registry&gt;

   **가상 파일 시스템**

         &lt;FileSystem Enabled="true" /&gt;

   **가상 글꼴**

         &lt;Fonts Enabled="false" /&gt;

   **가상 환경 변수**

   &lt;사용할 수 있는 환경 변수 = "true"&gt;

   &lt;시&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **가상 서비스**

         &lt;Services Enabled="false" /&gt;

3. **Userscripts** – 스크립트를 사용 하 여 가상 환경을 설정 또는 변경 하거나, 응용 프로그램을 실행 하기 전에 배포 또는 제거 시 스크립트를 실행 하거나, 응용 프로그램을 종료 한 후 환경을 "정리" 하는 데 사용할 수 있습니다. 샘플 스크립트를 보려면 sequencer에서 출력 하는 샘플 사용자 구성 파일을 참조 하세요. 아래 스크립트 섹션에서는 사용할 수 있는 다양 한 트리거에 대 한 자세한 정보를 제공 합니다.

4. **ManagingAuthority** – 패키지의 2 버전이 앱-v 4.6에 배포 되 고 다른 하나는 app-v 5.0에 배포 된 동일한 컴퓨터에 공존할 때 사용할 수 있습니다. App-v vNext를 사용 하 여 명명 된 패키지에 대 한 앱-V 4.6 확장 지점을 허용 하려면 UserConfig 파일에 다음을 입력 합니다 (여기서 PackageName는 App-v 4.6의 패키지 GUID).

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-acef-76fc5297fe81"/&gt;

### 동적 배포 구성 파일

**헤더** -배포 구성 파일의 헤더는 다음과 같습니다.

&lt;? xml 버전 = "1.0" 인코딩 = "utf-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> = "

**PackageId** 는 매니페스트 파일에 있는 것과 동일한 값입니다.

**본문** -배포 구성 파일의 본문에는 다음 두 가지 섹션이 포함 됩니다.

-   사용자 구성 섹션-이전 섹션에서 설명한 사용자 구성 파일과 동일한 콘텐츠를 허용 합니다. 패키지가 사용자에 게 게시 되 면이 섹션의 모든 appextensions 구성 설정이 사용자 구성 파일을 제공 하지 않는 한 패키지 내의 매니페스트에 해당 하는 설정 보다 우선 합니다. UserConfig 파일도 함께 제공 하는 경우 배포 구성 파일의 사용자 설정 대신 사용 됩니다. 패키지가 전역으로 게시 되는 경우 배포 구성 파일의 콘텐츠만 매니페스트와 조합 하 여 사용 됩니다.

-   컴퓨터 구성 섹션 – 컴퓨터의 특정 사용자가 아닌 전체 컴퓨터에 대해서만 구성할 수 있는 정보가 포함 됩니다. 예를 들어 HKEY \ _LOCAL \ _MACHINE VFS의 레지스트리 키입니다.

&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> = "

&lt;UserConfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**사용자 구성** -배포 구성 파일의 사용자 구성 섹션에 제공 되는 설정에 대 한 자세한 내용은 이전의 **동적 사용자 구성 파일** 섹션을 사용 합니다.

컴퓨터 구성-배포 구성 파일의 컴퓨터 구성 섹션은 컴퓨터의 특정 사용자가 아닌 전체 컴퓨터에 대해서만 설정할 수 있는 정보를 구성 하는 데 사용 됩니다. 예를 들어 HKEY \ _LOCAL \ _MACHINE 가상 레지스트리의 레지스트리 키입니다. 이 요소 아래에는 네 개의 하위 섹션이 허용 됩니다.

1.  **하위 시스템** -appextensions 및 기타 하위 시스템은 하위 시스템 아래에 노드로 정렬 됩니다 &lt; &gt; .

    &lt;MachineConfiguration&gt;

      &lt;시스템과&gt;

      ..

      &lt;/Subsystems 시스템&gt;

    ..

    &lt;/MachineConfiguration&gt;

    다음 섹션에는 다양 한 하위 시스템 및 사용 샘플이 표시 됩니다.

    **확장명**:

    일부 하위 시스템 (확장 하위 시스템)은 모든 사용자 에게만 적용 되는 확장을 제어 합니다. 하위 시스템은 응용 프로그램 기능입니다. 이는 모든 사용자에 게 적용 될 수 있으므로 이러한 유형의 확장을 로컬 시스템에 통합 하려면 패키지를 전역으로 게시 해야 합니다. 사용자 구성의 확장에 적용 되는 컨트롤과 설정에 대 한 규칙도 MachineConfiguration 섹션에도 적용 됩니다.

    **응용 프로그램 기능**: windows 운영 체제 인터페이스의 기본 프로그램에서 사용 됩니다. 특정 windows MIME 형식을 열 수 있는 경우에 따라 응용 프로그램에서 특정 파일 확장명을 시작 메뉴 인터넷 브라우저 슬롯의 contender으로 등록할 수 있습니다.또한이 확장에서는 가상 응용 프로그램을 기본 프로그램 설정 UI에 표시 합니다.

    &lt;ApplicationCapabilities 사용 = "true"&gt;

      &lt;Extensions&gt;

       &lt;확장 범주 = "AppV Capabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;CapabilityGroup&gt;

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/확장&gt;

    &lt;/확장&gt;

    &lt;/ApplicationCapabilities&gt;

    **기타 설정**:

    확장 외에도 다른 하위 시스템을 편집할 수 있습니다.

    **컴퓨터 전체 가상 레지스트리**: HKEY \ _Local \에서 가상 레지스트리의 레지스트리 키를 설정 하려는 경우 사용 됩니다. _Machine

    &lt;레지스트리&gt;

    &lt;시&gt;

      &lt;키 경로 = "\\REGISTRY\\Machine\\Software\\ABC"&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Ckey&gt;

      &lt;키 경로 = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;삭제&gt;

    &lt;/Registry&gt;

    **컴퓨터 규모의 가상 커널 개체**

    &lt;나타내는&gt;

    &lt;NotIsolate&gt;

       &lt;개체 이름 = "testObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/개체&gt;

2.  **제품 원본 Urloptout**: 패키지에 대 한 URL을 PackageSourceRoot를 통해 전역적으로 수정할 수 있는지 여부를 나타냅니다 (지점 시나리오 지원). 기본값은 false이 고, 다음 시작 시 설정 변경 내용이 적용 됩니다.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;제품 원본 Urloptout 사용 = "true"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** – 배포, 게시 또는 제거 시에 스크립트를 실행 하도록 패키지를 구성할 수 있습니다. 샘플 스크립트를 보려면 sequencer에서 생성 된 샘플 배포 구성 파일을 참조 하세요. 아래 스크립트 섹션에서는 사용할 수 있는 다양 한 트리거에 대 한 자세한 정보를 제공 합니다.

4.  **TerminateChildProcess**:-응용 프로그램 실행 파일을 지정할 수 있으며,이를 통해 해당 자식 프로세스가 종료 될 경우 해당 프로세스가 종료 됩니다.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### 스크립트

다음 표에서는 다양 한 스크립트 이벤트 및이를 실행할 수 있는 컨텍스트에 대해 설명 합니다.

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
<th align="left">스크립트 실행 시간</th>
<th align="left">배포 구성에서 지정할 수 있음</th>
<th align="left">사용자 구성에서 지정할 수 있음</th>
<th align="left">패키지의 가상 환경에서 실행할 수 있습니다.</th>
<th align="left">특정 응용 프로그램의 컨텍스트에서 실행할 수 있습니다.</th>
<th align="left">시스템/사용자 컨텍스트에서 실행: (배포 구성, 사용자 구성)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(시스템, 해당 없음)</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(시스템, 사용자)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지 Unpackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(시스템, 사용자)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(시스템, 해당 없음)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(사용자, 사용자)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(사용자, 사용자)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(사용자, 사용자)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(사용자, 사용자)</p></td>
</tr>
</tbody>
</table>

 

### 앱-V 5.0 매니페스트 파일을 사용 하 여 동적 구성 파일 만들기

수동으로 다음 세 가지 방법 중 하나를 사용 하 여 동적 구성 파일을 만들 수 있습니다. 앱 V 5.0 관리 콘솔을 사용 하거나 패키지를 시퀀싱 하 여 2 개의 샘플 파일을 사용 하 여 생성 됩니다.

App-v 5.0 관리 콘솔을 사용 하 여 파일을 만드는 방법에 대 한 자세한 내용은 [app-v 5.0 관리 콘솔을 사용 하 여 사용자 지정 구성 파일을 만드는 방법](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)을 참조 하세요.

파일을 수동으로 만들려면 이전 섹션의 위의 정보를 단일 파일로 결합할 수 있습니다. Sequencer에서 생성 된 파일을 사용 하는 것이 좋습니다.






## 관련 항목


[PowerShell을 사용하여 배포 구성 파일을 적용하는 방법](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[App-V 5.0 작업](operations-for-app-v-50.md)

 

 





