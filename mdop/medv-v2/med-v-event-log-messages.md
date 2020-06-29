---
title: MED-V 이벤트 로그 메시지
description: MED-V 이벤트 로그 메시지
author: dansimp
ms.assetid: 7ba7344d-153b-4cc4-a00a-5d42aee9986b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d8dcf1cce48d6c1e29d46b4db7ac1550aa9477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823078"
---
# <span data-ttu-id="332f9-103">MED-V 이벤트 로그 메시지</span><span class="sxs-lookup"><span data-stu-id="332f9-103">MED-V Event Log Messages</span></span>


<span data-ttu-id="332f9-104">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0의 로그 파일에서는 엔터프라이즈에서 MED-V를 배포 하 고 관리 하는 방법에 대 한 자세한 정보를 제공 하 고 기능을 확인 하거나 문제를 해결 하는 데 도움을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-104">The log files for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 provide detailed information about how to deploy and manage MED-V in your enterprise and help verify functionality or help troubleshoot issues.</span></span>

## <span data-ttu-id="332f9-105">이벤트 Id</span><span class="sxs-lookup"><span data-stu-id="332f9-105">Event IDs</span></span>


<span data-ttu-id="332f9-106">다음은 med-v를 배포 하거나 관리할 때 발생할 수 있는 문제를 해결 하는 데 도움이 되는 MED-V 이벤트 Id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-106">The following are a list of MED-V event IDs to help troubleshoot issues that you might encounter when you deploy or manage MED-V.</span></span>

### <span data-ttu-id="332f9-107">Fts</span><span class="sxs-lookup"><span data-stu-id="332f9-107">Fts</span></span>

<span data-ttu-id="332f9-108">처음 설치할 때 이벤트 Id를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-108">Shows the event IDs for first time setup.</span></span>

### <span data-ttu-id="332f9-109">이벤트 ID 3066</span><span class="sxs-lookup"><span data-stu-id="332f9-109">Event ID 3066</span></span>

<span data-ttu-id="332f9-110">가상 머신 시작 작업이 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-110">Start virtual machine operation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-111">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-111">Description</span></span>**  
<span data-ttu-id="332f9-112">MED-V 작업 영역을 만드는 데 사용 하는 VHD (가상 하드 디스크)에 잠재적인 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-112">A potential problem exists with the virtual hard disk (VHD) that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-113">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-113">Solution</span></span>**  
<span data-ttu-id="332f9-114">MED-V 용 VHD를 사용 하 여 가상 컴퓨터를 만들 수 있고 시작할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-114">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="332f9-115">이벤트 ID 3071</span><span class="sxs-lookup"><span data-stu-id="332f9-115">Event ID 3071</span></span>

<span data-ttu-id="332f9-116">가상 컴퓨터 준비에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-116">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-117">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-117">Description</span></span>**  
<span data-ttu-id="332f9-118">다양 한 문제로 인해 처음으로 설정 했을 때 문제가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-118">A problem occurred with first time setup that might have been caused by many different issues.</span></span> <span data-ttu-id="332f9-119">여기에는 네트워크 연결 문제 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-119">These include problems with network connectivity.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-120">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-120">Solution</span></span>**  
<span data-ttu-id="332f9-121">MED-V 호스트 에이전트를 다시 시작 하 여 처음 설정으로 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-121">Restart the MED-V Host Agent to rerun first time setup.</span></span>

### <span data-ttu-id="332f9-122">이벤트 ID 3078</span><span class="sxs-lookup"><span data-stu-id="332f9-122">Event ID 3078</span></span>

<span data-ttu-id="332f9-123">가상 컴퓨터 준비에 실패 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-123">Virtual machine preparation failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-124">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-124">Description</span></span>**  
<span data-ttu-id="332f9-125">MED-V 작업 영역을 만드는 데 사용 하는 VHD에 잠재적인 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-125">A potential problem exists with the VHD that you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-126">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-126">Solution</span></span>**  
<span data-ttu-id="332f9-127">MED-V 용 VHD를 사용 하 여 가상 컴퓨터를 만들 수 있고 시작할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-127">Verify that you can create a virtual machine with the VHD for MED-V and that it can be started.</span></span>

### <span data-ttu-id="332f9-128">이벤트 ID 3079</span><span class="sxs-lookup"><span data-stu-id="332f9-128">Event ID 3079</span></span>

<span data-ttu-id="332f9-129">가상 컴퓨터 준비를 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-129">Retrying virtual machine preparation.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-130">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-130">Description</span></span>**  
<span data-ttu-id="332f9-131">MED-V가 가상 컴퓨터를 준비 하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-131">MED-V is trying to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-132">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-132">Solution</span></span>**  
<span data-ttu-id="332f9-133">필요한 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-133">No action is required.</span></span> <span data-ttu-id="332f9-134">처음 설치를 완료 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-134">Let first time setup finish.</span></span>

### <span data-ttu-id="332f9-135">이벤트 ID 3080</span><span class="sxs-lookup"><span data-stu-id="332f9-135">Event ID 3080</span></span>

<span data-ttu-id="332f9-136">가상 컴퓨터를 준비 하는 동안 클라이언트가 중지 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-136">The client was stopped when preparing the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-137">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-137">Description</span></span>**  
<span data-ttu-id="332f9-138">가상 컴퓨터를 준비 하려고 할 때 MED-V가 예기치 않게 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-138">MED-V stops unexpectedly when it tries to prepare the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-139">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-139">Solution</span></span>**  
<span data-ttu-id="332f9-140">MED-V 호스트 에이전트를 시작 하 고 처음 설치를 완료 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-140">Start the MED-V Host Agent and let first time setup complete</span></span>

