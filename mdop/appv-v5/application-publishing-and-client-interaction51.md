---
title: 응용 프로그램 게시 및 클라이언트 상호 작용
description: 응용 프로그램 게시 및 클라이언트 상호 작용
author: dansimp
ms.assetid: 36a4bf6f-a917-41a6-9856-6248686df352
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 69fcf119faaf35e53ae36f386bcb3480e2ee3b0e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814732"
---
# 응용 프로그램 게시 및 클라이언트 상호 작용


이 문서에서는 일반적인 App-v 클라이언트 작업 및 로컬 운영 체제와의 통합에 대 한 기술 정보를 제공 합니다.

-   [Sequencer에서 만든 앱-V 패키지 파일](#bkmk-appv-pkg-files-list)

-   [Appv 파일에는 무엇이 있나요?](#bkmk-appv-file-contents)

-   [App-v 클라이언트 데이터 저장소 위치](#bkmk-files-data-storage)

-   [패키지 레지스트리](#bkmk-pkg-registry)

-   [앱-V 패키지 저장소 동작](#bkmk-pkg-store-behavior)

-   [로밍 레지스트리 및 데이터](#bkmk-roaming-reg-data)

-   [앱-V 클라이언트 응용 프로그램 수명 주기 관리](#bkmk-clt-app-lifecycle)

-   [앱-V 패키지의 통합](#bkmk-integr-appv-pkgs)

-   [동적 구성 처리](#bkmk-dynamic-config)

-   [Side-by-side 어셈블리](#bkmk-sidebyside-assemblies)

-   [클라이언트 로깅](#bkmk-client-logging)

참조에 대 한 자세한 내용은 [Microsoft app-v (Application Virtualization) 설명서 리소스 다운로드 페이지](https://www.microsoft.com/download/details.aspx?id=27760)를 참조 하세요.

## <a href="" id="bkmk-appv-pkg-files-list"></a>Sequencer에서 만든 앱-V 패키지 파일


시퀀서는 App-v 패키지를 만들고 가상화 된 응용 프로그램을 생성 합니다. 시퀀싱 프로세스는 다음 파일을 만듭니다.

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
<td align="left"><p>appv</p></td>
<td align="left"><ul>
<li><p>시퀀싱 프로세스의 캡처한 자산과 상태 정보를 포함 하는 기본 패키지 파일입니다.</p></li>
<li><p>전달 시 컴퓨터와 특정 사용자에 게 다시 적용할 수 있는 토큰화 된 형식의 패키지 파일, 게시 정보 및 레지스트리 아키텍처</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>. MSI</p></td>
<td align="left"><p>수동으로 또는 타사 배포 플랫폼을 사용 하 여 appv 파일을 배포 하는 데 사용할 수 있는 실행 가능 배포 래퍼입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>App-v 클라이언트를 실행 하는 컴퓨터의 모든 사용자에 게 전역으로 배포 되는 패키지의 모든 응용 프로그램에 대 한 기본 게시 매개 변수를 사용자 지정 하는 데 사용 되는 파일입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>App-v 클라이언트를 실행 하는 컴퓨터에서 특정 사용자에 게 배포 되는 패키지의 모든 응용 프로그램에 대 한 게시 매개 변수를 사용자 지정 하는 데 사용 되는 파일입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>생략 된 드라이버, 파일, 레지스트리 위치를 포함 하 여 시퀀싱 프로세스에서 발생 하는 메시지에 대 한 요약입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>.CAB</p></td>
<td align="left"><p><em>선택 사항: </em> 이전에 시퀀싱 된 가상 응용 프로그램 패키지를 자동으로 다시 작성 하는 데 사용 되는 패키지 가속기 파일</p></td>
</tr>
<tr class="odd">
<td align="left"><p>. appvt</p></td>
<td align="left"><p><em>선택 사항: </em> 일반적으로 재사용 되는 sequencer 설정을 유지 하는 데 사용 되는 sequencer 템플릿 파일입니다.</p></td>
</tr>
</tbody>
</table>

 

시퀀싱에 대 한 자세한 내용은 [응용 프로그램 가상화 순서 가이드](https://go.microsoft.com/fwlink/?LinkID=269810)를 참조 하세요.

## <a href="" id="bkmk-appv-file-contents"></a>Appv 파일에는 무엇이 있나요?


Appv 파일은 XML 및 XML이 아닌 파일을 단일 엔터티에 함께 저장 하는 컨테이너입니다. 이 파일은 OPC 형식을 사용 하 여 작성 됩니다 (기본적으로 제공 되는 패키징 규칙) 표준에 기반을 둔 것입니다.

Appv 파일 콘텐츠를 보려면 패키지 복사본을 만든 다음 복사 된 파일의 이름을 ZIP 확장명으로 바꿉니다.

Appv 파일에는 가상 응용 프로그램을 만들고 게시할 때 사용 되는 다음 폴더와 파일이 포함 됩니다.

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
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>루트</p></td>
<td align="left"><p>파일 폴더</p></td>
<td align="left"><p>시퀀싱 하는 동안 캡처한 가상화 된 응용 프로그램의 파일 시스템을 포함 하는 디렉터리입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types]. xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>Appv 파일의 핵심 콘텐츠 형식 (예: DLL, EXE, BIN)의 목록입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>App-v 패키지에서 파일의 위치 및 유효성 검사를 가능 하 게 하는 File, Block 및 BlockMap 요소를 사용 하는 appv 파일의 레이아웃입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>패키지를 추가, 게시 및 실행 하는 데 필요한 정보를 포함 하는 패키지에 대 한 메타 데이터입니다. 확장명 점 (파일 형식 연결 및 바로 가기)과 패키지와 연결 된 이름 및 Guid가 포함 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>특성 (예: 디렉터리, 파일, 불투명 한 디렉터리, 빈 디렉터리 및 긴 이름과 짧은 이름)을 포함 하 여 시퀀싱 하는 동안 캡처한 파일의 목록입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>시퀀싱 컴퓨터 (운영 체제 버전, Internet Explorer 버전, .Net Framework 버전) 및 프로세스 (업그레이드, 패키지 버전)에 대 한 정보입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>레지스트리 .dat</p></td>
<td align="left"><p>DAT 파일</p></td>
<td align="left"><p>패키지에 대 한 시퀀싱 프로세스 중에 캡처한 레지스트리 키 및 값</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>XML 파일</p></td>
<td align="left"><p>기본 및 게시 기능 블록에 대 한 파일 목록입니다. 게시 기능 블록에는 패키지를 게시 하는 데 필요한 .ICO 파일 및 파일의 필수 부분 (EXE 및 DLL)이 포함 되어 있습니다. 제공 되는 경우 기본 기능 블록에는 시퀀싱 프로세스 중에 스트리밍을 위해 최적화 된 파일이 포함 됩니다.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a>App-v 클라이언트 데이터 저장소 위치


App-v 클라이언트는 가상 응용 프로그램이 제대로 실행 되 고 로컬에 설치 된 응용 프로그램 처럼 작동 하도록 하는 작업을 수행 합니다. 가상 응용 프로그램을 열고 실행 하는 프로세스는 응용 프로그램에 사용자가 기대 하는 기존 응용 프로그램의 필수 구성 요소가 있는지 확인 하기 위해 가상 파일 시스템 및 레지스트리의 매핑을 필요로 합니다. 이 섹션에서는 가상 응용 프로그램을 실행 하는 데 필요한 자산에 대해 설명 하 고 App-v에서 자산을 저장 하는 위치를 나열 합니다.

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
<td align="left"><p>컴퓨터 단위 구성 문서 포함</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 카탈로그</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>사용자별 구성 문서 포함</p></td>
</tr>
<tr class="even">
<td align="left"><p>바로 가기 백업</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>패키지 게시 취소에서 복원을 가능 하 게 하는 이전 통합 지점을 저장 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>쓰기 시 복사 (COW) 로밍</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>패키지 수정에 대 한 쓰기 가능한 로밍 위치</p></td>
</tr>
<tr class="even">
<td align="left"><p>COW (기록 시 복사) 로컬</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>패키지 수정에 대해 쓰기 가능한 비 로밍 위치</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 레지스트리</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>컴퓨터 또는 전역적으로 게시 된 패키지 (컴퓨터 하이브)에 대 한 VReg를 포함 하 여 패키지 상태 정보를 포함 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>사용자 레지스트리</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>VReg를 포함 하는 사용자 패키지 상태 정보를 포함 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 레지스트리 클래스</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>추가 사용자 패키지 상태 정보를 포함 합니다.</p></td>
</tr>
</tbody>
</table>

 

표에 대 한 추가 세부 정보는이 문서의 아래 섹션 및 전체에서 제공 됩니다.

### 패키지 저장소

앱-V 클라이언트는 패키지 저장소에 탑재 된 응용 프로그램 자산을 관리 합니다. 이 기본 저장소 위치는 `%ProgramData%\App-V` 사용자가 `Set-AppVClientConfiguration` 로컬 레지스트리 ( `PackageInstallationRoot` 키 아래의 값)를 수정 하는 PowerShell 명령을 사용 하 여 설정 중에 구성할 수 있습니다 `HKLM\Software\Microsoft\AppV\Client\Streaming` . 패키지 저장소는 클라이언트 운영 체제의 로컬 경로에 위치 해야 합니다. 개별 패키지는 패키지 GUID 및 버전 GUID에 대해 이름이 지정 된 하위 디렉터리의 패키지 저장소에 저장 됩니다.

특정 응용 프로그램 경로의 예:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

설치 하는 동안 패키지 저장소의 기본 위치를 변경 하려면 [App-v 클라이언트를 배포 하는 방법을](how-to-deploy-the-app-v-client-51gb18030.md)참조 하세요.

### 공유 콘텐츠 저장소

공유 콘텐츠 저장소 모드에서 App-v 클라이언트를 구성 하는 경우 스트림 오류가 발생할 때 디스크에 데이터가 기록 되지 않으며,이는 패키지에 최소 로컬 디스크 공간 (데이터 게시)이 필요 함을 의미 합니다. 로컬 저장소를 제한할 수 있는 VDI 환경에서는 디스크 공간을 덜 사용 하는 것이 좋으며, 고성능 네트워크 위치 (SAN 등)에서 응용 프로그램을 스트리밍하는 것이 좋습니다. 공유 콘텐츠 저장소 모드에 대 한 자세한 내용은을 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**참고**  컴퓨터 및 패키지 저장소는 App-v 클라이언트에 대 한 공유 콘텐츠 저장소 구성을 사용 하 고 있는 경우에도 로컬 드라이브에 있어야 합니다.

 

### 패키지 카탈로그

App-v 클라이언트는 다음 두 가지 파일 기반 위치를 관리 합니다.

-   **카탈로그 (사용자 및 컴퓨터).**

-   **레지스트리 위치** -패키지가 게시 대상으로 지정 되는 방식에 따라 달라 집니다. 컴퓨터에 대 한 카탈로그 (데이터 저장소)와 각 개별 사용자에 대 한 카탈로그가 있습니다. 컴퓨터 카탈로그에는 모든 사용자 또는 모든 사용자에 게 적용 되는 전역 정보가 저장 되며, 사용자 카탈로그에는 특정 사용자에 게 적용 되는 정보가 저장 됩니다. Catalog는 동적 구성 및 매니페스트 파일의 컬렉션입니다. 파일 및 레지스트리의 패키지 버전에 대 한 불연속 데이터가 있습니다. 

### 컴퓨터 카탈로그

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>패키지를 추가 하 고 게시할 때 컴퓨터에서 사용자가 사용할 수 있는 패키지 문서를 저장 합니다. 그러나 게시 시 패키지가 "global" 이면 모든 사용자가 통합을 사용할 수 있습니다.</p>
<p>패키지가 전역이 아닌 경우에는 특정 사용자에 대해서만 통합이 게시 되지만, 클라이언트 컴퓨터의 모든 사용자에 게 수정 및 표시 되는 전역 리소스가 남아 있습니다 (예: 패키지 디렉터리는 공유 디스크 위치에 있음).</p>
<p>컴퓨터의 사용자가 패키지를 사용할 수 있는 경우 (전역 또는 비전역) 매니페스트는 컴퓨터 카탈로그에 저장 됩니다. 패키지가 전역으로 게시 되 면 컴퓨터 카탈로그에 저장 된 동적 구성 파일이 있는 것입니다. 따라서 패키지가 전역 인지 여부는 컴퓨터 카탈로그에 UserDeploymentConfiguration file (정책 파일)이 있는지 여부에 따라 결정 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기본 저장소 위치</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>이 위치는 패키지 저장소 위치와 다릅니다. 패키지 저장소는 패키지 파일의 골든 또는 초기 복사본입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>컴퓨터 카탈로그의 파일</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (전역적으로 게시 된 패키지)</p></li>
<li><p>UserDeploymentConfiguration.xml (전역적으로 게시 된 패키지)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>추가 컴퓨터 카탈로그 위치 (패키지가 연결 그룹의 일부인 경우 사용 됨)</p></td>
<td align="left"><p>다음 위치는 위에서 설명한 특정 패키지 위치에 추가 됩니다.</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지가 연결 그룹의 일부인 경우 컴퓨터 카탈로그의 추가 파일</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (전역적으로 게시 된 연결 그룹)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### 사용자 카탈로그

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>게시 프로세스 중에 만들어집니다. 패키지를 게시 하는 데 사용 되는 정보를 포함 하며 패키지를 특정 사용자에 게 프로 비전 하는 데 사용 되기도 합니다. 로밍 위치에서 만들어지고 사용자 관련 게시 정보를 포함 합니다.</p>
<p>사용자에 대 한 패키지를 게시 하면 정책 파일이 사용자 카탈로그에 저장 됩니다. 이와 동시에 매니페스트의 복사본도 사용자 카탈로그에 저장 됩니다. 사용자에 대 한 패키지 자격 자격이 제거 되 면 관련 패키지 파일이 사용자 카탈로그에서 제거 됩니다. 사용자 카탈로그를 보면 관리자가 동적 구성 파일의 존재 여부를 볼 수 있으며,이는 패키지가 해당 사용자에 게 부여 됨을 나타냅니다.</p>
<p>로밍 사용자의 경우 사용자 카탈로그는 로밍 또는 공유 위치에 있어야 기본적으로 대상 사용자의 레거시 App-v 동작을 유지할 수 있습니다. 자격 및 정책은 컴퓨터가 아닌 사용자에 연결 되므로 프로 비전 된 사용자와 로밍 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>기본 저장소 위치</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>사용자 카탈로그의 파일</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml 또는 UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>추가 사용자 카탈로그 위치 (패키지가 연결 그룹의 일부인 경우 사용 됨)</p></td>
<td align="left"><p>다음 위치는 위에서 설명한 특정 패키지 위치에 추가 됩니다.</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>패키지가 연결 그룹의 일부인 경우 컴퓨터 카탈로그의 추가 파일</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### 바로 가기 백업

게시 프로세스 중에 App-v 클라이언트가이 백업에 대 한 바로 가기 및 통합 지점을 백업 하면 `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` 패키지가 게시 취소 될 때 이러한 통합 지점을 이전 버전으로 복원할 수 있습니다.

### 파일 쓰기 시 복사

패키지 저장소에는 게시 서버에서 스트리밍된 패키지 파일의 초기 복사본이 포함 되어 있습니다. App-v 응용 프로그램이 정상적으로 작동 하는 동안 사용자 또는 서비스에서 파일을 변경 해야 할 수 있습니다. 이러한 변경 사항은 해당 응용 프로그램 복구의 기능을 보존 하기 위해 패키지 저장소에서 변경 되지 않으며,이는 이러한 변경을 제거 합니다. 이러한 위치 (COW)는 쓰기 시 복사 (이 하)는 로밍 위치나 비 로밍 위치를 모두 지원 합니다. 수정 내용이 저장 되는 위치는 응용 프로그램이 네이티브 환경에서 변경 내용을 작성 하도록 프로그래밍 된 위치에 따라 달라 집니다.

### COW 로밍

위에서 설명한 COW 로밍 위치는 일반적인% AppData% location 또는 \\Users\\{username}\\AppData\\Roaming 위치를 대상으로 하는 파일 및 디렉터리에 대 한 변경 내용을 저장 합니다. 이러한 디렉터리와 파일은 운영 체제 설정에 따라 roamed.

### COW 지역

COW 로컬 위치는 로밍 위치와 비슷하지만, 로밍 지원이 구성 된 경우에도 디렉터리 및 파일은 다른 컴퓨터에 roamed 되지 않습니다. 위에서 설명한 COW 로컬 위치는 표준 창에 적용 되는 변경 내용을 저장 하며% AppData% 위치는 아닙니다. 나열 된 디렉터리는 다를 수 있지만 일반적인 Windows 위치에는 두 위치 (예: 일반 AppData 및 일반 Appdatdatas)가 있습니다. 해당 **S** 는 가상 서비스가 로그온 한 사용자의 다른 관리자 권한으로 변경을 요청할 때 제한 된 위치를 나타냅니다. 비**S** 위치에는 사용자 기반 변경 내용이 저장 됩니다.

## <a href="" id="bkmk-pkg-registry"></a>패키지 레지스트리


응용 프로그램이 패키지 레지스트리 데이터에 액세스할 수 있으려면 App-v 클라이언트에서 패키지 레지스트리 데이터를 응용 프로그램에서 사용할 수 있도록 설정 해야 합니다. App-v 클라이언트는 모든 레지스트리 데이터에 대 한 백업 저장소로 실제 레지스트리를 사용 합니다.

새 패키지가 App-v 클라이언트에 추가 되 면 레지스트리의 복사본을 만듭니다. DAT 파일이 생성 됩니다 `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . 파일 이름은이 (가) 포함 된 버전 GUID입니다. DAT 확장명. 이 복사본이 만들어지는 이유는 패키지의 실제 하이브 파일을 사용 하지 않도록 하 여 나중에 패키지를 제거 하는 것을 방지 하는 것입니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>패키지 저장소의 레지스트리 .dat</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid} .dat</strong></p></td>
</tr>
</tbody>
</table>

 

패키지의 첫 번째 응용 프로그램이 클라이언트에서 시작 되 면 클라이언트는 하이브 파일의 내용을 단계적으로 진행 하거나 복사 하 여 대체 위치에 패키지 레지스트리 데이터를 다시 만듭니다 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . 준비 된 레지스트리 데이터에는 서로 다른 두 가지 유형의 컴퓨터 데이터와 사용자 데이터가 있습니다. 컴퓨터 데이터는 컴퓨터의 모든 사용자 간에 공유 됩니다. 사용자 데이터는 사용자에 대해 userspecific 위치에 대해 준비 됩니다 `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` . 컴퓨터 데이터는 패키지 제거 시간에 궁극적으로 제거 되며 사용자 데이터는 사용자의 게시 취소 작업에서 제거 됩니다.

### 패키지 레지스트리 준비 및 연결 그룹 레지스트리 준비

연결 그룹이 있는 경우 레지스트리를 준비 하는 이전 프로세스는 true를 유지 하지만, 하이브 파일을 하나 이상 처리 하는 대신 파일은 연결 그룹 XML에 표시 되는 순서 대로 처리 되며 첫 번째 작성자가 충돌을 발생 하 게 됩니다.

준비 된 레지스트리는 단일 패키지 케이스와 동일한 방식으로 유지 됩니다. 사용 하지 않도록 설정 될 때까지 연결 그룹에 대해 준비 된 사용자 레지스트리 데이터가 유지 됩니다. 연결 그룹 제거 시 준비 된 컴퓨터 레지스트리 데이터가 제거 됩니다.

### 가상 레지스트리

가상 레지스트리 (VREG)의 용도는 패키지 레지스트리와 기본 레지스트리를 통합 하 여 응용 프로그램에 병합 된 단일 보기를 제공 하는 것입니다. 또한 가상 프로세스의 컨텍스트에서 레지스트리를 변경한 내용이 별도의 COW 위치에 적용 되는 COW (write on copy) 기능을 제공 합니다. 즉, VREG는 레지스트리 COW-package-네이티브에서 채워진 위치를 기반으로 하는 단일 보기로 최대 세 개의 개별 레지스트리 위치를 결합 해야 합니다 &gt; &gt; . 레지스트리 데이터에 대 한 요청이 이루어지면 요청 된 데이터를 찾을 때까지 순서 대로 검색 됩니다. COW 위치에 저장 된 값이 있는 경우 다른 위치로 진행 되지 않지만 COW 위치에 데이터가 없는 경우에는 해당 데이터를 찾을 때까지 원래 위치로 이동 합니다.

### 레지스트리 위치

두 개의 패키지 레지스트리 위치와 두 개의 연결 그룹 위치가 있는데,이는 패키지가 개별적으로 게시 되었는지 또는 연결 그룹의 일부분에 따라 App-v 클라이언트가 레지스트리 정보를 저장 하는 것입니다. 패키지에는 세 가지 COW 위치, 연결 그룹의 경우 세 가지, 즉 VREG에서 만들고 관리 합니다. 패키지 및 연결 그룹에 대 한 설정은 공유 되지 않습니다.

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
<li><p>기계 Registry\Client\Packages\PkgGUID\REGISTRY (권한 상승 프로세스만 쓰기 가능)</p></li>
<li><p>사용자 로밍 (Registry\Client\Packages\PkgGUID\REGISTRY/수업을 제외한 HKCU에 작성 된 모든 항목</p></li>
<li><p>사용자 레지스트리 Classes\Client\Packages\PkgGUID\REGISTRY (관리자가 아닌 프로세스의 HKCU\Software\Classes 쓰기 및 HKLM)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>패키지</strong></p></td>
<td align="left"><ul>
<li><p>기계 Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>사용자 레지스트리 Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>원본</strong></p></td>
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
<li><p>기계 Registry\Client\PackageGroups\GrpGUID\REGISTRY (권한 상승 프로세스만 쓰기 가능)</p></li>
<li><p>사용자 Registry\Client\PackageGroups\GrpGUID\REGISTRY (\수업을 제외한 HKCU에 기록 된 모든 항목</p></li>
<li><p>사용자 레지스트리 Classes\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>패키지</strong></p></td>
<td align="left"><ul>
<li><p>기계 Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>사용자 레지스트리 Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>원본</strong></p></td>
<td align="left"><ul>
<li><p>기본 응용 프로그램 레지스트리 위치</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

HKLM에는 두 개의 COW 위치가 있습니다. 관리자 권한 및 비관리자 프로세스 관리자 권한 프로세스는 HKLM의 보안 COW에 HKLM 변경 내용을 항상 기록 합니다. 비 권한 프로세스는 항상 HKCU\\Software\\Classes. 아래의 비보안 COW에 HKLM 변경 내용을 기록 합니다. 앱이 HKLM에서 변경 내용을 읽는 경우 관리자 권한 프로세스는 HKLM 아래의 보안 COW 변경 내용을 읽습니다. 두 가지 모두에서 비 권한 읽기는 보안 되지 않은 COW에서 변경한 내용을 먼저 favoring.

### 창구 키

관리자는 창구 키를 사용 하 여 패키지 및 COW 위치를 우회 하 여 네이티브 레지스트리 에서만 읽을 수 있도록 특정 키를 구성할 수 있습니다. 통과 위치는 패키지에 따라 달라 지 며, 키에 대 한 경로를 추가 하 여 구성할 수 있으며, 키의 **PassThroughPaths** 이라고 하는 **REG \ _MULTI \ _SZ** value에 대 한 통과로 처리 되어야 합니다 `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . 이 다중 문자열 값 아래에 표시 되는 모든 키 (하위 항목)는 통과로 처리 됩니다.

다음 위치는 기본적으로 통과 위치로 구성 되어 있습니다.

-   HKEY _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY _CURRENT \ _USER \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet 설정

-   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY _LOCAL \ _MACHINE \\SOFTWARE\\Policies

-   HKEY _CURRENT \ _USER \\SOFTWARE\\Policies

통과 키의 목적은 가상 응용 프로그램이 성공한 작업 또는 통합을 위해 비가상 응용 프로그램에 필요한 VReg의 레지스트리 데이터를 기록 하지 않도록 하는 것입니다. 정책 키를 사용 하면 관리자가 설정한 그룹 정책 기반 설정이 패키지 설정 별로 사용 되지 않도록 할 수 있습니다. Windows 최신 UI 기반 응용 프로그램과 통합 하려면 AppModel 키가 필요 합니다. 관리에서 기본 통과 키를 수정 하지 않는 것이 좋으며 일부 경우에는 응용 프로그램 동작에 따라 추가 통과 키를 추가 해야 할 수 있습니다.

## <a href="" id="bkmk-pkg-store-behavior"></a>앱-V 패키지 저장소 동작


앱-V 5는 패키지 저장소를 관리 하며,이 위치는 appv 파일에서 확장 된 자산 파일이 저장 되는 장소입니다. 기본적으로이 위치 는%app Data%\\app-v에 저장 되며, 사용 가능한 디스크 공간에 의해서만 저장소 용량으로 제한 됩니다. 패키지 저장소는 이전 섹션에서 설명한 대로 패키지 및 버전의 Guid를 기준으로 구성 됩니다.

### 패키지 추가

App-v 패키지는 App-v 클라이언트를 사용 하 여 컴퓨터에 추가 될 때 준비 됩니다. App-v 클라이언트는 주문형 스테이징을 제공 합니다. 게시 또는 수동 추가 AppVClientPackage 경우 데이터 구조는 패키지 저장소 (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID})에 빌드됩니다. StreamMap.xml에 정의 된 게시 블록에서 식별 된 패키지 파일은 시스템에 추가 되 고, 시작 시 적절 한 응용 프로그램 자산을 확보 하기 위해 준비 된 최상위 폴더 및 하위 파일입니다.

### 패키지 탑재

패키지는 PowerShell을 사용 `Mount-AppVClientPackage` 하거나 **APP-V 클라이언트 UI** 를 사용 하 여 패키지를 다운로드 하 여 명시적으로 로드할 수 있습니다. 이 작업은 전체 패키지를 패키지 저장소에 완전히 로드 합니다.

### 스트리밍 패키지

스트리밍의 기본 동작을 변경 하도록 App-v 클라이언트를 구성할 수 있습니다. 모든 스트리밍 정책은 다음 레지스트리 키 아래에 저장 됩니다 `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` . 정책은 PowerShell cmdlet을 사용 하 여 설정 `Set-AppvClientConfiguration` 합니다. 스트리밍에 적용 되는 정책은 다음과 같습니다.

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
<td align="left"><p>Windows 8 이상에서는 3G 및 셀룰러 네트워크를 통해 스트리밍할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>백그라운드 로드 설정을 지정 합니다.</p>
<p><strong>0 </strong> - 사용 안 함</p>
<p><strong>1 </strong> – 이전에 사용한 패키지만 사용</p>
<p><strong>2 </strong> – 모든 패키지</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Package설치 루트</p></td>
<td align="left"><p>로컬 컴퓨터에 있는 패키지 저장소의 루트 폴더</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>패키지를 스트리밍할 위치 루트 재정의</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>VDI 시나리오에 공유 콘텐츠 저장소를 사용할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

 

이러한 설정은 클라이언트에 대 한 스트리밍 앱-V 패키지 자산의 동작에 영향을 줍니다. 기본적으로 App-v는 초기 게시 및 기본 기능 블록을 다운로드 한 후 필요한 자산만 다운로드 합니다. 스트리밍 패키지에 대해 설명 해야 하는 세 가지 특정 동작이 있습니다.

-   백그라운드 스트리밍

-   최적화 된 스트리밍

-   스트림 오류

### 백그라운드 스트리밍

PowerShell cmdlet을 `Get-AppvClientConfiguration` 사용 하 여 AutoLoad 설정으로 백그라운드 스트리밍에 대 한 현재 모드를 결정 하 고 Cmdlet Set-AppvClientConfiguration 또는 registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming 키)를 사용 하 여 수정할 수 있습니다. 백그라운드 스트리밍은 이전에 사용 하 던 패키지를 다운로드 하도록 Autoload 설정을 설정한 기본 설정입니다. 기본 설정 (값 = 1)을 기준으로 하는 동작은 응용 프로그램이 실행 된 후 백그라운드에서 App-v 데이터 블록을 다운로드 합니다. 이 설정은 실행 되었는지 여부에 관계 없이 모든 패키지 (값 = 0)에 대해 모두 사용 하거나 사용 하지 않도록 설정할 수 있습니다 (value = 2).

### 최적화 된 스트리밍

시퀀싱 하는 동안 기본 기능 블록을 사용 하 여 app-v 패키지를 구성할 수 있습니다. 이 설정을 사용 하면 시퀀싱 엔지니어가 특정 응용 프로그램 또는 응용 프로그램에 대 한 시작 파일을 모니터링 하 고 패키지의 응용 프로그램을 처음 실행할 때 스트리밍을 위해 App-v 패키지의 데이터 블록을 표시할 수 있습니다.

### 스트림 오류

게시 데이터 및 기본 기능 블록의 초기 스트림 후에 추가 파일에 대 한 요청이 스트림 오류를 수행 합니다. 이러한 데이터 블록은 필요한 기준에 따라 패키지 저장소에 다운로드 됩니다. 이를 통해 사용자는 패키지의 작은 부분만 다운로드할 수 있으며 일반적으로 패키지를 실행 하 고 일반 작업을 실행할 수 있습니다. 다른 모든 블록은 사용자가 현재 패키지 저장소에 없는 데이터가 필요한 작업을 시작할 때 다운로드 됩니다.

App-v 패키지 스트리밍에 대 한 자세한 내용은 다음을 방문 <https://go.microsoft.com/fwlink/?LinkId=392770> 하세요.

스트리밍 최적화의 순서는:에서 사용할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=392771> .

### 패키지 업그레이드

앱-V 패키지는 응용 프로그램의 수명 주기 전체에서 업데이트 해야 합니다. 앱-V 패키지 업그레이드는 각 버전이 자체 PackageRoot 위치에 만들어지기 때문에 패키지 게시 작업과 유사 `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` 합니다. 업그레이드 작업은 동일한 패키지의 다른 버전에서 동일한 및 스트리밍된 파일에 대 한 하드 링크를 만들어 최적화 됩니다.

### 패키지 제거

패키지가 제거 되는 경우 App-v 클라이언트의 동작은 제거에 사용 되는 방법에 따라 달라 집니다. App-v full 인프라를 사용 하 여 응용 프로그램의 게시를 취소 하면 사용자 카탈로그 파일 (전역적으로 게시 된 응용 프로그램의 컴퓨터 카탈로그)은 제거 되지만 패키지 저장소 위치와 COW 위치는 유지 됩니다. PowerShell cmdlet을 `Remove-AppVClientPackge` 사용 하 여 App-v 패키지를 제거 하면 패키지 저장소 위치가 정리 됩니다. 관리 서버에서 App-v 패키지를 게시 취소 해도 제거 작업이 수행 되지 않는다는 점에 유의 하세요. 두 작업 모두 패키지 저장소 패키지 파일을 제거 하지 않습니다.

## <a href="" id="bkmk-roaming-reg-data"></a>로밍 레지스트리 및 데이터


앱-V 5는 사용 중인 응용 프로그램이 작성 되는 방법에 따라 로밍할 때 가까운 기본 환경을 제공할 수 있습니다. 기본적으로 App-v는 운영 체제의 로밍 구성을 기반으로 하 여 로밍 위치에 저장 된 AppData를 로밍 합니다. 파일 기반 데이터를 저장 하는 다른 위치는 roamed 아닌 위치에 있으므로 컴퓨터에서 로밍 되지 않습니다.

### <a href="" id="bkmk-clt-inter-roam-reqs"></a>로밍 요구 사항 및 사용자 카탈로그 데이터 저장소

App-v는 사용자 카탈로그의 상태를 나타내는 데이터를 다음 형식으로 저장 합니다.

-   %Appdata%\\Microsoft\\AppV\\Client\\Catalog 아래에 있는 파일

-   레지스트리 설정 `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

이러한 파일 및 레지스트리 설정은 사용자의 카탈로그를 나타내므로 둘 다 roamed 이거나 지정 된 사용자에 대해 roamed 되지 않아야 합니다. App-v는 로밍% AppData%를 지원 하지 않지만 사용자 프로필 (레지스트리)을 로밍 하거나 그 반대로는 사용할 수 없습니다.

**참고**  **AppvClientPackage** cmdlet은 사용자의 app-v 상태가 `HKEY_CURRENT_USER` 누락 되거나% appdata%의 데이터와 일치 하지 않는 패키지의 게시 상태를 복구 하지 않습니다.

 

### 레지스트리 기반 데이터

App-v 레지스트리 로밍은 다음 표에 표시 된 것 처럼 두 가지 시나리오가 됩니다.

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
<td align="left"><p>표준 사용자로 실행 되는 응용 프로그램</p></td>
<td align="left"><p>표준 사용자가 app-v 응용 프로그램을 실행 하는 경우 앱-V 응용 프로그램에 대 한 HKLM 및 HKCU가 모두 컴퓨터의 HKCU 하이브에 저장 됩니다. 이는 서로 다른 두 개의 경로로 표시 됩니다.</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {UserSID} \ 소프트웨어</p></li>
</ul>
<p>위치는 운영 체제 설정에 따라 로밍할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>권한 상승으로 실행 되는 응용 프로그램</p></td>
<td align="left"><p>상승을 사용 하 여 응용 프로그램을 실행 하는 경우:</p>
<ul>
<li><p>HKLM 데이터는 로컬 컴퓨터의 HKLM hive에 저장 됩니다.</p></li>
<li><p>HKCU 데이터는 사용자 레지스트리 위치에 저장 됩니다.</p></li>
</ul>
<p>이 시나리오에서는 일반 운영 체제 로밍 구성을 사용 하 여 이러한 설정을 roamed, 결과 레지스트리 키 및 값이 다음 위치에 저장 됩니다.</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {UserSID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {UserSID} \ 소프트웨어</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### App-v 및 폴더 리디렉션

App-v 5.1에서 로밍 AppData 폴더 (% AppData%)의 폴더 리디렉션을 지원 합니다. 가상 환경이 시작 되 면 사용자의 로밍 AppData 디렉터리에서 로밍 AppData 상태가 로컬 캐시에 복사 됩니다. 반대로, 가상 환경이 종료 되 면 특정 사용자의 로밍 AppData와 연결 된 로컬 캐시가 해당 사용자의 로밍 AppData 디렉터리의 실제 위치로 전송 됩니다.

일반적인 패키지에는 사용자의 지원 저장소에 여러 위치가 포함 되어 있으며,이 둘 다 AppData\\Local 및 AppData\\Roaming.의 설정에 사용 됩니다. 이러한 위치는 사용자 프로필에 사용자 당 저장 되는 쓰기 위치의 복사본 이며, 패키지 VFS 디렉터리에 대 한 변경 내용을 저장 하 고 기본 패키지 VFS를 보호 하는 데 사용 됩니다.

다음 표에서는 폴더 리디렉션이 구현 되지 않은 경우 로컬 및 로밍 위치를 보여 줍니다.

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
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Systemx86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; 로밍 </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

다음 표에서는 로컬 및 로밍 위치,% AppData%에 대해 폴더 리디렉션이 구현 되었고 위치가 리디렉션 됨 (일반적으로 네트워크 위치)을 보여 줍니다.

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
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Systemx86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; 강력한 &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

현재 App-v 클라이언트 VFS 드라이버는 네트워크 위치에 쓸 수 없으므로 App-v 클라이언트는 폴더 리디렉션이 있는지 검색 하 고, 게시 하는 동안 로컬 드라이브에 데이터를 복사 하 고 가상 환경이 시작 되는 시기를 표시 합니다. 사용자가 App-v 응용 프로그램을 닫고 App-v 클라이언트에서 가상 환경을 닫으면 VFS AppData의 로컬 저장소가 네트워크에 다시 복사 되어 프로세스가 반복 되는 추가 컴퓨터로 로밍이 가능 합니다. 프로세스의 세부 단계는 다음과 같습니다.

1.  게시 또는 가상 환경 시작 중에 App-v 클라이언트는 AppData 디렉터리의 위치를 감지 합니다.

2.  로밍 AppData 경로가 local 또는 .ino AppData\\Roaming 위치가 매핑되면 아무런 작업도 수행 되지 않습니다.

3.  로밍 AppData 경로가 local이 아니면 VFS AppData directory가 로컬 AppData 디렉터리로 매핑됩니다.

이 프로세스는 App-v 클라이언트 VFS 드라이버에서 지원 하지 않는 비로컬% AppData%의 문제를 해결 합니다. 그러나이 새 위치에 저장 된 데이터는 폴더 리디렉션으로 roamed 되지 않습니다. 응용 프로그램이 실행 되는 동안 모든 변경 내용은 로컬 AppData 위치에 있으며 리디렉션된 위치에 복사 해야 합니다. 이 프로세스의 자세한 단계는 다음과 같습니다.

1.  앱-V 응용 프로그램이 종료 되어 가상 환경을 종료 합니다.

2.  로밍 AppData 위치의 로컬 캐시는 압축 되어 ZIP 파일에 저장 됩니다.

3.  ZIP 패키지 프로세스 끝에 있는 타임 스탬프는 파일의 이름을 만드는 데 사용 됩니다.

4.  타임 스탬프는 HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime의 마지막으로 알려진 AppData timestamp로 레지스트리에 기록 됩니다.

5.  폴더 리디렉션 프로세스가 호출 되어 로밍 AppData 디렉터리에 업로드 된 ZIP 파일을 평가 하 고 시작 합니다.

타임 스탬프는 충돌이 있는 경우 "마지막 작성자 승리" 시나리오를 결정 하는 데 사용 되며, 앱이 게시 되거나 가상 환경이 시작 될 때 데이터 다운로드를 최적화 하는 데 사용 됩니다. 폴더 리디렉션은 지원 정책이 적용 되는 다른 모든 클라이언트로부터 데이터를 사용할 수 있게 하 고, AppData\\Roaming 데이터를 클라이언트의 로컬 AppData 위치에 저장 하는 프로세스를 시작 합니다. 세부 프로세스는 다음과 같습니다.

1.  사용자가 응용 프로그램을 시작 하 여 가상 환경을 시작 합니다.

2.  응용 프로그램의 가상 환경은 가장 최근에 스탬프가 지정 된 ZIP 파일 (있는 경우)을 확인 합니다.

3.  마지막으로 알려진 업로드 된 타임 스탬프가 있는 경우 레지스트리가 선택 되어 있는지 확인 합니다.

4.  가장 최근의 ZIP 파일은 마지막으로 알려진 로컬 업로드 타임 스탬프가 ZIP 파일의 타임 스탬프 보다 크거나 같은 경우에만 다운로드 됩니다.

5.  마지막으로 알려진 로컬 업로드 타임 스탬프가 로밍 AppData 위치에서 가장 최근의 ZIP 파일 보다 이전인 경우 ZIP 파일은 사용자 프로필의 로컬 임시 디렉터리로 추출 됩니다.

6.  ZIP 파일이 성공적으로 추출 된 후에는 로밍 AppData 디렉터리의 로컬 캐시 이름이 바뀌고 새 데이터는 위치에 이동 합니다.

7.  이름이 변경 된 디렉터리가 삭제 되 고 응용 프로그램이 가장 최근에 저장 된 로밍 AppData 데이터와 함께 열립니다.

이렇게 하면 AppData\\Roaming 위치에 있는 응용 프로그램 설정의 성공적인 로밍이 완료 됩니다. 해결 해야 하는 유일한 유일한 조건은 패키지 복구 작업입니다. 프로세스에 대 한 세부 정보는 다음과 같습니다.

1.  복구 하는 동안 사용자의 로밍 AppData 디렉터리 경로가 로컬이 아닌 경우 검색 합니다.

2.  로컬이 아닌 로밍 AppData 경로 대상이 예상 되는 로밍 및 로컬 AppData 위치에 다시 생성 됨을 매핑합니다.

3.  레지스트리에 저장 된 타임 스탬프가 있으면 삭제 합니다.

이 프로세스는 AppData에 대 한 로컬 및 네트워크 위치를 모두 다시 만들고 타임 스탬프의 레지스트리 레코드를 제거 합니다.

## <a href="" id="bkmk-clt-app-lifecycle"></a>앱-V 클라이언트 응용 프로그램 수명 주기 관리


App-v 전체 인프라에서 응용 프로그램을 시퀀싱 한 후에는 앱-V 관리 및 게시 서버를 통해 사용자 또는 컴퓨터에 관리 되 고 게시 됩니다. 이 섹션에서는 공용 App-v 응용 프로그램 수명 주기 작업 (추가, 게시, 시작, 업그레이드 및 제거) 중에 발생 하는 작업과 App-v 클라이언트 관점에서 변경 되 고 수정 된 파일 및 레지스트리 위치에 대해 설명 합니다. App-v 클라이언트 작업은 App-v 클라이언트를 실행 하는 컴퓨터에서 시작 되는 일련의 PowerShell 명령으로 수행 됩니다.

이 문서에서는 App-v 전체 인프라 솔루션에 대해 중점적으로 설명 합니다. Configuration Manager 2012에서 앱-V 통합에 대 한 특정 정보는 다음 사이트를 참조 하세요 <https://go.microsoft.com/fwlink/?LinkId=392773> .

앱-V 응용 프로그램 수명 주기 작업은 사용자 로그인 (기본값), 컴퓨터 시작 또는 백그라운드 시간 지정 작업으로 트리거됩니다. 게시 서버, 새로 고침 간격, 패키지 스크립트 사용 등을 비롯 한 App-v 클라이언트 작업의 설정은 PowerShell 명령을 사용 하 여 클라이언트 설치 또는 설정 후에 구성 됩니다. TechNet에서 클라이언트를 배포 하는 방법 섹션을 참조 하세요. [App-v 클라이언트를 배포](how-to-deploy-the-app-v-client-51gb18030.md) 하거나 PowerShell을 활용 하는 방법:

```powershell
get-command *appv*
```

### 게시 새로 고침

게시 새로 고침 프로세스는 App-v 클라이언트에서 수행 되는 몇 가지 작은 작업으로 구성 됩니다. App-v는 작업 예약 기술이 아닌 응용 프로그램 가상화 기술 이므로, Windows 작업 스케줄러는 사용자 로그온, 컴퓨터 시작, 예약 된 간격으로 프로세스를 사용 하도록 설정 하는 데 이용 됩니다. 클라이언트를 올바른 설정으로 대규모 컴퓨터 그룹에 배포 하는 경우 위에 나열 된 설정 중 클라이언트 구성을 사용 하는 것이 좋습니다. 다음 PowerShell cmdlet을 사용 하 여 이러한 클라이언트 설정을 구성할 수 있습니다.

-   **추가-AppVPublishingServer:** 앱-V 패키지를 제공 하는 App-v 게시 서버를 사용 하 여 클라이언트를 구성 합니다.

-   **Set-AppVPublishingServer:** App-v 게시 서버에 대 한 현재 설정을 수정 합니다.

-   **Set-AppVClientConfiguration:** App-v 클라이언트에 대 한 currents 설정을 수정 합니다.

-   **동기화-AppVPublishingServer:** 수동으로 앱 V 게시 새로 고침 프로세스를 시작 합니다. 이는 게시 서버를 구성 하는 동안 생성 되는 예약 된 작업에도 이용 됩니다.

다음 섹션의 초점은 App-v 게시 새로 고침의 각 단계에서 발생 하는 작업을 자세히 설명 하는 것입니다. 항목에는 다음이 포함 됩니다.

-   App-v 패키지 추가

-   App-v 패키지 게시

### App-v 패키지 추가

게시 새로 고침 프로세스의 첫 번째 단계는 클라이언트에 App-v 패키지를 추가 하는 것입니다. 최종 결과는 `Add-AppVClientPackage` PowerShell의 cmdlet과 같으며, 게시 새로 고침 추가 프로세스 중에, 구성 된 게시 서버에 연결 되어 있으며, 응용 프로그램의 상위 수준 목록을 클라이언트에 다시 전달 하 여 자세한 정보를 가져와 단일 패키지 추가 작업을 수행 하지는 않습니다. 패키지 또는 연결 그룹 추가 또는 업데이트에 대 한 클라이언트를 구성한 다음 appv 파일에 액세스 하 여 프로세스가 계속 됩니다. 다음으로, appv 파일의 내용이 확장 되어 로컬 운영 체제의 적절 한 위치에 배치 됩니다. 다음은 패키지가 오류 스트리밍을 위해 구성 되었다고 가정 하 여 프로세스에 대 한 상세한 워크플로입니다.

**App-v 패키지를 추가 하는 방법**

1.  PowerShell 또는 게시 새로 고침 프로세스의 작업 순서 시작을 통한 수동 시작입니다.

    1.  App-v 클라이언트는 HTTP 연결을 설정 하 고 대상에 따라 응용 프로그램 목록을 요청 합니다. 게시 새로 고침 프로세스는 대상 컴퓨터 또는 사용자를 지원 합니다.

    2.  App-v 게시 서버는 시작 하는 대상, 사용자 또는 컴퓨터의 id를 사용 하 고 데이터베이스를 쿼리 하 여 자격이 있는 응용 프로그램 목록을 만듭니다. 패키지 기준에 대 한 자세한 내용은 서버에 추가 요청을 보내는 데 사용 하는 XML 응답으로 응용 프로그램 목록이 제공 됩니다.

2.  App-v 클라이언트의 게시 에이전트는 직렬화 된 다음 모든 작업을 수행 합니다.

    연결 그룹의 일부인 패키지 버전 업데이트를 처리할 수 없기 때문에 게시 취소 되거나 사용할 수 없는 모든 연결 그룹을 평가 합니다.

3.  추가 또는 업데이트 작업을 식별 하 여 패키지를 구성 합니다.

    1.  App-v 클라이언트는 Windows에서 AppX API를 이용 하 고 게시 서버에서 appv 파일에 액세스 합니다.

    2.  패키지 파일이 열리고 AppXManifest.xml 및 StreamMap.xml 패키지 저장소에 다운로드 됩니다.

    3.  StreamMap.xml에 정의 된 전체 스트림 게시 블록 데이터 패키지 Store\\PkgGUID\\VerGUID\\Root.에 게시 블록 데이터를 저장 합니다.

        -   아이콘: 확장 지점의 대상입니다.

        -   PE 헤더 (이식 가능한 헤더): 디스크에서 이미지에 대 한 기본 정보를 포함 하는 확장 지점의 대상으로, 직접 액세스 하거나 파일 형식을 통해 사용할 때 필요 합니다.

        -   스크립트: 게시 프로세스 전체에서 사용할 스크립트 디렉터리를 다운로드 합니다.

    4.  패키지 저장소 채우기:

        1.  나열 된 모든 디렉터리에 대해 압축을 푼 패키지를 나타내는 스파스 파일을 디스크에 만듭니다.

        2.  루트 아래 상위 수준 파일 및 디렉터리를 준비 합니다.

        3.  디렉터리가 디스크에 스파스로 나열 되 고 요청 시 스트리밍된 경우 다른 모든 파일이 생성 됩니다.

    5.  컴퓨터 카탈로그 항목을 만듭니다. 패키지 파일에서 Manifest.xml 및 DeploymentConfiguration.xml 만들기 (패키지에서 자리 표시자 DeploymentConfiguration.xml 파일을 만들 수 없는 경우)

    6.  레지스트리 HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog에서 패키지 저장소의 위치를 만듭니다.

    7.  패키지 저장소 에서%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. .dat 파일을 만듭니다.

    8.  앱-V 커널 모드 드라이버 HKLM\\Microsoft\\Software\\AppV\\MAV를 사용 하 여 패키지 등록

    9.  패키지 추가 타이밍에 대 한 AppxManifest.xml 또는 DeploymentConfig.xml 파일에서 스크립팅을 호출 합니다.

4.  추가 및 설정/해제를 통해 연결 그룹을 구성 합니다.

5.  대상에 게시 되지 않은 개체 (사용자 또는 컴퓨터)를 제거 합니다.

    **참고**  패키지 삭제는 수행 되지 않고 특정 대상 (사용자 또는 컴퓨터)의 통합 지점을 제거 하 고 사용자 카탈로그 파일 (전역으로 게시 된 컴퓨터 카탈로그 파일)을 제거 하지 않습니다.

     

6.  클라이언트 구성을 기반으로 백그라운드 로드 탑재를 호출 합니다.

7.  컴퓨터 또는 사용자에 대 한 게시 정보가 이미 있는 패키지는 즉시 복원 됩니다.

    **참고**  이 상태는 패키지의 백그라운드 추가를 사용 하 여 게시 취소 하지 않고 제거 하는 제품으로 발생 합니다.

     

이렇게 하면 게시 새로 고침 프로세스의 App-v 패키지 추가가 완료 됩니다. 다음 단계는 패키지를 특정 대상 (컴퓨터 또는 사용자)에 게시 하는 것입니다.

![패키지 파일 및 레지스트리 데이터 추가](images/packageaddfileandregistrydata.png)

### App-v 패키지 게시

게시 새로 고침 작업을 수행 하는 동안 특정 게시 작업 (AppVClientPackage)은 사용자 카탈로그에 항목을 추가 하 고, 사용자에 게 자격을 매핑하고, 로컬 저장소를 식별 하 고, 통합 단계를 완료 하 여 완료 합니다. 자세한 단계는 다음과 같습니다.

**게시 하는 방법 및 App-v 패키지**

1.  패키지 항목이 사용자 카탈로그에 추가 됩니다.

    1.  사용자 대상 패키지: UserDeploymentConfiguration.xml 및 UserManifest.xml 사용자 카탈로그의 컴퓨터에 배치 됨

    2.  컴퓨터 대상 (전역) 패키지: UserDeploymentConfiguration.xml는 컴퓨터 카탈로그에 위치 합니다.

2.  HKLM\\Software\\Microsoft\\AppV\\MAV에서 사용자에 대 한 커널 모드 드라이버를 사용 하 여 패키지 등록

3.  통합 작업을 수행 합니다.

    1.  확장 지점을 만듭니다.

    2.  백업 정보를 사용자의 레지스트리와 로밍 프로필에 저장 합니다 (바로 가기 백업).

        **참고**  이렇게 하면 패키지가 게시 취소 된 경우 확장 지점을 복원할 수 있습니다.

         

    3.  게시 타이밍을 대상으로 하는 스크립트를 실행 합니다.

연결 그룹의 일부인 App-v 패키지를 게시 하는 것은 위의 프로세스와 매우 유사 합니다. 연결 그룹의 경우 특정 카탈로그 정보를 저장 하는 경로에는 PackageGroups가 Catalog 디렉터리의 자식으로 포함 됩니다. 자세한 내용은 위의 컴퓨터 및 사용자 카탈로그 정보를 검토 하세요.

![패키지 파일 및 레지스트리 데이터 추가-전역](images/packageaddfileandregistrydata-global.png)

### 응용 프로그램 시작

게시 새로 고침 프로세스 후 사용자가 App-v 응용 프로그램을 시작 하 고 다시 시작 합니다. 이 프로세스는 매우 간단 하며 최소한의 네트워크 트래픽으로 빠르게 실행 하도록 최적화 되어 있습니다. App-v 클라이언트는 게시 중에 만들어진 파일에 대 한 사용자 카탈로그 경로를 확인 합니다. 패키지를 시작할 수 있는 권한이 설정 되 면 App-v 클라이언트는 가상 환경을 만들고, 필요한 모든 데이터 스트리밍을 시작 하 고, 가상 환경 만들기 중 적절 한 매니페스트 및 배포 구성 파일을 적용 합니다. 특정 패키지 및 응용 프로그램에 대해 가상 환경을 만들고 구성 하면 응용 프로그램이 시작 됩니다.

**App-v 응용 프로그램을 시작 하는 방법**

1.  사용자가 바로 가기 또는 파일 형식 호출을 클릭 하 여 응용 프로그램을 실행 합니다.

2.  App-v 클라이언트는 다음 파일에 대 한 사용자 카탈로그의 존재를 확인 합니다.

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  파일이 있으면 해당 특정 사용자에 대 한 응용 프로그램 자격이 제공 되 고 응용 프로그램에서 실행을 위해 프로세스가 시작 됩니다. 이 시점에 네트워크 소통량이 없습니다.

4.  그런 다음 App-v 클라이언트는 App-v 클라이언트 서비스에 대해 등록 된 패키지의 경로가 레지스트리에 있는지 확인 합니다.

5.  패키지 저장소의 경로를 찾을 때 가상 환경이 만들어집니다. 첫 번째 실행 인 경우 기본 기능 블록이 있으면이를 다운로드 합니다.

6.  다운로드 한 후 App-v 클라이언트 서비스는 매니페스트 및 배포 구성 파일을 사용 하 여 가상 환경을 구성 하 고 모든 App-v 하위 시스템을 로드 합니다.

7.  응용 프로그램이 시작 됩니다. 패키지 저장소 (스파스 파일)의 누락 된 파일에 대 한 앱-V는 필요한 기준에 따라 파일의 오류를 스트리밍합니다.

    ![패키지 파일 및 레지스트리 데이터 추가-스트림](images/packageaddfileandregistrydata-stream.png)

### App-v 패키지 업그레이드

앱-V 5 패키지 업그레이드 프로세스는 이전 버전의 App-v와 다릅니다. App-v는 서로 다른 사용자에 게 해당 하는 컴퓨터에서 여러 버전의 동일한 패키지를 지원 합니다. 패키지 저장소와 카탈로그는 새 리소스로 업데이트 되므로 언제 든 지 패키지 버전을 추가할 수 있습니다. 새 버전 리소스 추가와 관련 된 유일한 프로세스는 저장소 최적화입니다. 업그레이드 중에 새 파일만 새 버전 저장소 위치에 추가 되 고 변경 되지 않은 파일에 대 한 하드 링크가 만들어집니다. 이렇게 하면 파일을 하나의 디스크 위치에 표시 한 다음 디스크에 있는 파일 위치 항목이 있는 모든 폴더로 프로젝션 하 여 전체 저장소를 줄일 수 있습니다. App-v 패키지 업그레이드에 대 한 구체적인 정보는 다음과 같습니다.

**앱-V 패키지를 업그레이드 하는 방법**

1.  App-v 클라이언트는 게시 새로 고침을 수행 하 고 최신 버전의 App-v 패키지를 검색 합니다.

2.  새 버전의 적절 한 카탈로그에 패키지 항목이 추가 됨

    1.  사용자 대상 패키지: UserDeploymentConfiguration.xml 및 UserManifest.xml는 appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID 사용자 카탈로그의 컴퓨터에 배치 됩니다.

    2.  컴퓨터 대상 (전역) 패키지: UserDeploymentConfiguration.xml 는%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID의 컴퓨터 카탈로그에 위치 합니다.

3.  HKLM\\Software\\Microsoft\\AppV\\MAV에서 사용자에 대 한 커널 모드 드라이버를 사용 하 여 패키지 등록

4.  통합 작업을 수행 합니다.

    -   매니페스트 및 동적 구성 파일에서 EP (확장 지점)를 통합 합니다.

    1.  파일 기반 EP 데이터는 패키지 저장소의 연결 지점을 활용 하 여 AppData 폴더에 저장 됩니다.

    2.  새 버전을 사용할 수 있게 되 면 버전 1 EPs가 이미 존재 합니다.

    3.  확장 지점은 컴퓨터 또는 사용자 카탈로그에서 최신 또는 업데이트 된 확장 지점에 대 한 버전 2 위치로 전환 됩니다.

5.  게시 타이밍을 대상으로 하는 스크립트를 실행 합니다.

6.  필요에 따라 side-by-side 어셈블리를 설치 합니다.

### 사용 중인 앱-V 패키지 업그레이드

**App-v 5 SP2 시작**: 최종 사용자가 사용 중인 패키지를 업그레이드 하려고 하면 업그레이드 작업이 보류 상태로 전환 됩니다. 업그레이드는 다음 규칙에 따라 나중에 실행 됩니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업 종류</th>
<th align="left">해당 규칙</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업 (예: 패키지를 사용자에 게 게시)</p></td>
<td align="left"><p>보류 중인 작업은 사용자가 로그 오프 한 다음 다시 로그온 하면 수행 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업 (예: 연결 그룹을 전역적으로 사용 가능)</p></td>
<td align="left"><p>보류 중인 작업은 컴퓨터를 종료 한 후 다시 시작 하면 수행 됩니다.</p></td>
</tr>
</tbody>
</table>

 

작업이 보류 상태에 배치 되 면 App-v 클라이언트는 다음과 같이 보류 중인 작업에 대 한 레지스트리 키도 생성 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">사용자 기반 또는 전역 기반 작업</th>
<th align="left">레지스트리 키가 생성 되는 위치</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>사용자 기반 작업</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>전역 기반 작업</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

다음 작업을 완료 해야 사용자가 최신 버전의 패키지를 사용할 수 있습니다.

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
<td align="left"><p>이 작업은 컴퓨터에 따라 달라 지 며, 위의 패키지 추가 섹션의 단계를 완료 하 여 언제 든 실행할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 게시</p></td>
<td align="left"><p>위의 단계에 대 한 패키지 게시 섹션을 참조 하세요. 이 프로세스에서는 시스템의 확장 지점을 업데이트 해야 합니다. 이 작업을 완료 하면 최종 사용자가 응용 프로그램을 사용할 수 없습니다.</p></td>
</tr>
</tbody>
</table>

 

패키지 업데이트에 대 한 지침으로 다음 예제 시나리오를 사용 합니다.

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
<td align="left"><p>업그레이드 하려고 할 때 app-v 패키지를 사용 하 고 있지 않음</p></td>
<td align="left"><p>패키지의 다음 구성 요소는 가상 응용 프로그램, COM 서버 또는 셸 확장 중 어느 것에도 사용할 수 없습니다.</p>
<p>관리자가 최신 버전의 패키지를 게시 하면 다음에 패키지 내의 구성 요소 또는 응용 프로그램을 실행할 때 업그레이드가 작동 합니다. 새 버전의 패키지를 스트리밍하 고 실행 합니다. 앱-V 5 SP2의 이전 릴리스 버전에서의이 시나리오에서 변경 된 내용이 없습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리자가 최신 버전의 패키지를 게시할 때 app-v 패키지가 사용 됨</p></td>
<td align="left"><p>업그레이드 작업은 App-v 클라이언트에 의해 보류 중으로 설정 되며,이는 패키지를 사용 하 고 있지 않을 때 나중에 대기열에 대기 상태를 나타내는 것을 의미 합니다.</p>
<p>패키지 응용 프로그램을 사용 중인 경우 사용자는 가상 응용 프로그램을 종료 한 후 업그레이드가 발생할 수 있습니다.</p>
<p>패키지에 Windows 탐색기에서 영구적으로 로드 되는 셸 확장 (Office 2013)이 있는 경우 사용자는 로그인 할 수 없습니다. 사용자는 로그 오프 한 다음 다시 로그인 하 여 App-v 패키지 업그레이드를 시작 해야 합니다.</p></td>
</tr>
</tbody>
</table>

 

### 전역 vs 사용자 게시

2 가지 방법 중 하나로 app-v 패키지를 게시할 수 있습니다. 앱-V 패키지를 특정 사용자 또는 사용자 그룹에 통해 하 고 컴퓨터의 모든 사용자에 대해 앱 V 패키지를 전체 컴퓨터에 통해 하는 사용자를 지정 합니다. 패키지 업그레이드를 보류 하 고 App-v 패키지를 사용 하 고 있지 않은 경우 두 가지 유형의 게시를 고려 하세요.

-   **전역으로 게시**됨: 응용 프로그램이 컴퓨터에 게시 됩니다. 해당 컴퓨터의 모든 사용자가 사용할 수 있습니다. 앱을 다시 시작 하는 것을 의미 하는 App-v 클라이언트 서비스가 시작 될 때 업그레이드가 수행 됩니다.

-   **사용자가 게시**됨: 응용 프로그램이 사용자에 게 게시 됩니다. 컴퓨터에 여러 사용자가 있는 경우 해당 사용자의 하위 집합에 응용 프로그램을 게시할 수 있습니다. 업그레이드는 사용자가 로그인 하거나 다시 게시 되는 경우 (정기적으로, ConfigMgr의 정책 새로 고침 및 평가 또는 App-v의 정기 게시/새로 고침 또는 PowerShell 명령을 명시적으로 통해)에 수행 됩니다.)

### App-v 패키지 제거

전체 인프라에서 App-v 응용 프로그램을 제거 하는 것은 게시 취소 작업 이므로 패키지 제거를 수행 하지 않습니다. 프로세스는 위의 게시 과정과 동일 하지만 제거 프로세스를 추가 하는 대신 App-v 패키지에 대해 변경한 내용을 취소 합니다.

### App-v 패키지 복구

복구 작업은 매우 간단 하지만 컴퓨터의 여러 위치에 영향을 줄 수 있습니다. 앞에서 언급 한 COW (기록에서) 위치는 제거 되 고, 확장 지점은 통합 취소 된 다음 다시 통합 됩니다. COW 데이터 배치 위치는 레지스트리에서 등록 된 위치를 검토 하 여 검토 하세요. 이 작업은 자동으로 수행 되며 App-v 클라이언트 콘솔 또는 PowerShell (AppVClientPackage)을 통해 복구 작업을 시작 하는 것 외에는 관리 제어가 없습니다.

## <a href="" id="bkmk-integr-appv-pkgs"></a>앱-V 패키지의 통합


앱-V 클라이언트 및 패키지 아키텍처는 패키지를 추가 하 고 게시 하는 동안 로컬 운영 체제와 특정 통합을 제공 합니다. 3 개의 파일은 App-v 패키지의 통합 또는 확장 지점을 정의 합니다.

-   AppXManifest.xml: 패키지 저장소와 사용자 프로필에 저장 된 대체 복사본을 사용 하 여 패키지 내에 저장 됩니다. 시퀀싱 프로세스 중에 생성 된 옵션을 포함 합니다.

-   DeploymentConfig.xml: 컴퓨터 및 사용자 기반 통합 확장 지점의 구성 정보를 제공 합니다.

-   UserConfig.xml: 사용자 기반 구성만 제공 하 고 대상 사용자 기반 확장 지점은 있는 Deploymentconfig.xml의 하위 집합입니다.

### 통합 규칙

App-v 클라이언트를 사용 하 여 컴퓨터에 앱 V 응용 프로그램을 게시할 때 아래 목록에서 설명 하는 대로 몇 가지 특정 동작이 발생 합니다.

-   전역 게시: 바로 가기는 모든 사용자 프로필 위치에 저장 되며 다른 확장 지점은 HKLM hive의 레지스트리에 저장 됩니다.

-   사용자 게시: 바로 가기는 현재 사용자 계정 프로필에 저장 되며 다른 확장 지점은 HKCU 하이브의 레지스트리에 저장 됩니다.

-   백업 및 복원: 기존 네이티브 응용 프로그램 데이터 및 레지스트리 (예: FTA 등록)는 게시 하는 동안 백업 됩니다.

    1.  App-v 패키지에는 소유권이 최신 게시 된 App-v 응용 프로그램에 전달 되는 마지막 통합 패키지에 따라 소유권이 지정 됩니다.

    2.  소유 하 고 있는 App-v 패키지가 게시 취소 된 경우 한 App-v 패키지에서 다른 앱으로 소유권을 전송 합니다. 이는 데이터 나 레지스트리의 복원을 시작 하지 않습니다.

    3.  마지막 패키지가 확장 지점을 기준으로 게시 취소 되거나 제거 될 때 백업 된 데이터를 복원 합니다.

### 확장 지점

앱-V 게시 파일 (매니페스트 및 동적 구성)은 응용 프로그램이 로컬 운영 체제와 통합 될 수 있는 여러 확장 지점을 제공 합니다. 이러한 확장 지점은 바로 가기 배치, 파일 형식 연결 만들기, 구성 요소 등록 등 일반적인 응용 프로그램 설치 작업을 수행 합니다. 기존 응용 프로그램과 같은 방식으로 설치 되지 않은 가상화 된 응용 프로그램은 몇 가지 차이점이 있습니다. 다음은이 섹션에서 설명 하는 확장 요점의 목록입니다.

-   정의

-   파일 형식 연결

-   셸 확장

-   COM

-   소프트웨어 클라이언트

-   응용 프로그램 기능

-   URL 프로토콜 처리기

-   AppPath

-   가상 응용 프로그램

### 정의

짧은 컷은 OS와 통합 되는 기본 요소 중 하나 이며, App-v 응용 프로그램의 직접 사용자 시작에 대 한 인터페이스입니다. App-v 응용 프로그램을 게시 하 고 게시가 취소 되는 동안

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

앞에서 설명한 대로 앱-V 바로 가기는 기본적으로 새로 고침 작업에 따라 사용자의 프로필에 배치 됩니다. 전역 새로 고침 바로 가기 모든 사용자 프로필에서 사용자를 새로 고치면 특정 사용자의 프로필에 저장 됩니다. 실제 실행 파일은 패키지 저장소에 저장 됩니다. .ICO 파일의 위치는 App-v 패키지의 토큰화 된 위치입니다.

### 파일 형식 연결

App-v 클라이언트는 사용자가 파일 형식 호출을 사용 하거나 특수 하 게 등록 된 확장명 (.docx)이 있는 파일을 열어서 App-v 응용 프로그램을 시작할 수 있도록 게시 중에 로컬 운영 체제 파일 형식 연결을 관리 합니다. 다음 예제에 표시 된 대로 매니페스트 및 동적 구성 파일에 파일 형식 연결이 표시 됩니다.

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

**참고**  이 예제에서는 다음을 수행 합니다.

-   `<Name>.xdp</Name>` 확장명

-   `<Name>AcroExch.XDPDoc</Name>` ProgId 값 (인접 한 ProgId를 가리키는)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` 는 응용 프로그램 실행 파일을 가리키는 명령줄입니다.

 

### 셸 확장

셸 확장은 시퀀싱 프로세스 중 패키지에 자동으로 포함 됩니다. 패키지가 전역으로 게시 되 면 셸 확장에서는 응용 프로그램이 로컬에 설치 되어 있는 것과 동일한 기능을 사용자에 게 제공 합니다. 셸 확장 기능을 사용 하도록 설정 하려면 응용 프로그램에 추가 설정이 나 클라이언트에 대 한 구성이 필요 하지 않습니다.

**셸 확장 사용에 대 한 요구 사항:**

-   포함 된 셸 확장을 포함 하는 패키지는 전체적으로 게시 해야 합니다.

-   응용 프로그램, Sequencer, App-v 클라이언트의 "비트"는 일치 해야 하며 그렇지 않으면 셸 확장이 작동 하지 않습니다. 예:

    -   응용 프로그램 버전은 64 비트입니다.

    -   Sequencer가 64 비트 컴퓨터에서 실행 되 고 있습니다.

    -   패키지가 64 비트 App-v 클라이언트 컴퓨터로 전달 됩니다.

다음 표에서는 지원 되는 셸 확장을 보여 줍니다.

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
<td align="left"><p>상황에 맞는 메뉴에 메뉴 항목을 추가 합니다. 이 메서드는 상황에 맞는 메뉴가 표시 되기 전에 호출 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>끌어서 놓기 처리기</p></td>
<td align="left"><p>끌어서 놓기를 마우스 오른쪽 단추로 클릭 하 고 표시 되는 상황에 맞는 메뉴를 수정할 때의 동작을 제어 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>놓기 대상 처리기</p></td>
<td align="left"><p>파일 등의 놓기 대상 위에 데이터 개체를 끌어서 놓은 후의 동작을 제어 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>데이터 개체 처리기</p></td>
<td align="left"><p>파일이 클립보드에 복사 되거나 놓기 대상 위에 끌어 놓은 후의 동작을 제어 합니다. 놓기 대상에 추가 클립보드 형식을 제공할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>속성 시트 처리기</p></td>
<td align="left"><p>개체의 속성 시트 대화 상자에 페이지를 바꾸거나 추가 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>정보 팁 처리기</p></td>
<td align="left"><p>마우스 포인터로 팝업 도구 설명 안에 항목에 대 한 플래그 및 정보 팁을 검색 하 고 표시할 수 있습니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>열 처리기</p></td>
<td align="left"><p>Windows 탐색기 세부 정보 보기에서 사용자 지정 열을 만들고 표시할 수 있습니다 <em> </em> . 이를 사용 하 여 정렬 및 그룹화를 확장할 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>미리 보기 처리기</p></td>
<td align="left"><p>Windows 탐색기 미리 보기 창에 파일의 미리 보기를 표시할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 

### COM

App-v 클라이언트는 COM 통합 및 가상화에 대 한 지원이 포함 된 응용 프로그램 게시를 지원 합니다. COM 통합을 사용 하면 App-v 클라이언트가 로컬 운영 체제 및 개체의 가상화에 COM 개체를 등록할 수 있습니다. 이 문서의 목적을 위해 COM 개체의 통합에는 추가 세부 정보가 필요 합니다.

App-v는 패키지의 COM 개체를 두 가지 프로세스 유형 (out-of-process 및 in-process)으로 로컬 운영 체제에 등록할 수 있도록 지원 합니다. COM 개체 등록은 해제, 격리 및 통합이 포함 된 특정 App-v 패키지에 대 한 여러 작업 모드와 조합 하 여 수행 됩니다. 통합 모드가 out-of-process 또는 in-process 형식 중 하나로 구성 되어 있습니다. COM 모드 및 형식의 구성은 동적 구성 파일 (deploymentconfig.xml 또는 userconfig.xml)을 사용 하 여 수행 됩니다.

App-v 통합에 대 한 자세한 내용은 다음에서 확인할 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=392834> .

### 소프트웨어 클라이언트 및 응용 프로그램 기능

App-v는 운영 체제의 소프트웨어 클라이언트에 가상화 된 응용 프로그램을 등록할 수 있도록 하는 특정 소프트웨어 클라이언트 및 응용 프로그램 기능 확장 지점을 지원 합니다. 이렇게 하면 사용자가 전자 메일, 인스턴트 메시지, 미디어 플레이어 등의 작업에 대 한 기본 프로그램을 선택할 수 있습니다. 이 작업은 제어판에서 프로그램 액세스 및 컴퓨터 기본값 설정으로 수행 되며 매니페스트 또는 동적 구성 파일에서 시퀀싱 중에 구성 됩니다. 앱 기능은 App-v 응용 프로그램이 전역으로 게시 된 경우에만 지원 됩니다.

앱 V 기반 메일 클라이언트의 소프트웨어 클라이언트 등록의 예입니다.

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

**참고**  이 예제에서는 다음을 수행 합니다.

-   `<ClientConfiguration EmailEnabled="true" />` 전자 메일 클라이언트 통합에 대 한 전반적인 소프트웨어 클라이언트 설정

-   `<EMail MakeDefault="true">` 특정 전자 메일 클라이언트를 기본 전자 메일 클라이언트로 설정 하는 플래그입니다.

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` MAPI dll 등록이

 

### URL 프로토콜 처리기

응용 프로그램은 항상 파일 형식 호출을 활용 하는 가상화 된 응용 프로그램 이라고 할 수 없습니다. 예를 들어 문서 또는 웹 페이지 내에 mailto: link를 포함 하는 응용 프로그램에서 사용자는 mailto: 링크를 클릭 하 고 등록 된 메일 클라이언트를 가져올 것으로 간주 합니다. App-v는 로컬 운영 체제를 사용 하 여 패키지 별로 등록할 수 있는 URL 프로토콜 처리기를 지원 합니다. 시퀀싱 하는 동안 URL 프로토콜 처리기가 패키지에 자동으로 추가 됩니다.

특정 URL 프로토콜 처리기를 등록할 수 있는 응용 프로그램이 두 개 이상 있는 경우 동적 구성 파일을 사용 하 여 동작을 수정 하 고, 기본 응용 프로그램이 시작 되지 않아야 하는 응용 프로그램에 대해이 기능을 사용 하지 않도록 설정 하거나 해제할 수 있습니다.

### AppPath

AppPath 확장 지점은 운영 체제에서 직접 호출 하는 앱 V 응용 프로그램을 지원 합니다. 이 작업은 일반적으로 운영 체제에 따라 실행 또는 시작 화면에서 수행 되며, 관리자는 실행 파일에 대 한 특정 경로를 호출 하지 않고 운영 체제 명령 또는 스크립트에서 앱 V 응용 프로그램에 액세스할 수 있도록 합니다. 따라서 게시 하는 동안 수행 되는 모든 시스템에서 시스템 경로 환경 변수를 수정 하지 않아도 됩니다.

AppPath 확장 지점은 매니페스트 또는 동적 구성 파일에 구성 되며 사용자 용으로 게시 하는 동안 로컬 컴퓨터의 레지스트리에 저장 됩니다. AppPath 검토에 대 한 자세한 내용은을 참조 <https://go.microsoft.com/fwlink/?LinkId=392835> 하세요.

### 가상 응용 프로그램

이 하위 시스템은 다른 App-v 구성 요소에서 일반적으로 사용 되는 시퀀싱 중에 캡처한 응용 프로그램 목록을 제공 합니다. 특정 응용 프로그램에 속하는 확장 지점의 통합은 동적 구성 파일을 사용 하 여 해제할 수 있습니다. 예를 들어 패키지에 두 개의 응용 프로그램이 포함 된 경우 하나의 응용 프로그램에 속하는 모든 확장 지점을 사용 하지 않도록 설정 하 여 다른 응용 프로그램의 확장 지점 통합만 허용할 수 있습니다.

### 확장 점 규칙

위에서 설명한 확장 지점은 패키지가 게시 된 방식에 따라 운영 체제에 통합 되어 있습니다. 전역 게시는 사용자가 사용자 위치에서 확장 지점을 배치할 공용 컴퓨터 위치에 확장 지점을 배치 합니다. 예를 들어 바탕 화면에 만들어지고 전역으로 게시 된 바로 가기는 바로 가기 (%Public%\\Desktop) 및 레지스트리 데이터 (HKLM\\Software\\Classes)에 대 한 파일 데이터를 생성 합니다. 동일한 바로 가기에는 파일 데이터 (%UserProfile%\\Desktop)와 레지스트리 데이터 (HKCU\\Software\\Classes)가 있습니다.

확장 지점은 일부 확장 지점에는 전역 게시가 필요 하 고, 특정 운영 체제 및이를 전달 하는 아키텍처에 대 한 시퀀싱이 필요한 경우에는 모두 같은 방식으로 게시 되지 않습니다. 다음은 이러한 두 가지 키 규칙을 설명 하는 테이블입니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">가상 확장</th>
<th align="left">대상 OS 시퀀싱 필요</th>
<th align="left">전역 게시 필요</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>키</p></td>
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
<td align="left"><p>데이터 개체 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>속성 시트 처리기</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>정보 팁 처리기</p></td>
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

 

## <a href="" id="bkmk-dynamic-config"></a>동적 구성 처리


하나의 컴퓨터 또는 사용자에 게 App-v 패키지를 배포 하는 것은 매우 간단 합니다. 그러나 조직이 비즈니스 회선 및 지역 및 정치적 경계를 넘어 AppV 응용 프로그램을 배포 하는 경우 한 설정 집합을 사용 하 여 응용 프로그램을 한 번 시퀀싱 하는 기능은 불가능 합니다. App-v는 매니페스트 파일에서 시퀀싱 하는 동안 특정 설정 및 구성을 캡처하며, 동적 구성 파일을 사용 하 여 수정도 지원 하므로이 시나리오를 위해 디자인 되었습니다.

App-v 동적 구성은 컴퓨터 수준 또는 사용자 수준에서 패키지에 대 한 정책을 지정할 수 있도록 합니다. 동적 구성 파일을 사용 하면 시퀀싱 엔지니어가 패키지의 구성을 수정 하 여 개별 사용자 또는 컴퓨터 그룹의 요구를 처리할 수 있습니다. 일부 경우에는 App-v 환경에서 적절 한 기능을 제공 하기 위해 응용 프로그램을 수정 해야 할 수 있습니다. 예를 들어 \ _ \ * config.xml 파일을 수정 하 여 가상화 된 응용 프로그램이 다른 응용 프로그램에서 확장을 덮어쓰는 것을 방지 하기 위해 mailto 확장을 해제 하는 등 특정 작업을 지정 된 시간에 수행할 수 있도록 해야 할 수 있습니다.

App-v 패키지에는 시퀀스 작업을 대표 하는 appv 패키지 파일 내부의 매니페스트 파일이 포함 되어 있으며, 동적 구성 파일이 특정 패키지에 할당 되지 않은 경우 선택 하는 정책입니다. 순서 사후 작업을 위해 동적 구성 파일을 수정 하 여 다양 한 데스크톱 또는 다른 확장 지점을 가진 사용자에 게 응용 프로그램을 게시할 수 있습니다. 두 동적 구성 파일은 DDC (동적 배포 구성) 및 DUC (Dynamic User Configuration) 파일입니다. 이 섹션에서는 매니페스트 및 동적 구성 파일의 조합에 대해 중점적으로 설명 합니다.

### 동적 구성 파일의 예

아래 예제에서는 게시 후와 정상적으로 작동 하는 동안 매니페스트, 배포 구성 및 사용자 구성 파일의 조합을 보여 줍니다. 이러한 예제는 각 파일의 간략 한 예제입니다. 이 목적에는 파일의 조합이 표시 되며 각 파일에서 사용할 수 있는 특정 범주에 대 한 완전 한 설명이 되지 않습니다. 자세한 내용은 다음에서 App-v 5 시퀀싱 가이드를 참조 하세요. <https://go.microsoft.com/fwlink/?LinkID=269810>

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

## <a href="" id="bkmk-sidebyside-assemblies"></a>Side-by-side 어셈블리


App-v는 가상 응용 프로그램을 게시 하는 동안 클라이언트에서 시퀀싱 및 배포 하는 동안 SxS (나란히) 어셈블리의 자동 패키징을 지원 합니다. 시퀀싱 컴퓨터에 없는 어셈블리를 시퀀싱 하는 동안 app-v 5 SP2는 SxS 어셈블리 캡처를 지원 합니다. Visual c + + (버전 8 이상) 및/또는 MSXML 런타임으로 구성 된 어셈블리의 경우, 모니터링 중에 설치 되지 않은 경우에도 Sequencer가 이러한 종속성을 자동으로 감지 하 여 캡처합니다. Side-by-side 어셈블리 기능은 앱 V 시퀀서에서 시퀀싱 워크스테이션에 이미 있는 어셈블리를 캡처하지 않은 경우와 패키지 당 하나의 비트 버전으로 제한 되는 어셈블리를 privatizing 이전 버전의 App-v에 대 한 제한을 제거 합니다. 이 문제로 인해 클라이언트에 게 앱 V 응용 프로그램이 배포 되어 필요한 SxS 어셈블리가 없어 응용 프로그램 시작 실패가 발생 했습니다. 이렇게 하면 패키징 프로세스가 문서화 된 후 패키지에 필요한 모든 어셈블리가 사용자의 클라이언트 운영 체제에 로컬로 설치 되어 가상 응용 프로그램에 대 한 지원을 보장 합니다. 어셈블리 수와 필요한 종속성에 대 한 응용 프로그램 설명서의 부족을 기준으로이 작업은 관리 및 구현 챌린지입니다.

App-v의 side-by-side 어셈블리 지원에는 다음과 같은 기능이 있습니다.

-   시퀀싱 하는 동안 어셈블리의 설치 여부에 관계 없이 SxS 어셈블리의 자동 캡처.

-   앱-V 클라이언트는 게시 시간에 필요한 SxS 어셈블리 (표시 되지 않은 경우)를 클라이언트 컴퓨터에 자동으로 설치 합니다.

-   Sequencer는 Sequencer 보고 메커니즘에서 VC 런타임 종속성을 보고 합니다.

-   시퀀서는 이전에 대상 컴퓨터에 어셈블리가 설치 되어 있는 시나리오를 지원 하 여 시퀀서에 이미 설치 되어 있는 어셈블리를 패키지 하지 않도록 할 수 있습니다.

### SxS 어셈블리 자동 게시

SxS 어셈블리가 있는 App-v 패키지를 게시 하는 동안 App-v 클라이언트는 컴퓨터에서 어셈블리가 있는지 확인 합니다. 어셈블리가 없는 경우 클라이언트는 해당 어셈블리를 컴퓨터에 배포 합니다. 연결 그룹에 속하는 패키지는 어셈블리 설치에 대 한 정보를 포함 하지 않으므로 기본 패키지의 일부인 Side-by-side 어셈블리 설치에 의존 합니다.

**참고**  어셈블리를 사용 하 여 패키지를 게시 취소 하거나 제거 해도 해당 패키지의 어셈블리는 제거 되지 않습니다.

 

## <a href="" id="bkmk-client-logging"></a>클라이언트 로깅


App-v 클라이언트는 표준 ETW 형식으로 Windows 이벤트 로그에 정보를 기록 합니다. 특정 App-v 이벤트는 이벤트 뷰어, 응용 프로그램 및 서비스 Logs\\Microsoft\\AppV\\Client.에서 찾을 수 있습니다.

**참고**  App-v 5.0 SP3에서는 일부 로그가 통합 되어 다음 위치로 이동 했습니다.

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

이동한 로그 목록은 [앱-V 5.0 SP3 정보](about-app-v-50-sp3.md#bkmk-event-logs-moved)를 참조 하세요.

 

세 가지 특정 범주의 이벤트가 아래에 설명 되어 있습니다.

**관리자**: app-v 클라이언트에 적용 되는 구성에 대 한 이벤트를 기록 하 고 기본 경고 및 오류를 포함 합니다.

**작동**: app-v 클라이언트에서 완료 된 app-v 작업의 감사 로그를 만드는 개별 구성 요소의 일반 app-v 실행 및 사용을 기록 합니다.

**가상 응용 프로그램**: 가상화 하위 시스템을 시작 하 고 사용 하는 가상 응용 프로그램을 기록 합니다.






 

 





