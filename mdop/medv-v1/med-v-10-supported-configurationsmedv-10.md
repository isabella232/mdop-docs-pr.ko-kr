---
title: MED-V 1.0 지원되는 구성
description: MED-V 1.0 지원되는 구성
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812609"
---
# <span data-ttu-id="0c841-103">MED-V 1.0 지원되는 구성</span><span class="sxs-lookup"><span data-stu-id="0c841-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="0c841-104">이 항목에서는 환경에서 Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 1.0를 설치 하 고 실행 하는 데 필요한 요구 사항을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="0c841-105">MED-V 1.0 클라이언트 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0c841-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="0c841-106">MED-V 클라이언트 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0c841-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="0c841-107">다음 표에는 MED-V 1.0 클라이언트 설치에 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0c841-108">운영 체제</span><span class="sxs-lookup"><span data-stu-id="0c841-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="0c841-109">버전</span><span class="sxs-lookup"><span data-stu-id="0c841-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="0c841-110">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="0c841-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="0c841-111">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="0c841-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0c841-112">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c841-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-113">Professional Edition</span><span class="sxs-lookup"><span data-stu-id="0c841-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-114">SP2 또는 SP3</span><span class="sxs-lookup"><span data-stu-id="0c841-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-115">x86</span><span class="sxs-lookup"><span data-stu-id="0c841-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0c841-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c841-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-117">비즈니스, 엔터프라이즈 또는 Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="0c841-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-118">SP1 또는 SP2</span><span class="sxs-lookup"><span data-stu-id="0c841-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-119">x86</span><span class="sxs-lookup"><span data-stu-id="0c841-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="0c841-120">참고</span><span class="sxs-lookup"><span data-stu-id="0c841-120">Note</span></span>**  
<span data-ttu-id="0c841-121">MED-V 클라이언트는 네이티브 x64 모드에서 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="0c841-122">대신, MED-V는 windows 64 비트 (WOW64) 모드의 Windows에서 64 비트 컴퓨터를 통해 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="0c841-123">MED-V 1.0 클라이언트 구성</span><span class="sxs-lookup"><span data-stu-id="0c841-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="0c841-124">.NET Framework 버전</span><span class="sxs-lookup"><span data-stu-id="0c841-124">.NET Framework Version</span></span>**

<span data-ttu-id="0c841-125">MED-V 1.0 클라이언트 설치에 지원 되는 Microsoft .NET Framework 버전은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="0c841-126">.NET Framework 2.0 또는 .NET Framework 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="0c841-127">.NET Framework 3.0 또는 .NET Framework 3.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="0c841-128">.NET Framework 3.5 또는 .NET Framework 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="0c841-129">가상화 엔진</span><span class="sxs-lookup"><span data-stu-id="0c841-129">Virtualization Engine</span></span>**

<span data-ttu-id="0c841-130">Microsoft 기술 자료 문서 974918에서 설명 하는 핫픽스가 포함 된 microsoft 가상 PC 2007 SP1은 다음과 같은 구성에서 MED-V 1.0 클라이언트 설치에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="0c841-131">정적 VHD (가상 하드 디스크) 파일</span><span class="sxs-lookup"><span data-stu-id="0c841-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="0c841-132">같은 디렉터리 내에 있는 여러 개의 VHD 파일</span><span class="sxs-lookup"><span data-stu-id="0c841-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="0c841-133">동적 VHD 파일</span><span class="sxs-lookup"><span data-stu-id="0c841-133">Dynamic VHD file</span></span>

**<span data-ttu-id="0c841-134">인터넷 브라우저</span><span class="sxs-lookup"><span data-stu-id="0c841-134">Internet Browser</span></span>**

<span data-ttu-id="0c841-135">Windows Internet Explorer 7 및 Windows Internet Explorer 8은 MED-V 1.0 클라이언트 설치에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="0c841-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="0c841-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="0c841-137">MED-V 클라이언트는 Microsoft Hyper-v server 환경에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="0c841-138">MED-V 1.0 Workspace 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0c841-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="0c841-139">MED-V 작업 영역 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0c841-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="0c841-140">다음 표에는 MED-V 1.0 작업 영역에 대해 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0c841-141">운영 체제</span><span class="sxs-lookup"><span data-stu-id="0c841-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="0c841-142">버전</span><span class="sxs-lookup"><span data-stu-id="0c841-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="0c841-143">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="0c841-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="0c841-144">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="0c841-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0c841-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0c841-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-146">Professional</span><span class="sxs-lookup"><span data-stu-id="0c841-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-147">4(SP4)</span><span class="sxs-lookup"><span data-stu-id="0c841-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-148">86</span><span class="sxs-lookup"><span data-stu-id="0c841-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0c841-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c841-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-150">Professional Edition</span><span class="sxs-lookup"><span data-stu-id="0c841-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-151">SP2 또는 SP3</span><span class="sxs-lookup"><span data-stu-id="0c841-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="0c841-152">참고</span><span class="sxs-lookup"><span data-stu-id="0c841-152">Note</span></span></strong><br/><p><span data-ttu-id="0c841-153">SP3은 MED-V 작업 영역이 차기 버전의 MED-V와 호환 되도록 하는 데 적합 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="0c841-154">x86</span><span class="sxs-lookup"><span data-stu-id="0c841-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="0c841-155">MED-V 1.0 작업 영역 구성</span><span class="sxs-lookup"><span data-stu-id="0c841-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="0c841-156">.NET Framework 버전</span><span class="sxs-lookup"><span data-stu-id="0c841-156">.NET Framework Version</span></span>**

