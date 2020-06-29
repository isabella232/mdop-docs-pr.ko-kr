---
title: DaRT 10 지원되는 구성
description: DaRT 10 지원되는 구성
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813137"
---
# <span data-ttu-id="fbe3b-103">DaRT 10 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="fbe3b-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="fbe3b-104">이 항목에서는 환경에서 Microsoft 진단 및 복구 도구 집합 (DaRT) 10을 설치 하 고 실행 하는 데 필요한 필수 구성 요구 사항 및 지원 되는 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="fbe3b-105">운영 체제 요구 사항과 DaRT 10을 실행 하는 데 필요한 시스템 요구 사항이 모두 지정 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="fbe3b-106">DaRT 복구 이미지를 만들기 위해 고려해 야 하는 필수 구성 요소에 대 한 자세한 내용은 [dart 10 복구 이미지 만들기 계획 수립](planning-to-create-the-dart-10-recovery-image.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="fbe3b-107">이후 릴리스에 적용 되는 지원 되는 구성에 대해서는 해당 릴리스에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="fbe3b-108">두 가지 방법 중 하나로 DaRT를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="fbe3b-109">모든 기능을 IT 관리자 컴퓨터에 설치 하 여 DaRT 실행과 관련 된 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="fbe3b-110">또는 관리자 컴퓨터에 복구 이미지를 만드는 DaRT 기능만 설치한 다음 헬프 데스크 컴퓨터에서 DaRT (DaRT 원격 연결 뷰어)를 실행 하는 데 사용 되는 기능을 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="fbe3b-111">DaRT 10 필수 소프트웨어</span><span class="sxs-lookup"><span data-stu-id="fbe3b-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="fbe3b-112">DaRT를 설치 하기 전에 다음 선행 조건이 충족 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="fbe3b-113">관리자 컴퓨터 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="fbe3b-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="fbe3b-114">다음 표에는 DaRT 10 및 모든 DaRT 도구를 설치 하는 경우 관리자 컴퓨터의 설치 필수 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fbe3b-115">요소일</span><span class="sxs-lookup"><span data-stu-id="fbe3b-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-116">세부 정보</span><span class="sxs-lookup"><span data-stu-id="fbe3b-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fbe3b-117">Windows ADK (평가 및 개발 키트)</span><span class="sxs-lookup"><span data-stu-id="fbe3b-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-118">DaRT 복구 이미지 마법사에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="fbe3b-119">Windows 이미지를 사용자 지정, 배포 및 서비스 하는 데 사용 되며 windows 사전 설치 환경 (Windows PE)이 포함 된 배포 도구가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="fbe3b-120">원격 연결 뷰어 및/또는 충돌 분석기만 설치 하는 경우에는 ADK가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fbe3b-121">Windows 개발 키트 또는 소프트웨어 개발 키트 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="fbe3b-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-122">충돌 분석기에는 Windows 드라이버 키트의 Windows 10 디버깅 도구가 있어야 메모리 덤프 파일을 분석할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fbe3b-123">Windows 10 64 비트 또는 32 비트 ISO 이미지</span><span class="sxs-lookup"><span data-stu-id="fbe3b-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-124">DaRT에는 Windows 10 미디어의 windows RE (Windows 복구 환경) 이미지가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="fbe3b-125">만들려는 DaRT 복구 이미지 형식에 따라 32 비트 또는 64 비트 버전의 Windows 10을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="fbe3b-126">환경에서 두 시스템 유형을 모두 지 원하는 경우 두 버전의 Windows 10을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fbe3b-127">지원 센터 컴퓨터 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="fbe3b-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="fbe3b-128">다음 표에는 DaRT 10 원격 연결 뷰어를 실행 하는 경우 지원 센터 컴퓨터용 설치 필수 구성 요소가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fbe3b-129">요소일</span><span class="sxs-lookup"><span data-stu-id="fbe3b-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-130">세부 정보</span><span class="sxs-lookup"><span data-stu-id="fbe3b-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fbe3b-131">DaRT 10 원격 연결 뷰어</span><span class="sxs-lookup"><span data-stu-id="fbe3b-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-132">Windows 10 운영 체제에 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fbe3b-133">Windows용 디버깅 도구</span><span class="sxs-lookup"><span data-stu-id="fbe3b-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-134">충돌 분석기 도구를 설치 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fbe3b-135">최종 사용자 컴퓨터 필수 구성 요소</span><span class="sxs-lookup"><span data-stu-id="fbe3b-135">End-user computer prerequisites</span></span>

<span data-ttu-id="fbe3b-136">Windows 10 운영 체제 이외의 최종 사용자 컴퓨터에 설치 해야 하는 필수 소프트웨어는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="fbe3b-137">DaRT 10 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="fbe3b-138">관리자 컴퓨터 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-138">Administrator computer system requirements</span></span>