### <span data-ttu-id="332f9-141">이벤트 ID 3084</span><span class="sxs-lookup"><span data-stu-id="332f9-141">Event ID 3084</span></span>

<span data-ttu-id="332f9-142">가상 머신이 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-142">Virtual machine is not valid.</span></span> <span data-ttu-id="332f9-143">처음으로 다시 실행 해야 할 때가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-143">First time setup needs to be re-run.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-144">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-144">Description</span></span>**  
<span data-ttu-id="332f9-145">MED-V 호스트 에이전트에서 가상 컴퓨터의 문제를 발견 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-145">The MED-V Host Agent detected a problem with the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-146">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-146">Solution</span></span>**  
<span data-ttu-id="332f9-147">필요한 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-147">No action is required.</span></span> <span data-ttu-id="332f9-148">처음 설치를 완료 하도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-148">Let first time setup finish.</span></span>

### <span data-ttu-id="332f9-149">이벤트 ID 3099</span><span class="sxs-lookup"><span data-stu-id="332f9-149">Event ID 3099</span></span>

<span data-ttu-id="332f9-150">가상 머신을 시작 하기 위해 전화를 걸 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-150">Call to start virtual machine failed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-151">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-151">Description</span></span>**  
<span data-ttu-id="332f9-152">MED-V 작업 영역을 만드는 데 사용 하는 VHD에 잠재적인 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-152">A potential problem exists with the VHD you are using to create a MED-V workspace.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-153">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-153">Solution</span></span>**  
<span data-ttu-id="332f9-154">MED-V 용 VHD를 사용 하 여 가상 컴퓨터를 만들 수 있고 열 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-154">Verify that you can create a virtual machine with the VHD for MED-V and that it can be opened.</span></span>

### <span data-ttu-id="332f9-155">VM 관리</span><span class="sxs-lookup"><span data-stu-id="332f9-155">VM Management</span></span>

### <span data-ttu-id="332f9-156">이벤트 ID 4022</span><span class="sxs-lookup"><span data-stu-id="332f9-156">Event ID 4022</span></span>

<span data-ttu-id="332f9-157">VM에 대 한 명령을 실행 하는 동안 VMManagerException 심각한 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-157">VMManagerException Fatal error while issuing command to VM.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-158">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-158">Description</span></span>**  
<span data-ttu-id="332f9-159">최종 사용자가 로그 오프 하거나 MED-V 호스트를 종료 하 여 MED-V를 종료 하려고 했지만 VMTaskTimeout 구성 설정이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-159">The end user tried to exit MED-V by logging off or by shutting down the MED-V host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-160">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-160">Solution</span></span>**  
<span data-ttu-id="332f9-161">MED-V를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-161">Restart MED-V.</span></span>

### <span data-ttu-id="332f9-162">이벤트 ID 4028</span><span class="sxs-lookup"><span data-stu-id="332f9-162">Event ID 4028</span></span>

<span data-ttu-id="332f9-163">VM 작업 시간이 초과 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-163">VM Operation timed out.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-164">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-164">Description</span></span>**  
<span data-ttu-id="332f9-165">최종 사용자가 로그 오프 하거나 호스트를 종료 하 고 VMTaskTimeout 구성 설정을 초과한 경우 MED-V를 종료 하려고 시도 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-165">The end user tried to exit MED-V by logging off or by shutting down the host, and the VMTaskTimeout configuration setting was exceeded.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-166">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-166">Solution</span></span>**  
<span data-ttu-id="332f9-167">MED-V를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-167">Restart MED-V.</span></span>

### <span data-ttu-id="332f9-168">이벤트 ID 4038</span><span class="sxs-lookup"><span data-stu-id="332f9-168">Event ID 4038</span></span>

<span data-ttu-id="332f9-169">Vmsal에서 사용자에 게 오류 메시지를 게시 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-169">Vmsal posted an error message to the user.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-170">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-170">Description</span></span>**  
<span data-ttu-id="332f9-171">최종 사용자에 게 가상 응용 프로그램을 시작할 수 없다는 오류 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-171">An error message is displayed to the end user stating that MED-V could not start the virtual application.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-172">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-172">Solution</span></span>**  
<span data-ttu-id="332f9-173">오류가 한 행에 두 번 이상 기록 되는 경우, MED-V를 중지 하 고 Windows Virtual PC 콘솔을 사용 하 여 가상 컴퓨터에 연결 하 고 응용 프로그램을 전체 화면으로 시작 하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-173">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console and attempt to start the application in Full Screen.</span></span>

### <span data-ttu-id="332f9-174">이벤트 ID 4040</span><span class="sxs-lookup"><span data-stu-id="332f9-174">Event ID 4040</span></span>

<span data-ttu-id="332f9-175">TerminalServices가 게스트에서 초기화 되지 않았으므로 추가가 재생 됩니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-175">Recycling Additions because TerminalServices is not initialized in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-176">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-176">Description</span></span>**  
<span data-ttu-id="332f9-177">가상 컴퓨터에서 원격 데스크톱 서비스가 초기화 되지 않았으므로 MED-V가 가상 컴퓨터를 다시 부팅 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-177">MED-V rebooted the virtual machine because Remote Desktop Services was not initialized on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-178">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-178">Solution</span></span>**  
<span data-ttu-id="332f9-179">오류가 한 행에 두 번 이상 기록 되는 경우 MED-V를 중지 하 고 Windows 가상 PC 콘솔을 사용 하 여 가상 컴퓨터에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-179">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="332f9-180">이벤트 ID 4042</span><span class="sxs-lookup"><span data-stu-id="332f9-180">Event ID 4042</span></span>

