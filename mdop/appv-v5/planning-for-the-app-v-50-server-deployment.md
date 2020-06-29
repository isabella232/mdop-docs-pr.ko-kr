---
title: App-V 5.0 Server 배포 계획
description: App-V 5.0 Server 배포 계획
author: dansimp
ms.assetid: fd89b324-3961-471a-ad90-c8f9ae7a8155
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06c7c17fd081b89337bbecd31f20f6796338f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813457"
---
# App-V 5.0 Server 배포 계획


Microsoft App-v (Application Virtualization) 5.0 서버 인프라는 엔터프라이즈의 요구 사항에 따라 하나 이상의 서버 컴퓨터에 설치할 수 있는 특수화 된 기능 집합으로 구성 됩니다.

## 앱-V 5.0 서버 배포 계획


App-v 5.0 서버는 다음 기능으로 구성 됩니다.

-   관리 서버-App-v 5.0 인프라에 대 한 전반적인 관리 기능을 제공 합니다.

-   관리 데이터베이스 – App-v 5.0 management에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.

-   게시 서버 – 가상 응용 프로그램에 대 한 호스팅 및 스트리밍 기능을 제공 합니다.

-   보고 서버-App-v 5.0 reporting services를 제공 합니다.

-   보고 데이터베이스-App-v 5.0 reporting에 대 한 데이터베이스 사전 배포를 용이 하 게 합니다.

다음 목록에는 App-v 5.0 서버 인프라를 설치 하는 데 권장 되는 방법이 표시 됩니다.

-   App-v 5.0 서버를 설치 합니다. 자세한 내용은 [app-v 5.0 서버를 배포 하는 방법을](how-to-deploy-the-app-v-50-server-50sp3.md)참조 하세요.

-   데이터베이스, 보고 및 관리 기능을 별도의 컴퓨터에 설치 합니다. 자세한 내용은 관리 및 보고 [서비스와 별도의 컴퓨터에 관리 데이터베이스를 설치](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)하는 방법을 참조 하세요.

-   전자 소프트웨어 배포 (ESD)를 사용 합니다. 자세한 내용은 [전자 소프트웨어 배포를 사용 하 여 app-v 5.0 패키지를 배포 하는 방법을](how-to-deploy-app-v-50-packages-using-electronic-software-distribution.md)참조 하세요.

-   모든 서버 기능을 단일 컴퓨터에 설치 합니다.

## <a href="" id="---------app-v-5-0-server-interaction"></a> App-v 5.0 서버 조작


이 섹션에는 다양 한 App-v 5.0 서버 역할이 상호 작용 하는 방법에 대 한 정보가 포함 되어 있습니다.

App-v 5.0 관리 서버에는 패키지 및 할당 된 구성의 리포지토리가 포함 되어 있습니다. 관리 서버에 등록 된 서버를 게시 하는 경우 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 게시 새로 고침 요청을 받을 때 사용할 게시 서버에 연결 된 메타 데이터가 제공 됩니다. 단일 관리 서버에서 관리 하는 app-v 5.0 게시 서버는 서로 다른 클라이언트를 서비스할 수 있으며 다른 웹 사이트 이름과 포트 바인딩을 가질 수 있습니다. 또한 동일한 관리 서버에서 관리 하는 모든 게시 서버는 서로 복제 됩니다.

**참고**  관리 서버는 부하 분산을 수행 하지 않습니다. 연결 된 메타 데이터는 클라이언트 요청을 처리할 때 사용할 수 있도록 게시 서버로 전달 됩니다.

 

## 서버 관련 프로토콜 및 외부 기능


다음은 App-v 5.0 서버에 사용 되는 서버 관련 프로토콜에 대 한 정보를 표시 합니다. 또한이 표에는 각 서버 유형에 대 한 보고 메커니즘도 포함 되어 있습니다.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">서버 유형</th>
<th align="left">프로토콜</th>
<th align="left">필요한 외부 기능</th>
<th align="left">보고</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IIS 서버</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>이 서버 프로토콜 조합에는 관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 메커니즘이 필요 합니다. HTTP 또는 HTTPS를 사용 하는 경우 IIS 서버와 방화벽을 사용 하 여 서버가 인터넷에 노출 되지 않도록 보호 합니다.</p></td>
<td align="left"><p>내부</p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p>File</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>이 서버 프로토콜 조합에는 관리 서버와 스트리밍 서버 간에 콘텐츠를 동기화 하는 지원이 필요 합니다. 파일 공유 또는 스트리밍 기능과 함께 클라이언트 컴퓨터를 사용 합니다.</p></td>
<td align="left"><p>내부</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## 관련 항목


[App-V 배포 계획](planning-to-deploy-app-v.md)

[App-V 5.0 Server 배포](deploying-the-app-v-50-server.md)

 

 





