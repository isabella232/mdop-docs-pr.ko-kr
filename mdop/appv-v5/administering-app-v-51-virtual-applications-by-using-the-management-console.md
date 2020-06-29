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
# <span data-ttu-id="65d6d-103">관리 콘솔을 사용하여 App-V 5.1 가상 응용 프로그램 관리</span><span class="sxs-lookup"><span data-stu-id="65d6d-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="65d6d-104">Microsoft App-v (Application Virtualization) 5.1 관리 서버를 사용 하 여 환경에서 패키지, 연결 그룹, 패키지 액세스를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="65d6d-105">서버는 App-v 5.1 클라이언트를 실행 하는 권한이 부여 된 컴퓨터에 응용 프로그램 아이콘, 바로 가기 및 파일 형식 연결을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="65d6d-106">일반적으로 하나 이상의 관리 서버는 구성 및 패키지 정보에 대 한 공통 데이터 저장소를 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="65d6d-107">관리 서버는 AD DS (Active Directory 도메인 서비스) 그룹을 사용 하 여 사용자 권한을 관리 하 고 데이터베이스 및 데이터 저장소를 관리 하기 위해 SQL Server가 설치 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="65d6d-108">관리 서버는 응용 프로그램을 요청에 따라 최종 사용자에 게 스트리밍할 수 있으므로 이러한 서버는 신뢰할 수 있는 높은 대역폭 Lan이 있는 시스템 구성에 가장 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="65d6d-109">관리 서버는 다음 구성 요소로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="65d6d-110">관리 서버 – 관리 서버를 사용 하 여 패키지 및 연결 그룹을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="65d6d-111">게시 서버 – 앱-V 5.1 클라이언트를 실행 하는 컴퓨터에 게시 서버를 사용 하 여 패키지를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="65d6d-112">관리 데이터베이스-관리 데이터베이스를 사용 하 여 패키지 액세스를 관리 하 고 서버 동기화를 관리 서버에 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="65d6d-113">관리 콘솔 작업</span><span class="sxs-lookup"><span data-stu-id="65d6d-113">Management Console tasks</span></span>


<span data-ttu-id="65d6d-114">App-v 5.1 관리 콘솔을 사용 하 여 수행할 수 있는 가장 일반적인 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="65d6d-115">관리 콘솔에 연결하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="65d6d-116">관리 콘솔을 사용하여 패키지를 추가 또는 업그레이드하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="65d6d-117">관리 콘솔을 사용하여 패키지에 대한 액세스 권한을 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="65d6d-118">관리 콘솔을 사용하여 패키지를 게시하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="65d6d-119">관리 콘솔에서 패키지를 삭제하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="65d6d-120">관리 콘솔을 사용하여 관리자를 추가하거나 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="65d6d-121">관리 콘솔을 사용하여 게시 서버를 등록 및 등록 취소하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="65d6d-122">App-V 5.1 관리 콘솔을 사용하여 사용자 지정 구성 파일을 만드는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="65d6d-123">관리 콘솔을 사용하여 패키지의 다른 버전으로 액세스 권한 및 구성을 전송하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="65d6d-124">관리 콘솔을 사용하여 특정 AD 그룹의 가상 응용 프로그램 확장을 사용자 지정하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="65d6d-125">관리 콘솔을 사용하여 응용 프로그램 및 기본 가상 응용 프로그램 확장을 보고 구성하는 방법</span><span class="sxs-lookup"><span data-stu-id="65d6d-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="65d6d-126">App-v 5.1 관리 콘솔의 주요 요소는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="65d6d-127">관리 콘솔 탭</span><span class="sxs-lookup"><span data-stu-id="65d6d-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="65d6d-128">설명</span><span class="sxs-lookup"><span data-stu-id="65d6d-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65d6d-129">패키지 탭</span><span class="sxs-lookup"><span data-stu-id="65d6d-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="65d6d-130">패키지 <strong> </strong> 탭을 사용 하 여 패키지를 추가 하거나 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65d6d-131">연결 그룹 탭</span><span class="sxs-lookup"><span data-stu-id="65d6d-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="65d6d-132">연결 그룹 <strong> </strong> 을 관리 하려면 연결 그룹 탭을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65d6d-133">서버 탭</span><span class="sxs-lookup"><span data-stu-id="65d6d-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="65d6d-134"><strong>서버 탭을 사용 </strong> 하 여 새 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65d6d-135">관리자 탭</span><span class="sxs-lookup"><span data-stu-id="65d6d-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="65d6d-136"><strong>관리자 </strong> 탭을 사용 하 여 앱-V 5.1 환경에서 관리자를 등록, 추가 또는 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="65d6d-137">**중요**  웹 관리 콘솔을 여는 브라우저에서 JavaScript를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d6d-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="65d6d-138">이 앱에 대 한 기타 리소스-V 5.1 배포</span><span class="sxs-lookup"><span data-stu-id="65d6d-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="65d6d-139">Microsoft Application Virtualization 5.1 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="65d6d-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="65d6d-140">App-V 5.1 작업</span><span class="sxs-lookup"><span data-stu-id="65d6d-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





