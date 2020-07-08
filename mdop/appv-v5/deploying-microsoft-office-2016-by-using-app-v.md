---
title: App-V를 사용하여 Microsoft Office 2016 배포
description: App-V를 사용하여 Microsoft Office 2016 배포
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814620"
---
# App-V를 사용하여 Microsoft Office 2016 배포


Microsoft Application Virtualization 5.0 이상 버전을 사용 하 여 조직의 컴퓨터에 Microsoft Office 2016을 가상화 된 응용 프로그램으로 제공 하려면이 문서의 정보를 사용 합니다. Office 2013를 제공 하기 위해 App-v를 사용 하는 방법에 대 한 자세한 내용은 [app-v를 사용 하 여 Microsoft Office 2013 배포](deploying-microsoft-office-2013-by-using-app-v.md)를 참조 하세요. Office 2010를 제공 하기 위해 App-v를 사용 하는 방법에 대 한 자세한 내용은 [app-v를 사용 하 여 Microsoft Office 2010 배포](deploying-microsoft-office-2010-by-using-app-v.md)를 참조 하세요.

이 항목의 섹션:

-   [시작 하기 전에 알아야 할 사항](#bkmk-before-you-start)

-   [Office 배포 도구를 사용 하 여 App-v 용 Office 2016 패키지 만들기](#bkmk-create-office-pkg)

-   [앱에 대 한 Office 패키지 게시-V 5.0](#bkmk-pub-pkg-office)

-   [Office 앱-V 패키지 사용자 지정 및 관리](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a>시작 하기 전에 알아야 할 사항


App-v를 사용 하 여 Office 2016를 배포 하기 전에 다음 계획 정보를 검토 합니다.

### <a href="" id="bkmk-supp-vers-coexist"></a>지원 되는 Office 버전 및 Office 공존

다음 표를 사용 하 여 지원 되는 Office 버전에 대 한 정보를 확인 하 고 공존할 수 있는 Office 버전을 실행 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">검토할 정보</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)">지원 되는 Microsoft Office 버전</a></p></td>
<td align="left"><ul>
<li><p>지원 되는 Office 버전</p></li>
<li><p>지원 되는 배포 유형 (예: 데스크톱, VDI (개인용 가상 데스크톱 인프라), 풀링된 VDI)</p></li>
<li><p>Office 라이선스 옵션</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)">동시 버전의 Office를 사용 하 여 App-v 사용 계획</a></p></td>
<td align="left"><p>같은 컴퓨터에 여러 버전의 Office를 설치할 때의 고려 사항</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a>패키징, 게시 및 배포 요구 사항

App-v를 사용 하 여 Office를 배포 하기 전에 다음 요구 사항을 검토 하세요.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">작업</th>
<th align="left">요구 사항</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>패키징</p></td>
<td align="left">
<ul>
<li><p>사용자에 게 배포 하려는 모든 Office 응용 프로그램은 단일 패키지에 있어야 합니다.</p></li>
<li><p>App-v 5.0 이상에서는 Office 배포 도구를 사용 하 여 패키지를 만들어야 합니다. Sequencer는 사용할 수 없습니다.</p></li>
<li><p>Office와 함께 Microsoft Visio 2016 및 Microsoft Project 2016을 배포 하는 경우 Office와 동일한 패키지에 포함 해야 합니다. 자세한 내용은 <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> Office를 사용 하 여 Visio 2016 및 Project 2016 배포를 참조 하세요 </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>게시</p></td>
<td align="left"><ul>
<li><p>각 클라이언트 컴퓨터에 하나의 Office 패키지만 게시할 수 있습니다.</p></li>
<li><p>Office 패키지를 전역적으로 게시 해야 합니다. 사용자에 게 게시할 수 없습니다.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>예를 들어 원격 데스크톱 서비스를 사용 하 여 다음 제품을 공유 컴퓨터에 배포 합니다.</p>
<ul>
<li><p>엔터프라이즈 용 Microsoft 365 앱</p></li>
<li><p>Visio Pro for Office 365</p></li>
<li><p>Project Pro for Office 365</p></li>
</ul></td>
<td align="left"><p>공유 컴퓨터 정품 인증을 사용 하도록 설정 해야 합니다 <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> </a> .</p>
</td>
</tr>
</tbody>
</table>



### 패키지에서 Office 응용 프로그램 제외

다음 표에서는 패키지에서 특정 Office 응용 프로그램을 제외 하기 위해 권장 되는 방법에 대해 설명 합니다.

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
<td align="left"><p><strong> </strong> Office 배포 도구를 사용 하 여 패키지를 만들 때 excludeapp 설정을 사용 합니다.</p></td>
<td align="left"><ul>
<li><p>Office 배포 도구가 패키지를 만들 때 패키지에서 특정 Office 응용 프로그램을 제외할 수 있습니다. 예를 들어이 설정을 사용 하 여 Microsoft 단어만 포함 된 패키지를 만들 수 있습니다.</p></li>
<li><p>자세한 내용은 <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> excludeapp 요소를 참조 하세요 </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>DeploymentConfig.xml 파일 수정</p></td>
<td align="left"><ul>
<li><p>패키지를 만든 후 DeploymentConfig.xml 파일을 수정 합니다. 이 파일에는 App-v 클라이언트를 실행 하는 컴퓨터의 모든 사용자에 대 한 기본 패키지 설정이 포함 되어 있습니다.</p></li>
<li><p>자세한 내용은 <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> Office 2016 응용 프로그램 사용 안 함을 참조 하세요 </a> .</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a>Office 배포 도구를 사용 하 여 App-v 용 Office 2016 패키지 만들기


App-v 5.0 이상 버전의 Office 2016 패키지를 만들려면 다음 단계를 완료 하세요.

>**Important** &nbsp; 중요 &nbsp; App-v 5.0 이상에서는 Office 배포 도구를 사용 하 여 패키지를 만들어야 합니다. Sequencer를 사용 하 여 패키지를 만들 수는 없습니다.

### Office 배포 도구를 사용 하기 위한 필수 구성 요소 검토

Office 배포 도구를 설치 하는 컴퓨터에는 다음이 있어야 합니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">요소일</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>필수 구성 요소 소프트웨어</p></td>
<td align="left"><p>.Net Framework 4</p></td>
</tr>
<tr class="even">
<td align="left"><p>지원되는 운영 체제</p></td>
<td align="left"><ul>
<li><p>64 비트 버전의 Windows 10</p></li>
<li><p>64 비트 버전의 Windows 8 또는 8.1</p></li>
<li><p>64 비트 버전의 Windows 7</p></li>
</ul></td>
</tr>
</tbody>
</table>


>**참고**  이 항목에서 "Office 2016 App-V 패키지" 라는 용어는 구독 라이선스를 의미 합니다.


### Office 배포 도구를 사용 하 여 Office 2016 앱-V 패키지 만들기

Office 배포 도구를 사용 하 여 Office 2016 앱-V 패키지를 만듭니다. 다음 지침에서는 구독 라이선스를 사용 하 여 Office 2016 App-v 패키지를 만드는 방법에 대해 설명 합니다.

64 비트 Windows 컴퓨터에서 Office 2016 앱-V 패키지를 만듭니다. Office 2016 앱-V 패키지는 일단 만들어지면 32 비트 및 64 비트 Windows 7, Windows 8.1 및 Windows 10 컴퓨터에서 실행 됩니다.

### Office 배포 도구 다운로드

Office 2016 앱-V 패키지는 office 2016 App-v 패키지를 생성 하는 Office 배포 도구를 사용 하 여 만듭니다. 앱-V 시퀀서를 통해 패키지를 만들거나 수정할 수 없습니다. 패키지 만들기를 시작 하려면 다음을 실행 합니다.

1.  [간편 실행을 위한 Office 2016 배포 도구](https://www.microsoft.com/download/details.aspx?id=49117)를 다운로드 합니다.

> **중요** Office 2016 App-v 패키지를 만들려면 Office 2016 배포 도구를 사용 해야 합니다.
> 2. .Exe 파일을 실행 하 고 원하는 위치에 해당 기능을 추출 합니다. 이 프로세스를 더 쉽게 하려면 기능을 저장할 공유 네트워크 폴더를 만들 수 있습니다.

    Example: \\\\Server\\Office2016

3. setup.exe 및 configuration.xml 파일이 존재 하며 지정한 위치에 있는지 확인 합니다.

### Office 2016 응용 프로그램 다운로드

Office 배포 도구를 다운로드 한 후에이를 사용 하 여 최신 Office 2016 응용 프로그램을 얻을 수 있습니다. Office 응용 프로그램을 가져온 후 Office 2016 App-v 패키지를 만듭니다.

Office 배포 도구에 포함 된 XML 파일은 포함 된 언어 및 Office 응용 프로그램과 같은 제품 세부 정보를 지정 합니다.

1. **예제 XML 구성 파일을 사용자 지정 합니다.** Office 배포 도구를 사용 하 여 다운로드 한 샘플 XML 구성 파일을 사용 하 여 Office 응용 프로그램을 사용자 지정 합니다.

   1. 메모장 또는 즐겨 찾는 텍스트 편집기에서 샘플 XML 파일을 엽니다.

   2. 샘플 configuration.xml 파일을 열어 편집할 수 있는 상태에서 Office 2016 응용 프로그램을 저장 하는 제품, 언어, 경로를 지정 합니다. 다음은 configuration.xml 파일의 기본 예입니다.

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      >**참고**  구성 XML은 샘플 XML 파일입니다. 파일에는 주석 처리 된 줄이 포함 됩니다. 이러한 줄을 "주석 처리" 하 여 파일에 대 한 추가 설정을 사용자 지정할 수 있습니다. 이러한 줄을 "주석으로 처리" 하려면 "<!을 (를) 제거 합니다. --"줄의 시작 부분에 있고 줄 끝에서"--> "입니다.

      위의 XML 구성 파일은 Visio ProPlus를 포함 하 여 Office 2016 ProPlus 32 비트 에디션을 영어로 다운로드 하 여 Office 응용 프로그램이 저장 되는 위치인 \\\\server\\Office 2016에이를 설치 하도록 지정 합니다. 응용 프로그램의 제품 ID는 Office의 최종 라이선스에 영향을 주지 않습니다. 이후 단계에서 라이선스를 지정 하 여 다양 한 라이선스를 포함 하는 Office 2016 앱-V 패키지를 같은 응용 프로그램에서 만들 수 있습니다. 아래 표에는 XML 파일의 사용자 지정 가능한 특성 및 요소가 요약 되어 있습니다.

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left">입력</th>
      <th align="left">설명</th>
      <th align="left">예</th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p>요소 추가</p></td>
      <td align="left"><p>패키지에 포함할 제품 및 언어를 지정 합니다.</p></td>
      <td align="left"><p>해당 없음</p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>OfficeClientEdition (Add 요소의 특성)</p></td>
      <td align="left"><p>사용할 Office 2016 제품 버전 (32 비트 또는 64-비트)을 지정 합니다. <strong>OfficeClientEdition </strong> 가 유효한 값으로 설정 되지 않은 경우 작업이 실패 합니다.</p></td>
      <td align="left"><p><strong>OfficeClientEdition </strong> = &quot; 32&quot;</p>
      <p><strong>OfficeClientEdition </strong> = &quot; 64&quot;</p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Product 요소</p></td>
      <td align="left"><p>응용 프로그램을 지정 합니다. 여기에 프로젝트 2016 및 Visio 2016을 여기에 지정 하 여 응용 프로그램에 포함 시킬 추가 된 제품이 필요 합니다.

      제품 Id에 대 한 자세한 내용은 <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> Office 배포 도구에서 간편 실행 용으로 지원 되는 제품 id를 참조 하세요.</a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p>Language 요소</p></td>
      <td align="left"><p>응용 프로그램에서 지원 되는 언어를 지정 합니다.</p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>버전 (요소 추가의 특성)</p></td>
      <td align="left"><p>선택 사항. 패키지에 사용할 빌드를 지정 합니다.</p>
      <p>Office 원본의 v32.CAB에 정의 된 최신 광고 빌드를 기본값으로 설정 합니다.</p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>SourcePath (Add 요소의 특성)</p></td>
      <td align="left"><p>응용 프로그램이 저장 되는 위치를 지정 합니다.</p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>채널 (추가 요소의 특성)</p></td>
      <td align="left"><p>선택 사항. 다운로드 하거나 설치할 제품에 대 한 업데이트 채널을 지정 합니다. </p><p>업데이트 채널에 대 한 자세한 내용은 엔터프라이즈 용 Microsoft 365 앱의 업데이트 채널 개요를 참조 하세요.</p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      원하는 제품, 언어, 그리고 Office 2016 응용 프로그램이 저장 되는 위치를 지정 하도록 configuration.xml 파일을 편집한 후에는 구성 파일 (예: Customconfig.xml)을 저장할 수 있습니다.

2. **지정 된 위치에 응용 프로그램을 다운로드 합니다.** 관리자 권한 명령 프롬프트 및 64 비트 운영 체제를 사용 하 여 나중에 App-v 패키지로 변환 될 Office 2016 응용 프로그램을 다운로드 합니다. 다음은 세부 정보에 대 한 설명이 포함 된 예제 명령입니다.

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   예제:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>은 Office 배포 도구와 사용자 지정 Configuration.xml 파일 Customconfig.xml 포함 하는 네트워크 공유 위치입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>Office 배포 도구입니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/download</strong></p></td>
   <td align="left"><p>customConfig.xml 파일에서 지정 하는 Office 2016 응용 프로그램을 다운로드 합니다. 나중에 볼륨 라이선스를 사용 하 여 Office 2016 앱-V 패키지에서 이러한 비트를 변환할 수 있습니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>다운로드 프로세스를 완료 하는 데 필요한 XML 구성 파일을 전달 합니다 (이 예제에서는 customconfig.xml. 다운로드 명령을 사용한 후에는 구성 xml 파일에 지정 된 위치에서 Office 응용 프로그램을 찾을 수 있습니다 (이 예제에서는 \Server\Office2016.).</p></td>
   </tr>
   </tbody>
   </table>



### Office 응용 프로그램을 앱-V 패키지로 변환

Office 배포 도구를 통해 Office 2016 응용 프로그램을 다운로드 한 후 office 배포 도구를 사용 하 여 office 2016 App-v 패키지로 전환 합니다. 라이선스 모델에 해당 하는 단계를 완료 합니다.

**수행 해야 하는 작업에 대 한 요약:**

-   64 비트 Windows 컴퓨터에서 Office 2016 앱-V 패키지를 만듭니다. 그러나 패키지는 32 비트 및 64 비트 Windows 7, Windows 8 또는 8.1 및 Windows 10 컴퓨터에서 실행 됩니다.

-   Office 배포 도구를 사용 하 여 구독 라이선스 패키지에 대 한 Office 앱-V 패키지를 만든 다음 CustomConfig.xml 구성 파일을 수정 합니다.

    다음 표에는 사용 중인 라이선스 모델의 CustomConfig.xml 파일에 입력 해야 하는 값이 요약 되어 있습니다. 표 다음에 나오는 섹션의 단계에서는 필요한 정확한 항목을 지정 합니다.

>**Note** &nbsp; 참고 &nbsp; Office 배포 도구를 사용 하 여 엔터프라이즈 용 Microsoft 365 앱에 대 한 앱 V 패키지를 만들 수 있습니다. 볼륨 라이선스 버전의 Office Professional Plus 또는 Office Standard에 대 한 패키지 만들기는 지원 되지 않습니다.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">제품 ID</th>
<th align="left">구독 라이선스</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Office 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Office 2016 (Visio 2016)</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Office 2016 (Visio 2016 및 Project 2016)</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p>
<p>ProjectProRetail</p></td>
</tr>
</tbody>
</table>



**Office 응용 프로그램을 앱-V 패키지로 변환 하는 방법**

1. 메모장에서 CustomConfig.xml 파일을 다시 열고 파일을 다음과 같이 변경 합니다.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">매개 변수</th>
   <th align="left">값을 변경할 대상</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>SourcePath</p></td>
   <td align="left"><p>이전에 다운로드 한 Office 응용 프로그램을 가리킵니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ProductID</p></td>
   <td align="left"><p>다음 예제에 표시 된 대로 구독 라이선스를 지정 합니다.</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p>이 예제에서는 구독 라이선스를 사용 하 여 패키지를 만들기 위해 다음과 같이 변경 되었습니다.</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>SourcePath</strong></p></td>
   <td align="left"><p>는 이전에 다운로드 된 Office 응용 프로그램을 가리키도록 변경 된 경로입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>제품 ID</strong></p></td>
   <td align="left"><p>(으)로 변경 되었습니다 <code>O365ProPlusRetail</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>제품 ID</strong></p></td>
   <td align="left"><p>Visio는으로 변경 되었습니다 <code>VisioProRetail</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p>ExcludeApp (선택 사항)</p></td>
   <td align="left"><p>Office 배포 도구가 만드는 App-v 패키지에 포함 하지 않을 Office 프로그램을 지정할 수 있습니다. 예를 들어 Access 및 InfoPath는 제외할 수 있습니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>PACKAGEGUID (선택 사항)</p></td>
   <td align="left"><p>기본적으로 Office 배포 도구에서 만든 모든 App-v 패키지는 동일한 App-v 패키지 ID를 공유 합니다. PACKAGEGUID를 사용 하 여 각 패키지에 대해 다른 패키지 ID를 지정할 수 있으며,이를 통해 Office 배포 도구에서 만든 여러 App-v 패키지를 게시 하 고 App-v 서버를 사용 하 여 관리 합니다.</p>
   <p>이 매개 변수를 사용 하는 경우 사용자 마다 다른 패키지를 만드는 경우를 예로 들 수 있습니다. 예를 들어 일부 사용자를 위해 Office 2016만 사용 하 여 패키지를 만들고 다른 사용자 집합에 대해 Office 2016 및 Visio 2016을 사용 하 여 다른 패키지를 만들 수 있습니다.</p>
&gt;<strong>참고 </strong> 고유한 패키지 id를 사용 하는 경우에도 단일 장치에 하나의 앱 V 패키지만 배포할 수 있습니다.
   </td>
   </tr>
   </tbody>
   </table>



2. /Packager 명령을 사용 하 여 Office 응용 프로그램을 Office 2016 App-v 패키지로 변환할 수 있습니다.

   예:

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   예제:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>은 Office 배포 도구와 사용자 지정 Configuration.xml 파일 Customconfig.xml 포함 하는 네트워크 공유 위치입니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>Office 배포 도구입니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/packager</strong></p></td>
   <td align="left"><p>customConfig.xml 파일에 지정 된 라이선스 유형을 사용 하 여 Office 2016 앱-V 패키지를 만듭니다.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>패키징 단계에 대해 준비한 구성 XML 파일 (이 경우 customConfig)을 전달 합니다.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>\server\share\Office 2016AppV</strong></p></td>
   <td align="left"><p>새로 만든 Office App-v 패키지의 위치를 지정 합니다.</p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. Office 2016 App-v 패키지가 올바르게 작동 하는지 확인 합니다.

   1.  전역으로 만든 Office 2016 App-v 패키지를 테스트 컴퓨터에 게시 하 고 Office 2016 바로 가기가 표시 되는지 확인 합니다.

   2.  Excel 또는 Word 등의 몇 가지 Office 2016 응용 프로그램을 시작 하 여 패키지가 예상 대로 작동 하는지 확인 합니다.

## <a href="" id="bkmk-pub-pkg-office"></a>App-v 용 Office 패키지 게시-V


다음 정보를 사용 하 여 Office 패키지를 게시 합니다.

### Office 앱-V 패키지 게시 방법

다른 패키지에 사용 하는 것과 동일한 방법을 사용 하 여 Office 2016의 App-v 패키지를 배포 합니다.

-   System Center Configuration Manager

-   App-v Server

-   독립 실행형-PowerShell 명령

### 필수 구성 요소 및 요구 사항 게시

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">필수 구성 요소 또는 요구 사항</th>
<th align="left">세부 정보</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 클라이언트에서 PowerShell 스크립트 사용</p></td>
<td align="left"><p>Office 2016 패키지를 게시 하려면 스크립트를 실행 해야 합니다.</p>
<p>앱-V 클라이언트에서는 패키지 스크립트를 기본적으로 사용할 수 없습니다. 스크립팅을 사용 하도록 설정 하려면 다음 PowerShell 명령을 실행 합니다.</p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p>전체적으로 Office 2016 패키지 게시</p></td>
<td align="left"><p>Office App-v 패키지의 확장 지점은 컴퓨터 수준에서 설치 해야 합니다.</p>
<p>컴퓨터 수준에서 게시 하는 경우 필수 작업 또는 재배포 가능이 필요 하지 않으며 Office 2016 패키지를 전역적으로 응용 프로그램이 기본적으로 설치 된 Office와 동일 하 게 작동 하므로 관리자가 패키지를 사용자 지정할 필요가 없습니다.</p></td>
</tr>
</tbody>
</table>



### Office 패키지를 게시 하는 방법

다음 명령을 실행 하 여 Office 패키지를 전역적으로 게시 합니다.

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   App-v 서버의 웹 관리 콘솔에서 사용자 그룹을 사용 하는 대신 컴퓨터 그룹에 대 한 사용 권한을 추가 하 여 패키지를 해당 그룹의 컴퓨터에 전역으로 게시할 수 있습니다.

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a>Office 앱-V 패키지 사용자 지정 및 관리


Office App-v 패키지를 관리 하려면 다른 패키지에 대해 수행 하는 것과 동일한 작업을 사용 하지만 다음 섹션에서 설명 하는 몇 가지 예외가 있습니다.

-   [연결 그룹을 사용 하 여 Office 플러그 인 사용](#bkmk-enable-office-plugins)

-   [Office 2016 응용 프로그램을 사용 하지 않도록 설정](#bkmk-disable-office-apps)

-   [Office 2016 바로 가기를 사용 하지 않도록 설정](#bkmk-disable-shortcuts)

-   [Office 2016 패키지 업그레이드 관리](#bkmk-manage-office-pkg-upgrd)

-   [Visio 2016 및 Project 2016을 Office와 함께 배포](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a>연결 그룹을 사용 하 여 Office 플러그 인 사용

이 섹션의 단계를 사용 하 여 office 플러그 인을 Office 패키지와 함께 사용 하도록 설정 합니다. Office 플러그 인을 사용 하려면 App-v 시퀀서를 사용 하 여 플러그 인만 포함 된 별도의 패키지를 만들어야 합니다. Office 배포 도구를 사용 하 여 플러그 인 패키지를 만들 수는 없습니다. 그런 다음 다음 단계에 설명 된 대로 Office 패키지 및 플러그 인 패키지를 포함 하는 연결 그룹을 만듭니다.

**Office 앱-V 패키지에 대 한 플러그 인을 사용 하도록 설정 하려면**

1.  App-v Server, System Center Configuration Manager 또는 PowerShell cmdlet을 통해 연결 그룹을 추가 합니다.

2.  App-v 시퀀서를 사용 하 여 플러그 인을 순서 대로 합니다. 플러그 인을 시퀀싱 하는 데 사용 되는 컴퓨터에 Office 2016이 설치 되어 있는지 확인 합니다. Office 2016 플러그 인을 순서 대로 시퀀싱 하는 컴퓨터에서 Microsoft 365 앱 (비가상)을 사용 하는 것이 좋습니다.

3.  원하는 플러그 인을 포함 하는 App-v 패키지를 만듭니다.

4.  App-v server, System Center Configuration Manager 또는 PowerShell cmdlet을 통해 연결 그룹을 추가 합니다.

5.  만든 연결 그룹에 Office 2016 앱-V 패키지와 시퀀싱 한 플러그 인 패키지를 추가 합니다.

    >**중요** 연결 그룹의 패키지 순서에 따라 패키지 콘텐츠가 병합 되는 순서가 결정 됩니다. 연결 그룹 설명자 파일에서 Office 2016 App-v 패키지를 먼저 추가한 다음 플러그인 App-v 패키지를 추가 합니다.



6.  두 패키지가 모두 대상 컴퓨터에 게시 되 고 게시 된 Office 2016 App-v 패키지의 전역 설정에 맞게 플러그 인 패키지가 전역으로 게시 되었는지 확인 합니다.

7.  플러그 인 패키지의 배포 구성 파일에 Office 2016 App-v 패키지와 동일한 설정이 있는지 확인 합니다.

    Office 2016 App-v 패키지가 운영 체제와 통합 되어 있기 때문에 플러그 인 패키지 설정이 일치 해야 합니다. 배포 구성 파일에서 "COM 모드"를 검색 하 고 플러그 인 패키지에 "통합 됨"으로 설정 되어 있는지 확인 하 고 "InProcessEnabled" 및 "OutOfProcessEnabled"이 모두 게시 한 Office 2016 App-v 패키지의 설정과 일치 하도록 할 수 있습니다.

8.  배포 구성 파일을 열고 **사용할 수 있는 개체** 값을 **false**로 설정 합니다.

9.  시퀀싱 한 후에 배포 구성 파일을 변경한 경우 플러그 인 패키지가 파일과 함께 게시 되었는지 확인 합니다.

10. 만든 연결 그룹이 원하는 컴퓨터에 설정 되어 있는지 확인 합니다. 연결 그룹을 사용 하는 경우 Office 2016 App-v 패키지를 사용 하는 경우 생성 되는 연결 그룹은 "보류" 될 수 있습니다. 이 문제가 발생 하면 다시 부팅 하 여 연결 그룹을 사용 하도록 설정 해야 합니다.

11. 두 패키지를 성공적으로 게시 하 고 연결 그룹을 사용 하도록 설정한 후에는 대상 Office 2016 응용 프로그램을 시작 하 고, 게시 하 고 추가한 플러그 인이 필요한 대로 작동 하는지 확인 합니다.

### <a href="" id="bkmk-disable-office-apps"></a>Office 2016 응용 프로그램을 사용 하지 않도록 설정

Office 앱-V 패키지에서 특정 응용 프로그램을 사용 하지 않도록 설정할 수 있습니다. 예를 들어 Access를 사용 하지 않도록 설정할 수 있지만 다른 모든 Office 응용 프로그램의 기본은 사용할 수 있는 상태로 유지 됩니다. 응용 프로그램을 사용 하지 않도록 설정 하면 최종 사용자가 더 이상 해당 응용 프로그램의 바로 가기를 볼 수 없습니다. 응용 프로그램을 다시 시퀀싱 하지 않아도 됩니다. Office 2016 앱-V 패키지를 게시 한 후 배포 구성 파일을 변경 하는 경우 변경 내용을 저장 하 고 Office 2016 App-v 패키지를 추가한 다음 새 배포 구성 파일을 사용 하 여 새 설정을 적용 하는 Office 2016 App-v 패키지 응용 프로그램에 다시 게시 합니다.

>**참고** Office 배포 도구를 사용 하 여 앱-V 패키지를 만들 때 특정 Office 응용 프로그램 (예: Access 및 InfoPath)을 제외 하려면 **Excludeapp** 설정을 사용 합니다.


**Office 2016 응용 프로그램을 사용 하지 않도록 설정 하려면**

1.  **메모장과** 같은 텍스트 편집기를 사용 하 여 배포 구성 파일을 열고 "응용 프로그램"을 검색 합니다.

2.  사용 하지 않으려는 Office 응용 프로그램 (예: Access 2016)을 검색 합니다.

3.  "사용" 값을 "true"에서 "false"로 변경 합니다.

4.  배포 구성 파일을 저장 합니다.

5.  새 배포 구성 파일을 사용 하 여 Office 2016 App-v 패키지를 추가 합니다.

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  Office 2016 App-v 패키지를 다시 추가한 다음 새 배포 구성 파일을 사용 하 여 Office 2016 앱-V 패키지 응용 프로그램에 새 설정을 적용 합니다.

### <a href="" id="bkmk-disable-shortcuts"></a>Office 2016 바로 가기를 사용 하지 않도록 설정

패키지를 게시 취소 하거나 제거 하는 대신 특정 Office 응용 프로그램의 바로 가기를 사용 하지 않도록 설정할 수 있습니다. 다음 예제에서는 Microsoft Access의 바로 가기를 사용 하지 않도록 설정 하는 방법을 보여 줍니다.

**Office 2016 응용 프로그램의 바로 가기를 사용 하지 않도록 설정 하려면**

1.  메모장에서 배포 구성 파일을 열고 "바로 가기"를 검색 합니다.

2.  특정 바로 가기를 사용 하지 않도록 설정 하려면 원하지 않는 특정 바로 가기를 삭제 하거나 주석으로 처리 합니다. 하위 시스템을 표시 하 고 사용 하도록 유지 해야 합니다. 예를 들어 아래 예제에서는 Microsoft Access 바로 가기를 삭제 하 고, 하위 시스템 바로 가기 &lt; &gt; &lt; /바로 가기는 &gt; 그대로 유지 하 여 microsoft access 바로 가기를 사용 하지 않도록 설정 합니다.

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  배포 구성 파일을 저장 합니다.

4.  새 배포 구성 파일을 사용 하 여 Office 2016 App-v 패키지를 다시 게시 합니다.

앱-V 패키지에 대 한 배포 구성 (예: 파일 형식 연결, 가상 파일 시스템 등)을 수정 하 여 다양 한 추가 설정을 변경할 수 있습니다. 배포 구성 파일을 사용 하 여 App-v 패키지 설정을 변경 하는 방법에 대 한 자세한 내용은이 문서의 뒷부분에 나오는 추가 리소스 섹션을 참조 하세요.

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a>Office 2016 패키지 업그레이드 관리

Office 2016 패키지를 업그레이드 하려면 Office 배포 도구를 사용 합니다. 이전에 배포 된 Office 2016 패키지를 업그레이드 하려면 다음 단계를 수행 합니다.

**이전에 배포 된 Office 2016 패키지를 업그레이드 하는 방법**

1. 최신 Office 2016 응용 프로그램 소프트웨어를 사용 하는 Office 배포 도구를 통해 새 Office 2016 패키지를 만듭니다. 가장 최근의 Office 2016 비트는 Office 2016 App-v 패키지를 만드는 다운로드 단계를 통해 언제 든 지 얻을 수 있습니다. 새로 생성 된 Office 2016 패키지에는 최신 업데이트와 새 버전 ID가 포함 됩니다. Office 배포 도구를 사용 하 여 만든 모든 패키지에는 동일한 계보가 있습니다.

   > **참고** Office 앱-V 패키지에는 두 가지 버전 Id가 있습니다.
   > <ul>
   > <li>Office 배포 도구를 사용 하 여 만든 모든 패키지에서 고유한 Office 2016 App-v 패키지 버전 ID입니다.</li>
   > <li>새 버전의 Office가 있는 경우에만 변경 되는 두 번째 App-v 패키지 버전 ID, x.x. x 예: AppX 매니페스트 예를 들어 업그레이드 된 새 Office 2016 릴리스를 사용할 수 있고 이러한 업그레이드를 통합 하기 위해 Office 배포 도구를 통해 패키지를 만들면 X.x.x.x 버전 ID가 변경 되어 Office 버전 자체가 변경 되었음을 반영 합니다. App-v 서버는이 패키지를 구분 하는 데 x.x 버전 ID를 사용 하 고 이전에 게시 된 패키지에 대 한 새 업그레이드가 포함 되어 있음을 인식 하 고, 결과적으로 기존 Office 2016 패키지에 대 한 업그레이드로 게시 합니다.</li>
   > </ul>


2. 새로 만든 Office 2016 App-v 패키지를 새 업데이트를 적용 하려는 컴퓨터에 전역적으로 게시 합니다. 새 패키지에는 이전 Office 2016 App-v 패키지의 계보가 있으므로 업데이트를 사용 하 여 새 패키지를 게시 하면 이전 패키지에 새 변경 내용만 적용 되므로 속도가 빠릅니다.

3. 업그레이드는 전역적으로 게시 된 모든 앱-V 패키지와 동일한 방식으로 적용 됩니다. 응용 프로그램을 사용 중일 수 있으므로 컴퓨터를 다시 부팅할 때까지 업그레이드가 지연 될 수 있습니다.


### <a href="" id="bkmk-deploy-visio-project"></a>Visio 2016 및 Project 2016을 Office와 함께 배포

다음 표에서는 Visio 2016 및 Project 2016을 Office와 함께 배포 하기 위한 요구 사항 및 옵션에 대해 설명 합니다.

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
<td align="left"><p>Visio 2016 및 Project 2016을 Office와 함께 패키지 하 고 게시 하려면 어떻게 하나요?</p></td>
<td align="left"><p>Visio 2016 및 Project 2016을 Office와 동일한 패키지에 포함 해야 합니다.</p>
<p>Office를 배포 하지 않는 경우이 항목에서 설명 하는 패키징, 게시 및 배포 요구 사항에 따라 Visio 및/또는 프로젝트를 포함 하는 패키지를 만들 수 있습니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Visio 2016 및 Project 2016을 특정 사용자에 게 어떻게 배포할 수 있나요?</p></td>
<td align="left"><p>다음 방법 중 하나를 사용합니다.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">원하는 경우</th>
<th align="left">... 그런 다음이 방법을 사용 합니다.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>두 개의 다른 패키지를 만들어 각각 다른 사용자 그룹에 배포</p></td>
<td align="left"><p>다음 패키지를 만들고 배포 합니다.</p>
<ul>
<li><p>사용자가 Office만 필요로 하는 컴퓨터에는 Office 배포만 포함 된 패키지입니다.</p></li>
<li><p>사용자가 세 가지 응용 프로그램을 모두 필요로 하는 컴퓨터에 Office, Visio, 프로젝트 배포가 포함 된 패키지입니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>전체 조직에 대해 하나의 패키지만 사용 하려는 경우 또는 컴퓨터를 공유 하는 사용자가 있는 경우:</p></td>
<td align="left"><p>다음 단계를 따릅니다.</p>
<ol>
<li><p>Office, Visio, 프로젝트를 포함 하는 패키지를 만듭니다.</p></li>
<li><p>패키지를 모든 사용자에 게 배포 합니다.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker </a> 를 사용 하 여 특정 사용자가 Visio 및 Project를 사용 하지 못하도록 할 수 있습니다.</p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## 추가 리소스


[App-V를 사용하여 Microsoft Office 2013 배포](deploying-microsoft-office-2013-by-using-app-v.md)

[App-V를 사용하여 Microsoft Office 2010 배포](deploying-microsoft-office-2010-by-using-app-v.md)

[간편 실행을 위한 Office 2016 배포 도구](https://www.microsoft.com/download/details.aspx?id=49117)

**연결 그룹**

[Microsoft App-V v5에 연결 그룹 배포](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[연결 그룹 관리](managing-connection-groups.md)

**동적 구성**

[App-V 5.1 동적 구성 정보](about-app-v-51-dynamic-configuration.md)





