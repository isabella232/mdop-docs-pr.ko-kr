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
# <span data-ttu-id="fa4ca-103">관리 콘솔을 사용하여 App-V 5.0 가상 응용 프로그램 관리</span><span class="sxs-lookup"><span data-stu-id="fa4ca-103">Administering App-V 5.0 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="fa4ca-104">Microsoft App-v (Application Virtualization) 5.0 관리 서버를 사용 하 여 환경에서 패키지, 연결 그룹, 패키지 액세스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-104">Use the Microsoft Application Virtualization (App-V) 5.0 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="fa4ca-105">서버는 App-v 5.0 클라이언트를 실행 하는 권한이 부여 된 컴퓨터에 응용 프로그램 아이콘, 바로 가기 및 파일 형식 연결을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="fa4ca-106">일반적으로 하나 이상의 관리 서버는 구성 및 패키지 정보에 대 한 공통 데이터 저장소를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="fa4ca-107">관리 서버는 AD DS (Active Directory 도메인 서비스) 그룹을 사용 하 여 사용자 권한을 관리 하 고 데이터베이스 및 데이터 저장소를 관리 하기 위해 SQL Server가 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="fa4ca-108">관리 서버는 응용 프로그램을 요청에 따라 최종 사용자에 게 스트리밍할 수 있으므로 이러한 서버는 신뢰할 수 있는 높은 대역폭 Lan이 있는 시스템 구성에 가장 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="fa4ca-109">관리 서버는 다음 구성 요소로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="fa4ca-110">관리 서버 – 관리 서버를 사용 하 여 패키지 및 연결 그룹을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="fa4ca-111">게시 서버 – 앱-V 5.0 클라이언트를 실행 하는 컴퓨터에 게시 서버를 사용 하 여 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.0 client.</span></span>

-   <span data-ttu-id="fa4ca-112">관리 데이터베이스-관리 데이터베이스를 사용 하 여 패키지 액세스를 관리 하 고 서버 동기화를 관리 서버에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="fa4ca-113">관리 콘솔 작업</span><span class="sxs-lookup"><span data-stu-id="fa4ca-113">Management Console tasks</span></span>


<span data-ttu-id="fa4ca-114">App-v 5.0 관리 콘솔을 사용 하 여 수행할 수 있는 가장 일반적인 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-114">The most common tasks that you can perform with the App-V 5.0 Management console are:</span></span>

-   [<span data-ttu-id="fa4ca-115">관리 콘솔에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-beta.md)

-   [<span data-ttu-id="fa4ca-116">관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [<span data-ttu-id="fa4ca-117">관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [<span data-ttu-id="fa4ca-118">관리 콘솔을 사용하여 패키지를 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [<span data-ttu-id="fa4ca-119">관리 콘솔에서 패키지를 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-beta.md)

-   [<span data-ttu-id="fa4ca-120">관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [<span data-ttu-id="fa4ca-121">관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [<span data-ttu-id="fa4ca-122">App-V 5.0 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-122">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [<span data-ttu-id="fa4ca-123">관리 콘솔을 사용하여 패키지의 다른 버전으로 액세스 권한 및 구성을 전송하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [<span data-ttu-id="fa4ca-124">관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="fa4ca-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [<span data-ttu-id="fa4ca-125">관리 콘솔에서 응용 프로그램 및 기본 가상 응용 프로그램 확장 구성</span><span class="sxs-lookup"><span data-stu-id="fa4ca-125">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

<span data-ttu-id="fa4ca-126">App-v 5.0 관리 콘솔의 주요 요소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-126">The main elements of the App-V 5.0 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fa4ca-127">관리 콘솔 탭</span><span class="sxs-lookup"><span data-stu-id="fa4ca-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="fa4ca-128">설명</span><span class="sxs-lookup"><span data-stu-id="fa4ca-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa4ca-129">개요</span><span class="sxs-lookup"><span data-stu-id="fa4ca-129">Overview</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><strong><span data-ttu-id="fa4ca-130">App-v 시퀀서-v </strong> - 5.0 Sequencer 사용에 대 한 일반적인 정보를 검토 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-130">App-V Sequencer</strong> - Select this option to review general information about using the App-V 5.0 sequencer.</span></span></p></li>
<li><p><strong><span data-ttu-id="fa4ca-131">응용 프로그램 패키지 라이브러리 </strong> – <strong> 관리 콘솔의 패키지 페이지를 열려면이 옵션을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-131">Application Packages Library</strong> – Select this option to open the <strong>PACKAGES</strong> page of the Management Console.</span></span> <span data-ttu-id="fa4ca-132">이 페이지를 사용 하 여 서버에 추가 된 패키지를 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-132">Use this page to review packages that have been added to the server.</span></span> <span data-ttu-id="fa4ca-133">또한 연결 그룹을 관리할 수 있을 뿐만 아니라 패키지를 추가 하거나 업그레이드할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-133">You can also manage the connection groups, as well as add or upgrade packages.</span></span></p></li>
<li><p><strong><span data-ttu-id="fa4ca-134">서버 </strong> – <strong> 관리 콘솔의 서버 페이지를 열려면이 옵션을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-134">SERVERS</strong> – Select this option to open the <strong>SERVERS</strong> page of the Management Console.</span></span> <span data-ttu-id="fa4ca-135">이 페이지를 사용 하 여 App-v 5.0 인프라에 등록 된 서버 목록을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-135">Use this page to review the list of servers that have been registered with your App-V 5.0 infrastructure.</span></span></p></li>
<li><p><strong><span data-ttu-id="fa4ca-136">클라이언트 </strong> -app-v 5.0 클라이언트에 대 한 일반 정보를 검토 하려면이 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-136">CLIENTS</strong> – Select this option to review general information about App-V 5.0 clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa4ca-137">패키지 탭</span><span class="sxs-lookup"><span data-stu-id="fa4ca-137">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa4ca-138">패키지 <strong> </strong> 탭을 사용 하 여 패키지를 추가 하거나 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-138">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span> <span data-ttu-id="fa4ca-139">연결 그룹을 클릭 하 여 연결 그룹을 관리할 수도 있습니다 <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="fa4ca-139">You can also manage connection groups by clicking <strong>CONNECTION GROUPS</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa4ca-140">서버 탭</span><span class="sxs-lookup"><span data-stu-id="fa4ca-140">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa4ca-141"><strong>서버 탭을 사용 </strong> 하 여 새 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-141">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa4ca-142">관리자 탭</span><span class="sxs-lookup"><span data-stu-id="fa4ca-142">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa4ca-143"><strong>관리자 </strong> 탭을 사용 하 여 앱-V 5.0 환경에서 관리자를 등록, 추가 또는 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-143">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.0 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a><span data-ttu-id="fa4ca-144">이 앱에 대 한 기타 리소스-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="fa4ca-144">Other resources for this App-V 5.0 deployment</span></span>


-   [<span data-ttu-id="fa4ca-145">Microsoft Application Virtualization 5.0 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="fa4ca-145">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="fa4ca-146">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="fa4ca-146">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





