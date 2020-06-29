---
title: 연결 그룹에서 패키지 버전을 무시하는 방법
description: 연결 그룹에서 패키지 버전을 무시하는 방법
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813961"
---
# <span data-ttu-id="b0472-103">연결 그룹에서 패키지 버전을 무시하는 방법</span><span class="sxs-lookup"><span data-stu-id="b0472-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="b0472-104">Microsoft App-v (Application Virtualization) 5.0 SP3에서는 패키지 업그레이드를 간소화 하 고 만들어야 하는 연결 그룹의 수를 줄이기 위해 모든 버전의 패키지를 사용 하도록 연결 그룹을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-104">Microsoft Application Virtualization (App-V) 5.0 SP3 enables you to configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="b0472-105">이전 버전의 App-v에서 패키지를 업그레이드 하려면 연결 그룹을 사용 하지 않도록 설정 하 고 연결 그룹의 XML 정의 파일을 수정 하는 등 몇 가지 단계를 수행 해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-105">To upgrade a package in earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0472-106">앱-V 5.0 SP3이 포함 된 작업 설명</span><span class="sxs-lookup"><span data-stu-id="b0472-106">Task description with App-V 5.0 SP3</span></span></th>
<th align="left"><span data-ttu-id="b0472-107">앱-V 5.0 SP3을 사용 하 여 작업을 수행 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b0472-107">How to perform the task with App-V 5.0 SP3</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0472-108">연결 그룹을 사용 하지 않도록 설정 하지 않고 패키지를 업그레이드할 수 있도록 모든 버전의 패키지를 받아들이도록 연결 그룹을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="b0472-109">기능이 작동 하는 방식입니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="b0472-110">연결 그룹이 여러 버전의 패키지에 대 한 액세스 권한이 있는 경우 최신 버전이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="b0472-111">연결 그룹에 잘못 된 버전이 있는 선택적 패키지가 포함 된 경우 패키지가 무시 되 고 연결 그룹의 가상 환경이 만들어지지 않도록 차단 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="b0472-112">연결 그룹에 잘못 된 버전이 있는 선택적 패키지가 포함 되어 있지 않은 경우 연결 그룹의 가상 환경을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0472-113">메서드</span><span class="sxs-lookup"><span data-stu-id="b0472-113">Method</span></span></th>
<th align="left"><span data-ttu-id="b0472-114">단계</span><span class="sxs-lookup"><span data-stu-id="b0472-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0472-115">App-v Server – 관리 콘솔</span><span class="sxs-lookup"><span data-stu-id="b0472-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="b0472-116">관리 콘솔에서 <strong> 패키지 </strong> &gt; <strong> 연결 그룹을 선택 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-116">In the Management Console, select <strong>PACKAGES</strong> &gt; <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b0472-117">연결 그룹 라이브러리에서 올바른 연결 그룹을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="b0472-118"><strong> </strong> 연결 된 패키지 창에서 편집을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="b0472-119"><strong> </strong> 패키지 이름 옆에 있는 버전 사용 확인란을 선택 하 고 적용을 <strong> 클릭 </strong> 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="b0472-120">패키지를 추가 하거나 업그레이드 하는 방법에 대 한 자세한 내용은 <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> 관리 콘솔을 사용 하 여 패키지를 추가 하거나 업그레이드 하는 방법을 참조 하세요 </a> .</span><span class="sxs-lookup"><span data-stu-id="b0472-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b0472-121">독립 실행형 컴퓨터의 app-v 클라이언트</span><span class="sxs-lookup"><span data-stu-id="b0472-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="b0472-122">연결 그룹 XML 문서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="b0472-123">패키지를 업그레이드 하려면 <strong> package </strong> 태그 특성을 <strong> </strong> 별표 ( <strong>\*</strong> )로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="b0472-124">다음 cmdlet을 사용 하 여 연결 그룹을 추가 하 고 연결 그룹 XML 문서의 경로를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="b0472-125">추가-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="b0472-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="b0472-126">패키지를 업그레이드 하는 경우 다음 cmdlet을 사용 하 여 이전 패키지를 제거 하 고 업그레이드 된 패키지를 추가 하 고 업그레이드 된 패키지를 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="b0472-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b0472-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="b0472-128">추가-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b0472-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="b0472-129">게시-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="b0472-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="b0472-130">자세한 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b0472-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="b0472-131">예제 XML 파일, <strong> 선택적 패키지가 포함 된 연결 그룹 XML 파일 </strong> ,이 섹션에서는 <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> 연결 그룹에서 선택적 패키지를 사용 하는 방법에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0472-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="b0472-132">PowerShell을 사용하여 독립 실행형 컴퓨터에서 실행되는 App-V 5.0 패키지를 관리하는 방법</span><span class="sxs-lookup"><span data-stu-id="b0472-132">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="b0472-133">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b0472-133">Related topics</span></span>


[<span data-ttu-id="b0472-134">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="b0472-134">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





