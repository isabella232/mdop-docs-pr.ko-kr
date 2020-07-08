---
title: UE-V 2. x에 대 한 응용 프로그램 템플릿 스키마 참조
description: UE-V 2. x에 대 한 응용 프로그램 템플릿 스키마 참조
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827408"
---
# UE-V 2. x에 대 한 응용 프로그램 템플릿 스키마 참조


Microsoft UE-V (User Experience Virtualization) 2.0, 2.1 및 2.1 SP1은 XML 설정 위치 템플릿을 사용 하 여 UE-V를 통해 캡처 및 적용 되는 데스크톱 응용 프로그램 설정 및 Windows 설정을 정의 합니다. UE-V는 기본 설정 위치 템플릿 집합을 포함 합니다. UE-V 생성기를 사용 하 여 사용자 지정 설정 위치 템플릿을 만들 수도 있습니다.

고급 사용자는 설정 위치 템플릿의 XML 파일을 사용자 지정할 수 있습니다. 이 항목에서는 UE-V 2.1 (SP1) 및 2.0 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고 이러한 파일 편집을 위한 지침을 제공 합니다.

## UE-V 2.1 및 2.1 SP1 응용 프로그램 템플릿 스키마 참조


이 섹션에서는 UE-V 2.1 및 2.1 SP1 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고이 파일 편집에 대 한 지침을 제공 합니다.

### 이 섹션의 내용

