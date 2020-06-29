---
title: MED-V 가상 하드 디스크 압축
description: MED-V 가상 하드 디스크 압축
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823278"
---
# <span data-ttu-id="0eff5-103">MED-V 가상 하드 디스크 압축</span><span class="sxs-lookup"><span data-stu-id="0eff5-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="0eff5-104">이 기능은 선택 사항 이지만, Windows 가상 PC 이미지를 구성 하기 전에 VHD (가상 하드 디스크)를 압축 하 여 빈 디스크 공간을 확보 하 고 VHD 크기를 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="0eff5-105">**중요**  계속 하기 전에 Windows XP 이미지의 백업 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="0eff5-106">가상 하드 디스크 준비</span><span class="sxs-lookup"><span data-stu-id="0eff5-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="0eff5-107">Windows XP 이미지를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="0eff5-108">**시작**을 클릭 하 고 **모든 프로그램**, **Windows 가상 pc**, **windows 가상 PC**를 차례로 클릭 한 다음 windows XP 이미지를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="0eff5-109">DLL 캐시를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="0eff5-110">가상 머신의 명령 프롬프트에서 **sfc/cachesize = 1**을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="0eff5-111">가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="0eff5-112">가상 머신의 명령 프롬프트에서 **sfc/purgecache**를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="0eff5-113">설치 관리자, 임시 파일, 로그 파일, 페이지 파일, 공유 폴더 등 불필요 한 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="0eff5-114">시스템 복원을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-114">Turn off System Restore.</span></span> <span data-ttu-id="0eff5-115">Sysprep.inf 파일에서이 단계를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="0eff5-116">**제어판**에서 **시스템**을 두 번 클릭 한 다음 **시스템 복원** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="0eff5-117">**시스템 복원 해제**를 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="0eff5-118">최대 이벤트 로그 크기를 설정 하 고 모든 이벤트를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="0eff5-119">이벤트 뷰어를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-119">Open the event viewer.</span></span>

        <span data-ttu-id="0eff5-120">**시작**, **제어판**을 차례로 클릭 하 고 **관리 도구**를 두 번 클릭 한 다음 **이벤트 뷰어**를 두 번 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="0eff5-121">**응용 프로그램**을 마우스 오른쪽 단추로 클릭 하 고 **속성**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="0eff5-122">**로그 크기** 영역에서 **최대 로그 크기** 를 512kb로 설정한 다음 **필요에 따라 이벤트 덮어쓰기를**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="0eff5-123">**로그 지우기를**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-123">Click **Clear Log**.</span></span> <span data-ttu-id="0eff5-124">**이벤트 뷰어** 대화 상자가 나타나면 **아니요**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="0eff5-125">**속성** 창에서 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="0eff5-126">**보안** 및 **시스템** 로그에 대해 a ~ e 단계를 반복 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="0eff5-127">디스크 정리 도구를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="0eff5-128">**시작**을 클릭 하 고 **모든 프로그램**, **보조 프로그램**, **시스템 도구**를 차례로 클릭 한 다음 **디스크 정리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="0eff5-129">응용 프로그램에 맞게 페이지 파일을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="0eff5-130">**제어판**에서 **시스템**을 두 번 클릭 한 다음 **고급** 탭을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="0eff5-131">**성능** 영역에서 **설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="0eff5-132">**가상 메모리** 영역에서 **변경을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="0eff5-133">페이지 파일 설정을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="0eff5-134">Windows XP 이미지를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="0eff5-135">가상 하드 디스크의 조각 모음 및 사전 압축</span><span class="sxs-lookup"><span data-stu-id="0eff5-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="0eff5-136">Windows 7을 실행 하는 호스트 컴퓨터의 **제어판** 에서 **관리 도구**를 클릭 하 고 **컴퓨터 관리**를 두 번 클릭 한 다음 **디스크 관리**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="0eff5-137">디스크 관리 콘솔을 사용 하 여 가상 하드 디스크를 연결 (탑재) 한 다음 디스크 조각을 모읍니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="0eff5-138">ISO 추출 도구를 사용 하 여 \\Program Files\\Windows Virtual PC\\Integration 구성 요소 폴더에 있는 precompact .iso를 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="0eff5-139">precompact.exe 프로그램을 사용 하 여 Windows XP 가상 하드 디스크를 압축 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="0eff5-140">디스크 관리 콘솔을 사용 하 여 가상 하드 디스크를 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="0eff5-141">가상 하드 디스크 압축</span><span class="sxs-lookup"><span data-stu-id="0eff5-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="0eff5-142">Windows 가상 PC를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="0eff5-143">**시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **windows 가상 Pc**를 클릭 하 고 **windows 가상 pc**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="0eff5-144">Windows XP 이미지를 마우스 오른쪽 단추로 클릭 하 고 **설정을**선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="0eff5-145">Windows XP 이미지에 해당 하는 **하드 디스크** 를 클릭 한 다음 **수정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="0eff5-146">**가상 하드 디스크 압축**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="0eff5-147">**압축** 을 클릭 한 다음 **확인을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="0eff5-148">압축 한 가상 하드 디스크의 백업 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0eff5-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="0eff5-149">관련 항목</span><span class="sxs-lookup"><span data-stu-id="0eff5-149">Related topics</span></span>


[<span data-ttu-id="0eff5-150">MED-V에 대한 Windows 가상 PC 이미지 구성</span><span class="sxs-lookup"><span data-stu-id="0eff5-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="0eff5-151">MED-V에 대한 기술 참조</span><span class="sxs-lookup"><span data-stu-id="0eff5-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





