---
title: DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법
description: DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법
author: dansimp
ms.assetid: c0062208-39cd-4e01-adf8-36a11386e2ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 42d49c6c5c494da866785764e1c93a6bda2d667e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822593"
---
# <span data-ttu-id="4de39-103">DaRT 복구 이미지를 사용하여 원격 컴퓨터를 복구하는 방법</span><span class="sxs-lookup"><span data-stu-id="4de39-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="4de39-104">Microsoft 진단 및 복구 도구 집합 (DaRT) 10의 원격 연결 기능을 사용 하 여 최종 사용자 컴퓨터에서 원격으로 DaRT 도구를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 10 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="4de39-105">최종 사용자가 특정 정보를 사용 하 여 관리자나 헬프 데스크 직원을 제공 하면 IT 관리자나 지원 센터에서 최종 사용자의 컴퓨터를 제어 하 고 필요한 DaRT 도구를 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="4de39-106">복구 이미지를 만들 때 DaRT 도구를 사용 하지 않도록 설정한 경우에도 모든 도구에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="4de39-107">원격 연결을 제외한 모든 도구는 최종 사용자가 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="4de39-108">DaRT 복구 이미지를 사용 하 여 원격 컴퓨터를 복구 하려면</span><span class="sxs-lookup"><span data-stu-id="4de39-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="4de39-109">DaRT 복구 이미지를 사용 하 여 최종 사용자 컴퓨터를 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="4de39-110">일반적으로 dart 복구 이미지를 배포 하는 방법에 따라 다음 방법 중 하나를 사용 하 여 DaRT로 부팅 하 고 원격 컴퓨터를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="4de39-111">DaRT 복구 이미지 배포에 대 한 자세한 내용은 [dart 10 배포](deploying-dart-10.md)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4de39-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 10](deploying-dart-10.md).</span></span>

    -   <span data-ttu-id="4de39-112">문제가 있는 컴퓨터의 복구 파티션에서 DaRT로 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="4de39-113">네트워크의 원격 파티션에서 DaRT로 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="4de39-114">각 방법의 장점과 단점에 대 한 자세한 내용은 [DaRT 10 복구 이미지를 저장 하 고 배포 하는 방법 계획](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4de39-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

    <span data-ttu-id="4de39-115">DaRT로 부팅 하는 데 사용 하는 방법에 관계 없이 부팅 옵션에 대 한 부팅 장치를 사용 하도록 설정 하 고 최종 사용자가 사용할 수 있도록 할 옵션을 선택 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="4de39-116">참고</span><span class="sxs-lookup"><span data-stu-id="4de39-116">Note</span></span>**  
    <span data-ttu-id="4de39-117">BIOS 구성은 조직에 사용 되는 하드 디스크 드라이브, 네트워크 어댑터 및 기타 하드웨어의 종류에 따라 고유 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="4de39-118">네트워크 서비스를 초기화할 것인지 묻는 메시지가 표시 되 면 다음 중 하나를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="4de39-119">**Yes** -DHCP 서버가 네트워크에 있고 서버에서 IP 주소를 가져오려고 시도 하는 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="4de39-120">네트워크에서 DHCP 대신 고정 IP 주소를 사용 하는 경우, 나중에 DaRT의 **Tcp/ip 구성** 도구를 사용 하 여 고정 ip 주소를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="4de39-121">**No** -네트워크 초기화 프로세스를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="4de39-122">드라이브 문자를 다시 매핑할 것인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="4de39-123">Windows online을 실행 하는 경우 시스템 볼륨은 일반적으로 C 드라이브에 매핑됩니다. 그러나 Windows를 오프 라인으로 WinRE에서 실행 하면 원래 시스템 볼륨이 다른 드라이브에 매핑될 수 있으며이로 인해 혼란이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="4de39-124">다시 매핑하려는 경우 DaRT는 온라인 드라이브 문자와 일치 하도록 오프 라인 드라이브 문자를 매핑하려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="4de39-125">나중에 시작 프로세스에서 오프 라인 운영 체제를 선택한 경우에만 다시 매핑 처리가 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="4de39-126">**시스템 복구 옵션** 대화 상자에서 키보드 레이아웃을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="4de39-127">표시 된 시스템 루트 디렉터리, 설치 된 운영 체제 종류, 파티션 크기를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="4de39-128">운영 체제가 나열 되지 않고 드라이버 부족으로 문제가 발생할 수 있다고 의심 되는 경우 **드라이버 로드** 를 클릭 하 여 의심 되는 드라이버를 로드 한 다음 장치에 대 한 설치 미디어를 삽입 하 고 드라이버를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="4de39-129">복구 하거나 진단 하려는 설치를 선택 하 고 **다음**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="4de39-130">참고</span><span class="sxs-lookup"><span data-stu-id="4de39-130">Note</span></span>**  
   <span data-ttu-id="4de39-131">Windows 10 복구 환경 (WinRE)에서 마지막으로 시도 했을 때 Windows 10이 올바르게 시작 되지 않았다는 것을 감지 하거나 의심 되는 경우 **시동 복구가** 자동으로 실행 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="4de39-132">이 문제를 해결 하는 방법에 대 한 자세한 내용은 [DaRT 10 문제 해결](troubleshooting-dart-10.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4de39-132">For information about how to resolve this issue, see [Troubleshooting DaRT 10](troubleshooting-dart-10.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="4de39-133">**시스템 복구 옵션** 창에서 **Microsoft 진단 및 복구 도구 집합** 을 클릭 하 여 **진단 및 복구 도구 집합**을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="4de39-134">**진단 및 복구 도구 집합** 창에서 **원격 연결** 을 클릭 하 여 **DaRT 원격 연결** 창을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="4de39-135">지원 센터 원격 액세스를 제공 하 라는 메시지가 표시 되 면 **확인**을 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="4de39-136">DaRT 원격 연결 창이 열리고 티켓 번호, IP 주소 및 포트 정보가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="4de39-137">지원 센터 컴퓨터에서 **DaRT 원격 연결 뷰어**를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="4de39-138">**시작**을 클릭 하 고 **모든 프로그램**을 클릭 한 다음 **Microsoft dart 10**을 클릭 한 다음 **DaRT 원격 연결 뷰어**를 클릭 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 10**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="4de39-139">**DaRT 원격 연결** 창에서 필요한 티켓, IP 주소 및 포트 정보를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="4de39-140">참고</span><span class="sxs-lookup"><span data-stu-id="4de39-140">Note</span></span>**  
   <span data-ttu-id="4de39-141">이 정보는 최종 사용자 컴퓨터에서 생성 되며 최종 사용자가 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="4de39-142">최종 사용자 컴퓨터에서 사용할 수 있는 여러 개의 IP 주소를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="4de39-143">**연결**을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-143">Click **Connect**.</span></span>

<span data-ttu-id="4de39-144">IT 관리자는 이제 최종 사용자 컴퓨터의 제어권을가지고 있으며 DaRT 도구를 원격으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="4de39-145">참고</span><span class="sxs-lookup"><span data-stu-id="4de39-145">Note</span></span>**  
<span data-ttu-id="4de39-146">inv32.xml 라는 이름의 파일이 제공 되며, 포트 번호 및 IP 주소와 같은 원격 연결 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="4de39-147">기본적으로 파일 은%windir%\\system32.에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="4de39-148">원격 연결 프로세스를 사용자 지정 하려면</span><span class="sxs-lookup"><span data-stu-id="4de39-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="4de39-149">winpeshl.ini 파일을 편집 하 여 원격 연결 프로세스를 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="4de39-150">winpeshl.ini 파일을 편집 하는 방법에 대 한 자세한 내용은 [Winpeshl.ini 파일](https://go.microsoft.com/fwlink/?LinkId=219413)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4de39-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="4de39-151">다음 명령과 매개 변수를 지정 하 여 최종 사용자 컴퓨터에서 원격 연결을 설정 하는 방법을 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="4de39-152">명령</span><span class="sxs-lookup"><span data-stu-id="4de39-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="4de39-153">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4de39-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="4de39-154">설명</span><span class="sxs-lookup"><span data-stu-id="4de39-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="4de39-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="4de39-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="4de39-156">-nomessage</span><span class="sxs-lookup"><span data-stu-id="4de39-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4de39-157">확인 메시지가 표시 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="4de39-158">원격 연결은 </strong> 최종 사용자가 &quot; 확인 메시지에 Yes로 응답 한 것 처럼 계속 됩니다 &quot; .</span><span class="sxs-lookup"><span data-stu-id="4de39-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="4de39-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="4de39-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="4de39-160">none</span><span class="sxs-lookup"><span data-stu-id="4de39-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4de39-161"><strong>원격 연결이 실행 되 고 </strong> 있지 않거나 최종 사용자 컴퓨터에 유효한 연결이 설정 될 때까지 사용자 지정 스크립트가 계속 진행 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="4de39-162">중요</span><span class="sxs-lookup"><span data-stu-id="4de39-162">Important</span></span></strong><br/><p><span data-ttu-id="4de39-163">이 명령은 독립적으로 지정 된 경우 기능을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="4de39-164">올바르게 작동 하려면 스크립트에서 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="4de39-165">다음은 DaRT로 부팅 하려고 하는 즉시 **원격 연결** 도구를 열기 위해 사용자 지정 된 winpeshl.ini 파일의 예입니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="4de39-166">DaRT가 시작 되 면 RAM 디스크에 \\Windows\\System32\\에서 파일 inv32.xml 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="4de39-167">이 파일에는 연결 정보 (IP 주소, 포트, 티켓 번호)가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="4de39-168">이 파일을 네트워크 공유에 복사 하 여 지원 센터 워크플로를 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="4de39-169">예를 들어 사용자 지정 프로그램은 연결 파일에 대 한 네트워크 공유를 확인 한 다음 지원 티켓을 만들거나 전자 메일 알림을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="4de39-170">명령 프롬프트에서 원격 연결 뷰어를 실행 하려면</span><span class="sxs-lookup"><span data-stu-id="4de39-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="4de39-171">명령 프롬프트에서 **DaRT 원격 연결 뷰어** 를 실행 하려면 **DartRemoteViewer.exe** 명령을 지정 하 고 다음 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4de39-172">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4de39-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="4de39-173">설명</span><span class="sxs-lookup"><span data-stu-id="4de39-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4de39-174">-ticket = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="4de39-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4de39-175">여기서 &lt; <em> ticketnumber </em> &gt; 는 대시를 포함 하 여 원격 연결에 의해 생성 되는 티켓 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4de39-176">-ipaddress = &lt; <em> ipaddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="4de39-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4de39-177">여기서 &lt; <em> Ipaddress </em> &gt; 는 원격 연결에 의해 생성 되는 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4de39-178">-port = &lt; <em> port</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="4de39-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4de39-179">여기서 &lt; <em> 포트는 </em> &gt; 지정 된 IP 주소에 해당 하는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="4de39-180">세 개의 매개 변수가 모두 지정 되 고 데이터가 유효 하면 프로그램을 시작할 때 즉시 연결을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="4de39-181">매개 변수가 유효 하지 않은 경우에는 지정 된 매개 변수가 없는 것 처럼 프로그램이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4de39-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="4de39-182">관련 항목</span><span class="sxs-lookup"><span data-stu-id="4de39-182">Related topics</span></span>


[<span data-ttu-id="4de39-183">DaRT 10 작업</span><span class="sxs-lookup"><span data-stu-id="4de39-183">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="4de39-184">DaRT 10을 사용하여 컴퓨터 복구</span><span class="sxs-lookup"><span data-stu-id="4de39-184">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)