<span data-ttu-id="332f9-181">게스트의 추가를 재활용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-181">Failed to recycle additions in the guest.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-182">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-182">Description</span></span>**  
<span data-ttu-id="332f9-183">MED-V가 가상 컴퓨터에서 가상 컴퓨터 추가 기능을 재활용 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-183">MED-V failed to recycle virtual machine additions on the virtual machine.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-184">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-184">Solution</span></span>**  
<span data-ttu-id="332f9-185">오류가 한 행에 두 번 이상 기록 되는 경우 MED-V를 중지 하 고 Windows 가상 PC 콘솔을 사용 하 여 가상 컴퓨터에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-185">If the error is logged two or more times in a row, stop MED-V and connect to the virtual machine by using Windows Virtual PC console.</span></span>

### <span data-ttu-id="332f9-186">이벤트 ID 4043</span><span class="sxs-lookup"><span data-stu-id="332f9-186">Event ID 4043</span></span>

<span data-ttu-id="332f9-187">가상 머신에서 만료 된 암호를 재설정 하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-187">Failed to reset expired password in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-188">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-188">Description</span></span>**  
<span data-ttu-id="332f9-189">최종 사용자가 만료 되기 전에 가상 컴퓨터의 암호를 다시 설정 하지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-189">The end user did not reset the password in the virtual machine before it expired.</span></span> <span data-ttu-id="332f9-190">따라서 사용자는 네트워크 리소스에 액세스 하거나 작업을 저장 하지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-190">As a result, the user might not be able to access network resources or save work.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-191">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-191">Solution</span></span>**  
<span data-ttu-id="332f9-192">MED-V 게스트를 종료 하 고 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-192">Shut down the MED-V guest and restart it.</span></span>

### <span data-ttu-id="332f9-193">URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="332f9-193">URL Redirection</span></span>

### <span data-ttu-id="332f9-194">이벤트 ID 5005</span><span class="sxs-lookup"><span data-stu-id="332f9-194">Event ID 5005</span></span>

<span data-ttu-id="332f9-195">구성에서 VM 이름을 가져올 수 없습니다. 게스트 브라우저를 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-195">Couldn’t get VM name from configuration; can’t launch guest browser.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-196">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-196">Description</span></span>**  
<span data-ttu-id="332f9-197">URL 리디렉션이 구성에서 MED-V 작업 영역 이름을 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-197">URL Redirection could not obtain the MED-V workspace name from the configuration.</span></span> <span data-ttu-id="332f9-198">결과적으로, MED-V 작업 영역 브라우저에서 Windows 가상 PC에 리디렉션된 URL을 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-198">As a result, it cannot inform Windows Virtual PC to open the redirected URL in the MED-V workspace browser.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-199">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-199">Solution</span></span>**  
<span data-ttu-id="332f9-200">MED-V 작업 영역 이름이 설정 되어 있고 C:\\Users\\ &lt; *사용자* &gt; \ 가상 컴퓨터 디렉터리의 가상 컴퓨터 이름과 일치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-200">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="332f9-201">MED-V 작업 영역 이름은 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-201">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="332f9-202">예를 들어 사용자가 "Matt"이 고 작업 영역 이름이 "mattsworkspace" 이면 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name의 값은 "mattsworkspace" 이어야 하며, C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx. 파일이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-202">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace", and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="332f9-203">이벤트 ID 5006</span><span class="sxs-lookup"><span data-stu-id="332f9-203">Event ID 5006</span></span>

<span data-ttu-id="332f9-204">파이프 서버를 만들지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-204">Failed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-205">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-205">Description</span></span>**  
<span data-ttu-id="332f9-206">URL 리디렉션 서비스가 Internet Explorer와 통신 하는 데 파이프 서버를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-206">The URL Redirection service could not create the pipe server to communicate with Internet Explorer.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-207">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-207">Solution</span></span>**  
<span data-ttu-id="332f9-208">시스템 이벤트 로그에서 경로가 "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_"와 유사 하 게 시작 하 고 사용자의 사용자 이름 및 도메인 이름으로 끝나는 파일 또는 리소스를 만들려는 시도에 대 한 확인을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-208">Check system event logs for attempts to create a file or resource whose path begins similar to the following: "\\\\.\\pipe\\MEDVUrlRedirectionPipe\_" and ends with the user’s user name and domain name.</span></span> <span data-ttu-id="332f9-209">이 이벤트가 이벤트 로그에 표시 되지 않으면 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-209">If this is not present in the event log, restart the computer.</span></span>

### <span data-ttu-id="332f9-210">ConfigMgr (게스트)</span><span class="sxs-lookup"><span data-stu-id="332f9-210">ConfigMgr (Guest)</span></span>

### <span data-ttu-id="332f9-211">이벤트 ID 7001</span><span class="sxs-lookup"><span data-stu-id="332f9-211">Event ID 7001</span></span>

<span data-ttu-id="332f9-212">호스트 네트워크 구성 데이터의 형식이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-212">The host network configuration data is not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-213">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-213">Description</span></span>**  
<span data-ttu-id="332f9-214">호스트에서 받은 네트워크 구성이 잘못 된 형식의 XML 문자열 이거나 호스트에서 반환 된 네트워크 정보를 XML 문서에 쓸 수 없는 경우</span><span class="sxs-lookup"><span data-stu-id="332f9-214">Either the network configuration received from the host is an incorrectly formatted XML string, or the network information returned from the host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-215">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-215">Solution</span></span>**  
<span data-ttu-id="332f9-216">호스트 컴퓨터와 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-216">Restart the host computer and the virtual machine.</span></span>

### <span data-ttu-id="332f9-217">이벤트 ID 7005</span><span class="sxs-lookup"><span data-stu-id="332f9-217">Event ID 7005</span></span>

