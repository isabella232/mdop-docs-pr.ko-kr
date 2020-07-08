---
title: App-V의 이전 버전에서 마이그레이션 계획
description: App-V의 이전 버전에서 마이그레이션 계획
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813468"
---
# App-V의 이전 버전에서 마이그레이션 계획


다음 정보를 사용 하 여 이전 버전의 App-v에서 Microsoft Application Virtualization (App-v) 5.1으로 마이그레이션하는 방법을 계획 합니다.

## 마이그레이션 요구 사항


업그레이드를 시작 하기 전에 다음 요구 사항을 검토 하세요.

-   App-v 4.6 SP2 이전 버전에서 업그레이드 하는 경우 App-v 5.1 이상으로 업그레이드 하기 전에 먼저 버전 App-V 4.6 SP3으로 업그레이드 하세요. 이 시나리오에서는 먼저 App-v 클라이언트를 업그레이드 한 다음 서버 구성 요소를 업그레이드 합니다.
**참고:** App-v 4.6에서 메인스트림 지원이 종료 되었습니다.

-   App-v 5.1 또는 App-v 5.1 또는 **appv** 형식으로 변환 된 패키지를 사용 5.0 하 여 만든 패키지만 지원 합니다.

-   App-v 5.0 SP1에서 App-v 서버를 업그레이드 하는 경우에는 [앱-v 5.1에 대 한](about-app-v-51.md#bkmk-migrate-to-51) 지침을 참조 하세요.

## App-v 4.6을 사용 하 여 동시에 App-v 5.1 클라이언트 실행


App-v 4.6 SP3 클라이언트를 사용 하 여 동일한 컴퓨터에서 앱-V 5.1 클라이언트를 동시에 실행할 수 있습니다.

다중 사용자 App-v 클라이언트를 실행 하는 경우 다음을 수행할 수 있습니다.

-   두 클라이언트가 모두 실행 되 고 있는 경우 App-v 4.6 SP3 패키지를 App-v 5.1 형식으로 변환 하 고 두 패키지를 모두 게시 합니다.

-   변환 된 App-v 5.1 패키지에서 App-v 4.6 패키지의 파일 형식 연결 및 바로 가기를 사용할 수 있도록 변환 된 패키지에 대 한 마이그레이션 정책을 정의 합니다.

### 지원 되는 공존 시나리오

다음 표에서는 지원 되는 앱-V 공존 시나리오를 보여 줍니다. 공존할 수 있는 클라이언트를 실행할 때 주어진 릴리스의 최신 업데이트를 설치 하는 것이 좋습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-v 4.6 클라이언트 유형</th>
<th align="left">App-v 5.1 클라이언트 유형</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-v 4.6 SP3</p></td>
<td align="left"><p>App-V 5.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-v 4.6 SP3 RDS</p></td>
<td align="left"><p>App-v 5.1 RDS</p></td>
</tr>
</tbody>
</table>

 

### 공존할 클라이언트를 실행 하기 위한 요구 사항

공존할 수 있는 클라이언트를 실행 하려면 다음을 수행 해야 합니다.

-   App-v 5.1 클라이언트를 설치 하기 전에 App-v 4.6 클라이언트를 설치 합니다.

-   **App-v** 클라이언트 공존 노드에서 **마이그레이션 모드 설정** 그룹 정책 설정을 사용 하도록 설정 합니다 &gt; **Client Coexistence** . Admx 템플릿을 배포 하려면 [MDOP 그룹 정책 (admx) 템플릿을 다운로드 하 고 배포 하는 방법을](https://technet.microsoft.com/library/dn659707.aspx)참조 하세요.

**참고**  App-v 5.1 및 4.6을 함께 설치한 경우 app-v 4.6 패키지를 사용 하 여 앱-V 5.1 패키지를 동시에 실행할 수 있습니다. 그러나 앱-V 5.1 패키지는 동일한 가상 환경에서 App-v 4.6 패키지와 상호 작용할 수 없습니다.

 

### 클라이언트 다운로드 및 문서

다음 표에서는 App-v 4.6 클라이언트 다운로드 및 릴리스에 대 한 TechNet 설명서에 대 한 링크를 제공 합니다. 다운로드에는 App-v "일반" 및 RDS 클라이언트가 포함 됩니다. 다른 언급이 없는 한, App-v 클라이언트에 대 한 TechNet 문서는 두 클라이언트에 모두 적용 됩니다.

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">App-V 버전</th>
<th align="left">TechNet 문서 링크</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)">Microsoft Application Virtualization 4.6 SP3 정보</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)">Microsoft Application Virtualization 5.1에 대 한 정보</a></p></td>
</tr>
</tbody>
</table>

 

App-v 5.1 클라이언트 공존을 구성 하는 방법에 대 한 자세한 내용은 다음을 참조 하세요.

-   [앱-V 4.6 및 앱-V 5.1 클라이언트를 같은 컴퓨터에 배포 하는 방법](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [App-v 5.0 공존 및 마이그레이션](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>패키지 변환기를 사용 하 여 "이전 버전" 패키지 변환


앱-4.6 SP2 또는 이전 버전을 사용 하 여 만든 패키지를 마이그레이션하기 전에 앱-V 5.1에 다음 요구 사항을 검토 하세요.

-   패키지를 **appv** 파일 형식으로 변환 해야 합니다.

-   Package Converter는 App-v 4.5 이상을 사용 하 여 만든 패키지의 직접 변환만 지원 합니다. 이전 버전을 사용 하 여 만든 패키지에서 패키지 변환기를 사용 하려면 App-v 4.5 이상 버전의 sequencer를 사용 하 여 패키지를 업그레이드 한 다음 패키지 변환을 수행 해야 합니다.

패키지 변환기를 사용 하 여 패키지를 변환 하는 방법에 대 한 자세한 내용은 [이전 버전의 app-v에서 만든 패키지를 변환 하는 방법을](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)참조 하세요. 파일을 변환한 후에는 App-v 5.1 클라이언트를 실행 하는 대상 컴퓨터에 배포할 수 있습니다.






## 관련 항목


[App-V 배포 계획](planning-to-deploy-app-v51.md)

 

 





