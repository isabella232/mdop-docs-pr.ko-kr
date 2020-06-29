---
title: MED-V 설치 파일에 대한 명령줄 옵션
description: MED-V 설치 파일에 대한 명령줄 옵션
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826468"
---
# <span data-ttu-id="751a4-103">MED-V 설치 파일에 대한 명령줄 옵션</span><span class="sxs-lookup"><span data-stu-id="751a4-103">Command-Line Options for MED-V Installation Files</span></span>


<span data-ttu-id="751a4-104">Microsoft Enterprise 데스크톱 가상화 (MED-V) 2.0을 설치 하거나 제거할 때 명령 프롬프트에서 설치 파일을 실행 하는 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-104">When you install or uninstall Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="751a4-105">이 섹션에서는 명령 프롬프트에 MED-V를 설치 하거나 제거할 때 지정할 수 있는 다양 한 옵션에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-105">This section describes different options that you can specify when you install or uninstall MED-V at the command prompt.</span></span>

### <span data-ttu-id="751a4-106">명령줄 인수</span><span class="sxs-lookup"><span data-stu-id="751a4-106">Command-Line Arguments</span></span>

<span data-ttu-id="751a4-107">다음 명령줄 인수를 각 MED-V 설치 파일과 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-107">You can use the following command-line arguments together with their respective MED-V installation files.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="751a4-108">설치 파일</span><span class="sxs-lookup"><span data-stu-id="751a4-108">Installation File</span></span></th>
<th align="left"><span data-ttu-id="751a4-109">인수</span><span class="sxs-lookup"><span data-stu-id="751a4-109">Argument</span></span></th>
<th align="left"><span data-ttu-id="751a4-110">허용 값</span><span class="sxs-lookup"><span data-stu-id="751a4-110">Accepted Values</span></span></th>
<th align="left"><span data-ttu-id="751a4-111">형식</span><span class="sxs-lookup"><span data-stu-id="751a4-111">Type</span></span></th>
<th align="left"><span data-ttu-id="751a4-112">설명</span><span class="sxs-lookup"><span data-stu-id="751a4-112">Description</span></span></th>
<th align="left"><span data-ttu-id="751a4-113">Default</span><span class="sxs-lookup"><span data-stu-id="751a4-113">Default</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="751a4-114">호스트 에이전트</span><span class="sxs-lookup"><span data-stu-id="751a4-114">Host Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-115">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="751a4-115">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-116">&lt;설치 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="751a4-116">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-117">설치</span><span class="sxs-lookup"><span data-stu-id="751a4-117">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-118">설치 된 디렉터리 변경</span><span class="sxs-lookup"><span data-stu-id="751a4-118">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-119">설치 Files\Microsoft 엔터프라이즈 데스크톱 가상화 프로그램으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-119">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="751a4-120">MED-V 작업 영역 포장기</span><span class="sxs-lookup"><span data-stu-id="751a4-120">MED-V Workspace Packager</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-121">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="751a4-121">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-122">&lt;설치 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="751a4-122">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-123">설치</span><span class="sxs-lookup"><span data-stu-id="751a4-123">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-124">설치 된 디렉터리 변경</span><span class="sxs-lookup"><span data-stu-id="751a4-124">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-125">설치 Files\Microsoft 엔터프라이즈 데스크톱 가상화 프로그램으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-125">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="751a4-126">MED-V 작업 영역</span><span class="sxs-lookup"><span data-stu-id="751a4-126">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-127">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="751a4-127">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-128">&lt;설치 경로&gt;</span><span class="sxs-lookup"><span data-stu-id="751a4-128">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-129">설치</span><span class="sxs-lookup"><span data-stu-id="751a4-129">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-130">설치 된 디렉터리 변경</span><span class="sxs-lookup"><span data-stu-id="751a4-130">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-131">ProgramData\Microsoft\Medv\Workspace.로 이동 하는 설치</span><span class="sxs-lookup"><span data-stu-id="751a4-131">Installation goes to ProgramData\Microsoft\Medv\Workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="751a4-132">MED-V 작업 영역</span><span class="sxs-lookup"><span data-stu-id="751a4-132">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-133">VHD 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="751a4-133">OVERWRITE VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-134">0 또는 1</span><span class="sxs-lookup"><span data-stu-id="751a4-134">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-135">설치</span><span class="sxs-lookup"><span data-stu-id="751a4-135">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-136">VHD가 있거나 (0) 기존 VHD를 덮어쓰는 경우 설치에 실패 합니다 (1).</span><span class="sxs-lookup"><span data-stu-id="751a4-136">Fail installation if VHD exists(0) or overwrite existing VHD(1).</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-137">덮어쓰기가 발생 하지 않으며 VHD (가상 하드 디스크)가 이미 있는 경우 설치가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-137">Overwrite does not occur and installation fails if a virtual hard disk (VHD) already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="751a4-138">MED-V 작업 영역</span><span class="sxs-lookup"><span data-stu-id="751a4-138">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-139">SUPPRESSMEDVLAUNCH</span><span class="sxs-lookup"><span data-stu-id="751a4-139">SUPPRESSMEDVLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-140">0 또는 1</span><span class="sxs-lookup"><span data-stu-id="751a4-140">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-141">설치</span><span class="sxs-lookup"><span data-stu-id="751a4-141">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-142">MED-V 작업 영역을 설치한 후 시작 (0) 또는 시작 안 함 (1) MED-V-V</span><span class="sxs-lookup"><span data-stu-id="751a4-142">Start(0) or do not start(1) MED-V after MED-V workspace is installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-143">MED-V 작업 영역이 UI (사용자 인터페이스)와 함께 설치 된 경우에는 완료 페이지의 확인란이 MED-V를 <strong> </strong> 시작할지 여부를 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-143">If the MED-V workspace was installed with the user interface (UI), a check box on the <strong>Finish</strong> page controls whether to start MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="751a4-144">MED-V 작업 영역</span><span class="sxs-lookup"><span data-stu-id="751a4-144">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-145">DELETEDIFFDISKS</span><span class="sxs-lookup"><span data-stu-id="751a4-145">DELETEDIFFDISKS</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-146">0 또는 1</span><span class="sxs-lookup"><span data-stu-id="751a4-146">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-147">제거</span><span class="sxs-lookup"><span data-stu-id="751a4-147">Uninstallation</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-148">저장 (0) 또는 delete (1) ' MED-V에서 생성 된 Vhd</span><span class="sxs-lookup"><span data-stu-id="751a4-148">Keep(0) or delete(1) VHDs created by MED-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="751a4-149">Vhd는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-149">No VHDs are deleted.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="751a4-150">명령줄 인수의 예</span><span class="sxs-lookup"><span data-stu-id="751a4-150">Examples of Command-Line Arguments</span></span>