<span data-ttu-id="332f9-218">호스트 네트워크 구성에 대 한 변경 내용이 검색 되었지만 호스트 네트워크 구성 데이터의 형식이 잘못 되어 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-218">A change to the host network configuration was detected, but was not able to be applied because the host network configuration data was not properly formatted.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-219">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-219">Description</span></span>**  
<span data-ttu-id="332f9-220">호스트 네트워크 구성에 대 한 변경 내용이 가상 컴퓨터에 통신 되었지만 오류 때문에 가상 머신에서 처리 될 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-220">A change to the host network configuration was communicated to the virtual machine, but could not be processed in the virtual machine because of an error.</span></span> <span data-ttu-id="332f9-221">이 오류는 잘못 된 형식의 데이터 또는 WMI (Windows Management Instrumentation) CCMNetworkAdapter 인스턴스에 대 한 정보를 설정할 수 없는 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-221">This error could be caused by incorrectly formatted data or the inability to set the information into the Windows Management Instrumentation (WMI) CCMNetworkAdapter instance.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-222">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-222">Solution</span></span>**  
<span data-ttu-id="332f9-223">호스트 및 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-223">Restart the host and virtual machine.</span></span>

### <span data-ttu-id="332f9-224">ConfigMgr (호스트)</span><span class="sxs-lookup"><span data-stu-id="332f9-224">ConfigMgr (Host)</span></span>

### <span data-ttu-id="332f9-225">이벤트 ID 8006</span><span class="sxs-lookup"><span data-stu-id="332f9-225">Event ID 8006</span></span>

<span data-ttu-id="332f9-226">가상 컴퓨터를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-226">The virtual machine cannot be found.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-227">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-227">Description</span></span>**  
<span data-ttu-id="332f9-228">Windows 가상 PC 7에서 가상 컴퓨터를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-228">Windows Virtual PC 7 cannot locate the virtual machine.</span></span> <span data-ttu-id="332f9-229">가상 머신이 삭제, 이동, 제거 되었거나 액세스가 거부 되었을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-229">The virtual machine might have been deleted, moved, removed, or access was denied.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-230">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-230">Solution</span></span>**  
<span data-ttu-id="332f9-231">가상 컴퓨터를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-231">Reinstall the virtual machine.</span></span>

### <span data-ttu-id="332f9-232">이벤트 ID 8008</span><span class="sxs-lookup"><span data-stu-id="332f9-232">Event ID 8008</span></span>

<span data-ttu-id="332f9-233">워크스테이션의 네트워크 구성 정보를 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-233">The workstation's network configuration information could not be retrieved.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-234">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-234">Description</span></span>**  
<span data-ttu-id="332f9-235">대부분의 경우 .NET Framework의 시스템 호출 오류로 인해 MED-V 호스트에서 네트워크 구성 정보를 수집할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-235">Network configuration information could not be collected from the MED-V host, most likely because of a system call failure in the .NET Framework.</span></span> <span data-ttu-id="332f9-236">이 오류는 MED-V 호스트에서 반환 된 네트워크 정보를 XML 문서에 쓸 수 없는 경우에도 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-236">This failure can also occur if the network information returned from the MED-V host cannot be written to an XML document.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-237">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-237">Solution</span></span>**  
<span data-ttu-id="332f9-238">호스트 워크스테이션을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-238">Restart the host workstation.</span></span>

### <span data-ttu-id="332f9-239">이벤트 ID 8010</span><span class="sxs-lookup"><span data-stu-id="332f9-239">Event ID 8010</span></span>

<span data-ttu-id="332f9-240">가상 머신에서 네트워크 구성 데이터를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-240">The network configuration data could not be set in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-241">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-241">Description</span></span>**  
<span data-ttu-id="332f9-242">가상 컴퓨터가 잘못 된 상태 이거나 Windows 가상 PC 추가가 설치 되지 않았거나 사용 하도록 설정 되어 있지 않기 때문에 MED-V 호스트 NAT (network address translation)가 가상 컴퓨터에 통신 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-242">The MED-V hostnetwork address translation (NAT) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-243">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-243">Solution</span></span>**  
<span data-ttu-id="332f9-244">가상 컴퓨터를 종료 하 고 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-244">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="332f9-245">또한 가상 컴퓨터를 다시 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-245">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="332f9-246">이벤트 ID 8011</span><span class="sxs-lookup"><span data-stu-id="332f9-246">Event ID 8011</span></span>

<span data-ttu-id="332f9-247">가상 머신에서 네트워크 구성 데이터를 다시 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-247">The network configuration data could not be reset in the virtual machine.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-248">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-248">Description</span></span>**  
<span data-ttu-id="332f9-249">가상 컴퓨터가 잘못 된 상태 이거나 Windows 가상 PC 추가가 설치 되지 않았거나 사용 하도록 설정 되어 있지 않기 때문에 MED-V 호스트의 네트워크 구성 (브리지)을 가상 컴퓨터에 통신할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-249">The MED-V hostnetwork configuration (BRIDGED) could not be communicated to the virtual machine, most likely because the virtual machine is in a bad state or the Windows Virtual PC Additions were not installed or enabled.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-250">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-250">Solution</span></span>**  
<span data-ttu-id="332f9-251">가상 컴퓨터를 종료 하 고 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-251">Shut down and restart the virtual machine.</span></span> <span data-ttu-id="332f9-252">또한 가상 컴퓨터를 다시 설치 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-252">In addition, you might have to reinstall the virtual machine.</span></span>

### <span data-ttu-id="332f9-253">프린터 리디렉션</span><span class="sxs-lookup"><span data-stu-id="332f9-253">Printer Redirection</span></span>

### <span data-ttu-id="332f9-254">이벤트 ID 9001</span><span class="sxs-lookup"><span data-stu-id="332f9-254">Event ID 9001</span></span>

