---
title: 관리 콘솔을 사용하여 App-V 5.0 가상 응용 프로그램 관리
description: 관리 콘솔을 사용하여 App-V 5.0 가상 응용 프로그램 관리
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814868"
---
# 관리 콘솔을 사용하여 App-V 5.0 가상 응용 프로그램 관리


Microsoft App-v (Application Virtualization) 5.0 관리 서버를 사용 하 여 환경에서 패키지, 연결 그룹, 패키지 액세스를 관리할 수 있습니다. 서버는 App-v 5.0 클라이언트를 실행 하는 권한이 부여 된 컴퓨터에 응용 프로그램 아이콘, 바로 가기 및 파일 형식 연결을 게시 합니다. 일반적으로 하나 이상의 관리 서버는 구성 및 패키지 정보에 대 한 공통 데이터 저장소를 공유 합니다.

관리 서버는 AD DS (Active Directory 도메인 서비스) 그룹을 사용 하 여 사용자 권한을 관리 하 고 데이터베이스 및 데이터 저장소를 관리 하기 위해 SQL Server가 설치 되어 있습니다.

관리 서버는 응용 프로그램을 요청에 따라 최종 사용자에 게 스트리밍할 수 있으므로 이러한 서버는 신뢰할 수 있는 높은 대역폭 Lan이 있는 시스템 구성에 가장 적합 합니다. 관리 서버는 다음 구성 요소로 구성 됩니다.

-   관리 서버 – 관리 서버를 사용 하 여 패키지 및 연결 그룹을 관리 합니다.

-   게시 서버 – 앱-V 5.0 클라이언트를 실행 하는 컴퓨터에 게시 서버를 사용 하 여 패키지를 배포 합니다.

-   관리 데이터베이스-관리 데이터베이스를 사용 하 여 패키지 액세스를 관리 하 고 서버 동기화를 관리 서버에 게시 합니다.

## 관리 콘솔 작업


App-v 5.0 관리 콘솔을 사용 하 여 수행할 수 있는 가장 일반적인 작업은 다음과 같습니다.

-   [관리 콘솔에 연결하는 방법](how-to-connect-to-the-management-console-beta.md)

-   [관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [관리 콘솔을 사용하여 패키지를 게시하는 방법](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [관리 콘솔에서 패키지를 삭제하는 방법](how-to-delete-a-package-in-the-management-console-beta.md)

-   [관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [App-V 5.0 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [관리 콘솔을 사용하여 패키지의 다른 버전으로 액세스 권한 및 구성을 전송하는 방법](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [관리 콘솔에서 응용 프로그램 및 기본 가상 응용 프로그램 확장 구성](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

App-v 5.0 관리 콘솔의 주요 요소는 다음과 같습니다.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">관리 콘솔 탭</th>
<th align="left">설명</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>개요</p></td>
<td align="left"><p></p>
<ul>
<li><p><strong>App-v 시퀀서-v </strong> - 5.0 Sequencer 사용에 대 한 일반적인 정보를 검토 하려면이 옵션을 선택 합니다.</p></li>
<li><p><strong>응용 프로그램 패키지 라이브러리 </strong> – <strong> 관리 콘솔의 패키지 페이지를 열려면이 옵션을 선택 </strong> 합니다. 이 페이지를 사용 하 여 서버에 추가 된 패키지를 검토할 수 있습니다. 또한 연결 그룹을 관리할 수 있을 뿐만 아니라 패키지를 추가 하거나 업그레이드할 수도 있습니다.</p></li>
<li><p><strong>서버 </strong> – <strong> 관리 콘솔의 서버 페이지를 열려면이 옵션을 선택 </strong> 합니다. 이 페이지를 사용 하 여 App-v 5.0 인프라에 등록 된 서버 목록을 검토 합니다.</p></li>
<li><p><strong>클라이언트 </strong> -app-v 5.0 클라이언트에 대 한 일반 정보를 검토 하려면이 옵션을 선택 합니다.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>패키지 탭</p></td>
<td align="left"><p>패키지 <strong> </strong> 탭을 사용 하 여 패키지를 추가 하거나 업그레이드 합니다. 연결 그룹을 클릭 하 여 연결 그룹을 관리할 수도 있습니다 <strong> </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>서버 탭</p></td>
<td align="left"><p><strong>서버 탭을 사용 </strong> 하 여 새 서버를 등록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리자 탭</p></td>
<td align="left"><p><strong>관리자 </strong> 탭을 사용 하 여 앱-V 5.0 환경에서 관리자를 등록, 추가 또는 제거 합니다.</p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a>이 앱에 대 한 기타 리소스-V 5.0 배포


-   [Microsoft Application Virtualization 5.0 관리자 가이드](microsoft-application-virtualization-50-administrators-guide.md)

-   [App-V 5.0 작업](operations-for-app-v-50.md)

 

 





