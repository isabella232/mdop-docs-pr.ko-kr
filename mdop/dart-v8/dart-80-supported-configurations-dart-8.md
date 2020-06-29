---
title: DaRT 8.0 지원되는 구성
description: DaRT 8.0 지원되는 구성
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823928"
---
# <span data-ttu-id="79f15-103">DaRT 8.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="79f15-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="79f15-104">이 항목에서는 환경에서 Microsoft 진단 및 복구 도구 집합 (DaRT) 8.0을 설치 하 고 실행 하는 데 필요한 필수 구성 요구 사항 및 지원 되는 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="79f15-105">운영 체제 요구 사항과 DaRT 8.0를 실행 하는 데 필요한 시스템 요구 사항이 지정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="79f15-106">DaRT 복구 이미지를 만들기 위해 고려해 야 하는 필수 구성 요소에 대 한 자세한 내용은 [dart 8.0 복구 이미지 만들기 계획 수립](planning-to-create-the-dart-80-recovery-image-dart-8.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79f15-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="79f15-107">이후 릴리스에 적용 되는 지원 되는 구성에 대해서는 해당 릴리스에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79f15-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="79f15-108">두 가지 방법 중 하나로 DaRT를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="79f15-109">모든 기능을 IT 관리자 컴퓨터에 설치 하 여 DaRT 실행과 관련 된 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="79f15-110">또는 관리자 컴퓨터에 복구 이미지를 만드는 DaRT 기능만 설치한 다음 헬프 데스크 컴퓨터에서 DaRT (DaRT 원격 연결 뷰어)를 실행 하는 데 사용 되는 기능을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="79f15-111">DaRT 8.0 필수 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="79f15-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="79f15-112">DaRT를 설치 하기 전에 다음 선행 조건이 충족 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="79f15-113">관리자 컴퓨터 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="79f15-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="79f15-114">다음 표에는 DaRT 8.0 및 모든 DaRT 도구를 설치할 때 관리자 컴퓨터의 설치 필수 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79f15-115">요소일</span><span class="sxs-lookup"><span data-stu-id="79f15-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="79f15-116">세부 정보</span><span class="sxs-lookup"><span data-stu-id="79f15-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79f15-117">Windows ADK (평가 및 개발 키트)</span><span class="sxs-lookup"><span data-stu-id="79f15-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-118">DaRT 복구 이미지 마법사에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="79f15-119">Windows 이미지를 사용자 지정, 배포 및 서비스 하는 데 사용 되며 windows 사전 설치 환경 (Windows PE)이 포함 된 배포 도구가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="79f15-120">원격 연결 뷰어 및/또는 충돌 분석기만 설치 하는 경우에는 ADK가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="79f15-121">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="79f15-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-122">DaRT 복구 이미지 마법사에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79f15-123">Windows 개발 키트 또는 소프트웨어 개발 키트 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="79f15-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-124">충돌 분석기에는 Windows 드라이버 키트의 Windows 8 디버깅 도구가 있어야 메모리 덤프 파일을 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="79f15-125">Windows 8 64-bit ISO 이미지</span><span class="sxs-lookup"><span data-stu-id="79f15-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-126">DaRT에는 Windows 8 미디어의 windows RE (Windows 복구 환경) 이미지가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="79f15-127">만들려는 DaRT 복구 이미지 형식에 따라 32 비트 또는 64 비트 버전의 Windows 8을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="79f15-128">환경에서 두 시스템 유형을 모두 지 원하는 경우 두 가지 버전의 Windows 8을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="79f15-129">지원 센터 컴퓨터 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="79f15-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="79f15-130">다음 표에는 DaRT 8.0 원격 연결 뷰어를 실행 하는 경우 지원 센터 컴퓨터용 설치 필수 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79f15-131">요소일</span><span class="sxs-lookup"><span data-stu-id="79f15-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="79f15-132">세부 정보</span><span class="sxs-lookup"><span data-stu-id="79f15-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79f15-133">DaRT 8.0 원격 연결 뷰어</span><span class="sxs-lookup"><span data-stu-id="79f15-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-134">Windows 8 운영 체제에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="79f15-135">네트워크 프레임 워크 4.5</span><span class="sxs-lookup"><span data-stu-id="79f15-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-136">DaRT 복구 이미지 마법사에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79f15-137">Windows용 디버깅 도구</span><span class="sxs-lookup"><span data-stu-id="79f15-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79f15-138">충돌 분석기 도구를 설치 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="79f15-139">최종 사용자 컴퓨터 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="79f15-139">End-user computer prerequisites</span></span>

<span data-ttu-id="79f15-140">Windows 8 운영 체제 이외의 최종 사용자 컴퓨터에 설치 해야 하는 필수 소프트웨어는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="79f15-141">DaRT 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="79f15-142">관리자 컴퓨터 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-142">Administrator computer system requirements</span></span>

