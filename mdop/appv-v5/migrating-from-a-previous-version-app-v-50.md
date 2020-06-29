---
title: 이전 버전에서 마이그레이션
description: 이전 버전에서 마이그레이션
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813556"
---
# <span data-ttu-id="ea4a8-103">이전 버전에서 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="ea4a8-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="ea4a8-104">App-v 5.0를 사용 하면 기존 App-v 4.6 인프라를 보다 유연 하 고 통합 하 고 보다 쉽게 앱-V 5.0 인프라를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="ea4a8-105">마이그레이션 전략을 계획할 때는 다음 섹션을 고려 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="ea4a8-106">**참고**  App-v 4.6 및 App-v 5.0 간의 차이점에 대 한 자세한 내용은 [app-v 5.0에 대 한](about-app-v-50.md)앱- **v 4.6 및 app-v 5.0 섹션의 차이점** 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="ea4a8-107">이전 버전의 App-v를 사용 하 여 만든 패키지 변환</span><span class="sxs-lookup"><span data-stu-id="ea4a8-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="ea4a8-108">패키지 변환기 유틸리티를 사용 하 여 이전 버전의 App-v를 사용 하 여 만든 가상 응용 프로그램 패키지를 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="ea4a8-109">패키지 변환기는 PowerShell을 사용 하 여 패키지를 변환 하며 변환이 필요한 패키지가 여러 개 있는 경우 프로세스를 자동화 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="ea4a8-110">**중요**  기존 패키지를 변환한 후에는 패키지를 배포 하기 전에 패키지를 테스트 하 여 변환 프로세스가 성공적으로 수행 되었는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="ea4a8-111">기존 패키지를 변환 하기 전에 알아야 할 사항</span><span class="sxs-lookup"><span data-stu-id="ea4a8-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ea4a8-112">문제</span><span class="sxs-lookup"><span data-stu-id="ea4a8-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="ea4a8-113">해결 방법</span><span class="sxs-lookup"><span data-stu-id="ea4a8-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-114">패키지 스크립트는 변환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea4a8-115">변환 된 패키지를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-115">Test the converted package.</span></span> <span data-ttu-id="ea4a8-116">필요한 경우 스크립트를 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea4a8-117">패키지 레지스트리 설정 재정의가 변환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea4a8-118">변환 된 패키지를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-118">Test the converted package.</span></span> <span data-ttu-id="ea4a8-119">필요한 경우 레지스트리 재정의를 다시 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-120">DSC를 사용 하는 가상 패키지는 변환 후 연결 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea4a8-121">연결 그룹을 사용 하 여 패키지를 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-121">Link the packages using connection groups.</span></span> <span data-ttu-id="ea4a8-122"><a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">연결 그룹 관리를 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="ea4a8-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea4a8-123">환경 변수 충돌은 변환 중에 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea4a8-124">관련 된 .osd 파일의 모든 충돌을 해결 <strong> </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-125">변환 하는 동안 하드 코드 된 경로가 감지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea4a8-126">하드 코드 된 경로는 제대로 변환 하기가 어렵습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="ea4a8-127">패키지 변환기는 하드 코드 된 경로가 들어 있는 파일을 사용 하 여 패키지를 감지 하 고 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="ea4a8-128">하드 코드 된 경로를 사용 하 여 파일을 보고 패키지에 파일이 필요한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="ea4a8-129">그렇다면 패키지를 다시 시퀀싱 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ea4a8-130">패키지를 변환할 때 파일 또는 바로 가기가 실패 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="ea4a8-131">앱-V 4.6 패키지에서 항목을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="ea4a8-132">경로를 하드 코드화 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="ea4a8-133">경로를 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-133">Convert the path.</span></span>