<span data-ttu-id="751a4-151">다음 예제에서는 MED-V 작업 영역 포장기에서 만든 MED-V 작업 영역을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-151">The following example installs the MED-V workspace created by the MED-V workspace Packager.</span></span> <span data-ttu-id="751a4-152">설치 파일은 임시 디렉터리에 로그 파일을 만들고 자동 모드에서 설치 파일을 실행 하지만 완료 시 MED-V 호스트 에이전트를 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-152">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode, but does not start the MED-V Host Agent on completion.</span></span> <span data-ttu-id="751a4-153">설치 파일은 동일한 이름을 가진 이전 설치에서 남겨진 모든 VHD를 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-153">The installation file overwrites any VHD left behind by a previous installation that has the same name.</span></span>

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

<span data-ttu-id="751a4-154">다음 예제에서는 이전에 설치 된 MED-V 작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-154">The following example uninstalls the MED-V workspace that was previously installed.</span></span> <span data-ttu-id="751a4-155">설치 파일은 임시 디렉터리에 로그 파일을 만들고 자동 모드에서 설치 파일을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-155">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode.</span></span> <span data-ttu-id="751a4-156">설치 파일은 파일 시스템에서 남아 있는 가상 하드 디스크 파일을 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="751a4-156">The installation file deletes any remaining virtual hard disk files from the file system.</span></span>

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## <span data-ttu-id="751a4-157">관련 항목</span><span class="sxs-lookup"><span data-stu-id="751a4-157">Related topics</span></span>


[<span data-ttu-id="751a4-158">MED-V 구성 요소 배포</span><span class="sxs-lookup"><span data-stu-id="751a4-158">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

[<span data-ttu-id="751a4-159">MED-V에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="751a4-159">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