<span data-ttu-id="79f15-143">다음 표에는 DaRT 관리자 컴퓨터 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="79f15-144">**참고**  관리자 컴퓨터에 설치 하려는 추가 도구에 충분 한 공간을 할당 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="79f15-145">**참고**  Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="79f15-146">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79f15-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="79f15-147">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79f15-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="79f15-148">운영 체제</span><span class="sxs-lookup"><span data-stu-id="79f15-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="79f15-149">버전</span><span class="sxs-lookup"><span data-stu-id="79f15-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="79f15-150">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="79f15-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="79f15-151">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="79f15-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="79f15-152">운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="79f15-153">DaRT를 실행 하기 위한 RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f15-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="79f15-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-155">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-156">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-157">64비트</span><span class="sxs-lookup"><span data-stu-id="79f15-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-158">2GB</span><span class="sxs-lookup"><span data-stu-id="79f15-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-159">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f15-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="79f15-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-161">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-162">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-163">32비트</span><span class="sxs-lookup"><span data-stu-id="79f15-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-164">1GB</span><span class="sxs-lookup"><span data-stu-id="79f15-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-165">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f15-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79f15-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-167">표준, 엔터프라이즈, 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="79f15-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-168">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-169">64비트</span><span class="sxs-lookup"><span data-stu-id="79f15-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-170">512 MB</span><span class="sxs-lookup"><span data-stu-id="79f15-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-171">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="79f15-172">DaRT 지원 센터 컴퓨터 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="79f15-173">지원 센터에서 원격으로 컴퓨터 문제를 해결할 수 있도록 허용 하는 경우 지원 센터 컴퓨터에 원격 연결 뷰어가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="79f15-174">선택적으로 지원 센터 컴퓨터에 크래시 분석기 도구를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="79f15-175">DaRT 8.0는 DaRT 7.0 또는 DaRT 8.0 원격 연결 뷰어를 사용 하 여 지원 센터 근로자가 DaRT 8.0 컴퓨터에 연결할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="79f15-176">DaRT 7.0 원격 연결 뷰어에는 Windows 7 운영 체제가 필요 하지만 DaRT 8.0 원격 연결 뷰어에는 Windows 8이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="79f15-177">DaRT 8.0 원격 연결 뷰어와 기타 모든 DaRT 8.0 도구는 Windows 8을 실행 하는 컴퓨터에만 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="79f15-178">다음 표에는 DaRT 헬프 데스크 컴퓨터 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="79f15-179">운영 체제</span><span class="sxs-lookup"><span data-stu-id="79f15-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="79f15-180">버전</span><span class="sxs-lookup"><span data-stu-id="79f15-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="79f15-181">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="79f15-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="79f15-182">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="79f15-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="79f15-183">운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="79f15-184">DaRT를 실행 하기 위한 RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f15-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="79f15-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-186">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-187">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-188">64비트</span><span class="sxs-lookup"><span data-stu-id="79f15-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-189">2GB</span><span class="sxs-lookup"><span data-stu-id="79f15-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-190">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f15-191">Windows8 (원격 연결 뷰어 8.0에만 해당)</span><span class="sxs-lookup"><span data-stu-id="79f15-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-192">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-193">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-194">32비트</span><span class="sxs-lookup"><span data-stu-id="79f15-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-195">1GB</span><span class="sxs-lookup"><span data-stu-id="79f15-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-196">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f15-197">Windows 7 (원격 연결 뷰어 7.0에만 해당)</span><span class="sxs-lookup"><span data-stu-id="79f15-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-198">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-199">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="79f15-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-200">64 비트 또는 32 비트</span><span class="sxs-lookup"><span data-stu-id="79f15-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-201">1GB</span><span class="sxs-lookup"><span data-stu-id="79f15-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-202">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f15-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79f15-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-204">표준, 엔터프라이즈, 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="79f15-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-205">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-206">64비트</span><span class="sxs-lookup"><span data-stu-id="79f15-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-207">51</span><span class="sxs-lookup"><span data-stu-id="79f15-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-208">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="79f15-209">DaRT에는 최종 사용자 컴퓨터에 대해 다음과 같은 최소 하드웨어 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="79f15-210">Cd, dvd 또는 USB를 사용 하 여 엔터프라이즈에서 DaRT를 배포 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="79f15-211">CD 또는 DVD, USB 플래시 드라이브 또는 원격 또는 복구 파티션에서 컴퓨터를 시작 하기 위한 BIOS 지원입니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="79f15-212">DaRT 최종 사용자 컴퓨터 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="79f15-213">DaRT의 진단 및 복구 도구 집합 창에서 최종 사용자 컴퓨터는 다음 운영 체제 중에서 DaRT에 사용할 수 있는 지정 된 시스템 메모리 크기를 함께 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f15-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="79f15-214">운영 체제</span><span class="sxs-lookup"><span data-stu-id="79f15-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="79f15-215">버전</span><span class="sxs-lookup"><span data-stu-id="79f15-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="79f15-216">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="79f15-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="79f15-217">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="79f15-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="79f15-218">운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="79f15-219">RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="79f15-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f15-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="79f15-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-221">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-222">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-223">64비트</span><span class="sxs-lookup"><span data-stu-id="79f15-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-224">2GB</span><span class="sxs-lookup"><span data-stu-id="79f15-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-225">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79f15-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="79f15-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-227">모든 버전</span><span class="sxs-lookup"><span data-stu-id="79f15-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-228">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-229">32비트</span><span class="sxs-lookup"><span data-stu-id="79f15-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-230">1GB</span><span class="sxs-lookup"><span data-stu-id="79f15-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-231">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79f15-232">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79f15-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-233">표준, 엔터프라이즈, 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="79f15-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-234">해당 없음</span><span class="sxs-lookup"><span data-stu-id="79f15-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-235">64비트</span><span class="sxs-lookup"><span data-stu-id="79f15-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-236">512 MB</span><span class="sxs-lookup"><span data-stu-id="79f15-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="79f15-237">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="79f15-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="79f15-238">관련 항목</span><span class="sxs-lookup"><span data-stu-id="79f15-238">Related topics</span></span>


[<span data-ttu-id="79f15-239">DaRT 8.0 배포 계획</span><span class="sxs-lookup"><span data-stu-id="79f15-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