<span data-ttu-id="332f9-255">파일 사용 권한 오류.</span><span class="sxs-lookup"><span data-stu-id="332f9-255">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-256">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-256">Description</span></span>**  
<span data-ttu-id="332f9-257">최종 사용자는 읽기용으로 MED-V 프린터 파일을 열거나 만드는 데 필요한 폴더에 액세스할 수 있는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-257">The end user is not authorized to access the folder required to open or create the MED-V printer file for reading.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-258">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-258">Solution</span></span>**  
<span data-ttu-id="332f9-259">User\\AppData\\ 경로에 액세스할 수 있고 사용자에 게 읽기 및 쓰기 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-259">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="332f9-260">예를 들어 사용자가 "Matt"이 고 경로가 C:\\Users\\Matt\\AppData\\, 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-260">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\, and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="332f9-261">있는 경우 경로 C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ 및 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-261">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="332f9-262">이벤트 ID 9002</span><span class="sxs-lookup"><span data-stu-id="332f9-262">Event ID 9002</span></span>

<span data-ttu-id="332f9-263">파일 사용 권한 오류.</span><span class="sxs-lookup"><span data-stu-id="332f9-263">File Permission Error.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-264">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-264">Description</span></span>**  
<span data-ttu-id="332f9-265">최종 사용자에 게는 쓰기용으로 MED-V 프린터 파일을 열거나 만드는 데 필요한 폴더에 액세스할 수 있는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-265">The end user is not authorized to access the folder required to open or create the MED-V printer file for writing.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-266">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-266">Solution</span></span>**  
<span data-ttu-id="332f9-267">User\\AppData\\ 경로에 액세스할 수 있고 사용자에 게 읽기 및 쓰기 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-267">Ensure that the User\\AppData\\ path can be accessed, and that the user has permission to read and write to it.</span></span> <span data-ttu-id="332f9-268">예를 들어 사용자가 "Matt" 인 경우 경로 C:\\Users\\Matt\\AppData\\와 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-268">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="332f9-269">있는 경우 경로 C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ 및 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-269">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="332f9-270">이벤트 ID 9004</span><span class="sxs-lookup"><span data-stu-id="332f9-270">Event ID 9004</span></span>

<span data-ttu-id="332f9-271">MEDV 프린터 파일을 저장할 경로를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-271">Could not create path for storing MEDV printer files.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-272">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-272">Description</span></span>**  
<span data-ttu-id="332f9-273">프린터 리디렉션 서비스에서 파일에 액세스 하거나 프린터 정보를 저장 하는 데 필요한 디렉터리를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-273">The printer redirection service could not access files or create directories required for storing the printer information.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-274">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-274">Solution</span></span>**  
<span data-ttu-id="332f9-275">User\\AppData\\ 경로에 액세스할 수 있고 사용자에 게 읽기 및 쓰기 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-275">Verify that the User\\AppData\\ path can be accessed and that the user has permission to read and write to it.</span></span> <span data-ttu-id="332f9-276">예를 들어 사용자가 "Matt" 인 경우 경로 C:\\Users\\Matt\\AppData\\와 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-276">For example, if the user is "Matt", the path C:\\Users\\Matt\\AppData\\ and all files therein should have Read and Write permissions.</span></span> <span data-ttu-id="332f9-277">있는 경우 경로 C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ 및 포함 된 모든 파일에 읽기 및 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-277">And if it exists, the path C:\\Users\\Matt\\AppData\\Local\\Microsoft\\MEDV\\v2\\ and all files therein should have Read and Write permissions.</span></span>

### <span data-ttu-id="332f9-278">이벤트 ID 9005</span><span class="sxs-lookup"><span data-stu-id="332f9-278">Event ID 9005</span></span>

<span data-ttu-id="332f9-279">구성에서 VM 이름을 가져올 수 없습니다. 게스트 설치 관리자를 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-279">Couldn’t get VM name from configuration; cannot launch guest installer.</span></span> <span data-ttu-id="332f9-280">MED-V를 업데이트할 수 없습니다-호스트 네트워크가 검색 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-280">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-281">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-281">Description</span></span>**  
<span data-ttu-id="332f9-282">프린터 리디렉션 서비스가 med-v 구성에서 MED-V 작업 영역 이름을 가져올 수 없으며 MED-V 게스트에서 설치 관리자를 시작 하도록 Windows 가상 PC에 알릴 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-282">The printer redirection service was not able to obtain the MED-V workspace name from the MED-V configuration and cannot inform Windows Virtual PC to start the installer on the MED-V guest.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-283">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-283">Solution</span></span>**  
<span data-ttu-id="332f9-284">MED-V 작업 영역 이름이 설정 되어 있고 C:\\Users\\ &lt; *사용자* &gt; \ 가상 컴퓨터 디렉터리의 가상 컴퓨터 이름과 일치 하는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-284">Ensure that the MED-V workspace name is set and that it matches a virtual machine name in the C:\\Users\\&lt;*user*&gt;\\Virtual Machines directory.</span></span> <span data-ttu-id="332f9-285">MED-V 작업 영역 이름은 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-285">The MED-V workspace name is located at HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name.</span></span>

<span data-ttu-id="332f9-286">예를 들어 사용자가 "Matt"이 고 작업 영역 이름이 "mattsworkspace" 이면 HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name의 값은 "mattsworkspace" 이어야 하며 C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx. 파일이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-286">For example, if the user is "Matt" and the workspace name is "mattsworkspace", the value of HKLM\\SOFTWARE\\Microsoft\\Medv\\v2\\VM\\Name should be "mattsworkspace" and there should be a file that is named C:\\Users\\Matt\\Virtual Machines\\mattsworkspace.vcmx.</span></span>

