---
title: 앱-V 5.1 동적 구성 정보
description: 동적 구성을 사용 하 여 사용자의 App-v 5.1 패키지를 사용자 지정할 수 있습니다. 다음 정보를 사용 하 여 기존 동적 구성 파일을 만들거나 편집 합니다.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814963"
---
# 앱-V 5.1 동적 구성 정보 
동적 구성을 사용 하 여 동적 구성 파일을 편집 하 여 사용자 또는 그룹에 대해 App-v 5.1 패키지를 실행 하는 방법을 사용자 지정할 수 있습니다. 패키지 사용자 지정은 원하는 설정을 사용 하 여 패키지를 resequence 필요가 없습니다.  또한 패키지 콘텐츠 및 사용자 지정 설정을 독립적으로 유지 하는 방법을 제공 합니다.

가상 응용 프로그램 패키지에는 패키지에 대 한 모든 핵심 정보를 제공 하는 매니페스트가 포함 되어 있습니다. 이 정보에는 패키지 설정의 기본값이 포함 되며 추가 사용자 지정 없이 가장 기본적인 양식의 설정이 결정 됩니다. 

패키지를 만들 때 시퀀서는 패키지 매니페스트 데이터를 사용 하 여 기본 배포 및 사용자 구성 xml 파일을 자동으로 생성 합니다. 따라서 생성 되는 이러한 파일에는 시퀀싱 중에 구성 된 기본 설정이 반영 됩니다. Sequencer에서 생성 된 형식의 패키지에 이러한 파일을 적용 하면 해당 매니페스트에 제공 된 것과 동일한 기본 설정이 패키지에 포함 됩니다. 

이러한 생성 된 파일을 사용 하 여 필요에 따라 패키지에 직접적인 영향을 주지 않는 변경 작업을 수행 합니다. 구성 파일을 추가, 삭제 또는 업데이트 하려면 매니페스트 정보의 기본값을 변경 합니다.

>[!TIP]
>파일을 읽는 순서는 다음과 같습니다.<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>매니페스트</li></ul><p>첫 번째 항목은 마지막으로 읽은 항목을 나타냅니다. 따라서 해당 콘텐츠가 우선 하므로 모든 패키지에 패키지 매니페스트의 기본 설정이 기본적으로 포함 되 고 제공 됩니다.<ol><li> DeploymentConfig.xml 파일을 사용자 지정 하 고 사용자 지정 설정을 적용 하는 경우 패키지 매니페스트의 기본 설정이 재정의 됩니다. </li><li> UserConfig.xml을 사용자 지정 하 고 사용자 지정 설정을 적용 하는 경우 배포 구성 및 패키지 매니페스트 모두에 대 한 기본 설정이 재정의 됩니다. </li></ol>

## 사용자 구성 파일 내용 (UserConfig.xml)
UserConfig 파일은 앱-V 5.1 클라이언트를 실행 하는 컴퓨터에 패키지를 배포할 때 특정 사용자에 대해 적용 되는 구성 설정을 제공 합니다.  이러한 설정은 클라이언트의 다른 사용자에 게 영향을 주지 않습니다.

UserConfig 파일을 사용 하 여 패키지에 대 한 사용자 지정 설정을 지정 하거나 수정 합니다.

-   사용자 당 네이티브 시스템에 통합 된 확장: 바로 가기, 파일 형식 연결, URL 프로토콜, AppPaths, 소프트웨어 클라이언트, COM
-   가상 하위 시스템: 응용 프로그램 개체, 환경 변수, 레지스트리 수정, 서비스 및 글꼴
-   스크립트 (사용자 컨텍스트만)
-   기관 관리 (App-v 4.6를 사용 하 여 패키지 공존을 제어 하는 경우)

### 헤더

동적 사용자 구성 파일의 헤더는 다음과 같습니다.

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

**PackageId** 는 매니페스트 파일에 있는 것과 동일한 값입니다.


### Body

동적 사용자 구성 파일의 본문에는 매니페스트 파일에 정의 된 모든 앱 확장 지점 및 가상 응용 프로그램 구성에 대 한 정보가 포함 될 수 있습니다. 본문에는 네 개의 하위 섹션이 허용 됩니다.

