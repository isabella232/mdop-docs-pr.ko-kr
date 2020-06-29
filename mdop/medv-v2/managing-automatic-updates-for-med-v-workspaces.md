---
title: MED-V 작업 영역에 대한 자동 업데이트 관리
description: MED-V 작업 영역에 대한 자동 업데이트 관리
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825293"
---
# <span data-ttu-id="b5723-103">MED-V 작업 영역에 대한 자동 업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="b5723-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="b5723-104">MED-V 작업 영역은 자동 소프트웨어 업데이트 프로세스가 엔터프라이즈의 실제 컴퓨터와 같이 관리 되어야 하는 별도의 운영 체제를 포함 하는 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="b5723-105">호스트 운영 체제를 실행할 때 항상 게스트 운영 체제가 실행 되는 것은 아니지만, 필요한 경우 게스트 운영 체제에 소프트웨어 업데이트를 적용할 수 있도록 MED-V 가상 컴퓨터가 구성 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="b5723-106">Microsoft 엔터프라이즈 데스크톱 가상화 (MED-V) 2.0 솔루션은 MED-V 작업 영역에서 자동 소프트웨어 업데이트가 처리 되는 방식을 결정할 수 있는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="b5723-107">MED-V 작업 영역 절전 모드 해제 정책 관리</span><span class="sxs-lookup"><span data-stu-id="b5723-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="b5723-108">MED-V 작업 영역 깨우기 정책은 med-v 구성 설정에서 지정 하는 시간 동안 MED-V 가상 컴퓨터를 업데이트할 수 있도록 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="b5723-109">이는 바이러스 백신 응용 프로그램과 같은 Microsoft 이외의 솔루션에서 배포 하 고 제어 하는 Windows Update 및 업데이트를 Microsoft에서 게시 한 두 가지 업데이트에 모두 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="b5723-110">**중요**  MED-V 작업 영역 절전 모드 해제 정책은 Microsoft 업데이트 인프라에 최적화 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="b5723-111">Microsoft System Center Configuration Manager를 사용 하 여 타사 업데이트를 배포 하는 경우 Microsoft Update와 동일한 인프라를 활용 하는 System Center 업데이트 게시자를 사용 하는 것이 좋으며, 따라서 MED-V 작업 영역 웨이크업 정책의 혜택을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5723-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="b5723-112">자세한 내용은 [System Center 업데이트 Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="b5723-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="b5723-113">MED-V 작업 영역 패키지를 만들 때 최종 사용자가 로그온 할 때 (**빠른 시작**) 또는 최종 사용자가 게시 된 응용 프로그램 (**정상 시작**)을 처음으로 열 때 시작 되는 시간과 방법을 구성한 경우</span><span class="sxs-lookup"><span data-stu-id="b5723-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="b5723-114">또는 최종 사용자가이 설정을 제어할 수 있도록 하는 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="b5723-115">어느 경우 든 **빠른 시작** 옵션을 선택 하면 Med-v 호스트가 사용자로 로그온 한 경우에만 가상 컴퓨터가 계속 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="b5723-116">이 구성에서 호스트가 활성 상태일 때 MED-V가 활성화 되어 있으므로 MED-V에서 추가 처리를 요구 하지 않고 자동 업데이트가 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="b5723-117">그러나 **빠른 시작** 이 지정 되지 않았거나 가상 컴퓨터가 최대 절전 모드 또는 중단 되는 경우 med-v는 med-v가 정기적으로 사용 되지 않더라도 게스트 운영 체제가 정기적으로 업데이트 되는 med-v 작업 영역의 절전 모드 해제 정책을 통해 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="b5723-118">MED-V는 사용자가 지정 하는 구성 설정에 따라 가상 컴퓨터를 정기적으로 시작 하 여이 함수를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="b5723-119">이렇게 하면 가상 컴퓨터의 자동 업데이트 클라이언트가 해당 구성에 따라 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="b5723-120">MED-V 구성 설정에 의해 정의 된 기간이 경과한 후에는 MED-V가 가상 컴퓨터를 이전 상태로 되돌립니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="b5723-121">**참고**  최종 사용자가 업데이트 기간 동안 게시 된 응용 프로그램을 열면 필요한 업데이트가 적용 되지만 MED-V는 업데이트 기간이 종료 된 후 자동으로 hibernated 또는 종료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="b5723-122">대신 MED-V가 계속 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="b5723-123">MED-V 작업 영역 절전 모드 해제 정책에는 다음과 같은 세 가지 기본 구성 요소가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="b5723-124">게스트 업데이트 관리자</span><span class="sxs-lookup"><span data-stu-id="b5723-124">Guest Update Manager</span></span>**