### <span data-ttu-id="332f9-287">응용 프로그램 게시</span><span class="sxs-lookup"><span data-stu-id="332f9-287">Application Publishing</span></span>

### <span data-ttu-id="332f9-288">이벤트 ID 10015</span><span class="sxs-lookup"><span data-stu-id="332f9-288">Event ID 10015</span></span>

<span data-ttu-id="332f9-289">조정 프로세스 중에 파일 시스템 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-289">A file system error occurred during the reconcile process.</span></span> <span data-ttu-id="332f9-290">조정 프로세스는 파일 이름을 처리 하지 &lt; *filename* &gt; 않지만, 계속 해 서 다른 변경 내용을 처리 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-290">The reconcile process will not process the file &lt;*filename*&gt; but will continue to process any other changes.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-291">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-291">Description</span></span>**  
<span data-ttu-id="332f9-292">바로 가기를 만들거나 삭제 하는 동안 허가 되지 않은 액세스 또는 I/o 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-292">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-293">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-293">Solution</span></span>**  
<span data-ttu-id="332f9-294">파일 경로에 액세스할 수 있고 사용자에 게 지정 된 파일을 만들거나 삭제할 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-294">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="332f9-295">이벤트 ID 10021</span><span class="sxs-lookup"><span data-stu-id="332f9-295">Event ID 10021</span></span>

<span data-ttu-id="332f9-296">파일 &lt; *error\_information* &gt; 이름에 대 한 파일 작업 작업에 대 한 오류 오류 \ _information &lt; *\ _name* &gt; &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-296">Error &lt;*error\_information*&gt; for file operation &lt;*operation\_name*&gt; on file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-297">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-297">Description</span></span>**  
<span data-ttu-id="332f9-298">바로 가기를 만들거나 삭제 하는 동안 허가 되지 않은 액세스 또는 I/o 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-298">An unauthorized access or I/O error occurred when a shortcut was being created or deleted.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-299">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-299">Solution</span></span>**  
<span data-ttu-id="332f9-300">파일 경로에 액세스할 수 있고 사용자에 게 지정 된 파일을 만들거나 삭제할 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-300">Check that the file path can be accessed and that the user has permissions to create or delete the specified file.</span></span>

### <span data-ttu-id="332f9-301">게스트 패치</span><span class="sxs-lookup"><span data-stu-id="332f9-301">Guest Patching</span></span>

### <span data-ttu-id="332f9-302">이벤트 ID 11001</span><span class="sxs-lookup"><span data-stu-id="332f9-302">Event ID 11001</span></span>

<span data-ttu-id="332f9-303">게스트 웨이크업 작업 사용 메시지</span><span class="sxs-lookup"><span data-stu-id="332f9-303">Guest wakeup task usage message.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-304">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-304">Description</span></span>**  
<span data-ttu-id="332f9-305">/GuestWakeup 옵션을 사용 하 여 MedvHost.exe를 틀리게 실행 했거나 명령의 형식이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-305">MedvHost.exe with the /GuestWakeup option was executed incorrectly, or the command is formatted incorrectly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-306">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-306">Solution</span></span>**  
<span data-ttu-id="332f9-307">명령이 다음 형식으로 실행 되는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-307">Ensure that the command is executed with the following format:</span></span>

<span data-ttu-id="332f9-308">Medvhost.exe/GuestWakeup/d: &lt; *duration \ _in \ _minutes* &gt; /v: " &lt; *workspace \ _name* &gt; " 위치</span><span class="sxs-lookup"><span data-stu-id="332f9-308">Medvhost.exe /GuestWakeup /d:&lt; *duration\_in\_minutes*&gt; /v:”&lt; *workspace\_name*&gt;” where</span></span>

<span data-ttu-id="332f9-309">&lt;*기간 \ _in \ _minutes* &gt; 가상 컴퓨터가 활성 상태로 유지 되어야 하는 시간 (분)입니다 (기본값 240).</span><span class="sxs-lookup"><span data-stu-id="332f9-309">&lt;*duration\_in\_minutes*&gt; is the number of minutes that the virtual machine should stay awake (default is 240) and</span></span>

<span data-ttu-id="332f9-310">&lt;*작업 영역 \ _name* &gt; 은 활성화 되어야 하는 가상 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-310">&lt;*workspace\_name*&gt; is the name of the virtual machine that should be awakened.</span></span>

### <span data-ttu-id="332f9-311">이벤트 ID 11002</span><span class="sxs-lookup"><span data-stu-id="332f9-311">Event ID 11002</span></span>

<span data-ttu-id="332f9-312">MED-V를 업데이트할 수 없습니다-호스트 네트워크가 검색 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-312">Cannot update MED-V – No host network detected.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-313">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-313">Description</span></span>**  
<span data-ttu-id="332f9-314">호스트 네트워크 연결이 검색 되지 않아 게스트 패치가 완료 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-314">Guest patching could not finish because no host network connection was detected.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-315">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-315">Solution</span></span>**  
<span data-ttu-id="332f9-316">게스트 패치를 실행 하기 전에 MED-V 호스트를 활성 네트워크 연결에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-316">Connect the MED-V host to an active network connection before you run guest patching.</span></span>

### <span data-ttu-id="332f9-317">이벤트 ID 11003</span><span class="sxs-lookup"><span data-stu-id="332f9-317">Event ID 11003</span></span>

