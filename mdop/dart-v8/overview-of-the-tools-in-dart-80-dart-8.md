---
title: DaRT 8.0의 도구 개요
description: DaRT 8.0의 도구 개요
author: dansimp
ms.assetid: 1766c82e-c099-47d4-b186-4689b026a7e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: a058f6018888f446782aa8f3a18ee89570840c2a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824618"
---
# <span data-ttu-id="dc94f-103">DaRT 8.0의 도구 개요</span><span class="sxs-lookup"><span data-stu-id="dc94f-103">Overview of the Tools in DaRT 8.0</span></span>


<span data-ttu-id="dc94f-104">Office 진단 및 **복구 도구 집합** 창에서 Microsoft 진단 및 복구 도구 집합 (dart) 8.0의 경우 dart 8.0 복구 이미지를 만들 때 포함 하는 개별 도구를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you can start any of the individual tools that you include when you create the DaRT 8.0 recovery image.</span></span> <span data-ttu-id="dc94f-105">**진단 및 복구 도구 집합** 창에 액세스 하는 방법에 대 한 자세한 내용은 [DaRT 복구 이미지를 사용 하 여 로컬 컴퓨터를 복구 하는 방법을](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc94f-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="dc94f-106">사용할 수 있는 경우 **진단 및 복구 도구 집합** 창에서 **솔루션 마법사** 를 사용 하 여 마법사가 제공 하는 간략 한 인터뷰를 기반으로 특정 문제를 가장 잘 해결 하는 도구를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="dc94f-107">DaRT 도구 살펴보기</span><span class="sxs-lookup"><span data-stu-id="dc94f-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="dc94f-108">DaRT 8.0 도구에 대 한 설명은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-108">A description of the DaRT 8.0 tools follows.</span></span>

### <span data-ttu-id="dc94f-109">컴퓨터 관리</span><span class="sxs-lookup"><span data-stu-id="dc94f-109">Computer Management</span></span>

<span data-ttu-id="dc94f-110">**컴퓨터 관리** 는 문제 컴퓨터 문제를 해결 하는 데 도움이 되는 Windows 관리 도구 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="dc94f-111">DaRT의 **컴퓨터 관리** 도구를 사용 하 여 시스템 정보 및 이벤트 로그를 보고, 디스크를 관리 하 고, autoruns를 나열 하 고, 서비스 및 드라이버를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="dc94f-112">**컴퓨터 관리** 콘솔은 Windows 운영 체제를 시작할 수 없는 문제를 진단 하 고 해결 하는 데 도움이 되도록 사용자 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="dc94f-113">**참고**  DaRT로 동적 디스크 복구는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="dc94f-114">충돌 분석기</span><span class="sxs-lookup"><span data-stu-id="dc94f-114">Crash Analyzer</span></span>

<span data-ttu-id="dc94f-115">**충돌 분석기 마법사** 를 사용 하 여 복구 하려는 Windows 운영 체제의 메모리 덤프 파일을 분석 하 여 컴퓨터 오류의 원인을 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="dc94f-116">**충돌 분석기** 는 컴퓨터에 오류가 발생 한 드라이버에 대 한 메모리 덤프 파일을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="dc94f-117">그런 다음 **컴퓨터 관리** 도구의 **서비스 및 드라이버** 노드를 사용 하 여 문제 장치 드라이버를 사용 하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="dc94f-118">**충돌 분석기 마법사** 에는 복구 하려는 운영 체제용 Windows 및 기호 파일에 대 한 디버깅 도구가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="dc94f-119">DaRT 복구 이미지를 만들 때 두 요구 사항을 모두 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="dc94f-120">복구 이미지에 포함 되지 않은 경우 복구 하는 컴퓨터에서 해당 사용자에 게 액세스할 수 없는 경우에는 메모리 덤프 파일을 다른 컴퓨터에 복사 하 고 독립 실행형 버전의 **크래시 분석기** 를 사용 하 여 문제를 진단 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="dc94f-121">컴퓨터를 이미지로 한 경우에도 **충돌 분석기** 를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="dc94f-122">사용자 환경에서 문제를 일으키는 결함 있는 드라이버가 이미지에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="dc94f-123">**충돌 분석기**를 실행 하 여 문제 드라이버를 식별 하 고 이미지 안정성을 높일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="dc94f-124">**충돌 분석기**에 대 한 자세한 내용은 [충돌 분석기를 사용 하 여 시스템 오류 진단을](diagnosing-system-failures-with-crash-analyzer--dart-8.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc94f-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span></span>

### <span data-ttu-id="dc94f-125">Defender</span><span class="sxs-lookup"><span data-stu-id="dc94f-125">Defender</span></span>

<span data-ttu-id="dc94f-126">**중요**  DaRT Defender가 배포 된 환경에서는 맬웨어 감지를 위해 WDO (Microsoft Defender Offline) 보호 이미지를 대신 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-126">**Important** Environments with the DaRT Defender deployed should instead use the Microsoft Defender Offline (WDO) protection image for malware detection.</span></span> <span data-ttu-id="dc94f-127">Defender 도구가 DaRT로 통합 되는 방식 때문에 지원 되는 모든 DaRT 버전 배포는 해당 DaRT 이미지에 맬웨어 방지 업데이트를 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-127">Because of how the Defender tool integrates into DaRT, all supported DaRT version deployments cannot apply these anti-malware updates to their DaRT images.</span></span> <span data-ttu-id="dc94f-128">자세한 내용은 [Microsoft 진단 및 복구 도구 집합 (DaRT) 사용자가 맬웨어 검색에 Microsoft Defender offline (WDO)을 사용 해야 함-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc94f-128">For more information, see  [Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span></span>

 

<span data-ttu-id="dc94f-129">**Defender** 는 맬웨어 및 원치 않는 소프트웨어를 검색 하 고 보안 위험을 경고할 수 있도록 도와줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-129">**Defender** can help detect malware and unwanted software and warn you of security risks.</span></span> <span data-ttu-id="dc94f-130">이 도구를 사용 하 여 설치 된 Windows 운영 체제가 실행 되 고 있지 않은 경우에도 컴퓨터를 검색 하 고 맬웨어를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-130">You can use this tool to scan a computer for and remove malware even when the installed Windows operating system is not running.</span></span> <span data-ttu-id="dc94f-131">**Defender** 에서 악의적 또는 원치 않는 소프트웨어를 감지 하면 각 항목을 제거, 격리 또는 허용할 것인지 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-131">When **Defender** detects malicious or unwanted software, it prompts you to remove, quarantine, or allow for each item.</span></span>

<span data-ttu-id="dc94f-132">루트킷을 사용 하는 맬웨어는 실행 중인 운영 체제에서 자신을 마스킹할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-132">Malware that uses rootkits can mask itself from the running operating system.</span></span> <span data-ttu-id="dc94f-133">Rootkit를 사용 하는 바이러스 또는 스파이웨어가 컴퓨터에 있는 경우 대부분의 실시간 스캐닝 및 제거 도구가 더 이상이를 보거나 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-133">If a rootkit-enabled virus or spyware is in a computer, most real-time scanning and removal tools can no longer see it or remove it.</span></span> <span data-ttu-id="dc94f-134">문제가 있는 컴퓨터를 DaRT로 부팅 하 고 설치 된 운영 체제는 오프 라인 상태 이기 때문에 자신을 마스킹할 수 없는 rootkit 감지 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-134">Because you boot the problem computer into DaRT and the installed operating system is offline, you can detect the rootkit without it being able to mask itself.</span></span>

### <span data-ttu-id="dc94f-135">디스크 지휘관</span><span class="sxs-lookup"><span data-stu-id="dc94f-135">Disk Commander</span></span>

<span data-ttu-id="dc94f-136">**디스크** 를 통해 다음 복구 프로세스 중 하나를 사용 하 여 디스크 파티션이나 볼륨을 복구 하 고 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-136">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="dc94f-137">MBR (마스터 부트 레코드) 복원</span><span class="sxs-lookup"><span data-stu-id="dc94f-137">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="dc94f-138">하나 이상의 손실 된 볼륨 복구</span><span class="sxs-lookup"><span data-stu-id="dc94f-138">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="dc94f-139">디스크에서 파티션 테이블 복원 **지휘관** 백업</span><span class="sxs-lookup"><span data-stu-id="dc94f-139">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="dc94f-140">디스크에 파티션 테이블 저장 **지휘관** 백업</span><span class="sxs-lookup"><span data-stu-id="dc94f-140">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="dc94f-141">**경고가**  **디스크 사용을** 복구 하기 전에 디스크를 백업 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-141">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="dc94f-142">**디스크 지휘관**을 사용 하 여 볼륨을 손상 시킬 수 있으며,이를 액세스할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-142">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="dc94f-143">또한 디스크의 볼륨은 파티션 테이블을 공유 하기 때문에 한 볼륨에 대 한 변경 내용이 다른 볼륨에 영향을 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-143">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="dc94f-144">**참고**  DaRT로 동적 디스크 복구는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-144">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="dc94f-145">디스크 지우기</span><span class="sxs-lookup"><span data-stu-id="dc94f-145">Disk Wipe</span></span>

<span data-ttu-id="dc94f-146">디스크 **정리** 를 사용 하 여 디스크 또는 볼륨의 모든 데이터를 삭제할 수 있으며, 이렇게 하면 하드 디스크 드라이브의 서식을 다시 설정한 후 남아 있는 데이터도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-146">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="dc94f-147">**디스크 정리** 를 사용 하 여 단일 단계 덮어쓰기 또는 4 단계 덮어쓰기 중에서 선택 하 여 현재 미국 방어 표준의 부서에 부합 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-147">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="dc94f-148">**경고가**  디스크 또는 볼륨을 초기화 한 후에는 데이터를 복구할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-148">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="dc94f-149">볼륨을 지우기 전에 크기 및 레이블을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-149">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="dc94f-150">Explorer</span><span class="sxs-lookup"><span data-stu-id="dc94f-150">Explorer</span></span>

<span data-ttu-id="dc94f-151">**Explorer** 도구를 사용 하 여 컴퓨터를 복구 하거나 다시 저장 하기 전에 사용자가 로컬 드라이브에 저장 한 중요 한 데이터를 제거할 수 있도록 컴퓨터의 파일 시스템 및 네트워크 공유 위치를 탐색 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-151">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="dc94f-152">네트워크 공유에 드라이브 문자를 매핑할 수 있기 때문에 컴퓨터에서 네트워크로 파일을 쉽게 복사 하 여 네트워크에서 컴퓨터로 이동 하 여 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-152">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="dc94f-153">파일 복원</span><span class="sxs-lookup"><span data-stu-id="dc94f-153">File Restore</span></span>

<span data-ttu-id="dc94f-154">**파일 복원을** 통해 실수로 삭제 되었거나 너무 커서 휴지통에 맞지 않는 파일을 복원 하려고 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-154">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="dc94f-155">**파일 복원은** 일반 디스크 볼륨에 국한 되지 않지만 손실 된 볼륨 또는 BitLocker로 암호화 된 볼륨에서 파일을 찾아 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-155">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="dc94f-156">**참고**  DaRT로 동적 디스크 복구는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-156">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="dc94f-157">파일 검색</span><span class="sxs-lookup"><span data-stu-id="dc94f-157">File Search</span></span>

<span data-ttu-id="dc94f-158">컴퓨터를 reimaging 전에 로컬 하드 디스크에서 파일을 복구 하는 것이 중요 하며, 특히 사용자가 파일을 백업 하거나 다른 위치에 저장 하지 않았을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-158">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="dc94f-159">**검색** 도구는 파일 경로를 모르거나 모든 로컬 하드 디스크에서 일반적인 종류의 파일을 검색할 때 문서를 찾는 데 사용할 수 있는 **파일 검색** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-159">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="dc94f-160">특정 경로에서 특정 파일 이름 패턴을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-160">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="dc94f-161">또한 결과를 날짜 범위 또는 크기 범위로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-161">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="dc94f-162">핫픽스 제거</span><span class="sxs-lookup"><span data-stu-id="dc94f-162">Hotfix Uninstall</span></span>

<span data-ttu-id="dc94f-163">**핫픽스 제거 마법사** 를 사용 하면 복구 하려는 컴퓨터의 Windows 운영 체제에서 핫픽스 또는 서비스 팩을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-163">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="dc94f-164">운영 체제를 시작할 수 없도록 핫픽스 또는 서비스 팩이 의심 되는 경우이 도구를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-164">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="dc94f-165">이 도구를 사용 하 여 한 번에 하나의 핫픽스로 제거 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-165">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="dc94f-166">**중요**  핫픽스를 설치한 후 설치 또는 업데이트 된 프로그램이 핫픽스를 제거한 후에도 올바르게 작동 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-166">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="dc94f-167">Locksmith</span><span class="sxs-lookup"><span data-stu-id="dc94f-167">Locksmith</span></span>

<span data-ttu-id="dc94f-168">**Locksmith 마법사** 를 사용 하면 분석 하거나 복구 하는 Windows 운영 체제의 로컬 계정에 대 한 암호를 설정 하거나 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-168">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="dc94f-169">현재 암호를 몰라도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-169">You do not have to know the current password.</span></span> <span data-ttu-id="dc94f-170">그러나 설정 하는 암호는 로컬 그룹 정책 개체에 정의 된 요구 사항을 준수 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-170">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="dc94f-171">여기에는 암호 길이 및 복잡성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-171">This includes password length and complexity.</span></span>

<span data-ttu-id="dc94f-172">로컬 관리자 계정 등의 로컬 계정에 대 한 암호를 알 수 없는 경우에는 **Locksmith** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-172">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="dc94f-173">**Locksmith** 를 사용 하 여 도메인 계정에 대 한 암호를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-173">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="dc94f-174">레지스트리 편집기</span><span class="sxs-lookup"><span data-stu-id="dc94f-174">Registry Editor</span></span>

<span data-ttu-id="dc94f-175">**레지스트리 편집기** 를 사용 하 여 분석 하거나 복구 하는 Windows 운영 체제의 레지스트리를 액세스 하 고 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-175">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="dc94f-176">여기에는 키와 값 추가, 제거, 편집, 레지스트리 (.reg) 파일 가져오기 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-176">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="dc94f-177">**경고가**  **레지스트리 편집기**를 사용 하 여 레지스트리를 잘못 변경 하는 경우 심각한 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-177">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="dc94f-178">이러한 문제를 해결하려면 운영 체제를 다시 설치해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-178">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="dc94f-179">레지스트리를 변경 하기 전에 컴퓨터에 있는 중요 한 데이터를 백업 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-179">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="dc94f-180">레지스트리 변경에 따른 모든 책임은 사용자에 게 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-180">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="dc94f-181">SFC Scan</span><span class="sxs-lookup"><span data-stu-id="dc94f-181">SFC Scan</span></span>

<span data-ttu-id="dc94f-182">**SFC Scan** 도구는 **시스템 파일 복구 마법사** 를 시작 하 고 설치 된 Windows 운영 체제의 시작을 방해 하는 시스템 파일을 복구할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-182">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="dc94f-183">**시스템 파일 복구 마법사** 는 손상 되거나 누락 된 시스템 파일을 자동으로 복구 하거나 복구를 수행 하기 전에 메시지를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-183">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="dc94f-184">솔루션 마법사</span><span class="sxs-lookup"><span data-stu-id="dc94f-184">Solution Wizard</span></span>

<span data-ttu-id="dc94f-185">**솔루션 마법사** 는 일련의 질문을 제시 하 고 사용자의 답변에 따라 상황에 가장 적합 한 도구를 추천 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-185">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="dc94f-186">이 마법사는 DaRT의 도구에 익숙하지 않을 때 사용할 도구를 결정 하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-186">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="dc94f-187">TCP/IP 구성</span><span class="sxs-lookup"><span data-stu-id="dc94f-187">TCP/IP Config</span></span>

<span data-ttu-id="dc94f-188">문제가 있는 컴퓨터를 DaRT로 부팅 하면 DHCP (동적 호스트 구성 프로토콜)에서 자동으로 TCP/IP 구성 (IP 주소 및 DNS 서버)을 얻도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-188">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="dc94f-189">DHCP를 사용할 수 없는 경우 **Tcp/ip 구성** 도구를 사용 하 여 tcp/ip를 수동으로 구성 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-189">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="dc94f-190">먼저 네트워크 어댑터를 선택한 다음 해당 어댑터에 대 한 IP 주소와 DNS 서버를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc94f-190">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="dc94f-191">관련 항목</span><span class="sxs-lookup"><span data-stu-id="dc94f-191">Related topics</span></span>


[<span data-ttu-id="dc94f-192">DaRT 8.0 시작</span><span class="sxs-lookup"><span data-stu-id="dc94f-192">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

 

 