<span data-ttu-id="b5723-125">MED-V 호스트에 거주 하는이 독립 실행형 실행 프로그램은 미리 정의 된 구성 가능한 일정에 따라 가상 컴퓨터의 절전 모드를 해제 하는 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="b5723-126">업데이트 관리자가 매일 가상 컴퓨터를 종료 해야 하는 시간을 나타내는 구성 설정을 지정 하 고, 업데이트를 적용할 수 있도록 가상 컴퓨터를 활성 상태로 유지 해야 하는 기간 (분)을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="b5723-127">지정 된 시간 (분)에 도달 하면 게스트 업데이트 관리자가 다음에 사용할 수 있도록 준비 되어 가상 컴퓨터를 최대 절전 모드로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="b5723-128">Windows 작업 관리자를 통해이 실행 프로그램의 실행을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="b5723-129">게스트 다시 시작 관리 서비스</span><span class="sxs-lookup"><span data-stu-id="b5723-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="b5723-130">MED-V 호스트에 거주 하는이 서비스에는 세 가지 주요 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="b5723-131">게스트 업데이트 관리자와 함께 필요한 경우 사용자 로그온 시 가상 컴퓨터의 재시작을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="b5723-132">업데이트 설치로 인해 가상 컴퓨터 다시 시작이 필요한 경우를 감지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="b5723-133">그러면 구성에 따라 게스트 업데이트 관리자의 작업이 항상 예약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="b5723-134">게스트 업데이트 서비스</span><span class="sxs-lookup"><span data-stu-id="b5723-134">Guest Update Service</span></span>**

<span data-ttu-id="b5723-135">이 Windows 서비스는 MED-V 가상 컴퓨터에 설치 된 업데이트를 다시 시작 해야 하는 경우 모니터링을 담당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="b5723-136">서비스에서 다시 시작에 대 한 요구 사항이 발견 되 면 호스트에서 게스트 다시 시작 관리 서비스에 알립니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="b5723-137">MED-V 작업 영역 깨우기 정책에 대 한 구성 설정</span><span class="sxs-lookup"><span data-stu-id="b5723-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="b5723-138">레지스트리에 다음 두 가지 구성 값을 정의 하 여 가상 컴퓨터가 자동 업데이트를 수신 하는 시기 및 기간을 제어 합니다. awakens</span><span class="sxs-lookup"><span data-stu-id="b5723-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="b5723-139">이러한 값은 모두 HKLM\\Software\\Microsoft\\MEDV\\v2\\VM 키 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="b5723-140">**GuestUpdateTime** – 24 시간 시계 표준에 따라, med-v가 가상 컴퓨터를 업데이트 하기 위해 절전 모드를 해제 해야 하는 시간 및 분을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="b5723-141">HH: MM 형식으로 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="b5723-142">기본값은 00:00 (자정)입니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="b5723-143">**GuestUpdateDuration** – med-v가 업데이트를 위해 가상 컴퓨터를 활성 상태로 유지 해야 하는 시간 (분)을 구성 합니다. GuestUpdateTime 구성 설정에 지정 된 시점부터 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="b5723-144">기본값은 240 (4 시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="b5723-145">이 값을 0으로 설정 하면 MED-V 작업 영역 웨이크업 정책을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="b5723-146">MED-V 구성 값을 정의 하는 방법에 대 한 자세한 내용은 [Med-v 작업 영역 구성 설정 관리](managing-med-v-workspace-configuration-settings.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5723-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="b5723-147">**참고**  MED-V 모범 사례는 MED-V 가상 컴퓨터가 정기적으로 업데이트 되도록 계획 되는 시간과 일치 하도록 절전 모드 종료 간격을 설정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="b5723-148">또한 호스트 컴퓨터의 동작과 비슷하게 이러한 설정을 구성 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="b5723-149">ESD 시스템을 사용한 재부팅 알림</span><span class="sxs-lookup"><span data-stu-id="b5723-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="b5723-150">자동 업데이트를 적용 한 후에 MED-V 작업 영역에 다시 시작이 필요할 때마다 사용자가 MED-V에 알리려면 ESD 시스템을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="b5723-151">ESD 시스템을 통해 다시 시작 해야 하는 자동 업데이트를 적용 하는 경우에는 MED-V 작업 영역에서 다음과 같은 전역 이벤트에 신호를 보내는 스크립트를 작성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="b5723-152">**중요**  수정 전용 권한을 사용 하 여 이벤트를 열고 신호를 보내는 것이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="b5723-153">올바른 사용 권한으로 열지 않은 경우에는 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="b5723-154">이 이벤트를 신호 하면 MED-V가 캡처를 캡처하여 가상 컴퓨터에 다시 시작이 필요 하다는 것을 알립니다.</span><span class="sxs-lookup"><span data-stu-id="b5723-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="b5723-155">관련 항목</span><span class="sxs-lookup"><span data-stu-id="b5723-155">Related topics</span></span>


[<span data-ttu-id="b5723-156">MED-V 작업 영역에 대한 소프트웨어 업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="b5723-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