<span data-ttu-id="0c841-157">MED-V 1.0 작업 영역 설치에 대해 다음과 같은 지원 되는 Microsoft .NET Framework 버전 중 하나가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="0c841-158">.NET Framework 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="0c841-159">.NET Framework 3.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="0c841-160">.NET Framework 3.5 또는 .NET Framework 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="0c841-161">참고</span><span class="sxs-lookup"><span data-stu-id="0c841-161">Note</span></span>**  
<span data-ttu-id="0c841-162">.NET Framework 3.5 SP1은 MED-V 작업 영역이 MED-V의 향후 버전과 호환 되도록 하는 데 권장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="0c841-163">인터넷 브라우저</span><span class="sxs-lookup"><span data-stu-id="0c841-163">Internet Browser</span></span>**

<span data-ttu-id="0c841-164">MED-V 1.0 작업 영역 설치에는 windows Internet Explorer 6 SP2 및 Windows Internet Explorer 7이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="0c841-165">MED-V 작업 영역 이미지</span><span class="sxs-lookup"><span data-stu-id="0c841-165">MED-V Workspace Images</span></span>

<span data-ttu-id="0c841-166">가상 PC 2007 SP1을 사용 하 여 MED-V 작업 영역 이미지를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="0c841-167">MED-V 1.0 서버 시스템 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0c841-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="0c841-168">MED-V 1.0 서버 운영 체제 요구 사항</span><span class="sxs-lookup"><span data-stu-id="0c841-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="0c841-169">다음 표에는 MED-V 1.0 서버 설치에 지원 되는 운영 체제가 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0c841-170">운영 체제</span><span class="sxs-lookup"><span data-stu-id="0c841-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="0c841-171">버전</span><span class="sxs-lookup"><span data-stu-id="0c841-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="0c841-172">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="0c841-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="0c841-173">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="0c841-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0c841-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c841-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-175">Standard 또는 Enterprise</span><span class="sxs-lookup"><span data-stu-id="0c841-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-176">없음</span><span class="sxs-lookup"><span data-stu-id="0c841-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-177">X86 또는 x64</span><span class="sxs-lookup"><span data-stu-id="0c841-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="0c841-178">MED-V 1.0 서버 구성</span><span class="sxs-lookup"><span data-stu-id="0c841-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="0c841-179">.NET Framework 버전</span><span class="sxs-lookup"><span data-stu-id="0c841-179">.NET Framework Version</span></span>**

<span data-ttu-id="0c841-180">MED-V 1.0 작업 영역 설치에 대해 다음과 같은 지원 되는 Microsoft .NET Framework 버전 중 하나가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="0c841-181">.NET Framework 2.0 또는 .NET Framework 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="0c841-182">.NET Framework 3.0 또는 .NET Framework 3.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="0c841-183">.NET Framework 3.5 또는 .NET Framework 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="0c841-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="0c841-184">Microsoft SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="0c841-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="0c841-185">SQL Server가 MED-V 1.0 서버에서 로컬 또는 원격으로 설치 되는 경우 다음과 같은 Microsoft SQL Server 버전이 MED-V 1.0에 대해 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0c841-186">SQL Server 버전</span><span class="sxs-lookup"><span data-stu-id="0c841-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="0c841-187">버전</span><span class="sxs-lookup"><span data-stu-id="0c841-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="0c841-188">서비스 팩</span><span class="sxs-lookup"><span data-stu-id="0c841-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="0c841-189">시스템 아키텍처</span><span class="sxs-lookup"><span data-stu-id="0c841-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0c841-190">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="0c841-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-191">익스프레스, Standard 또는 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="0c841-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-192">SP2</span><span class="sxs-lookup"><span data-stu-id="0c841-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-193">X86 또는 x64</span><span class="sxs-lookup"><span data-stu-id="0c841-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0c841-194">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c841-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-195">익스프레스, Standard 또는 Enterprise</span><span class="sxs-lookup"><span data-stu-id="0c841-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-196">없음</span><span class="sxs-lookup"><span data-stu-id="0c841-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="0c841-197">X86 또는 x64</span><span class="sxs-lookup"><span data-stu-id="0c841-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="0c841-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="0c841-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="0c841-199">MED-V 서버는 Microsoft Hyper-v server 환경에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="0c841-200">MED-V 1.0 세계화 정보</span><span class="sxs-lookup"><span data-stu-id="0c841-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="0c841-201">MED-V는 영어 이외의 언어로 릴리스되지 않지만 MED-V 1.0 클라이언트, 작업 영역 및 서버 설치에는 다음과 같은 Windows 운영 체제 언어 버전이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c841-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="0c841-202">영어</span><span class="sxs-lookup"><span data-stu-id="0c841-202">English</span></span>

-   <span data-ttu-id="0c841-203">프랑스어</span><span class="sxs-lookup"><span data-stu-id="0c841-203">French</span></span>

-   <span data-ttu-id="0c841-204">독일어</span><span class="sxs-lookup"><span data-stu-id="0c841-204">German</span></span>

-   <span data-ttu-id="0c841-205">이탈리아어</span><span class="sxs-lookup"><span data-stu-id="0c841-205">Italian</span></span>

-   <span data-ttu-id="0c841-206">스페인어</span><span class="sxs-lookup"><span data-stu-id="0c841-206">Spanish</span></span>

-   <span data-ttu-id="0c841-207">포르투갈어(브라질)</span><span class="sxs-lookup"><span data-stu-id="0c841-207">Portuguese (Brazil)</span></span>