<span data-ttu-id="ea4a8-134">**참고**  기능을 활용 해야 하는 중요 한 응용 프로그램 또는 응용 프로그램을 변환 하는 데 App-v 5.0 sequencer를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="ea4a8-135">[앱-V 5.0를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법을](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="ea4a8-136">변환 후 변환 된 패키지가 열리지 않는 경우 App-v 5.0 sequencer를 사용 하 여 응용 프로그램을 다시 시퀀싱 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="ea4a8-137">이전 버전의 App-V에서 만든 패키지를 변환하는 방법</span><span class="sxs-lookup"><span data-stu-id="ea4a8-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="ea4a8-138">클라이언트 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="ea4a8-138">Migrating Clients</span></span>


<span data-ttu-id="ea4a8-139">다음 표에서는 클라이언트 업그레이드에 권장 되는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ea4a8-140">작업</span><span class="sxs-lookup"><span data-stu-id="ea4a8-140">Task</span></span></th>
<th align="left"><span data-ttu-id="ea4a8-141">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ea4a8-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-142">환경을 앱-V 4.6 SP2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="ea4a8-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="ea4a8-143">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</span><span class="sxs-lookup"><span data-stu-id="ea4a8-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea4a8-144">공존을 사용 하도록 설정 된 App-v 5.0 클라이언트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="ea4a8-145">앱-V 4.6 및 App-v 5.0 클라이언트를 같은 컴퓨터에 배포 하는 방법을 설명 </a> 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-146">앱-V 5.0 패키지 순서 및 롤아웃</span><span class="sxs-lookup"><span data-stu-id="ea4a8-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="ea4a8-147">필요에 따라 App-v 4.6 패키지의 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="ea4a8-148">앱-V 5.0를 사용 하 여 새 응용 프로그램을 시퀀싱 하는 방법 </a></span><span class="sxs-lookup"><span data-stu-id="ea4a8-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ea4a8-149">**중요**  공존 모드를 사용 하려면 App-V 4.6 SP3을 실행 중 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="ea4a8-150">또한 패키지를 시퀀싱 하는 경우 **사용자 구성 섹션** **에 설정** 되어 있는 관리 권한 설정을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="ea4a8-151">App-v 5.0 서버 전체 인프라 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="ea4a8-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="ea4a8-152">전체 App-v 5.0 인프라로 업그레이드 하는 직접적인 방법은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="ea4a8-153">App-v server를 업그레이드 하는 방법에 대 한 자세한 내용은 다음 섹션의 정보를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ea4a8-154">작업</span><span class="sxs-lookup"><span data-stu-id="ea4a8-154">Task</span></span></th>
<th align="left"><span data-ttu-id="ea4a8-155">추가 정보</span><span class="sxs-lookup"><span data-stu-id="ea4a8-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-156">환경을 App-v 4.6 SP3으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="ea4a8-157">응용 프로그램 가상화 배포 및 업그레이드 고려 사항 </a> .</span><span class="sxs-lookup"><span data-stu-id="ea4a8-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea4a8-158">앱-V 5.0 버전의 클라이언트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="ea4a8-159">App-v 클라이언트를 배포 하는 방법 </a></span><span class="sxs-lookup"><span data-stu-id="ea4a8-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ea4a8-160">App-v 5.0 서버를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="ea4a8-161">App-v 5.0 서버를 배포 하는 방법 </a></span><span class="sxs-lookup"><span data-stu-id="ea4a8-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ea4a8-162">기존 패키지 마이그레이션.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ea4a8-163"><strong>이 문서의 이전 버전의 app-v 섹션을 사용 하 여 만든 패키지 변환을 참조 하세요 </strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a8-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ea4a8-164">추가 마이그레이션 작업</span><span class="sxs-lookup"><span data-stu-id="ea4a8-164">Additional Migration tasks</span></span>


<span data-ttu-id="ea4a8-165">또한 끝점 재구성, 그리고 App-v 5.0 클라이언트를 실행 하는 컴퓨터에서 이전 버전을 사용 하 여 만든 패키지를 여는 등의 추가 마이그레이션 작업을 수행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="ea4a8-166">다음 링크는 이러한 작업을 수행 하는 방법에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea4a8-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="ea4a8-167">특정 컴퓨터의 모든 사용자에 대해 App-V 4.6 패키지에서 변환된 App-V 5.0 패키지로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="ea4a8-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="ea4a8-168">특정 사용자에 대해 App-V 4.6 패키지에서 App-V 5.0으로 확장 지점을 마이그레이션하는 방법</span><span class="sxs-lookup"><span data-stu-id="ea4a8-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="ea4a8-169">특정 컴퓨터의 모든 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="ea4a8-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="ea4a8-170">특정 사용자에 대해 App-V 5.0 패키지에서 App-V 4.6 패키지로 확장 지점을 되돌리는 방법</span><span class="sxs-lookup"><span data-stu-id="ea4a8-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="ea4a8-171">앱-V 마이그레이션 작업을 수행 하기 위한 기타 리소스</span><span class="sxs-lookup"><span data-stu-id="ea4a8-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="ea4a8-172">App-V 5.0 작업</span><span class="sxs-lookup"><span data-stu-id="ea4a8-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="ea4a8-173">간단한 Microsoft App-v 5.1 관리 서버 업그레이드 절차</span><span class="sxs-lookup"><span data-stu-id="ea4a8-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





