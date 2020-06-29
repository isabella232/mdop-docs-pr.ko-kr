---
title: 연결 그룹 파일 정보
description: 연결 그룹 파일 정보
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814932"
---
# 연결 그룹 파일 정보


**이 항목의 내용:**

-   [연결 그룹 파일 용도 및 위치](#bkmk-cg-purpose-loc)

-   [연결 그룹 XML 파일의 구조](#bkmk-define-cg-5-0sp3)

-   [연결 그룹의 패키지 우선 순위 구성](#bkmk-config-pkg-priority-incg)

-   [지원 되는 가상 응용 프로그램 연결 구성](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>연결 그룹 파일 용도 및 위치


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>연결 그룹 용도</p></td>
<td align="left"><p>연결 그룹은 패키지를 그룹화 하 여 패키지의 응용 프로그램이 서로 상호 작용할 수 있는 가상 환경을 만드는 데 사용 되는 App-v 기능입니다.</p>
<p>예: Microsoft Office에서 플러그 인을 사용 하려고 합니다. 플러그 인을 포함 하는 패키지를 만들고, Office를 포함 하는 다른 패키지를 만든 다음 두 패키지를 연결 그룹에 추가 하 여 Office에서 해당 플러그 인을 사용할 수 있도록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>연결 그룹 파일 작동 방식</p></td>
<td align="left"><p>응용 프로그램 가상화 5.0 연결 그룹 파일을 적용 하면 파일에 열거 된 패키지가 런타임 시 단일 가상 환경으로 결합 됩니다. Microsoft App-v (Application Virtualization) 5.0 연결 그룹 파일을 사용 하 여 기존 Application Virtualization 5.0 연결 그룹을 구성 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>예제 파일 경로</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>연결 그룹 XML 파일의 구조


**이 섹션의 내용:**

-   [연결 그룹을 정의 하는 매개 변수](#bkmk-params-define-cg)

-   [연결 그룹의 패키지를 정의 하는 매개 변수](#bkmk-params-define-pkgs-incg)

-   [App-v 5.0 SP3 예제 연결 그룹 XML 파일](#bkmk-50sp3-exp-cg-xml)

-   [앱-V 5.0 ~ App-v 5.0 SP2 연결 그룹 XML 파일 예](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>연결 그룹을 정의 하는 매개 변수

다음 표에서는 패키지를 제외한 연결 그룹 자체를 정의 하는 XML 파일의 매개 변수에 대해 설명 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필드</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>스키마 이름</p></td>
<td align="left"><p>스키마의 이름입니다.</p>
<p><strong>App-v 5.0 SP3에서 시작 가능 </strong> :이 표에 설명 된 새로운 "선택적 패키지" 및 "모든 버전 사용" 기능을 사용 하려는 경우 XML 파일에서 다음 스키마를 지정 해야 합니다.</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>이 연결 그룹의 고유 GUID 식별자입니다. 연결 그룹 상태는이 식별자와 연결 됩니다. 연결 그룹을 만들 때만이 식별자를 지정 합니다.</p>
<p>다음을 입력 하 여 새 GUID를 만들 수 있습니다 <strong>[Guid]::NewGuid()</strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>#</p></td>
<td align="left"><p>이 버전의 연결 그룹에 대 한 버전 GUID 식별자입니다.</p>
<p>연결 그룹을 업데이트 하는 경우 (예: 새 패키지를 추가 하거나 업데이트 하는 경우) 새 버전을 반영 하도록 버전 GUID를 업데이트 해야 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>연결 그룹의 표시 이름입니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Priority</p></td>
<td align="left"><p>연결 그룹의 선택적 우선 순위 필드입니다.</p>
<p><strong>"0" </strong> - 은 가장 높은 우선 순위를 나타냅니다.</p>
<p>우선 순위가 필요 하지만 구성 되지 않은 경우에는 사용할 올바른 연결 그룹을 확인할 수 없기 때문에 패키지가 실패 합니다.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>연결 그룹의 패키지를 정의 하는 매개 변수

&lt; &gt; 연결 그룹 XML 파일의 패키지 섹션에서 다음 표에 설명 된 대로 각 패키지의 고유한 패키지 식별자 및 버전 식별자를 지정 하 여 연결 그룹의 구성원 패키지를 나열 합니다. 목록의 첫 번째 패키지는 우선 순위가 가장 높습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필드</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageId</p></td>
<td align="left"><p>이 패키지의 고유 GUID 식별자입니다. 이 GUID는 최신 버전의 패키지를 게시할 때 변경 되지 않습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>#</p></td>
<td align="left"><p>패키지 버전의 고유 GUID 식별자입니다.</p>
<p><strong>App-v 5.0 SP3에서 시작 가능 </strong> : <strong> 패키지 버전에 "*"를 지정 하면 </strong> 사용 가능한 최신 패키지 버전의 GUID가 동적으로 삽입 됩니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IsOptional</p></td>
<td align="left"><p><strong>앱-V 5.0 SP3 </strong> : 연결 그룹 내에서 패키지를 선택적으로 만들 수 있도록 하는 매개 변수를 시작할 수 있습니다. 유효한 항목은 다음과 같습니다.</p>
<ul>
<li><p><strong>"true" </strong> – 연결 그룹의 패키지가 선택 사항입니다.</p></li>
<li><p><strong>"false" </strong> – 연결 그룹에 패키지가 필요 합니다.</p></li>
</ul>
<p><a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)">연결 그룹에서 선택적 패키지를 사용 하는 방법에 대해 알아봅니다 </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>App-v 5.0 SP3 예제 연결 그룹 XML 파일

다음 예제 연결 그룹 XML 파일은 이전 표의 필드 예를 보여 주고 App-v 5.0 SP3 용 새 항목을 강조 표시 합니다.

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>앱-V 5.0 ~ App-v 5.0 SP2 연결 그룹 XML 파일 예

다음 예제 연결 그룹 XML 파일은 앱-V 5.0 SP2를 통해 App-v 5.0에 적용 됩니다. 앞의 표에는 필드의 예가 표시 되지만 App-v 5.0 SP3에 대해 위에서 설명한 변경 사항은 제외 됩니다.

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>연결 그룹의 패키지 우선 순위 구성


패키지 우선 순위는 패키지 목록 순서를 사용 하 여 구성 됩니다. 문서의 첫 번째 패키지는 우선 순위가 가장 높습니다. 목록의 후속 패키지에는 우선 순위가 내림차순으로 표시 됩니다.

패키지 우선 순위는 가상 환경 초기화 중에 불가피 한 리소스 충돌의 해상도입니다. 예를 들어 동일한 가상 환경에서 여는 두 패키지가 동일한 레지스트리 DWORD 값을 정의 하는 경우 우선 순위가 가장 높은 패키지가 설정 된 값을 결정 합니다.

연결 그룹 파일을 사용 하 여 다음 방법을 사용 하 여 각 연결 그룹을 구성할 수 있습니다.

-   연결 그룹에 대 한 런타임 우선 순위를 지정 합니다.

    **참고**  우선 순위는 패키지가 둘 이상의 연결 그룹과 연결 된 경우에만 필요 합니다.

     

-   연결 그룹 내에서 패키지 우선 순위를 지정 합니다.

실행 중인 가상 응용 프로그램이 Microsoft Windows 탐색기와 같은 네이티브 응용 프로그램 요청에서 시작 되는 경우 priority 필드가 필요 합니다. App-v 클라이언트는 우선 순위를 사용 하 여 응용 프로그램을 실행할 연결 그룹 가상 환경을 결정 합니다. 이 문제는 가상 응용 프로그램이 여러 연결 그룹에 속해 있는 경우에 발생 합니다.

다른 가상 응용 프로그램을 사용 하 여 가상 응용 프로그램을 열면 원래 가상 응용 프로그램의 가상 환경이 사용 됩니다. 이 경우 우선 순위 필드는 사용 되지 않습니다.

**예:**

Microsoft Outlook이 가상 환경 **XYZ**에서 실행 되 고 있는 가상 응용 프로그램 연결 된 microsoft word 문서를 열면 가상화 된 Microsoft word의 연결 그룹 또는 런타임 우선 순위에 관계 없이 가상 환경 **XYZ**에서 microsoft word가 열립니다.

## <a href="" id="bkmk-va-conn-configs"></a>지원 되는 가상 응용 프로그램 연결 구성


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">구성</th>
<th align="left">예제 시나리오</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>대. exe 파일 및 플러그 인 (.dll)</p></td>
<td align="left"><ul>
<li><p>Microsoft Office를 모든 사용자에 게 배포 하지만 Microsoft Excel 플러그 인을 사용자의 하위 집합에만 배포 하려고 합니다.</p></li>
<li><p>적절 한 사용자에 대 한 연결 그룹을 사용 하도록 설정 합니다.</p></li>
<li><p>필요에 따라 각 패키지를 개별적으로 업데이트 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>대. exe 파일 및 미들웨어 응용 프로그램</p></td>
<td align="left"><ul>
<li><p>응용 프로그램에 미들웨어 응용 프로그램이 나 모두 동일한 미들웨어 런타임 버전에 의존 하는 여러 응용 프로그램이 필요한 경우</p></li>
<li><p>하나 이상의 응용 프로그램이 필요한 모든 컴퓨터는 응용 프로그램 및 미들웨어 응용 프로그램 런타임과 연결 그룹을 수신 합니다.</p></li>
<li><p>필요에 따라 여러 미들웨어 응용 프로그램을 단일 연결 그룹으로 결합할 수 있습니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">예</th>
<th align="left">예제 설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>재무 디비전에 대 한 가상 응용 프로그램 연결 그룹</p></td>
<td align="left"><ul>
<li><p>미들웨어 애플리케이션 1</p></li>
<li><p>미들웨어 애플리케이션 2</p></li>
<li><p>미들웨어 애플리케이션 3</p></li>
<li><p>미들웨어 응용 프로그램 런타임</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>HR 디비전에 대 한 가상 응용 프로그램 연결 그룹</p></td>
<td align="left"><ul>
<li><p>미들웨어 애플리케이션 5</p></li>
<li><p>미들웨어 애플리케이션 6</p></li>
<li><p>미들웨어 응용 프로그램 런타임</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>대. exe 파일 및 .exe 파일</p></td>
<td align="left"><p>다른 응용 프로그램에 의존 하는 응용 프로그램이 있고 운영 효율성, 라이선스 제한 또는 출시 시간 표시 막대에 대해 패키지를 유지 하려는 경우</p>
<p><strong>예:</strong></p>
<p>Microsoft Lync 2010를 배포 하는 경우 다음 세 가지 패키지를 사용할 수 있습니다.</p>
<ul>
<li><p>Microsoft Office2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>다음 연결 그룹을 사용 하 여 배포를 관리할 수 있습니다.</p>
<ul>
<li><p>Microsoft Office2010 및 Microsoft Communicator2007</p></li>
<li><p>Microsoft Office2010 및 Microsoft Lync2010</p></li>
</ul>
<p>배포가 완료 되 면 하나의 새 Microsoft Office2010 + Microsoft Lync2010 패키지를 만들거나, 별도의 패키지로 유지 하 고 유지 관리 하 고, 연결 그룹을 사용 하 여 배포할 수 있습니다.</p></td>
</tr>
</tbody>
</table>

 






## 관련 항목


[연결 그룹 관리](managing-connection-groups.md)

 

 