-   [XML 선언 및 인코딩 특성](#xml21)

-   [네임 스페이스 및 루트 요소](#namespace21)

-   [데이터 형식](#data21)

-   [Name 요소](#name21)

-   [ID 요소](#id21)

-   [버전 요소](#version21)

-   [Author 요소](#author21)

-   [프로세스 및 프로세스 요소](#processes21)

-   [응용 프로그램 요소](#application21)

-   [공통 요소](#common21)

-   [SettingsLocationTemplate 요소](#settingslocationtemplate21)

-   [부록: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>XML 선언 및 인코딩 특성

**필수: True**

**형식: 문자열**

XML 선언에서는 XML 버전 1.0 특성 ( &lt; ? XML 버전 = "1.0")을 지정 해야 합니다 &gt; . UE-V 생성기에서 만든 설정 위치 템플릿은 해당 인코딩이 명시적으로 지정 되어 있지 않지만 UTF-8 인코딩으로 저장 됩니다. 이 요소에 encoding = "UTF-8" 특성을 가장 좋은 방법으로 포함 하는 것이 좋습니다. 제품에 포함 된 모든 서식 파일은이 태그를 지정 합니다 (참조용%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\Templates 문서 참조). 예:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>네임 스페이스 및 루트 요소

**필수: True**

**형식: 문자열**

UE-V는 https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate 모든 응용 프로그램에 대 한 네임 스페이스를 사용 합니다. SettingsLocationTemplate은 루트 요소 이며 다른 모든 요소를 포함 합니다. 이 태그를 사용 하 여 모든 템플릿의 Reference SettingsLocationTemplate:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>데이터 형식

다음은 UE-V 응용 프로그램 템플릿 스키마에 대 한 데이터 형식입니다.

<a href="" id="guid"></a>**GUID** GUID는 "\\ {\ [a-fA-F0-9 \]-\ [a-fA-F0-9 \] 형식으로 된 표준 전역 고유 식별자 정규식을 설명 합니다. {8} {4} [a-Fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \\}". Filesetting\\Root\\KnownFolder 요소에서 잘 알려진 폴더의 서식을 확인 하는 데 사용 됩니다.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString는 모니터링할 프로세스의 파일 이름을 나타냅니다. 해당 값은 regex \ [^ \\ \ \\? \ \ \ * \ \ | &lt; &gt; 에 의해 제한 됩니다. /: \] +, (백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 문자를 포함 하지 않을 수 있습니다.)

<a href="" id="idstring"></a>**Idstring** IDString은 응용 프로그램 요소의 ID 값, SettingsLocationTemplate, 공통 요소 (공통 설정을 공유 하는 응용 프로그램 제품군을 설명 하는 데 사용 됨)를 나타냅니다. FilenameString (\\ [^ \\? \\ | &lt; &gt; )와 동일한 regex로 제한 됩니다. /:\]+).

<a href="" id="templateversion"></a>**서식 버전** 서식 파일 버전은 설정 위치 템플릿의 수정을 설명 하는 데 사용 되는 정수 값입니다. 값의 범위는 0 ~ 2147483647입니다.

<a href="" id="empty"></a>**비어 있음** Empty는 null 값을 참조 합니다. 이는 처리할 프로세스가 없다는 것을 나타내기 위해 Process\\ShellProcess에 사용 됩니다. 이 값은 응용 프로그램 템플릿에서 사용해 서는 안 됩니다.

<a href="" id="author"></a>**만든이** Author 데이터 형식은 서식 파일의 작성자를 식별 하는 복잡 한 유형입니다. 여기에는 **이름** 및 **전자 메일**이라는 두 개의 자식 요소가 포함 됩니다. Author 데이터 형식 내에서 Name 요소는 필수 항목이 며 전자 메일 요소는 선택 사항입니다. 이 형식은 SettingsLocationTemplate 요소 아래에 자세히 설명 되어 있습니다.

<a href="" id="range"></a>**범위** 범위는 **최소** 및 **최대**의 두 자식 요소로 구성 된 integer 클래스를 정의 합니다. 이 데이터 형식은 ProcessVersion 데이터 형식에서 구현 됩니다. 지정 된 경우 최소 및 최대 값을 모두 포함 해야 합니다.

<a href="" id="processversion"></a>**Processversion** ProcessVersion은 **주**, **부**, **빌드**, **패치**등 네 가지 자식 요소를 사용 하 여 형식을 정의 합니다. 이 데이터 형식은 Process 요소에서 ProductVersion 및 FileVersion 값을 채우는 데 사용 됩니다. 이 유형의 데이터는 범위 값입니다. 주요 자식 요소는 필수 이며 나머지는 선택 사항입니다.

<a href="" id="architecture"></a>**아키텍처가** 아키텍처에는 두 가지 가능 값 ( **Win32** 및 **Win64**)이 열거 됩니다. 이러한 값은 프로세스 아키텍처를 지정 하는 데 사용 됩니다.

<a href="" id="process"></a>**공정** 프로세스 데이터 형식은 UE-V를 통해 모니터링할 프로세스를 설명 하는 데 사용 되는 컨테이너입니다. 여기에는 **파일 이름**, **아키텍처**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**의 여섯 가지 하위 요소가 포함 되어 있습니다. 이 표에서는 각 요소의 해당 데이터 형식에 대해 자세히 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>요소</strong></p></td>
<td align="left"><p><strong>데이터 형식</strong></p></td>
<td align="left"><p><strong>Mandatory</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>이름이</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>아키텍처</p></td>
<td align="left"><p>아키텍처</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**프로세스** 프로세스 데이터 형식은 하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너를 나타냅니다. 프로세스 시퀀스 형식에서 처리 되는 두 개의 자식 요소에는 **process** 와 **shellprocess**지원 됩니다. 프로세스는 유형 프로세스의 요소이 고 ShellProcess는 데이터 형식이 비어 있습니다. 순서에서 하나 이상의 항목을 식별 해야 합니다.

<a href="" id="path"></a>**경로** RegistrySetting 및 FileSetting에서 Path를 사용 하 여 레지스트리와 파일 경로를 참조 합니다. 이 요소는 선택적 특성 두 개를 지원 합니다. **재귀** 및 **Deletfnota가 발견**되었습니다. 두 값 모두 default = "False"로 설정 됩니다.

Recursive는 경로 및 모든 하위 폴더가 파일 설정에 포함 되거나 모든 하위 레지스트리 키가 레지스트리 설정에 포함 됨을 나타냅니다. 두 경우 모두 현재 수준의 모든 항목이 캡처한 데이터에 포함 됩니다. FileSettings 개체의 경우 지정 된 폴더 내의 모든 파일이 UE-V를 통해 캡처한 데이터에 포함 되지만 폴더는 포함 되지 않습니다. 레지스트리 경로의 경우 현재 경로에 있는 모든 값이 캡처되고 자식 레지스트리 키가 캡처되지 않습니다. 두 경우 모두 대규모 데이터 집합 또는 많은 수의 항목을 캡처하는 것을 방지 하기 위해 주의를 기울여야 합니다.

DeleteIfNotFound 특성은 사용자의 설정 저장소 경로 데이터에서 설정을 제거 합니다. 이는 패키지에서 이러한 설정을 제거 하 여 설정 저장소 경로 파일 서버에 많은 양의 디스크 공간이 저장 되는 경우에 유용할 수 있습니다.

<a href="" id="filemask"></a>**FileMask** FileMask는 Path로 정의 된 폴더에 대 한 특정 파일 형식만 지정 합니다. 예를 들어 Path는 `C:\users\username\files` `*.txt` 텍스트 파일만 포함 하 고 FileMask 수 있습니다.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting는 레지스트리 키 및 값에 대 한 컨테이너와 UE-V 에이전트의 부분에 대 한 연결 된 원하는 동작을 나타냅니다. **Path**, **Name**, **Exclude**, 값 **경로** 및 **이름의**시퀀스를 포함 하 여 네 개의 자식 요소가이 형식으로 정의 됩니다.

<a href="" id="filesetting"></a>**Filesetting** FileSetting에는 파일 및 파일 경로와 연결 된 매개 변수가 포함 됩니다. **루트**, **경로**, **FileMask**및 **Exclude**의 네 가지 자식 요소가 정의 되어 있습니다. Root는 필수 이며 나머지는 선택 사항입니다.

<a href="" id="settings"></a>**설정** 설정은 특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다. 여기에는 앞에서 설명한 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다. 또한 다음과 같은 동작이 포함 된 다음 자식 요소도 포함할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>요소</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>비동기</p></td>
<td align="left"><p>비동기 설정 패키지는 응용 프로그램 시작을 차단 하지 않고 적용 되므로 설정이 계속 적용 되는 동안 응용 프로그램을 계속 진행할 수 있습니다. 이 방법은 SystemParameterSetting과 같이 API를 통해 비동기적으로 적용할 수 있는 설정에 유용 <code>get/set</code> 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>기본적으로 UE-V는 템플릿을 사용 하는 응용 프로그램의 마지막 인스턴스가 닫혀 있을 때만 응용 프로그램에 대 한 설정을 저장 합니다. 이 요소를 ' f l l e '로 설정 하면 UE-V가 응용 프로그램의 다른 인스턴스가 실행 되는 경우에도 설정을 내보냅니다. 적합 한 서식 파일 – UE-V를 사용 하 여 제공 되는 공용 요소 섹션이 포함 된 경우이 플래그를 사용 하 여 마지막 인스턴스가 닫힐 때까지 응용 프로그램 관련 설정이 내보내기 되지 않도록 하 여 응용 프로그램을 닫을 때 공유 설정을 항상 내보낼 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(2.1에서 도입 되었습니다.)</p>
<p>이 매개 변수는 패키지와 응용 프로그램의 현재 상태 간에 차이점이 없는 경우에도 가져온 설정 패키지를 적용 하도록 강제 합니다. 이 매개 변수는 설정 가져오기가 느려질 수 있으므로 특별 한 경우에만 사용 해야 합니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Name 요소

**필수: True**

**형식: 문자열**

Name은 설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 일반적으로 버전 정보를 참조 하지 않도록 하는 것은 ProductVersion 요소와는 다른 것이 될 수 있기 때문입니다. 예를 들어, `<Name>My Application</Name>` 대신를 지정 `<Name>My Application 1.1</Name>` 합니다.

**참고**  UE-V는 외부 Dtd를 참조 하지 않으므로 설정 위치 템플릿에서 명명 된 엔터티를 사용할 수 없습니다. 예를 들어 &reg; 등록 된 무역 표시 기호®를 참조 하는 데 사용 하지 마세요. 대신 정식 번호 매기기 참조를 사용 하 여 이러한 유형의 특수 문자를 포함 합니다 (예:® 문자에 대 한 & \ #174). 이 규칙은이 문서의 모든 문자열 값에 적용 됩니다.

<http://www.w3.org/TR/xhtml1/dtds.html>전체 문자 엔터티 목록을 보려면을 참조 하세요. U t f-8로 인코딩된 문서에는 유니코드 문자가 직접 포함 될 수 있습니다. UE-V 생성기를 통해 템플릿을 저장 하면 문자 엔터티가 해당 유니코드 표현으로 자동 변환 됩니다.

 

### <a href="" id="id21"></a>ID 요소

**필수: True**

**형식: 문자열**

ID는 특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다 (예: Get-help Evtemplate 및 가져오기-Uevtemplate 파일 프로그램 PowerShell cmdlet의 출력 참조). 규칙에 따라이 태그에는 모든 공백을 포함할 수 없으며 스크립팅이 간단해 집니다. 또는 등의 템플릿을 쉽게 식별할 수 있도록이 요소에 응용 프로그램의 버전 번호를 지정 해야 합니다 `<ID>MicrosoftCalculator6</ID>` `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>버전 요소

**필수: True**

**유형: Integer**

**최 솟 값: 0**

**최 댓 값: 2147483647**

버전은 변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다. UE-V 생성기는 템플릿이 저장 될 때마다이 번호를 하나씩 자동으로 증가 시킵니다. 이 필드에 정수 (integer) 값이 있어야 합니다. 같은 소수 값 `<Version>2.5</Version>` 은 허용 되지 않습니다.

**힌트:** 다음과 같은 XML 주석 태그를 사용 하 여 버전 변경에 대 한 노트를 저장할 수 있습니다 `<!-- -->` .

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**중요**  이 값을 쿼리하여 다음 인스턴스의 기존 서식 파일에 새 버전의 서식 파일을 적용 해야 하는지 여부를 확인 합니다.

-   예약 된 서식 파일 자동 업데이트 작업이 실행 되는 경우

-   업데이트 UevTemplate PowerShell cmdlet이 실행 되는 경우

-   Microsoft\\uev: SettingsLocationTemplate Update 메서드가 WMI를 통해 호출 되는 경우

 

### <a href="" id="author21"></a>Author 요소

**필수: False**

**형식: 문자열**

만든이는 설정 위치 템플릿의 작성자를 식별 합니다. **이름** 및 **전자 메일**이라는 두 개의 선택적 자식 요소가 지원 됩니다. 두 특성은 모두 선택 사항 이지만, 전자 메일 자식 요소가 지정 된 경우 Name 요소와 함께 있어야 합니다. 만든이는 설정 위치 서식 파일에 대 한 연락처의 전체 이름을 나타내고, 전자 메일은 작성자의 전자 메일 주소를 참조 해야 합니다. 이 정보는 [Ue-v 템플릿 갤러리](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)와 같이 공개적으로 게시 된 서식 파일에 포함 하는 것이 좋습니다.

### <a href="" id="processes21"></a>프로세스 및 프로세스 요소

**필수: True**

**Type: Element**

프로세스에는 적어도 하나 이상의 요소가 포함 되어 `<Process>` 있으며, 여기에는 **Filename**, **Architecture**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**이라는 자식 요소가 포함 됩니다. Filename 하위 요소는 필수 이며 나머지는 선택 사항입니다. 완전히 채워진 요소에는 다음 예제와 유사한 태그가 포함 됩니다.

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### 이름이

**필수: True**

**형식: 문자열**

Filename은 파일 시스템에 표시 되는 실행 파일의 실제 이름을 나타냅니다. 이 요소는 템플릿이 프로세스에 적용 되는지 여부를 평가 하기 위해 UE-V에서 사용 하는 기본 조건을 지정 합니다. 이 요소는 설정 위치 템플릿 XML에서 지정 해야 합니다.

올바른 파일 이름은 정규식 \ [^ \\? \ \? \ \ | &lt; &gt; 와 일치 하지 않아야 합니다. /: \] +, 즉 백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 (\\?)이 포함 되지 않을 수 있습니다. \* | &lt; &gt; /또는: 문자.

**힌트:** 이 정규식에 대해 문자열을 테스트 하려면 PowerShell 명령 창을 사용 하 여 **해당 파일 이름에 대 한**실행 파일의 이름을 대체 합니다.

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

**True** 값은 문자열에 잘못 된 문자가 포함 되어 있음을 나타냅니다. 다음은 잘못 된 값의 몇 가지 예입니다.

-   \\\\server\\share\\program.exe

-   프로그램 \ * .exe

-   Pro? ram.exe

-   프로그램 &lt; 1 &gt; .exe

**참고**  UE-V 생성기는 각각 문자 보다 크거나 작은 값을 &gt; &lt; 각각 인코딩합니다.

 

드문 경우 지만 FileName 값에 .exe 확장명을 포함할 필요는 없지만 값의 일부로 지정 해야 합니다. 예를 들어을 `<Filename>MyApplictication.exe</Filename>` 대신 지정 해야 합니다 `<Filename>MyApplictication</Filename>` . 두 번째 예제에서는 실행 파일의 실제 이름이 "MyApplication.exe" 인 경우 템플릿을 프로세스에 적용 하지 않습니다.

### 아키텍처

**필수: False**

**Type: Architecture (String)**

아키텍처는 대상 실행 파일이 컴파일된 프로세서 아키텍처를 나타냅니다. 유효한 값은 32 비트 응용 프로그램 또는 64 비트 응용 프로그램의 Win64에 대 한 Win32입니다. 있는 경우이 태그는 설정 위치 템플릿의 적용 가능성을 특정 응용 프로그램 아키텍처로 제한 합니다. 예를 들어%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\templates\\ MicrosoftOffice2010Win32.xml 및 UE-V와 함께 포함 된 MicrosoftOffice2010Win64.xml 파일을 비교 합니다. 이는 여러 버전의 실행 파일에 대 한 상대 경로가 변경 되거나 프로세서 아키텍처 간에 전환할 때 설정이 추가 또는 제거 된 경우에 유용 합니다.

이 요소가 없으면 설정 위치 템플릿은 프로세스의 아키텍처를 무시 하 고 파일 이름과 기타 특성이 적용 되는 경우 32 및 64 비트 프로세스에 모두 적용 됩니다.

**참고**  UE-V는이 버전의 ARM 프로세서를 지원 하지 않습니다.

 

### ProductName

**필수: False**

**형식: 문자열**

ProductName은 관리 목적 또는 보고를 위해 제품을 식별 하는 데 사용 되는 선택적 요소입니다. ProductName은 해당 값에 정규식 제한이 없다는 점에서 Filename과 다릅니다. 이를 통해 실행 파일 이름이 명확 하지 않을 수 있는 프로세스에 대 한 보다 쉽게 이해 하 게 됩니다. 예:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**필수: False**

**형식: 문자열**

FileDescription은 실행 파일의 관리 설명을 허용 하는 선택적 태그입니다. 자유 텍스트 필드 이며, 실행 파일의 기능을 식별 해야 하는 소프트웨어 패키지 내에서 여러 실행 파일을 구분 하는 데 유용할 수 있습니다.

예를 들어 적합 한 응용 프로그램에서는 다음과 같이 두 실행 파일 (MyApplication.exe 및 MyApplicationHelper.exe)의 함수에 대 한 미리 알림을 제공 하는 것이 유용할 수 있습니다.

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**필수: False**

**형식: 문자열**

ProductVersion는 파일의 주 버전과 부 버전을 참조 하 고 빌드 및 패치 수준에도 해당 합니다. ProductVersion는 선택적 요소 이지만, 지정 하는 경우 적어도 주요 자식 요소를 포함 해야 합니다. 값은 Minimum = "X" Maximum = "Y" 형식의 범위를 표현 해야 합니다. 여기서 X와 Y는 정수입니다. Minimum 및 Maximum 값은 동일할 수 있습니다.

제품 및 파일 버전 요소는 지정 되지 않은 상태로 남아 있을 수 있습니다. 이렇게 하면 서식 파일을 "버전에 맞게 표시" 하 여 템플릿이 지정 된 실행 파일의 모든 버전에 적용 되는 것을 의미 합니다.

**예 1:**

UE-V 생성기에 지정 된 제품 버전: 1.0는 다음과 같은 XML을 생성 합니다.

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**예 2:**

파일 버전: UE-V 생성기에 지정 된 5.0.2.1000는 다음과 같은 XML을 생성 합니다.

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**잘못 된 예제 1-완전 하지 않은 범위:**

최소 특성만 표시 됩니다. 범위에도 Maximum을 포함 해야 합니다.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**잘못 된 예제 2 – 주요 요소 없이 Minor가 지정 되었습니다.**

Minor 요소만 존재 합니다. 주 버전도 포함 해야 합니다.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**필수: False**

**형식: 문자열**

FileVersion은 게시 된 응용 프로그램의 릴리스 버전과 구성 요소 실행 파일의 내부 빌드 세부 정보를 구별 합니다. 대부분의 상업용 응용 프로그램의 경우 이러한 번호는 동일 합니다. 변경 되는 파일의 제품 버전은 파일의 일반 버전 식별을 나타내고, 파일 버전은 파일의 특정 빌드를 나타냅니다 (핫픽스나 업데이트의 경우). 이렇게 하면 검색 논리가 손상 되지 않은 파일을 고유 하 게 식별 합니다.

제품 버전과 특정 실행 파일 버전을 확인 하려면 Windows 탐색기에서 파일을 마우스 오른쪽 단추로 클릭 하 고 속성을 선택한 다음 세부 정보 탭을 클릭 합니다.

응용 프로그램에 FileVersion 요소를 포함 하면 더 세밀 하 게 조정할 수 있지만, 대부분의 응용 프로그램에서는 이러한 검색 논리가 필요 하지 않습니다. ProductVersion 요소 설정이 먼저 검사 되 고 FileVersion이 선택 되어 있는지 확인 합니다. 더 제한적인 설정이 적용 됩니다.

FileVersion의 자식 요소 및 구문 규칙은 ProductVersion와 동일 합니다.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>응용 프로그램 요소

응용 프로그램은 특정 응용 프로그램에 적용 되는 설정의 컨테이너입니다. 다음 필드/형식의 컬렉션입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>필드/형식</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>이름</p></td>
<td align="left"><p>설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 자세한 내용은 Name을 참조 <a href="#name21" data-raw-source="[Name](#name21)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다. 자세한 내용은 ID를 참조 <a href="#id21" data-raw-source="[ID](#id21)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>설명</p></td>
<td align="left"><p>서식 파일에 대 한 설명입니다 (선택 사항).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>버전</p></td>
<td align="left"><p>변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다. 자세한 내용은 버전을 참조 <a href="#version21" data-raw-source="[Version](#version21)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다. 컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다. 설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (2.1에서 도입 된)</p></td>
<td align="left"><p>이 템플릿을이 요소에 지정 된 프로필에만 연결할 수 있으며 WMI 또는 PowerShell을 통해 변경할 수 없음을 지정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>프로세스</p></td>
<td align="left"><p>하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너입니다. 자세한 내용은 프로세스를 참조 <a href="#processes21" data-raw-source="[Processes](#processes21)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정</p></td>
<td align="left"><p>특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다. 여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다. 자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data21" data-raw-source="[Data types](#data21)"> </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>공통 요소

일반적으로 응용 프로그램 요소와 유사 하지만 항상 둘 이상의 응용 프로그램 요소와 연결 됩니다. 공용 섹션은 해당 응용 프로그램 인스턴스 간에 공유 되는 설정 집합을 나타냅니다. 다음 필드/형식의 컬렉션입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>필드/형식</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>이름</p></td>
<td align="left"><p>설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 자세한 내용은 Name을 참조 <a href="#name21" data-raw-source="[Name](#name21)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다. 자세한 내용은 ID를 참조 <a href="#id21" data-raw-source="[ID](#id21)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>설명</p></td>
<td align="left"><p>서식 파일에 대 한 설명입니다 (선택 사항).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>버전</p></td>
<td align="left"><p>변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다. 자세한 내용은 버전을 참조 <a href="#version21" data-raw-source="[Version](#version21)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다. 컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다. 설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (2.1에서 도입 된)</p></td>
<td align="left"><p>이 템플릿을이 요소에 지정 된 프로필에만 연결할 수 있으며 WMI 또는 PowerShell을 통해 변경할 수 없음을 지정 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정</p></td>
<td align="left"><p>특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다. 여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다. 자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data21" data-raw-source="[Data types](#data21)"> </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>SettingsLocationTemplate 요소

이 요소는 단일 응용 프로그램 또는 응용 프로그램 집합에 대 한 설정을 정의 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>필드/형식</strong></p></td>
<td align="left"><p><strong>설명</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>이름</p></td>
<td align="left"><p>설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 자세한 내용은 Name을 참조 <a href="#name21" data-raw-source="[Name](#name21)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다. 자세한 내용은 ID를 참조 <a href="#id21" data-raw-source="[ID](#id21)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>설명</p></td>
<td align="left"><p>서식 파일에 대 한 설명입니다 (선택 사항).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>부록: SettingsLocationTemplate. xsd

다음은 해당 요소, 자식 요소, 특성 및 매개 변수를 보여 주는 SettingsLocationTemplate .xsd 파일입니다.

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## UE-V 2.0 응용 프로그램 템플릿 스키마 참조


이 섹션에서는 UE-V 2.0 설정 위치 템플릿의 XML 구조에 대해 자세히 설명 하 고이 파일 편집에 대 한 지침을 제공 합니다.

### 이 섹션의 내용

-   [XML 선언 및 인코딩 특성](#xml)

-   [네임 스페이스 및 루트 요소](#namespace)

-   [데이터 형식](#data)

-   [Name 요소](#name)

-   [ID 요소](#id)

-   [버전 요소](#version)

-   [Author 요소](#author)

-   [프로세스 및 프로세스 요소](#processes)

-   [응용 프로그램 요소](#application)

-   [공통 요소](#common)

-   [SettingsLocationTemplate 요소](#settingslocationtemplate)

-   [부록: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>XML 선언 및 인코딩 특성

**필수: True**

**형식: 문자열**

XML 선언에서는 XML 버전 1.0 특성 ( &lt; ? XML 버전 = "1.0")을 지정 해야 합니다 &gt; . UE-V 생성기에서 만든 설정 위치 템플릿은 해당 인코딩이 명시적으로 지정 되어 있지 않지만 UTF-8 인코딩으로 저장 됩니다. 이 요소에 encoding = "UTF-8" 특성을 가장 좋은 방법으로 포함 하는 것이 좋습니다. 제품에 포함 된 모든 서식 파일은이 태그를 지정 합니다 (참조용%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\Templates 문서 참조). 예:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>네임 스페이스 및 루트 요소

**필수: True**

**형식: 문자열**

UE-V는 https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate 모든 응용 프로그램에 대 한 네임 스페이스를 사용 합니다. SettingsLocationTemplate은 루트 요소 이며 다른 모든 요소를 포함 합니다. 이 태그를 사용 하 여 모든 템플릿의 Reference SettingsLocationTemplate:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>데이터 형식

다음은 UE-V 응용 프로그램 템플릿 스키마에 대 한 데이터 형식입니다.

<a href="" id="guid"></a>**GUID** GUID는 "\\ {\ [a-fA-F0-9 \]-\ [a-fA-F0-9 \] 형식으로 된 표준 전역 고유 식별자 정규식을 설명 합니다. {8} {4} [a-Fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \\}". Filesetting\\Root\\KnownFolder 요소에서 잘 알려진 폴더의 서식을 확인 하는 데 사용 됩니다.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString는 모니터링할 프로세스의 파일 이름을 나타냅니다. 해당 값은 regex \ [^ \\ \ \\? \ \ \ * \ \ | &lt; &gt; 에 의해 제한 됩니다. /: \] +, (백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 문자를 포함 하지 않을 수 있습니다.)

<a href="" id="idstring"></a>**Idstring** IDString은 응용 프로그램 요소의 ID 값, SettingsLocationTemplate, 공통 요소 (공통 설정을 공유 하는 응용 프로그램 제품군을 설명 하는 데 사용 됨)를 나타냅니다. FilenameString (\\ [^ \\? \\ | &lt; &gt; )와 동일한 regex로 제한 됩니다. /:\]+).

<a href="" id="templateversion"></a>**서식 버전** 서식 파일 버전은 설정 위치 템플릿의 수정을 설명 하는 데 사용 되는 정수 값입니다. 값의 범위는 0 ~ 2147483647입니다.

<a href="" id="empty"></a>**비어 있음** Empty는 null 값을 참조 합니다. 이는 처리할 프로세스가 없다는 것을 나타내기 위해 Process\\ShellProcess에 사용 됩니다. 이 값은 응용 프로그램 템플릿에서 사용해 서는 안 됩니다.

<a href="" id="author"></a>**만든이** Author 데이터 형식은 서식 파일의 작성자를 식별 하는 복잡 한 유형입니다. 여기에는 **이름** 및 **전자 메일**이라는 두 개의 자식 요소가 포함 됩니다. Author 데이터 형식 내에서 Name 요소는 필수 항목이 며 전자 메일 요소는 선택 사항입니다. 이 형식은 SettingsLocationTemplate 요소 아래에 자세히 설명 되어 있습니다.

<a href="" id="range"></a>**범위** 범위는 **최소** 및 **최대**의 두 자식 요소로 구성 된 integer 클래스를 정의 합니다. 이 데이터 형식은 ProcessVersion 데이터 형식에서 구현 됩니다. 지정 된 경우 최소 및 최대 값을 모두 포함 해야 합니다.

<a href="" id="processversion"></a>**Processversion** ProcessVersion은 **주**, **부**, **빌드**, **패치**등 네 가지 자식 요소를 사용 하 여 형식을 정의 합니다. 이 데이터 형식은 Process 요소에서 ProductVersion 및 FileVersion 값을 채우는 데 사용 됩니다. 이 유형의 데이터는 범위 값입니다. 주요 자식 요소는 필수 이며 나머지는 선택 사항입니다.

<a href="" id="architecture"></a>**아키텍처가** 아키텍처에는 두 가지 가능 값 ( **Win32** 및 **Win64**)이 열거 됩니다. 이러한 값은 프로세스 아키텍처를 지정 하는 데 사용 됩니다.

<a href="" id="process"></a>**공정** 프로세스 데이터 형식은 UE-V를 통해 모니터링할 프로세스를 설명 하는 데 사용 되는 컨테이너입니다. 여기에는 **파일 이름**, **아키텍처**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**의 여섯 가지 하위 요소가 포함 되어 있습니다. 이 표에서는 각 요소의 해당 데이터 형식에 대해 자세히 설명 합니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소</th>
<th align="left">데이터 형식</th>
<th align="left">Mandatory</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이름이</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="even">
<td align="left"><p>아키텍처</p></td>
<td align="left"><p>아키텍처</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>문자열</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**프로세스** 프로세스 데이터 형식은 하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너를 나타냅니다. 프로세스 시퀀스 형식에서 처리 되는 두 개의 자식 요소에는 **process** 와 **shellprocess**지원 됩니다. 프로세스는 유형 프로세스의 요소이 고 ShellProcess는 데이터 형식이 비어 있습니다. 순서에서 하나 이상의 항목을 식별 해야 합니다.

<a href="" id="path"></a>**경로** RegistrySetting 및 FileSetting에서 Path를 사용 하 여 레지스트리와 파일 경로를 참조 합니다. 이 요소는 선택적 특성 두 개를 지원 합니다. **재귀** 및 **Deletfnota가 발견**되었습니다. 두 값 모두 default = "False"로 설정 됩니다.

Recursive는 경로 및 모든 하위 폴더가 파일 설정에 포함 되거나 모든 하위 레지스트리 키가 레지스트리 설정에 포함 됨을 나타냅니다. 두 경우 모두 현재 수준의 모든 항목이 캡처한 데이터에 포함 됩니다. FileSettings 개체의 경우 지정 된 폴더 내의 모든 파일이 UE-V를 통해 캡처한 데이터에 포함 되지만 폴더는 포함 되지 않습니다. 레지스트리 경로의 경우 현재 경로에 있는 모든 값이 캡처되고 자식 레지스트리 키가 캡처되지 않습니다. 두 경우 모두 대규모 데이터 집합 또는 많은 수의 항목을 캡처하는 것을 방지 하기 위해 주의를 기울여야 합니다.

DeleteIfNotFound 특성은 사용자의 설정 저장소 경로 데이터에서 설정을 제거 합니다. 이는 패키지에서 이러한 설정을 제거 하 여 설정 저장소 경로 파일 서버에 많은 양의 디스크 공간이 저장 되는 경우에 유용할 수 있습니다.

<a href="" id="filemask"></a>**FileMask** FileMask는 Path로 정의 된 폴더에 대 한 특정 파일 형식만 지정 합니다. 예를 들어 Path는 `C:\users\username\files` `*.txt` 텍스트 파일만 포함 하 고 FileMask 수 있습니다.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting는 레지스트리 키 및 값에 대 한 컨테이너와 UE-V 에이전트의 부분에 대 한 연결 된 원하는 동작을 나타냅니다. **Path**, **Name**, **Exclude**, 값 **경로** 및 **이름의**시퀀스를 포함 하 여 네 개의 자식 요소가이 형식으로 정의 됩니다.

<a href="" id="filesetting"></a>**Filesetting** FileSetting에는 파일 및 파일 경로와 연결 된 매개 변수가 포함 됩니다. **루트**, **경로**, **FileMask**및 **Exclude**의 네 가지 자식 요소가 정의 되어 있습니다. Root는 필수 이며 나머지는 선택 사항입니다.

<a href="" id="settings"></a>**설정** 설정은 특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다. 여기에는 앞에서 설명한 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다. 또한 다음과 같은 동작이 포함 된 다음 자식 요소도 포함할 수 있습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>비동기</p></td>
<td align="left"><p>비동기 설정 패키지는 응용 프로그램 시작을 차단 하지 않고 적용 되므로 설정이 계속 적용 되는 동안 응용 프로그램을 계속 진행할 수 있습니다. 이 방법은 SystemParameterSetting과 같이 API를 통해 비동기적으로 적용할 수 있는 설정에 유용 <code>get/set</code> 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>기본적으로 UE-V는 템플릿을 사용 하는 응용 프로그램의 마지막 인스턴스가 닫혀 있을 때만 응용 프로그램에 대 한 설정을 저장 합니다. 이 요소를 ' f l l e '로 설정 하면 UE-V가 응용 프로그램의 다른 인스턴스가 실행 되는 경우에도 설정을 내보냅니다. 적합 한 서식 파일 – UE-V를 사용 하 여 제공 되는 공용 요소 섹션이 포함 된 경우이 플래그를 사용 하 여 마지막 인스턴스가 닫힐 때까지 응용 프로그램 관련 설정이 내보내기 되지 않도록 하 여 응용 프로그램을 닫을 때 공유 설정을 항상 내보낼 수 있도록 합니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Name 요소

**필수: True**

**형식: 문자열**

Name은 설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 일반적으로 버전 정보를 참조 하지 않도록 하는 것은 ProductVersion 요소와는 다른 것이 될 수 있기 때문입니다. 예를 들어, `<Name>My Application</Name>` 대신를 지정 `<Name>My Application 1.1</Name>` 합니다.

**참고**  UE-V는 외부 Dtd를 참조 하지 않으므로 설정 위치 템플릿에서 명명 된 엔터티를 사용할 수 없습니다. 예를 들어 &reg; 등록 된 무역 표시 기호®를 참조 하는 데 사용 하지 마세요. 대신 정식 번호 매기기 참조를 사용 하 여 이러한 유형의 특수 문자를 포함 합니다 (예:® 문자에 대 한 & \ #174). 이 규칙은이 문서의 모든 문자열 값에 적용 됩니다.

<http://www.w3.org/TR/xhtml1/dtds.html>전체 문자 엔터티 목록을 보려면을 참조 하세요. U t f-8로 인코딩된 문서에는 유니코드 문자가 직접 포함 될 수 있습니다. UE-V 생성기를 통해 템플릿을 저장 하면 문자 엔터티가 해당 유니코드 표현으로 자동 변환 됩니다.

 

### <a href="" id="id"></a>ID 요소

**필수: True**

**형식: 문자열**

ID는 특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다 (예: Get-help Evtemplate 및 가져오기-Uevtemplate 파일 프로그램 PowerShell cmdlet의 출력 참조). 규칙에 따라이 태그에는 모든 공백을 포함할 수 없으며 스크립팅이 간단해 집니다. 또는 등의 템플릿을 쉽게 식별할 수 있도록이 요소에 응용 프로그램의 버전 번호를 지정 해야 합니다 `<ID>MicrosoftCalculator6</ID>` `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>버전 요소

**필수: True**

**유형: Integer**

**최 솟 값: 0**

**최 댓 값: 2147483647**

버전은 변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다. UE-V 생성기는 템플릿이 저장 될 때마다이 번호를 하나씩 자동으로 증가 시킵니다. 이 필드에 정수 (integer) 값이 있어야 합니다. 같은 소수 값 `<Version>2.5</Version>` 은 허용 되지 않습니다.

**힌트:** 다음과 같은 XML 주석 태그를 사용 하 여 버전 변경에 대 한 노트를 저장할 수 있습니다 `<!-- -->` .

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**중요**  이 값을 쿼리하여 다음 인스턴스의 기존 서식 파일에 새 버전의 서식 파일을 적용 해야 하는지 여부를 확인 합니다.

-   예약 된 서식 파일 자동 업데이트 작업이 실행 되는 경우

-   업데이트 UevTemplate PowerShell cmdlet이 실행 되는 경우

-   Microsoft\\uev: SettingsLocationTemplate Update 메서드가 WMI를 통해 호출 되는 경우

 

### <a href="" id="author"></a>Author 요소

**필수: False**

**형식: 문자열**

만든이는 설정 위치 템플릿의 작성자를 식별 합니다. **이름** 및 **전자 메일**이라는 두 개의 선택적 자식 요소가 지원 됩니다. 두 특성은 모두 선택 사항 이지만, 전자 메일 자식 요소가 지정 된 경우 Name 요소와 함께 있어야 합니다. 만든이는 설정 위치 서식 파일에 대 한 연락처의 전체 이름을 나타내고, 전자 메일은 작성자의 전자 메일 주소를 참조 해야 합니다. 이 정보는 [Ue-v 템플릿 갤러리](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V)와 같이 공개적으로 게시 된 서식 파일에 포함 하는 것이 좋습니다.

### <a href="" id="processes"></a>프로세스 및 프로세스 요소

**필수: True**

**Type: Element**

프로세스에는 적어도 하나 이상의 요소가 포함 되어 `<Process>` 있으며, 여기에는 **Filename**, **Architecture**, **ProductName**, **filedescription**, **ProductVersion**및 **filedescription**이라는 자식 요소가 포함 됩니다. Filename 하위 요소는 필수 이며 나머지는 선택 사항입니다. 완전히 채워진 요소에는 다음 예제와 유사한 태그가 포함 됩니다.

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### 이름이

**필수: True**

**형식: 문자열**

Filename은 파일 시스템에 표시 되는 실행 파일의 실제 이름을 나타냅니다. 이 요소는 템플릿이 프로세스에 적용 되는지 여부를 평가 하기 위해 UE-V에서 사용 하는 기본 조건을 지정 합니다. 이 요소는 설정 위치 템플릿 XML에서 지정 해야 합니다.

올바른 파일 이름은 정규식 \ [^ \\? \ \? \ \ | &lt; &gt; 와 일치 하지 않아야 합니다. /: \] +, 즉 백슬래시 문자, 별표 또는 물음표 와일드 카드 문자, 파이프 문자, 기호 보다 크거나 작음, 슬래시 또는 콜론 (\\?)이 포함 되지 않을 수 있습니다. \* | &lt; &gt; /또는: 문자.

**힌트:** 이 정규식에 대해 문자열을 테스트 하려면 PowerShell 명령 창을 사용 하 여 **해당 파일 이름에 대 한**실행 파일의 이름을 대체 합니다.

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

**True** 값은 문자열에 잘못 된 문자가 포함 되어 있음을 나타냅니다. 다음은 잘못 된 값의 몇 가지 예입니다.

-   \\\\server\\share\\program.exe

-   프로그램 \ * .exe

-   Pro? ram.exe

-   프로그램 &lt; 1 &gt; .exe

**참고**  UE-V 생성기는 각각 문자 보다 크거나 작은 값을 &gt; &lt; 각각 인코딩합니다.

 

드문 경우 지만 FileName 값에 .exe 확장명을 포함할 필요는 없지만 값의 일부로 지정 해야 합니다. 예를 들어을 `<Filename>MyApplictication.exe</Filename>` 대신 지정 해야 합니다 `<Filename>MyApplictication</Filename>` . 두 번째 예제에서는 실행 파일의 실제 이름이 "MyApplication.exe" 인 경우 템플릿을 프로세스에 적용 하지 않습니다.

### 아키텍처

**필수: False**

**Type: Architecture (String)**

아키텍처는 대상 실행 파일이 컴파일된 프로세서 아키텍처를 나타냅니다. 유효한 값은 32 비트 응용 프로그램 또는 64 비트 응용 프로그램의 Win64에 대 한 Win32입니다. 있는 경우이 태그는 설정 위치 템플릿의 적용 가능성을 특정 응용 프로그램 아키텍처로 제한 합니다. 예를 들어%ProgramFiles%\\Microsoft 사용자 환경 Virtualization\\templates\\ MicrosoftOffice2010Win32.xml 및 UE-V와 함께 포함 된 MicrosoftOffice2010Win64.xml 파일을 비교 합니다. 이는 여러 버전의 실행 파일에 대 한 상대 경로가 변경 되거나 프로세서 아키텍처 간에 전환할 때 설정이 추가 또는 제거 된 경우에 유용 합니다.

이 요소가 없으면 설정 위치 템플릿은 프로세스의 아키텍처를 무시 하 고 파일 이름과 기타 특성이 적용 되는 경우 32 및 64 비트 프로세스에 모두 적용 됩니다.

**참고**  UE-V는이 버전의 ARM 프로세서를 지원 하지 않습니다.

 

### ProductName

**필수: False**

**형식: 문자열**

ProductName은 관리 목적 또는 보고를 위해 제품을 식별 하는 데 사용 되는 선택적 요소입니다. ProductName은 해당 값에 정규식 제한이 없다는 점에서 Filename과 다릅니다. 이를 통해 실행 파일 이름이 명확 하지 않을 수 있는 프로세스에 대 한 보다 쉽게 이해 하 게 됩니다. 예:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**필수: False**

**형식: 문자열**

FileDescription은 실행 파일의 관리 설명을 허용 하는 선택적 태그입니다. 자유 텍스트 필드 이며, 실행 파일의 기능을 식별 해야 하는 소프트웨어 패키지 내에서 여러 실행 파일을 구분 하는 데 유용할 수 있습니다.

예를 들어 적합 한 응용 프로그램에서는 다음과 같이 두 실행 파일 (MyApplication.exe 및 MyApplicationHelper.exe)의 함수에 대 한 미리 알림을 제공 하는 것이 유용할 수 있습니다.

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**필수: False**

**형식: 문자열**

ProductVersion는 파일의 주 버전과 부 버전을 참조 하 고 빌드 및 패치 수준에도 해당 합니다. ProductVersion는 선택적 요소 이지만, 지정 하는 경우 적어도 주요 자식 요소를 포함 해야 합니다. 값은 Minimum = "X" Maximum = "Y" 형식의 범위를 표현 해야 합니다. 여기서 X와 Y는 정수입니다. Minimum 및 Maximum 값은 동일할 수 있습니다.

제품 및 파일 버전 요소는 지정 되지 않은 상태로 남아 있을 수 있습니다. 이렇게 하면 서식 파일을 "버전에 맞게 표시" 하 여 템플릿이 지정 된 실행 파일의 모든 버전에 적용 되는 것을 의미 합니다.

**예 1:**

UE-V 생성기에 지정 된 제품 버전: 1.0는 다음과 같은 XML을 생성 합니다.

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**예 2:**

파일 버전: UE-V 생성기에 지정 된 5.0.2.1000는 다음과 같은 XML을 생성 합니다.

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**잘못 된 예제 1-완전 하지 않은 범위:**

최소 특성만 표시 됩니다. 범위에도 Maximum을 포함 해야 합니다.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**잘못 된 예제 2 – 주요 요소 없이 Minor가 지정 되었습니다.**

Minor 요소만 존재 합니다. 주 버전도 포함 해야 합니다.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**필수: False**

**형식: 문자열**

FileVersion은 게시 된 응용 프로그램의 릴리스 버전과 구성 요소 실행 파일의 내부 빌드 세부 정보를 구별 합니다. 대부분의 상업용 응용 프로그램의 경우 이러한 번호는 동일 합니다. 변경 되는 파일의 제품 버전은 파일의 일반 버전 식별을 나타내고, 파일 버전은 파일의 특정 빌드를 나타냅니다 (핫픽스나 업데이트의 경우). 이렇게 하면 검색 논리가 손상 되지 않은 파일을 고유 하 게 식별 합니다.

제품 버전과 특정 실행 파일 버전을 확인 하려면 Windows 탐색기에서 파일을 마우스 오른쪽 단추로 클릭 하 고 속성을 선택한 다음 세부 정보 탭을 클릭 합니다.

응용 프로그램에 FileVersion 요소를 포함 하면 더 세밀 하 게 조정할 수 있지만, 대부분의 응용 프로그램에서는 이러한 검색 논리가 필요 하지 않습니다. ProductVersion 요소 설정이 먼저 검사 되 고 FileVersion이 선택 되어 있는지 확인 합니다. 더 제한적인 설정이 적용 됩니다.

FileVersion의 자식 요소 및 구문 규칙은 ProductVersion와 동일 합니다.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>응용 프로그램 요소

응용 프로그램은 특정 응용 프로그램에 적용 되는 설정의 컨테이너입니다. 다음 필드/형식의 컬렉션입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필드/형식</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이름</p></td>
<td align="left"><p>설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 자세한 내용은 Name을 참조 <a href="#name" data-raw-source="[Name](#name)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다. 자세한 내용은 ID를 참조 <a href="#id" data-raw-source="[ID](#id)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>서식 파일에 대 한 설명입니다 (선택 사항).</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>버전</p></td>
<td align="left"><p>변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다. 자세한 내용은 버전을 참조 <a href="#version" data-raw-source="[Version](#version)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다. 컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다. 설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>프로세스</p></td>
<td align="left"><p>하나 이상의 프로세스 요소 컬렉션에 대 한 컨테이너입니다. 자세한 내용은 프로세스를 참조 <a href="#processes" data-raw-source="[Processes](#processes)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>설정</p></td>
<td align="left"><p>특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다. 여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다. 자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data" data-raw-source="[Data types](#data)"> </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>공통 요소

일반적으로 응용 프로그램 요소와 유사 하지만 항상 둘 이상의 응용 프로그램 요소와 연결 됩니다. 공용 섹션은 해당 응용 프로그램 인스턴스 간에 공유 되는 설정 집합을 나타냅니다. 다음 필드/형식의 컬렉션입니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필드/형식</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이름</p></td>
<td align="left"><p>설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 자세한 내용은 Name을 참조 <a href="#name" data-raw-source="[Name](#name)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다. 자세한 내용은 ID를 참조 <a href="#id" data-raw-source="[ID](#id)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>서식 파일에 대 한 설명입니다 (선택 사항).</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>버전</p></td>
<td align="left"><p>변경 내용에 대 한 관리 추적에 대 한 설정 위치 템플릿의 버전을 식별 합니다. 자세한 내용은 버전을 참조 <a href="#version" data-raw-source="[Version](#version)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>이 템플릿을 Microsoft 계정과 함께 사용할 수 있는지 여부를 제어 합니다. 컴퓨터의 사용자에 대해 MSA 동기화를 사용 하도록 설정 하면이 서식 파일이 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>MSA와 유사 하 게,이 템플릿을 Office365와 함께 사용할 수 있는지 여부를 제어 합니다. 설정을 동기화 하는 데 Office 365를 사용 하는 경우이 서식 파일은 자동으로 비활성화 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설정</p></td>
<td align="left"><p>특정 서식 파일에 적용 되는 모든 설정의 컨테이너입니다. 여기에는 레지스트리, 파일, SystemParameter 및 CustomAction 설정의 인스턴스가 포함 됩니다. 자세한 내용은 <strong> 데이터 형식의 설정을 참조 </strong> 하세요 <a href="#data" data-raw-source="[Data types](#data)"> </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>SettingsLocationTemplate 요소

이 요소는 단일 응용 프로그램 또는 응용 프로그램 집합에 대 한 설정을 정의 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필드/형식</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>이름</p></td>
<td align="left"><p>설정 위치 템플릿의 고유한 이름을 지정 합니다. 이것은 WMI, PowerShell, 이벤트 뷰어, 디버그 로그에서 템플릿을 참조할 때 표시 목적으로 사용 됩니다. 자세한 내용은 Name을 참조 <a href="#name" data-raw-source="[Name](#name)"> 하세요 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>특정 서식 파일의 고유 식별자를 채웁니다. 이 태그는 UE-V Agent가 런타임에 템플릿을 참조 하는 데 사용 하는 기본 식별자가 됩니다. 자세한 내용은 ID를 참조 <a href="#id" data-raw-source="[ID](#id)"> 하세요 </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>설명</p></td>
<td align="left"><p>서식 파일에 대 한 설명입니다 (선택 사항).</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>UI에 표시 되 고 언어 로캘로 지역화 되는 선택적 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>언어 로캘로 지역화 된 선택적 템플릿 설명입니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>부록: SettingsLocationTemplate. xsd

다음은 해당 요소, 자식 요소, 특성 및 매개 변수를 보여 주는 SettingsLocationTemplate .xsd 파일입니다.

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## 관련 항목


[사용자 지정 UE-V 2. x 템플릿 및 UE-V 2 .x 생성기 사용](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[UE-V 2.x에 대한 기술 참조](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





