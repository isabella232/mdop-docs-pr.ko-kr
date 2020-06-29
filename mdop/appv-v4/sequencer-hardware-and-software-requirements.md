---
title: Sequencer 하드웨어 및 소프트웨어 요구 사항
description: Sequencer 하드웨어 및 소프트웨어 요구 사항
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815533"
---
# <span data-ttu-id="2e31f-103">Sequencer 하드웨어 및 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2e31f-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="2e31f-104">이 항목에서는 Microsoft App-v (Application Virtualization) Sequencer를 실행 하는 컴퓨터에 대해 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="2e31f-105">시퀀서를 설치 하 고 각 응용 프로그램의 순서를 설정한 후에는 시퀀싱 된 컴퓨터에 클린 운영 체제 이미지를 복원 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="2e31f-106">다음 방법 중 하나를 사용 하 여 Sequencer를 실행 하는 컴퓨터를 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="2e31f-107">하드 드라이브를 다시 포맷 하 고 운영 체제를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="2e31f-108">다른 디스크 이미징 소프트웨어를 사용 하 여 Sequencer 이미지를 실행 하는 컴퓨터의 하드 드라이브를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="2e31f-109">다음 목록에는 App-v 시퀀서를 실행 하기 위한 권장 하드웨어 요구 사항이 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="2e31f-110">하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2e31f-110">Hardware Requirements</span></span>

-   <span data-ttu-id="2e31f-111">프로세서-Intel 펜티엄 III, 1Ghz (32 비트 또는 64 비트).</span><span class="sxs-lookup"><span data-stu-id="2e31f-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="2e31f-112">시퀀싱 프로세스는 단일 스레드 프로세스 이며 이중 프로세서를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="2e31f-113">메모리-1GB 이상, 2gb 권장.</span><span class="sxs-lookup"><span data-stu-id="2e31f-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="2e31f-114">하드 디스크-최소 15gb의 하드 디스크 공간을 사용 하는 40gb (하드 디스크 공간)</span><span class="sxs-lookup"><span data-stu-id="2e31f-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="2e31f-115">시퀀싱 하는 응용 프로그램에 필요한 하드 디스크 공간에는 세 배 이상 있는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="2e31f-116">**참고**  시퀀싱에는 디스크 사용량이 많이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="2e31f-117">빠른 디스크 속도를 통해 시퀀싱 시간을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="2e31f-118">소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2e31f-118">Software Requirements</span></span>

<span data-ttu-id="2e31f-119">다음 목록에서는 Sequencer 실행을 위해 지원 되는 운영 체제에 대해 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e31f-120">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2e31f-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2e31f-121">버전</span><span class="sxs-lookup"><span data-stu-id="2e31f-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="2e31f-122">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2e31f-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2e31f-123">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2e31f-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e31f-124">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="2e31f-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-125">Professional</span><span class="sxs-lookup"><span data-stu-id="2e31f-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-126">SP2 또는 SP3</span><span class="sxs-lookup"><span data-stu-id="2e31f-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-127">x86</span><span class="sxs-lookup"><span data-stu-id="2e31f-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2e31f-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e31f-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-129">비즈니스, 엔터프라이즈 또는 궁극적인</span><span class="sxs-lookup"><span data-stu-id="2e31f-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-130">서비스 팩, SP1 또는 SP2 없음</span><span class="sxs-lookup"><span data-stu-id="2e31f-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-131">x86</span><span class="sxs-lookup"><span data-stu-id="2e31f-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e31f-132">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="2e31f-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-133">Professional, Enterprise 또는 Ultimate</span><span class="sxs-lookup"><span data-stu-id="2e31f-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2e31f-134">x86</span><span class="sxs-lookup"><span data-stu-id="2e31f-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2e31f-135">¹ 4.5 (SP1 또는 SP2 포함), app-v 4.6에 대해서만 지원 됨</span><span class="sxs-lookup"><span data-stu-id="2e31f-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="2e31f-136">**참고**  App-v (Application Virtualization) 4.6 Sequencer는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="2e31f-137">시퀀서를 실행 하는 컴퓨터는 대상 컴퓨터에 설치 된 것과 동일한 응용 프로그램을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="2e31f-138">원격 데스크톱 서비스에 대 한 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="2e31f-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2e31f-139">운영 체제</span><span class="sxs-lookup"><span data-stu-id="2e31f-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2e31f-140">버전</span><span class="sxs-lookup"><span data-stu-id="2e31f-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="2e31f-141">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="2e31f-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2e31f-142">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="2e31f-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e31f-143">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="2e31f-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-144">스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2e31f-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-145">SP1 또는 SP2</span><span class="sxs-lookup"><span data-stu-id="2e31f-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-146">x86</span><span class="sxs-lookup"><span data-stu-id="2e31f-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2e31f-147">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="2e31f-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-148">스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="2e31f-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="2e31f-149">x86</span><span class="sxs-lookup"><span data-stu-id="2e31f-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2e31f-150">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="2e31f-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-151">표준, 엔터프라이즈 또는 데이터 센터</span><span class="sxs-lookup"><span data-stu-id="2e31f-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-152">SP1 또는 SP2</span><span class="sxs-lookup"><span data-stu-id="2e31f-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2e31f-153">x86</span><span class="sxs-lookup"><span data-stu-id="2e31f-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2e31f-154">**참고**  원격 데스크톱 서비스의 App-v (Application Virtualization) 4.6는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e31f-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="2e31f-155">관련 항목</span><span class="sxs-lookup"><span data-stu-id="2e31f-155">Related topics</span></span>


[<span data-ttu-id="2e31f-156">Application Virtualization Sequencer 개요</span><span class="sxs-lookup"><span data-stu-id="2e31f-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





