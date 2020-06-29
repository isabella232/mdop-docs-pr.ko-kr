---
title: Application Virtualization Client 하드웨어 및 소프트웨어 요구 사항
description: Application Virtualization Client 하드웨어 및 소프트웨어 요구 사항
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819733"
---
# Application Virtualization Client 하드웨어 및 소프트웨어 요구 사항


이 항목에서는 Application Virtualization 데스크톱 클라이언트 설치에 권장 되는 최소 하드웨어 및 소프트웨어 구성 및 원격 데스크톱 서비스용 Application Virtualization 클라이언트 (이전의 터미널 서비스)에 대해 설명 합니다.

## Application Virtualization 데스크톱 클라이언트


다음 목록에는 Application Virtualization 데스크톱 클라이언트에 대해 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항이 포함 되어 있습니다. 요구 사항은 Microsoft Application Virtualization (App-v) 4.6 SP2에 대해 먼저 나열 되며, 그 뒤에 App-V 4.6 SP2 이전의 버전에 대 한 요구 사항이 적용 됩니다.

**참고**  App-v (Application Virtualization) 데스크톱 클라이언트에는 호스트 운영 체제의 요구 사항 외에 추가 프로세서 또는 RAM 리소스가 필요 하지 않습니다.

 

### 하드웨어 요구 사항

하드웨어 요구 사항은 모든 버전에 적용 됩니다.

-   프로세서-사용 중인 운영 체제에 대해 권장 되는 시스템 요구 사항을 참조 하세요.

-   RAM-사용 중인 운영 체제에 대해 권장 되는 시스템 요구 사항을 참조 하세요.

-   Disk (디스크)-30MB 설치 및 6GB에서 캐시를 위한.

### 앱-V 4.6 SP2의 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">아키텍처 SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>이상을</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>비즈니스, 엔터프라이즈 또는 Ultimate Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise 또는 Ultimate Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP1 없음</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Pro 또는 Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
</tbody>
</table>

