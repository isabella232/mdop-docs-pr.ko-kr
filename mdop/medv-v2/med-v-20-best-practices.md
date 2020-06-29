---
title: MED-V 2.0 모범 사례
description: MED-V 2.0 모범 사례
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826113"
---
# <span data-ttu-id="6a387-103">MED-V 2.0 모범 사례</span><span class="sxs-lookup"><span data-stu-id="6a387-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="6a387-104">엔터프라이즈에서 MED-V를 계획, 배포 및 관리 하는 경우 유용한 모범 사례를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="6a387-105">자동으로 설치 프로그램을 실행 하도록 구성</span><span class="sxs-lookup"><span data-stu-id="6a387-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="6a387-106">원하는 설정을 지정할 수 있지만, 처음에는 설치 프로그램을 **무인** 모드로 실행할 수 있도록 sysprep.inf 파일을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="6a387-107">이렇게 하려면 **설치 관리자** 마법사를 계속 진행할 때 필요한 모든 설정 정보를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="6a387-108">MED-V 이미지를 구성 하는 방법에 대 한 자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a387-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="6a387-109">가상 머신에서 복원 지점 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="6a387-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="6a387-110">MED-V 작업 영역 패키지를 만들기 전에 가상 컴퓨터에서 복원 지점을 사용 하지 않도록 설정 하 여 차이점 보관용 디스크에 대 한 무제한 연결을 방지 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="6a387-111">자세한 내용은 [WINDOWS XP ()에서 시스템 복원을 해제 하 고 설정 하는 방법](https://go.microsoft.com/fwlink/?LinkId=195927) 을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="6a387-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="6a387-112">로컬 프로필을 사용 하도록 MED-V 이미지 구성</span><span class="sxs-lookup"><span data-stu-id="6a387-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="6a387-113">Windows XP에 대 한 응용 프로그램 호환성 환경에 적합 한 정책만 적용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="6a387-114">예를 들어 데스크톱 사용자 지정 정책을 일반적으로 적용할 필요는 없으며 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="6a387-115">로컬 프로필만 허용 하는 방법에 대 한 자세한 내용은 [로밍 사용자 프로필 ()에 대 한 그룹 정책 설정](https://go.microsoft.com/fwlink/?LinkId=205072) ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="6a387-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="6a387-116">그룹 정책 성능 업데이트 구성</span><span class="sxs-lookup"><span data-stu-id="6a387-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="6a387-117">기본적으로 그룹 정책은 한 번에 1 바이트씩 컴퓨터에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="6a387-118">이로 인해 MED-V가 도메인에 가입 되어 있는 경우 지연이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="6a387-119">그룹 정책의 성능을 높이려면 다음 레지스트리 키 값을 레지스트리로 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="6a387-120">레지스트리 하위 키: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="6a387-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="6a387-121">진입: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="6a387-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="6a387-122">형식: DWORD</span><span class="sxs-lookup"><span data-stu-id="6a387-122">Type: DWORD</span></span>

<span data-ttu-id="6a387-123">값: 1</span><span class="sxs-lookup"><span data-stu-id="6a387-123">Value: 1</span></span>

