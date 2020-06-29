---
title: Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항
description: Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819623"
---
# <span data-ttu-id="c7782-103">Application Virtualization Sequencer 하드웨어 및 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="c7782-104">이 항목에서는 Microsoft App-v (Application Virtualization) Sequencer를 실행 하는 컴퓨터에 대해 권장 되는 최소 하드웨어 및 소프트웨어 요구 사항에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="c7782-105">**중요**  Sequencer에서 로컬 시스템에 대 한 변경 사항 때문에 관리자 권한이 있는 계정을 사용 하 여 App-v 시퀀서 (**SFTSequencer.exe**)를 실행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="c7782-106">이러한 변경 사항에는 **C:\\program files files** 디렉터리에 파일 쓰기, 레지스트리 변경, 서비스 시작 및 중지, 파일에 대 한 보안 설명자 업데이트, 권한 변경 등이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="c7782-107">시퀀서를 설치 하 고 각 응용 프로그램의 순서를 설정한 후에는 시퀀싱 된 컴퓨터에 클린 운영 체제 이미지를 복원 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="c7782-108">다음 방법 중 하나를 사용 하 여 Sequencer를 실행 하는 컴퓨터를 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="c7782-109">하드 드라이브를 다시 포맷 하 고 운영 체제를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="c7782-110">다른 디스크 이미징 소프트웨어를 사용 하 여 Sequencer 이미지를 실행 하는 컴퓨터의 하드 드라이브를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="c7782-111">Microsoft 가상 PC 이미지와 같은 가상 운영 체제 이미지를 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="c7782-112">가상 컴퓨터를 사용 하면 관리를 최소화 하면서 정리 된 환경을 손쉽게 다시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="c7782-113">다음 목록에는 App-v 시퀀서를 실행 하기 위한 권장 하드웨어 요구 사항이 요약 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="c7782-114">요구 사항은 Microsoft Application Virtualization (App-v) 4.6 SP2에 대해 먼저 나열 되며, 그 뒤에 App-V 4.6 SP2 이전의 버전에 대 한 요구 사항이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="c7782-115">하드웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-115">Hardware Requirements</span></span>

