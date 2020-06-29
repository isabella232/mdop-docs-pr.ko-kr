---
title: 연결 그룹 파일 정보
description: 연결 그룹 파일 정보
author: dansimp
ms.assetid: bfeb6013-a7ca-4e36-9fe3-229702e83f0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5cb93326ce182d71de0f0f89cc569823d6154e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814932"
---
# <span data-ttu-id="1fee7-103">연결 그룹 파일 정보</span><span class="sxs-lookup"><span data-stu-id="1fee7-103">About the Connection Group File</span></span>


**<span data-ttu-id="1fee7-104">이 항목의 내용:</span><span class="sxs-lookup"><span data-stu-id="1fee7-104">In this topic:</span></span>**

-   [<span data-ttu-id="1fee7-105">연결 그룹 파일 용도 및 위치</span><span class="sxs-lookup"><span data-stu-id="1fee7-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="1fee7-106">연결 그룹 XML 파일의 구조</span><span class="sxs-lookup"><span data-stu-id="1fee7-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="1fee7-107">연결 그룹의 패키지 우선 순위 구성</span><span class="sxs-lookup"><span data-stu-id="1fee7-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="1fee7-108">지원 되는 가상 응용 프로그램 연결 구성</span><span class="sxs-lookup"><span data-stu-id="1fee7-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="1fee7-109">연결 그룹 파일 용도 및 위치</span><span class="sxs-lookup"><span data-stu-id="1fee7-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-110">연결 그룹 용도</span><span class="sxs-lookup"><span data-stu-id="1fee7-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-111">연결 그룹은 패키지를 그룹화 하 여 패키지의 응용 프로그램이 서로 상호 작용할 수 있는 가상 환경을 만드는 데 사용 되는 App-v 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="1fee7-112">예: Microsoft Office에서 플러그 인을 사용 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="1fee7-113">플러그 인을 포함 하는 패키지를 만들고, Office를 포함 하는 다른 패키지를 만든 다음 두 패키지를 연결 그룹에 추가 하 여 Office에서 해당 플러그 인을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fee7-114">연결 그룹 파일 작동 방식</span><span class="sxs-lookup"><span data-stu-id="1fee7-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-115">응용 프로그램 가상화 5.0 연결 그룹 파일을 적용 하면 파일에 열거 된 패키지가 런타임 시 단일 가상 환경으로 결합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-115">When you apply an Application Virtualization 5.0 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="1fee7-116">Microsoft App-v (Application Virtualization) 5.0 연결 그룹 파일을 사용 하 여 기존 Application Virtualization 5.0 연결 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-116">Use the Microsoft Application Virtualization (App-V) 5.0 connection group file to configure existing Application Virtualization 5.0 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-117">예제 파일 경로</span><span class="sxs-lookup"><span data-stu-id="1fee7-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="1fee7-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="1fee7-119">연결 그룹 XML 파일의 구조</span><span class="sxs-lookup"><span data-stu-id="1fee7-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="1fee7-120">이 섹션의 내용:</span><span class="sxs-lookup"><span data-stu-id="1fee7-120">In this section:</span></span>**

-   [<span data-ttu-id="1fee7-121">연결 그룹을 정의 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fee7-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="1fee7-122">연결 그룹의 패키지를 정의 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fee7-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="1fee7-123">App-v 5.0 SP3 예제 연결 그룹 XML 파일</span><span class="sxs-lookup"><span data-stu-id="1fee7-123">App-V 5.0 SP3 example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="1fee7-124">앱-V 5.0 ~ App-v 5.0 SP2 연결 그룹 XML 파일 예</span><span class="sxs-lookup"><span data-stu-id="1fee7-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="1fee7-125">연결 그룹을 정의 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fee7-125">Parameters that define the connection group</span></span>

<span data-ttu-id="1fee7-126">다음 표에서는 패키지를 제외한 연결 그룹 자체를 정의 하는 XML 파일의 매개 변수에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fee7-127">필드</span><span class="sxs-lookup"><span data-stu-id="1fee7-127">Field</span></span></th>
<th align="left"><span data-ttu-id="1fee7-128">설명</span><span class="sxs-lookup"><span data-stu-id="1fee7-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-129">스키마 이름</span><span class="sxs-lookup"><span data-stu-id="1fee7-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-130">스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="1fee7-131">App-v 5.0 SP3에서 시작 가능 </strong> :이 표에 설명 된 새로운 "선택적 패키지" 및 "모든 버전 사용" 기능을 사용 하려는 경우 XML 파일에서 다음 스키마를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fee7-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="1fee7-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-133">이 연결 그룹의 고유 GUID 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="1fee7-134">연결 그룹 상태는이 식별자와 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="1fee7-135">연결 그룹을 만들 때만이 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="1fee7-136">다음을 입력 하 여 새 GUID를 만들 수 있습니다 <strong>[Guid]::NewGuid()</strong> .</span><span class="sxs-lookup"><span data-stu-id="1fee7-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-137">#</span><span class="sxs-lookup"><span data-stu-id="1fee7-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-138">이 버전의 연결 그룹에 대 한 버전 GUID 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="1fee7-139">연결 그룹을 업데이트 하는 경우 (예: 새 패키지를 추가 하거나 업데이트 하는 경우) 새 버전을 반영 하도록 버전 GUID를 업데이트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fee7-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="1fee7-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-141">연결 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-142">Priority</span><span class="sxs-lookup"><span data-stu-id="1fee7-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-143">연결 그룹의 선택적 우선 순위 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="1fee7-144">"0" </strong> - 은 가장 높은 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="1fee7-145">우선 순위가 필요 하지만 구성 되지 않은 경우에는 사용할 올바른 연결 그룹을 확인할 수 없기 때문에 패키지가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="1fee7-146">연결 그룹의 패키지를 정의 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fee7-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="1fee7-147">&lt; &gt; 연결 그룹 XML 파일의 패키지 섹션에서 다음 표에 설명 된 대로 각 패키지의 고유한 패키지 식별자 및 버전 식별자를 지정 하 여 연결 그룹의 구성원 패키지를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="1fee7-148">목록의 첫 번째 패키지는 우선 순위가 가장 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fee7-149">필드</span><span class="sxs-lookup"><span data-stu-id="1fee7-149">Field</span></span></th>
<th align="left"><span data-ttu-id="1fee7-150">설명</span><span class="sxs-lookup"><span data-stu-id="1fee7-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-151">PackageId</span><span class="sxs-lookup"><span data-stu-id="1fee7-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-152">이 패키지의 고유 GUID 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="1fee7-153">이 GUID는 최신 버전의 패키지를 게시할 때 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fee7-154">#</span><span class="sxs-lookup"><span data-stu-id="1fee7-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-155">패키지 버전의 고유 GUID 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="1fee7-156">App-v 5.0 SP3에서 시작 가능 </strong> : <strong> 패키지 버전에 "\*"를 지정 하면 </strong> 사용 가능한 최신 패키지 버전의 GUID가 동적으로 삽입 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-157">IsOptional</span><span class="sxs-lookup"><span data-stu-id="1fee7-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="1fee7-158">앱-V 5.0 SP3 </strong> : 연결 그룹 내에서 패키지를 선택적으로 만들 수 있도록 하는 매개 변수를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="1fee7-159">유효한 항목은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="1fee7-160">"true" </strong> – 연결 그룹의 패키지가 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="1fee7-161">"false" </strong> – 연결 그룹에 패키지가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="1fee7-162"><a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)">연결 그룹에서 선택적 패키지를 사용 하는 방법에 대해 알아봅니다 </a> .</span><span class="sxs-lookup"><span data-stu-id="1fee7-162">See <a href="how-to-use-optional-packages-in-connection-groups.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="1fee7-163">App-v 5.0 SP3 예제 연결 그룹 XML 파일</span><span class="sxs-lookup"><span data-stu-id="1fee7-163">App-V 5.0 SP3 example connection group XML file</span></span>

<span data-ttu-id="1fee7-164">다음 예제 연결 그룹 XML 파일은 이전 표의 필드 예를 보여 주고 App-v 5.0 SP3 용 새 항목을 강조 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup 
   xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"  
   Priority="0"  
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="*"
         IsOptional=”true”
      />    
     <appv:Package
        PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
        VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
        IsOptional="false"
     />  
   </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="1fee7-165">앱-V 5.0 ~ App-v 5.0 SP2 연결 그룹 XML 파일 예</span><span class="sxs-lookup"><span data-stu-id="1fee7-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="1fee7-166">다음 예제 연결 그룹 XML 파일은 앱-V 5.0 SP2를 통해 App-v 5.0에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="1fee7-167">앞의 표에는 필드의 예가 표시 되지만 App-v 5.0 SP3에 대해 위에서 설명한 변경 사항은 제외 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16"?>
<appv:AppConnectionGroup
   xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
   AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
   VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
   Priority="0"
   DisplayName="Sample Connection Group">
   <appv:Packages>
      <appv:Package``      
         PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
         VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
      />
      <appv:Package
         PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
         VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      />
   </appv:Packages>
</appv:AppConnectionGroup
 ```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="1fee7-168">연결 그룹의 패키지 우선 순위 구성</span><span class="sxs-lookup"><span data-stu-id="1fee7-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="1fee7-169">패키지 우선 순위는 패키지 목록 순서를 사용 하 여 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="1fee7-170">문서의 첫 번째 패키지는 우선 순위가 가장 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="1fee7-171">목록의 후속 패키지에는 우선 순위가 내림차순으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="1fee7-172">패키지 우선 순위는 가상 환경 초기화 중에 불가피 한 리소스 충돌의 해상도입니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="1fee7-173">예를 들어 동일한 가상 환경에서 여는 두 패키지가 동일한 레지스트리 DWORD 값을 정의 하는 경우 우선 순위가 가장 높은 패키지가 설정 된 값을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="1fee7-174">연결 그룹 파일을 사용 하 여 다음 방법을 사용 하 여 각 연결 그룹을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="1fee7-175">연결 그룹에 대 한 런타임 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-175">Specify runtime priorities for connection groups.</span></span>

    <span data-ttu-id="1fee7-176">**참고**  우선 순위는 패키지가 둘 이상의 연결 그룹과 연결 된 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-176">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="1fee7-177">연결 그룹 내에서 패키지 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-177">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="1fee7-178">실행 중인 가상 응용 프로그램이 Microsoft Windows 탐색기와 같은 네이티브 응용 프로그램 요청에서 시작 되는 경우 priority 필드가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-178">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="1fee7-179">App-v 클라이언트는 우선 순위를 사용 하 여 응용 프로그램을 실행할 연결 그룹 가상 환경을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-179">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="1fee7-180">이 문제는 가상 응용 프로그램이 여러 연결 그룹에 속해 있는 경우에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-180">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="1fee7-181">다른 가상 응용 프로그램을 사용 하 여 가상 응용 프로그램을 열면 원래 가상 응용 프로그램의 가상 환경이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-181">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="1fee7-182">이 경우 우선 순위 필드는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-182">The priority field is not used in this case.</span></span>

**<span data-ttu-id="1fee7-183">예:</span><span class="sxs-lookup"><span data-stu-id="1fee7-183">Example:</span></span>**

<span data-ttu-id="1fee7-184">Microsoft Outlook이 가상 환경 **XYZ**에서 실행 되 고 있는 가상 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="1fee7-184">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="1fee7-185">연결 된 microsoft word 문서를 열면 가상화 된 Microsoft word의 연결 그룹 또는 런타임 우선 순위에 관계 없이 가상 환경 **XYZ**에서 microsoft word가 열립니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-185">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="1fee7-186">지원 되는 가상 응용 프로그램 연결 구성</span><span class="sxs-lookup"><span data-stu-id="1fee7-186">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fee7-187">구성</span><span class="sxs-lookup"><span data-stu-id="1fee7-187">Configuration</span></span></th>
<th align="left"><span data-ttu-id="1fee7-188">예제 시나리오</span><span class="sxs-lookup"><span data-stu-id="1fee7-188">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-189">대.</span><span class="sxs-lookup"><span data-stu-id="1fee7-189">An.</span></span> <span data-ttu-id="1fee7-190">exe 파일 및 플러그 인 (.dll)</span><span class="sxs-lookup"><span data-stu-id="1fee7-190">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1fee7-191">Microsoft Office를 모든 사용자에 게 배포 하지만 Microsoft Excel 플러그 인을 사용자의 하위 집합에만 배포 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-191">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="1fee7-192">적절 한 사용자에 대 한 연결 그룹을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-192">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="1fee7-193">필요에 따라 각 패키지를 개별적으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-193">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fee7-194">대.</span><span class="sxs-lookup"><span data-stu-id="1fee7-194">An.</span></span> <span data-ttu-id="1fee7-195">exe 파일 및 미들웨어 응용 프로그램</span><span class="sxs-lookup"><span data-stu-id="1fee7-195">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1fee7-196">응용 프로그램에 미들웨어 응용 프로그램이 나 모두 동일한 미들웨어 런타임 버전에 의존 하는 여러 응용 프로그램이 필요한 경우</span><span class="sxs-lookup"><span data-stu-id="1fee7-196">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="1fee7-197">하나 이상의 응용 프로그램이 필요한 모든 컴퓨터는 응용 프로그램 및 미들웨어 응용 프로그램 런타임과 연결 그룹을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-197">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="1fee7-198">필요에 따라 여러 미들웨어 응용 프로그램을 단일 연결 그룹으로 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-198">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1fee7-199">예</span><span class="sxs-lookup"><span data-stu-id="1fee7-199">Example</span></span></th>
<th align="left"><span data-ttu-id="1fee7-200">예제 설명</span><span class="sxs-lookup"><span data-stu-id="1fee7-200">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-201">재무 디비전에 대 한 가상 응용 프로그램 연결 그룹</span><span class="sxs-lookup"><span data-stu-id="1fee7-201">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1fee7-202">미들웨어 애플리케이션 1</span><span class="sxs-lookup"><span data-stu-id="1fee7-202">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="1fee7-203">미들웨어 애플리케이션 2</span><span class="sxs-lookup"><span data-stu-id="1fee7-203">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="1fee7-204">미들웨어 애플리케이션 3</span><span class="sxs-lookup"><span data-stu-id="1fee7-204">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="1fee7-205">미들웨어 응용 프로그램 런타임</span><span class="sxs-lookup"><span data-stu-id="1fee7-205">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1fee7-206">HR 디비전에 대 한 가상 응용 프로그램 연결 그룹</span><span class="sxs-lookup"><span data-stu-id="1fee7-206">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1fee7-207">미들웨어 애플리케이션 5</span><span class="sxs-lookup"><span data-stu-id="1fee7-207">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="1fee7-208">미들웨어 애플리케이션 6</span><span class="sxs-lookup"><span data-stu-id="1fee7-208">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="1fee7-209">미들웨어 응용 프로그램 런타임</span><span class="sxs-lookup"><span data-stu-id="1fee7-209">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1fee7-210">대.</span><span class="sxs-lookup"><span data-stu-id="1fee7-210">An.</span></span> <span data-ttu-id="1fee7-211">exe 파일 및 .exe 파일</span><span class="sxs-lookup"><span data-stu-id="1fee7-211">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="1fee7-212">다른 응용 프로그램에 의존 하는 응용 프로그램이 있고 운영 효율성, 라이선스 제한 또는 출시 시간 표시 막대에 대해 패키지를 유지 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="1fee7-212">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="1fee7-213">예:</span><span class="sxs-lookup"><span data-stu-id="1fee7-213">Example:</span></span></strong></p>
<p><span data-ttu-id="1fee7-214">Microsoft Lync 2010를 배포 하는 경우 다음 세 가지 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-214">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="1fee7-215">Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="1fee7-215">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="1fee7-216">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="1fee7-216">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="1fee7-217">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="1fee7-217">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="1fee7-218">다음 연결 그룹을 사용 하 여 배포를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-218">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="1fee7-219">Microsoft Office2010 및 Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="1fee7-219">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="1fee7-220">Microsoft Office2010 및 Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="1fee7-220">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="1fee7-221">배포가 완료 되 면 하나의 새 Microsoft Office2010 + Microsoft Lync2010 패키지를 만들거나, 별도의 패키지로 유지 하 고 유지 관리 하 고, 연결 그룹을 사용 하 여 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fee7-221">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="1fee7-222">관련 항목</span><span class="sxs-lookup"><span data-stu-id="1fee7-222">Related topics</span></span>


[<span data-ttu-id="1fee7-223">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="1fee7-223">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