### <span data-ttu-id="6a387-124">MED-V 이미지 대신 그룹 정책을 통해 법적 고 지 사항 배포</span><span class="sxs-lookup"><span data-stu-id="6a387-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="6a387-125">최종 사용자가 MED-V에 액세스 하기 전에 SLA (서비스 수준 계약)를 표시 하도록 하려면 나중에 그룹 정책을 통해 SLA를 적용 하 여 처음 설치 완료 후 최종 사용자에 게 SLA가 표시 되도록 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="6a387-126">**주의**  사항 **무인** 모드에서 처음 설치를 실행 하는 것이 좋지만 이미지 (가상 하드 디스크)에 SLA를 포함 하도록 로컬 정책 또는 레지스트리 항목을 설정 하는 경우 첫 번째 설정이 **유인** 모드로 실행 되도록 하거나 처음 설치 하는 데 실패할 수 있는지도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="6a387-127">가상 하드 디스크 압축</span><span class="sxs-lookup"><span data-stu-id="6a387-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="6a387-128">가상 하드 디스크를 압축 하 여 빈 디스크 공간을 확보 하 고 가상 하드 디스크의 크기를 줄이는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="6a387-129">가상 하드 디스크를 압축 하는 방법에 대 한 자세한 내용은 [Med-v 가상 하드 디스크 압축](compacting-the-med-v-virtual-hard-disk.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a387-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="6a387-130">파란색 화면 손상으로 다시 시작 하도록 가상 컴퓨터 구성</span><span class="sxs-lookup"><span data-stu-id="6a387-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="6a387-131">파란색 화면 충돌이 발생할 경우 MED-V 작업 영역 가상 컴퓨터를 자동으로 다시 시작 하도록 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="6a387-132">게스트에서이 설정을 구성 하려면 HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl 키의 AutoReboot 값을 "1"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="6a387-133">**시작**을 클릭 하 고 **제어판**을 클릭 한 다음 **시스템**을 클릭 하 여이 설정을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="6a387-134">그런 다음 **고급** 탭의 **시작 및 복구** 영역에서 **설정을**클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="6a387-135">**자동으로 다시 시작** 확인란을 선택 하 고 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="6a387-136">밀봉 하기 전에 MED-V 이미지 백업</span><span class="sxs-lookup"><span data-stu-id="6a387-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="6a387-137">봉인 하기 전에 MED-V 이미지의 백업 복사본을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="6a387-138">MED-V 이미지를 봉인 하는 방법에 대 한 자세한 내용은 [med-v에 대 한 Windows 가상 PC 이미지 구성을](configuring-a-windows-virtual-pc-image-for-med-v.md)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a387-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="6a387-139">배치 파일에서 설치 하는 경우 마지막으로 Windows Virtual PC 설치</span><span class="sxs-lookup"><span data-stu-id="6a387-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="6a387-140">배치 파일을 사용 하 여 MED-V 구성 요소를 설치 하는 경우 MED-V 호스트 에이전트 및 MED-V 작업 영역 패키지 파일 뒤에 Windows 가상 PC 및 Windows 가상 PC 핫픽스가 설치 되도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="6a387-141">이렇게 하면 Windows Update는 다시 시작을 요구 하 여 설치 프로세스에 간섭이 발생 하지 않도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="6a387-142">로컬 폴더에서 MED-V 작업 영역 설치</span><span class="sxs-lookup"><span data-stu-id="6a387-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="6a387-143">네트워크 위치에서 MED-V를 설치할 때 발생할 수 있는 문제 때문에 MED-V 작업 영역 설정 파일을 로컬로 복사한 다음 setup.exe를 실행 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="6a387-144">한 가지 방법 으로만 프린터 리디렉션 관리</span><span class="sxs-lookup"><span data-stu-id="6a387-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="6a387-145">프린터가 MED-V 게스트 가상 컴퓨터에 수동으로 설치 되어 있고 나중에 호스트 컴퓨터에 동일한 프린터가 설치 되어 있으면 게스트에 두 번 설치 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="6a387-146">이 문제를 방지 하려면 리디렉션을 사용 하지 않도록 설정 하 고 게스트에 수동으로 프린터를 설치 하거나 리디렉션을 사용 하도록 설정 하거나 게스트에 수동으로 프린터를 설치 하지 않는 등 한 가지 방법 으로만 프린터 리디렉션을 관리 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="6a387-147">MED-V 게스트 패치 설정 구성</span><span class="sxs-lookup"><span data-stu-id="6a387-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="6a387-148">MED-V 가상 컴퓨터가 레지스트리에서 관련 구성 값을 정의 하 여 자동 업데이트를 수신 하는 시기와 기간을 제어할 수 있습니다. awakens</span><span class="sxs-lookup"><span data-stu-id="6a387-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="6a387-149">MED-V 모범 사례는 MED-V 가상 컴퓨터에 대 한 정기 업데이트를 예약한 시간과 일치 하도록 절전 모드 해제 간격을 설정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="6a387-150">또한 호스트 컴퓨터의 동작과 비슷하게 이러한 설정을 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="6a387-151">MED-V 게스트 패치 설정을 구성 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역에 대 한 자동 업데이트 관리](managing-automatic-updates-for-med-v-workspaces.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a387-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="6a387-152">바이러스 백신/백업 소프트웨어 구성</span><span class="sxs-lookup"><span data-stu-id="6a387-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="6a387-153">바이러스 백신 활동이 가상 데스크톱의 성능에 영향을 주지 않도록 하려면, MED-V 호스트 컴퓨터에서 실행 중인 바이러스 백신 또는 백업 프로세스에서 다음 가상 컴퓨터 파일 형식을 제외 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6a387-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="6a387-154">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="6a387-154">\*.VMC</span></span>

-   <span data-ttu-id="6a387-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="6a387-155">\*.VUD</span></span>

-   <span data-ttu-id="6a387-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="6a387-156">\*.VSV</span></span>

-   <span data-ttu-id="6a387-157">\*. .VHD</span><span class="sxs-lookup"><span data-stu-id="6a387-157">\*.VHD</span></span>

## <span data-ttu-id="6a387-158">관련 항목</span><span class="sxs-lookup"><span data-stu-id="6a387-158">Related topics</span></span>


[<span data-ttu-id="6a387-159">MED-V에 대한 보안 및 보호</span><span class="sxs-lookup"><span data-stu-id="6a387-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