<span data-ttu-id="332f9-318">MED-V를 업데이트할 수 없습니다. A/C powerFailed가 실행 되 고 있지 않습니다. 파이프 서버를 만들지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-318">Cannot update MED-V – Host not running on A/C powerFailed to create pipe server.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-319">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-319">Description</span></span>**  
<span data-ttu-id="332f9-320">호스트가 전원 코드 대신 배터리 전원으로 실행 되는 것으로 나타나기 때문에 게스트 패치가 완료 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-320">Guest patching could not finish because the host appears to be running on battery power instead of from a power cord.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-321">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-321">Solution</span></span>**  
<span data-ttu-id="332f9-322">게스트 패치를 실행 하기 전에 호스트 컴퓨터를 전원 코드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-322">Connect the host computer to a power cord before you run guest patching.</span></span>

### <span data-ttu-id="332f9-323">클라이언트 UX</span><span class="sxs-lookup"><span data-stu-id="332f9-323">Client UX</span></span>

### <span data-ttu-id="332f9-324">이벤트 ID 14003</span><span class="sxs-lookup"><span data-stu-id="332f9-324">Event ID 14003</span></span>

<span data-ttu-id="332f9-325">다음 용지함 상태 메시지가 너무 길어서 표시할 수 없습니다: &lt; *용지함 \ _status \ _message*&gt;</span><span class="sxs-lookup"><span data-stu-id="332f9-325">The following tray status message was too long and could not be displayed: &lt;*tray\_status\_message*&gt;</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-326">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-326">Description</span></span>**  
<span data-ttu-id="332f9-327">MED-V가 트레이 도구 설명 또는 풍선 메시지에 비해 너무 긴 예기치 않은 문자열을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-327">MED-V created an unanticipated string that was too long for the tray tooltip or balloon message.</span></span> <span data-ttu-id="332f9-328">그 결과 표시 된 메시지가 잘렸습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-328">As a result, the displayed message was truncated.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-329">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-329">Solution</span></span>**  
<span data-ttu-id="332f9-330">이 오류는 MED-V가 도구 설명 텍스트를 무작위로 만드는 경우 발생할 수 있는 드문 경우입니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-330">This is a rare error that can occur when MED-V is randomly creating the tooltip text.</span></span> <span data-ttu-id="332f9-331">해결 방법이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-331">There is no solution.</span></span>

### <span data-ttu-id="332f9-332">이벤트 ID 14004</span><span class="sxs-lookup"><span data-stu-id="332f9-332">Event ID 14004</span></span>

<span data-ttu-id="332f9-333">처리 되지 않은 예외로 인해 MED-V가 중지 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-333">MED-V stopped due to an unhandled exception.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-334">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-334">Description</span></span>**  
<span data-ttu-id="332f9-335">처리 되지 않은 예외로 인해 MED-V가 예기치 않게 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-335">An unhandled exception caused MED-V to stop unexpectedly.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-336">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-336">Solution</span></span>**  
<span data-ttu-id="332f9-337">MED-V를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-337">Restart MED-V.</span></span>

### <span data-ttu-id="332f9-338">이벤트 ID 14005</span><span class="sxs-lookup"><span data-stu-id="332f9-338">Event ID 14005</span></span>

<span data-ttu-id="332f9-339">서버에서 mutex을 만들려고 했지만 이미 존재 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-339">Server attempted to create mutex but it already existed.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-340">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-340">Description</span></span>**  
<span data-ttu-id="332f9-341">MedvHost.exe의 두 번째 인스턴스는 메모리에 남아 있습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-341">A second instance of MedvHost.exe is stuck in memory.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-342">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-342">Solution</span></span>**  
<span data-ttu-id="332f9-343">TaskManager를 열고 모든 MedvHost.exe 프로세스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-343">Open TaskManager and end all MedvHost.exe processes.</span></span>

### <span data-ttu-id="332f9-344">이벤트 ID 14006</span><span class="sxs-lookup"><span data-stu-id="332f9-344">Event ID 14006</span></span>

<span data-ttu-id="332f9-345">레지스트리 값 레지스트리를 수정 또는 삭제 하는 중 오류가 발생 했습니다 &lt; . *\ _value* &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-345">Error modifying or deleting registry value &lt;*registry\_value*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-346">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-346">Description</span></span>**  
<span data-ttu-id="332f9-347">MED-V는 레지스트리의 지정 된 항목을 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-347">MED-V is unable to modify the specified entry in the registry.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-348">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-348">Solution</span></span>**  
<span data-ttu-id="332f9-349">관리 자격 증명을 사용 하 여 MED-V를 설치 하거나 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-349">Ensure that you install or uninstall MED-V with administrative credentials.</span></span>

### <span data-ttu-id="332f9-350">이벤트 ID 14007</span><span class="sxs-lookup"><span data-stu-id="332f9-350">Event ID 14007</span></span>

<span data-ttu-id="332f9-351">지정 된 파일 ( &lt; *filename* &gt; )이 잘못 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-351">The file specified (&lt;*filename*&gt;) is not valid.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-352">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-352">Description</span></span>**  
<span data-ttu-id="332f9-353">설치 또는 제거 하는 동안 손상 된 임시 파일이 MED-V 호스트에 전달 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-353">During install or uninstall, a corrupted temp file was passed to MED-V host.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-354">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-354">Solution</span></span>**  
<span data-ttu-id="332f9-355">Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-355">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="332f9-356">이벤트 ID 14008</span><span class="sxs-lookup"><span data-stu-id="332f9-356">Event ID 14008</span></span>

<span data-ttu-id="332f9-357">파일을 찾을 수 없습니다: &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-357">File not found: &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-358">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-358">Description</span></span>**  
<span data-ttu-id="332f9-359">설치 또는 제거 하는 동안 필요한 임시 파일의 경로를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-359">During install or uninstall, a path of a required temp file was not found.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-360">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-360">Solution</span></span>**  
<span data-ttu-id="332f9-361">Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-361">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span>

### <span data-ttu-id="332f9-362">이벤트 ID 14009</span><span class="sxs-lookup"><span data-stu-id="332f9-362">Event ID 14009</span></span>