1.  **[응용 프로그램](#applications)** 
2.  **[시스템과](#subsystems)**
3.  **[UserScripts](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### 응용 프로그램

패키지 내의 매니페스트 파일에 포함 된 모든 앱 확장에는 매니페스트 파일에 있는 응용 프로그램 ID가 할당 되어 있습니다. 응용 프로그램 ID를 사용 하 여 패키지 내에서 지정 된 응용 프로그램에 대 한 모든 확장을 설정 하거나 해제할 수 있습니다. 응용 프로그램 ID가 매니페스트 파일에 있어야 하며, 그렇지 않은 경우 무시 됩니다.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### 시스템과

AppExtensions 및 기타 하위 시스템으로 정렬

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

**Enabled** 특성을 사용 하 여 각 하위 시스템을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.

**Extensions** 

일부 하위 시스템 (확장 하위 시스템) 컨트롤 확장 이러한 하위 시스템은 바로 가기, 파일 형식 연결, URL 프로토콜, AppPaths, 소프트웨어 클라이언트, COM입니다.

확장 하위 시스템은 콘텐츠와 별개로 사용 하거나 사용 하지 않도록 설정할 수 있습니다. 예를 들어 바로 가기를 사용 하도록 설정 하면 클라이언트는 기본적으로 매니페스트에 있는 바로 가기를 사용 합니다. 각 확장 하위 시스템에는 노드가 포함 될 수 있습니다 \<Extensions\> . 이 자식 요소가 있으면 클라이언트는 해당 하위 시스템의 매니페스트 파일에 있는 콘텐츠를 무시 하 고 구성 파일의 콘텐츠만 사용 합니다. 

_**예제:**_ 

- 사용자 또는 배포 구성 파일에서이를 정의 하는 경우 매니페스트의 콘텐츠가 무시 됩니다.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- 다음만 정의 하는 경우에는 게시 하는 동안 매니페스트의 콘텐츠가 통합 됩니다.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- 다음을 정의 하는 경우에도 매니페스트 내의 모든 바로 가기가 무시 됩니다. 즉, 통합 된 바로 가기가 없습니다.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**지원 되는 확장 하위 시스템:**_ 

**바로 가기** 확장 하위 시스템은 로컬 시스템에 통합 되는 바로 가기를 제어 합니다.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

**파일 형식 연결** 확장 하위 시스템에서는 파일 형식을 프로그램과 연결 하 여 상황에 맞는 메뉴를 기본적으로 엽니다. 

>[!TIP]
>MIME 형식을 사용 하 여 하위 시스템을 설정할 수 있습니다.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

**Url 프로토콜** 확장 하위 시스템은 클라이언트 컴퓨터의 로컬 레지스트리에 통합 된 url 프로토콜 (예 _: mailto:_)을 제어 합니다. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

**소프트웨어 클라이언트** 확장 하위 시스템을 사용 하면 앱이 전자 메일 클라이언트, 뉴스 읽기 프로그램, 미디어 플레이어로 등록 되어 앱이 프로그램 액세스 및 컴퓨터 기본값 설정 UI에 표시 되도록 만들 수 있습니다. 대부분의 경우이 기능을 사용 하도록 설정 하거나 사용 하지 않도록 설정 해야 합니다. 또한 해당 클라이언트를 제외한 다른 클라이언트가 아직 사용 하도록 설정 하려는 경우에만 전자 메일 클라이언트를 사용 하도록 설정 하 고 사용 하지 않도록 설정할 수 있습니다.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

**Apppaths** 확장 하위 시스템은 응용 프로그램 경로를 사용 하 여 등록 된 앱을 엽니다. 예를 들어 contoso.exe에 _myapp_의 apppath 이름이 있는 경우 사용자는 실행 메뉴에서 _myapp_ 를 입력 하 고 contoso.exe를 열 수 있습니다.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

**COM** 확장 하위 시스템은 로컬 COM 서버에 등록 된 응용 프로그램을 허용 합니다. 모드는 다음과 같이 가능 합니다.

-   통합
-   격리 된 
-   꺼짐

```XML

<COM Mode="Isolated"/>
```

**가상 커널 개체**

```XML

<Objects Enabled="false" />
```

**가상 레지스트리** 는 HKCU 내의 가상 레지스트리에 레지스트리를 설정 합니다.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**가상 파일 시스템**

```XML

    <FileSystem Enabled="true" />
```

**가상 글꼴**

```XML

      <Fonts Enabled="false" />
```

**가상 환경 변수**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**가상 서비스**

```XML

      <Services Enabled="false" />
```

#### UserScripts

UserScripts를 사용 하 여 가상 환경을 설정 하거나 변경 합니다.  배포 시점에 스크립트를 실행 하거나 응용 프로그램이 종료 된 후 환경을 정리할 수도 있습니다. 예제 스크립트를 보려면 sequencer에서 생성 된 사용자 구성 파일을 참조 하세요. 아래 스크립트 섹션에서는 사용할 수 있는 다양 한 트리거에 대 한 자세한 정보를 제공 합니다.

#### ManagingAuthority

패키지의 두 버전이 앱-V 4.6에 배포 된 컴퓨터에 있고 그 ManagingAuthority가 app-v 5.0에 배포 되어 있는 경우 사용 합니다. App-v vNext를 사용 하 여 명명 된 패키지에 대 한 앱-V 4.6 확장 지점을 허용 하려면 UserConfig 파일에 다음을 입력 합니다 (여기서 PackageName는 App-v 4.6의 패키지 GUID).

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## 배포 구성 파일 (DeploymentConfig.xml)

DeploymentConfig 파일은 UserConfig 파일에 나열 된 것과 동일한 기능을 제공 하 여 컴퓨터 컨텍스트 및 사용자 컨텍스트에 대 한 구성 설정을 제공 합니다. 앱-V 5.1 클라이언트를 실행 하는 컴퓨터에 패키지를 배포 하는 경우 설정이 적용 됩니다.

DeploymentConfig 파일을 사용 하 여 패키지에 대 한 사용자 지정 설정을 지정 하거나 수정 합니다.

- 모든 UserConfig 설정
- 모든 사용자에 대해 전역 으로만 적용 될 수 있는 확장
- 글로벌 컴퓨터 위치에 대 한 가상 하위 시스템 (예: 레지스트리)
- 제품 원본 URL
- 스크립트 (컴퓨터 컨텍스트만 해당)
- 하위 프로세스를 종료 하는 컨트롤

### 헤더

동적 배포 구성 파일의 헤더는 다음과 같습니다.

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

**PackageId** 는 매니페스트 파일에 있는 것과 동일한 값입니다.

### Body

동적 배포 구성 파일의 본문에는 다음 두 가지 섹션이 포함 됩니다.

- **Userconfiguration:** 이전 섹션에 설명 된 사용자 구성 파일과 동일한 콘텐츠를 허용 합니다.  패키지를 사용자에 게 게시 하면 사용자 구성 파일을 제공 하지 않는 한이 섹션의 모든 appextensions 구성 설정이 패키지 내의 매니페스트에 해당 하는 설정 보다 우선 합니다. UserConfig 파일을 제공 하는 경우 배포 구성 파일의 사용자 설정 대신 사용 됩니다. 패키지를 전역적으로 게시 하는 경우 배포 구성 파일의 콘텐츠만 매니페스트와 조합 하 여 사용 됩니다. 자세한 내용은 [사용자 구성 파일 내용 (UserConfig.xml)](#user-configuration-file-contents-userconfigxml)을 참조 하세요.

- **MachineConfiguration:** 컴퓨터의 특정 사용자가 아닌 전체 컴퓨터에 대해서만 구성할 수 있는 정보를 포함 합니다. 예를 들어, VFS의 레지스트리 키를 HKEY_LOCAL_MACHINE.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### UserConfiguration

이 섹션에 대해 제공 된 설정에 대 한 정보는 [사용자 구성 파일 내용 (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) 을 참조 하세요. 

### MachineConfiguration

MachineConfiguration 섹션을 사용 하 여 전체 컴퓨터에 대 한 정보를 구성 합니다. 컴퓨터의 특정 사용자를 위한 것이 아닙니다. 예를 들어 가상 레지스트리의 레지스트리 키를 HKEY_LOCAL_MACHINE. 이 요소 아래에는 네 개의 하위 섹션이 허용 됩니다.

1.  **[시스템과](#subsystems-1)**
2.  **[제품 원본 Urloptout](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### 시스템과

AppExtensions 및 기타 하위 시스템으로 정렬

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

**Enabled** 특성을 사용 하 여 각 하위 시스템을 사용 하거나 사용 하지 않도록 설정할 수 있습니다.

**Extensions** 

일부 하위 시스템 (확장 하위 시스템) 컨트롤 확장 하위 시스템은 기본 프로그램에서 사용 하는 응용 프로그램 기능입니다. 이러한 유형의 확장의 경우 패키지가 로컬 시스템에 통합 되도록 전역으로 게시 되어야 합니다. 사용자 구성에서 확장에 적용 되는 컨트롤과 설정에 대 한 규칙도 MachineConfiguration 섹션에 적용 됩니다.

**응용 프로그램 기능**: 응용 프로그램이 자신을 등록 하도록 허용 하는 기본 프로그램에서 사용 됩니다.

- 특정 파일 확장명을 열 수 있습니다.
- 시작 메뉴 인터넷 브라우저 슬롯에 대 한 contender
- 특정 windows MIME 형식을 열 수 있습니다.

또한이 확장에서는 가상 응용 프로그램을 기본 프로그램 설정 UI에 표시 합니다.

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**지원 되는 확장 하위 시스템:**_ 

**컴퓨터 전체 가상 레지스트리** 확장 하위 시스템 HKEY_Local_Machine 내의 가상 레지스트리에 레지스트리 키를 설정 합니다.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**컴퓨터 규모의 가상 커널 개체**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### 제품 원본 Urloptout

제품 Sourceurloptout을 사용 하 여 _PackageSourceRoot_ (지사 시나리오 지원)를 통해 패키지에 대 한 URL을 전역적으로 수정할 수 있음을 표시 합니다. 변경 내용은 다음 시작에 적용 됩니다. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

배포, 게시 또는 제거 시에 스크립트를 실행 하도록 패키지를 구성할 수 있습니다. 예제 스크립트를 보려면 sequencer에서 생성 된 배포 구성 파일을 참조 하세요. 

아래 스크립트 섹션에서는 사용할 수 있는 다양 한 트리거에 대 한 자세한 정보를 제공 합니다.

#### TerminateChildProcess

응용 프로그램 실행 파일을 지정할 수 있으며,이는 응용 프로그램 exe 프로세스가 종료 될 때 자식 프로세스가 종료 됨을 말합니다.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## 스크립트

다음 표에서는 다양 한 스크립트 이벤트 및이를 실행할 수 있는 컨텍스트에 대해 설명 합니다.

| 스크립트 실행 시간       | 배포 구성에서 지정할 수 있음 | 사용자 구성에서 지정할 수 있음 | 패키지의 가상 환경에서 실행할 수 있습니다. | 특정 응용 프로그램의 컨텍스트에서 실행할 수 있습니다. | 시스템/사용자 컨텍스트에서 실행: (배포 구성, 사용자 구성) |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (시스템, 해당 없음)                                                               |
| 패키지              | X                                            | X                                      |                                                   |                                                     | (시스템, 사용자)                                                              |
| 패키지 Unpackage            | X                                            | X                                      |                                                   |                                                     | (시스템, 사용자)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (시스템, 해당 없음)                                                               |
| StartProcess                | X                                            | X                                      | X                                                 | X                                                   | (사용자, 사용자)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (사용자, 사용자)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (사용자, 사용자)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (사용자, 사용자)                                                                |

### 단일 이벤트 트리거에 여러 스크립트 사용

App-v 5.1는 app-v 4.6에서 App-v 5.0 이상으로 변환 하는 패키지를 포함 하 여 App-v 패키지에 대 한 단일 이벤트 트리거에 여러 스크립트를 사용 하도록 지원 합니다. 여러 스크립트를 사용할 수 있도록 앱-V 5.1는 App-v 클라이언트 설치의 일부로 설치 되는 ScriptRunner.exe 라는 스크립트 시작 관리자 응용 프로그램을 사용 합니다.

### 단일 이벤트 트리거에서 여러 스크립트를 사용 하는 방법

실행 하려는 각 스크립트에 대해 해당 스크립트를 ScriptRunner.exe 응용 프로그램에 인수로 전달 합니다. 그런 다음 각 스크립트에 대해 지정 하는 인수와 함께 각 스크립트를 개별적으로 실행 합니다. 트리거 당 하나의 스크립트 (ScriptRunner.exe)만 사용 합니다.

> [!NOTE]
> 
> 먼저 명령 프롬프트에서 다중 스크립트 줄을 실행 하 여 모든 인수가 제대로 작성 되었는지 확인 한 후 배포 구성 파일에 추가 하는 것이 좋습니다.

### 예제 스크립트 및 매개 변수 설명

다음 예제 파일 및 테이블을 사용 하 여 배포 또는 사용자 구성 파일을 수정 하 여 실행 하려는 스크립트를 추가 합니다.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**예제 파일의 매개 변수에는 다음이 포함 됩니다.**

#### \<AddPackage\>

패키지를 추가 하거나 패키지를 게시 하는 등 스크립트를 실행 하는 이벤트 트리거의 이름입니다.

#### \<Path\>ScriptRunner.exe\</Path\>

App-v 클라이언트 설치의 일부로 설치 되는 스크립트 시작 관리자 응용 프로그램입니다.

> [!NOTE]
> 
> ScriptRunner.exe는 App-v 클라이언트의 일부로 설치 되지만, App-v 클라이언트의 위치 는% path% 또는 ScriptRunner이 실행 되지 않습니다. ScriptRunner.exe은 일반적으로 C:FilesApplication Virtualizationfolder에 있습니다.

#### \<Arguments\>

`-appvscript` -실행할 실제 스크립트를 나타내는 토큰입니다.

`script1.exe` – 실행할 스크립트의 이름입니다.

`arg1 arg2` – 실행할 스크립트에 대 한 인수입니다.

`-appvscriptrunnerparameters` – script1.exe에 대 한 실행 옵션을 나타내는 토큰입니다.

`-wait` – 다음 스크립트로 진행 하기 전에 script1.exe 실행이 완료 되기를 ScriptRunner 알리는 토큰.

`-timeout=x` – X 초 후 현재 스크립트의 실행을 중지 하도록 ScriptRunner에 알리는 토큰. 다른 모든 지정 된 스크립트도 계속 실행 됩니다.

`-rollbackonerror` – 아직 실행 되지 않은 모든 스크립트의 실행을 중지 하 고 App-v 클라이언트로 오류를 ScriptRunner 알리는 토큰.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

ScriptRunner.exe의 전체 완료를 기다립니다.

전체 러너에 대 한 시간 제한 값을 개별 스크립트의 제한 시간 값에 대 한 합 보다 크거나 같도록 설정 합니다.

오류를 보고 하 고 rollbackonerror true로 설정 된 개별 스크립트가 있으면 ScriptRunner에서 App-v 클라이언트로 오류를 보고할 수 있습니다.

ScriptRunner는 해당 파일 형식이 컴퓨터에 설치 된 응용 프로그램과 연결 된 모든 스크립트를 실행 합니다. 연결 된 응용 프로그램이 없거나 스크립트의 파일 형식이 컴퓨터의 응용 프로그램과 연결 되어 있지 않으면 스크립트가 실행 되지 않습니다.

### 앱-V 5.1 매니페스트 파일을 사용 하 여 동적 구성 파일 만들기

수동으로 다음 세 가지 방법 중 하나를 사용 하 여 동적 구성 파일을 만들 수 있습니다. App-v 5.1 관리 콘솔을 사용 하거나 패키지를 시퀀싱 하 여 두 개의 샘플 파일을 생성 합니다. App-v 5.1 관리 콘솔을 사용 하 여 파일을 만드는 방법에 대 한 자세한 내용은 [app-v 5.1 관리 콘솔을 사용 하 여 사용자 지정 구성 파일을 만드는 방법](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)을 참조 하세요.

파일을 수동으로 만들려면 이전 섹션의 위의 정보를 단일 파일로 결합할 수 있습니다. Sequencer에서 생성 된 파일을 사용 하는 것이 좋습니다.



- [여기](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)에서 제안을 추가 하거나 투표 합니다.
- App-v 문제는 [App-v TechNet 포럼](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)을 사용 하세요.

## 관련 항목

- [PowerShell을 사용하여 배포 구성 파일을 적용하는 방법](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [PowerShell을 사용하여 사용자 구성 파일을 적용하는 방법](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [App-V 5.1 작업](operations-for-app-v-51.md)

---
