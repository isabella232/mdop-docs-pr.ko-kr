---
title: App-V 5.0 시작
description: App-V 5.0 시작
author: dansimp
ms.assetid: 3e16eafb-ce95-4d06-b214-fe0f4b1b495f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7979c81b7b57107f824b96d9fef8049a00c5b08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814553"
---
# <span data-ttu-id="9b988-103">App-V 5.0 시작</span><span class="sxs-lookup"><span data-stu-id="9b988-103">Getting Started with App-V 5.0</span></span>


<span data-ttu-id="9b988-104">앱-V 5.0를 사용 하면 필요한 기준에 따라 관리자가 실시간으로 응용 프로그램을 서비스로 배포, 업데이트 및 지원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-104">App-V 5.0 enables administrators to deploy, update, and support applications as services in real time, on an as-needed basis.</span></span> <span data-ttu-id="9b988-105">개별 응용 프로그램은 로컬로 설치 된 제품에서 중앙 관리 서비스로 변환 되며 컴퓨터를 미리 구성 하거나 운영 체제 설정을 변경할 필요 없이 필요할 때마다 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-105">Individual applications are transformed from locally installed products into centrally managed services and are available wherever you need, without the need to preconfigure computers or to change operating system settings.</span></span>

<span data-ttu-id="9b988-106">App-v는 다음 요소로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-106">App-V consists of the following elements:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b988-107">요소</span><span class="sxs-lookup"><span data-stu-id="9b988-107">Element</span></span></th>
<th align="left"><span data-ttu-id="9b988-108">설명</span><span class="sxs-lookup"><span data-stu-id="9b988-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b988-109">App-v 관리 서버</span><span class="sxs-lookup"><span data-stu-id="9b988-109">App-V Management Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9b988-110">App-v 데스크톱 클라이언트와 원격 데스크톱 서비스 (이전의 터미널 서비스) 클라이언트 모두에 가상 응용 프로그램을 제공 하는 App-v 인프라를 관리할 수 있는 중앙 위치를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-110">Provides a central location for managing the App-V infrastructure, which delivers virtual applications to both the App-V Desktop Client and the Remote Desktop Services (formerly Terminal Services) Client.</span></span></p></li>
<li><p><span data-ttu-id="9b988-111">하나 이상의 App-v 관리 서버가 단일 SQL Server 데이터 저장소를 공유할 수 있는 데이터 저장소에 대해 Microsoft SQL Server®를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-111">Uses Microsoft SQL Server® for its data store, where one or more App-V Management servers can share a single SQL Server data store.</span></span></p></li>
<li><p><span data-ttu-id="9b988-112">요청을 인증 하 고 보안, 계량, 모니터링, 데이터 수집을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-112">Authenticates requests and provides security, metering, monitoring, and data gathering.</span></span> <span data-ttu-id="9b988-113">서버는 Active Directory 및 지원 도구를 사용 하 여 사용자 및 응용 프로그램을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-113">The server uses Active Directory and supporting tools to manage users and applications.</span></span></p></li>
<li><p><span data-ttu-id="9b988-114">컴퓨터에서 App-v 인프라를 구성할 수 있는 Silverlight® 기반 관리 사이트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-114">Has a Silverlight®-based management site, which enables you to configure the App-V infrastructure from any computer.</span></span> <span data-ttu-id="9b988-115">응용 프로그램을 추가 및 제거 하 고, 바로 가기를 조작 하 고, 사용자 및 그룹에 대 한 액세스 권한을 할당 하 고, 연결 그룹을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-115">You can add and remove applications, manipulate shortcuts, assign access permissions to users and groups, and create connection groups.</span></span></p></li>
<li><p><span data-ttu-id="9b988-116">App-v 웹 관리 콘솔과 SQL Server 데이터 저장소 간의 통신을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-116">Enables communication between the App-V Web Management Console and the SQL Server data store.</span></span> <span data-ttu-id="9b988-117">이러한 구성 요소는 필요한 시스템 아키텍처에 따라 단일 서버 컴퓨터 또는 하나 이상의 개별 컴퓨터에 모두 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-117">These components can all be installed on a single server computer, or on one or more separate computers, depending on the required system architecture.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b988-118">App-v 게시 서버</span><span class="sxs-lookup"><span data-stu-id="9b988-118">App-V Publishing Server</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9b988-119">특정 사용자를 위한 응용 프로그램을 사용 하 여 App-v 클라이언트 제공</span><span class="sxs-lookup"><span data-stu-id="9b988-119">Provides App-V Clients with entitled applications for the specific user</span></span></p></li>
<li><p><span data-ttu-id="9b988-120">스트리밍을 위한 가상 응용 프로그램 패키지를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-120">Hosts the virtual application package for streaming.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b988-121">App-v 데스크톱 클라이언트</span><span class="sxs-lookup"><span data-stu-id="9b988-121">App-V Desktop Client</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9b988-122">가상 응용 프로그램 검색</span><span class="sxs-lookup"><span data-stu-id="9b988-122">Retrieves virtual applications</span></span></p></li>
<li><p><span data-ttu-id="9b988-123">클라이언트에 응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="9b988-123">Publishes the applications on the clients</span></span></p></li>
<li><p><span data-ttu-id="9b988-124">Windows 끝점의 런타임에 가상 환경을 자동으로 설정 하 고 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-124">Automatically sets up and manages virtual environments at runtime on Windows endpoints.</span></span></p></li>
<li><p><span data-ttu-id="9b988-125">레지스트리와 파일 변경 등의 사용자 특정 가상 응용 프로그램 설정을 각 사용자&#39;s 프로필에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-125">Stores user-specific virtual application settings, such as registry and file changes, in each user&#39;s profile.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b988-126">앱-V 원격 데스크톱 서비스 (RDS) 클라이언트</span><span class="sxs-lookup"><span data-stu-id="9b988-126">App-V Remote Desktop Services (RDS) Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b988-127">원격 데스크톱 세션 호스트 서버에서 공유 데스크톱 세션에 대 한 App-v 데스크톱 클라이언트의 기능을 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-127">Enables Remote Desktop Session Host servers to use the capabilities of the App-V Desktop Client for shared desktop sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b988-128">App-V 시퀀서</span><span class="sxs-lookup"><span data-stu-id="9b988-128">App-V Sequencer</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9b988-129">기존 응용 프로그램을 가상 응용 프로그램으로 변환 하는 데 사용 하는 마법사 기반 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-129">Is a wizard-based tool that you use to transform traditional applications into virtual applications.</span></span></p></li>
<li><p><span data-ttu-id="9b988-130">다음과 같이 구성 된 "package" 응용 프로그램을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-130">Produces the application “package,” which consists of:</span></span></p>
<ol>
<li><p><span data-ttu-id="9b988-131">APPV (시퀀싱 된 응용 프로그램) 파일</span><span class="sxs-lookup"><span data-stu-id="9b988-131">a sequenced application (APPV) file</span></span></p></li>
<li><p><span data-ttu-id="9b988-132">독립 실행형 작업을 위해 구성 된 클라이언트에 배포할 수 있는 MSI (Windows Installer 파일)</span><span class="sxs-lookup"><span data-stu-id="9b988-132">a Windows Installer file (MSI) that can be deployed to clients configured for stand-alone operation</span></span></p></li>
<li><p><span data-ttu-id="9b988-133">Report.XML, PackageName_DeploymentConfig.XML 및 PackageName_UserConfig.XML을 비롯 한 여러 XML 파일</span><span class="sxs-lookup"><span data-stu-id="9b988-133">Several XML files including Report.XML, PackageName_DeploymentConfig.XML, and PackageName_UserConfig.XML.</span></span> <span data-ttu-id="9b988-134">UserConfig 및 DeploymentConfig XML 파일은 패키지의 기본 동작에 대 한 사용자 지정 변경을 구성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-134">The UserConfig and DeploymentConfig XML files are used to configure custom changes to the default behavior of the package.</span></span></p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9b988-135">이러한 요소에 대 한 자세한 내용은 [앱-V 5.0의 상위 수준 아키텍처](high-level-architecture-for-app-v-50.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b988-135">For more information about these elements, see [High Level Architecture for App-V 5.0](high-level-architecture-for-app-v-50.md).</span></span>

<span data-ttu-id="9b988-136">이 제품을 처음 사용할 경우에는 문서를 철저히 읽어 보는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-136">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="9b988-137">프로덕션 환경에 배포 하기 전에 테스트 네트워크 환경에서 배포 계획의 유효성을 검사 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-137">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="9b988-138">관련 기술에 대 한 수업을 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-138">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="9b988-139">Microsoft 교육 기회에 대 한 자세한 내용은의 Microsoft 교육 개요를 참조 하세요 <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="9b988-139">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="9b988-140">**참고**  이 관리자 가이드의 다운로드 가능한 버전을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-140">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="9b988-141">그러나 문서를 선택 하 고, 컬렉션에서 그룹화 하 고, 인쇄 하거나, 파일 ()에 파일로 내보내는 기능을 제공 하는 TechNet 라이브러리의 특별 한 모드에 대해 배울 수 있습니다 <https://go.microsoft.com/fwlink/?LinkId=272491> https://go.microsoft.com/fwlink/?LinkId=272491) .</span><span class="sxs-lookup"><span data-stu-id="9b988-141">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272491> (https://go.microsoft.com/fwlink/?LinkId=272491).</span></span>

 

<span data-ttu-id="9b988-142">앱-V 5.0 관리자 가이드의이 섹션에서는 배포 계획을 시작 하기 전에 제품에 대 한 기본적인 이해를 제공 하기 위해 App-v 5.0에 대 한 상위 수준의 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-142">This section of the App-V 5.0 Administrator’s Guide includes high-level information about App-V 5.0 to provide you with a basic understanding of the product before you begin the deployment planning.</span></span>

## <span data-ttu-id="9b988-143">앱 시작-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9b988-143">Getting started with App-V 5.0</span></span>


-   [<span data-ttu-id="9b988-144">App-V 5.0 정보</span><span class="sxs-lookup"><span data-stu-id="9b988-144">About App-V 5.0</span></span>](about-app-v-50.md)

    <span data-ttu-id="9b988-145">앱-V 5.0에 대 한 간략 한 개요와 조직에서 사용할 수 있는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-145">Provides a high-level overview of App-V 5.0 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="9b988-146">App-V 5.0 SP1 정보</span><span class="sxs-lookup"><span data-stu-id="9b988-146">About App-V 5.0 SP1</span></span>](about-app-v-50-sp1.md)

    <span data-ttu-id="9b988-147">App-v 5.0 SP1 및 조직에서 앱을 사용 하는 방법에 대 한 개략적인 수준의 개요를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-147">Provides a high-level overview of App-V 5.0SP1 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="9b988-148">App-V 5.0 SP2 정보</span><span class="sxs-lookup"><span data-stu-id="9b988-148">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

    <span data-ttu-id="9b988-149">App-v 5.0 SP2에 대 한 간략 한 개요와 조직에서 사용할 수 있는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-149">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="9b988-150">App-V 5.0 SP3 정보</span><span class="sxs-lookup"><span data-stu-id="9b988-150">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

    <span data-ttu-id="9b988-151">App-v 5.0 SP2에 대 한 간략 한 개요와 조직에서 사용할 수 있는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-151">Provides a high-level overview of App-V 5.0SP2 and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="9b988-152">App-V 5.0 평가</span><span class="sxs-lookup"><span data-stu-id="9b988-152">Evaluating App-V 5.0</span></span>](evaluating-app-v-50.md)

    <span data-ttu-id="9b988-153">조직에서 사용할 앱-V 5.0을 최적화 하는 방법에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-153">Provides information about how you can best evaluate App-V 5.0 for use in your organization.</span></span>

-   [<span data-ttu-id="9b988-154">App-V 5.0의 개략적인 아키텍처</span><span class="sxs-lookup"><span data-stu-id="9b988-154">High Level Architecture for App-V 5.0</span></span>](high-level-architecture-for-app-v-50.md)

    <span data-ttu-id="9b988-155">App-v 5.0 기능에 대 한 설명과 함께 작동 하는 방식에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-155">Provides a description of the App-V 5.0 features and how they work together.</span></span>

-   [<span data-ttu-id="9b988-156">App-V 5.0의 접근성</span><span class="sxs-lookup"><span data-stu-id="9b988-156">Accessibility for App-V 5.0</span></span>](accessibility-for-app-v-50.md)

    <span data-ttu-id="9b988-157">장애가 있는 사용자가이 제품 및 해당 문서에 더욱 쉽게 액세스할 수 있도록 하는 기능 및 서비스에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b988-157">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="9b988-158">이 제품에 대 한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="9b988-158">Other resources for this product</span></span>


-   [<span data-ttu-id="9b988-159">Microsoft Application Virtualization 5.0 관리자 가이드</span><span class="sxs-lookup"><span data-stu-id="9b988-159">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="9b988-160">App-V 5.0 계획</span><span class="sxs-lookup"><span data-stu-id="9b988-160">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

-   [<span data-ttu-id="9b988-161">App-V 5.0 배포</span><span class="sxs-lookup"><span data-stu-id="9b988-161">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

-   [<span data-ttu-id="9b988-162">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="9b988-162">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

-   [<span data-ttu-id="9b988-163">App-V 5.0 문제 해결</span><span class="sxs-lookup"><span data-stu-id="9b988-163">Troubleshooting App-V 5.0</span></span>](troubleshooting-app-v-50.md)






 

 