<span data-ttu-id="332f9-363">매개 변수 파일 이름을 읽을 수 없습니다 &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-363">Unable to read parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-364">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-364">Description</span></span>**  
<span data-ttu-id="332f9-365">설치 또는 제거 프로세스가 진행 되는 동안 MED-V가 임시 파일을 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-365">During the install or uninstall process, MED-V was unable to read a temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-366">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-366">Solution</span></span>**  
<span data-ttu-id="332f9-367">Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-367">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="332f9-368">또한 사용자에 게 Temp 폴더에 대 한 필요한 권한과 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-368">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="332f9-369">이벤트 ID 14010</span><span class="sxs-lookup"><span data-stu-id="332f9-369">Event ID 14010</span></span>

<span data-ttu-id="332f9-370">매개 변수 파일 이름을 역직렬화 하는 동안 오류가 발생 했습니다 &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-370">Error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-371">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-371">Description</span></span>**  
<span data-ttu-id="332f9-372">설치 또는 제거 프로세스가 진행 되는 동안 MED-V에 손상 된 임시 파일이 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-372">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-373">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-373">Solution</span></span>**  
<span data-ttu-id="332f9-374">Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-374">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="332f9-375">또한 사용자에 게 Temp 폴더에 대 한 필요한 권한과 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-375">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="332f9-376">이벤트 ID 14011</span><span class="sxs-lookup"><span data-stu-id="332f9-376">Event ID 14011</span></span>

<span data-ttu-id="332f9-377">매개 변수 파일 이름을 역직렬화 하는 동안 예기치 않은 오류가 발생 했습니다 &lt; *filename* &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-377">Unexpected error deserializing parameter file &lt;*filename*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-378">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-378">Description</span></span>**  
<span data-ttu-id="332f9-379">설치 또는 제거 프로세스가 진행 되는 동안 MED-V에 손상 된 임시 파일이 발견 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-379">During the install or uninstall process, MED-V encountered a corrupted temp file.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-380">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-380">Solution</span></span>**  
<span data-ttu-id="332f9-381">Temp 폴더의 모든 파일을 삭제 하 고 MED-V를 다시 설치 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-381">Delete all files in the Temp folder and reinstall or uninstall MED-V.</span></span> <span data-ttu-id="332f9-382">또한 사용자에 게 Temp 폴더에 대 한 필요한 권한과 권한이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-382">In addition, verify that the user has the necessary rights and permissions to the Temp folder.</span></span>

### <span data-ttu-id="332f9-383">이벤트 ID 14012</span><span class="sxs-lookup"><span data-stu-id="332f9-383">Event ID 14012</span></span>

<span data-ttu-id="332f9-384">폴더 폴더의 설정 권한이 &lt; *folder\_name* &gt; 사용자 &lt; *사용자 이름*에 대해 \ _name 하는 동안 예기치 않은 오류가 발생 했습니다 &gt; .</span><span class="sxs-lookup"><span data-stu-id="332f9-384">Unexpected error when settings rights on folder &lt;*folder\_name*&gt; for user &lt;*username*&gt;.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-385">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-385">Description</span></span>**  
<span data-ttu-id="332f9-386">MED-V가 설치 중 특정 폴더에 대 한 권한 및 사용 권한을 설정할 수 없는 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-386">An error occurs when MED-V is unable to set rights and permissions on certain folders during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-387">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-387">Solution</span></span>**  
<span data-ttu-id="332f9-388">다음 폴더에 대 한 관리자 권한을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-388">Check the administrator rights to the following folders:</span></span>

<span data-ttu-id="332f9-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span><span class="sxs-lookup"><span data-stu-id="332f9-389">@"%ProgramData%\\Microsoft\\Medv\\AllUsers"</span></span>

<span data-ttu-id="332f9-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span><span class="sxs-lookup"><span data-stu-id="332f9-390">@"%ProgramData%\\Microsoft\\Medv\\MedvLock"</span></span>

<span data-ttu-id="332f9-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span><span class="sxs-lookup"><span data-stu-id="332f9-391">@"%ProgramData%\\Microsoft\\Medv\\Monitoring"</span></span>

### <span data-ttu-id="332f9-392">이벤트 ID 14013</span><span class="sxs-lookup"><span data-stu-id="332f9-392">Event ID 14013</span></span>

<span data-ttu-id="332f9-393">잠금 파일을 만들 때 예기치 않은 오류가 발생 했습니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-393">Unexpected error when creating lock file.</span></span>

<a href="" id="description"></a>**<span data-ttu-id="332f9-394">설명</span><span class="sxs-lookup"><span data-stu-id="332f9-394">Description</span></span>**  
<span data-ttu-id="332f9-395">MED-V가 설치 중 @ "%ProgramData%\\Microsoft\\Medv\\MedvLock" 폴더에 파일을 만들 수 없는 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-395">An error occurs when MED-V is unable to create a file in the @"%ProgramData%\\Microsoft\\Medv\\MedvLock" folder during installation.</span></span>

<a href="" id="solution"></a>**<span data-ttu-id="332f9-396">해결 방법</span><span class="sxs-lookup"><span data-stu-id="332f9-396">Solution</span></span>**  
<span data-ttu-id="332f9-397">MedvLock 폴더에 대 한 관리자 권한을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="332f9-397">Check the administrator rights to the MedvLock folder.</span></span>

## <span data-ttu-id="332f9-398">관련 항목</span><span class="sxs-lookup"><span data-stu-id="332f9-398">Related topics</span></span>


[<span data-ttu-id="332f9-399">MED-V 문제 해결</span><span class="sxs-lookup"><span data-stu-id="332f9-399">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





