---
title: 연결 그룹 가상 환경 정보
description: 연결 그룹 가상 환경 정보
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814884"
---
# <span data-ttu-id="7c27a-103">연결 그룹 가상 환경 정보</span><span class="sxs-lookup"><span data-stu-id="7c27a-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="7c27a-104">이 항목의 내용:</span><span class="sxs-lookup"><span data-stu-id="7c27a-104">In this topic:</span></span>**

-   [<span data-ttu-id="7c27a-105">패키지 우선 순위를 결정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7c27a-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="7c27a-106">연결 그룹의 하나의 가상 디렉터리에 동일한 패키지 경로 병합</span><span class="sxs-lookup"><span data-stu-id="7c27a-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="7c27a-107">패키지 우선 순위를 결정 하는 방법</span><span class="sxs-lookup"><span data-stu-id="7c27a-107">How package priority is determined</span></span>


<span data-ttu-id="7c27a-108">가상 환경과 해당 현재 상태는 개별 패키지가 아닌 연결 그룹과 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="7c27a-109">연결 그룹에서 앱-V 패키지를 제거 하면 연결 그룹의 일부로 존재 하는 상태가 패키지와 함께 마이그레이션되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="7c27a-110">동일한 패키지가 두 개의 다른 연결 그룹에 속해 있는 경우 app-v에서 사용할 연결 그룹을 표시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="7c27a-111">예를 들어 연결 그룹에는 각각 동일한 레지스트리 DWORD 값을 정의 하는 두 개의 패키지가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="7c27a-112">사용 되는 연결 그룹은 **Appconnectiongroup** XML 문서 내에서 패키지가 표시 되는 순서에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="7c27a-113">첫 번째 패키지의 우선 순위가 가장 높습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="7c27a-114">두 번째 패키지의 우선 순위가 가장 높습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="7c27a-115">다음 예제 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c27a-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="7c27a-116">다음과 같이 첫 번째 및 세 번째 패키지에 동일한 DWORD 값 ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region)가 정의 되어 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="7c27a-117">패키지 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="7c27a-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="7c27a-118">패키지 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="7c27a-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="7c27a-119">Package 1이 먼저 표시 되므로 AppConnectionGroup의 가상 환경은 단일 DWORD 값이 5 (HKEY _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5)입니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="7c27a-120">즉, 패키지 1, 패키지 2 및 패키지 3의 가상 응용 프로그램이 HKEY \ _LOCAL \ _MACHINE에 대해 쿼리하면 5 값이 모두 표시 됨을 의미 합니다. \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="7c27a-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="7c27a-121">다른 가상 환경 리소스도 비슷하게 해결 되지만, 일반적인 경우는 레지스트리에서 충돌이 발생 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="7c27a-122">연결 그룹의 하나의 가상 디렉터리에 동일한 패키지 경로 병합</span><span class="sxs-lookup"><span data-stu-id="7c27a-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="7c27a-123">연결 그룹에 있는 둘 이상의 패키지에 동일한 디렉터리 경로가 포함 된 경우 경로가 연결 그룹 가상 환경 내의 단일 가상 디렉터리로 병합 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="7c27a-124">이러한 경로 병합을 통해 한 패키지의 응용 프로그램이 다른 패키지의 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="7c27a-125">연결 그룹에서 패키지를 제거 하면 제거 된 해당 패키지의 응용 프로그램이 연결 그룹의 나머지 패키지에 있는 파일에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="7c27a-126">앱이 연결 그룹에서 파일 이름을 찾는 순서는 연결 그룹 매니페스트 파일에 앱 V 패키지가 나열 되는 순서 대로 지정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="7c27a-127">다음 예제에서는 **패키지 a** 및 **패키지 B**의 연결 그룹에 있는 파일 이름 조회의 순서와 관계를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c27a-128">패키지 A</span><span class="sxs-lookup"><span data-stu-id="7c27a-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="7c27a-129">패키지 B</span><span class="sxs-lookup"><span data-stu-id="7c27a-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c27a-130">\ \ \</span><span class="sxs-lookup"><span data-stu-id="7c27a-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c27a-131">\ \ \</span><span class="sxs-lookup"><span data-stu-id="7c27a-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c27a-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="7c27a-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c27a-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="7c27a-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7c27a-134">위 예제에서 가상화 된 응용 프로그램이 특정 파일을 찾으려고 하면 먼저 패키지 A가 일치 하는 파일 경로를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="7c27a-135">일치 하는 경로를 찾을 수 없는 경우 다음 매핑 규칙을 사용 하 여 패키지 B를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="7c27a-136">두 응용 프로그램 패키지의 동일한 가상 폴더 계층 구조에 **test.txt** 이라는 파일이 있는 경우 첫 번째 일치 파일이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="7c27a-137">하나의 응용 프로그램 패키지의 가상 폴더 계층 구조에 **bar.txt** 이라는 이름의 파일이 있지만 다른 파일에는 없는 경우에는 일치 하는 첫 번째 파일이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c27a-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="7c27a-138">관련 항목</span><span class="sxs-lookup"><span data-stu-id="7c27a-138">Related topics</span></span>


[<span data-ttu-id="7c27a-139">연결 그룹 관리</span><span class="sxs-lookup"><span data-stu-id="7c27a-139">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