Setup.exe 메서드를 사용 하는 경우 다음 소프트웨어 필수 구성 요소가 자동으로 설치 됩니다. Setup.msi 설치 프로그램을 사용 하는 경우 다음 제품을 먼저 설치 해야 합니다.
- **Microsoft Visual c + + 2005 Sp1 재배포 가능 패키지 (x86)**-Microsoft Visual c + + 2005 Sp1 재배포 가능 패키지 (x86) 설치에 대 한 자세한 내용은 [Microsoft Visual c + + 2005 Sp1 재배포 가능 패키지](https://go.microsoft.com/fwlink/?LinkId=119961) (x86) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=119961) . App-v 클라이언트의 버전 4.5 SP2의 경우 [Microsoft Visual c + + 2005 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트](https://go.microsoft.com/fwlink/?LinkId=169360) ()의 Vcredist\_x86.exe를 다운로드 https://go.microsoft.com/fwlink/?LinkId=169360) 합니다.
  -   **Msxml (Microsoft CORE Xml services) 6.0 sp1 (x86)**-MICROSOFT Core xml SERVICES (msxml) 6.0 sp1 (x86)을 설치 하는 방법에 대 한 자세한 내용은 [Microsoft core XML services (MSXML) 6.0 sp1 (x86](https://go.microsoft.com/fwlink/?LinkId=63266) ) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=63266) .

App-v (Application Virtualization) 4.6 데스크톱 클라이언트의 경우 Setup.exe 메서드를 사용 하는 경우 다음 추가 소프트웨어 선행 조건이 자동으로 설치 됩니다. Setup.msi 설치 프로그램을 사용 하는 경우에는 다른 필수 구성 요소도 설치 되어 있어야 합니다.

-   **Microsoft visualc + + 2008 SP1 재배포 가능 패키지 (x86)**-Microsoft visualc + + 2008 Sp1 재배포 가능 패키지 (x86) 설치에 대 한 자세한 내용은 [microsoft visualc + + 2008 Sp1 재배포 가능 패키지 (x86](https://go.microsoft.com/fwlink/?LinkId=150700) ) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=150700) .

### App-v 4.6 SP2 앞의 버전에 대 한 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">아키텍처 SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 또는 SP3</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>비즈니스, 엔터프라이즈 또는 Ultimate Edition</p></td>
<td align="left"><p>서비스 팩, SP1 또는 SP2 없음</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise 또는 Ultimate Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP1 없음</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
</tbody>
</table>
¹ 4.5 SP1 및 SP2, app-v 4.6 및 4.6 SP1만 지원 됩니다.

App-v (Application Virtualization) 4.6 데스크톱 클라이언트는 이러한 운영 체제의 x86 및 x64 Sku를 지원 합니다.

Setup.exe 메서드를 사용 하는 경우 다음 소프트웨어 필수 구성 요소가 자동으로 설치 됩니다. Setup.msi 설치 프로그램을 사용 하는 경우 다음 제품을 먼저 설치 해야 합니다.

-   <strong>Microsoft Visual c + + 2005 SP1 재배포 가능 패키지 (x86) </strong> -Microsoft Visual c + + 2005 Sp1 재배포 가능 패키지 (x86) 설치에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> Microsoft Visual c + + 2005 Sp1 재배포 가능 패키지 (x86) </a> ()를 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> . App-v 클라이언트의 버전 4.5 SP2의 경우 <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> Microsoft Visual c + + 2005 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트 ()에서 Vcredist_x86.exe를 다운로드 </a> <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> 하세요.

-   <strong>MSXML (microsoft Core XML Services) 6.0 SP1 (x86) </strong> -Microsoft CORE Xml services (msxml) 6.0 sp1 (x86)을 설치 하는 방법에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> MICROSOFT Core xml SERVICES (msxml) 6.0 sp1 (x86) ()을 참조 하세요 </a> <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> .

-   <strong>Microsoft 응용 프로그램 오류 보고 </strong> -이 소프트웨어의 설치 프로그램이 <strong> 자동으로 </strong> 압축이 풀리는 보관 파일의 support\watson 폴더에 포함 되어 있습니다.

App-v (Application Virtualization) 4.6 데스크톱 클라이언트의 경우 Setup.exe 메서드를 사용 하는 경우 다음 추가 소프트웨어 선행 조건이 자동으로 설치 됩니다. Setup.msi 설치 프로그램을 사용 하는 경우에는 다른 필수 구성 요소도 설치 되어 있어야 합니다.

-   <strong>Microsoft Visual c + + 2008 SP1 재배포 가능 패키지 (x86) </strong> -Microsoft Visual c + + 2008 Sp1 재배포 가능 패키지 (x86) 설치에 대 한 자세한 내용은 <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> Microsoft Visual c + + 2008 Sp1 재배포 가능 패키지 (x86) </a> ()를 참조 하세요 <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> .

## 원격 데스크톱 서비스용 Application Virtualization 클라이언트

다음은 원격 데스크톱 서비스에 대 한 응용 프로그램 가상화 클라이언트에 권장 되는 하드웨어 및 소프트웨어 요구 사항입니다. Appv461_3에 대 한 요구 사항이 먼저 나열 되 고 그 뒤에 App-V 4.6 SP2 이전의 버전에 대 한 요구 사항이 표시 됩니다.

원격 데스크톱 서비스용 App-v (Application Virtualization) 클라이언트에는 호스트 운영 체제의 요구 사항 외에 추가 프로세서 또는 RAM 리소스가 필요 하지 않습니다.

### 하드웨어 요구 사항

하드웨어 요구 사항은 모든 버전에 적용 됩니다.

-   프로세서-사용 중인 운영 체제에 대해 권장 되는 시스템 요구 사항을 참조 하세요.

-   RAM-사용 중인 운영 체제에 대해 권장 되는 시스템 요구 사항을 참조 하세요. 이러한 요구 사항은 사용자 및 응용 프로그램의 수에 따라 달라 집니다.

-   Disk (디스크)-30MB 설치 및 6GB에서 캐시를 위한.

### 앱-V 4.6 SP2의 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">아키텍처 SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>서비스 팩 또는 SP1 없음</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Setup.exe 메서드를 사용 하는 경우 다음 소프트웨어 필수 구성 요소가 자동으로 설치 됩니다. Setup.msi 설치 프로그램을 사용 하는 경우 다음 제품을 먼저 설치 해야 합니다.

-   **Microsoft visualc + + 2005SP1 재배포 가능 패키지 (x86)**-Microsoft visualc + + 2005 Sp1 재배포 가능 패키지 (x86) 설치에 대 한 자세한 내용은 [microsoft visualc + + 2005 Sp1 재배포 가능 패키지 (x86](https://go.microsoft.com/fwlink/?LinkId=119961) ) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=119961) . App-v 클라이언트의 버전 4.5 SP2의 경우 [Microsoft Visual c + + 2005 서비스 팩 1 재배포 가능 패키지 ATL 보안 업데이트](https://go.microsoft.com/fwlink/?LinkId=169360) ()의 Vcredist\_x86.exe를 다운로드 https://go.microsoft.com/fwlink/?LinkId=169360) 합니다.

-   **Microsoft CORE Xml services (msxml) 6.0 sp1 (x86)** MICROSOFT Core xml SERVICES (msxml) 6.0 sp1 (x86)을 설치 하는 방법에 대 한 자세한 내용은 [Microsoft core XML services (MSXML) 6.0 sp1 ()](https://go.microsoft.com/fwlink/?LinkId=63266) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Microsoft Application Error Reporting**-이 소프트웨어의 설치 프로그램은 자동 압축 풀림 보관 파일의 **support\\watson** 폴더에 포함 되어 있습니다.

App-v (Application Virtualization) 4.6 데스크톱 클라이언트의 경우 Setup.exe 메서드를 사용 하는 경우 다음 추가 소프트웨어 선행 조건이 자동으로 설치 됩니다. Setup.msi 설치 프로그램을 사용 하는 경우에는 다른 필수 구성 요소도 설치 되어 있어야 합니다.

-   **Microsoft visualc + + 2008 SP1 재배포 가능 패키지 (x86)**-Microsoft visualc + + 2008 Sp1 재배포 가능 패키지 (x86) 설치에 대 한 자세한 내용은 [microsoft visualc + + 2008 Sp1 재배포 가능 패키지 (x86](https://go.microsoft.com/fwlink/?LinkId=150700) ) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=150700) .

### App-v 4.6 SP2 앞의 버전에 대 한 소프트웨어 요구 사항

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">운영 체제</th>
<th align="left">버전</th>
<th align="left">서비스 팩</th>
<th align="left">아키텍처 SKU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</p></td>
<td align="left"><p>서비스 팩 또는 SP2 없음</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>SP1 또는 SP2</p></td>
<td align="left"><p>x86 및 x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>표준, 엔터프라이즈 또는 데이터 센터 에디션</p></td>
<td align="left"><p>서비스 팩 또는 SP1 없음</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

원격 데스크톱 서비스를 위한 App-v (Application Virtualization) 4.6 클라이언트는 이러한 운영 체제의 x86 및 x64 Sku를 지원 합니다.

## 관련 항목
- [Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Application Virtualization 시스템 요구 사항](application-virtualization-system-requirements.md)
- [명령줄을 사용하여 클라이언트를 설치하는 방법](how-to-install-the-client-by-using-the-command-line-new.md)
- [Application Virtualization Client를 수동으로 설치하는 방법](how-to-manually-install-the-application-virtualization-client.md)
- [Application Virtualization Client를 업그레이드하는 방법](how-to-upgrade-the-application-virtualization-client.md)