-   <span data-ttu-id="c7782-116">프로세서-Intel 펜티엄 III, 1Ghz (32 비트 또는 64 비트).</span><span class="sxs-lookup"><span data-stu-id="c7782-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="c7782-117">시퀀싱 프로세스는 단일 스레드 프로세스 이며 이중 프로세서를 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="c7782-118">메모리-1GB 이상, 2GB 권장.</span><span class="sxs-lookup"><span data-stu-id="c7782-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="c7782-119">하드 디스크-최소 15gb의 하드 디스크 공간을 사용 하는 40gb (하드 디스크 공간)</span><span class="sxs-lookup"><span data-stu-id="c7782-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="c7782-120">시퀀싱 하는 응용 프로그램에 필요한 하드 디스크 공간에는 세 배 이상 있는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="c7782-121">**참고**  시퀀싱에는 디스크 사용량이 많이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="c7782-122">빠른 디스크 속도를 통해 시퀀싱 시간을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="c7782-123">앱-V 4.6 SP2의 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="c7782-124">다음 목록에서는 App-v 4.6 SP2 시퀀서를 실행 하기 위해 지원 되는 운영 체제에 대해 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7782-125">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c7782-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="c7782-126">버전</span><span class="sxs-lookup"><span data-stu-id="c7782-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="c7782-127">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c7782-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c7782-128">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c7782-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-129">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="c7782-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-130">Professional</span><span class="sxs-lookup"><span data-stu-id="c7782-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-131">이상을</span><span class="sxs-lookup"><span data-stu-id="c7782-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-132">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7782-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-134">비즈니스, 엔터프라이즈 또는 궁극적인</span><span class="sxs-lookup"><span data-stu-id="c7782-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-135">SP2</span><span class="sxs-lookup"><span data-stu-id="c7782-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-136">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-137">Windows7</span><span class="sxs-lookup"><span data-stu-id="c7782-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-138">Professional, Enterprise 또는 Ultimate</span><span class="sxs-lookup"><span data-stu-id="c7782-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-139">서비스 팩 또는 SP1 없음</span><span class="sxs-lookup"><span data-stu-id="c7782-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-140">x86 및 x64</span><span class="sxs-lookup"><span data-stu-id="c7782-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-141">Windows8</span><span class="sxs-lookup"><span data-stu-id="c7782-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-142">Pro 또는 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c7782-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c7782-143">x86 및 x64</span><span class="sxs-lookup"><span data-stu-id="c7782-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7782-144">**참고**  App-v (Application Virtualization) 4.6 SP2 시퀀서는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="c7782-145">시퀀서를 실행 하는 컴퓨터는 대상 컴퓨터에 설치 된 것과 동일한 응용 프로그램을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="c7782-146">App-v 4.6 SP2 앞의 버전에 대 한 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="c7782-147">다음 목록에서는 App-v 4.6 SP2 앞의 버전용으로 시퀀서를 실행 하기 위해 지원 되는 운영 체제에 대해 간략하게 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7782-148">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c7782-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="c7782-149">버전</span><span class="sxs-lookup"><span data-stu-id="c7782-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="c7782-150">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c7782-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c7782-151">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c7782-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-152">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="c7782-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-153">Professional</span><span class="sxs-lookup"><span data-stu-id="c7782-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-154">SP2 또는 SP3</span><span class="sxs-lookup"><span data-stu-id="c7782-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-155">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7782-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-157">비즈니스, 엔터프라이즈 또는 궁극적인</span><span class="sxs-lookup"><span data-stu-id="c7782-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-158">서비스 팩, SP1 또는 SP2 없음</span><span class="sxs-lookup"><span data-stu-id="c7782-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-159">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-160">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="c7782-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-161">Professional, Enterprise 또는 Ultimate</span><span class="sxs-lookup"><span data-stu-id="c7782-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c7782-162">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7782-163">¹ 4.5 (SP1 또는 SP2 포함), app-v 4.6에 대해서만 지원 됨</span><span class="sxs-lookup"><span data-stu-id="c7782-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="c7782-164">**참고**  App-v (Application Virtualization) 4.6 Sequencer는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="c7782-165">시퀀서를 실행 하는 컴퓨터는 대상 컴퓨터에 설치 된 것과 동일한 응용 프로그램을 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="c7782-166">App-v 4.6 SP2 용 원격 데스크톱 서비스에 대 한 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7782-167">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c7782-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="c7782-168">버전</span><span class="sxs-lookup"><span data-stu-id="c7782-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="c7782-169">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c7782-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c7782-170">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c7782-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-171">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7782-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-172">스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c7782-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-173">SP2</span><span class="sxs-lookup"><span data-stu-id="c7782-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-174">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-175">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="c7782-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-176">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="c7782-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-177">SP2</span><span class="sxs-lookup"><span data-stu-id="c7782-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-178">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-179">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7782-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-180">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="c7782-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-181">서비스 팩 또는 SP1 없음</span><span class="sxs-lookup"><span data-stu-id="c7782-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-182">x64</span><span class="sxs-lookup"><span data-stu-id="c7782-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7782-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-184">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="c7782-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="c7782-185">x86 또는 x64</span><span class="sxs-lookup"><span data-stu-id="c7782-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7782-186">**참고**  Application Virtualization (App-v) 원격 데스크톱 서비스에 대 한 4.6 SP2는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="c7782-187">App-v 4.6 SP2 보다 앞에 있는 버전의 원격 데스크톱 서비스에 대 한 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7782-188">운영 체제</span><span class="sxs-lookup"><span data-stu-id="c7782-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="c7782-189">버전</span><span class="sxs-lookup"><span data-stu-id="c7782-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="c7782-190">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="c7782-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="c7782-191">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="c7782-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-192">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="c7782-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-193">스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c7782-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-194">SP1 또는 SP2</span><span class="sxs-lookup"><span data-stu-id="c7782-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-195">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-196">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7782-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-197">스탠더드 버전, Enterprise Edition 또는 Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="c7782-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-198">서비스 팩 또는 SP2 없음</span><span class="sxs-lookup"><span data-stu-id="c7782-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-199">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7782-200">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="c7782-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-201">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="c7782-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-202">SP1 또는 SP2</span><span class="sxs-lookup"><span data-stu-id="c7782-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-203">x86</span><span class="sxs-lookup"><span data-stu-id="c7782-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7782-204">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7782-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-205">표준, 엔터프라이즈 또는 데이터 센터 에디션</span><span class="sxs-lookup"><span data-stu-id="c7782-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-206">서비스 팩 또는 SP1 없음</span><span class="sxs-lookup"><span data-stu-id="c7782-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7782-207">x64</span><span class="sxs-lookup"><span data-stu-id="c7782-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7782-208">**참고**  Application Virtualization (App-v) 원격 데스크톱 서비스에 대 한 4.6 SP2는 이러한 운영 체제의 32 비트 및 64 비트 버전을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7782-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="c7782-209">관련 항목</span><span class="sxs-lookup"><span data-stu-id="c7782-209">Related topics</span></span>


[<span data-ttu-id="c7782-210">Application Virtualization Client 하드웨어 및 소프트웨어 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="c7782-211">Application Virtualization 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="c7782-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="c7782-212">Application Virtualization Sequencer 설치 방법</span><span class="sxs-lookup"><span data-stu-id="c7782-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="c7782-213">Application Virtualization Sequencer 업그레이드 방법</span><span class="sxs-lookup"><span data-stu-id="c7782-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





