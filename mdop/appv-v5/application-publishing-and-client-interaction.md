---
title: 응용 프로그램 게시 및 클라이언트 상호 작용
description: 응용 프로그램 게시 및 클라이언트 상호 작용
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb648db11009d6f3331d68c5fb8ba74b578fa52c
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910843"
---
# <a name="application-publishing-and-client-interaction"></a>응용 프로그램 게시 및 클라이언트 상호 작용


이 문서에서는 일반적인 App-V 클라이언트 작업과 로컬 운영 체제와의 통합에 대한 기술 정보를 제공합니다.

-   [Sequencer에서 만든 App-V 패키지 파일](#bkmk-appv-pkg-files-list)

-   [appv 파일에는 무엇이 있나요?](#bkmk-appv-file-contents)

-   [App-V 클라이언트 데이터 저장소 위치](#bkmk-files-data-storage)

-   [패키지 레지스트리](#bkmk-pkg-registry)

-   [App-V 패키지 저장소 동작](#bkmk-pkg-store-behavior)

-   [로밍 레지스트리 및 데이터](#bkmk-roaming-reg-data)

-   [App-V 클라이언트 응용 프로그램 수명 주기 관리](#bkmk-clt-app-lifecycle)

-   [App-V 패키지 통합](#bkmk-integr-appv-pkgs)

-   [동적 구성 처리](#bkmk-dynamic-config)

-   [나란히 어셈블리](#bkmk-sidebyside-assemblies)

-   [클라이언트 로깅](#bkmk-client-logging)

추가 참조 정보는 [Microsoft App-V(Application Virtualization) 설명서 리소스 다운로드 페이지를 참조하세요.](https://www.microsoft.com/download/details.aspx?id=27760)

## <a name="app-v-package-files-created-by-the-sequencer"></a><a href="" id="bkmk-appv-pkg-files-list"></a>Sequencer에서 만든 App-V 패키지 파일


Sequencer는 App-V 패키지를 만들고 가상화된 응용 프로그램을 생성합니다. 시차 프로세스를 통해 다음 파일이 생성됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">File</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>.appv</p></td>
<td align="left"><ul>
<li><p>시차 프로세스에서 캡처된 자산 및 상태 정보를 포함하는 기본 패키지 파일입니다.</p></li>
<li><p>배달 시 컴퓨터 및 특정 사용자에게 다시 응용될 수 있는 토큰화된 양식의 패키지 파일, 게시 정보 및 레지스트리의 아키텍처입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>.MSI</p></td>
<td align="left"><p>.appv 파일을 수동으로 배포하거나 타사 배포 플랫폼을 사용하여 배포하는 데 사용할 수 있는 실행 파일 배포 래퍼입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>App-V 클라이언트를 실행하는 컴퓨터의 모든 사용자에게 전역으로 배포되는 패키지의 모든 응용 프로그램에 대한 기본 게시 매개 변수를 사용자 지정하는 데 사용되는 파일입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>App-V 클라이언트를 실행하는 컴퓨터의 특정 사용자에게 배포된 패키지의 모든 응용 프로그램에 대한 게시 매개 변수를 사용자 지정하는 데 사용되는 파일입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>생략된 드라이버, 파일 및 레지스트리 위치를 포함하여 시차 프로세스에서 생성되는 메시지의 요약입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>.CAB</p></td>
<td align="left"><p><em>선택 사항: 이전에 시퀀서된 가상 응용 프로그램 패키지를 자동으로 다시 생성하는 데 사용되는 패키지 </em> 가속기 파일입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>선택 사항: 일반적으로 다시 사용되는 Sequencer 설정을 유지하는 데 사용되는 Sequencer 템플릿 </em> 파일입니다.</p></td>
</tr>
</tbody>
</table>

 

시차에 대한 자세한 내용은 [Application Virtualization 5.0 Sequencing Guide를 참조하십시오.](https://www.microsoft.com/download/details.aspx?id=27760)

## <a name="whats-in-the-appv-file"></a><a href="" id="bkmk-appv-file-contents"></a>appv 파일에는 무엇이 있나요?


appv 파일은 XML 및 비 XML 파일을 단일 엔터티에 함께 저장하는 컨테이너입니다. 이 파일은 OPC(Open Packaging Conventions) 표준을 기반으로 하는 AppX 형식을 기반으로 합니다.

appv 파일 내용을 보시고 패키지의 복사본을 만들어 복사한 파일의 이름을 ZIP 확장명으로 바니다.

appv 파일에는 가상 응용 프로그램을 만들고 게시할 때 사용되는 다음 폴더와 파일이 포함되어 있습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">유형</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>루트</p></td>
<td align="left"><p>파일 폴더</p></td>
<td align="left"><p>시차 중에 캡처된 가상화된 응용 프로그램의 파일 시스템을 포함하는 디렉터리입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types].xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>appv 파일의 핵심 콘텐츠 형식 목록(예: DLL, EXE, BIN)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>App-V 패키지에서 파일의 위치 및 유효성 검사를 사용하도록 설정하는 File, Block 및 BlockMap 요소를 사용하는 appv 파일의 레이아웃입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>패키지 추가, 게시 및 시작에 필요한 정보가 포함된 패키지의 메타데이터입니다. 확장점(파일 형식 연결 및 바로 가기)과 패키지와 연결된 이름 및 GUID를 포함합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>특성(예: directories, files, 불투명한 폴더, 빈 폴더 및 길고 짧은 이름)을 포함하여 시차 중에 캡처된 파일 목록입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>시맨싱 컴퓨터(운영 체제 버전, Internet Explorer 버전, .Net Framework 버전) 및 프로세스(업그레이드, 패키지 버전)에 대한 정보</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry.dat</p></td>
<td align="left"><p>DAT 파일</p></td>
<td align="left"><p>패키지에 대한 시차 프로세스 중에 캡처된 레지스트리 키 및 값입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>기본 및 게시 기능 블록에 대한 파일 목록입니다. 게시 기능 블록에는 패키지 게시를 위해 ICO 파일과 파일의 필수 부분(EXE 및 DLL)이 포함되어 있습니다. 이 기능이 있는 경우 기본 기능 블록에는 시차 프로세스 중에 스트리밍에 최적화된 파일이 포함됩니다.</p></td>
</tr>
</tbody>
</table>

 

## <a name="app-v-client-data-storage-locations"></a><a href="" id="bkmk-files-data-storage"></a>App-V 클라이언트 데이터 저장소 위치


App-V 클라이언트는 가상 응용 프로그램이 제대로 실행되도록 하고 로컬에 설치된 응용 프로그램처럼 작동하도록 하는 작업을 수행합니다. 가상 응용 프로그램을 열고 실행하는 프로세스를 수행하려면 가상 파일 시스템 및 레지스트리에서 매핑해야 응용 프로그램에 사용자가 예상하는 기존 응용 프로그램의 필수 구성 요소가 포함됩니다. 이 섹션에서는 가상 응용 프로그램을 실행하기 위해 필요한 자산에 대해 설명하고 App-V에서 자산을 저장하는 위치를 나열합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">이름</th>
<th align="left">위치</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>패키지 저장소</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>읽기 전용 패키지 파일의 기본 위치</p></td>
</tr>
<tr class="even">
<td align="left"><p>컴퓨터 카탈로그</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>컴퓨터당 구성 문서 포함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 카탈로그</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>사용자당 구성 문서 포함</p></td>
</tr>
<tr class="even">
<td align="left"><p>바로 가기 백업</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>패키지 게시를 게시하지 않은 상태로 복원할 수 있는 이전 통합 지점 저장</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COW(기록 중 복사) 로밍</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>패키지 수정을 위한 쓰기 가능 로밍 위치</p></td>
</tr>
<tr class="even">
<td align="left"><p>COW(기록 중 복사) 로컬</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>패키지 수정을 위해 로밍할 수 없는 쓰기 가능 위치</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 레지스트리</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>컴퓨터용 VReg 또는 전역적으로 게시된 패키지(Machine hive)를 비롯한 패키지 상태 정보가 들어 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 레지스트리</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>VReg를 포함한 사용자 패키지 상태 정보 포함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>User Registry 클래스</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>추가 사용자 패키지 상태 정보가 들어 있습니다.</p></td>
</tr>
</tbody>
</table>

 

표에 대한 자세한 내용은 아래 섹션과 문서 전체에서 제공됩니다.

### <a name="package-store"></a>패키지 저장소

App-V 클라이언트는 패키지 저장소에 탑재된 응용 프로그램 자산을 관리합니다. 이 기본 저장소 위치는 이지만 로컬 레지스트리( 키 아래 값)를 수정하는 PowerShell 명령을 사용하여 설치 중에 또는 설치 후에 구성할 수 `%ProgramData%\App-V` `Set-AppVClientConfiguration` `PackageInstallationRoot` `HKLM\Software\Microsoft\AppV\Client\Streaming` 있습니다. 패키지 저장소는 클라이언트 운영 체제의 로컬 경로에 있어야 합니다. 개별 패키지는 패키지 GUID 및 버전 GUID에 대해 명명된 하위디렉터에 패키지 저장소에 저장됩니다.

특정 응용 프로그램에 대한 경로의 예:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

설치 중에 패키지 저장소의 기본 위치를 변경하려면 App-V 클라이언트를 [배포하는 방법을 참조하세요.](how-to-deploy-the-app-v-client-gb18030.md)

### <a name="shared-content-store"></a>공유 콘텐츠 저장소

App-V 클라이언트가 공유 콘텐츠 저장소 모드로 구성된 경우 스트림 장애가 발생할 때 디스크에 데이터가 기록되지 않습니다. 즉, 패키지에 최소한의 로컬 디스크 공간(게시 데이터)이 필요하게 됩니다. 로컬 저장소가 제한될 수 있으며 SAN과 같은 고성능 네트워크 위치에서 응용 프로그램을 스트리밍하는 VDI 환경에서는 디스크 공간을 적게 사용하는 것이 좋습니다. 공유 콘텐츠 저장소 모드에 대한 자세한 내용은 을 <https://go.microsoft.com/fwlink/p/?LinkId=392750> 참조하세요.

**참고**  
App-V 클라이언트에 대해 공유 콘텐츠 저장소 구성을 사용하는 경우에도 컴퓨터 및 패키지 저장소가 로컬 드라이브에 있어야 합니다.

 

### <a name="package-catalogs"></a>패키지 카탈로그

App-V 클라이언트는 다음 두 개의 파일 기반 위치를 관리합니다.

-   **카탈로그(사용자 및 컴퓨터)**

-   **레지스트리 위치** - 패키지가 게시 대상으로 지정되는 방식에 따라 다를 수 있습니다. 컴퓨터에 대한 카탈로그(데이터 저장소)와 각 개별 사용자에 대한 카탈로그가 있습니다. 컴퓨터 카탈로그는 모든 사용자 또는 모든 사용자에게 적용할 수 있는 전역 정보를 저장하고, 사용자 카탈로그는 특정 사용자에게 적용 가능한 정보를 저장합니다. Catalog는 동적 구성 및 매니페스트 파일의 모음입니다. 패키지 버전당 파일 및 레지스트리 모두에 대한 불연별 데이터가 있습니다. 

### <a name="machine-catalog"></a>컴퓨터 카탈로그

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>패키지가 추가 및 게시될 때 컴퓨터의 사용자가 사용할 수 있는 패키지 문서를 저장합니다. 그러나 게시 시 패키지가 "전역"인 경우 모든 사용자가 통합을 사용할 수 있습니다.</p>
<p>패키지가 전역 패키지가 아닌 경우 통합은 특정 사용자에 한해 게시되지만 여전히 클라이언트 컴퓨터의 모든 사용자에게 수정되고 표시되는 전역 리소스가 있습니다(예: 패키지 디렉터리가 공유 디스크 위치에 있는 경우).</p>
<p>컴퓨터의 사용자가 패키지를 사용할 수 있는 경우(전역 또는 전역이 아닌 경우) 매니페스트는 컴퓨터 카탈로그에 저장됩니다. 패키지가 전역으로 게시되는 경우 컴퓨터 카탈로그에 저장된 동적 구성 파일이 있습니다. 따라서 패키지가 전역인지 여부 결정은 컴퓨터 카탈로그에 정책 파일(UserDeploymentConfiguration 파일)이 있는지 여부에 따라 정의됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기본 저장소 위치</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>이 위치는 패키지 저장소 위치와는 동일하지 않습니다. 패키지 저장소는 패키지 파일의 골든 또는 기본 복사본입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 카탈로그의 파일</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml(전역적으로 게시된 패키지)</p></li>
<li><p>UserDeploymentConfiguration.xml(전역적으로 게시된 패키지)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>패키지가 연결 그룹의 일부일 때 사용되는 추가 컴퓨터 카탈로그 위치</p></td>
<td align="left"><p>다음 위치는 위에서 언급한 특정 패키지 위치 외에 있습니다.</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지가 연결 그룹의 일부인 경우 컴퓨터 카탈로그의 추가 파일</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml(전역으로 게시된 연결 그룹)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="user-catalog"></a>사용자 카탈로그

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>게시 프로세스 중에 만들어집니다. 패키지를 게시하는 데 사용되는 정보를 포함하며, 시작 시 특정 사용자에게 패키지가 프로비전되도록 하는 데도 사용됩니다. 로밍 위치에 만들어지며 사용자별 게시 정보를 포함합니다.</p>
<p>사용자에 대해 패키지를 게시하면 정책 파일이 사용자 카탈로그에 저장됩니다. 동시에 매니페스트의 복사본도 사용자 카탈로그에 저장됩니다. 사용자에 대한 패키지 권리가 제거되면 관련 패키지 파일이 사용자 카탈로그에서 제거됩니다. 관리자는 사용자 카탈로그를 보고 동적 구성 파일의 존재를 볼 수 있습니다. 이는 패키지가 해당 사용자에게 자격을 부여할 수 있는 것일 수 있습니다.</p>
<p>로밍 사용자의 경우 사용자 카탈로그는 기본적으로 대상 사용자의 레거시 App-V 동작을 유지하도록 로밍 또는 공유 위치에 위치해야 합니다. 권리 및 정책은 컴퓨터가 아니라 사용자와 연결됩니다. 따라서 프로비전된 사용자와 함께 로밍해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기본 저장소 위치</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 카탈로그의 파일</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>패키지가 연결 그룹의 일부일 때 사용되는 추가 사용자 카탈로그 위치</p></td>
<td align="left"><p>다음 위치는 위에서 언급한 특정 패키지 위치 외에 있습니다.</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지가 연결 그룹의 일부인 경우 컴퓨터 카탈로그의 추가 파일</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <a name="shortcut-backups"></a>바로 가기 백업

게시 프로세스 동안 App-V 클라이언트는 모든 바로 가기 및 통합 지점을 백업하고 이 백업을 통해 패키지가 게시되지 않은 경우 이러한 통합 지점을 이전 버전을 복원할 수 `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` 있습니다.

### <a name="copy-on-write-files"></a>기록 중 파일 복사

패키지 저장소에는 게시 서버에서 스트리밍된 패키지 파일의 기본 복사본이 포함되어 있습니다. App-V 응용 프로그램을 정상 작동하는 동안 사용자 또는 서비스에서 파일을 변경해야 할 수 있습니다. 이러한 변경 내용은 응용 프로그램을 복구하는 기능을 유지하기 위해 패키지 저장소에서 변경되지 않습니다. 이렇게 하면 이러한 변경 내용이 제거됩니다. COW(Copy on Write)라는 이러한 위치는 로밍 및 비로밍 위치를 모두 지원합니다. 수정 내용이 저장되는 위치는 응용 프로그램이 네이티브 환경에 변경 내용을 작성하기 위해 프로그래밍된 위치에 따라 다를 수 있습니다.

### <a name="cow-roaming"></a>COW 로밍

위에서 설명한 COW 로밍 위치는 일반적인 %AppData% 위치 또는 \\Users\\{username}\\AppData\\Roaming 위치를 대상으로 하는 파일 및 위치에 대한 변경 내용을 저장합니다. 그런 다음 운영 체제 설정에 따라 이러한 폴더와 파일이 로밍됩니다.

### <a name="cow-local"></a>COW 로컬

COW 로컬 위치는 로밍 위치와 유사하지만 로밍 지원이 구성되어 있는 경우에도 다른 컴퓨터로는 로밍되지 않습니다. 위에서 설명한 COW 로컬 위치는 %AppData% 위치가 아니라 일반적인 창에 적용할 수 있는 변경 내용을 저장합니다. 나열된 Director는 다양하지만 일반적인 모든 Windows 위치(예: Common AppData 및 Common AppDataS)에 대한 두 개의 위치가 있습니다. **S는** 가상 서비스가 로그온한 사용자와 다른 상승된 사용자로 변경을 요청할 때 제한된 위치를 지정합니다. S가 아닌**위치는** 사용자 기반 변경 내용을 저장합니다.

## <a name="package-registry"></a><a href="" id="bkmk-pkg-registry"></a>패키지 레지스트리


응용 프로그램이 패키지 레지스트리 데이터에 액세스하려면 App-V Client에서 응용 프로그램에서 패키지 레지스트리 데이터를 사용할 수 있도록 해야 합니다. App-V 클라이언트는 실제 레지스트리를 모든 레지스트리 데이터에 대한 백업 저장소로 사용 합니다.

새 패키지가 App-V 클라이언트에 추가될 때 레지스트리 복사본입니다. 패키지의 DAT 파일이 에 `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` 만들어집니다. 파일의 이름은 의 버전 GUID입니다. DAT 확장명입니다. 이 복사본을 만든 이유는 패키지의 실제 하이브 파일이 사용되지 않도록 하여 나중에 패키지를 제거하지 못하게 하기 위한 것입니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>패키지 저장소의 Registry.dat</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</strong></p></td>
</tr>
</tbody>
</table>

 

클라이언트에서 패키지의 첫 번째 응용 프로그램이 시작될 때 클라이언트는 Hive 파일에서 콘텐츠를 단계 또는 복사하여 대체 위치에 패키지 레지스트리 데이터를 다시 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` 생성합니다. 단계별 레지스트리 데이터에는 두 가지 유형의 컴퓨터 데이터와 사용자 데이터가 있습니다. 컴퓨터 데이터는 컴퓨터의 모든 사용자에서 공유됩니다. 사용자 데이터는 각 사용자에 대해 사용자에 대해 사용자지정 위치에 대해 `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` 준비됩니다. 컴퓨터 데이터는 궁극적으로 패키지 제거 시 제거되고 사용자 데이터는 사용자 게시되지 않은 작업에서 제거됩니다.

### <a name="package-registry-staging-vs-connection-group-registry-staging"></a>패키지 레지스트리 준비와 연결 그룹 레지스트리 준비 비교

연결 그룹이 있는 경우 레지스트리 준비의 이전 프로세스는 true를 보유하지만 처리해야 할 하이브 파일이 하나인 대신 두 개 이상의 파일이 있습니다. 파일은 연결 그룹 XML에 나타나는 순서대로 처리됩니다. 첫 번째 작성기에서 충돌이 해결됩니다.

단계적 레지스트리는 단일 패키지 사례와 동일한 방식으로 유지됩니다. 단계적 사용자 레지스트리 데이터는 사용하지 않도록 설정될 때까지 연결 그룹에 대해 남아 있습니다. 연결 그룹 제거 시 단계적 컴퓨터 레지스트리 데이터가 제거됩니다.

### <a name="virtual-registry"></a>가상 레지스트리

VREG(가상 레지스트리)의 목적은 패키지 레지스트리의 단일 병합된 보기와 응용 프로그램에 대한 기본 레지스트리를 제공하는 것입니다. 또한 COW(Copy-On-Write) 기능도 제공합니다. 즉, 가상 프로세스의 컨텍스트에서 레지스트리에 대한 변경 내용이 별도의 COW 위치로 변경됩니다. 즉, VREG는 최대 3개의 개별 레지스트리 위치를 레지스트리 COW- package - native 레지스트리의 채워진 위치에 따라 단일 보기로 &gt; 결합해야 &gt; 합니다. 레지스트리 데이터에 대한 요청이 만들어진 경우 요청한 데이터를 찾을 때까지 순서대로 찾습니다. COW 위치에 값이 저장되어 있는 경우 다른 위치로 이동하지는 않습니다. 그러나 COW 위치에 데이터가 없는 경우 해당 데이터를 찾을 때까지 패키지 및 네이티브 위치로 진행됩니다.

### <a name="registry-locations"></a>레지스트리 위치

패키지를 개별적으로 게시하는지 또는 연결 그룹의 일부로 게시하는지 여부에 따라 App-V 클라이언트가 레지스트리 정보를 저장하는 두 개의 패키지 레지스트리 위치와 두 개의 연결 그룹 위치가 있습니다. 패키지에 대한 COW 위치 3개와 VREG에서 만들어 관리되는 연결 그룹에 대해 3개의 COW 위치가 있습니다. 설정 및 연결 그룹에 대한 설정은 공유되지 않습니다.

**단일 패키지 VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>위치</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>COW</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\REGISTRY(승진 프로세스만 작성할 수 있습니다.)</p></li>
<li><p>User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</p></li>
<li><p>User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>패키지</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>기본</strong></p></td>
<td align="left"><ul>
<li><p>기본 응용 프로그램 레지스트리 위치</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**연결 그룹 VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>위치</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>COW</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY(상승 프로세스만 작성할 수 있습니다.)</p></li>
<li><p>User Registry\Client\PackageGroups\GrpGUID\REGISTRY(Software\Classes를 제외한 HKCU에 기록된 모든 것)</p></li>
<li><p>User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>패키지</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>기본</strong></p></td>
<td align="left"><ul>
<li><p>기본 응용 프로그램 레지스트리 위치</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

HKLM에는 두 개의 COW 위치가 있습니다. 상승된 프로세스 및 상승되지 않은 프로세스. 상승된 프로세스는 항상 HKLM의 보안 COW에 HKLM 변경 내용을 작성합니다. 상승되지 않은 프로세스는 항상 HKCU\\Software\\Classes에서 비보안 COW에 HKLM 변경 내용을 작성합니다. 응용 프로그램이 HKLM에서 변경 내용을 읽을 때 상승된 프로세스는 HKLM의 보안 COW에서 변경 내용을 읽습니다. 비보안 COW에서 변경한 내용을 우선적으로 적용하기 위해 두 가지 모두에서 상승되지 않은 읽기를 합니다.

### <a name="pass-through-keys"></a>통과 키

통과 키를 사용하면 관리자가 패키지 및 COW 위치를 우회하여 기본 레지스트리에서만 읽을 수 있도록 특정 키를 구성할 수 있습니다. 통과 위치는 패키지와 관련이 없는 컴퓨터의 전역 위치로 키에 경로를 추가하여 구성할 수 있습니다. 이 경로는 키의 **PassThroughPaths라는** **REG\_MULTI\_SZ** 값에 대한 통과 값으로 처리해야 `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` 합니다. 이 다중 문자열 값 아래에 나타나는 키와 해당 자식 키는 통과 키로 처리됩니다.

다음 위치는 기본적으로 통과 위치로 구성됩니다.

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local 설정\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local 설정\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet 설정

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Policies

통과 키의 목적은 가상 응용 프로그램이 성공적인 작업 또는 통합을 위해 비 가상 응용 프로그램에 필요한 레지스트리 데이터를 VReg에 작성하지 않도록 하는 것입니다. Policies 키를 사용하면 관리자가 설정한 그룹 정책 기반 설정이 패키지 설정에 따라 사용되지 않습니다. AppModel 키는 최신 UI 기반 응용 프로그램과 Windows 필요합니다. 관리는 기본 통과 키를 수정하지 않는 것이 되지만, 경우에 따라 응용 프로그램 동작에 따라 통과 키를 추가해야 할 수 있습니다.

## <a name="app-v-package-store-behavior"></a><a href="" id="bkmk-pkg-store-behavior"></a>App-V 패키지 저장소 동작


App-V 5는 appv 파일의 확장된 자산 파일이 저장되는 위치인 패키지 저장소를 관리합니다. 기본적으로 이 위치는 %ProgramData%\\App-V에 저장되고 사용 가능 디스크 공간으로만 저장소 기능 면에서 제한됩니다. 패키지 저장소는 이전 섹션에서 설명한 패키지 및 버전의 GUID로 구성됩니다.

### <a name="add-packages"></a>패키지 추가

App-V 패키지는 App-V 클라이언트를 통해 컴퓨터에 추가된 후 단계적으로 구성됩니다. App-V 클라이언트는 요청 시 준비를 제공합니다. 게시 또는 수동 Add-AppVClientPackage 중에 데이터 구조는 패키지 저장소(c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID})에서 빌드됩니다. 앱에 정의된 게시 블록에 식별된 패키지 StreamMap.xml 시스템에 추가되고 시작 시 적절한 응용 프로그램 자산이 존재하도록 최상위 폴더 및 하위 파일이 단계적으로 추가됩니다.

### <a name="mounting-packages"></a>탑재 패키지

패키지는 PowerShell을 사용하여 또는 `Mount-AppVClientPackage` **App-V** 클라이언트 UI를 사용하여 패키지를 다운로드하여 명시적으로 로드할 수 있습니다. 이 작업은 전체 패키지를 패키지 저장소에 완전히 로드합니다.

### <a name="streaming-packages"></a>스트리밍 패키지

스트리밍의 기본 동작을 변경하도록 App-V 클라이언트를 구성할 수 있습니다. 모든 스트리밍 정책은 레지스트리 키 에 `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` 저장됩니다. . 정책은 PowerShell cmdlet을 사용하여 `Set-AppvClientConfiguration` 설정됩니다. 스트리밍에는 다음 정책이 적용됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">정책</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>On Windows 8 3G 및 셀룰러 네트워크를 통해 스트리밍할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>백그라운드 로드 설정을 지정합니다.</p>
<p><strong>0 </strong> - 사용 안 하게</p>
<p><strong>1 </strong> – 이전에 사용된 패키지만</p>
<p><strong>2 </strong> - 모든 패키지</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>로컬 컴퓨터의 패키지 저장소에 대한 루트 폴더</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>패키지를 스트리밍해야 하는 루트 오버라이드</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>VDI 시나리오에 공유 콘텐츠 저장소를 사용할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

 

이러한 설정은 클라이언트로 App-V 패키지 자산을 스트리밍하는 동작에 영향을 미치게 됩니다. 기본적으로 App-V는 초기 게시 및 기본 기능 블록을 다운로드한 후에만 필요한 자산을 다운로드합니다. 스트리밍 패키지에 대해 설명해야 하는 세 가지 특정 동작이 있습니다.

-   백그라운드 스트리밍

-   최적화된 스트리밍

-   스트림 폴트

### <a name="background-streaming"></a>백그라운드 스트리밍

PowerShell cmdlet을 사용하여 자동 로드 설정을 사용하여 백그라운드 스트리밍을 위한 현재 모드를 결정하고 cmdlet을 사용하여 Set-AppvClientConfiguration 또는 `Get-AppvClientConfiguration` 레지스트리(HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming 키)에서 수정할 수 있습니다. 백그라운드 스트리밍은 자동 로드 설정이 이전에 사용된 패키지를 다운로드할 수 있는 기본 설정입니다. 기본 설정(값=1)을 기반으로 하는 동작은 응용 프로그램이 시작된 후 백그라운드에서 App-V 데이터 블록을 다운로드합니다. 이 설정은 시작 여부에 따라 모든 패키지(value=0)를 함께 사용하지 않도록 설정하거나 모든 패키지(값=2)에 대해 사용하도록 설정할 수 있습니다.

### <a name="optimized-streaming"></a>최적화된 스트리밍

시차 중에 기본 기능 블록을 사용하여 App-V 패키지를 구성할 수 있습니다. 이 설정을 사용하면 시맨싱 엔지니어가 특정 응용 프로그램 또는 응용 프로그램에 대한 시작 파일을 모니터링하고 App-V 패키지의 데이터 블록을 패키지의 응용 프로그램을 처음 실행할 때 스트리밍하도록 표시할 수 있습니다.

### <a name="stream-faults"></a>스트림 오류

게시 데이터의 초기 스트림과 기본 기능 블록이 지난 후 추가 파일에 대한 요청은 스트림 폴트가 수행됩니다. 이러한 데이터 블록은 필요한 경우 패키지 저장소에 다운로드됩니다. 이렇게 하면 사용자가 패키지의 일부만 다운로드할 수 있으며 일반적으로 패키지를 시작하고 일반 작업을 실행할 수 있습니다. 사용자가 현재 패키지 저장소에 없는 데이터가 필요한 작업을 시작하면 다른 모든 블록이 다운로드됩니다.

App-V 패키지 스트리밍에 대한 자세한 내용은 을 <https://go.microsoft.com/fwlink/?LinkId=392770> 방문하세요.

스트리밍 최적화를 위한 시차는 에서 사용할 수 <https://go.microsoft.com/fwlink/?LinkId=392771> 있습니다. .

### <a name="package-upgrades"></a>패키지 업그레이드

App-V 패키지는 응용 프로그램의 수명 주기 동안 업데이트해야 합니다. App-V 패키지 업그레이드는 패키지 게시 작업과 유사합니다. 각 버전은 자체 PackageRoot 위치에 만들어집니다. `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . 업그레이드 작업은 동일한 패키지의 다른 버전에서 동일하고 스트리밍된 파일에 대한 하드 링크를 만들어 최적화됩니다.

### <a name="package-removal"></a>패키지 제거

패키지가 제거될 때 App-V 클라이언트의 동작은 제거에 사용되는 방법에 따라 달라 집니다. App-V 전체 인프라를 사용하여 응용 프로그램 게시를 제거하면 사용자 카탈로그 파일(전역으로 게시된 응용 프로그램의 컴퓨터 카탈로그)이 제거되지만 패키지 저장소 위치 및 COW 위치는 유지됩니다. PowerShell cmdlet을 사용하여 App-V 패키지를 제거하면 패키지 `Remove-AppVClientPackge` 저장소 위치가 정리됩니다. 관리 서버에서 App-V 패키지를 게시하면 제거 작업이 수행되지 않습니다. 두 작업 모두 패키지 저장소 패키지 파일을 제거하지 않습니다.

## <a name="roaming-registry-and-data"></a><a href="" id="bkmk-roaming-reg-data"></a>로밍 레지스트리 및 데이터


App-V 5는 사용되는 응용 프로그램이 작성되는 방식에 따라 로밍 시 기본에 가까운 환경을 제공할 수 있습니다. 기본적으로 App-V는 운영 체제의 로밍 구성에 따라 로밍 위치에 저장된 AppData를 로밍합니다. 파일 기반 데이터를 저장하는 다른 위치는 로밍되지 않은 위치에 위치하기 때문에 컴퓨터에서 컴퓨터로 로밍되지 않습니다.

### <a name="roaming-requirements-and-user-catalog-data-storage"></a><a href="" id="bkmk-clt-inter-roam-reqs"></a>로밍 요구 사항 및 사용자 카탈로그 데이터 저장소

App-V는 사용자 카탈로그의 상태를 나타내는 데이터를 다음 형태로 저장합니다.

-   %appdata%\\Microsoft\\AppV\\Client\\Catalog에 있는 파일

-   레지스트리 설정 아래 `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

이러한 파일 및 레지스트리 설정은 사용자의 카탈로그를 나타내기 때문에 둘 다 로밍해야 합니다. 또는 주어진 사용자에 대해 로밍하지 말아야 합니다. App-V는 %AppData%로밍을 지원하지 않지만 사용자의 프로필(레지스트리)을 로밍하지 않습니다. 또는 그 반대의 경우도 마찬가지입니다.

**참고**  
**Repair-AppvClientPackage** cmdlet은 사용자의 App-V 상태가 누락되거나 %appdata%의 데이터와 불일치하는 패키지의 게시 상태를 복구하지 `HKEY_CURRENT_USER` 않습니다.

 

### <a name="registry-based-data"></a>레지스트리 기반 데이터

App-V 레지스트리 로밍은 다음 표에 나와 있는 두 가지 시나리오에 속합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>표준 사용자로 실행된 응용 프로그램</p></td>
<td align="left"><p>표준 사용자가 App-V 응용 프로그램을 시작하면 HKLM 및 HKCU for App-V 응용 프로그램이 모두 컴퓨터의 HKCU hive에 저장됩니다. 이 경로는 두 가지 고유한 경로로 나타날 수 있습니다.</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</p></li>
</ul>
<p>위치는 운영 체제 설정에 따라 로밍에 사용할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>권한 상승을 통해 실행된 응용 프로그램</p></td>
<td align="left"><p>권한 상승을 통해 응용 프로그램이 시작된 경우:</p>
<ul>
<li><p>HKLM 데이터는 로컬 컴퓨터의 HKLM hive에 저장됩니다.</p></li>
<li><p>HKCU 데이터가 사용자 레지스트리 위치에 저장됩니다.</p></li>
</ul>
<p>이 시나리오에서는 이러한 설정이 일반 운영 체제 로밍 구성으로 로밍되지 않습니다. 결과 레지스트리 키와 값은 다음 위치에 저장됩니다.</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="app-v-and-folder-redirection"></a>App-V 및 폴더 리디렉션

App-V 5.0 SP2는 로밍 AppData 폴더(%AppData%)의 폴더 리디렉션을 지원합니다. 가상 환경이 시작된 경우 사용자의 로밍 AppData 디렉터리의 로밍 AppData 상태가 로컬 캐시에 복사됩니다. 반대로 가상 환경이 종료될 때 특정 사용자의 로밍 AppData와 연결된 로컬 캐시가 해당 사용자의 로밍 AppData 디렉터리의 실제 위치로 전송됩니다.

일반적인 패키지에는 AppData\\Local 및 AppData\\Roaming의 설정에 대해 사용자의 백업 저장소에 매핑된 여러 위치가 있습니다. 이러한 위치는 사용자 프로필에 사용자당 저장되고 패키지 VFS 디렉터에 대한 변경 내용을 저장하고 기본 패키지 VFS를 보호하는 데 사용되는 복사 위치입니다.

다음 표에는 폴더 리디렉션이 구현되지 않은 로컬 및 로밍 위치가 표시됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">패키지의 VFS 디렉터리</th>
<th align="left">백업 저장소의 매핑된 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

다음 표에는 %AppData%에 대해 폴더 리디렉션이 구현되고 위치가 리디렉션된 경우(일반적으로 네트워크 위치로) 로컬 및 로밍 위치가 표시됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">패키지의 VFS 디렉터리</th>
<th align="left">백업 저장소의 매핑된 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

현재 App-V 클라이언트 VFS 드라이버는 네트워크 위치에 쓸 수 없습니다. 따라서 App-V 클라이언트는 폴더 리디렉션의 존재를 감지하고 게시하는 동안 및 가상 환경이 시작될 때 로컬 드라이브의 데이터를 복사합니다. 사용자가 App-V 응용 프로그램을 닫고 App-V 클라이언트가 가상 환경을 닫고 나면 VFS AppData의 로컬 저장소가 다시 네트워크에 복사되어 프로세스가 반복되는 추가 컴퓨터로 로밍할 수 있습니다. 프로세스의 자세한 단계는 다음입니다.

1.  게시 또는 가상 환경 시작 중에 App-V 클라이언트는 AppData 디렉터리의 위치를 검색합니다.

2.  로밍 AppData 경로가 로컬 또는 ino AppData\\Roaming 위치가 매핑된 경우 아무 것도 실행되지 않습니다.

3.  로밍 AppData 경로가 로컬이 아닌 경우 VFS AppData 디렉터리는 로컬 AppData 디렉터리에 매핑됩니다.

이 프로세스는 App-V 클라이언트 VFS 드라이버에서 지원되지 않는 로컬이 아닌 %AppData%의 문제를 해결합니다. 그러나 이 새 위치에 저장된 데이터는 폴더 리디렉션을 사용하여 로밍되지 않습니다. 응용 프로그램을 실행하는 동안 변경된 모든 내용은 로컬 AppData 위치에 적용되고 리디렉션된 위치에 복사해야 합니다. 이 프로세스의 자세한 단계는 다음입니다.

1.  App-V 응용 프로그램이 종료된 후 가상 환경을 종료합니다.

2.  로밍 AppData 위치의 로컬 캐시는 압축되어 ZIP 파일에 저장됩니다.

3.  ZIP 패키징 프로세스 종료 시 타임스탬프를 사용하여 파일의 이름을 지정합니다.

4.  타임스탬프는 HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID \\AppDataTime 레지스트리에 마지막으로 알려진 AppData 타임스탬프로 &gt; 기록됩니다.

5.  폴더 리디렉션 프로세스를 호출하여 로밍 AppData 디렉터리에 업로드된 ZIP 파일을 평가하고 초기화합니다.

타임스탬프는 충돌이 있는 경우 "마지막 기록기" 시나리오를 결정하는 데 사용되어 App-V 응용 프로그램이 게시되거나 가상 환경이 시작될 때 데이터 다운로드를 최적화하는 데 사용됩니다. 폴더 리디렉션은 지원 정책이 적용된 다른 클라이언트에서 데이터를 사용할 수 있도록 설정하고 AppData\\Roaming 데이터를 클라이언트의 로컬 AppData 위치에 저장하는 프로세스를 시작됩니다. 자세한 프로세스는 다음을 참조합니다.

1.  사용자는 응용 프로그램을 시작하여 가상 환경을 시작합니다.

2.  응용 프로그램의 가상 환경은 타임스탬프가 적용된 최신 ZIP 파일이 있는 경우 해당 파일을 검사합니다.

3.  레지스트리에서 마지막으로 업로드된 타임스탬프(있는 경우)가 확인됩니다.

4.  마지막으로 알려진 로컬 업로드 타임스탬프가 ZIP 파일의 타임스탬프보다 크거나 같지 않으면 가장 최근의 ZIP 파일이 다운로드됩니다.

5.  마지막으로 알려진 로컬 업로드 타임스탬프가 로밍 AppData 위치에 있는 가장 최근 ZIP 파일보다 이전인 경우 ZIP 파일은 사용자 프로필의 로컬 임시 디렉터리로 추출됩니다.

6.  ZIP 파일이 성공적으로 추출된 후 로밍 AppData 디렉터리의 로컬 캐시의 이름을 변경하고 새 데이터가 제 위치로 이동됩니다.

7.  이름 변경된 디렉터리가 삭제되고 응용 프로그램이 가장 최근에 저장된 로밍 AppData 데이터로 열립니다.

그러면 AppData\\Roaming 위치에 있는 응용 프로그램 설정의 성공적인 로밍이 완료됩니다. 해결해야 하는 다른 조건은 패키지 복구 작업뿐입니다. 프로세스의 세부 정보는 다음을 참조합니다.

1.  복구하는 동안 사용자의 로밍 AppData 디렉터리 경로가 로컬 경로가 아닌지 검색합니다.

2.  로컬이 아닌 로밍 AppData 경로 대상을 매핑하면 예상 로밍 및 로컬 AppData 위치가 다시 설정됩니다.

3.  레지스트리에 저장된 타임스탬프(있는 경우)를 삭제합니다.

이 프로세스는 AppData의 로컬 및 네트워크 위치를 모두 다시 만들고 타임스탬프의 레지스트리 레코드를 제거합니다.

## <a name="app-v-client-application-lifecycle-management"></a><a href="" id="bkmk-clt-app-lifecycle"></a>App-V 클라이언트 응용 프로그램 수명 주기 관리


App-V 전체 인프라에서 응용 프로그램을 시퀀스한 후 App-V 관리 및 게시 서버를 통해 응용 프로그램을 관리하고 사용자 또는 컴퓨터에 게시합니다. 이 섹션에서는 일반적인 App-V 응용 프로그램 수명 주기 작업(추가, 게시, 시작, 업그레이드 및 제거) 중에 발생하는 작업과 App-V 클라이언트 관점에서 변경 및 수정된 파일 및 레지스트리 위치에 대해 자세히 설명합니다. App-V Client 작업은 App-V Client를 실행하는 컴퓨터에서 시작된 일련의 PowerShell 명령으로 수행됩니다.

이 문서에서는 App-V 전체 인프라 솔루션에 초점을 맞추고 있습니다. App-V와 Configuration Manager 2012의 통합에 대한 자세한 내용은 을 <https://go.microsoft.com/fwlink/?LinkId=392773> 방문하세요.

App-V 응용 프로그램 수명 주기 작업은 사용자 로그인(기본값), 컴퓨터 시작 또는 백그라운드 시간 지정 작업으로 트리거됩니다. 게시 서버, 새로 고침 간격, 패키지 스크립트 사용 설정 등을 비롯한 App-V 클라이언트 작업에 대한 설정은 클라이언트 설치 또는 PowerShell 명령을 사용하여 설치 후 설치 중에 구성됩니다. TechNet에서 클라이언트를 배포하는 방법 섹션: [App-V 클라이언트를](how-to-deploy-the-app-v-client-gb18030.md) 배포하거나 PowerShell을 활용하는 방법을 참조하세요.

```powershell
get-command *appv*
```

### <a name="publishing-refresh"></a>게시 새로 고침

게시 새로 고침 프로세스는 App-V 클라이언트에서 수행되는 몇 가지 작은 작업으로 구성됩니다. App-V는 작업 예약 기술이 아니라 응용 프로그램 가상화 기술이기 때문에 Windows 작업 스케줄러를 사용하여 사용자 로그온, 컴퓨터 시작 및 예약된 간격으로 프로세스를 사용하도록 설정할 수 있습니다. 위에 나열된 설치 중에 클라이언트를 구성하는 것이 올바른 설정을 사용하여 대규모 컴퓨터 그룹에 클라이언트를 배포할 때 선호되는 방법입니다. 이러한 클라이언트 설정은 다음 PowerShell cmdlet을 사용하여 구성할 수 있습니다.

-   **Add-AppVPublishingServer:** App-V 패키지를 제공하는 App-V 게시 서버로 클라이언트를 구성합니다.

-   **Set-AppVPublishingServer:** App-V 게시 서버의 현재 설정을 수정합니다.

-   **Set-AppVClientConfiguration:** App-V 클라이언트의 현재 설정을 수정합니다.

-   **Sync-AppVPublishingServer:** App-V 게시 새로 고침 프로세스를 수동으로 초기화합니다. 이는 게시 서버를 구성하는 동안 만들어진 예약된 작업에도 활용됩니다.

다음 섹션에서는 App-V 게시 새로 고침의 여러 단계에서 발생하는 작업을 자세히 설명합니다. 항목은 다음과 같습니다.

-   App-V 패키지 추가

-   App-V 패키지 게시

### <a name="adding-an-app-v-package"></a>App-V 패키지 추가

클라이언트에 App-V 패키지를 추가하는 것은 새로 고침 게시 프로세스의 첫 번째 단계입니다. 최종 결과는 `Add-AppVClientPackage` PowerShell의 cmdlet과 동일합니다. 단, 새로 고침 추가 프로세스가 진행되는 동안 구성된 게시 서버에 연결하여 클라이언트에 높은 수준의 응용 프로그램 목록을 다시 전달하여 단일 패키지 추가 작업이 아니라 보다 자세한 정보를 끌어 들이게 됩니다. 패키지 또는 연결 그룹 추가 또는 업데이트에 대해 클라이언트를 구성한 다음 appv 파일에 액세스하여 프로세스가 계속됩니다. 그런 다음 appv 파일의 내용이 확장되고 해당 위치의 로컬 운영 체제에 배치됩니다. 다음은 패키지가 장애 스트리밍에 대해 구성된 경우 프로세스의 자세한 워크플로입니다.

**App-V 패키지를 추가하는 방법**

1.  게시 새로 고침 프로세스의 PowerShell 또는 작업 순서 시작을 통해 수동 시작

    1.  App-V 클라이언트는 HTTP 연결을 설정하고 대상에 따라 응용 프로그램 목록을 요청합니다. 새로 고침 게시 프로세스는 대상 컴퓨터 또는 사용자를 지원합니다.

    2.  App-V 게시 서버는 시작 대상, 사용자 또는 컴퓨터의 ID를 사용하여 데이터베이스에서 자격이 있는 응용 프로그램 목록을 쿼리합니다. 응용 프로그램 목록은 클라이언트가 패키지 기준에 따라 추가 요청을 서버에 보내는 데 사용하는 XML 응답으로 제공됩니다.

2.  App-V 클라이언트의 게시 에이전트는 직렬화된 아래의 모든 작업을 수행합니다.

    연결 그룹에 포함되는 패키지 버전 업데이트는 처리될 수 없습니다.

3.  추가 또는 업데이트 작업을 식별하여 패키지를 구성합니다.

    1.  App-V 클라이언트는 앱의 AppX API를 Windows 서버에서 appv 파일에 액세스합니다.

    2.  패키지 파일이 열리면 패키지 AppXManifest.xml StreamMap.xml 패키지 저장소로 다운로드됩니다.

    3.  게시 블록 데이터에 정의된 데이터를 완전히 StreamMap.xml. 게시 블록 데이터를 패키지 저장소\\PkgGUID\\VerGUID\\Root에 저장합니다.

        -   아이콘: 확장 지점의 대상입니다.

        -   PE 헤더(PE 헤더): 직접 액세스하거나 파일 형식을 통해 디스크의 이미지 필요에 대한 기본 정보를 포함하는 확장점 대상입니다.

        -   스크립트: 게시 프로세스 전체에서 사용할 스크립트 디렉터리를 다운로드합니다.

    4.  패키지 저장소를 채우는 경우:

        1.  나열된 모든 디렉터에 대해 추출된 패키지를 나타내는 디스크에 스파스 파일을 생성합니다.

        2.  루트 아래에 최상위 파일 및 폴더를 단계화합니다.

        3.  다른 모든 파일은 디렉터리가 디스크에서 스파스로 나열되어 있으며 수요에 따라 스트리밍되는 경우 만들어집니다.

    5.  컴퓨터 카탈로그 항목을 생성합니다. 패키지 Manifest.xml DeploymentConfiguration.xml 파일을 만들고 패키지에 DeploymentConfiguration.xml 파일을 만들지 않습니다.

    6.  레지스트리 HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog에서 패키지 저장소의 위치 만들기

    7.  패키지 저장소에서 %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat로 Registry.dat 파일을 만드세요.

    8.  App-V 커널 모드 드라이버 HKLM\\Microsoft\\Software\\AppV\\MAV에 패키지 등록

    9.  패키지 추가 타이밍에 AppxManifest.xml DeploymentConfig.xml 파일에서 스크립팅을 호출합니다.

4.  연결 그룹을 추가 및 사용 또는 사용 안 하도록 설정하여 구성합니다.

5.  대상(사용자 또는 컴퓨터)에 게시되지 않은 개체를 제거합니다.

    **참고**  
    이렇게 하면 패키지 삭제가 수행되지 않고 특정 대상(사용자 또는 컴퓨터)에 대한 통합 지점이 제거되고 사용자 카탈로그 파일(전역적으로 게시된 컴퓨터 카탈로그 파일)이 제거됩니다.

     

6.  클라이언트 구성에 따라 백그라운드 부하 탑재를 호출합니다.

7.  컴퓨터 또는 사용자에 대한 게시 정보가 이미 있는 패키지는 즉시 복원됩니다.

    **참고**  
    이 조건은 패키지를 백그라운드로 추가한 후 게시를 하지 않고 제거 제품으로 발생합니다.

     

이렇게 하여 게시 새로 고침 프로세스의 App-V 패키지 추가가 완료됩니다. 다음 단계에서는 특정 대상(컴퓨터 또는 사용자)에 패키지를 게시합니다.

![패키지에 파일 및 레지스트리 데이터를 추가합니다.](images/packageaddfileandregistrydata.png)

### <a name="publishing-an-app-v-package"></a>App-V 패키지 게시

새로 고침 게시 작업 중에 특정 게시 작업(Publish-AppVClientPackage)은 사용자 카탈로그에 항목을 추가하고, 사용자에게 권한을 매핑하고, 로컬 저장소를 식별하고, 통합 단계를 완료하여 완료합니다. 자세한 단계는 다음과 같습니다.

**App-V 패키지를 게시하는 방법**

1.  패키지 항목이 사용자 카탈로그에 추가됩니다.

    1.  사용자 대상 패키지: UserDeploymentConfiguration.xml UserManifest.xml 및 패키지가 사용자 카탈로그의 머신에 배치됩니다.

    2.  컴퓨터 대상(전역) 패키지: UserDeploymentConfiguration.xml 카탈로그에 배치됩니다.

2.  HKLM\\Software\\Microsoft\\AppV\\MAV에서 사용자에 대한 커널 모드 드라이버로 패키지를 등록합니다.

3.  통합 작업을 수행합니다.

    1.  확장 지점을 생성합니다.

    2.  사용자의 레지스트리 및 로밍 프로필(바로 가기 백업)에 백업 정보를 저장합니다.

        **참고**  
        이렇게 하면 패키지가 게시되지 않은 경우 확장 지점을 복원할 수 있습니다.

         

    3.  게시 타이밍을 대상으로 하는 스크립트를 실행합니다.

연결 그룹의 일부인 App-V 패키지를 게시하는 것은 위의 프로세스와 매우 유사합니다. 연결 그룹의 경우 특정 카탈로그 정보를 저장하는 경로에는 PackageGroups가 카탈로그 디렉터리의 자식으로 포함됩니다. 자세한 내용은 위의 컴퓨터 및 사용자 카탈로그 정보를 검토합니다.

![패키지에 파일 및 레지스트리 데이터 추가 - global.](images/packageaddfileandregistrydata-global.png)

### <a name="application-launch"></a>응용 프로그램 시작

새로 고침 게시 프로세스가 끝날 때 사용자는 App-V 응용 프로그램을 시작한 다음 다시 실행합니다. 이 프로세스는 매우 간단하며 최소한의 네트워크 트래픽으로 빠르게 시작하도록 최적화되어 있습니다. App-V 클라이언트는 사용자 카탈로그의 경로에서 게시 중에 만들어진 파일을 검사합니다. 패키지를 시작할 수 있는 권한을 설정한 후 App-V 클라이언트는 가상 환경을 만들고, 필요한 모든 데이터 스트리밍을 시작하고, 가상 환경을 만드는 동안 적절한 매니페스트 및 배포 구성 파일을 적용합니다. 특정 패키지 및 응용 프로그램에 대해 가상 환경을 만들어 구성하면 응용 프로그램이 시작됩니다.

**App-V 응용 프로그램을 시작 하는 방법**

1.  사용자가 바로 가기 또는 파일 형식 호출을 클릭하여 응용 프로그램을 실행합니다.

2.  App-V 클라이언트는 사용자 카탈로그에 다음 파일이 있는지 확인

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  파일이 있는 경우 응용 프로그램은 해당 특정 사용자에 대한 자격을 가지며 응용 프로그램은 시작 프로세스를 시작하게 됩니다. 현재 네트워크 트래픽이 없습니다.

4.  다음으로 App-V 클라이언트는 App-V 클라이언트 서비스에 등록된 패키지의 경로가 레지스트리에 있는지 검사합니다.

5.  패키지 저장소 경로를 찾을 때 가상 환경이 만들어집니다. 첫 실행인 경우 기본 기능 블록이 있는 경우 다운로드됩니다.

6.  다운로드 후 App-V 클라이언트 서비스는 매니페스트 및 배포 구성 파일을 통해 가상 환경을 구성하고 모든 App-V 하위 시스템이 로드됩니다.

7.  응용 프로그램이 실행됩니다. 패키지 저장소의 누락된 파일(스파스 파일)에 대해 App-V는 필요한 경우 파일을 스트림 폴트합니다.

    ![패키지에 파일 및 레지스트리 데이터 추가 - 스트림.](images/packageaddfileandregistrydata-stream.png)

### <a name="upgrading-an-app-v-package"></a>App-V 패키지 업그레이드

App-V 5 패키지 업그레이드 프로세스는 이전 버전의 App-V와 다릅니다. App-V는 다른 사용자에게 자격이 있는 컴퓨터의 여러 버전의 동일한 패키지를 지원합니다. 패키지 저장소 및 카탈로그가 새 리소스로 업데이트될 때 패키지 버전을 추가할 수 있습니다. 새 버전 리소스 추가와 관련한 유일한 프로세스는 저장소 최적화입니다. 업그레이드하는 동안 새 파일만 새 버전 저장소 위치에 추가하고 변경되지 않은 파일에 대해 하드 링크가 만들어집니다. 이렇게 하면 파일을 한 디스크 위치에만 표시한 다음 디스크에 파일 위치 항목이 있는 모든 폴더로 투영하여 전체 저장소가 줄어듭니다. App-V 패키지 업그레이드의 구체적인 세부 정보는 다음과 같습니다.

**App-V 패키지를 업그레이드하는 방법**

1.  App-V 클라이언트는 새로 고침 게시를 수행하고 최신 버전의 App-V 패키지를 검색합니다.

2.  패키지 항목이 새 버전에 적합한 카탈로그에 추가됩니다.

    1.  사용자 대상 패키지: UserDeploymentConfiguration.xml UserManifest.xml 및 는 appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID의 사용자 카탈로그에 있는 컴퓨터의 컴퓨터로 배치됩니다.

    2.  컴퓨터 대상(전역) 패키지: UserDeploymentConfiguration.xml %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID의 컴퓨터 카탈로그에 배치됩니다.

3.  HKLM\\Software\\Microsoft\\AppV\\MAV에서 사용자에 대한 커널 모드 드라이버로 패키지를 등록합니다.

4.  통합 작업을 수행합니다.

    -   매니페스트 및 동적 구성 파일의 EP(확장 지점)를 통합합니다.

    1.  파일 기반 EP 데이터는 패키지 저장소의 정크 지점을 활용하는 AppData 폴더에 저장됩니다.

    2.  버전 1 EP는 새 버전을 사용할 수 있을 때 이미 있습니다.

    3.  확장 지점은 최신 또는 업데이트된 확장 지점에 대한 컴퓨터 또는 사용자 카탈로그의 버전 2 위치로 전환됩니다.

5.  게시 타이밍을 대상으로 하는 스크립트를 실행합니다.

6.  필요한 경우 나란히 어셈블리를 설치합니다.

### <a name="upgrading-an-in-use-app-v-package"></a>사용 중인 App-V 패키지 업그레이드

**App-V 5 SP2부터:** 최종 사용자가 사용 중인 패키지를 업그레이드하려고 시도하면 업그레이드 작업이 보류 중 상태가 됩니다. 업그레이드는 다음 규칙에 따라 나중에 실행됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 유형</th>
<th align="left">적용 가능한 규칙</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업(예: 사용자에게 패키지 게시)</p></td>
<td align="left"><p>보류 중인 작업은 사용자가 로그오프한 후 다시 로그온한 후에 수행됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업(예: 연결 그룹을 전역으로 사용)</p></td>
<td align="left"><p>컴퓨터가 종료된 다음 다시 시작될 때 보류 중인 작업이 수행됩니다.</p></td>
</tr>
</tbody>
</table>

 

작업이 보류 중 상태가면 App-V 클라이언트는 다음과 같이 보류 중인 작업에 대한 레지스트리 키도 생성합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용자 기반 또는 전역 기반 작업</th>
<th align="left">레지스트리 키가 생성되는 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업</p></td>
<td align="left"><p>KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

사용자가 최신 버전의 패키지를 사용하려면 먼저 다음 작업을 완료해야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>컴퓨터에 패키지 추가</p></td>
<td align="left"><p>이 작업은 컴퓨터 관련 작업으로 위의 패키지 추가 섹션에 있는 단계를 완료하여 원하는 대로 수행할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 게시</p></td>
<td align="left"><p>단계는 위의 패키지 게시 섹션을 참조하세요. 이 프로세스를 수행하려면 시스템에서 확장 지점을 업데이트해야 합니다. 이 작업을 완료하면 최종 사용자가 응용 프로그램을 사용할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

다음 예제 시나리오를 패키지 업데이트 가이드로 사용하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">시나리오</th>
<th align="left">요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>업그레이드할 때 App-V 패키지가 사용되지 않습니다.</p></td>
<td align="left"><p>가상 응용 프로그램, COM 서버 또는 셸 확장과 같은 패키지 구성 요소를 사용할 수 없습니다.</p>
<p>관리자는 최신 버전의 패키지를 게시하고 다음에 패키지 내부의 구성 요소 또는 응용 프로그램을 시작하면 업그레이드가 작동합니다. 새 버전의 패키지가 스트리밍 및 실행됩니다. 이 시나리오에서는 App-V 5 SP2의 이전 릴리스 App-V 5에서 변경된 것이 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리자가 최신 버전의 패키지를 게시할 때 App-V 패키지가 사용 중임</p></td>
<td align="left"><p>업그레이드 작업은 App-V Client에서 보류 중으로 설정되어 있습니다. 즉, 패키지를 사용하지 않을 때 나중에 대기하고 수행됩니다.</p>
<p>패키지 응용 프로그램이 사용 중이면 사용자가 가상 응용 프로그램을 종료하고 나면 업그레이드가 발생할 수 있습니다.</p>
<p>패키지에 셸 확장(Office 2013)이 있는 경우 Windows 탐색기를 통해 영구적으로 로드되는 사용자는 로그인할 수 없습니다. 사용자는 App-V 패키지 업그레이드를 시작하려면 로그오프했다가 다시 로그인해야 합니다.</p></td>
</tr>
</tbody>
</table>

 

### <a name="global-vs-user-publishing"></a>전역 및 사용자 게시

App-V 패키지는 두 가지 방법 중 하나를 사용하여 게시할 수 있습니다. 특정 사용자 또는 사용자 그룹에 대해 App-V 패키지를 사용할 자격이 있는 사용자 및 컴퓨터의 모든 사용자에 대해 App-V 패키지를 전체 컴퓨터로 권한을 부여하는 Global입니다. 패키지 업그레이드를 연 후 App-V 패키지를 사용하지 않는 경우 다음 두 가지 유형의 게시를 고려하세요.

-   **전역으로 게시:** 응용 프로그램이 컴퓨터로 게시됩니다. 해당 컴퓨터의 모든 사용자가 사용할 수 있습니다. 업그레이드는 App-V 클라이언트 서비스가 시작될 때 실행됩니다. 즉, 컴퓨터를 다시 시작하게 됩니다.

-   **게시된 사용자:** 응용 프로그램이 사용자에게 게시됩니다. 컴퓨터의 사용자가 여러 명인 경우 응용 프로그램을 사용자의 하위 집합에 게시할 수 있습니다. 업그레이드는 사용자가 로그인하거나 다시 게시될 때(주기적으로, ConfigMgr 정책 새로 고침 및 평가 또는 App-V 주기적 게시/새로 고침 또는 PowerShell 명령을 통해 명시적으로) 진행됩니다.

### <a name="removing-an-app-v-package"></a>App-V 패키지 제거

전체 인프라에서 App-V 응용 프로그램을 제거하는 것은 게시되지 않은 작업으로, 패키지 제거를 수행하지 않습니다. 프로세스는 위의 게시 프로세스와 동일하지만 제거 프로세스를 추가하는 대신 App-V 패키지에 적용된 변경 내용을 되돌리게 됩니다.

### <a name="repairing-an-app-v-package"></a>App-V 패키지 복구

복구 작업은 매우 간단하지만 컴퓨터의 여러 위치에 영향을 줄 수 있습니다. 앞서 언급한 COW(기록 중 복사) 위치가 제거되고 확장 지점이 통합되지 않은 후 다시 통합됩니다. COW 데이터 배치 위치를 검토하여 레지스트리에 등록된 위치를 검토하세요. 이 작업은 자동으로 수행되며 App-V 클라이언트 콘솔에서 또는 PowerShell(Repair-AppVClientPackage)을 통해 복구 작업을 시작하는 것 외의 관리 제어는 없습니다.

## <a name="integration-of-app-v-packages"></a><a href="" id="bkmk-integr-appv-pkgs"></a>App-V 패키지 통합


App-V 클라이언트 및 패키지 아키텍처는 패키지를 추가하고 게시하는 동안 로컬 운영 체제와 특정 통합을 제공합니다. 세 개의 파일은 App-V 패키지에 대한 통합 또는 확장점을 정의합니다.

-   AppXManifest.xml: 패키지 저장소 및 사용자 프로필에 저장된 변경 복사본을 사용하여 패키지 내부에 저장됩니다. 시차 프로세스 중에 만들어진 옵션이 들어 있습니다.

-   DeploymentConfig.xml: 컴퓨터 및 사용자 기반 통합 확장 지점의 구성 정보를 제공합니다.

-   UserConfig.xml: Deploymentconfig.xml 구성만 제공하며 사용자 기반 확장 지점만 대상으로 하는 하위 집합입니다.

### <a name="rules-of-integration"></a>통합 규칙

App-V 응용 프로그램이 App-V 클라이언트를 통해 컴퓨터에 게시되는 경우 아래 목록에 설명된 바와 같이 몇 가지 특정 작업이 수행됩니다.

-   전역 게시: 바로 가기가 모든 사용자 프로필 위치에 저장되고 다른 확장 지점은 HKLM hive의 레지스트리에 저장됩니다.

-   사용자 게시: 바로 가기가 현재 사용자 계정 프로필에 저장되고 다른 확장 지점은 HKCU hive의 레지스트리에 저장됩니다.

-   백업 및 복원: 기존 네이티브 응용 프로그램 데이터 및 레지스트리(예: FTA 등록)가 게시 중에 백업됩니다.

    1.  App-V 패키지는 마지막으로 게시된 App-V 응용 프로그램에 소유권이 전달되는 마지막 통합 패키지를 기반으로 소유권이 부여됩니다.

    2.  소유 App-V 패키지가 게시되지 않은 경우 소유권이 App-V 패키지에서 다른 패키지로 이전됩니다. 이렇게 하면 데이터 또는 레지스트리의 복원이 시작되지 않습니다.

    3.  확장 지점에 따라 마지막 패키지가 게시되지 않은 경우 또는 제거될 때 백업된 데이터를 복원합니다.

### <a name="extension-points"></a>확장점

App-V 게시 파일(매니페스트 및 동적 구성)은 응용 프로그램이 로컬 운영 체제와 통합될 수 있도록 하는 여러 확장 지점을 제공합니다. 이러한 확장 지점은 바로 가기 배치, 파일 형식 연결 만들기 및 구성 요소 등록과 같은 일반적인 응용 프로그램 설치 작업을 수행합니다. 기존 응용 프로그램과 동일한 방식으로 설치되지 않는 가상화된 응용 프로그램인 경우 몇 가지 차이점이 있습니다. 다음은 이 섹션에서 다루는 확장점 목록입니다.

-   바로 가기

-   파일 형식 연결

-   셸 확장

-   COM

-   소프트웨어 클라이언트

-   응용 프로그램 기능

-   URL 프로토콜 처리기

-   AppPath

-   가상 응용 프로그램

### <a name="shortcuts"></a>바로 가기

짧은 잘라 내는 OS와의 통합의 기본 요소 중 하나이자 App-V 응용 프로그램을 직접 실행하기 위한 인터페이스입니다. App-V 응용 프로그램을 게시 및 게시하는 동안

패키지 매니페스트 및 동적 구성 XML 파일에서 특정 응용 프로그램 실행 파일의 경로는 다음과 같은 섹션에서 찾을 수 있습니다.

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

앞서 설명한 것 처럼 App-V 바로 가기 키는 새로 고침 작업에 따라 사용자 프로필에 기본적으로 배치됩니다. 전역 새로 고침은 모든 사용자 프로필에 바로 가기를 저장하고 사용자 새로 고침은 해당 바로 가기를 특정 사용자 프로필에 저장합니다. 실제 실행 파일은 패키지 저장소에 저장됩니다. ICO 파일의 위치는 App-V 패키지의 토큰화된 위치입니다.

### <a name="file-type-associations"></a>파일 형식 연결

App-V 클라이언트는 게시 중에 로컬 운영 체제 파일 형식 연결(사용자가 파일 형식 호출을 사용하거나 특별히 등록된 확장명(.docx)을 사용하여 App-V 응용 프로그램을 시작할 수 있도록 합니다. 파일 형식 연결은 아래 예제와 같은 매니페스트 및 동적 구성 파일에 있습니다.

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

**참고**  
이 예에는 다음이 해당됩니다.

-   `<Name>.xdp</Name>` 은 확장명입니다.

-   `<Name>AcroExch.XDPDoc</Name>` 은 ProgId 값입니다(이 값은 Adjoining ProgId를 포인트)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` 은 응용 프로그램 실행을 포인트로 하는 명령줄입니다.

 

### <a name="shell-extensions"></a>셸 확장

셸 확장은 시맨싱 프로세스 중에 패키지에 자동으로 포함되어 있습니다. 패키지가 전역으로 게시되면 셸 확장은 응용 프로그램이 로컬로 설치된 경우와 동일한 기능을 사용자에게 제공합니다. 셸 확장 기능을 사용하도록 설정하기 위해 클라이언트에서 응용 프로그램을 추가로 설정하거나 구성할 필요는 없습니다.

**셸 확장 사용에 대한 요구 사항:**

-   포함된 셸 확장이 포함된 패키지는 전역으로 게시해야 합니다.

-   응용 프로그램, Sequencer 및 App-V 클라이언트의 "비트 수"가 일치해야 합니다. 또는 셸 확장이 작동하지 않습니다. 예를 들어 다음과 같은 가치를 제공해야 합니다.

    -   응용 프로그램의 버전은 64비트입니다.

    -   Sequencer가 64비트 컴퓨터에서 실행되고 있습니다.

    -   패키지가 64비트 App-V 클라이언트 컴퓨터로 배달됩니다.

다음 표에는 지원되는 셸 확장이 표시됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">처리기</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>상황에 맞는 메뉴 처리기</p></td>
<td align="left"><p>상황에 맞는 메뉴에 메뉴 항목을 추가합니다. 이 호출은 상황에 맞는 메뉴가 표시되기 전에 호출됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>끌어서 놓기 처리기</p></td>
<td align="left"><p>마우스 오른쪽 단추로 끌어서 놓기 시 작업을 제어하고 나타나는 상황에 맞는 메뉴를 수정합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>대상 처리기 놓기</p></td>
<td align="left"><p>파일과 같은 놓기 대상 위에 데이터 개체를 끌어 놓은 후의 작업을 제어합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>데이터 개체 처리기</p></td>
<td align="left"><p>파일을 클립보드에 복사하거나 놓기 대상 위에 끌어 놓은 후의 작업을 제어합니다. 놓기 대상에 추가 클립보드 형식을 제공할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>속성 시트 처리기</p></td>
<td align="left"><p>개체의 속성 시트 대화 상자에 페이지를 바꾸거나 추가합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotip 처리기</p></td>
<td align="left"><p>항목에 대한 플래그 및 정보tip 정보를 검색하고 마우스로 마우스를 띄우면 팝업 도구tip 안에 표시할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>열 처리기</p></td>
<td align="left"><p>탐색기 세부 정보 보기에서 사용자 지정 열을 Windows <em> 수 </em> 있습니다. 정렬 및 그룹을 확장하는 데 사용할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>미리 보기 처리기</p></td>
<td align="left"><p>파일 미리 보기가 탐색기 미리 보기 창에 Windows 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### <a name="com"></a>COM

App-V 클라이언트는 COM 통합 및 가상화를 지원하는 게시 응용 프로그램을 지원합니다. COM 통합을 통해 App-V 클라이언트는 로컬 운영 체제에 COM 개체를 등록하고 개체의 가상화를 할 수 있습니다. 이 문서에서는 COM 개체의 통합을 위해 추가 세부 정보가 필요합니다.

App-V는 패키지의 COM 개체를 Out-of-process 및 In-process의 두 가지 프로세스 유형으로 로컬 운영 체제에 등록할 수 있습니다. COM 개체 등록은 해제, 격리 및 통합을 포함하는 특정 App-V 패키지에 대해 하나 또는 여러 작업 모드의 조합으로 수행됩니다. 통합 모드는 Out-of-process 또는 In-process 유형에 대해 구성됩니다. COM 모드 및 형식의 구성은 동적 구성 파일(deploymentconfig.xml 또는 userconfig.xml.

App-V 통합에 대한 자세한 내용은 에서 사용할 수 <https://go.microsoft.com/fwlink/?LinkId=392834> 있습니다.

### <a name="software-clients-and-application-capabilities"></a>소프트웨어 클라이언트 및 응용 프로그램 기능

App-V는 운영 체제의 소프트웨어 클라이언트에 가상화된 응용 프로그램을 등록할 수 있도록 하는 특정 소프트웨어 클라이언트 및 응용 프로그램 기능 확장 지점을 지원합니다. 이를 통해 사용자는 전자 메일, 인스턴트 메시징 및 미디어 플레이어와 같은 작업에 대한 기본 프로그램을 선택할 수 있습니다. 이 작업은 프로그램 액세스 및 컴퓨터 기본값 설정이 있는 제어판에서 수행하고 매니페스트 또는 동적 구성 파일에서 시차를 지정하는 동안 구성됩니다. 응용 프로그램 기능은 App-V 응용 프로그램이 전역적으로 게시될 때만 지원됩니다.

App-V 기반 메일 클라이언트의 소프트웨어 클라이언트 등록 예

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

**참고**  
이 예에는 다음이 해당됩니다.

-   `<ClientConfiguration EmailEnabled="true" />` 전자 메일 클라이언트를 통합하기 위한 전체 소프트웨어 클라이언트 설정

-   `<EMail MakeDefault="true">` 은 특정 전자 메일 클라이언트를 기본 전자 메일 클라이언트로 설정하는 플래그입니다.

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` 는 MAPI dll 등록입니다.

 

### <a name="url-protocol-handler"></a>URL 프로토콜 처리기

응용 프로그램이 항상 파일 형식 호출을 활용하는 가상화된 응용 프로그램이라고 하지는 않습니다. 예를 들어 문서 또는 웹 페이지 내부의 링크에 mailto 추가를 지원하는 응용 프로그램에서 사용자는 mailto: 링크를 클릭하고 등록된 메일 클라이언트를 얻게 됩니다. App-V는 로컬 운영 체제를 사용하여 패키지당 등록할 수 있는 URL 프로토콜 처리기입니다. 시차를 지정하는 동안 URL 프로토콜 처리기도 패키지에 자동으로 추가됩니다.

특정 URL 프로토콜 처리기 등록할 수 있는 응용 프로그램이 두 개 이상 있는 경우 동적 구성 파일을 사용하여 동작을 수정하고 기본 응용 프로그램을 시작하지 말아야 하는 응용 프로그램에 대해 이 기능을 표시하거나 사용하지 않도록 설정할 수 있습니다.

### <a name="apppath"></a>AppPath

AppPath 확장 지점은 운영 체제에서 직접 App-V 응용 프로그램을 호출할 수 있습니다. 일반적으로 이 작업은 운영 체제에 따라 실행 또는 시작 화면에서 수행됩니다. 이를 통해 관리자는 실행 프로그램에 대한 특정 경로를 호출하지 않고도 운영 체제 명령 또는 스크립트에서 App-V 응용 프로그램에 액세스할 수 있습니다. 따라서 게시하는 동안 수행되는 시스템 경로 환경 변수를 모든 시스템에서 수정하지 않습니다.

AppPath 확장 지점은 매니페스트 또는 동적 구성 파일에 구성되고 사용자에 대해 게시하는 동안 로컬 컴퓨터의 레지스트리에 저장됩니다. AppPath 검토에 대한 자세한 내용은 <https://go.microsoft.com/fwlink/?LinkId=392835> 을 참조하세요.

### <a name="virtual-application"></a>가상 응용 프로그램

이 하위 시스템은 시차 중에 캡처되는 응용 프로그램 목록을 제공합니다. 이 목록은 일반적으로 다른 App-V 구성 요소에서 사용됩니다. 동적 구성 파일을 사용하여 특정 응용 프로그램에 속한 확장점의 통합을 사용하지 않도록 설정할 수 있습니다. 예를 들어 패키지에 응용 프로그램이 두 개 포함된 경우 다른 응용 프로그램의 확장 지점만 통합할 수 있도록 한 응용 프로그램에 속한 모든 확장 지점을 사용하지 않도록 설정할 수 있습니다.

### <a name="extension-point-rules"></a>확장점 규칙

위에서 설명한 확장 지점은 패키지가 게시된 방식에 따라 운영 체제에 통합됩니다. 전역 게시는 사용자 게시가 사용자 위치에 확장점을 두는 공용 컴퓨터 위치에 확장점을 제공합니다. 예를 들어 바탕 화면에 만들어 전역으로 게시된 바로 가기를 사용하면 바로 가기(%Public%\\Desktop) 및 레지스트리 데이터(HKLM\\Software\\Classes)에 대한 파일 데이터가 생성됩니다. 동일한 바로 가기에는 파일 데이터(%UserProfile%\\Desktop) 및 레지스트리 데이터(HKCU\\Software\\Classes)가 있습니다.

확장 지점이 모두 동일한 방식으로 게시되는 것은 아니며, 일부 확장 지점에는 전역 게시가 필요하고 다른 확장 지점은 전달되는 특정 운영 체제 및 아키텍처에서 시차를 지정해야 합니다. 다음은 이러한 두 가지 주요 규칙을 설명하는 표입니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">가상 확장</th>
<th align="left">대상 OS 시quencing 필요</th>
<th align="left">전역 게시 필요</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>바로 가기</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>파일 형식 연결</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>URL 프로토콜</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppPaths</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>COM 모드</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>소프트웨어 클라이언트</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>응용 프로그램 기능</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>상황에 맞는 메뉴 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>끌어서 놓기 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Data 개체 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>속성 시트 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Infotip 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>열 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>셸 확장</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>브라우저 도우미 개체</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Active X 개체</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a name="dynamic-configuration-processing"></a><a href="" id="bkmk-dynamic-config"></a>동적 구성 처리


App-V 패키지를 한 컴퓨터 또는 사용자에게 배포하는 것은 매우 간단합니다. 그러나 조직이 비즈니스 라인과 지리적 및 정치적 경계에 AppV 응용 프로그램을 배포할 때 한 가지 설정 집합으로 응용 프로그램을 한 번 시퀀서하는 능력은 불가능해집니다. App-V는 매니페스트 파일에서 시차를 지정하는 동안 특정 설정 및 구성을 캡처하지만 동적 구성 파일을 사용하여 수정을 지원하기 때문에 이 시나리오를 위해 디자인되었습니다.

App-V 동적 구성을 사용하면 컴퓨터 수준 또는 사용자 수준에서 패키지에 대한 정책을 지정할 수 있습니다. 동적 구성 파일을 사용하면 시맨싱 엔지니어가 개별 사용자 또는 컴퓨터 그룹의 요구를 해결하기 위해 패키지의 구성(사후 시맨싱)을 수정할 수 있습니다. 경우에 따라 App-V 환경 내에서 적절한 기능을 제공하기 위해 응용 프로그램을 수정해야 할 수 있습니다. 예를 들어 \_\*config.xml 파일을 수정하여 mailto 확장명을 사용 중지하여 가상화된 응용 프로그램에서 다른 응용 프로그램의 확장명을 덮어들이지 않도록 하는 등 응용 프로그램 실행 중에 특정 작업이 수행될 수 있도록 허용해야 할 수 있습니다.

App-V 패키지에는 appv 패키지 파일 내부에 매니페스트 파일이 포함되어 있으며, 이는 시차 작업을 나타내며 동적 구성 파일이 특정 패키지에 할당되지 않는 한 선택 정책입니다. 사후 시차를 통해 동적 구성 파일을 수정하여 응용 프로그램을 다른 데스크톱 또는 다른 확장 지점의 사용자에게 게시할 수 있습니다. 두 동적 구성 파일은 DDC(동적 배포 구성) 및 DUC(동적 사용자 구성) 파일입니다. 이 섹션에서는 매니페스트 및 동적 구성 파일의 조합에 대해 중점적으로 설명합니다.

### <a name="example-for-dynamic-configuration-files"></a>동적 구성 파일의 예

아래 예제에서는 게시 후 및 정상 작동 중에 매니페스트, 배포 구성 및 사용자 구성 파일의 조합을 보여 주며, 이러한 예제는 각 파일의 약어 예제입니다. 각 파일에서 사용할 수 있는 특정 범주에 대한 전체 설명이 아닌 파일의 조합만 보여 주기 위한 것입니다. 자세한 내용은 다음에서 App-V 5 시연 가이드를 참조하세요. <https://go.microsoft.com/fwlink/?LinkID=269810>

**매니페스트**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**배포 구성**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**사용자 구성**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a name="side-by-side-assemblies"></a><a href="" id="bkmk-sidebyside-assemblies"></a>나란히 어셈블리


App-V는 가상 응용 프로그램 게시 중에 시차를 지정하고 클라이언트에서 배포하는 동안 SxS(Side-by-Side) 어셈블리의 자동 패키징을 지원합니다. App-V 5 SP2는 시덱싱하는 머신에 없는 어셈블리에 대해 시차 중에 SxS 어셈블리 캡처를 지원합니다. 또한 Visual C++(버전 8 이상) 및/또는 MSXML 런타임으로 구성된 어셈블리의 경우 Sequencer는 모니터링 중에 설치되지 않은 경우에도 이러한 종속을 자동으로 검색하고 캡처합니다. 나란히 어셈블리 기능을 사용하면 App-V Sequencer가 이미 시퀀싱하는 Workstation에 이미 있는 어셈블리를 캡처하지 않은 이전 버전의 App-V와 패키지당 하나의 비트 버전으로 제한되는 어셈블리를 privatizing하는 제한이 제거됩니다. 이 동작으로 인해 필요한 SxS 어셈블리가 없는 클라이언트에 App-V 응용 프로그램이 배포되면 응용 프로그램 시작 오류가 발생합니다. 이렇게 하면 패키징 프로세스가 문서화된 다음 패키지에 필요한 모든 어셈블리가 가상 응용 프로그램에 대한 지원을 보장하기 위해 사용자의 클라이언트 운영 체제에 로컬로 설치되도록 합니다. 어셈블리 수와 필요한 종속성에 대한 응용 프로그램 설명서가 부족한 경우를 기준으로 이 작업은 관리 및 구현 문제 모두에 해당했습니다.

App-V의 나란히 어셈블리 지원에는 다음과 같은 기능이 있습니다.

-   시차 작업 중에 SxS 어셈블리의 자동 캡처(어셈블리가 시차용 작업소에 이미 설치되어 있는지 여부에 관계 없이)

-   App-V 클라이언트는 필수 SxS 어셈블리가 없는 경우 게시 시 클라이언트 컴퓨터에 자동으로 설치합니다.

-   Sequencer는 Sequencer 보고 메커니즘에서 VC 런타시 종속성에 대한 보고를 합니다.

-   Sequencer를 사용하면 이미 Sequencer에 설치된 어셈블리를 패키지로 지정하지 않을 수 있습니다. 그러면 이전에 대상 컴퓨터에 어셈블리가 설치된 시나리오를 지원합니다.

### <a name="automatic-publishing-of-sxs-assemblies"></a>SxS 어셈블리 자동 게시

SxS 어셈블리를 통해 App-V 패키지를 게시하는 동안 App-V 클라이언트는 컴퓨터의 어셈블리가 존재하는지 검사합니다. 어셈블리가 없는 경우 클라이언트는 어셈블리를 컴퓨터로 배포합니다. 연결 그룹의 일부인 패키지는 기본 패키지에 포함된 Side by Side 어셈블리 설치를 사용하게 됩니다. 연결 그룹에는 어셈블리 설치에 대한 정보가 포함되지 않습니다.

**참고**  
어셈블리가 있는 패키지를 게시하거나 제거하면 해당 패키지에 대한 어셈블리가 제거되지 않습니다.

 

## <a name="client-logging"></a><a href="" id="bkmk-client-logging"></a>클라이언트 로깅


App-V 클라이언트는 표준 ETW Windows 로그에 정보를 기록합니다. 특정 App-V 이벤트는 이벤트 뷰어의 응용 프로그램 및 서비스 로그\\Microsoft\\AppV\\Client에서 찾을 수 있습니다.

**참고**  
App-V 5.0 SP3에서는 일부 로그가 통합되고 다음 위치로 이동했습니다.

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

이동된 로그 목록은 [App-V 5.0 SP3 정보를 참조하세요.](about-app-v-50-sp3.md#bkmk-event-logs-moved)

 

아래에 설명된 세 가지 이벤트 범주가 있습니다.

**관리자:** App-V 클라이언트에 적용되는 구성에 대한 이벤트를 기록하고 기본 경고 및 오류를 포함

**작업:** App-V 클라이언트에서 완료된 App-V 작업의 감사 로그를 만드는 개별 구성 요소의 일반적인 App-V 실행 및 사용을 기록합니다.

**가상 응용 프로그램:** 가상 응용 프로그램 시작 및 가상화 하위 시스템 사용을 기록합니다.






 

 





