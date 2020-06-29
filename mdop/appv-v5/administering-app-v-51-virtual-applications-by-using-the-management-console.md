---
title: 관리 콘솔을 사용하여 App-V 5.1 가상 응용 프로그램 관리
description: 관리 콘솔을 사용하여 App-V 5.1 가상 응용 프로그램 관리
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814865"
---
# 관리 콘솔을 사용하여 App-V 5.1 가상 응용 프로그램 관리


Microsoft App-v (Application Virtualization) 5.1 관리 서버를 사용 하 여 환경에서 패키지, 연결 그룹, 패키지 액세스를 관리할 수 있습니다. 서버는 App-v 5.1 클라이언트를 실행 하는 권한이 부여 된 컴퓨터에 응용 프로그램 아이콘, 바로 가기 및 파일 형식 연결을 게시 합니다. 일반적으로 하나 이상의 관리 서버는 구성 및 패키지 정보에 대 한 공통 데이터 저장소를 공유 합니다.

관리 서버는 AD DS (Active Directory 도메인 서비스) 그룹을 사용 하 여 사용자 권한을 관리 하 고 데이터베이스 및 데이터 저장소를 관리 하기 위해 SQL Server가 설치 되어 있습니다.

관리 서버는 응용 프로그램을 요청에 따라 최종 사용자에 게 스트리밍할 수 있으므로 이러한 서버는 신뢰할 수 있는 높은 대역폭 Lan이 있는 시스템 구성에 가장 적합 합니다. 관리 서버는 다음 구성 요소로 구성 됩니다.

-   관리 서버 – 관리 서버를 사용 하 여 패키지 및 연결 그룹을 관리 합니다.

-   게시 서버 – 앱-V 5.1 클라이언트를 실행 하는 컴퓨터에 게시 서버를 사용 하 여 패키지를 배포 합니다.

-   관리 데이터베이스-관리 데이터베이스를 사용 하 여 패키지 액세스를 관리 하 고 서버 동기화를 관리 서버에 게시 합니다.

## 관리 콘솔 작업


App-v 5.1 관리 콘솔을 사용 하 여 수행할 수 있는 가장 일반적인 작업은 다음과 같습니다.

-   [관리 콘솔에 연결하는 방법](how-to-connect-to-the-management-console-51.md)

-   [관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [관리 콘솔을 사용하여 패키지를 게시하는 방법](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [관리 콘솔에서 패키지를 삭제하는 방법](how-to-delete-a-package-in-the-management-console-51.md)

-   [관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [App-V 5.1 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [관리 콘솔을 사용하여 패키지의 다른 버전으로 액세스 권한 및 구성을 전송하는 방법](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [관리 콘솔을 사용하여 응용 프로그램 및 기본 가상 응용 프로그램 확장을 보고 구성하는 방법](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

App-v 5.1 관리 콘솔의 주요 요소는 다음과 같습니다.

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
<td align="left"><p>패키지 탭</p></td>
<td align="left"><p>패키지 <strong> </strong> 탭을 사용 하 여 패키지를 추가 하거나 업그레이드 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>연결 그룹 탭</p></td>
<td align="left"><p>연결 그룹 <strong> </strong> 을 관리 하려면 연결 그룹 탭을 사용 합니다.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>서버 탭</p></td>
<td align="left"><p><strong>서버 탭을 사용 </strong> 하 여 새 서버를 등록 합니다.</p></td>
</tr>
<tr class="even">
<td align="left"><p>관리자 탭</p></td>
<td align="left"><p><strong>관리자 </strong> 탭을 사용 하 여 앱-V 5.1 환경에서 관리자를 등록, 추가 또는 제거 합니다.</p></td>
</tr>
</tbody>
</table>

 

**중요**  웹 관리 콘솔을 여는 브라우저에서 JavaScript를 사용 하도록 설정 해야 합니다.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>이 앱에 대 한 기타 리소스-V 5.1 배포


-   [Microsoft Application Virtualization 5.1 관리자 가이드](microsoft-application-virtualization-51-administrators-guide.md)

-   [App-V 5.1 작업](operations-for-app-v-51.md)

 

 