<span data-ttu-id="fbe3b-139">다음 표에는 DaRT 10 관리자 컴퓨터 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="fbe3b-140">**참고**  관리자 컴퓨터에 설치 하려는 추가 도구에 충분 한 공간을 할당 했는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="fbe3b-141">**참고**  Microsoft는 현재 서비스 팩 및 경우에 따라 바로 이전 서비스 팩을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="fbe3b-142">제품에 대 한 지원 시간 표시 막대를 찾으려면 [지원 되는 수명 주기 서비스 팩](https://go.microsoft.com/fwlink/p/?LinkId=31975)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="fbe3b-143">Microsoft 지원 기간 정책에 대 한 자세한 내용은 [Microsoft 지원 기간 지원 정책 FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="fbe3b-144">운영 체제</span><span class="sxs-lookup"><span data-stu-id="fbe3b-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-145">버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-146">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="fbe3b-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-147">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="fbe3b-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-148">운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-149">DaRT를 실행 하기 위한 RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbe3b-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fbe3b-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-151">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-152">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-153">64비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-154">2GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-155">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbe3b-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fbe3b-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-157">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-158">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-159">32비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-160">1GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-161">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="fbe3b-162">DaRT 지원 센터 컴퓨터 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="fbe3b-163">지원 센터에서 원격으로 컴퓨터 문제를 해결할 수 있도록 허용 하는 경우 지원 센터 컴퓨터에 원격 연결 뷰어가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="fbe3b-164">선택적으로 지원 센터 컴퓨터에 크래시 분석기 도구를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="fbe3b-165">DaRT 10 헬프 데스크 근로자는 DaRT 7.0, DaRT 8.0, DaRt 8.1 또는 DaRT 10 원격 연결 뷰어를 사용 하 여 DaRT 10 컴퓨터에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="fbe3b-166">Dart 7.0, DaRT 8.0 및 DaRt 8.1, 원격 연결 뷰어에는 각각 Windows 7, Windows 8 또는 Windows 8.1 운영 체제가 필요 하지만, DaRT 10 원격 연결 뷰어에는 Windows 10이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="fbe3b-167">DaRT 10 원격 연결 뷰어와 기타 모든 DaRT 10 도구는 Windows 10을 실행 하는 컴퓨터에만 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="fbe3b-168">다음 표에는 DaRT 헬프 데스크 컴퓨터 설치에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="fbe3b-169">운영 체제</span><span class="sxs-lookup"><span data-stu-id="fbe3b-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-170">버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-171">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="fbe3b-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-172">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="fbe3b-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-173">운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-174">DaRT를 실행 하기 위한 RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbe3b-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fbe3b-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-176">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-177">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-178">64비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-179">2GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-180">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbe3b-181">Windows10 (원격 연결 뷰어 10.0에만 해당)</span><span class="sxs-lookup"><span data-stu-id="fbe3b-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-182">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-183">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-184">32비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-185">1GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-186">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbe3b-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="fbe3b-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-188">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-189">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-190">64비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-191">2GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-192">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbe3b-193">Windows8 (원격 연결 뷰어 8.0에만 해당)</span><span class="sxs-lookup"><span data-stu-id="fbe3b-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-194">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-195">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-196">32비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-197">1GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-198">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbe3b-199">Windows 7 (원격 연결 뷰어 7.0에만 해당)</span><span class="sxs-lookup"><span data-stu-id="fbe3b-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-200">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-201">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="fbe3b-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-202">64 비트 또는 32 비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-203">1GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-204">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbe3b-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbe3b-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-206">표준, 엔터프라이즈, 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="fbe3b-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-207">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-208">64비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-209">2GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-210">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbe3b-211">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fbe3b-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-212">표준, 엔터프라이즈, 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="fbe3b-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-213">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-214">64비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-215">2GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-216">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fbe3b-217">DaRT에는 최종 사용자 컴퓨터에 대해 다음과 같은 최소 하드웨어 요구 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="fbe3b-218">Cd, dvd 또는 USB를 사용 하 여 엔터프라이즈에서 DaRT를 배포 하는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="fbe3b-219">CD 또는 DVD, USB 플래시 드라이브 또는 원격 또는 복구 파티션에서 컴퓨터를 시작 하기 위한 BIOS 지원입니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="fbe3b-220">DaRT 10 최종 사용자 컴퓨터 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="fbe3b-221">DaRT 10의 진단 및 복구 도구 집합 창에서는 최종 사용자 컴퓨터가 DaRT에 사용할 수 있는 지정 된 시스템 메모리 크기와 함께 다음 운영 체제 중 하나를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe3b-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="fbe3b-222">운영 체제</span><span class="sxs-lookup"><span data-stu-id="fbe3b-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-223">버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-224">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="fbe3b-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-225">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="fbe3b-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-226">운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="fbe3b-227">RAM 요구 사항</span><span class="sxs-lookup"><span data-stu-id="fbe3b-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fbe3b-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fbe3b-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-229">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-230">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-231">64비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-232">2GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-233">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fbe3b-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fbe3b-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-235">모든 버전</span><span class="sxs-lookup"><span data-stu-id="fbe3b-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-236">해당 없음</span><span class="sxs-lookup"><span data-stu-id="fbe3b-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-237">32비트</span><span class="sxs-lookup"><span data-stu-id="fbe3b-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-238">1GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fbe3b-239">1.5 GB</span><span class="sxs-lookup"><span data-stu-id="fbe3b-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fbe3b-240">관련 항목</span><span class="sxs-lookup"><span data-stu-id="fbe3b-240">Related topics</span></span>


[<span data-ttu-id="fbe3b-241">DaRT 10 배포 계획</span><span class="sxs-lookup"><span data-stu-id="fbe3b-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





